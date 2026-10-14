---
访谈时间: 2026-07-29
访谈时间说明: "无法确认 Machina 现场各段访谈的独立录制日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: 2026-07-29T12:49:19Z
嘉宾名字: "Péter Fankhauser; Bernt Børnich; Amanda McMaster; Jonathan Hurst"
嘉宾公司名称: "ANYbotics; 1X; Boston Dynamics; Agility Robotics"
参与嘉宾:
  - 姓名: "Péter Fankhauser"
    公司或机构: "ANYbotics"
    职务: "联合创始人兼首席执行官"
  - 姓名: "Bernt Børnich"
    公司或机构: "1X"
    职务: "创始人兼首席执行官"
  - 姓名: "Amanda McMaster"
    公司或机构: "Boston Dynamics"
    职务: "临时首席执行官"
  - 姓名: "Jonathan Hurst"
    公司或机构: "Agility Robotics"
    职务: "联合创始人兼首席机器人官"
  - 姓名: "Jason Calacanis"
    公司或机构: "LAUNCH; All-In Podcast"
    职务: "LAUNCH 创始人兼首席执行官；All-In Podcast 联合主持人"
播客名称: "All-In Podcast"
播客url地址: "https://www.youtube.com/watch?v=TqNiSTeNtb0"
youtube_video_id: "TqNiSTeNtb0"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳后结合完整上下文转写为简体中文"
全文提及的关键名词:
  - "ANYbotics"
  - "ANYmal"
  - "explosive atmosphere"
  - "predictive inspection"
  - "ANYmal X"
  - "1X"
  - "NEO"
  - "teleoperation"
  - "embodied AGI"
  - "world model"
  - "egocentric video"
  - "hard takeoff"
  - "Boston Dynamics"
  - "Spot"
  - "Atlas"
  - "mean time between intervention"
  - "Robot-as-a-Service"
  - "Google DeepMind"
  - "Agility Robotics"
  - "Digit V5"
  - "sim-to-real transfer"
  - "AMR"
  - "dull, dirty, dangerous"
  - "AppLovin"
  - "Hyundai"
  - "Amazon"
  - "Toyota"
  - "Tesla Optimus"
---

# The $1/Hour Robot Is Coming: Four Industry Leaders Explain What’s Next

## Transcript

### 开场

**Jason Calacanis：**

大家好，我是 Jason Calacanis。我现在人在法国巴黎，参加一个叫 Machina 的会议。它讨论的是现实世界里的 AI，也就是 AI 如何从屏幕走进物理世界。接下来是我与几家领先机器人公司的现场访谈。

本期节目由 AppLovin Ads 赞助。AppLovin 从一个 8 美元的域名、没有 VC 融资起步，成长为全球最大的广告平台之一。现在同一套引擎也用于电商广告，让广告主在移动游戏里触达超过 10 亿日活用户。广告主给出目标，平台自动寻找买家并按利润优化。有一家厨具品牌的销售额从 400 万美元增长到 1,600 万美元并实现盈利，按当时速度预计当年可达到 8,000 万美元。

### ANYbotics：四足机器人先从高价值工业巡检落地

**Jason Calacanis：**

我们在巴黎的机器人公司系列访谈继续。Péter Fankhauser 博士是 ANYbotics 的联合创始人兼 CEO。你在这个领域做了接近 20 年，公司成立约 10 年，前五年更像研究实验室，过去五年则开始部署这类四足机器人。你们怎样定义它？

**Péter Fankhauser：**

我们不把它只当成一只会走路的机器狗，而是一套工业巡检解决方案。它负责在关键基础设施里采集数据、理解设施状态。四条腿只是承载这套能力的形态。

**Jason Calacanis：**

为什么四足形态先成为行业标准？现在不止一家厂商做这种机器人，它似乎比双足 humanoid 更早达到一定部署规模。

**Péter Fankhauser：**

自然界里很多动物有四条腿，这是有原因的。四足形态兼顾机动性、平衡和稳定性，可以爬楼梯，也能进入大多数人能够到达的地方。工业现场经常有湿滑地面、雨雪、泥土、草丛和不规则落脚点，较宽的支撑面和四个落脚点很重要。对我们服务的设施来说，四条腿是非常合适的形态。

**Jason Calacanis：**

那为什么不把人形机器人的上半身装到四条腿上，做成 centaur？Optimus、NEO、Atlas 都是双足站立，人们总担心它们跌倒，砸到人或伤到脚踝。

**Péter Fankhauser：**

当然可以这样设计，关键还是 use case。如果机器人要在咖啡店等狭窄空间工作，需要在人类视线高度操作，也许 humanoid 更好。但在我们的工业设施里，空间相对充足，稳定性优先，因此四足形态更合理。

**Jason Calacanis：**

你们已经在数百个现场部署了数百台机器人。单台采购成本大致是十几万到几十万美元，后续还有服务费用。它们显然不是家用产品，而是搭载许多昂贵传感器和强大算力的工业设备。以天然气管线为例，它可以全天候巡检，并发现人类感觉不到的问题，对吗？

**Péter Fankhauser：**

对。我们的重点不是简单替代人工，而是问机器人能否做得比人更好，甚至做到 superhuman。人眼和耳朵感知不到所有信号，例如极小的气体泄漏、设备异常升温或特殊声学信号。机器人可以装热成像相机、麦克风、声学传感器、气体浓度传感器以及本地 AI，把这些信息持续采集并分析。

真正的经济价值是避免停机。一些工业资产停运一小时就会损失数十万美元收入。只要机器人帮助客户提前发现问题，节省几分钟或几小时的停机时间，就可能覆盖机器人的成本。因此我们有条件在机器人上使用昂贵传感器和高性能 GPU。

**Jason Calacanis：**

这么强的本地计算意味着电池负担也很大。一次任务能运行一两个小时吗？

**Péter Fankhauser：**

大约两小时，之后机器人自动返回 docking station 充电，再继续下一轮任务。有些客户每天运行 14 次甚至 40 次任务。例如 electric arc furnace 启动时，客户特别想知道那一分钟里发生了什么。现场温度很高，不适合人进入，机器人却可以在关键时点带着热成像设备进去。

客户并不真正关心机器人本身，他们要的是数据和洞察。机器人只是准确采集数据的手段。我们要求 hands-free autonomy，不应该还要有人专门照顾它。部分计算必须留在机器人端实时执行，例如避障、数据质量检查和应对断网。若拍出模糊照片后才上传云端，已经太晚了。云端则适合做上下文分析、历史趋势比较和停机模式分析。

**Jason Calacanis：**

客户是否要求机器人连续工作 12 小时或 24 小时？

**Péter Fankhauser：**

确实有人希望更长时间运行，但多数场景每天有效工作约八小时已经足够，机器人有充电窗口。再提高频率会出现边际收益递减。过去人工一天可能只巡检一到两次，机器人能提高到八次、十五次或二十次，频率已经大幅增加，而且不用把人置于危险中，数据质量也更高。

**Jason Calacanis：**

你们最像科幻小说的部署是什么？

**Péter Fankhauser：**

任何 offshore 场景都很令人兴奋。工程师乘直升机去海上设施，一次飞行就可能花费数万美元。海上设施人少、环境恶劣，设备必须高度可靠。我们服务石油平台，也服务 offshore wind。机器人不是在海水里行走，而是在数百台风机汇集到的海上变电或换流平台上巡检。那里通常有人值守，但让机器人承担重复巡检依然很有价值。

机器人已经能在挪威约零下 20 摄氏度的环境运行，也能在沙漠里承受零上 40、50 甚至 60 摄氏度的高温。真正需要机器人的正是低温、高温、粉尘、潮湿等恶劣条件。我们还做了可以进入 explosive atmosphere 的特殊版本。在油气和化工现场，空气中可能有 methane，任何火花都会带来灾难，所以机器人必须被严格保证不会产生点火源。危险、偏远、枯燥和重复的任务最适合交给机器。

**Jason Calacanis：**

若机器人已经能发现泄漏，下一步显然是让它关阀、开柜，最后直接修好设备。什么时候可以做到？

**Péter Fankhauser：**

演示环境里已经可以做一些动作，但真实工业现场要求 99.9% 级可靠性，尤其在爆炸性环境中，差距仍然很大。第一步会是关闭 lever、打开 cabinet，最终再发展到双臂甚至三四条机械臂去修理设备。AI 会帮助我们，但还有大量工程工作。

许多 humanoid 折衣服演示发生在高度受控的室内环境。换成室外冰雹、冻结温度、强风或污染物，perception 和 manipulation 都会困难得多。我们相信长期能解决，但不能把 demo 当成已经可规模部署的产品。

**Jason Calacanis：**

你们机器人的零部件有多少来自中国？

**Péter Fankhauser：**

目前是零。并不是因为欧盟或挪威法律禁止，而是历史上我们主要在本地采购，芯片等来自美国，且公司十年前起步时自己开发了很多架构。对部分客户而言，供应链来源和数据主权很重要。

当然，今天全球已有不少低成本商品化硬件。我们会区分哪些是主动核心部件，哪些只是金属结构，在成本、能力和安全之间做聪明选择。中国仍是机器人零部件最积极的供给方，但欧洲和美国也有优秀公司；若只是劳动密集型装配，可以去更多地区，真正关键的是掌握核心部件能力的供应商。

**Jason Calacanis：**

中国厂商可能复制 IP，用便宜 80% 的机器人争夺同一批客户。你怎样看竞争威胁？

**Péter Fankhauser：**

现在不少中国机器人首先是一件能漂亮行走、甚至后空翻的硬件，工程质量很好。但客户不会只比较“哪台机器走得更好”，而是比较完整解决方案。工业部署还需要 autonomy、巡检 intelligence、workflow integration、数据治理和售后能力。

信任也很关键。我们采集的是关键基础设施里的高度敏感数据，因此需要完整的 cybersecurity 体系和 ISO 认证。客户不会愿意在核电站或其他关键设施里放置十几台由不可信第三方控制、持续拍摄并上传数据的相机。硬件价格只是竞争的一部分。

**Jason Calacanis：**

欧洲和 NATO 正在重新武装。你是否认为欧洲必须建立自己的防务技术？ANYbotics 会不会把四足平台用于军事？

**Péter Fankhauser：**

我个人认为欧洲有责任建设保护自己的技术能力。但 ANYbotics 已经选择并深入工业巡检这条路线。我们目前不做军事产品，也没有这样的计划。看起来只是把四条腿送进军队，实际上 military communication、autonomy、human-in-the-loop 和毫秒级响应要求都完全不同。若要认真解决军事问题，需要不同的产品和团队，而不是给现有机器人换一个客户标签。

我们确实收到过相关请求，但诚实的问题是：只交付一台会走路的机器人是否真正解决了任务？答案通常是否定的。工业巡检允许花时间预先设置任务，让机器人按路线自主运行；战场更强调即时遥控、抗干扰通信和另一套 autonomy。除了四足移动底盘，应用软件几乎都不同。

**Jason Calacanis：**

中国已经展示给四足机器人装枪，Ukraine 战场也证明无人机改变了战争。作为工程师，你怎么看武装机器人？

**Péter Fankhauser：**

我不喜欢，而且认为这很危险。工程师应该为建设有益技术感到自豪。防御是一回事，主动攻击和在机器人上安装枪械是另一回事。机器人技术正在成熟，但还没有成熟到可以轻率地把人的生命交给它决定。

目前看到的很多中国武装四足机器人视频更像早期 demonstration，并不代表已经像 Ukraine 的无人机那样形成成熟作战类别。四年前，ANYbotics、Boston Dynamics 等公司共同发表公开信，反对把通用机器人武器化。我们的理由很直接：这既危险，也愚蠢。ANYbotics 现在的任务仍然是非军事工业应用。

**Jason Calacanis：**

明白了。祝你们继续顺利发展。

### 1X：从 NEO 家庭机器人走向开放的 embodied AI 平台

**Jason Calacanis：**

下一位是 1X 创始人兼 CEO Bernt Børnich。1X 的 NEO 是面向家庭的 humanoid。你们收了很多预订，并承诺 2026 年把产品送进用户家里。你们能按时交付吗，价格又是多少？

**Bernt Børnich：**

承诺就必须兑现，我们会在 2026 年发货。但一开始速度会很慢，我们想把事情做对。2026 年先会有少量客户真正收到 NEO，我非常期待。

定价仍在演变。预售时有两种模式：一种是 early adopter 全额预付，另一种是 subscription。随着产品继续开发，订阅的最终结构也会和最早客户一起完善。我们还没有正式完整宣布另一件更重要的事：NEO 会开放给更多开发者，成为一个平台。

**Jason Calacanis：**

也就是说会有 app store 或 skill store。比如有人开发“做沙拉”技能，用户可以购买或订阅。

**Bernt Børnich：**

这会是其中一部分，但 1X 的目标远不止消费机器人。家庭市场非常重要，不过我们的长期使命是通过 humanoid 为整个社会创造 labor abundance。我们认为 NEO 已经成为一个很独特的平台，让其他人围绕它开发，可以把应用从家庭扩展到社会各个行业。

开放生态也会反过来改善消费者体验。开发者会做更多面向家庭的技能，同时有更多数据和模型加速 autonomy，最终让家里的 agent 能独立完成大量任务。

**Jason Calacanis：**

预订量是不是大约 2 万？

**Bernt Børnich：**

我们没有公布总数，但规模不小。前 1 万个名额在头几天就售罄。预售方案里也有大约每月 500 美元的订阅模式。

**Jason Calacanis：**

那它更像 Google Glass 或 Vision Pro 的第一代产品，服务愿意承受不完美体验的最早一批高端用户。

**Bernt Børnich：**

完全正确。我们一直明确说明，2026 年拿到家用 humanoid，产品必然还有棱角。它可能会跌倒。好消息是，按最近进展看，我们也许能交付接近 fully autonomous 的体验。预售时我们不敢承诺，因为当时太早，现在仍不会把它写成绝对保证，但趋势表明它可以在完全自主模式下完成相当有用的工作。

如果用户要求所有任务从第一天起就毫无失败，系统仍可能需要 teleoperation 或人工指导。不过用户若愿意接受能力边界，纯自主体验已经越来越可行。

**Jason Calacanis：**

Teleoperation 很有意思。纽约有一家鸡肉三明治店招不到收银员，于是雇了一位在菲律宾、时薪约 3 美元的员工，通过 Zoom 接单和处理客服。NEO 是否也能采用这种模式？我让它倒橙汁时，远程操作员临时接管。

**Bernt Børnich：**

各种模式都会发生。假设你经营橙汁店，购买一批 NEO 后会获得机器人操作系统、fleet management 和数据采集设备。数据采集手套使用与 NEO 相同的 tactile sensor 和 vision system。你可以让人在店里示范任务，把数据交给我们的系统做 dense captioning、fine-tuning 和部署，最终得到自动化门店。

如果模型还不能稳定完成任务，就让人偶尔 teleoperate，新的操作数据会继续改善模型。如果任务太复杂，也可以长期完全遥控。平台会覆盖从“只想自动化自己工作流”的开发者，到希望把自家 foundation model 部署到机器人上的实验室。

**Jason Calacanis：**

所以 NEO 是开放平台。如果 OpenAI、Anthropic 或独立 world model 公司有更好的模型，也可以装到 NEO 上。

**Bernt Børnich：**

是的。我们当然真诚相信 1X 自己的模型会最好，因为我们控制从制造、硬件到最终产品的全栈。如果拥有这些条件还做不出最佳模型，那就是我们的失败。但我们相信竞争，也会允许其他模型在 NEO 上运行。

现在没有任何一个 general model 能解决全部机器人问题。若未来几年我们把工程团队困在每个客户的后院，逐一对接 ERP 和特殊流程，就没有精力解决真正的一般问题。1X 想集中攻克 embodied AGI，同时让生态伙伴负责大量具体落地。机器人生态越大，所有参与者都受益。

**Jason Calacanis：**

很多任务不值得单独安排一个操作员。例如便利店机器人可能每小时只帮顾客把东西搬到车上一次。一个远程团队可以同时监控几十台 NEO，只在必要时接管。

**Bernt Børnich：**

我自己就有一个不会消失的 teleoperation 场景。我经常往返 Norway 和 San Francisco，也参加很多会议。出差时，我希望通过 NEO 在公司现场办公：把设备戴到 NEO 上，我就像成为 NEO 本身，可以在工厂里走动、拿起零件、观察细节、与员工交谈并参加会议。无论 autonomy 多强，这种远程 presence 仍有独立价值。

另一类场景是偏远电站。设备可能在森林深处，最近的工程师开车也要一小时。那里可以常备一台机器人，故障发生后，专家几分钟内远程进入现场、扳动开关并检查设备。任务几个月才发生一次，不值得专门训练一个自主模型，但“把全球最佳专家瞬间传送到现场”非常有价值，外科手术等领域也有类似潜力。

过去一年我们还发现，NEO 新一代手部的硬件能力已经高到 teleoperation 本身无法完全发挥。操作员感觉不到机器人触觉传感器感知的全部信息。若为人类搭建完整 haptic system，又会变得笨重、迟缓。

因此，训练基础 dexterity 时，更有效的办法是让人直接佩戴机器人的传感器，并尽量不妨碍自然动作。比这更重要的是 1X 坚持了十年的押注：只要机器人足够接近人类，就能用互联网上人类活动的视频训练它。我们已看到这条路线出现很强的 scaling law 迹象，这也是建立 1X World Model Lab 的原因。

**Jason Calacanis：**

你们怎样规模化构建 world model？是让工厂员工戴眼镜和手套反复操作，还是雇数据公司采集独有数据？

**Bernt Børnich：**

这些都会做，但真正关键的是理解 data pyramid。最顶端是 teleoperation data。它直接来自机器人，质量最高，但规模最小。操作员会尝试又快又好地完成任务，也会失败并重来，我们只挑出达到人类水平的优质样本用于模型 alignment。这种数据不需要特别多。

下一层是人类佩戴与机器人相同传感器采集的数据。它不是机器人本体动作，但非常接近，而且更容易扩展。再下一层是人类第一视角的 egocentric video。它离机器人又远一步，不过 NEO 的手与人手高度相似，因此仍然有用。最底层是互联网上的一般视频，也就是整个世界和人类活动的视频。

一般视频的规模比其他层级大得近乎荒谬。YouTube 和其他视频库包含海量人类行为。要达到真正 intelligence，所需数据可能比未来几年所有公司能采集的 egocentric 或传感器数据高出多个数量级。AI 历史上的重大突破，往往来自某家公司找到办法使用一种此前无法利用的巨大新数据源。我们押注一般视频就是机器人领域的这类数据源。

这里的数量级差异很关键。行业当然可以投入更多人，在工厂、家庭和实验室里戴传感器采集高质量动作，但这种生产速度仍然受人力和设备约束。公开视频已经记录了人怎样拿取、移动、打开、倒入、清洁和装配无数物体。问题不是数据是否存在，而是机器人形态与人相差太远时，模型无法把这些动作可靠迁移过去。NEO 的人形比例、手部结构和观察视角，都是为了缩小这段 distribution gap，而不仅是为了让产品看起来像人。

为了利用它，机器人每个细节都要尽量接近人类。人的皮肤、组织、摩擦、受力后的非线性形变、接触桌面时的冲击能量都会影响动作。人的手掌和臂展也各不相同。1X 与其他机器人公司的核心差异，就是我们全力用互联网视频预训练自己的模型，而且所谓 cross-embodiment 不是从另一台机器人迁移，而是从人类迁移。

长期看，最好的数据终究会是机器人自己的数据，因为它同时包含 action、tactile 和 force。但要先有一个足够好的 base model，让机器人能够部署到社会中，为客户完成愿意付费的任务，才会自然产生海量高质量机器人数据。用人类视频预训练，是破解这个 catch-22 的起点。

**Jason Calacanis：**

什么时候机器人会进入递归式进步？今天的 AI agent 已经能围绕销售、客服、定价等目标互相协作。未来是否可以只告诉餐厅机器人“持续做出让顾客愉悦的 Michelin 水准食物”，让它自己练习如何把水波蛋做得更好，并最终自己造机器人、数据中心和芯片工厂？

**Bernt Børnich：**

这不是纯粹科幻，而是我们认真思考的问题，只是时间很难预测。进步速度越来越快。一年前的我会比现在悲观得多，因为每次重新观察，AI 的进展都快于我的预期。

我非常确信，距离 hard takeoff 不到十年。这里的 hard takeoff 是指机器人能够制造机器人、建设 data center 和 chip fab、完成采矿与精炼，形成真正自给自足的劳动供给系统。我现在的主观押注是三年，但即使花十年，从人类历史尺度看也只是瞬间。

纯数字 intelligence 无法创造自己的物理 substrate，必须有 physical AI。它也会极大推进科学。我们平台已经收到很多自动化实验室工作的需求。若 AI 不能亲自搭建设备、执行实验并观察结果，它就很难独立推进科学。准确年份不确定，但我认为这是几年而不是几十年的事情。

**Jason Calacanis：**

如果你判断三年，悲观上限是十年，那么五到七年已经足够惊人。用户怎样订购 NEO？

**Bernt Børnich：**

直接去我们的网站下单。2026 年购买机器人应该像在线购买 Tesla 一样简单，价格也应透明。

节目中段由 Plaud 赞助。对依赖会议、尽调电话、董事会讨论和客户访谈的人来说，准确措辞和数字很重要。Plaud 把对话转成可搜索的信息，让用户不必反复滚动录音或依赖记忆。

### Boston Dynamics：从炫技实验室转向真实部署与两年内 ROI

**Jason Calacanis：**

我们很幸运请到 Amanda McMaster。你现在是 Boston Dynamics 的 interim CEO。Boston Dynamics 是现代机器人行业的 OG，几十年来人们一直在看你们的机器人后空翻、做动作、被推倒后重新站起。公司所有权也几经变化：先是独立和 venture-backed，后来被 Google 的 Sergey Brin 与 Larry Page 收购，又卖给 SoftBank，今天由 Hyundai 控股。这个历史是否准确？

**Amanda McMaster：**

准确。现在公司已经不再只是 AI lab experiment，也不再是一家只做 R&D 的公司。我们的重点是把机器人部署到真实世界。Spot 是最先商业化的产品，它是一台用于工业环境的 autonomous quadruped，也就是大家熟悉的四足机器人。

**Jason Calacanis：**

Spot 也启发了《Black Mirror》里追人的机器狗。当然那是 dystopian 版本，你们追求的是有益应用。Spot 实际部署到了什么规模？

**Amanda McMaster：**

它已经在真实客户现场创造价值。现在有超过 500 家客户，分布在 46 个以上国家。按实际部署和使用量看，Spot 是目前全球使用最广泛的移动自主机器人之一。

**Jason Calacanis：**

为什么？客户最常把它用于 security，还是 industrial inspection？

**Amanda McMaster：**

工业巡检是最重要的价值来源。客户让 Spot 做 acoustic inspection、仪表读数、vibration detection 等任务。若工厂里有昂贵资产，就可以让机器人持续监控。白天它做设备巡检，晚上还可承担 perimeter security。

真正的拐点是客户能否看到 ROI。它当然会跳舞，外形也容易让人喜欢，但商业阶段早已不再由舞蹈演示驱动。我们要求客户通常能在两年以内看到投资回报。

**Jason Calacanis：**

过去这些巡检即使被规定要做，也主要靠人。人会漏检、会犯错，且难以持续采集一致数据。Spot 可以带 video、acoustic、vibration、radar 等多种传感器，在水处理厂、桥梁、管线和其他基础设施里不停巡查。

机器人硬件售价和商业模式是什么？客户买硬件、租用软件大脑，还是按小时付费？

**Amanda McMaster：**

Spot 最初采用 capex 模式，因为工业客户习惯把它当成工业工具购买。价格取决于配置：base robot 大约 10 万美元，若加上完整传感器、服务、系统集成和现场部署，一年总投入可到 30 万美元。可以理解成从 Tesla 到 Ferrari 的价格跨度。

Atlas 可能更多采用 Robot-as-a-Service。Humanoid 客户在不同阶段可能需要迅速增加或减少机器人数量，RaaS 能降低进入门槛并提供弹性。

**Jason Calacanis：**

工业机器人寿命应该超过五年。如果它每天能工作 20 至 22 小时，只在充电时休息，按小时摊销其实很低。

**Amanda McMaster：**

我们用 mean time between intervention 衡量可靠性。Spot 已经超过 3,000 小时，也就是说一年通常只需要人介入几次。单块电池续航约 90 分钟，机器人会自动坐到 charging station 上充电。现场也可以配两台，让一台充电时另一台继续任务。

Atlas 则设计了自己更换电池的能力。它有两块电池，躯干旋转后可以替换其中一块，同时保留另一块供电，因此续航不会成为同样的约束。

**Jason Calacanis：**

按这个利用率，运营成本可能只有每小时几美元。相对而言，负责管线巡检的 union worker 加上福利、养老金后的完全成本可能是每小时 40、50 或 60 美元。机器人是否已经明显改变客户对 use case 的判断？

**Amanda McMaster：**

我们不把 Spot 的主要叙事设为 labor replacement，尽管客户计算 ROI 时可能会看这项指标。更重要的是，有些巡检任务虽然名义上分配给人，实际上没有稳定完成。机器人可以让员工转向需要判断和专业知识的工作，而不是重复走动和抄读数。

更好的价值衡量方式是避免多少损失。Spot 曾发现工厂里的空气泄漏，而那类故障若持续可能造成每天 300 万美元损失。客户真正关心的是机器人帮助避免了多少停机和事故，而不是简单少雇了几个人。

**Jason Calacanis：**

行业现在谈 labor replacement 是否仍然敏感？

**Amanda McMaster：**

必须承认劳动替代会是评估机器人的一个维度，因为人类岗位数量让 total addressable market 很容易估算。但它不应成为唯一讨论。机器人最先应消除的是危险、压迫性和损害身体的工作，也就是行业常说的 dull、dirty、dangerous。每个人只有一个身体，不应把它耗费在可以安全自动化的任务上。

**Jason Calacanis：**

Atlas 的 onboard compute 和 cloud compute 怎样分工？若机器人所在设施有高速连接，能否把耗电的大模型移到云端？

**Amanda McMaster：**

可以把系统理解为有两个大脑。第一个大脑负责机器人的 physicality，也就是 Boston Dynamics 最擅长的动态移动、平衡、可靠操控以及和真实世界接触的低延迟控制。这部分必须在机器人端运行。

第二个是 reasoning layer，让机器人获得环境的 semantic understanding。这部分可以在云端，可以由我们自己建设，也可能与 Google DeepMind 或其他 AI 合作伙伴共同提供。

外面还要再包一层客户专属知识，包括某家工厂的 workflow、任务流程、工具摆放方式，以及机器人该怎样接入既有系统。这一层可能在本地，也可能在云端，要根据安全、延迟和客户要求决定。

**Jason Calacanis：**

机器人有多少在美国制造，或至少不依赖中国与台湾？

**Amanda McMaster：**

我们的机器人是 100% 在美国体系内制造的。机器人主权是严肃问题。美国市场正在出现大量廉价中国机器人，但我认为不应该允许不可信的中国 humanoid 进入美国关键环境，因为这不安全。我们已经听到某些中国四足机器人把数据通过 back channel 传回中国的案例。

美国在 semiconductor 领域已经看到了失去产业控制力的后果，不能在机器人上重演。国家需要保护 IP，把制造生态放在美国或可信盟友，并建立 coordinated national robotics strategy。Boston Dynamics 已参与一些政策讨论，希望更多美国公司一起承担这项任务。

**Jason Calacanis：**

这不只是美国自己要赢，还要让其他国家选择美国平台，而不是中国平台。无人机已经改变 Ukraine 和 Middle East 战场。Spot 与 Atlas 在 military 场景是什么立场？

**Amanda McMaster：**

Boston Dynamics 一直公开坚持 anti-weaponization。就当前业务而言，武器化也会分散公司对工业 use case 的注意力。作为临时 CEO，我的职责是让团队聚焦于公司最有把握取胜并创造收入的市场。

这并不意味着拒绝所有政府项目。我们与政府保持合作，也开展非武器化任务。例如 EOD，也就是 explosive ordnance disposal，是机器人非常合理的用途；机器人可以处理爆炸物、把 medical kit 送进危险区域，或在不让士兵冒险的情况下执行侦察和救援。

**Jason Calacanis：**

但中国已经展示给自家四足机器人安装 AK-47。若对手部署，Boston Dynamics 是否最终必须为美国做同类产品？

**Amanda McMaster：**

这是很艰难的问题，希望永远不必回答。看到武装机器人确实令人恐惧。我知道 Boston Dynamics 拥有世界上能力最强的机器人之一。如果未来真的到了必须作出选择的时候，我们会作出正确决定。但今天还没有到那一步，因此我会继续让团队专注于能创造客户价值和收入的应用。

**Jason Calacanis：**

我半开玩笑地说，CIA、FBI 和 Department of War 很可能已经有人给各种机器人装了武器，只是不会公开告诉我们。无论如何，Boston Dynamics 是一家非常重要的美国公司。

你们目前总部仍在 Boston 附近的 Waltham。考虑到 Bay Area 聚集了大量 AI 和机器人人才，会不会在西海岸设点？

**Amanda McMaster：**

我们位于 Waltham，也接受部分 remote work，并正在考虑扩展到 West Coast。人才在哪里，公司就要认真评估在哪里建立团队。

### Agility Robotics：Digit V5、安全认证与 humanoid 的真实经济性

**Jason Calacanis：**

最后一位嘉宾是 Professor Jonathan Hurst，Agility Robotics 联合创始人兼 Chief Robot Officer。你 2008 年取得机器人学博士学位，在这个领域做了超过 20 年。过去 36 个月明显升温。你怎样比较最近两年与此前二十年？

**Jonathan Hurst：**

二十年前做机器人时，industry 里对这类方向还很陌生。工业界谈 robotics 更多是固定 automation system；humanoid、autonomous mobile robot 和通用 intelligence 主要属于大学研究。研究者一边做智能，一边做能承载智能的硬件。

现在这些能力终于开始进入真实世界并产生直接影响，不再只是论文主题。大学也看到需求，越来越多学生愿意学机器人，相关项目快速增长。整个领域进入指数式扩张阶段。

**Jason Calacanis：**

Humanoid 和 AI 都经历过多次 false start，也有过 AI winter。这一次为什么不同？为什么未来二三十年，机器人数量甚至可能接近人类数量？

**Jonathan Hurst：**

做一台“看起来像人”的机器人很容易，所以过去一百年一直有人展示 humanoid。真正困难的是，让机器人在为人设计的空间里完成有用任务。今天我们开始看到后者，这就是本轮周期与过去不同的地方。

机器人不一定必须在外形上完全像人，只要具备一定 humanoid 结构，并能完成有经济价值的工作，就会形成真实影响。更重要的是，人们现在能看见 generality 的路径。AI 让机器人获得更广泛的 context awareness，市场因此相信它很快能完成越来越多种任务。

**Jason Calacanis：**

Large language model 似乎免费解决了很多感知问题。机器人看一张桌子，已经知道上面有 phone、paper、tea 和 water，甚至可能估计容器容量。三四年前，工程师得为每种物体单独编程。

**Jonathan Hurst：**

Perception 过去极难，如今接近被普遍能力覆盖，这是巨大拐点。但不要因此认为机器人控制也已经免费获得。LLM 像 internet 一样成为所有公司都能使用的基础设施，是抬高全行业水位的工具。可互联网上并不存在“在某种传感器输入下，每个电机应该输出多少 torque command”的海量训练集。

要控制机器人，仍要自己创造数据。方法包括 learning from demonstration、teleoperation、animation、motion capture 等。但这些方法有硬上限。人远程控制机器人时，往往无法发挥机器人的最优能力，动作只是人类操作方式的映射。机器人必须通过自己的练习找到最适合自身硬件的行为，这就进入 world model、simulation 和 sim-to-real transfer 的问题。

**Jason Calacanis：**

多家公司正在让人戴手套或远程控制机器人，示范切菜、做沙拉和倒水。World model 能彻底解决控制问题吗？

**Jonathan Hurst：**

World model 是解决方案的一部分，但不是 silver bullet。你可以在模型里重建整座 warehouse 和其中物体的 physics，让数百万个机器人副本在几天内反复练习，而不必在现实中摔坏餐具或伤人。

但 sim-to-real gap 一直存在。仿真不可能完美模拟玻璃里的液体波动、杯壁 condensation、接触摩擦和机器人每个关节的真实 dynamics。最终仍需要大量真实世界练习。行业会同时使用 simulation、world model、human demonstration、teleoperation 和现场数据，不会由某一个方法独自完成跨越。

**Jason Calacanis：**

是否会出现类似 chess 或 Go 的时刻，把机器人放在厨房里，让它持续试错，自动进入递归学习？还是必须由 world model 公司和人类在 Michelin 厨房里精细共同训练？

**Jonathan Hurst：**

答案仍然是所有工具一起用。可能不够戏剧化，但我不认为会突然出现单一 singularity。更像雪球沿山坡向下，随着资金、工程时间和更多人才投入，能力越来越快地积累。

Simulation 可以让机器人低成本探索失败动作，human demonstration 可以迅速给出可行解附近的样本，teleoperation 可以在真实任务中接管并留下纠错数据，而现场自主运行会暴露仿真里没有的长尾问题。World model 把这些信息组织成可预测环境，但机器人仍要面对现实材料、光照、摩擦和负载变化。能力增长来自这些数据源和训练方法互相强化，不是某个实验室按下一个按钮。

人类经过进化，非常擅长从少量示范学习，再通过练习改善。机器人目前需要远多于人的数据和样本，我们还没有完全学会怎样“教机器人学习”。不过机器人也有独特优势：它们有 Wi-Fi。一个人学会拉 violin，不能把技能直接上传给另一个人；一台机器人学会后，同型号机器人都可获得这份能力，其他硬件只需做适配。

**Jason Calacanis：**

Agility 的产品是 Digit。当前大约是第四代，Digit V5 将在今年晚些时候发布。你们已经有数十台在真实现场工作。今天 forward deployment 是什么样，未来一两年又会怎样？

**Jonathan Hurst：**

当前任务仍是边界较清晰的 multipurpose workflow，例如拿起 bin 或 tote 并搬运。之所以需要 humanoid，是因为大物体需要两条手臂，狭窄空间里把箱子举到高货架上，还需要全身协调与动态平衡。这个 use case 足以证明 humanoid 形态有价值。

但 humanoid 的真正价值是 versatility。接下来会把能力扩展到 each picking，也就是逐件拣选；装满一个箱子后搬走；以及 palletizing、depalletizing 等更多流程。能在同一环境里不断增加任务，经济性才会迅速提高。

Digit V5 的关键不是做出新的炫技动作，而是安全。它将是第一批能够保持动态平衡、离开封闭 work cell，并且不需要在人与机器人之间设置实体隔离栏的 humanoid。机器人可以和人处在同一个 warehouse 空间，这才是 Agility 的 scaling moment。

**Jason Calacanis：**

外行可能低估这个变化。在 Tesla 或 Toyota 工厂参观时，自动化区域地面都有不能越过的线。人一越线，整条生产线会停下，代价可能达到上百万美元。现在行业是否终于有信心让机器人在人旁边工作，而不担心它跌倒砸伤人？

**Jonathan Hurst：**

这不是突然有信心，而是过去两三年非常刻意的系统工程。我们早期与 Amazon 部署时，机器人能完成任务，R&D 目标已经达到，于是我们说可以扩大部署。Amazon 的回答是“不行，它还不满足安全要求”。

随后团队从底层到顶层重新设计机器。要让一个动态平衡的 humanoid 在没有隔离栏的情况下通过工业安全要求，几乎每个 subsystem 都必须调整。安全不是在软件上加一个开关，而是对整机机械、电气、控制和故障模式作 holistic design。

**Jason Calacanis：**

工业级 humanoid 的 bill of materials 是否是数万美元？

**Jonathan Hurst：**

我们不公布具体 BOM，但成本确实在持续下降。规模化后，机器人售价会接近汽车。更重要的问题是它能创造多少价值。若一台机器人每天工作 20 小时、寿命五年，累计生产时间非常大。

Digit V5 依靠更快充电和新一代电池，目标是在 24 小时里工作约 20 小时。按一年约 8,000 小时、五年约 40,000 小时计算，即使机器人初期价格不低，单位小时成本也会迅速下降。

这项计算也解释了为什么不能只看机器人的采购价。工业客户购买的是多年可用的生产能力。如果设备大部分时间能自主工作，只在极少数故障或维护时需要人介入，那么资本成本会被数万小时摊薄。反过来，若机器人频繁跌倒、停机、等待人工复位，即使 BOM 很低，也没有商业价值。可靠性、充电速度、任务切换能力和现场安全共同决定真实 cost per productive hour。

**Jason Calacanis：**

市场普遍预期大规模时单台成本会降到 2 万、3 万或 4 万美元。若按 4 万美元、五年 4 万小时粗算，硬件摊销接近每小时 1 美元。西方工厂工人的完全成本可能每小时 20、30 或 40 美元，其他国家也可能在 10 美元左右，理论上会出现约 90% 成本压缩。当然，真正达到这个成本要先部署到十万台规模。

Agility 会按机器人工作小时收费，还是出售设备？

**Jonathan Hurst：**

两种模式都有。偏好 capex 的客户可以买机器人；希望降低风险和进入门槛的客户可以使用 Robot-as-a-Service。我们暂不公布具体每小时价格。

随着能力增加，机器人创造的价值会提高，同时制造成本下降。机器人服务价格在很长时间内仍由可替代的人类劳动成本锚定，因此定价相对缺乏弹性。制造成本与客户愿意支付的劳动价值之间存在足够空间，让客户节约成本，也让机器人公司建立可持续业务。

**Jason Calacanis：**

什么时候 Amazon、Target 这类公司的工厂里，机器人会超过 51% 的工人？

**Jonathan Hurst：**

在很多流程里，机器人其实已经占多数。工厂已有大量 AMR、conveyor belt 和 industrial robot arm，而且数量继续增长。Humanoid 只是自动化的新形态，会进一步提高 productivity。

美国人口并没有快速增长，GDP 要增长就要靠效率和能力提高。Automation 是其中的重要方式。但完全 lights-out 的新建工厂未必最需要 humanoid。若 autonomous truck 到达一座 24/7 运转、结构固定的全自动分拣中心，再由另一辆 autonomous truck 离开，专用自动化设备通常效率更高。

Humanoid 的优势是走进原本为人设计的环境，执行原本为人设计的 workflow。在一座新工厂完全自动化时，世界上还有大量 legacy factory 需要在现有布局里逐步增加自动化。Retail、grocery store、hospital、construction site 和把包裹送到居民门口，也长期是人类环境，更适合 humanoid。

**Jason Calacanis：**

未来完全可能是一辆 Waymo 式 robotaxi 或 autonomous delivery vehicle 到达住宅，一台机器人下车，把包裹送到门口。Agility 做过这类测试吗？

**Jonathan Hurst：**

这是我们最早与 Ford 探索的 use case 之一。网上还能找到视频：第一代 Digit 从车里下来，走过台阶，把包裹放到门廊。大约七年前就能演示。

但“能做”不等于“最好的第一市场”。在成本、安全和部署复杂度上，仓储搬运更适合先规模化。Last-mile delivery 仍在 roadmap 上，只是不会抢在当前工业市场之前。

**Jason Calacanis：**

有哪些外界觉得不明显、但能对世界产生很大正面影响的机器人应用？

**Jonathan Hurst：**

很难判断什么算“不明显”。单是把东西从一个地方拿起、放到另一个地方，就是巨大的 use case。这能让人摆脱机器人行业经典的 3D 工作：dull、dirty、dangerous。

我希望未来孩子们回看今天，会像我们看 1900 年煤矿工人的劳动条件一样，说“难以相信人曾经这样工作”。今天许多职业是 1900 年的人无法想象的，生活质量也高得多。机器人带来的生产力提升，应当让未来工作变得更安全、更有价值。

**Jason Calacanis：**

你仍然教授机器人学，研究生项目已有上百人。对担心职业前景的年轻人来说，这是不是很好的方向？

**Jonathan Hurst：**

是巨大的机会。技术快速变化时，刚毕业的学生反而有优势。工作二三十年的人熟悉过去的做法，需要重新学习；学生可以直接掌握新范式。没人能准确预测十年后的职业名称，但 engineering 的核心能力会长期适用。

机器人行业也不只有 PhD 和 master's 路径。它会需要大量更接近 electrician、HVAC technician、carpenter 或 contractor 的技能型岗位。当前机器人还不能完全自己组装自己，所以 manufacturing、assembly、field deployment、robot operation 和 maintenance 都需要人。随着部署扩大，维护机器人会形成很大的技术工人市场。

**Jason Calacanis：**

半认真问一个 Star Wars 问题。General Grievous 可以同时挥舞多把 lightsaber，为什么 humanoid 不做成四条或六条手臂，朝不同方向工作？

**Jonathan Hurst：**

设计机器人要从 first principles 出发，寻找完成任务的最简单结构。一条手臂只能拿较小物体，两条手臂就能搬大物体，所以从一条增加到两条的效用很明确。第三条手臂能增加多少额外 utility，却不一定足以覆盖机械、控制和安全复杂度。增加到四条、五条或六条手臂，需要协调的系统急剧增加。未来也许有合理场景，但必须由真实需求驱动，而不是因为看起来酷。

**Jason Calacanis：**

科幻作品里最喜欢哪台机器人？

**Jonathan Hurst：**

可能是 WALL-E 和 EVE。我喜欢那种机器人不断建设、创造，并坚持完成设计目标的愿景。Baymax 也很好，它的存在目的非常明确，就是帮助人。

Baymax 的故事也提醒我们，软件 safeguards 非常重要。删除或改变记忆和控制逻辑后，一台原本有益的机器人也可能变得危险。真实工业机器人必须通过系统安全流程，具备 supervisory circuit、emergency stop 和其他独立保护层，使单点软件故障不能伤害人。这可以理解成现实工程版的 prime directives。

**Jason Calacanis：**

Agility Robotics 正在招聘。公司有哪些地点？

**Jonathan Hurst：**

我们在 Oregon 的 Salem 起步，现在仍有团队；正在 California 的 Fremont 建设新设施，那里会集中做 robot behavior development，机器人全天运行，工程师可以直接在现场改进；我们在 Pittsburgh 也有团队，靠近 Carnegie Mellon。三个地点都是机器人领域很好的中心。

**Jason Calacanis：**

对年轻人来说，robotics 是值得投入的方向。要看技术将往哪里走，而不是只看今天的岗位。感谢你分享这些经验。

**Jonathan Hurst：**

谢谢邀请。
