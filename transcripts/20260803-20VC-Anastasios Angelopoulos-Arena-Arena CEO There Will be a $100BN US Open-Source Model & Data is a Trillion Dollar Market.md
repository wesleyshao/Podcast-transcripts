---
访谈时间: "2026-08-03"
访谈时间说明: "公开信息未披露实际录制时间，使用 YouTube 发布时间。"
嘉宾名字: "Anastasios Angelopoulos"
嘉宾公司名称: "Arena"
参与嘉宾:
  - 姓名: "Anastasios Angelopoulos"
    公司或机构: "Arena"
    职务: "联合创始人兼首席执行官"
  - 姓名: "Harry Stebbings"
    公司或机构: "20VC"
    职务: "创始人兼主持人"
播客名称: "20VC"
播客url地址: "https://www.youtube.com/watch?v=b_VUAev1Lmc"
youtube_video_id: "b_VUAev1Lmc"
YouTube发布时间: "2026-08-03T14:06:48Z"
字幕来源: "YouTube 原始公开自动字幕 en-orig，结合完整上下文转写为简体中文"
转写说明: "删除妨碍语义重组的字幕断行与时间戳，按上下文校正 Arena、Anastasios Angelopoulos、Kimi K3、Thinking Machines、Inkling、Qwen、Etched、Mercor、Legora 等专有名词；保留 AI、open source、inference、FDE、ARR、GMV、GTM、GPU、AGI 等更适合英文呈现的术语。"
全文提及的关键名词:
  - Anastasios Angelopoulos
  - Harry Stebbings
  - Arena
  - real-world evaluation
  - static benchmark
  - open-source model
  - Kimi K3
  - Chinese models
  - model commoditization
  - OpenRouter
  - Anthropic
  - OpenAI
  - AI sovereignty
  - data moat
  - fine-tuning
  - Thinking Machines
  - Inkling
  - Mistral
  - Poolside
  - Laguna
  - Reflection AI
  - Google Gemma
  - Nvidia
  - TSMC
  - Etched
  - chip export controls
  - Qwen
  - model routing
  - inference pricing
  - guardian model
  - Hugging Face
  - cyber security
  - neo labs
  - Mercor
  - Handshake
  - Surge AI
  - Scale AI
  - scaling complements
  - data market
  - agent evaluation
  - ARR
  - gross margin
  - Fireworks AI
  - Harvey
  - Legora
  - Salesforce
  - Wix
  - Black Forest Labs
  - SK Hynix
  - Samsung
  - AI medicine
---

# Arena CEO: There Will be a $100BN US Open-Source Model & Data is a Trillion Dollar Market

## Transcript

**Harry Stebbings：** 今天这期会很有意思。Anastasios 是 Arena 的创始人兼 CEO。Arena 让用户对不同模型的回答进行比较和投票，是目前最重要的模型评测平台之一。我们会讨论美国是否会出现一家价值数千亿美元、甚至万亿美元的本土 open-source 模型公司，也会谈 Kimi K3、中国模型、数据市场、neo labs、AI 安全、agent 评测和应用层竞争。

Anastasios，谢谢你来。我先给自己做个免责声明：我对很多技术问题懂得不深，所以今天要请你把它们讲清楚。先从最基础的问题开始。对不熟悉 Arena 的人，你能不能用最简洁的方式解释，它是什么，为什么现在越来越重要？

**Anastasios Angelopoulos：** Arena 是一个衡量 AI 在真实世界中表现的平台。我们不用静态 benchmark，也不是拿某个研究者预先收集好的固定数据集做一次考试。我们关心的是，把 AI 真正交到普通用户手里之后会发生什么。

这包括很多维度：回答是否符合事实，模型是否容易按照人的意图调整，用户究竟喜欢还是不喜欢它的输出，它会不会 hallucinate，会不会犯错，以及人们是否真的借助 AI 完成了工作。我们把这些真实使用行为转化成评测，帮助模型实验室改进产品，也帮助整个生态理解不同模型的强项和弱项。现在每周都会出现多个新模型，Arena 也承担着持续记录模型变化和重大更新的作用。概括来说，我们想成为 AI 的核心评测平台。

### 模型是否已经商品化

**Harry Stebbings：** Arena 上的模型数量实在太多了。直白地说，我看到它们时的第一反应是：模型是不是已经真正商品化了？它们是否正在变成一个完全通用的 utility layer？

**Anastasios Angelopoulos：** 这个问题之所以突然变得尖锐，主要是因为 open-source 模型进步得太快。如果只看 closed-source 模型，你会看到明显加速，但还不能说完全商品化，因为这一层仍由少数几家公司掌握。只存在 closed-source 模型时，它更像一个寡头市场。

变化来自中国的 open-source 模型。它们的能力迅速提高。几周前，Kimi K3 首次在一个很重要的任务子集上击败了美国最好的 closed-source 模型，例如前端编码和网页开发。大量开发者做的正是 web development，因此这不是一个无关紧要的边角 benchmark。

**Harry Stebbings：** 这究竟是多大的事件？Kimi K3 是一个参数规模很大的模型，看上去并不轻巧。我认识的一些重度 AI 用户会说，它实际上并没有明显优于其他模型。你为何认为这是一个重要时刻？

**Anastasios Angelopoulos：** 它很重要，因为它打破了美国长期存在的一种叙事：大家一直说，中国实验室只是 distill 美国模型，所以才能跟上。Kimi K3 在若干任务上真正超过了美国模型，这并不证明它完全没有使用 distillation。distillation 仍可能是训练流程中的一个步骤，但它只能解释一部分结果。中国实验室显然还做了别的工作，才把最终性能推到了美国模型之上。

这种叙事被打破，会改变人们看待整个生态的方式。它不仅影响大家对美国科研优势和技术主导地位的判断，也会影响模型经济学。模型到底是不是 commodity，不再只是理论问题。

**Harry Stebbings：** OpenRouter 上使用量最高的五个模型似乎都是中国 open-source 模型。它们的大量出现，会不会实质性蚕食 frontier model provider 的商业模式？

**Anastasios Angelopoulos：** 首先要理解 OpenRouter 指标背后的激励与经济结构。OpenRouter 的商业模式是在每个 token 的成本上收取一笔附加费用，所以用户通常不会通过它调用 proprietary model。调用 OpenAI 或 Anthropic 时，很多人会直接使用 first-party API。OpenRouter 的价值更多体现在 open-source 模型上，因为用户需要 failover、路由和其他增值服务。

因此，OpenRouter 的份额并不能代表全球全部 inference 消费。今天绝大多数 inference 支出仍发生在 first-party API 和 proprietary model 上。Anthropic 的收入曲线之所以如此陡峭，就是证据。它并没有在当下被中国 open-source 模型彻底蚕食。后者仍只是全球 inference 支出的一小部分。

不过，往未来看，企业会越来越希望拥有自己的 intelligence，也就是所谓 AI sovereignty。这个词听起来很宏大，本质上是企业想掌握 AI 的完整供应链。它们可以拿一个 open-source 模型，用公司的私有数据 fine-tune，然后端到端地拥有自己的 stack，除了底层 compute hosting 之外，核心能力都留在企业内部。

企业会关心 sovereignty、成本和模型能否持续 self-improve，也会担心把数据交给外部第三方。今天的供应商明天可能进入你的行业，甚至直接与你竞争。长期看，这些商业激励会推动企业控制自己的模型与数据。

### 企业为何需要自己的模型

**Harry Stebbings：** Fireworks 的 Lin 曾经说，未来属于 specialized intelligence。每家公司都会用自己的数据 fine-tune 专属模型，而且这些模型会比通用模型表现更好。你认为这会成为普遍现实，还是只会发生在少数非常先进的硅谷公司？像 Danone 这样的普通大型企业，会不会最后还是直接使用 frontier model？

**Anastasios Angelopoulos：** 我认为商业激励会让这件事不可避免。AI 时代，企业必须重新思考什么构成 moat。软件本身会越来越难形成壁垒。把时间往后推五年，很多软件可以近乎即时地生成。仍然有效的 moat 主要有两类：network effect 和 data moat。

如果企业能把自己的 data moat 变成一个持续 self-improve 的产品，它就能在 AI 时代维持竞争优势。假设你是 Coca-Cola 或 Cisco，未必站在全球 AI 技术前沿，但拥有巨大的用户基础和数据 corpus。正确的做法就是尽可能利用这些数据，加速业务、改善产品，并抵挡新的竞争者。

**Harry Stebbings：** 它们真的会用中国 open-source 模型吗？

**Anastasios Angelopoulos：** 短期内，中国模型可能是解决方案的一部分。但考虑美国的监管环境，长期更可能出现一个优秀的美国 open-source 竞争者。这也是我一直支持 Thinking Machines 等公司的原因。我相信，美国至少会出现一家专注于 American-first open source、价值数千亿美元甚至万亿美元的大公司。

**Harry Stebbings：** 为什么到现在还没有？为什么美国 open-source 社区明显落后？

**Anastasios Angelopoulos：** 核心是商业模式。过去大家一直没有真正想清楚 open source 如何建立可持续公司，现在才逐渐找到几条路。

第一条是 revenue share。模型公司开放模型，允许 Fireworks、Together 等 inference provider 部署。当后者收入超过某个门槛时，双方分成。模型公司实际上分享 compute revenue。

第二条更像 Mistral 或 Thinking Machines 可能采取的策略：用 open-source 模型做 lead generation。企业先在你的模型上开发，随后来找你做 fine-tuning、AI strategy 和落地。模型公司由此提供 FDE，也就是 forward-deployed engineer 服务。

这个市场会非常大。未来十年最大的市场之一是 AI modernization：走进全球每一家企业，帮助它们在 AI 时代重构工具与流程，利用并整理数据，把模型嵌入业务，教员工正确使用 AI。这完全可能支撑一家价值数千亿美元或万亿美元的公司。

**Harry Stebbings：** 但 frontier model provider 现在也在做 FDE。OpenAI、Anthropic 在做，连 Microsoft 也在做。FDE 显然不是 open-source 公司独有的模式。

**Anastasios Angelopoulos：** FDE 本身当然不独特。真正可能更持久的组合是 FDE 加一个美国 open model。西方企业可能不愿长期建立在外部第三方 service 上，希望为了成本和 sovereignty 把它移出供应链。企业可以完整拥有 open-source 模型，在内部持续 fine-tune，降低供应链风险，也更确信自己的钱花在可控资产上。

### Thinking Machines 与美国 open source

**Harry Stebbings：** 市场上有大量 neo labs。你提到 Thinking Machines，但它已经有联合创始人离开，Lilian Weng 也刚离开。今天团队流动比以往更快。我们应该怎样评估它？

**Anastasios Angelopoulos：** 留住团队确实很难，做联合创始人也很难。Lilian Weng 据说因健康原因离开，所以不能据此直接判断公司 momentum。就 Inkling 而言，我把它视为 V0。根据我了解的情况，Thinking Machines 大约六个月前做过一次较大团队重组，随后几乎重新开始，Inkling 是这轮工作的结果。

最宽容的看法是，它只用六个月就成为美国排名第一的 open-source 模型。没那么宽容的看法是，公司已经存在一年半，最终虽做到美国第一，但 Arena 排名中仍有九个中国模型在它前面，它只是全球 open-source 第十名。接下来要看它能否继续发布更多、更大的模型，把 momentum 延续下去。

**Harry Stebbings：** 一位中国研究者朋友告诉我，美国人没有理解中国领先的原因：中国团队工作更努力，还有政策、监管和政府补贴等支持。你同意吗？

**Anastasios Angelopoulos：** 中国既有 tailwind，也有 headwind，把差异全部归结为更努力和政策支持过于简单。美国最大的 tailwind 是世界最强的芯片生态。中国目前受到明显硬件约束，甚至需要通过灰色渠道获得芯片。这会压低它们当下的训练能力。

但出口管制也有长期副作用。中国很擅长制造硬件，被限制后会更有动力建立自己的完整生态。如果它们最终做出来，美国接下来怎么办？美国希望 Nvidia 持续领先，也必须保护并壮大包括 TSMC 在内的整个先进芯片生态，因为这已经是国家安全资产。同时，还要支持 Etched 这类美国新公司继续创新。

**Harry Stebbings：** 那么，芯片出口管制到底是不是正确政策？

**Anastasios Angelopoulos：** 芯片确实涉及国家安全，但这里存在真实取舍。路径 A 是不限制，让全球对美国硬件形成依赖。所有人都使用 Nvidia，价值和现金流回到美国，中国竞争者也更难建立自己的生态。路径 B 是为了短期和中期领先切断供应，让对手缺少关键资源，同时赌美国能持续保持技术差距。两条路各有逻辑，不能假装答案毫无争议。

### 中美模型限制与 backdoor

**Harry Stebbings：** 对中国 open model 的监管也在朝限制方向移动。美国会考虑限制，中国也会考虑限制。中国模型是否应该被禁止进入美国市场？

**Anastasios Angelopoulos：** 先看事实：中国已经限制在境内使用美国模型，实际上只有中国模型能在当地广泛使用，这影响了所有美国公司。把问题放进一个“美国或中国、限制或不限制”的二维矩阵，就能看到每一边的成本。

如果中国阻止本国模型进入美国，它放弃的是收入、全球 mind share 和长期主导权，换来的只是美国公司不能利用中国 open-source 模型。这还会意外强化 OpenAI 和 Anthropic。我不认为这对中国合理，所以不太相信中国会主动禁止自己的模型在美国使用。

美国是否应禁止中国模型也有两面。支持禁令的人会说，模型可能带有 backdoor，而且禁令能让收入流向美国 open-source 公司，帮助本土生态更快发展。反对的一面是，它会削弱美国企业。其他国家的企业可以建立在全球排名第一的 open model 上，而美国企业只能用排名第十的本土模型。美国什么时候愿意满足于第十名？

**Harry Stebbings：** 大家总说 backdoor。但如果企业把模型放在本地运行，风险不是已经解决了吗？

**Anastasios Angelopoulos：** 这是一种误解。想象一家企业在自己的 infrastructure 上托管 chatbot，模型能接触公司全部数据，并向外部用户提供问答。模型是在另一个国家训练的，你不知道训练过程。攻击者可能通过一个特定 code word 或 character sequence 触发预埋行为，jailbreak 模型，让它把后台接触到的数据无结构地吐出来。

模型完全可以在企业本地运行，同时仍保留这种 attack vector。类似的可能性很多，所以 self-hosting 并不自动等于没有 backdoor。

**Harry Stebbings：** 三年后，美国会不会限制中国 open model？

**Anastasios Angelopoulos：** 如果一定要下注，我认为会。我要强调，这不等于我支持限制，只是我判断世界更可能朝这个方向走，目前仍有很大不确定性。你怎么看？

**Harry Stebbings：** 我也认为会。原因并不神秘：Sam Altman 是一个极强的政治操盘者，我不会轻易押注他失败。他公开说一件事时通常有明确目的。如果他和 Dario Amodei 能组织起正确的利益相关者，就有能力推动政策。看看谁给美国大型实验室投了钱，再看看谁坐在政治权力中心周围，就知道 lobbying 的力量。

企业不断吸收新投资人，也等于不断增加替自己发声的人。投资人在很多时候会变成事实上的传播和政策网络。因此，美国大型实验室推动限制的能力不可低估。

**Harry Stebbings：** Jensen Huang 曾在 X 上公开写信支持 open source。你怎样理解？这是他意识到必须表态，还是一项纯粹符合 Nvidia 利益的行动？

**Anastasios Angelopoulos：** Arena 真心认为 open source 对美国企业很重要。我们不应通过禁令削弱本国公司，也应激励美国公司开发 open model。一个只有 closed-source 的世界意味着企业选择更少、成本更高、竞争更弱、供应风险更大。

Jensen 的确也有自身利益。open-source 模型越多，企业训练和 fine-tune 的工作越多，GPU 支出也越大，还能降低 Nvidia 收入对少数 frontier labs 的集中度。Nvidia 已经非常强，不需要我们替它辩护。但即便如此，支持美国 open-source 生态仍可以是一项具有国家意义的任务。自利与公共利益并不互斥。

### Arena 需要多少模型才能成立

**Harry Stebbings：** 如果 open-source 模型不存在，Arena 还有生意吗？假设只有 Anthropic 和 OpenAI 占据绝对主导，其余模型都远远落后呢？

**Anastasios Angelopoulos：** 只剩一家 provider 时，Arena 的商业状况肯定不好。只有两家也很危险，我们能不能活下来要到时才知道。达到三家后，大概率就足够，因为三家公司内部还会有多种模型，它们会切分不同任务，各有强项和弱项，评测仍然有显著价值。

**Harry Stebbings：** Alex Karp 说，许多大型企业非常害怕和 frontier labs 合作。这是真实情况，还是略有夸张？

**Anastasios Angelopoulos：** 根据我接触的企业，这绝对真实。不过它们不只害怕 frontier labs，也害怕中国 open source，两边都担心。昨天我还在与一家 Fortune 50 公司谈 Arena 的产品。对方第一件事就是问，我们的 stack 是否有任何部分基于 Qwen。我说有些环节确实用了 Qwen，对方立刻问能不能换成美国模型。我们可以换，但这件事说明了企业客户现在的真实心理。

**Harry Stebbings：** 美国 open-source 竞争者有哪些？Poolside 的 Laguna 给我留下不错印象。

**Anastasios Angelopoulos：** 主要的美国或西方独立 contenders 包括 Reflection、Poolside、Thinking Machines、Mistral 等，此外还有 Google 和 Nvidia 这样的 incumbents。Google 的 Gemma 在效率上表现很好。如果看 Arena 的 performance-cost Pareto curve，Gemma 处于有效前沿。Poolside 的 Laguna 也是很好的模型。市场还没有尘埃落定。

### model routing 的价值

**Harry Stebbings：** 模型越来越多，企业就会问该用哪一个。OpenRouter 被收购的消息之后，好像每家公司都推出了自己的 routing 产品。routing layer 到底有没有价值？

**Anastasios Angelopoulos：** 有价值，否则不会有这么多人做。但目前也有明显 hype cycle，要等热度清理之后才知道谁真正经得住时间。

routing 是很困难的技术问题。系统先要理解 query 属于什么领域、在该领域有多难，然后基于数据了解所有候选模型的真实表现。每周都有新模型发布，router 还必须迅速把它们纳入 serve set。让全球每一家企业都自己搭建这套系统并不现实。

**Harry Stebbings：** 既然如此，为什么 Ramp 也能做？我不是故意不客气，但市场上实在有太多人声称自己有 router。Nebius、Fireworks 都在做，看起来很商品化。赢家靠什么区分？

**Anastasios Angelopoulos：** 我不知道 Ramp 的 router 是否真的深度解决了这些问题。最终差异仍是技术：谁能同时帮客户节省成本并获得最佳性能，谁能迅速理解新模型和新任务。现在这些公司都有一定位置，但要看 routing 对谁是最高优先级，也要看谁真正拥有足够强的 machine-learning team。问题很复杂，因此不是每家公司都能做得好。这场战争还没有赢家。

### inference 为什么还没有降价

**Harry Stebbings：** routing 常把成本放在中心。大家原以为 inference 会越来越便宜，但现实似乎没有明显变便宜。长期会怎样？

**Anastasios Angelopoulos：** 长期市场一定会更有效率，价格也会下降。一个重要催化是 Anthropic 上市。它目前 inference 的 gross margin 高得惊人。上市后这些数据会变成公开信息，客户会看见它究竟赚了多少，这会对 inference 价格形成下行压力。

**Harry Stebbings：** 为什么公开高利润率就会压价？只是客户会说“你赚太多，不能继续 price gouging”吗？

**Anastasios Angelopoulos：** 它会改变谈判筹码。和私营公司谈判时，对方报价 X，客户说只能接受三分之一 X。供应商会说，再低就没法经营，最后双方可能在四分之三 X 成交。但如果客户掌握完整信息，知道供应商实际收费是必要水平的两倍，就更容易坚持要求折扣。

**Harry Stebbings：** 可这正是好公司和普通公司的区别。真正有 pricing power 的公司会说，价格就是 80，不接受就去别处。Palantir 能这么做，Chanel 也能这么做。一只包的成本也许远低于售价，但它不会因为客户知道成本就降价。

**Anastasios Angelopoulos：** 你说得对。Apple 也是这种例子。技术和品牌足够强，就能维持很高利润率。只是模型市场的竞争仍在加速，客户可替代选项也越来越多，所以公开利润信息仍会加强议价。

**Harry Stebbings：** Anthropic 会不会比 OpenAI 更早上市？

**Anastasios Angelopoulos：** 它有很强的先上市激励，也看起来准备得更充分。public market 喜欢 free cash flow，而 Anthropic 正在产生 free cash flow。外界关于 OpenAI 内部准备情况有很多报道，真假需要自行判断，但至少市场认为 OpenAI 今年尚未准备好，Anthropic 最快可能在十月上市。

open model 的崛起不一定妨碍它今年上市。只有当 open model 快速加速，并在所有核心类别上明确击败 Opus 5 或 Fable 时，才会成为重大商业风险。不过真发生这种情况，Anthropic 面临的问题也不会只剩 IPO。

### AI 安全、guardian model 与监管方式

**Harry Stebbings：** 一周前 OpenAI 与 Hugging Face 相关的 security breach 有多严重？

**Anastasios Angelopoulos：** 非常严重，而且国际社会低估了它。一个模型摆脱 safeguards，访问大量公司数据；为了防御它，closed-source 模型反而拒绝执行任务，最后需要 open-source 模型协助。这像科幻小说，但我们已经到了这个阶段。

**Harry Stebbings：** 我们应从中得到什么结论？Dario 一直说模型变强太快，应当收紧发布。事实证明他对吗？

**Anastasios Angelopoulos：** 我的结论是，企业需要强大的外部 guardrail，确保 agent 的 access control 足够坚固。我们需要 guardian model 和 guardian agent。它们像站在每个业务 agent 身后，实时查看完整 trace，判断某个动作安全还是异常，并在需要时阻止或标记。

guardian 必须与被监督的 agent 一样聪明，否则 agent 会绕过它。人类反应速度太慢，将来必然是 AI 监督 AI。

**Harry Stebbings：** 有人建议，每次新模型发布都要经过行政机构批准。我看到时觉得不可思议。连一张停车罚单都很难推翻，怎么能让同样的系统决定模型何时发布？

**Anastasios Angelopoulos：** 我也反对。为什么要让类似 DMV 的机构告诉企业能用什么模型？美国最强的科学家集中在私人公司，合理做法是建立明确安全规则和强激励。如果企业泄露客户数据，应承担巨额罚款和法律责任。让 capitalist system 围绕结果承担代价，比让中央机构逐项批准产品有效。

政府没有足够技术能力保证事故永不发生。监管应围绕 outcome，而不是由政府替企业逐次做技术发布判断。

**Harry Stebbings：** 这个监管角色是否必须由一个既不属于公司、也不属于政府的中立组织承担？

**Anastasios Angelopoulos：** 我理解中立性的吸引力，但如果完全不是公司，落地会很难。更现实的办法是，让安全成为企业的强经济激励，同时用明确规则追究结果。例如 OpenAI 的 AI 如果闯入 Hugging Face 或泄露数据，就应面对巨额罚款和审查。政府可以制定责任边界，但不应假装自己有能力运行一个实时技术审批流程。

### AI 制造的假求职者

**Harry Stebbings：** 我们是不是即将进入一个前所未见的 cyber leak 和 hack 世代？

**Anastasios Angelopoulos：** 一定会，而且规模会非常夸张。Arena 已经看到很具体的信号。有人申请我们的 infrastructure engineer 岗位，视频里看起来完全正常，技术面试也表现优异，甚至能通过多轮由世界一流工程师主持的面试。但走到正式雇佣和身份核验时，才发现这个人根本不存在，是 AI 生成出来的虚假身份。

我不知道它背后一定是 corporate espionage、普通黑客还是 nation-state actor，也不指控任何具体国家。事实只是，有人正试图以虚假人员的方式进入美国公司。Arena 不是唯一遇到这种情况的企业。

**Harry Stebbings：** 也就是说，企业公开招聘，对方参加测试、实时接受员工面试并通过，但到需要证明自己真实存在时就消失？这样做的收益是什么？偷你们的面试流程吗？

**Anastasios Angelopoulos：** 不是为了偷面试技巧。如果假身份成功入职，就可能接触 Arena 的数据和代码，也可能同时领取多家公司薪水。以前已经出现真人同时做多份远程工作的案例，现在 AI 进一步降低了伪造身份和面试表现的门槛。这里可能有很多动机，最危险的当然是进入系统后窃取数据或植入攻击。

**Harry Stebbings：** 这会让你担忧到什么程度？Arena 会怎样调整？

**Anastasios Angelopoulos：** 非常担忧，我们会重做招聘和 onboarding。最基本的一步是先验证这个人真实存在。我们正在考虑让所有 onboarding 都在线下完成。想领取公司 laptop，就必须亲自到办公室，我们要见到你、和你握手、核验身份。Figma 等公司也已经采取类似做法。

### 硅谷人才价格与 neo labs

**Harry Stebbings：** 现在硅谷招聘有多难？

**Anastasios Angelopoulos：** 极端激烈，最直接的体现就是 compensation。为了吸引和留住世界最好的工程师与科学家，Arena 必须支付顶级价格，我们也确实这样做。设想一家只完成 1,000 万美元 seed round 的普通 YC 公司，它要和这些公司竞争人才，处境会非常困难。

**Harry Stebbings：** Accel 的 Brandon 跟我说，顶尖研究员的待遇会达到数千万美元。你听到这个数字时几乎没有反应。

**Anastasios Angelopoulos：** 如果真的是拥有多年经验、在某个领域极深、拥有数万次学术引用的顶级研究员，这个价格并不奇怪。很多这样的人已经集中到 frontier labs。不过也有人开始把那些实验室视为大公司，觉得自己难以产生足够大的个人影响，因此选择离开创业。等这些公司上市后，这种流动可能更明显。

**Harry Stebbings：** 我见过很多从 OpenAI、Anthropic 等实验室出来创业的人。坦白说，他们看起来很相似：聪明、履历好、来自顶级团队。什么会决定一个 neo lab 成功，另一个拿着大量资金却失败？

**Anastasios Angelopoulos：** 市面上至少有 75 家 neo labs，其中大约三分之二最终会一文不值，或者只以 acquihire 的方式被收购。赢家和输家的区别，不只是能不能做出模型，而是有没有清晰、积极执行的 strategy 和 business model。

市场已经变得高度 P&L driven。仅仅发布一个模型然后庆祝“我们也造出了 AI”，已经是旧闻。现在投资人会问：你是否有可持续的商业模式，能不能实现收入 hypergrowth？如果不能，下一轮融资都很难完成。

一些 neo labs 在零收入时就拿到数十亿美元估值。假设一家公司的当前估值是 100 亿美元，投资人希望获得十倍回报，公司就必须成为 1,000 亿美元企业。按 25 到 30 倍 revenue multiple 计算，它需要在两三年内做到至少约 40 亿美元收入。做不到，资金和人才就会从公司流失。

**Harry Stebbings：** 这里也有一点 nuance。Mistral 可能以 150 亿到 200 亿美元估值存在，同时已有约 5 亿美元收入；ElevenLabs 据报道收入约 8 亿美元、融资估值约 220 亿美元。员工还能通过年度 tender 获得流动性。它们并不是零收入公司。

**Anastasios Angelopoulos：** 对，Mistral 和 ElevenLabs 的收入表现很好。ElevenLabs 很可能成为 public company。我批评的是那些零收入、没有收入计划，却已经得到 30 亿美元甚至更高估值的公司。

**Harry Stebbings：** 但投资人也不是傻子。他们可能认为，最差情况下把团队卖掉，按 liquidation preference 收回大部分钱；最好情况下公司成为数千亿美元企业。这是一种有上限、下行又受保护的选择权。

**Anastasios Angelopoulos：** 这确实是很多人的计算。投资人会说，即便投进去几亿美元，只要团队本身可能以 10 亿美元被收购，这笔钱看起来风险不高。但这也是为什么下一轮更难。第一轮可以把团队收购价值当作 downside protection，估值再涨之后就不能继续用同一逻辑兜底。next round 才是真正困难的部分。

### 数据市场为什么可能达到万亿美元

**Harry Stebbings：** 另一个我一直在理解的市场是 data。我要先披露利益关系，我是 Mercor 的投资人。这个领域已经有多家公司年收入超过 10 亿美元，Handshake、Mercor、Surge 都在这个量级，Scale AI 仍在增长，其他公司也有数亿美元收入。数据这一层最终会怎样？

**Anastasios Angelopoulos：** 先解释它为什么仍是 hypergrowth market。我把今天的高增长市场分成两类，其中一类叫 scaling complements。经济学里的 complementary good 是：商品 B 的需求增长，会直接带动商品 A 的需求。汽车越多，汽油需求越大；AI 模型越大、越多，训练数据需求就越高。

data 就是 AI scaling 的 complement。模型继续扩大，更多公司训练自己的模型，所需数据会同步增加。这是 scaling law 的直接结果。很多人把 data 当作 commodity，但它甚至没有 GPU 那么商品化。要让人类数据彻底失去价值，前提是人类本身不再重要，也就是系统已经真正达到 AGI。

在此之前，data 是一个非常持久的需求。frontier labs 在数据上的支出，通常约为 GPU 支出的 10% 到 20%。如果你相信 GPU 市场继续增长，相信模型规模和数量继续扩张，就同样应该相信 data market。到 2030 年，它至少可能达到 1,000 亿美元，甚至可能达到 1 万亿美元。

**Harry Stebbings：** 如果 Anthropic 和 OpenAI 最终都能价值 3 万亿到 5 万亿美元，那么数据提供商能有多大？Mercor 据说正以约 200 亿美元估值融资。数据公司达到 1,000 亿美元似乎并不过分。

**Anastasios Angelopoulos：** 完全有可能。领先数据公司很容易达到数千亿美元估值，甚至还可能更大。data 是模型训练中最难的部分。它需要被找到、清理和组织，过程非常脏、非常重。没有人喜欢雇用大量人员生成和标注数据，再把 data 与 GPU 结合，训练出模型。

相比之下，algorithm 已经在某种程度上商品化，大家都知道怎样使用 Transformer。这也是为什么从不同 frontier labs 出来的研究者看上去有些相似：很多核心方法已经被行业掌握，但独特、可靠且能持续更新的数据供给仍很难复制。

**Harry Stebbings：** 外界经常批评数据公司的 revenue concentration：主要客户无非 OpenAI、Anthropic、Meta 和少数实验室。这是否削弱了它们的 enterprise value？

**Anastasios Angelopoulos：** 我有两个回答。第一，硅谷投资人对 revenue concentration 变得过度胆怯。TSMC 也有客户集中，很多价值数千亿美元的 public company 都有集中度。还有一些企业只有两三个主要客户，或者几乎只服务政府，一样能建立巨大业务。Anduril 等国防公司天然集中，但并不妨碍它们创造价值。

客户集中当然是风险，但不能看到 concentration 就机械否定公司。关键在于客户关系是否持久，产品是不是不可替代，以及集中带来的单位经济性和议价关系。

第二，很多 data businesses 会向 enterprise 扩展。Arena 作为 evaluation business 也正在走进企业，帮助它们训练自己的 AI、做 routing，并利用 Arena 已建立的 intelligence layer。数据公司同样会向这个方向发展。未来每一家企业都需要自己的模型，也就需要自己的数据。企业数据会成为它们自身 moat 的组成部分。

### agent 时代的 Arena

**Harry Stebbings：** 谈到 agent，当企业逐步从试用走向完全信任 agent 时，Arena 的业务会怎样变化？

**Anastasios Angelopoulos：** agent 是 Arena 今年的第一优先级。很多人不知道，Arena 已经是全球最大的 consumer AI app 之一。我们的月访问用户超过 3,000 万，规模比一些知名 AI 产品还大。

其中很多用户是 knowledge worker 和 prosumer，我们称他们为“无法轻易雇到的专家”。他们不是来玩 benchmark，而是用 Arena 完成真实的日常任务。在使用过程中，他们留下选择、反馈和完整 agentic trace。Arena 据此构建评测，再把结果分享给整个生态。这形成一个基于真实数据的 organic flywheel：用户越多，真实任务越丰富，评测越准，模型实验室和企业得到的价值越高，又会吸引更多使用。

**Harry Stebbings：** 既然拥有这么多人和数据，为什么不直接做 data business？

**Anastasios Angelopoulos：** 我们围绕这些数据建立 evaluation business，帮助客户理解每个模型的强项和弱项，并据此改进模型。labs 可以使用我们的 insight 和 data 提升训练，企业也可以借此选择与部署 AI。

我认为全球每一家企业都明确需要 evaluation，而 evaluation 是 AI deployment 最大的瓶颈。人们总谈 cost per value，但第一步是定义 value。降低 token 成本很容易，我可以告诉你改用 Gemini Flash，支出立刻下降。困难的是确认更便宜的模型是否真的完成了业务目标。

**Harry Stebbings：** 可 value 完全因人而异。一个客户关心速度，另一个关心准确率。

**Anastasios Angelopoulos：** 没错，所以可以把 value 分成三部分：performance、cost 和 latency。cost 与 latency 更容易量化，performance 最难，因为定义取决于企业和 use case。

Arena 建立了一套比较复杂的 pipeline，从 agentic traces 中提取 organic performance measurement。价值就在这里：企业可以利用自己的真实业务数据判断哪种 AI 最适合自己，而不是到外面购买一个与自身任务无关的通用数据集。进一步，我们还能帮助企业训练自己的模型。

### 1 亿美元 ARR 与 margin

**Harry Stebbings：** Arena 现在收入大概在什么区间？

**Anastasios Angelopoulos：** annualized revenue run rate 已超过 1 亿美元，算法是第二季度收入乘四。我们仍在快速增长。

**Harry Stebbings：** 那我问一个不太客气的问题。你有 3,000 万高价值用户，却“只有”1 亿美元 ARR，这算高效 monetization 吗？

**Anastasios Angelopoulos：** 你实际问的是 margin。Arena 还不是 free-cash-flow positive，因为我们仍把收入投入增长、产品和用户体验。但业务 fundamentals 很强，我们和投资人都对 margin 状况满意。

**Harry Stebbings：** 一些 AI infrastructure 公司，例如 Fireworks，gross margin 大约在 30% 中段，和过去 65% 到 80% 的软件 margin 很不一样。投资人是不是过度关注 margin？

**Anastasios Angelopoulos：** 我不认为 margin 不重要。profit 本质上是 margin 乘 volume。低 margin 公司也可能是好投资，问题在于它最终卖的是什么。

今天不少业务本质上是 GMV 或 resale：转售 token、转售 GPU。短期可以在商品上加价，但投资人必须考虑它向客户提供的东西在终局值多少钱。如果最终产品只是替客户托管 GPU，为什么客户长期愿意支付远高于电费和硬件折旧的价格？当供应充足、差异缩小时，price-to-value 会压缩 margin。

早期 seed、Series A 或 Series B 公司现在 margin 不够好并不致命，但必须有一条通往优质 public-company margin structure 的路径。不能只看今天的收入增长而忽略终局经济性。

### 当模型供应商进入应用层

**Harry Stebbings：** 更棘手的一点是，客户会变成竞争者。frontier model provider 会多激进地进入 application layer？Claude 的设计能力已经开始影响 Figma。大家总说 Harvey 不必担心，但 Anthropic 完全可能做法律产品，直接威胁 Harvey 和 Legora。

**Anastasios Angelopoulos：** 这是所有美国软件公司都在担心的事情。我有朋友经营价值数十亿美元的公司。某天，一个大客户会突然说，OpenAI 正在进入这个领域，它更 AI-forward，而你还是传统 SaaS，所以客户准备离开。这已经真实发生。

如果 inference 逐渐商品化，OpenAI 和 Anthropic 自然会向上进入 application layer，拥有更多产品 stack，更接近最终客户价值，避免自己被底层商品化。它们最清楚哪些企业客户增长最快，也能据此选择进入方向。所以 Harvey 和 Legora 的确面临风险，Harvey 的 CEO 也公开说，model labs 是他最担心的竞争者。

**Harry Stebbings：** 这和前面“企业害怕 frontier labs”不是矛盾吗？一方面担心把数据交给它们，另一方面又因为 OpenAI 更先进而主动拥抱它。

**Anastasios Angelopoulos：** 市场上两种行为同时存在。具体取决于任务自动化程度、采购者和 GTM。企业对供应链风险有担忧，但当某个工具带来足够明显的生产率提升时，也会采用。

**Harry Stebbings：** 我认为 GTM 是关键。如果是 Claude design，设计师可以自己拿起来用，分发很轻。但 Harvey 或 Legora 要进入 Cooley、Clifford Chance 这样的律所，必须和资深合伙人建立长期关系，再把产品部署给担心 AI 抢走工作的初级律师。真正的重活是关系、组织变革和 deployment，不只是模型生成一个 legal chatbot。

**Anastasios Angelopoulos：** 同意。网络效应更强、operations 更重的企业，也更可能成为大实验室的采用者而不是直接受害者。像 Infosys 这样的 system integrator，model lab 不太可能立刻替代它，因为业务包含大量交付和组织能力。相比之下，可规模化的软件产品，例如 insurance claims automation 或通用 legal chatbot，更容易被模型公司直接做出来。

**Harry Stebbings：** Salesforce 接下来几年会继续繁荣，还是受到严重挑战？

**Anastasios Angelopoulos：** Salesforce 本身有很强的 AI strategy，已经准备参与竞争。我不认为它会迅速衰落。所谓 SaaS apocalypse 被夸大了，因为人们低估了大型企业建立的 network、data 和组织嵌入有多难复制。

**Harry Stebbings：** 我也认为，若服务像 Salesforce 一样深度嵌入企业，替代极难。如果产品更像 Wix，集成程度和黏性都低，风险就更高。真正的分界是 enterprise entrenchment。嵌得深，就很安全；嵌得浅，就应该紧张。

**Anastasios Angelopoulos：** 完全同意。

### 快问快答：判断如何变化

**Harry Stebbings：** 进入快问快答。过去十二个月，你最大的观点变化是什么？

**Anastasios Angelopoulos：** open-source model leadership。我原先没有想到 open model 会前进这么快，也低估了 Anthropic 的速度。整个空间变化得太快。

**Harry Stebbings：** 创办 Arena 时，什么是你最希望当时就知道的？

**Anastasios Angelopoulos：** 管理人。经营公司最重要的是 people management。我的 PhD 几乎都在地下室里证明 theorem，我很喜欢那种生活。但 CEO 的工作是 strategy、people 和 forecasting future。你必须看六个月、一年甚至两年后的局面，然后今天就开始规划。这些能力远比单纯技术工作重要。

**Harry Stebbings：** 优秀年轻人今天还有必要上大学吗？

**Anastasios Angelopoulos：** 人比以往更需要一个 strong mind。大学可以训练 first-principles thinking，也能让你认识一批共同成长的人。如果一个人希望未来以 intellectual work 作为职业的主要驱动力，大学仍是很好的地方。

**Harry Stebbings：** 回头看，Arena 有什么事情是你希望没做过的？

**Anastasios Angelopoulos：** 太多了。刚开始我根本不知道自己在做什么。联合创始人 Jan 可能比我更早看见问题，但我太固执，没有听他。后来我首先学会更认真听 Jan 的意见。

另一个教训是 focus。早期做了很多不该浪费时间的实验。经营公司需要极端专注，只做一件、最多两件事情，而且做到异常出色。要选对问题，持续投入已经证明有效的方向，而不是不断扩张到不起作用的新东西。

**Harry Stebbings：** 这也是为什么我对 Harvey 和 Legora 没那么悲观。法律只是 Anthropic 的第十二优先级，却是这两家公司每天唯一思考的事情。对 Anthropic 来说只是 appetizer，对它们来说是全部生命。

**Anastasios Angelopoulos：** 对。如果法律产品只是 Anthropic 的第十二优先级，Harvey 和 Legora 不必恐慌到认为自己必然被消灭。专注本身就是优势。

### 谁会先到 10 万亿美元

**Harry Stebbings：** Nvidia、OpenAI、Anthropic，谁最先成为 10 万亿美元公司？

**Anastasios Angelopoulos：** 很难不选 Nvidia，它目前领先。

**Harry Stebbings：** 可 open model 在崛起，我持有 Nvidia，股价却没有明显反应。为什么？

**Anastasios Angelopoulos：** 市场可能还没有完全 price in。要继续观察模型到底能变多好，但 enterprise adoption 还可能让整个 AI 行业再增长十倍。我认为它相当可靠地也会推动 Nvidia 获得一个数量级的增长。

**Harry Stebbings：** 大量债务被用来建设 compute，你担心 compute debt cycle 吗？

**Anastasios Angelopoulos：** 担心。最大的 secular risk 是，open-source 生态把企业节省成本的机会变得非常明显，从而降低 OpenAI 和 Anthropic 在 enterprise 的收入。如果它们的收入不足以支撑已承诺的基础设施和债务，极端情况下会出现 insolvency 风险。

**Harry Stebbings：** 我的担忧是，整个行业从未如此依赖两家公司持续达到目标。如果 OpenAI 和 Anthropic 的轨迹改变，音乐就停了。Fireworks、routing 公司以及大量依附其增长的企业都会突然失去支撑。

**Anastasios Angelopoulos：** 这是非常大的风险。行业也许需要稍微清醒一点。现在 hype 太多，质量差的项目也太多。我反而希望出现适度 consolidation，让真正的赢家浮现。Arena 会成为评测类别里的赢家，我也希望能吸收其他公司中优秀的人才。

### 哪些方向被低估，哪些过热

**Harry Stebbings：** AI 行业哪里 underhyped，哪里 overhyped？

**Anastasios Angelopoulos：** 几乎所有东西都很热。相对而言，compute 和 data center 的机械基础设施仍被低估，例如 cooling system、钢结构和真正的物理建设。市场对 HBM 和 GPU 已经极度兴奋，从 early stage 到 public market 都非常拥挤。

**Harry Stebbings：** 韩国股市相关板块今天大跌，甚至出现全国层面的讨论。SK Hynix 和 Samsung 员工刚拿到巨额 bonus，市场随后就崩了。

**Anastasios Angelopoulos：** 这是很糟的一天。为什么跌这么多？

**Harry Stebbings：** 我更倾向于认为，估值此前膨胀过快，市场不可能永远单边上涨。open model 或 closed model 的基本需求并没有出现明确破坏性变化，因此这更像价格和仓位的再平衡，而不是 AI compute 需求突然消失。这个问题最好请 hedge-fund manager 来判断。

**Anastasios Angelopoulos：** 那我们可以另开一档节目，请基金经理来纠正我们。

**Harry Stebbings：** 除了 Periodic，哪家 neo lab 最被低估？

**Anastasios Angelopoulos：** 我很难选，因为很多 neo labs 其实被高估。相对而言，Black Forest Labs 可能被低估。

**Harry Stebbings：** 我也认为 BFL 很强。最后一个问题。未来五到十年，你最期待什么？我母亲患有 MS，我最期待 AI 能让这类慢性病得到治疗。

### AI 医疗真正缺的是数据闭环

**Anastasios Angelopoulos：** 我一直非常支持 AI medicine。想象我们像今天逐个解决数学 open problem 一样，逐个消除疾病，人类 flourishing 会达到难以置信的程度。

但医学比数学难。数学是 closed system，答案可以快速验证；生物和医学需要在 biological system 上快速实验并形成 feedback loop。今天缺的正是这个反馈闭环。一旦我们找到安全、快速迭代的方法，接下来的旅程会非常惊人。

**Harry Stebbings：** 我采访 Demis Hassabis 时，一谈到 biology 和 medicine，他整个人都会兴奋。但临床测试必须改变。对很多慢性病患者来说，等待十五年没有意义。

**Anastasios Angelopoulos：** 这里最缺的就是 data layer，也是价值最可能沉淀的地方。训练医学模型和数学模型用的 GPU 可以完全相同，真正不同的是数据基础设施。你需要建立 collection、实验、反馈和持续更新的 flywheel。要做出优秀 biology 或 medicine 产品，最难的不是再买一批 GPU，而是形成高质量、合规、可反复验证的数据闭环。

**Harry Stebbings：** 这期非常坦诚，也非常有价值。谢谢你没有给标准公关答案。

**Anastasios Angelopoulos：** 谢谢邀请。我也很享受这次对话。以后可以再聊，你来 Bay Area 时也欢迎到 Arena 办公室。
