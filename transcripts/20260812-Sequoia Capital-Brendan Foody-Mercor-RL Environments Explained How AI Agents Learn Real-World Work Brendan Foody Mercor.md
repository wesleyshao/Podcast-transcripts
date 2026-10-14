---
访谈时间: 2026-08-12
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: "2026-08-12T13:00:28Z"
嘉宾名字: "Brendan Foody"
嘉宾公司名称: "Mercor"
参与嘉宾:
  - 姓名: "Brendan Foody"
    公司或机构: "Mercor"
    职务: "联合创始人兼首席执行官"
播客名称: "Sequoia Capital"
播客url地址: "https://www.youtube.com/watch?v=a00xIn5kwhM"
youtube_video_id: "a00xIn5kwhM"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳后结合完整上下文转写为简体中文"
全文提及的关键名词:
  - "RL environments"
  - "reinforcement learning"
  - "RLVR"
  - "Mercor"
  - "Brendan Foody"
  - "behavior cloning"
  - "SFT"
  - "RLHF"
  - "agentic data"
  - "frontier evals"
  - "worlds"
  - "apps"
  - "tasks"
  - "verifiers"
  - "rubrics"
  - "unit tests"
  - "MCP"
  - "CLI"
  - "Apex Agents"
  - "GDPval"
  - "Cursor"
  - "Harvey"
  - "Cognition"
  - "Ramp"
  - "synthetic data"
  - "trajectory analysis"
  - "post-training"
  - "cyber defense"
  - "virtual coworkers"
---

# RL Environments Explained: How AI Agents Learn Real-World Work | Brendan Foody, Mercor

## Transcript

### 开场与话题安排

**主持人：**

Mercor 在过去几个月发展非常快，收入规模从大约 10 亿美元的年化水平增长到约 20 亿美元的年化水平。Brendan Foody 站在企业如何进行 post-training、如何建立自己的 intelligence 这一变化的最前沿。今天先请 Brendan 用大约 15 分钟介绍 RL environments，之后留出时间回答现场问题。

**Brendan Foody：**

今天主要讨论 RL environments。为了说明它为什么会出现，先回顾 data market 的历史，以及这段历史如何连接到 Mercor 的起源。

### 从 crowdsourcing 到 agentic data

2020 年，市场主要处在为 behavior cloning 众包数据的阶段。那时大量数据是 supervised fine-tuning，也就是收集输入和输出；另一类是 RLHF 数据，由标注者在几个模型回答之间选择更喜欢的一个。这个阶段帮助行业推进了 GPT-3 的 fine-tuning，也推动了 ChatGPT 和 GPT-4 的发展。

但大约从 2024 年开始，市场出现巨大转变。行业逐渐离开低技能、以行为模仿为主的 crowdsourcing 数据，进入 agentic data 阶段。问题变成：怎样找到全世界能力最高的专家，让他们协作构建 frontier evals 和 RL environments，帮助下一代模型学习更复杂的工作？软件工程师、律师、医生、银行家等专业人士，可以测量各自领域的 intelligence frontier，再利用这些测量结果改善模型能力。

Mercor 早期的大项目是 deep research。它是最早大规模扩展的 prominent RL agent 之一。Mercor 与各家 frontier labs 合作，逐渐成为领先实验室的主要 agentic data vendor，也服务 Harvey、Cognition、Ramp 等 application-layer 公司。过去 12 个月最令人兴奋的变化，是 agentic data 范式中的 RLVR 开始加入拥有丰富 apps 和 worlds 的 RL environments，让 agents 学会使用人们每天在电脑上使用的各种工具。

这些技术最初是在 frontier labs 里发展的，现在正扩散到 application layer 和各位正在构建的产品。应用公司开始意识到，AI strategy 有三个核心支柱：compute、algorithms 或 researchers，以及自己构建的数据集。数据集往往是最能形成差异化的因素。

### RL environment 的三个组成部分

一个 RL environment 通常包括三个部分。

第一部分是 worlds。它包含真实项目或公司中会出现的全部消息、幻灯片、文档、表格以及其它文件。world 代表 agent 工作时所处的上下文，不只是一个孤立的 prompt。

第二部分是 apps。它们是 Salesforce、ServiceNow、Microsoft 365 等常用应用的高保真 clone，agent 可以通过 MCP、CLI 或其它工具接口与之交互。若希望 agent 真正学会笔记、销售、法律、财务或运营工作，就必须把真实工作中会用到的工具和状态呈现出来。

第三部分是 tasks。task 包含 prompt 和 verifier。verifier 可以是 rubric，也可以是 unit test，既可以用于 evaluation，也可以用于 training。三者组合起来，才形成一个可以让 agent 执行工作、得到反馈并继续学习的环境。

frontier labs 面临的难题，是如何覆盖经济中所有工作的分布：每个领域的 worlds、apps、tasks 都有很多变化。美国 Bureau of Labor Statistics 的 GDPval 体系覆盖 205 个职业领域；但真正铺开时，还要为每个职业考虑对应的应用、场景、文件类型、协作方式和任务。它不是为一个 benchmark 写几道题，而是构建一套能够接近真实工作分布的系统。

### 为什么人类专家仍然不可替代

Mercor 的 talent network 在过去 24 个月使用了大量 expert hours。仅 2026 年第二季度，进入这些环境构建流程的专家工作量就达到约 250 万小时，而且增速仍在加快。原因是必须把 environment 的分布扩展到经济中的每一个类别。

在大多数领域，只有人类能够测量 frontier。数学是少数例外，因为数学可以有干净的 simulation environment，模型能够通过答案是否正确获得相对清晰的反馈。但在制作 slide deck 这样的任务中，模型往往很难可靠地识别自己的错误。让模型给自己的作品打分，有点像让学生自己批改作业。

因此需要专家像教授批改论文、助教批改幻灯片一样制定 rubric。人类学习很大一部分来自周围人的反馈，而不是把所有东西都接入一个干净的 calculator 或 simulation。专家的作用不是机械地写每一条答案，而是理解这个领域的完整问题空间，知道什么是现实、什么是合格、什么是严重错误。

### Verifier 为什么难做

建立 verifier 很难，因为一个任务可能有很多合理路径。比如一个法律 slide deck，可能有十种不同的优秀结构，也可能有几十种错误。要构建全面的 verifier，必须理解整个 solution area，不能只用一个模板去判断答案。

Mercor 会让专家先描述真实工作中的场景，再设计 data room。这个流程和大型律师事务所的项目类似：律师先把现实中处理过的情景写出来，列出相应的 messages、emails、files 以及文件大小等信息，形成完整的资料室。模型可以参与填充资料，就像软件工程师不再完全手写代码，而是编排 agents 更高效地完成工作；但专家仍要控制环境是否真实、重要信息是否完整。

在一个公开的 legal environment 示例中，顶级律所的律师设计了一个真实项目情景，并把 data room 渲染进 Google Workspace 的 clone。模型随后需要回答一个法律问题：在 Oil and Petroleum Act 及完整 data room 上下文下，Star Tanker Tankers International Limited 相对于 Cooper Jefferies Energy Corporation 的 maximum total liability 是多少。关键不只是最终数字，还包括模型是否找到所有相关文件、是否理解法律事实、是否把责任计算过程完整写出。

律师会为这类答案制定 rubric criteria，描述准确模型回答的特征。Rubric 还要避免 reward hacking，也就是模型学会钻评分规则的空子，却没有真正解决任务。把 100 条模型 trajectory 交给 verifier 评分，并保证每个分数都准确，是很有挑战的工程和研究问题。

### Apex Agents 与 post-training 结果

Mercor 会把这些 rubric、data、agent trajectories 组合起来，做 agenda quality control、训练和结果验证，最终形成 high-quality verifiers 和 leaderboards。Leaderboard 给出模型在某一特定领域的综合得分，可以比较不同模型的能力。

Brendan 展示了 Apex Agents 的例子。这个数据集有 1,800 个 tasks，使用约 50 万美元的 compute 对 GLM 47 做 post-training。Corporate law 的表现从 4.7% 提高到 26.6%。更重要的是，这个提升并不只发生在训练用的 Apex Agents 数据上，还较好地泛化到了 GDPval 和不包含相同 data rooms 的 Apex V1。即使只看其它 benchmark，也能观察到一定的 nominal gains。

Mercor 正在与 Harvey 等客户合作，构建对应具体领域的环境。Cursor 是 application-layer 公司拥有自己 industry-leading model 的早期例子，它的模型为客户创造了大量价值。Brendan 预计未来 12 个月会出现更多类似案例：应用公司拥有自己的 intelligence，并把它作为竞争壁垒的一部分。

### 三种数据采购方式

第一种方式是按 task 采购。客户会说，他们需要某个法律领域的 environment data shape，并愿意按每个 task 支付约 2,000 美元。某些 frontier labs 每月可能购买 50,000 个 tasks，因此规模可以很大。有些复杂 task 需要人类花数小时，甚至一个月完成，价格会按具体任务定制。

第二种是 off-the-shelf data。Mercor 已经投入大量资金构建可供多个客户使用的数据集。很多新兴 labs 更偏向购买现成数据，因为没有必要让十家实验室各自重复构建完全相同的数据。一次构建、服务多个客户，可以形成规模经济。

第三种是只提供专家，让客户自己组织专家完成工作。这种 hourly model 曾经帮助 Harvey 招聘律师，但随着客户需求变大，业务通常会转向更大规模的数据产品。

### 如何给 data 定价

现场提问：怎样给 data 定价，怎样判断 data 的价值？

Brendan 的第一种思路是从客户想实现的 model improvement 倒推。客户可能希望在某个 leaderboard 上达到 frontier，供应商就可以估算实现这个目标需要多少 tasks，再据此定价。比如 Nvidia 可能愿意为一个 frontier open-source model 支付非常高的价格，但要把 data、compute、算法和研究人员等所有因素的贡献拆开，并不是简单的商品定价。

第二种思路是成本加 margin。如果一个 task 需要人类工作 10 小时，专家时薪 150 美元，成本基础大约是 1,500 美元，然后再根据任务的差异化程度和 frontier 程度决定 margin。实际价格区间很宽，从 50 美元到 10,000 美元都可能存在。

### Data quality 的两个维度

Data quality 通常包含两个核心问题：realism 和 verifier accuracy。

Realism 是环境是否反映真实工作的分布。要自动化 corporate law，就要确认环境真的是现实律师会遇到的环境，而不是只像法律题。专家会帮助写 outline、安排资料、核对应用状态，并把驱动真实感的 taxonomy 拆出来。

Verifier accuracy 则是评分是否准确。假设用 rubric 给 Kimi K3 的 100 条 trajectories 打分，理想情况是这些结果与人类把 100 条 trajectories 排名的结果相同。Mercor 会使用 trajectory analysis：先 rollout 目标模型的多条 trajectories，再进行评分，让 agentic quality-control system 和人类 review 检查分数是否符合目标。Human feedback evals 或 preference labels 也可以用来评估 auto grader。

### Synthetic data 与专家判断

Brendan 认为，synthetic data 经常被不同的人用来指不同东西。RLVR 本身就是一种对 synthetic data 的下注：不让人类直接写完所有 SFT，而是让模型产生大量 synthetic trajectories，再逐条打分，让模型从这些轨迹中学习。

第二种用法是在构建 environment 和 tasks 时让模型参与。写法律 memo 的律师当然可以使用 Claude 或 ChatGPT 来提高效率，搭建 data room 的专家也应该使用模型。但模型并不能独立决定 legal environment 是否合理，也不能可靠判断自己写出的 memo 哪些好、哪些坏。

人类仍是关键，因为要测量的是超出当前模型 frontier 的能力。若让模型自己提出法律环境，再让它判断自己的法律 memo，信号会很噪声化，无法形成稳定训练目标。需要具备更高领域能力的人类专家建立现实分布、设计任务并验证评分标准，模型则用来扩大专家的产能。

### 为什么 RL environments 现在变得重要

Deep research 是较早的 RL environment 形态，因为它有 tool use，搜索就是模型所在 environment 里的工具。专家通常提供 rubric，而不一定亲自填充大量 apps，所以那是更轻量的环境。

2025 年 apps 变得重要，是因为行业发现，让模型真正有用的瓶颈，越来越多在于模型能否使用 code base 中的上下文和电脑上的工具。如果用户最终会在真实工作中使用这些工具，那么训练数据也必须呈现相应的 data distribution。模型不能只学会在一个聊天框里回答问题，还要学会读文件、操作应用、完成多步骤任务并处理真实状态。

未来仍会扩大 worlds、apps、tasks 三个维度的多样性，但 Brendan 特别提到两个变化。第一是 ultra-long horizon。现在大多数 agents 还没有被训练去处理超过 10 小时的任务，未来要构建人类需要 100 小时甚至 1,000 小时才能完成的任务。

第二是 virtual coworkers。人类工作中 60% 或 70% 的任务可能需要与其他人互动，但现有 evals 测量模型如何与他人互动的比例可能只有约 1%，Tau Bench 只是少数例外。真实工作需要 agent 与同事、客户、供应商和其它 agents 协作，因此社会互动是一个巨大的 realism gap。

### Rubric generation 与 cyber defense

现场提问：能否用模型扩大 rubric generation，让 expert 不再成为瓶颈？

Brendan 说，AI copilot 可以和 expert 一起创建 task 与 verifier。专家观察 trajectory，理解模型在哪里出错，copilot 帮忙整理候选 rubric。但不能直接让一个更弱的模型可靠写出它自身犯错的所有标准。它可能只写对一半，剩下的噪声会让训练无法工作。

因此最需要人的部分通常仍是 task creation。许多 environment 的填充可以大量使用 synthetic data，专家只需要写 outline、保证熟悉真实环境并检查 realism；但 task 本身涉及目标、边界和正确性，通常更依赖专家。若一个模型明显弱于 Kimi K3，某些情况下可以学习 Kimi K3 产生的 tasks，但这只是特定蒸馏场景下的例外。

Cyber defense 或 incident response 可能是 verifier 更容易扩展的领域。因为可以让 attacker agent 和 defender agent 互相对抗，系统能通过攻击是否成功、漏洞是否被修复等结果取得相对清晰的信号。人类主要负责设计真实的 cyber environment、设定多样的系统状态和攻击路径，而不是为每一条轨迹手工打分。

### 如何判断 base model 是否太弱

如果同一数据集用在多个模型上，模型可能得到不同的最终表现。参数规模会影响模型是否 trainable，但 Brendan 更常看 pass at 16 与 pass at 1 之间的差距。

如果模型生成 16 条 trajectories，全部完全错误，那么即使再生成 100 条，也可能只偶然答对一条，模型很难从数据中学习。理想情况是 pass at 1 失败，但 16 条 trajectories 中有一两条成功。这样模型已经在能力范围边缘看到了正确路径，post-training 才有机会把这条路径的概率提高。

这个启发式说明，数据质量不能脱离 base model 讨论。相同的 environment 对较强模型可能是有效的 learning signal，对更弱模型却可能只是不可达的目标。企业在设计 post-training 时，必须同时看数据难度、模型初始能力、trajectory 的成功率和 verifier 的分辨率。

### 企业应该自己做什么

最后的提问是：企业在 RL post-training 中，哪些部分应该自己掌握，哪些部分可以交给合作伙伴？

Brendan 认为，这也是 Mercor 大量 custom data 业务存在的原因。Mercor 可以为关键客户建立完全独占、隔离的团队，构建客户拥有的数据集。客户保留由自身业务产生的 competitive advantage，同时利用 Mercor 已经搭建的 infrastructure、platform 和 talent network。

有些公司会尝试自己构建全部人才网络和基础设施，但 frontier labs 和最好的模型已经说明，与拥有规模经济的 partner 合作通常更有效。专家网络、数据管理、环境平台、质量控制和训练流程都需要长期投入。对 application companies 来说，真正重要的是决定哪些业务知识和生产数据必须自己掌握，哪些重复性基础设施可以通过合作获得。

**Brendan Foody：**

感谢大家。Mercor 希望把最初只在 frontier labs 中使用的 technology 继续带到 application layer，让更多公司建立自己的 intelligence，并通过真实数据和专家反馈训练出真正服务于具体工作的 agents。
