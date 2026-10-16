---
访谈时间: 2026-10-09
访谈时间说明: YouTube 发布日为 2026-10-09；主持人称录制当日 Google 发布 Nano Banana 2.1，实际录制日期未披露，按发布日记录
嘉宾名字: EAZ（主持人）
嘉宾公司名称: In the Loop AI（原 Limitless）
参与嘉宾:
  - 姓名: EAZ
    公司或机构: In the Loop AI
    职务: 主持人
播客名称: In the Loop AI（原 Limitless）
播客url地址: https://www.youtube.com/watch?v=X3JxgxfO9zo
youtube_video_id: X3JxgxfO9zo
YouTube发布时间: 2026-10-09
字幕来源: yt-dlp en-orig 原始字幕
全文提及的关键名词:
  - Google / Alphabet
  - Gemini / Gemini 4 Argon / Gemini 3.1 Pro
  - Nano Banana 2.1
  - Anthropic / Claude / Claude Code / Opus / Sonnet
  - OpenAI / ChatGPT / Codex
  - Meta / Meta Muse
  - DeepMind / Demis Hassabis
  - Jeff Dean
  - John Jumper / AlphaFold
  - Sundar Pichai
  - TPU
  - Google Cloud
  - Artificial Analysis Index
  - Qualcomm（赞助）
  - In the Loop / Limitless
companies:
  - Google
  - Anthropic
  - OpenAI
  - Meta
  - DeepMind
industries:
  - 人工智能
  - 云计算
  - 消费互联网
technologies:
  - Gemini
  - Claude Code
  - TPU
  - 图像生成
keywords:
  - Gemini 4
  - Google人才流失
  - 垂直整合
tags:
  - Google
  - Anthropic
  - OpenAI
  - Meta
  - DeepMind
  - 人工智能
  - 云计算
  - 消费互联网
  - Gemini
  - Claude Code
  - TPU
  - 图像生成
  - Gemini 4
  - Google人才流失
  - 垂直整合
---

# Google just surprised everyone (Gemini 4)

## Transcript

**EAZ：** 说到 AI，你会预期 Google 站在顶端。然而过去大约六个月，他们经历了一段「跌落神坛」。旗舰模型 Gemini 在去年年底见顶后，一次又一次推迟；Anthropic、OpenAI，甚至 Meta，都把他们甩在身后。粗算下来，自 Google 上一款模型之后，市场上大概又冒出了十五款新模型。坏消息不止于此：Google AI 团队近期还失去了关键成员。最显眼的是 DeepMind 的 Demis Hassabis——他不得不抽身去做别的事；他们还失去了首席 AI 科学家 Jeff Dean——在很多人眼里几乎是 Google 的「教父」，Gmail 之外大量爆款产品、驱动 Gemini 以及 Claude、ChatGPT 等模型的 TPU，以及多篇奠基性论文，都和他有关。他离开的理由是：在 Google 再也做不了自己想做的工作。市场反应可想而知是灾难性的——股价数小时内跌约 5%，市值蒸发数百亿美元。

但最近，我觉得风向开始变了。当然，抛开 AI，Google 本身仍是极其成功的公司，大约是全球市值第三；我不是在否定这一点。可如果 AI 才是未来，公司必须能转身。看 Meta、看 Amazon，尽管赛道不同，它们都能砸钱、砸时间、砸资源去搞清楚 AI。Google 其实起步更早，可以说在这条赛道上待了几十年。经历人员、时间与资源重新配置之后，他们必须重新把脚踩回赛道——而我们或许开始看到苗头。上周他们发布（至少是官宣）了 Gemini 4 Argon；若基准测试靠谱，这款模型相当强，能和 Anthropic、OpenAI 最强产品扳手腕。就在我录这期的今天，他们还发布了全新图像生成模型 Nano Banana 2.1。Google 的发布节奏又回来了。这期我想拆一拆：发生了什么、Google 现在站在哪、未来可能怎样。以上就是今天这期《In the Loop》，由 Qualcomm 赞助。

插一句：你可能在想，EAZ，布景怎么变了，还少了联合主持？节目有一大堆更新，两天前发过视频专门解释。长话短说：Limitless 品牌升级成 In the Loop，DNA 还在，我们会工作日每天带来前沿 AI 与科技动态。

先把舞台搭好。过去大约七个月，Google 最强模型，几乎全面落后于 Anthropic 与 OpenAI 的每一款旗舰——包括 Opus、Sonnet 这类相对更便宜的档位，也包括 OpenAI 侧更低档的型号。对方「最便宜、按理说最弱」的模型，仍能压过 Google 的最强——这很怪，因为去年年底 Gemini 还在顶端：他们曾完成过一次华丽翻盘；GPT 横空出世后 Google 被批评跟不上，直到 Gemini 出来、深度嵌进搜索等产品，舆论才改观。之后又出了问题——是研究、是人员，还是产品型公司的焦点问题？反正他们交不出一款真正能打的模型。

同期，Claude Code 迎来指数级爆发，成为 Anthropic 旗舰产品。那时 AI 编程还很神秘，公司不清楚该优先自动化编码还是研究之类；Claude 第一次让人看清：编码与 AI 天然契合，前沿会在这里被摸清。OpenAI 大约在 Claude Code 上线一个月后也反应过来，全面转向做竞品 Codex，并借此把模型追平 Claude。现在是 Anthropic 对 OpenAI——他们用模型去构建更好的下一代模型，也就是所谓递归自我改进。Google 眼睁睁看着这一切，却觉得「可以再等等，先把产品路线图上别的东西做完再回头搞编码」——代价很大。可惜之处在于：Google 拥有地球上最大量级的分发之一。市值大约 4.1 万亿美元，仍是全球最有价值公司前三；全产品线用户大约三十亿量级。没有第二家公司像 Google 这样，同时覆盖普通消费者与企业客户——Docs、Slides、Sheets 等渗透极深。互联网上无论搜索、生产还是分析，几乎处处都有有竞争力的 Google 替代方案；AI 爆发时，你本该预期他们再演一次同样的戏码。Gemini 一度做到了，但他们没能守住节奏。

别只听我说：看 Artificial Analysis Index——Anthropic 约一周半前发布的 Claude 5.5 大约 58 分，OpenAI 的 GPT-6 Astra 大约 53，而 Google 的 Gemini 3.1 Pro 还是二月份的——在 AI 时间线上那已经是「好几年」。为什么交不出有效产品？我认为有工作文化问题。从八月五日前后、甚至更早，他们就在流失关键人才。我们以前聊过：与 Demis 共享诺贝尔奖、做出 AlphaFold 的 John Jumper，去了 OpenAI；Jeff Dean 则离开创办自己的 AI 实验室（听起来像 Discovery Loop 一类），聚焦自动化研究——先从 AI 再到物理与科学——而这正是领先前沿实验室在做的事。为什么像 Jeff Dean 这样的「死忠」觉得必须离开、而不能在 Google 内部做这件事？我觉得工作文化出了问题，随之是大规模出走；Demis 也不得不退居二线去做别的事。留下的是一支需要重写战略的空荡荡团队。

但我承认，这听起来对全球市值第三、仍在狂赚钱的公司太「末日」。数据上：Search 的 AI 模式用户过十亿，AI Overviews 大约到 25 亿；他们处理的 token 大约每分钟 220 亿；Google Cloud 报了约 82% 增长——那是他们的 AI 资本开支与基础设施业务，用自研 TPU（对标英伟达 GPU）向其他实验室卖训练与推理。企业侧仅 Gemini 企业付费席位就有约 800 万，还不算 Cloud 企业产品。Google 是印钞机，现金储备也名列前茅；同时他们也在激进砸钱建算力与数据中心。

但有错位：当下 Google 的姿态，更像优秀的超大规模云/基础设施商——建数据中心、做芯片、把算力卖给别人做训练与推理。这没问题，可 Google 的 DNA 本不是「纯研究实验室」，而是研究实验室与产品公司的完美杂交——这也是他们成为巨头的原因。他们还没把这套能力翻译成 AI 产品优势。若维持这种产品/工作文化，他们可能沦为 hyperscaler 或 neocloud，而真正做出新模型、新 agent 的公司，会吃掉未来几十年的经济机会。因此，现在比任何时候都更需要 Google 换挡、想出回到 AI 竞赛的替代战略。

我个人希望 Google 赢——他们优势太大：不是单一巨石，互联网几乎每个角落都有触角，是垂直整合程度最高的公司，其他 AI 实验室难以比拟。OpenAI、Anthropic 模型很强，但缺分发、没有数十亿用户；Meta 有用户，却缺最前沿模型。Google 有钱、有资源、有专长，本该做出最佳垂直整合 AI 产品，也有数据去塑造成最佳消费或企业体验。现实却是：团队割裂、算力分配怪异——这队有算力那队没有，或者算力砸在影响几十万人而非数百万人的产品上；同时把算力卖给竞争对手，为了短期财报好看，而不是自己训练模型、打长线。

那在丢掉大约一半 AI 人才、重找结构与打法之后，Google 会怎么走？我们或许能从新模型看到答案。他们官宣了 Gemini 4 Argon——官方称在真实软件工程、知识工作、网络安全防御等复杂工作流上达到前沿表现。Sundar Pichai 强调的基准评估里（我们一向不太迷信基准，但能给你体感）：它在多项上打过 GPT-6 Astra 与 Claude 侧旗舰。左侧顶部是「知识工作」——大约对应软件型岗位七到八成任务：不是软件工程本身，而是朝九晚五用电脑、Slack、CRM、表格、策略文档、客服消息……该模型在这类任务上压过其他前沿对手，覆盖面其实比很多基准更大。再看 agentic coding——基准里的「奶油顶」：Deep Suite 一类允许模型拉起多个自身副本做 agentic 推理协作解题。Gemini 4 在这类测试上大约领先四到六个百分点。科学、数学、长上下文、计算机使用、多模态推理等也表现不错。整体看，这对 Google 是重大升级；Artificial Analysis Index 上他们曾落后大约 25 分，如今跳到约 53，追平 GPT-6 Astra。

但我还没法给真实上手评测——因为他们尚未对公众开放，担心网络安全事故。这几乎成了每家实验室发新模型的固定戏码：训完发现可能严重不对齐、可能逃出沙箱，于是先让安全防护方上手。今年初 Claude 某预览版也做过类似事；讽刺的是，现在已有能力相当的开源模型，我们还没看到（至少没公开看到）大规模 AI 破坏。原则仍成立：要有效、安全地发布 AI。Google 似乎在走政府自愿性质的流程，大概一到两周，公众版或许一周左右后可见。Bloomberg 报道已有内部人士上手，评价褒贬不一：有人说员工真拿来干活时没那么好，某些编码任务吃力——这也一直是我对 Gemini 的个人感受：基准很漂亮，真用起来往往还是回到 GPT 或 Claude。我保留判断，等亲手摸到 Gemini 4。我谨慎乐观：他们终于在过去一年最拖后腿的编码上，可能摸到了什么。

不止模型：他们还发了全新图像生成 Nano Banana 2.1——几小时前刚上。我不会假装自己跑过一堆 demo；但从已有视觉样例看，社交媒体要「完蛋」了——真实到离谱，反射更准，手指齐全，没有多余肢体。Google 在多模态上本就在局：图像、视频、世界模型（Genie 3 一类）都曾领先。过去六个月发布偏慢，现在开始看到回潮，以及产品与工作文化的转向。

退后一步，怎么看 Google？我仍坚持：这是一家有无数赚钱路径、跑道以「年」计的了不起的公司——但也就只有「数年」，变化可以很快。过去十二个月 Anthropic、OpenAI 的 ARR 暴增——传闻 Anthropic 从预期约 100 亿飙到约 1000 亿量级、OpenAI 也到约 700 亿 ARR；若轨迹延续（这是很大的 if），大约两年半可能追平 Google 的 ARR。Google 大概就有这么长窗口把 AI 战略搞清楚。类似还有 Apple 这类「拖得起」的公司。值得称赞的是：Google 愿意在公开场合试产品，即便有时摔得很惨，也能迭代。最终取决于团队、资源怎么花，以及失去最重要那批 AI 人才后如何转向。Jeff Dean，看着你走真挺可惜。

最后别忘：Google 是少数能垂直整合整条 AI 栈的大公司——有 TPU（训练与推理），有模型本身，还有跨 Maps、Search、Ads 等数十亿用户的分发，可以一夜之间把 AI 铺进去。球仍在 Google 场上，他们需要比现在更快行动。给我希望的是：我曾长期看空 Meta，不觉得他们能翻盘——他们却用 Meta Muse 这类个人 AI agent 让我刮目相看。Google 理论上能来一出类似的，就看他们想不想、肯不肯砸资源。

这就是我对 Google 整件事的看法。我一直很想更新 Google 观点——我仍然看多这家公司，但曾挣扎于他们如何翻盘；我一直在等旗舰模型，也许就是 Gemini 4 Argon。等不及上手；若有 Google 的朋友在听，请让我玩玩并给诚实测评。

最近几周很疯：这是节目品牌升级后的新版本——保留 Limitless 的 DNA，每周带来对顶尖 AI 趋势的洞察。若喜欢这期，请订阅、评论，最好打开通知；有不同意见也欢迎——我一直在挑自己论点的漏洞，我也是边学边搞明白。有互补视角或我漏掉的 Google 角度，私信或评论都行。觉得朋友会受益，就转发链接。我们也在 Spotify、Apple Music 等平台。谢谢收听 Qualcomm 赞助的《In the Loop》，下期见。
