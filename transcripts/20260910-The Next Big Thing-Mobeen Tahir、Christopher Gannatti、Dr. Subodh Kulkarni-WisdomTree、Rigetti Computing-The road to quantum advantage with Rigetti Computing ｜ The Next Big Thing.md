---
访谈时间: 2026-09-10
YouTube发布时间: 2026-09-10
字幕来源: YouTube en-orig 自动字幕缓存，经上下文转写
嘉宾名字: Dr. Subodh Kulkarni
嘉宾公司名称: Rigetti Computing
参与嘉宾:
  - 姓名: Mobeen Tahir
    公司或机构: WisdomTree
    职务: Director of Macroeconomics and Thematic Research
  - 姓名: Christopher Gannatti
    公司或机构: WisdomTree
    职务: Global Head of Research
  - 姓名: Dr. Subodh Kulkarni
    公司或机构: Rigetti Computing
    职务: President and CEO
播客名称: The Next Big Thing
播客url地址: https://www.youtube.com/watch?v=XbrpAfiMvGw
youtube_video_id: XbrpAfiMvGw
全文提及的关键名词:
  - Rigetti Computing
  - quantum computing
  - quantum advantage
  - superconducting gate-based quantum computing
  - qubit
  - two-qubit gate fidelity
  - chiplet
  - dilution refrigerator
  - superconducting flex cable
  - optical fiber
  - ABAA
  - hybrid computing
  - CPU
  - GPU
  - QPU
  - NVIDIA CUDA
  - CUDA Quantum
  - error correction
  - Riverlane
  - FPGA
  - Shor algorithm
  - post-quantum cryptography
  - HPE
  - Pittsburgh Supercomputing Center
  - IBM
  - Google
  - D-Wave
  - AI
  - AGI
---

# The road to quantum advantage with Rigetti Computing｜The Next Big Thing

## Transcript

### 量子计算为什么是计算范式的变化

**节目开场：** 量子计算可能代表计算历史上最根本的一次变化。传统计算机的基本信息单位 bit 永远是 0 或 1；量子计算中的 qubit 可以同时处于多种状态。当足够多的 qubit 以正确方式纠缠、操控时，量子计算机可能处理一些复杂到让地球上任何经典计算机都无法在有意义时间内求解的问题。

世界各地的政府都在投入大量资金，量子计算竞赛已经开始。本期主持人是 WisdomTree 的宏观经济与主题研究负责人 Mobeen Tahir，以及 WisdomTree 全球研究负责人 Christopher Gannatti。嘉宾是 Rigetti Computing 总裁兼 CEO Dr. Subodh Kulkarni，节目讨论从量子芯片、工程路线、数据中心落地到 post-quantum cryptography 的完整路径。

### 从化学工程、半导体到量子计算

**Mobeen：** Subodh，你过去先后在 IBM、3M 工作，后来在半导体行业创办和经营公司，最后在 2022 年加入 Rigetti。你接受过化学工程训练，是什么让你进入量子计算？半导体经验又怎样改变了你对这个行业的判断？

**Subodh Kulkarni：** 我在印度 IIT Bombay 学的是化学工程，之后来到美国，在 MIT 完成化学工程和电气工程方向的硕士与博士学习。早期我是一名研究 semiconductor interface 的科学家，后来进入 IBM，参与 CMOS technology 和 DRAM 相关的研发。IBM 是 CMOS 技术的发明者之一，我在纽约和 Fishkill 等地接触了半导体制造的基础问题。

之后我去了 3M，逐步进入管理岗位。在加入 Rigetti 之前的十年，我担任 CyberOptics 的 CEO。这是一家上市公司，为半导体制造商和电子制造商提供传感器与系统。我接手时，公司股价大约是 4 美元；九年后公司以约 54 美元每股的价格出售，给股东和管理团队带来了不错的结果。

交易完成后，Rigetti 董事会联系了我。我的第一反应是：为什么是我？我不是量子物理学家。但研究之后我很快理解了原因。superconducting quantum computing 的核心是一个 chip，它在很多方面非常像 semiconductor chip。虽然要用特殊材料和特殊制造流程，但它同样建立在 silicon wafer 上，也使用很多半导体设备，包括 Applied Materials、Lam Research、Tokyo Electron 等公司的工具，测量和检测流程也与半导体产业相似。

过去二十年，量子计算主要由物理学家推动。他们擅长研究基础物理、发表 Nature 论文和验证实验现象，但行业现在接近商业化，就必须把工程师带进来。物理学家发现了基本原理，工程师需要把实验室 prototype 变成一致、可靠、可制造、可维护的产品。

这是从 transistor 到现代计算机的自然演化。Shockley 等人发明 transistor 后，需要数以百计、数以千计甚至数以万计的工程师，才能把它转成计算机、数据中心和日常设备。Richard Feynman 是量子计算概念的重要先驱，但要把量子计算带出实验室，需要半导体、材料、制造、控制和产品工程经验。因此，Subodh 认为自己加入的时间点很好：行业正在从“证明量子效应存在”转向“把量子设备可靠地放进数据中心”。

### Rigetti 的历史与技术路线

**Subodh：** Rigetti 由 Chad Rigetti 创立。他在 Yale 获得量子物理博士学位，之后在 IBM 工作多年。2013 到 2014 年间，他决定创办 Rigetti，认为商业化量子计算可能有不同于 IBM 的路径。公司在加州成立，完成了多轮融资。2022 年，公司没有继续进行 Series D，而是通过 SPAC 上市。

SPAC 上市有优点，也有缺点。一个明显的问题是，相比传统 IPO，尽职调查可能不够充分。上市之后，Chad Rigetti 与董事会出现严重分歧并离开 CEO 职位，董事会开始寻找熟悉上市公司治理、半导体和高科技产品化的人，这就是我加入公司的背景。

Rigetti 一直专注于 superconducting gate-based quantum computing，技术路径和 IBM 比较接近。加入公司时，行业和 Rigetti 内部都在讨论 qubit 数量扩张，但我来自半导体行业，很清楚质量比数量重要。在半导体领域，我们不会先问一块芯片能塞多少晶体管，而是先把基本物理和基本制造质量做好；只要质量达到要求，利用成熟工具扩展规模通常是工程问题。

量子计算当时却常常只讨论有多少 qubit。我的观点是，如果 qubit fidelity 只有 95%，那么拥有 300 个、300 万个 qubit 都没有意义。真正重要的指标是 two-qubit gate fidelity，也就是信息从一个 qubit 传递到另一个 qubit 时的准确率。

加入 Rigetti 时，公司的 two-qubit gate fidelity 约为 95%，远远不够实用。过去三年多，我们几乎停止了单纯追求规模的工作，把重点放在 fidelity 上。现在 two-qubit gate fidelity 已进入 99.5% 到 99.6% 区间，one-qubit gate fidelity 已达到 99.9% 甚至更高。这个水平已经足以重新讨论规模，但我们仍然不认为它足够进入实际数据中心。我们需要接近 99.7% 或 99.8%，最好接近 99.9%，才能进入真正的 quantum advantage 阶段。

### 超导门型路线：速度和规模的优势

Rigetti 采用 superconducting gate-based architecture。它的两个核心优势是 scale 和 speed。因为它使用许多类似半导体的制造技术，并且通过电子信号进行控制，gate speed 可以达到几十纳秒。

其他路线，例如 trapped ion 或 neutral atom，需要移动离子或原子，gate speed 通常在数百微秒级。超导路线的速度可能快 1000 到 10000 倍。代价是 fidelity 更难做好：天然的离子或原子系统可以达到略高的 fidelity，而超导系统必须解决材料、界面、制造均匀性和控制脉冲的问题。

Subodh 认为，这是一项工程挑战，而不是不可解决的基础物理问题。IBM、Google、Fujitsu、Toshiba、中国政府支持的实验室等都在投入 superconducting gate-based quantum computing。全球量子计算投资中，超过 90% 甚至 95% 可能集中在这条路线，原因就是它兼具速度和可扩展性。

### Open modular architecture 与竞争壁垒

Rigetti 面临 IBM、Google 和中国政府支持实验室的竞争，因此必须建立技术 moat。公司的第一个差异化是 open modular architecture。整个 stack 从量子芯片、硬件层到软件层，都被拆成可以相对独立升级的模块，并允许第三方解决方案接入。

IBM、Google 等大公司更像在制造 mainframe：自己控制从芯片到软件的完整 stack，不轻易允许外部公司进入。Rigetti 的思路是把优秀的外部能力组合进来。

例如，云部署需要 AWS、Microsoft Azure 等平台；IBM 和 Google 自己拥有 cloud business，但 IBM 未必有能够和 AWS、Azure、Google Cloud 正面竞争的云业务。软件 distribution layer 方面，NVIDIA CUDA 几乎形成事实标准，所以 Rigetti 与 NVIDIA 合作，而不是试图重新发明一个软件生态。控制系统方面，公司与 Quanta 等企业合作；error correction 方面，与英国剑桥的 Riverlane 合作。

这种模块化让 Rigetti 能够利用产业链中最强的伙伴，同时降低自己必须从零构建整个 stack 的压力。它也使公司可以根据数据中心实际标准替换控制系统、纠错硬件和云接口，而不需要推倒重来。

### Chiplet 与纠缠连接

Rigetti 的第二个差异化是 chiplet architecture。chiplet 在传统半导体中已经很常见。先进的 iPhone 和 NVIDIA GPU 都会采用 chiplet，因为制造小尺寸芯片比制造一块很大的、均匀性很高的芯片容易。多个约 1 厘米见方的小 chiplet，可以通过 interposer 横向组合成更大的芯片。

量子计算同样面临大芯片制造困难，但量子 chiplet 有额外挑战。传统半导体只需要通过 wiring layer 把 transistor 连接起来，而量子 chiplet 必须让不同 chiplet 上的 qubit 发生 entanglement。Rigetti 使用 interposer，并在 interposer 中集成 tunable coupler，使不同 chiplet 之间能够产生需要的耦合。

这使得 chiplet 不只是扩大尺寸的制造方法，也成为量子架构的 IP 和 know-how 壁垒。公司认为，chiplet、open modular architecture 和后续的控制、纠错技术，会共同形成自己的竞争位置。

### 从 100 个 qubit 到 1000 个 qubit：连线问题

**Christopher：** 超导量子系统要把微波脉冲、频率控制和信号线送入一个比外太空还冷的环境。当前系统约有 100 多个 qubit，未来可能需要 1000、10000 甚至更多 qubit。每个 qubit 需要大约 3 条，有时 4 条线；如果继续用 coaxial cable，物理空间很快会不够。

**Subodh：** 这是全行业的共同问题。dilution refrigerator 的芯片温度约为 10 millikelvin，比外太空还冷。目前全球真正建成、能够运行超过 100 个 qubit 的 superconducting system 主要是 IBM 约 120 个、Rigetti 约 108 个、Google 约 105 个。很多公司会宣布数千、数百万 qubit 的 roadmap，但实际运行的系统远没有那么大。

在 100 个 qubit 时，coax cable 仍然可以处理；到了 1000 个 qubit，就需要管理约 3000 到 4000 条 coax，难度显著增加。Rigetti 计划逐步采用 superconducting flex cable。传统电子产品中的 flex cable 并不新，但在 10 millikelvin 环境下，需要让 flex cable 具备 superconducting 性质，这带来新的材料和制造问题。

公司正在与大学和企业合作研究 superconducting flex cable，并已发表相关论文。预计未来一到两年，flex cable 会开始进入量子系统。它不是实现 1000 个 qubit 的绝对必要条件，因为理论上也可以继续使用 coax，但 flex cable 会让工程实现更容易，Rigetti 计划把它用于未来两到三年的 1000-qubit system。

再往后，到了 10000 或 100000 个 qubit，flex cable 也会遇到上限。因此 Rigetti 与荷兰 Qblox 等公司研究 transduction。方案是把量子系统使用的 microwave signal 转成 optical signal，通过 optical fiber 传入和传出。相比 flex cable，光纤在空间上可以带来一个数量级甚至两个数量级的优势。Subodh 认为，这为十年左右之后的百万 qubit system 提供了可能路径。

### ABAA：解决频率和串扰

量子芯片的另一个困难是频率控制。理想情况下，每一个 qubit 只响应一个非常窄的频率，控制一个 qubit 时不会干扰其他 qubit。但真实 qubit 会对一个频率范围有响应，范围越宽，cross-talk 越严重，规模越大越难单独控制。

IBM、Google 等公司会使用 laser annealing：芯片制造后，用高功率激光逐个处理 qubit，加热特定界面，改变材料 morphology，从而把响应频率范围缩窄。这种方法确实有效，但速度慢、需要逐个移动和对准激光。当 qubit 数量从 100 增加到 1000 时，难度不是简单增加十倍，而是因为定位、时间和校准问题出现数量级上升。

Rigetti 采用 alternating bias assisted annealing，也就是 ABAA。公司通过整个 qubit 表面施加一系列正负 DC flux pulse，让电流通过不同 interface，从整体上改变材料 morphology，进行 frequency targeting。与从侧面逐个处理的激光方法不同，ABAA 可以同时作用于更大的区域，并且是一个更适合制造的过程。

Subodh 说，ABAA 让频率控制效果比 laser annealing 好近一个数量级，并且可以同时处理多个甚至全部 qubit，因而更适合规模化。Rigetti 发布 ABAA 结果后，政府实验室主动联系，希望加快技术扩展，公司也在与政府实验室和其他研究机构合作。

### CPU、GPU、QPU 的混合计算

**Mobeen：** 量子计算机不会替代手机、笔记本里的 CPU，也不会简单替代数据中心里的 GPU。未来的关键可能是 CPU、GPU 与 QPU 的 hybrid infrastructure。这个系统到底如何分工？

**Subodh：** 现在的 data center 已经是 CPU 与 GPU 共存。CPU 适合 sequential computing，例如加法、减法、数据库排序和一系列简单但需要快速执行的计算。GPU 适合 parallel computing，可以把大量相似任务并行处理。NVIDIA CUDA 的作用之一，就是把工作流区分成 sequential 与 parallel，再把结果组合起来，让最终用户不必知道任务究竟在哪个硬件上完成。

QPU 的位置是进一步把 parallel computing 中“多个并行流之间需要反复交互”的部分拿出来。GPU 在这种 simultaneous interaction 场景中需要不断暂停、同步、交换信息再继续，start-stop 的开销很大。生成式 AI 和大型语言模型就存在大量这类复杂交互。

因此未来更现实的架构是 tri-furcation：sequential workload 交给 CPU，普通 parallel workload 交给 GPU，而 parallel streams 之间高度相互作用、包含大量变量同时影响的部分交给 QPU。QPU 是 GPU 的 accelerator，不是完整数据中心的替代品。

量子计算机不适合做 2+3。它可能比普通计算器慢百万甚至十亿倍，而且输出还是一个概率分布，不一定每次都给出确定的 5。量子计算适合的是成千上万变量同时互动的复杂 tensorial math，例如优化、预测、天气模型、药物发现、蛋白质折叠和金融预测。简单判断方法是：如果问题本质上在问“有多少种可能、哪一种概率更高”，它可能适合 QPU；如果只是顺序执行的加减乘除，就应该交给 CPU。

Rigetti 正与 HPE 以及 Pittsburgh Supercomputing Center 合作建立 hybrid system。Pittsburgh Supercomputing Center 是 Carnegie Mellon University 与 University of Pittsburgh 的联合项目，项目由 NSF 支持。未来用户可以通过一个 HPC 加量子计算系统测试真实工作负载，比较它与传统超级计算机的性能和成本。

IBM 和 Google 也在研究 hybrid computing，但 Rigetti 希望成为较早提供任何人都能使用的 hybrid system 的公司之一。Subodh 认为，量子计算的真正商业路径不是突然出现一台完全替代 CPU、GPU 的机器，而是逐步作为 data center accelerator 融入工作流。

### Quantum advantage 的定义与四个门槛

**Christopher：** AI 行业曾经有 ChatGPT moment。量子计算的 ChatGPT moment 是什么？99.5% 到 99.7% 的 two-qubit gate fidelity 是否就是关键？

**Subodh：** Rigetti 对 quantum advantage 的定义很简单：量子计算相对于 classical computing，在 performance 或 cost 上出现清晰优势，足以让 data center manager 说“我愿意使用 quantum computer”。不是在实验室里完成一个漂亮的 benchmark，也不是宣布有多少 qubit，而是出现可以看得见 ROI 的真实使用。

要达到这个阶段，至少需要四件事。

第一，需要约 1000 个 physical qubit。Rigetti 当前约为 100 个，未来两到三年将向 1000 个迈进。

第二，需要接近 99.9% 的 two-qubit gate fidelity。99.8% 也可能有用，但越接近 99.9% 越好。当前 mid-99%，仍然不够。

第三，gate speed 需要优于约 40 纳秒。Rigetti 现在约为 60 纳秒，Subodh 认为工程上不是特别遥远，但必须和 CPU/GPU 的工作速度相匹配，否则 hybrid computing 没有实际意义。

第四，需要实时 error mitigation 或 error correction。即使 fidelity 达到 99.9%，每次运行仍会产生错误。不能只在计算完成后慢慢离线修正，数据中心需要实时抑制或纠正错误。

综合这四个门槛，Rigetti 对 quantum advantage 的时间判断约为三年，可能是两年半，也可能是四年。公司认为自己在行业里相对保守，不赞成把“今天已经实现 quantum advantage”和“还要四年才能对企业产生实际影响”同时说成真。

### Error correction 与 Riverlane

Rigetti 与英国剑桥的 Riverlane 合作做 real-time error correction。Riverlane 大约有 140 到 150 名顶尖科学家，与 Rigetti 规模相近。双方使用 FPGA-based error correction，先利用 Xilinx 等现成 FPGA 进行实时处理；如果 NVIDIA 的 GPU-based error correction 足够成熟，Rigetti 也希望接入 GPU，而不是把自己锁死在 FPGA 上。

当前最大的问题是，量子计算系统产生的错误太多，任何 FPGA、GPU 或 CPU 都可能被错误数据淹没。因此，芯片侧必须先显著降低错误率，纠错侧再准备能够实时处理剩余错误的硬件。这个问题不是 Rigetti 独有，而是全行业共同面对的工程瓶颈。

Rigetti 与 Riverlane 共同发表过接近实时纠错的研究成果。Google 之前展示过 surface code error correction，但主要是 offline 且速度较慢；Rigetti 与 Riverlane 的路线试图把类似 surface code 的方案推向更快、更接近实时的状态。Subodh 认为，error correction 很可能是量子计算进入 data center 前最后必须真正解决的环节。

量子硬件和软件是一个迭代过程。软件开发者需要知道最终硬件可以提供什么样的错误率、速度和连接方式，硬件团队也需要根据软件 workload 继续改进。因此，不是先完成硬件再开始软件，而是两者共同迭代。Rigetti 的 open modular architecture 能让公司根据纠错方案、控制器和软件工具的进展替换合作伙伴。

### Shor algorithm 与 post-quantum cryptography

节目随后讨论量子计算可能带来的安全风险。Shor algorithm 可以在足够强的量子计算机上破解部分现有公钥加密。早期估计，破解 128-bit encryption 可能需要约一百万 physical qubit；随着算法和纠错技术进步，估计已经下降到约 10000 个 physical qubit。未来两三年，这个门槛还有可能降到约 1000 个，恰好接近行业讨论的下一代量子系统规模。

这意味着“harvest now, decrypt later”以及关键基础设施风险值得重视。攻击者可能先收集今天加密的数据，等未来量子计算能力成熟后再解密。水、电、食品、银行、券商和政府系统都依赖数字基础设施，量子攻击可能造成比传统网络攻击更深的系统性后果。

Subodh 认为，post-quantum cryptography 已经在推进，NIST 等机构以及各国政府正在推动企业到 2030 年具备 PQC readiness。问题是很多人知道这个话题，却没有真正演练。Rigetti 自己也还没有全面实施 PQC，这说明从“知道风险”到“迁移所有系统”仍有很大距离。

他认为 128-bit encryption 可能在约五年内面临更现实的风险，虽然也可能需要更久；如果时间缩短到三年，就必须立即提高警报。256-bit 和 512-bit 的破解难度更高，但关键基础设施不能等到量子机器出现后再开始迁移。PQC 的任务不是阻止量子计算，而是让加密系统在量子时代仍然安全。

### 量子计算的早期应用

**Mobeen：** 一旦达到 quantum advantage，最早落地的行业会是什么？优化、药物发现、材料科学、金融服务和密码学经常被提到，你最关注哪些？

**Subodh：** 量子计算会逐步进入 data center，不会突然通过一次轰动宣告改变世界。起初，量子处理器会作为 GPU 的 accelerator，混合系统可能在后台运行，很多终端用户甚至不知道某个步骤使用了 QPU。

最适合早期量子加速的，是优化、天气预测、药物 discovery、protein folding、金融 forecasting 等问题。这些问题有大量变量同时互动，具有 tensorial structure 或 probabilistic nature。量子计算更像一个能够处理高度复杂、多维关系的“人脑式”设备，适合判断在多种相互作用下哪一种状态更可能发生。

量子计算不会一定出现类似 ChatGPT 的瞬间。GPU 进入 data center 也不是某一天突然发生的，早期只是低调地作为加速器逐步部署，后来 AI 让其价值被大众看见。量子计算可能也会经历同样过程：从几个专业场景开始，逐渐提高重要性，而不是靠一个产品发布让所有公司突然采用。

Subodh 对量子计算与 AGI 的关系也感兴趣。当前 AI 行业投入数万亿美元在数据中心、CPU 和 GPU 上，希望在四五年内达到 AGI。另一派研究者，包括 Geoffrey Hinton 和 Yann LeCun，则认为单纯扩大现有 generative AI 路径可能无法达到 AGI。Google、法国 CERN 等机构正在研究量子计算是否能以更高效的方式帮助实现某些 AGI 目标。

他不认为这个方向已被证明，但如果当前 AI 路线出现瓶颈，量子计算可能成为另一条路径。它未必会出现一个确定的 ChatGPT moment，却可能在 AI 的某些优化、概率推断、复杂模拟问题中逐渐成为重要的 accelerator。

### 从芯片制造到可交付产品

后续判断应以硬件数据、软件纠错、混合系统和客户 ROI 共同验证，不能只看远期 roadmap。

量子产业最终仍要回到可重复制造、稳定运行、真实付费需求和可验证的单位经济性，才能完成商业化并形成长期竞争力，而不只是实验室影响力、概念热度或远期故事堆积出来的估值叙事和市场想象驱动的高估值。

**Christopher：** 你提到物理学家和工程师的分工。对投资者来说，这是否意味着量子计算行业正在从“科研成果竞争”变成“产品和制造能力竞争”？

**Subodh：** 是的。量子物理仍然是基础，但从今天起，产品能否持续运行、能否重复制造、能否由客户远程访问、能否和数据中心的控制系统协同，越来越重要。一个在实验室里只运行一次的结果，和一个能够全年稳定运行、接受软件更新、被客户购买的系统，是完全不同的产品。

半导体产业的经验是，很多性能指标在实验室中第一次实现时会非常惊艳，但制造良率、材料一致性、封装、热管理、测试和供应链最终决定商业化速度。Rigetti 把这些问题提前纳入架构设计，是因为量子系统不应当到了 1000 个 qubit 才发现无法接线、无法校准或无法维护。

因此，公司在 qubit fidelity 上的取舍并不是放弃规模，而是先建立能够被复制的质量标准。若每个 qubit 的误差率没有达到要求，增加数量只会增加错误传播和校准复杂度；若质量达到门槛，chiplet、interposer、flex cable 和光纤等工程技术才能真正放大规模。

### 芯片、封装和低温系统的共同约束

量子计算的难点并不只在 qubit 本身。超导 qubit 必须在极低温下工作，控制脉冲需要从室温一路进入 dilution refrigerator，再在不同温度层级完成衰减、过滤和放大。每增加一个 qubit，就可能增加控制线、读取线、热负载和校准参数。真正的系统工程必须同时解决信号完整性、空间、温度、噪声和维护问题。

coaxial cable 在早期系统中比较直观，也容易验证，但当 qubit 数量增加时，线缆数量会使冷却系统和封装变得越来越复杂。superconducting flex cable 的价值不只是节省体积，还可能让控制线以更密集、更规则的方式进入低温腔体。optical transduction 则把问题进一步转换为光信号的密度和低温兼容性，为更远期的大规模系统保留空间。

chiplet 也必须和封装一起考虑。多个 qubit chiplet 之间需要通过 interposer 连接，并且让 qubit 之间发生真实的 entanglement，而不是仅仅把几个独立芯片放在同一个封装里。tunable coupler 的设计、跨 chiplet 的频率管理和连接可靠性，都会决定 chiplet architecture 是否真的比单块大芯片更好。

### ABAA 的制造意义

**Mobeen：** ABAA 听起来既是 qubit 频率校准方法，也是制造流程的一部分。它对大规模生产的价值是什么？

**Subodh：** 每个 qubit 的响应频率都存在一个 distribution curve。我们希望它像一根很窄的针，只对自己的控制频率敏感；现实中它会覆盖一个范围，因此微波脉冲可能触发邻近 qubit，造成串扰。规模越大，频率重叠的概率越高。

laser annealing 的思路是逐个处理 qubit，改变关键 interface 的 morphology，让频率分布变窄。这个方法可以工作，但它需要精确移动激光，并且每个 qubit 都需要单独完成处理和验证。ABAA 通过正负 bias pulse 作用于整片表面，让整个区域的材料 interface 同时发生可控变化。它的优点不是只有结果更好，也包括流程更适合制造。

如果一个方法在 100 个 qubit 上有效，但每个 qubit 都需要单独对准，那么它未必能扩展到 1000 个或 10000 个 qubit。ABAA 的价值在于减少逐个校准的时间，提升批处理能力。这也是为什么政府实验室希望进一步扩大 ABAA 合作：它可能不仅提升一台机器的性能，还改变量子芯片的生产方式。

### 混合计算不是简单的硬件拼接

**Christopher：** 很多人会把 hybrid computing 理解为把一台 QPU 和一台 GPU 放在机架上。但你描述的其实还涉及软件分发层和任务切分。

**Subodh：** 正确。真正的混合系统需要一个软件层判断任务结构，而不是让用户手工决定每一个函数调用到哪个硬件。CUDA 现在已经可以把任务分配到 CPU 或 GPU。未来可能是 CUDA Quantum 或其他 software layer，把任务进一步分成 sequential、parallel 和 simultaneous interaction 三种部分。

例如，一项金融优化任务可能包括数据读取、数据库排序、参数预处理、并行模拟、多个情景之间的交互、结果统计和最终报告。CPU 适合数据整理，GPU 适合大量相同操作，QPU 可能适合变量之间同时互动的优化核心。只有把整个 workflow 串起来，客户才会看到系统级 ROI。

这也是为什么 Rigetti 与 HPE 和 Pittsburgh Supercomputing Center 的项目重要。它不是单独展示一台量子芯片，而是把 QPU 放在一个已有 HPC 环境里，让研究人员使用真实计算资源。客户最终关心的是一项任务花费多少时间、多少能源、多少云资源，以及 QPU 加速是否足以抵消接入、编程和纠错成本。

### 量子优势的四项指标需要同时成立

Subodh 强调，1000 个 physical qubit 单独出现并不等于 quantum advantage。若 fidelity 只有 95%，规模越大可能只是产生更多错误；若 fidelity 很高但 gate speed 太慢，CPU/GPU 等待 QPU 的时间会抵消加速；若硬件性能足够但不能实时纠错，数据中心也不能把它当作稳定服务。

因此，Rigetti 把 1000 qubit、接近 99.9% two-qubit fidelity、低于 40 纳秒 gate speed 和实时 error correction 视为共同门槛。四项指标之间相互影响：更高的 fidelity 降低纠错负担，更快的 gate speed 提高整个混合任务的吞吐量，更多 qubit 提供更复杂问题的计算空间，实时纠错则让结果可以在业务流程里使用。

这也是 Subodh 对部分行业表述保持谨慎的原因。有些公司会说 quantum advantage 已经实现，但当被问到什么时候可以为企业带来重要收入时，又给出几年之后的时间点。按照 Rigetti 的定义，如果数据中心管理者今天还没有理由因为成本或性能而使用 QPU，就很难称为真正的商业 quantum advantage。当前行业仍处于 R&D 和工程完善阶段。

### 纠错的硬件、软件和算法协同

Riverlane 的价值不仅是提供一个 FPGA 方案，而是参与硬件、软件和 error-correction code 的共同迭代。surface code、LDPC 等方案各有优缺点，D-Wave 讨论的 dual-rail 方法也采用不同思路。无论哪一种路线，系统都需要在不直接观测量子状态的情况下，利用周边交互和 syndrome information 推断错误。

量子纠错看起来反直觉：不能直接问 qubit“你是不是错了”，因为观测本身可能破坏状态；工程师必须测量与 qubit 互动的辅助信息，再用算法判断错误类型和位置。不同的纠错方案会对 qubit 数量、控制速度、连接方式和实时处理能力提出不同要求。

Rigetti 采用 open modular architecture，意味着它可以和 Riverlane 的纠错能力、NVIDIA 的 GPU 纠错研究、其他公司的 FPGA 或 CPU 方案保持连接。公司不希望在今天就赌死一种永远不变的纠错硬件，而是希望在未来三年根据错误率、带宽、功耗和实时性选择最优组合。

### PQC 迁移为何不能等到量子机出现

如果 Shor algorithm 未来能在约 1000 到 10000 个 physical qubit 上破解 128-bit encryption，金融、政府和工业系统就需要提前迁移到 post-quantum cryptography。迁移不是换一个密码库那么简单，还包括证书体系、身份认证、设备固件、数据库、备份、供应链和第三方接口。

很多机构已经意识到风险，却还没有实际演练。Subodh 在公开演讲中询问听众谁知道 PQC，很多人举手；但当他问谁已经在自己的组织里实践 PQC，通常几乎没有人举手。他认为这不是因为大家不在乎，而是迁移成本高、旧系统复杂、量子风险看起来仍在未来。

问题在于，关键数据的生命周期可能长于量子计算商业化的时间。今天被窃取的政府、医疗、金融和工业数据，可能在几年后才需要解密；如果等到第一台可用量子计算机出现，再开始升级，时间可能不够。Rigetti 作为量子硬件公司并不因此认为量子威胁是纯粹的宣传，反而希望行业同时推进量子计算和 PQC readiness。

### 产业路线与投资者应观察什么

从产业视角，投资者不能只用 qubit 数量比较 Rigetti、IBM、Google、D-Wave 或其他公司。更有意义的指标包括 qubit fidelity、two-qubit gate error、gate speed、连接方式、可制造性、芯片良率、低温系统、纠错路线、云平台接入、客户 workload 和混合系统的 ROI。

Rigetti 的潜在优势来自几个组合：半导体产品化经验、superconducting gate-based speed、chiplet 与 interposer IP、ABAA 制造流程、open modular architecture、与 NVIDIA、Riverlane、HPE 等合作伙伴的连接。每一项都需要继续用硬件结果和客户使用验证，不能因为有合作或论文就直接等同于商业成功。

风险同样是组合性的。fidelity 可能提升不及预期，chiplet 之间的 entanglement 可能难以稳定，wiring 和低温系统可能成为瓶颈，实时 error correction 可能需要更多 qubit 和功耗，QPU 与 GPU 的软件接口可能不成熟，客户也可能发现传统 HPC 足够便宜。即使量子计算长期重要，单一公司也未必捕获全部价值。

**Subodh：** 我们对路线有信心，但不能把三年时间表当成确定承诺。两年半、三年或四年都可能发生。公司更希望用实际系统、公开指标和可访问的 hybrid workload 证明进展，而不是只发布远期数字。

### 收尾：从实验室到数据中心

后续验证还应覆盖公开可复现实验、客户任务的端到端成本、云端调用稳定性、系统维护成本以及与传统算法的同口径对比。只有这些指标持续改善，量子优势才会从管理层路线图转化为可交付产品证据。

节目最后总结，Rigetti 的核心判断不是“量子计算会替代经典计算”，而是量子系统会与 CPU、GPU 和云平台共存。公司选择 superconducting gate-based route，是因为它在速度和规模上更接近半导体工程；选择 chiplet、ABAA、open modular architecture 和外部合作，是为了把系统从实验室 prototype 推向可制造、可升级、可接入数据中心的产品。

真正需要验证的不是发布会上的 qubit 数字，而是 two-qubit fidelity、gate speed、纠错、混合工作流和 ROI 是否同时达到要求。Rigetti 给出的约三年 quantum advantage 时间表仍是公司判断，不是确定结果；量子计算仍处于 R&D 与工程验证阶段，数据中心管理者尚未大规模采用。

主持人提醒观众，WisdomTree 和本期嘉宾的观点会变化，节目内容不构成研究、预测、投资、税务或买卖证券的建议。过去表现不代表未来结果。Subodh 感谢主持人邀请，主持人也表示，真正值得关注的是量子计算如何在不替代 CPU/GPU 的情况下，逐步成为复杂问题的专用加速器。对 Rigetti 来说，后续验证点包括下一代 qubit 数量、fidelity、芯片互连、纠错结果、Pittsburgh hybrid system 的开放使用，以及真实客户是否愿意为量子加速付费。

节目最后总结，Rigetti 的核心判断不是“量子计算会替代经典计算”，而是量子系统会与 CPU、GPU 和云平台共存。公司选择 superconducting gate-based route，是因为它在速度和规模上更接近半导体工程；选择 chiplet、ABAA、open modular architecture 和外部合作，是为了把系统从实验室 prototype 推向可制造、可升级、可接入数据中心的产品。

真正需要验证的不是发布会上的 qubit 数字，而是 four-qubit fidelity、gate speed、纠错、混合工作流和 ROI 是否同时达到要求。Rigetti 给出的约三年 quantum advantage 时间表仍是公司判断，不是确定结果；量子计算仍处于 R&D 与工程验证阶段，数据中心管理者尚未大规模采用。

主持人提醒观众，WisdomTree 和本期嘉宾的观点会变化，节目内容不构成研究、预测、投资、税务或买卖证券的建议。过去表现不代表未来结果。Subodh 感谢主持人邀请，主持人也表示，真正值得关注的是量子计算如何在不替代 CPU/GPU 的情况下，逐步成为复杂问题的专用加速器。
