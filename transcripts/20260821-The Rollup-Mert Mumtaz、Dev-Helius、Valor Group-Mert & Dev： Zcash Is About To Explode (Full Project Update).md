---
访谈时间: 2026-08-21
访谈时间说明: "无法确认实际访谈时间，使用 YouTube 发布时间。"
嘉宾名字: "Mert Mumtaz、Dev"
嘉宾公司名称: "Helius、Valor Group"
参与嘉宾:
  - 姓名: "Mert Mumtaz"
    公司或机构: "Helius"
    职务: "CEO"
  - 姓名: "Dev"
    公司或机构: "Valor Group"
    职务: "创始人，负责推动 Zcash 扩容；Osmosis 创始人"
  - 姓名: "Andy"
    公司或机构: "The Rollup"
    职务: "主持人"
播客名称: "The Rollup"
播客url地址: "https://www.youtube.com/watch?v=Cmq6TUnZjeE"
youtube_video_id: "Cmq6TUnZjeE"
YouTube发布时间: "2026-08-21T02:30:12Z"
字幕来源: "YouTube 原始字幕 en-orig，经上下文转写为简体中文"
全文提及的关键名词:
  - Zcash
  - Mert Mumtaz
  - Dev
  - Helius
  - Valor Group
  - Osmosis
  - Orchard
  - Ironwood
  - Tachyon
  - shielded pool
  - formal verification
  - zero-knowledge proof
  - post-quantum privacy
  - recursive proofs
  - Zcash tokenomics
  - proof of work
  - CipherPunk Technologies
  - Bitcoin
  - Ethereum
companies: []
industries:
  - 加密
  - 支付
technologies:
  - Zcash
  - 比特币
  - 零知识证明
  - 以太坊
keywords:
  - 隐私
  - 代币经济
tags:
  - 加密
  - 支付
  - Zcash
  - 比特币
  - 零知识证明
  - 以太坊
  - 隐私
  - 代币经济
---

# Mert & Dev: Zcash Is About To Explode (Full Project Update)

## Transcript

主持人：欢迎回到 The Rollup。今天我们请到 Mert Mumtaz 和 Dev，讨论 Zcash 在 Ironwood 升级之后的进展、接下来的 Tachyon 升级，以及它如何面对扩容和量子计算风险。先做一个简短的频道提示：如果你喜欢节目，请点赞并订阅。下面进入正题。

主持人：Dev，第一次来到节目，先向观众介绍一下你的背景，以及你现在在 Zcash 上做什么。

Dev：我创办了 Valor Group，基本目标是让 Zcash 具备规模化能力，解决它走向纯 proof-of-work、信用卡级别支付网络时的瓶颈。我们希望在两到三年内，让系统达到每秒五万笔以上的交易量，接近 Mastercard 或 Visa 的量级，同时做到亚秒级确认，并把整个系统推进到 post-quantum 安全。这个目标需要覆盖整个技术栈，从节点软件到钱包。实际上，今天扩容的主要阻塞点并不只在节点侧，钱包侧同样是关键限制。

我的背景是在 ZK 领域做了十多年。我们团队的 Fractal 论文是较早讨论 post-quantum recursion 的工作之一，后来整个行业逐渐采用了其中的思路，例如使用 binary fields 和 STARKs。十年过去，很多当年的研究已经变成行业共识。我还是 Tendermint 和 Cosmos 的创始团队成员，参与过从底层到上层的系统工作，后来又和其他人一起创办了 Osmosis。现在我们把这些扩容经验带到 Zcash。

主持人：你长期相信 ZK，也在 Cosmos 生态走了很长一段路，是什么让你最终决定转向 Zcash？

Dev：如果别人问我为什么做 crypto，我一直会想到 private payments 这个梦想。但它有几个很大的启动问题。首先，隐私系统需要先有用户和链上活动，否则隐私本身没有意义。其次，系统必须足够快，用户体验必须足够好，还要解决 go-to-market 问题。我们创办 Osmosis 时，认为行业剩下的几大问题是 scaling、privacy 和 MEV。到 2021 年，scaling 在很大程度上已经进入执行阶段，虽然仍有很多工程工作，但路线已经逐渐清楚。于是隐私成为更值得投入的方向。

后来 DeFi 的市场压力把我们带到了别的地方，但隐私这个目标一直没有消失。我们最终要回答的问题是：是给 Solana 加一层隐私，还是直接让 Zcash 这样的原生隐私网络赢下来？我认为后者更好。随着 AI 加速，社会会需要一种不妥协的隐私，而这种隐私必须在 base layer 上实现。因此我们决定全力让 Zcash 的隐私能力变得尽可能好，并且让普通人也能使用。

主持人：Mert，今天的主题之一是 Ironwood 之后的更新。我们上一次谈话是在升级前，当时讨论了各种可能结果。现在已经有超过 85%，可能接近 90% 的 Zcash 从 Orchard pool 迁出。过去六周到底发生了什么？哪些事情进展顺利？你们学到了什么？

Mert：先把背景再讲清楚。Zcash 团队在加强内部 red teaming 的过程中发现了一个 vulnerability。大约一年前，甚至更早，我们已经看出 AI 特别擅长暴露 security flaws，因为它可以持续、深入地检查更多代码路径。所以 Zcash 在多个核心团队中加强了内部审查、审计和 red teaming，而不只是依靠一两个团队。除了 Dev 负责的 Valor Group，还有 Shambo 的团队、Tachyon、Shielded Labs、Zotal，以及后来成立的 Zcash Labs。Zcash 有这么多真正参与协议的核心团队，这是经常被低估的优势。

在这个过程中，熟悉 Zcash 技术的 Taylor 使用当时最新的一些 AI 工具发现了一个 vulnerability。它可能允许攻击者在 Orchard pool 中伪造 shielded notes。这里有很多误导信息，因为有些人没有理解 turnstile 机制。这个问题如果发生，影响的是特定的 pool，而不是全部 Zcash 供应量；Orchard 本身只是总供应量的一部分。

当时 Zcash 的价格和关注度都很高，市场里出现了各种传言，例如“团队在无限印钱”。这在逻辑上并不成立，因为无限供应会带来无限卖压，也无法解释 shielded pool 的总规模变化。隐私系统的难点在于，完美隐私意味着某些信息必须保持私密，包括谁持有什么资产。于是你不能像 Bitcoin 那样直接把所有余额相加来验证供应量。Zcash 有 turnstile 一类的边界机制来解决可审计性问题，但它也让外部观察者更容易制造 FUD：大家可以说“这件事可能发生，也可能没有发生”，却不容易立即用公开余额反驳。

Dev 和 Sean 等人主导了多条并行工作线，包括 formal verification，以及和相关团队一起发布新的 pool。这样一来，当资产从 Orchard 迁移到 Ironwood 后，如果 turnstile 没有触发，就可以判断那次 vulnerability 没有被利用。我们在统计意义上大约有 95% 的把握，从逻辑上则接近 99.999% 地确信没有被利用。因此，过去那一轮风险基本已经过去。

更重要的问题是，以后怎样避免类似问题。对于投资者来说，不能只问“这次有没有损失”，还必须问“这种问题会不会再发生”。核心团队现在已经从数学上证明了相关电路的 soundness，也就是无法通过 undetectable counterfeit bug 伪造资产。这样，风险的数量级下降了一个数量级。未来的 Tachyon 工具还会提供 quantum-proof 能力，使用更简单的电路和算术，减少可出错的移动部件。

主持人：Dev，请用最容易理解的方式解释 formal verification。为什么 Mert 能够对没有 counterfeit notes 这么有信心？

Dev：过去要信任 Zcash，基本上要相信一群聪明工程师写了正确的 spec，也相信他们的审计没有遗漏。Bitcoin 的供应量可以通过运行 full node 来统计，因为余额是公开的。Zcash 有 shielded pools，不能直接查看每个人的余额，于是你会统计进入和离开 pool 的资产，这就是 turnstile 思路。

formal verification 做的事情是给出一个数学证明，证明代码的 implementation 与 spec 完全一致。Zcash 过去的问题不是设计了错误的 spec，而是 Orchard 的 implementation 有一个很细微的 bug，经过多年才被发现。现在我们证明了每一笔交易使用的 circuit 都满足想要的性质：如果一笔 payment 的 proof 通过，就意味着某个人拥有相应的 notes，而且交易的总输入等于全部输出。如果输入是五个 ZEC，就不可能凭空输出超过五个 ZEC。

这不是一个神秘的词。可以把它想成一串大规模的逻辑推理：如果所有棕色狗都很友善，Sally 是一只棕色狗，那么 Sally 很友善。formal verification 只是把这种推理扩展到数百万个条件。只要基础 cryptography 假设成立，经过验证的 Ironwood pool 就没有伪造问题。它清理了代码库中大量潜在的不一致，过去的争议也因此有了更明确的边界。

主持人：现在大家已经把目光放到 Tachyon。外界常说存在从 Bitcoin 向 Zcash 的迁移，尤其是考虑到 Bitcoin 的量子风险。你们在实际市场中看到了什么？Tachyon 除了量子防护，还有哪些值得关注的内容？

Mert：Zcash 相对于整个 crypto 仍然是很小的资产，甚至 Dogecoin 的市值都可能在它之上。它不需要发生大规模的 Bitcoin 迁移，只要 Bitcoin 持有者拿出一小部分资金配置 Zcash，就足以产生明显影响。如果各个主要生态里有 5% 的人配置一点 Zcash，结果就会很可观。

我把 privacy 看成 crypto 的最后一个 PVE。它并不必然与其他链的目标冲突。一个人可以继续在 Solana 上经营公司，同时在个人层面持有 Zcash。和其他争夺交易应用、launchpad 或类似产品的市场不同，真正试图成为 private money 的项目并不多。Zcash 仍然接近早期 cypherpunk 理想，也有明确的实际用途。

还有一个 network effect：匿名集不断扩大后，竞争者很难从中抽走流动性。我的一位 real estate agent 听我解释 Zcash 是什么后，很快就买了一些。他并不需要听到“马上 moon”的故事，只需要理解 private money 对某些场景有用。当然，价格也可能下跌，这不是收益承诺。一个简单、直观的产品理念，有时比复杂的互联网叙事更容易传播。

Tachyon 由多个团队协调推进，核心工作之一是 quantum proofing，另一个是降低 state growth，尤其是 nullifier 带来的问题，为 Zcash 的扩容铺路。

Dev：Tachyon 大致有四个方向。第一，是把整个隐私系统推进到 post-quantum。Ironwood 解决了一个重要问题：如果你现在把资金放进 Ironwood，即使进入休眠二十年，未来也能迁移到新的 quantum pool。Tachyon 会进一步做到 full post-quantum privacy，不再依赖一些条件性假设。即使量子计算机知道某个地址，也不能从系统中学习到交易信息。

第二，是扩容。我们会把 recursive zero-knowledge proofs 引入 Zcash。2017 年左右，我们在 Fractal 上研究 post-quantum recursion，后来这种方向被行业广泛采用，常见的名称包括 accumulation 或 folding。这个能力进入 Zcash 后，交易相关的数据量可以下降五倍以上，更重要的是，节点处理时间和 state size 不再是主要扩容维度。之后的主要限制会变成共识带宽以及钱包，而不是计算本身。

第三，是降低 metadata leakage。隐私很难，因为系统必须避免各种边缘情形泄露信息。例如 multi-signature 场景，或者用户开始签名后网络断开很久、又没有重新签名。普通用户通常只会暴露“出现过某种边缘情形”，但 Tachyon 会继续减少这类信息泄露。

第四，是钱包体验。现在的 Zcash wallet 需要同步，余额有时不会立即显示，用户会误以为资金出了问题。我们已经把同步速度提高了大约六倍，但目标是从根本上改变钱包工作方式。今天如果有一百万笔交易，钱包可能需要扫描一百万项；在 Tachyon 体系下，目标是零扫描或接近零扫描。

主持人：Cameron Winklevoss 说 Zcash 是唯一的 quantum-resistant network，随后隐私领域的人反驳说它还没有完全量子安全。Tachyon 是否是让这句话可以完整成立的关键升级？

Dev：量子安全有几个层次。第一是有没有明确的升级计划。Zcash 已经有计划，而 Bitcoin 仍然没有完全明确采用哪一种新 signature。第二是现在持有资产，能否在未来二十年保持安全。Ironwood 已经解决了 Zcash 的这个问题。第三是 privacy，在 Orchard 里已经做了很多工作，Tachyon 会消除剩余的条件性泄露。第四是还有没有其他量子升级。Tachyon 之后还会有一个升级，但它的重要性较低，因为用户已经可以安全地从旧 pool 迁移到 quantum pool。

我们已经完成了四个层次中最重要的两个，第三个预计几个月后出来。Bitcoin 需要更换 signature scheme，并处理一些历史资产的特殊情况，例如 Satoshi 的 coins。如果未来冻结所有非 post-quantum 资金，Satoshi 的 coins 可能没有简单的恢复路径。Zcash 在 Ironwood 里已经提供了 quantum recoverability，因此用户现在迁移进去就可以等待后续升级。

Mert：量子计算机可能还要很久才会真正出现，AI 也许会加速部分研究，但 error correction 等物理层瓶颈不一定能被快速解决。对于 store of value 来说，最重要的不是假设永远没有风险，而是不要出现意外。一个资产必须是低熵的载体，才能在高熵环境中储存价值。货币如果高度波动，商业活动就无法定价，储蓄和投资也会变得混乱。

如果我把钱放在这里，希望五年后它仍然存在。我不要求价格不变，但不能接受尾部风险突然把资产归零。因此量子问题最重要的是要有一份明确计划和具体时间表，让投资者可以降低对极端风险的担忧。最糟糕的做法是完全忽略量子风险。最好的情况是量子计算来得晚，但你已经准备好；最坏的情况是系统被攻破。一个路径保留选择权，另一个路径可能走向毁灭。Bitcoin 是万亿美元级资产，拥有很多聪明人，所以我相信它最终会准备好，但它现在没有理由把这个问题放到最后。

主持人：这似乎涉及去中心化网络的协调问题。为什么 Zcash 的贡献者能够达成共识、实施升级，而 Bitcoin 还没有做到？

Mert：crypto 的一个常见误区，是把 decentralization 和 uncoordinated 混为一谈。去中心化不等于没有组织，也不等于没有共同愿景。它更像是没有中间人的协调。一个项目仍需要围绕基本理想和价值观进行协调。Zcash 比较小，信息和目标更容易统一；同时它有很简单的原则：privacy matters，security is critical，网络必须能用于 ZEC payments。

Zcash 从一开始就形成了持续更新的文化。它当年率先使用 zero-knowledge proofs，大家都知道第一版不是终点，未来要不断更新 cryptography。现在要从 ZK 走向 post-quantum ZK，再考虑 private information retrieval 等新方向。与此同时，真正不该改变的东西，例如 halving schedule，也不应因为每次升级而随意修改。

Bitcoin 社区有风险厌恶的一面：网络已经达到一万亿或两万亿美元，就有人认为只要重复过去的做法就够了。但“什么都不改变”本身也是一种风险，因为历史不会机械地重复。对于 Zcash 来说，这恰好构成了改进的机会。Ironwood、Tachyon、quantum proofing 和 recoverability 都在表达同一个方向：把 Zcash 加固成真正可托付的 money 和 store of value。

主持人：CipherPunk Technologies 最近宣布要建立一支大型 Zcash mining 组织，声称可能达到 Zcash mining hash rate 的约 16%。这会让网络更去中心化，还是会因为单一组织掌握较大算力而更集中？它会怎样影响未来扩容？

Dev：大家经常误解 consensus layer 的 decentralization。Ethereum 有几十万 validator，但只看排名前五的实体，就可能已经占到 60% 以上。proof of work 更透明，因为有公开的 mining pool 追踪器，但这些追踪器通常看不到矿工背后的公司归属，例如 Foundry、Cyberpunk 或不同地区的矿工。真正深入观察后，集中程度有时比想象中更高。

挖矿存在明显规模优势。集中在有冷却条件的仓库里运营，比在家里放几台机器更有效率。CipherPunk 的加入反而增加了一个公开的矿工实体，而且它还参与治理，持有大量 Zcash，并公开发布每一项投票立场。对网络而言，多一个能够被观察、能够公开表达治理观点的参与者，是一项去中心化改善。无论如何，现在的矿工数量至少比之前多一个，这比没有新增参与者更好。

主持人：最后给刚进入 Zcash 生态的人做一个 tokenomics 速览。它有固定的 21 million supply，也使用 proof of work。它的发行和治理资金是怎样运作的？

Mert：Zcash 的高层结构模仿 Bitcoin，发布时间稍晚一些。它是在 2016 年 proof-of-work 时代启动的，没有很多后来常见的 high FDV、low float 游戏。代币从上线以来长期承压，这件事从分配角度看反而有一个好处：留下来的持有人更多是相信项目、并且在公开市场买入的人。它没有某个拥有巨大早期 bag 的 VC 在四年后集中 unlock，也没有一个秘密的集中释放计划。

Zcash 不是在所有交易所都能买到，shielded Zcash 的可用性尤其有限，某些司法辖区也会下架隐私币。但从 proof-of-work 分配方式和公开市场流动性看，它没有传统高估值 L1 那种巨额 VC 解锁悬在头顶。随着更多人理解它，分配仍有改善空间，但整体结构已经相对透明。

Dev：早期 Zcash 需要资金支持研究和开发，因为 zero-knowledge proof 研究不可能凭空完成。历史上，部分 block emissions 曾经用于资助开发团队，大约是 block rewards 的 20%，而这套机制几年前已经结束。现在这部分历史形成的资金进入一个由多签控制的 lock box，必须按照 token holder 投票的结果分配。

Zcash 的一个特点是 private token-holder voting。投票持续几周，参与者可以提交意见，外部看不到每个人的余额和投票金额，最后只能看到 aggregate totals。项目方可以提出一个 retroactive proposal，说明自己完成了某项工作，请求社区支付报酬。除此之外，还有由 DAO 管理的 upfront community grants。这是两种开放的资金来源：一种是事后奖励，一种是事前资助。

主持人：也就是说，没有新的协议收入或新的 block rewards 持续注入这个 lock box，当前主要是协议早期设定的那部分机制，它有时间边界。到 2028 年之后，社区可以重新投票决定是否延长、修改，或把全部奖励留给矿工。

Dev：对，当前仍有历史机制的延续，但它有结束时间，之后是否更新要由社区重新决定。

主持人：感谢两位回来更新。我们一直相信 shielded money 的 thesis，也很期待 Ironwood、Tachyon 和 quantum-proof money 的后续进展。感谢你们推动这条路线。

Mert、Dev：谢谢邀请。

主持人：我们再把 Ironwood 的风险边界说得更具体一些。过去外界把“隐私池里无法直接数余额”和“供应量不可审计”混为一谈。真正的情况是，系统仍然有可公开检查的输入输出边界，只是不能公开每一笔 shielded payment 的发送者和接收者。对一个 lending market 来说，如果一个池子里有一千万 USDC，另一个池子里有一百万 USDC，那么第二个池子里的 bug 只会直接影响那一百万，而不是整个市场。Zcash 的 pool 迁移和 turnstile 也提供了类似的隔离边界。

Mert：是的。之前的争论很大程度上来自大家无法从外部直接观察隐私余额，所以任何人都可以把“没有证据”包装成“可能发生过”。Ironwood 的迁移让这个问题有了可观察的结果。如果有人真的利用了 Orchard 的 counterfeit vulnerability，迁移时的 turnstile 结果应该会显示异常。没有出现这样的信号，就意味着那条攻击路径没有兑现。再配合 formal verification，对投资者来说，判断依据从“相信几个聪明的人”变成了“相信可以复核的数学性质”。

Dev：还要强调，formal verification 并不是说所有代码、所有外部依赖永远不可能出错。它证明的是指定电路和实现之间的关系，以及交易输入输出满足的约束。基础密码学假设、编译器、运行环境仍然要保持正确，但至少最关键的资产守恒关系已经被明确写成了 proof。这个变化非常重要，因为过去的审计可能发现明显问题，却很难证明不存在所有未知问题；现在我们把最核心的“不允许凭空创造资产”变成了形式化约束。

主持人：Tachyon 还会怎样影响钱包和节点？

Dev：今天钱包的痛点不只是速度慢，而是用户不知道同步到底发生了什么。钱包必须扫描大量交易，寻找哪些输出属于自己，余额暂时不显示时，用户会担心资金是否丢失。随着递归证明和新的钱包结构上线，用户不再需要把历史数据全部扫描一遍。网络将用更紧凑的证明告诉钱包它需要知道的状态。这样，用户体验会接近普通支付应用，扩容也不再由每一次历史状态增长拖慢。

Mert：这会改变 Zcash 的用户画像。真正的 private money 不能只对密码学研究者友好，它必须像普通支付工具一样容易使用。对普通用户来说，最重要的不是知道 nullifier 的定义，而是能否在几秒内看到余额、完成支付，并且不用担心未来量子计算机出现时资产突然失效。Tachyon 把 privacy、security 和 usability 放在同一条路线里。

主持人：如果 Bitcoin 将来也采用新的 signature scheme，为什么 Zcash 仍然有价值？

Mert：因为这不只是“能不能签名”的问题。Bitcoin 需要考虑当前公开地址、已经暴露的公钥、长期未移动的 coins，以及升级过程中哪些账户能够迁移。签名方案本身也有状态管理的复杂性。Zcash 的优势在于它已经把 quantum recoverability 设计成 store-of-value 路线的一部分。用户现在迁移到 Ironwood，不必等量子计算机真的出现才开始行动。

如果网络在最后一刻才升级，所有人会同时迁移，流动性、钱包软件、交易所和节点都会承受压力。提前把资产放进可恢复的 pool，相当于把迁移风险分散到更长时间。量子威胁什么时候出现当然不能精确预测，但升级准备可以提前完成。对长期资产来说，减少这种“突然需要协调所有人”的尾部风险，本身就是经济价值。

主持人：你们多次提到 Zcash 是一个小资产。小市值既意味着增长空间，也意味着流动性和治理风险。你们如何看这个平衡？

Mert：小并不等于没有用。它意味着只要很小比例的资本开始理解 private money，边际影响就可能很大。但我们没有在说 Zcash 必然上涨，也没有告诉任何人应该买入。它可以下跌，隐私币也可能受到交易所政策、司法辖区和流动性限制。我们说的是产品功能和网络定位：如果用户需要真正的隐私支付，那么目前可选择的项目并不多。

Dev：网络效应也不能只用交易所数量衡量。shielded pool 的匿名集越大，隐私越强。一个新的隐私层即使技术上不错，也需要重新吸引用户、资金和交易活动，才能达到同样的匿名集。Zcash 已经运行多年，围绕它的基础设施和开发团队也在增加。它当然还没有解决所有问题，但它在一个竞争相对不拥挤的方向上持续积累。

主持人：关于挖矿和治理，CipherPunk 如果掌握 16% hash rate，是否会带来 51% 风险？

Dev：不能只看一个百分比就下结论。proof-of-work 的安全性依赖多个矿工、矿池和实际设备拥有者，而公开矿池名称不一定等于最终控制者。大型运营商有成本优势，因此算力会自然集中在专业仓库。真正需要关心的是是否有不同实体、是否能公开表达不同治理立场、以及其利益是否与网络长期生存一致。CipherPunk 不只是增加算力，还公开持币和投票观点，这使它比一个无法识别的隐藏矿工更容易被社区监督。

Mert：去中心化不是“每个人都拥有同样的一台机器”，而是没有一个中间人可以单方面改变规则。参与者越多、观点越公开、用户越能迁移和验证，系统越有韧性。Zcash 目前有多个核心团队，这些团队在不同技术模块上协作，而不是把所有关键代码都交给一个公司。Tachyon 之所以能推进，也和这种多团队协作有关。

主持人：最后再解释一下治理资金的来源。早期的 block reward 分配不是一种永久收入，也不等于现在有人可以随意从协议抽钱。历史上的 20% block reward 机制有明确的结束时间，lock box 的资金按 token-holder 的结果分配。社区 grants 则是另一条路线，由 DAO 参与者决定事前支持哪些工作。

Dev：而且 private voting 让参与者可以表达意见，却不必公开自己的余额。最终结果是 aggregate vote totals，而不是每个地址的财富情况。这符合 Zcash 想保护隐私的整体原则。未来如果机制需要改变，社区可以在 2028 年之后重新讨论，是继续支持开发、调整比例，还是把奖励全部留给 miners。这里的关键是规则公开、时间边界清楚，不能把一次历史安排误读成永久承诺。

主持人：所以今天的核心不是一句“Zcash 要爆发”，而是三条工程路线同时推进：Ironwood 解决当前资产的 quantum recoverability，Tachyon 继续完善 post-quantum privacy 和递归证明，钱包和多团队协作则决定这些技术能否真正变成可用的 private money。感谢两位把技术、风险和 tokenomics 都讲清楚。
