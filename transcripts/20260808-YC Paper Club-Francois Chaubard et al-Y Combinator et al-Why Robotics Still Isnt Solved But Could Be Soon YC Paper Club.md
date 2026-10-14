---
访谈时间: 2026-08-08
访谈时间说明: 未能从公开节目资料独立确认线下活动日期，按 YouTube 发布日期记录。
YouTube发布时间: 2026-08-08T14:00:16Z
嘉宾名字: Francois Chaubard; Marcel Torne; Milan Ganai; Tyler Ga Wei Lum; Niko West; Bill Jiao; Guanming Wang
嘉宾公司名称: Y Combinator; Stanford University、Physical Intelligence; Stanford University、Waymo; Stanford University; Rerun; General Instinct; General Instinct
参与嘉宾:
  - 姓名: Francois Chaubard
    公司或机构: Y Combinator
    职务: 主持人
  - 姓名: Marcel Torne
    公司或机构: Stanford University、Physical Intelligence
    职务: 博士生、前研究实习生
  - 姓名: Milan Ganai
    公司或机构: Stanford University、Waymo
    职务: 博士生、研究人员
  - 姓名: Tyler Ga Wei Lum
    公司或机构: Stanford University
    职务: 博士生
  - 姓名: Niko West
    公司或机构: Rerun
    职务: 联合创始人、CEO
  - 姓名: Bill Jiao
    公司或机构: General Instinct
    职务: 联合创始人
  - 姓名: Guanming Wang
    公司或机构: General Instinct
    职务: 联合创始人
播客名称: YC Paper Club
播客url地址: https://www.youtube.com/watch?v=myDCd0hNqQU
youtube_video_id: myDCd0hNqQU
字幕来源: Y Combinator Root Access 官方页面公开完整 transcript，结合 YouTube 公开自动字幕 json3（en-orig）核对并转写为简体中文
全文提及的关键名词:
  - robotics
  - teleoperation
  - sim-to-real gap
  - embodiment drift
  - sensory motor
  - vision-language-action model
  - VLA
  - Multi-Scale Embodied Memory
  - Physical Intelligence
  - high-level policy
  - low-level policy
  - temporal attention
  - in-context adaptation
  - embodied reasoning
  - chain of thought
  - variational inference
  - R&B Encore
  - action forcing
  - SimToolReal
  - goal-conditioned policy
  - reinforcement learning
  - FoundationPose
  - SAM
  - domain randomization
  - Play2Perfect
  - Rerun
  - robotics application company
  - neo integrator
  - world action model
  - WAM
  - inverse dynamics model
  - diffusion transformer
  - flow matching
  - classifier-free guidance
  - ImageRAM
  - FAST-WAM
  - JEPA
  - General Instinct
  - DreamZero
  - Jetson Thor
---

# Why Robotics Still Isn't Solved - But Could Be Soon | YC Paper Club

## Transcript

### 十年过去，为什么每年都说“明年机器人就解决了”

**Francois Chaubard：** 欢迎来到 YC Paper Club。今天其实可以叫 YC Robotics Club。回看我的职业生涯，这已经是我遇到“明年机器人就会被解决”的第十年。

十年前 AlphaGo 出现时，大家说算法显然已经有了，接下来只要扩大规模。随后 MuJoCo 出现，我们可以在大约三千次迭代中训练机器人学会行走，于是又说，明年机器人一定会解决。后来 UMI 数据采集和 ALOHA 成了突破，人们看到机器人可以浇花、修自行车、操作咖啡机，甚至给人刮脸，再一次觉得算法已经找到，剩下只是规模化。到了 2026 年，diffusion policy、multi-step reasoning 和 VLA 都在进步，许多人向我保证今年就是“机器人之年”。

现在 2026 年已经过半。消费者确实可以预订 1X 的 NEO，但还买不到 Physical Intelligence 或 Figure 那类通用机器人。机器人在固定 work cell 里取得了一些成功，能料理家务的 Rosie 仍未出现。我们还剩六个月，也许我的判断会错，但至少可以确定，这一年是机器人 demo 之年，而不是大规模可靠部署之年。

最直接的约束是 teleoperation 数据极难采。只靠一个小型夹爪、腕部相机和有限反馈完成演示，非常别扭，也非常不稳定。如果行业的训练路线依赖这类数据，又需要把它扩大几个数量级，我们就不能只喊“更多数据”。我把当前障碍归纳成四堵墙。

第一堵墙是现实世界的物理建模。视频模型在模拟环境中可以生成看似合理的未来，却不一定服从真实物理。你让模拟汽车驶向 Whole Foods，场景可能魔法般变回公路，车辆根本不会真正撞上建筑。Dreamer、world model 等方法在游戏中很有价值，但从视觉连续性跨到可信物理仍有巨大 sim-to-real gap。加入可变形物体后更难；再把动作作为条件，要求模型学习从状态 `S_t` 和动作到 `S_{t+1}` 的转移，所需数据量会进一步上升。

只预测“下一帧看起来像什么”与预测“采取某个动作后下一状态会怎样”是两件不同的事。后者必须覆盖动作空间中大量很少发生的组合，还要尊重碰撞、摩擦、材料形变和接触力。一个视觉上自然的视频可以在物理上完全错误；机器人若依据这种错误未来行动，代价不是画面瑕疵，而是撞坏设备或伤到人。

第二堵墙是 action space 的表示。高维机器人动作很难获得既紧凑、又支持快速学习的表示。过去我们会用 feature pyramid 等办法压缩巨大状态或 Q matrix，但对真实机器人来说，如何表示动作、接触和多关节协调，仍不是一个已经解决的问题。

第三堵墙，也是我认为最被低估的一堵，是 sensory-motor 问题。人的皮肤和神经末梢能感知法向力、切向力、湿度、温度、振动和摩擦系数，而且覆盖全身。最好的机器人往往只在指尖放一个很小的 force-torque sensor，再配一个腕部相机。人把手伸进背包，不看也能摸出充电线；机器人没有类似 epidermis，做不到这种通过触觉建立 world model 的能力。人在严寒中手指麻木时，连解开冰球鞋带都会明显困难，这个例子恰好说明丰富触觉对 manipulation policy 有多重要。

第四堵墙是长期部署者才会充分体会的 embodiment drift。同一个控制指令对应的实际力和位移会随时间改变。执行器会进灰、腐蚀、生锈，电池输出会衰减，车辆油门与加速度之间的关系也会漂移。原来用 teleoperation 采集的示范因此逐渐过时，VLA 从观测到动作的映射不再匹配当前硬件。若每次漂移都要重新采数据、重训整个模型，商业部署就很难持续。

今晚的报告分别尝试绕过这些问题。Marcel 是 Chelsea Finn 实验室的博士生，会介绍他在 Physical Intelligence 实习时做的多尺度具身记忆；Milan Ganai 跟随 Marco Pavone 和 Clark Barrett 读博，也在 Waymo 工作，会讨论机器人如何自举出与动作相关的推理；Tyler 跟随 Jeannette Bohg 和 Karen Liu 读博，会介绍 SimToolReal；Rerun 联合创始人 Niko 会谈真实部署的数据与运营；General Instinct 的 Bill 和 Guanming 则会解释 world action model 以及怎样让它实时运行。

### Marcel Torne：让 VLA 记住自己做过什么

**Marcel Torne：** 我在 Stanford 读博，今天介绍的是我在 Physical Intelligence 实习期间参与的 Multi-Scale Embodied Memory。先看我们训练过的一组“机器人奥运会”任务：机器人可以全自主开锁、把里外翻转的衣服折好、制作 peanut butter sandwich。它们的 dexterity 已经很强，但最长任务大约只有两分钟。

真正有用的家用或工业机器人需要完成长得多的任务，例如制造一个完整物件、整理整间卧室，或者做完一顿饭后清洁厨房。这类任务要求机器人持续跟踪进度和时间，保持可靠的精细操作，还要在遇到新情况或自己犯错后现场调整。我认为，这些能力都离不开 memory。

问题是，现有很多 VLA，包括 π0、π0.5 和 GR00T 一类 policy，本质上接近 memoryless。机器人每个时间步接收一组新观测，却不知道此前发生过什么。结果很直观：洗盘子的机器人不知道已经洗了多久，会无限重复；做 grilled cheese 的机器人不知道食物在锅里放了多久，最后把它烧焦。

大家没有简单地给 policy 加上很长的历史，是因为有两类成本。第一是 effectiveness。加入过去观测会造成 distribution shift，而可用训练数据又不足，policy 有时反而变差。第二是 efficiency。视觉上下文越长，训练与 inference 的计算量、显存和延迟越高，真实控制回路难以承受。

我们的答案是 compression，并把控制系统拆成两个尺度。high-level policy 负责判断下一步该做什么，low-level VLA 负责产生真正的机器人动作。记忆也拆成两种：短期记忆保留一小段密集视觉帧，服务于精细 manipulation；长期记忆把过去几分钟压缩成 language representation，交给 high-level policy 跟踪任务状态。

短期视觉记忆使用基于 Vision Transformer 的新 encoder。它不只编码当前帧，还加入 temporal attention，让当前图像 token 吸收之前帧的信息；随后丢弃旧帧 token，只保留已经汇聚历史的当前表示。这样既能从已有 ViT 权重初始化，因为新增部分主要是 temporal attention，又能大幅减少 token 数量，保持较快 inference。

这类短期 memory 让机器人完成需要连续感知的任务。制作 grilled cheese 时，它既执行拿取、翻面等精细动作，也能等待正确时长，不会把食物烧焦。卸 grocery bag 时，有些物品只有腕部相机探进袋中才能看到，机器人必须记住袋里有哪些物品、还剩几个。擦窗时，它要记住哪些区域已经处理，避免永远停留在同一片位置。

长期记忆采用 recurrent textual scratchpad。high-level policy 每一步都会更新一段文字，记录已经发生的事情；更新后的 memory 再作为下一次预测的输入。与保存几分钟视频相比，文字 token 少得多，训练和推理都更便宜。policy 还能在事实变化后修改记忆，因此它不是一次写死的计划。相较把全部历史图像直接塞进 context，这种表示也较不容易受视觉分布变化影响。

我们用它完成了持续十几分钟的备餐任务。机器人会准备某个 recipe 所需的所有物品，绿色框里可以直接看到它不断更新的 memory string。与 no-memory 和其他记忆基线比较，这套方法取得更好的任务完成率。

这里的两级结构还有一个实际意义。low-level policy 不需要理解整顿饭的全部历史，只需稳定执行“打开冰箱”“拿起某件物品”这类短动作；high-level policy 也不必以高频率输出每个关节位置，只需维持任务进度、物品状态和异常记录。把不同时间尺度混进同一个巨大 context，不仅更贵，也更难知道失败究竟来自规划还是控制。分层后，研究者可以分别检查高层 memory string 与低层 visual token。

短期 memory 与长期 memory 解决的也不是同一个问题。腕部相机刚才看见袋底的物品，属于几秒尺度的 dense visual evidence；某块奶酪已在锅中等待几分钟、某个柜门从左侧打不开，属于需要压缩并长期保留的事件。前者若只转成文字会丢失抓取细节，后者若保存全部视频则极其浪费。因此 multi-scale 不是简单增加两个 context window，而是按任务所需的时间分辨率分配表示。

我尤其看好 memory 带来的 in-context adaptation。没有记忆的 policy 若第一次没能打开冰箱，或第一次抓 chopsticks 失败，会一次又一次重复同一动作。加入记忆后，机器人能记录失败并改变策略。它抓筷子失败后会把手放得更低再抓；从一侧打不开冰箱后，会换到另一侧。这种在不重训的情况下根据刚发生的错误调整，是当前 VLA 很欠缺的能力。

**观众：** 长期记忆完全用文字表示时，你们怎么知道应该把哪些信息写进去？

**Marcel：** 目前 high-level policy 用 SFT 训练，我们为数据做了人工标注。也就是说，团队必须事先判断哪些信息重要，再告诉 annotator 要持续记录什么。这是 proof of concept 的限制。下一步很自然的方向，是直接在 memory space 上做 reinforcement learning，让 reward 帮助模型学习什么该记、什么该忘，而不是永远由研究者手写规则。

**观众：** inference 时文字记忆实际存在哪里，又怎样影响动作？

**Marcel：** 记忆文本很短，可以放在 RAM 里。每次 high-level policy 运行时把它当普通 text token 输入 VLA，由高层输出下一段动作描述，再让 low-level policy 执行。

**观众：** 把任务写成高层文字后，怎样保证它能泛化到不同环境？例如 omelet 有很多做法。任务更复杂时，需要增加多少训练 episode？

**Marcel：** 我们给高层的是很具体的任务描述。准备 recipe 时，会说明物品在哪里、具体需要哪些东西，例如做 pizza 的材料。high-level policy 本身是用互联网数据训练的 VLM，因此只需较少机器人数据也能对语义任务泛化。low-level VLA 与任务规划分离，它只接收很短的“下一步做什么”描述。在厨房里学会基本 manipulation 后，任务变复杂并不等于每个长任务都要重新收集同等规模的机器人轨迹。

**观众：** grilled cheese 的例子似乎只加一个 timer 也能解决。只用文字会不会限制记忆表示空间？

**Marcel：** 人类记忆显然不全是文字。理想状态可能是一个 latent embedding，直接保留所有重要历史。但当前很难监督和调试这种 latent memory。文字给模型加入了强 inductive bias，也让研究者能读、能检查、能修正，所以是眼下最实际的起点。我也很希望后续探索 latent 或混合表示。

### Milan Ganai：推理不是越多越好，必须对动作有预测力

**Milan Ganai：** 我在 Stanford 读博，曾在 AWS 和 Waymo 做研究。我要谈的是怎样让机器人教自己推理。VLA 通常从一个 internet-scale 的 VLM 开始，例如 Gemini 或 Qwen，再用相对稀缺的机器人数据继续训练。manipulation 数据可能来自 teleoperation，自动驾驶数据可能来自人开车时记录的轨迹。最后模型接收图像、感知特征和 language instruction，输出 steering、end-effector position 等动作。

近来的趋势是把 embodied reasoning 加进 action prediction，类似 LLM 的 chain of thought。机器人数据很少，所以任何能补充 supervision 的 annotation 都很有价值。文字 reasoning 还有一个好处：人可以读懂机器人为什么作出某个决定。

但“什么是好的具身推理”不是一个已知答案。第一是 grounding problem。互联网上没有一套 oracle reasoning trace，告诉机器人面对每种 embodiment 应该怎样思考；我们也不能打开人的大脑，读取从图像到手指动作之间的内部过程。于是模型和训练数据形成 chicken-and-egg problem。

第二是 verbosity。推理可以是规划，例如“走向 pepper、拿起 pepper”；也可以是 perception trace，例如列出画面所有物体和 bounding box；还可以持续报告 gripper position 或车辆在道路上的位置。但机器人对 latency 很敏感。每一步都重新规划可能是冗余，枚举所有物体可能被无关目标干扰，持续描述夹爪位置也未必能提高下一步动作准确率。因此真正的问题不是“要不要推理”，而是特定 form factor 和 embodiment 在什么时刻应该推理什么。

我们的工作叫 Self-Supervised Bootstrapping of Action-Predictive Embodied Reasoning，方法名是 R&B Encore，即 refined and bootstrapped embodiment-specific chain-of-thought reasoning。它是一个让 embodied-reasoning VLA 自我改进的 pre-training cycle。我们把不可观测的 reasoning 看作连接已知 context 与 action 的 latent variable，再借用 variational inference 的框架进行筛选。

系统有两个主要部分。reasoning proposer 像 annotator model，面对一段 demonstration 提出多种候选 reasoning：是列出 visible objects 和 movement，还是写 plan 与 gripper position，或写 visible objects 与 subtask。reasoning validator 再依据三个维度评分。

第一是 concision，避免 reasoning 太长。第二是 non-triviality，鼓励能泛化、不是机械复述的内容。第三，也是最重要的一项，是 action predictiveness：这段 reasoning 是否真与该 embodiment 随后采取的动作对齐。对候选打分和 resample 后，会得到一套合成但 action-aligned、embodiment-aligned 的 reasoning 数据。研究者既能分析哪种推理有效，也能用它重训 VLA，提高 policy 的稳健性。

我们在多个 embodiment 上验证。对 manipulation，描述 movement 加 gripper position 的推理较有效；把整个场景的所有 perceptual object 都列出来反而较差，因为大量无关物体会分散注意力。过滤无关 perceptual trace 后，success rate 和 task saliency 都提高。

在真实硬件 manipulation 中，经过该循环训练的 VLA 对 novel target object 和 cluttered scene 的 out-of-distribution 表现更好。对 legged locomotion 和 navigation，structural affordance 与 movement 比 terrain 描述和 counterfactual 更重要。对 self-driving，我们用同一方法清洗 human annotation。meta action、visible object 和与当前感知相关的推理有用，虚构经历或无关推理应删除；清洗后 L2 path error 和 collision rate 等指标改善。

这些结果还说明，reasoning quality 不能只由语言流畅度判断。一个 trace 可以准确描述路边所有物体，却因为没有突出影响行车轨迹的对象而降低 policy 表现；另一段很短的 trace 只指出前方车辆减速，却可能更 action-predictive。validator 因此不是挑“最像人类解释”的文本，而是判断它是否在给定 context 下帮助预测真实 action。

在 manipulation 场景里，visible-object list 之所以常被筛掉，不是 perception 永远无用，而是画面里有太多 distractor。真正应保留的是与 target、grasp 和 movement 直接相关的信息。legged locomotion 中，地形名称本身未必足够，台阶、缝隙或表面能否支撑下一步的 structural affordance 更接近动作决策。不同 embodiment 最有价值的 reasoning vocabulary 因此会不同。

这里有三个结论。第一，selective reasoning 比 exhaustive reasoning 更重要。一段推理即使事实正确，也可能对当前动作无用。第二，self-supervised bootstrapping 能缓解 reasoning 数据与 reasoning model 相互依赖的问题。第三，这个方法能跨 manipulation、navigation、driving，以及从 1B 到 30B 参数的 VLA 工作。具身推理不是一套对所有机器人统一套用的模板，而是一种需要被发现、部署并谨慎预算的计算资源。

**Francois：** 狗也能完成大量具身推理，却显然不是在 text token 里思考。你怎样看不依赖 token 的推理？

**Milan：** 模型可以在连续 latent space 中进行 non-textual reasoning，不受文字格式限制，但这需要合适的 architecture 和 theory。我们当前选择文字，是为了利用 LLM 和 VLM 已从海量互联网数据中获得的 prior，把它迁移到 robotics 这种 data-scarce regime。文字不是唯一终点，而是目前最容易借力的表示。

**观众：** 自动驾驶本来就有 streaming latency。给 autonomous vehicle 加 reasoning，目的只是产生更好的 self-supervised data，还是 inference 也必须运行这些推理？

**Milan：** reasoning 的核心价值是把 prior 注入模型，像 co-training data 一样辅助学习，并不要求部署时每一步都生成文字。我们有一个 action forcing 方法，训练时使用 reasoning annotation，inference 时可以丢掉 reasoning 输出，直接产生动作。这样保留训练收益，同时避免实时延迟。

**观众：** reasoning 完成后状态可能已经移动，旧推理会不会因 state-space drift 伤害后续动作？

**Milan：** 我们假设 reasoning 基于当前图像和当前 instruction 实时产生，不是长期固定不变的 plan，因此不会天然引入那种持续漂移。当然，系统仍必须以最新观测刷新它。

**观众：** 你说 counterfactual 不太有用，是否意味着应该彻底删除这类推理？

**Milan：** 不是。这个结论针对我们测试的 benchmark，也取决于当前场景。自动驾驶的大量时间只是沿直路前进，周围没有新事件，这时每一步生成 counterfactual 没有价值。plan reasoning 也可能有用，但没必要每个时间步重复。我们的主张是按需要分配，而不是永久禁止某一类 reasoning。

### Tyler Ga Wei Lum：用随机物体和随机目标学会零样本工具操作

**Tyler Ga Wei Lum：** 我要介绍 SimToolReal。演示里的每段视频都是 1 倍速，而且全部由同一个 frozen policy 控制。这个 policy 训练时没有见过展示中的工具和任务。换一把 brush、一把 hammer，或者换一种目标动作，都不需要重训。转动 screwdriver 等动作有很高 dexterity，普通 parallel-jaw gripper 很难完成，必须用 multi-fingered hand。

policy 以 60 Hz 运行，同时控制 22 degree-of-freedom 的手和 7 degree-of-freedom 的机械臂。这种精细度本身很难由人通过 teleoperation 稳定演示。多指手与人手之间存在 embodiment mismatch，操作者又缺少 force feedback，即便只是 in-hand rotation，也只能缓慢而谨慎地控制。因此我们不从 teleoperation imitation 开始，而是完全在 simulation 中用 sim-to-real reinforcement learning 训练。

GPU-accelerated simulation 可以并行运行数万台机器人，以大约现实时间一千倍的速度生成 experience。几天里就能积累相当于数十年的 interaction data。policy 不是复刻有限的人类示范，而是直接优化 reward-maximizing behavior，所以能探索出很难 teleoperate 的灵巧动作。Dextreme 早期展示过这种方法的能力，不过既往工作通常为每个 skill 训练一套 policy：抓取一套、reorientation 一套、object spinning 一套、tool use 又一套。每个新行为都要重新设计 reward、做 task-specific engineering 并训练。

我们问的是，能否只训练一次，让同一个 policy 完成整段任务。以刷子为例，机器人先抓住刷子，在手内调整到功能性姿态，再用它扫动物体；中间不人工切换 policy。

关键抽象是把 dexterous tool manipulation 统一为 goal reaching。policy 不需要知道任务标签叫 sweeping 还是 hammering，只需要把物体从 current pose 移到 desired pose。因此训练的是 goal-conditioned policy：给它一连串目标姿态，它就控制手和臂把任意物体逐步移动过去。

训练时，我们在 simulation 中程序化生成 cylinder、cuboid 等 primitive object，随机采样目标姿态，再用 massively parallel RL 学习操作随机物体抵达随机目标。当然，真正系统还包含 system identification、domain randomization、RL exploration 等大量细节，演讲没有逐项展开。

inference 时，目标姿态序列可以来自任何来源。本工作选择 human video demonstration。FoundationPose 与 SAM 从人类视频中提取工具应当经过的 pose sequence，RL policy 再以 60 Hz 逐个追踪。人类视频没有提供 robot action，也没有参与训练或 fine-tuning；它只像 task prompt 一样，在执行时告诉 frozen policy 物体该沿什么轨迹运动。

具体输入包括 proprioception、current object pose、物体可抓取区域的 bounding box，以及 current goal pose。LSTM policy 输出整只手和机械臂的 joint position target。于是一个新任务不再等于一次新训练，而只是换一串 goal pose，几分钟内就可以尝试新物体和新行为。

我们用同一个 frozen policy 测试 12 种训练中没见过的工具和目标行为，每个 tool family 都取得实质进展。长柄工具表现尤其好；较重工具更容易掉落，较小物体则常被手遮挡，导致 pose tracker 失败，表现较弱。

这项设计刻意把“生成目标”与“追踪目标”分开。SimToolReal 解决的是后一项：只要外部系统给出合理 trajectory，它就尽量用真实手臂完成。它并没有宣称从一句自然语言自动规划出所有 pose，也没有把 human demonstration 当成 imitation-learning label。这样的边界很重要，因为演示里看似完整的任务，实际由 perception、goal generation 和 low-level control 三部分共同完成，当前论文只重点验证最后一部分的泛化。

为了检验训练目标是否真的支持下游泛化，我们在训练不同 checkpoint 上做 train-test correlation。训练侧只使用 primitive object 和 random goal，测试侧使用没见过的真实工具以及从人类演示提取的 trajectory。随着 generic goal-reaching objective 的训练表现提高，unseen tool 上的 real-world performance 也明显上升。这说明随机物体、随机目标不是与真实任务无关的玩具目标，而能学习到可迁移的 inverse-dynamics-like prior。

与两类常见 baseline 比较也能看出差异。fixed-grasp baseline 能拿起工具，却只能靠机械臂整体旋转，经常让工具撞到桌面。它说明“找到并保持一个 grasp”对很多工具使用任务并不够，手内 reorientation 很关键。kinematic retargeting 则把人类 fingertip motion 映射给机器人，但不推理 contact force，往往连稳定抓取都做不到。

失败分析中，pose tracking 是最大来源；之后是抓住后掉落，再后是初次抓取失败。不过 policy 的 recovery 很强。hammer 被撞出手后，它会立即重新抓起并继续任务。团队开源了 code、simulation asset 和 policy weight，还提供可直接在浏览器或手机运行的 interactive demo。demo 在本地设备推理，不是远程服务器，所以会明显消耗手机电量。

这种失败排序也改变后续工程优先级。若大约六成失败来自外部 pose tracker，继续扩大 RL policy 不一定是最有效投入。小物体被手遮挡时，再好的 controller 也会收到错误 state。更合理的改进可能是多相机、腕部视角、更稳健的 object tracking，或把已有 pose-based policy distill 成直接使用 image observation 的 policy。论文的 dexterity 很强，但系统 success rate 仍受 perception stack 的最弱环节约束。

我再介绍后续工作 Play2Perfect。很多 assembly task 需要持续接触和毫米级精度，从零学习非常困难。我们的思路是，先解决容易的自由空间“玩物体”，再解决困难的精密装配。第一阶段通过 task-agnostic play 预训练共享 dexterous prior，方式与 SimToolReal 的通用训练接近；第二阶段在 sparse-reward、contact-rich assembly task 上 fine-tune；最后 zero-shot 部署到真实世界。它可以完成 tight insertion 和 multi-part assembly。SimToolReal 提供广泛、快速、对新工具反应式的 dexterity，Play2Perfect 再把这种 prior 延伸到精密接触任务。

预训练的意义是先让 policy 学会稳定抓持、调整姿态和恢复，而不是在几乎没有 reward 的装配环境里从随机动作开始。fine-tuning 随后只需学习插入、对齐和持续接触等 task-specific 部分。这个顺序与 language model 的 pre-training、fine-tuning 类似，但 prior 来自大规模物理 interaction，而不是文本。

**观众：** 演示里的 recovery 非常强。你们专门训练过恢复吗？

**Tyler：** 没有单独写一个 recovery objective，但 domain randomization 中会随机对物体施力。物体有时会被撞出手，policy 在 simulation 中便获得重新捡起的经验。如果不加入 random force，训练中从不掉东西，部署时的 recovery 很可能差得多。

**观众：** 训练用的 primitive 与真实 brush、spatula 有多相似？

**Tyler：** 很多工具都有一段可抓取区域，可以近似成 bounding box。policy 不接收完整 mesh，只知道可抓取区域的大致边界。simulation 只用 cylinder 和 cuboid，是因为简单几何能快两到三倍，也避免维护复杂 asset。spatula 或长柄工具能较好近似；bowl、scissors 等形状可能被它以奇怪方式抓起，却未必是任务需要的 grasp。

**观众：** 这套方法怎样扩展到 articulated object 或更一般的真实物体？即使可以模拟全世界，pose-goal 范式本身是否足够？

**Tyler：** simulation 有明确边界。water、zipper、开易拉罐等交互很难忠实模拟，更现实的路径可能是把 simulation 学到的 prior 带到现实世界，再用真实 experience fine-tune。更抽象地说，我们的 policy 类似 pose space 里的 inverse dynamics model。如果物体不能用一个 pose 表示，例如 towel，可以改用 keypoint；再一般化，可以把 current video state 和 goal video state 交给模型，让它产生抵达目标的动作。难点会转移到 inference 时怎样生成正确 goal。

**观众：** 交互 demo 里，机械臂连续寻找目标时有时会越扭越多，最后因自身缠绕失败。能否在动作之间加入 reset dynamics，选择反方向绕回去？

**Tyler：** 理论上，足够好的 RL 应该学会在关节接近极限时绕回，但我们没有一个确定答案。真实应用也不常要求机械臂持续极端扭转，不过这确实暴露了当前训练分布和长期 constraint handling 的缺口。

**观众：** 单一 policy 上迭代时，怎样发现它在其他任务回退？有系统 eval 吗？

**Tyler：** real-world eval 很贵，也很慢。若不做上百次 trial，很难区分 90% 与 87% success rate，少量测试更像 vibe check。我们尽量在 simulation 中放入真实测试物体和 trajectory，自动检查新 checkpoint 是否普遍改善。但 simulation 也可能奖励现实中不可行的“魔法般抛接”，而 pose tracker 会在真实环境失败，所以最终仍需要 human insight。通用机器人 eval 远未解决。

**Francois：** 你用了一个“史前”的 LSTM。为什么不是 transformer？

**Tyler：** RL 代码非常敏感。已有稳定 codebase 原本就支持 LSTM，我们先试它，结果工作得很好。transformer 在无限数据下可能更像强大的 data sponge，但这里不是离线吸收一个无限数据集，而是 policy 持续更新。已有一些比较没有显示 transformer 必然更好，所以当时没有足够理由重写系统。现在 coding agent 降低了实验成本，当然可以再试。

**Francois：** diffusion policy 论文的表格也常被忽略，其中 convolutional model 在约一半任务上胜过 transformer。transformer 往往更敏感，调参质量会显著影响结论。

**Francois：** random goal 在代码里到底怎样生成？

**Tyler：** 就是很直接地采样 position 与 rotation 作为第一个目标，之后每个目标相对前一个目标采样 delta pose，距离最多约 10 厘米，旋转差最多约 90 度。它很适合训练从 A 到 B 的控制，却不负责生成任务目标。当前目标来自人类视频；未来可以让 high-level planner 观察完整场景后产生 pose sequence。

**观众：** 有多少失败来自错误 pose estimation？只用 third-person view，还是也试过 first-person view？

**Tyler：** 大约 60% 失败来自 pose tracking，是系统最大瓶颈，尤其是容易被手遮住的小物体。长柄、特征丰富的刷子更容易追踪。实验主要使用一个选好角度的 third-person camera，没有系统比较 first-person。未来可以使用腕部相机，或把 pose-based policy distill 成 image-based policy，但 goal conditioning 的实现仍需解决。

### Niko West：先用 teleoperation 解决一个付费问题，再让 autonomy 成为扩张杠杆

**Niko West：** 我是 Rerun 联合创始人兼 CEO。创办公司之前，我做了大约十年用于现实产品的 machine learning 与 computer vision。Rerun 在构建 physical AI 的 unified data layer，覆盖从 data collection 到 training 的工具与基础设施。

开源 Rerun SDK 用于 logging、visualization、query、data loading 和 transformation。Rerun Hub 则是面向大量云端 physical data 的 data catalog 与 storage backend。因为我们同时服务 frontier lab 和只有两个人的 YC startup，所以能看到很多机器人公司的实际工作方式。

我最看好的一种模式是 robotics application company，也有人叫它 neo integrator。这类公司不先造一个解决所有事情的 foundation robot，而是端到端接管一个完整 business problem。现在 data center management、construction、warehouse 和 manufacturing 里已出现这种模式。

它们要非常擅长 deployment、support 和 operations，尽可能少做 custom hardware；通常从 teleoperation 开始，先证明仅靠人远程控制也能让业务成立，再 fine-tune 现有 model。我的判断是，这会像上一代 SaaS 一样，把大量现实世界工作变成可持续服务。物理世界的摩擦不会突然消失，恰好给应用公司留下长期经营空间。

如果我不做 Rerun，而要创建这种公司，我会按一个简单次序开始。第一，找一个客户真愿意付钱的单一问题。第二，用 off-the-shelf hardware 和 teleoperation 尽快部署。第三，建立最基本的学习、评测和数据循环，然后持续迭代与扩张。

假设我要自动化 paper plane factory。我们不会先在实验室训练多年，而是先卖出服务、部署设备，再观察现实经营。physical world 很残酷，任何部件都会坏，实验室里不可能预想到所有 failure mode。只有进入客户环境，才知道端到端 business requirement 是什么。若任务能由 teleoperator 完成，通常就有机会逐步训练 model 自动化其中大部分；反过来，一个实验室模型能做 demo，不代表它能满足客户业务。

部署后可能学到很多原先不知道的事实。也许工厂每天必须产出一千架合格纸飞机才有经济性；也许折坏并不可怕，只要能便宜地自动识别和剔除，因为 paper 很便宜。客户最在意的也许不是单架速度，而是新 plane design 的 onboarding time。一个小小的 paper tray 可能让取纸失败减少 50%。teleoperator 可能要训练 20 小时才能达到客户要求，这会改变招聘和排班。客户还可能愿意为能捡纸、装箱的 V2 支付十倍价值。便宜 research arm 也一定会在持续使用后损坏，迫使公司更换 supplier。

下一步不是马上训练自己的 foundation model，而是做 physical AI 的 hello world：选一个开放的 π model 或类似模型，用几小时 teleoperation demonstration fine-tune，让它至少完成最简单 case。必须尽早做，因为训练结果会反过来改变数据采集和运营。先收完所有数据、最后才训练，是常见且代价很高的错误。

之后要建立 repeatable evaluation。首先，在办公室复制客户环境。真正已经交付产品的机器人公司，几乎都会有客户场景 replica，因为团队需要大量测试。其次，把业务真正重视的质量编码进评测。纸飞机可能要求边缘锋利、左右对称、形状符合 design、weight distribution 正确。generic model company 不会替你定义这些指标，这正是 application company 的知识和 stickiness。

一开始应手工评估，直到团队真正理解 failure，再考虑自动化、外包或训练 evaluator。每个 rollout 的 metadata、failure classification 和环境信息都要持续记录。评测不是最后打一个 success rate，而是整个 learning loop 的 backbone。

所谓 good data，不是画面漂亮，而是能让 model 变好的数据。团队必须不断 training、evaluation、debugging，再修改 collector instruction。大型 robotics lab 的研究者在排查 policy 时，经常发现最有效的修复不是更换 architecture，而是要求 data collector 改变动作方式、停止重复某种错误，或增加某类 variability。真实部署需要持续检查 bug、覆盖范围和 annotation，而不是预先收一个巨大但僵化的数据集。

如果客户要求很快支持新 design，公司可能要把任务拆成 composable subtask，设计 task taxonomy 和可重复 annotation。简单场景可让 operator 一边说话，或踩 foot pedal 标注；复杂场景需要离线 annotation workflow，这会直接改变运营组织。

传统 Postgres、LLM data infra 或 feature store 不一定适合机器人。physical data 是 multimodal、multi-rate、episodic 的，还包含 3D semantics 与深层嵌套结构。把它硬塞进 table database，query 很困难，存储和处理也低效。若底层 data layer 选错，团队会在上面堆大量 workaround，拖慢每一次 debug。

具备基本循环后，公司就可以 hill climb：真实服务产生有价值的数据；repeatable eval 告诉团队是否改善；训练与采集快速迭代；full-stack debugging 帮助定位问题来自 sensor、hardware、operation、data 还是 model。真实机器人是“千刀万剐式”的工程，失败不会只来自一个算法瓶颈。

后续扩张当然包括更大数据、更多 compute、更新算法，以及 tactile、depth、sound 等 sensor。但同样重要的是 sales、assembly、shipping、unboxing、field support 和 operator management。纯 model company 通常不会深入这些环节，它们反而能成为 application company 的 moat。我们见到一些资本投入不大的团队已经产生可观收入并快速增长，它们共同点不是拥有最大模型，而是 turnaround 极快、系统尽量简单、所有 moving part 都可观测。

frontier lab 与 application company 的算力使用方式也不同。前者会给每位 researcher 配置大量 GPU 做 model experiment，也会投入很多 CPU 来缩短搜索、数据探索和处理的 latency。应用创业公司更看重灵活、简单、moving part 少的系统，因为新数据必须很快进入训练，现场问题必须能沿 sensor、operator、network、hardware 和 policy 全栈追踪。对它们来说，能在一天内定位一次客户失败，通常比把通用 benchmark 提高一个小数点更有价值。

teleoperation 也不是最终产品，它先承担三项作用：验证客户是否真的愿意付钱，建立遇到异常时的人类兜底，并持续产生与真实业务一致的 demonstration。随着模型能力提高，人工介入率下降，gross margin 和可扩张性才逐步改善。若从第一天就要求 100% autonomy，公司可能在还没理解客户问题前烧完资本。

所以我的主张是：至少应该有人去创办 robotics application company。市场很大，base model 会持续改善，物理世界又有足够摩擦支撑真正商业模式。创业者不一定需要十亿美元 seed round，却仍需要很强的 AI、engineering 与 operations。

**Francois：** 哪些领域已经看到较早成功？

**Niko：** 能 teleoperate 的任务最容易起步。data center 是明显类别，warehouse 里还有大量重复搬运；劳动力可能不贵，却短缺且难管理。能交付可靠机器人的公司常常 100% 受 supply constraint，而不是缺 demand。小规模 tabletop manufacturing 和 food 也有不少活动。

**观众：** 如果这种模式这么好，为什么还没有很多机器人应用公司做到数十亿美元收入？

**Niko：** 低成本试一个应用所需的基础条件最近才成熟。现在市场上有更多可买到的 arm，base model 比两年前好得多。过去每家公司都必须自己补齐硬件和模型基础，只能先融资巨额资本、追求更通用的目标。如今可以更便宜地从单点问题出发。

**观众：** 在模型达到可部署水平前，怎样估算一个任务需要多少数据？怎样决定继续做还是换问题？

**Niko：** 这正是“teleop first”的价值。很多业务并不要求完全 autonomy，robotaxi 也未必需要每个环节全自动。公司可以把 autonomy 当作 scaling factor：先靠 teleoperation 运行并产生收入，再训练模型、画自己的 scaling curve。没人能在真空中准确猜出数据量，而且你原以为必须解决的动作，到了客户现场可能根本不是最重要的问题。先运营，就不用凭空下注。

**Niko：** 更具体地说，先由人远程完成任务，团队就能知道一小时服务值多少钱、哪类失败客户可以接受、人在什么环节必须介入，以及介入一次需要多长时间。模型上线后，不必立刻取代全部人工，只要持续减少最昂贵、最频繁的介入，就已经改善单位经济性。每轮训练后再用固定客户场景复测，才能画出真正属于这个任务的数据规模曲线。若曲线很早就停滞，团队可以检查问题究竟来自观测、硬件、标注还是任务定义；若还没有客户和真实场景，所谓需要多少数据只是猜测。

**Niko：** 这也是为什么我反复强调先手工理解评测。自动评分器若建立在错误目标上，只会更快地优化错误事情。纸飞机工厂也许不在意偶尔折坏一张纸，却极其在意新设计要多久才能上线；若团队只优化单次成功率，就会错过真正决定收入的变量。把客户要求转成可重复测试，再让每次现场失败回流到训练集，才是应用公司的核心循环。

### Bill Jiao 与 Guanming Wang：world action model 为什么强，又为什么太慢

**Bill Jiao：** 我和 Guanming 来自 General Instinct。我早期做 VLM，也在 Siemens 做过预测 time series 的 foundation model；Guanming 主要做 robotics reinforcement learning。我们的公司为 physical AI model 提供高性能 inference infrastructure。LLM 有 vLLM 和 SGLang，world action model 与 VLA 则可以使用 General Instinct。

Jim Fan 的演讲里有一个“VLA 已死，未来属于 world action model”的 meme。VLA 通常是在 VLM 上接 action head，由当前视觉观测直接预测动作。world action model，简称 WAM，则用 diffusion transformer 同时预测未来画面与 future kinematics。机器人相机给出当前 video observation，模型先“想象”未来 frame，再以它为条件产生动作。

Nvidia DreamZero 是一个例子。模型用 flow matching 预测 future frame，也预测 future action chunk，在多项 benchmark 上超过 π 系列和 Nvidia 其他模型。显式学习未来 dynamics，确实可能提升 action generation。

问题是 video diffusion 极重。即使做过多种优化，类似模型仍可能需要两张 B200 才能运行，每张大约 7 万美元。若一台机器人都要配这样的计算，经济上无法规模化。VLA 没有死，一个原因恰恰是它比较小。

**Guanming Wang：** 先解释 WAM 的训练与 inference。训练时，current observation 作为 flow matching condition；未来视频的 clean latent 被逐步加入 noise，模型学习 velocity field，再通过 ODE 把 noisy latent 还原为 future latent。inference 从 pure noise 开始，沿反方向迭代，生成未来状态。

在典型 architecture 中，左侧是 video prediction，右侧是 inverse dynamics model。为了产生含 16 帧的一个 chunk，diffusion transformer 可能因 classifier-free guidance 运行 32 次：每一步既算 conditional flow matching，也算 unconditional 分支，再组合 gradient。某些设置会 autoregressively 做 50 甚至 100 个 denoising step，以换取质量。这就是主要延迟来源。

训练阶段拥有 ground-truth future，可以把 clean latent 按不同 noise level 扰动，并监督模型恢复对应 velocity。部署阶段却没有真实未来，只能从 noise 开始反复求解。视频分辨率、frame 数、denoising step 和 classifier-free guidance 分支会相乘，因此 WAM 的成本不只是“比 VLA 多生成几张图”，而是整个 diffusion loop 被放进机器人实时控制周期。

一种路线是少生成视频。ImageRAM 不预测整个 future video，只预测 `T+N` 的终点图像。FAST-WAM 更激进：它认为 world representation 已经存在 DiT hidden state 中，因此训练 action head 时直接使用 hidden state，不再通过 decoder 还原视频。显式生成的 WAM 像在 Google Maps 里打开完整 VR 预览；latent WAM 则像只看 navigation representation，再决定车辆动作。

核心问题变成，怎样在不解码所有像素的情况下保留丰富 world representation。JEPA 路线会用两个 encoder 分别编码 current observation 与 future observation，再最小化 latent 之间的 prediction loss，例如 MSE，让当前表示学会预测未来。另一条路线把未来看作多种可能组成的 distribution，通过 flow matching 学习 action distribution，而不是只回归一个平均未来。

我们从 infrastructure 角度组合多项优化。第一，distill VAE encoder-decoder。第二，distill DiT，让 backbone 变小。第三，把原先共用的 DiT 拆成 video transformer 和 action transformer，action 侧通过 cross-attention 读取 video hidden state，不必把 future frame 全部 decode。第四，把原本 50 或 100 步的 flow matching sampling distill 到一至两步，大幅缩短 latency。第五，探索 pixel 之外的 modality，例如 mask、optical flow 或只保留高能量 key frame cache，让表示集中在未来 0.5 秒真正与动作有关的区域。

拆成两个 transformer 不代表丢掉 world model。video branch 仍负责形成关于未来 dynamics 的 hidden representation，action branch 则读取这些 latent feature 并产生 kinematics。显式 frame 只是训练 representation 的一种监督，不一定是部署时必须交付的产品。只要 latent 保留了接触、运动方向和对象状态变化，decoder 就可能被裁掉。

asymmetric denoising 也基于同一原则。相邻视频帧大部分像素没有变化，平均重建整幅图会把大量 compute 花在静止背景。若能根据 key-frame cache 的 energy 识别真正发生动作的区域，就可以对高信息部分使用更精细预测，对其他部分只维持低成本 latent。mask 与 flow 是候选表示，因为它们比完整 RGB 更直接描述“哪里将移动、怎样移动”。

在我们的实现中，world action model 可以在 Jetson Thor 上约 500 毫秒产生一个含 16 个动作的 chunk。重点不是宣称 world model 已经免费，而是把原本只能在昂贵 datacenter GPU 上运行的 architecture 推向 edge、real-time deployment。

**观众：** 训练时从 clean future latent 逐渐加噪可以理解，但 inference 从 pure noise 出发，怎样保证最后收敛到正确未来，而不是继续退化成噪声？

**Guanming：** 训练过程让模型学习整个加噪路径的反向 velocity field，所以 inference 能从 pure noise 逐步回到 clean future latent。它与 curriculum 的直觉接近，但原始方法要走约 50 步，因此很慢。我们通过 distillation 把它压到两三步，同时尽量不牺牲 performance。

**观众：** WAM 的提升是否来自 action head 被迫关注更丰富的 frame detail？多 agent 场景中，它会不会为了预测世界而形成某种 theory of mind？

**Guanming：** 最基本的区别是，VLA 常由 current observation 直接预测 current action，没有显式 future kinematics supervision。WAM 让模型预测未来视频。比如手里拿着水瓶然后松手，未来 pixel 会显示瓶子下落，这迫使模型学习动作、physics 和视觉变化之间的关系。我们相信这种 future dynamics representation 能帮助动作生成。至于多 agent 的 theory of mind，这场报告没有给出独立验证，不能仅凭视频预测能力推断模型已经形成这种认知。

**Francois：** 为验证这个假设，能否先训练 transformer 做 next-frame prediction，然后拆掉生成 head，只留下表示给 action head？

**Guanming：** 可以，这正是 latent WAM 的方向。更高效的实现还可以用 mixture of transformers，让 image-editing backbone 与 action expert 分离，再由 action expert cross-attend backbone 最后一层。ImageRAM 和 FAST-WAM 都表明不必显式 decode frame，hidden state 本身可携带 world representation。

**Francois：** test time planning 呢？能否采样十个 end state 和十套 action，再选最好的一个执行？

**Guanming：** flow matching 本身就在学习可能动作的 distribution，并从中采样 trajectory。teacher forcing 帮助模型学习这个 distribution。不过“采样多个候选后用什么 objective 选最好”仍需要额外 evaluator；这场分享主要解决生成速度，而不是完整 planning stack。

**Francois：** 为什么选择做 WAM 的 vLLM，而不是按 Niko 的建议做一家端到端 robotics application company？

**Guanming：** 这个让 Bill 回答。

**Bill：** 我们相信 world understanding 很重要，但研究界现在更关注如何让模型尽可能 general。任何模型最终都必须放到 edge，在 real time 运行。当前很少有公司专门为 physical AI 做这层 infrastructure，我们希望先把模型真正跑进机器人里。

**观众：** WAM 的预测是只从 `T-1` 到 `T`，还是会包含更长 frame history？

**Guanming：** 这取决于 chunk size。训练常一次预测未来 16 帧，也可以做 32 帧或更多。chunk 越长，future state 越难学习，计算和误差累积也更重，因此不是越长越好。

**观众：** 是否了解只编码相邻 frame 差异的工作，例如 temporal-difference encoding，而不是重建每一帧？

**Guanming：** 这与我们的 asymmetric denoising 思路相近。可以度量 key frame cache 的 energy，只对动作细节最多的 frame 使用更高分辨率预测，其余部分留在 latent space。这样模型不必平均花计算重建所有未来 frame，而是把资源集中在当前动作真正改变世界的部分。

**Guanming：** 这里要区分两个目标。训练时预测未来画面，是为了迫使模型理解物体接下来怎样运动；部署时把每个未来像素完整显示出来，并不是机器人完成动作所必需。只要内部表示保留了运动方向、接触变化和可能结果，动作模块就可以直接读取。我们的优化工作正是减少那些只为生成漂亮视频、却不提高控制质量的计算，同时保留对未来动力学真正有用的监督。
