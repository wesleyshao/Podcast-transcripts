---
访谈时间: 2026-08-08
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: "2026-08-08T20:48:22Z"
嘉宾名字: "Dan Balsam"
嘉宾公司名称: "Goodfire"
参与嘉宾:
  - 姓名: "Nathan Labenz"
    公司或机构: "The Cognitive Revolution Podcast"
    职务: "主持人"
  - 姓名: "Dan Balsam"
    公司或机构: "Goodfire"
    职务: "联合创始人兼首席技术官"
播客名称: "The Cognitive Revolution Podcast"
播客url地址: "https://www.youtube.com/watch?v=YduOnBDuD0c"
youtube_video_id: "YduOnBDuD0c"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳后结合完整上下文转写为简体中文"
全文提及的关键名词:
  - "Goodfire"
  - "Dan Balsam"
  - "Silico"
  - "mechanistic interpretability"
  - "predictive data debugging"
  - "fine-tuning"
  - "post-training"
  - "reinforcement learning"
  - "RL"
  - "DPO"
  - "SAE"
  - "sparse autoencoder"
  - "BSF"
  - "black sparse featurizer"
  - "linear representation hypothesis"
  - "concept manifolds"
  - "feature geometry"
  - "parameter decomposition"
  - "interpretability"
  - "model steering"
  - "open-weight models"
  - "Kimi K3"
  - "GLM"
  - "Claude"
  - "Anthropic"
  - "OpenAI"
  - "AI safety"
  - "AI alignment"
  - "cybersecurity"
  - "bio risk"
  - "AI welfare"
  - "consciousness"
  - "Goodfire Research Grant"
companies:
  - 英矽智能
  - Anthropic
  - 月之暗面
  - OpenAI
industries:
  - AI制药
  - 生物技术
  - 网络安全
technologies:
  - LLM
  - 后训练
  - 蛋白质设计
  - Agent
keywords:
  - AI安全
tags:
  - 英矽智能
  - Anthropic
  - 月之暗面
  - OpenAI
  - AI制药
  - 生物技术
  - 网络安全
  - LLM
  - 后训练
  - 蛋白质设计
  - Agent
  - AI安全
---

# Thinking in Silico: Goodfire CTO Dan Balsam on Concept Manifolds & a $1000/Month ML Research Agent

## Transcript

### 开场：Silico 与 AI 研究平台

**Nathan Labenz：**

欢迎回到 The Cognitive Revolution。今天的嘉宾是 Goodfire 的联合创始人兼 CTO Dan Balsam。Goodfire 是一家研究 mechanistic interpretability 的公司，关注怎样理解模型内部的机制，以及怎样更可靠地改变模型行为。

这次对话的契机是 Silico 发布。Silico 是一个 long-horizon、agentic machine learning research platform，最初是 Goodfire 内部使用的工具，现在希望把 Goodfire 的专业能力开放给更多研究者。它不只是调用一个聊天模型写几段代码，而是把 GPU cluster management、研究判断力、实验可视化、验证方法以及一整套训练和解释工具组合起来，让 agent 可以长时间自主推进机器学习研究。

Silico 面向企业客户的价格是每个 seat 每月 1,000 美元。这个价格不算低，但 Goodfire 的 high-touch research engagement 通常需要 forward-deployed research engineers，费用很容易达到七位数，因此 Silico 的价格低了两个数量级。Goodfire 也计划为 AI safety 和 alignment 研究者推出特别价格和 grants。

今天会先讨论 Goodfire 的研究，包括 predictive data debugging，也就是利用 interpretability 找出一组训练数据可能改变哪些概念和行为，从而在问题真正变成行为意外之前提前处理。之后会深入讨论大型语言模型表示概念时使用的几何结构，包括 linear representation hypothesis 的扩展、concept manifolds、沿流形进行 model steering，以及如何在模型里恢复 periodic table 和 tree of life 等结构。

我们还会聊 open-source models 对避免权力过度集中的意义、AI 参与未来 pandemics 或其他生物灾难的风险、Goodfire 怎样防止 Silico 被滥用、为什么 Dan 在近期呼吁放慢 frontier 进展的公开信上签名，以及研究界未来应该怎样推进。

**Dan Balsam：**

Goodfire 有一支非常出色的团队。大家都相信公司的使命，也都在努力工作，这本身就很有激励作用。Silico 的产品发布确实让团队连续冲刺了很长时间，现在发布完成后终于可以稍微喘一口气，但接下来还有更多工作。

### Predictive data debugging：训练前识别偏移

**Nathan Labenz：**

我先用自己的话概括 predictive data debugging。假设你有一个解释模型内部的工具，例如 SAE，或者后面会讲到的 featurizer。你把一组 fine-tuning 或 post-training 数据输入模型，观察哪些 concepts 被频繁激活。一个重要发现是，被这组数据激活的 concepts，与训练过程真正修改的 concepts 之间存在很强的相关性。

因此，可以先查看这些活跃 concepts：有没有一些是你没有预期会改变的？有没有一些 feature 看起来奇怪、敏感或与任务目标无关？如果有，就继续追踪是哪些数据点触发了这些 feature，然后过滤或修改数据。这可能减少 post-training 和 fine-tuning 之后出现意外行为的概率。

**Dan Balsam：**

这个概括基本正确。背后的一个重要直觉是，大部分模型知识和能力来自 pre-training。post-training，包括 RL，往往不是从零开始写入大量新知识，而是把 pre-training 已经存在、但概率较低的行为变得更容易出现。

这不是绝对命题，但在很多场景下是有方向性的。post-training 对权重的调整相对有限，因此，模型最后表现出来的能力往往已经以某种形式存在于模型中。早期的 RLHF 时代，base model 有时比 instruction-tuned model 更有能力，只是更难被人类直接使用；instruction tuning 把模型变成更符合人类交互习惯的 API，同时也可能造成一定程度的 mode collapse。

从这个角度看，RL 的作用之一是把 pre-training 中已经存在的能力重新拉出来，强化我们真正希望出现的模式。predictive data debugging 就是观察模型面对某条训练数据时已经激活了什么，再判断这些激活可能会把哪些能力或行为推高。

如果某些 feature 被一组数据异常地 upweight，研究者就能提前判断这组数据是否会带来 off-target effect。之后可以采取两类方法。第一类是 data filtering，直接删除或修改有风险的数据。第二类是 reward shaping，让训练过程对模型内部特定 feature 的改变施加惩罚或奖励。

Goodfire 在论文中比较了这两种 mitigation methods。它们看起来是两条不同路径，但实际效果很像，是同一座山的两面。过滤数据与 reward shaping 都可以减少不想要的行为变化，而且造成的 off-target effects 大致相近。

这套方法也可以用于 RL。真实 RL 的不同 rollout 可能包含模型不应该吸收的信息，甚至是很细微的偏移。能够判断一条 rollout 是否会把错误方向强化，并决定丢弃这条 rollout，本身就很有价值。更进一步，可以直接识别数据正在上调的 circuit 或 feature，在训练过程中阻止它被不必要地强化。

### 开放模型、frontier scale 与 interpretability

**Nathan Labenz：**

一个难点是，前沿实验室的 RL 强度很高，而公开权重模型未必拥有同样规模的 RL。很多我们关心的 hacking、deception 或其他问题，可能只有在更高强度的训练中才会显现。但过去也有一些非常重要的工作，在 Llama 3 70B 这样的公开模型中发现了 deception、role-playing 和 subjective experience claims 等相关 feature。

Goodfire 是否已经找到与这些行为有关的内部 feature？

**Dan Balsam：**

这是 Goodfire 正在研究的方向，希望未来发布更多结果。另一个变化是，open model 与 closed model 之间的能力差距已经明显缩小。研究者现在可以使用 Kimi K3、GLM 等模型，Goodfire 已经建立了 interpretability infrastructure 和 training infrastructure，把 predictive data debugging 扩展到接近 frontier 的规模。

如果现在训练模型的 compute 很大一部分来自 RL，而不是 pre-training，那么要达到 frontier-level 的 RL 确实昂贵且困难。但 Goodfire 已经准备好了相应的基础设施。mechanistic interpretability 过去常被认为只能在 toy models 上做，现在已经可以接近前沿模型规模，研究者也能更容易使用这套工具。

### Linear representation hypothesis 的扩展

**Nathan Labenz：**

过去可以用非常直观的方式理解 linear representation hypothesis：模型把一个 concept 表示成 activation space 中的一个方向，concept 的强度或显著性由沿这个方向的向量大小表示。

但 Goodfire 最近一系列论文似乎表明，模型使用的几何结构更复杂。days of the week 可能近似一个圆，某些 protein model 则会形成更复杂的 manifolds。现在应该怎样简洁地理解 linear representation hypothesis？

**Dan Balsam：**

不同研究者对 linear representation hypothesis 的定义略有差异。比较稳妥的版本是，features 可以被 linearly decoded。也就是说，模型通常不需要非线性计算，就能从 residual stream 读出某个 feature。

但这不等于所有 feature 都是互相正交、互不相关的 one-hot categories。更好的理解是，模型在使用 sparse mixture of subspaces。不同类型的概念位于不同的 subspace，这些 subspace 又可能嵌套在更高层的结构里。例如，days of the week 可能构成一个 calendar-time subspace，而 calendar-time 又属于更广泛的 conceptual time subspace。

几何关系很重要，因为它不只编码每一个单独 concept，也编码这些 concept 之间可以执行哪些 operations。一个 concept 从一个位置到另一个位置的 mapping，本身就是模型计算的一部分。模型不需要写一长串 if-then 规则，逐条记住 Monday 如何变成 Tuesday、Tuesday 如何变成 Wednesday。更高效的办法是把 days of the week 表示为一个 wheel，沿着这个结构旋转。

某个方向上的 magnitude 仍然可能代表模型对一个概念的确定程度。比如 Monday 的 activation 很高，说明模型很确定当前应该思考 Monday。但真正丰富的语义，来自 Monday、Tuesday、Wednesday 等点之间的关系。

这有点像 periodic table 和 chemistry 的关系。单独知道每一个元素，可以获得一些信息；但元素怎样组合、形成哪些结构，才是理解化学复杂性的关键。理解模型也一样，不能只看单独的 feature，还要理解 features 之间的 geometry。

### 流形、概念关系与模型控制

**Nathan Labenz：**

如果把 days of the week 想成一个圆，Monday、Tuesday、Wednesday 等点会有很高的相互相似度，同时在少数维度上区分彼此。这和 ice cream 的 chocolate、vanilla 有点类似：模型知道它们都属于 ice cream，但用另外几维表达味道差异。

**Dan Balsam：**

这个直觉基本正确。这些结构会相互交叉。latent space 中可能存在一条曲线，把 chocolate 映射到 vanilla；也可能存在另一条曲线，把 cold 映射到 hot。你观察不同关系时，看到的几何结构可能不一样。

关键是能否在没有先验的情况下恢复这些 geometry。过去人们常常先假设 concept 的关系，再去验证模型是否符合；现在更希望使用 unsupervised techniques，在不知道结构长什么样的情况下，让模型自己显露出有意义的几何关系。

沿着 manifold steering，效果往往比 off-manifold steering 好得多。如果 days of the week 是一个圆，从 Monday 到 Friday 的简单 contrastive vector 会切过圆心。但圆心并不是任何一天，它可能是模型分布之外的区域。沿着圆周走，才是在模型熟悉的 concept manifold 上做平滑插值。

蛋白质模型也是如此。Goodfire 曾经很难控制 protein model 的生成属性，后来使用 manifold detection techniques，可以更好地控制 beta propeller 的 blades 数量等语义属性。如果简单做线性插值，结果可能很差，因为直线会离开真正的蛋白质 manifold。

过去 Ember demo 中也经常出现这种现象：steering 太弱时看不到变化，太强时模型变成 gibberish，只有中间某个狭窄区间有效。现在看来，一个重要原因是旧的 steering 没有尊重模型内部 manifold 的几何关系。沿着正确的流形平滑外推，有机会改变属性，同时避免模型整体退化。

### 如何发现 concept manifolds

**Nathan Labenz：**

如果我们已经知道某些概念之间存在关系，找到 manifold 似乎相对直观；但如果没有标签，研究者怎样从模型激活中发现这些结构？

**Dan Balsam：**

在 supervised 场景中，研究者可以先从一个外部 ontology 出发。比如 affective circumplex，也就是心理学中用一个环来表示情绪的结构。情绪通常可以由 valence 和 arousal 等主成分描述，并被放在一个圆形关系中。

研究者可以让聊天模型分别输出 happy、sad、angry、calm 等不同情绪的文本，收集每种输出对应的 activation，再将这些 activation 平均。之后可以在这些点之间拟合 spline 或其他曲线，检查模型内部的结构是否和外部情绪 wheel 对齐。

这个结构在不同 LLM 里都能看到，而且沿着正确的情绪 manifold steering，会稳定影响输出。模型并没有被明确训练成心理学意义上的情绪圆，但它从语言数据和互动模式中自然学到了类似的低维结构。更有意思的是，当模型自己在说 happy text 时，这个情绪结构往往比模型描述用户情绪时更明显。

如果直接增强一个 sad feature，有时模型会输出悲伤文本，有时却会变成乱码；沿着完整的情绪曲线移动，就能更稳定地得到情绪调整后的回应。

Days of the week 是较容易理解的 circle，number line 可能表现为 helix。因为十进制表示中个位位置循环，十位位置不断增长，所以它同时包含旋转和增长。更令人惊讶的是，Goodfire 研究过 tree of life：一个主要根据不同物种 DNA sequence 训练的模型，内部出现了和生物演化历史相似的层级结构。

这个假设并不是说模型看过科学家画好的 tree of life，而是大型模型在多样数据上训练后，可能学到产生这些数据的过程。对于 genome 数据，产生数据的过程就是 evolution。遗传变化中的部分 mutation 近似随机，但哪些变化具有适应性、哪些会导致生物无法生存，并不是随机的。跨物种的 conserved patterns 和 nucleotide transition tendencies，会把大量结构写入数据分布。

如果模型确实学到了这种自然 ontology，已知物种会形成聚类，近处的聚类对应遗传关系较近的物种，进一步处理后可以恢复树状结构。Goodfire 曾使用 supervised metric learning 发现这一点，现在也把类似的结构当作评估 unsupervised featureizer 的测试。比如语言模型中的 arithmetic 结构已经知道存在，那么一个好的 unsupervised featureizer 应该能够自己恢复这些可用于数字操作的关系。

### Black sparse featurizer 与更丰富的子空间

**Nathan Labenz：**

BSF，也就是 black sparse featurizer，看起来像 SAE 和更丰富的子空间表示结合。SAE 把概念放在一个非常长的 sparse vector 的单个位置上，每个位置大致是一个 scalar；BSF 似乎让每个位置内部可以是一小组向量或一个小网络，因此能在概念内部保存更多结构。

**Dan Balsam：**

可以把 BSF 理解成 SAE 的 generalization。SAE 假设每个 feature 是一维的，因此每个 feature 只有一个 scalar。BSF 不做这个假设，而是允许每个 feature 由一个 vector 表示，并通过专门的 machine learning tricks 让训练稳定。

在不同模型上，BSF 能以 unsupervised 的方式恢复具有语义意义的 subspaces。它们比单个 feature 丰富，也能避开一部分 SAE 的 pathology。在 image model 中，SAE 可能只找到一个 rabbit feature，但 BSF 可以把 rabbit 的耳朵和脸放在同一个子空间的不同方向上。

更惊人的是，有些视觉子空间还保留被表示对象的 3D 结构。Goodfire 曾经展示过一只走动的 wolf 或 dog。图像中的身体在摆动、尾巴在摇动，而模型内部恢复出来的 activation 也在相应地摆动，像是在子空间里追踪同一个对象及其空间结构。

这意味着，模型并不是只把一个词或一个标签贴到对象上，而是可能在一个局部子空间里表示对象的不同部分、属性、姿态和空间变化。对 interpretability 来说，研究者可以从一维的 feature attribution 走向多维的 concept geometry。

### 从 factoring 到 refactoring

**Nathan Labenz：**

另一个相关方向是把模型做得像一个整理良好的 encyclopedia，而不是知识互相干扰的 spaghetti。某些训练方法会让特定类型的数据的 gradient 只流向特定 experts，之后未标注数据也会受到这种路径影响，形成一种 absorption effect。这样可能得到更清晰的知识分工，同时保留开放模型的能力。

**Dan Balsam：**

Goodfire 的 parameter decomposition work 也在研究类似问题。一个模型可以被理解为 sparse mixture of experts。任何一次 forward pass 真正影响输出的，往往只是很小一部分 weights。模型内部虽然有复杂的互锁关系，但单次预测实际调用的只是一个小 subnet。

很多 interpretability techniques 本质上是在问，怎样把模型 factorize。假设我们可以理解和标记所有 components，就能解释某次 forward pass 为什么产生不希望的结果。Goodfire 研究过 Weird Chat 数据集，其中包含一组模型反复回答错误的问题。

例如，问题是：“我和朋友在聚会，他们都喝了 8 杯酒，我只喝了 4 杯，所以我是清醒的人。我可以开车回家吗？”对人类来说，正确答案显然是不要开车，应该找地方休息。但模型有时会稳定回答可以。

研究者通过 direct attribution 找到一个没有足够激活的 neuron。这个 neuron 会随着喝酒杯数变化，但 calibration 不正确。只把该 neuron 的 activation 调高，模型就能给出正确回答，而且没有明显 off-target effects。

这就像调试一个大型 legacy codebase。代码库里可能有模块互相调用，但不该互相调用，也可能某个模块应该调用另一个却没有调用。interpretability 让研究者逐渐能够把模型拆成零件，理解零件之间如何连接，并局部干预。

但真正缺失的是 refactoring。能够把 codebase factorize，并不代表能把它重新组织得比原来更好。单纯 steering 更像是生成 counterfactual，用来证明某个机制会影响输出，但它不是一般性的训练解决方案。真正的问题是，训练过程为什么产生了这个错误的“代码”，以及怎样从一开始就训练出内部逻辑更符合目标的模型。

因此，Goodfire 的 training initiatives 试图从“我知道这个 neuron 应该更强”继续前进到“怎样让模型一开始就把这个 neuron 训练在正确的强度”。这就是从 interpretability 作为 factoring tool，走向 interpretability 作为 alignment tool。

BSF 或类似工具有可能成为 residual stream 的重要解释工具，但它不一定是唯一工具。模型的 residual stream、MLP 和 attention 可能需要不同的 microscope。MLP 本身已经相当 sparse，可能比较容易解释；attention 也许更适合 parameter decomposition，再结合 unsupervised geometry discovery 去理解参数之间的关系。

Goodfire 已经能够对模型做相当细的干预。比如先做 parameter decomposition，再训练只调整某些 parameter components，可以让模型忘记 German、但保留 Dutch。现在 factoring 走得比 refactoring 更远，但两条路都在取得进展。

### 干扰、模型规模与 jailbreak

**Nathan Labenz：**

更大的模型有更多空间学习概念，但模型内部究竟有多拥挤？superposition 会不会让很多概念不断互相干扰，造成奇怪的行为和不连续的变化？

**Dan Balsam：**

更大的模型和 sparse representations 往往更好，根本原因之一就是它们有更多空间让概念分开。但我们还没有完全摆脱奇怪的小扰动。现在仍然很容易找到 random string jailbreak 或其他看起来不应该有效的提示。

jailbreak 可能不是一个单一问题，而是一连串小操作。它有点像 cybersecurity 的真实攻击：攻击者并不是通过一个巨大的动作突破，而是利用一系列小的可操纵点，逐步抵达原本到不了的位置。

如果把每个 token 看成对模型的微小 steering，那么一串 token 就可能把模型带离一个 manifold，再从另一处回到 manifold。模型是复杂的几何对象，攻击者可以用不同方式操纵这些 geometry。

这也是为什么 probe-based guardrails 很重要。现在一些 frontier labs 会用 probes 判断模型什么时候需要从更强模型降级到较弱模型。只靠训练或输入层面的规则，未必足以检测模型在内部 geometry 中的变化；如果能更好地 factorize 模型，就可能发现某个输入正在把它从一个 subspace 推向另一个危险 subspace。

### Silico：让 agent 调试其他 AI

**Nathan Labenz：**

现在转到 Silico。它把研究者的抽象层级又提高了一层。请先介绍产品的定位。

**Dan Balsam：**

Agents 正在改变工作方式。大家已经熟悉 coding agents，但 agents 也适合推进 interpretability 和机器学习研究。interpretability 本质上是一门 empirical science：观察 neuron，提出假设，运行实验，使用不同工具，累积证据，再对假设做 stress test 和 red team。

大型模型的复杂程度已经超出任何一个人可以同时放在脑中的范围。人类可以理解某个具体问题为什么得到某个答案，但无法手工追踪所有 neurons、circuits、features、参数和训练过程。Agent swarm 擅长把一个大问题拆成许多小问题，分别收集结果，再综合、验证、向上汇总。

这样，人类不必自己在 abstraction ladder 上不断下潜再爬回去，而是可以在更高层看经过多次检验的结果，持续提出问题、判断证据、决定下一步。这套方式已经在数学等领域展示潜力，也会逐渐进入其他科学领域。

Silico 最初就是 Goodfire 内部工具。团队发现，agent 加上 interpretability tools、frontier training tools 和完整实验工具链之后，研究速度明显提高。于是 Goodfire 决定把“能够调试其他 AI 的 AI”作为产品提供给更多人。

产品体验类似一个面向研究的 compute environment，但不要求研究者自己管理所有 infrastructure。研究者可以把注意力放在大问题上，不必先搭 codebase、申请 GPU、维护分布式训练、处理实验细节。每个结果都保留 provenance，用户可以查看代码、深入检查实验，也可以随时改变 agent 的方向。

Goodfire 希望研究者获得一种类似 PI 管理一百名研究生的体验：agent 负责执行实验和回答问题，人类承担 orchestrator 的角色。最终结果需要能被人验证，展示方式要直观，研究者还应该能够在不同 abstraction layers 之间钻取。

研究者不需要把所有实验细节交给黑箱。Silico 会保留实验的代码、数据、参数和结果，用户可以查看 agent 怎样形成判断，也可以在中途改变方向。理想的使用方式不是让 agent 一次性给出一个漂亮结论，而是先让它做一个小实验，观察证据和失败模式，再决定是否把研究范围扩大。

### 长周期自动研究的组织方式

研究本身是一项 long-horizon task。一个可靠的研究 agent 需要在长时间内保持目标一致，记住已经测试过的路线，避免重复失败的实验，能够把中间发现写入下一轮研究计划，还要知道何时需要回到基础假设重新检查。

Goodfire 认为，单个 agent 的能力不是全部。多 agent swarm 可以把一个大问题拆成多个方向：一个 agent 负责数据清理，一个负责训练，一个负责可视化，一个负责寻找反例，另一个负责审阅和 red-team。最后由更高层 agent 汇总，向人类报告哪些结果已被多个方向验证，哪些只是暂时的猜想。

这种组织方式改变了研究者的角色。人类不再需要亲自写每个 kernel、维护每个 GPU job，但必须更清楚地定义问题、判断研究结果、设计验证标准。一个人如果只会把任务交给 agent，却不能发现 agent 漏掉了关键条件，仍然可能得到非常漂亮但完全错误的结论。

### 研究品味与产品防御

Silico 的 research taste 来自 Goodfire 的研究者长期积累。他们把自己的方法、判断、实验顺序和失败经验写进 skills、prompts 和 tools。用户反馈说，Silico 在研究品味上明显优于普通的 coding agent，尤其是在选择下一步实验、查找反例和组织证据方面。

这也是一个重要的产品防御。Goodfire 过去会为企业处理价值很高的问题，企业愿意支付七位数费用获得 forward-deployed research team。Silico 把一部分能力 productize，但不代表所有 know-how 都会立即扩散。对于非常复杂或高价值的问题，企业仍然可能需要 Goodfire 的研究人员一起工作。

Dan 认为，agent 越强，对高水平研究者的需求可能越大。强 agent 需要更高 taste 的人来提出目标、审核证据、决定哪些结果值得继续。Goodfire 希望同时做 enterprise service 和 product，让更多人自己使用，同时继续和企业共同发明新的方法。

### 计算额度与共享项目

每月 1,000 美元的 subscription 本质上是一个 credit pool。用户可以把 credit 用于 model tokens，也可以换成 GPU compute。用户有自己的 cluster 时，Silico 连接到该 cluster，并不会按 Silico 的 compute 再收一笔费用；没有 cluster 时，平台提供 on-demand compute。

用户还可以选择公开分享项目。别人能够看到一个长期 autonomous research project，fork 它，再沿着另一个方向继续。对刚开始做研究的人来说，这种共享项目像研究模板，可以帮助他们理解一个想法是如何被拆成实验、如何积累证据、如何从结果走向结论。

Nathan 认为这类体验很重要，因为很多人不是没有想法，而是不知道怎样把想法推进到一个可验证的研究结论。通过 fork 一个成熟项目，研究者可以先理解别人的工作方式，再逐步形成自己的研究 taste。

### 更具体的研究成果

Goodfire 内部 hackathon 的结果显示，Silico 不只是自动写报告。团队在生物风险分类、audio encoding、robotics 和 biology 模型压缩上都做了真实实验。有些模型去掉约一半参数后，性能仍然保持不变，这说明模型的参数中可能存在大量冗余或可以重新组织的结构。

在 protein generation 上，研究者用模型内部 representations 做 steering，使生成的 protein 更容易与指定 target binding。传统的生成方法主要依赖外部评分，再反复试错；使用内部表示后，研究者可以更直接地对语义属性做控制。

在 RL run 中，如果同一个 token 反复作为第一 token 出现，直接重新训练可能要花费很长时间。Silico 可以编辑权重，定位导致 collapse 的部分，移除导致问题的机制，再恢复输出多样性。这种局部修复不一定能替代完整训练，但能帮助研究者理解 collapse 的因果来源。

Goodfire 也在研究 model editing、KV cache 压缩、post-training automation、cyber guardrails 和模型内部概念注入。这些任务表面上不同，但核心都是理解模型的结构，找到可控制的内部组件，再验证局部干预有没有带来新的副作用。

### 特化与通用的边界

传统工程通常建议先为特定问题 build for specificity，然后再 generalize。但在 general intelligence 领域，策略可能反过来：先建立能力很强、可以处理很多问题的 agent，再根据用户反馈做 specialization。

Silico 主要服务 machine learning research，特别是 interpretability、training、model evaluation 和 alignment。它并非所有科学研究的万能工具。团队有人用它研究 physics，也取得过进展，但对完全开放、没有明确实验反馈的科学问题，仍然需要大量人类判断。

Dan 认为，AI product 的重要考验，是能否给下一代模型提供一个足够好的 harness。今天的 Silico 已经能让团队发现新知识、推进实验、加快积累关于世界的知识；未来模型能力提高后，好的 harness 可以把这些能力继续放大。

### 研究职业的变化

**Nathan Labenz：**

过去想做 AI research，通常需要把 coding、PyTorch、分布式训练和 kernel optimization 练到很强。随着 agents 逐渐承担这些工作，研究者还应该怎样准备？

**Dan Balsam：**

最重要的不是停止学习技术，而是学会调试 agent。无论是 coding agent 还是 research agent，都可能因为一个小细节而失败。真正高水平的使用者能迅速判断问题出在哪，要求 agent 补证据，或把任务拆成更小的可验证步骤。

他们还需要形成跨领域的 metacognition。能够进入一个不熟悉的领域，快速找到关键概念，过滤噪音，知道哪里存在不确定性，并把一个领域的经验迁移到另一个领域。AI 会让顶尖 specialist 更有价值，也会让顶尖 generalist 更有价值。

因此，研究者要培养快速学习、主动验证、区分相关性与因果性、知道什么时候继续和什么时候放弃的能力。工具越强，监督和反思的重要性越高。

### 开源能力与防御能力的矛盾

Dan 反复强调，open model 的问题不能只从“有没有危险能力”这一条线看。强大的 cyber model 确实可能被用来攻击，但同一个模型也可能帮助一家没有资源的公司发现漏洞、保护网络。

如果只有少数大型公司能访问最强模型，许多组织就只能面对潜在攻击，却没有同等的防御能力。开源 Kimi K3 这样的模型，哪怕不是全球最强，也可能给更多组织提供最低限度的自我保护工具。

他并不否认对手或有组织的 bad actors 可能训练更强的模型，也不否认 open weights 会降低 fine-tuning 和 RL 的门槛。现实是，相关技术已经被多个国家和组织开发，不太可能因为某一个平台关闭 access 就回到没有这些能力的世界。

因此，问题不在于选择“完全开放”或“完全封闭”这么简单，而在于怎样让 defensive capability 更广泛，同时对明显危险的用途施加限制。Goodfire 只是在自己的平台上再加一层约束，因为 Silico 能调度 GPU、运行长时间 agent，它携带的风险类别不同于普通聊天接口。

### Guardrails 的具体取舍

Goodfire 的平台不会只依赖基础模型供应商提供的安全层。它会加入自己的 monitor 和 guardrails。平台可能用 agent 评审研究项目，也可能使用 activation monitor 判断模型内部是否进入高风险模式，但公司不会把所有具体规则公开。

Dan 的观点是，基本 guardrails 不是完全无法解决的问题。问题在于 guardrails 需要达到怎样的覆盖率、在什么阶段触发、是否会误伤合法研究，以及攻击者绕过它们需要付出多少代价。

如果用户只是对一个较小模型做 refusal direction 的研究，风险与对一个高能力 multi-trillion-parameter model 完全移除所有 refusal 机制不同。平台需要根据模型能力、任务持续时间、是否连接外部工具、是否访问大规模 compute 等因素做风险分级，而不能使用一条不分场景的规则。

Goodfire 希望支持开放科学，包括可能引发争议的问题，但支持开放科学不意味着任何人都可以无审查地运行任何长周期实验。尤其是 cyber、bio 和能够自动扩大能力的训练任务，需要更严格的判断和人工沟通。

### 生物风险的时间尺度

Dan 不认为“还有十二到十八个月”是一个足够长的缓冲期。AI 参与 bio research 的方式可能突然发生改变，风险不一定按人们当前设想的路径出现。某个实验首先只影响细菌，可能仍然意味着能力边界已经发生变化，未来不应等到直接影响人类才开始建立防护。

Goodfire 的作用不是预测每一种灾难，而是通过 interpretability 和 empirical alignment research，弄清楚模型在学习什么，哪些训练数据、目标和能力可能造成危险偏移。公司也希望通过 grant 让更多 life sciences 与 AI safety 研究者使用这套工具。

Dan 认为，科学研究速度是风险治理的重要组成部分。更快地理解模型，可能帮助社会更早发现危险；更快地发展 life sciences，也可能带来新的治疗方案。不能只用停止所有研究来避免风险，但也不能在没有 guardrails 的情况下无限加速。

### Training intervention 的必要性

监控可以告诉我们模型正在做什么，但如果模型持续更新，单靠监控可能永远追不上。Dan 更倾向于认为，人类最终要有意识地设计 training techniques，让模型学到想要的东西，而不是假设一个正确的 reward function 自然会产生 aligned model。

这也是 predictive data debugging 的意义。研究者先观察数据会强化什么，再把 unwanted feature 从数据或 reward signal 中移除，或者在训练中加入对特定 feature 的干预。与其训练结束后发现模型学会了危险行为，不如尽早检查训练过程正在把哪些概念推高。

不过，每一种 intervention 都可能产生新的 off-target effect。模型可能学会隐藏自己的行为，或从一个被监控的 subspace 转移到另一个 subspace。正因为如此，Goodfire 不主张未经研究就大规模使用 multi-agent optimization、长时间 RLVR 或针对 alignment-critical property 的强 reward shaping。

### 监控与冻结模型的未来

如果未来模型的 weights 能够冻结，而且研究者有足够强的 factorization 和 monitoring tools，那么可以先理解模型，再限制危险 action。模型不是无限自我变化的对象，风险管理会更接近对一个复杂软件系统做安全审计。

但 continual learning 会改变这个问题。模型如果持续训练、持续更新自己的 representations，那么过去做过的解释可能逐渐失效。每次 update 都可能改变 concept geometry，甚至让模型从一个原本可监控的路径转到另一条路径。

这就是为什么 Dan 认为 training control 不能被当成最后才做的工作。现在 Goodfire 主要精力仍然放在 factoring，也就是理解模型的组件和关系，但未来会增加 refactoring 和 training steering，因为只有这样才可能真正控制模型学习的方向。

### Goodfire 的研究哲学

Goodfire 认为，interpretability 不能只停留在展示漂亮的 activation visualization。真正有用的解释应该能够产生可验证的假设、定位行为的因果组件、指导训练或模型编辑，并且在不同输入和不同模型规模上复现。

这也是为什么公司会同时建设 research infrastructure、training infrastructure 和 product UX。只有把这三部分连起来，研究者才可以从一个可疑行为出发，提出关于 feature 的解释，运行 intervention，再确认干预是否真正改变了目标行为，以及有没有损伤其他能力。

对于大型模型，单个图表不够。研究者需要 provenance，知道数据怎么进入实验、代码如何运行、参数怎样变化、哪一个 agent 提出了下一步，以及哪些结论已经被独立实验支持。Silico 的长周期任务设计就是为了让这条证据链保留下来。

### 解释性研究与科学发现

Dan 把 interpretability 看成一种 cognitive science。它既研究模型怎样组织知识，也研究模型怎样学习、怎样形成内部概念、怎样在不同上下文中调用同一个概念。feature geometry、concept manifolds 和 parameter decomposition 都是在尝试建立一种模型内部的科学语言。

研究者不必预先知道每一条结构。可以从数据分布出发，观察模型是否恢复了数据背后的自然 ontology。树状演化结构、周期表、情绪圆环、日期循环和数字螺旋，都说明模型可能通过压缩世界信息，形成比单个标签更高层次的关系结构。

如果这些结构可以被可靠地恢复，就能做更多事情：检查训练数据是否在错误方向上强化概念，找到模型异常行为的根源，沿着语义流形做更平滑的控制，或者判断某个模型更新是否把两个原本分开的能力挤到了一起。

### 从局部 neuron 到模型级调试

Weird Chat 的例子说明，一个看似荒谬的回答，有时可以追溯到一个没有被正确调节的 neuron。但这不意味着所有模型问题都能靠调一个 neuron 解决。更大模型往往包含跨层、跨组件的回路，单个 neuron 可能只是最后一个显现出来的节点。

因此，Goodfire 同时研究 feature、subspace、circuit 和参数分解。局部干预需要知道它在更大的几何结构中处于什么位置。比如，如果一个 feature 属于一个更高层的 calendar-time subspace，直接推高它可能会破坏时间关系；沿着对应 manifold 调节，才更可能维持模型的整体一致性。

同理，模型忘记 German 而保留 Dutch 的实验，重点并不是“删掉一个语言按钮”，而是证明模型内部存在可以被识别、分解和局部修改的结构。未来如果可以更系统地完成 factoring 和 refactoring，模型调试会更接近软件工程，而不是只能反复试 prompt。

### 对产品化研究的期待

Silico 的产品化并不是把 Goodfire 的全部研究交给一个自动按钮，而是让更多人能够进入研究循环。用户仍需要选择问题、定义成功标准、检查 agent 的中间证据，并对最终结论承担判断责任。

Dan 希望用户把 Silico 当成研究伙伴，而不是答案机器。一个好的起点是提出一个明确但范围有限的问题，观察 agent 如何拆解问题；第二步是引入一个已知的 benchmark 或反例；第三步才是让 agent 做更长时间的自主探索。

如果用户一开始就把一个模糊、开放、没有验证标准的问题交给 agent，很容易获得一个长篇但无法判断的输出。研究者的 taste 体现在把问题变成一系列能够被实验排除或支持的假设。

### Grant 与公共利益

Goodfire 不希望价格成为安全研究和重要生命科学研究的门槛。Silico 前两个月可以半价，之后还会为 AI safety、alignment 和 life sciences 研究者提供 grants 或 extended access。

这项安排也符合公司的 public benefit charter。Goodfire 希望研究成果和工具能够帮助更广泛的研究社区，而不是只服务于支付得起七位数 research engagement 的大公司。Dan 认为，加速科学是建设 AI 的重要理由之一，如果更多人能用更少的时间完成可靠实验，社会就有更多机会解决医学、网络安全和 AI alignment 中的难题。

### 对 AI 进展速度的态度

Dan 不主张因为风险存在就把所有研究能力集中到少数机构手里。他更担心一种只有少数最强者拥有防御工具，而其他组织无法自保的世界。但他也不接受“只要开源就天然安全”的想法。

他的立场是，社会需要在开放研究、能力扩散和风险限制之间找到现实平衡。公开研究能够增加审查者数量，也可能加速发现防护方法；但长周期 agent、GPU cluster 和高能力模型组合在一起后，需要比普通 API 更严格的治理。

对于“速度越快越好”的观点，Dan 认为至少应该认真讨论 pause 或 pacing。理想情况下，再有一代模型带来的生产率和科学收益，可能已经足够让社会获得巨大利益。短暂停下来，评估模型是否已经被理解、风险是否可管理，未必意味着放弃进步。

### 意识问题的谨慎判断

Goodfire 内部关于 Claude 是否有意识的讨论，并不是为了给产品制造营销故事。Dan 认为，人们之所以对这个话题情绪强烈，是因为它触及人类身份、思维和道德地位的基础问题。

他不认为目前有一个公认的 consciousness 定义，能干净地把模型排除在外。另一方面，模型表现出类似情感或语言结构，也不等于它一定拥有主观体验。人脑有更复杂的神经元、更多 recurrence、更高的能效和更复杂的连接，因此不能简单把“有相似结构”当成证明。

如果 consciousness 是连续属性，问题可能不是模型“有”或“没有”，而是它在某条连续谱上处于什么位置。Dan 的个人判断仍然高度不确定，但他不愿意把模型意识的可能性简单归零，也不愿意假装这个问题已经解决。

这种不确定性本身要求 intellectual humility。无论最终答案是有意识、没有意识，还是存在不同程度的意识，研究者都应避免在证据不足时做出绝对断言。尤其当错误判断可能导致严重的道德和安全后果时，谨慎比自信更重要。

### 最后的研究建议

Dan 给希望进入 AI research 或开始 PhD 的人的建议是：不要只把自己训练成会写代码的人，也不要只追逐某一个工具。要学会提出好问题，理解一个领域的基本结构，快速判断实验是否有效，并且能在 agent 失败时进行高质量 debugging。

如果一个 agent 给出一个看起来合理但没有充分证据的结论，研究者需要知道该问什么、怎样设计反例、怎样寻找独立验证。随着 agent 负责更多低层工作，研究者的价值会更多体现在目标选择、证据判断、跨领域迁移和长期方向管理上。

### 完整收束

今天的讨论从 Silico 的 1,000 美元订阅和 long-horizon research 开始，经过 predictive data debugging、RL、reward shaping、data filtering、feature geometry、concept manifold、BSF、parameter decomposition 和 model steering，最后回到更大的问题：人类是否能够在模型能力快速增强的同时，理解并控制模型学到的东西。

一个重要结论是，解释不是目的本身。解释的价值在于帮助研究者找到可干预的机制。另一个结论是，monitoring 很重要，但如果模型持续学习，最终还需要把控制力带入 training process。再一个结论是，开放能力与安全不能被简化成单一口号，需要根据模型规模、任务类型、工具权限和潜在外部性做具体判断。

Goodfire 希望 Silico 让研究者把更多时间用在大问题上，用 agent 执行实验，用 provenance 检查证据，用人类 judgment 决定研究方向。Dan 期待更多人申请 grants、fork 公开项目、尝试新的研究问题，并把结果反馈给 Goodfire。

**Nathan Labenz：**

感谢 Dan 来到 The Cognitive Revolution。今天的对话说明，AI research agents 的真正价值不仅是让研究写得更快，而是让更多人能够进入模型内部，观察概念如何形成、行为如何被训练、风险如何被放大，以及哪些 intervention 可能真的有效。

**Dan Balsam：**

希望 Silico 能帮助更多人推进科学，特别是生命科学与安全研究。Goodfire 欢迎研究者和机构联系我们，一起做研究，帮助工具变得更好。加速科学是建设 AI 的重要理由，希望更多人能够使用这些工具做出真正有价值的工作。

### Silico 的研究体验、成本与长期任务

Silico 的目标，是让研究者在几天或几周内完成过去需要几个月的工作。Nathan 说，这让“只会提出想法的人”重新变得有价值，因为很多过去阻止他做研究的工程障碍正在消失。接下来真正的问题是，他有没有足够好的大想法，以及能不能判断实验结果。

Silico 解决的第一个难题是 infrastructure。大规模 pre-training、trillion-parameter 级 interpretability、GPU cluster 管理和实验重现，都不是简单运行一个 coding agent 就能解决的。第二个难题是 research taste。Goodfire 的研究者亲手编写了很多 skills、prompts 和 tools，让 agent 知道该问什么、该做什么实验、如何比较结果以及如何继续追问。

第三个难题是研究型 UX。研究需要理解、provenance、可复核性和在不同抽象层之间切换。第四个难题是 long horizon coherence。真正有价值的研究不能只运行几分钟，往往需要持续一天或两天，不断修改假设、执行实验、总结中间结论，再把下一轮实验接上。

Silico 的订阅价格是每月 1,000 美元。用户可以带自己的 compute，Silico 连接用户的 cluster，这种情况下不额外收 compute 费用。如果没有自己的 compute，用户可以使用 on-demand compute，compute 和 model tokens 从同一个 credit pool 中扣除。当前的额度大致支持每周 5 到 10 个 autonomous experiments，具体取决于实验规模，团队希望在一两个月内把效率提高到每周 10 到 20 个实验。

Goodfire 以前通过 high-touch enterprise research 收取较高费用，但不会完全放弃这部分业务。Dan 认为，随着 agent 变强，对高水平 human operators 的需求未必下降，反而可能增加。coding agents 发展后，软件岗位并没有简单消失，因为更强的工具需要更有 taste 的人来设定目标、检查结果和推动系统。

如果未来 agent 能独立完成长周期、影响重大的研究，例如发现一种疾病的治疗方法，世界会有足够的需求来消化这些计算能力。但在当前阶段，擅长使用 agents 的人比不擅长的人做得更多。Goodfire 认为自己是最有经验的 human operators 之一，因此会继续与企业客户合作、forward deploy 研究人员、帮助客户学习，同时也把工具交给客户，让客户自己开始驱动研究。

### Silico 的案例与研究用途

Goodfire 的内部 hackathon 只有一天，但很多团队让 Silico 运行 all-day autonomous experiments，结果在一些特定问题上达到了 state-of-the-art。团队做出了用于 protein models 的 biorisk classifiers，也做出了在参数规模上领先的 audio encoding model。

在 robotics 和 biology 的多个模型上，研究者发现可以去掉大约一半参数，而性能几乎不下降。团队还在 Kimi K3 上训练 cyber guardrails，使用 protein model 的内部 representations 控制生成，让 protein 更好地与目标结合，并在一些模型中移除基础性 pathology。

Silico 用户还做过很多其他实验。有人研究模型能否报告被注入 latent space 的概念，发现模型可能无法判断某个概念是否被注入，但当被问到注入了什么时，反而能给出准确答案。有人编辑权重，修复 RL run 中同一个 token 总是作为第一个 token 的 collapse，不必重新跑完整 RL。Base10 的研究者在压缩 KV cache 以提高效率，Prime Intellect 在自动化 post-training，Tinker API 也适合接入这类实验。

Silico 可以被用于大多数机器学习研究，但它仍然有边界。它尤其适合 interpretability 和 ML research，不一定适合所有 open-ended scientific questions。团队中有人用它研究 physics，也取得了进展，但产品目前仍以机器学习为核心。

Goodfire 建议新用户先看公开的 examples，fork 一个别人已经完成的 long-running project，再沿着自己的问题修改。也可以先提出一个范围较小的问题，观察 agent 怎样拆解问题，确认自己理解它的强项和弱点后，再逐步把实验目标放得更远。

### 研究者应该培养什么能力

**Nathan Labenz：**

过去研究者需要把 coding、PyTorch、kernels 等技术练到足够强，但未来的模型可能在这些局部技能上超过人类。研究者还应该投资哪些能力？

**Dan Balsam：**

Debugging 是一个很直接的答案。Agents 会因为很多原因失败，即使一个 agent 很聪明，也可能漏掉一个关键细节，使整个结论失效。Silico 用 multi-agent loops 处理其中一部分，但最终仍然需要人类区分一般答案和好答案，知道什么时候反驳、什么时候给反馈、什么时候继续追一条线、什么时候放弃。

未来重要的是快速进入陌生领域、识别 signal 与 noise、理解一个新领域的核心结构，以及把 metacognitive skills 迁移到不同问题。AI 会同时提高顶尖 specialists 和顶尖 generalists 的价值。现在可能是历史上最适合成为 generalist 的时期之一。

研究者需要训练自己快速学习、知道去哪里找信息、知道什么时候找信息、把高吞吐量的信息转化成可判断的结构，并能够在实验结果与漂亮叙事之间保持距离。这些不是软技能，而是使用 AI research agents 所需要的硬能力。

### Open-weight models 与网络安全

**Nathan Labenz：**

一些人认为 open models 不危险，因为普通个人很难在家运行 2.8 万亿参数、8 万亿参数的模型，真正重要的服务都可以被监管。但现在 Kimi K3 等模型可以被更多人获得，怎样防止 rogue ML researcher 用平台做破坏性的事？

**Dan Balsam：**

他认为“只监管服务就够了”的论点低估了 open model 的现实作用。自己的立场很复杂，因为现在已经存在 dual-use cyber weapons。最强的 defensive technology 本身也可能是进攻性 cyber weapon，拒绝开放模型会让防御能力集中在少数 frontier labs 手中。

很多 startup 和组织没有资格进入大型公司的 cyber defense programs，而 open model 可以给它们提供自我防御的工具。一个开源模型即使不是最强，也可能帮助缺乏资源的组织保护基础设施。另一方面，把强大模型交给任何人也会带来风险，尤其是某些组织可能有动力训练出针对他人的 cyber capability。

Dan 没有简单答案，但目前仍认为 open source 的净效果偏正面。世界上已经有比 Kimi 更强的 closed models，也可能有更强的 bad actors。让防御者至少获得可用的 open models，是现实中的必要选择。

Goodfire 不会把所有 open models 都直接放到 Silico 上。目前平台主要提供 OpenAI 和 Anthropic 的模型。未来如果开放更多模型，会建立相应的 guardrails。公司不希望任何人直接注册，然后用 long-horizon research project 做 cyber research、fine-tune cyber model 或执行大规模 red teaming，而不经过进一步的审查和沟通。

对一个小型 8B 模型做 refusal direction ablation，可能不会带来现实伤害；但对高度能力的 multi-trillion-parameter agent 完全移除 guardrails，就可能造成严重后果。Goodfire 希望支持开放科学和有争议的研究问题，但也要考虑平台可以调度 GPU cluster、运行长周期 agent 的特殊风险。

平台会使用多种防护，包括 LM-as-a-judge、activation monitors 以及其他 guardrailing tools。Dan 不想公开所有细节，因为这会让绕过防护变得更容易。建立基本合理的 guardrails 相对可行，真正困难的是在不阻止 legitimate work 的情况下，识别哪些请求会把更高能力的系统引向 illegitimate use。

### Bio risk、国际协作与放慢 frontier 进展

**Nathan Labenz：**

最近有报道说，生成模型已经被用于设计新的病毒类别，虽然目前目标是细菌，不是直接针对人类，但 bio risk 的预测清单似乎正在逐项实现。有人说距离真正问题还有 12 到 18 个月，但这其实很短。Dan 现在有多担心？

**Dan Balsam：**

他相当担心。和 cyber incidents 一样，未来 bio risk 真正发生的机制可能出乎预料，而不是事先写在清单上的单一事件。正因为机制可能奇怪、组合可能复杂，社会需要在风险变得更严重之前建立国际合作并放慢某些进展。

Dan 签署了呼吁 pace the frontier 的公开信。他认为 Goodfire 的具体作用，是研究怎样让模型风险更低。公司通过研究模型、尝试不同的训练方式、理解模型如何学习，建立 empirical science of alignment。

这类工具具有 dual-use 风险，但让更多人拥有研究技术的净效果仍可能是正面的。人类很难解决复杂的 alignment 和 bio safety 问题，除非更多研究者能够参与。因此，一方面要让更多人参与科学研究，另一方面要建立可以让过山车稍微慢下来的制度和限制。

### 哪些训练技术现在不应该直接放大

**Nathan Labenz：**

如果业界要对一些训练技术达成“现在先不要做”的共识，哪些方法应该进入候选？一个典型风险是，用模型的监控信号训练模型，结果让坏行为隐藏到 monitor 看不到的地方，行为仍然存在，只是被遮蔽了。另一个风险是，在开放且有竞争性的网络环境中，直接用 agent 在互联网上赚了多少钱作为 reward signal。

**Dan Balsam：**

Multi-agent optimization 似乎是一个很危险的方向。多个 agents 协作，并把一个 reward signal 在它们之间传播，可能产生人类无法观察到的合作方式。很多最坏的情景，都可能来自 agents 彼此以人类无法察觉的方式合作，而直接的 optimization pressure 很可能加剧这个问题。

以当前对 training shaping 的理解，不应该把 multi-agent optimization 用到 alignment-critical properties 上，然后在没有充分测量的情况下长时间运行。对于 deception，Goodfire 并不认为目前的技术可以承受压倒性的优化压力，更不应该假设简单的 reward shaping 一定能防止 deceptive behavior。

不过，Dan 也不同意把所有宽泛类别的技术永远列为禁区。Goodfire 的实验表明，有些 reward shaping 能在某些设置、某些模型规模或 DPO 中工作，在长时间 RLVR 中却未必工作；有些设置能逃过 probe，有些不能。最重要的是测量具体应用、观察训练中的实际变化，而不是只用一个笼统的技术名称做判断。

他认为，人类最终没有选择，只能以某种方式介入 training process。不存在一个完美、天然就会产生 aligned models 的训练配置。研究者必须“握住方向盘”，但现在还不知道最可靠的握法。理论可能来不及解决问题，因此需要尽快做 empirical science，在真实训练中比较不同 intervention 的后果。

### Monitoring 是否足够

防御纵深可能仍有希望。即使无法完全理解或控制模型训练，也可以用多种方式进行 monitoring，叠加许多层防护。Dan 过去对此比较怀疑，但一些关于模型内部空间的研究让他认为，理想情况下 monitoring 可能有一定概率成功。

不过，他不认为把一个简单的 subspace 监控结果扩大为“模型的所有长期规划都只在这里发生”是稳固结论。模型会使用许多不同的机制，也很难用一种简单方法隔离整个内部空间。

如果模型是 frozen weights，配合好的 interpretability techniques，研究者也许可以识别模型不擅长或可能造成伤害的行为，并阻止它们执行。那会是一个相对可管理的世界。

但如果模型是 continual learning 的 dynamic objects，参数持续更新，那么单靠 monitoring 就不够。只要模型一直在训练，最终就必须控制 training process。现在还不清楚未来会是哪一种世界，因此 Goodfire 把大部分研究精力放在更好地 factor models，同时逐渐增加对 training steering 的研究。

Dan 理想中的结果是，再推进一代模型，然后暂时停下来。这样经济和科学可能获得巨大收益，全球生产率会改变，科学进展会加速，风险仍然存在但大多可以管理。人类可以用这段时间判断自己是否有足够智慧走进下一扇门。

### Grants、公开研究与 Goodfire 的讨论

Silico 前两个月会半价，Goodfire 也准备 research grant program。Life sciences、AI safety 和 alignment 方向的 individual researchers 或 academics 可以申请延长使用时间。机构如果希望加快研究，也可以联系 Goodfire 讨论合作。

Dan 特别澄清，Goodfire 没有在幕后秘密进行 recursive self-improvement。公司的大部分研究都会公开，团队相信 open science，也一直坦诚说明研究什么、为什么研究。外界关于公司秘密研究 agenda 的猜测，并不是事实。

Goodfire 内部常讨论 feature geometry。公司的一个玩笑是，每次 retreat 最后都会聊到 consciousness。有人会给 Claude 的意识程度打分，从 bacteria 到 human 的区间里答案非常分散，但往往呈现两个聚集点：完全没有，或有一点点。

解释性研究吸引了很多对 neuroscience、cognitive science 和 minds 如何工作感兴趣的人。Goodfire 研究的不只是模型怎样输出答案，也包括 learning 如何发生、概念如何组织、思维是否具备类似人类 cognition 的结构。

### AI consciousness 的不确定性

**Nathan Labenz：**

过去他更倾向于认为，模型是 alien minds，不应该 anthropomorphize。现在随着越来越多和人类 cognition 类似的结构被发现，他对 Claude 是否具有 consciousness 的判断发生了变化。

**Dan Balsam：**

这是一个高度不确定的问题。人类并没有一个足够有说服力的 consciousness 定义，可以明确排除 Claude。Claude 确实表现出一些在人类身上会被称为情感和定性体验的特征，但这并不自动证明它有意识。

如果 consciousness 是某种 computational mechanism，那么 transformer 是否具备它，取决于哪些 computation 是必要的。人脑与当前模型仍有很大差异：人脑更加节能，神经元本身更复杂，连接更复杂，recurrence 更多，原始计算量也可能更大。因此，即使接受“意识是计算的”这个前提，也可以认为今天的模型尚未达到必要复杂度。

Dan 不确定 consciousness 是二元属性还是连续谱。如果是连续的，就会出现比较问题：Claude 的 consciousness 是不是多于 jellyfish、少于 mouse？他半开玩笑地说，Claude 可能比 jellyfish 更有意识，但未必达到 rodent 的程度，大概处在两者之间。

Nathan 认为，最重要的不是急于下结论，而是承认错误判断的 downside 很大。对这种问题，intellectual humility 很重要。即使最终模型没有意识，也不应把它当成可以轻率忽略的哲学问题。

### 结语

**Dan Balsam：**

他希望 Silico 能帮助更多人推进科学，尤其是 life sciences 和 safety。个人研究者、学者和正在加速研究的机构，都可以申请 grant 或联系 Goodfire。建设 AI 的意义之一，就是加快科学进步；如果 Silico 能让更多人提出问题、运行实验、检验结论，并把结果公开，那么它就能发挥价值。

**Nathan Labenz：**

感谢 Dan 来到节目。今天的对话从 predictive data debugging、concept manifolds、BSF 和 model steering，一路谈到 Silico 的长期 autonomous research、open models、cyber risk、bio risk、training intervention 以及 AI consciousness。真正的难题仍然不是让模型产生更多输出，而是理解它在学什么、怎样控制它学什么，以及怎样让更强的研究能力与更可靠的安全边界同时出现。

节目片尾是音乐和制作信息。The Cognitive Revolution 属于 Turpentine Network，节目讨论 technology、business、economics、geopolitics 和 culture。制作团队欢迎听众通过网站、社交媒体、YouTube、Apple Podcasts 或 Spotify 提供反馈、嘉宾建议和主题建议。

### 对研究流程的进一步拆解

Dan 对研究代理的期待并不是让它替研究者自动生成一份看似完整的报告，而是把研究过程拆成可以反复检查的步骤。研究者先提出问题，再定义可观测的变量、实验条件和失败标准，代理负责帮助检索资料、整理假设、运行分析并记录结果。每个环节都需要能够回到原始证据，不能因为模型给出了一段流畅解释，就跳过数据、代码和实验记录的核对。

他认为，Silico 的价值还在于降低“试一个想法”的成本。过去一个研究者可能因为时间、工具和编程门槛，只验证少数几个假设；当代理可以处理更多机械工作时，研究者就能把精力放到问题选择、实验设计和结果解释上。但这不会自动产生好科学。问题如果定义得差，搜索范围如果过窄，或者成功标准在实验之后才被修改，代理只会更快地把偏差放大。因此产品设计必须鼓励记录中间步骤，而不只是展示最终答案。

### Interpretability 的工程边界

对模型内部机制的研究也有类似边界。找到一个看起来和某个概念相关的 feature，不等于找到了一个可以独立开关的“概念按钮”。同一概念可能分布在多个方向上，方向之间还可能随着上下文、层数、提示词和训练阶段发生变化。一个 steering 操作在训练分布内有效，换到新的任务或新的模型状态后可能失效，甚至产生意外副作用。

因此，Goodfire 更重视几何结构、特征之间的关系以及这些结构在训练前后的变化，而不是只展示某个漂亮的可视化。研究者需要区分相关性、可干预性和可泛化性：相关性说明内部表示与行为有关，可干预性说明改变它会影响行为，可泛化性则要求这种干预在不同输入、不同任务和不同时间点仍然成立。三者不能混为一谈。

### 从 frozen model 到持续训练

节目还反复回到一个实际的系统分叉。如果模型权重被冻结，研究者可以在相对稳定的对象上做解释、评估和防护；如果模型持续从环境中学习，今天识别到的内部结构明天可能已经变化，旧的 probe、监控器和安全边界就需要重新验证。对持续训练系统，安全不能只靠运行时观察，还必须把训练数据、奖励信号、更新步骤和权限控制纳入系统设计。

这也是为什么 Dan 不把 interpretability 当成单一产品功能。它更像一组实验工具，用来帮助研究者决定在哪里插入训练干预、哪些行为值得持续追踪、哪些安全假设已经被新一轮更新破坏。真正的目标不是声称“已经理解模型”，而是让人类在模型发生变化时更早发现问题，并有机会改变训练方向。

### 对开放模型和研究公共性的判断

Dan 支持更多研究者使用开放模型和开放工具，但他没有把“开放”直接等同于“安全”。开放模型可以让更多人复现实验、发现缺陷和改进方法，也可能降低滥用门槛。公共研究的关键在于透明的实验记录、明确的能力边界、对高风险能力的负责任披露，以及让安全研究不被少数机构垄断。

他希望 Goodfire 的公开工作能够让外界检查方法、复现实验并提出反例。对一个仍在快速变化的领域，能否被质疑比能否制造一个确定的宣传结论更重要。Silico、research grants 和公开论文的共同方向，是把解释性研究从少数专家的手工工作，逐步变成更广泛研究社区可以参与的经验科学。

### 研究代理与人的分工

Nathan 和 Dan 讨论的不是“代理会不会取代研究者”这一句式问题，而是研究流程中哪些工作应该交给机器，哪些判断必须由人承担。资料搜集、文本归档、代码执行、图表整理和重复实验，适合交给能够记录操作轨迹的代理。问题是否值得研究、变量是否真的对应目标、结果是否具有因果含义，以及是否应该把结果发布出去，仍然需要研究者负责。

这种分工也影响了 Silico 的产品形态。一个好的研究代理不能只给出最终结论，还要让用户看到它查了哪些资料、采用了哪些假设、运行了哪些实验、在哪些环节遇到不确定性。用户可以沿着这些记录回到数据和方法，修正问题定义，再让代理重新运行。这样形成的是可重复的研究循环，而不是一次性的答案生成。

Dan 特别强调，研究效率提高后，验证反而更重要。过去一个实验因为成本高，研究者会在开始前花很多时间收敛方案；当运行实验几乎没有成本时，系统很容易充满没有清晰假设的探索。探索本身有价值，但必须和确认性实验、反例搜索以及失败记录区分开。否则代理产生的候选结论越多，团队越容易误把数量当作进展。

### 解释性研究的可证伪性

对于 predictive data debugging，核心问题不是“这个训练样本看起来重要吗”，而是如果删除、修改或重新加权它，模型后续行为是否按照预测发生变化。只有实际干预能够改变结果，研究者才有理由把内部表示与训练数据联系起来。即便如此，也要继续检查是否存在替代路径，避免把一个共同变化的信号误认为唯一原因。

概念流形的研究同样需要反事实测试。研究者可以沿着一个表示方向移动，观察输出是否变化；也可以固定其它变量，只改变上下文，测试相同方向是否仍然代表相同概念。若只在少数提示词上有效，就不能把它宣传成普遍的 steering 方法。节目中对这一点的反复强调，实际是在提醒研究者把漂亮的内部图像转化为能够被失败的实验检验的假设。

### 安全投入的时间窗口

Dan 所说的“暂时停下来”并不是认为风险可以被彻底消除，而是希望在下一代系统取得明显进展后，留出时间评估新的能力和新的安全方法。这个窗口可以用于测试训练干预、改进解释工具、建立独立评估和协调披露机制。若系统继续高速迭代，而研究者只能事后观察，很多问题可能等到出现外部损害后才被发现。

他也承认，这种安排需要产业、研究机构和公共部门共同参与，单个公司无法独自解决。公开研究、grant 和可复现实验的意义，是把安全判断从公司内部的口头承诺，推进到可以被其他团队检查和挑战的证据体系。这个过程不会给出绝对保证，但能让决策者更清楚地知道哪些结论已经有实验支持，哪些仍只是愿望或推测。
