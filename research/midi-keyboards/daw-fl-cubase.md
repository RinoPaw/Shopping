# Windows / FL Studio / Cubase DAW 集成核查

日期：2026-10-24。范围：目前候选 MIDI 控制器的**官方功能与配置路径**。尚未在用户电脑上连接实体设备进行实测。**此文件不查价格。**

## 结论摘要

- **MiniLab 37、Launchkey 37 MK4、Launchkey Mini 37 MK4** 均有明确的 FL Studio 与 Cubase 官方集成支持。此前将 MiniLab 37 当作只能做通用 MIDI 的看法已经过时。
- **FLkey 2 37** 是深度 FL Studio 专用方向；同厂 Launchkey MK4 在跨 DAW 上更灵活。即使 FLkey 2 可以用 HUI 适配其他宿主，也不等价于在 Cubase 中有专用完整脚本。
- **KeyStep 37 mk2** 偏向 MIDI/CV 音符、Arp、外部音序，DAW 的轨道/插件深度控制需要另行映射；不要与 MiniLab 的专用 DAW 脚本混为一谈。
- 所有“集成支持”只代表厂商文档。Windows 中真实识别、功能按键、插件参数映射及断开重连仍需按 [test-protocol.md](test-protocol.md) 验证。

## 精确型号对照

| 型号 | FL Studio | Cubase | 关键限制 |
|---|---|---|---|
| Arturia MiniLab 37 | Arturia 提供 **Script 1.4** 和指南；新版 FL Studio 可包含脚本 | Arturia 提供 **MIDI Remote Script 1.4** 与指南，可导入 | 与 Analog Lab 的 Arturia 模式是另一种控制情境；注意 MIDI/DAW 双端口选择 |
| Novation Launchkey 37 MK4 | 有专用控制集成；8 编码器可控制 Channel Rack、Mixer、EQ 等 | 有专用控制集成；编码器支持 Cubase Quick Controls 和 EQ 等 | 37 键无实体推子；部分第三方插件需要自定义 CC 映射 |
| Novation Launchkey Mini 37 MK4 | 与 MK4 系列的跨 DAW 集成理念一致，官方明确列入 FL Studio | 官方列入 Cubase 集成 | 迷你键床、触控 pitch/mod 条；DAW 功能丰富，但不能弥补手感限制 |
| Novation FLkey **2** 37 | 专用 FL Studio Script，Channel Rack、Pattern、Mixer Inserts 支持更充分 | HUI 兼容为主 | 使用 Cubase 时不能套用 FL Studio 专用按钮功能假设 |
| Arturia KeyStep 37 mk2 | 作为 MIDI 音符控制器使用，可自行 MIDI Learn | 作为 MIDI 音符控制器使用，可自行 MIDI Remote 映射 | 缺少 MiniLab 风格的多推子和常用 DAW 控制模块，适合更强调音序器/外部硬件的人 |
| AKAI MPK Mini Plus II | 2026 年新款宣称增加 DAW Maps，需确认 FL Studio 的准确功能 | 需要具体新款脚本/映射文档 | 不可借用旧 MPK Plus 评价，不应假设有与 Launchkey 同等深度的 Cubase 控制 |
| M-VAVE SMK-37 Pro | USB/BLE MIDI 预期可完成基本输入；特定 DAW 预置方案需进一步验证 | 同左 | V016 修复过 MIDI 音符发送延迟；待做 Windows 真实按键/连奏复现 |

## Arturia MiniLab 37：官方设置要点

官方 [DAW Integration FAQ](https://support.arturia.com/hc/en-us/articles/27901264120348-MiniLab-37-DAW-Integration) 说明：

### FL Studio
1. 使用包含 MiniLab 37 脚本的新版 FL Studio，或从 Arturia 的 [官方资源页](https://www.arturia.com/support/downloads-manuals/product/minilab-37) 下载脚本 1.4。
2. MiniLab 37 切换到 DAW 模式（Shift + Prog pad）。
3. 如未自动识别：FL Studio 的 MIDI settings 中更新脚本并选择 Arturia MiniLab 37，按照官方图示设置 MIDI/DAW ports。
4. 厂商说明的 DAW 输入/输出端口编号为 236；独立 Analog Lab VST 的输入端口另有要求，勿机械将全部输入都设成同一端口。
5. Windows 不同用户的 FL Studio 版本和安装路径可能不同，按实际设置核对。

### Cubase
1. 下载 Arturia 的 Cubase Script 1.4 与指南。
2. MiniLab 37 进入 DAW 模式；在 Cubase MIDI Remote Manager 中导入 `Arturia_MiniLab 37.midiremote`。
3. 官方特别提醒在 Cubase Studio Setup > MIDI Port Setup 中避免重复将 DAW 控制口纳入 'All MIDI Inputs'，否则走带按键可能被误当音符。
4. 这已经是有官方脚本的实际集成，不能写成“Cubase 只支持通用 MIDI”。

官方来源：[资源及 1.4 脚本](https://www.arturia.com/support/downloads-manuals/product/minilab-37)；[完整 FAQ](https://support.arturia.com/hc/en-us/articles/27901264120348-MiniLab-37-DAW-Integration)；[Cubase PDF 指南](https://dl.arturia.net/products/minilab-37/daw-integration-guide/MiniLab_37_Cubase_Daw_Integration_Guide_1_0_EN.pdf)。

## Novation Launchkey 37 MK4：官方控制范围

[官方 DAW user guide（2026-07 更新）](https://userguides.novationmusic.com/hc/en-gb/articles/27612230389138-DAW-control-with-the-Launchkey-37)：

- FL Studio：厂商插件预置映射，编码器可以切换至 Channel Rack Volume/Pan、Mixer Volume/Pan、EQ 页面；第三方 VST 可能需要 Custom Mode。
- Cubase：Plugin 模式映射 8 个 Quick Controls；Mixer EQ 模式控制四段 EQ 的频率和增益，屏幕反馈参数名。
- 包含走带、轨道切换、参数翻页、打击垫等操作；功能因 DAW 而异。
- [Windows Cubase Script 1.1 下载](https://downloads.novationmusic.com/novation/launchkey-mk4/launchkey-mk4-37) 可核验，升级前要确认固件版本。

## Novation FLkey 2 与 Launchkey MK4 官方代际/功能对照

[Novation 原厂对照表（2026-07）](https://support.novationmusic.com/hc/en-gb/articles/35765627682834-What-are-the-differences-between-Launchkey-Mk4-and-FLkey-2)。

- 两者的 37 键型号均采用同级合成器动作全尺寸键床、16 pads、8 encoders、USB-C，且**都没有实体推子**。
- FLkey 2 提供 **FL Studio Pattern pad mode、Mixer Inserts 编码器、针对 Channel Rack 和相关工作流的专用控制**。
- Launchkey MK4 有面向多个 DAW 的原生脚本；如果以后使用 Cubase、Ableton 或多个 DAW，潜在切换成本更低。
- 官方建议主要使用 FL Studio 选 FLkey 2，使用多个 DAW 选 Launchkey MK4；这是厂商立场，需实测映射质量。
- [FLkey 2 37 官方尺寸](https://userguides.novationmusic.com/hc/en-gb/articles/35710499749010-FLkey-2-37-Weight-and-Dimensions)：557 × 251 × 79 mm，与 Launchkey 37 的标称尺寸相同。

## 注意：Novation 的 37 键 Split/Layer 官方资料互相矛盾

- [Launchkey 37 2026 版入门介绍（user guide v4.0）](https://userguides.novationmusic.com/hc/en-gb/articles/27612216764306-Introduction-to-the-Launchkey-37) **写有** Split/Layer。
- [Launchkey Mini 37 的同代入门介绍](https://userguides.novationmusic.com/hc/en-gb/articles/27441246154642-Introduction-to-the-Launchkey-Mini-37) **同样写有** Split/Layer。
- 但 [Novation 原始产品发布介绍](https://novationmusic.com/articles/introducing-the-new-launchkey-the-creative-controller/) **明确限定 49/61 键型号有 Split/Layer**，MusicRadar 2024 实测也写过较小型号缺失。官方技术参考的部分功能还注明“only on SKUs having keyboard split”。
- 因为2026版本的手册可能是统一模板或随固件功能改动，**目前必须标为官方资料冲突，不能据此向用户保证 37 键已支持键盘分区**。需要从固件发行记录、当前型号菜单或厂商客服得到具体确认。Chord Map 里的 'Split: Bass + Chord' 是**和弦垫演奏技巧**，概念不同于物理琴键分区。

## 未解决的实际问题

1. Windows + **FL Studio**：MiniLab 37 的 4 推子究竟可以原生映射多少个 Mixer / 插件参数？Launchkey 37 的 8 个 encoders 用翻页控制是否更有效？
2. Windows + **Cubase**：把不同工程存为模板后，两个品牌的控制脚本是否会自动识别多轨与多个 VST？
3. 登录和软件赠品：必须查当前厂商注册与二手软件许可证转移规则；不能根据卖家“送软件”自行假设可转移。
4. 实际演奏：在同一个音源测键床与 velocity；至少要有本人短时间试弹或两个不同使用者实拍。

