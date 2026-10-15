---
访谈时间: 2026-08-04
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: 2026-08-04T12:00:29Z
嘉宾名字: "Josh Meier; Matt McPartlon"
嘉宾公司名称: "Chai Discovery"
参与嘉宾:
  - 姓名: "Josh Meier"
    公司或机构: "Chai Discovery"
    职务: "联合创始人"
  - 姓名: "Matt McPartlon"
    公司或机构: "Chai Discovery"
    职务: "联合创始人"
  - 姓名: "Pat Grady"
    公司或机构: "Sequoia Capital"
    职务: "主持人"
  - 姓名: "Sonali Singh"
    公司或机构: "Sequoia Capital"
    职务: "主持人"
播客名称: "Sequoia Capital"
播客url地址: "https://www.youtube.com/watch?v=wv53mDmY-k0"
youtube_video_id: "wv53mDmY-k0"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳并结合完整上下文转写为简体中文"
原始字幕缓存: "/Users/wesley/.codex/automations/youtube/caption_cache/wv53mDmY-k0.en-orig.source.txt"
原始语言: "English"
全文提及的关键名词:
  - "Chai Discovery"
  - "Chai-1"
  - "Chai-2"
  - "drug design"
  - "drug discovery"
  - "de novo antibody design"
  - "hit rate"
  - "protein folding"
  - "AlphaFold 2"
  - "diffusion model"
  - "variational autoencoder"
  - "amino acid sequence"
  - "protein structure"
  - "scaling law"
  - "bitter lesson"
  - "wet lab"
  - "computer-aided design"
  - "molecular CAD"
  - "Protein Data Bank"
  - "ESM"
  - "glycosylation"
  - "GPCR"
  - "manufacturability"
  - "developability"
  - "personalized medicine"
  - "rare disease"
  - "OpenAI"
  - "GPT-1"
  - "GPT-2"
  - "David Baker"
  - "Eli Lilly"
  - "Novartis"
  - "Pfizer"
  - "GPU"
  - "data flywheel"
companies:
  - OpenAI
  - LLY
  - PFE
industries:
  - 生物技术
  - AI制药
  - 制药
technologies:
  - LLM
  - 蛋白质设计
  - 扩散模型
  - GPU
keywords:
  - 规模定律
  - 数据飞轮
tags:
  - OpenAI
  - LLY
  - PFE
  - 生物技术
  - AI制药
  - 制药
  - LLM
  - 蛋白质设计
  - 扩散模型
  - GPU
  - 规模定律
  - 数据飞轮
---

# Chai Discovery's Bitter Lesson: Drug Design Is Another Scaling Problem

## Transcript

### 开场：先把模型做简单，才能真正扩展

**Matt McPartlon：**

Chai 的一个重要指导原则是 simplicity（简单性）。以 Chai-1 为例，它大约有 23 个不同的子模块。想迭代这种模型时会非常困难，因为研究人员必须分别理解每个模块，再理解它们相互作用时的行为和动态，这种方法并不容易扩展。

所以我们会反过来问：怎样把系统简化？什么才是真正重要的部分？当核心结构足够清楚以后，整个研究流程，以及寻找可以继续 scaling 的方向，都会简单很多。

简单并不等于模型能力弱，而是尽量让同一套学习机制从数据中获得多种能力。每增加一个手工模块，团队就多一套需要监控的假设、接口和失败模式。短期可能更容易解决单个 benchmark，长期却会阻碍扩大模型、替换数据或把能力交付到产品。Chai 更愿意承担通用模型早期不够完美的代价，换取随后通过 scale 持续改善的结构。

**Sequoia 主持人：**

今天邀请到 Chai Discovery 的两位联合创始人 Josh 和 Matt。Chai 用 AI 设计分子，可以把它看作一家面向生物学的 foundation model lab。这个说法很宏大，那么 Chai 真正的大想法是什么？

### 从“药物发现”转向“药物设计”

**Josh Meier：**

Chai 想让药物发现更接近工程。LLM 已经能很好地生成代码，因为代码是一种非常清晰的抽象，人可以用它表达想让系统完成什么。今天的生物学还不是这样，很多工作依赖 trial and error（试错）。

回看现代生物技术早期，今天许多药物的发现带有很强偶然性。我们希望把这个过程工业化，建立类似软件和现代工程中的 abstraction layer（抽象层），让生物学家能够快速迭代，并把这种能力带入药物发现。

**Sequoia 主持人：**

是否可以把药物开发看成一条移动的边界：一边是可以被工程化的部分，另一边是必须在真实世界测试的部分？随着技术进步，可以工程化的比例不断增加。哪些发展推动了这条边界？

**Josh Meier：**

这是一种合理的理解方式，但实验室并不会消失。lab 的关键作用是验证设计是否正确，而 verification 同样是 AI 的核心主题。如果能评估并验证模型，就能沿着正确方向持续优化。

真正需要改变的是，让 drug discovery 更像 drug design。之所以叫“发现”，是因为行业常常在寻找 haystack 中的一根 needle：筛选数百万乃至数十亿个分子，试图碰到一个有效分子。

**Sequoia 主持人：**

所以这里并不是把“可以计算”和“必须实验”硬切成两段，而是让模型先把巨大搜索空间压缩到更值得验证的一小部分。lab 仍然给出真值，只是每次进入 lab 的候选不再完全依赖运气。

**Josh Meier：**

对。模型负责把研究者关于形状、结合位置、功能和可开发性的要求变成候选分子，实验负责判断这些要求在真实 biology 中是否同时成立。验证结果再回到模型，推动下一轮设计。工程化的本质是让这个循环可重复、可测量，而不是声称计算机已经替代现实世界。

理想状态是，研究人员先描述目标分子应该具有的状态和性质，再由模型把它实现出来。实验次数可能因此减少，但也可能恰恰相反：当每次实验的 ROI 上升，行业反而会做更多实验。软件工程师因工具提高生产率以后，市场对软件工程师的需求并没有消失；wet lab 也可能出现相同情况。

所以目标不是简单消灭实验，而是改变工作范式，让设计先行，让每次实验都验证一个更有价值的假设。

### 蛋白质 AI 从 2018 年到 AlphaFold 2 的跃迁

**Sequoia 主持人：**

请先描述当前的 state of the art，再回顾五年前、三年前和一年前。最近有哪些重大突破？

**Matt McPartlon：**

过去十年，这个领域发生了很大变化。蛋白质折叠领域长期有一项每两年举行一次的竞赛。组织者会保留一批从未公开、也没有存入数据库的蛋白质作为目标，各学术团队比赛谁能最准确预测结构。

直到 2018 年，性能才第一次出现明显的 step change；2020 年 AlphaFold 2 又带来一次跃迁。真正启动这轮发展的，是 deep learning。

我早期在导师实验室参与过最早的一批深度学习蛋白质结构系统。模型先预测蛋白质中氨基酸之间的距离，再由一个 renderer 根据不完整、有噪声的距离信息生成蛋白质结构。令人惊讶的是，只用相对有限的信息，机器学习系统就已经能生成大体正确、看起来像真实蛋白质的结果。

当时仍缺乏今天这样的分辨率，有点像早期图像生成：画面模糊、颗粒感很强，而现在几秒钟就能生成高分辨率图片。蛋白质模型也经历了类似演进。

最初问题是 protein folding，也就是给定氨基酸序列，预测它怎样折叠。结构预测逐渐可行以后，行业开始解决下一个问题：给定一个蛋白质结构，能否设计一条会折叠成该结构的 sequence？这已经更接近药物设计，因为研究人员开始工程化蛋白质，让它匹配某种形状或执行某种功能。这大约发生在 2021 至 2022 年。

早期系统会先输出氨基酸两两距离，但这些距离既不完整又带噪声，还需要另一个程序把约束拼成三维结构。它能证明 deep learning 捕捉到了真实规律，却不能保证原子级细节。随后模型逐步把结构、序列和相互作用放进更统一的表示，才从“预测自然界已有蛋白质”走向“生成自然界没有、但满足目标功能的蛋白质”。

随后，结构预测与序列设计逐渐结合。diffusion model 的出现，让模型可以同时生成蛋白质结构和序列，并加入更真实的约束。例如给模型一个具有特定形状的 target，再指定希望分子在哪个位置结合。

### 为什么 2024 年是创办 Chai 的时间点

**Sequoia 主持人：**

你们在 2024 年看到了什么，认为那是创办公司的正确时机？

**Josh Meier：**

这个决定经历了很多讨论。我记得在 Matt 家里的一次早期讨论，他向我展示 antibody-antigen structure prediction（抗体与抗原结构预测）的结果。

很长一段时间，行业认为抗体的蛋白质折叠太难。Protein Data Bank 中的抗体数据不够多，因此很多人认为模型解决不了这个问题，antibody design 也遥不可及。早期深度学习蛋白质设计更多聚焦 mini proteins。它们本身很有价值，但并不是大多数制药公司最需要的药物形式。

真正的 holy grail，是在计算机上设计具有治疗功能的抗体。如果连抗体折叠后的形状都不能预测，又怎么可能设计它？2024 年前后，我们开始看到抗体结构预测真正出现成功迹象，设计问题也第一次变得可触及。

mini protein 与抗体虽然都由氨基酸组成，但药物产业的需求并不相同。抗体拥有更成熟的制造、给药和商业基础，也需要模型处理更复杂的可变区与抗原界面。看到模型能跨过抗体结构预测这道门槛，意味着它开始接近制药行业真正愿意部署的形式，而不只是学术上漂亮的蛋白质样品。

### 生物学没有表面上那么割裂

**Matt McPartlon：**

人们常觉得 biology 很吓人，需要记住无数概念。我自己也曾经这样。我没有生物学背景，最初学习纯数学，博士阶段研究 theoretical computer science，直到博士第三年才转向 deep learning 和 protein structure prediction。

刚进入这个领域时，一切看起来非常复杂：antibody 是什么，mini protein 又是什么？但从模型角度看，它们最终都是 amino acid sequences，只是不同类型的 prompt。

ChatGPT 既可以回答数学题，也可以帮助写英文作业。同样，只要找到表示氨基酸序列的方法，一个统一模型也可以预测和设计多类蛋白质。用这个视角看，很多看似割裂的生物问题其实彼此相连。

### Josh 从早期 OpenAI 把 scaling 思想带到蛋白质

**Sequoia 主持人：**

Matt 介绍了自己的背景。Josh，你和团队其他核心成员来自哪些领域？

**Josh Meier：**

我从小就对 AI 和 biology 感兴趣。我的高中有 stem cell lab，我也一直写程序。职业生涯早期加入 OpenAI，当时它还是 nonprofit。我参与了 GPT-1、GPT-2 和 scaling laws。

我当时一直在想：如果模型可以学习 English、German 和 French，为什么不能学习 DNA 与 protein 的语言？此后这就成为我的研究方向，也大致是 Matt 进入该领域的时期。

把 AI 用到生物学，需要找到合适的 deep learning architecture、compute configuration、model architecture 和任务。人们过去认为抗体问题太难，但新的架构开始显示出第一批成功迹象，当时最关键的变化就是 diffusion models。

### Diffusion 为什么适合蛋白质设计

**Matt McPartlon：**

diffusion 出现以前，行业尝试过多种生成模型。有些方法在数据非常多时能工作，图像领域也积累了很多改进技巧，我们借用了其中不少思想。但真正第一次稳定生成合理蛋白质结构，是 diffusion model 出现以后。

**Sequoia 主持人：**

为什么 diffusion 有效？有没有直观解释？

**Matt McPartlon：**

diffusion 不是一步生成。此前一种主要范式是 variational autoencoder，它试图一次把输入分布压缩成类似 fuzzy Gaussian vector。对蛋白质来说，这个任务太难，当时的方法还不成熟。

diffusion 相当于给模型更多思考步骤。训练时先给它一个略有破损的蛋白质，问怎样把它修好一点；再逐渐增加噪声，让蛋白质变得越来越破碎，然后反复教模型完成很小的修复步骤。

生成时，模型只需要一遍遍执行“让它稍微好一点”：修一点，再修一点。把复杂的蛋白质生成拆成大量局部改进步骤，对生物结构特别有效。

**Sequoia 主持人：**

这让我想到和女儿玩的游戏：让 ChatGPT 画一只独角兽，然后不断要求它变得更强，最后得到世界上最强的独角兽。

**Matt McPartlon：**

原理听起来差不多，只是蛋白质当然没有那么简单。

### 怎样组建跨 AI、化学和生物学的 Avengers 团队

**Sequoia 主持人：**

要完成这件事，似乎需要同时懂 chemistry、biology、AI 和工程的一支“Avengers 团队”。你们怎样找到并说服这些人加入？

**Josh Meier：**

我们一直很务实。创始团队最初以 AI researchers 为主，他们懂 scaling model，或者知道怎样让模型在这个领域工作。但每一代模型达到新里程碑以后，下一阶段需要的团队能力都会扩大。

开发 Chai-2 时，我们开始招募世界级 antibody engineers 和 scientists。Andy Young 加入时，有人甚至问 Chai 是否已经转型去做完整 drug pipeline，因为如果 Andy 加入而不自己开发药物，看起来似乎很反常。现在 Andy 在几个月内运行的 antibody campaigns，可能比过去整个职业生涯还多。

Nathan Rollins 也是例子。他在家接受教育，很早就进入大学，14 岁进入后来获得蛋白质设计 Nobel Prize 的 David Baker 实验室，18 岁开始博士研究，拥有很多原创想法。

当模型变得足够强，产品团队也必须跟上。研究人员能把模型推到强大状态，但必须有合适的 interface，用户才能真正使用。联合创始人 Jack 曾在 Stripe 工作；Monaz 曾是 Stripe 代码贡献量最高的十人之一；Neil 经营过 cybersecurity 公司。当我们把系统部署给大型合作伙伴，安全和产品工程就变得非常重要。

这些角色不是装饰性的“跨学科配置”。antibody scientist 要判断候选是否符合真实开发流程，product engineer 要让科学家能准确输入 target、结构修饰和约束，security engineer 要保护药企的专有项目与数据，GPU engineer 则要保证研究人员扩大模型时不会因为基础设施失效而丢掉数周训练。

扩大训练规模以后，还需要擅长 GPU 底层优化的人，避免系统在大规模运行时崩溃。最近一家 hyperscaler 给我们发 Slack，说某个 cluster 的 GPU 过热，可能是 Chai 同时运行得太多。我们的反应是：“这不正是这些 GPU 的用途吗？”至少说明团队在充分使用算力。

### 招人顺序由模型能力决定，而不是提前堆组织

**Josh Meier：**

说服这些人加入，最重要的是结果和明确需求。我们不会在模型还不能设计抗体时先招一批 antibody engineers，因为他们来了也没有真正可以使用的工具。

即使开始招人时，我们仍担心 Chai-2 不能处理 multispecific 等复杂抗体格式。部分专家到岗后的前几周，模型才刚刚进步到能支持他们开展案例。好在模型迭代足够快，能力很快上线。

团队一直保持很小，每个人都略微超负荷，这迫使我们排序，只做最重要的事情。随着模型里程碑变化，团队构成也逐步扩大，而不是一开始就复制一家完整制药公司的全部部门。

**Matt McPartlon：**

研究团队同样强调工程能力。创始工程师 Kevin Wu 开发过最早的 protein diffusion models 之一，执行速度非常快。

Chai 既是 AI research lab，也是 protein design 团队，但最终交付的是 software。因此研究人员也必须是优秀工程师，代码库必须保持高质量。只有把 research talent 与 production engineering 同时维持在高标准，模型才能从论文结果变成合作伙伴真正使用的系统。

### Chai-2 把抗体结合成功率从约 0.1% 提高到约 15%

**Sequoia 主持人：**

AlphaFold 证明模型能预测蛋白质如何折叠，diffusion 证明模型能生成蛋白质。你们最新模型似乎又带来一个 aha moment：生成的分子不只长得像蛋白质，还能具有治疗性质、与目标紧密结合。现在模型生成分子的质量怎样？

**Josh Meier：**

创办 Chai 时，一个核心 thesis 就是聚焦 de novo generation，也就是从头生成分子。当时很多 AI drug discovery 工作，是拿一个已有分子做一点改良，而且要让实验室持续处于 loop 中：获得实验数据，再做一轮优化。

我们问的是，能否把更多工作直接在计算机上完成？是否有足够数据，或者能否采集足够数据，让模型 zero-shot 生成同时具备多种目标性质的分子？

第一步必须把成功率提高。公司成立时，antibody design 的 state of the art 结合成功率大约是 0.1%，也就是设计 1000 个分子，实验室里大约只有一个能与目标结合。

这意味着必须筛选大量分子，也意味着反馈信号非常弱。许多 target 可能完全没有 hit；即使有少数 hit，也不足以统计这些分子是否还具备 drug-like properties。

Chai-2 把成功率提高到约 15%。同样筛选 1000 个分子，可以得到约 150 个 hit。这样就能观察分子性质的统计分布，建立更可靠的 lab evaluations，再继续向上优化。现在我们已经开始把更多目标性质从设计起点就写进生成引擎。

从约一个 hit 增加到约 150 个 hit，不只是“成功分子多了 150 倍”。更关键的是，研究者终于拥有足够样本比较 affinity、manufacturability、稳定性和其他 drug-like properties。过去一个项目可能因为 1000 个候选全部失败而没有任何学习信号；现在即使部分 hit 不适合继续开发，也能从整个分布中判断模型偏差和下一轮应优化什么。

**Matt McPartlon：**

Josh 和我都没想到进展这么快。最初做预算时，我们甚至认为三四年后做到 20% 已经很理想；当时觉得达到 1%，也就是每 100 个分子有一个成功，就会是突破。

实际结果说明，我们采用的哲学和方法确实有效。biology 常被当成 bespoke problem，但底层原则与 self-driving 和 LLM 类似：数据、模型和计算规模共同决定能力。

### Bitter lesson：扩大数据、模型和算力，而不是堆专用模块

**Sequoia 主持人：**

把文字 tokenize 已经很难，把 biology tokenize 又是另一回事。你们怎样找到 scaling laws？

**Matt McPartlon：**

Chai 是一家很相信 bitter lesson 的公司：扩大数据、模型和 compute。要有效扩展，就必须先找到 scaling laws，否则只是在浪费时间和资源。

不透露具体技术细节的前提下，最重要的原则之一就是简单。Chai-1 大约有 23 个独立子模块。如果每次迭代都要理解所有模块及其相互动态，研究速度会越来越慢。我们会不断删除不必要复杂性，找出真正决定性能的部分。结构简化以后，更容易判断损失、数据和算力沿什么方向扩展。

**Josh Meier：**

我们吸收了 deep learning 其他领域的经验，但生物数据不同，Chai 的模型完全从零构建，并不是拿现成 LLM 在蛋白质数据上 fine-tune。

blue-sky research 很开放，因此公司必须坚持少数指导原则：simplicity，相信通过扩大 compute、data 和 model 获得通用能力，以及 rigor（严谨）。

biology 很容易让研究者自我欺骗。wet lab 的 error bar 很大。代码 benchmark 从 16% 提到 17% 或 18%，可能真有差别；生物实验如果误差是正负 5%，几个相近数字可能根本代表同一结果。模型必须带来足够大的 step change，而且要在广泛任务上成立，不能只在一两个案例上好看。

这也是 Chai 不愿为某个演示临时加模块的原因。一个专用修补可能让单项 benchmark 上升，却增加后续训练、调试和产品化复杂度。如果新方法不能随着更多数据和 compute 继续改善，也不能推广到同类 target，它就不是团队想要的 compounding improvement。

### 生物实验虽然慢，却可能比代码更可验证

**Sequoia 主持人：**

biology 常被认为是不容易验证的领域。你们怎样建立 eval，确认模型真的进步？

**Josh Meier：**

我反而认为这是更可验证的领域之一。实验读数非常客观。代码看似可验证，可以检查能否编译、是否通过 unit tests，但代码品味、可维护性和技术债很难完全量化。

设计分子时，我们可以具体测量很多性质。一个分子可能与 target 结合，但能否制造？这类似软件的技术债，却可以用实验测出来。验证不像运行 unit test 那样五秒钟完成，可能需要几天或几周，但至少结果会迫使研究者诚实面对模型是否有效。

eval 的作用首先是指导模型 hill climb，而不是只用于对外宣传。每次模型进步都要通过实验室的 objective readout，再把可靠能力固化成可以交付的产品。

### “难 target”在科学、模型和产品团队中含义不同

**Sequoia 主持人：**

有些 target 可以用传统筛选方法，只是过程慢；另一些则被认为 undruggable。模型目前是在加速已有 target，还是已经能打开过去无法成药的新 biology？

**Matt McPartlon：**

这又回到建模哲学。很多时候，增加第 24 个专用模块似乎能立即解决某个新 target，但我们会问：这个改进能长期维护吗？它只是 incremental patch，还是能复利式提升整个 target class 的通用能力？

例如，我们讨论 protein 的 glycosylation sites 时，可能会想增加特殊表示。但某些 sequence motif 本身就告诉模型这里应该出现糖基化。只要继续压低 loss，模型理应自行学到这种隐藏特征。

如果真正相信 scaling laws，就应相信更好的通用模型会逐步解锁这些 target，而不是每遇到一个问题就堆一个手工模块。当然，这并不取消严谨验证，所有新能力仍要被实验挑战。

**Josh Meier：**

Chai 不同团队对 hard target 的定义甚至完全不同。science team 可能指一个从未被有效调控、难以成药的 GPCR；ML team 可能指模型连结构都折不出来的蛋白质；product team 则可能面对带有多种 glycosylation、又嵌在 membrane 中的蛋白质，不知道怎样让用户准确表达。

这种差异是 feature，不是 bug。各团队从不同方向并行推动，系统就不会只依赖一个瓶颈。Chai 的目标不是做一两个分子，也不是建立只有五个候选药的 pipeline，而是建立面向分子的 computer-aided design suite，改变整个行业发现药物的方式。无论“难”怎样定义，平台都必须处理。

科学团队解决的是分子是否在现实中发挥功能，ML 团队解决的是模型是否理解结构和相互作用，产品团队解决的是复杂 biology 能否被准确表达给系统。任何一层落后，用户都会觉得 target “不可用”。三层同时推进，才能把一次研究成功变成其他药企可以重复使用的设计能力。

### Molecular CAD：把九个月压缩到九周、九天

**Sequoia 主持人：**

“面向分子的 computer-aided design suite”具体是什么？

**Josh Meier：**

它的核心，是让 biology 像工程学。研究者不再从巨大 library 中盲目捞取分子，也不必做无数轮没有方向的试错，而是预先指定分子的设计原则和目标性质，再由 engine 实现一个可在实验室制造的分子。

实验和模型仍会迭代，因为最初 hypothesis 可能是错的。但 CAD suite 可以大幅缩短从 idea 到 testable hypothesis 的时间。

如果今天发现一个分子需要九个月，未来缩短到九周，再缩短到九天，每一个数量级提升都会成倍扩大研究者能够测试的想法。速度和 hard target 最终会汇合：过去难以破解的 target，如果能快速迭代更多假设，也可能变得可以解决。

### 十年后的药物研发：从 first in class 到“最终答案”

**Sequoia 主持人：**

假设 molecular CAD 已经成为标准，wet lab 也吸收了很多创新。从未来往回看，十年后的行业会是什么样？

**Josh Meier：**

第一，药物质量会提高。今天一些 molecule 进入 clinic 时只有目标状态的 80%，因为发现一个分子太难，企业为了时间表仍会推进。它可能帮助部分患者，却可能一年后就被竞争者更好的分子替代。这不是行业资源最有效的使用方式。

第二，一些今天太难的 disease 会变得可处理。行业长期尝试 Alzheimer's，却没有取得足够进展。

第三，一些今天经济上不值得开发的疗法会进入可行范围，例如 personalized medicine 和 rare disease。患者群较小，传统研发成本难以回收；如果设计、实验和上市速度更快、成本更低，小人群适应症也可能成立。

今天企业还会因为时间表推进一个只达到理想状态 80% 的分子，随后被更好的竞品替代。更快的 design loop 不只是提前上市，也允许团队在进入高成本临床阶段以前尝试更多方案，减少把资本投入“勉强可用”分子的概率。由此节省的，不只是发现阶段几个月时间，还可能包括后期失败和重复开发的巨大成本。

**Matt McPartlon：**

过去企业追求 first in class 或 best in class。未来更理想的目标可能是 last in class，也就是做出不再需要被后来产品替代的“最终答案”。

药物会更有 intentionality：针对具体疾病，避免今天许多药物存在的负面相互作用。大量性质最终可以在计算中建模。今天还做不到全部，但已经存在清晰路径。

### 为什么选择平台，而不是自己建立完整药物管线

**Sequoia 主持人：**

外界常把 Chai 与 Isomorphic Labs 放在同一领域。Isomorphic 自己开发药物，而 Chai 帮助现有制药行业更快、更便宜地开发更好的药。为什么选择平台路线？

**Josh Meier：**

两条路线都很好，也都能创造巨大价值。Chai 从一开始就希望建设行业基础设施。我们在 Matt 家看到早期结果时就判断，未来大多数药物会用这种方式发现，那么必须有人把通用基础设施建出来。

创始团队此前也做过 full-stack drug pipeline，把 AI 模型和临床项目放在同一家公司。Chai 更相信 bitter lesson：模型进步以后，新增资金应该继续投入更好的模型，而不是大量转入 clinical trial。

平台商业模式形成一个正循环。模型变好，合作伙伴愿意付费，今天的合作收入又让我们继续投资模型。相比自己承担一条条临床管线，它更容易规模化，也可能对世界产生更广泛影响。

full-stack pipeline 的潜在回报集中在少数成功药物，但资本也会被毒理、临床、注册和商业化长期占用。Chai 选择把资金继续用于 model quality、compute 和通用产品，以合作收入支持下一代模型。它放弃了单个药物的全部经济权益，换取同时服务更多 target 和更多制药公司的可能性。

广泛合作还能防止自我欺骗。如果只做少数 target，公司可能为几个分子做出极其精细的优化，却不知道模型能否泛化到行业当年要开发的另外 500 个分子。

Eli Lilly、Novartis、argenx 和 Pfizer 等合作伙伴不会轻易接受未经验证的结论。原始自动字幕把 `argenx` 识别成了 “Organics”，此处依据 Chai 官方合作清单校正。模型必须真正交付，不能只是偶尔成功，也不能生成一个不完整分子后再让内部 chemists 手工修好。平台路线在很多方面更难，因为合作伙伴会直接检验通用性；但如果做成，回报也更大。

### Pharma 并不排斥 AI，只是要求证据

**Sequoia 主持人：**

真正向制药企业交付以后，你们发现它们的需求或 AI 成熟度与预期有什么不同？

**Josh Meier：**

创办公司时，很多人说 pharma 不懂怎样使用 AI，不是技术前沿行业。实际经验并非如此。制药公司是非常严谨的客户，会测试每一项声明；但看到可靠数据以后，也会迅速加大采用。

Pharma 本来就是 innovation industry。一款药只能在有限期限内拥有 exclusivity，企业必须持续再投资。Eli Lilly 现在是一家万亿美元级制药公司，但如果不能持续推出更多 blockbuster drugs，它不会永远维持这个规模。

这种经济结构迫使企业持续采用新技术。行业竞争激烈，这对患者是好事，也要求每家公司保持领先。只要模型跨过证据门槛，我们看到合作伙伴很快扩大使用，并以非常有创造力的方式部署。

**Sequoia 主持人：**

因此，药企采用慢并不必然说明它们保守，也可能是在等待足够大的、能够超出实验误差的结果。一旦证据成立，专利期限和 blockbuster 更新压力反而会迫使它们迅速行动。

**Josh Meier：**

正是如此。合作伙伴不会因为一段 AI 叙事改变研发流程，但会因为可重复的 hit rate、可制造性和真实项目数据改变。部署速度取决于证据质量，而不是公司是否愿意使用新技术。

**Matt McPartlon：**

合作模式也建立了正确 incentive。模型更好，客户结果更好，合作自然扩大。Chai 一直非常聚焦，内部 science team 也会 dogfood 模型，设计 binder、antibody 等分子，持续探索模型已经能做什么。

当模型解锁一个新 use case，我们会问：现在能生成什么新数据？这些数据怎样反过来训练下一代模型？Chai 从未认为只要做出一个模型就能解决所有问题。模型会经历多次迭代，每次能力提升都会带来新的实验和数据，形成 flywheel。

### 数据从哪里来：结构数据库、序列数据库与实验回流

**Sequoia 主持人：**

Chai 不能像训练普通 LLM 那样抓取互联网文本。训练数据来自哪里，又怎样复利增长？

**Matt McPartlon：**

结构数据的 gold standard 是 Protein Data Bank。自 1970 年前后开始，真实实验室科学家持续把蛋白质和其他分子的 crystal structures 存入数据库。没有这些数据，structure prediction 和 design 就不会存在。

我进入这个领域时采取非常 structure-pilled 的方法：怎样让模型输出 3D coordinates？这既不像 LLM，也不像 image model，是一类独特问题。

Josh 当时采取几乎相反的路径。他是 ESM 的早期作者之一，研究怎样把 language model 用于 protein sequences。

如果训练模型预测蛋白质序列中的 missing amino acid，就像语言模型预测句子下一个词，模型必须理解这个氨基酸周围的 microenvironment。要知道哪些氨基酸与周围环境兼容，它实际上需要理解蛋白质的 3D shape。因此，只学习 sequence，模型内部也会逐渐形成结构表示。

两类主要数据因此是：Protein Data Bank 的结构数据，以及规模可能达到数万亿 token 的 sequence databases。模型足够好以后，可以在海量序列上预测新结构，再把更准确的结构用于训练下一代模型，形成复利效应。

结构数据数量较少但质量高，sequence data 数量巨大却包含重复与噪声。只依赖前者会受样本规模限制，只依赖后者又可能缺少直接三维监督。Chai 把两者结合：用高质量结构校准模型，用海量序列扩大覆盖，再让更强模型从序列推断更多结构。实验室新数据则提供与设计任务最接近的反馈。

**Josh Meier：**

现在有人问 Chai 到底属于 sequence paradigm 还是 structure paradigm。答案是都不是，也都是。团队非常务实，只想解决问题，实际系统当然会结合两者。

互联网上的 biological sequence tokens 甚至可能多于 English tokens，只是其中很多重复、嘈杂或没有直接用途，整理本身需要大量技巧。

更重要的是，模型现在已经能设计送进实验室的新分子。Chai 每次实验都会产生 exhaust data，这些反馈又能改善模型。这与 LLM 的发展类似：我在 OpenAI 时曾尝试对 GPT-1 architecture 做 reinforcement learning，当时基础模型不够好，实验没有成功。base model 达到一定水平以后，新的训练方法才突然变得有效。生物模型现在也开始越过这个临界点，行业重新重视怎样让模型参与数据生成。

### 竞争对手不是另一家模型公司，而是自然和成熟实验流程

**Sequoia 主持人：**

AI protein design 变得很热门，竞争也越来越激烈。Chai 怎样保持在 frontier？

**Josh Meier：**

第一仍是看结果、保持严谨、不自我欺骗。我们做大量 eval，主要为了优化模型。Chai-2 首先把 hit rate 提高到不再需要 large library screening 的水平，几个月后又把 manufacturability 等 developability properties 加入设计。

当新能力出现，我们会尽快强化它，做到 production ready，再交付客户。

但我不把竞争理解成与其他 model provider 一对一较量。所有人真正面对的基准是 nature，以及行业几十年优化出的现有 drug discovery 流程。

Matt 不愿为了短期效果给模型增加第 24 个模块，而传统 wet lab protocol 可能已经积累了第 240 个步骤，并被经验丰富的科学家反复优化。

Andy Young 二十年前在 MIT 参与早期 yeast display，后来在 Pfizer 和 Genentech 积累约 20 年经验，还参与过获批抗体药物。他用传统工具就能做出好抗体。这才是 AI 必须超越的真实门槛。

AI 的长期 ceiling 应该高得多，否则没有必要创办 Chai。目标不是做一只速度快十倍的 mouse，而是创造过去不可能出现的突破性药物。我们认为几个月前已经跨过能推动大型药企采用的拐点，接下来要继续提高质量。

### 最好的部分是结果，最难的部分是大规模可靠运行

**Sequoia 主持人：**

对考虑加入 Chai 的人来说，工作中最好和最差的部分分别是什么？

**Matt McPartlon：**

最好的是所有人都非常 mission-driven。大家努力工作，有明确的共同目标。这种投入程度很少见，可能只在我博士实验室的一些同事身上见过。公司从一开始就有清晰哲学和路线，团队也真正认同它。

如果一定要说不喜欢的，除了办公室不在 Dandelion Chocolate 楼上，真正困难的是让系统在规模化环境中持续工作。

创办 Chai 时我们有 128 块 GPU，我当时觉得一家 lab 拥有这么多算力已经不可思议，因为博士组里四个人只共享八块 GPU。现在基础设施和 compute resources 大得多。

GPU 可以并行，但规模本身带来新问题：怎样长期保持 cluster 健康？怎样让大型训练连续运行几个月？失败后怎样自动恢复？怎样降低通信开销、优化模型并充分利用资源？这些是增长带来的好问题，但仍然很难。

一项训练运行数月时，单块 GPU、网络连接或 checkpoint 流程的小故障都可能扩大成巨大时间损失。系统必须自动发现失败、保留状态并恢复，而不是每次让研究者从头开始。模型研究和 distributed systems engineering 因而不能分开，这也是 Chai 把自己视作软件公司的原因。

**Sequoia 主持人：**

一位 CEO 说过，人要么承受失败的痛苦，要么承受增长的痛苦，当然更愿意选择后者。

**Josh Meier：**

我最喜欢的同样是结果。团队很多人在 AI 领域工作多年，终于把积累用于真正重要的问题。几年前，我们会庆祝一篇不错的 paper，却仍然问：这真的让世界变好了吗？会影响患者吗？现在答案开始变成肯定。

每次出现突破结果、产品新功能帮助客户，或 science team 收到新的 lab result，都会让人兴奋，因为这可能深刻改变世界。

但这也对应最困难的一面：真实合作伙伴已经依赖系统。发布新一代模型时，必须保证没有 bug、没有 regression。公司不能再得到一个漂亮研究结果后就转向下一篇 paper，而要维护 production-level codebase，让更多人可以安全贡献。

联合创始人 Zach 常说，如果希望长期移动得快，短期有时必须稍微慢一点，把基础搭好。不能为了下一个结果随手增加第 25 个模块。全球最大的公司正在依赖 Chai，我们必须承担责任，让系统持续工作。

### Chai 名字的由来

**Sequoia 主持人：**

为什么公司叫 Chai Discovery？

**Josh Meier：**

Chai 来自 Chemistry and AI，我们也确实喜欢 chai tea，办公室里有很多相关东西。

许多 biotech 公司名字很复杂。我们想选一个简单、容易使用的名字，因为公司的使命本来就是让整个药物设计过程变简单。

**Sequoia 主持人：**

这个名字也让不了解 biology 的人更容易接近公司。你们要做的产品本来横跨复杂学科，如果连公司和界面的语言都充满术语，就会把希望使用模型的药物设计者挡在外面。

### 未来 6 至 12 个月：真实项目部署与更可控的分子设计

**Josh Meier：**

我最期待的是已经启动的 deployments。我们公布了几项合作，希望看到合作伙伴把结果真正带上线。模型并没有被放在 shelf 上，而是在真实项目中使用，用于研究会给患者带来严重伤害的疾病。如果 Chai 能为这些项目提供有效分子，就可能改变患者生活。

进展速度令人难以置信。一年前，模型还不能 zero-shot 一个分子并让团队有足够信心认为项目会成功；现在有人可能 zero-shot 一个分子后就判断，可以把项目推进 clinic。再过一年，第一批这类分子甚至可能进入患者体内。

这里的 zero-shot 不是跳过全部验证，而是模型在没有针对该 target 做多轮实验优化以前，就生成具有较高成功概率的候选。随后仍要完成实验、制造、临床前和临床流程。真正改变的是起点质量和循环速度，而不是取消药物安全标准。

Matt 在上一家公司拥有一些用计算机生成分子的专利，现在相关分子已经进入患者。未来几年，会不会有数十乃至数百个 Chai 设计的分子进入人体？这种规模令人震撼。

**Matt McPartlon：**

团队投入很大，有人问会不会 burnout。但当工作不断取得进展时，努力本身非常有动力。下一代模型会比上一代更好，每次又会发现新的问题。

我最期待的是让设计更 controllable。客户带来一个 target 时，我们不应只是希望得到不错的 affinity，而应该能够精确控制结果，例如要求一个特定强度的 binder。很多技术问题已经接近被解决，我希望把它们逐一确定下来，再看它们打开什么新方向。

**Sequoia 主持人：**

Matt、Josh，感谢你们用工程方式改造 biology，也感谢今天分享 Chai 的故事。

**Josh Meier、Matt McPartlon：**

谢谢邀请。
