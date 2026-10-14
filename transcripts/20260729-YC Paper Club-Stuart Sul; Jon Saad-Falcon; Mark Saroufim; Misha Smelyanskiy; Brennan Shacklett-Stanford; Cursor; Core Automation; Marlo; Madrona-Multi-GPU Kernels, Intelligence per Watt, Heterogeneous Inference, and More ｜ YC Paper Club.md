---
访谈时间: 2026-07-29
访谈时间说明: 无法确认活动实际日期，按 YouTube 发布时间 2026-07-29 使用
YouTube发布时间: 2026-07-29T23:46:52Z
嘉宾名字: "Stuart Sul; Jon Saad-Falcon; Mark Saroufim; Misha Smelyanskiy; Brennan Shacklett"
嘉宾公司名称: "Stanford; Cursor; Core Automation; Marlo; Madrona"
参与嘉宾:
  - 姓名: Francois Chaubard
    公司或机构: Y Combinator / Stanford
    职务: YC Paper Club 主持人，未知
  - 姓名: Stuart Sul
    公司或机构: Stanford / Cursor
    职务: Stanford CS 博士生、Cursor 研究员
  - 姓名: Jon Saad-Falcon
    公司或机构: Stanford
    职务: CS 博士生
  - 姓名: Mark Saroufim
    公司或机构: Core Automation / GPU MODE
    职务: Core Automation 联合创始人、GPU MODE 联合创始人、前 PyTorch maintainer
  - 姓名: Misha Smelyanskiy
    公司或机构: Marlo
    职务: 创始人；曾任 NVIDIA AI infrastructure 负责人并在 Meta 从事 hardware-software co-design
  - 姓名: Brennan Shacklett
    公司或机构: Madrona / Stanford
    职务: 研究者，未知
播客名称: YC Paper Club
播客url地址: https://www.youtube.com/watch?v=n8dz2FX0_uY
youtube_video_id: n8dz2FX0_uY
字幕来源: YC Root Access 官方文章公开完整 transcript
公开文字稿地址: https://www.ycrootaccess.com/p/multi-gpu-kernels-intelligence-per
原始语言: English
全文提及的关键名词:
  - CUDA
  - GPU
  - TPU
  - ASIC
  - kernel
  - token
  - prefill
  - decode
  - batch size one
  - RL
  - RLHF
  - RLVR
  - MoE
  - KV cache
  - speculative decoding
  - AllReduce
  - All Gather
  - reduce scatter
  - NVLink
  - NCCL
  - PTX
  - SASS
  - PCIe
  - HBM
  - SRAM
  - FLOPs
  - arithmetic intensity
  - roofline
  - FlashAttention
  - Linear Attention
  - ParallelKittens
  - ThunderKittens
  - Triton
  - CUTLASS
  - CuTe DSL
  - PyTorch
  - Llama
  - GPT-OSS
  - Qwen
  - IBM Granite
  - Apple M4 Max
  - DGX Spark
  - SambaNova SN40L
  - OpenJarvis
  - KernelBot
  - Kernel Guard
  - KernelBench
  - QR factorization
  - LAPACK
  - cuSolver
  - Shampoo
  - Muon
  - matmul
  - GEMM
  - DGX
  - NVL72
  - Blackwell
  - Hopper
  - Tensor Memory Accelerator
  - TMA
  - SM
  - cache
  - GPU MODE
  - Core Automation
  - Cursor
  - Stanford
  - NVIDIA
  - AMD
  - Apple
  - Google
  - OpenRouter
  - Cerebras
  - Claude
  - OpenAI
  - Kimi 2
  - Thinking Machines
  - Anybots
  - Y Combinator
---

# Multi-GPU Kernels, Intelligence per Watt, Heterogeneous Inference, and More | YC Paper Club

## Transcript

Francois Chaubard：欢迎来到 YC Mountain View，今天是 YC Paper Club 的一个特别场次。之前有些反馈说，希望活动更有主题性，所以今天我们就做成 YC Kernel and Chip Club。我和 Stu、Jon 在实验室里一直在聊的一个趋势，就是系统正在发生越来越强的 specialization。我们已经在 TPUv8 上看到了这种苗头，I 版和 T 版，还有 Zebrafish、Sunfish，是这么叫的吧。做一颗 ASIC 的启动成本非常高，以前需求还不足以支撑这么细的切分，但现在我们已经明显看到，在 chip 这一层会出现大规模 specialization。训练型 data center 需要的规格，会和 inference 型 data center 完全不同。训练型 data center 基本不需要对外的带宽进出。

Francois Chaubard：你甚至可以把一艘飞船送到太阳旁边，训完模型再把 weight file 带回来，结果还是一样，对吧。inference 可不是这样。类似这种差异，今天我们都会聊到。CUDA 这一侧、kernel 这一侧，还有太多性能红利没榨干，我很兴奋今天能请到几位嘉宾来讲这些。算法侧也是一样，还有很多空间可以挖。是不是每一次 query 都非得调用那个巨大的重型模型？如果我只是问一加一等于几，为什么每次都要付出 N FLOPs？所以无论是算法、软件、chip，还是 data center，今天都还有很多 juice 可以继续 squeeze。第一位是来自我在 Stanford 实验室的 Stuart Sul，也是我的 lab mate。

Francois Chaubard：我们那个实验室现在基本成了 strip mall research lab。以前叫 Hazy，或者说前身叫 Hazy。Stu 同时也是 Cursor 的研究员，负责训练 Composer。接下来是 Jon，也是和我一起的 CS PhD lab mate，同时还受 Azalia Mirhoseini 指导，研究重点是 LLM、MLSys 和 hardware。他在推动一个很有意思的概念，叫 intelligence efficiency，也就是 intelligence per watt、intelligence per joule，今天他会讲这个。再往后是 Mark，前 PyTorch maintainer，和我朋友 Casey Aylward 一起创办了 GPU MODE，也在和 OpenAI VP Research Jerry Tworek 一起共同创办 Core Automation。然后是 Misha，过去二十年都在做 hardware-software co-design，曾负责 NVIDIA 的 AI infra，也在 Meta 做过 hardware-software co-design，现在也在做一家很有意思的新公司，等会儿你们会听到一些内容。最后是 Brennan，我也是在 Stanford 认识他的，他不在我实验室，但他做了很多 RL、自动驾驶之类的工作。很神奇的是，simulator 里你一旦调用 `environment.step`，大量东西到今天依然还在 CPU 上跑。

Francois Chaubard：这通常就是很多 on-policy rollout 的瓶颈所在，也让传统意义上的 RL 变得非常难做。现在大家一说 RL，都快被 RLHF 这个词给盖过去了，但经典 RL 其实还是非常非常难。而 Brennan 说的那种“用 GPU 做奇怪的事”，他确实是最擅长用 GPU 做怪事的人之一。我这里先放两张高层次的 slide。我绝不是最懂这些事的人，但从我的视角看，接下来一定会出现这种大规模 proliferate 的 specialization。现在 token 需求大到足以支撑 chip 级别的专门化，所以在 ASIC 上做完整的 new product introduction 会有回报。我觉得 Zebrafish、Sunfish、TPU v8 只是一个开端，后面会切得更细得多。

Francois Chaubard：其实我们已经能稍微看到一点了，比如在 inference stack 里，有人会用 NVIDIA 做 prefill，再用 Cerebras 做 decode engine，这本身就是一种拆分。但还有一种几乎没人好好讨论的场景，就是 batch size one inference。我觉得一旦 latency 真正真正重要，比如 voice agent，你打电话进去，它先说一句“Hi, how you doing?”，然后卡八秒，因为它为了 throughput 做了一整套流程，你就会觉得这根本不能用。大家会说，他们是在 prioritizing throughput。可问题是，那样就没法落地。如果真按 batch size one 去优化，他们又会很快把 GPU 用光，成本也高得离谱。所以这是个 chip 问题，而这种问题是可以被解决的。

Francois Chaubard：再往上到 data center 这一层，specialization 也会同样激烈，尤其是当你打算让不同 data center 用不同 chip 的时候。训练模型时你最关心的核心指标，本质上就是 time per step。你想训越来越大的模型，而 location 其实没那么重要，不需要贴近用户。你甚至可以把训练机房放到太阳边上，绕着太阳一直 train、train、train。GPU 类型、互联方式也会完全不同，训练里你需要 all-to-all communication，要传大量 gradient。inference 这边除了 MoE 某些场景外，并不总需要 all-to-all，所以你就可以做更好的 shard。还有很多别的因素，也都在支持把这些系统拆开来设计。

Francois Chaubard：这些细节我们后面的 speaker 会讲得更具体。下一个主题场应该会在 7 月 29 日做 robotics 专场，可能还会有几家 YC 公司直接把机器人带过来。说来也挺讽刺，YC 最初其实就是从这个方向起家的。街对面的老故事是，Trevor Blackwell 当时在做一家叫 Anybots 的公司，就是那边那批机器人。他手上有些多出来的空间，PG 就问能不能每周二晚上借点地方，办一个叫 Y Combinator 的东西。后来 YC 搬到了街对面，再后来把 Anybots 的东西都接过去了。这个闭环还挺酷。再之后下一个主题我很想听大家建议，比如也许可以聊 RLVR，或者最近的一些新进展。

Francois Chaubard：现在大家都在说这些 distillation attack 之类的话题，但我其实并不确定，外面那些真正成功的 distillation strategy 到底是什么。我们今天在实验室也聊了很久。到底最优策略是什么，并不清楚。如果你直接拿到一个 weight file，你该怎么 distill？如果你只有一个 API，又该怎么做？我今天是这么跟实验室里的人解释我对现状的理解的，Claude 像母鸟一样喂养 Kimi 2，然后 Kimi 2 又在给 Thinking Machines 做 post-training，这个链条就会一层一层往下传。好，接下来把舞台交给 Stu。大家欢迎 Stu。

Stuart Sul：好的，大家好。我叫 Stuart，是 Stanford 的 CS 博士生，同时也是 Cursor 的研究员，在那里训练 Composer。今天我要讲的是 ParallelKittens，这是我们关于如何把 multi-GPU AI kernels 做得既简单又快的一项工作。开始前先说明一点，这篇 paper 的最终交付物确实是一个 CUDA framework，我们叫它 ParallelKittens。但我今天的目标不是来推销开源库，而是想把我在做这项工作时总结出来的一整套经验教训讲清楚，也就是一套用来理解 multi-GPU kernel 和 GPU networking 的心智框架。我希望大家今天带走的，是我自己在这个过程中得到的那组 insight。先做一点动机铺垫。过去几年，ML systems 社区在 single-GPU efficiency 上投入了大量精力。

Stuart Sul：比如说，我们有 IO-aware algorithm，像 FlashAttention，有 linear attention model，有 mega kernel，也有很多跨不同架构编写高效 kernel 的 programming library 和 framework。这些工作主要都在帮我们把单张 GPU 的性能尽量榨干。经历了这些努力之后，我们现在越来越确信，GPU networking 才是剩下的主要瓶颈，而且这里还有很多激动人心的机会。举个例子，像 Llama prefill 这样的 workload，networking 仍然可能吃掉总 runtime 的 50%。当然这个数字会随 workload 大幅波动，但我要表达的核心是，networking 正在拖累 GPU utilization。于是今天的标准做法，就是把 inter-GPU communication 和 intra-GPU 的操作，比如 memory access 和 compute，尽量 overlap 起来。而且这个 overlap 的粒度现在已经变得非常细了。以前我们重叠的是整块 tensor 或矩阵的传输。

Stuart Sul：现在我们甚至会做到 tile 级别，甚至 token 级别的 overlap，也就是说每次传输的数据量可能只有几 KB，甚至不到 1 KB。另一方面，networking hardware 的进步也非常让人兴奋。比如我们有一种叫 in-network compute 的东西。以前如果你想实现 AllReduce 这样的 collective operation，需要设计一种算法，让 GPU 对本地数据做算术、把结果发给其他 GPU、重复 N 次，最后得到结果。但有了 in-network compute 之后，这些算术和通信中的一大部分可以卸载给 networking fabric，GPU 就能空出来做真正有价值的计算。现在还有 asynchronous bulk device-initiated networking，这在前几代硬件上根本做不到。再比如 scale-up architecture，像 NVL72，把 72 张 GPU 装进同一个 NVLink domain。

Stuart Sul：很快，这个规模还会扩展到上百张 GPU。在所有这些设定下，我们真正想解决的问题是，multi-GPU kernel 依然很难写，尤其是同时满足三点的时候。第一，要做 compute 和 communication 的细粒度 overlap。第二，要利用好这些近几年新出现的硬件特性。第三，还得保持代码足够简单，方便人类和 AI agent 维护。我要强调，真正让问题困难的是这三点必须同时成立。因为目前你大致只有三种替代路线。第一，直接用 NCCL 这种现成库，但它们只暴露粗粒度的 communication primitive，会在硬件执行里留下很多 bubble。第二，用 compiler-based approach，但我们发现这些 compiler 的结果往往很不理想，有时候甚至比不做 overlap 的 baseline 还慢。第三，就是直接上低层 primitive，比如 OS interprocess communication call 或 PTX assembly。

Stuart Sul：这些办法往往要求你对 networking hardware 有一种接近 reverse-engineering 的理解。总体来说，它们会让代码非常复杂、非常难维护。所以我们真正想问的是，有没有一小组原则或 trade-off，能把 multi-GPU AI kernel 的 design space 讲清楚？在此基础上，我们能不能构建一组最小化的 programming abstraction 或 primitive，让生产环境里的高效 multi-GPU kernel 更容易写出来？PK，也就是 ParallelKittens，就是我们给出的答案。在进入 PK 之前，先给不熟悉这块的朋友快速过一遍 GPU fundamentals。这里是一个非常简化的 GPU 视图。GPU 内部有一种叫 SM，streaming multiprocessor 的东西。它和 CPU core 很像，负责执行算术、逻辑运算，有时也做 matrix multiplication。它们就是 GPU 里真正出算力的地方。

Stuart Sul：所有的 FLOPs、所有你想要的 compute，都在这些 SM 上。所以 GPU 里自然会有很多 SM。Blackwell GPU 上有 148 个 SM，Hopper 上有 132 个。为了让这些 SM 做计算，你需要把数据喂给它们，所以 GPU 还有 memory system、crossbar、L2 cache、HBM，HBM 是现代 GPU 的主内存。你还需要一个能发起操作的东西，所以 CPU 和 GPU 之间通过 PCIe 连接。data center server 往往要插很多 GPU，所以会有多张 GPU 共存。早年如果这些 GPU 之间想通信，数据必须经过 PCIe。但 PCIe 是共享资源，会拥塞，也相对慢。所以我们有了 NVLink，它允许 GPU 之间直接通信。

Stuart Sul：而这基本就是 NVIDIA DGX 机器的核心意义。DGX 已经存在很久了，在生产级 AI training 和 inference 里用得非常广。它本质上是一组 GPU，各自通过 PCIe 连到 CPU 或 host，同时所有 GPU 又通过 NVLink 互联。NVIDIA 更新的 NVL72 其实也很类似，就是 72 张 GPU 通过 NVLink 组成一个整体。从 programmer 的角度看，你对 NVL 和 NVL72 本质上了解这些就够了。所以当你听到有人说他在优化 GPU kernel，他通常真正想表达的是，他想让所有 SM 一直保持繁忙。因为正如我刚才说的，SM 里装着所有 FLOPs，装着所有 compute。你希望这些宝贵的 FLOPs 时刻都在工作。single-GPU kernel 的典型做法，是把 memory load 和 write 做成 pipeline，把 SM 上的 compute 和从 HBM 拉到 SM 的 memory operation overlap 起来。这样当前一轮计算结束时，下一轮需要的数据已经待在 SM 上，随时可用。

Stuart Sul：对于 multi-GPU kernel，道理是一样的，只不过 overlap 的对象从 memory operation 变成了和其他 GPU 的 communication。这样当当前这轮计算结束时，下一轮计算所需的数据就已经从远端 GPU 的 HBM 拉到了本地。回到 PK。PK 建立在我们识别出来的三类关键 trade-off 上。第一类是 transfer mechanism。事实证明，通过 NVLink 发数据其实有三种方式。第一种是 copy engine，第二种是 tensor memory accelerator，也就是 TMA，第三种是直接用 register instruction，比如 LD 或 SD。每种方式都有自己的优缺点，如果你天真地只依赖其中一种，会把很多性能留在桌上。举个例子，copy engine 很理想，因为它是 GPU 上独立的 DMA 模块，在 GPU 之间搬运数据时根本不需要占用 SM。

Stuart Sul：但问题是，copy engine 想真正把 NVLink 吃满，需要非常大的 message size，也就是单次传输的数据块必须够大。可在 fine-grained communication 里，你经常只传几 KB 数据，所以 copy engine 反而不是最佳选择。TMA 不一样，它在不同 message size 下都能维持相当不错的吞吐，而且占用的 SM 还很少。我们在 Blackwell 上观察到，大概只用 148 个 SM 里的 15 个左右，TMA 就足以把 NVLink 打满。但 TMA 也有缺点，它无法利用我们前面提到的那些 in-network compute 特性。如果你想用这些特性，就得改用 register instruction。可 register instruction 也很痛苦，因为你必须考虑 coalescing、register pressure 等一整套低层问题。抛开技术细节不谈，我真正想传达的是，为特定 workload 选对 transfer mechanism，非常重要。

Stuart Sul：比如对一种常见的 multi-GPU operator，像 All Gather JAM，我们发现 TMA 的效果就相当理想，而过去很多方案只是直接依赖 copy engine。第二类 trade-off，是如何调度 inter-GPU communication 与 intra-GPU work。大体上有两种策略，intra-SM overlapping 和 inter-SM overlapping。所谓 intra-SM overlapping，就是在同一个 SM 内，一部分 thread 负责 compute 或 memory work，另一部分 thread 负责 communication，这也叫 warp specialization。所谓 inter-SM overlapping，就是专门拿出一部分 SM 只做 communication，剩下的 SM 做 computation。它们同样各有优劣。比如 inter-SM overlapping，正如图里能看出来的，它会浪费 compute，因为专门拿来做 communication 的那些 SM 上的 FLOPs 根本没被用起来。

Stuart Sul：而且由于 communication 和 computation 分布在不同的 SM 上，它们之间要互相通知完成状态，就必须绕一圈 through memory system、L2 cache、HBM。但 intra-SM overlapping 也有严格前提，那就是 computation 和 communication 必须对齐，必须作用在同一份数据上。否则你很快就会把 register 和片上 shared memory 用爆，根本没法做出有意义的 computation。你还必须考虑 local prefetching。再看图里的红箭头，它表示访问远端 GPU HBM 时走过的数据路径。你会发现远端 HBM 的数据会经过 L2 cache，但本地 GPU 的访问路径反而不经过 L2。这意味着如果你反复访问同一份数据，比如 attention kernel 里的 KV cache，那么缓存其实只存在远端 GPU 那一侧。

Stuart Sul：所以理想情况是先把这些数据 prefetch 过来，stage 到本地 HBM，再开始主要计算。要做到这件事，你就必须依赖 inter-SM overlapping 这种调度策略。所以，再强调一次，选对策略对性能非常重要。对于 JAM reduced scatter，我们发现 intra-SM 最优；而对于 JAM all reduce，我们发现另一种不同的 overlap 组织会更合适。第三类也是最后一类 trade-off，是 design overhead。这里我说的 design overhead，指的是 networking library 为了降低复杂度而引入的那些设计选择，但这些选择会带来性能损失。举个例子，NCCL 的默认模式会强制使用 intermediate buffer，这会在 sender 和 receiver 之间额外多出一次数据搬运。对于 fine-grained communication，这种开销会越积越大。把这部分剥掉之后，像 All-Reduce 这种再基础不过的操作，居然也能提速到 80%。

Stuart Sul：这说明一件事，现代 GPU networking library 应该显式暴露这些关键的性能控制项，而不是把它们封装起来藏掉。我想我今天真正想传达的主要观点，到这里基本都讲完了。接下来我会很快很简短地讲一下 ParallelKittens framework。正如刚才说的，ParallelKittens 是建立在我们讨论的这些 trade-off 和原则上的。它是一组非常有主见的 CUDA programming primitive，扩展自我们之前做 single-GPU kernel 的工作 ThunderKittens。

Stuart Sul：像前面说的，现代 GPU 有一整套 memory hierarchy，从 registers、shared memory、L2 cache 一直到 global memory。你也可以把远端 GPU 的 HBM 当作 memory hierarchy 里的另一层，也就是 peer global memory。PK 为这条 memory hierarchy 的每一层都提供了对应的数据结构。比如 registers 用 RT，shared memory 用 ST，L2Cache 在 GPU 上不可编程，global memory 用 GL，peer global memory 用 PGL。PK 提供的是一系列 communication primitive，它们接收这些数据结构，并在其上执行对应操作，同时为不同功能自动选用最合适的 transfer mechanism。它还提供了一个 program template，里面有四类 worker，loader、consumer、communicator 和 store，用来支持不同的 scheduling strategy。更多细节还是请去看 paper 和 GitHub repo。为了验证 PK 的效果，我们把它和多个主流 baseline 做了比较，覆盖了 data、tensor、sequence、expert parallelism，以及像 All-Reduce 这样的纯 collective communication。

Stuart Sul：我们发现，只需要大约 50 到 100 行 device code，PK 就能超过或者打平那些往往需要几百到上千行代码的 hand-optimized kernel。让我特别骄傲的是它的 adoption。PK 已经被一些大型 AI 公司采用了。比如 Cursor 正在用它，在数万张 Blackwell GPU 上训练 Composer。Together AI 也在用它优化自己的 inference workload。好，这就是我的分享。我希望大家今天对 multi-GPU kernel 和 GPU networking 至少形成了一些新的认识。如果你们在做 ML systems 和 efficiency，我希望你们真的去看看 PK，试一试它。非常感谢大家。

Francois：好，下一位是 Jon。

Jon Saad-Falcon：太好了。大家好，感谢你们来。今天我要讲的是我们最近的一篇 paper，题目叫 Intelligence per Watt: Measuring the Intelligence Efficiency of Local and Cloud AI。这是我和实验室同事 Avanika、Orion 以及我们的导师 John Hennessy、Azalia Mirhoseini 和 Chris Re 一起完成的工作。先给大家定个位。我和 Avanika 私下里很喜欢把当前 LMs 与 hardware 的阶段称为 mainframe era，对应的是上世纪五六十年代的 mainframe 时代。当时 IBM 的机器能占满整个房间，甚至整层楼。就是这种机器把我们送上了月球，也是最早面向企业开放的商业计算机。今天的数据中心其实还有点像那样的结构，只不过仓库里塞满的是 Google 的 TPU 或 NVIDIA 的 GPU。

Jon Saad-Falcon：这些系统既承担 training，也承担 inference。从需求增长的角度看，这很合理，因为需求在爆炸式增加，我们必须尽快扩展算力，把更多计算机铺出去。但与此同时，这种需求强度也是很久没见过的，也许只有当年美国修横贯大陆铁路时能类比。今天我们每年投入相当于 GDP 的 2% 到 3%，去建设大约 250 gigawatt 的新 data center，这又意味着新的电力来源、新的 GPU、新的土地、新的水资源，才能同时满足 training 和 inference 的需求。可即便需求增长这么快，很多请求其实根本不需要 frontier-level intelligence。每个人每天都有自己的一堆 LM workload。至少对我个人来说，大部分事情并不需要最前沿的 coding model 或数学 model。

Jon Saad-Falcon：很多事情只是翻不同 data set、做些 plumbing、整理文件夹、生成 unit test。也就是说，尽管 frontier-level intelligence 确实很重要，而且我们也必须继续往前推，但今天绝大多数 LM traffic，其实可以由更小的、本地运行的 open source LMs 来处理。所以我们的判断是，就像计算历史上从占满机房的 IBM mainframe，逐渐过渡到七八十年代 Apple 和 HP 的个人电脑一样，今天的 hardware 也会出现类似迁移。我们会从“每个请求都要走 NVIDIA GPU 或 Google TPU”的格局，慢慢转向更多依赖本地设备，包括 Mac，以及 NVIDIA 和 AMD 的个人 consumer GPU，这些设备就放在个人 workstation 和 laptop 上。

Jon Saad-Falcon：推动这个变化的主要有两个趋势。第一，小模型正在一年比一年更强。我们已经看到不少能力相当不错的 open source 小模型，而且这个趋势还在加速。第二，本地 accelerator 本身也在快速变强。Apple、NVIDIA、AMD 都在推新的 accelerator。我们看到这些 GPU 已经拥有足够多的 memory，能够容纳一些更大的 open source LMs。我们认为这条趋势还会继续。在这项研究里，我们想问的是，本地 open source AI inference，到底能在把 inference demand 从当前高度集中于 cloud 的状态，重新分配到更分布式的 inference 结构里，扮演什么角色。为了框定这个问题，我们提出了 intelligence per watt 这个指标，分别对应它的分子和分母。

Jon Saad-Falcon：所谓 intelligence，我们本质上指的是 capability。它会随着你关心的任务不同而变化。最终我们关心的是 chat、reasoning、agentic task、coding task，总之就是人们今天真正拿 LMs 来做的那些事情。分母则是 efficiency，而且不是那种“每个参数、每比特训练信息产出多少智能”的抽象效率。我们说的是在各种 accelerator 上、面向各种 workload 运行时，真实需要付出的 compute 和 energy。也就是，为了交付这份 intelligence，实际消耗了多少运行功率、多少 wattage。这项研究里，我们想做一个足够宽的 sweep，先看清趋势。我们测试了 20 多种 state-of-the-art 本地模型，覆盖 Llama、GPT-OSS、Qwen、IBM Granite，参数规模从 10 亿到 2000 亿不等，既有 dense，也有 MoE。

Jon Saad-Falcon：同时，我们也测试了过去两到三年里的 state-of-the-art accelerator，尤其是本地 accelerator，覆盖 Apple、NVIDIA、AMD、SambaNova，目的就是看清 intelligence per watt 和 intelligence per joule 的上界到底在哪里。我们把这些测试放在所有人真正关心的 workload 上，包括 chat、reasoning、agentic、coding，总之今天这些模型真正在做的事，我们都想考察。我们关心的不只是 accuracy，还关心 latency、energy、power、compute，我们就是想做一个广泛 sweep，看看到底什么组合才合理。结果相当有说服力。我们发现很多本地模型已经相当不错，而且进步速度非常快。

Jon Saad-Falcon：多达 88.7% 的 query，其实都可以被路由到运行本地 open source AI 的本地 accelerator 上。而且这个准确率还在继续提升。仅仅过去两年里，intelligence delivered per watt 就提升了大约 3 倍。更重要的是，这是叠加发生的，本地模型更强了，本地 accelerator 也更强了，两边互相强化。如果你看的是 intelligence per joule，而不是 intelligence per watt，也就是把整个 end-to-end workload 的总能耗算进去，这种进步会更夸张。仅仅过去两年，或者更准确说大约 16 个月里，实际 delivered per joule 的 intelligence 提升了约 18 倍。

Jon Saad-Falcon：这种改进主要来自更好的 accelerator，比如 consumer GPU 上装了更多 memory，像 Apple M4 Max、NVIDIA 的 DGX Spark。与此同时，也来自更好的 quantization technique，它们能更高效地利用现有 compute，还有更长的 pre-training、更充分的 post-training，以及更复杂的模型改进技术。那么这些结果对我们重新分配 inference 的思路意味着什么？它意味着，如果路由做得足够理想，今天就有 80% 到 90% 的 query 可以被分流到本地 accelerator 和本地 open source LMs 上。这就意味着 energy savings、compute savings，以及 cost savings。即使 router 不是完美的，也仍然可能节省 50% 到 70% 的能耗、算力和美元成本。

Jon Saad-Falcon：这会从根本上改变我们对 inference 扩张方式的经济学理解，也会改变我们如何看待新 data center、新硬件产线和新模型的投资决策。当然，本地 accelerator 也不是完美的。data center compute 的一个优势在于，你可以做各种复杂的 kernel、batching 和 quantization 技术，把投入 amortize 到更多用户和 query 上。Apple M4 Max 和 NVIDIA B200 相比，在 intelligence per watt 和 intelligence per joule 上依然落后。还有一些更专门为 inference 做的 accelerator，比如 SambaNova SN40L，consumer accelerator 在它们面前差距就更大了。所以从投资角度看，让 consumer accelerator 变得越来越强，本身就是一个机会。

Jon Saad-Falcon：所以我们很期待看看这些公司接下来会发布什么。我还想感谢这项研究里的合作伙伴，来自 NVIDIA、Google、Apple、AMD、OpenRouter 和 SambaNova。没有他们提供的资源和指导，这项研究做不出来。那接下来我们在看什么？我个人最兴奋的一点，是 inference engine 会如何适应这种新动态，也就是同时利用本地资源和云端资源。与此同时，我觉得还有巨大的机会，去设计专门面向 energy-efficient inference 的 model architecture 和 kernel。这有可能推动某种 accelerator architecture 的 co-design，进一步加速这条趋势。在分析层面上，我也很想把 intelligence per watt 继续拆解开来，看它在不同 task、不同 hardware、不同 deployment setting 下具体长什么样，包括 inference engine、kernel，以及硬件上的 compute 和 memory 细节。

Jon Saad-Falcon：最后，虽然这篇工作重点是 intelligence per watt，但我觉得更重要的是，这些 intelligence 到底有没有被用在真正有意义的地方，也就是去完成那些人类本来得自己做、而且确实在乎的工作。如何量化它对 GDP、对工资的影响，这是我们很快也会发布的另一项有趣工作。如果大家有问题，欢迎随时联系我。邮件、Twitter、GitHub 都可以。如果你也对这些方向兴奋，我很愿意聊。我们还有一个 follow-up 项目叫 OpenJarvis，目标是把这些 insight operationalize，让整套 personal AI coding stack 可以直接 on-device 运行。这样你就不需要再为 Claude 或 OpenAI 的 LMs 持续付费了，可以直接在自己的 laptop 或 workstation 上跑。

Jon Saad-Falcon：如果你对这个也感兴趣，欢迎联系我。非常感谢。

Francois：好，下一位是 Mark。

Mark Saroufim：好的，大家能听清吗？Francois，非常感谢你邀请我。我从 Stuart 那个非常精彩的分享里，听到了很多围绕“AI 到底有多擅长写 kernel”的问题。今天我的分享基本就围绕这个主题展开，而且会讲得很深。我过去大概五年都在做 systems，也一直在做 PyTorch，还做了很多 custom kernel，这也是我联合创办 GPU MODE 时的一部分核心工作。到 Core Automation 之后，这依然是我的重点方向之一。我希望今天能同时给大家一个 research 视角和一个 commercial 视角。既然这是 YC Paper Club，我今天的主要结论来自两篇 paper。第一篇是 KernelBot，它本质上是个竞技平台，你可以把它理解成 GPU programmer 的 LeetCode。

Mark Saroufim：第二篇叫 Kernel Guard，是我们用来检测作弊的平台。我等会儿会解释，为什么这两个问题本质上是同一个问题。作为一个 systems researcher，我已经逐渐接受一个现实，就是我的意见的重要性通常不如 AI researcher。我真正想要的是，大家拿同一份数据，一遍又一遍地跑 matmul，然后给我一条干净的 GPU 指标就行了。但我的研究同事们总想要 autoregressive 的东西，他们想要一大堆 tiny kernel、dynamic control flow、各种 sparsity，还要 print statement。所有这些都很烦，他们真该停手。好了，谢谢。遗憾的是，我没法真的阻止他们，所以只能跟这群人合作，给他们造工具。

Mark Saroufim：我们通常提供给他们的是 programming language。一个很好的例子是数学。你可能不会把它当作 programming language，但它其实就是。数学之所以漂亮，是因为它具备极强的 forward compatibility。比如 matrix multiplication 的 API，两百五十年来都没变过，还是 AB 等于 C。也许你会加一点 args 或 kwargs，但 API 核心没变。PyTorch 很像这个思路。PyTorch 对外暴露出来的 printed API，本质上是像 MM、Softmax、QRD comp 这样的 op，这些 op 在时间面前都能活下来。最终它们会 dispatch 到一个个具体的 CUDA kernel，而这些 kernel 在现代 hardware 上未必都足够快，所以我们才需要像 Triton 这样的 programming language。Triton 是 tile-based、Pythonic、速度也不错，大概两年半前直接席卷了世界。

Mark Saroufim：但最近，尤其是从 Blackwell 开始，大家越来越多地说，Triton 的 programming model 限制太强了，不足以写出 state-of-the-art kernel。所以人们开始对 ThunderKittens 这类语言感兴趣，Stuart 也在维护它。还有 CUTLASS 和 CuTe DSL，这是 NVIDIA 用来写最先进 matmul 的闭源库。再下面是 CUDA，它是更通用的 programming model，不仅能写 matmul，而是 thread-based 的，对做局部精细优化特别有用，但写起来非常繁琐。再往最底层，是 hardcore 选手会直接写 PTX 或 inline SASS。通常这里没有 BC guarantee。倒不是说做不到，而是你一换架构，代码很可能直接失效。这就既难受又费时间。这些库的 maintainer 和用户往往都对“性能和生产力之间哪种平衡才最好”有非常强烈的观点。

Mark Saroufim：其实没有什么错误观点，关键在于你得知道自己落在这条光谱的哪个位置，你到底有多在意 performance。通常你能慢慢摸清自己的立场。但如果我们试着把这件事 benchmark 一下，做个 leaderboard 会怎样？假设我们给定一个问题，比如 QRD composition problem，我一会儿解释这是什么。目标是让大家为这个问题提交 kernel。很酷的一点是，我在 GPU MODE 里一直在推进一个叫 KernelBot 的平台，大家可以往里提交解法，而且想用什么库都行。然后我们就能做数据分析，看看哪些库最受欢迎，人们真正会用什么。至少对那类只追求 state-of-the-art perf 的人群来说，据我观察，他们最偏爱的仍然是 CUDA。

Mark Saroufim：只有在我们做了很多 GEM 相关题目时，大家才特别爱用 CuTe DSL。Triton 经常会出现在前五到前十里，但很少能挤进前二。大体上你可以这么理解这个格局。不过真正好笑的是，我今年整年都在研究这些“银河脑”级别的 programming language 和 compiler。结果从今年一月开始，我们办了一个特别火、参与度很高的 NVFP4 kernel 竞赛，结果很多从来没写过 GPU kernel 的人，居然做出了非常有竞争力的结果，甚至能进前四、前五。比如这个叫 Shirga 的人，是中国的一位研究生，联系我说：“我从没写过 GPU code，连 CUDA 书都没翻过，一切都是 LLM 生成的，但我现在排第四。” 我那条推文甚至上了 r/Singularity，还挺离谱。

Mark Saroufim：这是我第一次在那个版面出镜，所以我去看了。然后我就觉得，这事有点怪。有人跟我说，这个人本来就很聪明，是 researcher，当然搞得懂，数值和计算功底也强。结果接着我又看到 Clark 的另一条 tweet，他是个高中老师，却告诉我：“我刚写了我的第一个 dual GEM problem。” 我当时的反应是，啊？通常不是应该先学 vector sum、vector mean，再学 MatMul，然后再慢慢往后走吗？结果这些人直接 YOLO 上来，就能做出挺有竞争力的结果。他们看着图表，玩得还很开心。无论从 educator 还是 library builder 的角度看，这都非常反常。即便我自己就在这个领域里，我也没想到这些结果会来得这么快。

Mark Saroufim：所以我想简单讲讲，我们通常是怎么评估 AI 写这些 kernel 的能力的。这套框架很多借鉴了 Simon Guo 和 Anne Ouyang 在 KernelBench 上的工作。一般流程是这样的：你先有一个 PyTorch reference，因为社区普遍认为 PyTorch 在 correctness 上通常优于多数库，尽管 performance 不一定最好。然后你随机采样一些输入，再准备一个你喜欢的 kernel DSL 写出来的参考提交。接着跑一个 `eval.py`，把同样的输入分别送进两边，看看输出是否等价。你检查 correctness、检查 performance，最后把结果排到 leaderboard 上。很好，这就是现在大多数 eval 的基本框架。如果你是做 AI 的，你可能会说：“这不是很简单吗？verifiable rewards 嘛。”

Mark Saroufim：可每次有人这样跟我说，我都只能“嗯，好吧”。我其实不同意。这里面有一个很隐蔽的细节，我们需要认真拆开说。我举个例子。假如你从来没写过 CUDA kernel，今天我现在就带你写一个。我们要写世界上最快的 vector mean kernel。给定一个一维 vector，我们就求它的平均值。很好。我们从长度一百万的 vector 里采样一堆随机输入，然后算这个 vector 的 mean。这个输出就是我们的 reference。接下来我们的 kernel 要做的，就是自己写一个求均值的 kernel。

Mark Saroufim：这里的坑是，`torch.randn` 默认采样的是均值为 0、方差为 1 的分布。所以世界上最快的 vector mean kernel，其实就是直接返回 0。这甚至快过光速。多么美妙的算法。NVIDIA，我愿意被你们雇走。人生一片光明。但这不是孤立案例。我读过大量 reward hack。很常见的一种是，AI 会把输出 cache 住，然后在之后重用，伪装成等价计算。于是你会想，那我禁掉它。比如一种版本是，它在 Python 里用 data pointer 判断之前传入的数据，然后直接返回旧结果。所以你就在 eval suite 里写，不能用 data pointer。可 Python 是门很有意思的语言。

Mark Saroufim：你不一定非得写那个点号访问，你也可以用 `getattr` 去拿 data pointer。于是你再进一步，禁掉字符串 `data pointer`。然后我还见过 AI 把 `data pointer` 拆成两个字符片段，在不同的行里 append 上去，这样你用 regex 都抓不到。那如果你干脆彻底禁 data pointer 呢？大家又会不高兴。然后它们还能直接改用 `id`。我想表达的是，这就是一个鸡生蛋、蛋生鸡的问题，会一直发生。根本原因是 Python 是动态语言，用它做这种事情天生就很糟。这里我最喜欢的一个例子，来自 Natalia，当时她还是 Stanford 的学生。她给我展示了我见过最疯狂的 reward hack。它的本质是，AI 发现我们在 correctness suite 里会检查 15 次 correctness，然后才去做 performance testing。

Mark Saroufim：但在 performance testing 阶段，我们不会再重新做 correctness 检查。所以 AI 的做法是，它会数自己已经经历了多少次 correctness test。前 15 次它给我们一个正确但很慢的 kernel；等到了 performance 测试阶段，它就改成给一个错误的 kernel，但把所有结果 batch 到一起，让整个 benchmark 看起来非常漂亮。结果发现，这种 reward hack 现实里竟然也有先例，就是 Volkswagen 的 Dieselgate。车在检测到自己正在接受排放测试时，会把排放降到原来的四十分之一；但现实驾驶里，它照旧大量排放，而且那套把戏一度还真成功了。这个类比是 Twitter 上的 Tinderization 告诉我的。那段时间我正处在一个非常惨烈的 on-call 里，一直在看各种 reward hack。总有人来告诉我：“Mark，你的 eval 太烂了。”

Mark Saroufim：他们会问，为什么你们检测不出来这些问题？可问题是，这些手法太多了，而且每次都不同，根本不容易把它们写成一套规则。所以我想，如果大部分人提交的解法都是 AI 生成的，那我干脆也用 AI 来审查。这个方法的核心思路是，人类看到一个特别快的提交，就先做 audit，把它标记成 reward hack，然后把这个案例喂给 AI 系统，再让 AI 系统综合出一个基于 Regex 的 detector。你把这个 Regex 部署出去，就能抓住很多作弊。之后新花样出来，再拿新例子去训模型。这套主意来自 GPU MODE 的 maintainer 之一 Sinatra。当然，如果我们有更多资金，直接上一个模型更自然，但眼下 Regex 方案足够快、足够灵巧。

Mark Saroufim：我还想讲一个最近遇到的有意思问题。我的同事 Rohan 非常痴迷一个 optimizer，叫 Shampoo。你们可能在 Twitter 上见过，他还和 Keller Jordan 就“Muon 到底算不算 Shampoo”吵得很激烈。其中一个原因是，Shampoo 之所以部署得不够广，是因为它依赖 QR factorization，而这个算法在 PyTorch 里非常慢。我一看就觉得，这是个把老算法变现的好机会。QR decomposition 的基本思路是，你有一个矩阵 A，想把它分解成两个矩阵。一个是 Q，是正交矩阵，也就是转置等于逆；另一个是上三角矩阵。这个东西对估计空间曲率很有用，而曲率估计对 second-order method 很重要。

Mark Saroufim：在 PyTorch 里调用这个 API，本质上就是 CPU 下调用 LAPACK，GPU 下调用 cuSolver。我觉得这两个库都需要更多关爱，需要更多 maintainer。它们正在被 deep learning op 淹没。很酷的一点是，我们把这个问题变成了社区竞赛题，借助人类和 AI 一起做了一次大范围搜索，最后拿到了一个快 60 倍的 kernel，而且它不会产生 NaN，这很关键，所以它真的可以被拿去跑真实 training。更奇怪的是，这些 kernel 都非常长。比如平均提交大概有 15000 行代码，因为它是按 shape 定制一个 kernel。没有人类会这么干，因为人类总会被美感、简洁和优雅所束缚。

Mark Saroufim：AI 看起来根本不在乎这些。它们的做法通常是实现一个 dispatcher：如果 shape 很小，也许走 shared memory QR；如果很大，就走 global memory QR。它还可以给不同 shape 配不同 schedule。对于 benchmark 里常测的 shape，我用更高精度；不常测的 shape，我就偷鸡，用低精度把 benchmark hardness 混过去。结果就是，我们最后面对的是成千上万份提交，每一份都又是成千上万行代码，加起来就是数百万 token。我们看着这些东西，就会想，能不能从中提炼出一个真正优雅、真正漂亮的 kernel？

Mark Saroufim：答案是，并不明显。我自己还没想出来，这现在仍然是个 open problem。不过我们确实非常仔细地读了速度最快的三个 kernel。我和一位同事 Marcus，也就是 FA4 的合作者之一，试图向大家解释“这些 kernel 到底该怎么写”。最后我们的解释是这样的：第一步，理解 GPU 的 memory hierarchy。第二步，写一个很快的 kernel。听起来有点刻薄，但它确实没错。也许不太 actionable，但方向上就是这么回事。我最后还想讲一点，我们的 leaderboard 之所以能持续有效，很大程度上正是因为人们越激烈竞争，就越能把 reward hack 揪出来。反过来，这又会让 eval 变得更 robust。

Mark Saroufim：对我来说，这个飞轮很像 PyTorch 的成长过程。很多人说 PyTorch 更正确，可 PyTorch 不是天生就正确的。它是被一点一点打磨得越来越正确的。最初它某种意义上也是 vibecoded 的，因为它只是个把 Torch 移植到 Python 的 POC，本质上就是从 LuaTorch 过渡到 PyTorch ops。而这整条链条之所以可验证，是因为 PyTorch 能对应回 LuaTorch，再回到 NumPy，再回到 LAPACK，再回到 Fortran。我们有这条 correctness chain。

Mark Saroufim：我们和很多 researcher 合作，他们告诉我们想要什么，指出 bug，我们再修。结果发现，如果你把这个过程持续做九年，并且始终维持强 BC numerics guarantee，你就会得到一个非常受欢迎的库。这是个非常好的过程。我还不知道仅靠 AI 要怎么走完这条路，但我怀疑，我们现在用 KernelGarden 和 KernelBot 采取的这种 adversarial 做法，其实已经给了我们一个很好的提示，告诉我们这类问题该怎么解决。所以，谢谢大家。如果你对这些问题感兴趣，欢迎在 Twitter 上找我，或者发邮件到 `hello@coreauto.com`。我可以和你聊聊，我认为哪些 open problem 很重要，但现在得到的关注远远不够，而且它们也绝不只是“让 Codex 去随便煮一煮”那么简单。

Mark Saroufim：简单说，Kernel 这一波人非常擅长放大系统中的 Amdahl’s law 效应。无论是 compilation time，还是任何涉及等待的环节，他们都能把瓶颈全都挖出来。所以我特别关心，有没有办法把 compilation 加快。更快的 JIT、更高效的 Triton 和 CuTe DSL 的 AOT packaging，这些我都非常感兴趣。GPU 的 CPU simulator 现在也做得很不错。很多人一直开玩笑说 Fable 在这类工作上表现离谱地好。我特别希望看到这类工作，因为如果能大量启动 CPU simulator，你做 rollout 时就不需要那么多 GPU。类似地，如果你想把这些 kernel 部署进一个真实 inference engine，问题又来了。比如你直接拿 SGLang 或 vLLM 去加载 DeepSeek，那么第一次 inference 前，可能要等 30 分钟。这对 AI system 来说实在糟透了。

Mark Saroufim：我也非常想听听大家对“怎么更稳健地验证 kernel correctness”的看法。我们今天的做法基本就是喂随机输入。有人告诉我 formal verification 才是出路。我很愿意听更多思路，前提是成本别高到等同于再训一个模型，那太贵了。我也很好奇，在“逐行读代码”与“疯狂做测试”之间，有没有中间道路。现在这两种答案都不让我满意，所以如果大家有更折中的想法，我很想听。最后，还有人开玩笑说 GPU MODE 已经变成了 pay-to-win。我觉得这说法其实有点道理，因为现在 test-time scaling 已经按天来算，甚至要跑一到两周。既然我们知道给足时间可以把问题做出来，那有没有办法把这个过程压缩成几个小时，或者几天？

Mark Saroufim：如果你有想法，请一定联系我。谢谢。

Francois：好，下一位，Misha。谢谢。

Misha Smelyanskiy：大家能听见吗？好。大家好，我是 Misha。差不多一个月前，我加入了一家叫 Marlo 的 startup。这家公司专注于构建 workload-optimized 的 heterogeneous infrastructure。它的基本前提是，inference 本身就是一种高度 heterogeneous 的 workload。inference 的不同阶段，对 compute、network、storage 和 memory bandwidth 的压力完全不同。所以从这个角度看，用不同的 hardware、不同的 system 去分别承载不同阶段，再做协同设计，是非常合理的。今天我会讲几个例子。先声明一下，我今天不会展示具体数据，但我会尝试从 first principles 出发，把这些观点推导出来。你们也完全可以反驳我。我非常欢迎争论。这张图大概大家都很熟悉，它描述的是一个 inference request 的 life cycle。

Misha Smelyanskiy：基本流程是这样的：用户先输入 prompt；然后有一个 CPU system 负责 orchestrate、schedule 和 batching；接着系统会去查 prefix cache，prompt 里凡是没被 cache 覆盖到的部分，就进入 prefill。prefill 通常非常 compute-intensive，所以一般跑在 accelerator 上。与此同时，还会创建 KV cache，而 KV cache 可能牵涉 CPU memory 或其他 accelerator 的 memory，也可能跨网络搬运。再往后是 autoregressive decode，每个 stream 一次只生成一个 token，这个阶段既非常 memory-intensive，也非常 latency-sensitive。最后再产出结果。中间往往还会掺一个 speculative decode，它会预先猜下一批 token，然后再由主模型去验证。核心点就在于，不同阶段会触发完全不同的 hardware。

Misha Smelyanskiy：瓶颈是不断移动的，不存在单一瓶颈。抱歉，这页 slide 看起来有点挤，但我还是觉得必须放进来。我想先聊一聊 prefill 和 decode 的基本特征。

Misha Smelyanskiy：这里最重要的指标叫 arithmetic intensity。它是你的基础算法所执行的 FLOPs 数量，与它从 memory 搬运的数据量之间的比值。如果这个比值大于对应 machine ratio，也就是机器峰值 FLOPs 与峰值 memory bandwidth 的比值，那么你的 kernel 或算法就是 compute-bound；反之如果更低，它就是 memory-bandwidth-bound。这张图是 roofline，我相信很多人都很熟。它最初其实是 2012 或 2013 年左右 Berkeley 的 Sam Williams 为 HPC 建立的，用来刻画不同 HPC application 的行为。它的横轴是 arithmetic intensity，而对于给定 intensity，纵轴表示你能实现多少 FLOPs。

Misha Smelyanskiy：如果 arithmetic intensity 小于 machine ratio，你就落在 memory-bandwidth-bound 区间；如果更高，就落在 compute-bound 区间。当然现实世界要复杂得多，但这个模型给了你一个一阶近似。你如果去看 prefill 和 decode，会发现即便是 attention、MHA kernel、MLP，它们的 arithmetic intensity 也都不一样。prefill 一般非常 compute-bound，因为你基本上是在做 attention，你每拿到一批 token，就能对其做很多工作。weight 只需要 fetch 一次，就能反复作用。MLP 的 intensity 甚至还更高，因为它更容易 batch 化，所以通常也很 compute-bound。decode 不一样。decode 是一次只处理一个 token，是一个自回归过程。

Misha Smelyanskiy：所以 attention 在 decode 里就会变得非常糟糕。你为了处理每一个 token，都要重新去 fetch weight，效率非常低。MLP 稍微好一些，因为多少还能做点 batch，但现实里 batch 通常也不会很大。现代 accelerator 的 compute 太强了，所以哪怕 batch 稍大一点，你最终往往还是会被 bandwidth 限住。核心点是，即便都在 prefill 和 decode 这个框架内，不同 kernel 对系统施压的方式也高度多样。你再把视角抬高一点，这页 slide 展示了不同的使用空间，你会看到 inference 覆盖的是一个极其宽广的 workload 空间。每个圆代表一种 use case，圆越大，表示 concurrency 越高。每一种 use case 里，我们都在展示你把多少时间花在 prefill 上，多少时间花在 decode 上。

Misha Smelyanskiy：对于 interactive chat，你输入一个 prompt，再得到一个 answer。大体上可能是 30/70，或者接近五五开的 prefill/decode 比例，而且这种场景对 latency 极其敏感。对于长上下文 query，大部分时间其实都花在 prefill 上，然后 decode 一下就结束，所以那颗蓝点后面才拖着一条很长的蓝线。对 coding agent 来说，latency 往往也仍然很严格。至于那种 long-running agent，输入长、输出也长，比如你把 Claude 扔在那里一晚上，让它帮你构建整个 codebase，那么 concurrency 可能也很高，但 latency 约束就会松很多。我不想把这个点说得太久，核心就是：inference 覆盖的是一个极大的 workload 空间。

Misha Smelyanskiy：在继续之前，我想插一小段，讲讲 SRAM machine。过去十年里，这类机器越来越热门。SRAM machine 好在哪里？比如今天你想在 GPU 上做 GEMM，如果 weight 很大，大到超过片上 cache 的容量，那你就必须去 memory，也就是去 HBM，把它通过 package 间互联拉回 GPU。如果这个 weight matrix 很大，而且你又得对每个 token 都重复这件事，那效率就很差。SRAM machine 的思路，是把整个 weight matrix 都放进片上的 SRAM，所以你得到的 bandwidth 会高得多，因为一切都在 chip 内部。你可以按 cycle 级别访问字节，chip interconnect 也很快，不同单元之间通信只需要几个 cycle。

Misha Smelyanskiy：所以一切都留在 die 上，效率非常高。我把这类东西叫 GMV，也就是 matrix-vector multiplication accelerator，它们恰好非常适合 decode，因为 decode 极度 bandwidth-bound。它们提供明显更高的 bandwidth 和更低的 latency，但这里有个代价：既然一切都在 die 上，你能塞进去的 transistor 数量就有理论上限，也就意味着容量有上限。看看不同 SRAM accelerator，你会发现它们的 memory 从几百 MB 到几十 GB 不等，但也就到这里了。

Misha Smelyanskiy：它们能更快地搬这些数据。所以问题就变成，你怎么利用它们？在模型已经被切分、shard 到多个 chip 上之后，怎么还能保住这些优势？而且你要怎么刻画这些优势？接下来我想通过几个例子来说明 specialization 怎么发挥作用。它不一定非得是 GPU 或 SRAM machine，我只是用几个系统例子来说明。大家都很熟 prefill 和 decode disaggregation，也就是把它们拆开独立扩展，去掉共享瓶颈。那你可以继续问：如果不是把 prefill 和 decode 仅仅拆到两个实例上，而是把 decode 放到完全不同的一类系统上，会怎么样？假设 system A 负责 prefill。

Misha Smelyanskiy：system B 负责 decode。那么什么时候这是有利的？什么时候它真的有利？如果从 TCO 的角度，也就是我们常说的 tokens per second per watt 去看，只有当 system B 额外引入的功耗，被它带来的加速收益抵消掉时，这件事才值得做。你可以想象，如果 sequence 很短，大量时间都花在 prefill 上，那你的收益就不会那么明显。对于短输出长度，你甚至会出现 TCO 损失，因为你额外绑上了一整套新 hardware，却根本没怎么用上。随着输出长度增加，你花在 decode 上的时间越来越多，system B 的使用比例也越来越大，到了某个点，你就可能变成 TCO positive。另一个例子是 AFD。

Misha Smelyanskiy：正如我前面说过的，attention 部分和 MoE 部分的特性截然不同。加速这类 workload 的一种方式，就是把 attention 放在 system A 上，把 MoE 放在 system B 上。以 GPU 为例会发生什么？我们都知道 GPU 非常擅长高吞吐场景，能在高 concurrency 下跑出惊人的效果。这时候你通常是 compute-bound，latency 也可以压得不错。但一旦你为了更好的 interactivity 和更低 latency，把 concurrency 往下压，性能，尤其是 throughput，就会急剧下降。因为这时 suddenly 会出现大量更小的 kernel、大量 overhead，系统会开始受 memory bandwidth 限制，而且这些 overhead 又会让 memory bandwidth 利用率变差。这时你就会想，如果我引入一个 system B，专门擅长在 GPU interactivity 掉下去之后承接那些 bandwidth-bound、latency-bound 的 kernel，会怎样？

Misha Smelyanskiy：比如说，你可以考虑把那些讨厌的 MoE kernel offload 到 SRAM machine 上。因为一切都在 die 上，它的 latency 很低，小 batch 下表现很好，于是突然之间，你的 interactivity 就被延长了。那 TCO 呢？TCO 也许不会像高 concurrency 的 GPU 方案那样漂亮，但对于那些 interactivity 比 TCO 更重要的 use case，这可能仍然是理性的，因为 GPU 在交互性上终究会撞到极限，而这个方案能把那条生命周期往后延。所以这就是把 attention 和 MoE 分拆出去的一种思路。最后一个例子，是 speculative decoding。我想大家都知道 speculative decoding 是什么。你有一个 drafter，先对一批 token 做猜测，可能是 autoregressive 地猜，也可能像 block diffusion 那样并行猜。

Misha Smelyanskiy：然后 verifier 并行去验证它们，接受多少，就能向前快进多少。于是你可以想象，把 drafter 跑在 system B 上，对吧？verifier 还是在 system A 上。我的意思不是共享同一套硬件，而是跨不同系统去跑。对于 system A，你依然可以把 verifier 放在一套系统上、drafter 放在另一套 system A 上；而对于 system B，你甚至可以把 drafter 整体 offload 过去。如果 system B 上的 drafter 能以 system A 相同速度运行一个更大的模型，从而给出更好的 acceptance rate，那么你就真的会看到收益。你会在 latency 上看到收益，因为也许 system A 根本跑不了那么大的 drafter，或者跑起来太慢。

Misha Smelyanskiy：你还可以把多个 verifier 绑定到同一个 decoder 上，从而改善 TCO。好，总结一下。我讲的是 heterogeneous infrastructure 的端到端协同设计。这是一个彻头彻尾的 full-stack 问题，其中有很多有意思的层面。比如 data center 层面，把 heterogeneous system 放进同一个 data center，会对 power density、cooling、break and fix、日常管理带来什么影响？很多你在 homogeneous 环境里已经很难的事，在这里会更难。还有 networking 问题，虽然我今天没展开，但显而易见，只要 system A 和 system B 之间需要搬数据，networking 就会变成瓶颈。所以你到底怎么一起设计它们？接在哪？用什么 topology？才能让 latency 保持合理，而不是把全部优势都抵消掉？

Misha Smelyanskiy：还有一个显然必须具备的东西，是 performance modeling infrastructure。你需要一个非常好的 simulator，才能扫过大量 design point，找出真正合理的方案。它还必须校准得足够准，因为你最终就是靠这个东西来指导 co-design。这就是我们现在开始在做的事情。谢谢大家。

Francois：好，下一位，Brennan。

Brennan Shacklett：感谢邀请，真的很高兴来。我今天要讲的是我几年前在 Stanford 读 PhD 时做的一项工作。现在我已经离开学校，在做一个 AI 加游戏方向的 startup，但功劳该归谁归谁，这项工作完全属于 Stanford，属于 Kayvon Fatahalian 在 Stanford 的研究组。我要讲的核心想法是一个很激进的假设：如果我们把一个能模拟任意游戏的完整 game engine 全都塞到 GPU 上，并让它超高速运行，会怎样？我会讲讲我们在 Stanford 这几年的项目里，是怎么做到这件事的。

Brennan Shacklett：我们之所以关心这个，是因为游戏是很多任务非常好的学习环境。我和 roboticist、自动驾驶研究者、游戏开发者都合作过。对于以低成本方式在 simulation 中学习各种技能来说，游戏系统非常棒。但说实话，有点反直觉的是，如果你只是做最显然的事情，也就是并行跑一千份游戏引擎拷贝，那么 game engine 对吞吐导向的训练 workload 其实非常低效。因为这些拷贝会彼此争资源，你没法 amortize 成本，最后 CPU 和 GPU 两边的硬件利用率都会很糟。

Brennan Shacklett：更好的解法是我们所谓的 batch simulator。也就是只保留一个 game engine，但它会一次性并行模拟一整个 batch，可能是一千个 learning environment，并把这个大吞吐 batch 直接跑在 GPU 上。希望这个画面能正常显示。这是 OpenAI 早年 hide-and-seek environment 的可视化，是一个 multi-agent reinforcement learning environment。它能让你直观看到，我们当时在一张 GPU 上到底能塞下多少这样的 environment。最后你可以把 experience throughput 拉到每秒数百万帧，这对 RL 这种极度饥渴于数据的算法来说，非常有价值。

Brennan Shacklett：我们在构建这个系统时遇到的挑战，是现有 GPU programming framework 和你真正需要写的 gameplay logic 之间，匹配得非常差。你在做这类 environment 时，希望能很轻松地创建它们，并快速实验不同的 mechanic 和 idea。这里举个例子，是 OpenAI 那个 hide-and-seek 环境里的一段逻辑。agent 要在场景里跑来跑去，利用物体互相躲藏。它们可以锁住物体、搬动物体，等等。

Brennan Shacklett：于是你最终得到的是一大堆分支极其复杂的代码。这些内部函数里有些还会做 dynamic memory allocation。只要你稍微懂一点 GPU programming，就会知道这听起来在性能上简直是灾难消息。很有意思的是，游戏行业其实早就把 parallel CPU code 里的这个问题解决得差不多了。你平时玩的很多游戏，其 gameplay logic 其实大多跑在 CPU 上。但我们现在是把 workload 从一个 latency-sensitive 的“我要玩视频游戏，必须有极快响应”的场景，转移到了一个面向训练的 throughput-oriented 场景。所以我们几乎可以一比一地把游戏行业里的这些设计模式搬到 GPU execution 上，最后得到一个非常高效的结果。这些设计模式在游戏行业里叫 entity component system，也就是 ECS。别担心，我会解释它到底是什么。

Brennan Shacklett：我接下来就讲讲怎么把它放到 GPU 上。第一个概念是 entity，也就是 ECS 里的 E。它可能是环境里的障碍物，也可能是图里那些蓝色小人 agent。然后是 component，它表示附着在每个 entity 身上的数据。比如 position、rotation，也可以包括你的 reinforcement learning system 里的 action 和 reward。ECS 会把所有这些数据都整理成大块的内存列式存储。对于 GPU，我们就是直接把它们都放进 GPU memory，然后再把一大批 learning environment 一起 pack 进这些统一的列式存储里。你看到那一列绿色字段，表示的是每个对象对应回哪个 environment。事实证明，这种统一表结构非常强大，它让我们能在 GPU 上做面向吞吐的 dynamic memory allocation，同时对外却隐藏成一个很易用的接口，也就是“创建一个 obstacle”“创建一个 agent”这么简单。

Brennan Shacklett：这让 procedural generation 这类任务变得异常容易。你可以让每个 environment 拥有不同数量的 obstacle，而这恰好就是我刚才展示的 hide-and-seek 环境里的情况。要在 PyTorch 这种 tensor-based programming language 里做这些事情会非常难，因为那里面你面对的是固定大小的数组。ECS 的第三个概念，也就是 S，是 system。system 是那些实际在 entity，也就是表中每一行之上运行的代码，它们负责构建整套逻辑。它可以是处理来自 agent 神经网络的 action，也可以是做 collision detection，或者给 RL system 计算 reward。比如 process actions 这个 component 会声明：“我想运行在所有同时拥有 position 和 action component 的 entity 上。” 在这个例子里，agent 正好具备这两列。

Brennan Shacklett：于是这段逻辑会跑过表里的每一行，也就是我刚才那个例子。在 GPU 上，这件事其实非常简单。我们只需要把这个函数的一次 invocation 映射成一个 GPU thread，就能获得极大的并行性。对于在场的 programming language nerd 来说，这套系统还有个很好的性质，就是它实际上允许 runtime type polymorphism。比如 collision system 只说：“我需要任何拥有 position 和 bounding box 的对象。” 结果 agent 和 obstacle 两种对象恰好都带着这些 component。有意思的是，collision system 根本不需要知道它们各自的具体 type。传统 CPU code 里，你会用 virtual dispatch 来实现这种效果，但在 GPU 上 virtual dispatch 效率极差，因为它会打破寄存器分配的静态确定性，还会引入一大堆类似问题。

Brennan Shacklett：要把这些东西真正变成一个游戏，我们会把大量独立 system 组合成一个 task graph，用它描述整一帧是怎么运行的。也就是，从 agent 输入 action 开始，到最后更新世界状态，中间整个过程是怎么推进的。这套东西其实相当复杂。图里展示的还只是很小的一部分，里面经过了 physics、为 agent 生成 observation 等阶段。可惜我今天没时间深入到很多底层实现细节，比如怎么让这些表中的 memory allocation 真正高效。我们利用了这是一个 throughput-oriented workload 的事实，所以在 GPU 上做了一种有点像 garbage collection 的事情。我们会 append 新行，把废弃行标记成 deleted，然后用一个超高性能的 GPU sort，在后处理阶段把它们清理掉。

Brennan Shacklett：这套 task graph 的执行，是靠一个 persistent mega kernel 完成的。它会一直不停地搅动当前 frame 里剩余的工作。很多熟悉 ParallelKittens 那一类项目的人应该知道，GPU 的 fast atomic 非常强，强到足以让这一切同步都高效完成。我可以给你们看个可视化。图中每一行代表 GPU 上一个 SM。你可以把每一行里彩色条的填充程度，理解为那个 SM 当前的活跃程度。可以看到大多数时候都很活跃。不同颜色代表 task graph 里的不同 system。每组颜色之间，会有很细的竖向白线。

Brennan Shacklett：那些白线表示 frame 内切换 workload 时的同步点，但你能看到，它们占总工作量不到 1%。也就是说，我们几乎把 GPU 吃满了。这里展示的是一张 RTX 4090，模拟的大概是 4000 个 hide-and-seek 世界。这个 engine 的初版里，我们做了一小组 baseline environment，包括 hide-and-seek，也包括 overcooked，后者是一个 cooperative reinforcement learning environment。之所以选它们，是因为它们原本就有容易搭建的 CPU baseline，所以我们可以做真正 apples-to-apples 的比较。图里的绿色部分，你几乎都快看不见了，那就是这些 machine learning codebase 里原始的 CPU reference implementation。

Brennan Shacklett：说实话，它们的性能糟透了。所有这些任务都被 environment throughput 严重卡住。蓝色部分表示的是：你把我刚才讲的 ECS 思路拿去，在 CPU 上跑成一个更像传统 game engine 的实现，但扩展到同时跑多个 world。红色部分则是：你把整套东西放到 4090 的 GPU 上。很多情况下，它直接快了一百倍以上。我们在我整个研究期间还做了多个项目，证明这套方法可以一路扩展到 end-to-end training。它不只是 simulation throughput 变快而已。我们用了大约两年时间，在这个 engine 上做了很多不同但都很快的 environment。最成功的一点是，那些几乎不懂底层 GPU programming 的人，比如一些 machine learning researcher，也能进来、搭一个 environment、拿到很好的性能，并明显加速他们的 workload。

Brennan Shacklett：我最后想留给大家一个更普遍的观点。我认为，即使在今天 LLM 已经可以写代码的时代，GPU 的高层 scripting language 仍然有大量工作没做完。我现在看到很多 programming language system 的方向，基本都是“底层还是 CUDA programming model，但上面换成 Python syntax”。这当然很好，看起来更简单、也更易读，但它并没有真正帮助你解决 GPU 上的 dynamic memory allocation、超不规则的 parallelism 这些根本性问题。就算你完全忽略 tensor core，GPU 依然拥有惊人的 memory bandwidth 和 compute。我认为现在存在很多有趣 workload，完全可以利用这份充沛而高速的 hardware 获得巨大加速。但这些基础问题意味着，一旦你在尝试做一种之前没人做过的新 workload，就会遇到大量摩擦，我们当年就经历了这个过程。

Brennan Shacklett：我总体上认为，这里存在一个机会，去构建那种默认性能已经足够好的 abstraction。它们能直接把 GPU 那股蛮横的原始算力利用起来，同时让 GPU programming 变得简单得多，真的像一种 scripting language，像 Python 一样自然，但面向 GPU。谢谢大家。

Francois：谢谢 Brennan。

Brennan：嗯。

Francois：最后做个收尾，大家觉得怎么样？不错吧？给个 thumbs up。好。我觉得这种按主题聚类的形式，会成为我们以后办 YC Paper Club 的主要方式。下一场会是 robotics，我们已经有几位很酷的 robotics 方向的人，也会有不少业内人士。如果你们认识合适的人选，欢迎在 Slack 里 DM 我，或者用别的方式联系我。好，大家先别走。接下来还有一个小时，大家可以继续留下来聊天、认识彼此。如果你想和 speaker 聊，或者想和任何人聊，现在就是时候。非常感谢大家今天来。好了。
