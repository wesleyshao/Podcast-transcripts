---
访谈时间: 2026-08-10
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间。"
YouTube发布时间: "2026-08-10T14:05:48Z"
嘉宾名字: "Alex Atallah；Harry Stebbings"
嘉宾公司名称: "OpenRouter；20VC"
参与嘉宾:
  - 姓名: "Alex Atallah"
    公司或机构: "OpenRouter"
    职务: "创始人、CEO"
  - 姓名: "Harry Stebbings"
    公司或机构: "20VC"
    职务: "创始人、主持人"
播客名称: "20VC"
播客标题: "OpenRouter CEO: Why Chinese Open Models Are Beating the US | Why Enterprises Fear OpenAI & Anthropic"
播客url地址: "https://www.youtube.com/watch?v=K72oZoloA4M"
全文提及的关键名词:
  - "OpenRouter"
  - "OpenSea"
  - "LLM routing"
  - "inference provider"
  - "open-weight model"
  - "hyperscaler"
  - "Fireworks AI"
  - "Together AI"
  - "Kimi K3"
  - "GLM 5.2"
  - "token economics"
  - "Jevons paradox"
  - "model loyalty"
  - "memory"
  - "agent harness"
  - "model distillation"
  - "DeepSeek"
  - "Moonshot AI"
  - "NVIDIA"
  - "Meta"
  - "Claude Design"
  - "Figma"
  - "prompt injection"
  - "PII redaction"
  - "enterprise AI cost"
youtube_video_id: "K72oZoloA4M"
字幕来源: "YouTube en-orig 原始字幕，结合完整上下文转写为简体中文"
原始语言: "English"
转写说明: "完整读取原始字幕后按上下文转写；结合节目说明校正自动字幕中的公司名、模型名与基础设施术语，保留全部主要问答、数据、限定条件和反方观点。"
---

# OpenRouter CEO: Why Chinese Open Models Are Beating the US | Why Enterprises Fear OpenAI & Anthropic

## Transcript

【冷开场】

**Alex Atallah：** 这可能会成为科技史上最大的市场，甚至可能是人类历史上最大的市场。现在很多公司因为 routing 很时髦，就开始造 router，但 model labs 迟早也有多种动机进入你的领域。仅 7 月，我们就上线了 70 个 models，平均每 10 小时一个。美国在 open-weight models 上仍然落后很多。GLM 5.2 对开放权重而言是一次非常大的跃迁。

**Harry Stebbings：** 今天的嘉宾是 OpenRouter 创始人兼 CEO Alex Atallah。OpenRouter 是连接整个 LLM 世界的 unified interface 和 gateway。市场有传闻称 Stripe 曾提出 100 亿美元收购，公司最近一轮融资估值也已超过 10 亿美元。现在正是谈论这个市场最合适的时点。

## 从 OpenSea 带到 OpenRouter 的扩张经验

**Harry Stebbings：** Alex，我期待这场对话很久了。正式谈 OpenRouter 前，先回到你创办 OpenSea 的经历。你从那段旅程里带走了什么？

**Alex Atallah：** OpenSea 是第一个 NFT marketplace，和 OpenRouter 一样，很长时间都保持极小团队，直到 Series A 前后才扩张。2020 年 10 月 NFT 突然爆发时，我们严重 understaffed，servers、search index 都快撑不住，网站连续出现几次大故障。我当时最大的目标，就是别让 OpenSea 成为 crypto 世界里的 Twitter fail whale。

我们花了一段时间建立团队、修好 platform 与 infrastructure，让容量扩张变得可预测。Crypto traffic 特别依赖具体内容和社区情绪，会突然出现巨大峰值，所以即使还没有真实的 10 倍流量，也必须提前做 load testing，确认站点能承受 10 倍负载。

这段经历把 infrastructure discipline 深深刻进了我脑子。OpenRouter 面对的 AI market 同样剧烈，Anthropic 等公司会出现难以预测的增长，我们自己的流量也是。OpenRouter 并非没有遇过颠簸，但整体表现比我在 OpenSea 时稳定得多。最重要的传承，是从一开始就把“始终在线、用户可以依赖”当成产品本身，而不是增长后才补的后台工作。

## 创业假设里最大的意外：独立 inference providers 出现了

**Harry Stebbings：** 回看 OpenRouter 的 founding thesis，model ecosystem 里什么变化最出乎你们意料？

**Alex Atallah：** 最大意外，是市场出现了一整层专门托管和 serving open-weight models 的公司。早期并不确定这会不会成为一个 monopoly：也许三家 hyperscalers 会包办所有开放模型，startups 根本没有位置。

现实恰好相反。你几乎听不到有人在 hyperscaler 上直接运行 GLM，大家更多使用 Fireworks、Together 等 inference providers。它们上线新模型更快，也更擅长处理 serving 里的各种 edge cases。

OpenRouter 早期甚至不展示 providers 的名字，只写“provider 1”和“fallback provider”。我们本来想做 model labs 的 marketplace，却不确定 inference layer 自己是否也能成为 marketplace。后来发现，它不但会成为市场，而且 uptime 不会被供应端自动解决。不同 providers 对同一模型的 hosting quality、速度和稳定性都长期存在差异，需要持续路由和 failover。

## Inference 会不会被彻底 commoditize

**Harry Stebbings：** 很多人认为 inference provider layer 很容易商品化，最终利润率会被竞争压平，甚至整个中间层会消失。你怎么看？

**Alex Atallah：** 目前市场严重 supply-constrained，几乎每家 inference provider 都持续缺 GPUs，而且这种状态还会维持一段时间。你也许会问，Google、Amazon 或 Azure 为什么不买下全部 GPUs，把独立 providers 挤出市场？一个重要原因是 GPU makers 自己不希望 customer concentration。

NVIDIA 的重要目标之一，是让 GPU allocation 分散在许多客户手中。它希望 compute layer 保持异质性和竞争。这既符合 NVIDIA 利益，也符合 end users 利益，因为独立 providers 会探索不同的 serving innovations。

即使同一个 Kimi K3，不同 provider 的 benchmark 也有明显差别。Moonshot 公布过各 provider 的 serving results，我们自己也全天候测量开放模型在不同 providers 上的 quality、speed、price 和 uptime。结果不仅不同，还会随时间改变。这些模型具有 non-deterministic 特征，服务栈里很小的优化都可能改变实际效果。

把它说得更直白一些，供应商交付的并不是完全同质的计算单位。同一组权重在不同机器、不同推理引擎和不同并发策略下，可能表现出不同延迟、稳定性和答案质量。某家供应商今天领先，几小时后也可能因为容量紧张、软件更新或另一家完成优化而失去优势。模型本身又有随机性，不能只测一次就永久固定排序。因此，我们持续重复相同测试，观察变化是否稳定，再决定是否调整流量。这个市场需要的是动态发现机制，而不是每季度做一次采购评估后就不再改变。

Fireworks 的 Lin 曾说，“一个 token 并不等于另一个 token”。Provider 能让同样的 token 走更直接的路径，以更低延迟、更高有效质量到达结果。OpenRouter 的工作之一，就是发现哪家 provider 让 token 更有效率，并立即把更多流量导过去。

我们在 central router technology 上投入极多。大型 models 的表现几乎每五分钟就可能出现明显变化，只要检测到 quality improvement、speedup 或 price reduction，router 就会实时重新分配 traffic。因此，provider 的底层优化不是用户看不见就没有价值，好的路由会把改善直接转化成更多需求。

**Harry Stebbings：** 如果只能投资一家 inference provider，你选谁？

**Alex Atallah：** 我必须保持中立。不过我喜欢两类团队：一类做 custom hardware 和非常 low-level optimization；另一类努力降低 customization 成本。今天 fine-tune 往往会生成一个相对独立的新模型，但一些 providers 正在开发 LoRA 或 cartridges，让 adaptation 更容易跨 base models 迁移。未来切换底模也许只需几十或几百美元，而不是重新训练一整套模型。

**Harry Stebbings：** 明白了，你最喜欢 Fireworks。

## 专用企业模型不会消灭 multimodel future

**Harry Stebbings：** Lin 认为企业不应永远租 intelligence，而应拥有基于 proprietary data 训练的专用模型。如果每家公司都有最适合自己的 model，对 OpenRouter 是好事还是坏事？

**Alex Atallah：** 绝对是好事。OpenRouter 从第一天起就希望提高 AI ecosystem 的 neurodiversity，我们认为 multimodel future 不可避免。

假设某个 model 一度满足一家公司的所有需求。只要后来有人用不同 data 构建了一个 neurodivergent model，讲话方式、思考路径和创意都不一样，企业就会有动力同时使用两者。Creativity 无法像数学题一样用单一可验证指标衡量；两个接受不同训练的 models 并行工作，通常更可能产生单一模型永远想不到的方案。

企业当然会拥有一个服务核心 workflow 的 specialized model，但也会继续调用其他 models。周围生态也在不断使用新数据训练新能力。无论目标是降低成本、改善 margin 还是增长收入，公司都有动力测试外部创新，并把多个 models 组合起来取得更好表现。

自己的模型必须持续迭代，不可能赢下整个 intelligence market。这个市场会大到没有任何一个 model 能覆盖全部需求。企业更合理的选择，是让自己的模型在某个对业务至关重要的 specialty 上成为公认最佳，并把 branded intelligence 变成 brand moat 的延伸。

从博弈角度看，即使一家企业已经把内部数据训练进专属模型，它的竞争对手也在做同样的事，外部实验室还会不断购买或获得新的数据。企业若拒绝测试外部成果，就等于主动放弃别人创造的新知识、成本下降和能力提升。专属模型因此不是一劳永逸的终点，而是一个必须持续与外部生态比较、合并和升级的核心资产。它可以承载公司的风格、偏好和专业流程，却不应成为阻止员工使用其他能力的围墙。

## Routing layer 的竞争与 OpenRouter 定价

**Harry Stebbings：** 现在很多公司都发布 router 或 gateway，routing technology 是否正在 commoditize？

**Alex Atallah：** 很多公司只是因为 routing 流行而做 router。这样一开始就进入“复制别人”的思维，是为了存在、为了给现有客户补一个功能，而不是为了赢得这个市场。把 gateway 当 side product 的公司，天然会落后于 100% 专注于 router、gateway 和 LLM marketplace 的团队。

另一个问题是 user leverage。给 developers 接入更多 models，本质上是把整个 AI ecosystem 的创新杠杆交给他们，降低对任何单一供应商的依赖。如果 gateway 只开放一部分市场，或缺少定制能力，它就在替用户和企业员工删掉本应拥有的选项。OpenRouter 的核心不是多列几个 model names，而是通过 choice 提高用户议价权和行动自由。

**Harry Stebbings：** 但 pay-as-you-go 收取 5.5% fee。客户小时候喜欢，规模大后会觉得太贵，最终自己造 router。

**Alex Atallah：** 5.5% 是 pay-as-you-go plan。我们后来推出完全不同的 enterprise pricing，按 committed spend 定价，对承诺额度不再收同样费用，效果很好。很多觉得贵的公司其实还不知道 enterprise plan，当然这也说明我们需要把 pricing 讲得更清楚。

我们还会推出 self-serve business plan。如果客户 bring your own inference 或 bring your own API keys，相关 fee 会消失。只有客户直接使用 OpenRouter 提供的 capacity、又不在 enterprise commitment 里时，pay-as-you-go fee 才适用。Committed spend 也帮助我们预测 demand、提前准备 capacity。

## 三年后的收入核心仍可能是计划外 inference capacity

**Harry Stebbings：** 三年后 OpenRouter 最大的 revenue line 会是什么？

**Alex Atallah：** 这取决于整体 AI economy。如果未来四年仍以每年 10 到 15 倍甚至更快速度增长，企业会持续低估自己需要多少 inference。那样的话，收入仍会主要来自今天的核心能力：帮助 enterprises 和 startups 补足 unplanned inference capacity。

当客户突然要测试一个原本没计划用的 model，某个 model 用量远超预期，或者主 provider 故障时，我们提供 failover、uptime 和额外 capacity，确保 AI product 不会因此停摆。只要整个市场持续低估需求，这项能力就会很值钱。

如果增长率降下来，SMB SaaS 等标准化产品可能成为更大收入来源。经济总量终究有极限，不可能永远每年增长十几倍，因此收入结构会随市场成熟而变化。

## Token 价格下跌与 Jevons paradox

**Harry Stebbings：** 过去约 18 个月，token prices 下跌约 90%。你们按 spend 获利，单价下降看似会缩小收入池，这对业务到底好不好？

**Alex Atallah：** 常见解释是 Jevons paradox：价格下降 10 倍，usage 增长超过 10 倍。很少有人把它建成可靠模型，但我们有相当干净的案例。

OpenAI 在 OpenRouter 上把一个 model 的价格先降 5 倍，再与我们协调继续降 2 倍，两周内合计降到原来的十分之一。Usage 随后增长了 13 倍，并在新平台上稳定下来，之后继续按原有速度增长。这个案例的 confounding variables 很少，几乎是标准的 Jevons paradox：价格降 10 倍，用量增 13 倍。

而且当时 DeepSeek 和 GLM 也正以很有竞争力的价格增长。降价前，GLM 长期位于 OpenRouter token volume 前三至前四；降价后，OpenAI 的这个 model 超过 GLM，成为很久以来第一款进入平台用量前列的 OpenAI model。这说明价格调整能显著改变 model mix，不只是把同一批需求重新计价。

## OpenRouter 数据能代表整个市场多少

**Harry Stebbings：** 外界常根据 OpenRouter 排名说，最热门的五个 models 都来自中国。批评者认为 OpenRouter 只占市场一小部分，很多 frontier API usage 根本不经过你们，所以排名不代表真实市场。你的数据偏差在哪里？

**Alex Atallah：** 我们会结合客户调查和外部 surveys 估算偏差。OpenRouter 确实更能代表相信 multimodel future、主动使用多个 models 的公司。市场上仍有少数“只用 OpenAI”的公司，它们通常直接使用 hyperscaler、OpenAI、Anthropic 或 Gemini，我们看不到那些流量，因此数据会 undercount frontier models。

不过这种 single-model company 已越来越少。只要一家企业开始认为自己需要其他 models，OpenRouter 数据对它就更具代表性。随着 multimodel thesis 普及和平台规模扩大，数据质量也会继续改善。正确用法不是把平台份额当作整个市场的精确 census，而是把它看作多模型开发者行为的高频样本。

## 企业究竟更怕 frontier labs，还是 Chinese models

**Harry Stebbings：** 有人说企业对 frontier model providers 感到恐惧。你从客户那里看到这种情绪吗？

**Alex Atallah：** 我没有看到普遍恐慌，但 Claude Design 发布时，尤其围绕 Figma，确实出现过一阵不安。真正危险的是只做 go-to-market wrapper 的 startup：它把 AI 接入某个垂直市场，主要差异只是 integrations 和 system prompt。

担忧的关键不是基础模型公司会立刻复制每一家小公司的全部产品，而是它们会选择对大客户续约最有帮助的职能切入。若一家模型供应商已服务工程团队，再拿下设计、销售或财务团队，就会在同一企业内部形成更多支持者，也更难被替换。于是，原本看起来很小、收入也不大的功能，可能具有很高的战略价值。创业公司必须证明自己拥有更深的工作流、数据和用户关系，而不能只依赖基础模型公司暂时没有推出同名界面。

只要 model lab 不在意那个市场，这类公司可以活得不错；但 labs 有动力逐步进入。一个动机，是让目标 enterprise 内更多 teams 依赖自己的 models。Claude Design 即使未给 Anthropic 带来显著直接收入，也可能让 design team 形成依赖，与已经使用 Anthropic 的其他团队一起提高 account stickiness。某个职能一旦对 model lab 变得战略重要，服务该职能的 wrapper startup 就会面对直接竞争。

**Harry Stebbings：** 很多 founders 说自己从 Figma 转到 Claude Design。它会显著伤害 Figma 吗？

**Alex Atallah：** 我看到不少 designers 尝试它，包括我们自己的团队，但没有听到足够多的 repeat-use story。我也没和大量 designers 深聊，因此不知道最终结果。至少 Figma 公布的经营数字仍然很强，不能因为社交媒体上的尝鲜故事就断言核心业务被替代。

**Harry Stebbings：** 这就是上市公司的痛苦，业绩很好，股价照样下跌。

## 每十小时一个新 model，agent labs 也会训练自己的模型

**Harry Stebbings：** 现在每天似乎都有两三个新 models。未来一到三年，这种开发速度还能继续吗？

**Alex Atallah：** 7 月我们上线了 70 个 models，平均每 10 小时一个。新的 agent labs 也开始出现，它们最终往往会训练自己的 models，因为拥有 model 能让 agent company 把能力直接分发给现有用户。Cognition 已有 model，Cursor 也有，其他 agent companies 很可能跟进。我们现在只是看到开端。

GPU makers 希望制造更多模型竞争和多样性，OpenRouter 也希望如此，investors 则总想尝试可能以不同路径改善 intelligence 的新团队。这些 incentives 足以继续吸引 founders 创建 neo-labs。如果 American open-weight models 增多，美国 agent labs 就会获得不依赖 Chinese base model 的训练起点，进一步带动本土生态。

## 对 Chinese open models 的责任边界

**Harry Stebbings：** Chinese open models 发展得又快又好，美国是否应该担忧？OpenRouter 可能把企业流量路由到某个带 backdoor 或受政府影响的 Chinese model，你是否负有责任？

**Alex Atallah：** 美国确实落后很多。Poolside、Thinking Machines 等团队正在推进，但差距仍在。OpenRouter 的责任，是为所有 models 提供安全访问。Customer trust 是最高目标；如果某个 model 被普遍认定为 unsafe，我们会下架。如果风险可以通过技术缓解，我们会与 model lab 合作，把 safety practices 做到行业最佳或更好。

OpenRouter 是员工发现和尝试新 models 的集中入口，也因此适合统一部署 controls。我们提供 prompt-injection protection，能自动识别疑似 injection 的 prompts；也提供 PII redaction 等安全层，enterprise 可以一键覆盖所有 inference。目标是让员工探索新模型时，不必为每个 provider 重新搭建一套防护。

Models 有点像互联网。公司不能因为互联网存在坏内容，就全面禁用互联网；正确做法是建立 guardrails，并用 AI 本身改进 guardrails。我们当然不能假装知道 Moonshot 或 Alibaba Qwen 内部发生的一切。作为 US company，OpenRouter 会遵守美国规范，避免做不负责任的事，但不能把无法验证的内部信息说成事实。

**Harry Stebbings：** 美国企业更害怕 frontier models 还是 Chinese models？

**Alex Atallah：** 通常更害怕 frontier models。企业最困惑的是 data policy：发出的 prompts 去了哪里、存多久、谁能查看。Frontier closed models 不能放在企业自己的 machine 或任意 provider 上运行，这种不确定性很像过去对 public cloud 与 private VPC 的争论，企业很容易识别这种风险。

**Harry Stebbings：** 这很反常。企业能见到硅谷公司的总部和领导者，却比对遥远的中国团队更担心它们。

**Alex Atallah：** 的确反常，尤其当前最强 cyber capabilities 也集中在 frontier models。最近 OpenAI、Anthropic、Meta 都公开过自家模型参与 cyber incident，外界看起来像在比赛谁“黑过人”。但一旦事件发生，公开披露仍是正确选择。掩盖不会长期有效，也不能因为披露会被当成炫耀就选择不说。

## Kimi、GLM 与中美开放模型差距

**Harry Stebbings：** 最新 Kimi model 得到大量关注，它真的像宣传中那么重要吗？

**Alex Atallah：** Kimi 很好，但在 cyber capability 和 long-horizon tasks 上仍落后于 frontier models。对 open weights 来说，GLM 5.2 才是一次真正的大台阶；Kimi 更像 Moonshot 追上了那一级能力。Kimi 的 writing voice 和 tone 很好。一些 frontier models 在 coding 变强后，文字表达反而退化，充满模板化转折，读起来很痛苦；Kimi 长期保持了有辨识度的写作质量。

**Harry Stebbings：** 十二个月后，US open source 与 Chinese open source 的差距会扩大还是缩小？我的担心是扩大。DeepSeek 一旦成为 national champion，中国可以集中政策、资金和资源；Moonshot 这样的新团队出现后，也能快速得到支持。美国开放团队则要在昂贵研究环境里与 OpenAI、Anthropic 竞争，还要解释并不清晰的 business model。

**Alex Atallah：** 中国确实拥有非常优秀的 researchers，美国经常低估这一点。不过 Chinese labs 也会在 cyber posture 和信息 censorship 上承受更多约束。今天有人抱怨 American models 因 cybersecurity 过度拒绝，但这种对比未必永远成立。

中国 models 在境外的能力很强，境内 guardrails 却可能非常严格。一个值得研究的问题是，DeepSeek 在中国境内究竟能提供多少超出 Great Firewall 的信息。如果 firewall 对中国十年后的治理仍然重要，开放 models 与信息控制之间迟早会发生变化。现在对中国团队“完全不在意模型开放后会做什么”的判断，也许过于简单。

**Harry Stebbings：** 我的判断之所以悲观，还因为两边所处的资源组织方式不同。一旦中国确认某个团队代表国家竞争力，监管障碍、资金和产业配套都可能迅速围绕它集中。美国开放团队则必须自己证明商业模式、募集巨额资本，同时与资金最充足的封闭实验室争夺研究人才。开放权重的社会价值很大，却不天然产生足以覆盖昂贵训练的现金流，这让融资叙事更难。

**Alex Atallah：** 这种比较有道理，但不能忽略美国仍拥有硬件、云基础设施、资本市场和大量顶尖研究人才。中国模型也不是完全没有约束。随着它们对国家战略越来越重要，网络安全、内容边界和境内外版本差异都可能变得更受重视。未来差距取决于双方能否把研究人才、算力与可持续商业生态组合起来，不能只按某一刻的发布数量线性外推。

## Developers 有 loyalty，只是 switching cost 不是唯一原因

**Harry Stebbings：** 你能观察整个生态。Developers 对 models 有 loyalty 吗？

**Alex Atallah：** 有。我们努力把 switching cost 降到接近零，让用户能随时尝试新 model，同时测量每个 model 的 retention 和 churn，也会把数据分享给 model labs：新用户从哪里来，离开后去了哪个 model。未来还会向公众开放更多数据。

即使市场出现更适合某个 use case 的新 model，仍有人持续使用旧 model。第一个原因是“我的 app 现在能工作，不想弄坏”。Support bot 如果换模型后突然说出奇怪的话，工程师就要重新调整 prompts、evals 和 guardrails，未必值得。

第二，新 model 不一定更便宜。旧 model 的 price 通常随时间下降；每次 intelligence jump 出现时，新一代价格曲线也会跳高，再逐步下行。因此，无论 closed 还是 open weights，立刻切到最新版本未必最 cost-effective。

第三是对 outputs 的信任。用户习惯某个 model 的语气和判断方式，也会形成自己的 personal evals，也许只是几道随机但非常在意的测试。如果新 model 没通过，他们就会继续用熟悉的版本。Loyalty 不完全来自品牌，更来自 production stability、历史优化和个人信任。

## Memory 会属于哪一层

**Harry Stebbings：** 过去很多人认为 memory 是最强 retention mechanism：OpenAI 知道我住在伦敦、做播客，因此以后更适合我。Memory 还会锁住用户吗？

**Alex Atallah：** 会，但关键是 memory 最终住在哪里。它可以属于 model、inference provider、app、infrastructure provider，或 router。每一层都会尝试以不同方式拥有 memory，而且各有优势。

放在 app layer，memory 拥有最多业务 context，也不绑定 model；放在 model layer，可能在 personalization benchmark 上表现最好，产生更高的最终 intelligence。未来也许可以同时组合 model memory 与 infrastructure/app memory，但两套记忆会不会互相冲突，目前还不知道。

没有任何一层能捕获全部有价值的 memory。Apps 掌握大量 model labs 看不到的 context。如果 labs 想获得这些内容，就必须给 apps 足够 incentives。Memory 因此不会自动把整个价值链收回 model provider，更可能形成多层竞争与协作。

例如，应用最清楚用户正在完成哪项工作、哪些记录属于同一个项目，模型供应商则可能最了解怎样把长期偏好编码成对当前模型有效的提示。基础设施层还能跨应用识别重复需求。把记忆只放在一处，会牺牲其他位置独有的信息；把所有记忆同时注入，又可能造成冲突、重复和上下文污染。最终胜出的方案很可能需要明确记忆的来源、有效期和优先级，让各层在用户授权下协作，而不是任何一层无条件垄断。

## Router 会不会先被 agent harness 吞掉

**Harry Stebbings：** Claude Code、Cursor 把 model 和 harness 打包在一起。独立 router 会不会还没长大，就被 agent framework 吸收？

**Alex Atallah：** OpenRouter 早期的一个核心判断，是 apps 低估了用户选择 model 的欲望。2023、2024 年的很多 app 甚至不告诉用户底层用了什么，认为大家只想要抽象的“AI”。我们认为用户会在意自己在和谁交流，就像解决问题时会在意找的是哪位员工。后来 Notion 等 app 也开始让用户选择 model，验证了这点。

Harness 同样是一种 user experience，developers 会对不同 harnesses 建立偏好。Harness 的价值不在于 system prompt 里塞越多东西越好。Models 能力提升后，过多旧指令反而成为 handicap。Anthropic 曾展示过，删掉 system prompt 中一些内容后，后续 user prompts 的冲突减少，性能反而更好。现在不少 harness 正通过删除 code 来适配最新 frontier models。

这不表示 harness 会消失。它让非 model lab 的 developer 仍能拥有 user relationship，因此经济价值很高。Harness 与普通 app 的差别，主要在 composability：一个 harness 可以调用另一个 harness，也能在 cloud sandbox 里启动新 harness。

Models 对 Unix 和 bash commands 训练充分，因此组合 harness 通常比操纵任意 app 更 deterministic。让 agent 控制一个 app，可能要找登录方式、启动 virtual browser、索取密码、识别 input field，再寻找 API docs，充满 unknown unknowns；组合 Unix-based harnesses 时，这些不确定性少得多。Developer 还可以直接进入 harness，检查状态并用自然语言干预，比盯着一串 API calls 更透明。

## Meta、model discovery 与 utility layer

**Harry Stebbings：** Meta 重建 model lab，并让 Alex Wang 站到更中心的位置。你对 Muse 的成果满意吗？

**Alex Atallah：** 他们做得不错。重建 model lab 需要时间，也要处理 organizational debt。Meta 有足够资源成为 serious challenger，并可利用 social network 和对人与关系的理解，做其他 labs 不那么关注的能力。

但 Muse 仍需要清晰 niche。用户还不知道什么时候应该选择它、核心优势是什么。它刚发布 coding harness，目前仍在追求 general capability。真正关键的时刻，是它能明确告诉市场：“我们在这件事上远好于其他 models。”

**Harry Stebbings：** 我最近常用 Arena，把同一 prompt 并行交给多个 models。它会让我发现原本绝不会主动尝试的 Kimi、Muse 或其他 models。我不再忠于一个品牌，只看四份结果，选最好的。这是否说明 model layer 正变成 utility？

**Alex Atallah：** 并行运行多个 models 是非常好的 architecture。可以让一个高能力 frontier model 担任 orchestrator，再调用四个成本更低的 open models 作为 sub-agents。OpenRouter 已帮助很多 developers 这样做，也提供针对通用 models 优化的 sub-agent server tool。

低成本 sub-agents 适合 deterministic tasks：输出形状明确、问题类型已知、历史上有稳定解法，例如 text classification。Orchestrator 则读取这些结果，继续处理未知、non-deterministic 的部分。不是所有任务都需要 160 IQ 的昂贵 model，让 120 IQ models 承担可验证子任务，往往能同时改善成本和吞吐量。

## 怎样建设 American open-model ecosystem

**Harry Stebbings：** 如果让你负责一项计划，推动美国开放模型更有力地与中国竞争，你会做什么？

**Alex Atallah：** 我会先与现有 American labs 深聊，了解 distilling Chinese models 对它们到底有多有效。很多 Chinese open-weight licenses 允许 distillation。团队可以使用这些 models 的 outputs，对自己的模型做 reinforcement learning。这是所有 AI labs 都会使用的重要方法，可能帮助美国开放模型快速追赶。

Distillation 还允许团队检查 rollout outputs。如果担心源模型的 voice、constitution 或 alignment 不符合目标，可以在训练数据进入自己模型前进行过滤。它不是把另一个模型神秘地原样复制过来，而是可观察、可选择的 teaching process。

第二是 compute。美国目前相对中国仍有明显 compute advantage，但有才华的 neo-labs 很难及时取得足够资源。NVIDIA 已做了一些工作，还可以联合 Google TPUs、Amazon Trainium 和新型 chip companies，把 compute 更有效地交给正确团队。

**Harry Stebbings：** 我不认为优势会持续很久。DeepSeek 和 ByteDance 都在 aggressively 研发自有 chips，export controls 反而迫使它们解决这个问题。中国能四周建一座桥，也可能很快解决 chip bottleneck。

**Alex Atallah：** 同意。美国必须在 chip race 上保持领先，这对整个竞争至关重要。

**Harry Stebbings：** Distillation 是否不道德？外界常用“他们只是 distilled 了别人的模型”来贬低团队。

**Alex Atallah：** Distillation 就是一种构建模型的技术。Closed-weight labs 也做 distillation，大模型教小模型本来就是常见做法。它还可以把生态里发现的新能力传授给专用模型。

Model lab 有权在 terms of service 中禁止竞争性 distillation，并切断违反者访问。如果用户只是做一个高度专注、并不与基础模型竞争的小模型，据我所知多数 frontier labs 并不完全禁止。市场会同时存在允许和不允许 distillation 的 providers，OpenRouter 会帮助双方执行各自 terms，而不是擅自替权利人改规则。

## Stripe 收购传闻与 Alex 想资助的问题

**Harry Stebbings：** 市场传闻 Stripe 将以 100 亿美元收购 OpenRouter，这会发生吗？

**Alex Atallah：** 我不能评论。无论发生什么，我们都会继续执行当前 vision。OpenRouter 对生态很关键：它让安全的 AI access 不被一个 monopoly 控制，让所有人能探索充满活力的 model ecosystem；当新的 providers、server tools 或 inference-adjacent technologies 上线时，用户可以立即发现，并接入现有 AI stack。

**Harry Stebbings：** 如果你拥有公司很大一部分，100 亿美元交易意味着个人得到巨额财富，很难完全不想吧？

**Alex Atallah：** 我不太想这个，也没有很高个人消费。若未来使用 personal capital，我希望支持那些社会需要、却不适合 venture capital 的问题：它们没有清晰 business model，很难融资，但现在 AI 可以审阅过去无法处理的大量 data，让研究成为可能。我还没准备好公开具体计划，不过想帮助 researchers 取得 grants。

David Fialkow 资助电影是一个很好的类比。他支持商业上很难立项、政治上又敏感的重要故事，比如讲述 Jamal Khashoggi 的 The Dissident，以及揭露俄罗斯 doping 的 Icarus。没有这类个人资助，故事可能永远不会被拍出来。我希望做的也是让那些“被禁忌或被忽略、但值得研究”的项目有机会发生。

## Quick-fire：neo-labs、Anthropic 与动态员工成本

**Harry Stebbings：** OpenRouter 上最被低估的 model 是什么？

**Alex Atallah：** Poolside 的 models 很好。这是一家有意思的 American lab，模型不大但 coding 很有效，还在建设很多实用 access tools，团队也很好。

**Harry Stebbings：** 三年内 70% neo-labs 会死亡，同意吗？

**Alex Atallah：** 不同意，70% 太高。如果被大型 lab 收购也算死亡，确实会有 consolidation，那我可能估计 50%。

**Harry Stebbings：** Anthropic 的 Dario 是否应该少一些负面，多一些正面？

**Alex Atallah：** 行业需要一个对未来极度警惕的人。我个人欣赏 Anthropic 的 paranoia。当然，也不希望它把其他 labs 全部赶下桌。但我相信 neurodiversity，Anthropic 提供的谨慎声音正是多样性地图中重要的一部分。如果没有人极端认真地思考坏结果，这个角色就会空缺。

**Harry Stebbings：** 你坐在全市场 usage 之上，看到什么疯狂现象，却很少有人讨论？

**Alex Atallah：** 企业正在为 inference spend 惊慌，不知道如何把它纳入 opex。过去员工成本主要是一笔静态 salary，季度或绩效周期才调整；现在不同员工的实际成本会因 AI usage 而动态变化。

很多公司目前让中央团队决定 routing，未来这项选择很可能下沉到 employee level。员工最清楚自己的任务，应该选择最适合的 tools 和 models。公司则需要把员工产出与其使用昂贵、便宜模型的组合成本放在一起看。

这并不是要把每一次模型调用都变成员工考核，而是承认人工成本与计算成本已经共同构成完成工作的真实投入。两个产出相近的人，一个能把可重复任务交给便宜模型，只在关键判断上调用昂贵能力；另一个让最贵模型处理所有琐事，他们对公司的经济贡献显然不同。反过来，若昂贵调用确实显著提高质量或缩短交付时间，也不能只看账单就惩罚。管理者需要把结果、风险与消耗放在一起衡量。

公司还应先改善工具、默认路由和成本可见性，再要求员工负责。员工只有看得到每种选择的价格和效果，才可能主动优化。最值得推广的做法不是机械限额，而是让优秀员工展示怎样拆分任务、怎样用低成本能力完成确定性步骤，再把高价值上下文交给强模型。这会把成本治理从财务部门事后追账，变成日常工作方法的一部分。

我建议管理者仍做正常 performance assessment，但再加入 AI cost effectiveness，形成几个 quadrants。值得庆祝的是高产出、成本也高效的员工；需要关注的是表现一般、却消耗极高 inference spend 的员工。问题不是简单给每人砍预算，而是找出为什么他的 AI workflow 昂贵且无效，并修正选择。

员工也不是被动承受一个动态“身价”，因为使用哪些 models、怎样设计任务都在自己控制之中。AI 时代的 employee cost 不再只是 salary，而是 salary 加上可变 intelligence consumption。企业规划、绩效和 unit economics 都必须适应这一点。

**Harry Stebbings：** 最后，今天最令你兴奋的方向是什么？

**Alex Atallah：** 一个是 rare-disease research。它长期受 intelligence 和 inference bottleneck 限制，需要提出、测试大量想法，过去人力无法覆盖。

另一个是 crowdsourcing 城市与乡村生活质量改善。假设有人提出识别美国或英国所有 lead pipes 的办法，但缺少资源把方法做成熟、做 stress test，现在 AI 可以给这个想法杠杆。Brilliant ideas 分布在全世界，却不总在有资金和机构支持的人手里。AI 让更多人能把疯狂但有效的想法推进到可验证阶段，我们也许会因此解决许多社会已经放弃的怪问题。

**Harry Stebbings：** 我期待这场面对面对话很久了，你没有让我失望。谢谢参加。

**Alex Atallah：** 我也很享受，谢谢。
