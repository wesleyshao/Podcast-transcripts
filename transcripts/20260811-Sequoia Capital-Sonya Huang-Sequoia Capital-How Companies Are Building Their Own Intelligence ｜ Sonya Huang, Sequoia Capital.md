---
访谈时间: 2026-08-11
访谈时间说明: "无法确认独立演讲日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: 2026-08-11T12:00:09Z
嘉宾名字: "Sonya Huang"
嘉宾公司名称: "Sequoia Capital"
参与嘉宾:
  - 姓名: "Sonya Huang"
    公司或机构: "Sequoia Capital"
    职务: "合伙人"
播客名称: "Sequoia Capital"
播客url地址: "https://www.youtube.com/watch?v=bMMv0bZzONg"
youtube_video_id: "bMMv0bZzONg"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳后结合完整上下文转写为简体中文"
全文提及的关键名词:
  - "sovereign AI"
  - "open-weight models"
  - "closed model APIs"
  - "model weights"
  - "AI COGS"
  - "latency"
  - "proprietary data"
  - "application layer"
  - "intelligence layer"
  - "AGI labs"
  - "applied research"
  - "evals"
  - "model routers"
  - "harness engineering"
  - "post-training"
  - "mid-training"
  - "pre-training"
  - "online learning"
  - "synthetic data"
  - "RL environments"
  - "context engineering"
  - "MCP"
  - "Harvey"
  - "Factory"
  - "Glean"
  - "OpenEvidence"
  - "Semgrep"
  - "Anthropic"
  - "OpenAI"
  - "NVIDIA"
  - "Kimi K3"
  - "GLM 5.2"
companies:
  - Sequoia
  - Glean
  - Anthropic
  - NVDA
  - OpenAI
industries:
  - 半导体
technologies:
  - GPU
  - LLM
  - 后训练
  - 开源模型
keywords:
  - 主权
  - AGI
tags:
  - Sequoia
  - Glean
  - Anthropic
  - NVDA
  - OpenAI
  - 半导体
  - GPU
  - LLM
  - 后训练
  - 开源模型
  - 主权
  - AGI
---

# How Companies Are Building Their Own Intelligence | Sonya Huang, Sequoia Capital

## Transcript

### 开场：从口号走到技术实践

**Sonya Huang：**

大家早上好，感谢各位到场。今天大约有 80 位被投公司创始人与人工智能负责人在场，一起讨论一个非常及时的主题：拥有自己的智能，也就是 sovereign AI。

今天的活动一半是行动号召，一半是技术实施课。因此我们安排了高密度的技术演讲与演示。目标不只是反复谈“建设自己的 AI”，而是让大家一起学会怎样真正走到那里。各位的时间都很宝贵，我们直接开始。

### Sovereign AI 是什么，又不是什么

先看机会本身。sovereign 的原义是拥有完整自治权的独立国家。相应地，sovereign AI 指企业拥有自己的智能，不依赖外部主体，一直拥有到模型权重这一层。

这里有一个重要限定：我们绝不是要求被投公司停用 Opus 或 GPT。编程智能体、桌面工作和前沿级接口都非常适合使用闭源模型接口。这不是一场要求企业全面退出闭源模型的运动。

我们观察到的实际变化是，越来越多企业希望在产品的某些部分建立自己的 AI 能力，并沿着垂直整合的方向拥有更多智能。今天的内容是为已经开始这段旅程的企业提供工具。

这个想法并不孤立。过去一个月，sovereign AI 的讨论明显升温。Alex Karp、Satya Nadella 等人都公开支持企业拥有自己的 intelligence。上周 Jensen Huang 也带头推动美国继续允许 open-weight models，随后获得近乎一致的广泛支持。

市场传递的信息非常清楚：企业想拥有自己的智能，想自有而不是租用模型权重。根本原因是，智能已经成为太核心、太基础的产品属性，不能完全外包。

### 集中式与分散式 intelligence 的两种未来

sovereign AI 进入 zeitgeist 是好事，因为它对应一种更积极的未来。

一种未来是集中式智能：一个全能 AI 以黑箱形式驱动越来越多全球 GDP，不断吸收世界其他参与者的数据残留和数据飞轮。智能、经济权力和改进能力都集中到单一系统。

另一种未来是分散式智能：世界共同使用一个坚实的基础层，但每个人、每家公司都在上面建设自己的智能。它适配各自的数据、行业、个性化需求、工作方式和品味。生态因此繁荣，个体差异得以保留，不会由一家公司吞下其余所有参与者。

我认为第二种未来更加乐观。Sequoia 已与数十家正在建设自有 AI 的公司合作。从这些案例中，我们看到企业选择这条路主要有四个原因。

### 企业为什么要拥有模型：成本、速度、性能与命运

第一个原因是成本。对毛利率很低、为零甚至为负的企业，sovereign AI 不是锦上添花，而是必需品。这里有一个反直觉现象：AI 产品越成功，AI 销售成本往往越高。因此，最早开始拥有自有模型的，恰恰经常是 AI 部署最先进、调用量最大的公司。

第二个原因是速度。在某些领域，编程是一个例子，网络安全是另一个例子，小型、蒸馏后的定制模型可以胜过大型通用模型，因为延迟是产品体验的核心。

第三个原因是性能。这是相对较新的变化。去年，大多数公司并不是为了获得更好性能才选择拥有智能。现在，开放模型在特定领域经过企业自己的数据训练后，已经可能超过闭源模型。今天后续议程会详细解释怎样做到这一点。

第四个原因是掌握自己的命运。Anthropic 和 OpenAI 与生态中的很多公司合作得很好，这一点值得肯定。但企业越来越希望拥有一套独立的支撑，不让核心产品能力完全取决于外部供应商的接口、价格、路线图和政策。

crypto 时代有一句给 DeFi 用户的口号：“Not your keys, not your crypto。”如果资产由别人托管，它从根本上就不完全属于你。

AI 版本可以写成：“Not your weights, not your product。”如果一款产品要真正属于企业，企业至少应能控制并托管决定其核心表现的模型权重。

### 竞争从 application layer 下沉到 intelligence layer

Pat Grady 在 AI Ascent 使用过一张图，讨论应用层的争夺。过去的判断是，AGI 实验室与应用公司从两个方向争夺最终面向用户的产品：基础模型实验室从模型向上走，应用公司从用户需求向下走。

现在出现了新的动态。战场不再只是应用层，而越来越成为智能层。竞争不只是谁控制产品、UI、商业化和外层包装，而是谁能拥有智能本身，谁能在自己的产品里塑造更优的智能。产品本身就是智能，新的争夺点也从产品表面下沉到智能层。

在我看来，现在最令人兴奋的“新实验室”其实是应用公司内部的应用研究。Harvey、Factory、Glean、OpenEvidence、Semgrep 等公司都在产生有价值的研究。工作范围包括评测、基准测试、运行框架工程，以及用于微调的新算法等。

这说明民主化智能生态正在快速创新。应用公司正成为新一代 AI 实验室。

### 从零到一：四步建设企业自己的 intelligence

假设大家已经认同这个方向，接下来的问题是：怎样从零走到一，再从一走到一百？

我会给出一套带有明确立场的框架和技术路线。它只是起点，每家公司都不同，而且我本人不是工程师，因此不要把它当成唯一答案。

第一步是战略：哪些 AI 能力应该自有，哪些可以租用。

第二步是团队：怎样招募和组织一支能够生产智能的团队。

第三步是可见性：怎样让外部客户和人才看得见企业的研究能力。这一步经常被忽略，却非常重要。

第四步是技术路线：企业需要组装哪些基础模块，才能真正拥有并持续改善自己的智能。

### 第一步：按能力决定自有还是租用

sovereign AI 不是二元选择。企业不是只能在 0% 与 100% 自主之间二选一。真正重要的是，明确划出哪些智能必须自己拥有，哪些可以放心外包。

可以用四个因素判断。

第一是成本：相关模型调用在整体销售成本中有多重要？如果产品每次用户操作都触发调用，成本会不会随着成功而失控？

第二是速度与延迟：低延迟是否属于 P0，也就是不可妥协的最高优先级？

第三是性能：使用企业数据调优开放权重模型，是否可能比通用闭源模型在这个领域表现更好？过去企业常在“不太在乎性能”时使用开放权重，现在某些领域恰好相反。

第四是专有数据：为了改善模型而输入的数据，究竟有多专有，对企业竞争力有多关键？

编程可以说明这种拆分。编程智能体目前大多仍然租用，因为企业需要很强的开箱即用性能，而延迟不是绝对 P0。代码补全则不同：速度极其重要，调用频率又高，接口成本很快累积，因此多数代码补全已运行在企业自有智能上。

网络安全公司也可能主要为了速度、性能和高度定制的后训练而拥有模型。生物科技公司则因专有数据的价值而转向自有模型。

这就是第一套决策框架：不要问“公司是否全面自建模型”，而要逐项问，每一种 AI 能力在成本、延迟、性能和数据专有性上处于什么位置。

### 第二步：团队要像研究实验室，不是平台服务组

建设团队没有单一路径。实验室负责人可以来自研究，也可以来自工程。有人曾在 Apple、Google Brain 做研究；有人先后在 Microsoft、Ramp 承担工程职位。适合哪种履历，取决于公司要做的是更基础还是更偏应用的研究。

组织设计同样重要。传统 AI 团队经常采用中心辐射结构：一个平台团队支持多个 AI 产品或应用团队。很多公司顺手把 sovereign AI 工作也塞给现有 AI 平台团队，我不建议这样做。

拥有智能从根本上不是一项平台服务能力。团队成员必须能快速思考、站在前沿开展研究，并主动生产新能力。他们应该打进攻，而不只是响应其他团队的服务请求。

更好的方法是从头建立小型新团队，必要时把它定义为独立实验室。小团队也能走得很远。Harvey 已发表大量研究，而团队只有七人。因此可以从小开始，但组织使命必须清楚。

### 第三步：研究必须让外部世界看得见

legibility 的重要性被严重低估。我相信现场很多公司已经在内部做出优秀研究，但外部世界未必看得见。

Winston Weinberg 曾说，CEO 的职责有两部分：一是推动 substantive results，二是 control the narrative，也就是让市场理解公司到底在建设什么。我完全同意。

在企业拥有 AI stack 的过程中，legibility 很重要，因为每个买家都在选择自己的 AI champion。客户每天会听到类似宣传，需要判断哪个 vendor 真有能力把自己带到目标状态。客户希望选择真正知道自己在做什么的团队。

因此，企业越来越需要发布自己的研究。legibility 可以表现为高质量 technical marketing、单独命名的 labs 或 research group，以及用很高 taste 发布研究成果。它不是表面包装，而是客户、研究者和潜在人才识别技术能力的必要界面。Sequoia portfolio companies 应认真对待这一点。

### 第四步：从 evals 到在线学习的技术路线

每家公司的路线不同，但一个常见顺序如下。

先完成 strategy，明确 own 与 rent 的边界。

然后定义 evals。这项工作不 glamorous，也不好玩，却是后续所有决策的基础。前期做得越扎实，后续比较模型、训练方法和生产表现时越有把握。evals 必须在最开始就做好。

接下来，企业可尝试 model routers 与 harnesses。有些公司用 out-of-the-box models 已能获得足够好表现，另一些会从 post-training 获得显著提升。更少数的公司需要进一步进入 mid-training 或 pre-training。

最终目标，是让 live customer data 形成 feedback loop。每一次客户交互都能帮助模型和企业 intelligence 改善，而不是把生产数据永远隔离在训练流程之外。

### 2026 年的新变化：自有 stack 可以超过 frontier

拥有 stack 的重要价值，是现在已经可能获得 frontier-level performance。这是一个较新的变化，很大程度上来自最新 open-weight models 的进步，尤其是演讲所提到的 Kimi K3 与 GLM 5.2。

这些模型的 baseline 已接近 frontier。由于 weights 可用，它们比 closed APIs 更具可塑性。配合扎实的 post-training、prompt 与 harness engineering、online learning，企业自己的 stack 有机会在特定 domain 超过通用 frontier model。

这不是说每家企业都一定能做到，也不是说 open weights 在所有任务上更强。关键是，2026 年以后，“拥有模型必然牺牲性能”不再成立。在企业数据和工作流高度专有的领域，自有 stack 反而可能成为 performance edge。

### Production stack 与 development stack

从 infrastructure 角度，可以把体系分成 production 与 development 两侧。

左侧是 production stack，也就是 user-facing intelligence，决定用户最终看到的每一个 token。最简单的抽象是：一个 harness 放在 model 之上。

旁边是 development stack，也就是把 intelligence 做好的工具、数据和 vendors。

在 closed model ecosystem 中，整体结构很简单。底层使用 Opus、GPT 等 foundation models，通常还会附带可直接使用的 harness。企业也可以写自己的 harness、prompts、context 注入和 evals，但一般不必大量收集训练数据，也不必训练自己的 model。

这种结构的 floor 较高：企业很快就能做出不错的产品。但 ceiling 较低：企业无法真正把 proprietary data 和 online production data 变成持续改善自有 intelligence 的资产。

一旦企业决定拥有 intelligence，就像打开 Pandora's box。原来干净的一次 API call，会变成完整模型训练与运维系统。

企业需要选择 open-source base，再做大量 post-training。harness 不再只有一个开箱即用答案，而是要从多个 open harnesses 中选择，并自行配置 logic、tools 与 context。相比一个即插即用的 agent，工程复杂度显著增加。

### Context、数据与持续改进闭环

context 对 performance 极其重要，而且有多种形态。

它可以来自 Turbopuffer 一类 vector database，也可以来自 Glean 一类 enterprise knowledge graph；可以通过 MCP 使用 open-source connectors，也可以采用全新方法。Engram 的 Dan Berman 正在研究把 context 编码进 weights 本身。

当企业拥有 AI 后，development stack 的重要性明显提高。团队必须持续监控 evals，知道自己的 intelligence 与替代方案相比表现怎样，也要观察 model performance 在 production 中是否 drift。

企业还需要大量 high-quality data 做 domain post-training。数据可能是 expert trajectories，可能是 synthetic data，也可能是 RL environments。最后还必须设计 online learning，让每一次 user interaction 都有机会改善系统。

换句话说，拥有模型不是把一个 open-weight checkpoint 部署到自己的服务器就结束。真正的壁垒来自 evals、data、harness、context、反馈闭环和组织学习速度的组合。

### 当天工作坊与结尾

今天安排了一系列 technical workshops，覆盖企业建设自有 AI 所需的关键环节，唯一不包括从零 pre-train 一个 foundation model。

Fireworks 的 Lynn 会讲 post-training。LangChain 的 Harrison 会讲 harnesses 与 evals。Mercor 的 Brendan 会讲 RL environments、synthetic data 等主题。Trajectory 会讲 online learning。

最后，Harvey 会把这些环节整合起来，解释其完整 AI stack 与 strategy。Harvey 昨天刚宣布 Harvey Research，今天很多演讲者也是它的技术合作伙伴。

我们尽可能邀请了 portfolio 内外最合适的讲者。希望大家不仅理解为什么应该拥有部分 intelligence，也能在今天结束时更清楚地知道，该从哪一种 capability、哪一支团队、哪一套 evals 和哪一个 feedback loop 开始。
