# 第二梯队 MIDI 键盘：独立测评、用户反馈与缺陷状态

更新：2026-10-24。本文件收集可追溯的来源，属于**型号研究**，暂不分析价格。评价“可信度”表示某条证据能支持什么结论，并非产品质量打分。

## 1. Novation Launchkey Mini 37 MK4

**官方事实**
- [Novation 型号规格](https://us.novationmusic.com/products/launchkey-mini-37)：37 个 mini synth-action 琴键；16 个 poly-aftertouch pads；8 个 encoders；触摸式 pitch/mod 条；477.8 × 176.8 × 49 mm；支持 FL Studio/Cubase/Live 等专用 DAW 集成。
- 相比 [Launchkey 37 MK4](https://novationmusic.com/products/launchkey-37)：宽度节省约 **79.2 mm**，深度节省约 **74.2 mm**。由于用户宽度上限为 595 mm，两个型号均符合，因此只有在桌面**深度**、移动携带或控制布局有实际限制时，小键方案才有明显的空间收益。
- [MusicRadar 2024-09-19 同代 25/37 Mini 实测](https://www.musicradar.com/music-tech/midi-controllers/novation-launchkey-mini-mk4-review) 认为功能设计与 OLED 反馈好，迷你琴键的可演奏性有限。此评测覆盖同代 25/37 Mini。

**社区意见分歧**
- [Reddit r/Novation 2025-12 至 2026-03 的讨论](https://www.reddit.com/r/Novation/comments/1pkbg9r/whats_the_keybed_like_on_the_launchkey_mini_37/)：
  - 一名确实拥有 Mini 37 的用户喜欢短键程带来的快速触发，尤其用于节奏型演奏，并且喜欢 pads。
  - 另一名拥有 Mini 37 的用户抱怨黑键靠内侧触发困难、和弦指法受限，最终更换成全尺寸 37。
  - 还有使用者对 **custom mode 下无限编码器的相对式 CC 操作**表达不满；此问题可能随设备设置或固件变化，**没有复现，不能断言所有 DAW/模式都有问题**。
- [Reddit 2026-05 实际拥有者的 velocity 控制抱怨](https://www.reddit.com/r/Novation/comments/1tre7n4/upgrading_from_launchkey_mini_to_mk4_49_or_61/)：在模拟原声贝斯的插件中难以稳定控制不同力度；属于个人病例，不证明所有设备如此。
- [Reddit 2026-02 Mini vs Full 37 用户决策](https://www.reddit.com/r/Novation/comments/1r7s8v2/ended_up_getting_2_mk4_launchkeys_which_do_you/)：有从 Mini 转为全尺寸的例子，也有人为可携带性保留 Mini。

**当前判断**：保留为**明确需要薄机身/携带时的备选**；用户已有 595 mm 宽度，且主要做旋律和和弦输入，实际优先级低于全尺寸 Launchkey 37 与 Slim 琴键的 MiniLab 37。下一步必须检查桌面深度与真实连贯力度表现。

## 2. Arturia KeyStep 37 mk2

**客观能力**
- 37 个 slim keys，支持 velocity 和 **键床触后**；4 个编码器，可分 4 组提供合计 16 个 MIDI CC；带复杂的独立音序器和琶音器、CV/Gate、USB-C、5-pin MIDI。
- [Synth Anatomy 2026-02-26 长篇实测](https://synthanatomy.com/2026/02/arturia-keystep-37-mk2-review-a-no-brainer-midi-cv-controller-and-sequencer.html)：关注手感、CV/LFO/包络、64 步独立音序、mutate/spice、编码器；**评测样机由 Arturia 免费提供，作者披露厂商不能审稿**。作者评价键床表现良好，但承认个别操作逻辑和功能取舍。
- [Gearnews 同型号实测](https://www.gearnews.com/arturia-keystep-37-mk-2-review-synths/)：OLED、改良音序器和更深入的硬件控制是优势，原有部分功能直达路径减少。
- [Reddit r/arturia 2026-10-06 用户提问](https://www.reddit.com/r/arturia/comments/1wywh4e/how_to_make_most_out_of_keystep_37_mk2_with/)：原有 MiniLab 用户发现 KeyStep 很难找到现成的 Arturia VST 模板；其他回复建议手动 MIDI Learn，且提到四编码器可发送 CC。此为少量用户反馈，**没有证明全平台缺乏官方脚本**。

**差异**：如果日后会买独立硬件合成器、半模块或 CV 设备，KeyStep 的价值明显上升；当前以电脑内 FL Studio/Cubase 音符录入为主，pads/推子/DAW 一键控制有限，未必值得为单独音序器牺牲这些功能。

**当前判断**：**特定工作流的优先备选**，重点看键床触后是否对表达有价值；不因为没有鼓垫就否定其音乐创作价值。

## 3. M-VAVE SMK-37 Pro

**官方规格**
- [M-VAVE/Sinco 原厂型号页](https://www.sincoaudio.com/product?id=smk-37-pro)：37 力度键、16 pads、8 encoders、4 推子、BLE/USB-C MIDI、2000mAh 电池，458 × 181 × 50 mm。
- [原厂下载页](https://www.cuvave.com/download) 明确给出 **SMK-37 PRO V016（2026-08-12）**。请区分 SMK-37 Pro / Elite / 其他非 Pro 型号。

**可追踪的已知缺陷与修复**
- [2026-08-14 Reddit 用户反馈](https://www.reddit.com/r/midi/comments/1vogyx2/mvave_smk_37_pro_and_elite_key_notes_lag/) 指出，KEYS 页面退出时连续按键可能丢掉前两个 note，**通过有线连接仍可复现**；说明不是 BLE 音频延迟问题。
- [SMK-37 固件整理资料](https://github.com/jonathaslacerda/smk-37-pro-docs/blob/main/firmware/FIRMWARE.md) 引用 V016 更新说明：修复琴键 MIDI note 发送延迟（'Resolved MIDI note-sending latency issue for keys'）；[Elektronauts 用户 2026-08-30](https://www.elektronauts.com/t/m-vave-smk-37-pro-affordable-dx7-emulator/234750?page=3) 明确报告 V016 改善。
- 官方网站和社区整理能交叉核实 **V016 已发布且说明有修复**；不能保证所有批次当前固件已升级，也不能声称所有 note 丢失和异常完全消失。
- 2026 年 10 月有第三方自定义固件实验与刷机故障报告。对普通购物代理来说，**不建议把第三方刷机能力计入设备价值，也无需让用户尝试改固件**。

**新增 B 站证据**：[新杭qwq《SMK-37 Pro 功能概览》](https://www.bilibili.com/video/BV11WtdzHEZ6/) 2025-08-12，视频中披露厂家寄送样机，演示内置 FM 音源、屏幕和弦显示、独立音序器、16 pads 及 USB 相关使用。技术功能可参考，但由于商业关系和拍摄时间均先于 V016，**不视为当前固件质量/稳定性的独立测评**。见 [重试质检报告](review-retry-evidence-qc.md)。

**当前判断**：**低成本方案但带明确固件验证项**。必须确认目标设备实际 firmware version，并做 USB MIDI note-on 连续触发与 UI 切换测试；缺乏稳定实测之前不进入首选。

## 4. AKAI MPK Mini Plus II

- [AKAI 官方产品页](https://www.akaipro.com/mpk-mini-plus-ii/)：2026 款；37 个 mini keys，493 × 192 × 54 mm、全彩 160×80 LCD、8 pads、8 编码器、pitch/mod 实体轮，USB-C 和 MIDI out/CV。
- [AKAI 官方代际 FAQ](https://support.akaipro.com/en/support/solutions/articles/69000884506-mpk-mini-plus-ii-frequently-asked-questions)：相较初代，新增 DAW Maps、MPC 集成、NKS、更多和弦/琶音工具及彩屏。
- [MusicRadar 2026-10-23 报道](https://www.musicradar.com/music-tech/akais-mpk-mini-plus-ii-is-here-the-usd169-midi-controller-takes-a-step-up-with-second-gen-upgrade) 仍属于**发布新闻**，不能证明新键床改善幅度或长期质量。
- 当前离首发仅两天，**没有可充分交叉核实的独立长期实测**。媒体提到键床“改良”，目前应视为厂商宣称等待验证。
- 必须将 II 与旧 MPK Mini Plus、MPK Mini MK3/MK4 的测评和固件资料严格分开。

**当前判断**：**新品观察**。可作为第 4–5 款候选候补，但暂不凭猜测提高到首选。

## 综合与下一步

- 三种琴键类型：Launchkey 37 全尺寸、MiniLab 37 slim、Launchkey Mini/AKAI mini。应在同一钢琴 VST 下先比较键距、黑键靠内侧的触发、轻/重力度与和弦连贯性。
- 实体演奏重于“广告功能多少”。预先设定的用户目标是**旋律和和弦输入、编曲**，所以在可容纳全尺寸 37 键时，应优先评估实际琴键可控性。
- 当前 Windows FL Studio/Cubase 控制能力，请结合 [daw-fl-cubase.md](daw-fl-cubase.md)；实际阶段继续以 [test-protocol.md](test-protocol.md) 为准。
- 2026-10-24 后续重试已恢复 Desktop Commander，且原 B 站页再次确认 **muted=true、volume=0、paused=true**。新增 [SMK-37 Pro 较早厂商送测视频的时间码，以及两条严重串台字幕的拒收记录](review-retry-evidence-qc.md)。自动字幕即使可下载也不能直接当作完整可信测评。
- 待评价资料足够、明确 3–5 款短名单以后再核对淘宝、京东、拼多多、闲鱼的实际 SKU 与价格。
