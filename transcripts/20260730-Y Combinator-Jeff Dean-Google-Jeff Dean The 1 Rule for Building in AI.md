---
访谈时间: 2026-07-30
访谈时间说明: 无法从公开资料确认Startup School现场实际访谈日期，文件名与本字段使用YouTube发布时间
YouTube发布时间: 2026-07-30T21:03:53Z
嘉宾名字: Jeff Dean
嘉宾公司名称: Google
参与嘉宾:
  - 姓名: Jeff Dean
    公司或机构: Google
    职务: 首席科学家
  - 姓名: Diana Hu
    公司或机构: Y Combinator
    职务: Group Partner、节目主持人
播客名称: Y Combinator
播客url地址: "https://www.youtube.com/watch?v=CxXgV54KzpQ"
youtube_video_id: CxXgV54KzpQ
字幕来源: Y Combinator官方公开完整文字稿，经完整上下文转写为简体中文
公开文字稿来源: "https://www.ycrootaccess.com/p/jeff-dean-the-1-rule-for-building"
全文提及的关键名词:
  - Jeff Dean
  - MapReduce
  - BigTable
  - TensorFlow
  - TPU
  - Gemini
  - AI agents
  - machine learning
  - inference hardware
  - latency
  - energy efficiency
  - RAM
  - HBM
  - batching
  - context engineering
  - multi-agent systems
  - inference-time compute
  - AlphaFold
  - continual learning
  - AlphaChip
  - AlphaEvolve
  - model distillation
  - automated experimentation
  - learned evaluator
companies:
  - GOOGL
industries:
  - 存储
technologies:
  - TPU
  - 推理
  - Agent
  - 蛋白质设计
keywords:
  - 创业
tags:
  - GOOGL
  - 存储
  - TPU
  - 推理
  - Agent
  - 蛋白质设计
  - 创业
---

# Jeff Dean: The 1% Rule for Building in AI

## Transcript

### AI 是否已经达到初级工程师水平

**Diana Hu：** 我们开始吧，Jeff？

**Jeff Dean：** 好，开始吧。

**Diana Hu：** 欢迎你，也非常感谢你身体不舒服还来到现场。

**Jeff Dean：** 我的嗓子哑了。我平时不是这个声音，不过我们尽力而为。

**Diana Hu：** 你参与构建了 MapReduce、BigTable、TensorFlow、TPU 和 Gemini。单是回顾这些工作就可以聊一小时，但我尤其喜欢你仍会公开作出大胆预测。2025 年 5 月，你在 AI Ascent 上说，AI 已达到初级工程师水平。现在过去大约一年，这个判断有多接近现实？

**Jeff Dean：** Model 在 agent-based、长时间运行的 coding tasks 上进步很快，现在已经相当有能力。具体要看你怎样定义“初级工程师”，但总体而言，我觉得这个判断非常接近现实。

**Diana Hu：** 当时你低估了什么？

**Jeff Dean：** Model 处理越来越复杂任务的能力，增长速度比我预想的更快。不只 coding，agent-based systems 也开始在其他领域表现出色。我认为这会成为未来的重要趋势。

**Diana Hu：** 那再给我们一个大胆预测。到 2027 年会看到什么？

**Jeff Dean：** 我们会看到更多 ML systems 自身的自动化。系统能够运行大量实验，把复杂目标拆成 sub-problems，让每个子问题进入紧密的自动实验循环，再把结果组合起来，最终产生能力更强的新系统。

这不只适用于 ML，也适用于其他科学和工程领域。只要问题具有可测量的 objective，今天的系统就有机会持续推进。我认为，自动分解问题、自动实验并把答案重新组合，会非常令人兴奋。

### 2001 年的“整个搜索索引都能放进 RAM”

**Diana Hu：** 回到 2001 年。当时 Google Search 运行在硬盘上，你和 Sanjay Ghemawat 计算后发现，整个搜索索引终于可以装进当时所有机器的 RAM。你们在几天内把新的内存版搜索系统上线，Google Search 因此变得很快。历史常以新形式重演。2026 年的“终于能全部放进内存”时刻是什么？

**Jeff Dean：** 今天的问题略有不同。我认为会出现越来越多高性能、低能耗的 inference hardware。大家正在意识到，inference 是让 agent-based systems 服务更多人的关键。Latency 非常重要，而 hardware specialization 能让系统比 GPU、TPU 等更通用的计算设备更节能、延迟更低。

**Diana Hu：** 所有人都习惯了等待 model 回复。

**Jeff Dean：** 等待一点也不好玩。

**Diana Hu：** 你的意思是，也许以后不必等？

**Jeff Dean：** 想象一下，如果 latency 改善 50 倍，可以做什么。

### Agent 将连续运行数天乃至数周

**Diana Hu：** 现场六千名观众对 AI 普遍相信的某个假设中，哪一个其实已经错了？

**Jeff Dean：** 很多人还没有意识到，agent-based systems 不只能在一个问题上运行一两个小时。在一些问题领域，如果底层 model 足够强，它们可以连续运行数天甚至数周，完成非常复杂的任务。已有一些人看到苗头，但多数人还没有真正内化这一点。它会产生很大影响。

**Diana Hu：** 你让 agent 连续运行数周完成过什么任务？

**Jeff Dean：** 可以让 agent 用另一种 programming language，重新实现一整套软件，从而获得更好的 safety 或 performance properties。它们已经能够相当认真、完整地做这类工作。

### 三分钟语音输入与 TPU 的起点

**Diana Hu：** 你以擅长 napkin math 闻名。2013 年，Google 的 speech recognition 刚开始真正可用。你估算，如果每个 Google 用户每天只对手机说三分钟，让系统完成 speech recognition，就需要把 Google server fleet 扩大一倍。成本会非常高。于是你们开始做 custom chip，这成为 TPU 的起点。

**Jeff Dean：** 当时基于 deep learning 的 speech models 已经给出很好的结果，但计算成本远高于旧系统。它们把 error rate 降低了一半，相当于只用几个月调整 model、扩大规模、改善数据，就取得过去二十年的 speech recognition 进步。

我们开始担心：speech 一旦更好用，用户就会更多地用它写邮件、和手机交流。那项粗略计算正是为了回答需求增长后的成本。结果表明，只靠当时的 CPU 无法经济地扩张，我们需要更好的方案。

TPU 专门处理低精度 dense linear algebra，而这正是几乎所有现代 machine learning algorithms 的核心。如果一颗芯片只擅长低精度密集线性代数，不能运行 Chrome 或 Word，却能极好地完成 ML inference，那仍然非常有用。

几年后，这套系统产生的芯片比当时 CPU 和 GPU 的 energy efficiency 高 30 至 80 倍，latency 低 20 至 30 倍。

**Diana Hu：** TPU 后来成为 Transformer 时代的基础设施，而 Transformer 是在 TPU 发明后才出现的。你们不可能提前知道这一点。

**Jeff Dean：** 所以 TPU 本质上仍是 general-purpose linear algebra system。我们知道 ML algorithms 会持续演化，不能把芯片专门化到只服务一种算法，但又要足够专门化，才能使用大型 multiplier units、高速 memory，以及后来把许多芯片高效连接起来的 high-speed interconnect。我们在很多代产品中不断扩展和提高它的性能。

### 创业者该做什么 napkin math

**Diana Hu：** 今晚，想成为创业者的人应该计算什么，才有机会做出像 TPU 一样重要的东西？

**Jeff Dean：** 观察你所在领域的问题与 bottlenecks。问自己：有没有一种完全不同的解法，能让性能或能力提高一个甚至两个数量级？不要被今天解决问题的方式锚定，从 first principles 重新思考。有时这样盯着问题看，会发现别人没有考虑的好主意。

**Diana Hu：** 多年前你写过著名的《Latency Numbers Every Engineer Should Know》，列出了 cache miss、disk seek、network packet 从 California 到 Netherlands 所需时间等数字。很多 distributed systems engineers 把它贴在墙上。到 2026 年，这张表的 AI 版本应该包含什么？

**Jeff Dean：** 要知道 accelerator 的 main memory 到 on-chip memory、再到 multiplier unit 的 bandwidth；一次乘法操作需要多少能量；芯片之间的 interconnect bandwidth 是多少；在这种带宽下能连接多少芯片；当规模从 500 颗芯片扩到 10,000 颗时，network bandwidth 会下降多少。这些数字会直接影响你如何思考和解决问题。

### AI 系统真正稀缺的单位是能量

**Diana Hu：** 你说，现在衡量很多事情的最终单位是能量。一次数学运算大约消耗一 picojoule，但移动数据和完成 data I/O，能耗可高一千倍。

**Jeff Dean：** 对。仅仅把数据从 accelerator 的 HBM 搬到 processor，让处理器开始计算，就有这样的差距。

**Diana Hu：** 这个差距悄悄决定了哪些产品和 algorithms 能成立。哪些被创业者误以为是 model problem 的问题，其实是 energy 或 data I/O problem？

**Jeff Dean：** 搬数据比计算高一千倍的能耗差异，会塑造大量 ML 系统设计。如果没有这个差距，就不必 batching。现实中，我们必须把许多 examples 或 tokens 组成 batch，让同一次数据移动被更多计算摊销。这样付出的能耗不是一千倍，而是“一千倍除以 batch size”。

但 batching 不利于超低 latency。因此，hardware 的能耗结构会一路影响上层系统设计。训练 model 时，把 data set 组织成 batches、按 epochs 运行，看似是 model 选择，实际很大程度上是 systems 和 data I/O 的约束。理想状态也许是 batch size one training，但其效率远低于大 batch。

**Diana Hu：** 你会不会花几个星期，解决 batch size 等于一的训练？

**Jeff Dean：** 我最近更多考虑 inference，因为 inference 对低 latency 的要求更直接，training 并不一定需要极低延迟。我认为 inference hardware 还有很大专门化空间。

**Diana Hu：** 具体在想什么？

**Jeff Dean：** 尽量减少 data movement，使用极低 precision operations。如果已经知道实际需要哪种 precision，也许硬件就只支持那一种，不必为很多精度格式付出复杂度和能耗。

**Diana Hu：** 有人把 AI 看成一个巨大的 compression problem。只有真正理解数据，才能有损压缩后再恢复信息。

**Jeff Dean：** 如果真正理解数据，确实应该能够很好地压缩它。Transformer architecture 到目前为止是一种效果很好的方式。这是我的同事们做出的优秀工作。

### Model 之外，context engineering 成为关键

**Diana Hu：** 过去，AI progress 常等同于更多数据、更大 model 和更多 parameters。过去一年，进步越来越来自 model 周围的 retrieval、tools、memory 和 agent harness，大家把这些统称为 context engineering。

**Jeff Dean：** Model 只是整个系统的一部分。目标是构建能够解决真正有意义问题的完整系统。Model 需要知道如何调用 tools、retrieve 相关信息，也可能记住过去任务曾检索过什么，再把有用信息放进当前 context。

Context 中的信息对 model 非常清晰。相比之下，training data 的数万亿 tokens 被混合进数千亿乃至数万亿 parameters，特定事实并不总是清楚。当前任务直接提供的 context，更容易被 model 精确使用。

系统还要理解有哪些 tools，哪一个适合下一阶段，怎样把问题拆成一系列 tool calls，是否应该尝试多条路径，以及如何评价不同结果。复杂 agent 和 multi-agent systems 的 orchestration 会越来越重要。

**Diana Hu：** 这个机会对现场每个人开放。Training model 需要巨量 GPUs 和数据；做 context engineering，只需要调用 Gemini 等 API，再建设自己的 retrieval、tools 和流程。大家怎样才能真正擅长它？

**Jeff Dean：** 最好的方法，是亲自用 models、harnesses 和 tools 解决问题。观察 model 在哪里失败。很多时候，你不需要从外部调整 model parameters，而是可以提供更好的 guidelines，或者给 model 编写 skills，教它如何使用适合这类问题的工具。

这样会逐渐形成一个自我改善的 setup。你也会更理解，model 若想解决问题，还缺少哪些信息。

### 把 Jeff Dean 的性能优化方法写成 skill

**Diana Hu：** 你自己做过什么 context engineering？哪些 skills 或 tools 明显改变了工作流？

**Jeff Dean：** 几周前，我和 Sanjay 在改进一些 very low-level libraries 的性能。Google 内部有一个 microbenchmark library，可以测量各种 operations、填充 data structure 等任务的耗时。有些 data structures 会在 Google 数百万个 processes 中使用，所以性能很重要。

传统做法是先测当前 benchmark，修改代码，再重跑 benchmark，看性能是否改善；之后扩大 benchmark 范围，检查 cache footprint 等指标。

我们写了一个 skill，把人类工程师执行这些步骤的方法教给 model。它可以测量 benchmark、修改代码、再次测量效果并迭代。对某些问题，这套流程工作得很好。本质上，我们把自己解决问题的方法，转写成 model 可以执行的形式。

**Diana Hu：** 如果别人拿到这个 skill，岂不是也能像 Jeff Dean 一样做性能优化？这听起来价值无限。

**Jeff Dean：** 我和 Sanjay 几个月前公开过一份约三十页的《Performance Hints》，总结各种性能技巧。有人把它压缩后提供给 models，发现 model 对性能问题的 reasoning 变好了。

**Diana Hu：** 所以大家可以直接取得这份文档，让 model 学习这些提示，再优化自己的代码。它是公开的。

### 长期 agent 为什么在第 30 或第 50 步失控

**Diana Hu：** 很多人都见过 agent 在第 30 或第 40 步偏离目标。前十步不错，到第 50 步就开始不稳定。今天真正的约束是什么，是 context、evaluators，还是 open-loop system 中误差不断累积？

**Jeff Dean：** 我们当然希望 agent 运行很长时间，以解决更复杂的问题。但它们今天有时在调用 tools 十次后就开始失效。一个原因是，model 正在做自己缺乏经验的事情。它在某种 training distribution 上学习，一旦任务偏离熟悉分布，像多数 ML models 一样，performance 会突然下降。离 comfort zone 越远，失败概率越高。

可以给 model 提供 skills 和 hints，让它留在自己擅长的“明亮道路”上。也可以使用 multi-agent systems，让多个 agents 尝试不同路径，再由另一个 model 或 agent 评价哪些路径更有希望，淘汰已经偏离的方案。

这种 inference-time compute，本质上是在可能的解法空间中搜索。它能显著提高长期 agent flows 的 performance 和 reliability。

**Diana Hu：** Google 内部怎样实现？

**Jeff Dean：** 我们有 harnesses，也有大量适配内部开发环境的 skills，教 agents 使用 coding、code review、performance measurement、log fetching 等内部 tools。Base model 并没有在 Google 专有日志系统上训练过，但有了正确的 skill definition，就能有效使用它。这样可以显著提高 agent 的实用性。

### 两三人团队在哪里还能赢过 Google

**Diana Hu：** Google 从 processor 到 product 都在 co-design。哪些层会由 Google 持续积累优势，哪些地方两三人团队仍能赢？

**Jeff Dean：** Google、Gemini models 和我们的 hardware infrastructure，目标是建设几乎什么都能做的 general models。但正因为要通用，我们不会把足够多注意力放在每一个具体领域。

创业团队可以选择自己真正热爱的 domain，设计更好的 product surface，配合专门 skills，甚至训练不在通用 model 能力组合中的 specialized model，做出准确度和质量都很高、使用体验令人愉快的产品。这是两三个人在一个房间里也可能拥有的优势。

但要警惕 general models 正在迅速扩大能力边界。创业者必须判断：自己的能力优势能否持久，frontier model 会在六至十二个月内补上，还是还需要两三年？这个时间差应进入选题决策。

**Diana Hu：** 创业者具体应该怎样选择？

**Jeff Dean：** 第一，选一个你极其兴奋、真心想建设、也相信对世界有用的问题。如果每天醒来都不想做，或者做出来对任何人都没有价值，那么起点就错了。

第二，测试当前 general models 在这个领域能做什么。如果 model 完全失败，这是好信号。如果它已经能做一部分，只是还不够好，反而未必是好信号，因为更多 training data、更大规模或下一代 model 很可能很快补齐。

应该寻找 general model 成功率只有 0% 或 1% 的问题，而不是已经达到 20% 的问题。

**Diana Hu：** 这些问题通常是什么形态？是否来自 training set 之外？

**Jeff Dean：** 一种情况，是产品可以接触 general model 没有的数据。例如，Google 擅长组织世界信息，但帮助用户组织全部 personal information，可能需要只有产品自身能取得的私有 context。这会形成优势。

另一种情况，是某个非常困难的窄领域。如果取得正确 training data，就可以用相对可负担的 compute，训练一个高度准确的 niche model。它不必通用，却能成为解决重要问题的 building block。

AlphaFold 是例子。它专门解决 protein folding，不是 general model，却极其成功，成为研究蛋白质结构的重要工具。Material science、chip design 等领域也可能适合这种路径。

### AI-native founder 的核心能力是写清楚规格

**Diana Hu：** 假设创业者已经选好问题。你说过，管理 50 或 100 个 agents 的关键，是写出非常清晰的 design docs 或 specs。怎样练习？

**Jeff Dean：** 和 virtual agents 合作时，把想要的结果说得越清楚，成功率越高。清晰 specification 为 agent 提供目标、边界和规则；描述过少，agent 就必须猜测你的意图，而它猜出的东西可能和你想象的不同。

Computer science 从一开始就强调，写代码之前先定义软件要完成什么。今天 agent 可以负责写代码，但 specification 的重要性反而上升。过去交给聪明的人类工程师，对方拥有组织 context，也会主动追问；agent 有时也会问，但可靠性还不相同。

Software translation 是当前 coding agent 非常擅长的任务，因为已有实现就是极其详细的 specification。把 Python 系统改写成 Go 时，model 可以读取全部 Python tests，把 tests 一起翻译成 Go，比对两个版本的行为，直到差异消失。目标定义得如此清楚，model 就能非常有效。

### 当数百个 agents 都会写代码，稀缺的是品味

**Diana Hu：** 假设每位创始人都能同时运行数百个 agents，所有代码都由它们完成，最稀缺的技能是什么？

**Jeff Dean：** 是对“应该让 agents 做什么”拥有极好的 taste。研究者可以掌握全部工具和技巧，但真正决定成果的往往是选择哪个问题。把一个无聊问题执行得非常漂亮，不如选中一个重要问题并成功解决。

人类会负责引导大量 AI-assisted computation，更快完成工作。Model 未必擅长最高层的判断，所以最应该专注的是：你究竟希望 models 完成什么。

**Diana Hu：** Taste 听起来很抽象，怎样具体训练？

**Jeff Dean：** 一部分来自经验。做过很多不同问题之后，会更清楚哪些新问题刚刚变得可能，哪些旧技术可以重新组合，还缺哪一个 open problem 才能产生真正有用的结果。

可以写下一批你认为未来十二个月会变得重要的事情。你也许只选其中一个去做，但十二个月后回头检查：哪些判断真的重要，哪些被别人做出来，哪些仍未发生。这样会给自己的判断系统增加更多 samples，逐渐训练 taste。

### 一个疯狂假设：允许晶体管每天出错二十次

**Diana Hu：** 我们刚才还谈到，用很疯狂的 thought experiments 训练判断。

**Jeff Dean：** 对。不要把所有人默认的前提都当成不可改变。过去六十年，silicon chip design 和 fabrication 不断缩小 transistor，并努力把 error rate 降到极低。行业默认，相同设计生产出的每一颗 chip 都应该完全相同，不允许 bits 翻转，还用 ECC memory 等机制增加安全余量。

但在 macro scale 的 distributed systems 中，我们并不假设每个零件可靠。我们用会坏的 disks 构建可靠的大型 distributed file systems。单块盘可能失败，但数据不能丢。因此会在不同 machines、不同 racks 保存三份数据，也会使用 Reed-Solomon encoding，使 rack switch、machine 或 disk 失效时仍能恢复。

那么，为什么不在 transistor scale 采用更极端的相同思想？可以做一个 thought experiment：如果一套系统里的 transistors 不是每一百万年才出一次错，而是每天出错二十次，会怎样？

**Diana Hu：** 天哪。

**Jeff Dean：** 这会形成完全不同的 design point，也许允许 fabrication 采用全新方法。若要把 signal 从一处传到另一处，而 transistors 极不可靠，就可能沿多条冗余路径同时传输，确保至少一条成功。

我不是说行业一定应该这样做。很多假设延续五十年，是因为它们确实有充分理由。但应当定期重新检查。这个想法也很像 neuromorphic computing 或 human brain：大脑里的单一路径并不十分可靠，重要信号通常有多条路径保证传达。

### MapReduce 也来自一次重新抽象

**Diana Hu：** 过去有哪些疯狂假设，最后真的变成重要系统？

**Jeff Dean：** TPU 是一个例子：在 ML 还没有今天这么重要时，就假设可以为一个看似很窄的问题领域专门设计硬件。

MapReduce 是另一个例子。我、Sanjay 和同事曾反复建设 Google crawling 和 indexing systems，写了大量手工 parallelized code，还要加入 checkpointing，确保任务运行在一百或一千台 computers 上、部分机器死亡时仍能恢复。

这些复杂代码常把真正简单的业务逻辑淹没。比如，我们只是想读取全部 webpages，生成从 URL 到页面语言的 mapping，却要同时处理并行、容错和重启。

我们想起 functional languages 的训练，发现可以把一大类问题抽象成 Map 和 Reduce。上层只描述计算，下层 library 统一处理 checkpointing、parallelization 和 reliability。我们问的是：如果眯着眼看，能否让很多不同问题都符合这一抽象？答案是可以。MapReduce 因此成为 Google 大规模、可靠计算的核心方法。

### AI 构建 AI，自动化科学方法

**Diana Hu：** AlphaChip 可以做 chip layout，AlphaEvolve 会提出 solutions、evaluate 并保留有效结果。你们似乎正在建设能不断叠加、由 AI 构建 AI 的系统。

**Jeff Dean：** 更普遍地说，scientific method 的循环是：提出实验、实现实验、运行评价、获得结果。今天越来越多问题可以把整个循环自动化，不只是做几次实验，而是高频运行大量实验，因为 loop 的 latency 可以大幅降低。

这将影响 science、engineering、ML model design 和 chip design。Orchestration framework 可以接收 high-level objective，把它拆成 sub-problems。每个子问题进入自动实验循环，探索最好的解法；之后框架再把各子问题结果组合成高层答案。

这会加快 ML progress、science 和 engineering，影响非常大。

**Diana Hu：** 最适合的领域，似乎是有高质量 evaluators、甚至接近可形式化验证的问题。

**Jeff Dean：** 对，但有时 evaluator 本身需要变快。大约十年前，我的同事研究 quantum chemistry。要判断某个 molecule configuration 的性质，可以运行 density functional theory simulator，但计算一个样本可能要一整夜。

他们收集昂贵 simulator 的输入和输出，再训练一个 neural approximation。这个 learned evaluator 几乎同样准确，却快 300,000 倍。

这会彻底改变科学方法。如果有一千万个候选要筛选，过去可能需要六个月并到处筹集 compute；有了高速近似 evaluator，吃午饭的时间就能筛完。很多领域都可能构建更快的 validation models，用近似但足够准确的答案，加速整个 experimental loop。

### Model 自我改进与每单位算力的发现数量

**Diana Hu：** 哪些问题最可能从这种加速科学方法中获益？

**Jeff Dean：** ML 本身显然是一个。能否让 model 通过大量实验 recursively self-improve？

今天，大型研究团队先提出 ideas，运行一批 small-scale experiments，挑出有效方案，再放大规模验证，最后把结果整合成下一版 model recipe。没有根本障碍阻止我们把这个循环大幅自动化。

Model 可以自己决定探索哪些方向，或者由人类给出高层提示，例如尝试某类新 architecture。之后系统运行许多实验、识别有效结果，并更快地纳入下一版设计。最终要优化的指标，是每单位 compute input 能产生多少 discoveries。

### Distillation 论文被 NeurIPS 拒绝

**Diana Hu：** 每个人未来都会遭遇很多拒绝。2014 年，你、Geoff Hinton 和 Oriol Vinyals 写过 model distillation 论文，用大型 teacher model 训练更小、更便宜、parameters 更少的 model。今天整个行业都在使用这项技术，但论文当年被 NeurIPS 拒绝。

**Jeff Dean：** 我不责怪 program committee。论文通常只有三位 reviewers，其中有人认为它“不太可能产生重大影响”。但我们当时知道这是极其重要的问题，因为如果要让更多人在 speech、vision 等领域使用高能力 model，就必须把大 model 的能力转移到更便宜的 model。

Reviewer 也许没有运营 large-scale AI services 的经验，更关注它是否属于基础理论突破。论文被拒绝没有关系，我们把它放到 arXiv，大家读到了，也开始使用。

今天，Gemini 会用大型 Pro model 帮助生成更小的 Flash models，这正是 Flash 在同等 size 和 speed 下保持很强能力的原因之一。

**Diana Hu：** 所以，即使被拒，也要继续。

**Jeff Dean：** 这正是我会从 distillation 故事中“提炼”出的教训。

### 25 岁的 Jeff Dean 今天会去 frontier lab 还是创业

**Diana Hu：** 1999 年你加入 Google 时，它只有约二十人。如果把 25 岁的 Jeff Dean 传送到今天，他会加入 frontier lab，还是自己创业？

**Jeff Dean：** 这是很个人的选择。对我而言，最重要的问题是：你是否真的关心自己在做的事？如果和喜欢的同事取得进展、解决问题，它是否会以正面方式改变世界？它可以帮助很窄的群体，比如 biochemists；也可以帮助 programmers 或所有互联网消费者。

应该努力创造正面影响，和喜欢的人一起工作，并尽全力做好。

Frontier lab 或成熟大组织提供结构、很多拥有不同知识的优秀同事、丰富问题，以及能影响全球大量用户的平台。两三位朋友组成 startup，则需要对一个问题非常有热情，也要承担项目失败和无法扩张的风险，但成功时会非常有回报。

无论走哪条路，都问自己：如果最好的结果发生，世界会不会明显变好？如果世界只会说“有点酷，但也就这样”，那不值得投入人生。

### 怎样寻找聪明且适合长期合作的人

**Diana Hu：** 你指导和管理过许多工程师，也建设过巨型系统。小团队怎样找到聪明人，并发挥他们的能力？

**Jeff Dean：** 要找在团队所需领域拥有真正技能的人，也要找你愿意长期相处、见到就开心的人。解决困难问题会花大量时间，所以团队成员最好 low ego、愿意合作，并拥有互补技能。

我很喜欢小团队里每个人都知道一些别人不知道的东西。大家共同完成任何一个人单独都做不到的事，同时在过程中互相学习。

应把 engineering 或 research career 看成一个装满 techniques 的 tool belt，不断添加新工具。未来遇到问题时，也许它需要四种特殊工具，而你原本只有三种。工具越多，可解决的问题越多。

### Jeff Dean 希望下一代解决的问题

**Diana Hu：** 现场很可能有人最终做出像 MapReduce、TPU 或 distillation 一样重要的成果。你希望他们解决什么问题？

**Jeff Dean：** 世界很大，问题很多。我先列几个，并不是完整清单。

我尤其期待全新的 hardware approaches，包括刚才那类关于不可靠 transistors 的思想实验，以及效率高得多的 inference hardware。

ML 也可能出现完全不同、data efficiency 高得多的 algorithms。今天的 large-scale models 到训练完成时，看到的数据可能是一个人到十八岁接触信息量的一千倍，但十八岁的人类在很多任务上仍然更强，在另一些任务上也能与 frontier models 相当。我们能否构建数据效率高得多、可以持续学习并从自身行动中学习的系统？

Continual learning 是非常重要的问题，multi-agent interactions 也值得研究。

还可以思考，怎样改善全球人们之间的 discourse。能否让交流更文明，能否按兴趣帮助一个人认识世界上本应认识的其他人？

世界上有许多很酷的问题。我们应该努力让更多真正有价值、真正令人兴奋的事情发生。

**Diana Hu：** 非常好。谢谢你，Jeff Dean，今天就到这里。

**Jeff Dean：** 谢谢大家。
