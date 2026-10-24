# 2026-10-24 测评渠道重试与证据质检

## 连接恢复

- 用户请求“再试试”后，使用 Desktop Commander Remote 的 list_devices，证实当前在线设备仍为原 rino-pc。
- `chrome-devtools status` / `list_pages` 均成功；原 Chrome 调试会话与四个购物平台标签页保留，无需重新配置或登录。
- 在保留的 B 站视频页通过脚本验证：`video.muted = true`、`volume = 0`、`paused = true`；未触碰系统或日常 Chrome 音量。
- 直接在已登录 B 站页面使用站点公开视频搜索/播放器接口获取视频基础信息和自动字幕。无需新开并播放视频，避免干扰桌面声音。对带失效临时签名的字幕 URL 仅使用实时生成链接，不写进仓库。

## 新定位的 B 站视频

| 方向 | 视频 | 确认 | 使用限制 |
|---|---|---|---|
| Arturia KeyStep 37 mk2 | [键盘中国 KeyboardCN：《KeyStep 37 mk2 玩法功能全方位介绍》](https://www.bilibili.com/video/BV1JSA8zGEaU/)，2026-02-28，8:50 | 标题明确是 **37 mk2**，视频有自动字幕链接 | 字幕 **严重串台**：内容是笑话/歌曲片段，后半程缺失，**判定不可靠，不得基于该字幕写评价**；另寻独立评测 |
| Arturia KeyStep mk2 | [垢教授：《孤独的进化——Arturia KeyStep mk2》](https://www.bilibili.com/video/BV1XpCJBnEzA/)，2025-11-13，17:58 | 明确为 2025 年发布的 **32 键 KeyStep mk2**，与 2026 年 37 mk2 为不同 SKU | 可参考家族音序器思路，**绝不能把它当 KeyStep 37 mk2 上手测评** |
| M-VAVE SMK-37 Pro | [新杭qwq：《SMK-37 Pro 功能概览》](https://www.bilibili.com/video/BV11WtdzHEZ6/)，2025-08-12，9:43 | 完整自动字幕可读取，内容与产品一致 | 视频中明确表示 **厂商寄送样机**；且拍摄早于 2026-08 的 V016 固件 |
| M-VAVE SMK-37 Pro | [yuyao9853428：《SMK37 pro 上手体验+音色库试玩》](https://www.bilibili.com/video/BV17VMhzWEnk/)，2025-06-15，25:18 | 页面真实存在，自动字幕有索引 | 字幕只有无关的几十秒段落（“这瓜保熟吗”），**判定串台，不能用作设备使用证据** |
| M-VAVE SMK-37 Pro | [LiangChenMusic：《SMK 37 Pro 入门指南》](https://www.bilibili.com/video/BV162KqzMEqA/)，2025-06-27，7:29 | 页面存在 | 播放器没有提供可用 AI 字幕，尚未分析完整内容 |
| Novation FLkey 2 37 | 搜索“FLkey 37 mk2 测评” | 命中大量 **2022 原版 FLkey 37** 视频 | 2022 年型号不能混用为 2026 年 FLkey 2 37；暂缺准确的中文版二代上手 |

## M-VAVE SMK-37 Pro 功能视频的时间码（来自 AI 字幕，待人工听写校对）

来源：新杭qwq / BV11WtdzHEZ6。作者 01:09 明确说明设备由厂家寄送。

| 时间段 | 视频中展示或描述的功能 | 对用户价值 |
|---|---|---|
| 01:09–02:30 | 设备能以内部 FM 合成器独立发声，有内置音色和音序器；视频播放了音色例子 | 对离开 DAW 的创作、随手试音有价值，但录音品质不能靠字幕评定 |
| 02:30–03:20 | 屏幕显示正在弹奏的音及和弦名称；可显示一键和弦结果 | 有利于理解和弦构成，尤其编曲及乐理学习阶段 |
| 03:20–04:35 | 旋钮、推子 MIDI 映射、16 pads 和硬件音序器的说明 | 能提供参数控制，但没有针对 Cubase/FL Studio 的实测脚本比较 |
| 04:35–06:04 | 演示直接使用设备录制/编辑音序片段并播放 | 可验证硬件独立创作思路 |
| 06:04–07:35 | 演示 Arp、Scale、屏幕音阶图示 | 有学习辅助效果；音阶功能对熟练编曲者未必提高效率 |
| 07:35–09:43 | 演示 USB 相关音频输入、FM 音色参数和效果器控制 | 具体 USB 音频支持和驱动配置应以现行官方手册/固件为准 |

### 固件时代差异，必须明确

本视频发布于 **2025-08-12**，而当前官方 [M-VAVE 固件页面](https://www.m-vave.com/product?id=smk-37-pro) 显示 **V016 / 2026-08-12**。固件整理 [V016 修复说明](https://github.com/jonathaslacerda/smk-37-pro-docs/blob/main/firmware/FIRMWARE.md) 包含 MIDI note latency fix 和 USB Rec 等功能变更。

因此视频只可证明较早版本存在特定功能，**不能用于评价 2026 年新固件在实际稳定性/延迟上的表现**。

## KeyStep 37 mk2 的独立来源补充

- [MusicRadar：Arturia KeyStep 37 mk2 实测](https://www.musicradar.com/music-tech/controllers/arturia-keystep-37-mk2)：37 slim 键、触后、OLED、独立 64-step / 8-note polyphony sequencer，以及 4 编码器和丰富 MIDI/CV 接口。部分操作从面板改为菜单，优缺点均有讨论。
- [Synth Anatomy / 2026-02-26：完整评测](https://synthanatomy.com/2026/02/arturia-keystep-37-mk2-review-a-no-brainer-midi-cv-controller-and-sequencer.html)：**Arturia 免费提供样机，作者已披露**；肯定外部合成器控制、琶音器和音序生成，批评部分原有操作选项减少。不能把这条的主观感受当作无商业关系的用户长期评价。
- [KeyStep 家族代际对照](https://pianoandsynth.com/arturia-keystep-models-compared/)：37 mk2 发布于 2026-02，32 键 mk2 发布于 2025-11；注意旧代材料的时间和型号。

## 测评代理质量规则（新增）

- 获取官方自动字幕后，应检查 **首段、中段和尾段** 是否与视频主题及发布时间匹配，再进行归纳。
- 字幕可能来自站点生成的错误转写、复用/串台、剪辑音乐/片头以及数据接口异常。若主体与器材明显不符，标记 **rejected: transcript mismatch**，保留视频原始 URL，但拒绝任何器材结论。
- 有厂商送测/赞助关系，只把视频中的**可见功能演示**作为较可靠事实；外观/手感和推荐结论需其他独立用户验证。
- 对 2026 年新型号严格核 SKU：**KeyStep mk2（32 键）≠ KeyStep 37 mk2；FLkey 37（2022）≠ FLkey 2 37（2026）**。
- 最新固件与旧视频之间的时间差需要记录，不能用旧测评证明最新版问题已修复。
- 目前仍没有 MiniLab 37 与 Launchkey 37 MK4 **同台、同 VST、同速度曲线**的客观对照，保持两者主候选身份。
- **本次没有查找零售价格，没有下单、联系卖家或改动账号。**
