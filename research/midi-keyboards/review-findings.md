# 第一轮测评证据与筛选结论（2026-10-24）

**阶段：先研究型号/真实体验，不比较任何商品价格。** 这份文件只记录已查看的公开评测和用户反馈。品牌参数、样机短期测评、个人意见、固件历史分开处理。网络来源无法替代亲手弹奏测试。

## 中文视频核查进度

已使用用户授权的本地 Chrome 核实 [B 站候选视频 BV 链接与可访问信息](bilibili-source-triage.md)。例如垢教授的 [Launchkey MK4 使用分享](https://www.bilibili.com/video/BV1fhwqePELp/) 的作者简介明确说琴键手感不合心意、遗憾没有推子。这是作者主观观点，**未完整观看视频**，当前 B 站非登录浏览器仅提示试看 30 秒。所有尚未完整看的视频仍按「待复核」处理。

## 总体发现

1. **37 键已足够成为默认方向。** MiniLab 37 的独立实测认为比 25 键更适合兼顾和弦、低音和旋律；其他 37 键型号也在 595 mm 上限内。
2. **键床手感是最大分歧。** Launchkey 37 MK4 获 MusicRadar 正面评价，WIRED 对 25/37 的合成器键床不太满意。两者只是测评者主观感受差异，不能算客观产品缺陷。
3. **Mini 键床要单独把关。** SoundGuys 真正测试了 Launchkey Mini 37 MK4 两周，赞赏工作流但提示小键/无配重；2024-12 的一位购买者明确抱怨琴键偏硬与力度曲线。这个用户反馈未获充分独立验证。
4. **MiniLab 37 易于上手，但深度 DAW 控制和小屏幕是取舍。** The Verge 作者认为控制区布局符合直觉，同时指出塑料感明显、屏幕小、琶音器参数编辑烦琐。
5. **M-VAVE SMK-37 Pro 出现过有线 MIDI 延迟问题，已有官方修复声明。** 官方 V016（2026-08-12）发布说明明确针对琴键音符发送延迟修复，Elektronauts 用户报告更新后显著改善；未在 Windows FL Studio/Cubase 做本地复现，不能断言所有设备问题都已消失。
6. **FLkey 2 37 仅在确认主用 FL Studio 时才是高优先级。** Novation 官方规格显示 FL Studio 原生脚本 + 其他 DAW 的 HUI 兼容；只要 DAW 还在 FL 与 Cubase 之间犹豫，跨 DAW 的 Launchkey 37 MK4 更稳妥。
7. **AKAI MPK Mini Plus II 在 2026-10-22 刚发布。** 已有商家上手、官方规格与新版 DAW 映射，但没有足量可靠长期用户记录，不能拿一代的老评价冒充二代。

## 型号详情

### A1. Arturia MiniLab 37

- 原始测评：[The Verge / Terrence O'Brien / 2026-06-11](https://www.theverge.com/tech/948024/arturia-minilab-37-midi-controller-review)。
- 测评事实：作者实际接触该机，认可 37 键的创作跨度、较浅的机身和更直观的控制排列。
- 明确不足：塑料外壳显得廉价；琴键有弹簧感；屏幕过小，音色浏览和琶音器进阶参数需要层层操作；其 DAW 控制需要接受手动映射或相对基础的控制深度。
- 社区独立线索：[2026-09-26 Reddit / MiniLab 37 琴键感受讨论](https://www.reddit.com/r/synthesizers/comments/1wqun2e/arturia_minilab_37_and_alternatives_key_feel/)：有回复认为比 MicroBrute 琴键回弹干脆；少量样本，仅是主观体验。
- **状态：优先实测**。重点验证 Slim 琴键在钢琴音色、连贯和弦/旋律下的表现；Cubase/FL Studio 的映射和四推子价值。

### A2. Novation Launchkey 37 MK4（全尺寸）

- 原始测评：[MusicRadar / Martin Delaney / 2024-11-26](https://www.musicradar.com/music-tech/midi-controllers/launchkeys-are-a-reminder-that-sometimes-a-keyboard-is-still-what-you-need-even-with-ableton-live-novation-launchkey-mk4-25-and-37-review)；[WIRED / Terrence O'Brien / 2024-11-25](https://www.wired.com/review/novation-launchkey-mk4/)。
- 一致信息：全尺寸 37 个合成器键、16 pads、8 无限旋钮、OLED、USB-C、5-pin DIN MIDI out，官方 [Cubase 脚本](https://downloads.focusrite.com/novation/launchkey-mk4/launchkey-mk4-37) 可下载。
- 主要分歧：MusicRadar 认可琴键；WIRED 对 25/37 键版本的键床和 pads 手感评价较一般。WIRED 尤其认为其鼓垫不适合高要求的 finger-drumming。
- 限制：37 键不支持大尺寸型号提供的键盘分区；显示旋钮参数时存在交互限制。
- 官方规格：[Novation Launchkey 37](https://novationmusic.com/products/launchkey-37)，宽 557、深 251、高 79 mm。
- **状态：优先实测**。37 键全尺寸方案中主要参考产品；需要验证重度输入时手感和 Cubase、FL Studio 的映射。

### A3. Novation Launchkey Mini 37 MK4

- 真正该精确型号的评测：[SoundGuys / Chase Bernath / 2025-02-07](https://www.soundguys.com/novation-launchkey-mini-mk4-37-review-132486/)：使用两周、Ableton Live 12、固件 1.1.1157.0；**测评样机由厂商提供**。作者重视 OLED、和弦/音阶功能、DAW 兼容，缺点是学习成本和小键、无配重。
- [MusicRadar / 2024-09-19](https://www.musicradar.com/music-tech/midi-controllers/novation-launchkey-mini-mk4-review) 的评测明确覆盖 Mini 25/37 两种版本，也指出小琴键演奏性弱于更大规格。
- [Reddit / 2024-12-12 个人主帖](https://www.reddit.com/r/synthesizers/comments/1hcns2y/novation_launchkey_mini_mk4_has_awful_keybed_and/)：一名购买者对 Mini 37 MK4 的琴键和力度曲线强烈不满，但认可 pads、DAW 集成。该抱怨属于单例，不认定普遍问题。
- **状态：优先实测，但键床风险待解**。用于验证 477.8 mm 的紧凑布局是否值得牺牲琴键尺寸。

### B1. Novation FLkey 2 37（即 FLkey 37 MK2）

- [官方产品说明](https://novationmusic.com/products/flkey-37)：37 synth-action keys、16 pads、8 encoders、FL Studio 专用 Channel Rack/Mixer/插件控制脚本，其他 DAW 通过 HUI。宽 557 mm。
- [官方兼容要求](https://support.novationmusic.com/hc/en-gb/articles/4921548925330-FLkey-Which-version-of-FL-Studio-do-I-need)：FLkey 2 37 需要 FL Studio 21.0.3 或更新版本。
- [In The Mix 视频 / 2026-05-19](https://www.youtube.com/watch?v=7g_hqbdOQUU)：展示新一代 FLkey 系列流程，**作者明确披露视频得到 Novation 支持**，仅作为操作演示，独立性不足。
- 注意：2022 年原 FLkey 37 的 [Sound On Sound 测评](https://www.soundonsound.com/reviews/novation-flkey-37) 属于旧型号，绝不能转述成 FLkey 2 的键床体验。
- **状态：条件保留**。决定把 FL Studio 作为主 DAW 后再提高优先级。

### B2. Arturia KeyStep 37 mk2

- [Gearnews / Rob Puricelli / 2026-02-26 实测](https://www.gearnews.com/arturia-keystep-37-mk-2-review-synths/)：肯定更丰富的音序生成、Spice/Mutate、OLED、额外的 CV Mod；批评取消部分直达 Arp/Seq 控件、旋钮无触摸感应，供电依赖 USB。
- [Synth Anatomy / 2026-02-26 实测](https://synthanatomy.com/2026/02/arturia-keystep-37-mk2-review-a-no-brainer-midi-cv-controller-and-sequencer.html)：作者明确披露 Arturia 免费寄送评测机，同时声明厂商不参与审稿。
- 官网两处尺寸相互矛盾：[产品详情页](https://static.arturia.net/zh/products/hybrid-synths/keystep-mk2/keystep-37-mk2) 标 58 × 547 × 148 mm（高宽深），[商店页](https://www.arturia.com/store/zh/keystep-37-mk2) 标 550 × 147 × 35 mm（宽深高）；虽然两种宽度均符合 595 mm，但**不能声称官方宽度唯一精确值已核定**，应标为 547–550 mm 待核。
- **状态：条件保留**。为以后外接硬件合成器、独立音序探索保留；电脑 DAW 工作流需衡量其额外功能的价值。

### B3. AKAI MPK Mini Plus II

- [官方一、二代差异 FAQ](https://support.akaipro.com/en/support/solutions/articles/69000884506-mpk-mini-plus-ii-frequently-asked-questions)：二代增加 MPC 集成、彩屏、旋律生成工具、DAW 映射、NKS；USB-B 升 USB-C；Windows 兼容。
- [RA / 2026-10-22 发布新闻](https://ra.co/news/86262)，[MusicRadar / 2026-10-23 新闻](https://www.musicradar.com/music-tech/akais-mpk-mini-plus-ii-is-here-the-usd169-midi-controller-takes-a-step-up-with-second-gen-upgrade)。
- [Sweetwater / 2026-10-22 商家上手文章](https://www.sweetwater.com/insync/the-akai-mpk-mini-plus-ii-wants-to-help-you-write-the-song/)：演示和弦、琶音及 Pads；**商家内容不能当独立品质评测**。
- 新款移除初代的部分物理连接（如 MIDI in、模拟同步），需在升级比较时核验。
- **状态：观察名单**。发布只有两天，未得到足够独立长期琴键/质量记录。

### B4. M-VAVE SMK-37 Pro

- [厂商官网](https://www.cuvave.com/product?id=smk-37-pro)：37 键、16 pads、8 encoders、4 推子，USB-C/BLE MIDI，尺寸 458 × 181 × 50 mm。
- [官方固件下载](https://www.cuvave.com/download)：SMK-37 PRO **V016 / 2026-08-12**。
- [历史故障报告 / Reddit 2026-08-14](https://www.reddit.com/r/midi/comments/1vogyx2/mvave_smk_37_pro_and_elite_key_notes_lag/)：有线模式亦遇到 UI 切换后前几个音符丢失/延迟。
- [官方 release notes 的社区整理](https://github.com/jonathaslacerda/smk-37-pro-docs/blob/main/firmware/FIRMWARE.md) 显示 V016 含琴键 MIDI note sending latency 修复；[Elektronauts / 2026-08-30](https://www.elektronauts.com/t/m-vave-smk-37-pro-affordable-dx7-emulator/234750?page=3) 有用户报告更新后改善。
- [Reddit / 2026-10-24 使用者负面反馈](https://www.reddit.com/r/Synthesizer/comments/1xdsebc/what_are_your_thoughts_on_the_mvave/) 对键床和菜单表示不满，但其单机音源体验不能直接等同于 USB-MIDI 控制场景的体验。
- 目前 B 站大量内容来自品牌和乐器商家，如 [科乐MIDI 2025-07-06 视频](https://www.bilibili.com/video/BV1pB3ezyEx5/)，这些可核功能演示，不宜当作独立耐久评测。
- **状态：条件保留**。需要确认所售产品固件≥V016，并要求有线 Windows 真实 MIDI note-on 速度与按键力度实测。

## 评测证据空白与具体下一步

- 目前缺少同一测评者对 **MiniLab 37、Launchkey 37 MK4、Launchkey Mini 37 MK4** 同一音源/力度曲线下的直接 A/B 实测。
- FL Studio、Cubase 在 Windows 上的实际 MIDI 映射仍需针对具体版号进行独立验证；厂商的“支持”只证明预期兼容，不保证日常流程。
- 大量 B 站内容目前仅定位到标题和搜索列表，没有完整视频操作记录，**不得臆测 UP 主视频中未公开的赞成或批评观点**。
- 购买阶段还未开始，不能用价格提前淘汰型号。
- 接下来聚焦 A1–A3 的键床与 DAW 实测，随后判断 B1–B4 是否值得进入最终 3–5 款短名单。
