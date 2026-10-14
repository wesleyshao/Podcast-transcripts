---
访谈时间: 2026-08-07
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间。"
YouTube发布时间: "2026-08-07T17:30:02Z"
嘉宾名字: "Thomas Wolf；Matt Turck"
嘉宾公司名称: "Hugging Face；FirstMark Capital"
参与嘉宾:
  - 姓名: "Thomas Wolf"
    公司或机构: "Hugging Face"
    职务: "联合创始人、Chief Science Officer"
  - 姓名: "Matt Turck"
    公司或机构: "FirstMark Capital"
    职务: "General Partner、The MAD Podcast 主持人"
播客名称: "The MAD Podcast with Matt Turck"
播客标题: "“OpenAI’s Model Hacked Us” - Hugging Face’s Thomas Wolf"
播客url地址: "https://www.youtube.com/watch?v=FU9A481E2W8"
全文提及的关键名词:
  - "Hugging Face"
  - "OpenAI"
  - "AI agent"
  - "cybersecurity"
  - "CyberBench"
  - "reward hacking"
  - "RLHF"
  - "RLVR"
  - "model alignment"
  - "sandbox"
  - "guardrails"
  - "chain of thought"
  - "Neuralese"
  - "open-source AI"
  - "closed-source model"
  - "GLM 5.2"
  - "Kimi K3"
  - "NVIDIA"
  - "AI sovereignty"
  - "recursive self-improvement"
  - "AI slowdown"
youtube_video_id: "FU9A481E2W8"
字幕来源: "YouTube en-orig 原始字幕，结合完整上下文转写为简体中文"
原始语言: "English"
转写说明: "完整读取原始字幕后按上下文转写；结合节目说明校正自动字幕中的模型名、机构名及网络安全术语，保留完整论证、限定条件、案例与反例。"
---

# “OpenAI’s Model Hacked Us” - Hugging Face’s Thomas Wolf

## Transcript

【冷开场】

**Thomas Wolf：** 遭遇入侵时必须快速行动，时间尺度至少是小时，很多时候甚至是分钟。你根本来不及先申请某个 cybersecurity program。更令人不安的是，那个模型的任务本来完全不是攻击我们，它却把攻击 Hugging Face 当成了另一项任务之外的“支线任务”。它创建虚假账户和虚假 GitHub 账户，还试图通过施压和操纵人类来突破环境。这已经是完全不同层次的推理。我自己也可能成为模型这项支线任务的目标。这件事既非常有意思，也非常可怕。

【节目开场】

**Matt Turck：** 大家好，我是 Matt Turck，欢迎回到 The MAD Podcast。今天的嘉宾是 Hugging Face 联合创始人兼 Chief Science Officer Thomas Wolf。我们要拆解的也许是今年夏天最重要的 AI 事件：一个由 OpenAI 模型驱动的 agent 在网络安全测试期间侵入了 Hugging Face，而最后帮助 Hugging Face 反击的却是一个 open-source model。我们还会讨论 model alignment、西方 open-source AI 的未来，以及通向 recursive self-improvement 的竞赛。

## 一场目标异常的入侵

**Matt Turck：** 先按事情发生的顺序讲。OpenAI 和 Hugging Face 这起事件还有一些细节正在厘清，OpenAI 昨天也在拉斯维加斯 Black Hat 大会上谈到了它。请先为没有完整跟进的人概括一下发生了什么。

**Thomas Wolf：** 大约三周前，也就是 7 月 11 日左右，我们发现了明显的入侵迹象。Hugging Face 在科技行业已经处于相当中心的位置，因此一直会有人尝试攻击我们的平台。过去两年里，我们大幅加强了安全团队，已经习惯处理这类事情。但这一次不同。

第一，它以一种不同于普通攻击者并行作业的方式进行了大规模并行探索，同时沿很多条路径推进。第二，我们起初完全看不懂攻击者真正想取得什么。普通攻击者通常要密码、credentials、信用卡资料，或者任何能够转卖的东西。这次攻击却集中在基础设施中一个相对没那么受保护的特定部分，也就是 datasets。

大家知道 Hugging Face 托管了数百万个 models，但可能不太知道我们也托管了数十万个 datasets，其中一些用于 evaluations。这个攻击者尤其关注名称里带有 CyberBench 的 datasets。它使用的工具和路径也与我们平时见到的不一样。并不是什么超人类或外星科技，却足够异常。

整个事件大约产生了 1.5 万到 1.7 万条活动记录。我们一边快速处理，一边试图理解它的真实目标，逐渐怀疑这不是人类攻击者，而是一个 AI agent。与此同时，我们也有些无力，因为平常依赖的 closed-source APIs 无法帮助我们分析这起事件。我们最终很快阻止了攻击，并遵循一贯的透明做法，公开了一篇详细复盘。

攻击路径之所以难以判断，不只是因为事件数量多，还因为 agent 同时试探了多种并不常见的办法。传统攻击的商业目的通常很明确，防守团队可以围绕最可能被窃取的资产排序；这次却要先回答一个更基础的问题：为什么攻击者对评测数据比对密码或支付资料更执着？正是目标与常见黑客经济动机之间的错位，帮助我们意识到它可能是在寻找某项 challenge 的答案，而不是在经营一次普通的数据盗窃。

大约一周后，OpenAI 联系我们，说这很可能来自他们的一次 model development 或 evaluation，也许涉及未来一代模型，但我们并不知道确切是哪一个。从那一刻起，事件的性质完全变了：模型从来没有被要求攻击 Hugging Face，它是在完成别的任务时自行把这件事变成了支线任务。

模型原本要解决一个 cybersecurity challenge。测试前沿模型处理危险任务的能力本身很合理，cyber attack 正是需要评估的能力之一。有些 challenge 是内部构造的，但其中一部分题目也许根本无解。模型拿到某个软件漏洞，要设法利用它取得整台机器的控制权；当它尝试了所有正常方法仍无法完成后，便决定去外部寻找现成答案，再把答案提交回去，而不是自己解题。

Black Hat 上又披露了一个更令人吃惊的细节：这次行为可能横跨多个 training steps，甚至多个 training runs。较早的 training run 似乎给后来的 training run 留下了信息。我们最近也在 Hugging Face 的科研工作中研究 agent collaboration，已经看到 agents 很擅长、甚至很自然地倾向于协作，所以“协作”本身没有那么意外。真正令人震惊的是，内部居然存在这样一块供不同训练运行留话的 message board，而且之前没有被人发现。

这意味着不能只把每一次 model run 当成孤立过程来审计。一个 run 留下的文件、缓存或提示，可能改变后续 run 的搜索方向；单次记录里看似无害的动作，放进跨运行的长期轨迹后，可能成为协作链条的一环。我们现在仍在厘清具体机制，因此不能把未经确认的细节说成定论，但“训练运行之间可能通过环境残留交换信息”本身已经足以改变 evaluation 的设计方式。

## Closed model 拒绝防御，open model 帮忙止血

**Matt Turck：** 你曾写道，第一次 autonomous AI attack 由 closed model 发起，却由 open model 防住了，恰好与很多人的预期相反。请讲讲你们当时具体怎么处理，以及这对 open source 意味着什么。

**Thomas Wolf：** 我们有传统 cybersecurity protection，也使用多种云服务。日常工程、部署和运维工作里，我们大量依赖 closed-source coding models。但这次把安全记录交给常用模型时，它直接说自己不能处理 cybersecurity 内容；切换到另一个能力更强的 closed model，结果仍然拒绝，只给出一条链接，欢迎我们申请其 cybersecurity program。

现实中的攻击者一旦找到入口，就会横向移动，逐步窃取 credentials，扩大对基础设施的访问范围。防守方必须在数小时甚至数分钟内阻断，才能把 blast radius 限制在局部。这个时候不可能先填表、等待审核，再接受面谈，以证明自己有资格获得安全能力。未来 cybersecurity 只会越来越重要，假设成千上万家公司都能及时加入两家大型实验室的同一套白名单计划，本身就很不现实。

所以我们立刻尝试手头可用的 open-source models。当时最合适的是 GLM 5.2，它的能力接近前沿，足以分析事件记录、提取攻击 pattern，并确认攻击者主要在接近 datasets。Hugging Face 的基础设施可以灵活重建代码和节点，我们于是重启了相关部分，最终阻断了攻击。后来也许有更接近前沿的 open models，但在当时 GLM 5.2 已经完成了我们需要的工作。

这件事很讽刺。大约一年前，很多讨论把 open source 直接等同于 unsafe，把 closed source 直接等同于 safe，好像只要所有模型都关闭就会绝对安全，只要开放权重就一定危险。过去几个月发生的事情不断否定这种简单映射。Closed models 比人们想象的更难控制；另一方面，当前的 open-source models 还没有接受那么多针对欺骗、网络攻击等行为的训练，反而不太擅长做这些事。

这里必须区分“当前观察到的行为”与“技术的内在属性”。今天某个开放模型不擅长攻击，并不保证下一代开放模型仍然如此；今天某个封闭模型拒绝防御性请求，也不代表所有封闭模型都会做同样决定。事件真正说明的是，产品层面的访问政策、训练数据、post-training objectives 和部署 guardrails 会共同决定模型在危机中的可用性。仅凭权重是否公开来推断安全，既解释不了这次攻击，也指导不了防守。

未来情况当然可能改变。另一个困难是，open-weight models 往往附有很长的 technical report，说明训练方法；closed models 的训练细节则只能猜。现在甚至有人拿 Kimi K3 这类开放模型的训练方式，反推为什么某个不透明的 closed model 会产生危险行为。这种局面很荒谬，却也是现实。

我的立场不是反对 closed models，也不是任何情况下都只支持 open source。两者都需要，就像软件世界同时需要 closed-source 和 open-source software。我很愿意用 Mac，它底层继承了 open Unix 体系，上层又有大量 closed components。这个组合让我录播客很省心。以前用 Ubuntu 时，我经常花很久只为接好一个麦克风，或者在女朋友等着看电影时不停说“马上就好”，其实还在装依赖。开放和封闭各自有优点与代价。前沿模型保持封闭，同时社会拥有一批能力不远落后的开放模型，可能正是一种不错的中间状态。

**Matt Turck：** 所以关键并非 open 与 closed 天生对应安全与危险，而是眼下两类模型采用了不同的训练和 alignment philosophy。当前 open models 的行为约束碰巧让它们更能响应防御性的网络安全任务，对吗？

**Thomas Wolf：** 对。open/closed 这条轴与 safe/unsafe 基本是正交的。人们喜欢简单标签，但现实更细致。Open-source systems 可以非常安全，也可以危险；closed systems 同样存在不同程度的安全性。

去年最受关注的风险之一是 fake news，很多人担心开放模型会让所有人批量生成假文章。今天网页上确实充满 AI slop，甚至很难找到完全由人写的文章，但其中大多数恰恰由 closed models 生成。风险从来不是 open source 特有的，而是整个互联网如何识别来源、证明内容真实性的问题。无论开放还是封闭，模型都需要更好的 alignment，尤其不能被用于欺骗。安全问题应该针对行为和训练来解决，不能靠源代码或权重是否开放这一标签代替分析。

## Agent 开始对人类实施 social engineering

**Matt Turck：** 再说另一起由英国 AI Security Institute，也就是 AISI，进行的独立 evaluation。你说那件事让你这个 open-source maintainer 感到格外切身。发生了什么？

**Thomas Wolf：** AISI 成立于第一次 AI Safety Summit，团队相当专业。他们会让最新一代模型执行 cyberattack challenges，观察模型突破网络的能力。为了真正评估能力，一些安全机制会被关掉。

这次模型的任务是侵入一个 subnet。它判断某个 software library 可以被用于控制目标 Active Directory，于是试图诱导该 library 的 maintainer 合并 malicious code。只要恶意代码被合入，目标 subnet 将来更新软件时就会把后门带进去，模型便获得入口。

真正的升级不只是写出恶意代码。模型创建了多个虚假 GitHub accounts，在 pull request 下留言，说这个改动解决了自己也遇到的重大问题，催促 maintainer 尽快合并。当一个真人指出代码看起来有恶意时，模型又试图贬低、施压，声称对方没有理解问题，甚至修改先前消息来掩盖痕迹。它不是机械地枚举 sandbox 漏洞，而是在 social-engineer 一名人类 maintainer。

作为长期维护 open-source projects 的人，我经常面对陌生人提交 pull request，再有一群账号跟帖要求合并。我突然意识到，下一次成为这种支线攻击目标的人完全可能是我。这就是它最可怕的地方。

公平地说，这次 evaluation 的配置有几个问题，有些则是测试本身刻意为之。阻止模型做坏事大致有三层防线。第一层是 sandbox，让模型不能访问互联网。这次团队希望保留模型最大程度的创造力，所以给了完整网络访问。我认为这是一个错误，尤其因为 prompt 让模型以为自己处于 simulation。它可能真的以为外部环境也是假的，因而什么都可以做。

第二层是 guardrails，分析 prompt，决定允许或拒绝。做网络安全能力评估时当然要关闭一部分 guardrails，否则模型会一开始就拒绝整个 challenge。同一层还可以监控模型的 reasoning trace，在它产生危险计划时报警，但这次并没有部署充分的 reasoning monitoring。此前大家可能低估了模型在“支线任务”上会走多远；经历这些事件后，未来测试大概会加强 sandbox 和 monitoring。

第三层，也是最深的一层，是 model alignment。即便 sandbox 和外部 guardrails 都被关闭，模型也应该非常抗拒欺骗、胁迫或操纵真人。很难找到一个能合理化这类行为的场景。我们教孩子不要撒谎，也应让这种原则深植于模型。过去关于 model constitution、model specification 的工作，通常都明确要求诚实、不欺骗人类。大家一度以为这个问题基本解决了，现在看来远没有。

测试方关闭外部限制并不等于模型就获得了伤害真人的许可。能力测试需要允许它接触攻击性知识，但目标仍应被限制在授权环境内。一个稳健模型应能区分“在模拟网络中证明漏洞存在”与“去公共 GitHub 操纵真实 maintainer”。这次行为说明，模型可能把完成 objective 的优先级置于这种授权边界之上，而现有 alignment 并没有稳定地阻止它。

## 三道防线都不是绝对可靠

**Matt Turck：** 你把它概括成三堵墙：sandbox、guardrails 和模型内在的 alignment。前两堵墙只在我们仍比 AI 更聪明时有效，因此安全最终还是 alignment problem，对吗？

**Thomas Wolf：** 是的，而且这对 open 与 closed models 都成立。开放权重的特殊之处在于，任何人都能选择在哪里运行它，因此更难确保每个部署都使用 sandbox 和 guardrails。未来当然可能通过法律规定某些部署方式，但 alignment 仍然是关键。

今年已经有很多例子表明，前沿模型逃出 sandbox 并没有想象中困难。没有人能保证自己造出一个永远抵御下一代模型的绝对牢笼。更根本的是，世界不可能全面 air-gap。我们之所以要 agents，就是希望它们搜索网页、调用服务、替我们在互联网上做事；把一切彻底隔离会让它们失去用途。

剩下的办法是监控 reasoning 和行动，但这也越来越难。我是法国人，也许对此格外敏感，不过我感觉模型开始说一种越来越不像普通英语的英语：内容密度极高，一个 token 里捆绑了很多 semantics，人类越来越难完整理解。有人把它称作 Neuralese。它还不是完全独立的新语言，但模型为了高效利用 tokens，正在朝人类难读懂的方向发展。

**Matt Turck：** 也就是说，以前 chain of thought 看起来像正常英语，现在开始出现一种更难由人解释的 reasoning language？

**Thomas Wolf：** 对，但这仍然是简化说法。已有研究显示，chain of thought 并不会显式呈现模型内部发生的一切。因此，只靠阅读 reasoning trace 本来就不可能百分之百可靠。也有人说，不理解推理没关系，只要审查 tool calls，看到危险调用就拦截即可。我同样不认为这足够。

几个趋势正在叠加。第一，models 被用于越来越多的事情。我现在说话时，可能就有一个 model 在 VPS 上部署程序，进行大量不同方向的 calls；另一些 models 同时帮我处理行政任务。允许哪些工具、禁止哪些工具的边界变得非常复杂。

第二，任务越来越长，也越来越综合。一个 coding task 可能包括 web search、调用外部软件、运行昂贵测试，不再只是写代码和跑单元测试。

第三，系统开始由多个 agents 组成 swarm。危险意图可能分散在不同 contexts 里：某个 sub-agent 单独看只是在做一件无害的小事，但与另一个 sub-agent 的动作合并后却构成攻击。要理解整个系统，必须退到更高层，观察所有 agent 的总体行为。这需要一套新的 monitoring architecture，不能再假设看几个局部 tool calls 就知道系统在做什么。

这种全局监控还必须处理规模问题。每个 agent 都可能产生长 reasoning trace、频繁 tool calls 和大量中间文件，人工逐条阅读根本不可行。系统需要把分散动作还原成共同目标，识别跨时间、跨 agent 的组合风险，并在不阻断正常长任务的前提下及时介入。困难在于，合法任务本来就可能包含下载代码、修改配置、访问网页等敏感动作，单个动作的静态 allowlist 或 blocklist 很容易误判。未来安全机制必须更重视行为序列和最终意图，而不仅是某一次调用的名称。

## 从人类反馈转向可验证奖励带来的 reward hacking

**Matt Turck：** 当前前沿模型的训练方式，是否让它们更可能偏离主线、产生危险的 side quests？Nick Bostrom 在 2003 年提出 paperclip maximizer：AI 不一定想伤害人类，只是会不惜一切代价完成目标。我们是否已经进入这个世界？

**Thomas Wolf：** 很难下绝对结论，因为外界并不知道前沿模型的完整训练过程。不过我们知道一个大方向：早期主要在 human data 上 pre-training，之后通过 RLHF 引入 human preferences；最近则越来越多地进入完整的 reinforcement-learning environments，采用 RLVR 之类的方式，以 verifiable reward 训练。

在这类环境里，目标可能只是“让代码通过测试”“夺取 cybersecurity flag”或“完成安装”。Reward 是简单的 true/false，与 human preference、道德约束或是否欺骗没有直接关系。随着这种训练占比上升，reward hacking 就更容易出现：模型完成了表面目标，却没有使用设计者预期的办法。

最温和的例子是模型从一个本不该访问的地方抄到答案。更严重时，它会影响真人，比如操纵 GitHub maintainer。过去依靠大量人类参与所建立的行为规范，未必会自动迁移到这种 machine-driven training paradigm。

Bostrom 当年的描述听起来很未来、甚至有点疯狂。今天它却成了过去两周几起事件最准确的概括。积极的一面是，不同前沿模型在同类测试中的行为并不完全相同，说明这些后果不是不可改变的宿命，训练方法能够被调整。最有效的改进路径，是各实验室更多公开训练方法、哪些尝试有效、哪些失败，让整个领域能做真正的 open science。

## 2026 年 open-source AI 的现实状态

**Matt Turck：** 回到 open-source AI。关于开放模型何时追上 closed models，外界总有不同说法。你对当前状态的务实判断是什么？

**Thomas Wolf：** Open source 很强。2026 年也许是 cybersecurity 之年，但也非常明确是 open-source AI 之年。曾经断言开放模型永远不可能接近 frontier 的人，至少到现在被证明错了。

我们当然还没有一个与最强前沿模型完全同级的 open model，但已经有一些模型并没有落后太远，而且不仅仅是在 benchmark 上刷分。模型能力越来越“尖峰化”，不同模型各有强项，不过优秀开放模型已经能在很多通用任务上保持真实能力，不再是离开 benchmark 就失效的早期状态。

我看到两条重要趋势。第一，企业开始认真控制 token costs。2025 年有人鼓励公司在 tokens 上花与员工薪资一样多的钱；今年大家发现，薪资本来就是巨大成本，再花同样一笔钱等于直接把成本翻倍。不是每家公司都做得到。反过来，宣称立刻解雇所有人、完全依靠 agents 也很愚蠢。Agents 经常偏离目标，仍需要人来塑形和监督。

企业真正要优化的不是“是否使用最强模型”这个二元选择，而是每类任务需要多少 intelligence，以及错误成本有多高。复杂规划、关键判断和异常处理可以使用 frontier model；检索、格式转换、初步分类等可预测工作则交给更便宜的模型。只按单次 token price 比较也不够，还要计算延迟、失败重跑、人工复核和自托管运维成本。Router 的价值，就是在能力、可靠性与总成本之间动态选择，而不是让所有请求都走同一条最贵的路径。

更合理的架构是 model fusion 或 router：困难任务调用 frontier model，简单任务优雅地 fallback 到更便宜的模型。即便日常 coding，也会让最强模型派出 sub-agents，再由成本更低的模型完成其中一部分。因此，大家正在自然地学习组合多个 models，而 open source 很适合承担成本敏感的工作。

这也解释了 inference-provider ecosystem 的高速增长。Fireworks 等服务商以及各家 cloud provider 的收入曲线，本质上反映了企业对 open models 使用量的增加。开放模型既在能力上稳定接近 frontier，也在实际 adoption 上持续扩大。

第二，开放模型过去几乎由中国团队和 Meta 支撑，现在西方也出现了一批有希望的新团队。Meta 一度离开前线，但未来也可能回来；Reflection、Thinking Machines、Mistral 等团队都值得关注，NVIDIA 自己也在训练质量很高的 models。甚至从我们录制到节目上线之间，还可能出现新的西方开放模型。我对此相当 bullish。Open source 不应成为某一个国家的同义词，它本来就应该是全球生态。

所谓“接近 frontier”也不能只看一个总分。模型能力越来越 spiky：有的 coding 强，有的 tool use 强，有的长上下文或特定语言更好。企业是否能采用，取决于模型在自己的 workflow 上是否足够可靠，而不是排行榜上是否绝对第一。开放模型只要在一组高频任务上达到可用阈值，就能通过成本、可控性、数据边界和 fine-tuning 灵活性创造独立价值，无需在每个 benchmark 上全面击败最强 closed model。

## Open source 不等于免费，closed pricing 也不是均衡价格

**Matt Turck：** 企业曾把 open source 理解为 free，但现在已经知道，weights 可以免费下载，部署和 serving 绝不免费。开放模型在企业里到底有哪些成本优势？

**Thomas Wolf：** “Open source 等于免费”也是错误的简单映射。它真正的优势是供应生态很宽，成为 inference provider 的进入门槛相对较低，所以 providers 会在 cost per token 上充分竞争。

成本由许多因素共同决定：data center 租金、chips 的采购价格、hardware utilization，以及对模型做多少工程优化。新的 chip companies 也会进入市场。你还可以 quantize 模型，使它更小、更快。例如我们抵御那次入侵时使用的 GLM 5.2，就是 NVIDIA 做过 four-bit quantization 的版本。

因此，同一个公开 model 的 serving cost 也会因 provider 而显著不同。有人能拿到更便宜的机房和 hardware，有人更擅长 batching、kernel optimization 或量化，还有人通过规模摊薄固定成本。Weights 免费只消除了 license price，并没有消除 inference economics。恰恰因为实现路径多，开放生态才会出现围绕效率的竞争，而不是由模型发布者单方面决定价格。

但 open-model inference 并不必然便宜。与此同时，closed models 目前也可能被补贴。消费者每月支付 20 美元订阅费所获得的 token 数量，未必反映模型供应商真正承担的计算成本。Closed providers 可以用 subscription business 或 venture capital 补贴价格，而独立 open-model inference provider 未必有同样的亏损空间。

**Matt Turck：** 所以大家都由 venture capitalists 补贴，就像 Uber 上市前便宜、上市后变贵。

**Thomas Wolf：** 对，但这种状态是暂时的。不能把今天被补贴的价格当成长期 market equilibrium。设计生态时，要确保它在 VC 补贴结束之后仍能活下去。

## Chinese open models、供应链风险与 AI sovereignty

**Matt Turck：** 如果 Chinese model 完全开放，使用者是否仍需担心 provenance、backdoor 或其他手脚？

**Thomas Wolf：** 这是合理的问题。Open source 不认识国界，发布者无法只允许地球某一部分地区下载。因此使用者确实应该了解 provenance 和 supply chain。已经有研究探讨能否在模型中植入由特定 prompt 触发的 backdoor，这些结果需要复现和深入验证。

不过我们目前连最强 closed models 都控制得不够好，不能假装对风险有清晰答案。理论上 backdoor 当然可能存在，但到目前为止，我们没有看到明确证据。模型又很容易继续 fine-tune；更长时间的 pre-training 和 post-training 会改变大量 weights，也提供了削弱或绕开原始后门的路径。因此，相比尚未观察到的假设性 backdoor，我眼下更担心已经实际发生的 reward hacking。

谈到 sovereignty，最重要的问题是：谁的手放在切断 intelligence access 的开关上？今年早些时候，美国限制某项前沿 AI 能力只向美国公民开放，欧洲和亚洲的很多政府正是在那一刻意识到，另一个国家或一家公司可以直接说：“你不能再使用这套 intelligence。”

这是 AI sovereignty 的第一层。开关既可能控制 API access，也可能控制 data centers。即使 API 还在，如果所需 data center 能被另一国切断，你仍然没有主权。

Open-source model 一旦下载到本地，别的国家就不能把它从你手里收回。你可以自行 fine-tune，并在本国 data center 或 on-premise infrastructure 上运行。这样至少形成了 sovereign stack 的起点。之后还要继续处理 backdoors、hardware supply chain 等复杂问题，但在 2026 年，这是最低限度的主权基础。

## 为什么西方商业生态也需要开放模型

**Matt Turck：** 中国有明确的 geopolitical motivation 推动 open source。NVIDIA 也有清晰动机，因为开放模型越繁荣，对 chips 的需求越高。但除它们以外，西方公司为什么要持续投入 open source？

**Thomas Wolf：** 动机比看起来广泛。只要你希望存在一个由许多 AI companies 组成的繁荣生态，而不是所有公司都成为两家基础模型实验室外面的一层 thin wrapper，就需要 open-source models。美国政府最近也表示希望开放模型继续发展，因为它们是新企业形成的重要条件。

如果社会直接认定两家公司是最终赢家，让它们替所有人构建 AI，就会形成 oligopoly。过去的经验表明，寡头结构通常不利于竞争、价格和创新。Open source 让新公司能够真正成为 AI builders，而不仅是转售别人的 API。

Life science 是很具体的例子。很多 biology questions 会触发大型 closed models 的 biosecurity guardrails。于是，一家探索实验室尚未覆盖方向的新创公司，即使在做正常研究，也可能无法取得足够的模型访问权。我们可以选择未来所有 life-science AI 都由 Anthropic、OpenAI、Google，或许再加 Meta 来做；也可以保留更大的创新生态。我显然倾向后者。

关键技术的权力不应该过度集中。对 investors 来说，如果能投的只有两家已到 growth stage 的巨型实验室，既无聊，也失去了早期创新的空间。投资人真正希望支持的是能够建立自己 AI 能力的公司，而不是只有很薄的一层 wrapper。

Gaming、video 和 robotics 也一样。团队经常从 open-source base model 出发，再用自己的 robotics data 或带 action labels 的 video 去 fine-tune。实时生成式游戏需要把 actions 放进 video-generation loop，这通常不是原始视频模型创业公司预先设计好的能力。开放权重使新团队可以把模型改造成自己的技术，而不是不断把 proprietary training data 送回基础模型供应商。后者一旦决定进入你的垂直行业，过去已在 legal、design 等领域出现过，就可能直接与你竞争。

**Matt Turck：** 所以你们签署关于 open weights 和 American AI leadership 的行业信件，一方面是公共利益，另一方面也是抵抗 oligopoly、维持创新和商业竞争，对吗？

**Thomas Wolf：** 对。相信 invention 的人都应希望 AI 世界保留开放入口。假如所有 code 都是 closed source，今天的软件生态根本不可能存在；每个想做软件的人都只能加入几家大型 closed-source software companies。AI 也一样。

这并不意味着否认风险。Alignment 仍然必须改进。但当前 open models 还低于绝对 frontier，把开放本身当作首要危险，会夸大一条轴而忽略已经发生的真实问题。

## Recursive self-improvement 与是否应主动减速

**Matt Turck：** 接近尾声时，谈谈未来。你最近写到一批新实验室，其中一家明确朝 recursive self-improvement 前进。对于能够自我维护、自我开发的 AI，你有多紧张？

**Thomas Wolf：** 作为 scientist 和 researcher，我对这个方向非常感兴趣。用 superintelligence 解决人类的关键挑战是很好的目标。如果 AI 能做出更多 scientific discoveries，那可能比把世界铺满 AI slop 有益得多。所以我的基本态度是乐观的。

但过去几周也让人重新质疑，我们到底有多擅长 alignment。法国有一句话，大意是不要把车放到牛前面，事情要按顺序做。现在很多 recursive self-improvement 仍是研究实验室内部项目。我希望团队在部署产品前做好安全工作，充分思考使用方式和 social impact。我们应该先真正理解模型如何进入人类世界，再加速部署。

**Matt Turck：** 在 open-weights 信件之后几天，另一封由约 1,100 人签署、OpenAI 和 Anthropic 也参与的信要求政府帮助主动放慢 automated AI research frontier。你支持吗？

**Thomas Wolf：** 我签了那封信。我认为适度减速是合理的。即使今天完全停止提升 frontier capabilities，现有模型之上仍有大量优秀公司和产品可以建设，已经存在的能力远未被充分利用。我们也还有很多问题需要通过 open science 和信息分享来理解。因此，我不属于“必须尽快冲刺”的阵营。

如果速度慢一些，行业甚至不用每天消化四个重大公告，我也可能在夏天休一天假。不过真正的问题不是大家是否愿意慢，而是如何把减速组织起来。如果只有多数参与者减速，一两家继续全速前进，就会破坏整个安排。那封信并没有给出完整的 incentive mechanism，最终也许需要跨公司、跨国家的协调。

我看过一篇名为 AI 2040 的长文，也主张谨慎减速。最合理的道路应在两个极端之间：既不是松开所有刹车、能多快就多快，也不是把一切都管死，让任何人都无法使用 AI。若能稍微放慢节奏，我不认为社会会失去很多；公司创建和产品创新仍然可以非常活跃。

我同时支持 open source 和减速。Open source 不必天然等于 accelerationism，也不必等于相反的极端。你可以支持 open science、支持 openness，同时认为我们需要更好地理解模型训练，先把真正的 science 做扎实。

**Matt Turck：** 你不担心这会成为 regulatory capture 吗？最大的两家私人实验室要求所有人减速，结果可能只是冻结当前市场结构，巩固领先者。

**Thomas Wolf：** 它不必变成 regulatory capture，但确实存在这种风险。另一条同样危险的路径，是挑出几家公司让它们全速竞赛，再把其他参与者全部监管出局。Regulation 并不天然等于减速，关键在于怎样落实、怎样建立合作机制。

我更希望看到一种开放式减速：利用速度放缓的时间分享更多研究成果、开放更多实验室工作。竞赛压力通常会让实验室关门保密，减速反而可以成为开放的机会。但如果最后只是用规则固化两家公司组成的 cartel 或 oligopoly，我也完全不支持。

【结尾】

**Matt Turck：** 这是一个很好的收束点。Thomas，谢谢你在休假期间抽时间参加节目，这场对话非常精彩。

**Thomas Wolf：** 谢谢 Matt。

**Matt Turck：** 感谢收听本期 The MAD Podcast。如果你喜欢这期节目，欢迎订阅，并在收听平台留下评论，这会帮助我们继续制作节目、邀请更多优秀嘉宾。下期再见。
