---
访谈时间: 2026-08-04
访谈时间说明: "官方 Podcast RSS 与 YouTube 同日发布，无法确认独立录制日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: 2026-08-04T02:00:07Z
嘉宾名字: "Vladimir Novakovski"
嘉宾公司名称: "Lighter"
参与嘉宾:
  - 姓名: "Vladimir Novakovski"
    公司或机构: "Lighter"
    职务: "联合创始人兼首席执行官"
  - 姓名: "未知（The Rollup 主持人）"
    公司或机构: "The Rollup"
    职务: "主持人；原始字幕未明确姓名"
播客名称: "The Rollup"
播客url地址: "https://www.youtube.com/watch?v=3EqhnsaSVaw"
youtube_video_id: "3EqhnsaSVaw"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳并结合完整上下文转写为简体中文"
原始字幕缓存: "/Users/wesley/.codex/automations/youtube/caption_cache/3EqhnsaSVaw.en-orig.source.txt"
原始语言: "English"
全文提及的关键名词:
  - "Lighter"
  - "LIT token"
  - "perpetual futures"
  - "Ethereum"
  - "Robinhood Chain"
  - "Robinhood"
  - "Telegram Wallet"
  - "zero-knowledge proof"
  - "Lighter Core"
  - "Lighter VM"
  - "Ethereum L2"
  - "market maker"
  - "global liquidity layer"
  - "KYC"
  - "KYB"
  - "CFTC"
  - "CLARITY Act"
  - "tokenized stock"
  - "pre-IPO stock"
  - "options"
  - "quarterly buyback"
  - "token burn"
  - "revenue sharing"
  - "SK Hynix"
  - "Anthropic"
  - "OpenAI"
  - "SpaceX"
  - "Cognition"
  - "AI agent"
  - "TWAP"
  - "RFQ"
  - "Citadel"
companies:
  - Lighter
  - HOOD
  - Citadel
  - Cognition
  - Anthropic
industries:
  - 加密
  - 金融
  - 商业航天
technologies:
  - 以太坊
  - LLM
  - Agent
  - 零知识证明
keywords:
  - IPO
  - 合规
  - 监管
tags:
  - Lighter
  - HOOD
  - Citadel
  - Cognition
  - Anthropic
  - 加密
  - 金融
  - 商业航天
  - 以太坊
  - LLM
  - Agent
  - 零知识证明
  - IPO
  - 合规
  - 监管
---

# Vladimir Novakovski: Why Robinhood Chain And Lighter Both Bet On Ethereum (Composability Thesis)

## Transcript

### 开场

**Vladimir Novakovski：**

Lighter 的重点，是为流动性最高的 token 建立最高效的交易方式。四五年前谈这些概念，人们还会问 blockchain 到底是什么、token 又是什么。行业里有些群体很强调阵营，但过去也确实出现过很多不良参与者。

Lighter 建在 Ethereum 之上，并向链上提交证明。我们每天处理数亿笔订单，对应数十亿美元交易量。我是 Vlad，Lighter 联合创始人兼首席执行官。

**The Rollup 主持人：**

在正式开始前提醒一下，超过 70% 的观众还没有订阅。我们每周采访金融行业的重要创业者和投资者，最直接的支持方式就是点赞并订阅频道。

欢迎回到 The Rollup。今天再次来到 Tokenization Tower，与 Lighter 首席执行官 Vladimir Novakovski 交流。Vlad，欢迎回来。

**Vladimir Novakovski：**

很高兴再次来到这里。

### Robinhood 伦敦发布会与首次现场交易

**The Rollup 主持人：**

你刚从伦敦回来，参加 Robinhood 的 “The World Is Flat”活动。Robinhood Chain 开局很快，Lighter 的 perpetual DEX 也已接入 Robinhood Wallet。发布会和正式宣布合作的过程怎么样？

**Vladimir Novakovski：**

另一位 Vlad，也就是 Vlad Tenev，在舞台表现方面比我更有戏剧天赋。那是一场主题很独特、也很有趣的活动。有社区成员在会后开玩笑说：“伦敦之死被大大夸张了。”实际上伦敦依然很有活力。

发布会上有一次 perpetual trade 的现场演示。Vlad Tenev 对观众说：“看看这个速度。”我们的工程师当然很高兴。更有意思的是，那次演示实际上是系统完成的第一笔交易。就在演示前约 30 分钟，系统还没有完全正常运行。Lighter 和 Robinhood 的团队冒险把它直接放到现场，最终成功了。

**The Rollup 主持人：**

过去几周到几个月，Lighter 在 token、市场认知和平台使用方面都明显增长。你们还调整了平台延迟和速度，并增加了新交易标的。最近两三周最重要的更新和当前核心重点是什么？

### 3000 台 Mac mini 为全部操作生成证明

**Vladimir Novakovski：**

基础设施方面一直在做持续改进。我们最近发布了一份技术深度说明，解释整个技术栈如何运行。

Lighter 使用约 3000 台分布在美国各地的 Mac mini 来生成证明，验证平台上的每一项操作都被正确、公平地处理。证明范围不只包括最终成交，还包括每一笔订单、撤单和强制平仓。也就是说，这些机器此刻仍在为平台发生的操作生成 zero-knowledge proof（零知识证明）。

我们也公开了对延迟、成本和新实例运行方式的设计。Robinhood Chain 上的新实例开局数据很好，整个 Robinhood Chain 的发布也很成功。

接下来最大的项目是 options。它会打开很多新机会，例如 pre-IPO stocks options（未上市公司股票期权）。即使相关公司的实际股票还不能自由交易，也不意味着其期权不能被交易。Lighter 已经提供部分未上市公司 perpetual products，未来机构或许还能交易 tokenized option，而不必直接持有尚未上市的股票。

**The Rollup 主持人：**

这比单纯增加一个交易品种更重要。perpetual 允许市场对未上市公司的方向定价，而 option 进一步提供期限、波动率和非线性收益。传统机构可能因为合规或转让限制无法买卖真实 pre-IPO shares，但仍有可能在受支持的环境中交易 tokenized option，用来表达观点或管理风险。

**Vladimir Novakovski：**

对，这正是我们正在开发的方向。它需要同时解决定价、流动性、结算和监管问题，所以伦敦接触的合作伙伴会分别参与技术栈的不同部分。

我们在伦敦见到了很多有兴趣参与这一技术栈不同环节的潜在合作伙伴，目前正在全速推进。

### 为什么 Robinhood 使用独立 Lighter 实例

**The Rollup 主持人：**

perpetual 平台正逐渐进入受监管环境。Lighter 在 Robinhood Chain 上运行的是一个独立实例，而 Lighter Core 会继续存在。未来是否还会出现要求 KYC、AML、面向机构的实例？不同实例会不会造成流动性碎片化？为什么独立实例是进入受监管市场的更好方法？

**Vladimir Novakovski：**

架构选择一定有取舍。我们最大的两个合作伙伴是 Robinhood 和 Telegram Wallet，但它们使用的方式并不相同。Telegram Wallet 直接使用 Lighter Core，Robinhood 则使用新的独立实例。我们还有很多不同类型的集成，相关信息可以在 Lithub，也就是名称类似 GitHub 的网站上看到。

Robinhood 选择独立实例很合理，因为它正在扩展自己的 chain，而且目前链上活动增长很快，是我见过最好的新链发布之一。如果 Robinhood Chain 没有获得使用量，唯一有吸引力的产品只是 perpetual，那么独立部署可能不划算。但在链本身快速增长的情况下，这个选择成立。

关键是，Robinhood Chain 和 Lighter Core 最终都建立在 Ethereum 之上，因此它们可以互操作。这一底层关系常被外界忽略。

zero-knowledge proof 让做市商可以在两个实例之间快速移动资本。目前跨实例调拨可以在几分钟内完成。随着 Lighter VM、与 Axiom 的合作，以及我们与 Ethereum Foundation 推动 L2 互操作性的工作，所需时间还会继续缩短。

对普通交易者来说，只要每个市场都有足够流动性，他并不需要关心流动性怎样到达。交易者可以在 Robinhood Chain 上交易 tokenized stock，也可以在 Lighter Core 上交易 gold perpetual。大型做市商会把这些市场视作一个全球订单簿，并在后台平衡头寸。

流动性是否碎片化，不是简单的“是或否”。真正的衡量标准，是资本在市场之间移动有多慢。如果资本几乎没有移动摩擦，独立实例仍然可以共享同一个更大的流动性基础。

**The Rollup 主持人：**

换句话说，ZK 架构的价值不是把所有用户强制放进同一个前端，而是让做市商在后台迅速把库存和保证金从一个实例调到另一个实例。交易者看到的是各自市场上的深度，做市商看到的则是一个可以统一管理的全球头寸。

**Vladimir Novakovski：**

没错。只要跨实例调拨时间足够短，做市商就不必在每个实例永久锁定一套彼此隔离的资本。我们现在把时间缩短到分钟级，下一步还要继续降低。

### 独立实例允许采用不同监管和杠杆参数

**Vladimir Novakovski：**

独立实例的优势，是可以针对不同资产、用户和监管要求采用不同参数。假设未来 Robinhood 的美国核心客户可以在应用内交易 perpetual，他们已经完成 KYC，这个受监管实例就可能拥有与 Lighter Core 不同的杠杆限制和风险参数。

即使 Lighter Core 和 Robinhood 都取得相关牌照，两者也不一定采用完全一样的参数。传统金融中，CME 与 ICE 的规则和参数同样不完全相同。我们要保留这种产品与监管灵活性，同时让底层基础设施继续互操作。

**The Rollup 主持人：**

那么，Lighter Core、Robinhood 当前实例和未来美国受监管实例之间，做市商都能互通吗？监管限制并不是技术限制。

**Vladimir Novakovski：**

监管限制主要影响不愿完成 KYC 或 KYB 的做市商。大型机构通常愿意完成这些程序，因此技术上没有额外障碍。像 Citadel 这样的机构可能只参加受监管实例，但有些做市商同时拥有岸上和离岸实体，可以参与多个实例，并在链上快速移动合规资本。

### 不会为没有强分发能力的平台随意复制实例

**The Rollup 主持人：**

这种模式会不会发展成半打甚至更多实例？

**Vladimir Novakovski：**

只有合作方拥有很强的 distribution（分发能力）时，独立实例才有意义。并没有成千上万个平台具备 Robinhood 这样的分发能力。这确实是对 Robinhood 增长能力的一次下注。

Telegram 同样拥有很强的分发能力，但对它来说，直接连接 Lighter Core 更合理。我们不会强迫所有伙伴采用一种模式，而会根据其产品、监管和用户结构决定。

各国规则也可能很特殊。例如，某个司法辖区可能要求股票交易者完成 KYC，却允许 perpetual 在另一套规则下交易。如果当地数字银行要向客户提供这两类产品，我们就要按当地约束实现规则，同时让它尽可能连接全球流动性。

### Lighter 同时是产品公司和基础设施公司

**The Rollup 主持人：**

从这个角度看，Lighter 不只是一个面向用户的 perpetual 交易前端，更像可以接入全球消费平台的流动性层。你们当然仍要维护 Lighter.xyz 的界面和核心交易体验，但更大的目标似乎是成为各种分发渠道背后的 perpetual 技术底座。

**Vladimir Novakovski：**

这是一个好问题。我们的背景来自传统金融和 Silicon Valley。技术上很早就理解 blockchain，但并不是在 crypto-native 社区中长大的，更像转学到新学校的孩子。

早期投资者大多来自 Silicon Valley，他们一直问：你们究竟是产品公司，还是基础设施公司？onchain 世界最吸引人的地方，是我们不必二选一，可以同时成为两者。这也是我们喜欢这个领域的原因。

### LIT 回购、销毁与社区沟通

**The Rollup 主持人：**

流动性层的增长最终会回到 LIT token。上次谈合作时，我们讨论过收入、增长和回购。此后你们在 X 上公开交易 hash，并销毁了一批 LIT。按当时价格计算，规模大约为 3000 万美元。

市场此前不确定被回购的 token 是否会重新流入市场、用途是什么。你们通过销毁给出了非常明确的回答。为什么这样做？你希望为 token 持有人建立什么标准？

**Vladimir Novakovski：**

我们从社区反馈中学到很多。核心经济设计没有改变，但沟通方式变得更清晰。

Lighter 从第一天起就是美国实体。我们不想为了表面上的“去中心化”搭建一堆没有实际必要的实体。传统金融体系在美国很强，onchain 体系也应该在这里发挥重要作用。

从美国实体的税务和成本基础角度看，销毁已经回购、成本基础不同的 token，比直接销毁 treasury wallet 中的另一批 token 更有效率。后者成本基础更高，更适合保留。但无论具体销毁哪一批，对所有 token 持有人的经济效果相同。

之前社区没有完全理解这一点。我们没有因为反馈改变销毁的经济目的，而是把执行和解释讲得更清楚。

回购已经程序化运行超过六个月，销毁以后也会程序化。第一次销毁覆盖了两个季度，此后计划按季度执行，例如第三季度结束后再次执行。未来几个季度或几年，商业模式可能调整，我们会向社区说明，但有一件事不会改变：所有价值都会归集到 token（value will all accrue to the token）。

**The Rollup 主持人：**

这也是市场要求交易 hash 的原因。口头承诺回购，并不能回答被买回的 token 是否会重新出售；公开链上执行并销毁，才让供应变化可检查。大约 3000 万美元只是按当时 token 价格计算的主持人估值，不等同于经审计财务报表中的回购金额。

**Vladimir Novakovski：**

链上系统的优势就是可以把执行公开出来。社区可以检查发生了什么，而不只依赖公司新闻稿。我们也会提前解释成本基础和 treasury 处理方式，减少大家把会计选择误解为经济利益改变的情况。

### “LIT token 就是股权”，不存在双重价值结构

**The Rollup 主持人：**

外界会问，Lighter 是美国公司，既然有公司股权，token 与股权是否形成双重结构？

**Vladimir Novakovski：**

公司股权确实存在，但它形成于 TGE 以前。对我们而言，TGE 是一次阶段转换。我们并不想既保留全部股权价值，又额外发行 token 获得第二套价值。

token 出现以后，我们告诉原有股权投资者：从现在开始，股权唯一的经济意义，是按照既定归属时间表代表其 token 持有量。如果投资者不接受，可以退出。上一轮股权融资获得约五倍超额认购，因此愿意承接退出份额的投资者很多。最终只有约 1% 的 cap table 选择退出，其余投资者用行动接受了价值归集到 token 的结构。

这套安排仍然是 Novakovski 对公司结构的陈述。本期节目没有展示公司章程、token 权利文件、清算顺位、投票权或监管意见，因此“token 就是股权”应按照管理层给出的经济设计理解，不能自动等同于传统证券账户中具有完整法定股东权利的普通股。

未来如果法规和基础设施成熟，新公司从成立第一天起就可以把股权 tokenized，不必先建立传统股权结构，再倒推兼容 token。

**The Rollup 主持人：**

再明确一次：Lighter 是在 Delaware 注册的 C Corporation，现有公司股权最终由流通 token 供应代表，不存在股权与 token 各自截留一部分价值的双重结构。也就是说，token 就是股权？

**Vladimir Novakovski：**

是的，正是这样。

### CLARITY Act 与链上收入分享

**The Rollup 主持人：**

CLARITY Act 的相关条款可能允许向 token 持有人分享收入，条件包括收入由链上业务程序化产生，分配参数由去中心化或 DAO 式投票治理。具体规则还有细节，但这可能让相应 token 不被认定为 security，对 Lighter 和整个行业都很重要。

**Vladimir Novakovski：**

可以进一步想象 tokenized stock 的未来。公司本身未必从事 blockchain 业务，但创办公司和资本形成可以默认使用 DeFi rails。

有些 token 本来就应该被视为 securities，但证券规则也需要更新。SEC 不只在判断哪些资产属于证券，也在重新考虑证券由谁持有、如何发行和流通。许多规则几十年没有现代化。未来的企业家应该可以直接在链上创建公司，而不必被 19 或 20 世纪形成的基础设施限制。

### 收入来源从 Bitcoin 行情中分散出来

**The Rollup 主持人：**

Robinhood 实例、RWA、SK Hynix、其他 pre-IPO perpetual，以及未来的 options，都可能扩展收入来源。我看到的一组数据是，Lighter 最近七日平均收入约每天 7 万美元，之后一度升至约每天 10 万美元；更早几个月约为每天 8 万美元。

crypto 牛市回来后收入当然可能提高，但现在的特点是，收入开始与 Bitcoin 价格分散，LIT 价格也不再完全跟随 Bitcoin。多元收入结构对 Lighter 有多重要？你对 2027 年收入有什么预期？

**Vladimir Novakovski：**

SK Hynix 是一个有意思的例子。Lighter 在 2 月就开始上线韩国股票 perpetual，是首批这样做的 DEX 之一。此后又增加了更多韩国股票和 pre-IPO 产品。

AI 行业正在发生很多事件，而用户现在可以交易这些事件。例如某家公司发布新模型，Anthropic 在 benchmark 上表现更好或更差，用户可以通过相关市场表达判断。

**The Rollup 主持人：**

几乎每一条 AI 新闻都成了 perpetual 交易量的催化剂。它未必提高其他 crypto 资产的投机需求，有时甚至分流 Bitcoin 的交易兴趣，但 AI IPO 或模型事件会直接带来 perpetual 成交量、平台收入和回购资金。

**Vladimir Novakovski：**

是的。AI IPO 热潮也吸收了大量风险资本。市场可能会经历三家规模极大的 IPO，其中一家已经发生，我指的是 SpaceX，另外两家尚未完成。等这些大型交易结束后，可能会有更多风险资本重新寻找 crypto-native assets。

不过，我们并不追求 revenue maxing，也就是不会为了每一分钱收入牺牲产品。Lighter 的目标是提供好产品和新市场。零售用户费用为零，非零售费用也低于几乎所有竞争对手。

现阶段重点是继续扩大使用量。收入和有机活动当然是健康信号。进入 2027 年以后，我们会随着合作伙伴开放新司法辖区和新客户群而增长，同时继续扩大 Lighter Core。

收入多元化的核心逻辑，是不只依赖 BTC perpetual 的成交量。当韩国股票、pre-IPO assets、AI 事件市场和未来 options 分别带来交易时，单一 crypto 行情降温不一定让全部收入同时消失。但这些市场的实际深度仍取决于客户需求和做市商是否愿意持续报价。

现在给出 2027 年具体收入数字还太早。但目前支付给证明生成系统的成本约占收入的 10%，因此商业模式的单位经济性很好。我们的核心仍是客户，而不是短期把费用抽到最高。

### 机构和零售是两条获客轨道，但共享做市基础设施

**The Rollup 主持人：**

市场也在讨论 Robinhood Chain 向 Ethereum 支付了多少 rent，以及 Ethereum 是否应该提高收费。先不展开这个问题。到 2026 年底，Lighter 如何分别规划机构和零售增长？CFTC 牌照、Robinhood Chain 实例和 Lighter Core 看起来像两条不同轨道。

**Vladimir Novakovski：**

对 maker 端来说，两条轨道其实高度一致。与某个做市商建立关系以后，可以继续邀请它进入新实例，提供资本迁移方式和 API。taker 端的客户获取则不同。

我们计划在 9 月底、10 月初去亚洲参加一系列会议，与 crypto-native 的早期核心客户交流。产品方面还在研究 RFQ、面向大户的新工具等。go-to-market 团队目前大致一半服务核心零售，一半服务合作伙伴。部分合作伙伴本身拥有世界级营销与分发能力，所以我们可以同时推进两条路线。

### 中国 AI 公司与可交易事件市场

**The Rollup 主持人：**

回到 pre-IPO 和事件驱动 perpetual。中国 AI 市场会不会成为 Lighter Core 的重要部分？DeepSeek 或其他中国 AI、存储公司未来可能上市。

**Vladimir Novakovski：**

毫无疑问会。具体到如何比较模型，我以前的联合创始人 Scott Wu 创办了 Cognition，也就是 Devin 的开发公司。Cognition 建立了一套较为中立的 benchmark，用于衡量不同 AI 模型的编程能力。

它已经比较 Anthropic 和 OpenAI，未来如果加入中国模型，就能观察这些模型处于什么位置。这类结果可能形成可交易的 alpha。至于本周、下周具体上线哪些公司，仍由客户需求和做市商能够提供的流动性决定。

### Citadel 经历教会他先考虑极端风险

**The Rollup 主持人：**

从创业者和 CEO 角度，你在 Citadel 和传统金融体系中学到的什么经验，会进入 Lighter 的每一个产品决策？

**Vladimir Novakovski：**

我的职业经历大致分为传统金融和 Silicon Valley 两段。传统金融教会我“应该造什么”，Silicon Valley 教会我“怎样把它造出来”，包括如何选团队、建立流程和寻找投资者。

在传统金融中亲历 2010 年 flash crash，让我形成了一套压力测试问题：某项技术能否挺过 flash crash？如果再次发生 2008 年危机，它会怎样处理？如果再出现一个 Madoff，它能否暴露问题？后来行业确实出现了另一个类似事件，也就是 SBF。

因此，Lighter 的 security-first 架构、对每笔订单和撤单生成证明，以及对极端行情的关注，不只是技术展示，而是来自传统金融风险事件的经验。

### 与 Vlad Tenev 的合作

**The Rollup 主持人：**

你与 Robinhood 的 Vlad Tenev 多久交流一次？你们会一起规划哪些策略？

**Vladimir Novakovski：**

我们的关系很好，但我不适合谈具体策略。Vlad Tenev 很像一位 Renaissance man。前一分钟可以讨论 tokenized stock 的内部机制，下一分钟就转向数学模型和用 formal verification 证明定理。他曾经是 Terence Tao 的研究生，而 Terence Tao 是世界上最优秀的数学家之一，所以我们的对话跨度很大。

### 下一步：options、AI agent 与程序化交易

**The Rollup 主持人：**

最近几周 Lighter 在产品、token、社区沟通和回购执行上都有进展。接下来最核心的优先事项是什么？

**Vladimir Novakovski：**

首先是更多 RWA 和 options。另一个出乎我们预料、很受欢迎的方向，是程序化交易策略，例如 TWAP 和 pair trading。

AI agent 也可能参与。未来用户可以直接用英文描述自己的市场 thesis，然后让 AI agent 根据这套判断执行交易，而不是手动把观点拆成一系列订单。

例如，用户可以描述两个资产之间的相对价值判断、触发条件和风险边界，让 agent 自动选择 pair trade、TWAP 或其他执行方式。这种体验把策略表达从编写 API 代码，降到自然语言层面。不过，节目只讨论了产品方向，没有说明 agent 如何限制仓位、处理错误推理或在极端行情中停止交易。

**The Rollup 主持人：**

市场也越来越多地讨论 private TWAP。Lighter 在这方面走到哪里？

**Vladimir Novakovski：**

从技术上看，private TWAP 与 ZK 技术栈很契合。但从客户需求排序看，它目前不是前两三项，更接近前十项，因此短期优先级不会超过用户明确要求的产品。

**The Rollup 主持人：**

Vlad，感谢你的时间。希望你在纽约过得愉快，今天天气确实很好。

**Vladimir Novakovski：**

谢谢，干杯。
