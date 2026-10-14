---
访谈时间: 2026-08-27
访谈时间说明: "使用YouTube发布时间；字幕为完整原始字幕。"
嘉宾名字: Mo Jalil、Oskar Thoren
嘉宾公司名称: ETH Systems
参与嘉宾:
  - 姓名: David
    公司或机构: Bankless
    职务: 主持人
  - 姓名: Mo Jalil
    公司或机构: ETH Systems
    职务: 联合创始人
  - 姓名: Oskar Thoren
    公司或机构: ETH Systems
    职务: 联合创始人
播客名称: Bankless
播客url地址: https://www.youtube.com/watch?v=3xYjCDPZ5DU
youtube_video_id: 3xYjCDPZ5DU
YouTube发布时间: 2026-08-27T10:30:28Z
字幕来源: YouTube en-orig完整字幕，经上下文转写为简体中文
文字稿来源: "/Users/wesley/.codex/automations/youtube/caption_cache/3xYjCDPZ5DU.en-orig.source.txt"
原始语言: English
全文提及的关键名词:
  - Ethereum
  - ETH Systems
  - Ethereum Foundation
  - Institutional Privacy Task Force
  - PSE
  - zero-knowledge proofs
  - DeFi
  - Aave
  - Uniswap
  - Morpho
  - Lido
  - Zcash
  - stablecoin
  - tokenized deposits
  - interdealer compression
  - private RFQ
  - DVP
  - DID
  - privacy market map
  - cypherpunk
---

# Why Wall Street Still Can’t Fully Use Ethereum

## Transcript

【音乐】

David：Bankless Station，我今天请到了 Mo Jalil 和 Oskar Thoren。他们是 ETH Systems 的联合创始人。ETH Systems 是从 Ethereum Foundation 新近独立出来的团队，聚焦三个方面：Ethereum、机构和隐私。我认为这正是整个加密行业，包括 Ethereum 在内，非常迫切需要的事情，只有解决它，Ethereum 才有机会进入下一个阶段。Oskar、Mo，欢迎来到 Bankless。

Mo、Oskar：David，谢谢你邀请我们。

David：为什么 Ethereum 需要隐私？Oskar，先请你回答。

Oskar：我会说，Ethereum 是一项非常优秀的基础技术，可以作为一种中立的信用基础层运行得很好。但它显然没有把隐私内置进去，所以你会看到很多人一直在寻找解决方案，有些方案针对基础层，有些针对应用层。可以说，这就是 Ethereum 生态缺失的一块拼图，而这正是我们要做的事情。

Mo：收听 Bankless 的人可能已经知道这些，所以如果我不得不反复说同样的话，请大家见谅。对于机构来说，他们通常真正关心两件事。第一是自己的业务，第二是合规。因为这两件事，他们往往会倾向于选择自己能够控制的环境。

另一方面，公开的 Ethereum 有深厚的流动性、许多新的业务机会，也有很多已经被验证过、但可以做得更好的方法。然而，如果没有密码学，你不可能同时得到这两方面。对于机构来说，密码学是它们获得 Ethereum 好处的必要条件。

David：能不能谈谈你们各自的背景？这对你们来说并不是第一天。也许是 ETH Systems 的第一天，或者说成立第一个月，但它只是你们很长职业轨迹的下一步。我们需要了解哪些背景，才能理解你们把关于 Ethereum、隐私和机构的工作带到 ETH Systems 的原因？Mo，你先说。

Mo：我最早其实在传统金融领域。我曾经在 Goldman Sachs 构建算法交易系统，大约做了五年。因此，我很了解投资银行这类机构需要什么。之后我又在对冲基金领域工作了若干年。对我来说，那是职业轨迹中很有意思的一段时间，因为我在观察各种不同的事情。

我记得自己读到 Bitcoin white paper 时非常震撼，但那时还太早，确实早得多。几年之后，我加入了 Ethereum Foundation，负责很多亚太地区的业务拓展工作。那是去年。当时 Tomas 担任联合执行董事。那段时间有一件事变得非常明显：如果这些机构想使用公开的 Ethereum，它们就需要隐私，需要密码学。

我认识 Oskar 已经有一段时间了，所以我打电话给他，说：“Oskar，我觉得有件事很适合你，我们应该聊聊。”

Oskar：我进入 Ethereum 和加密领域大约有十年了，很早就开始关注隐私。在隐私还不是一个热门话题的时候，我就在 Status 工作，并创建了一个研发实验室。我们开发过各种点对点通信协议，用于抗审查系统、隐私系统以及相关场景。所以很长时间以来，我一直在做协议设计，关注基础设施层面的隐私和抗审查。

过去五六年，我又深入研究了 zero-knowledge proofs，做了各种相关工具，包括作为 Ethereum Foundation PSE 的早期成员参与工作。我还写过一本介绍 zero-knowledge proofs 的小书，做过与 folding schemes 相关的研究，也做过让客户端 proving 更容易的工具。

最近几年，我一直在 Ethereum Foundation 的一些项目中工作，也在隐私战略和新的 access layer 方面为他们提供建议。正如 Mo 所说，我们就是在那里认识的，并启动了 Institutional Privacy Task Force。

对我来说，一个重要变化是：过去我主要关注个人隐私。个人隐私仍然非常接近我的内心，但我注意到，机构隐私的需求非常、非常大。过去几年，随着监管变得更加清晰，情况发生了变化。很多机构实际上非常重视隐私，在某些情况下，它们对隐私的重视程度甚至高于个人。

我觉得这很令人兴奋，也意味着更大的机会。过去一年，我们一直在公共环境中开展工作，最近又把它独立成一个单独的实体，大约一个月前完成了 spinout。

Mo：补充一点。我们独立出来时，手里已经有一整年的工作成果，不是从零开始。我们做过多场 workshop，和很多不同机构进行实际合作；发布过 public goods，包括一张市场地图，梳理机构正在考虑的各种使用场景，以及这些场景如何对应到 Ethereum 的隐私解决方案。

我们还写过一些分析，讨论 private disbursements、公开 ledger 与 private rails 等问题。换句话说，虽然 ETH Systems 这个组织成立还不到一个月，但我们所做的工作不只是过去一年，背后其实有接近十年的积累。

David：Oskar，你提到过 EF 的隐私战略，也说过机构隐私和个人隐私不同。我想了解这两件事。不过先从隐私战略开始。什么是隐私战略？能不能把它讲清楚？

Oskar：这和当时 PSE 在 Ethereum Foundation 所处的背景有关。我们试图把这项工作带进 Ethereum Foundation，弄清楚它应该关注哪些隐私问题。现在这部分工作已经发生了变化，也有很多其他人在参与，所以我不想过多代表 Ethereum Foundation 讨论它当前具体在做什么。

但就我们在 Institutional Privacy Task Force 中做的事情而言，我们试图连接两个世界。一边是机构，另一边是生态系统。和机构谈话时，它们通常并不了解 Ethereum 生态。它们看到的可能只是：“这是一条 blockchain，没有隐私。”

但事实是，Ethereum 生态在不同协议、供应商和解决方案方面非常丰富。我们要做的，就是向机构解释这个空间长什么样；同时也和生态中的公司、协议工程师等沟通，告诉他们这些用户真正需要什么。

因此，我们开发了 privacy market map，讨论这些用户的具体要求。要求可能非常复杂，涉及业务需求、法律约束和具体使用场景。接着，我们把这些需求映射到一组解决方案，包括供应商和协议，再做 POC 和技术说明，展示哪些部分还缺失，以及如何组合这些 building blocks，构建出符合用户需要的协议和产品。

Mo：我快速补充一点。Oskar 提到了 PSE，可能有些听众不知道它是什么。Ethereum 生态其实已经深耕隐私很多年了。现在隐私特别热门，尤其是过去一年 Zcash 和其他隐私协议受到关注，但 Ethereum 很早就有密码学研究实验室，已经持续了大约七年。这就是 PSE，Privacy and Scaling Explorations，也就是 Ethereum 的隐私守护者，一群讨论并构建隐私解决方案的人。

David：你们说的这些是否意味着，我们在代码层面已经拥有所需的隐私解决方案，只是机构需要知道它们存在、知道怎样使用？还是说，在 Ethereum 上建设隐私系统仍然需要继续开发？我们到底处在这条演进路径的什么位置？

Oskar：这是个好问题。我会说两种情况都有。过去十年，部分工作得益于 Ethereum Foundation，也得益于 Zcash 和独立研究者。很多密码学技术已经被推动到可用程度，随后也出现了一些公司，把它们进一步做得更容易使用。

但在面对具体约束时，我们仍然有一段路要走。机构使用场景往往不是显而易见的，特别是各种具体限制。你不能简单地说：“使用一个 privacy rollup 就好了。”真正深入细节后，会发现不同机构不一定愿意接受同样的取舍。

我们和不同公司谈话时，会看到非常宽的光谱。一端是非常复杂的机构，它们拥有自己的研发部门，有二十名员工和密码学博士，已经研究这个领域多年。另一端是技术团队并不强、但想要 white-label 解决方案的机构。

它们寻找的目标也不一样。有的场景是面向零售，需要大规模 TPS；有的场景则更重视 high-assurance security。具体需要什么，完全取决于我们讨论的是哪一种用户和哪一种业务。

Mo：我不知道 Oskar 会不会反驳我，但至少对我们关注的使用场景来说，这很大程度上是一个工程问题，而不是研究问题。

【广告】

自托管已经胜出，但它仍有可用性问题。写在纸上的 seed phrase 仍然是一个单点故障。手机会丢，设备会坏，备份会消失。Bitkey 是为现实情况设计的 self-custodial hardware wallet。它采用 two-of-three multi-sig，把密钥分散到你的手机、Bitkey hardware device 和 Block 三个地方。任何单独一把密钥都不能移动你的 Bitcoin，Block 也永远不能单独移动它。

你不需要担心丢失或暴露 seed phrase。如果手机、Bitkey，甚至两者都丢了，内置的 recovery 机制仍然能让你找回资产。硬件屏幕还可以让你在批准交易前确认目标地址。重点是，在获得更多控制权的同时，不会因为一次错误就把一切置于风险之中。

【音乐】

现在下载 Bitkey，并使用促销代码 banklist，Bitkey 可享受九折。本期节目由 Bitkey 赞助。

市场不会一次只移动一种资产。今天是 Bitcoin，明天可能是 NVIDIA，接下来是 gold，然后是 S&P 500。但大多数交易者仍然要在不同平台、不同账户和不同资金池之间管理组合。

Bitget 改变了这一点。它的新 Stocks 2.0 产品让你可以直接用 USDT 交易 tokenized equities，而且就在你已经用于加密交易的同一个应用里。这不只是另一个 tokenized stock 产品。Stocks 2.0 围绕更深的流动性、更快的执行和市场最低一档的费用设计，费用只有 0.04%，并且对标的股票提供一比一的经济敞口。

股息、股票拆分和其他公司行动会自动反映，帮助你的仓位与真正想获得敞口的资产保持一致。一个平台、一个账户，却能接触多个市场，包括 crypto、equities、commodities 等，并且都可以用 USDT 访问。Bitget，让交易更聪明。你可以通过节目说明中的链接开始交易。本内容不是投资建议。

我交易 crypto 已经接近十年。这些年我用过很多钱包、交易所、aggregator 和不同的前端，但我一直在寻找同一件事：一个界面，能够覆盖多条链和大量资产，拥有深厚流动性；我可以在那里交易 perps、赚取收益、进行 confidential trading，同时仍然控制自己的全部资金。

我从来没有真正找到这样的体验。我总是在切换钱包、处理 gas fees，最后被 slippage 吞噬。near.com 不一样。它在根本上让我感觉不同：我可以从任何链完成自己想做的事情，而且所有活动都保持 confidential。【音乐】我甚至可以 confidentially earn yield。这才是 crypto 应有的工作方式。

near.com wallet 由 NEAR 驱动，已经跨链转移超过 250 亿美元，使用 post-quantum signing，在主网上运行超过五年且零停机。near.com 是在链上活动并保持控制权的简单方式。通过节目说明中的 Bankless 链接，可以返还 20% 的交易费用。本内容不是投资建议。

David：所以，研究似乎基本完成了，而工程就是 Ethereum 今天所处的阶段。研究大部分已经完成，现在主要是工程问题。能不能讲一个典型案例，谈谈你们和最普通的机构进行对话时，最常见的隐私需求是什么？

是账户余额的隐私吗，比如 stablecoins？如果它们想创建或使用 real-world assets，是不想披露自己拥有多少资产吗？还是资产转移本身？比如 business-to-business stablecoin payments，企业可能不希望把这类活动公开在链上。你们谈话中最常见的隐私需求是什么？

Mo：我可以补充一些背景。首先，我们覆盖的使用场景很广，而我们的时间通常花在那些还没有被解决的问题上。你刚才提到的 private payments、tokenized deposits 等，很多人已经了解，也有些组织在某些国家已经解决了这些问题。

我们关注的是还没有被认真研究的工作。我举几个例子。我们曾经和一家一级投资银行谈过 interdealer compressions。事情通常是这样：每天结束时，银行把所有交易交给一个受信任的第三方，而它们每年为此支付数百万美元，甚至数千万或数亿美元。

这个受信任的第三方会查看一家银行的交易和所有头寸，再查看另一家银行的交易和头寸，然后把它们 net out。没有人喜欢这样做，但大家之所以接受，是因为交易压缩有价值，而且可以降低资本要求。银行不需要准备那么多资本，也不需要执行那么多交易。

有人来问我们：“等一下，这件事能不能在没有这个第三方的情况下完成？”这正是 Ethereum 这类基础性新技术、shared state 可以带来价值的地方。它有机会在不依赖该第三方的情况下完成相同的工作。

问题在于，如果直接放到公开链上，整个世界都能看到所有东西。这是一个非常具体的使用场景。我和其他团队谈过，大多数人还没有真正理解这项业务，或者没有意识到它需要被解决。但它本身就是一项规模达数十亿美元的业务，值得认真研究。

关于 private payments，我们也和不同司法辖区的很多机构谈过。它们的需求各不相同。private payments 这个概念可能是已知的，但具体司法辖区会产生不同的排列组合，使它不再是一个简单问题。

Oskar：我们经常谈隐私，这很重要。但我不希望大家只关注隐私。如果你在构建 confidential and secure systems，安全属性同样重要，还要考虑抗审查、可扩展性等问题。

因此，很多工作也是在提高整个领域的严谨程度。机构已经拥有产品市场匹配，它们可能已经有一个每年流动数十亿美元的系统。它们要把业务迁移到 Ethereum，必须确信系统会按照预期运行。

这和 live coding 一个应用不同。你必须仔细思考系统具有什么安全属性。隐私当然是其中之一，而且是比较棘手的一项，但它只是多个属性中的一个。必须从整体上考虑这些属性，并建立技术规格。只有所有属性都满足，机构才会真正愿意迁移到 Ethereum。

David：我知道这可能不是“最流行使用场景”这个问题最令人满意的答案。也许是因为你们选择的是那些非常边缘、非常具体的问题。有没有一个已经完成端到端合作的案例？你们从和机构开始谈隐私需求，到一起做工作，最后让它以 confidential 的方式使用 Ethereum。有没有可以讲的故事？

Mo：我可以讲一个故事，但不知道能不能说出名字。

David：如果是隐私话题，我猜你们不能说。

Mo：是的，机构尤其是规模越大的机构，越不愿意分享这些信息。不过我们可以谈几个案例。

先说 payment。每个人都理解 payment：我给你付款，如果发生在链上，所有人都能看到。这是一个非常标准的场景。但在某个司法辖区，情况不标准。这个机构希望 payment confidential，而且希望把系统推广到几乎整个国家。

他们认为 blockchain 很好，payment 也很好，但必须能够为整个国家提供规模化服务。普通 payment 通常只有两个参与者：sender 和 receiver。但在这个国家，监管要求 payment 必须有四个参与者：sender、receiver、order taker，以及政府。

他们花了两到三年时间尝试用 privacy-preserving 的方式解决，而且我会把年份匿名化。他们研究了各种已有协议，但都没能以可接受的方式完成。系统能不能达到所需 TPS？计算成本会不会高到无法接受？这些问题都没有得到满意答案。

过去一年左右，我们一直在发布 market map 和分析文章，也做了一些探索性工作，研究哪些方案可能在 Ethereum 上实现。他们看到我们完成的一个 POC 后说：“等一下，我们已经尝试了 X、Y、Z，持续了三四年，也发布过一份十六页的报告，解释为什么做不到。但 Ethereum Foundation 出来的这项工作，似乎真的可能满足我们的需求。”

他们联系了我们，希望引用我们的工作，并一起构建一个真正能够解决需求的方案。这类项目的意义不仅在于解决一个有趣的问题，也不仅在于帮助少数人。它可能被规模化部署，影响数千万人。

如果我们没有做 open-source 工作，没有把结果发布出来，没有让别人看到，他们可能会把这个问题再搁置很长时间。更糟的是，他们可能转而使用某种 private network。

Oskar：机构的销售周期通常很长，所以让项目启动需要大量工作，也会涉及相当多的保密内容。你必须等很久，才能看到完整成果。

我们在 Ethereum Foundation 工作时获得的一个重要启发，也是促使我们成立 for-profit entity 的原因，是我们和很多机构进行合作时，经常有人说：“我们很想继续和你们合作，怎么付钱给你们？”我们只能回答：“不行，我们是 nonprofit，必须保持中立。”

有时对话就在这里停下了。金融机构需要一个商业对手方，而我们作为 nonprofit 必须后退，让其他人接手。但这也说明需求有多大。现在我们独立成为 for-profit entity，商业协议就容易得多，机构更容易理解，合同也更直接。

David：我听到的是，你们要做很多 bespoke solution，要针对某个合规司法辖区中特定机构的具体隐私排列组合进行建设。我的担忧是，如果一直做 bespoke work，就很难规模化。一个完美贴合的手套只适合一只手。

另一个方向是把隐私更多地内置到 Ethereum 的核心组件里，比如 Uniswap、Aave、EOA、我的地址和我的 ledger。如果这些核心功能具备隐私，Ethereum 的整体可扩展性会大得多。等到 Ethereum 有了高保真、易用、接近默认开启的隐私，机构也许可以调整一点自己的系统，适应同一个 privacy form factor。

如果大家使用同一个标准，Ethereum 和整个世界的隐私总量都会大幅增加。所以我想问，你们做的这些 bespoke work 能否规模化？难道我们不应该把隐私更多地写进 Ethereum core，而不是只在边缘做定制？

Mo：我认为两件事可以同时做。这就是 Ethereum 伟大的地方。其次，我们谈 bespoke builds，但每个市场、每个行业本身都非常大，可能涉及数亿美元甚至数十亿美元。

我们的思路不是纯粹做 bespoke builds，那确实是个糟糕的想法。我们的做法是先理解高度具体的使用场景，因为不了解问题就无法解决。然后把理解转化成可泛化、可以被其他人复用的方案。

例如 interdealer compressions 对每一家投资银行都有用。刚才提到的 multi-party DVP 也可以推广。我们的计划是泛化这些工作，并沿两个方向推进。

第一，能 open source 的部分就公开分享。这样可以让整个空间的隐私实践变得更加扎实。第二，把可复用组件放到一个位置，让它们形成一个 stack，用户可以轻松打开并使用。

我把 bespoke work 看成创业时的 idea maze。你必须进入真实问题，弄清楚什么可行。Paul Graham 说过要做那些无法规模化的事情，这在和机构合作时非常重要。机构已经拥有自己的系统，里面流动着数十亿美元。要把它们带上链，必须从它们所在的地方开始，而不能只从 DeFi-native 一侧出发。

已经有很多团队在 crypto-native 一侧工作，再往传统金融方向推进。但从 TradFi 一侧出发、把机构需求转化为 Ethereum 产品的人还不够多。两边都做，才是正确方式。

Oskar：我同意。这个领域已经投入很多资源建设 generic infrastructure，但“build it and they will come”并不总是成立，尤其是面对有非常具体要求的大型机构。

所以，先追踪具体问题，再进行泛化是有价值的。我们会通过 open-source libraries 推出 building blocks，也会写 technical specifications。规格会尽量让方案可以泛化；对于特殊情况，则清楚标明它是 special case，使组件能够被替换、插拔、模块化。

基础隐私当然非常好，我们也希望看到它。它会开启更多使用场景。但这不是我们现在的主要工作。除此之外，还要考虑 liquidity、interoperability 和不同经济区域等问题。

因此，最好的办法可能是同时利用两种路径。我们当前的第一优先级仍然是把机构带到 Ethereum 上。

Mo：再补充一点。有些机构已经运行了一百多年。你必须从它们建立业务的地方开始搭桥：“这是你们现在的业务，好，我们把它翻译过来。”如果强迫它们反过来适应 crypto-native 的方式，可能不会奏效。我们已经看到很多团队尝试这样做，但没有成功。

David：ETH Systems 是 startup 还是 nonprofit？它的法律实体是什么？

Mo：ETH Systems 是 for-profit entity。

David：是 for-profit？我本来想问，这是不是应该做成一家 startup，去追求一个真正具有 venture scale 的结果。你们确实是 for-profit。那你们是不是已经在按 KPI、TVL、volume 以及抽成模式来建设？

Mo：是的，我们是 for-profit，主要有几个原因。我们讨论过很多次。这个工作将是一个多年的旅程，而最清晰、最可持续的资金来源，是把它做成 for-profit entity。

Public goods funding 非常困难。在我看来，grants 应该给真正需要它的人。第二，我们合作的机构在最后一公里往往要求对手方必须是 for-profit，才能通过采购流程。Nonprofit 有时反而是一个 red flag，它们无法和你合作。

所以我们选择 for-profit route。不过，生态里仍有很多 sister organizations 和朋友是 nonprofit，它们可以负责实施相关工作。

Oskar：就个人经历而言，过去七年我主要与 nonprofit 合作，我非常珍视那种深度研发、public goods 和开放建设的价值。但这次的业务模式很直接，有客户愿意为某项工作付费，而我们能够帮助客户。特别是考虑到 Mo 刚才提到的 commercial counterparty 需求，做成 for-profit 很合理。

我们并不只做商业项目。我们的工作有两条 stream：一条由业务驱动，另一条是 open source。理想情况下，两者完全一致。

业务驱动的工作包括和机构交流，理解它们的业务和法律要求，再把这些要求映射为技术约束和设计。我们会做教育、architecture review、production environment 的 POC 等。

从这些工作中，我们会获得许多 business intelligence 和技术细节。有些细节无法公开讨论，但我们会把它们泛化，再用来推出 open-source building blocks，提升整个领域的能力并帮助别人理解问题。

这延续了我们在 Ethereum Foundation 做的工作，具体形式包括 POC、案例说明、关于如何实现特定属性的 write-up、open-source libraries 和 technical specifications。

这对生态本身有价值，也有助于沟通和吸引世界级人才。Open source 很难做得过多。很多安全和隐私属性必须通过 open-source solutions 来实现，不能把东西藏起来，依赖 security by obscurity。

如果要信任一个系统，就应该要求 open specifications 和 open source。这对我们极其重要。我们会在业务需求和 open-source work 之间保持平衡，一方面对需求务实，另一方面在开放工作上坚持原则，使用 permissive licensing，让其他人可以继续构建。

Mo：还有一个很重要的副作用。我们的工作经常会产生意料之外的影响。一个好处是，真正的机构可能会为某些 public goods 提供资金，最后整个生态都能使用这些成果。

David：所以你们是一个 consultant dev shop，机构付钱请你们建设技术方案？还是更接近 Uniswap、Aave：你们编写并部署链上系统，让机构的工作流具备隐私，同时追求一个大规模、可扩张的结构？

换句话说，这里有一条光谱。一端是私人付费的顾问，结果可能只是一个项目规模；另一端是一个极其可扩张的系统。你们和机构对话，观察整个市场，理解需要什么，等时机成熟后建设一个 venture scale 的产品。你们处在这条光谱的哪个位置？

Mo：对我们来说答案很清楚，是后者。我们喜欢产品。我上一家公司就是 CTO，负责构建产品；Oskar 一生都在构建产品。对于规模化解决方案来说，产品是正确路径。

但正如你说的，这是一条光谱。我们仍然需要投入大量时间理解真实的基础使用场景，采用 forward-deployed engineer 的模式，和交易台坐在一起，弄清楚他们每天在做什么。

目标是把这些学习成果转化为可规模化推出、可以大范围部署的产品。

David：你们在研究市场、获取信息、证明问题方面走到什么程度了？你们觉得自己已经足够了解未来要建设的产品，还是仍然需要大量 research and development？

Oskar：机构销售周期很长，所以在押注一个或几个产品之前，先做多次 collaboration、POC 和 architecture review，往往是有用的。我们有很多 active collaborations，但要完成这些合作、确认竞争优势和真正值得加倍投入的方向，还需要时间。

Mo：我们已经有几个想法，其中一些可能会改变行业，但还需要进一步测试 thesis。我们要真正理解那些基础问题是否已经得到回答，目前还没有完全走到那一步。

不过，市场上已经有 venture-scale business 的例子，比如 private RFQ。我个人认为 Zama 最近做的事情可能是一项很大的业务。在它之前，我不认为有很多团队把这个方向推到那种规模。

我预测未来二十四个月会出现一批类似的公司。原因是，一个典型的机构合作至少需要十八个月：前几个月和机构建立联系、进行教育；接着几个月走完 procurement；然后再花接近一年推出第一个版本。

David：现在机构真正上链、在去中心化的公开 blockchain 环境中做事的意愿有多强？答案显然是有一些。但你们谈话时，是你们去说服机构上链，还是机构主动来找你们，说“我们真的想上链，但受到这些约束”？为了让机构来到 Ethereum，你们需要做多少 selling？

Mo：这听起来可能很糟糕，但我其实不是一个很好的 salesman。大多数人是主动来找我们的。首先，这说明他们理解 blockchain 的价值。其次，要感谢 DeFi。他们看到 Aave、Uniswap 和 Lido 发生的事情，这些产品让他们非常感兴趣。

他们想要这些能力，但要以合规方式实现。所以需求实际上非常巨大。某种意义上，这可以被称为 institutional DeFi。你会看到不同组织和 DeFi protocol 正在修改自己的产品，以满足这个方向。

需求正在到来。长期关注 blockchain 的机构过去会说：“如果能这样做，那太棒了。”随着监管清晰度提高，以及 GENIUS Act 等变化，闸门开始打开。

我们并不需要做很多 selling。需求基本来自这些企业自身。它们过去做 POC，有 innovation teams 试验新东西。但去年发生了变化：CEO 有时会打电话给创新团队说：“你们已经研究这件事五年了。现在我们真的要做业务。”

David：也许事情会这样展开。Ethereum 有一个 DeFi 生态，也就是核心的 campfire，包括 Uniswap、Aave、stablecoins、Pendle、Morpho 等。我把它叫作 Ethereum 的中心，所有热度都在那里。

机构看着这一切，会说：“这很有道理，我想在那里做业务。”但在直接接入这些系统之前，可能会先出现一个非常不同、甚至相互隔离的机构生态。它会是 private 的，也符合机构的需求形式。

直接把机构接入 Ethereum core 可能太早，也太有野心。我们可能要先让机构业务逻辑在一个独立的 private sandbox 中运行。机构在那里做起来后，会说：“这个系统对我们有效。”接着有人会为它建设一种 compliant 的方式，让它接入 Morpho。

以后，这些系统再逐步交织，两个 Ethereum 版本不再完全分离，而是互相连接、共同增长。你们似乎在点头。你们是否也认为，合理的演进是先分开，再逐渐找到融合方式？

Mo：你是不是参加过我们的会议？这正是我认为事情会发生的方式。

和机构交流时，你会看到一条路径。有的机构走得更远，有的非常复杂，它们已经在思考如何和 institutional DeFi 集成，如何与其他系统组合。这正在自然发生，越成熟的参与者越早开始规划。

但机构需要学习，因为这是一个新系统、新世界。它们需要提升自己的思考能力。很多工作其实是 translation work。许多公司已经存在了一百年，它们有 compliance officer，而现有的法律框架是为旧世界写的。所有这些都需要更新。

这和 policy work 有关，也和如何把政策要求映射为技术能力有关。这是整个领域正在经历的、持续数十年的转型，还会持续很久。但更聪明、更成熟的资金会试图提前行动，抢在变化之前。

我和 asset managers 谈话时，常常会有传统资产管理机构主动说：“我们想把这些产品放到链上。我们看到你们在做什么，只需要找出实现方式。”尤其是更具前瞻性的 asset managers，他们确实很感兴趣。我几乎每周或每两周都会遇到一次这样的对话：“我们要怎样做？”

David：那最终会解锁什么？请你为我描绘一幅图景。隐私很难，crypto 的速度也比我们交易 meme coins 时慢了。我想象一下 2033 年，七年后，你们完成了需要完成的工作，机构的兴趣继续增长。一个拥有机构和隐私的世界，最乐观、最有野心的情况是什么？

Mo：对于绝大多数非 crypto-native 的人来说，最理想的情况是隐私技术变得不可见。最好的技术是你看不到它，但能获得它带来的能力。

想象一下，我可以交易 US stocks，不需要身处美国，也不需要泄露身份，因为我拥有一个数字身份系统，比如 DID。那会非常棒。

我们喜欢的思路是，不只是有数万亿美元通过链上系统，而且所有复杂的技术都隐藏在背后，但我仍然能获得今天 DeFi 的好处。我可以接触世界上任何股票和各种资产，同时得到 blockchain 的能力：可转移性、对资产的所有权，以及可编程性。

七年后，绝大多数金融基础设施在 blockchain 上运行是非常现实的。现在它已经发生了，最大的参与者都在做这件事。希望这些基础设施最终运行在 Ethereum 上。

Oskar：crypto 和 Ethereum 的一些核心属性是 transparency、auditability 和 verifiability。

我记得更早的时候，曾经和 Bitcoiners 讨论 Lightning Network 的采用。他们会说，Lightning channels 是 private 的，看不到 volume，实际上 Lightning 上有巨大的交易量，只是被隐藏了。

Ethereum 的人会回答：“你们是在忽悠我们。Lightning 是个笑话。它藏在 private state channels 后面，并不意味着那里真的发生了什么。我们当然无法验证，但没有证据表明它有真实活动。”

我把这个故事拿来作类比：如果我们把 asset transfers 做成 private，把 TVL 和 AUM 隐藏起来，那么我们也失去了让 DeFi 有趣并值得信任的一些核心属性。我们看不到底层系统，就不知道它到底有没有运行。

David：我希望保留的 verifiability 和 auditability 包括 trading volume、资产的 market cap，以及 TVL。当 private assets 存入 Morpho 时，Morpho 应该能够报告这些资产的 AUM。或者，当资产在 Uniswap 或某种 private AMM 上 confidentially traded 时，活动的真实指标仍然应该可报告。

至于是谁在交易，我其实不在乎。今天是八月七日星期五，Ethereum 上有一头价值 5500 万美元的 whale 把 stablecoins 转进 Uniswap layer one 上的某个代币。大家会说：“看，这个人来了。”因为我们看到有 5500 万美元 stablecoins 转入这个 token，市场就提前买入，试图跑在 whale 前面。这不是金融应有的工作方式。

另一个例子是 Hyperliquid 上的 trader。人们会研究交易账户，发现某个账户在 Robinhood 上市前，提前正确交易了所有即将上线的 meme coins。Auditability 很有价值，但任何人都不应该看到别人的交易、账户和全部交易历史。

完全透明在 crypto Twitter 上很有戏剧性，但对于机构来说，这是一种根本性约束。我仍然希望看到交易 volume，也希望看到资产本身被交易。除了隐藏 individual accounts，我希望保留其他大部分信息。

Oskar：完全可以做到。隐私并不意味着所有信息都隐藏。通过 cryptography、zero-knowledge proofs 等技术，你可以证明所关心的 aggregate metrics。

所以系统可以让你选择哪些信息透明，哪些信息保持隐私。Ethereum public blockchain 的 programmability 使你能够设计出同时具备两种属性的系统。

【广告】

Bankless Nation，我们为你们打造了 Bankless MCP。ChatGPT 和 Claude 擅长许多事情，但如果你问它们基础 crypto 以外的问题，比如 protocol mechanics、tokenomics，或者上周 crypto 发生了什么，它们的不足就会暴露出来。问题在于 context。

Bankless 花了近十年建立 crypto 数据档案，包括两千多份 podcast transcripts、一万篇文章，以及与真正建设这个行业的人进行的大量对话。现在，我们把这些资料整理成 Bankless MCP。你可以把它连接到 Claude 或 ChatGPT，让 AI 在整个 Bankless archive 的支持下回答 crypto 问题。

每一篇新的 Bankless article 或 episode 都会自动加入，context 会持续更新。Bankless MCP 只对 Bankless premium subscribers 开放。你可以访问 bankless.com 升级 premium，然后在几分钟内连接 MCP。这样，你使用的 AI LLM 就能更好地回答 crypto 问题。节目说明中有链接。

我们还要推出一档新 podcast，帮助大家理解和应对 crypto cycle。我们认识的最佳 crypto cycle investor 之一叫 Michael Nato，他经营 The DeFi Report。他曾在 10/10 price drop 之前给我发出 sell alert，周期分析一直非常准确。

今年我们开始每周录制 podcast episodes，讨论他的 portfolio、持仓、market structure、Bitcoin 和 Ether 的 entry targets、fair market value，以及我们处于周期的什么位置。新节目每周三发布，每期三十分钟，短而有冲击力。

我认为这轮 crypto cycle 比多数周期更难驾驭，所以让我们一起完成。无论你使用 podcast、YouTube、Apple 还是 Spotify，都可以搜索 The DeFi Report，也可以使用节目说明中的链接。现在已经有新的一期在等待你。

【音乐】

David：Ethereum 生态或 Ethereum Foundation、实际 Ethereum protocol，有什么能帮助你们解除阻碍？我觉得可能有两个方向。

一个是 DeFi ecosystem。比如 Morpho、Aave、Uniswap，能否帮助你们让这些系统更容易、更广泛地具备隐私？你们需要 Ethereum community 或 DeFi ecosystem 做什么？

另一个方向是 Ethereum Foundation 和实际的 Ethereum protocol。有没有 EIP 或 protocol upgrade，可以让你们的工作更容易？Ethereum 应该怎样帮助你们？

Mo：我先说 DeFi ecosystem。我们已经知道生态中的很多不足。比如，如果你是 Morpho 或 Aave，我已经在和其中一些团队交流。我希望它们主动来找我们，让我们一起研究怎样修改产品，使它们适合某些规模可能非常大的特殊使用场景。

所以我的请求很简单：来找我们，和我们交流，看看产品怎样一起建设。我们非常开放。

另外，我们会有 public goods，大约每三四周发布一篇 write-up。如果你做了很棒的工作，这对你自己也有好处，可以为我们的 open-source repo 做贡献。现在就可以告诉你，查看这些内容的银行数量很多。

如果你有产品，或者做出了直观、有用、令人兴奋的工具，或者你有一个 DeFi protocol，就来我们的 repo 贡献吧。Open source，fork 它，按你的方式修改它，然后贡献回来。这对你会很有帮助。

Oskar：我们和生态里很多人交流。过去一两年，大家开始更开放地思考产品可能有哪些用途。可能这部分受 retail movements、市场周期和其他因素影响。

我们希望大家对谁最适合使用某个产品或协议保持开放，也要考虑用户在什么要求和约束下运营。我们通过 privacy market map 公开这些内容。

我们在 Ethereum Foundation 也看到了一个巨大的 disconnect：机构想要的东西和生态提供的东西之间存在很大差距。我们试图搭桥，在两者之间创造 feedback loop，但这显然是一项需要全生态共同参与的工作，还有很多事情可以做。

Mo：还有最后一点。Oskar 带来了一个我非常认同的视角：cypherpunks in the boardroom。这听起来非常反直觉，因为这两类人通常不会交谈。

我们希望成为一座桥，让那些对全人类普遍有益的默认属性被内置进系统。但要做到这一点，就必须进入真正做决策的会议室。

David：让我非常乐观的一件事，是听到 Danny Ryan 分享自己在会议室里的观察。Danny 是 cypherpunk，但他和银行交流时，双方其实在说同一件事，只是使用不同的词。

这有点像 horseshoe theory。Danny 说 decentralization 很重要；银行内部的人说：“我想移除所有 counterparties。”人们会发现，这其实是同一个目标。

世界权力中心的需求和 cypherpunks 之间存在很多协同。它们似乎位于政治或其他光谱的完全两端，但正在建设的产品、需要满足的条件和真正想要的结果，可能是相同的。你们也有类似经验吗？

Oskar：我认为是这样。很多工具和 affordances，个人重视的东西和机构重视的东西，其实非常相似，包括抗审查、隐私、open source 和 security。

我觉得 Ethereum 的一大优点是，你可以同时拥有这两种系统。对于极度怀疑机构的人，他们可能会说：“我们不想和传统金融交谈。”这完全可以保留。你仍然可以在 Ethereum 上建设非常 cypherpunk 的系统：no KYC、100% anonymous 等。

但你也可以建设另一类系统，它们拥有相似的属性，只是在不同约束下设计。比如某个公司必须遵守的法律框架。

我还认为，人们可能会过于严厉地评价某些机构，只因为它们受到监管约束。和它们交谈后，你会发现很多机构也会做 regulatory arbitrage。它们只是在不同环境中运营，这和个人没有那么不同。

个人可能会想：“我买一杯咖啡时不做 private payment，因为不值得。”机构也会说：“这个合同我要在这个 legislation 或 jurisdiction 下完成，因为那里能给我想要的属性。”从更高层次看，这并没有那么不同，只是运营环境不同。如果你能给它们想要的东西，它们就会满意。

David：Oskar，你们正在做一项非常重要的工作。谢谢你们做这些事情，祝你们一切顺利。

隐私在 2026 年仍然是一个问题，整个行业仍然缺少它。越多的人参与这个问题、建设解决方案越好。就 Ethereum 而言，这可能是我能想到的最大 unlock。感谢你们来到节目，接下来请回去继续工作。

Mo、Oskar：谢谢 David，谢谢邀请。

David：Bankless Nation，你们知道规则。Crypto 有风险，但我们之所以在这里，就是因为它有风险。机构已经登陆，我们还要继续向更远的西部前进。这是一片 frontier，不适合所有人，但很高兴你们和我们一起走在 Bankless 的旅程上。非常感谢。

【音乐】
