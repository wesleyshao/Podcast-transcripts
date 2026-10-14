---
访谈时间: 2026-08-03
访谈时间说明: 无法确认实际访谈日期，按 YouTube 发布时间 2026-08-03 使用
YouTube发布时间: "2026-08-03T22:42:52Z"
嘉宾名字: "Dmitri Dolgov"
嘉宾公司名称: "Waymo"
参与嘉宾:
  - 姓名: "Dmitri Dolgov"
    公司或机构: "Waymo"
    职务: "联席 CEO"
播客名称: "Y Combinator"
播客url地址: "https://www.youtube.com/watch?v=Gp4zrV3-6N8"
youtube_video_id: "Gp4zrV3-6N8"
字幕来源: "YC Root Access 官方文章公开完整 transcript"
公开文字稿地址: "https://www.ycrootaccess.com/p/dmitri-dolgov-seven-lessons-from"
原始语言: "English"
全文提及的关键名词:
  - "Waymo"
  - "Waymo Driver"
  - "physical AI"
  - "digital AI"
  - "VLM"
  - "ConvNet"
  - "Transformer"
  - "LiDAR"
  - "radar"
  - "Doppler"
  - "Phoenix"
  - "Bay Area"
  - "foundation model"
  - "multimodal world action language model"
  - "encoder-decoder"
  - "system one"
  - "system two"
  - "think fast"
  - "think slow"
  - "bitter lesson"
  - "end-to-end"
  - "structure-augmented end-to-end"
  - "open loop"
  - "closed loop"
  - "behavioral world model"
  - "sensing world model"
  - "Google DeepMind"
  - "Genie 3"
  - "critic"
  - "safety and readiness framework"
---

# Waymo Co-CEO Dmitri Dolgov: The Demo Is Only 1% Of The Work

## Transcript

Dmitri Dolgov：各位下午好，很高兴来到这里。我们平时谈很多活在屏幕里的 AI，也就是 digital AI。今天我想讲另一类 AI，Waymo 这些年一直在造的、真正活在现实物理世界里的 AI，也就是 Waymo Driver。顺便问一句，在场坐过 Waymo 的人有多少？请举手。人数比我想象得还多，尤其我知道很多人并不是 Bay Area 本地来的。还没体验过的人，这几天如果在湾区有空，我真建议你们去坐一次。既然这是 Startup School 2026，我就把这场分享组织成 7 条 lessons，讲讲 Waymo 这些年学到的东西：到底怎样才能把今天 physical AI 里最成熟的一类产品安全地造出来、真正推向社会、再把它扩到大规模。

我先用一个很短的视频开场。那是我最近带着孩子坐 Waymo 时拍下来的一段路况。车正通过一个路口，前面两辆人工驾驶车辆突然横切进来。Waymo Driver 的反应既安全又平顺，后排的孩子因为正在忙自己的事，甚至没意识到刚才发生了什么。对我来说，那一刻非常有力量。我在这项技术、这个产品上已经做了接近 20 年，它刚刚做成了一件很重要的事：它安全地处理了风险，它保护了我的孩子，也保护了周围所有人，而整个过程安静到几乎没人察觉。我觉得这会成为理解 physical AI 的一个核心主题，最好的 AI 时刻，很多时候看上去像是什么都没发生。任务只是被安全、平稳地完成了。

这样的时刻每天都在 Waymo 车队里发生。今天，Waymo Driver 每周服务大约 500,000 单行程，每周完成超过 4 million fully autonomous miles，在美国 15 座城市里运行。拿一个更直观的对比来说，这相当于平均美国司机 300 多年的年行驶里程，每周都在发生。更重要的是，它是在 superhuman 的安全表现下完成这些事情的。所以问题来了：要把一个 physical AI agent 在现实世界中大规模部署出去，到底需要什么？硅谷常见一句话叫 move fast and break things。但你面对的是 atoms，不是 bits，break things 这件事根本不可接受。你真正必须做到的，是 move fast and ship safely。

这比口号难太多了。你必须从第一天开始就把系统做得 robust，必须从第一天开始就让安全成为模型、训练配方、系统工程的基础，而不是后来贴上去的补丁。更底层的原因是，physical AI 和 digital AI 面对的是不同的问题结构。我把这种差异概括成 4 个 gap。

第一，是 cost-of-errors gap。一个 language model、chatbot、copilot 出错，很多时候代价只是你重试一次；physical AI 出错，代价可能按人的生命来计，没有“撤销”和“重来”按钮。第二，是 latency gap。VLM 或数字助手慢几秒甚至几分钟，很多场景还能忍；一辆在高速上行驶的车 1 秒就能前进大约 100 英尺，所以毫秒级差异都很关键。你得把所有 inference 和决策，都放在一个能塞进后备厢的车载 compute 里实时跑完。第三，是 data gap。digital AI 背后有互联网，这几乎是人类已积累知识和表达的巨大预标注语料库；physical AI 没有一份现实世界版的“互联网”可直接拿来用。第四，是 validation gap。digital AI 很多时候可以先上线一个“差不多够用”的版本，让用户替你发现 edge cases，再不断迭代爬坡；physical AI 不能这么干。因为错误代价太高，在你第一台机器人上路、第一英里 autonomous mile 开跑前，你就得先把安全门槛和置信度抬到非常高。

但事情又不只是保守。physical AI 还有一个现实：系统真正进入世界以后带来的经验，是实验室里任何离线开发都替代不了的。你既不能把东西关在实验室里做到“完美”后再一夜之间满规模部署，也不能没边界地把用户当实验对象。所以你必须极其清楚地定义 agent 的 operating conditions 和 deployment parameters，再围绕它搭建一整套严密的部署框架，指导系统如何负责任地扩张。这件事决定了你能不能赢得客户、社区、监管者，乃至你自己对系统的信任。

在 Waymo，这些 gap 是以自动驾驶的形式体现出来的，但它们几乎会出现在所有稍微复杂一点的 physical AI agent 身上。只不过驾驶是第一个已经让公众大规模直接接触到这 4 个 gap 的领域。所以，下面我想按 7 条 lessons 来讲，我们这些年到底是怎么跨过这些 gap 的。今天我只讲技术层面，不展开公司运营和商业化本身。单看每一条，它们未必听上去石破天惊，很多你可能在别处也听过，但我希望，把这些教训放回 Waymo 真正部署 physical AI、并把它安全 scale 出去的过程里，你们能更具体地看到它们为什么重要。

### 第一条教训：Demo 和 Product 之间的鸿沟，比你以为的大得多

先说一句可能让人沮丧的话：一个能跑起来的 demo，最多只完成了 1% 的工作。后面那些 performance 的 nines、reliability 的 nines，才是大头。如果你现在正在创业，八成正盯着第一个 prototype、第一个能站住台的 demo。那个时刻当然非常迷人。第一次系统能跑通、那个“前 90%”终于出现时，你会有一种“问题已经被解掉了，接下来只需要往前推”的强烈感觉。Waymo 当年也经历过这个阶段。项目 2009 年启动时，我们给自己设了两个很硬的目标。第一，自动驾驶模式下行驶 100,000 英里。第二，在 Bay Area 选 10 条路线，每条 100 英里，覆盖不同路况和环境，每一条都要从头到尾零人工接管完成。

那时候团队大概只有十几位工程师，我们大约用 18 个月完成了这两个目标。注意，这发生在今天大家熟悉的一切 AI 浪潮之前，在 ConvNet、Transformer、VLM 成为主流之前。可即便如此，我们还是做到了。以 demo 的标准看，自动驾驶在 2010 年几乎就“解决了”。白天能开，夜里能开，交通流能处理，行人、自行车、红绿灯、施工区、高速路、地面道路都能应付。当时我们觉得自己已经 capability complete，感觉像站在山顶。

但一旦你真往 product 走，现实会立刻给你一记重击。把一件事做成 1 次，或者把 10 条路线各跑成 1 次，和把它做成一个无人驾驶、可规模化、可面向公众连续提供服务的产品，根本不是一回事。我们又花了大约 10 年才真正开始对外提供服务，再花了大约 5 年，才把规模推到每周 500,000 单。也就是说，demo 用了 18 个月，product 花了大约 15 年。到今天，我们累计已经完成远超 20 million fully autonomous trips，跑了远超 200 million fully autonomous miles。我们在美国 15 座城市里有 rider-only 车辆在跑，而且规模还在指数式增长。走到第一个 100 million miles 用了 15 年，再跑下一个 100 million miles 只用了大约 7 个月。从最早开启 rider-only 服务到覆盖 4 座城市，我们花了 8 年；而今年早些时候，我们在 1 天里就新开了 4 座城市。

为什么从 demo 到 product 要这么久？因为这里有一个谁都绕不过去的工程现实：reliability 和 performance 活在一个指数型的“nines 梯子”上。达到第一个 90% 或 99%，通常是容易的；但你每多加一个 9，成本和努力大约都要再乘 10。你必须一开始就知道，你的产品到底需要多少个 9。一个 demo 也许只要 1 个 9，一个 assist product 或 copilot 也许要几个 9；但一个要在真实公共道路上自己开、周围还有孩子和行人的 fully autonomous AI agent，需要的是一整叠 9。在这种规模下，long tail 不再是边角料，它就是你的整个问题本身。每周开数百万英里之后，一个“百万英里才遇到一次”的 rare event，就会变成你的 daily reality。

更麻烦的是，后面的每一个 9，都不是靠把前面那套方法“再坚持久一点”就能拿到。你不可能靠重复做同样的事，把 2 个 9 顺延成 6 个 9。你得换方法，甚至换范式。可靠性是这样，模型表现也是这样。前两个 9 也许靠规范工程和修 bug 能拿到；后面几个 9，你就得上 fully redundant systems、tiered fallback architectures 这类根本不同的东西。也正因为如此，这个领域“起步容易，做成极难”。每一波 AI breakthrough 都会让起步更容易。deep learning 也好，ConvNet 也好，Transformer、VLM 也好，都会让 demo 和 prototype 的搭建门槛大幅下降。但 long tail 那部分虽然也会受益，变化幅度却远没前端那么夸张。于是每一轮 hype cycle 都会产出一堆炫目的 demo，却只留下极少数真正的 product。这个周期里反复出现的错误，就是把本来应该省给那些 nines 的预算，先花在了 demo 上。

我不是想给创业早期泼冷水。那段时期非常魔幻，也非常珍贵，值得充分利用。但前提是你得老实面对你到底在造什么产品，它到底要求多少个 9 的 reliability 和 performance，以及你有没有在关键地方抄近道。否则，后面等你的往往不是惊喜，而是极其粗暴的现实教育。我的建议很简单：先数清楚你需要几个 9，再去数 demo views。

### 第二条教训：先选对技术曲线，而不是只盯着前期爬坡速度

一旦你知道自己的产品需要多少个 9，很多事情其实已经被决定了。它会反过来决定你该选什么架构、什么技术路径。每一种技术都有自己的 performance-versus-effort 曲线。通常起点看上去都很陡，进展很快，但随后会变平。常见失败模式是，你选了那条前期爬坡最快的路线，顺着陡坡往上冲，觉得自己赢了，甚至直接把这条斜率外推到未来，结果冲到一半才发现，这条曲线的天花板远低于产品真正需要的性能门槛。你当然可以为了原型、学习或者验证某个想法，暂时走一条“起步更快”的路，但你得诚实：你是在为 demo 服务，还是在为 product 服务？

自动驾驶里最典型的例子就是 sensing。到底该用哪些传感器，行业里争论了很多年。传感器越多，能力通常越强，但成本和复杂度也会上去。人类只靠眼睛开车，这是一个很强的 existence proof。假如你的目标只是大致接近人类表现，或者做一个 assist product，那么只靠 camera 之类的弱 sensing 路径，完全有它的合理性。但如果你的目标是 full autonomy，而且是 clearly superhuman 的表现，那么你很快就会发现，弱 sensing 对应的安全曲线会过早变平。Waymo 的选择一直是多模态 sensing，我们同时用 cameras、LiDAR 和 radar，而且不是把它们当彼此的 backup，而是把它们融合成同一个、比任何单一传感器都更精确的世界视图。

camera 的优点是高分辨率、有颜色信息，但它是被动传感，在黑暗、眩光等条件下会明显退化。LiDAR 能直接给你周围世界的 3D 结构。radar 很擅长穿透 fog、rain、snow 这类环境条件，而且能利用 Doppler 直接测速度。LiDAR 和 radar 都是主动传感器，所以即便是完全漆黑，或者正对刺眼落日，它们的表现仍然很强。在 Waymo 的 stack 里，每种模态都有各自的 encoder，随后所有信息都会被 fuse 进统一表征。

这不是纸上谈兵。比如在 Phoenix 的沙尘环境里，camera 看到的画面非常接近人眼：几乎什么都看不清；但 LiDAR 在同一帧里能更早、更清楚地看见路边站着的行人。如果对方下一步跨进车道，早检测几拍，对安全结果就可能是决定性的。再比如夜里经过施工隔离墩，camera 几乎看不到，LiDAR 却能更早捕捉到正要翻过护栏跳进路面的行人。再比如黑灯瞎火的路边，几只狗追着球跑，几个孩子又在追狗，camera 里几乎一片黑，LiDAR 却能更早把孩子从侧面捞出来。还有一种经常被忽略的场景，是传感器本身的物理遮挡。假如你没有 sensing redundancy，一片树叶糊到关键传感器上，就足以让机器人直接瘫掉。我们自己就遇到过这样的事，有一辆车被树枝卡住了雨刷，没法甩掉，但因为有冗余 sensing，车还是能安全回 depot 做彻底清洁。

所以我的建议是，不要把自己锚死在今天的硬件价格上。Waymo Driver 的硬件今天已经做到第 6 代。每一代不只是能力更强，硬件复杂度和成本也在大幅下降。你如果用“今天某个零部件太贵”来给整个公司定战略，本质上等于把公司押在一个保质期很短、很快就会失效的数字上。硬件一定会变，很多组件一定会 commodity 化、会降价。真正该做的是为未来的硬件曲线设计系统，并且让自己随时 ready to upgrade。

### 第三条教训：每一波技术浪潮都要骑上去，但更重要的是统一和简化

技术变得太快了，尤其是现在。所以公司必须学会反复 riding those tech waves，而且每次 riding 的时候，不能只看 capability 和 performance 的提升，还要同时看 unification 和 simplification。过去这些年，我们基本上每遇到一次大的 AI 技术浪潮，就会围绕它把 Waymo Driver 的核心能力重建一遍，而且很多时候我们自己也在往前推进 state of the art。2013 年左右，ConvNet 浪潮起来时，我们把它重押在 computer vision 和 perception 上；到 2017 年左右 Transformer 出来，我们又大规模把它用到 perception，以及 behavior prediction、decision making、planning 上。

驾驶这件事，其实和 language modeling 并没有大家想得那么远。道路上的 driving 也是一种“对话”，只是你交流的不是文字，而是车身动作、速度变化、让行关系和时序信号。它同样发生在 sequence 里，既需要 local continuity，也需要 global context。到今天，我们又在吸收最新的 VLM 和 frontier world models。问题在于，把最新技术拿来做孤立的 capability research，往往还不算最难；最难的是把它稳定地拉进 production，放进一个 safety-critical 的系统里，不引入 regression，不打断已有部署和 scale 的节奏，同时还别把整个 stack 越做越碎。

我有两条很具体的建议。第一，每当一种新技术出现时，当然应该让 tiger team 去试，甚至应该积极去赌。但你必须在立项时就想清楚，如果这个项目成功了，后面怎么进你完整的产品系统。很多技术项目最浪费、也最伤士气的一种死法，就是技术目标明明完成了，最后却没有任何通往生产系统的路径。第二，评估新技术时，不要只问“它让我多了什么能力”，还要问“它有没有让我的 stack 更简单”“它带来的是 fragmentation，还是 unification”。你真正该设的 launch bar，不只是突破性的性能，还包括激进的简化和统一。

Waymo 这些年真正练出来的，就是这块肌肉。它最后产出的核心成果之一，就是我们的 Waymo foundation model。这个名字拆开看就清楚了：它是一个 multimodal world action language model。multimodal，意味着它能同时处理 cameras、LiDAR、radar 等多模态输入；world model，意味着它本身理解世界如何运作，包括 physics、dynamics、social context 和 semantics；action model，意味着它不是被动旁观世界，而是系统的一部分，它必须理解 agent 自己的动作会怎样改变世界，并能区分好动作和坏动作；aligned with language，则让它可以借助 VLM 解锁更一般的世界知识，尤其是在那些稀有、语义负担很重的 long-tail 场景里。

在结构上，它是典型的 encoder-decoder 架构。encoder 接收多模态 sensing，把它压缩成既高效又尽可能保留关键信息的表示，交给 generative 的 decoder 去做后续推理和生成。它是一个 end-to-end 模型，所以梯度可以从最终任务一路 backpropagate 到前层，让 encoder 真正学到 generative 部分所需的 rich representation。与此同时，它又采用了 system one / system two，也就是 think fast / think slow 的双路径架构。

think fast 那条路径，主要融合原始的 camera、LiDAR、radar 数据，用来做毫秒级的 safety-critical 决策。你可以把它理解成驾驶本能，或者 agent 的 lizard brain。比如行人突然冲出路面，或者自行车突然切进来，它就得立刻做出反应。think slow 那条路径，则负责更复杂的语义理解和场景级 reasoning。这类问题通常不会在毫秒里剧烈变化，所以你可以用更高的 latency 去换更强的理解能力。举个例子，如果 Waymo Driver 遇到路边一辆起火的车，fast path 也许只会把它当成一个普通障碍物，觉得几何上“前方可通行”；而 slow path 会识别出“那是一辆着火的车”，在更大的 scene context 里进行语义判断，于是可能决定绕行，哪怕前方从纯几何角度看是畅通的。再往后，decoder 负责真正生成和理解行为，预测其他 actor 会怎么动，并据此规划自己的 driving decisions。

这套 Waymo foundation model 已经在支撑不同世代的 Waymo Driver 硬件，也支撑不同 vehicle platforms，比如 Jaguar I-PACE、Ojai、Hyundai Ioniq。未来它也会去支撑更多产品形态，比如 trucking，甚至 personally owned vehicles。我们刻意把大量复杂性 upstream 到高容量的 foundation forward model 里，再把车上那层 specialization 尽量做轻，这直接加快了整个研发节奏。总结这一条，真正重要的不是“今天有没有跟上技术热点”，而是公司是否有能力一次又一次地把技术浪潮安全吸收进生产系统，不回退、不掉速、不把复杂度淹没自己。

### 第四条教训：bitter lesson 依然成立，但结构该怎么用，比口号本身更重要

AI 领域有一条非常著名的判断：一般性方法，只要能更好地吃下大规模 compute 和 data，最终几乎总会打败那些依赖人工手工知识注入的方法。这就是 Richard Sutton 在 2019 年明确写出来的 bitter lesson。Waymo 这些年几乎在每一波技术更迭里都亲眼见到它成立。每一次，真正赢出来的，都是那些能更好利用 compute 和 data 的方法。这也是我们为什么下注 foundation model。一个高容量模型配上更强的 data 和 compute，往往会展现出更好的 scaling laws，然后你再把它 distill 到更小、更高效、能在 agent 上实时运行的模型里，通常比一开始就死盯着小模型更划算。

不过，bitter lesson 在 physical AI 里有一个很细腻、也很容易被误用的地方，就是 structure。结构用得对，你会站在 bitter lesson 这一边；结构用得不对，你就会站到它的对立面。简单说，抵触 scale 的 structure 最终会输；引导 scale、帮助 scale 的 structure 会赢。这在 end-to-end 的讨论里最典型。end-to-end 模型有很多好处。它允许你把最终任务的梯度一路传回整个模型，让 encoder 和 decoder 之间的接口由 learned representations 自己长出来；已知架构成熟、训练流程也清晰，配合 imitation learning，纯 black-box 的 end-to-end 往往能带来非常快的前期进展。对于某些产品，这已经够了。

但如果你的目标是在 safety-critical 的现实环境里做出 superhuman 水平的 fully autonomous agent，基本款、原教旨的 vanilla end-to-end 不够。这时候关键就变成：你加入的 structure，到底是在限制模型、缩窄解空间，还是在不损失一般性的前提下帮你 scale？我用一个玩具例子讲清楚这个问题。假设你想造一个在现实世界里下围棋的机器人。它有 camera 看棋盘，也有 actuator 去落子。一种做法是从 pixels 直接 end-to-end 到 actuation，甚至用人类对局视频去学。这当然会是个很有意思的研究项目。但如果你的目标是造出世界上最强的围棋机器人，这就不是最有效的路线。因为围棋这件事有一个极其清晰的中间表示，也就是 19x19 的棋盘状态。它已经完整表达了这项任务里你最关心的世界状态。利用这个中间结构，并没有限制模型，反而给了你一个更高效的 scale 通道。

现实世界当然不像围棋这么干净。正因为现实世界没有这样一个现成、完美、纯人工设计的中间表示，我们才需要 end-to-end、learned representation 和 learned embedding。但现实世界并不是完全无结构。你有 physics，有 traffic rules，有大致可预测的 objects 行为。把这些 structure 和 learned representation 结合起来，可以同时提高 performance、简化 validation、改善 scaling laws。这就是 Waymo 现在走的路线，我们把它叫作 structure-augmented end-to-end。

它的做法是，在 learned embeddings 之外，再补上一层 materialized structured representations。这样做有几个非常关键的好处。第一，是 inference time validation。模型不再是一个“传感器进去、控制信号出来”的纯黑箱，你就能在车辆实时运行时，加上一层很强的 correctness 和 safety validation layer。对于现实世界里的 agent，这极其重要。第二，是大规模训练和评估的效率。如果你只有纯黑箱 end-to-end，那么训练和评估都只能在从 sensors 到 decisions 再到 actuation 的全链路空间里做，成本很高。中间那层结构化表示让你可以 mix and match，有的训练和 evaluation 在紧凑的 structured space 里做，有的再在完整的 end-to-end 空间里做。第三，是反馈信号更强。不管是做 evaluation、设计 metrics，还是做 reinforcement learning 的训练配方和 loss function，有了 materialized structure，你都能得到更强、更可验证的信号。

所以这一条真正的结论不是“别做 end-to-end”，而是：尽量下注在 maximally learned、minimally constrained 的系统上，同时有意识地利用 structure 去增强 performance 和 scaling laws，尤其是在 training 和 evaluation 里。

### 第五条教训：任何 serious 的 physical AI 公司，最后都绕不过一个高保真 simulator

说到 training 和 evaluation，就自然来到下一条 lesson。你想把一个 agent 安全地放进现实世界，大规模、真实感强、高保真的 simulator 几乎不是可选项，而是必需品。训练和评估大体有两种方式：open loop 和 closed loop。open loop 比较像被动观察输入输出对，你可以拿它做评估，也可以做训练，imitation learning 就是这种风格。典型问题是：“如果你处在这个场景里，你会怎么做？”然后根据答案打分。closed loop 完全不同。你做一个动作，世界因为这个动作发生变化，传感器再把变化反馈给你，你再做下一个动作，如此循环。你评估和训练的是动作序列，以及世界在这个序列下如何演化。

对于 safety-critical 的 physical AI agent 来说，能够真正做出一个动作、再评估它带来的 counterfactual 后果，是绝对必要的。要完成这件事，你需要的不是一个“顺手做的配套工具”，而是一个真正意义上的 simulator，而一个真正合格的 simulator，本身就是一个很大的 AI model。造出一个高质量、足够真实的 simulator，难度并不比造 agent 本身低。它必须理解世界怎么运作，理解 physics、semantics、traffic、weather 等等。它的质量必须高到不只是“看起来像”，而是足以支持你在高置信度下训练和评估一个即将进入安全敏感现实环境的 agent。换句话说，你最终要造的是高精度的 generative world model。

Waymo 很早就在做这件事。甚至在 world models 这个词流行之前，我们就已经在做 behavioral world model。现在进入 end-to-end 时代之后，仅有 behavior realism 还不够，你还要有 sensing realism。老实说，把 end-to-end model 训练出来本身，很多时候已经不算最难；真正难的是怎样在 closed loop 里把它评准。于是我们又进一步做 sensing world model。因为我们的主模型采用了 structure-augmented end-to-end，所以 simulator 也能借用同样的结构：behavioral world model 在结构化中间表示空间里运行，和它紧耦合的 sensing world model 再生成真实的传感器仿真。我们的 world model 还利用了 Google DeepMind 的 Genie 3 成果，这让我们不但能生成高度可控、高度真实的 behavior 场景，还能把 sensing 侧也做得足够逼真。

一旦你有了这套能力，你就不只是能在“历史上真实发生过”的场景里评估和训练新版本 agent，而是能在从未于现实中见过的、纯合成的 rare scenarios 里训练和评估。比如，模拟高速公路车道里停着一辆坏车；再极端一点，模拟一架飞机在你前方迫降到高速公路上；或者一头大象在路口乱跑；或者 Golden Gate Bridge 上突然下雪；甚至一只 dinosaur 在路上行走。重点不在于这些例子猎奇，而在于 closed loop simulation 是 evaluation 的硬要求，对 training 也有极高价值。没有大规模、高保真的 simulator，你几乎不可能把 physical AI 安全地推向现实世界。

### 第六条教训：你最终得造出一个 AI ecosystem，而不只是一个模型

问题复杂到这个程度以后，你就不能只造一个 model，然后说“差不多了”。你必须造出一个完整的 ecosystem，而且还得有一个能持续加速自己的 flywheel。因为要把这件事做成规模化系统，你实际上至少要造 3 个 AI。第一个是 agent，本体，也就是 Waymo 里的 driver。第二个是 simulator，它是 agent 的虚拟练习场。第三个是 critic，负责严苛评判 agent 的表现，并告诉它如何改进。好消息是，这 3 者底层需要的 reasoning 和 generative 能力大量共享，所以在 Waymo 的体系里，它们都建立在同一个 foundation world model 上。

当这 3 根柱子搭起来以后，就能形成一个非常强的 flywheel。agent 被部署到现实世界，生成数据；这些数据反过来校准 simulator，让它更真实；simulator 又能产出更难的 edge cases，交给 critic 去评分，也交给 agent 去学习；agent 变得更聪明，再部署到现实世界里，生成更多数据，于是整个飞轮开始转得越来越快。当然，flywheel 自己也会盲转，甚至原地空转。要让它朝你想要的方向加速，唯一的办法就是 metrics。

### 第七条教训：真正的战略护城河，不是模型本身，而是 eval 和 metrics

所以最后一条 lesson 很直接：model 本身只是 table stakes，eval 和 metrics 才是你真正的战略护城河。我的建议甚至可以说得更狠一点：在你造技术之前，先造 eval；在你造产品之前，先造 metrics。你如果不能定量定义什么叫 good enough，那你并不是在造 product，你只是在不停修 demo。今天最好的 model architecture 往往很快就会被整个行业知道，新 idea 扩散得也非常快。data 当然重要，但没有好 metrics，你就像在黑夜里飞，既不知道哪部分 data 真有价值，也评估不了你对系统做的任何改动到底有没有 ROI。

但 physical AI 对 eval 的要求，比 digital AI 深得多、广得多。只做 model-level evaluation 完全不够。你要验证的是整个系统：从最底层的 physical layer，到车辆 onboard 的 behavior layer，再到所有 offboard components，以及围绕它们运行的 operational processes。Waymo 内部把这整套东西叫作 safety and readiness framework。我们花了很多年去构建和打磨它，它指导我们的开发、部署和 scale。我认为，这就是 Waymo 最重要的资产之一。

原因其实很朴素：在 physical AI 里，trust 就是一切。而 eval 和 metrics，就是你赢得 trust 的手段。你不会因为某个 clever 的 technical solution、某个 state-of-the-art architecture、或者一个 flashy demo，就真正得到用户和社会的信任。你只能在真实世界里一天一天地证明：系统是安全的，系统是有效的。当然，这种证明也不能只关起门来对自己说。正因为如此，我们会公开发布安全数据和持续中的安全研究。最终，真正构成商业优势的，不是你会说什么，而是你已经在真实世界里跑出来了什么。模型会被泄露，算法会被复制，但那种由 hundreds of millions of miles 的 fully autonomous 真实运营、evidence-grade evaluation、以及公开可审计证据支撑起来的能力，复制起来要难得多。

### 这些 lessons 不是分开的，它们会彼此放大

如果你把整套 playbook 拉远一点看，会发现没有哪一条是独立工作的。nines 决定你的门槛，逼着你选对技术路径，避免陷在 local minimum；有意识地利用 structure，以及一次次 ride technology waves 的能力，让你能真正爬到那个门槛；而由 agent、simulator、critic 组成、再由 eval 和 metrics 引导的 AI ecosystem，才让你拥有那个会不断自我强化的 flywheel。正是这些因素叠加在一起，才让 Waymo Driver 最终达到了 strongly superhuman 的安全表现。

我们最近公开的一版安全数据，基于超过 220 million fully autonomous miles。结果显示，在我们运营的区域里，Waymo Driver 在导致 serious injury 的 crash 上，大约比 human drivers 好 17 倍。这件事之所以重要，不是因为它让 dashboard 上的某个数变漂亮了，而是因为今天这个世界上，大约每 26 秒就有一个人死于道路交通事故。按 Waymo 目前的运行规模计算，我们大约每 8 天就在避免一次 serious injury。这背后不是抽象的统计学，而是有人所爱的人，今晚可以安全地从门口走进家里。

而这还只是 physical AI 最早期的安全收益。如果把视角再拉大一点，机会其实巨大。今天的 physical AI，某种程度上就像几年前的 digital AI：我们已经有 generative world models，有可用的 architectures，有越来越 affordable 的 compute 和 sensing，有被证明存在的 scaling laws，也终于有了一个在规模上真正跑起来的 product。过去 10 年，AI 的主战场在数字世界里；我认为，接下来 10 年，主战场同样会发生在物理世界里。

如果你们之中有人决定去 build in this space，我的祝愿很简单：祝你好运，也祝你玩得开心。但别忘了，你到底是为谁而建。你的 mission 和你的 customers，才是最重要的。如果没有这些，技术最终就只是个 science project。说到底，技术再令人兴奋，也比不上真正改变人们生活这件事本身带来的满足感。
