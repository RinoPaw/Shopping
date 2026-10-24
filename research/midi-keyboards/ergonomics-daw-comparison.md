# 37 键 MIDI 控制器：实际桌面空间与双 DAW 工作流对照

2026-10-24；来源优先级：厂商规格/官方 DAW 文档，其次[官方 FL Studio 脚本静态审计](fl-studio-minilab37-script-audit.md)，其次独立用户体验。当前没有连接真实硬件进行共同环境 A/B 演奏。

## 硬限制与桌面形态

用户约束：机身宽度 **≤595 mm**，键数 **≤37**；主要制作音乐并录入旋律与和弦，Windows 上会选择 FL Studio 或 Cubase。

| 精确型号 | 键盘类型 | 宽 × 深 × 高（mm） | 宽度剩余 | 机身底面矩形投影面积 | 控制特色 |
|---|---|---|---:|---:|---|
| **MiniLab 37** | 37 slim keys | **503 × 183 × 54** | 92 mm | 920.5 cm² | 4 实体推子、8 无限旋钮、8 pads，pitch/mod 触控 |
| **Launchkey 37 MK4** | 37 full-size synth-action | **557 × 251 × 79** | 38 mm | 1398.1 cm² | 8 无限旋钮、16 pads、实体 pitch/mod 轮、额外工作流按键，**无推子** |
| **KeyStep 37 mk2** | 37 slim keys + 键床 aftertouch | **547 × 148 × 58**（原厂详情页） | 48 mm | 809.6 cm² | 4 编码器、独立音序器、MIDI/CV，**无 pads/推子** |
| **Launchkey Mini 37 MK4** | 37 mini synth-action | **477.8 × 176.8 × 49** | 117.2 mm | 844.8 cm² | 8 编码器、16 pads、pitch/mod 触摸条，**无推子** |
| **FLkey 2 37** | 37 full-size synth-action | **557 × 251 × 79** | 38 mm | 1398.1 cm² | 面向 FL Studio 的 Channel Rack/Pattern/Mixer 控制，**无推子** |

该投影面积是宽×深的简单几何计算；**不含插线口、踏板、鼠标活动范围、支架、手掌空间，亦非重量或人体工程学评分**。Launchkey 37 的几何桌面占用约为 MiniLab 37 的 **1.52 倍**，机身深度多 **68 mm**。KeyStep 37 mk2 深度仅 148 mm，特别适合放在显示器/电脑键盘前后留有空间的桌面；但接线净空仍需核。

**非常重要：** 机身宽度合格不代表摆放一定合适。需在桌面标出各机型深度以及 USB、音频和踏板的走线距离。KeyStep 37 mk2 另一官方商店页的宽度曾写 550 mm，见 [候选全集](candidates.md) 的冲突说明。尺寸将以具体在售版本官方手册/实物为最终准则。

### 原始尺寸和配置来源
- [Arturia MiniLab 37 官方页](https://www.arturia.com/products/hybrid-synths/minilab-37/overview)
- [Novation Launchkey 37 官方规格](https://novationmusic.com/products/launchkey-37)
- [Arturia KeyStep 37 mk2 官方规格](https://www.arturia.com/products/hybrid-synths/keystep-mk2/keystep-37-mk2)
- [Novation Launchkey Mini 37 官方规格](https://us.novationmusic.com/products/launchkey-mini-37)
- [Novation FLkey 2 37 官方尺寸](https://userguides.novationmusic.com/hc/en-gb/articles/35710499749010-FLkey-2-37-Weight-and-Dimensions)

## FL Studio：预期可完成的真实工作流

| 任务 | MiniLab 37（官网 FAQ + Python 源码） | Launchkey 37 MK4（官方指南） | FLkey 2 37（官方功能对照） |
|---|---|---|---|
| 播放/停止/录制、节拍器 | 有明确 transport 事件处理 | 有实体工作流按钮和 DAW 集成 | FL 专用集成 |
| 浏览器与 Channel Rack 导航 | 源码有 `Navigator` / `ToggleBrowserChannelRack` 处理 | Pads 可选 Channel Rack 音源 | 深度 Channel Rack / Pattern 操作 |
| 混音音量/声像 | 默认脚本对**当前选中 Mixer Track**提供音量/声像控制，具体焦点改变处理路径 | 8 个编码器可切换 Channel Rack Volume/Pan、Mixer Volume/Pan 五个页面之一 | 有专门 Mixer Inserts / Patterns 等功能 |
| 旋钮/推子 | **4 实体推子 + 8 编码器**；原生插件映射表，第三方 VST 可能要 MIDI Learn/MultiLink | **8 编码器、无实体推子**；预设面向原生插件；第三方 VST 使用 Custom Mode | **8 编码器、无实体推子** |
| 常用鼓垫 | 8 pads；FL 脚本有 FPC 映射 | 16 pads；配合 FL Channel Rack 和 DAW 模式 | 16 pads；高度围绕 Channel Rack/Pattern |
| 实际兼容条件 | 官方 v1.4 脚本；近期 FL Studio 可内置，旧版需手动部署 | 官方 Windows 说明适用 **FL Studio 24+** | 官方说明最低 **FL Studio 21.0.3+** |

与 FL Studio 相关的官方依据：
- [Arturia MiniLab 37 集成 FAQ](https://support.arturia.com/hc/en-us/articles/27901264120348-MiniLab-37-DAW-Integration)
- [官方 Python 脚本静态审计](fl-studio-minilab37-script-audit.md)
- [Novation Launchkey 37 全 DAW 控制指南](https://userguides.novationmusic.com/hc/en-gb/articles/27612230389138-DAW-control-with-the-Launchkey-37)
- [Novation Launchkey MK4 的 FL Studio 设置要求](https://support.novationmusic.com/hc/en-gb/articles/20499018257554-Launchkey-MK4-FL-Studio-Setup)
- [Novation FLkey 2 最低版本要求](https://support.novationmusic.com/hc/en-gb/articles/4921548925330-FLkey-Which-version-of-FL-Studio-do-I-need)
- [Novation Launchkey MK4 vs FLkey 2 比较](https://support.novationmusic.com/hc/en-gb/articles/35765627682834-What-are-the-differences-between-Launchkey-Mk4-and-FLkey-2)

## Cubase：专用映射与部署差异

- **MiniLab 37**：Arturia 有官方 Cubase MIDI Remote Script 1.4。操作路径：在控制器切换 DAW Mode，Cubase MIDI Remote Manager 导入 `Arturia_MiniLab 37.midiremote`。原厂特别提醒只把真正的 MIDI 音符输入端口包含于 “All MIDI Inputs”，防止 DAW 按键重复触发音符。参考 [Arturia FAQ](https://support.arturia.com/hc/en-us/articles/27901264120348-MiniLab-37-DAW-Integration)。
- **Launchkey 37 MK4 / Launchkey Mini 37 MK4**：Novation 说明 **Cubase 14.0.20+** 通常无需另外安装脚本，可自动识别；旧版 Cubase 可以使用 Novation 安装器。Launchkey 37 的 **8 Quick Controls**、Channel EQ 四段频率/增益、pads 的 Select/Arm 与 Mute/Solo 都有官方控制定义。参考 [Cubase Setup](https://support.novationmusic.com/hc/en-gb/articles/20225881390482-Using-Launchkey-MK4-in-Cubase)、[Launchkey DAW Guide](https://userguides.novationmusic.com/hc/en-gb/articles/27612230389138-DAW-control-with-the-Launchkey-37)。
- **FLkey 2 37**：面对 Cubase 时主要走通用 HUI/普通 MIDI 控制，核心优势来自 FL Studio；不应假设在 Cubase 拥有与 Launchkey 对等的专用映射。
- **KeyStep 37 mk2**：可使用 USB-MIDI 发送音符/aftertouch 及 CC；官方定位偏音序/硬件与普通 MIDI 控制。轨道选择、VST 快捷键等需要自行安排 MIDI Remote 或其他映射。

## 选型决策树（无价格参与）

1. 先测是否想保留全尺寸键距：若全尺寸让双手和弦/力度更舒服，**Launchkey 37 MK4** 在 595 mm 限制内应是主要候选，接受 251 mm 深度及无推子。
2. 若更看重 **桌面纵深、Slim 键手感与实体推子**，优先 MiniLab 37；尤其偏向 Analog Lab、多种 DAW 的工作流。
3. 若很在意**琴键 aftertouch、硬件独立音序或未来连接合成器**，优先试弹 KeyStep 37 mk2；其 148 mm 机身深度同时很有吸引力。
4. 若 DAW 最终锁定 FL Studio 并常做 Pattern/Channel Rack 的编曲，保留 FLkey 2 37 作 Launchkey 的直接竞争者。
5. Launchkey Mini 37 MK4 在需要携带、机身深度更小或个人确实喜欢 mini 手感时才进最终比较。

**下一步：** 两台主候选 MiniLab 37 与 Launchkey 37 MK4 已有官方规格、至少两份使用者测评和 DAW 配置资料，可进入真实商品 SKU/售价核验；KeyStep 37 mk2 与 FLkey 2 37 先当条件候选、Launchkey Mini 37 MK4 当空间备选。先核目标型号，再查四站价格。
