# 37 键及以下 MIDI 键盘：横向测评与淘汰理由

> 2026-10-24 · 面向 Windows / FL Studio / Cubase · 用户约束：**≤37 键、宽度 ≤595 mm**，主要任务是编曲时录入旋律、和弦，暂无预算上限，允许二手。
>
> **证据边界：** 本报告是一篇综合资料型横评，依据原厂规格、官方脚本静态阅读、多个媒体实测及真实用户经验。没有把这 12 台实际摆在同一张桌上测试；无法保证主观键床、力度或延迟的跨设备排名。定性结论都按当前用户场景解释，未有量化实验时不使用伪精确分数。价格另见后续价格调查，不参与第一层筛选。

## 先弄懂 7 个评测维度

1. **琴键结构与旋律/和弦输入（最高权重）**：mini / slim / full-size 的键宽、黑键根部可操作空间、回弹、重复音。键数相同，键宽和弹奏体验可能差很多。所谓“半配重”同样不能替代真实触感或力度测试。
2. **力度（velocity）准确性**：是弹弱/中/强是否稳定的核心。要用 MIDI Monitor 实际记录，不依赖演示里的 VST 音质。**琴键触后（keybed aftertouch）与鼓垫触后（pad aftertouch）完全不同**。
3. **FL Studio/Cubase 映射与生产力**：走带、录音、撤销、轨道选择、Channel Rack、Mixer、插件参数、重启保留。官方脚本证明功能意图，不能证明 Windows 实测没有 bug。
4. **控制区**：无限编码器、实体推子、pads、弯音/调制轮或触控条、参数显示，以及翻页/Shift 操作层级。
5. **音乐创作功能**：Arp、Chord、Scale、独立音序器、外部 MIDI/CV。根据用户主做电脑编曲的工作流权衡。
6. **桌面布局**：除了 595 mm 宽度，还要看深度、设备重量及接线净空。
7. **可靠性与软件生态**：固件、驱动、蓝牙连接、附赠音源、二手机器注册码及官方转移流程。

**注意**：MIDI 键盘通常发送 MIDI 事件，录出来的钢琴/合成器音色取决于 VST、音源和音频系统。不能凭视频音色直接给键床“音质评分”。

## A. 主要候选横向表

| 精确型号 | 琴键 / 宽×深 mm | 值得选的地方 | 对当前用途的主要弱点 | 暂定地位 |
|---|---|---|---|---|
| **Arturia MiniLab 37** | 37 slim / **503×183** | 三个八度输入、4 实体推子+8 编码器、8 实体 pads（2 bank）、FL Studio/Cubase 官方脚本、Analog Lab 生态 | 较窄琴键；无键床触后；8 pads 的手感被个别评论批评偏硬；小屏幕；非所有 VST 自动映射；Pitch/Mod 为触摸条 | **整体最均衡，第一顺位** |
| **Novation Launchkey 37 MK4** | 37 **全尺寸** synth / **557×251** | 尺寸上限内的全尺寸键、16 带复音触后的 pads、8 无限编码器、实体 Pitch/Mod 轮、较深跨 DAW 控制及 Arp/Chord | 机身深且重（2.18 kg）、**没有实体推子**、琴键手感不同评测分歧明显、Shift/模式层级较多；37 键机身不提供 49+ 型号的真正键盘 zones | **重视演奏/完整 DAW 控制者的第一替代** |
| **Arturia KeyStep 37 mk2** | 37 slim + **键床触后** / 547–550×148（官网宽度不一致） | 唯一近似键盘尺寸中的触后突出项、64-step 独立音序、MIDI/CV 扩展、极浅机身 | **无鼓垫、无推子**、轨道混音与 DAW 控制不如 MiniLab/Launchkey 直接、某些控制进入菜单、USB 供电 | **键床触后/硬件音序条件优先** |
| **Novation FLkey 2 37** | 37 全尺寸 synth / **557×251** | FL Studio Pattern、Channel Rack、Mixer Inserts、Sequencer Graph Editor 和插件插入等专用映射 | Cubase 主要使用 HUI/通用 MIDI，跨 DAW 没有 Launchkey 同等级原生支持；**无实体推子**、深度较大；若 DAW 未定，专用优势有落空风险 | **确定主用 FL Studio 才进入前三** |
| **Novation Launchkey Mini 37 MK4** | 37 mini / **477.8×176.8** | 紧凑轻便、16 pads、8 编码器、跨 DAW 控制、Arp/Chord 功能和全尺寸版很接近 | **迷你短键程**对大手、黑键根部的和弦及中力度控制可能不利；无推子；Pitch/Mod 触摸条；仅 3.5mm MIDI Out | **便携/桌面深度特别敏感时保留** |

## B. 容易漏掉的真正对手

### AKAI MPK Mini Plus II（2026-10-22 上市）

37 mini keys，**493×192 mm**，8 枚 MPC 风格 pads、8 编码器、实体 Pitch/Mod 轮、彩屏和独立音序、MIDI/CV。

- **它的真正优点**：鼓垫与节奏创作、MPC 生态、传统弯音轮、音序及连接能力结合得紧凑。二代有官方 DAW Maps、NKS、Progression/Strum/Mutate。官方 FAQ 现明确列出 **FL Studio v26、Cubase 15** 脚本，必须更新此前“DAW 兼容未知”的判断。
- **它输在什么地方**：键床依然是 mini；鼓垫只有 8 枚实体 pads；没有 MiniLab 的四推子，也没有 Launchkey 的 37 个全尺寸琴键；2026-10 刚上市，键床与按键寿命没有足量独立长期报告。DAW 脚本还受 **FL Studio v26 / Cubase 15** 等具体版本约束。
- **裁定**：升级为 **重要观察候选，功能上可以与前三竞争**，但不能拿初代口碑冒充二代成熟度。

资料：[AKAI 官方产品](https://www.akaipro.com/mpk-mini-plus-ii/) / [二代官方 FAQ](https://support.akaipro.com/en/support/solutions/articles/69000884506-mpk-mini-plus-ii-frequently-asked-questions)。

### M-VAVE SMK-37 Pro

37 速度敏感键，**458×181 mm**，蓝牙 MIDI / USB MIDI、8 编码器、4 推子、16 pads，且有内置 FM 音源相关玩法。

- **真优势**：功能表和桌面空间非常有竞争力，可以独立尝试音色/音序、无线连接是便利项。
- **输在什么地方**：没有与 MiniLab/Launchkey 同等可靠的长期键床对照；曾有**有线模式 MIDI 发送延迟/前几个 note 异常**用户报告。官方于 2026-08-12 发布 V016 并说明修复发送延迟，但不能把发布修复等同于每一台卖货设备都已升级且毫无异常。DAW 原生脚本的成熟性证据也较薄弱。
- **裁定**：**高功能密度、需严格固件验收的备选**。必须实测 Note On 延迟/丢失和菜单切换后的连奏，再考虑购买。

资料：[官方规格/固件](https://www.m-vave.com/product?id=smk-37-pro) / [原厂下载](https://www.m-vave.com/download) / [SMK 用户固件整理](https://github.com/jonathaslacerda/smk-37-pro-docs/blob/main/firmware/FIRMWARE.md)。

### M-Audio Oxygen Pro Mini

32 个 mini semi-weighted 风格琴键，宽约 **401 mm**；4 推子、4 编码器、8 pads、走带按钮、Smart Chord/Scale。

- **优势**：MusicRadar 的 2021 实测认可键盘手感、丰富的 DAW 控制与参数编辑，控制区能正面竞争 MiniLab。
- **输在什么地方**：只有 32 键，少于用户允许的 37；一些真实用户报告黑键力度不一致、pads 漏触、个别按键失灵，属样本有限的投诉，不能断言整批次故障；相对旧一代软硬件体验要查具体 Windows/DAW 版本。
- **裁定**：重要次优备选，尤其爱实体推子但桌面纵深有限者；**质量案例未查清时别直接下单**。

资料：[MusicRadar 长篇测评](https://www.musicradar.com/reviews/m-audio-oxygen-pro-mini) / [Reddit 真实故障报告（个例）](https://www.reddit.com/r/midi/comments/17hq5lp/oxygen_pro_mini_really_that_bad_quality/)。

## C. 其他型号为什么暂时不进前排

| 型号 | 长处 | 针对当前用途的关键不足 |
|---|---|---|
| AKAI MPK Mini Plus 初代 | 37 键、鼓垫、音序、CV/MIDI | 较早代的接口/显示和专用 DAW Map 不及刚上市的二代；现在没有特别值得选择初代的已证实理由（将来可随二手价格重新评估） |
| **Native Instruments Komplete Kontrol M32** | 32 键、8 编码器、NI / Komplete / NKS 音色浏览 | 只有 32 键，**没有鼓垫或推子**；对不确定是否主用 NI 音源的用户，其最大软件生态优势用不上 |
| **Korg microKEY2-37** | 37 Natural Touch mini 键、实体 Pitch/Mod 轮、机身仅 **139 mm 深** | 机身 **565 mm 宽**，虽合格但横向节省有限；**没有鼓垫、推子与八个可映射编码器**；DAW 控制更靠鼠标 |
| **Nektar Impact LX Mini** | 25 键，8 pads、8 pot、DAW 集成，宽 390 mm | **仅 25 键**，双手和弦/旋律音域明显更受限，除非极端便携无需优先 |
| **Arturia KeyStep Pro** | 37 slim 键、触后、4 轨独立音序器和强大 MIDI/CV | **589 mm 宽，仅剩 6 mm 余量**；208 mm 深、硬件控制复杂，若主做 DAW 录入则高概率闲置多轨音序能力 |
| **Arturia AstroLab 37** | 37 slim 键、内置音源和现场独立发声，宽 515 mm | 属于有内置声音引擎的独立硬件合成器；如果当前只要 MIDI 输入，就会多出用不到的整套硬件与音色系统 |

官方参考：[Korg microKEY2](https://www.korg.com/uk/products/computergear/microkey2/page_1.php) / [Nektar LX Mini](https://nektartech.com/products/impact-lx-mini/) / [Arturia KeyStep Pro](https://www.arturia.com/store/midi-controllers-sequencers/keystep-pro) / [AstroLab 37](https://www.arturia.com/products/hardware-synths/astrolab/astrolab-37) / [NI M32](https://www.musicradar.com/news/best-cheap-MIDI-keyboards)。

## D. 逐维结论（适合口头测评）

- **旋律与和弦的手部空间**：Launchkey 37 MK4 / FLkey 2 37 有全尺寸键距；MiniLab 37 与 KeyStep 37 mk2 的 slim 是紧凑折中；Mini 37、AKAI Plus II 更适合轻量旋律、鼓点及短句录入。此为键床形态带来的机械倾向，**不是本人同场客观手感成绩**。
- **演奏力度**：目前没有对所有品牌做统一 MIDI velocity 测试，因此**不排通用力度冠军**。MiniLab 两个 B 站实操测评较积极，Launchkey 37 两位中文使用者的软硬评价相反；Mini 37 用户对中等力度的稳定性有明确个例抱怨。
- **鼓垫**：Launchkey 系列 16 枚 FSR pads + poly aftertouch 在数量/表达上有优势；AKAI 8 枚 MPC 风格 pads 值得鼓手手指实测；MiniLab 8 枚 2 bank pads 有使用者觉得偏硬；KeyStep 37 mk2 无 pads。
- **混音与效果参数**：MiniLab 37 / SMK-37 Pro 的四个实体推子能直接做动态动作；Launchkey/FLkey 的无限编码器方便翻页、避免旋钮“跳值”，但37 键没有推子。**Arturia 官方 FL Studio 1.4 脚本默认不会把 4 推子简单等同于 4 个不同 Mixer 音轨的音量**。
- **DAW**：若 FL Studio 已确定为唯一主 DAW，则 FLkey 2 37 的 Channel Rack / Pattern / Mixer Inserts 等专用功能领先；跨 DAW 时 Launchkey 37 与 MiniLab 37 都有原厂集成。Launchkey 37 Cubase 14.0.20+ 官方支持自动识别；MiniLab 需要正确导入/选择官方 MIDI Remote。AKAI 二代在 FL26/Cubase15 也已有原厂脚本，新品表现待查。
- **音序/外部硬件**：KeyStep 37 mk2 与 KeyStep Pro 领先外部设备控制；AKAI 二代有音序/MIDI/CV；若大部分 MIDI 要在 DAW Piano Roll 后期编辑，这一优势权重可以降低。
- **桌面**：Launchkey 37 557×251 mm，占地矩形约 **1398 cm²**；MiniLab 503×183 mm，约 **920 cm²**，前者约多 52% 机身底面面积。KeyStep 37 mk2 更浅，约 148 mm。以上均不计插线空间。

## E. 个体需求下的最终评价

**已确认的信息**：用户曾使用过一台放在酒店的 Yamaha YDP-103，但它不归用户所有，不属于可调用的日常设备。本次仍需要评估独立购买的桌面 MIDI 控制器，宽度限制 595 mm，DAW 尚未在 FL Studio/Cubase 中定案，预算暂不设上限。

1. **综合第一选择：MiniLab 37**。适合以旋律和和弦为核心，同时希望有实体混音控制、软件音色和良好桌面比例。风险是 Slim 键适应程度和较硬鼓垫。
2. **优先完整琴键：Launchkey 37 MK4**。全尺寸 37 键，Cross-DAW 工作流成熟、打击垫数量多。如果弹琴空间比小巧和推子重要，它可能排到第一；重点试弹并确认 251 mm 深度。
3. **专攻 FL Studio：FLkey 2 37**。在主 DAW 确定之前暂不提前锁定。
4. **触后/硬件编曲：KeyStep 37 mk2**。适合独立 Arp/Seq、模块合成器，当前 DAW 场景可能用不上大半能力。
5. **鼓点/新一代多功能：AKAI MPK Mini Plus II**。有趣且官方已补足两大 DAW 脚本，但是 mini 琴键及缺乏长期可靠性证据，先留在重点复核名单。
6. **极致紧凑：Launchkey Mini 37 MK4**；**功能密度/无线：SMK-37 Pro**；**32 键且需要推子：Oxygen Pro Mini**。三者都有明确使用场景，暂不把主观差评包装成整体产品故障。

### 仍需实际验证，不能“测评口播造数据”

- 同台力度测试：每种弱/中/强反复 30 次、记录 MIDI velocity，评估不同琴键均匀性。
- Windows DAW：载入、重启、切换插件后跟随映射，具体测 FL Studio 与 Cubase 的同一操作任务。
- 反复插拔、固件确认、二手授权转移、鼓垫轻触阈值和编码器反向跳变。
- 价格及 SKU 在单独的文件调查；不把搜索列表其他规格的低价套到 37 键。

## 核心来源

- [Arturia MiniLab 37 官方规格](https://www.arturia.com/products/hybrid-synths/minilab-37/overview)
- [Novation Launchkey 37 MK4 官方规格](https://novationmusic.com/products/launchkey-37)
- [Novation FLkey 2 vs Launchkey MK4 官方比较](https://support.novationmusic.com/hc/en-gb/articles/35765627682834-What-are-the-differences-between-Launchkey-Mk4-and-FLkey-2)
- [AKAI Plus II FAQ / DAW 脚本版本](https://support.akaipro.com/en/support/solutions/articles/69000884506-mpk-mini-plus-ii-frequently-asked-questions)
- [MusicRadar Launchkey 25/37 MK4](https://www.musicradar.com/music-tech/midi-controllers/launchkeys-are-a-reminder-that-sometimes-a-keyboard-is-still-what-you-need-even-with-ableton-live-novation-launchkey-mk4-25-and-37-review)
- [WIRED Launchkey MK4](https://www.wired.com/review/novation-launchkey-mk4/)
- [The Verge MiniLab 37](https://www.theverge.com/tech/948024/arturia-minilab-37-midi-controller-review)
- [KeyStep 37 mk2 MusicRadar 实测](https://www.musicradar.com/music-tech/controllers/arturia-keystep-37-mk2)
- [Oxygen Pro Mini MusicRadar 评测](https://www.musicradar.com/reviews/m-audio-oxygen-pro-mini)
- [MiniLab 37 B 站两份实测](review-minilab-37-bilibili.md)
- [Launchkey 37 MK4 B 站两份使用体验](review-launchkey-37-mk4-bilibili.md)
- [官方 FL Studio 脚本静态审计](fl-studio-minilab37-script-audit.md)
