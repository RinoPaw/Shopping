# MiniLab 37 / FL Studio：Arturia 官方脚本静态审计

审计日期：2026-10-24。目的：判断 MIDI 控制器的硬件旋钮、推子与 DAW 操作实际能完成什么，降低凭宣传功能选购的风险。**这是官方发布脚本的静态代码阅读；没有安装、执行脚本，亦没有实体 MIDI 设备参与测试。**

## 可追溯来源

- Arturia [MiniLab 37 DAW Integration FAQ](https://support.arturia.com/hc/en-us/articles/27901264120348-MiniLab-37-DAW-Integration)
- Arturia [MiniLab 37 官方脚本下载页](https://www.arturia.com/support/downloads-manuals/product/minilab-37)，FL Studio Script **1.4**（官网列出 2026-06-08）。
- 下载原始文件：[MiniLab_37_FL_Studio_Daw_Integration_Script_1_4.zip](https://dl.arturia.net/products/minilab-37/daw-integration-script/MiniLab_37_FL_Studio_Daw_Integration_Script_1_4.zip)
- 2026-10-24 下载包 SHA-256：`767669910cac51ab85767cdcc36a481db8250f5f98c24e5d9834f8fff67438ad`
- 在用户已授权 Windows 设备的临时目录中只展开、读取官方 ZIP 的 11 个 Python 文件；**未运行其中任何 Python 代码、未复制到 FL Studio、未修改本机 MIDI 设置**。未将官方脚本源码加入本仓库。

## 从源代码直接看到的功能

| 代码位置 | 静态结论 | 是否可保证实际可用 |
|---|---|---|
| `MiniLab37Process.py`，`Record/Start/Stop/Loop/SetClick/TapTempo` | 直接调用 FL Studio `transport` 模块，处理走带、录音、循环、节拍器和 Tap Tempo | **实现明确**，但需要相应版本 FL Studio/脚本实际加载才能验证 |
| `MiniLab37Process.py`，`Navigator/ToggleBrowserChannelRack` | 调用 FL Studio `ui` API 在浏览器/Channel Rack 之间切换、上下浏览、预听等 | 实现明确；不同 DAW 焦点/窗口状态时的行为要测试 |
| `MiniLab37Process.py`，`SetVolumeTrack/SetPanTrack` | 在未聚焦插件窗口时，把部分硬件控件绑定到**当前选中 Mixer Track 的音量、声像**；聚焦插件时转入插件控制逻辑 | **不会自动等同四个推子同时控制四个不同的 Mixer 通道** |
| `MiniLab37Plugin.py`，`PARAM_ID` | 代码定义 8 个旋钮和 4 个推子的插件参数编号；对多种 FL Studio 内置插件设置明确的 `PARAM_MAP` | **目标内置插件依映射表可控**；不能凭这份代码保证任意 VST 自动控制 |
| `MiniLab37Plugin.py`，`recognized_plugin` 分支 | 对 `FLEX`、`FPC`、`FL Keys`、`Sytrus`、`GMS`、`Harmor` 等多款原生插件做专用映射，调用 `plugins.setParamValue` | 需要对应插件的参数排列与当前脚本一致 |
| `MiniLab37Plugin.py`，未识别插件分支 | 默认仅返回普通“Knob N / Fader N”显示和原始控制值，**没有在这个分支自动调用插件参数设置函数** | 第三方 VST 应按 Arturia FAQ 通过 FL Studio MultiLink / MIDI Learn 手动映射 |
| `MiniLab37Process.py`，`OnDrumEvent` 和 `FPC_MAP` | 对鼓垫 Note On/Off 进行 FL Studio FPC 常用音符映射，并将事件交由 FL Studio 继续处理 | 实现明确；实际 Pads / 插件音符布局需要设备确认 |
| `MiniLab37Navigation.py` / `MiniLab37Display.py` | 向小屏幕写入当前参数、轨道、节拍器、播放状态等反馈 | 脚本实现明确；显示及时性与兼容性尚未实测 |

### 潜在代码质量问题（仅静态观察）

`MiniLab37Plugin.py` 的 `NATIVE_PLUGIN_LIST` 中，`BassDrum`、`Fruit kick`、`MiniSynth`、`PoiZone` 对应的连续字符串**缺少列表分隔逗号**。Python 可以合法地将相邻字符串字面量拼接成一个字符串，导致这些单独的名称不能逐项匹配该列表。`MiniLab37Return.py` 的 `PluginParamReturn` 使用这一列表判断是否读取参数以刷新反馈。

因此存在**某些内置插件反馈/参数刷新路径可能遗漏**的静态风险。该风险没有通过官方 FL Studio 运行测试确认，不能认定最终用户一定遇到此 Bug，亦不能据此直接降低产品整体可靠性评分。

## 与 Novation Launchkey 37 MK4 的同用途对照（分开标证据等级）

Novation [官方 Launchkey 37 DAW 控制指南](https://userguides.novationmusic.com/hc/en-gb/articles/27612230389138-DAW-control-with-the-Launchkey-37) 的文档明确列出：

- **FL Studio**：8 个无限编码器可切换 5 页：Channel Rack Volume / Pan、Mixer Volume / Pan、Mixer EQ；原生 FL Studio 插件有固定参数预设，第三方插件可能需要 Custom Encoder Mode 自定义。
- **Cubase**：8 个编码器可以操作 8 个 Quick Controls；Mixer 编码器还有 EQ 页面；Pads 可以切换 Select/Arm 与 Mute/Solo。
- Launchkey 37 硬件**没有实体推子**，更多混音控制通过无限编码器和页面完成。
- Novation [FL Studio 设置指南](https://support.novationmusic.com/hc/en-gb/articles/20499018257554-Launchkey-MK4-FL-Studio-Setup) 适用 **FL Studio 24 或更新版本**，预期自动识别，失败时有手动端口配置步骤。
- Novation [Cubase 设置指南](https://support.novationmusic.com/hc/en-gb/articles/20225881390482-Using-Launchkey-MK4-in-Cubase) 指出 Cubase **14.0.20 或更新版本**可自动识别而无需另装脚本；较旧版本按 Novation 提供的安装器执行。

这是一份**源代码静态检查 vs 原厂手册**的非对称证据比较。没有安装 Launchkey 实机，也没有找到/审阅 Novation 在 FL Studio 中运行的集成脚本源码，不能把文档中的预期功能当成双方运行的客观效率比较。

## 本次可供选型的实际结论

1. MiniLab 37 的 4 推子和 8 旋钮有完整的 FL Studio 接入路径，且存在大量原生插件专用映射，功能比“纯 USB Note 输入”丰富。
2. **不要许诺它的四个推子天然等于四轨混音台。** 官方脚本会根据焦点窗口和目标插件改变行为，若需要四轨同时音量控制，还应在实机检查脚本、用户预设或手动映射。
3. **第三方插件映射是两家共同的核查重点。** MiniLab 静态源码里的未知插件分支没有自动映射，Launchkey 官方文档也提示第三方插件可能需要 Custom Mode。
4. 对 Windows 使用者，Launchkey 在 Cubase 14.0.20+ 的开箱识别更简便；MiniLab 有可导入的 Cubase MIDI Remote 脚本。实际运行仍以最终宿主版本为准。
5. 不需要购买设备就能完成下一阶段：先进一步核对 Novation/Arturia 的 MIDI Remote 具体映射及设备深度（占位），将可验证的操作写成测试表。仍**未进入报价阶段**。
