---
访谈时间: 2026-08-12
YouTube发布时间: 2026-08-12T15:41:58Z
访谈时间说明: 使用 YouTube 发布时间；内容来自 Startup School 2026 演讲及问答，未能独立确认录制日期
youtube_video_id: cRZNwgvcWUg
嘉宾名字: Chelsea Finn
嘉宾公司名称: Physical Intelligence
参与嘉宾:
  - 姓名: Chelsea Finn
    公司或机构: Physical Intelligence
    职务: 联合创始人
播客名称: Y Combinator
播客url地址: https://www.youtube.com/watch?v=cRZNwgvcWUg
字幕来源: YouTube automatic_captions en-orig
全文提及的关键名词:
  - Physical Intelligence
  - physical AI
  - robotics
  - reinforcement learning
  - long-term autonomy
  - memory
  - PIO7
  - compositional generalization
  - throughput
  - teleoperation
  - foundation model
  - robot data
  - open source
companies: []
industries:
  - 机器人
technologies:
  - LLM
  - 强化学习
  - 预训练
keywords:
  - 开源
tags:
  - 机器人
  - LLM
  - 强化学习
  - 预训练
  - 开源
---

# Chelsea Finn: This is the State of the Art in Robotics

## Transcript

Chelsea Finn：大家好，今天我想谈谈 physical intelligence 的最新进展，尤其是通用机器人如何在真实世界中发挥作用。

两年前，我创办了 Physical Intelligence。我们真正关心的问题是：能不能开发出一种技术，让任何机器人完成真实世界中的任何任务？我去年也在这个活动上分享过进展。当时我们已经让机器人完成了非常复杂的任务，例如把衣物从烘干机中取出并折叠；我们还第一次展示了机器人在从未见过的房间里完成有用任务。

过去一年，我们又让机器人完成了很多工作：清洗油腻的锅、削胡萝卜、制作烤奶酪三明治、切西葫芦等。但今天我不想只展示机器人完成不同任务的精彩视频，而是想讨论，让机器人在真实世界有用究竟需要什么。

这里有两个方面。第一是 general purpose，也就是如何开发通用模型；第二是如何把这些模型带到真实世界，让它们真正产生影响、对人有用。我先从真实世界中的可用性开始。

要把一项技术带到真实世界，回顾过去 AI 是如何进入生产环境的很有帮助。如果按照主要生产发布来排列，早期 machine learning 的实际应用包括商品推荐和广告排序。大约五年后，deep learning 被用于相同类型的任务，这是一次重要进步，因为 deep learning 不需要为每一种复杂输入和输出专门设计算法，更容易迁移到其他应用。

再往后，2022 年 ChatGPT 发布，这是 machine learning 和 AI 进入生产应用的另一个重要时刻。它是第一个被大量普通用户直接使用的 general-purpose model，五天内就达到一百万用户。最近，Claude Code 和其他 coding agents 也展示了通用模型在真实世界中的实用性。

从这些应用中可以看出，generalist models 正越来越多地被用于现实问题。但还有一个细节：在过去真正产生利润的 machine learning 应用中，通常是客户根据 AI 的推荐做最终决定。只要客户还在做决定，系统偶尔犯错通常仍然可以接受，因为人可以识别错误，或在错误发生后采取不同动作。因此，这些系统不必百分之百完美，也可以很有用。

Physical AI 和 robotics 则不同。机器人在物理世界中直接做决定，决定会影响真实物体和真实的人。只有在机器人能够高度自主运行时，它才会真正有用。因此，physical AI 必须比过去部署的许多 machine learning 系统少犯很多错误。

最近一个令人鼓舞的例子是 Waymo。一年前，Waymo 已经超过每周 25 万次 autonomous rides。这说明，基于 machine learning 的系统确实可以直接在物理世界中以可信、自治的方式运行，也让我们对其他 physical AI 应用抱有希望。

如果要开发真实世界中的通用机器人，就必须让机器人长时间自主运行，而不是让人在旁边不断根据模型的预测替它做决定。

## 长期自主运行

假设我们希望机器人制作 espresso。要让它真正有用，它必须可靠地制作 espresso，这样我们才不需要频繁 babysit 它。这个任务本身就很难：机器人需要用非常精确并且有力的控制把 portafilter 插入正确位置；要平稳处理装有液体的杯子，不能洒出；还需要准确把握时间，而时间控制在很多其他 machine learning 领域并不是核心难点。更重要的是，我们希望它的可靠率超过 90%。

传统 machine learning 的第一步是收集数据集、训练模型并评估模型质量。第一次通常很难就达到足够可靠的水平。实际做法是不断迭代：收集更多数据，提高 label 质量和细节，收集 edge cases，也就是模型工作不好的场景，再调整数据集的平衡。这样一般能提高可靠性，但人手动调整的过程最终会受到人的精力限制，很难做到极高可靠性。

更好的方案是让 AI 系统自己寻找需要更多数据和 supervision 的位置，自动迭代目标场景。如果可以自动运行很多轮，而不是依靠人反复调整，就有机会让 physical AI 达到 99% 以上的可靠性。这个方法很像 reinforcement learning：机器人尝试任务，从失败中学习，再自行变得更好。

## 让机器人强化学习可以扩展

语言模型有 PPO、GRPO 等算法，通过大规模计算扩展到复杂推理。但把同样的方法直接应用到 robotics 存在困难。语言模型的一次尝试只是运行一次模型；如果要做一百万次一分钟的机器人轨迹，粗略估算就相当于 700 个 robot-days，才能为一个甚至比 espresso 更短的任务获得足够高的可靠性。这里不是单纯增加 data center compute，而是让真实硬件在真实世界里一次次尝试任务，成本完全不同。

因此，需要更高效的迭代算法。第一个低效点是 dead-end trajectories。比如机器人要把纸箱折好并堆叠，却不小心同时抓住两个贴在一起的箱子。如果让它继续，它可能一直尝试同时折两个箱子，这些数据并不能教会模型如何改进，反而浪费机器人在错误路径上的时间。

我们可以让人尽早介入，示范如何恢复。操作员会通过 teleoperation 分开两个箱子，引导夹爪重新进入正确位置。如果机器人还不能自行恢复，人就再次介入，让它回到正确轨道。这样可以尽早结束错误轨迹，或让机器人学会恢复，而不是把时间耗在无用尝试上。

第二个低效点是，PPO 和 GRPO 一类算法会针对同一个 prompt 做很多次尝试，可能滚出 10 次或 50 次，用来估计哪些 response 好、哪些 response 坏。机器人可以把这个成本在不同 prompt 之间摊销，学习一个更一般的 value estimate，用来判断什么是正向进展，什么是负向进展。

具体做法是训练 general-purpose value function，输入大量机器人经验视频。它可以判断，机器人在折叠衣服时把衣服重新弄散是负向进展；也能判断它是否在向目标前进。同一个 value function 还可以用于完全不同的场景，例如从冰箱中取出物品。一个预测距离成功还剩多长时间的通用 value model，可以大幅减少从经验中学习所需要的尝试次数。

整个 improvement algorithm 的流程是：先用多样数据训练 foundation model；再让机器人从模型中获得经验，并在人需要时介入，避免 dead-end trajectories；然后训练一个通用 value function，估计什么是好、什么是坏；最后用这些经验继续改进模型。这种方法可以把 foundation model fine-tune 到更高性能。

在制作 latte 的任务中，机器人负责 espresso，人负责蒸牛奶。模型直接根据机器人摄像头的图像控制各个关节。它需要把 portafilter 插入正确位置，等待适当时间让 espresso 流出，把蒸好的牛奶倒入杯中。最难的一步是把装得很满的 latte 从操作位置移动到杯垫上。机器人必须精细保持杯子平衡，让液体不洒出来。

我们不只是运行一次这个 policy，而是让它连续运行 13 小时，测试它是否能长时间稳定制作 latte，而不是只在演示中成功一次。结果表明，机器人可以在很长时间内保持足够可靠，不会频繁犯错。

在这个过程中，机器人直接从自己的 camera images 预测动作并控制 joints。它必须精确处理 portafilter 的插入、等待 espresso 流出的时间、把牛奶倒入杯子，以及最后把一杯几乎装满的 latte 从工作位置送到 coaster。最后一步看似简单，实际上对力、速度、平衡和液体状态都很敏感。它不能只在某一帧看起来正确，而要把整条动作链平稳地完成。

同样的算法也用于其他任务。Dandelion Chocolate Factory 离我们办公室只有几个街区，我们把他们通常由人完成的工作交给机器人：组装纸箱、贴标签和堆叠纸箱。我们还把算法用于折叠和收起衣物，测试机器人能否在多个此前没有见过的家庭环境中处理没有见过的衣物，而不是只在一个固定环境里重复任务。

视频不一定能展示全部信息，所以我们还量化测量 reliability 和 speed。我们关心每小时能组装多少纸箱，也就是 throughput，因为 throughput 同时反映成功率和速度。从 pre-training 到 SFT，再到 RL post-training，success rate 和 throughput 都显著提高。仅 RL 阶段就带来了约 2 倍的 throughput 提升。制作 espresso 的 success rate 达到 90% 以上。

这部分的结论是，我们可以为复杂的 robot manipulation tasks 建立可扩展的高可靠性 recipe。通过经验和人工介入，throughput 提高约 2 倍，更重要的是，机器人可以在真实工作流中长时间自主运行。不过，机器人仍然会犯错，也仍然比人慢，还有大量提升空间。我们只运行了少数几轮 improvement，继续增加迭代可能带来更高可靠性。

## Memory 与长任务

让机器人自主运行更长时间的另一个关键 ingredient 是 memory。很多 state-of-the-art robotics foundation models 没有 memory 或 context，只根据当前传感器和摄像头读数预测下一步动作。没有 memory，机器人可以完成短 motor skills 和重复任务；但如果任务包含多个连续步骤，就必须记录已经完成了哪些步骤。

为什么这些模型没有 context？一个原因是直接把过去的视频塞进模型非常昂贵。假设把 10 秒视频作为 context，视频以 robotics 常见的 50 Hz 采样，同时输入机器人四路摄像头，每张图像约 256 tokens，那么仅 10 秒就要输入约 50 万 tokens。即使降低到每秒一帧，也要输入约 1 万 tokens，而且只覆盖 10 秒记忆。

我们开发了多时间尺度的 memory。短期部分保留约 10 秒视频，但用比直接输入更高效的方式计算。对于几分钟或几小时的长期记忆，不需要保存每一帧视频，而是用 text 总结过去发生了什么，再把过去 10 到 15 分钟压缩后的文字记忆提供给模型。

有了不同时间尺度的 memory，机器人可以连续 10 到 15 分钟完全自主完成清理厨房的任务。它不是重复制作 espresso，而是要擦拭台面、用纸巾擦干、扔掉纸巾、把芥末放回冰箱、把餐具放进橱柜、清洗水槽里的脏盘子等。memory 让它能够跟踪这些步骤，并在任务过程中保持进度。

David Hoffman：所以，长期 autonomy 和短动作的区别，不只是让同一个动作重复更多次。清理厨房要求机器人记得自己已经擦过哪一部分、哪些物品还没有收好、下一步应当处理什么。如果没有 memory，它看到的只是当前画面，无法知道这是一项已经进行到中途的长任务。

Chelsea Finn：对。短期 video memory 负责保留当前动作所需的细节，例如一个物体刚刚怎样移动；长期 text memory 则保留任务进度和更长时间尺度的事实。这样可以把有限的 token budget 用在真正需要视觉精度的部分，而不是把几分钟内的每一帧都重复送进模型。

对于机器人来说，context 的设计本身也是系统的一部分。你不能简单地把语言模型的长上下文方案搬过来，因为机器人需要实时控制，摄像头数量多，控制频率高，延迟和成本会直接影响动作。将视频压缩成不同时间尺度的记忆，是在实时性、信息量和成本之间的折中。

## 通用 physical intelligence model

接下来，我们把长期自主运行的 ingredients 放进一个 general-purpose model，让一个模型完成此前展示的各种任务。要理解 robotics 的位置，可以回顾 generalist AI 过去 15 年的演进。

2012 年，一个从头训练的 deep learning 系统第一次超过为特定 benchmark 专门设计的算法。当时是 ImageNet 图像分类 benchmark，过去的方法都为这个任务定制，而 deep learning 系统却以更一般的方法超过了它们。几年后，行业从每次都从头训练转向使用 pre-trained models，再针对 downstream tasks fine-tune。BERT 和 ImageNet 预训练模型都说明，预训练可以带来更好的下游性能。

之后，行业从 pre-training 加 fine-tuning 转向可以 out of the box 使用的 generalist models，GPT2 以及今天的大多数 consumer models 都体现了这一变化。2021 年左右，我们还看到了 compositional generalization 的早期迹象，例如 DALL·E。

Physical AI 三年前还处在很早阶段。2023 年，机器人项目通常从头收集 bespoke dataset，再针对单个项目训练模型。这类似于每个图像分类项目都从头收集 ImageNet。如果每个机器人项目都要重新收集数据集，就很难进步到 general-purpose model。最近 robotics 逐渐拥有了一些好用的 pre-trained models，但还没有真正进入 out-of-the-box 和 compositional generalization 的阶段。

我们希望达到两个目标。第一是 out-of-the-box model，从类似 BERT 的预训练模型进一步走向类似 GPT 的通用模型。现在，如果想让机器人在某个任务上达到最佳性能，通常仍然需要 fine-tuning。我们之前展示的开锁、RL post-training 制作 espresso 等任务，都针对单个任务做了 fine-tune；这并不是通用模型。

第二个目标是 compositional generalization。比如把 avocado 和 chair 两个概念组合起来，说明模型至少对 avocado 和 chair 各自是什么有一定概念理解，能够把两者组合成一个同时包含两个概念的结果。这还带来 data efficiency：训练数据不需要覆盖所有概念组合，不需要在数据集中真实出现 avocado chair，模型也可能生成或完成相关组合。

经过实验，我们使用尽可能多、尽可能多样的数据：不同质量的 robot demonstrations、机器人 policy rollouts、强化学习阶段的训练数据、人的视频以及 web data。为了处理这些异质数据，模型需要足够 capacity，也需要得到足够多的 context。

Foundation model 的输入包括 memory、整体 instruction、当前 subtask instruction，还包括说明数据质量、episode 长度等信息的 metadata。我们还可以提供 sub-goal image，告诉模型几秒钟后应该达到什么样的视觉状态。部署时，高层 policy 预测下一步 subtask，world model 生成下一个 sub-goal image。

我们称这个单模型为 PIO7。它可以折叠有领衬衫，完成非常精确的装配步骤，把螺丝插入并钻进机器人手臂，也能替垃圾桶更换垃圾袋。

最关键的比较是，PIO7 这个预训练单模型与此前针对咖啡制作、纸箱组装等任务专门训练的 PIO6 specialists 相比如何。测量 throughput 和 success rate 后，我们看到 PIO7 在多个任务上达到或超过通过 RL post-training 得到的 specialist，也超过了 SFT specialist。这说明一个模型可以 out of the box 高质量地完成很多任务，而不需要为每个任务单独 fine-tune。

David Hoffman：PIO7 的意义更像是一个起点，而不是一段孤立的 demo。它在折衣服、装配和更换垃圾袋之间共享同一个模型；当任务组合发生变化时，模型可以利用已有的 object concept、action concept 和环境理解，而不是把每种组合都当成新问题。

Chelsea Finn：compositional generalization 的价值就在这里。比如训练数据分别包含打开某种容器的技能和处理某种食物的技能，部署时可能遇到没有见过的 appliance 和新的物体。如果模型只记忆训练样本，它就会失败；如果它真正学到了一些概念和动作之间的关系，就可能把旧技能组合到新环境中。

## Compositional generalization

我们测试的第一个组合泛化场景是让机器人操作一个训练数据中极少出现的 air fryer：打开空气炸锅，把红薯放进去，再关上它。原本我们以为数据集中没有 air fryer，分析后发现实际上只有三段相关 episode，而且数量少到不太可能影响结果。机器人把打开、关闭 appliance 的技能与此前没有见过的物体组合起来，并且能由高层 policy 自主完成。

第二个测试是在任务和 robot platform 之间做组合泛化。我们有一个机器人平台上的折叠衣物数据，但没有在一个尺寸、关节长度和结构都完全不同的大型工业机器人平台上收集折衣数据。机器人却可以直接尝试在新的平台上折叠衣服。第一次看到它成功时，我们非常惊讶，因为新平台没有针对该任务的训练数据。模型还会生成 sub-goal images，帮助它判断怎样逐步接近折叠完成的状态。

新的机器人平台也是同样的测试。大型工业机器人的尺寸、linkage 长度和关节排列都与原来收集数据的平台不同，但折衣的任务结构仍然存在。模型利用 sub-goal image 逐步尝试，可能第一次速度较慢、需要小幅纠正，但最终能够完成任务。它不是凭空拥有完美技能，而是把已有知识迁移到新的 embodiment。

定量结果也显示，随着 PIO7 等更先进模型出现，在此前没见过的机器人平台上折叠毛巾和衬衫的性能显著提高，甚至接近 human teleoperation，尽管我们没有为这个平台收集折衣的专门训练数据。

我们还做了 ablation，测试多样数据和详细 prompting 各自有多重要。移除最丰富、最多样的数据后，模型在 held-out tasks 上的性能大幅下降；随机删掉 20% 数据，下降幅度则小得多。这说明真正多样的数据对于泛化到新任务非常重要。

我们也测试了 metadata prompting。如果没有 metadata，加入更多低质量数据时，性能可能从 80% 数据到 100% 数据反而下降；加入 metadata 后，即使增加低质量数据，性能仍然上升。这说明模型可以利用数据质量、episode 长度等上下文，从低质量数据中榨取更多价值，而不是把所有数据当成同样可靠。

David Hoffman：因此，训练数据不是简单的“成功或失败”二元标签。一个没有完成任务的 episode 可能仍然包含有价值的局部动作；一个成功的 episode 也可能包含不稳定的步骤。metadata 让模型知道应当如何解释这些数据，这对于把各种来源的数据放入同一个 foundation model 很重要。

Chelsea Finn：对。我们希望模型既能理解整体 instruction，也能处理当下 subtask，还能利用 memory 和未来目标图像。这样，训练数据中未必需要出现每一个完整任务，模型可以把局部技能、物体概念和任务进度组合起来。

因此，这一阶段的结论是：单模型可以达到或超过针对下游任务 post-train 的 specialists，类似从 BERT 风格的预训练模型走向可以直接使用的 GPT；同时，我们看到类似 DALL·E 的 compositional generalization，机器人可以把技能迁移到新的 appliance 和新的 robot platform。这里展示的视频和实验都是 out of the box 结果，没有额外 post-training，技术报告中还有更多实验细节。

## 当前部署和未来问题

如果回到 generalist AI 的时间线，我认为 physical intelligence 已经进入类似 GPT 和 DALL·E 的阶段，而且只用了几年。模型不只在实验室里展示，也开始部署到真实环境。YC 公司 Ultra 和 Weave 已经把 PI models 进行 fine-tune 并用于折叠衣物、仓库包装等任务。模型还可以适配很多 robot embodiments：双臂平台、无人机、四旋翼、手术机器人和拖拉机。

这说明 physical intelligence 不只是 demo 或研究成果，也开始在真实世界产生影响。未来几年，我们会看到更多机器人真正部署到物理环境中。

部署也会带来新的工程问题。模型必须在机器人上稳定运行，数据管线要可靠，硬件和 software stack 要能够处理长时间运行，企业还要评估安全、维护和失败恢复。对于仓库包装、折叠衣物、拖拉机或手术机器人来说，模型在实验室里偶尔成功远远不够；真正的标准是它能否在没有人持续 babysit 的情况下，完成实际工作流。

Physical Intelligence 也在招聘。如果有人对这些工作感兴趣，可以查看开放职位。

David Hoffman：距离 robotics 的 ChatGPT moment 还有多远？它会是什么样？

Chelsea Finn：我不确定它会像语言模型中的 ChatGPT moment。ChatGPT 五天获得一百万用户，但 physical model 的分发渠道会慢得多，因为你必须有一台真实机器人。Waymo 的部署已经非常惊人，但把模型安装、验证到真实设备上仍然需要时间。机器人行业可能不会出现一个拥有 ChatGPT 那样分发速度的单一时刻。

不过，从能力来看，模型已经开始在真实世界中有用。达到 ChatGPT 类似的能力水平，很可能就在未来几年内。

物理模型的发布节奏也会受到硬件分发速度限制。语言模型可以通过网页或手机快速触达用户，但机器人模型需要安装在具体 embodiment 上，经过校准、测试和安全验证。因此，机器人行业可能不会出现一个单日爆发的用户数曲线，而是通过不同公司、不同平台和不同工作流逐步扩散。

David Hoffman：小团队什么时候应该从扩展 per-site models 转向 generalist policy？

Chelsea Finn：至少可以从 generalist policy 开始，再立即针对自己的任务 fine-tune。现在已有很强的开源 generalist policies，例如 PI0 和 PIO5，很多人已经从中获得实际价值。我们也在和 tractor company、Ultra、Weave 等伙伴合作，把最新模型用于他们的应用。

唯一不适合直接使用大模型的场景，是非常受限的环境。例如某些手术机器人位于地下手术室，没有互联网连接，GPU 也很弱。这时可以在 workstation 上做 local inference，但要认真考虑模型大小和硬件限制。除此之外，直接从 PIO5 或自己喜欢的模型开始 fine-tune，通常是很好的路径。机器人领域仍有大量工作要做，关键是把技术可靠地带入现实环境。

David Hoffman：机器人行业发展这么快，今天读 PhD 对想进工业界的人有什么优点和缺点？

Chelsea Finn：我原本并不打算读 PhD，想直接进入工业界。我的父母都是工程师，也在工业界工作。我父亲甚至曾经说不会雇一个 PhD，所以我一度觉得读 PhD 可能会妨碍就业。不过他在 civil engineering，情况不同。

我后来很喜欢自己的 PhD。PhD 是学习如何处理 uncertainty、如何选择好问题的机会。在 research 中，没有人把问题交给你，你必须自己选；你也不知道这个问题在六个月、两年或十年内能否取得进展。这种对不确定性的训练非常有用，尤其适合 startup 和 AI frontier，因为今天没有人知道让模型持续变强的最佳路线是什么。

PhD 还提供了自由研究令人兴奋问题的机会。但工业界同样有大量机会。机器人系统需要 software stack 稳定运行，需要硬件，需要 machine learning infrastructure 和 data infrastructure。很多工程工作不需要 PhD，研究工作也越来越包含工程。最终取决于个人目标；如果你喜欢研究、享受在前沿处理困难问题，PhD 仍然是很好的路径，但工业界也有很多优秀选择。

读 PhD 的价值不只是发表论文或学习某个具体算法，更在于训练自己在不知道答案时继续工作。机器人和 AI 的 frontier 仍然充满不确定性，很多看似合理的路线可能在几个月后被新结果推翻。能否判断问题是否值得做、能否承受长期没有明确反馈，对研究和创业都很重要。

反过来，工业界的优势是可以直接面对真实约束。模型要在有限的 compute 上运行，hardware 要可维护，数据管线要稳定，产品要满足用户和业务需求。这些工作同样需要很强的技术判断，不应当被看成 PhD 之外的次要选择。

David Hoffman：语言模型从互联网学习，但机器人没有 internet-scale 的 physical experience data。机器人对应的数据从哪里来？

Chelsea Finn：machine learning 的原则是 train 要匹配 test。语言模型训练的是互联网中的语言，因为模型未来要预测、补全文本并回答问题；互联网正好包含大量这类数据。

机器人对应的数据就是机器人在真实环境中运行的 experience。Physical Intelligence 通过 teleoperation 收集机器人完成各种任务的初始数据，长期来看，还需要收集机器人部署后的 autonomous experience。就像语言模型现在会运行模型来生成 synthetic data，未来机器人也会在许多真实环境中尝试任务，产生大量经验数据。

人的视频、YouTube、web data 和带 caption 的图像同样有用。图像可以告诉模型厨房里水槽右边有冰箱，人的视频也能提供关于任务和环境的知识。这些数据可以帮助训练能够理解长期任务、进行 multimodal reasoning 并控制机器人的 frontier model。

但人类视频不能替代机器人自身的 experience。看 Roger Federer 打网球，不代表我就能像他一样打球；机器人看人做事，也不能直接学会在自己的 platform 上完成同样动作。机器人必须在自己的 embodiment 上积累真实经验。未来需要大型数据集，human video 有用，但真实 robot experience 是关键组成部分。

这些数据还必须覆盖失败和恢复。只收集成功示范会让系统不知道遇到偏差时怎么办；teleoperation 的价值不仅是教机器人完成动作，也可以让人展示如何从错误状态恢复。随着机器人在真实环境中自主运行，它们会产生更多边缘情况、失败轨迹和修复经验，这些经验能够反过来训练下一代模型。

但真实经验的成本意味着，数据获取策略会影响行业结构。硬件数量、数据收集速度、不同平台之间的兼容性，都会决定一个团队能否扩大训练规模。开放模型可以降低 software 门槛，却不能完全消除真实世界数据和机器人 hardware 的成本。

David Hoffman：通用机器人模型会像大型语言模型一样通过 open source democratize，还是 embodied data 和硬件成本会让最好的模型集中在少数资源丰富的实验室？

Chelsea Finn：embodied data 和硬件的成本确实可能让 robotics 的情况不同。互联网上很难直接获得这类数据，模型 distillation 也更困难。但我们已经看到大型数据集和强模型开源，很难确定最终会怎样。

即使语言模型领域有闭源公司，很多公司也会开源，例如 Gemma 和 GPT 的开放版本。开源可以帮助建立围绕技术的生态。因此我仍然乐观，认为 robotics 会有强大的 open source community，但它未必完全复制语言模型的路径。

David Hoffman：模型是直接输出 raw motor commands，还是输出目标手部位置，再由 controller 求解关节角度？

Chelsea Finn：我们展示的模型主要输出 target joint positions，也就是每个关节需要达到的角度，再由 PD controller 追踪这些目标。模型也训练了 target gripper positions，表示夹爪在三维空间中应该处于什么位置；也可以从中反推出关节位置。另一条路线是直接输出 motor torques、voltages 或 efforts。

不同方案各有优缺点。直接输出 voltage 可能让模型控制更 stiff 或更柔软的动作；如果使用固定 controller，模型就不能控制这一维度。我们发现 joint control 和 gripper 的三维空间 control 都运行良好，目前这不是 bottleneck。相比之下，我更愿意把注意力集中在真正的 bottleneck 上。

David Hoffman：机器人需要 imagination，也就是在动作前想象下一步应该发生什么吗？

Chelsea Finn：PIO7 有类似能力，可以想象未来图像，再努力达到那个状态。在折衣实验中，使用这种 future-image imagination 的性能确实优于不使用。但模型在没有它的情况下也表现得出乎意料地好，所以我们没有把它作为唯一重点。预测未来可能是一个很有意义的训练目标，但现在还很难判断 imagination 是否是不可替代的关键组件。经验上它有帮助，但帮助程度可能没有预期那么大。

David Hoffman：现在机器人任务很惊艳，但动作很慢。怎样提高速度？

Chelsea Finn：reinforcement learning 已经带来速度提升。我们还有一个叫 RL token 的 release，展示了比 human teleoperation 更快的策略。一个瓶颈是 teleoperation 本身，因为这是教机器人最简单的方法，但人操作机器人时速度较慢。接下来要么让数据生成得更快，要么让 policy 比数据更快。我们已经看到 policy 稍微快于数据的证据，下一步是继续扩大这种优势，或直接改进数据收集速度。

David Hoffman：最近看到机器人完成的最令人惊讶的任务是什么？接下来想让它完成什么？

Chelsea Finn：最惊讶的不是某一个任务，而是 PIO7 在组装 pinwheel 时展示的能力。训练数据中，每次都是用右手拿 pin、左手拿纸并插入。但一次错误导致纸在右侧、pin 在左侧，机器人没有见过用左手插 pin 的数据。它却用左夹爪拿纸，再用右夹爪拿 pin，完成了交换后的动作。

这说明模型学到了一种左右手之间的 equivariance，能够把行为从一只手迁移到另一只手，即使 post-training 和 pre-training 数据都没有出现过这种具体组合。这是一个很有意思的 emergent capability。

至于接下来想看什么，我更关心长期可靠性，而不是某个具体任务。我们最近让机器人安全地使用刀具切蔬菜。一旦机器人能安全使用刀具，很多任务都会打开新的可能性。

David Hoffman：软件工程师如何进入 robotics？

Chelsea Finn：机器人行业本身有大量 software engineering，可以直接加入 robotics company 做软件工程。也可以自己动手。Physical Intelligence 有一位同事 Jenny，之前做 algorithmic trading，后来在 Harvey 做法律相关工作。她对机器人很感兴趣，于是买了一台便宜机器人放在卧室里，尝试 fine-tune 开源模型让它完成任务。她把结果分享出来，然后给我发了 cold email，表达想加入实验室。她真正动手尝试过，说明了自己的兴趣和能力，后来加入了 Physical Intelligence。

所以，一个好方法是先买或借一台便宜机器人，尝试开源模型，记录遇到的问题和结果，再把这段经历放到简历或作品集中。现在有很多 open-source tools，可以让软件背景的人开始接触 robotics。

从软件转入 robotics 的另一条路径，是先加入机器人公司的软件、数据或基础设施团队，再逐步接触控制和模型。机器人系统不是只有一个 neural network，实际部署还需要设备通信、传感器处理、任务调度、数据记录、评估、故障恢复和安全约束。软件工程师可以从这些部分开始，之后再把自己的实验经验带到模型工作中。

David Hoffman：所以，最重要的不是先拥有一份完美的机器人履历，而是证明自己愿意在真实设备上动手。买一台便宜机器人，尝试开源模型，展示你遇到什么失败、如何调试以及最后学到了什么，本身就是很有说服力的 signal。

Chelsea Finn：没错。机器人领域还有很多开放问题，实践经验会帮助你理解哪些问题是 bottleneck，哪些只是实现细节。无论最终走 PhD、研究还是工程路线，持续做实验、记录结果并和社区分享，都是进入这个领域的好方法。

David Hoffman：你提到 robotics 的数据不像互联网文本那样容易获得。那在实际训练中，怎样判断一条数据是否值得保留？是不是只有成功轨迹才有价值？

Chelsea Finn：不是。成功轨迹当然重要，因为它告诉模型什么动作能够完成任务，但失败轨迹同样包含大量信息。一次失败可能暴露出抓取位置不对、接触状态变化、动作顺序错误，或者机器人已经进入了一个需要恢复的状态。如果把失败简单丢掉，模型就不会学习怎样识别和修复这些状态。我们更关心的是记录失败发生的上下文，以及后续有没有人工干预、用了什么恢复动作、恢复后是否完成了任务。

这也是为什么真实部署的数据管线很关键。系统需要记录相机画面、关节状态、夹爪状态、目标动作、时间顺序、任务阶段和环境中的变化。还要区分任务失败、传感器异常、通信延迟和人为停止。若把所有结果都压成一个 success 或 fail 标签，训练者会失去判断问题根因所需的细节。高质量数据不只是更长的视频，而是有清楚的任务上下文、可对齐的控制信号和可解释的结果。

David Hoffman：这听起来像 robotics 也需要类似软件工程里的 observability。

Chelsea Finn：完全是这样。机器人运行时必须能回答它刚才看到了什么、决定了什么、执行到哪一步、为什么停下来，以及下一次应该怎样避免同样的错误。只有把这些信息保存下来，研究人员才可以快速定位 bottleneck。否则团队很容易把工程故障误认为模型能力不足，或者把一个偶然成功误认为已经解决了问题。

在现实环境中，任务边界也会不断变化。厨房里的光线、台面摩擦、物体摆放、液体重量和器具形状都可能不同。一个模型在实验室里表现很好，并不代表它能直接面对这些变化。我们会观察它在新对象、新房间和新任务组合上的表现，也会看它能否在中途受阻后继续工作。对真实用户来说，能够恢复、能够说明自己不确定，通常比偶尔完成一个很难的演示更有价值。

David Hoffman：所以通用性并不等于每个任务都做到同样高的成功率。

Chelsea Finn：对。通用机器人需要同时处理几种能力：从视觉和语言中理解目标，把目标分解成可执行的子任务，控制身体完成动作，并在环境改变时重新规划。不同任务对这些能力的要求不一样。倒咖啡需要连续控制和对液体状态的判断，整理厨房需要长时间记忆和多步规划，使用刀具则需要更严格的安全约束。我们不应该只看一个平均分，而要看每个失败边界，以及模型在失败后能否恢复。

这也解释了为什么我们不把单一的 benchmark 当成终点。benchmark 可以帮助比较方法，但机器人真正进入世界后，还要面对运行时间、维护、数据回传、硬件磨损和人员安全。一个策略如果只能在短视频里成功，却无法连续运行几个小时，或者遇到轻微偏差就需要人工接管，就还没有达到可部署的阶段。长期可靠性需要新的评估方式，也需要研究、产品和现场工程一起参与。

David Hoffman：你认为未来的模型会越来越像一个统一的机器人基础模型，还是会由许多专门模块组成？

Chelsea Finn：我预计两者都会存在。一个更通用的模型可以提供感知、语言理解、任务分解和动作先验，让系统不必为每个新任务从零开始。但具体设备仍然需要专门的控制器、校准程序、安全规则和硬件接口。模型负责把抽象目标转换成有用的动作意图，底层系统则要保证动作符合设备限制。把所有东西塞进一个模型里未必是最可靠的工程方案，模块之间的接口和反馈回路同样重要。

我们现在看到的 PIO7 之所以有价值，也不只因为它完成了某个动作，而是因为同一套表示能够在不同任务、物体和 embodiment 之间迁移。新平台仍然需要收集数据和做适配，但起点更高。未来的关键问题是，哪些知识可以在模型中共享，哪些知识必须通过现场数据重新学习，以及如何在不牺牲安全性的情况下让适配速度足够快。

David Hoffman：这会不会改变机器人公司的成本结构？

Chelsea Finn：会，但现在还不能给出一个简单答案。模型能力提高可能减少每个客户从头采集数据的成本，也可能让硬件平台更容易扩展到新的任务。但机器人仍然有制造、维护、部署和售后成本，真实世界的 data collection 也不便宜。成本下降取决于模型是否能跨任务复用、是否能减少人工 teleoperation、是否能更早发现失败，以及硬件是否足够稳定。只看模型参数量或演示效果，无法判断最终的商业效率。

因此，机器人研究的一个重要方向是把能力提升和数据、算力、人工干预的成本一起衡量。如果一个新方法只提高了实验室分数，却需要更多人工接管，或者训练和部署成本增长得更快，它未必是更好的系统。相反，一个稍慢但能够稳定运行、在失败后自动恢复、能减少人工介入的系统，可能更接近真正的产品价值。

感谢大家收听。
