---
访谈时间: "2026-07-29"
访谈时间说明: "公开信息未披露实际录制时间，使用 YouTube 发布时间；官方 Podcast RSS 同日发布。"
嘉宾名字: "Paul Frambot"
嘉宾公司名称: "Morpho"
参与嘉宾:
  - 姓名: "Paul Frambot"
    公司或机构: "Morpho"
    职务: "联合创始人兼首席执行官"
  - 姓名: "David Hoffman"
    公司或机构: "Bankless"
    职务: "联合创始人兼主持人"
播客名称: "Bankless"
播客url地址: "https://www.youtube.com/watch?v=rU151J-rmbU"
youtube_video_id: "rU151J-rmbU"
YouTube发布时间: "2026-07-29T11:00:38Z"
字幕来源: "YouTube 原始公开自动字幕 en-orig，结合完整上下文转写为简体中文"
转写说明: "删除妨碍语义重组的字幕断行与时间戳，按上下文校正 Morpho Blue、Morpho Midnight、Aave、Uniswap、Hester Peirce、curator、obligation 等自动字幕误识别；保留 DeFi、TradFi、TVL、USDC、AMM、order book、zero-coupon obligation 等专有词。"
全文提及的关键名词:
  - Paul Frambot
  - David Hoffman
  - Morpho
  - Morpho Blue
  - Morpho Midnight
  - fixed-rate lending
  - fixed-term lending
  - zero-coupon obligation
  - interest-rate model
  - curator
  - vault
  - order book
  - DeFi
  - TradFi
  - USDC
  - stablecoin
  - undercollateralized lending
  - onchain identity
  - tokenized stocks
  - securities lending
  - Coinbase
  - Robinhood
  - Apollo
  - Apple
  - Uber
  - Airbnb
  - Starbucks
  - Uniswap
  - Aave
  - Compound
  - EtherDelta
  - Dharma
  - MetaMask
  - SEC
  - CFTC
  - Hester Peirce
  - net interest margin
  - capital efficiency
  - CLARITY Act
---

# Morpho Just Removed DeFi's Most Important Number

## Transcript

**David Hoffman：** Bankless Nation，Paul Frambot 再次来到节目。这次我们要讨论 Morpho 推出的新协议 Morpho Midnight，也会谈 Morpho 与 vault 生态最近的整体进展。Paul，欢迎回来。

**Paul Frambot：** 谢谢再次邀请我。

### Morpho Midnight 是什么

**David Hoffman：** Morpho Midnight 到底是什么？

**Paul Frambot：** 它基本上是 Morpho Blue 之后的下一代 Morpho。Morpho 提供借贷基础设施：一端让资金获得利息，另一端让借款人得到融资。使用 Morpho Blue 创建 lending market 时，可以选择 collateral asset、loan asset、oracle，再提供 variable-rate、open-term 的借贷体验。过去两年，这种结构使用方便，也很适合被动参与。

但我们与越来越多机构交流后发现，一个关键能力缺失了：对利率的控制。无论是通过 Robinhood、Coinbase 等大型应用借款的普通用户，还是大型机构，都希望知道自己究竟要支付多少。尤其对机构而言，rate 是风险定价的核心。TradFi 里几乎不会让利率依赖某条任意公式或 DAO governance，而 DeFi 目前恰恰常常如此。

综合消费者对可预测性的需求与机构对定价权的需求，我们越来越确定：DeFi 融资不能继续完全依赖所谓 interest-rate model。真正基础的结构应该回到 zero-coupon obligation。因此，Morpho Midnight 是一套 fixed-rate、fixed-term 的借贷基础设施，让任何人创建具有确定期限、由市场形成固定利率的 lending and borrowing market。

**David Hoffman：** 这像是把 TradFi 中普遍存在的基础设施搬到 Morpho。早期 DeFi 先创造了适合链上散户的形式，例如 AMM 和 Morpho Blue。普通用户不太在意利率是否稳定，愿意承受市场利率上下波动；机构却不接受。他们应该一直在对你们说：“请提供我们熟悉的产品形态。”

**Paul Frambot：** 早期 DeFi 有很多约束。gas 很贵，链上参与者主要是拿 MetaMask、资金不多、也不是金融专家的个人。协议不得不把大量复杂性内置进去，为用户提供被动体验，因为当时没有成熟中介可以替用户处理。

Uniswap v2 的 LP 和交易体验都相对被动；Compound、Aave 也替用户管理风险、利率和几乎一切参数。随着生态扩大，参与者越来越专业，他们希望获得更多控制。协议因而应该把部分职责模块化，交给市场参与者。市场通常能更好地定价，也会发现更多用例。

Uniswap v2 到 v3，逐渐把 liquidity management 外部化；到了 v4，直接在 smart-contract 层做 LP 或交易反而更复杂，因为 DeFi 已经形成多层结构，由 market makers、MEV bots 和不同 auctions 共同提高效率。借贷也经历同样变化。

这种“变得更难直接使用”并不代表底层退步，而是专业分工出现了。早期协议必须把每项选择都替用户做好，才能让市场启动；成熟市场则应把风险选择、价格判断和头寸管理交给最擅长的参与者，再由上层产品把复杂过程包装成普通用户可以使用的界面。底层越中立、上层越专业，市场能够容纳的需求反而越多。

Morpho Blue 比 Aave 更难直接使用，因为用户面对成千上万个 markets 和 vaults，所以需要 curators 帮助简化体验。Midnight 再前进一步：协议不仅不应该替市场管理风险，也不应该决定利率。DeFi 正在分层，这是好事。它会提高灵活性和市场效率，并把机构真正需要的控制权交给它们。

### 赞助信息

**旁白：** 过去近十年，我使用过许多 wallets、exchanges、aggregators 和 frontends，却一直在寻找同一种体验：一个界面连接多链深度流动性，可以私密行动，同时仍由自己控制资金。Near.com 允许用户通过一个账户跨链操作，并保持活动机密。NEAR 已用 post-quantum signing 处理超过 230 亿美元跨链资金，并保持五年以上运行。通过 Bankless 链接可返还 20% 交易费。本内容不构成投资建议。

市场不会一次只交易一种资产，资金会在 Bitcoin、Nvidia、gold 和 S&P 之间轮动，但很多交易者仍把不同资产分散在多个平台和资金池。Bitget Stocks 2.0 支持直接用 USDT 交易 tokenized equities，费用为 0.004%，并提供对 underlying stock 的 1:1 economic exposure；dividends、stock splits 等 corporate actions 会自动反映。本内容不构成投资建议。

### 为什么 fixed-rate、fixed-term 才是真正 primitive

**David Hoffman：** DeFi 早期一些 primitive 很优雅。EtherDelta 把 order book 搬上 Ethereum，却不适合当时的链。随后 Uniswap 用 `x*y=k` 把参数交给市场，这与区块链结构高度契合，也让像我这样通过 crypto 学金融的人很容易理解。

Morpho Midnight 的 market 包含 loan token、collateral asset、maturity date，以及 vault manager 可能采用的 permissions。它听起来没有那么“DeFi native”，反而像 TradFi 提出需求后，Morpho 为它们造了产品。fixed-rate、fixed-term lending 真的是金融必然收敛到的 primitive，还是传统金融自上而下设计出来的习惯？

**Paul Frambot：** 我对此有很强的判断：fixed-rate、fixed-term 是融资唯一真正的 primitive。

只要采用 variable rate，就必须回答“它根据什么变化”。无论答案是一条 utilization curve、治理决定还是其他函数，最终都有任意性，意味着它依赖外部规则，因而不是 primitive。真正 primitive 不应依赖另一个定价机制才能存在。

公式化浮动利率并非毫无用处，它在早期市场参与不足时，能用一套自动规则维持供需平衡，让用户无需持续挂单。但“适合启动市场”不等于“应成为永久底层”。当报价者、做市者和资产管理者已经足够多时，继续让公式垄断价格发现，反而会压制市场表达真实风险的能力。Midnight 的变化，是把临时替代品移开，让参与者重新拥有报价权。

fixed-rate、fixed-term market 的核心是 zero-coupon obligation。它是非常简单的对象，到期价值为 1，而当前交易价格相对 1 的折价就决定利率。这比把大量逻辑塞进 lending pool 更简单。过去无法直接采用这种结构，是因为协议必须替普通用户管理利率；当 curators 等中间层能够处理复杂性后，协议就没必要继续内置任意 rate model。

**David Hoffman：** EtherDelta 除了 UX 很差，另一个问题是参与者太少。Uniswap 的机制更适合当时链上的参与者规模。2017 年的 Dharma，以及更早的 EthLend，其实也尝试过 peer-to-peer、fixed-rate、fixed-term loan，却没有成功。原因是不是当时没有足够的市场参与者、专业程度和流动性？

**Paul Frambot：** 大体正确，我会分成三点。

第一，当时 gas 限制了复杂操作。第二，也是最重要的，市场缺乏 liquidity。这里的 liquidity 不只是钱，而是足够多不同角色共同做市，让参与者能进出市场而不显著改变价格。当时根本没有这种条件。Compound 提供简单、被动的体验，反而更符合一群拿着 MetaMask、不了解金融的用户。

今天情况不同。Apollo 等全球最大的 private-credit asset managers 已经接触并投入 Morpho 生态。这些是最复杂的 portfolio managers，它们不需要 DAO 替自己设定利率和风险。相反，我向全球大型 TradFi 机构介绍 DeFi 时，大约一半会说：“interest-rate model 是我们见过最荒谬的东西。”

站在资产管理者角度，它们要针对某一风险自行决定 rate 与 terms。DeFi 现有结构却让公式或 governance 替它们决定。它们认为 Aave 更像 asset manager：用户把钱放进去，由协议或治理选择风险画像。真正专业的资产管理者不愿依赖别人完成自己的核心工作。

借贷之所以比交易更晚走到这一步，是因为交易主要回答“什么价格成交”，借贷还必须同时回答违约概率、抵押品波动、清算路径、期限错配和流动性需求。风险是多维的，单一利用率曲线只能把复杂判断压缩成一个数字。对散户而言这是一种便利，对机构而言却等于失去管理职责中最重要的部分。

第三，Dharma 等早期设计本身也有很多问题。Midnight 解决了 liquidity fragmentation：同一笔流动性可以同时向成千上万个隔离市场提供可借额度。此类跨市场设计是能否从零到一的关键。

交易与借贷的演进速度也不同。trading 的维度较少，Uniswap 更早收敛到干净 primitive；lending 涉及多维风险，本来就需要更多管理层和更长演化过程。

### 一个 Midnight market 怎样组成

**David Hoffman：** 请从最底层解释一个 Morpho Midnight market 的构造，再谈多个 markets 怎样组合。

**Paul Frambot：** 它和 Morpho Blue 没有那么不同。你仍有 collateral asset、loan asset，以及为两者定价的 oracle。区别是，不再使用 interest-rate model，而是设置 term。Morpho Blue 里的 utilization curve 会根据供需公式决定利率；Midnight 把这一步外部化，让市场自己决定 rate。

Morpho 团队是 computer scientists，不是替用户作金融判断的人。我们希望尽可能从基础设施中移除金融决策。Midnight 首次真正做到这一点。

可以把每个 Midnight market 理解为可交易的 zero-coupon obligation。它不完全等同于 bond，但经济结构类似：obligation 距离 maturity 的交易价格决定利率。这就是核心 primitive。

Midnight 会有大量不同 obligations，普通用户不可能自己逐一管理，因此仍然需要 vault。vault 负责在多个 markets 之间分配资金。使用 Morpho Blue vault 时，curator 主要选择愿意承担的风险；使用 Midnight 时，还可以明确价格，例如愿意向 Bitcoin-backed loan market 出借，但年化低于 5% 就不成交。

curator 还能管理 liquidity。它可以接受锁定六个月以提高 capital utilization，也可以保留更多即时可提资金。普通用户看到的仍是类似 Morpho Blue 的 vault；后台则由 curator 买入、滚动和聚合各种 obligations。

也就是说，同一个金库可以先声明愿意承担哪些抵押风险，再声明每类风险最低可接受的收益率，最后决定为赎回保留多少现金。过去这些变量被协议公式混在一起，新的结构把它们拆开。专业管理者可以明确区分“信用判断”“价格判断”和“流动性管理”，而最终用户仍只需要选择一个符合自身目标的金库。

**David Hoffman：** 但 borrower 与 lender 的行为都变了，因为双方承诺固定期限。Midnight 必须重新启动这一段供需。

**Paul Frambot：** 对。最终用户大多仍想被动参与，Robinhood、Coinbase 用户不会自己管理成千上万条 obligation，所以 vault 会替他们滚动头寸。

启动策略的特殊之处在于，Morpho vaults 已经拥有数十亿美元资金。代码中有一个参数，打开后这些 vaults 就可以配置 Midnight。我们非常清楚这是重大决定，因此希望 launch 尽可能慢。market makers、lenders 和 borrowers 需要先熟悉代码、完成 API integration。过去半年 DeFi 经历了很多风险事件，我们不想仓促把巨量流动性导入新协议。

当市场足够成熟，治理可以允许 vaults 分配资金到 Midnight。那时引入十位数美元规模并不困难。Morpho Blue 与 Midnight 的组合，是 DeFi 独有的可组合性：一个新 fixed-rate primitive 可以直接连接旁边已经存在的大型 liquidity network。

团队故意不在第一天打开开关，是因为“已有数十亿美元可调用”既是优势，也是风险。新市场需要先证明报价、清算、退出与接口在真实环境中都能运转；借款人、出借人和做市者也要形成稳定行为。先让小规模自然交易暴露问题，再逐步接入旧金库资金，可以避免用巨大流动性掩盖尚未成熟的价格发现。

### 开放基础设施、order book 与 rate curve

**Paul Frambot：** 我用一个词概括 crypto 的优势：openness。它带来两项具体好处。

第一是更好的 pricing，因为竞争开放而激烈。Coinbase 用户通过 Morpho 链上借款时，可能有成千上万 lenders 竞争提供最优利率，而且这些资金来自全球。结果是，Coinbase 的 DeFi borrow product 可以给出比 centralized desk 更好的融资价格。链上环境会压缩 lending rate 与 borrowing rate 之间的 spread，这是最关键的 use case。

第二是 accessibility。代码开源，状态可读，接入成本低。Morpho 能以同一组代码集成大量 fintech。open-source 与 open infrastructure 的复利效应很强，虽然启动 network effect 需要克服很大惯性，但一旦形成，adoption 与 liquidity 会滚雪球。

**David Hoffman：** Midnight 创建的 obligation 本身是一种 token，类似 zero-coupon bond。假设一年期贷款年化 5%，obligation 初始价值约 95，到期兑换 100。它能在参与者之间交易。二级市场怎样形成，是 order book 吗？

**Paul Frambot：** 是 order book。curators 可以提交四类 orders：make borrow offer、take borrow offer、make lend offer、take lend offer。作为 lend maker，可以按指定 rate 向 borrowers 报价；成交后双方进入贷款。任何一方想提前退出，可以接受现有报价，也可以自己挂单。

primary market 与 secondary market 处于同一个 construct，协议几乎不区分两者。假设某个 obligation 年底到期，原 lender 想提前一个月退出，刚好可能与只想持有一个月的人匹配。相同 obligation 是 fungible 的，并非每笔都是孤立 OTC contract。

这种设计也解释了为何期限固定不等于资金一定锁死到期。出借人与借款人承诺的是一组可交易权利义务，而不是永远绑定的双边关系。只要二级市场有报价，原参与者可以把头寸转让给新参与者。某人需要六个月融资，另一人只愿持有五个月，最后一个月仍可以由第三方接手，多个不同流动性偏好因此汇入同一市场。

Midnight 还有跨市场网络效应，例如 multi-market offers 和 callbacks。一笔 liquidity 可以服务多个隔离 markets，所以不会因为 obligation 数量多而机械碎片化。

**David Hoffman：** 我过去不喜欢 fixed-rate、fixed-term market，是因为单份双边合约不等于市场。Uniswap 或 Aave 把很多人直接聚合在一处，市场就是协议本身。Midnight 的答案似乎是：先创造大量可互换 building blocks，聚合后市场才浮现。

**Paul Frambot：** Midnight 同时具备两种效果。对某个确定 collateral、loan asset 和 maturity 的 obligation，所有头寸都像 Aave token 一样 fungible，构成连续市场，并非两方私下签约；大量 obligations 之间又通过 vault 与 multi-market liquidity 形成横向 network effect。

**David Hoffman：** 市场会逐渐形成 stablecoin、ETH、Bitcoin 的完整 rate curve。

**Paul Frambot：** Midnight 发布仅十小时，市场只有约 10 万美元流动性时，就已经有人画出五六张 rate curve。我不得不提醒大家，规模太小，任何人都可能操纵。但它仍然很有意思，因为 DeFi 乃至传统金融会得到过去不存在的新数据点。随着资产 tokenization 与参与者专业化，很多资产会首次形成 native interest-rate curve。

短期看，这些曲线不一定直接给 Morpho 带来很多商业价值，更像我的研究兴趣。真正让我兴奋的是，Midnight 可以发现“信任的价格”。

这些曲线在规模很小时不能被当作可靠基准，因为少量交易就能改变显示利率。但随着深度增加，它们会成为公开的期限结构：市场可以比较同一资产不同到期日的资金成本，也可以比较不同抵押品、身份条件和信用证明对应的风险溢价。过去分散在私下报价中的信息，会变成连续、可观察的数据。

### 从 collateral 到“信任的价格”

**Paul Frambot：** 借款人进入 Morpho 时，需要证明自己值得获得融资。今天通常通过存入大量 Bitcoin 或其他 collateral 来证明。Midnight 的通用模块允许借款人表达更多 trust assumptions：可以是 collateral，也可以是 identity、receivables、业务收入证明或其他材料。curators 看到这些信息后自行定价。

我大约一年前写过一篇文章叫《The Price of Trust》，背后就是 Midnight。它可以成为一台给信任条件定价的机器。

理论上，我可以公开证明自己是 Paul、是 Morpho CEO，然后申请借 10 万美元。市场也许愿意借给我，只是 rate 很高。协议不替任何人判断信用，而由愿意承担风险的人报价。

行业谈 undercollateralized loans 已经六年，却总问“DeFi protocol 怎样承销”。答案是：代码不应该替人授信，credit 本身非常复杂；但全球最大的 private-credit funds 知道怎样 underwriting，也知道怎样给风险定价。要解锁 undercollateralized credit，就必须把 risk 与 rate 都外部化，让市场给任意风险报价。

协议负责的是表达与撮合，不是宣布谁值得信任。借款人把能够证明自己的材料放入统一结构，出借人选择哪些材料可信、需要多少补偿。不同管理者可以对同一份证明给出完全不同的利率，竞争结果就是这组信任条件的市场价格。错误判断由报价者承担，而不是把风险隐藏在一条看似客观的协议公式里。

**David Hoffman：** 也可能有人声称自己代表 Apple，拿出所谓文件申请借款，但材料是假的。

**Paul Frambot：** 对。判断欺诈不是 Morpho 的职责。协议只让相关 assertions 公开在链上。我们当前也没有优先推动这类无抵押场景，launch 会先聚焦 overcollateralized crypto loans。通用模块只是允许借款人附上链上 trust signal，例如某种 oracle 或 zero-knowledge proof，再由 curators 判断。

**David Hoffman：** 如果真正的 Apple 想获得 credit line，就需要让律师签署文件、公开确认身份与承诺。出借人如果发现 Apple 违约，可以在链下法院起诉。执行发生在链下，而链上的价值是开放匹配。

**Paul Frambot：** 正是如此。onchain 的作用是把 N 个 lenders 与 N 个 borrowers 放进全球 auction，提高 price discovery 与效率，降低 Apple 或任何借款人的 cost of capital。未来申请 home mortgage 时，不必只接受一家银行给出的利率，而可以让成千上万 lenders 竞价。

Morpho 不负责链下 enforcement，但可以建立一套表达“为何可信”的语言和抽象。好的表达体系会帮助资本形成，并把融资市场扩展到目前 collateral 之外的资产。

**David Hoffman：** 这还会推动 onchain identity。地址需要积累身份、还款历史和 credit history。

**Paul Frambot：** Midnight 可能成为 identity layer 的第一个真正 product-market fit。过去身份协议缺乏商业理由；现在，如果提供身份证明能让 cost of capital 降低几个 basis points，身份立刻拥有可计算价值。

### stablecoin、tokenized stocks 与机构进入顺序

**David Hoffman：** 哪些资产最适合 Midnight？稳定币借贷、以 Bitcoin 和 Ether 作 collateral 显然会继续。还会有新资产吗？

**Paul Frambot：** stablecoin 是主要焦点。Morpho 约 92% 的 loans 是 stablecoins，而一般 lending protocols 可能只有 50% 至 60%，其余很大一部分是 ETH leverage。Morpho 已经是 EVM 上最大的 USDC DeFi protocol 之一，而且优势明显。我们相信 stablecoin market 最终增长最大。

另一方面，出借与做空 ETH、Bitcoin、tokenized stocks 也有价值。长期看，securities lending 在 TradFi 是巨大市场，在合适 compliance guards 下，Midnight 也应支持。这些市场规模也许较小，但会形成重要 use case。

**David Hoffman：** 哪类新机构会因为 Midnight 上链？

**Paul Frambot：** 所有设有 crypto arm 的大型机构，如果还没有接触 Midnight，未来 24 个月大概率都会接触。我们确实与它们都谈过，也和其中不少做过 proof of concept；一些已经不再停留在 PoC，而是在启动完整业务。这是 institutional adoption 的重要节点。

采用顺序通常是 wallets、exchanges、fintechs、neobanks、asset managers，最后才是大型 banks。每一类中最激进者先行动，随后迫使更保守的大公司跟进。

这个顺序反映的是组织风险承受能力。钱包和交易所本来就在链上，试验新借贷轨道的边际成本最低；金融科技与新银行有分发能力，也愿意用新产品争夺用户；资产管理机构只有在控制权和风险定价足够清楚时才会大规模进入；传统银行受监管、旧系统和既有利润模式约束最多，因此通常最后行动。但一旦同类竞争者证明链上资金成本更低，保守机构也会被迫跟进。

**David Hoffman：** Ethereum 上的 neobank、neobrokerage 正在发展。stablecoin 和 wallet 降低了创建 neobank 的门槛，tokenized stocks 又让应用更容易提供 brokerage。Morpho Blue 与 Midnight 还可以为这些资产提供 margin account。

**Paul Frambot：** 对。任何金融应用如果没有 loan 和 yield，很难成为完整、可防御的产品。Morpho 让这些平台连接全球 liquidity network，提供收益与融资。

更广的变化是，任何拥有 distribution 的公司都会想把用户基础 financialize。只要给账户嵌入 self-custodial wallet，就能访问 onchain networks。Twitter、Uber、Airbnb 或任何高频应用，都可能让用户余额获得 interest。Uber 已经有 Uber Cash，未来可以通过链上基础设施提供收益。

不只 neobanks 会受益，所有拥有用户分发能力的应用都可能变成某种“银行”。它们最大的优势不是金融牌照，而是来自原有业务的 distribution。

**David Hoffman：** Starbucks 很早就展示过类似模式。用户先把几十美元存进 Starbucks wallet，公司由此持有数亿美元客户余额并获得 float 收益。现在任何有分发能力的应用，都能很容易变成带 yield 的 Venmo。

**Paul Frambot：** 对。大约最近三个月，crypto 已经成为构建 financial app 最容易的技术路径。链上金融产品的质量还没有在所有领域领先，但 payments 和 yield 已经很强，其他部分会持续改善。

Paul 的判断并不是每家公司都要变成受监管银行，而是账户、钱包和开放收益网络会被拆成可复用组件。拥有用户关系的应用只需选择合规边界和产品风险，就能把原本闲置的余额连接到融资市场。过去只有大型金融机构能承担的系统集成，逐渐变成普通软件团队也能调用的基础设施。

### 压缩 net interest margin

**David Hoffman：** 机构只有在链上 capital efficiency 更高时，才会把资金搬过来。Midnight 怎样实现这一点？

**Paul Frambot：** capital efficiency 最终是一切。链上贷款的 cost of capital 更低，会成为下一轮采用最大的 gravity pull。financing 是 finance 的基石，而 TradFi 的融资市场竞争不足，为金融系统创造了很高 net interest margin。我估计，这个中间层对整个经济收取约 200 至 300 basis points。

链上 rails 是开放的。只要基础设施允许市场自行定价，开放竞争就会压缩 net interest margin。这既是 Morpho 会被憎恨的原因，也是会被喜爱的原因：它会摧毁一批现有 business models，同时替借款人和储户节省大量成本。

传统体系中，借款人看到的是银行给出的最终贷款利率，储户看到的是存款收益，两者之间的差额包含机构资本、分支网络、流动性管理、监管成本和利润。链上并不会让所有成本归零，但它能把报价和资金来源放进同一公开市场，减少信息不透明与封闭分发带来的额外价差。只要竞争者可以无许可加入，超额利润就更难长期维持。

技术史本来就是不断颠覆行业。finance 因监管与信任要求，变化比其他行业慢，但现在拐点已经到来。banks 和 asset managers 很清楚，过去的盈利方式会因链的开放性而消失。它们可以阻止，也可以主动拥抱。game theory 决定了后者更合理，因为已有竞争者率先行动；这对 TradFi 已经不是可选项。

**David Hoffman：** 压缩 net interest margin，本质上是在压缩银行最重要的利润来源，并把价值返还给两端。Bitcoin、ETH 和 stablecoin 让用户减少对银行 money 的依赖；Midnight 又把银行后端的 fixed-rate、fixed-term loan 搬上链。对一个叫 Bankless 的节目来说，这当然令人兴奋。

**Paul Frambot：** 更重要的不只是“固定利率、固定期限”，而是 rate 由开放市场决定。它建立了一个对 trust 的开放 marketplace，是实现竞争性 cost of capital 最纯粹的形式。

我把 borrowers 看作想在世界上实现某种 ambition、却需要资本的人；lenders 则是相信他们、愿意提供资本的人。这本应是一项很高尚的活动。finance 看起来常常只是搬运价值、自己收税，但它真正连接的是 ambition 与 belief。问题在于，今天负责连接两者的基础设施成本太高。

Morpho 的使命，是压低“人彼此信任的成本”。开放 rails 让资金提供者竞争，给对手方最好的 terms。这正是我继续在 crypto 工作的原因。

### 2027 年 TVL 与稳定币市场

**David Hoffman：** 你预计 2027 年底 Morpho Midnight 的 TVL 会有多少？

**Paul Frambot：** 很大程度取决于何时解锁 TradFi use cases。crypto-backed loans 今天大约是 600 亿美元市场。Midnight 最终可能吃掉很大份额，并超过 Morpho Blue，但这一 market 仍只是数百亿美元，而且需要几年。

真正改变数量级的是新市场。如果网络接入管理数万亿美元资产的新型 curators 或 asset managers，addressable market 会快速扩大。我不是说 Midnight 2027 年就有数万亿美元，因为很多时间点不由我控制。

我的底线希望是超过 100 亿美元，并在规模上超过 Morpho Blue；做不到我会非常失望。另一方面，如果到时超过 1,000 亿美元，我也不会惊讶。Morpho Blue 用两年达到约 100 亿美元，因此这样的数量级并非毫无依据。

这两个数字代表不同情景。超过 100 亿美元主要依靠现有加密抵押贷款、稳定币需求和金库资金迁移即可实现；接近 1,000 亿美元则需要新型机构、链下资产和更大信用市场真正接入。前者是执行与流动性启动问题，后者还取决于监管、身份、法律执行以及传统资产管理者是否把完整业务搬到链上。

**David Hoffman：** Blockchain Capital 的嘉宾认为，到 2030 年链上 stablecoins 达到 2 万亿美元仍是保守预测。这必然伴随 credit、borrowing 和 lending markets 爆发。

**Paul Frambot：** 我同意方向，但我不擅长给出精确时间与数量。CLARITY Act 是否通过等外部事件都会显著改变速度。我在 DeFi 更擅长判断长期方向，而不是准确预测哪一年达到哪个数字。

稳定币规模增长也不会自动等比例转化为借贷规模。资金必须有真实借款需求、可接受的风险证明、足够深的退出市场和清晰监管框架，才会从支付余额变成信用资产。Midnight 试图补齐的是期限、定价与风险表达三块基础设施；最终增长速度仍取决于链上经济是否产生足够多愿意为资本付费的使用者。

### 节目推广

**旁白：** Bankless 推出一档帮助投资者判断 crypto cycle 的新节目，由 The DeFi Report 的 Michael Nadeau 主持。节目每周讨论其 portfolio、market structure、entry targets、Bitcoin 与 Ether fair value 以及周期位置，每周三更新。

Bankless Premium RSS 还提供额外研究型访谈并去除广告。使用 premium feed 的听众每年大约可以减少 20 小时广告时间，同时直接支持节目。

### Hester Peirce、vault 与法律责任

**David Hoffman：** Hester Peirce 最近对 vault sector 发布了一份态度尊重、但也提出关键担忧的声明。她说部分 vault 可能属于 investment company 或 investment contract，某些 lending strategies 产生的 notes 也可能是 securities。你的反应是什么？

**Paul Frambot：** 我不惊讶。上周我一直在 Washington，与 SEC、CFTC、senators 和 staffers 多次会面。我们和监管机构保持密切沟通。

她的完整文章非常有思考。vault stack 很多，结构差异极大。有些完全 non-custodial、immutable，curator 只能在 timelock 约束下调整风险参数；另一些本质上只是 Fireblocks wallet，用户把钱转入后，管理者几乎拥有全部决定权。整个市场存在连续 spectrum。部分结构确实可能是 investment company，另一些则未必。

关键是监管者已经理解 vault 不是单一产品，而是由 non-custodiality、control、agency 程度不同的结构组成。lending protocol 也一样，有的协议对风险参数拥有很大控制权，Morpho 的目标则是尽量不保留这种 agency。

**David Hoffman：** Peirce 特别说，“vault”是一个故意宽泛、通用的描述，没有统一定义。crypto 经常创造这种词。token 也一样，有的 token 就是 security，有的只是 receipt token 或 utility；词本身几乎没有解释力。

**Paul Frambot：** 我创造 curator 这个词时，也故意保持宽泛，因为当时并不知道这种角色最终会怎样发展。它有点像 asset manager，却又 non-custodial，不能直接管理资产；部分活动又确实与资产管理相似。

面对真正的新事物，先创造一个中性新词是稳妥办法。随着行业与监管者划定哪些活动属于 investment contract、哪些不受 SEC 监管，词汇可以做第二轮迭代，增加 network token、security token 等更明确的修饰语。

**David Hoffman：** 我最近采访过一个用 AI 检查 vault source 与嵌套关系的团队。一个 vault 可能存入另一个 vault，后者又进入更多 vault。用户以为只是把 USDC 放进一个 6% yield vault，底层却展开成 17 个 vault，风险拓扑非常复杂。

我们最后得出的困境是：vault vertical 没人愿意承担 liability。Morpho 希望只做 neutral technology platform，curators 也不想担责。但如果这个行业要扩大 100 倍，某一层可能必须注册、合规并承担明确 duty，同时也获得更多 upside。你怎样看？

**Paul Frambot：** 可以把角色分成 distributor、curator 与 infrastructure。

Morpho 作为 market 与 vault infrastructure，责任是提供安全、经过审计的代码，并给 curator 一个受控环境。Morpho vault 不能任意存入其他 vault，只能进入 Morpho markets。curator 增加新 market 必须经过 timelock。在 timelock 到期前，用户可以提取 stablecoins；如果 vault 当时不具备足够 liquid assets，也可以 in-kind 提取底层 position。

只要配置正确，即使 North Korea 明天攻破某个 curator，用户仍有几天时间在变更生效前退出。curator 无法悄悄立刻偷走资金，这就是 non-custodiality，也是 infrastructure 应提供的保证。

distributor 显然有责任，因为它选择向用户呈现哪一个选项，应该尽可能披露风险。至于是否承担法律责任，我不是裁决者。

curator 是否担责高度取决于 vault stack。如果它完全决定资金去哪，拥有实质 control，却声称没有 liability，很难令人信服；但如果 vault 极其 non-custodial，curator 只承担 operational 而非 managerial role，结论又可能不同。每种配置细节都重要。

因此，不能仅凭“金库”或“策展人”两个标签决定监管性质。需要逐项检查谁能改变投资范围、谁能移动资金、变更要等待多久、用户能否在变更前退出、底层头寸是否透明，以及面向用户的承诺是什么。控制越大、用户依赖越强，承担管理责任的理由就越充分；反之，如果角色只是执行公开且受限的操作，责任更接近技术服务。

**David Hoffman：** 我的直觉也是 curator 最接近应承担更多 legal liability 的一方，因为它决定风险水平与风险类型。相应地，它也应获得更多 upside 和 skin in the game。一个责任更重、回报也更高的职业角色，可能让行业在合规和安全前提下扩张。

**Paul Frambot：** 这大体符合我的直觉，但必须保留 caveat。核心在于 curator 与最终用户之间的 implicit contract：用户认为谁在保护资金，期望依赖谁作判断？如果 curator 只是按预设规则执行操作，和用户把它当作 discretionary manager，法律性质应当不同。

**David Hoffman：** 我还会采访 Upshift、Veda、Stake 等团队，继续追问 vault vertical 中谁应承担更多责任。不是因为承担 liability 本身高尚，而是明确责任可能让整个行业更安全、规模更大。

Paul，很高兴看到 Morpho Midnight 上线。现阶段让它有机发展、让市场参与者熟悉；未来某天打开开关，让 Morpho Blue 与 Midnight 的流动性相连，会是另一个重要节点。感谢你介绍这个新 primitive。

这场讨论的核心不是把传统债券机械复制到链上，而是把期限、风险与价格从协议治理中拆出来，让不同专业参与者公开竞争。早期链上借贷用统一公式换取易用性；新阶段则希望由上层金库保留易用界面，底层市场恢复真实报价。能否同时获得可预测利率、充足流动性、透明责任和更低资金成本，将决定 Midnight 是否真正超过既有产品。

最终检验标准仍是实际成交、违约表现、资金留存和机构持续采用，而不是发布初期的概念热度。

**Paul Frambot：** 谢谢 David。

**David Hoffman：** Crypto 有风险，投入资金可能全部损失。机构正在进入，行业也在继续探索更远的边界。这条路不适合所有人，但感谢你和 Bankless 一起前进。
