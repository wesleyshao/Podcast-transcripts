---
访谈时间: "2026-07-29"
访谈时间说明: "公开信息未披露实际录制时间，使用 YouTube 发布时间。"
嘉宾名字: "Sergej Kunz"
嘉宾公司名称: "1inch"
参与嘉宾:
  - 姓名: "Sergej Kunz"
    公司或机构: "1inch"
    职务: "联合创始人（Co-Founder）"
播客名称: "The Rollup"
播客url地址: "https://www.youtube.com/watch?v=6NHfPjc7E-E"
youtube_video_id: "6NHfPjc7E-E"
YouTube发布时间: "2026-07-29T15:05:27Z"
字幕来源: "YouTube 原始公开自动字幕 en-orig，结合完整上下文转写为简体中文"
转写说明: "删除字幕时间戳与妨碍语义重组的断行，按官方 RSS 校正 Sergej Kunz、1inch、Aqua、Pathfinder、Fusion、UniswapX、MEV、Solana、Robinhood Chain、Merkl 等自动字幕误识别；回测与杠杆示例均保留嘉宾原有风险提示。"
全文提及的关键名词:
  - Sergej Kunz
  - 1inch
  - Aqua
  - shared liquidity
  - Pathfinder
  - Fusion
  - intent-based protocol
  - Dutch auction
  - UniswapX
  - MEV
  - sandwich attack
  - atomic swap
  - hash time-locked contract
  - Solana
  - EVM
  - liquidity provider
  - just-in-time liquidity
  - Dune
  - Merkl
  - USDC
  - USDT
  - USDe
  - WBTC
  - cbBTC
  - UNI
  - Uniswap
  - Robinhood Chain
  - tokenized equities
  - RWA
  - KYB
  - capital efficiency
  - smart contract risk
companies:
  - Circle
  - Uniswap
  - HOOD
  - Tether
industries:
  - 加密
  - 金融
technologies:
  - 以太坊
  - 稳定币
  - Solana
  - 代币化
keywords: []
tags:
  - Circle
  - Uniswap
  - HOOD
  - Tether
  - 加密
  - 金融
  - 以太坊
  - 稳定币
  - Solana
  - 代币化
---

# Ethereum’s Sleeping Giant Just Woke Up - 1inch Co-Founder on Launch of Aqua

## Transcript

### Aqua 上线，以及 1inch 从聚合器走到共享流动性

**主持人：** 欢迎回到 The Rollup。今天的嘉宾是 1inch 联合创始人 Sergej Kunz。你们刚刚发布 Aqua 共享流动性协议（shared liquidity protocol）。你身后的 Trojan horse 很有《奥德赛》的感觉。为了这次产品上线，你看起来在办公室工作的时间远多于睡觉。Aqua 正式上线后，你现在感觉怎样？

**Sergej Kunz：** 很高兴来这里。坦率说，这让我想起 2019 年我们在 hackathon 上创建 1inch 的时候。团队像参加 hackathon 一样昼夜工作，每天只睡几个小时，但我们做到了。Aqua 已经以可用于生产的状态上线，系统很稳定，我们想实现的功能也都具备了，大家对此非常高兴。

**主持人：** Aqua 的推出紧接着你们与 Dune 合作完成的一项研究。研究结论之一是，liquidity provider 因现有结构损失了大约 1.5 亿美元的潜在手续费。我们稍后详细讨论研究和 Aqua。1inch 从链上市场早期一路经历 bridge、exchange、aggregator 和 AMM 的演化。请先简要回顾 1inch 的发展过程，以及哪些经验最终把你们带到今天。

**Sergej Kunz：** 2019 年，我和联合创始人 Anton 在世界各地参加 Ethereum hackathon，做过许多项目。我们在其中一次 hackathon 上想到一个很直接的主意：为什么不做一个小型 DApp，直接与 blockchain 交互，计算资产交换时能获得最佳执行结果的 smart routing？

2019 年的流动性还不像今天这样碎片化。随着市场变复杂，我们在 2020 年推出 Pathfinder 算法。这是整个团队协作的结果，它能利用多个市场的不同深度，把一笔交易拆到多条路径上。有时为了买到某种 memecoin，最优路径需要经过中间 token 或中间流动性，因为该 token 只与某些特定资产形成交易对，而用户可能希望直接用 USDC 买入。智能路由成了 1inch 的核心能力。竞争者后来也开始尝试类似方法，这对用户是好事，也迫使我们持续改进。到现在，我们仍然认为自己在聚合路由领域处于领先位置。

但聚合路由还不够。用户自己发起链上交易时，要承担整个执行过程的风险。MEV bots 开始截取用户交易价值，其中典型方式是 sandwich attack：你准备在 Uniswap pool 里 swap，bot 先在你的交易前面成交一次，再在后面反向成交，尽量吃掉你所允许的最大 price impact。

我们因此想到，用户不应该自己承担这些执行风险。用户只需要声明意图，例如“我想用 USDC 换某种 memecoin”，其余风险应由专业 market maker 承担。这促成了 intent-based protocol 和 1inch Fusion。Fusion 使用 Dutch auction。后来 UniswapX 的 white paper 也采用了我们这项研究和 Fusion 技术中的思路。

随后我们又看到 bridge 市场的问题。传统 bridge 很慢、风险高，历史上还发生过多次攻击。用户不仅要寻找具体 bridge，还得一直关注它是否可靠，当时也没有多少好用的聚合器。我们的思路是把 intent-based protocol 与 cross-chain atomic swap 结合起来。

我们找到一项早在 2012 年就在 BitcoinTalk 论坛提出的技术构想，即 hash time-locked contract。它很适合与 intent-based 方法组合。用户可以声明：“我要在 Ethereum 上卖出 ETH，并在另一条链上获得目标资产。”系统通过 escrow contract 和 secret 驱动的原子流程完成交易。用户只表达结果，market maker 承担执行风险，在目标链上交付用户预期的资产。

关键在于整个过程具有原子性。若某个 market maker 在目标链停止执行，其他参与者可以接续；否则交易会回滚，资产回到用户钱包，不会出现流程停在中间、资金却丢失的状态。这类非托管技术的教育成本比较高。接入一个 custodial service 当然更容易，也可能在下一个 block 就得到执行，但如果优先考虑安全与 non-custody，atomic swap 更符合目标。

我们后来把 intent-based protocol 扩展到 Solana。Solana 上的 MEV 问题很严重，我们的设计从协议层保护用户。随后又支持 Solana 与 EVM-compatible chains、各类 L2 之间的 atomic swap。现在用户可以在 Robinhood Chain、Ethereum、Solana 等不同网络之间交换资产，这已不是等待发明的概念，而是实际可用的技术。

走到这里，1inch 已经有 intent-based protocol，也有经典聚合器。聚合算法被 MetaMask、Trust Wallet 等 integrator，以及一些 arbitrage trader 和 market maker 使用。下一步自然是：为什么不建立自己的 liquidity provisioning venue？

这个方向其实始于 2021 年。当时我们开始研究由用户自行定义 price range 的交易策略。它有点像 limit order，但不只是某个固定价格，而是用户可以规定资产在哪一段价格内卖出、买入，或者双向交易。策略还可以沿某种 bonding curve 移动，也可以只向一个方向成交而不做反向交易。我们当时已经做过 prototype，只是市场条件还不成熟。

如今 intent、resolver network、MEV 和针对 liquidity pool 的 JIT attack 等条件都摆在一起，Aqua 到了合适的发布时间。它是 1inch 自己的 liquidity venue，用来支持 intent-based swap，也能把交易在同一场所内部结算，从而减少跨多个 Balancer、Curve、Uniswap pool 的复杂路径和 gas cost。可以把它理解为 1inch 产品体系里的另一块核心基础设施。

Aqua 的 strategy 非常灵活。现在主要有 full-range、concentrated liquidity，以及面向 stablecoin 的 packed liquidity 三类，未来还可以扩展到 flash loan 等更多形式。系统对 developer 开放，也从一开始就考虑了 institutional participant。

机构可以建立独立 position，不必把自己的流动性与公共 pool 里的其他资金混在一起。permissionless pool 里有时会出现来源有问题的资产，机构通常希望只让符合要求的参与者与自己的流动性结算。1inch Resolver Network 中的 resolver 会经过 KYB 和 compliance check，这让机构能使用隔离的流动性，同时保留链上结算能力。我们是在为未来的 finance 建基础设施。Aqua 并不只是另一个与 Uniswap pool 正面对打的产品，它是一种新的结构。

### 三个月激励计划与用户反馈

**主持人：** 1inch 从 Ethereum 早期一路经历 intent、bridge、swap 和机构合规，现在重点变成提高 capital efficiency，并释放原本闲置的价值。你曾说 liquidity provisioning 的现有结构已经失灵，只是过去没有替代方案，所以大家看不出问题有多严重；Aqua 出现后，LP 不必继续接受低效的 pool structure。

我们稍后讨论技术设计。The Rollup 的听众会先关心激励：参与 Aqua 的用户怎样获得奖励？

**Sergej Kunz：** 1inch Foundation 提议用激励帮助 liquidity provider 学习并开始使用 Aqua。除 Foundation 提供的 1INCH token 激励外，还有额外 500,000 USDC。奖励将在接下来的三个月通过合作伙伴 Merkl 分发。

Merkl 有成熟的基础设施，我们已把它整合到 1inch web application 和前端中。用户可以实时看到累计收益，并按周领取奖励。目标不只是吸引资金，也是让更多人真正使用新产品，并向我们反馈技术和使用体验。

### 资金留在钱包，同一份本金服务多套策略

**主持人：** 用户虽然会说“把资金放进 Aqua”，但资金实际仍留在自己的 wallet，这是很有力量的设计。相同资金可以同时配置到多套 liquidity strategy。我的理解有点像 just-in-time liquidity：订单出现并满足条件时，协议才使用你的流动性；资金不需要一直锁在 pool 里。请具体解释 Aqua 如何提高 capital efficiency，以及为什么它有机会让 LP 获得当前漏掉的大量手续费。

**Sergej Kunz：** 我先讲自己的经历。我曾在 Uniswap 提供流动性，一次在前端调整 maximum acceptable price impact 时设得稍高，结果连“提供流动性”这个动作也被 sandwich 了，最终拿到的资产少于预期。

我后来研究自己所在的 pool，发现每当较大的交易到来，MEV bot 就会临时注入大量流动性，拿走这笔交易的大部分手续费，然后马上撤出。这意味着长期留在 pool 里的普通 LP，实际收入远低于理论上应得的水平。

另一个问题是费用档位。假设 ETH/USDC pool 的 fee 固定为 30 bps，所有 LP 都挤在同一个档位里，自己的流动性会被稀释。但根据实时市场条件、投入金额和 price range，数学上的合适费率可能是 29 bps，也可能只有 4 至 5 bps。用户应该能够自由选择适合自己的费率与范围，而不是只能接受 pool 预设的少数档位。这与 1inch 一贯的 intent 思路相同：用户定义自己愿意怎样交易。

我们从 2021 年起就在 limit order 中研究这类 strategy。现在有了成熟的 resolver、intent 基础设施，也看清了 MEV 与 JIT liquidity 对传统 pool 的影响，Aqua 才真正具备上线条件。

Aqua 的关键能力是 shared liquidity。用户可以创建一个 multisig 或 subwallet，把愿意用于被动收益的 10,000 USDC 放进去，然后基于同一余额建立不同策略。subwallet 本质上是一个由主钱包拥有的 multisig，例如主钱包可以是 MetaMask。这样，用户可把日常资产与高风险策略分开：主钱包保留其他资产，subwallet 专门容纳自己愿意承担风险的资金。

如果用户愿意使用 leverage，还可以先把 USDC 存入 lending market，再借出相当于本金数倍的其他资产，然后直接在同一 wallet 中创建 Aqua trading strategy。举例说，在传统 Uniswap pool 里，用户可能把 5,000 USDC 和 5,000 USDT 放进一个 pool；在另一个结构里，可以借出 USDT、再次存入，再循环操作。也可以借 USDe 或其他资产，在它们之间建立多套 position，并为每套 position 选择较窄的 range 和不同 fee。

这里必须强调，循环借贷会显著放大风险，不只是收益。资产可能 depeg，仓位可能被 liquidate，smart contract 也可能出现问题。后面提到的倍数都是示例，不是收益承诺，也不是 financial advice。

我今天自己做了一套策略：把 ETH 和 Bitcoin 相关资产放入 wallet，在 WBTC 与 Coinbase 的 cbBTC 之间建立 position。cbBTC 在 Ethereum 上的流动性相对不足，因此已经出现交易量和手续费。从经济暴露看，两边都代表 Bitcoin，方向性价差通常较小，但仍然存在 wrapper depeg、liquidation 与 smart contract risk。

如果通过循环借贷把 10,000 美元名义本金扩展到 30,000 至 40,000 美元，表面上可以得到约 3 至 4 倍的 capital efficiency。它在传统 Uniswap pool 里很难实现，但不能把“更高名义使用率”误解为无风险收益。杠杆越高，depeg 或清算造成的损失也越大。

另一个简单例子是 UNI。持有人可能希望参与 Uniswap governance。如果把 UNI 存入传统 liquidity pool，通常无法继续直接使用这些 token 的治理权；如果资产仍在自己 wallet 中，就能保留 governance right，同时把同一余额用于 UNI/ETH 等交易策略。这就是“资金仍在钱包”带来的额外用途。

我们还上线了 Aqua Learn。用户可以在 1inch.com/aqua 查看视频、说明和 research paper。页面也提供 backtest：我们用过去 365 天的数据比较 Aqua position 与 Uniswap position 的表现。结果显示，position 越多，同一份 capital 被使用的机会越多，capital efficiency 也会提高。

未来还能在 Aqua 上开发更多 strategy。flash loan 就是一例：有人只在单笔 transaction 内借用资产，并为此支付 fee。现在我们仍在探索上层应用，同时重点帮助大型 liquidity provider、looping community、institutional participant 等理解产品。机构尤其不愿把自己的资金与完全 permissionless 的 pool 混合，Aqua 可以让它们选择合规的 resolver 和独立流动性环境。

**主持人：** 机构需要 compliance，但这和链上生态的 permissionless 属性存在张力。Aqua 把区分放在 application layer：permissionless 用户和机构都能使用相同的底层效率工具，但机构可以保留所需的隔离与合规边界。

传统模式是把资金存入 protocol，锁在 smart contract 中，等待买卖双方与 pool 交易。Aqua 的范式不同：流动性仍在用户钱包。简化地说，用户先授予限定额度与策略条件；只有符合条件的订单到来，protocol 才从 wallet 中取用相应 token。

这意味着相同 10,000 USDC 可以同时面向多个 venue 或策略提供报价，而不是先切成八份、分别锁进八个 pool。哪个 venue 的订单先匹配，才实际使用这笔资金。于是，同一份 principal 可以接触四个、五个、六个甚至八个来源的 order flow，提高潜在成交量和手续费机会。

Aqua 据介绍已覆盖 13 条 EVM chains，也在 DevNet 运行过一段时间。随着 RWA、tokenized equities 和 stock token 增加，用户是否可以持有 tokenized Apple、NVIDIA 等股票，同时从链上交易这些资产产生的手续费中获得收入？

### RWA、tokenized equities 与相对价格带来的交易量

**Sergej Kunz：** 现在已经可以这样做。用户可以进入 Robinhood Chain，对 tokenized stocks 建立 Aqua position。与传统 liquidity pool 相比，这种结构更节省资本。传统方法需要把 10,000 USDC 拆成许多小份，分别放进不同 pool；Aqua 则允许一个 wallet 的同一份 liquidity 支持多套 strategy。

我们与 Dune 的研究显示，传统 pool 中大约 85% 的流动性处于 idle 状态。换成 10,000 美元的例子，就是约 8,500 美元在大部分时间没有真正参与成交。若同一资产还能支持其他有 volume 的 trading pair，闲置部分就有机会被利用。

比如用户在 Robinhood Chain 持有多种 tokenized stocks，可以在它们之间建立 position，并自行设置 fee。arbitrage trader 会根据不同股票的相对价格变化成交。股票并不总是同步上涨或下跌；即使大盘同向波动，不同公司之间仍会出现相对变化。

这与 crypto blue chips 有所不同。Bitcoin、Ethereum，乃至许多 DeFi blue chips 和 memecoin，经常在同一市场周期中高度同向。tokenized stocks 之间的相对价格变化更多，这种“相对运动”形成 arbitrage activity，也就是 LP 可以争取的 volume。

我认为这是 Web3 下一阶段的重要方向：RWA 与 stock token 获得全天候交易采用后，用户不只持有股票资产本身，还能从围绕这些资产产生的链上交易量中获得 fee。这是 open finance，也是可组合的 money lego。但它仍然伴随 tokenization、smart contract、market 和 liquidity risk。

### 85% 闲置率、最多 4 倍回测效率，以及参数选择

**主持人：** 根据你们的 365 天研究，传统热门 pool 的平均收益大概怎样？同一份流动性换到 Aqua 后，可能增加多少？

**Sergej Kunz：** 我们的 backtest 没有把结果表达成固定 APR 或 APY，而是估算 fee earnings。结果高度取决于用户配置了多少 pair，以及 fee 和 price range 是否合适，不能给出一个适用于所有人的单一收益率。

根据报告，对某些交易对而言，较合适的 fee 可能在 3 至 4 bps 左右，ETH/USDC 也可能落在这个量级。但这不是固定答案，最佳参数取决于当时的 market condition、capital amount 和 range。添加更多有效 pair，可以提高资产在各个价格区间被使用的概率，进而增加潜在收入。

有一组 backtest 比较了六个 Aqua position 与 Uniswap 的结果，Aqua 的 fee generation efficiency 最多达到约 4 倍。再次强调，这只是用过去 365 天数据完成的 simulation，不是未来结果保证，也不是 financial advice。

我们还推出了 leaderboard。排名依据不是 TVL，因为 shared liquidity 结构没有传统意义上的 TVL；也不是用户声明的 yield，而是 position 实际产生的 volume。成交量越多，理论上能获取的 fee 越多。因此真正困难的工作，是找到合理的 fee 与 price range 组合。

1inch 还会发布进一步研究，解释我们推导的数学方法，帮助计算 range、fee 和投入资本之间的合适组合。它是技术工具，不是投资建议。

**主持人：** 最后一个问题。你不必公开全部“答案”，但能否给社区一些方向：当前有哪些交易对的效率特别低，LP 可能通过补充流动性改善市场？

**Sergej Kunz：** 我对现有市场和交易对做了较深入的研究，并把结果做成 3D visualization。通过这个图可以看到潜在的 low-hanging fruit。我计划把它公开在自己的站点，让大家自行研究。

有些市场已经非常 liquid，和现有 LP 竞争很难，但只要价格变化，仍可能产生 arbitrage volume。对于 UNI、AAVE 这类波动较大的 token，如果用户用对 USDC 的 position 并设置合适 fee，在大幅上涨、下跌或恢复性波动时可能获得成交量。但这只说明市场机制，并不保证获利。range、fee、impermanent loss、smart contract、asset price 和流动性条件都会改变结果。

**主持人：** Sergej，祝贺你们在这个行业坚持这么久。很多团队已转向 AI 或其他方向，1inch 从早期一路走到现在。也祝贺 Aqua 共享流动性协议正式上线。用户可以在 1inch 的 Aqua 页面阅读研究、查看数据和激励计划。你提到激励会持续三个月。感谢参加节目。

**Sergej Kunz：** 谢谢邀请，很高兴来这里交流。
