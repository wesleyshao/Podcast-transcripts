---
访谈时间: 2026-08-06
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间。"
YouTube发布时间: "2026-08-06T14:45:12Z"
嘉宾名字: "Shafi Goldwasser；Tim Roughgarden；Justin Thaler"
嘉宾公司名称: "MIT CSAIL、Simons Institute；a16z crypto、Columbia University；a16z crypto、Georgetown University"
参与嘉宾:
  - 姓名: "Shafi Goldwasser"
    公司或机构: "MIT CSAIL、Simons Institute"
    职务: "Turing Award 获得者、密码学家"
  - 姓名: "Tim Roughgarden"
    公司或机构: "a16z crypto、Columbia University"
    职务: "a16z crypto Head of Research、计算机科学教授、主持人"
  - 姓名: "Justin Thaler"
    公司或机构: "a16z crypto、Georgetown University"
    职务: "a16z crypto Research Partner、计算机科学副教授"
播客名称: "a16z crypto"
播客标题: "How Shafi Goldwasser Co-Invented Zero-Knowledge Proofs"
播客url地址: "https://www.youtube.com/watch?v=7JwErM_ANy8"
全文提及的关键名词:
  - "zero-knowledge proof"
  - "interactive proof"
  - "mental poker"
  - "simulation paradigm"
  - "prover"
  - "verifier"
  - "Arthur-Merlin proof"
  - "IP = PSPACE"
  - "multi-prover interactive proof"
  - "probabilistically checkable proof"
  - "sum-check protocol"
  - "SNARK"
  - "Fiat-Shamir transformation"
  - "Merkle tree"
  - "computational soundness"
  - "RSA"
  - "lattice-based cryptography"
  - "blockchain rollup"
  - "Zcash"
  - "verifiable computation"
  - "machine learning"
youtube_video_id: "7JwErM_ANy8"
字幕来源: "YouTube en-orig 原始字幕，结合完整上下文转写为简体中文"
原始语言: "English"
转写说明: "完整读取原始字幕后按上下文转写；结合官方节目说明校正人物、论文与协议名称，保留理论定义、历史顺序、假设边界及主持人会后讨论。"
---

# How Shafi Goldwasser Co-Invented Zero-Knowledge Proofs

## Transcript

【冷开场】

**Shafi Goldwasser：** 零知识的定义，从某种意义上说，就是在对话结束后，你会相信我的主张，但除此之外不会发现任何新信息。

最初定义交互式证明时，我们要求证明者即使拥有无限计算能力也不能欺骗验证者。多年后，研究开始假设证明者受计算能力限制。你确信他无法作弊，一部分原因变成了：他的计算资源不够，聪明不到能找到作弊方法。

**Justin Thaler：** 我一直好奇，为什么零知识与交互式证明这两个概念会一同出现？

**Shafi Goldwasser：** 答案是隐私。引入交互、随机性和小概率误差，就是为了获得隐私。后来 Goldreich、Micali、Wigderson 的论文才表明，交互和概率性还能让证明者证明传统证明无法高效表达的更强命题。

## 节目介绍

**Tim Roughgarden：** 欢迎收听 First Principles，这是 a16z crypto 团队制作的系列节目。我是 Tim Roughgarden，a16z crypto Head of Research。今天讨论密码学的一项根本突破：怎样证明一件事为真，却不揭示它为什么为真。

这个洞见产生了零知识证明，它是理论计算机科学最强大的概念之一。最初的纯理论进展，如今已成为 crypto 中发展最快的领域之一，为隐私保护系统、rollups 和可验证计算提供基础。

今天的嘉宾是 Turing Award 获得者 Shafi Goldwasser。她与 Silvio Micali、Charles Rackoff 共同发明零知识证明。参与对话的还有 a16z crypto Research Partner、Georgetown University 计算机科学副教授 Justin Thaler。

我们会讨论看似玩具的问题，比如心智扑克，怎样促使 Goldwasser 与合作者定义交互式证明和零知识；这些工作又怎样打开更深层的 verification 理论，包括 IP = PSPACE 和概率可检验证明。后者表明，复杂计算可以只查看证明的少数随机位置就完成检查。最后，我们会讨论由 SNARKs 驱动的现代区块链系统。

## 心智扑克怎样催生零知识

**Tim Roughgarden：** 今天谈区块链时，经常听到两个词：SNARKs，以及零知识意义上的隐私。二者很大程度源自交互式证明系统，尤其是著名的 GMR 论文，也就是 Goldwasser、Micali、Rackoff 的工作。请带我们回到当时：研究环境是什么样，为什么提出这些问题，又怎样走到最终结果？

**Shafi Goldwasser：** 当时当然没有 SNARKs，没有智能合约、区块链、cloud，甚至没有 World Wide Web。我是 Berkeley 的研究生，导师开了一门密码学和数论课程。课程主要讲数论，最后两讲才涉及密码学。

他介绍了 RSA。当时它几乎是唯一的公钥加密方案。他还讲到一篇“怎样玩心智扑克”的论文，作者基本还是 RSA 那几个人，只是顺序可能不同。

问题是，两个人身处世界不同地方，通过电话玩牌，手边却没有实体牌。他们怎样创建一副牌、洗牌、发牌？课后，我和 Silvio 对这个问题非常兴奋。其实我们都不怎么打牌，我甚至不知道一副牌有 52 张，因为我成长的地方当时没人打牌。

这与零知识和交互式证明有什么关系？当时已有一个协议，用加密方式定义牌组并完成发牌，也有定义说明怎样安全、合规地玩。但游戏结束后，验证双方是否遵守规则的方法，是把所有东西全部公开：每一步加密了什么、发送了哪些消息、这些动作在真实牌局中对应什么。

后来有人告诉我们，真正的 poker 不是这样玩的。牌面朝下时发生了什么，本来就不应全部公开。于是问题变成：怎样在不揭示牌面的情况下，证明你正确执行了规则？怎样证明你正确发牌，却不公开加密内容和加密随机性？

我们先为一个非常具体的问题设计协议，证明某张牌被正确打开，其中使用了数论。它不是“一切都能以零知识完成”的一般性结论，只针对一个特定语言。

但设计它时，我们意识到几件事。第一，要在不揭示全部信息的情况下完成证明，必须有交互。第二，必须允许错误概率，引入随机性。无论装备牌组还是证明步骤都包含随机性，因此证明者有极小概率骗过验证者。我们接受这一点，因为概率可以做得非常小。

证明的概念必须改变：它可以是交互式的，一方是证明者，另一方是验证者；验证者愿意接受一个很小的错误概率。这样才可能在证明过程中不揭示全部信息。

与此同时，我们还必须精确定义“没有揭示其他信息”。这后来成为零知识的定义。对当时的我们而言，它并不只是一个深奥玩具，而是全部研究生活，因为这是我们赖以毕业和发表的论文。

## 模拟范式：怎样定义“什么都没学到”

**Shafi Goldwasser：** 随后问题开始一般化。我们能否处理不止一个例子？能否定义强度不同，而不一定是 perfect 零知识的形式？

零知识的核心是：交互结束后，你相信我的 claim，却没有发现其他任何东西。可“其他任何东西”怎样定义？我们使用操作性定义：你在与证明者交互前能够进行的任何计算，交互后仍只能进行同样的计算。

证明验证者交互后得到的知识没有增加，要使用模拟范式。必须展示：无论验证者交互后拥有怎样的 view 或知识，都可以在完全没有证明者、没有真实交互时由 simulator 生成。如果能够模拟，就说明对话没有传递命题真伪以外的额外信息。这听起来很绕，但那就是起点。

**Tim Roughgarden：** 所有概念是很快形成的吗？从导师给出的题目到最终论文，哪些部分卡了很久？

**Shafi Goldwasser：** 导师并没有直接提出我们最终解决的问题。他介绍的是心智扑克论文，随后又介绍 Lipton 的一篇工作，指出原方案有漏洞，会泄露关于牌的一 bit information。于是最初问题只是：怎样连这一 bit 都不泄露？

事后看，真正的灵感是意识到，问题归结为怎样 encrypt 一 bit，并证明它是 0 或 1，却不揭示其他信息。

ideas 当时接连出现，我们很兴奋，提出了有趣定义并证明它。但研究生还有 advisor。导师会问“这个情形呢？那个情形呢？”你会发现自己没想过，只能继续补充。

最初只是心智扑克，后来一般化成零知识证明，再与 Charlie Rackoff 合作形成完整论文。论文前后投稿大约六次，一直被拒，才最终发表。过程当然有很多 bumps，但我们非常坚定。今天我的论文被拒一两次，也许不会再那样坚持；当时我们确信定义是正确的，问题也非常有意思，几乎像打一场仗。

**Tim Roughgarden：** 对下一代 PhD students 来说，这说明 tenacity 是研究轨迹的重要部分。

**Shafi Goldwasser：** 绝对如此。每次被拒后，如果你都假设审稿人无所不知，就无法继续推进。我们没有这么假设。我的 co-author Silvio 也非常好斗，因此是“两个人对一个”。

## 交互最初为什么与隐私绑定

**Justin Thaler：** 给普通人解释交互式证明时，常用一个比较正式的比喻：一位数学家向另一位证明定理，不是在黑板写 50 页，而是通过 conversation 让对方相信。这里似乎没有 private information。为什么零知识与交互式证明会一起出现？答案就是 poker 吗？

**Shafi Goldwasser：** 不，答案是隐私。之所以引入交互、随机性和错误概率，就是为了保护隐私，poker 只是具体例子。

更一般地，你可能要证明一个 composite number 是两个特定形式 prime numbers 的乘积，却不直接给出 factorization。交互让这件事成为可能。

后来 Goldreich、Micali、Wigderson 展示了另一个方向：验证者可以被说服两个 graphs 不是 isomorphic。当时我们不知道怎样给出 conventional short 证明，这里却不需要零知识。由此才意识到，交互与概率性不仅服务隐私，也能证明传统证明系统难以表达的命题。

还有一点：数学家最初并不喜欢交互式证明。多年后他们接受了，但我早期在 colloquium 中把这种东西称为证明时，有人直接说“这不是证明”，因为传统证明必须 zero error。

现实中，数学家写出的证明有时完全错误，更多时候是超长复杂证明中存在很难定位的 mistake。尽管如此，如果一开始只是向数学界提议一种带错误概率的新证明概念，很难被接受。隐私提供了必要理由，随后人们才发现它还能证明更困难的定理。

## Arthur-Merlin、知识证明与复杂度理论分支

**Shafi Goldwasser：** 还有一种证明系统在我们之后几年提出，却因为我们的论文反复被拒，最后差不多同期发表，那就是 Arthur-Merlin 证明。

它通常是简化的一轮：Arthur 是验证者，Merlin 是证明者。它不考虑很多 rounds，也不讨论隐私；Arthur 基本只负责 toss coins。零知识 setting 中，验证者也许会 toss coins，但会基于隐藏随机性发送消息，让证明者不知道硬币结果，这成为验证者检查证明者是否诚实的能力来源。

我们一直用“证明定理正确”来描述问题，但今天很多应用其实是证明者知道某件验证者不知道的东西。例如证明自己知道 password，或者证明自己签署了 contract、持有 signature key。重点不一定是定理本身正确，而是“我知道该定理的证明”。如果我确实知道证明，证明就存在。

交互式证明最初同时包含交互、概率性和零知识。此后研究分裂成不同方向。复杂度理论研究者并不在意隐私，他们被另一个问题吸引：交互能否证明越来越困难、对应越来越高复杂度 class 的命题？

接着又有人问，是否真的需要交互。结果表明，可以把标准 non-交互式证明用类似纠错码的方式重写。如果原始经典证明有一个错误，编码后的新证明会出现很多错误。

这很有用，因为验证者只需随机 probe 新证明的少数位置，只要原始证明有错，就有较高概率碰到错误。由此产生一种可做局部检查的新证明 notion：可以讨论验证者读取多少内容，而不必读完整证明，也可以量化错误概率。

这个对象更容易被传统 combinatorialists 和 computer scientists 研究，并最终通向 SNARKs。原证明很长，现实应用中甚至没有合适地方存放或发送。于是要把它 compress，仍允许验证者在压缩承诺中抽查并以高概率发现原始错误。

在哈希函数和 Merkle trees 等工具下，long 证明可以被 succinctly committed。验证者只检查少量位置，却仍能在原始 uncompressed 证明错误时高概率发现问题。

## 从 multi-证明者到 IP = PSPACE

**Tim Roughgarden：** 复杂度理论这条分支，是很多人第一次接触交互式证明的方式，比如从 Arora 与 Barak 的教材读 IP = PSPACE。今天构建 SNARKs 的主要范式之一 sum-check 协议，也出现在那些证明中。你第一次听到 sum-check、IP = PSPACE 或前置结果时在哪里？交互式证明的能力是否让你意外？

**Shafi Goldwasser：** 我们已经知道它比标准证明更强，中间还有一段 multi-证明者工作。最初只有一个证明者，之后我们问：如果有两个证明者会怎样？

可以把他们想象成涉嫌犯罪的两名 suspects，crime 就是证明中存在 error。二人被关在不同房间，无法沟通。验证者向一个人提问，再向另一个提出随机问题，通过两人的答案是否 consistent，判断他们有没有联合作弊。问题是，这比 single 证明者更强吗？

Noam Nisan 当时是 MIT postdoc。他设计协议，让 two 证明者向验证者证明 permanent 的值。permanent 是著名的困难问题，属于很高的空间复杂度。这个协议已包含很多 sum-check 思想。

后来 Noam 去 Brazil 等地旅行。趁他不在，Fortnow、Karloff、Lund 等人找到了把 two-证明者协议变成 one-证明者的方法，先处理 permanent。消息迅速传播后，Weizmann 的 Adi Shamir 把它推进到最后一步，证明 IP = PSPACE。

我当时在 MIT，我们开 seminar 讨论这些结果。它当然令人惊讶，因为 ideas 并不直接，既复杂又漂亮，而且今天仍用于区块链等 concrete 协议。但我没有远离这段发展，相关研究者都在 Princeton、Berkeley、MIT 之间流动。

当一项结果一步步出现时，你会逐渐打破“只能触及表面”的心理边界，开始相信还有更多能力。真正让我意外的是，你们今天居然真的把这些理论用起来了。

## 为什么 sum-check 适合现实 SNARK

**Tim Roughgarden：** Justin，从现实性能看，sum-check 对 SNARKs 有什么独特价值？

**Justin Thaler：** 历史路径是：single-证明者交互式证明、multi-证明者交互式证明、PCP，然后最初的 SNARKs 从 PCP 构建。但从今天回看，这条路径很特别。

Fiat-Shamir transformation 的安全性仍有理论开放问题，但 practitioners 愿意采用。它提供一种 generic method 去除协议交互。因此，构建 SNARK 不一定要经过 PCP。事实上，PCP 先把协议变成 non-交互式，编译成简洁 argument 时交互又回来，最后再用 Fiat-Shamir 去掉，这条绕路并不自然。

今天更合理的方式，是直接从交互式证明或 two-证明者交互式证明出发，不经过 PCP，最后只在终点用 Fiat-Shamir 消除交互。

我个人最初研究 SumCheck，只觉得它是解决简单问题的优美协议。多年后才发现它像一把完美锤子，几乎所有问题都能成为 nail。

SumCheck 有很多 rounds of 交互。它非常适合强迫证明者真正执行大量工作，让验证者无需重复，同时不会支付太高 overhead。

密码学很昂贵。为了保持验证者快、证明 short，证明者必须提交承诺数据，通常要做大量 hashing、group operations 等。提交承诺的数据越多，生成承诺越慢，还必须额外证明已提交数据不是 random garbage。

sum-check 把交互用到极致，因此可以非常节制地使用密码学承诺。PCP 通常在内部使用 univariate 多项式，因为没有交互时要靠它保持证明 short；如果允许大量 rounds，multivariate 多项式很自然，可以每个变量对应一轮交互。社区经过 PCP 路线后，如今又回到了最初的交互式 roots。

这里的工程差异不是表面上的协议风格，而是证明者要承担的真实成本。PCP 路线倾向于先生成一大块可查询的编码，再以密码学承诺把它固定下来；承诺越大，哈希、群运算以及证明承诺内容有效的工作就越多。sum-check 则把一个多变量命题逐轮压缩，每一轮处理一个变量，验证者只保留少量随机挑战和中间值。于是协议可以把昂贵的密码学操作限制在较小的边界上，把主要工作留给更便宜的有限域运算。这也解释了历史路径为何先从 PCP 构造简洁论证，再通过 Fiat-Shamir 等方法消除交互，而今天的高性能系统又重新重视早期交互式证明的结构。理论并没有被工程抛弃，工程只是重新发现了哪一部分理论最省成本。

## 抽象：把计算写成 algebraic formula

**Shafi Goldwasser：** 这段发展最迷人的地方是抽象的力量。心智扑克最初看起来只是 curiosity，但研究逐步追问：交互是否必要，需要多少交互，怎样消除交互？

sum-check 在工程上高效，但它抽象上从哪里来？从 poker、证明知道 password、证明 contract 有效继续一般化，最终问题变成：怎样证明一项计算被正确执行。

某个算法或 Turing machine 接收输入，产生输出。你想让另一人相信输出正确，却不要求他重新运行整项计算。

如果查看算法或 machine 的规则，可以把每一步写成 algebraic formula：前一项数据经某种计算得到下一项数据。变量的取值就是实际数据。sum-check 所“求和”的，是这条公式在全部计算 steps 上的展开。

首先必须把 Turing machine 或 circuit 的计算抽象为 algebraic formula，才会出现后来可被 sum-check 处理的对象。令人惊叹的是，这种为了理论而提出的抽象，最后恰恰也是 concrete 应用的正确实现方式。

**Justin Thaler：** 完全同意。以 #SAT 为例，它要求计算 Boolean formula 的 satisfying assignments 数量。sum-check 直接对所有 assignments 求和，判断每个 assignment 是否满足 formula，几乎是完美匹配。

我第一次在 Arora 与 Barak 教材中读到 sum-check 时非常震撼。人们可能以为那只是干净的理论抽象，后来实践会另走一条路。但今天 SNARK design 的主流趋势，正是把计算 transcript 按 step-by-step 写出来，用 simple virtual machine 或 CPU 表达，再用 sum-check 证明每一步都正确。

实现细节与“求 formula 全部 satisfying assignments”不完全相同，但本质就是 1980 年代末、1990 年代初那套思维。相似处和少量偏离共同形成了今天的系统。

## 为什么许多“ZK 证明”其实没有零知识

**Shafi Goldwasser：** 我也有一个问题。最初的工作同时讨论交互、概率性和隐私。后来加入简洁性，又努力消除交互。但据我理解，人们今天称很多系统为 ZK-SNARK，实际却没有零知识。隐私是消失了、不重要了、代价太高，还是未来会回来？

**Tim Roughgarden：** 你正在和世界上每天最受这种术语错误困扰的两个人对话。

**Justin Thaler：** 今天所谓 SNARK 社区，经常把“ZK”当作“简洁”的同义词。系统可能真的有零知识，也可能没有。一些应用需要隐私，另一些不需要。当前最流行的一部分应用不需要隐私，因此很多被称作“ZK 证明”的东西实际上不是 ZK。

例如用 SNARK 扩展区块链：链下的不受信任参与者发布证明，证明自己正确执行了大量计算。所有区块链节点只检查证明，无需从头重算，这里未必需要隐私。

但 Zcash 的私密货币转账确实需要隐私，因此使用真正的 ZK。

今天流行的 SNARK 能否全部改成 ZK，只是大家暂时没做？答案略微复杂。原则上基本都能，但不同方案加入 ZK 后的性能开销不同。

我预计会发生两件事。第一，隐私应用会重新变重要。Zcash 出现得很早，随后隐私一度退居次要位置，但它会回来，届时更多系统必须真正成为 ZK。第二，最终胜出的 techniques 会天然带有 ZK，而没有明显 overhead。大概会这样演化。

## 从 information-theoretic 证明到 computational argument

**Shafi Goldwasser：** 多年来还有一项概念变化。最初定义交互式证明时，我们要求证明者是 all-powerful。无论证明者有多强，都必须证明协议正确，或把错误概率压到极小。

后来 Brassard、Chaum、Crépeau 等人提出 argument。它仍是交互式，但不再是无条件证明，而是假设证明者计算能力有限。你相信他不能骗你，是因为他没有足够计算能力找到作弊策略。Silvio 后来用类似思路走向 SNARK。

这个概念很迷人。要证明的定理甚至可能是错的，但验证者之所以接受，是因为没有计算受限证明者能让他相信反面。

最初数学家要求证明 100% 正确。然后我们说，可以允许错误概率，只要能量化为一 googol 分之一之类极小数字。再后来，我们说：对于任何只能在合理时间内计算的人，这个命题都算正确。没有人能用现实资源找出攻击，因此在实践中已经“足够正确”。

现实与一个真正正确的 reality 在可用计算资源下不可区分，于是我们把它当作正确。这种 paradigm 带来大量效率和进步，但它与最初的绝对证明当然不是同一件事。

可以把这里的可靠性分成三层。第一层是传统数学证明，错误命题不存在任何可接受证明。第二层是信息论意义上的交互式证明，即使证明者拥有无限计算能力，欺骗验证者的概率也只能是一个明确、极小的数。第三层是计算可靠性：欺骗性证明在逻辑上可能存在，但受到现实时间和资源约束的证明者无法构造出来。第三层换来了更短证明和更高效率，也意味着系统必须明确依赖什么困难假设、假设针对哪类对手、允许对手拥有多少计算资源。把“现实中找不到攻击”说成“绝对不存在攻击”会混淆这三层，而现代密码学的严谨性恰恰在于不做这种偷换。

**Justin Thaler：** 也就是错误命题的 convincing 证明可能存在，只是没人找得到。

我进入职业生涯相当久以后，才开始研究这类问题：solution 从逻辑上总是存在，但很难找到。你从第一天研究 RSA secret key 的证明 of 知识时，就已经面对这类结构。

**Shafi Goldwasser：** 这里还更进一步。不是证明难找，而是命题可能根本不正确。

**Justin Thaler：** 像一层层 onion。第一层是 solution 总存在，但关心证明者是否知道；下一层是允许 false 命题的 convincing 证明存在，只要无人能找到。不同 flavors 和 layers 构成了优美理论。

## computational 对手的思维能否用于算法分析

**Shafi Goldwasser：** 有趣的是，这种思维并没有真正进入算法世界。谈算法运行时时，通常给最坏情形保证；也有人讨论在某种概率 distribution 下更快。

可以换一种说法：也许存在让算法极慢的实例，但没有计算受限对手能找到。现实中遇到的实例都表现良好。

这和简单地说“坏例子很少”并不相同。一个坏实例可能在数学上存在，却需要超出现实能力的搜索才能构造；另一种情况则是坏实例很容易构造，只是在某个经验分布中出现概率较低。若要把密码学式论证用于算法分析，就必须说明输入来自什么分布、对手能看到什么信息、拥有多少时间，以及成功制造坏实例的概率上界。只有这些边界被写清楚，“受限对手找不到”才是可检验的保证，而不是用平均表现掩盖最坏情形。

cryptographer 会自然地把问题理解为与对手对抗。对手试图证明算法比你宣称的慢。如果受限对手永远找不到坏例子，那么“算法在极少数永远找不到的情形中很慢”，与“另一个复杂算法拥有更好最坏情形界限”，实践上有什么区别？

密码学早已接受：对手有特定计算能力；只要能在这条边界内战胜对手，无论目标是证明正确性还是维持隐私，方案就有效。其他领域也可以采用这种思维，但目前并不常见。

**Tim Roughgarden：** 最接近的 analog 也许是 smoothed analysis。它不是 computational 概念，而是 statistical 概念，说明 simplex 算法等方法的坏实例是测度为零或非常罕见。

**Shafi Goldwasser：** 对。

**Tim Roughgarden：** 人类也很难构造那些实例。偶尔 Mihalis Yannakakis 这样的研究者会发表漂亮论文，给出 local search 指数级缓慢的坏例子，但我没见过基于“受限对手找不到坏例子”的 computational treatment。这会很有意思。

## 研究发现不是线性路径

**Tim Roughgarden：** 到这里有两个反思。第一，ideas 的发展高度非线性。textbook 会用完美逻辑顺序呈现概念，好像它们本来就应该按同样顺序被发现。但交互式证明、零知识、简洁性的真实发现过程并非如此。

更根本地说，这些 ideas 甚至无法完全排成一条线，而是一张彼此丰富连接的 web。最初一同被发现的概念当时似乎属于同一问题，人们未必理解为什么；它们后来又一次次在同一个研究空间里重逢。discovery 过程不是 textbook 后来重构的路线。

第二，是具体与一般、玩具示例与一般理论之间的作用。Chris Dixon 经常说，下一项技术一开始看起来会像 toy。poker 正体现了这点。研究者的任务，是追问它根本上在讲什么，同时在最简单例子和最一般理论之间来回移动。复杂度理论的归约与 completeness，正是让一个问题代表无限问题集合。

很多远离 mathematics 或理论的人，听我说研究是高度创造性活动时会惊讶。我更愿意把它与写音乐、做雕塑或艺术创作相比，而不是 clinical、goal-driven 的活动。Shafi，游戏性和玩具示例对你建立深层理论重要吗？

## 叙事、游戏性与创造力

**Shafi Goldwasser：** 研究者各不相同。有些人没有 example 就无法推进。如果只告诉他交互式证明包含随机性和 rounds，他不知道你在说什么；必须给具体问题，比如证明 15 = 3 × 5，却不直接告诉验证者 3 和 5。

对我而言，我需要叙事。这既关于 creativity，也关于 motivation：是什么让你愿意持续工作？

人们常以为 theoretician 已经得到一个清晰问题，只需掌握很多 mathematics，再靠超强 technical skill 应用工具、解决问题。我的经历不同。脑中首先必须有一个 story，不只是孤立 math 问题。然后才从叙事中抽出具体数学问题。

心智扑克是一类叙事。Manuel Blum 还讲过 Alice、Bob 与一只 dog 的故事。两人住在不同城市，分开后都想得到 dog，于是要通过电话 coin flip 决定归属。可怎样隔着电话公平抛硬币？有了这个故事，才能开始问怎样实现。

区块链 space 同样有叙事：一个 global ledger，人们在上面发布内容、运行智能合约。它本身还不是 math 问题，但可以由此定义数学问题，再寻找 techniques。

怎样解决当然需要 creativity。如果所有人都能做，就不需要我们，论文也没有理由发表，business 也很难盈利。

对我来说，创造力需要一个能让 mind wander 的空间。seminar 很适合：别人讲自己的工作，你坐在那里不能离开，思绪开始游走。某个被描述的 idea 会碰到自己脑中的思维网络，从那里产生新连接。

## 密码学今天是否足够 rigorous

**Tim Roughgarden：** 另一个问题是，密码学今天足够 rigorous 吗？你的 Turing Award citation 除了我们谈到的工作，还特别肯定你为密码学建立 rigorous foundations。此后领域一直在假设可信度与可获得结论之间权衡。Fiat-Shamir 在不同 context 中仍有 open 安全性 questions。你怎么看严谨性与不同 plausibility 假设？

**Shafi Goldwasser：** 我们当时非常重视精确定义和证明 methods。严谨性帮助领域发展，因为好的定义往往更短、更容易解释，也能证明与其他 notions 等价，让后来研究建立在强基础之上。

今天仍然 rigorous 吗？一方面是。我们已经有一套定义 cryptographic 安全性的方法手册。设计原语时，要建立对手模型，定义对该原语而言“安全”是什么，再证明它在对手面前安全。

证明通常是归约：如果因数分解困难，或者某项假设成立，协议就安全；多方计算中也许假设双方不能私下互动。归约还应 tight。如果有人 break 协议，攻击应能转换成 fast factoring 算法、密钥泄露或其他明确后果。

我们希望学生和 practitioners 设计新协议时遵循这套 recipe。但领域规模比过去大得多，从业者也多得多，不确定每个人是否会检查其他人的工作。早期社区很小，大家会互相读论文，这还可行。

今天应用更多，为了效率会产生牺牲严谨性的诱因，不完全满足“从假设到原语的严密归约”。每个 case 应单独评价。

我接受假设。比如 factoring 假设。原则上 quantum computer 可以 factor，今天的“原则上”比过去更接近现实。研究者开始讨论真正执行 factorization 需要多少 qubits 和具体 constants。

因此领域从 factoring 转向基于格的假设。据目前所知，quantum computers 无法在多项式 time 内解决这些问题。

但基于格的系统可能达不到区块链所需效率。于是区块链可能使用双线性配对等假设，它们原则上可由经典 computer 攻击；研究者也会提出新假设，因为它们看起来合理，又能显著提高效率。例如假设知识提取只能通过某一种方式完成，再据此构建高效 scheme。

只要假设被精确陈述，并证明协议安全性等价于该假设，我认为处在 win-win。若有人 break 协议，对 a16z 也许是坏事，却对 mathematics 是好事，因为我们发现了新结构。明确归约也让攻击概率更低。

自然演化就是这样。想获得效率，就不能永远只使用最古老、最受信任的假设，必须承担经过说明的假设风险。

## 零知识在 law 中的应用

**Tim Roughgarden：** 你近 5 到 10 年仍非常活跃，包括 machine learning 和 law。进入这些应用领域，是 intellectual pivot，还是密码学与复杂度理论的同一 mindset 仍然适用？

**Shafi Goldwasser：** 先讲 law。我在 Berkeley 担任 Simons Institute director 时，与一些 law colleagues 合作。更早在 Radcliffe 待过一年，也与刚卸任 law school dean 的 Martha Minow 有交流。我们想开一门 law and 密码学或 law and 算法课程。

从叙事看，在 judge 面前证明 innocence 很像证明。当然，law 会尽量避免给事件真实性精确标注概率，因为一旦写出数字，就可能证明它不正确。evidence notion 也不等于证明。但理解 lawyers 怎样思考很有意思。

一个研究问题是 wiretapping。法院下达监听令后，police 或 FBI 可以监听一些电话。warrant 终止后，相关文件可能还要 90 天才公开。公众无法访问时，怎样监督这些 wiretaps？

我们的方案把 encryption、零知识与区块链结合：把监听记录加密后放到区块链，在法定期限内维持隐私，到未来某个时点自动公开。现有 cryptographic tools 可以处理这个法律治理问题。

另一个例子是 FBI 用专有保密软件发现 pornography ring，并在 court 声称有大量 evidence 证明被告参与非法网络活动。defense 可能要求查看 software，但一旦公开，FBI 以后就无法继续使用。

这变成一个非常自然的零知识 question：怎样证明执法者确实使用某个特定 software 得到证据，却不揭示 software 本身？证明与零知识在 law 中因此有直接用途。

## 让 AI 在回答同时给出证明

**Shafi Goldwasser：** 第二个方向是 machine learning。今天它和区块链一样热门，也提出了极好的问题。

OpenAI、Google、Meta 等聊天机器人给出答案时，为什么应该相信？假设 prompt 是 math question，模型给出答案。我们知道不能直接相信。对整体分布而言它可能 90% 正确，但某一道具体题仍可能错。

能否要求聊天机器人为具体答案提供 mathematical 证明？我们与 Stefan Wills、Paradise、Guy Rothblum、Olga Goldreich 等合作者尝试把交互式证明 notion 适配到机器学习场景。

目标是训练聊天机器人不仅给出平均 90% 正确的答案，还为每个答案学会生成证明。模型不仅学习解决问题，也学习证明自己的解法。算法已经在一些真实语言模型和任务上取得成功，我认为证明 notion 在这里有很大未来。

未来也可能需要零知识证明，例如在不揭示训练数据的情况下证明某项模型行为。可探索空间很多。

我曾和一位资深 computer scientist 朋友聊天，他对 machine learning 很怀疑。我说，我们很幸运这一切现在发生，而不是 15 年后，因为我们还来得及把已有知识用于改变技术轨迹。为什么只保持怀疑？应该进入其中。

**Tim Roughgarden：** 早期技术有很多 moving parts，模型也未统一，确实令人挫败。但正因为还早，研究者仍能影响方向。这是 computer scientist 的特权：每十年出现一轮新技术与应用，每次都带来新机会。

**Shafi Goldwasser：** 对。未来具体聊天机器人或 language-模型架构也许会被其他东西取代，但“能证明时就应证明答案”这一原则应该留下来。我们不该相信听到的一切。

我还从亲身经历得到这个判断。曾听人说聊天机器人可以做理财顾问，我很兴奋，回家后制定一套新的 investment plan。后来发现，整个方案建立在对某项 rule 的错误理解上。

我不得不找 lawyers，花 5,000 到 6,000 美元才确认它错了。之前别人说方案不对，我还坚持说：“不，它是对的，ChatGPT 告诉我的。”

**Tim Roughgarden：** 你确实是早期采用者，同时亲历所有好处和风险。这个故事最后又回到证明与知识。

**Shafi Goldwasser：** 是的，证明非常 fundamental。

**Tim Roughgarden：** Shafi，非常感谢你抽出时间。

**Shafi Goldwasser：** 再见，祝你们今天愉快。

## 会后讨论：toy 问题为什么能打开整个领域

**Tim Roughgarden：** 这场对话很精彩。先回到心智扑克。它不是唯一一个看似 toy、最后发展成深理论的例子。Justin，游戏性和玩具示例对你的研究重要吗？

**Justin Thaler：** 对我个人很重要，只是方式不同。我对 sum-check 的研究，来自用它解决 computer scientists 研究的最简单问题。协议能以有趣方式直接解决它们，让实现变快也需要新 insight。

后来发现，同样的算法和 ideas 完全一般，可以证明 arbitrary 计算。理论的力量就是可泛化性与抽象。最值得研究的对象经常是最干净、最简单，看起来像 toy 的问题，却能打开完整计算世界。

poker 尤其有趣，因为它看起来游戏化，甚至看似轻佻，实际却很复杂。computer science 史上长期存在这种模式：看起来不重要、不深刻的游戏化 topic，最终解锁整个领域的核心概念。

**Tim Roughgarden：** crypto 行业常谈 memes 与叙事。很多著名研究论文，真正广为流传的是第二页那个简单 example。知道 example 的人，可能是读完整论文者的 1,000 倍。

graph-coloring 零知识协议也许就是一种早期 meme。它把理论变成能够传播的对象，至少按 1980 年代 ideas 传播速度来看如此。

证明结果、发展理论还不够。要让理论成功，必须让别人理解、兴奋并继续建设。simple example 可以传达一般理论的 essence。

Shafi 也明确说叙事对研究重要。比如 Alice 与 Bob 隔电话 coin flip，或者今天的全球分布式账本。研究者把叙事转成 mathematics，给出定义，说明想要的性质，再设计协议、定理和 guarantees。industry 中叙事帮助 project 成功，理论研究也类似。

**Justin Thaler：** clear goal 很有澄清作用。人类从 ancient Greeks 起两千年都使用同一种 mathematical 证明：写在书里，逐步检查。交互式证明是自然一般ization，却被当时数学家厌恶。现实中数学家也通过 conversation 互相说服，但最终仍重视 written formal 证明。

有了正确模型，才会出现正确协议，再产生更多结果。没有交互式-证明模型，就没有 sum-check；没有复杂度 theorist 发明 sum-check，就没有最终支撑全球 digital infrastructure 的实际 SNARKs。

ideas 还会来回发展。有时先出现算法，研究者再退后一步问：它究竟解决什么问题，为什么觉得它好，有哪些性质？写清性质后，再从 clean slate 出发，也许会找到比原算法更好的方案。这就是抽象的力量，但没有清晰叙事和 goal，就不知道该做哪种抽象。

## 新 ideas 为什么一再被拒

**Tim Roughgarden：** GMR 论文多次被拒。不了解研究的人，会以为经典结果都从天而降、一次成型，并从第一天就广受承认。现实中，authors 要反复提高表达清晰度、补 examples、创造让概念传播的 effects；社区也需要时间吸收新 ideas。为什么真正优秀的新 ideas 连 seasoned experts 都难以第一次认出？

**Justin Thaler：** experts 总想理解新工作与既有成果的关系。GMR 论文花很多篇幅解释零知识、交互式证明与其他 notions 如何相关，实际它们与旧东西根本不一样。reviewers 会不断问“这与既有研究是什么关系”。完全新反而成为劣势，因为作者无法指着某项公认工作说“这是明确的一步改进”。

**Tim Roughgarden：** 最容易理解的是：这里有一个大家已知的问题，新结果以公认指标超过 state of the art。如果是从未出现的新定义，人们不知道它有趣还是 trivial。

theoreticians 最害怕接受一篇后来发现很 trivial 的论文。为了减少这种错误，reviewers 可能对尚未完全理解的工作过度负面。

**Justin Thaler：** 从论文发表到 sum-check 展示交互式证明的全部力量花了五年，从模型最初出现算也许接近十年。我们很不擅长预测新事物的 implications。研究按定义不可预测，否则就不是研究。

Shafi 说“怎样解决问题？当然靠创造力。如果不需要创造力，别人早就做了。”这句话非常准确。
