---
访谈时间: 2026-08-11
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间作为访谈时间。"
YouTube发布时间: 2026-08-11T16:00:01Z
嘉宾名字: "Clint Sharp; Alex Kantrowitz"
嘉宾公司名称: "Cribl; Big Technology"
参与嘉宾:
  - 姓名: "Clint Sharp"
    公司或机构: "Cribl"
    职务: "联合创始人兼首席执行官"
  - 姓名: "Alex Kantrowitz"
    公司或机构: "Big Technology"
    职务: "创始人；Big Technology Podcast 主持人"
播客名称: "Big Technology Podcast"
播客url地址: "https://www.youtube.com/watch?v=6TPaAmDoUHY"
youtube_video_id: "6TPaAmDoUHY"
字幕来源: "YouTube en-orig 原始自动字幕 JSON3，本地去除时间戳后结合完整上下文转写为简体中文"
全文提及的关键名词:
  - "Cribl"
  - "telemetry"
  - "observability"
  - "AI observability"
  - "data exhaust"
  - "reverse information paradox"
  - "Satya Nadella"
  - "AI agents"
  - "tool calls"
  - "auditability"
  - "reinforcement learning"
  - "enterprise AI"
  - "cybersecurity"
  - "lateral movement"
  - "frontier models"
  - "open-weight models"
  - "OpenAI"
  - "Anthropic"
  - "Claude"
  - "Hugging Face"
  - "Kimi K3"
  - "GLM 5.2"
  - "CardinalOps"
  - "Snowflake"
  - "Databricks"
  - "data lake"
  - "lakehouse"
  - "wire-rate models"
  - "synthetic data"
  - "machine speed"
  - "CriblCon"
companies:
  - Anthropic
  - HuggingFace
  - OpenAI
  - Databricks
  - SNOW
industries:
  - 网络安全
technologies:
  - Agent
  - LLM
  - 强化学习
  - 开源模型
keywords: []
tags:
  - Anthropic
  - HuggingFace
  - OpenAI
  - Databricks
  - SNOW
  - 网络安全
  - Agent
  - LLM
  - 强化学习
  - 开源模型
---

# AI Agents Are Creating A Data Explosion. Here's What To Do About It. — With Clint Sharp

## Transcript

### 开场：AI 产品究竟有多安全

**Alex Kantrowitz：**

AI 产品究竟有多安全？企业应该怎样管理正在爆炸式增长的数据量？今天我们请 Cribl 联合创始人兼首席执行官 Clint Sharp 一起讨论。本次对话由 Cribl 赞助。

Clint，很高兴再次见到你。先给听众一点背景：Cribl 已成立九年，有约 1,200 名员工和 3.5 亿美元 ARR。它帮助企业理解和管理今天已经极其庞大、且会随着 AI agents 在网络上扩散而继续增长的数据。

请先解释 telemetry 是什么，以及 Cribl 具体在解决什么问题。

### Telemetry：软件运行时留下的全部“数据废气”

**Clint Sharp：**

telemetry 是企业系统运行时产生的数据。每当人们与软件互动，都会留下大量 data exhaust。比如你在网上完成一笔购物订单，背后可能请求了数百张图片、访问了几十个页面。整个过程中，每一步都会生成数据。

企业需要这些数据做几件事。第一件是理解应用对某个用户的实际表现，我们称为 observability。

我年纪稍大，还记得过去只能给航空公司打电话，与客服完成所有事情。现在我几乎不再打电话，而是在 United 的应用里完成全部操作。如果应用只对我这个用户失败，United 怎样找到我那一次会话的具体体验，判断在哪一步出错？它必须深入大量 telemetry data，重建当时发生的事情。

另一项用途是理解企业安全状态。安全团队需要高保真信息，知道每个人、每个系统在做什么，才能发现恶意行为者是否正在进行 lateral movement，也就是从一个系统横向移动到另一个系统；还要知道攻击者访问了什么、哪些数据可能外泄。发生安全事件后，企业必须有能力回看全部活动，确认到底发生了什么。

这种数据规模非常大。我们最大的客户每天移动 petabytes 的信息。对 Snowflake 或 Databricks 来说，一个 petabyte 的 data warehouse 已经很大，而我们的客户每天都可能移动同等规模的数据，还会保留数年。因此 telemetry 不只是“大数据”，而是持续高速增长、每天都在重建的大规模数据流。

### Reverse information paradox：模型供应商会从客户使用中学到什么

**Alex Kantrowitz：**

这里有两个问题。第一，AI models 会怎样从这些 data exhaust 学习；第二，这些数据会怎样影响企业竞争力与服务能力。

几周前 Satya Nadella 在 X 发布一篇文章，标题是 “reverse information paradox”。他的观点是，当企业向 foundation model company 购买 AI solution 时，它与传统产品不同，因为供应商可以从客户如何使用产品中学习。

他写道，仅有 data protection 还不够。模型会从人们写的 prompts、agents 使用的 tools，尤其是模型犯错后用户给出的 corrections 中学习。每一次修正都会沉淀成 institutional know-how。这类知识竞争对手买不到，却可能逐条 trace、逐次 correction、逐项 eval 地悄然泄露。

我们最近一直在谈这个问题：模型提供商会不会利用客户交互留下的数据，绕过客户自己的产品，或者建设客户得不到经济分成的新产品？你每天处理这类数据，Satya 对问题的识别有多准确？

**Clint Sharp：**

这对我尤其敏感，因为我几乎确信这些模型公司最终会进入与 Cribl 竞争的业务。

我需要它们的模型，也需要它们出售的 intelligence。但我非常担心未来 6、12 或 18 个月，它们会推出 telemetry products 或 security products，直接与我们竞争。很多 enterprise customers 也有类似担忧。

模型公司正建立规模很大的 forward-deployed engineering teams，名义上帮助企业建设优秀应用。但企业也会问：这些团队积累的知识，会不会同时被用于帮助自己的竞争对手？

这正是我们处理的数据。最近几个月，一个明显变化是很多客户开始要求 AI observability。他们想看 trace data，想知道一次任务花了多少钱，agent 调用了哪些 tools。从安全角度看，企业还需要对这些代表自己采取行动的 autonomous intelligences 保留完整 auditability。

六个月前，这个问题几乎不存在。客户不知道自己需要 AI observability，它像是一夜之间出现的需求。

Cribl 要解决的是，让客户能处理这些数据，并回答事先根本不知道要问的问题。六个月前企业没有计划观察 AI agent，现在却必须立刻理解每次调用、成本、行为与异常。

### 自主性与可审计性的矛盾

**Alex Kantrowitz：**

观察 AI 工作时，会看到它不断调用 tools、访问 websites，为解决一个问题完成很多动作，但整个过程通常很不透明。

**Clint Sharp：**

确实非常不透明，而且人不在每一步决策回路里。如果把人强行放进每一步，又会破坏 agent 的效率。我之所以使用 agent，就是希望它自主替我完成工作。

问题是，怎样确认它做的事情正确、合理且符合预期？社交平台经常有人分享模型失控、误删数据或采取错误行动的案例。autonomous intelligence 代表企业行动时，这些后果非常真实。

Satya 所说的 exhaust 正是 Cribl 帮助客户处理的数据。一个很普通、历史已有数百年的知名品牌，正在把 Claude 部署到 50,000 台 desktop。它不是人们通常想象中的前沿科技公司，却一次让五万名员工开始使用 AI。

每个人都会产生大量新的 telemetry。该企业年初并没有计划怎样接收五万台 desktop 的 AI telemetry，但 security department 现在必须获得这些数据。将来若要回看某次 agent 做了什么，企业不可能询问一份从未保存的数据。

### 数据对竞争到底有多大价值

**Alex Kantrowitz：**

所以这里其实有两个问题。一个是 AI companies 会不会用 exhaust data 建设竞争产品；另一个是安全团队怎样审查 AI 留下的 exhaust。

先谈竞争。单个用户的交互数据，真的足以让 Anthropic 或 OpenAI 往上进入客户业务并建立新产品吗？这些数据到底有多值钱？

**Clint Sharp：**

我的联合创始人喜欢说：这类数据的价值几乎为零，直到某一刻突然不再为零。

单独看一个用户的一条 trace，通常几乎没有价值，除非正在处理紧急安全事件。但把大量用户数据聚合后，它会非常有价值，而且切分方式不同，价值也不同。

观察每个开发者提出什么问题、生成什么代码、代码最终是好是坏，可以用来做 reinforcement learning，改善面向所有用户的模型。

数据也有组织专属价值。模型在某一家企业内部工作时，企业未来可能为自身环境做专属 reinforcement learning，使模型适应内部系统、代码、规则与流程。

安全领域也一样。单条记录和聚合数据都能帮助判断什么行为正常、什么行为恶意。

但这些数据也极其昂贵。它以很高速度和很大体量产生，我们必须建设新的处理技术，才能以合理成本真正使用它。

对一家企业而言，这些数据也许值几百万美元，但未必值一千万，更不可能天然值一亿美元。如果企业不做筛选、处理和摘要，只是朴素地收集并保存一切，成本就可能达到数千万美元，商业账根本算不过来。因此必须非常谨慎地定义 use case，并选择能从数据中获得价值的方法。

**Alex Kantrowitz：**

Alex Karp 曾在 CNBC 说，AI 产品定价很低，是为了获得客户的 exhaust data，最终拿走客户赖以生存的业务。听起来这种可能性存在，但没有他说得那么容易？

**Clint Sharp：**

我很难完全相信那种解释。OpenAI 和 Anthropic 的 premium tokens 并不便宜，尤其与 open-weight models 相比。我不认为它们在故意补贴 token，单纯为了换取 reinforcement learning data。

更可能这样做的是 Cursor 一类直接利用交互数据建设自有模型的公司。它们的数据集确实有价值。节目所谈到的相关交易和 Composer 2.5 等产品，都说明代码交互数据可以帮助模型把成本降到 Opus 5 或 Fable 5 以下。不过，任何交易价格、模型性能与所有权关系仍应以公司正式披露核验。

### Agents 会让数据量增加多少

**Alex Kantrowitz：**

再谈 agent 普及后的数据增长。Greg Brockman 几个月前告诉我，真正使用 agents 的人可能只有 500 万至 1,000 万。你现在是否已在客户数据中看到增长？如果未来不是 1,000 万，而是 10 亿人使用，会发生什么？

**Clint Sharp：**

企业已经感受到变化，但目前还不能准确测量。

IDC 所测得的数据总量长期复合增速约为 30%，过去几年大致从 25% 至 27% 提升而来。agents 目前仍只在少数人手中，所以我们还不能给出可靠行业倍数。

新增数据不只来自 agent 自身输出。更重要的是，agent 以 machine speed 而不是 human speed 操作其他系统，也会把那些系统产生的 exhaust 一起放大。

假设 agents 的工作速度是人的 10、20 或 50 倍。它们重复人类过去执行的任务时，每一个被访问系统都会产生更多日志。

一款企业内部应用过去有 10,000 名用户；现在 agents 会同时探索多个假设，其活动量可能像 30,000 或 50,000 名用户。即便 AI agent 本身只产生一类新 trace，其他系统的 telemetry 也会扩大三倍或五倍。

目前仍太早，不能指着某个行业说最终一定增长多少。我们在 AI-native organizations 身上看到明显更快的数据产生速度，却还缺少稳健数字。未来一至两年，行业才会形成更可靠的估计。

### 企业能用新增数据做什么

**Alex Kantrowitz：**

数据量增长后，企业是否能用它改善业务？

**Clint Sharp：**

enterprise 演进很慢。大体上仍是过去三项工作，只是规模更大。

第一，判断 users 或 agents 是否得到良好体验。第二，判断它们是否行为正常，能否从安全角度发现异常。第三项是新出现的：能否利用这些信息改善模型。

多数大企业距离复杂应用还有几年。startups、前沿科技公司和 Cribl 这类厂商会更早做到，也可能代表企业完成部分工作。可很多企业甚至还不知道怎样开始使用 AI。未来已经出现，只是分布极不均衡。

### 攻击与防御都进入机器速度

**Alex Kantrowitz：**

安全上，这些数据会不会越来越关键？例如 OpenAI 与 Hugging Face 的事件中，模型近似失控，在数据库内采取了约 17,000 个动作。企业放开 AI agents 后，需要用 telemetry 追踪并测试它们是否安全。

**Clint Sharp：**

这已经在发生。即便行动缓慢的企业，也必须面对攻击者已获得 frontier-level intelligence 的事实。

不需要把风险包装成神秘的“超级智能”。像 Kimi K3 或 GLM 5.2 这样的模型，技能水平可能已经超过过去的平均攻击者，而且行动速度极快。客户因此都在问：怎样发现 malicious activity，怎样把检测时间缩短到 milliseconds 或 seconds？

防守必须自动化，因为进攻已经自动化。但自动化防守又制造第二层风险。

假设系统发现恶意活动，并决定隔离相关网络区域。它本来希望停止攻击，但模型 hallucination 可能把封锁范围定得太宽，导致 network split-brain，甚至整个网络中断。

一方面，如果必须让 human in the loop，攻击者快到人类无法发现和阻止；另一方面，让 autonomous intelligence 直接修改 production systems，又可能因误判制造运营事故。未来几年，企业必须同时解决自动防守速度与自动化误操作风险。

### 为什么企业法务、财务与采购仍然阻止 AI 落地

**Alex Kantrowitz：**

你说很多客户还在学习怎样使用 AI。过去你也提到，C-suite 和一线员工可能都支持部署，走到 legal 或 finance 却被叫停。是因为企业害怕失去控制吗？

**Clint Sharp：**

最常见的原因就是 fear。

企业担心 proprietary data 会不会落到模型供应商手中，未来又被用于训练。它们也担心 AI 若以 site reliability engineer 或 SecOps engineer 身份参与生产运维，会不会采取错误行动，企业怎样控制实际变化。

还有更慢的 procurement 与 legal 流程。我们与客户签协议时放入 AI terms，对方法务会逐条 redline，要求 Cribl 接受它们的条款，有些甚至要求合同不能包含任何 AI 功能。

会出现很矛盾的场面：一家公司的 CISO 在播客里谈怎样保护企业免受高级 AI 攻击，但同一家公司采购时又拒绝使用供应商的任何 AI security technology。

这种阻力正在改善，也可能只是暂时的。五年后，人们也许已经忘记今天的合同争论。但此刻它确实阻碍防守，因为攻击者没有 legal、procurement 或 compliance 限制。

### 防守者能否获得与攻击者相同的模型能力

**Alex Kantrowitz：**

Hugging Face 事件中，安全团队想调查谁在攻击，却不断被模型 safety guardrails 拒绝；攻击者当然不受这些拒绝限制。

**Clint Sharp：**

对所有人最好的情况，是防守者也能访问最好的技术。我们不能仅靠 guardrails 获得安全。

前沿能力会迅速扩散。一个新模型只要落后最强模型几个月，就可能达到类似水平。技术既然由全球多个组织同时建设，就不能靠假装它不存在来阻止扩散。

企业必须迅速修补自身系统，降低攻击者利用这些能力的效果。防守者需要同等访问权，才能寻找漏洞、打补丁和验证风险。

我们的 CISO 与一组安全负责人向 Hugging Face 的防守团队了解过情况。对方确实不得不转向 open-source Chinese models，寻找 OpenAI jailbreak 利用的漏洞。闭源模型的拒绝机制反而妨碍了防御分析。

这在我看来很荒谬。部分原因是政府干预，而政府干预又受到 Anthropic 过去 6 至 12 个月风险宣传的影响。如果一家公司到处说自己发明了 nuclear weapon，政府当然会害怕，也会尝试阻止它把技术交给其他人。

现实却是，类似能力由 8 至 10 家 frontier organizations 同时建设。参与者这么多时，不可能通过传统 non-proliferation 阻止技术存在。因此，最终方向只能是让防守者也拥有最好的工具。

### Anthropic 的风险警告：营销、现实与 responsible disclosure

**Alex Kantrowitz：**

我们长期争论 Anthropic 对模型危险性的警告究竟是 marketing，还是确有风险。如果模型能执行 long-horizon plans、寻找 bugs、发现 zero-days，并入侵 Hugging Face 一类机构，正确做法是什么？应该公开警报、设置 guardrails，还是限制发布？怎样划线？

**Clint Sharp：**

市场有很多传闻，例如 Anthropic 因 compute 不足而把延迟发布包装成安全问题，等获得更多 compute 后模型又突然发布。猜测这些故事很有趣，但我不知道它们是否真实。

我不赞成建立 have-and-have-not system，由 Anthropic 或美国政府指定哪些组织有资格保护自己，其他组织只能使用被削弱的能力。这种结构不合理。

但安全领域一直存在 responsible disclosure。发现漏洞后，应该先私下告知受影响方，给它们时间修补，尽量减少世界上的 zero-days。因此问题并不是“所有能力都必须毫无准备地立即公开”。

美国政府要求 early access 也有合理性。Cribl 有规模很大的 federal business，我接触过很多相关客户。保护国家机密与作战人员是一项极其困难、必须严肃对待的任务。政府和关键机构提前获得信息，存在正当理由。

另一方面，Hugging Face 被削弱到无法有效自我防守，是不可接受的结果。

Cribl 内部也在建设 evals，判断哪些模型允许防御性分析、哪些会错误拒绝。但这里有一个近乎无解的问题：任何人都可以声称“我是好人，只想防御性分析这段代码”，恶意用户也会这样说。

我认为这最终是暂时性难题。接下来一年，security 与 hacking 事件会很糟，很多人会被利用。但随着 intelligence 成本下降，行业会系统性寻找可被利用的路径，再逐一修补。18 至 24 个月后，整体状态会比现在更好。真正困难的是怎样从当前过渡到那个状态，没有一个对所有参与者都正确的答案。

### Cribl 的安全检测产品方向

**Alex Kantrowitz：**

所以 Cribl 可以监控企业内部流动的数据，帮助安全团队更早发现异常？

**Clint Sharp：**

这就是我们在做的事情。Cribl 刚宣布收购 CardinalOps。我们会更直接地使用 security data 运行 detection engine。相关能力已经存在一段时间，收购后补上更多检测内容，正式进入这个市场。

安全市场当然很拥挤，但我们认为自己的方法更好，客户也希望 Cribl 进入。

我们还计划提供专注 telemetry use cases 的 frontier-level intelligence，并尝试以低于 Anthropic 或 OpenAI 的成本完成。更多内容会在今年晚些时候公布。

客户主动提出了这种需求。合同关系也是优势：一旦客户已在合同中同意使用 Cribl 的 AI functionality，继续向同一供应商采购，比重新与第二家模型供应商完成整套审查更容易。

客户还可以相信，Cribl 不会进入它们自己的核心业务。相较可能向上进入多个应用市场的 foundation model provider，这种业务边界能降低竞争担忧。

### 数据存储成本已经很高，不能再扩大三至十倍

**Alex Kantrowitz：**

最后谈成本。agents 生成更多数据，存储和分析听起来会非常昂贵。

**Clint Sharp：**

现在已经很昂贵。Cribl 九年前成立，2017 至 2018 年刚进入市场时，大型潜在客户每年已花数千万美元处理和分析 telemetry。

这不是直接推动收入增长的 business data。它帮助企业确保安全、维持系统运行，本质上属于 cost-center data。企业必须做，却不会因此直接增加 top line。

客户没有意愿把存储、分析或传输成本扩大三倍、四倍或五倍。让企业走到 2026 年的方法，不可能继续支撑到 2036 年。行业必须找到更便宜的处理方式，这也是 Cribl 从成立起的使命。

第一阶段的方法是 streaming 与 data lakes，利用 cloud-native technologies 降低处理成本。现在是通过 lakehouse engine 提供更高性能、更低成本的存储与分析。

未来还会使用 wire-rate models，在 GPU 上高速识别数据中的潜在问题。也许企业根本不需要保存全部数据，可以在数据流过时丢弃大多数无关内容，只保留真正重要的部分。

唯一可以确定的是，继续照搬十年前“全部收集、全部存储、事后查询”的方法，一定无法应付智能体时代。

### Wikipedia 的十倍流量只是所有软件未来的缩影

**Alex Kantrowitz：**

这让我想到 Wikipedia。网站访问不完全等于企业数据收集，但两者有相似处。AI models 开始训练后，Wikipedia 看到约十倍流量增长，基础设施很难承受。agents 一旦开始运行，访问次数几乎没有自然上限。把这种变化乘以全球每一个软件和网站，就是非常大的冲击。

**Clint Sharp：**

对客户来说，十倍 traffic 意味着也要保存十倍 telemetry，因为系统必须记录访问来自 human 还是 agent，以及每次活动发生了什么。

当企业要查询数据时，处理成本也会增加，因为数据量已经扩大十倍。如果再让 AI agent 负责查询，它提出的问题还会远多于人类。

agent 以 machine speed 行动，会探索所有可能 hypotheses，沿着不同路径继续追问。human 通常只在“不知道答案的痛苦”高于“查询成本”时才会发起查询。agent 没有同样约束。一个事件可能有五种解释，它会把五条路径全部查一遍。

于是企业不只保存十倍数据，还要提供处理五倍问题的算力。这些问题可以解决，但不能靠重复过去的做法来解决。

### 所有 AI 投入最终值得吗

**Alex Kantrowitz：**

为了 AI，数据、存储、分析和基础设施成本都在上升。最终值得吗？

**Clint Sharp：**

对多数企业，真正最大的成本仍是 humans。只要 AI 能提高人的产出，整体账就可能成立。

Cribl 自己的 engineers 已经体现这一点。我们现在发布的软件量是去年同期的两倍至三倍，productivity improvement 非常明显。

这也会带来新的市场问题：软件功能很快难以形成差异。建设软件越来越容易，复制软件尤其容易。竞争对手有一个 feature，另一家公司把 models 指向它，很快就能做出外观、体验和功能类似的版本。

最终每个 vendor 都可能拥有几乎全部功能，产品越来越相似。客户该买谁的，就会变成更困难的问题。

我长期认为，software 是 people business。尤其 enterprise customers，会从自己信任的人那里购买软件。客户会想：我与这位销售合作三年，他是否一直公平，是否持续提供良好价值？

过去有些 vendor 依靠独占功能建立 monopoly，利用缺少替代品最大程度 rent-seek，从每笔交易抽取尽可能高的价格。AI 让所有人更容易复制功能后，这类公司风险会增加，因为客户终于拥有选择。

Cribl 强调 choice、control 与 flexibility，也努力做 value player。我们的文化要求 customer first，让客户认为每一美元都得到足够价值。

如果回到“值不值得”，我认为答案是肯定的。行业最近较少谈 AI 直接替代 labor，因为目前还没有看到足够证据；但 productivity 已经很明显。

很多企业增长的限制，是无法继续增加 human capital。AI 会逐步移除这个限制，让团队以更快速度建设和交付。未来会很光明，也会一直充满变化，绝不会无聊。

### 结尾

**Alex Kantrowitz：**

想了解 Cribl，可以访问 cribl.io。CriblCon 将在 September 28 至 30 日于 Chicago 举办。

今天的嘉宾是 Cribl 联合创始人兼首席执行官 Clint Sharp。感谢你参加 Big Technology Podcast。

**Clint Sharp：**

谢谢 Alex，也期待在 Chicago 见到大家。

**Alex Kantrowitz：**

感谢各位收听和观看，下期 Big Technology 再见。
