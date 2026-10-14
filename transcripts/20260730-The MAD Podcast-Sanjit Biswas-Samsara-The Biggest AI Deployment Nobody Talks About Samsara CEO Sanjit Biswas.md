---
访谈时间: 2026-07-30
访谈时间说明: 未能从公开字幕或节目简介独立确认实际录制日期，按 YouTube 发布日期记录。
YouTube发布时间: 2026-07-30T12:30:25Z
嘉宾名字: Sanjit Biswas
嘉宾公司名称: Samsara
参与嘉宾:
  - 姓名: Matt Turck
    公司或机构: The MAD Podcast
    职务: 主持人
  - 姓名: Sanjit Biswas
    公司或机构: Samsara
    职务: 联合创始人、首席执行官
播客名称: The MAD Podcast
播客url地址: https://www.youtube.com/watch?v=3FHsGiONOGw
youtube_video_id: 3FHsGiONOGw
字幕来源: YouTube 原始公开自动字幕 en-orig，结合完整上下文转写为简体中文
全文提及的关键名词:
  - Samsara
  - physical AI
  - IoT
  - edge AI
  - Agent Studio
  - asset tag
  - Bluetooth Low Energy
  - vehicle gateway
  - AI dash cam
  - video-language model
  - generative AI
  - data network effect
  - autonomous trucking
  - humanoid
  - electrical grid
  - data center
  - ARR
  - ROI
  - Meraki
  - Cisco
---

# The Biggest AI Deployment Nobody Talks About | Samsara CEO Sanjit Biswas

## Transcript

**节目片头：** 这些数据不是在互联网上能找到的 token。你无法抓取 Reddit，就知道某个施工现场发生了什么。Samsara 系统每天会驶过美国 99% 的道路，通常一天不止一次。上周我拜访一家大型能源公用事业公司，对方告诉我：过去 125 年建成了一定规模的电网容量，未来五年要把它扩大到三倍。Samsara 连接数百万辆车，每年处理 25 万亿个数据点。我们估计，过去一年帮助避免了约 38 万起道路事故。

**Matt Turck：** 欢迎来到 The MAD Podcast。今天的嘉宾是 Samsara 联合创始人兼 CEO Sanjit Biswas。Samsara 市值约 200 亿美元，运营的可能是物理世界中规模最大的 AI 部署之一。我们会谈 physical AI、面向卡车司机和一线工人的 agent、humanoid、自动驾驶卡车，以及为什么 AI 热潮本质上也是一次基础设施建设工程。

我们在节目中经常谈 AI 模型和软件 agent，却较少讨论 AI 如何面对交通、施工、工厂和公用事业的物理现实。现在大家提到 physical AI，通常想到 humanoid 或 robotaxi。从你的角度看，physical AI 是什么？

**Sanjit Biswas：** Physical AI 就是把 AI 应用于物理世界。地球的基础设施远不只是 Waymo robotaxi 行驶的道路，还包括施工现场、电网、街道下面的管道，以及现实中所有运转的设施。

它最有意思的难点是，物理世界还没有被充分数字化。这里没有积累几十年的 bits，可以直接做 tokenization、快速摄取和推理。大量价值因此被困在无法读取的现实流程里。

我们首先要把位置数字化，例如通过 GPS tracking；也把 camera 当成 sensor，用大量视频帧细致理解现场。除此之外还有天气、道路降水、限速等数据。把这些现实信号融合起来，才能释放真正的价值。

**Matt：** 工业自动化已经存在几十年，甚至几百年，之后又经历了 IoT 浪潮，Samsara 的股票代码本身就是 IOT。今天的 AI 阶段与此前有什么本质区别？

**Sanjit：** 几百年确实是理解物理基础设施的正确尺度。从古罗马开始，道路、管线和维护流程就长期存在。过去检查道路，需要人到现场看路况、查上次施工记录，甚至挖开之后才知道地下是什么。

Sensor 让数据采集成为可能，之后要解决的是如何处理数据、产生有意义的 insight，并最终决定应该采取什么 action。过去约二十年的重点是 reporting，也就是把数据摄取后做成漂亮表格，让人自己分析。过去两三年，AI 开始能理解这些信息、寻找外部线索并给出判断。现在 agentic AI 还能替人采取行动，例如安排维护工作，甚至执行其中一部分。

这三个阶段的区别很实际。第一阶段告诉管理者“某台设备昨天出现过异常”；第二阶段结合设备历史、天气和作业环境，解释异常可能意味着什么；第三阶段则主动查找维修窗口、创建工单并通知现场。Physical AI 的价值不是多一张 dashboard，而是把现实数据一路连接到下一步工作。

**Matt：** 为什么 Silicon Valley 没有更早全面进入这个领域？我们大量讨论 chatbot 和数字世界的 agent，也有 Tesla 和 humanoid。是数字 AI 必须先成熟，还是物理世界本来就是另一套难题？

**Sanjit：** AI 从数字世界开始很合理。数字世界已有海量 bits 和非常好的训练集，模型可以从数万亿 token 启动。物理世界更混乱，还多了一层 hardware。

“Hardware is hard”并不是一句玩笑。设备必须经受现场环境，经由不可靠网络回传数据，还要真正安装到一线。企业必须让数百万一线工人采用新技术，并把它嵌入每天的工作流程。这些都是脏活、慢活，低垂果实远少于连接一个现成大型数据库。

但运输、建筑、能源、公用事业等实体行业合计约占全球 GDP 的 40% 至 50%。潜在影响巨大，只是创业者必须卷起袖子深度进入现场。

数字软件通常可以远程部署并快速迭代，现场系统却必须处理电源、耐久性、安装方式、无线覆盖、工会和员工培训。模型离线时，卡车和施工机械仍要继续工作；网络恢复后，数据还要正确同步。真正的产品是 hardware、firmware、connectivity、cloud 和组织采用的总和，任何一环失败都会让 AI 无法落地。

**Matt：** 物理环境是否也更不宽容，错误的后果会严重得多？

**Sanjit：** 当然。许多 physical operation 直接关系人命。安全系统可以保护工人，但设计者也必须避免引入新风险。由于这些设备是数字技术，还必须做 cybersecurity hardening，不能给基础设施打开新的攻击面。

施工现场本来就危险，有多吨重的土方机械，视野有限，设备操作员和现场人员都承担风险。我们的核心问题是，能否用数据降低这些固有风险。我们把危险本身看成技术可以改善的机会。

**Matt：** 请用一分钟说明 Samsara 做什么。

**Sanjit：** Samsara 是服务 physical operations 的技术公司，客户包括建筑企业、能源公用事业、供应链和物流公司。我们帮助他们把运营数字化。

产品包含 GPS tracker、dash camera、asset tracker 等硬件，也有摄取数据的 cloud service，以及用于闭环决策的 AI 和 application。目标不是只给人看报告，而是帮助人采取行动，理想情况下自动完成行动。

我们通常从明确、可验证的现实问题切入，再逐渐扩张。最初重点是车队，因为这些行业往往拥有成千上万辆工作车辆。后来我们进入更广泛的一线运营，并把 Samsara 平台数据、第三方来源和现场数据融合起来。

**Matt：** 公司刚超过 20 亿美元 ARR，保持盈利，并以约 30% 增长。还有哪些数字能说明规模？

**Sanjit：** 即使我每天接触这些数字，它们仍显得抽象。系统每年处理约 25 万亿个数据点，包括 GPS、video、第三方 API 等；连接数百万辆车，也有数百万一线工人每天使用我们的 app。

我们更关注这些数据在现实中产生了什么结果。过去一年，我们估计帮助避免约 38 万起车祸。通过优化路线、减少发动机怠速等看似简单但依赖执行的措施，客户还减少了数十亿磅二氧化碳排放。

这些结果不是靠一个通用模型单独完成的。系统必须持续知道车辆在哪里、司机处于什么状态、道路和天气如何、设备是否正常，再在真正有风险的瞬间给出反馈。对工程师而言，38 万起事故不是抽象 engagement metric，而是技术在物理世界减少损害的直接衡量。

**Matt：** 38 万起事故是很惊人的数字，主要来自识别司机疲劳吗？

**Sanjit：** 疲劳只是其中之一。重型卡车和施工行业的人可能在高温环境工作十到十二小时，轮班结束时非常疲惫。夜间、雾天、雨雪后，事故率也会提高。

系统在风险上升时向司机发出实时警报，让人更警觉，也能纠正长期坏习惯。美国大约 10% 的人不经常系安全带，比例因州和行业而异，但系上安全带是改善事故结果最有效的简单动作之一。司机有时只开一小段路，或因为分心而忘记，一次及时提醒就可能救命。

另一个典型行为是看手机。司机觉得只是瞄一眼消息，但车辆可能已经前进一个 football field，约 100 yards。实时提醒能在危险习惯发生当下打断它，而不是等事故后再做培训。

**Matt：** 说说你的创业经历。你从 Stanford、MIT 到 Meraki，再到 Samsara。第一家公司是在读博时创办的吗？

**Sanjit：** 是的。我和联合创始人 John 在二十多年前读 MIT 博士时认识。当时 Wi-Fi 刚出现，我们做了名为 Roofnet 的研究项目，在 2000 年代初覆盖 MIT 与 Harvard 之间的 Cambridge 城区，提供免费 Wi-Fi。

这是一个很实践导向的研究项目，我们研究 routing protocol 和大规模网络架构。后来 Meraki 从中诞生。我们觉得 Wi-Fi 能连接大量用户，很有价值，就把研究成果压缩成一个盒子，让其他人也能方便建设大型网络。

最初我们甚至没把它当公司，只是在 Boston bootstrap 一个项目，后来搬到 California。2006 年 Wi-Fi 仍是新技术，企业还在解决 guest access、大规模网络管理，以及如何应对刚出现的 YouTube 带宽需求。

这段经历让我们喜欢上了解决现实问题。团队有深厚 networking 背景，也招募了不少研究生同学。设备开始进入真实世界后，Meraki 每年收入都翻倍。我们的创业旅程其实是一次意外起步。

Meraki 的早期挑战同样不是只有无线算法。企业需要让访客接入网络、集中管理大量 access point，并应对当时刚兴起的视频流量。把学术 routing research 变成客户可直接使用的盒子，让我们理解了 systems product：研究成果只有经过硬件、云管理和简单部署的重新设计，才能真正扩大规模。

**Matt：** 创建 Samsara 时，你们并没有仓库、装卸码头或施工场地经验。创业者怎样在陌生行业变成专家？

**Sanjit：** 我们确实从未在 loading dock、warehouse 或 construction yard 工作，但一直对这些系统有“书呆子式”的好奇。电网到底如何运行？一个 Amazon 包裹走了多远、在哪些仓库停过？这些问题都很吸引我们。

离开 Cisco 后，我们没打算立刻再创业，只是好奇心驱使我们读大量资料。但 physical operation 无法只从书里学，必须到现场。要进入现场，就需要一个能给客户带来帮助的理由。于是我们从市场和客户问题出发创办 Samsara，经历非常陡峭的学习曲线。

作为第二次创业者，这种陌生反而有好处。如果继续做熟悉领域，我们可能会过度依赖“Meraki 当年就是这样做”的经验。Samsara 的客户是运营部门，不是纯技术买家；我们直接销售并直接与客户合作，而不是主要通过 channel。这种差异迫使我们回到 beginner's mind。

**Matt：** 深入看产品。硬件 sensor 像眼睛和耳朵，软件与 AI 是大脑，最近新增的 agentic layer 则像负责行动的手臂。这个类比准确吗？

**Sanjit：** 大体准确，但每一层之间都需要 connective tissue。以桌上的 asset tag 为例，它可以装在施工设备上，内部有 accelerometer，能判断设备移动频率；有比消费设备更强的 industrial-grade Bluetooth；还有电池、firmware 和坚固外壳，甚至被卡车碾过后仍能工作。

它通过数百万 Samsara gateway，以及数千万可充当 relay 的手机和手持设备，把数据安全送到 cloud。数据链路从现实运动、accelerometer、Bluetooth 一直延伸到云端。

到云端后还必须组织信号。数据如果噪声太大，AI 的 signal-to-noise ratio 就很低。我们先清洗和结构化数据，再由“大脑”存储、分析并向用户呈现 insight。Agentic layer 则直接采取 action。

同一事件常由多种 sensor 共同确认。Accelerometer 记录设备突然移动，GPS 给出位置，camera 解释现场发生了什么，engine diagnostic 则说明司机是否踩了刹车。若这些时间序列没有正确对齐，模型会把无关信号拼在一起。数据工程和设备时钟看起来不如模型新鲜，却决定最终判断是否可靠。

例如纽约下雨时，系统可以要求当地整个车队增加 following distance。过去这种调整需要有人盯着几千辆车逐个修改设置，现实中通常根本不会做。现在 AI 可以一致地、大规模执行，这就是“手臂”层的价值。

**Matt：** Asset tag 使用的是哪类连接？

**Sanjit：** 它用 Bluetooth Low Energy，也就是消费级 fitness device 和 AirPods 使用的 BLE。Bluetooth 这些年进步很大，吸收了很多其他无线标准的优点，工业 tracker 可以获得很长的传输距离。我们还在标准之上加入安全层，保护 tag、资产和位置数据的隐私。

桌上这款 tag 的电池约可用三年，另一些能用六年以上。我们最近还发布了 tracking label，它像一张很薄的贴纸，约可运行 45 天，足以覆盖一次单向运输。它不用 lithium-ion battery，货物到达后可以直接丢弃。

贴纸内部有薄型电池、Bluetooth chip 和 Samsara firmware，会持续广播位置信号。创新不在于我们自己发明电池或 silicon，而是 systems integration：把合作伙伴的零件整合成可靠产品，再接入覆盖数百万车辆的 Samsara 网络。

45 天寿命是为一次运输周期设计，不追求永久使用；三年或六年设备则适合高价值工具和工业资产。不同 form factor 在成本、续航、强度和回传频率之间取舍。客户真正购买的是“这个资产现在在哪里、是否被使用”，而不是一块 Bluetooth 芯片，所以系统必须从标签一直连到可操作的 cloud record。

这类似 Apple AirTag 的生态，但属于 industrial-strength 版本。不同客户的车辆、gateway 和手机会互相 relay 信号，单个低成本标签因整个网络而获得广泛覆盖。

**Matt：** Vehicle gateway 又做什么？

**Sanjit：** 它像装在卡车、施工机械或其他移动资产上的 black box。它从发动机计算机和 diagnostic port 采集信息，包括油耗、故障码、司机是否踩油门或刹车等。

这些信号经过整理后形成很长的 time series。即使一个 fault code 也有丰富上下文，仔细解析可以了解特定发动机、燃料类型、空气压力等状态。只有长期连续数据，才能判断故障是偶发噪声、持续恶化，还是需要立即维修。

**Matt：** AI dash cam 呢？

**Sanjit：** 普通 dash cam 已经很有用，Uber 司机发生道路纠纷时能迅速证明事实。Samsara 做的是 connected dash cam：记录 HD video，拥有本地存储和云连接，并在 edge 运行 AI model。

朝外的 camera 结合天气与道路状况，提醒司机增加 following distance；朝内的 camera 识别疲劳、手机使用等行为，实时向司机反馈。司机可以 self-correct、self-coach。

如果人在拿起手机的瞬间反复听到声音警告，这种 negative reinforcement 会打断习惯。我们大约六七年前把 AI inference 引入 edge 后，这成为重要突破，之后不断增加可识别的风险类型。

**Matt：** Dash cam 以前只是安全设备，现在也成为司机与 AI 沟通的 interface。

**Sanjit：** 对。设备已经在驾驶室，就可以在上班前播报当天路线、traffic 和 weather。司机也可以按按钮联系 dispatch，说明因为取工具等原因会迟到。原本单向采集的安全设备，由此变成连接司机、调度和 AI 的双向操作界面。

**Matt：** 温度等其他 sensor 也由 Samsara 制造吗？

**Sanjit：** 整套系统由我们设计，但不是每个零件都自研，而且它是 open system。新款卡车常常已有 API，我们可以 cloud-to-cloud 连接，不一定再装 black box。关键是把数据统一组织，并与客户其他资产无缝整合。

实体运营中的车队通常高度混杂，可能同时有 Ford、GM、Caterpillar、Freightliner 和其他设备。Samsara 充当 orchestration layer。自有硬件很重要，但第三方软件、OEM API 和现成 sensor 也都可以进入同一系统。

**Matt：** 数据进入 cloud 后，是不是放进巨大 data warehouse，再经过 ETL transformation？

**Sanjit：** 从 ingestion 角度看是这样。我们使用现代 hyperscaler cloud，不是只有一座超大型自建数据中心。系统存储和组织海量数据，并运行许多自动处理流程。

之后，不同角色通过 UI 和协作界面使用它。一线司机是常规用户；dispatcher 安排车辆；safety manager 处理风险；compliance manager 完成监管文件；maintenance 团队判断哪辆车回到 yard 后需要维修；管理层则关心是否按时到达、车队效率如何，以及怎样把同一流程扩展到数千或数万名员工和资产。Samsara 的大多数客户都是这种大型 enterprise。

**Matt：** 面对传统行业和多种 buyer persona，特别是在加入 AI 后，你们怎么说服客户购买？

**Sanjit：** 这类技术非常直观，客户看到真实运行就很快理解。我们会去现场 demo，并做小规模 trial。设备是 plug-and-play，可以直接在客户自己的行业和环境测试。

Physical operation 往往同时有多个问题：事故太多、车辆怠速浪费燃料、工具遗留在工地而每年花数百万美元补买等。我们先在一个团队或地区证明能解决这些问题。客户是自己行业的专家，看到结果后立刻能判断 ROI。

他们不是因为产品贴着 AI 或 big data 标签而采购，而是因为它确实减少建筑业务事故、找回工具、降低油耗或改善准时率。销售必须从可量化业务结果出发。

小规模 trial 还有一个作用，是同时说服不同部门。Safety team 看到事故下降，finance team 看到保险和燃料成本，maintenance team 看到故障提前发现，一线员工则看到工具更容易找回。一个产品能从同一套数据产生多项 ROI，才有条件从单一区域扩展到整个 enterprise。

**Matt：** 如果模型逐渐 commodity 化，Samsara 的长期 moat 是 data layer 吗？

**Sanjit：** 无论模型是否 commodity 化，它们吸收数据和推理的能力都很强。Samsara 的独特位置在于把未数字化的 operational data 带进来。

这些不是从网上能找到的 token。你不能抓取 Reddit，就知道某一时间某个施工现场发生了什么；simulation 也不能完全替代真实现场。客户要知道的是，当时那台设备、那条道路、那名司机和那种天气的具体情况。

取得这些数据，需要 hardware 与 software 配合，也需要 change management：把设备部署到现场，让员工采用，并与客户共同理解业务。我们十多年来一直在做这件事。它需要持续下现场，从客户业务倒推产品，无法真正一键部署。

这种 data moat 也不是把所有客户原始视频简单堆在一起。价值在于建立对道路、设备类型、风险行为和运营流程的结构化理解，并在隐私和客户权限边界内复用模式。例如恶劣路口的风险可以提醒经过同一路段的其他车队，但某家公司具体工地上的商业数据仍属于该客户。

**Matt：** 不同客户之间有 data network effect 吗？客户 X 在地区 Y 的 dash cam 经验，能否帮助地区 Z 的客户？

**Sanjit：** 很明显有。公司虽然不同，但大家在同一批道路上行驶。Samsara 系统一天内覆盖美国约 99% 的道路，而且通常会重复经过多次。

这可以用来识别高风险路口、恶劣天气和路面风险，再提前警告其他司机。Camera 与 accelerometer 还能找出 pothole。Chicago 等城市想知道冬季过后出现了哪些坑洞，应按严重程度以什么顺序维修。每次车辆经过大幅颠簸，就可以调取视频判断原因，还能持续观察坑洞是否扩大、路面裂缝是否恶化。

覆盖率带来的优势不仅是样本多，而是更新频率高。同一条路一天被不同车辆经过多次，系统可以区分一次偶发颠簸和持续恶化的路面缺陷，也能比较降雨或降雪前后的变化。城市因此不必等居民投诉或派人逐路检查，而能按位置、严重程度和发展速度安排维修。

Asset tracker 也受益于网络。单个 Bluetooth tag 放在数英亩大的工地上，自己可能无法回传。但运材料的公司、施工总包、电气承包商等任何一方的车辆或手机经过，都可能拾取信号。数百万车辆和数千万 handset 共同形成庞大的 mesh network。

**Matt：** Edge 和 cloud 分别做什么？比例如何？

**Sanjit：** 一般来说，edge 负责 inference 和 data collection。采集的数据成为训练集，模型 weights 从 cloud 下发，在设备端以每秒多帧运行，完成实时、低延迟检测，并立即向司机闭环报警。

采用 edge 首先是现实需要。很多客户在偏远地区运营，cellular signal 不稳定；其次是 latency，危险发生后越快反馈，司机越可能立即纠正。这个架构在实际环境中更 robust。

但边界并非固定。需要更大算力或跨事件分析时，也可以在 cloud inference。设备与云之间有 real-time tunnel，可以按任务动态分配。

**Matt：** Edge 上运行的是较小模型吗？例如完成特定图像任务的传统 convolutional neural network？

**Sanjit：** CNN 是我们最早使用的模型，源于 ImageNet 时代，例如判断画面里是否出现手机。后来模型更复杂，通常共享一个 backbone，再配多个 classifier、head 或 attention head。

检测到司机手里有物体只是第一步，还要判断那是 phone、vape pen、sandwich，及其正在进行什么动作。这不是一次 single-shot detection。朝外、侧面和后方 camera 也会做 depth estimation，判断车辆是否接近 lamp post、mailbox 或其他障碍，所需模型与普通 CNN 不同。

**Matt：** Generative AI 给产品带来了什么根本变化？主要是 video reasoning 吗？

**Sanjit：** 这是重要变化之一。过去视频事件需要人工 reviewer，甚至外包到低成本地区，现在 cloud model 可以大规模完成。

例如卡车突然急刹，简单规则会认定司机分心后才反应；但完整视频可能显示前方突然冲出 deer 或 dog，司机是在做正确的 defensive maneuver。Video-language model 可以理解上下文，反而给司机正向反馈。

判断是否闯红灯也需要理解道路 geometry、信号、车辆轨迹和环境，不是单帧分类。我们会使用 VLM、JEPA-style model 等不同模型家族。

Generative video 的另一用途是 coaching。企业不可能让安全经理逐一与数万司机坐下来回顾每周驾驶。AI 可以生成 coach avatar，外观可以像公司的 VP of Safety，也可以是客户希望采用的其他人物，为每位司机生成个性化周度培训。这类能力五年前很难想象。

关键是把“检测事件”和“解释事件”分开。传统模型很擅长识别急刹、手机或安全带，generative model 则能把多个事件组织成司机可理解的反馈：哪些行为值得肯定、哪种习惯需要改变、下周应重点注意什么。它把有限的安全经理时间放到最复杂的案例，同时让每个司机都得到基础 coaching。

**Matt：** 模型是自研、open source，还是来自 OpenAI、Anthropic、Gemini？

**Sanjit：** 我们对模型保持开放。Frontier lab 进展很快，系统会同时使用多家模型。Open source，尤其 open weights，也很有吸引力，因为提供 operational freedom。我们可以 distill 模型，把它缩小后放到设备上。

有些现场任务则从头训练，模型可能只有数千万 parameters，却针对非常具体的环境。选择标准不是品牌，而是任务准确率、latency、成本、可部署性和安全性。

同一产品也不必永久绑定一个模型。Cloud reasoning 可以调用 frontier model，edge detection 则更适合经过 distillation 的 open-weights model 或专用小模型。现场设备的 compute、功耗和网络带宽有限，因此“更大”不自动等于“更好”。Samsara 会按任务拆分模型，并在新模型出现时替换其中一层。

**Matt：** 你们在 2026 年 6 月底 Las Vegas 的 Beyond 大会上发布了 Agent Studio。此前你把产品演进描述为连接运营、理解运营，再到采取行动。Agent Studio 如何接上这条路线？

**Sanjit：** 几年前我们已把 LLM 引入产品，叫 Samsara Assistant，本质上是连接客户 operational data 的 chatbot。客户会问：“谁是最安全的司机？”“哪些卡车需要维修？”这通常是一次或少数几轮对话。

过去一年 agent 的突破，是能在更长时间范围内工作。AI 不再只用一秒回答问题，而是自己制定计划、执行多步任务。Coding 领域已经看到这种影响，physical operation 也一样。

我在大会演示了 warranty agent。系统看到 fault code 后，会打开对应 service manual，读取客户与 OEM 单独谈定的 warranty agreement，再根据车辆年龄和 mileage 判断该故障是否在保修范围。

确认后，它可以建立 work order、填入维修步骤，并搜索其他车辆是否有同类故障。原本需要一到两小时人工查资料和填表，现在不到一分钟完成。相同模式可以用于 reporting、每日司机 briefing 和许多其他任务。

Warranty agent 的难点不是只从手册里搜索一个 fault code。不同 OEM、车型、里程和客户谈判合同对应不同条款，agent 必须证明每一步匹配关系，并把结果落到真实工单。它还可以把单车故障扩展成 fleet-level 检查，提前找出同型号车辆是否正在出现相同信号，从事后报修转向预防性维护。

**Matt：** 你们似乎先从风险较低的 use case 开始。保修申请判断错了固然不好，但不会直接伤害人命。

**Sanjit：** 我更愿意说，我们从最实用、最能产生影响的地方开始。现实中大量 warranty claim 根本没人申请，因为员工没有时间查手册、核对合同和完成 paperwork。自动化不是先替代一个已经很高效的人，而是把原本完全没做的工作补上。

长期目标是自主运行一部分运营流程。例如每天早班前重新规划路线。技术已经能做到，但需要业务 context：某条路线长期由某位司机负责，是因为他与客户合作了十年。Agent 不能只看最短距离，还必须理解这种关系。我们先在确定有价值的任务中积累经验，再与客户决定下一步。

**Matt：** 真正能工作的 agent，究竟有多少靠 agentic reasoning，又有多少依赖传统 code、workflow 和 rule？

**Sanjit：** Agentic reasoning 对制定计划和长时执行是巨大突破，但仍要明确任务目标。这个定义过程就是一种轻量 workflow，也包含 guardrail：什么时候 agent 必须求助，什么时候不应继续钻进 rabbit hole。

在 physical operation 中，guardrail 还包括权限边界。一个 agent 可以起草 warranty claim 或建议调整路线，却不应未经批准就改变高风险安全参数。任务越接近人身安全、昂贵设备或监管责任，越需要确定性 rule、审计日志和 human approval。自主程度应由结果可逆性决定。

成功系统是 operational context、workflow、guardrail 与 agent reasoning 的组合，任何一部分单独使用都不够。

我们的产品原本就有 workflow。多数商业车队在每个 shift 开始和结束时做 walk-around inspection，Samsara 每年记录约 3 亿到 3.5 亿次。过去只是手机上的步骤清单，司机逐项拍照、确认设备安全。现在可以把检查结果与 diagnostic information、location、上次检查者和照片内容结合，agent 才能真正理解问题并采取行动。

例如司机在照片里标记轮胎异常，agent 可以核对最近胎压 time series、车辆当天路线和上一次检查，判断是新问题还是重复报告，再决定是否允许车辆出发、安排哪家维修点。Workflow 保证必需步骤不被跳过，reasoning 则处理规则未穷举的现实情况，human escalation 负责高风险决定。

**Matt：** 今天的 agent 还做不到什么？

**Sanjit：** 能力 ceiling 几乎每周都在变。新模型很强，很难判断绝对上限，但实践中仍会走神、陷入 loop。模型也许最终能找到答案，问题是能否在十秒、一分钟或一小时内找到。

随着 compute、algorithm 和 model architecture 共同改善，今天需要一天的任务可能缩短到一小时甚至更少。当前真正的 ceiling 经常不是理论可行性，而是 latency 与成本是否符合业务要求。

**Matt：** 如果把视野放到未来一两年，而不是十年，什么今天勉强可做的事会成为常态？

**Sanjit：** 一个例子是 AI driver ride-along。传统车队经理会陪司机跑完整八小时，不只是看车速，而是观察是否经常查看后视镜、是否保持警觉、是否有稳定安全习惯。

让模型理解全天视频需要巨大 video compute。今天已经能做，但成本很高。随着每百万 token 成本快速下降、模型能力提高，一两年内会变成可大规模交付的产品。

Ride-along 观察的不是某一帧是否违规，而是八小时内持续形成的驾驶习惯：司机是否反复检查后视镜、是否提前观察路口、遇到复杂情况时是否保持注意力。把长视频 token 化后，计算量远高于短事件检测。只有 inference throughput 提高一个数量级，企业才可能为每位司机持续运行这种分析。

上周末我测试了 Cerebras 这类 wafer-scale chip 公司提供的 inference。他们运行一个加速版大型模型。相同模型在高速 GPU 上可能约 100 token/s，在其 cloud 上能达到约 800 至 1,500 token/s，接近十倍。这样的非线性跃升会解锁过去因为太慢或太贵而无法落地的任务。

**Matt：** Dash cam 还有社会层面的意义。它像一种未来蓝图：AI 不只在被询问时出现，而是全天伴随专业人员、观察每个动作。即使目的是安全，也容易让人觉得 Big Brother 在监控。你们怎样让客户、司机和一线员工接受，而不是愤怒地拆掉 camera？

**Sanjit：** 我们花很多时间与司机和其他一线工人交流，因为他们是主要用户，也是系统真正的受益者。

很多人忽略了 dash cam 最大的用途其实是 exoneration，也就是事故后证明司机无责。以客户 Home Depot 为例，知名品牌经常收到“你们的卡车撞了我的车”之类索赔。司机明明工作规范，却要面对无法自证的指控，非常沮丧。

这也解释了为什么“监控”与“保护”不能只由设备本身决定。同一段视频若只用于寻找处罚理由，员工当然会抵触；若它更常证明司机无责、记录良好表现并阻止危险，员工能看到直接收益。部署成败取决于企业文化、告知方式、数据访问权和申诉机制，而不只是 detection accuracy。

HD video 可以清楚显示车辆在哪里、事故是否发生、由谁造成。如果确实有责任，公司可以和解赔付；如果没有，企业和司机就能用证据反驳。大约 90% 的时间，司机表现良好却没人看到。分析完整行程后，系统也能识别 defensive driving 等好行为，而不是只记录错误。

企业如果把这些证据用于正向激励，像 employee of the month 一样表扬安全驾驶，员工会更支持。更重要的是，施工、油田等行业的伤害直接落在工人身上。安全系统的目标是让每个人下班时与上班时一样完整地回家。

前提是透明、尊重隐私，并明确数据怎样使用。Camera 不是 hidden device，司机应在部署前知道它记录什么、不记录什么、如何帮助自己。

**Matt：** 但 AI 也会成为工作质量的 judge，就像世界杯 VAR 判断 offside。如何避免误用？

**Sanjit：** 关键词仍是 transparency 和 change management。企业要在一开始解释设备目的、能力和员工能从中得到什么。Home Depot 部署后，汽车索赔减少约 65%，这对公司管理层、地区负责人和司机都是明确收益。

理论上任何技术都可能被坏人滥用，但持续让人坐着观看每个司机既低效又无聊。更现实的控制是，系统只标记规定事件，员工知道数据保留与调用规则，企业公开说明哪些决策会使用 AI。用持续可见的价值与明确边界，才能获得整个组织的信任。

**Matt：** 展望五到十年，physical operation 会变成人与 robot 混合的 fleet 吗？

**Sanjit：** 会有更多 robot。今天进入 manufacturing plant 或 fulfillment center，已经能看到大量 automation。二十年前常见的搬运伤害减少了，因为 robot 真正在做 heavy lifting，但现场仍需要人处理交接和例外。

类似变化会进入施工、公路建设和电网改造。平整施工场地是重复性很强的任务，robot 可以在午夜到早上八点的第三班连续处理路旁五英里地面。未来五年内，这类场景很可能实现。

自动化最先进入的任务具有几个共同点：路径明确、动作重复、环境边界可控制、出错后容易停机。夜间平整路基既能利用人类较少工作的时段，也减少工人暴露于大型机械附近的时间。材料协调、现场例外和跨工种决策则仍由人负责，因此 mixed fleet 会比完全无人现场更早成为主流。

施工其余部分充满 exception：材料没到、现场条件改变、必须临时调整工序。人类仍依靠经验和判断协调这些问题，robot 同时把道路铺平。自动化与人不会简单互斥，而是按任务特征分工。

物流也一样。最后一公里需要取包裹、进商店补货，复杂度很高，也许未来 humanoid 能做；在此之前，Dallas 到 Phoenix 的 long-haul 路段更容易自动化。现实车队会长期同时包含不同品牌、不同型号的人类驾驶设备和 robot。

**Matt：** 自动卡车和 construction humanoid 在 Samsara 业务中扮演什么角色？

**Sanjit：** 客户普遍受到 labor supply 限制。这些行业 labor-intensive、asset-heavy，工作很多却缺人，因此欢迎自动化。

Samsara 希望提供 single pane of glass，统一编排人和机器。Dallas 的自动卡车即将到仓库时，系统可以提前准备接货流程、通知最终客户；tracking label 贴在 pallet 上，从供应链交接、到达工地直至安装，全程产生数百个 ping。

消费者今天可能只看到包裹“离开仓库、运输中、派送中”等五次更新，工业客户则需要知道昂贵 aerospace assembly 此刻究竟在哪里，因为另一项工作正等着它。设备开始自行移动后，这种端到端可见性会更重要。

**Matt：** Self-driving truck 是否近在眼前？三年后会有 10% 还是 75% 卡车自动驾驶？

**Sanjit：** Robotaxi 会更快，因为它通常在区域内运行，乘客从城市一端到另一端的需求相似，车辆也更标准化，所以消费者会先看到明显变化。

长途 A 到 B 运输只是 commercial vehicle 活动的一小部分。更多车辆属于 field service，例如 HVAC technician、plumber、electrician，驾驶只是为了去现场完成工作；另一些属于建筑行业，甚至在建设道路本身。这是当前 autonomy 不擅长的 messy long tail。

因此商业车队全面自动化可能需要十到二十年，而不是三年。Cement mixer、garbage truck 等设备高度定制，autonomy system 扩散到每种专业车辆的曲线，比标准 sedan 或 van 慢得多。

这并不意味着未来十年没有商业价值。某些封闭路线、仓库间干线和重复施工任务会率先自动化，其他车辆仍由人驾驶。客户因此更需要一个同时看见 autonomous truck、人类司机、传统设备和货物标签的平台，而不是等待整个行业一次性切换到无人化。

**Matt：** Samsara 处于运输、公用事业、制造等实体经济核心。你现在看到美国工业活动是在放缓还是加速？AI 和 data center 是否真实影响客户？

**Sanjit：** 客户比过去任何时候都忙，美国实体经济的建设强度很高。上周我与一家大型能源 utility 在现场交流。对方说，过去 125 年公司建成了一定规模的 grid capacity，未来五年要把可供电能力扩大到三倍。也就是用五年完成过去 125 年存量的两倍新增建设。

即使采用新技术，这也需要极其庞大的基础设施投入，他们已经忙到无法再快。类似情况出现在很多行业。这家 utility 还说，约 90% 的新增需求来自 data center。AI 数据中心需求快速增长后，电力、输配电、施工与设备都成为瓶颈，Samsara 的许多客户直接参与解决这些问题。

这里的 AI 需求最终会转化成大量现实作业：建设发电和输电设施、运输变压器和材料、安排工程车辆、检查现场安全、维护新资产。模型训练看似发生在 cloud，实际扩张速度却受到 electrician、车辆、许可、grid connection 和施工效率限制。Samsara 的机会正位于这种数字需求与物理供给之间。

**Matt：** 客户雇用大量 skilled trades。最近有人半开玩笑说，如果律师工作会被 AI 自动化，不如转行做 plumber。你怎么看这些职业？

**Sanjit：** 我先提醒想转行的律师，plumbing 很脏也很难。多个 trade 已出现 labor shortage，包括 electrician、long-haul truck driver 和持 commercial driver's license 的人员，需求还在增长。

Data center boom 是典型例子，现在 electrician 数量明显不够。Meta 等公司已经发起 reskill 计划，培训更多人进入电工行业。下一步是提高稀缺技术工人的效率，不能让他们到现场后一直等材料，而应把时间用在真正需要技能的工作上。

这些职业也在现代化。Electrician 的很大一部分负担，是赶到正确现场、确保材料齐备、弄清任务。AI 可以提前完成这些协调和认知工作，让人专注于难以替代的专业判断与动手能力。

所以 AI 与 skilled trade 的关系不只是替代。电网和 data center 建设把工作需求推高，AI 则帮助有限的人力完成更多项目。若材料、车辆和工单协调仍低效，再多模型也无法缓解现场瓶颈；把稀缺人员从等待和文书中释放出来，反而是最直接的产能提升。

**Matt：** Sanjit，感谢这次很有价值的交流。Samsara 所做的工作在整体经济中非常重要，也很高兴更深入了解你们的产品。

整场讨论的共同主线是，physical AI 的瓶颈从来不只是模型。必须先取得现场数据，再把硬件部署、网络连接、组织采用、可靠推理和真实行动连成闭环。只有闭环能稳定运行，25 万亿数据点才会转化成更少事故、更低成本和更高基础设施产能。

**Sanjit：** 谢谢，很高兴参加。

**节目结尾：** 感谢收听 The MAD Podcast。欢迎订阅、评论并在收听平台留下评价。
