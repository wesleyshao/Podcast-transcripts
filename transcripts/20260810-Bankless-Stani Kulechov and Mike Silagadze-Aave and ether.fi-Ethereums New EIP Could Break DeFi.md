---
访谈时间: 2026-08-10
访谈时间说明: 未能从公开节目资料独立确认实际录制日期，按 YouTube 发布日期记录。
YouTube发布时间: 2026-08-10T10:30:03Z
嘉宾名字: David Hoffman; Stani Kulechov; Mike Silagadze
嘉宾公司名称: Bankless; Aave; ether.fi
参与嘉宾:
  - 姓名: David Hoffman
    公司或机构: Bankless
    职务: 联合创始人、主持人
  - 姓名: Stani Kulechov
    公司或机构: Aave
    职务: 创始人、CEO
  - 姓名: Mike Silagadze
    公司或机构: ether.fi
    职务: 创始人、CEO
播客名称: Bankless
播客url地址: https://www.youtube.com/watch?v=NCvOUkryd1k
youtube_video_id: NCvOUkryd1k
字幕来源: YouTube 公开自动字幕 json3（en-orig），结合完整上下文转写为简体中文
全文提及的关键名词:
  - Ethereum
  - ETH
  - EIP
  - stake targeting
  - stake tapering
  - ETH issuance
  - minimum viable issuance
  - proof of stake
  - solo staking
  - liquid staking token
  - LST
  - Lido
  - Rocket Pool
  - ether.fi
  - Aave
  - DeFi
  - stablecoin
  - carry trade
  - funding leg
  - nominal yield
  - real yield
  - EIP-1559
  - monetary policy
  - CLARITY Act
  - ETF
  - Coinbase
  - Binance
  - SharpLink
  - BitMine
  - Tom Lee
  - Bitcoin
  - credible neutrality
companies:
  - Aave
  - Lido
  - Binance
  - BitMine
  - COIN
industries:
  - 加密
  - 支付
  - 宏观
technologies:
  - DeFi
  - 以太坊
  - 比特币
  - 稳定币
keywords:
  - 稳定币法案
tags:
  - Aave
  - Lido
  - Binance
  - BitMine
  - COIN
  - 加密
  - 支付
  - 宏观
  - DeFi
  - 以太坊
  - 比特币
  - 稳定币
  - 稳定币法案
---

# Ethereum’s New EIP Could Break DeFi

## Transcript

### stake tapering 为什么引发反弹

**David Hoffman：** Ethereum 社区出现了一项引发激烈争论的新 EIP。今天请 Aave 的 Stani 和 ether.fi 的 Mike 一起讨论 stake targeting，也叫 stake tapering。这本质上是 ETH issuance 和货币政策之争。

六名 Ethereum 研究者与开发者提出的问题是，网络没有约束 ETH staking 比例的上限。目前约 34% ETH 已参与 staking。只要 staking 仍有正收益，理论上比例就会持续向 100% 靠近。总 staking 越多，协议发行并支付给验证者的 ETH 总量也越大。

提案者担心两个结果。第一，Ethereum 金融体系里的 vanilla ETH 会逐渐被 staked ETH derivative 取代，例如 Lido 的 stETH、Rocket Pool 的 rETH 和 ether.fi 的 eETH。若最终几乎所有 ETH 都以 derivative 形式流通，原生资产会从 DeFi 里消失。第二，Ethereum 可能为 security 支付过多。研究者认为约 30% 至 40% 的 ETH staking 已足以保障网络，没有必要让一半甚至全部供应都被质押。

这项 EIP 上周发布，EF 内外都出现强烈反对。按 proposed curve，staking ratio 接近目标后，新增 staking yield 会迅速下降；若 staking 接近 50%，yield 可能趋近于零。我要听听实际运营 DeFi 与 staking 产品的建设者怎样评估后果。

### Stani：提问合理，方案却可能伤害三类核心参与者

**David：** Stani，你第一次看到提案时是什么反应？

**Stani Kulechov：** “Ethereum 是否为 security 付得太多”是合理问题。Ethereum 的核心价值之一就是 resilient network 和很强的 security。像我和 Mike 这样的 builder 选择 Ethereum，很大程度上正因为这项保证，所以为安全付费本身没有错，关键是价格是否合理。

我认为提案背后还有一个没有明说的目标：在 bearish market 中减少 issuance，希望改善 ETH price appeal。机制表面讨论 staking 比例、限制 issuance、压低 staking yield，实际想让 ETH 看起来更稀缺、更像 value-capture asset。但它很可能达不到这个目标，反而产生三个负面结果。

第一，它会破坏 solo staking 的经济性。独立验证者没有规模优势，硬件、网络、维护和税务成本都由个人承担。现金流下降后，solo staker 可能收到税单，却没有足够 yield 覆盖，甚至变成负收益。这样不是促进 decentralization，而是把人赶出网络。

第二，institution 需要 predictable cash flow，尤其当它们设计 ETF、custody、lending 或其他 financial product 时。机构进入 ETH 的重要原因之一，就是它与 Bitcoin 不同，存在可核算的 staking cash flow。若协议突然改变 yield curve，原有 underwriting 会失效，也会削弱未来分销。

第三，Ethereum 已建立在 DeFi rails 上。今天网络里最成功的应用大多属于 DeFi，这并不可耻。Ethereum 最有可能替代或改善的是金融体系，而 ETH 提供底层 security。提案者说，staking yield 降低后，用户可以去 Aave 等 DeFi 协议找收益，但很多 DeFi yield 本来就来自 native staking。把底层收益拿走，不能假设应用层凭空补出同等、同风险的 cash flow。

零收益还会让 ETH 变成 funding leg。carry trade 会借入最便宜、最低收益的资产，卖出后换成更 productive 的资产。全球最大的例子之一是 Japanese yen carry trade：借低息 yen，换成 dollar，再赚取更高利率。若 ETH 变成零收益资产，市场会借 ETH、卖 ETH，再持有能产生 cash flow 的资产。这会创造持续 sell pressure，与提案希望提高 ETH 价值的目标相反。

### Mike：solo staker 会退出，staking 反而更集中

**David：** Mike，你最在意哪些危险信号？

**Mike Silagadze：** 几乎每一部分都令我沮丧。首先是 process。提案在讨论是否进入下一次 hard fork 前几天才出现，给人的观感是有人想在缺乏充分辩论时把它塞进去。无论原意是否如此，这种 perception 已经损害信任，而且最后产生了相反效果，社区迅速集中反对。

更奇怪的是，提案被包装成有利于 solo staker，实际上最先受损的就是他们。个人 node operator 的 cost basis 最高，没有 economy of scale。按当前硬件与网络成本，2% 至 2.5% yield 已接近 break-even。ETHStaker 的近期调查显示，许多 solo staker 把约 2% 视为 reserve price，低于这个水平就会关闭 node。不能靠“他们会为了理想继续亏钱”来设计协议。

相反，Coinbase、Binance、SharpLink、BitMine 等大型实体持有用户或公司沉淀的 ETH，capital cost 接近零。即使 yield 只剩 20 或 50 basis points，它们仍可能 staking。独立节点退出，大型托管者继续，网络会更 centralized。

LST 也会集中。若一个 liquid staking product 只能赚极少 basis point revenue，就必须达到巨大 scale，才付得起 developer、auditor 和运营。小 LST 无法生存，资金会向一个最大产品聚集。这与提案声称改善 decentralization 的方向相反。

**Mike：** 可以把这笔账算得更直白。独立验证者需要买机器、支付带宽、维护软件，还要承担停机与惩罚风险；交易所或大型资产负债表公司拿到的 ETH 原本就躺在账户里。收益降到很低后，前者每运行一台节点都可能亏钱，后者只要边际收入为正就会继续。相同的收益曲线因此不会平等影响所有参与者，而会系统性偏向已经拥有规模和客户资金的大机构。

液体质押服务也要持续做安全审计、客户端兼容、治理、前端、流动性与事故处理。如果收入只剩万分之几，一个小团队无法仅靠几十万或几百万美元资产维持这些固定成本。市场会自然集中到拥有最大资产池和最深交易流动性的少数服务商。提案若只看“质押总比例下降”，却不看剩余质押由谁控制，就可能用较低的总量换来更差的权力分布。

而且 LST 不只是在 staking 中间抽一层。它可以在 application layer 提供不适合写进 network layer 的 user protection。假设 North Korea 攻击并盗走 ether.fi 大量 liquid-staked ETH，我们有可能通过明确 governance process 进行 application-level fork 或补救。基础协议不应轻易为单一应用做这种恢复，但应用层可以提供保险、治理与用户保护。

传统金融中，derivative market 远大于 spot market。若 Ethereum 真成为全球金融平台，几乎所有 ETH 最终都会进入某种 derivative、deposit claim 或 credit structure。现实里消费者买 groceries，也不是搬运银行金库里的现金，而是转移对银行的 claim。要求经济活动只使用 EOA 里最原始的 ETH，就像要求所有人携带 gold coin。金融中介可以被改造得更透明、更低成本，却不会因为协议偏爱 vanilla asset 就完全消失。

货币供应也不应机械冻结。严肃经济体需要 money supply 随经济规模变化。Milton Friedman 曾主张货币供应按固定约 3% 速度增长，理由之一就是持续 deflation 也会伤害经济。把“零 issuance”当成天然正确，是把 Bitcoin 的 hard-money 逻辑生搬到 Ethereum。若要解决 LST 的协议风险，我甚至更倾向讨论 enshrined LST，而不是用 issuance curve 冲击整个 DeFi 系统。

### 如果底层收益归零，DeFi 会发生什么

**David：** 这可能是最重要的问题。假设提案通过，staking 接近 50% 后 yield 趋近零，DeFi 的二阶、三阶后果是什么？

**Mike：** 按现在的结构，top 10 DeFi protocol 中可能有七个面临大规模 capital exodus。短期 government bill 的 yield 是传统金融大量 derivative 的底层。若美国政府突然说，持有 T-bill 的人太多时就把 rate taper 到零，上面依赖这条基础曲线的产品都会被重定价。

Ethereum staking yield 也是类似的 foundational yield layer。即便 100% ETH staking，在不计 EIP-1559 burn 的极端假设下，issuance 大约也只是 1.5%。真正要问的是，这 1.5% 是否构成足以破坏系统的问题。把它减少半个百分点，却让大量协议、抵押结构和机构产品失去底层现金流，代价可能远高于所谓节省。

**Mike：** 这个极端数字还把交易费销毁假设成零。现实中，网络活动越多，销毁通常越多，净供应增长会低于毛发行。若应用增长带来更多交易，部分安全预算会被销毁自动抵消。因此不能只看验证者收到多少新币，还要看净发行、网络收入和经济规模。提案把一个会随使用量自我调整的体系，改成随质押比例急剧压低回报的体系，却没有证明后者能产生更高净价值。

把安全预算称为“多付的钱”也容易忽略它购买的服务。验证者维持共识、处理交易并让价值数千亿美元的资产保持可结算。只要支付比例温和，且网络价值和使用量增长，这笔费用可以像基础设施支出一样合理。真正需要削减的是没有带来安全或分散性的无效支出，而不是先设定零收益结论，再要求所有参与者适应。

若考虑 burn，net inflation 还会更低。我甚至认为，若从经济增长角度看，提高 yield 的论据可能比归零更强。不过我的主张不是提高，而是不要随意改动一个承载大量合约和资产的底层 yield curve。

**Stani：** DeFi protocol 对资产本身相对 agnostic，资金会换去别的资产，协议未必消失。但 ETH 会失去 productive-asset 属性。没有 native staking yield，用户只有沿 risk curve 向上走，才能寻找 ETH-denominated return。可扩展、低风险的 ETH 收益来源并不多，很多 lending demand 和流动性本来就是由 LST 提供。

LST 让用户可以在 staking exposure 与流动性之间转换，不必排长时间的 validator exit queue。它又能进入 lending protocol，成为 collateral 或借贷标的。若底层 yield 被移除，这些需求不会自动转成同风险的其他 DeFi yield。

最大的受益者可能是 stablecoin。持有 ETH 并看重 staking cash flow 的用户，会比较链上 dollar yield。传统市场里，当 cash rate 很低，资金流向 equity、commodity 和 risk asset；当 cash 本身收益高，而其他资产缺少 cash flow，资金就回到 cash。链上也一样。ETH yield 归零而 stablecoin 仍能获得 dollar rate，资金会从 ETH 转成 stablecoin。

这还会强化 ETH 作为 carry trade funding leg 的角色。交易者借入零收益 ETH，卖出换取 stablecoin 或其他 productive asset，再赚取利差。新增 sell pressure 会压低 ETH，正好违背提案者想让 ETH 更像优质货币和价值储藏的初衷。我没有看到这项提案经过足够多基于真实经济机制的 review。

**Stani：** Aave 这样的借贷协议不会因为某个资产收益下降就停止运作，它会接受市场真正想借和想存的资产。变化会体现在资产构成：如果 ETH 缺少基础现金流，而链上美元仍能分享国债或货币市场利率，存款人会转向美元资产；借款人则更愿意把 ETH 当成廉价融资来源。协议表面总量甚至可能继续增长，但增长不再以 ETH 为中心。

这会产生一个容易被忽略的反馈。更多人借 ETH 并卖出，市场上的可借需求看似提高，借款利率可能短期上升；但这个利率来自做空或套息需求，不等于持有 ETH 的长期生产力改善。与此同时，原本用质押收益覆盖借贷成本、构造低风险组合的资金会退出。不能把所有利率都称作“应用层会重新创造的收益”，必须区分它来自网络安全服务、真实交易费，还是来自承担更高价格和清算风险。

**Mike：** “七个头部协议遭遇资金外流”不是说每个合约会当天停止，而是它们的基础抵押品、收益基准和组合结构会一起重定价。很多策略把质押收益当作接近链上无风险利率，再在其上叠加借贷、流动性和杠杆。若底层突然接近零，用户要么接受更低回报，要么提高杠杆和合约风险，要么离开 ETH 体系。三个选择都不是提案者所说的“让普通持有人更安全”。

### 对提案最强的辩护：保护 vanilla ETH 持有人

**David：** 我仍能理解提案中的一个 noble 目标。用户不应为了不被 issuance 稀释，被迫把 ETH 放进 Lido、Rocket Pool 或 ether.fi。它们比 bank 更开放，但仍是 intermediary。Ethereum 的初衷之一就是减少中介。

stake targeting 让用户可以 self-sovereign 地持有 vanilla ETH，不需要为了追上 issuance rate 进入第三方 derivative。这很像 Bitcoin 的 hard money 与 sound money。

还要区分 nominal yield 与 real yield。staking reward 中由新发行 ETH 支付的部分是 nominal；来自 transaction fee，以及可能计入的 burn，才更接近 real yield。人们喜欢玩 nominal-yield game，但若大家同比例被稀释，它看起来可能只是会计游戏。stake tapering 可以让普通人不用参与这场游戏。

**Mike：** 这是一种很窄的 cash-accounting 视角。若整个经济增长，money supply 增长慢于经济，持有人仍获得 real growth。issuance 支付给运行网络、提供 security 和 user protection 的参与者，这些服务又帮助生态扩大。不能只看到 token 数量增加，就断言价值被浪费。

**Mike：** 假设网络经济活动增长十分之一，而供应只增长百分之一。即便验证者收到新发行，单位 ETH 对经济活动的索取权仍可能增加。新发行不是凭空送给毫无贡献的人，而是支付给让账本持续运行、安全可用的人。若这些人又把收益用于节点、审计、开发和获客，发行会反过来提高网络价值。只比较发行前后钱包里的币数，无法判断这笔支出是否产生回报。

相反，把所有人锁在固定供应里也不保证价值自然上升。若资产因为持续通缩而不适合作为债务单位，借款人会担心未来需要用更贵的 ETH 偿还，企业也更不愿用它计价长期合同。一个只适合囤积、不适合借贷和结算的资产，可以是价值储藏，却未必能支撑 Ethereum 想建立的完整金融经济。

把 vanilla ETH 当成唯一“真实”资产，隐含的是不相信 Ethereum 会成为成熟经济。成熟经济一定会出现 derivative、institution、protection、chargeback 和 deposit claim。银行不会把全部 ETH 放在一个裸 wallet 里，企业也不会每笔支付都直接转原始 coin；它们需要风险隔离、治理和恢复机制。LST 用约 5 至 10 basis points 成本提供一层服务，已经比传统体系便宜很多。

**Mike：** 普通人今天刷卡买东西，商家收到的不是一张从央行金库搬来的纸币，而是一连串对银行、支付网络和存款体系的权利。它们当然会引入信用与治理风险，但也提供欺诈处理、账户恢复、对账和退款。链上金融的目标可以是把这些权利做得透明、可验证、可自由退出，而不是假装成熟经济能够完全不需要任何衍生权利。

液体质押代币也是这种应用层权利。它把一段退出期、验证者运营和惩罚风险包装成可转移资产，让用户继续参与支付、借贷和做市。若服务收费只有几个基点，却能提供流动性和事故治理，就不能只因为它不是原生 ETH 而认定它天然有害。真正需要比较的是集中度、智能合约风险和治理质量，而不是名称里有没有“原生”。

如果所有人只是把 ETH 堆在地址里等升值，Bitcoin 式逻辑还能自洽；若目标是承载金融经济，就不可能消灭金融化。即使协议取消 staking，市场仍会创造 wrapper 和 claim。derivative 的存在不是 staking yield 单独造成的。

### 应用层已经能把安全收益分配给终端用户

**David：** 另一种 steelman 是，提案想让 end user 免费获得 Ethereum security 的价值。但 DeFi 本来就在 democratize yield。若最终 100% ETH staking，LST 与 Aave、ether.fi 等应用可以把收益重新分配给持有者，效果近似于让普通账户免受 issuance 稀释。

换句话说，stake tapering 想达到的目标，application layer 已经在完成。DeFi 是 ETH 的 financialization 与 democratization layer。协议若把这项工作 enshrine 到 base layer，相当于从一个已经运转的开放市场手里拿走功能。

**Mike：** 还可以把 staking yield 理解为 savings rate。一个人在经济中创造产品或服务，获得 ETH 后选择不消费，而是保存。他 staking 这笔 ETH、帮助 network security，也等于让财富继续在经济中发挥作用，所以获得利息。

储蓄回报还会影响持有者行为。收到 ETH 的开发者、企业或个人若能通过低风险质押获得温和回报，就更愿意长期持有，而不是立刻卖成美元。这个“愿意持有”的作用既帮助价格稳定，也扩大验证者集合。把收益削到低于运营成本，既减少独立安全提供者，也减少愿意以 ETH 作为长期储蓄的人。

当然，质押不是传统银行贷款，不能把两者完全等同。验证者获得的是执行共识和承担惩罚风险的报酬，储蓄利率只是它在经济层面的附带作用。争论的困难就在这里：同一条发行曲线同时决定安全预算、持有激励和链上基准收益。只按其中一个目标优化，必然把成本转嫁给另外两个目标。

如果 Ethereum economy 每年增长 10%，money supply 增长 1%，系统仍有约 9% real growth。持有人一方面可能从 ETH appreciation 受益，另一方面获得 network reward。staking 目前同时承担两项功能：支付 security，也提供事实上的 savings rate。把两项混在同一机制里确实产生复杂性，但不能因为 security 似乎“够了”，就忽略经济仍需要储蓄回报。

### minimum viable issuance 是否要求继续削减

**David：** 支持者会说，Ethereum 历次 monetary policy 改动都朝减少 issuance 的方向走。这不是任意转向，而是延续一贯 social contract：只支付 minimum viable issuance。既然当前仍高于保障 security 所需的最低发行，就应继续降低。

**Stani：** 我理解任何人都不想为服务多付钱。issuance 是全体持有人向维护网络者支付的费用，当然不应失控到每年 20% 或 30%。但经济不是 vacuum。生态在增长、有 capital inflow，支付一部分 issuance 去获得 security、distribution 和参与者多样性，未必是浪费。

“最低可行发行”也不是一个脱离环境的常数。攻击成本、验证者结构、硬件成本、ETH 价格和应用锁定价值都会变化。今天三成质押看似足够，不代表把收益压低后仍能保持同样数量和同样多样性的验证者。真正应衡量的是边际减少发行节省多少稀释，同时会让多少独立节点退出、让多少质押转向托管机构，以及整个网络在极端事件下损失多少韧性。

若研究者只用总质押价值估算安全，可能高估高度集中质押的防御效果。由少数交易所、托管商和公司控制的一大批验证者，面对监管命令、软件故障或共同治理失误时，会表现出相关性。数量相同但运营者更分散的验证者集合，安全质量可能更高。因此发行支付的不只是总金额，还在购买参与者多样性。

机构不会只看“是否 deflationary”，它们会看资产与业务增长，以及 cash payout 相对增长是否合理。growth-stage business 有时会支付很高成本来买 distribution 和 market share。Ethereum 也正在完成机构分销的 last mile，而不是一个增长已经结束、只需榨取稀缺性的成熟资产。

ETH ETF 已存在，更多 institution 正在研究 custody、lending 和 treasury product。若 CLARITY Act 通过，美国银行可能无需逐项预审批就能开展更多 crypto business。ETH 有 savings rate，是它相对 Bitcoin 的差异化之一；同时还面对 Solana 等网络竞争。此时突然杀掉 yield，会破坏机构对产品的 underwriting，把增量资金推向 stablecoin 或 competing network。

机构产品通常要提前写入收益假设、托管流程、风险披露和客户材料。协议若在产品刚进入分销阶段时大改曲线，损失的不只是当年少收几个百分点，而是让风控部门怀疑以后还能否稳定建模。一个资产可以拥有灵活治理，也可以拥有可预测性，但重大货币政策变化必须经过足够长、足够开放的讨论，给持有人和产品发行人消化时间。

Stani 所说的“最后一公里”不是断言机构一定会买，而是当前恰好出现监管、托管和分销渠道逐步开放的窗口。ETH 与 Bitcoin 的竞争点之一，是既有较强货币属性，又能产生链上现金流并承载应用。若为了更像 Bitcoin 而去掉后两项优势，机构完全可能直接选择更熟悉的 Bitcoin，或者选择收益更高的其他网络。

predictability 因此非常重要。已经进入的机构，是按 ETH 具有 cash flow 的假设配置；未来机构也需要可预期规则。想让 Ethereum 替代当前低效金融体系，就必须吸引它们进入，同时用 diverse staker base 保持 security。把这一切简单归类为不够去中心化的“机构逻辑”，并不能解决现实竞争。

**David：** Tom Lee 是很好的例子。他投入约 100 亿美元买 ETH，并把 staking yield 当作向其他机构介绍 ETH 的重要卖点。若一年后 protocol 把 yield 杀掉，不仅损害他的 business，也会吓退以后可能跟进的人。

**Stani：** 没有可核算 yield，这类 treasury company 只能更依赖 MicroStrategy 风格的 financial engineering。staking cash flow 让它们能从基本面 underwriting ETH。机构并没有要求 Ethereum 减少这一小部分 issuance；它们更关心 network 和 use case 是否继续增长。

社区现在更该修产品。Ethereum 仍缺少足够好的 privacy 和 scalability，security 是它已经具备的优势。需求不足不能靠反复玩 issuance game 解决。若削弱 security 与现金流，却不改善产品，可能同时损害三项竞争力。

**Mike：** 省下约 0.5% 或 1% issuance，却饿死真正推动生态增长的参与者，是 zero-sum thinking。security provider、LST、DeFi protocol 和 institution 把 reward 重新投入开发与分销。减少 issuance 不会自动把同等价值加到 ETH price，negative externality 反而可能摧毁 Ethereum 最有价值的部分。

### 更合理的“Bitcoin 式保守”是低收益，不是零收益

**David：** staking yield 是 proof of stake security 的基础，不可能真的从 Ethereum 消失。它不必是 10% 的双位数，但可以非常 conservative。Bitcoin 没有 staking yield；把 Bitcoiner mindset 合理应用到 Ethereum，应是约 2% 的低收益，而不是强行把 Ethereum 变成 Bitcoin。

Ethereum 已经是主要 issuing blockchain 中 yield 很低的一个，也低于许多 sovereign bond。保守发行、稳定安全和应用层金融化可以共存。追求绝对零 issuance，可能为了模仿另一种资产而舍弃 Ethereum 自己的结构优势。

**David：** “保守”应当意味着变化慢、规则可预测、支付与安全需求相称，而不是任何正发行都被视为失败。Ethereum 选择权益证明后，就选择了用收益吸引持有人承担验证职责。若完全不愿为这项工作支付，最终只能依赖已有大量资产、愿意把验证当附带业务的大型实体，这反而更接近集中托管体系。

而且低但稳定的收益能让市场形成一条清楚的基准曲线。借贷、期货、流动性质押和机构产品可以在这条曲线上定价风险溢价。收益随质押比例突然接近零，会让基准变成难以预测的政策变量。对一套希望承载长期合同的金融基础设施，稳定的低收益可能比理论上更“稀缺”的零收益更有价值。

**Stani 与 Mike：** 我们同意。问题不是要无限提高 yield，而是不要在缺乏完整经济分析时，把它 taper 到破坏独立验证者、机构产品和 DeFi 的程度。

### legitimacy 与 process 可能比曲线参数更重要

**David：** 在结束前，还有 process legitimacy。社区已经在公开讨论，但两位还有什么要补充？

**Mike：** 无论事实如何，外部 perception 是，这项重大改动在最后一刻被放上桌，像要在很少 debate 下进入 hard fork。Ethereum 必须认真管理这种观感。

协议治理的合法性不仅来自“任何人都能在论坛发言”，还来自意见是否有机会影响结果。若提案在关键会议前几天才公开，应用开发者、验证者和机构很难完成经济建模，更无法提出替代方案。即使流程形式上开放，时间不足也会让参与者认为决定早已做完。

反过来，这次激烈反弹也说明 Ethereum 社区仍有制衡能力。提案没有因为研究者身份就自动进入升级，建设者可以公开列出一阶与多阶后果。Mike 的担忧是，如果最终反馈被忽略，社区会把这次过程理解为研究机构与实际经济脱节；若反馈促成延期、修改或撤回，公开争论反而能增强合法性。

El Salvador 选择 Bitcoin 作为 reserve asset，一项重要原因是规则 ossified、可预测。Satoshi 已经离开，没有治理小组会突然改变 Bitcoin 的核心货币属性。它因而接近一种 natural money 或 digital gold。

假设一个 nation state 正在决定用 Bitcoin 还是 Ethereum 支撑一部分 national economy。它看到 Ethereum 可能突然调整 issuance、staking、gas economics，或者先推动 rollup-centric roadmap、随后又改变重点，就会担心 governance rug。即使每位研究者都出于善意，机构仍会按规则能否预测来决策。

Ethereum 在 smart-contract platform 中原本拥有最 secure、stable、credibly neutral 的声誉。草率观感会把它拉向其他经常主动修改经济参数的网络。若两者都可能频繁改变，机构会问 Ethereum 的差异究竟在哪里。

**Stani：** 我从 2015 年起就在 Ethereum 生态。长期可靠性与 legitimacy 非常重要。社区现在担心的不是研究者提出问题，而是收到大量具体 feedback 后，EF 是否真正倾听。过去一些 proposal 也有 backlash，但这次范围更大。

这项提案没有明显让 solo staker、institution 或 DeFi builder 受益。理论组成部分可以讨论，可一旦放进现实经济，结果可能与作者目标相反。开发者最担心 EF researcher 与生态其他参与者逐渐脱节，而且最终不采纳 builder 提供的经济反馈。若 process 给人“意见不会改变结果”的印象，损失的不只是这一条曲线，而是 Ethereum governance 的可信度。

### 最终判断

**David：** 节目开始时，我觉得这项 EIP 在真空里有吸引力，只是现实中不该支持。讨论后，我连真空里的支持也放弃了。

我原先认同保护原生 ETH 持有人、减少被迫进入中介、避免为不需要的安全多付钱。两位嘉宾让我看到，这些目标不能只靠改变一条发行曲线实现。应用层已经能把质押收益带给普通用户，独立验证者又需要最低收入维持；若忽略这些现实，所谓自我托管收益会以更集中验证和更弱应用经济为代价。

Ethereum 的 DeFi layer 是优势，协议应该利用它，而不是把 ETH 从应用层拉走。开放的 application market 已经在分配 security yield、提供流动性与用户保护。提案试图解决的问题没有想象中严重，却可能破坏解决这些问题的现有体系。

我也不认为它最后会通过，原因正是社区正在进行这种公开对话，把 solo staking、DeFi、institution 与 monetary policy 的后果说清楚。结论不是 issuance 永远不能讨论，而是不能为了让数字更稀缺，就忽略 Ethereum 作为一套真实金融经济的运行方式。

这次争论最终留下的检验标准很明确：任何后续版本都应同时量化净发行、独立验证者退出、质押集中度、应用层资金迁移和机构产品重定价，而不能只展示总质押比例与理论安全下限。只有收益端和代价端都能被公开验证，货币政策调整才具备足够依据。
