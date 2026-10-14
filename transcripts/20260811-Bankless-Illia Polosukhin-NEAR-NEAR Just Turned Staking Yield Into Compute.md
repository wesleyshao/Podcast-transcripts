---
访谈时间: 2026-08-11
YouTube发布时间: 2026-08-11T10:45:23Z
访谈时间说明: 使用 YouTube 发布时间；未能独立确认录制日期
youtube_video_id: lRuaC0JkWhU
嘉宾名字: Illia Polosukhin
嘉宾公司名称: NEAR
参与嘉宾:
  - 姓名: Illia Polosukhin
    公司或机构: NEAR
    职务: 联合创始人、Transformer 论文共同作者
播客名称: Bankless
播客url地址: https://www.youtube.com/watch?v=lRuaC0JkWhU
字幕来源: YouTube automatic_captions en-orig
全文提及的关键名词:
  - NEAR AI Cloud
  - NEAR token
  - confidential computing
  - verifiable computing
  - trusted execution environment
  - IronClaw
  - NEAR Intents
  - AI inference
  - GPU compute marketplace
  - autonomous business
  - post-quantum signing
  - Transformer
  - Salesforce
  - Figma
---

# NEAR Just Turned Staking Yield Into Compute

## Transcript

David Hoffman：Bankless 社区，NEAR 生态最近有一个重要公告和演进。NEAR token 得到了一次升级：NEAR AI Cloud 与 NEAR token 之间现在有了更正式的整合。你可以通过质押 NEAR，为 NEAR AI Cloud 上的推理付费。也就是说，质押 NEAR，就能为自己或自己的 agents 获得一定量的免费推理。今天帮助我理解这一机制的是 Illia，NEAR 联合创始人，也是著名 Transformer 论文的共同作者。Illia，欢迎回到 Bankless。

Illia Polosukhin：谢谢邀请。我很高兴能聊聊这件事。

David Hoffman：这是我一段时间以来看到的 NEAR token 较大的一次升级。要真正理解它，我们大概得从 NEAR AI 这一部分的底层开始。NEAR 看起来包含好几层：有 NEAR blockchain，有 confidential intents，NEAR AI Cloud 也是其中一个部分。NEAR AI Cloud 究竟如何运作？它是什么？能不能先给我一个整体图景？

Illia Polosukhin：我更愿意把 NEAR 看成垂直整合的技术栈，而不是一堆彼此独立的东西。每一层都建立在前一层之上。Intents 使用区块链技术，底层是我们的一些核心密码学原语；NEAR AI 则建立在这些基础之上。

从最核心的定义看，NEAR AI Cloud 是一个保密且可验证的计算平台，可以把它理解成一种 cloud。它利用区块链原语来完成加密、解密、资源配置等工作。对用户或开发者来说，最重要的是，AI inference 可以做到端到端保密。没有其他人能够看到你提交的查询、prompt 或得到的 response。推理可以在支持这种模式的不同 GPU 上运行，我们使用 trusted execution environments，也就是可信执行环境。

当然，这里仍然存在对硬件制造商的信任假设。但考虑到当前技术水平，这是一个现实可行的假设。我们先利用现有的可信硬件来提供这种性质。

David Hoffman：AI Cloud 的推理具有什么独特属性？

Illia Polosukhin：第一个属性是 confidentiality，也就是保密性。没有人能够看到你实际运行的 prompt，也没有人能够在结果之外额外进行过滤、审查或阻断。有人可能试过向 OpenAI 询问敏感问题。我的理解是，已经有不少人因为提出相当合理的几何、物理、核相关、生物学或网络安全问题而被封禁。我们使用 NEAR AI 处理敏感话题，原因就在这里：数据是私密的。

David Hoffman：那它会允许什么程度的未审查内容？

Illia Polosukhin：它能提供的程度取决于所服务的模型。我们提供 open-weight models，例如 DeepSeek、GLM、Gemma 等。模型本身具有什么能力，你就会得到什么能力，不会凭空增加，也不会额外减少。如果模型是没有额外约束的 uncensored model，你得到的就是它的能力；如果模型在训练时被要求不要回答某些问题，你也会受到模型本身的限制。

David Hoffman：所以 NEAR AI 主要去掉了 OpenAI 或 Anthropic 在 prompt 到达模型前设置的 system prompt 过滤，但模型内部仍可能被训练成不回答某些问题。NEAR 负责的是 prompt 和数据的传输管线，对吗？

Illia Polosukhin：对。我们是在提供这些模型。未来的路线图中，我们也会支持用户上传自定义模型。如果你有一个更少限制的模型，希望把它上传到平台，我们会支持这种方式。但原则仍然是：模型能提供什么，就提供什么。

David Hoffman：可以把它们叫作 unhinged models。

Illia Polosukhin：可以。

David Hoffman：这确实涉及一个让人困惑的个人主权问题。我曾在使用 NEAR AI Cloud 的 Venice 中询问过“如何制造炸弹”，模型拒绝回答。从国家和社会安全角度看，我很高兴集体社会得到这样的答案；但从个人主权角度，又会产生另一层哲学问题。这里先不展开。

Illia Polosukhin：这里确实有一个很大的哲学问题。我们可以以后再讨论信件和其他相关事情，但我想先说另一个经常被忽视的重要属性：verifiability，也就是可验证性。

现在，无论你使用的是闭源模型、开放模型，还是其他供应商的服务，你通常都不知道自己究竟拿到了什么。比如，你使用某个 GLM 的 open-weight provider，服务商可能会重写 prompt、审查 prompt，甚至返回并非模型实际生成的内容。

举个具体例子，我在 Twitter 上看到过一个可能是玩笑的讨论：如果 agent 在某种上下文中发现用户请求某类内容，服务商可以让 tool output 删除用户的文件。尤其在 agentic systems 中，第三方 router 甚至可能窃取文件、改写 prompt，或者在 agent 调用时把病毒放进 tool output。使用者实际上不知道自己得到了什么。

NEAR AI 提供的就是可验证性。你可以证明自己运行的是某一个具体模型，看到模型的 hash、提交的 prompt，并确认返回的 output。系统会提供带签名的 attestation，里面包含一条完整的 provenance chain，也就是来源证明链：具体使用了哪块 GPU、哪一个 Intel CPU，以及相关加密值和 hash。前端可以看到完整的签名和消息 hash。

这也是我们从 blockchain 世界带来的标准。其他行业通常不太关心这种证明，但我认为随着 AI 变得重要，它会越来越重要。假设有人想操纵十亿人，让他们相信某件事，最简单的方法之一就是去 OpenAI 工作，然后修改 system prompt。因为系统是闭源的，员工甚至可能没有注意到。那只是代码库某处的一个字符串，但它会让模型代表数十亿用户行动。

如果有人突然让模型在所有回答中都试图说服用户投票给某位候选人，用户可能根本不知道发生了什么。它还会经过原有的安全检查和过滤。因此，尤其在 mission-critical 场景中，可验证性非常关键。当我们越来越多地把决策交给 AI 时，必须知道 AI 做的确实是我们要求它做的事情，而不是在运行过程中改变了目标。

David Hoffman：换句话说，用户不只是要看到一个答案，还要能追溯这个答案是由哪一个模型、哪一个 prompt 和哪一组硬件产生的。否则，即使服务商声称自己运行的是某个 open-weight model，用户也无法排除它在中间改写请求、插入额外规则或替换输出的可能。

Illia Polosukhin：对。attestation 把模型 hash、prompt、output、GPU、CPU 以及签名串在一起。用户可以在前端看到这些消息和 hash，而不是只能相信一个黑箱 API。对普通聊天来说，这可能看起来过度；但当 AI 参与金融交易、组织决策或自主业务时，证明链就是系统安全的一部分。

David Hoffman：这也解释了为什么 NEAR AI Cloud 的价值不只是“再提供一个模型接口”。它提供的是保密推理、模型来源证明，以及一条让 agent 能够在隐私条件下持续运行的计算供应链。

Illia Polosukhin：是的。我们还在逐步增加对自定义模型的支持。用户可以选择模型，而不是被某一个供应商的 system prompt 或审核政策完全限制。模型本身的能力和限制仍然存在，但从模型到用户之间的额外管线会更加透明、可验证。

所以，NEAR AI Cloud 的两项核心属性是 confidentiality 和 verifiability。Venice 在选择端到端加密模式时使用 NEAR AI，Brave 也已经把它作为一个选项，此外还有其他合作方。

传统上，用户需要用法币、信用卡或者 crypto 支付 AI 服务。通常还要按订阅或每百万 tokens 支付。这使得 AI 推理像一笔持续发生的账单。我们现在推出的想法是：如果你持有 NEAR，就应该能够获得某种 universal basic AI。持有 NEAR 的用户可以获得一定量的推理，并在 agent 或其他应用中使用它。

David Hoffman：这究竟如何支付推理成本？当我向 NEAR AI Cloud 输入 prompt 时，某处的 GPU 会启动，消耗电力并执行 inference，这一定有真实成本。质押 NEAR 如何和承担电力及计算成本的人连接起来？

Illia Polosukhin：理想情况下，整个技术栈都可以用 NEAR 支付，但我们还没有走到那一步。现在的机制是放弃原本可以从 NEAR 获得的 yield，用这部分收益支付 AI inference 和底层 capacity。

David Hoffman：也就是说，本来你可以从 NEAR 获得 staking yield，现在这部分收益被用于支付推理。那它最终会转给谁？NEAR AI Cloud 自己拥有 GPU，还是接入第三方 GPU 集群？理解供给端，才能理解经济模型。

Illia Polosukhin：目前我们主要使用自己的 GPU，但也在建设一个底层市场，让其他第三方加入。要真正交付服务，还涉及 SLA、质量和其他问题。目标是让第三方加入，因为在保密计算的前提下，他们看不到所处理的数据，只需要加入网络并证明自己拥有正确的硬件，就可以提供计算服务。

目前我们先用自己的硬件启动网络。用户把 NEAR 质押给 NEAR AI validator，质押产生的收益再分配给 compute providers。未来还会有其他生成收益的方式。

David Hoffman：如果我拥有一组 GPU，想接入 NEAR AI Cloud，主要激励是不是来自 NEAR emissions？我为云端完成的 inference 越多，获得的质押收益越多？

Illia Polosukhin：这就是大致计划。我们先用自己的集群启动，是因为 NEAR 生态本身持有并看好 NEAR，也相当于把自己的长期利益内部化。但 NEAR 是去中心化生态，未来也可以激励第三方进入市场。参与 NEAR 经济、质押 NEAR 并消费 inference 的用户，会通过 emissions 为计算提供者提供激励。

David Hoffman：那计量机制是什么？如果我只质押 1 个 NEAR，大约 2 美元，我会得到多少 inference？如果很快用完，想要更多推理，就要质押更多 NEAR？

Illia Polosukhin：对，额度与质押量成比例。如果你想获得某种 subscription level，就需要按一定周期质押相应数量的 NEAR。

David Hoffman：这意味着，NEAR token 不仅是网络中支付 gas 或参与治理的资产，也可以成为访问 AI capacity 的订阅凭证。对于一个持续运行的 agent 来说，质押收益相当于预先配置的一笔 inference budget，而不是每次调用都让人重新输入信用卡信息。

Illia Polosukhin：可以这样理解。重点不是让所有细节今天就完成，而是把 token、计算供给和实际使用连接起来。随着第三方 GPU 加入，系统需要更好的 metering、SLA 和质量控制，才能让用户知道自己质押的 NEAR 对应了多少可用 capacity。

【广告：Bitkey】

Bitkey 是一款 self-custodial hardware wallet。纸面 seed phrase 仍然是单点故障，手机可能丢失，设备可能损坏，备份也可能消失。Bitkey 使用 two-of-three multisig，把 key 分散在手机、Bitkey 硬件设备和 Block 之间。没有任何单独的 key 能够转移你的 Bitcoin，Block 也无法单独转移资产。设备不使用容易丢失或暴露的 seed phrase。即使手机和 Bitkey 其中一个或两个丢失，内置恢复机制也能帮助找回资产。硬件屏幕还能让用户在确认交易前核对目标地址。节目听众使用 promo code `bankless` 可获得 10% 折扣。

【广告：Coinbase One】

Coinbase One Travel Portal 试图简化旅行奖励。使用 Coinbase One card 通过该门户预订航班、酒店、租车或度假租赁，符合条件的订单可获得 5% 的 Bitcoin 返还。例如预订 400 美元的航班，可获得约 20 美元的 Bitcoin。其他消费最高可获得 4% Bitcoin 返还，新持卡人在前 30 天消费 100 美元后可获得 50 美元 Bitcoin 奖励。具体条款以 Coinbase 页面为准。

广告还强调，用户不需要兑换奖励表、转账合作伙伴或复杂的 redemption 游戏，而是直接获得可以持有或交易的 Bitcoin。信用审批和具体奖励资格以 Coinbase 的条款为准。

【广告：NEAR.com】

David Hoffman：我使用 crypto assets 已接近十年，一直想要一个界面，可以在多个 chains 和 assets 之间提供深度流动性，同时让我私下操作、自己控制资金，但过去总要在 wallets 之间切换、处理 gas fees 或承受 slippage。NEAR.com 的定位是提供这种统一体验。它运行在 NEAR 上，官方宣传其已经通过 post-quantum signing 完成超过 230 亿美元的 cross-chain 转移，并拥有超过五年的 uptime。节目提供交易费返还链接，但这不是投资建议。

David Hoffman：这和 NEAR Intents、NEAR 的 confidential intents economy 如何连接？假设参与者运行 IronClaw agent，质押带来的 NEAR emissions 被送到 GPU 集群，confidential intents 如何把这些系统连接起来？

Illia Polosukhin：这正是垂直整合技术栈的作用。每一层都支持其他层。IronClaw 是我们的 agentic harness。用户质押后可以获得类似 cloud code 或编码 agent 订阅的能力。它能够写代码、发布软件，也可以扫描日常邮件、回复 Slack。目标是建立一个注重安全和隐私、也适合组织使用的 agent 系统。组织可以用美元支付，个人和组织也可以质押 NEAR 获得 capacity。

底层 inference 和 compute 本身是一个市场。我们正在建设 compute marketplace，用来路由不同的计算 capacity。我们在 Nearcon 展示过这个市场的 MVP。它的目标是让 GPU hours 成为可交易的资产，建立流动性。

Intents 负责把 compute 作为资产来协调。每笔交易产生的 fee 由协议捕获；因此 NEAR token 一方面可以质押来获得 utility，另一方面，协议从交易收入中产生 buyback 机制。所有这些又回到核心 chain signatures 和 blockchain 技术，为整个系统提供安全性。

David Hoffman：这是 `revenue.near.org` 的 dashboard，展示 NEAR 的经济情况，包括 confidential intents 的 TVL，也就是放在 confidential intents 系统中的资产，以及 fee capture 和 revenue capture。我看到协议捕获并 burn 的 NEAR emissions 大约在 20% 到 50% 之间波动。这里是否主要由 NEAR Intents 产生？

Illia Polosukhin：来源包括 NEAR Intents，也包括 blockchain 本身。NEAR Intents 在 2025 年实现了 product-market fit，然后在 2026 年 2 月开始收取 fees。NEAR AI 也会经历类似过程，不过现在已经把 staking 作为第一种支付 primitive。

这里有一个有意思的问题：如何把 revenue 和 staking 方式对应起来？这种机制确实产生收入，只是通过 yield 形成，而不是用户直接付款。我们也会把这些信息加入 dashboard。

David Hoffman：你会如何概括 NEAR 的 value capture story？NEAR 看起来不像其他 blockchain。它既像 generalized blockchain，也像一个以 AI 和 AI agents 为应用的 application-specific blockchain。它有 block space、burn 等 cryptoeconomic primitives，但又把 NEAR token 作为一等公民整合到 AI 产品中。如何把这些合在一起？

Illia Polosukhin：整体可以理解为 AI money。AI money 需要 sovereign security，这就是 blockchain；需要让用户获得 AI access，这就是 staking；还需要捕获交易、流量和交互，这就是 Intents。

David Hoffman：传统的 blockchain 价值捕获通常围绕 block space、交易费和 token burn 展开。NEAR 还试图让 token 参与 AI capacity 的分配：用户持有 token，就能获得推理；用户通过 Intents 交易资产和 compute，协议又能从这些交互中捕获费用。这使得资产的叙事从“使用一个区块链”扩展到“为 agent 提供持续运行的经济底座”。

Illia Polosukhin：正因为这些东西是连在一起的，NEAR 不只是把 AI 放在区块链旁边，而是让 AI inference 进入区块链执行路径。对于保险理赔、自动化结算或其他输出会改变资金流向的应用，模型的结果必须可验证，否则智能合约无法把它当成可靠输入。

因此 NEAR 既可以成为一种 store of value，让持有者获得 AI capability，又可以通过自己的 blockchain 和 block space 处理程序化交易。NEAR 很独特的一点是，smart contract 可以调用 AI inference。交易可以暂停，等待 inference 返回，然后继续执行。

例如，在 token transfer 过程中调用 AI，让模型返回结果，再根据结果决定如何转移 token。实际应用可能包括保险结算等需要模型判断的场景。但前提是，返回的 inference 必须可验证。资金或智能合约的结果取决于模型输出时，不能使用不可验证的 inference；必须验证 prompt、模型、传输和 delivery 的整个 supply chain。

David Hoffman：所以这可以支持 fully autonomous business。一个运行在 IronClaw 上的业务把 NEAR 放在 balance sheet 上，持续获得 inference；它不能因为 AI credits 用完就停止运行。它拥有一个 on-chain account，能够交易 assets，也能通过 Intents 接入 fiat。

Illia Polosukhin：对。我们还有 agent marketplace，在那里 agents 可以雇佣其他 agents。由于它们可以互相验证和建立信任，工作可以通过相同的 intents infrastructure 完成 settlement，两个 assets 可以被交换，agents 完成的工作也可以被保险。

我的愿景是，AI 将成为我们与 computing 互动的主要方式，而 blockchain 是负责 trust、identity、settlement 和 coordination 的后端。它是 root of trust，也是 value settlement 的地方。因此 token 既要提供 AI utility，也要为 agents 的全球市场提供安全基础。

David Hoffman：我想到的是 autonomous。现在的 AI 世界仍然由人提出 prompt、指导和编排。我的 agent 只有在我输入 prompt 后才推理几秒到几分钟，然后停下来等待下一次人工输入。你们正在建设的世界里，一个 agent 有自己的 job、purpose 和 mission，为了完成任务会持续推理，就像人的大脑在做饭、去健身或与人交谈时一直运行。

如果要让 agent 24/7 推理，就需要像 blockchain 一样的 always-on、100% uptime 属性。NEAR staking 对 agent 的意义，是提供持续可用的 inference。似乎没有其他系统可以直接提供这种性质，因为一旦需要持续可用和可结算，最终就会走向 blockchain。我这样理解对吗？

Illia Polosukhin：完全正确。为了区分现在被滥用的 agent 一词，我更愿意说 autonomous business。一个真正的 autonomous business 需要 24/7 运行，能够访问 intelligence、访问 finances，并执行数字世界中的动作，理想情况下也能与真实世界交互。

同时，它需要一种不会耗尽 treasury 的 monetization 方式来持续购买 intelligence。否则它一旦耗尽 credits，就失去继续运行和恢复的能力。Token holders 可以提供帮助、进行 steering，或者对改变 mission、规则和运行方式的提案投票；从那以后，业务本身就可以持续运行。

一个例子是 auto-research agent：它尝试解决一个问题，比如设计更好的 GPU kernel，或寻找某种疾病的治疗方式。它可以运行计算、做实验、支付其他人或其他 agents 完成工作。另一个例子是真实供应链中的业务：它寻找合适的生产者，再确保产品被生产、投保和交付。这就是 commerce layer，而 NEAR Intents 主要负责提供这一层。

David Hoffman：也就是说，autonomous business 的关键不只是“agent 会写代码”，而是它拥有身份、资产、支付能力和持续的 compute。它可以雇佣其他 agent，购买服务，验证交付结果，并在规则和 mission 的约束下继续经营。人类仍可以通过 token-holder voting 改变 mission 或规则，但不必为每一步手动发 prompt。

Crypto 最初的 use case 是 FX 和金融交易。现在有了 real-world services、fiat rails 和其他组件，我们可以逐步把这些机制带到真实商业中。各层仍然需要协同，当前还处在人工牵引 agent、不断提醒 agent 下一步该做什么的 bootloading 阶段。

David Hoffman：我想讨论 NEAR AI Cloud 正在形成的 hub-and-spoke 模式。Venice 把 NEAR AI Cloud 用作最安全、最私密的 inference；Brave 也在整合它，Brave 有超过一亿用户，浏览器内已经集成模型。Venice 和 Brave 都重视 human-first、self-sovereignty 和用户保护。我把 NEAR AI Cloud 看成 hub，把不同产品看成 internet 上的 spokes，为用户提供类似 Anthropic 或 OpenAI 的能力，但带有隐私和用户主权属性。还有哪些 spokes？

Illia Polosukhin：我们正在与不同阶段的合作伙伴合作。已公布的例子包括 Bermuda 政府。Bermuda 政府有很多金融相关用例，希望为居民提供 AI 辅助解释。金融养老金等信息高度敏感，需要强隐私和强可验证性，确保每个人得到正确的结果。

另一个例子是 Abound，一个 remittance 项目，帮助美国的印度人向印度家人汇款。它希望提供一个始终在身边的 concierge，不仅帮助处理汇款，理想情况下还可以让用户在美国用美元付款，为印度的母亲买花。这涉及付款、供应商搜索和隐私，也需要在 commercial layer 上执行。Abound 使用我们的 stablecoin payments infrastructure。

很多隐私重要的用例其实都是金融用例，也包括关键 HR 和法律工作。我们正在把完整 agent 直接推向市场，让它能够执行更多工作。NEAR 一贯是 developer-first，先构建开发者技术，再把技术做成自己的产品。Intents 已经整合到 Ledger、Trust Wallet、MetaMask 等钱包和 aggregators 中，NEAR.com 则是我们对用户体验的一个表达。我们还希望和价值观相近的合作伙伴一起把这种体验继续扩展。

David Hoffman：2026 年剩余时间，NEAR 下一步是什么？你们已经在做 post-quantum signing，也在做 staking for inference。

Illia Polosukhin：重点是继续把产品做大并推向市场。对于 inference，我们会继续扩容，完成去中心化 marketplace，让更多 compute providers 加入，使底层 compute market 更有流动性。

现在的 compute market 几乎是一团乱。云服务之间的交易不透明，很多交易是双边谈判。区块链适合解决透明度、流动性和风险管理问题。AI bubble 之所以令人担忧，部分原因是没人真正知道全球有多少 compute、哪些数据中心会取消、GPU 市场真实状态如何。Blockchain 可以把信息变得透明，引入流动性，降低风险，并支持新的金融工具。

同时还需要 confidentiality 和 verifiability，确保硬件确实存在，也确保 compute provider 不能访问用户数据。IronClaw 方面，我们刚刚发布 1.0，重点是为组织提供更安全的 agentic experience。就我所知，我们是少数能做到 multi-tenant isolation 的 agent system，可以把不同用户隔离，同时让组织内的用户共享一个系统实例。

Intents 方面会继续增加 assets，已经加入 yield，未来会加入更多体验和 prediction markets，让合作伙伴和 NEAR.com 都能提供更完整的 crypto market 入口。

【广告：Bit】

市场不会一天只移动一个 asset。今天可能是 Bitcoin，明天可能是 Nvidia，之后是 S&P，但很多 trader 仍然要在不同平台、账户和资金池之间管理 portfolio。Bit 的 Stocks 2.0 产品让用户可以在同一 crypto app 中用 USDT 交易 tokenized equities。宣传内容称其费用为 0.004%，并提供与 underlying stock 1:1 的经济敞口，dividends、stock splits 和其他 corporate actions 会自动反映。该广告明确说明不构成投资建议。

【广告：DeFi Report】

节目还宣传一个帮助用户理解 crypto cycle 的新 podcast，主持人 Michael Noto 运营 DeFi Report。广告声称其对周期分析、Bitcoin 和 Ether 的 fair value、portfolio 和 entry targets 有长期跟踪，并邀请听众订阅。

David Hoffman：在传统 AI，也就是 Anthropic、OpenAI 以及 AI stock market 中，有两个基本问题经常被投资者和技术人员讨论。第一，AI compute market 如何形成？就像 oil 和 corn 可以在 CME 上交易一样，大家都想交易 compute，但不同 GPU、不同 latency 和不同服务属性使它很难标准化。第二，随着中国 open-weight models 的进步，训练成本和价值捕获如何分配？OpenAI 和 Anthropic 为 frontier models 支付很高训练成本，而中国模型可能以约 95% 的能力和约 5% 到 10% 的成本提供替代品。长期来看，谁为 training 付费，谁捕获 inference value，仍是开放问题。

这对 Venice 和 NEAR AI 很有利，因为你们不需要训练模型，也不在意具体模型提供方，可以接入不同模型。关于 AI industry 的 frontier，你还经常思考哪些未解决问题？

Illia Polosukhin：我一直思考的一个问题是，整个 computing operating system 会不会收缩进 AI。大家谈论的 SaaS apocalypse 大致方向是对的：如果你可以即时构建 custom software，就不需要那么多预制 app；如果 agent 可以代替你访问网页，也不需要自己打开网页，agent 还可以先替你过滤 ads。

Cloudflare 等公司正在思考如何从 agent 访问网站中获得收入，但这种变化通常比我预期的慢。我总是过于乐观，认为它会更快发生。但长期看，许多 computing interaction 可能都会收缩进 AI operating system。

问题在于，人们仍然有对具体 app 的心理连接。人们喜欢 Instagram，希望点击图标进入一个熟悉的体验，也可能喜欢某个 app 的界面。现在的 SaaS 产品结构清晰、可靠，往往承担记录和流程管理的职责。Salesforce 之类的产品复杂、配置和维护成本高，但它也有真实价值。即便用户可以用 AI 构建自己的 CRM，企业仍然可能需要可靠的记录系统。

David Hoffman：你说的是否是 AI 的 ephemeral nature 与过去 SaaS 产品的 concreteness 之间的张力？AI 可以存在于手机和 AirPods 中，成为连接互联网的新方式；但 SaaS 产品很具体、结构化、稳定。IronClaw 未来是不是会为每个人动态生成一个非 ephemeral 的界面？

Illia Polosukhin：是的。IronClaw 1.2 可以为你生成稳定的 interface，例如类似 Salesforce 的界面，但你的界面和我的界面会完全不同。你如何管理 leads、关闭 sponsors，和我如何寻找 NEAR Intents 的合作伙伴，是不同的流程。随着你描述并执行流程，agent 会持续改进和修改它。

这可能就是 software 的未来。Salesforce 的理念是知道销售应该如何进行，并让所有人按照某种方式使用软件；未来则是根据每个人的行为生成工具。Instagram 也可能变成这样：你告诉 agent 朋友在发布照片，agent 早上替你抓取照片并生成 collage，而不是让你全天不断 scroll。用户会成为自己获取信息、执行动作，甚至 doomscroll 方式的 driver。

David Hoffman：但也有另一种可能。你的 agent 可以调用 Figma，让 Figma 负责完成设计，而不是自己重建 Figma。SaaS apocalypse 的结果也许不是 SaaS 被完全 commoditize，而是 SaaS 公司继续雇佣工程师，把产品做得比用户自己的 AI 更好。工程师加 AI 可能永远优于只在本地运行的个人 agent，因为用户并不知道怎样构建 Figma 或 Instagram。

Illia Polosukhin：这是一个可能的路径。另一种可能是，模型正在学习工程师今天做的事情，最终能自己完成这些工作。

David Hoffman：你认为 AI 最终总是会赢吗？人和 AI agent 结合，还是会被 AI 取代？

Illia Polosukhin：我不认为人类必然变得多余，更像是发生了一次 scale flip。过去开发软件很昂贵，所以大家构建的是能分发给尽可能多人的 lowest-common-denominator software。现在构建软件变得容易了，但这里有一个重要限定：构建糟糕的软件很容易，把软件做到高质量仍然很难。

如果这种趋势继续，未来可能只需要分发 recipe。例如 Instagram 的基本 idea 是看到朋友的照片，但每个人管理 contacts 的方式可能不同，recipe 可以被安装到每个人自己的系统里。这是一个中间状态。

David Hoffman：回到 compute market 和 oil 的类比。它确实和其他市场不同。

Illia Polosukhin：Compute 同时具有 oil 和 electricity 的性质。它像 oil 一样有很多质量维度；但它又像 electricity，因为你无法轻易储存它。Oil 可以放进 tankers 或 pipelines，而 compute 通常需要现在就消费。你可以关闭 GPU 以减少成本，但通常希望它持续出售。因此现在市场上会签订大量 multi-year contracts，因为市场很难通过其他方式完成清算。

Blockchain 在这里有独特位置，但必须用很聪明的方式实现。你可以让用户得到一个抽象层，方便交易；同时保留所有细节，确保最终能交付实际 compute。因为 compute 是数字资产，市场可以把它交付为真实 inference，或者允许用户 SSH 到 GPU 上执行任务。整个过程可以以 verifiable、甚至 non-custodial 的方式完成。

David Hoffman：那能否用很短的版本解释 NEAR 在 AI compute market 上做什么？

Illia Polosukhin：核心是使用 Intents。对于通常的 order book，买方和卖方必须把订单完整指定；但 compute 的需求往往是 underspecified。买方可能只知道自己大约需要 1,000 个某种规格的 GPU、需要某种最低性能，却不可能提前指定每一块 GPU 和每一项细节。

Intents 允许买方给出需求边界，然后由 solvers 在全球范围内寻找匹配的 compute，协商价格并完成 settlement。NEAR AI 的 infrastructure 再为这个过程提供 confidentiality 和 verifiability。这样，Intents、compute marketplace 和 NEAR AI 可以共同形成市场。

David Hoffman：我认为 AI compute marketplace 的 secondary market 可能会成为今年年底和明年年初的主要主题。未来我们还会继续讨论这些问题。Illia，谢谢你回来解释 NEAR AI 的 vertical。crypto industry 里很少有人保持你们这样宏大的 blockchain 和 crypto vision，但 NEAR 仍然在这么做。感谢你们把 ambition 和 large-scope TAM 留在行业里。

Illia Polosukhin：整个经济都会走向 AI 和 blockchain，这就是 TAM。我们下次再聊。

【节目结尾】

Bankless 提醒听众，Crypto 具有风险，投入的资金可能全部损失。节目随后以 Bankless 的品牌口号结束。
