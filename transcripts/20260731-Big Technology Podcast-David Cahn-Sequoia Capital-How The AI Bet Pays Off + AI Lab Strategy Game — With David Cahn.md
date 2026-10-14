---
访谈时间: 2026-07-31
访谈时间说明: 无法确认实际访谈日期，使用 YouTube 发布时间作为访谈时间
YouTube发布时间: 2026-07-31T11:13:17Z
嘉宾名字: David Cahn
嘉宾公司名称: Sequoia Capital
参与嘉宾:
  - 姓名: David Cahn
    公司或机构: Sequoia Capital
    职务: 合伙人
  - 姓名: Alex Kantrowitz
    公司或机构: Big Technology Podcast
    职务: 创始人兼主持人
播客名称: Big Technology Podcast
播客url地址: https://www.youtube.com/watch?v=IwjEuO2-3Y4
youtube_video_id: IwjEuO2-3Y4
字幕来源: YouTube 原始公开自动字幕 en-orig
原始语言: English
全文提及的关键名词:
  - AI
  - AGI
  - GPU
  - TPU
  - CapEx
  - ROI
  - ARR
  - token
  - inference
  - Nvidia
  - CUDA
  - Anthropic
  - OpenAI
  - Google
  - Meta
  - Microsoft
  - Amazon
  - Apple
  - SpaceX
  - Tesla
  - Neuralink
  - Boring Company
  - Sequoia Capital
  - Big Technology Podcast
  - ChatGPT
  - Claude
  - Claude Code
  - Claude Co-Work
  - Gemini
  - Azure
  - AWS
  - GCP
  - Oracle
  - Broadcom
  - Hock Tan
  - SK Hynix
  - Micron
  - Samsung
  - Jensen Huang
  - Sam Altman
  - Dario Amodei
  - Ilya Sutskever
  - Yann LeCun
  - Sundar Pichai
  - Satya Nadella
  - Mark Zuckerberg
  - Elon Musk
  - Andrej Karpathy
  - Alex Wang
  - StarCraft
  - Azad
  - The Player of Games
  - Hyperion
  - Transformer
  - SaaS
  - Devin
  - Sierra
  - Harvey
  - Juicebox
  - Gravity
  - Ramesh Raskar
  - Theresa Payton
  - Ambika Rajagopal
  - Sharon Gai
  - Rory Blundell
  - Torah
  - Quran
  - Gospels
  - Mahabharata
  - Peter Thiel
  - Michael Burry
---

# How The AI Bet Pays Off + AI Lab Strategy Game — With David Cahn

## Transcript

Alex Kantrowitz：

AI 行业到底要赚多少钱，才能把已经投进去的钱赚回来？又是哪家公司正在执行最可能胜出的策略？接下来我们就来聊这个话题，嘉宾是 Sequoia 合伙人 David Cahn。

欢迎来到 Big Technology Podcast，这是一档围绕科技世界及其外部影响、保持冷静和细腻讨论的节目。今天这期非常精彩。David Cahn 今天来到节目里。过去一段时间，我们几乎每周都会在节目里提到他的文章。今天我们要聊，AI 这轮投资到底需要什么样的回报，才能真正回本。然后我们会一家公司一家公司地过，看谁的策略最可能赢，谁的策略又可能不行。

David，很高兴终于见到你，欢迎来到节目。

David Cahn：

谢谢邀请，Alex。

Alex Kantrowitz：

你的文章第一次进入我们视野，大概是在 2024 年。当时你在讨论，要让 AI 这笔下注成立，究竟需要什么样的 ROI。那时候“AI ROI”这个词还没真正流行起来。大家普遍觉得，这项技术里肯定有某种巨大的承诺，所以当然要砸很多钱进去，不然就会被甩下，对吧？

但你很早就开始说，至少应该把一些数字摆出来，看看为了让这件事回本，到底需要达到什么量级。这个思路最早体现在你 2024 年那篇《AI’s $200 Billion Question》里。那篇文章之所以抓住了我们，是因为你非常明确地展示了，AI 需要创造大约 2000 亿美元的 lifetime revenue，才能把投资赚回来。而且那时候这个数字就已经看起来不是闹着玩的了。

我先读一小段，然后我们再聊它今天还怎么适用。你当时写道：“每在 GPU 上花 1 美元，大约还需要再花 1 美元的 energy cost，才能在 data center 里运行这块 GPU。所以，如果 Nvidia 到年底的 GPU revenue run rate 达到 500 亿美元，那就意味着累计大约 1000 亿美元的数据中心支出。再假设建这些数据中心的人需要赚到 50% 的 margin，那么仅仅是当年这一批 GPU CapEx，就需要在这些 GPU 的生命周期里创造 2000 亿美元 revenue，才能把 upfront capital investment 赚回来。”

也就是说，仅仅在 2024 年，或者说离今天不过两年前的时候，讨论的还是 2000 亿美元 lifetime revenue。我们现在再看今天。保守一点说，big tech 在今年和明年，也就是 2026 和 2027 两年合计的 CapEx，已经在朝着 2 万亿美元以上走了。我这里就按 2 万亿美元保守估算。

按你的算法，这意味着这套 AI infrastructure 最终需要创造 4 万亿美元的 lifetime revenue，才能把这笔钱赚回来。

所以，先给我们一个量级感。4 万亿美元到底是什么概念？这是科技公司平常就会赚到的钱吗？还是非常罕见的量级？以当前的投资水平来看，你觉得它真的有可能赚回来，并让这些投资人最终拿回本钱吗？

David Cahn：

先补两句。首先，2000 亿那个数字其实对应的是 2023 年，2024 年对应的是 6000 亿。

Alex Kantrowitz：

好。

David Cahn：

不过不管怎样，这些数字现在都已经大得离谱了。现在回头再听当时那些数字，甚至会觉得有点“可爱”。事情显然已经被放大到了完全不同的量级。2026 年出现了一次非常明显的再加速，所以才会出现从 2000 亿到 6000 亿这样的问题，基本相当于 3 倍增长。2025 年是 8500 亿，增速一度放缓；然后到了 2026 年，它又几乎翻倍，到了 1.5 万亿。正如你说的，再往 2027 年看，这个数字显然还会继续往上走，已经超过 1.5 万亿了。

还有一点要强调，这些数字是 cumulative 的。所以如果你真想问“总共要承受多大的 CapEx 负担”，你的思路应该是：每花 1 美元 CapEx，最终都得拿到某种 ROI。那你就必须把这些年份全都加起来。也就是 2000 亿，加 6000 亿，加 8500 亿，再加 1.5 万亿。仅仅从 ChatGPT 出现之后到现在，大概已经累积了接近 3 万亿美元需要被回收。再把 2027 算进去，这个数字只会更大。

我觉得现在大家都开始意识到，这些数有多大了。第一篇真正病毒式传播的文章，其实是《$600 Billion Question》，时间是 2024 年夏天。我觉得它之所以当时爆开，部分原因是那正好是 Nvidia 成为全球市值最高公司的时候。刚开始我发这些文章的时候，其实没什么人关心，这甚至都不是大家重点讨论的话题。让我觉得很夸张的是，两年半过去了，这仍然是头号讨论主题。

所以我尽量快一点把框架讲清楚。我猜你的听众过去一年里应该已经听过很多关于这个问题的讨论。现在大家都把它叫作 AI ROI debate，而且它正打得如火如荼。每次有一家 big tech 公司发 earnings，你都会听到两边的声音。

我最初写这些文章，本来就是想把问题提出来。我认为必须同时看两边。就像你开场说的，我们要保持冷静，双面都看。一方面，AI 很可能会成为人类历史上最伟大的革命。今天，99% 的 cognitive work 还是人类在做。50 年后，人类也许只做 1%。所以，一场巨大的革命正在到来，这一点我们都看得到。

但另一方面，如果戴上 financial analyst 的帽子，从市场角度看，任何事情都会经历 boom-bust cycle。我们必须冷静面对实现路径所需的时间、投资究竟流向哪里、回报最终归谁。历史告诉我们的一个重要事实是，会有赢家，也会有输家。

在这种 hype 极强、兴奋度极高的阶段，人们往往先默认所有人都会赢；接着在某个时间点，又反过来默认所有人都会输。现实不是这样。现实是，有些人会赢，有些人会输。而且我们等会儿聊到一些 game theory 和 company-specific 的东西时，会更清楚地看到这一点。

我觉得对我们这些不在场内、而是在场外观察的人来说，最有意思的问题恰恰是：谁会赢？我觉得人类天生就会被这个问题吸引，我自己也一样。你越往里看、越往深处看，就越会发现，推动这一切的并不是什么抽象数学，而是具体的人类个性。最早它可能是一个“6000 亿美元的问题”，但在那个问题的下游，其实是人、公司文化，以及这些公司彼此互动所形成的 ecosystem effect。

Alex Kantrowitz：

对，这点没错。我们后面会聊到那一面。但我还是想先回到最初的问题，也就是这个 revenue 量级到底有多大。

不如你拿它跟现有行业做个对比。比如，整个 SaaS industry 一年的总收入都不到 1 万亿美元。全部 big tech 的年收入加起来也不到 1 万亿美元。你再给我们一个直观刻度，解释一下：为了回收这 4 万亿美元，究竟得有多大的收入规模？以及在你看来，这件事有多可行。

David Cahn：

在 2024 年夏天那几篇后续文章里，有一篇我写的是 AI CapEx 的 game theory，我当时就试图量化一下：我们到底在谈什么。

按你说的，用大数来估一下，cloud software 大概可以分成两个大桶。一个是 cloud infrastructure，也就是 AWS、Azure、GCP 这类，大概是 5000 亿美元市场；另一个是 SaaS applications，粗略也可以看作 5000 亿美元市场。合起来算 1 万亿美元吧，虽然实际上可能还不到这个数。

所以你正在讨论的是非常大的数字。

然后，AI 投资里的第二层常见说法是：好吧，但 AI 对应的 TAM 其实不是 software revenue。这个说法我觉得是对的。AI 真正对应的 TAM，其实是 human labor。human labor 的确是远远大于 software 的可触达市场。

但即便如此，问题也没那么简单。有人最近给我发了一个统计，大意是说，全球 services revenue 有多少多少万亿美元，如果 AI 自动化掉其中 10%，而且 labs 能把这部分价值全部 capture 住，那就够回本了。

我会说，好，这个推演很好听，但你的假设实在太大了。你等于假设了：所有服务行业里 10% 的工作会被自动化；而且后面还有一层问题，那就是这些自动化释放出来的价值，到底由谁 capture。

所以，从长期看，就像我刚才说的，我认为 99% 的 cognitive labor 最终都会由 AI 完成。从那个意义上说，长期根本不存在 ROI 问题。

但金融市场永远存在 timing tension。长期不是明天。公司今天就在花钱，于是市场会不断来回拉扯，试图判断：那个“长期”什么时候才会到来？这些投入是否会在短中期看到回报？

Alex Kantrowitz：

所以你的意思其实是：它是可行的。

David Cahn：

不只是可行，而且我们其实已经在取得惊人的进展。我在写 1.5 万亿那篇文章时也说过这一点。Anthropic 过去一年的表现，对任何研究公司增长史的人来说，都称得上 mind-blowing。它是历史上增长最快的公司。

所以我觉得这不只是“理论上可行”。它已经出现了非常真实、非常有形的进展。回头看我当初写《$600 Billion Question》的时候，我的判断大概是：OpenAI 拿走了 AI 收入里的 lion’s share。那时候它的 revenue 大概是 120 亿美元。

而今天，OpenAI 和 Anthropic 合起来已经是 1000 亿美元以上的收入规模。当然，AI 里绝大部分收入，仍然是被这两家公司拿走的，vast vast vast majority 仍然集中在它们身上。所以这件事距离“真正充分展开”还有很长的路。

但进展确实极其明显。我认为这一点很重要，而且我觉得这是好事。

Alex Kantrowitz：

对。我回去重看你那些老文章时，也很明显感觉到了这一点。当时你在盘点，我们大概能看到的 AI revenue 到底有多大，会把 OpenAI 算进去，也会把 Anthropic 算进去，还会把各大 cloud service 也算进去。

而这项技术有意思的地方就在于，它正在生出全新的 use case，也生出了全新而且很赚钱的业务线。我再举你 2025 年一篇文章里的例子。你当时写到，ChatGPT 和 Anthropic 的收入都在快速增长：ChatGPT 的 revenue run rate 已经超过 120 亿美元，Anthropic 的 revenue run rate 达到 50 亿美元，同时还有一批新公司正在从 0 快速冲到 1 亿美元收入。

说实话，我觉得当时唯一一个真正确信 Anthropic 今年收入会涨 10 倍的人，大概就是 Dario 了。他说得特别明确：他们在 2024 年是 10 亿美元，2025 年要做到 100 亿美元。后来会怎样还不知道。当时听起来很疯狂，但现在看，很明显这大概率真的会发生。

而之所以能做到，是因为这项技术开启了新的东西。Claude Code、Claude Co-Work 之类的产品出现了，于是 Anthropic 就从一家“有相当规模 API 业务的 AI 公司”，变成了一家真正的产品 powerhouse。

David Cahn：

说实话，没有什么会比这些问题最终都被解答更让我开心。所以对我来说，始终是把等式两边都摆出来。

现实是，成本端扩张的速度，可能跟收入端一样快。所以你会看到一个 numerator、一个 denominator。你在一边取得了进展，但另一边的坑也被挖得更大了。

尤其是 2026 年，一个非常明显的现象是，在 AI coding 大规模起飞之后，hyperscalers 又一次大幅加码 CapEx。所以如果你看 2026 年，会觉得 AI 发展太快了，快到大家连两周前发生了什么都很难记住。

但如果把时间拨回到 2025 年 1 月，虽然现在听起来已经像很久以前了，当时 Microsoft 和 Amazon 其实都在收缩 CapEx。那时候市场上甚至有一种说法是：“让 Oracle 去做不就好了？反正这事风险很大，不如让 Oracle 去扛。”

结果 Microsoft 和 Amazon 都被股市惩罚了。大家说，它们对 AI 不够 bullish。于是它们又被迫重新回到牌桌。

到 2026 年，我们已经走到这样一个阶段：不仅所有人都在局内，而且所有人都在 massively accelerating。我觉得曾经还有过一个阶段，大家会问：人们会不会开始理性一点？会不会真的算一算账？

现在我觉得已经到了一个点，人们根本不在乎数学了。All in，彻底 all in，先干了再说。这就是我对 2026 年的总体感受。而我认为，今年早些时候确实出现过一个重要催化剂，把局面推成了这样。

Alex Kantrowitz：

说到“不在乎数学，只管 all in”，你最近还写过一句话。我记得应该是 2025 年写的。你当时说：“现在已经很清楚了，除非实现 AGI，否则没有任何东西足以证明接下来十年拟议中的这些投资是合理的。”你现在还这么认为吗？

David Cahn：

对，我还这么认为。这也是你和我最开始因为这个话题互发邮件的时候，真正开始深入交流的点。

说来也巧，我记得我写那篇文章时，刚读完《Hyperion》；而现在 Meta 新的数据中心名字就叫 Hyperion，多少有点意思。

回到正题。当时大家讨论的是 10 gigawatts、30 gigawatts、100 gigawatts 的 CapEx。这些数字已经大到天文级别，当然，还是得说明一下，那已经远远超过我们今天实际看到的水平。

但如果你把那些 CapEx 规模真放进脑子里去想，唯一可能把它们赚回来的方式，就是 AGI。

所以我觉得市场经常搞错的一点是，Wall Street 的天然视角总是：这只股票会涨 2%，还是跌 2%？它永远在这种短期波动里打转。一个月跌 10%，大家就“天哪”；一个月涨 10%，大家也“天哪”。

但现实里，我觉得我们正在走到一条真正分叉的路径上。

路径一是：我们得到 AGI，所有这些投入不但能赚回来，而且还能赚更多。它会成为人类历史上最伟大的技术，媒体一直说的那些话都会成真。

路径二是：我们把时间判断错了，coding 之后并没有出现下一个足够大的应用，然后你就会迎来一次大清算。

我觉得在某种意义上，市场既低估了 AGI 的概率，也低估了一次大修正的概率；与此同时，又极大高估了 status quo bias。也就是大家默认眼下这种状态可以一直持续下去：我们每年花 2000 亿美元 CapEx，GPU 出租出去之后 revenue 也在增长，但本质上并没有出现真正的新业务线。

那是不可持续的。

所以这也是为什么我老在谈这些公司领导者的 game theory 和内在逻辑。你看 Sundar、Satya、Sam、Elon、Dario，他们已经把自己的信念说得很清楚了。他们相信，他们正在追逐 AGI。

这件事已经没有争议。这些人对自己在做什么是极其清楚的。反倒是金融市场，有时候会选择性忽略他们说的话，因为如果你说“我买 Google 是因为它在押注 AGI”，对很多人来说，脑子就是不太转得过来。

于是大家又会把故事往回缩，说，哦，应该还是某种 ROI 逻辑吧；Microsoft 发 earnings 的时候，会看 Azure incrementality 是 X 还是 X 加 2%，然后股价围绕那个其实并不关键的数字波动。

但真正重要的问题是：我们到底会不会抵达 AGI？以及，外界能否看到足够多的证据，让这些公司继续维持当前这种开支规模？

因为现在我们已经开始进入 negative free cash flow territory 了。开支规模已经大到会越来越难持续。

但从所有可见证据来看，hyperscalers 仍然会继续非常激进地往这个方向推进。

Alex Kantrowitz：

有意思的是，市场现在似乎已经把很多投资建立在“AGI 很快就会发生”的想象上了。

但正如你说的，lab 领导人最近的一些公开表态，反而有点在放缓或者淡化这个 timeline。Dario 当然觉得也许今年、或者明年就会发生。可是 Sam Altman 谈的是 gentle singularity。Ilya 说过 pre-training is over。Yann LeCun 更是一路强硬地说，LLMs 根本不是通往 AGI 的路径。

你怎么看这种错位？一边是构建这项技术的人释放出的信号，一边是市场和投资者像是在押注 AGI 很快就会来。如果说哪里最不一致，我觉得这可能就是头号不一致。

David Cahn：

这正是我 2025 年最痴迷的话题。我那一年几乎完全被这个问题占据了。

我之所以如此着迷，一部分原因是，我投资 AI 到现在差不多 10 年了。我是一个长期且坚定的 AI bull。而且我是 Transformer 论文出来一年后开始投 AI 的。算早，但也不算最早，当然还有更早的人。

我一直遵循的投资哲学是：作为投资人，你的工作就是跟随那些真正聪明的创业者。最终有些事情会因为证据太明显而变成共识，而你的工作就是在它变成共识之前先看到。

所以，也许你是在 ChatGPT 出现前 5 年开始投 AI，但你不会在 ChatGPT 出现前 10 年就开始大规模下注。你得跟着那些真正的领军人物。

我当时看到的情况是，Ilya、Sam、Greg 这些人都出来说，AGI 还有 10 年。顺便说一句，作为一个跟了 AI 10 年的人，这种说法对我来说非常合理。任何这种级别的事都需要时间。

而 2024、2025 年我特别钻进去研究的一件事，是数据中心到底怎么建。我写过一篇叫《Servers Dealing Power》的文章。为了写那篇，我非常深入地研究了数据中心的实际建设逻辑。我还飞去看了很多 data center。然后我得到一个非常具体的认识：从你宣布要建一个 data center，到它真的建成，大概要 2 年。考虑到现在我们看到的大量社区阻力，未来甚至可能更久。

所以我当时的感觉是，在 Excel 表格里或者在图表里画 exponential scaling 特别容易，但在物理世界里，要把 exponential scaling 真正落地，是非常困难的。

这也就是为什么我在 2025 年那么执着地反复讲这件事。我觉得市场在谈论这件事的方式，与那些真正聪明的技术人士谈论它的方式之间，出现了巨大分歧。

在很多技术领袖的判断里，AGI 可能还有 10 年，甚至 20 年。而我这两年一直反复讲的一点是：AGI 一定会非常惊人。等我 80 岁的时候，这个世界将会完全不同。人类生活方式的每个方面都会不同。

所以从某种意义上说，所有这些乐观预测其实都没有错，甚至还可能低估了未来世界会发生多大的变化。

但时间线，以及通往那个未来的 path dependency，非常重要。金融市场非常在意 path dependency。很多赢家和输家就是在这条路径上分化出来的，因为在通往终点的过程中，你必须做对战略决策。

如果你是一个 grandmaster，我觉得 Elon 是，Sam Altman 也是，这些人会提前规划很多步：如果这一步发生，那么下一步是什么，再下一步是什么。

我认为这些 lab 领导者都在提前规划很多很多步。我们如果只看 financial statements，实际上是在过度简化。我们必须去看：他们的 master plan 到底是什么？它能不能成功？谁的 master plan 最合理？

这也是我一直在收集数据的原因。我在一篇文章里写过，每次看到一条 AI headline，我脑子里都会自动浮现一种“骑士走到 E6”那种感觉。也就是说，这个动作对整个棋盘意味着什么？它暗示了什么？

我脑子里像是一直在搭一个 world model。它当然不可能是对的，甚至大概率在一百个地方都是错的。但我会根据每一个新动作不断更新这个 world model。有些动作跟既有模型一致，所以只是非常小的更新；有些动作则完全是新信息，会迫使你重新修正：这些人到底在做什么？背后的策略究竟是什么？

如果你能把这样一个 world model 真正装在脑子里，它对你预测未来 5 到 6 年的帮助，远远大于去盯 Azure incrementality 是 X 还是 Y。

而我认为过去一年里最大的更新之一，就是所有这些人都说了同一句话：AGI 还有 10 年。这是一个极其重大的更新。

Alex Kantrowitz：

嗯。好，我确实很想聊这些 strategic moves。我已经铺垫了几次了。再问最后一个这部分的问题，然后我们休息一下。

你一直在谈“AI bubble”这个概念。我不打算直接问你“现在是不是 AI bubble”，因为你之前已经说过，其中有些部分确实像泡沫。

但我真正想问的是，为什么这件事会这么让人困惑？因为你会看到，市场共识在“这是泡沫”和“不是泡沫”之间来回摇摆。

比如今年年初，一开始是：当然是泡沫，你看看大家花了多少钱。然后突然变成：AI can code，那就说明这不是泡沫，因为它会吃掉整个 SaaS，甚至更多，还能 capture 全部价值。然后现在又变成：coding 这件事已经被市场接受了，但 spending 还要更高，所以又更像泡沫了。

你能不能讲讲，当人们思考“AI bubble”时，应该怎么想？为什么它会这么难判断？

David Cahn：

“Bubble”这个词本身就情绪负担极重，我觉得这就是一部分原因。几乎每个人都在 talking their book，所以你会看到 Michael Burry 这种人出来说“这是个泡沫”，而他本来就是做空派，当然会这么说，因为他 short 了一堆东西。

同时又有很多人是做多的，所以他们当然会说，一切都会很好。

所以难点就在于，你要一边解析每个人在说什么，一边还得考虑他们到底持有什么、为什么要这么说。

我觉得这很 tricky。

而“bubble”这个词本身带着很强的情绪包袱。每个人一听到这个词就会紧张起来。然后你还有一个更宏观的 mega trend，就是过去 50 年，Silicon Valley 基本上是在吞掉整个世界。押注“科技不会继续吞掉世界”，这件事本身就显得非常危险，而且老实说，大概率是个错误下注。

再看 AI，你会觉得，如果它像过去那些技术革命一样，那它当然会改变世界。

而且只要你真正用过这些技术，你是能看到未来的。我记得 2024 年我大概是 Devin 的第一个非员工用户，那个 coding agent。你一旦真的去体验，就会意识到，这些东西会变得极其强大。

所以，你一边使用这些技术，一边看到它们会替代 cognitive labor；再一边看那些具体 use case，比如 Sierra 在 customer service 里做的事，Harvey 在法律里做的事，Juicebox 在招聘里做的事，你会觉得，哇，这些工作将彻底不同。

于是你站在前线，看到世界一定会变，然后还要努力去预测这个变化怎么落地。而这一切落地需要时间。

所以我反而会尽量回避“bubble”这个词，因为一旦进入泡沫讨论，整个 conversation 很快就会变得非常狭隘。突然间，所有事情都只剩下一两个维度。你一说“bubble”，很多人的大脑就像是直接关机了，然后站到某个阵营里，通常只是因为他们自己的 financial incentive 在哪里。

这种情况下，就很难再进行真正有智识含量的讨论。

而我感兴趣的是 nuanced conversation。因为别忘了，我 80% 的工作是在某家公司的 boardroom 里，跟创始人和团队一起想：我们要怎样穿越这个 AI cycle？怎样确保我们成为另一边的赢家？

这才是我每天真正花时间在做的事情：怎样赢，怎样设计战略。

所以对我来说，“是不是 bubble”其实没那么重要。未来某个时间点一定会有修正，我们要做的是活过那些修正。长期来看，这项技术显然会成功。我们要确保自己是赢家，而且要足够激进，确保在穿越这一切之后依然能站在胜利的一边。

所以，我觉得与其用这种二元词汇把讨论直接封死，不如认真把细腻的那部分谈出来。

Alex Kantrowitz：

这也正是我们在这档节目里努力做的事。好，我们先休息一下。回来之后，我们来聊 David 所说的“世界历史上最伟大的 strategy game”，以及这些 big tech 公司究竟是怎么参与这场游戏的。稍后回来。

Alex Kantrowitz：

大家好，我是 Alex Kantrowitz。

[音乐]

我想跟你们介绍一部我和 Gravity 一起做的纪录片，我们想借它来探索 AI agent security 的未来。

[音乐]

为了弄清楚，我们到底是否真的为 autonomous agents 做好了准备，我采访了 MIT 教授 Ramesh Raskar、前白宫 CIO Theresa Payton、Michelin 的 Group Chief Data and AI Officer Ambika Rajagopal，以及前 Alibaba 高管 Sharon Gai。他们都从不同角度，对这个正在演化的领域给出了很有价值的洞见。

最后，我们还和 Gravity 的 CEO Rory Blundell 一起讨论了未来的道路。

[音乐]

如果你想跟着 Gravity 一起踏上这段旅程，可以点击节目说明里的链接，观看这部完整纪录片。

[音乐]

Alex Kantrowitz：

欢迎回来，这里是 Big Technology Podcast，本期嘉宾是 David Cahn。他是 Sequoia Capital 的合伙人。你可以在 `dcahn.substack.com` 看到他的文章。我强烈建议你订阅。David 每次发东西，我都会确保自己认真读。

我们来聊聊这场伟大的 strategy game，也就是这些 big tech 公司彼此之间到底在进行什么样的博弈。

不如这样，我给你读一些我写的一句话概括，你来判断我有没有抓到它们的策略，以及你觉得那是不是一个好策略。

David Cahn：

好啊。我觉得那篇文章算是我 2026 年最喜欢的一篇。所以对我来说，有意思的地方在于，chess 当然是一个很明显的 strategy game 隐喻，大家自然会想到用国际象棋来理解这件事。

但我觉得更有意思的隐喻其实是 StarCraft 和 Azad。

StarCraft 对玩过的人来说非常直观，没玩过也值得至少去读读它的机制。因为 StarCraft 本质上是一个 resource allocation game，而 AI 也是一个 resource allocation game。

所以接下来，当我们逐家公司展开时，最重要的问题其实是：你的 resources 是什么？你怎么分配这些 resources？

然后还有一层问题。StarCraft 里有三个种族。对应到现实里，就是：你的 intrinsic abilities 是什么？你的先天能力和禀赋是什么？我们等会儿可能会讲，Google 像一种 race，Microsoft 又像另一种 race。你到底有什么内生能力？

我在那篇文章里用到的第三个隐喻，是 Iain Banks 在《The Player of Games》里虚构出来的 Azad。那个文明里，大家通过玩一场策略游戏来决定谁当 emperor。

而我觉得 AI 现在正在发生的事情，就是这样。围坐在这张 4D chessboard 周围的八个玩家，都认为自己在为宇宙中最高 stakes 的东西而战。他们是在争夺“宇宙皇帝”的位置。不管那意味着什么，也许就是谁控制 AGI，谁就拥有那个位置。

所以，等会儿我们会进入更细的公司层面。但在我看来，一切都要回到：这些玩家相信什么？他们手里有什么资源？他们所在“种族”的固有 strengths，又让他们可以怎样行动？

Alex Kantrowitz：

好，那我们就一家一家来，看能聊多少。

先说 Anthropic。我的一句话概括是：用产品和 API 主导 enterprise，主导 code。

你觉得这个概括怎么样？他们的 resource allocation play 是什么？

David Cahn：

我不同意。我觉得那根本不是 Anthropic 的核心策略。

我认为他们的策略是：垄断全球最顶尖的 AI talent，然后赢，仅此而已。

Alex Kantrowitz：

展开说说。

David Cahn：

我觉得 Anthropic 的策略一直非常一致。他们代表某种明确的立场，而且他们自己非常清楚自己代表什么。正因为如此，他们才能招到极其卓越的人才。而这些人才会进一步复利。因为在他们看来，很多人也会同意这一点，包括 Zuck 显然也同意，talent 就是当下最稀缺的资源。

所以，先把这个稀缺资源，也就是 talent，尽可能地圈住。让这些人为你而战，这就是赢法。

Alex Kantrowitz：

这点挺有意思。如果 Anthropic 的打法真是这样，那它在 Meta 前几年那场 superintelligence lab 挖人狂潮里，流失的人确实比很多竞争对手少得多。

另一个值得琢磨的点是，假设我们真的进入一个 LLM commoditize 的世界，那么你最终就必须靠 product 去赢。如果你拥有最强的人才，你就有可能拥有最好的 models，也可能拥有最好的 products。这看起来确实是 Anthropic 现在的某种打法。你觉得这个理解成立吗？

David Cahn：

但我还是要反驳。因为我觉得大家恰恰就是在这里开始混淆模型，把重点搞偏了。

你必须聚焦在“真正的策略是什么”。而 Anthropic 的策略，如果你往回回测到它还没有被公认成功之前，就会发现它始终如一：他们非常深刻、在哲学层面上相信 AGI。所有事情都围绕着通往 AGI 这件事展开。他们相信自己会到达那个终点。

而他们需要 talent 才能到达。

到目前为止，至少证据显示，他们确实有能力继续推动 frontier。在他们自己的视角里，他们会继续把 frontier 向前推。是的，他们当然也会做产品；他们有产品当然是好事；他们也需要 revenue，才能吸引更多投资资金。但归根结底，一切还是围绕 AGI。

这是我的判断。当然，我只是一个局外人在观察。我不在场内，我也不可能知道全部。但从外面看，他们的策略非常一致，而且他们会继续执行下去。

至于 commoditization 的噪音、China model 的噪音，或者其他外围噪音，我怀疑在他们内部都只是噪音而已。对他们来说，只要继续执行就行了。Andrej Karpathy 刚加入，很多好事正在发生，他们就是那种“继续冲”的状态。

如果你真的走进那栋楼，我虽然没那么常去，但我猜大家在午餐桌上不会在聊“某个中国模型的商品化威胁”。他们大概只会讨论：怎么拿到最好的人？怎么继续推进 frontier？怎么确保我们有足够的 compute 来做这件事？

Alex Kantrowitz：

好。那我会说，他们这套模型的 flaw 在于，如果 AGI 最后变成 commoditized，这套打法就会暴露风险。也就是说，这个策略最大的弱点，是 AGI 本身也可能被 commoditize。你怎么看？

David Cahn：

那是你的 prerogative。对我来说，我不是 grandmaster。我不太喜欢站在场外说“那个 grandmaster 下错了”。我只是一个 game 的学生。

Alex Kantrowitz：

这并不意味着他们是坏棋手。只是说，在 chess 里，当你把棋子走向一个方向时，其他方向就被你主动关闭了。既然我们在讨论博弈，那就要承认，每一次选择都会暴露某个 flank。你朝这边走，就说明那边没走，那边就可能成为你的 weakness。

David Cahn：

但这就回到我前面说的：你到底真正掌握了哪些基础资源？这也是为什么 chess 这个隐喻会失效，而 StarCraft 会更有意思。

如果 models commoditize，对一个以 frontier work 为核心的 startup 来说当然不是好事。所以你必须押注某一个具体世界。也许这个押注是错的，但 startup 本来就有风险。问题是，你必须有观点。

而 Anthropic 这盘棋最美的地方就在于，它在这个策略上极度一致。如果它做出的那些前提假设最后被证明是对的，它就会非常非常有价值。

每个人都必须做假设，而这些假设通常应该建立在你可用资源的基础上。正因为如此，Microsoft 才会去押 commoditization，因为从 Microsoft 的战略位置出发，这个押注本身是合理的。

而宇宙是 probabilistic 的。我们不知道哪一种情景一定会发生。

所以我反过来问你：如果你是 Dario，你会做得和现在不一样吗？

对我来说，我会完全照着 Dario 现在做的来。我不会改。因为你不可能在所有概率世界里都同时获胜。你必须推动那个你认为最有可能成真的世界。

这也是为什么我更像一个 chess player，而不是 poker player。我更关心的是：如何推动世界进入我想要的 endgame。

当你真的坐在公司内部的时候，人就是这么思考的。Wall Street 把一切都当成概率博弈；CEO 则像下棋一样思考：我要如何 checkmate 对手？我要如何到达 AGI？胜利条件是什么？怎么去？

所以，从一个正在下棋的人视角看，不断担心“别的世界会不会发生”并没有生产力。更有用的是说：我们要朝我们相信的结果推进。也许最后错了，没关系。商业本来就复杂，世界本来就复杂。你不可能 100% 正确。

但如果你被这些外围可能性分散了注意力，尤其是在大公司里会发生这种事，一桌人每个人都有不同意见，那其实会更难。因为那意味着你根本无法一致地执行一套策略。

至少对 Dario、对 Sam，我觉得包括很多 startup 也是如此，再加上 Elon，他们都在非常一致地执行策略，而且看上去做得还不错。

Alex Kantrowitz：

有意思，因为我给 OpenAI 写的一句话，其实听起来跟你刚刚给 Anthropic 的概括很像。我对 OpenAI 的一句话是：build the smartest possible AI，剩下的以后再说。

David Cahn：

我还是不同意。

Alex Kantrowitz：

好。

David Cahn：

我觉得 OpenAI 的策略是：所有人都低估了 AGI，所以我们要 all in AGI。

而且我们会是最激进的那一个。其他人都会比我们承担更少的风险，而最终我们会被证明是对的，并赢下来。

如果你去看他们在 compute 上的策略，这个判断会非常贴近现实。

而且这依然是一套很自洽的策略。Sam 一直在讲这件事：这些东西是 exponential 的，人们会系统性低估 exponential。

然后，回到我一直强调的资源视角，OpenAI 还有一个额外优势，就是它某种意义上“发明了这个领域”。我认为“invented the field advantage”是一直存在的。他们内部仍然有非常强的人才储备。甚至可以说，Zuck 试图正面与 OpenAI 竞争、但到目前为止没有真正撼动它，这反过来恰恰证明了 OpenAI 剩下的人才有多强。

而且我觉得 Sam 的策略非常清楚：我们就是要比所有人更激进。

Alex Kantrowitz：

所以你的意思有点像，OpenAI 是在对 Anthropic 的策略做一个“yes-and”。也就是说：对，我们也在冲 AGI，而且我们会比你冲得更猛、更快。

David Cahn：

对。这就是 Sam 作为 leader 的人格。我觉得这一直都非常明显。

大家总是很容易忘记前面的事。可别忘了，当年这个 lab 还完全不被当回事的时候，他就敢为它融到 10 亿美元，那在当时看起来像疯了。然后他又从 Microsoft 那里拿到了 100 亿美元。

所以我总是建议大家回测这些人的历史决策，去问一个问题：当我看这些早期动作时，它们是在印证，还是在否定，我对这个人战略思维的判断？

这些人首先都是人，是复杂的人。而且他们的影响将是全球级别的。所以分析他们的决策完全是合理的。

但如果你回看 Sam 的历史，你会发现他一直都是坚定的大信徒，而且一直都是棋盘上最激进的那个人。

Alex Kantrowitz：

对。那如果你不愿意讲 weakness，我来讲。

如果你这么走，也就是比所有人更狠地 all in，那么你暴露出来的 flank 就是我们前面说的 duration mismatch。你越是比别人更快更猛地冲进去，就越容易出现技术进展时间线和业务承压时间线不匹配的问题。

好，这个我先记在这。我们进入下一家，Google。

顺便说一句，这真的很有意思。谢谢你陪我玩这个 game within the game。

David Cahn：

我们就像解说员一样，站在场边看场上那些人在打。

Alex Kantrowitz：

确实就是这种感觉。好，那我对 Google 的一句话是：把 Search 改得刚刚好，尽量留住客户；同时祈祷一切顺利。再另外尝试做出好模型和好 cloud services，但不要让它们彼此打起来。

David Cahn：

Google 很难讲。

我们先说说，如果是我来设计 Google 的策略，我会怎么做；然后再看它实际上在做什么。

Google 有两个巨大优势。第一，它有一个来自 Search 的 cash machine，这台机器能为很多事情提供资金。第二，它有 TPU。

我真的无法夸张地说明，“拥有 TPU”到底是多大的优势。他们已经做这颗 chip 做了很多年，而且它确实是一颗很好的 chip。

甚至有人认为，Anthropic 之所以做得这么好，部分原因就是它在用 TPU。

所以如果是我来掌舵 Google，我会 all in TPU。

我觉得它某种程度上也确实在做，但它现在基本还是把 TPU 囤着自己用，只是开始慢慢松开闸门，让外界也能用一些。

我一直很惊讶的一点是，你看 Jensen，会发现这个人 30 年来在一件事上都极其一致：ecosystem。

你去台湾，Jensen 就像民族英雄一样。甚至很可能有上百个人是因为 Jensen 的风格而发了财，因为他根本不在乎多拿那一个百分点。他的想法是：“大家都会赢，一切都会顺利。”

Jensen 会让别人变富。我觉得这是他最厉害的地方之一。他不是那种“我要当全球最值钱公司，别人都别想拿”。他的心态是：“你们也可以分一点 juice。”

所以 Jensen 一直在构建 ecosystem。你看 CUDA，你看围绕这颗 chip 建起来的整个系统。

如果我明天要创业、要进这个行业，我会非常愿意和 Jensen 合作。因为你知道他会善待你，会成为一个很好的 business partner。

Google 的风格则更内向、更封闭。过去 30 年，Google 一直是所有东西都自己造。Everything is built in-house，everything is invented here。

他们明明发明了 AI 背后的很多核心技术，但又好像始终没太弄明白该怎样把这些东西真正用起来。

当然，他们历史上也很擅长并购，擅长收公司、擅长收人才，技术团队也很强。但如果是我管 Google，对我来说最聪明的事就是：all in TPU。

你想想，Nvidia 都已经是 5 万亿美元公司了。Google 完全有可能仅凭 TPU，就打造一家 multi-trillion-dollar company。

但现在回到 Google 真正在做什么。

因为它在囤 TPU，我觉得它实际上更像是在走“追 AGI”的路线。只不过我不确定它有没有为这件事做好最好的组织准备。

因为从越来越多迹象看，它是在往 OpenAI 式的策略走：我们把 TPU 留给自己，尽量招最好的 researcher，努力做出最好的 breakthrough，让 Gemini 变得很强，让 Gemini 真正能竞争。

也许这就是对的。也许 AGI 的 prize 大到你根本没必要去做某种 hedge bet 或 ecosystem bet。

但我会挣扎的一点在于：前面我说 Dario 下得很美，Sam 下得也很美。作为 game 的学生，我是可以欣赏到那种“棋下得漂亮”的美感的。

Google 是一家惊人的公司，资源惊人，优势也惊人。所以从公司层面讲，它其实是最容易被欣赏的一家。

但一旦你开始看“具体怎么下这盘棋”，它有时会显得很 disjointed。

所以，我没法像前面两家那样，给出特别明确的判断。

它正在花 2000 亿美元 CapEx；它的 cloud business 也在加速。

顺便说一句，这里面还经常有一些最基础的 finance 101 被忽略。比如，如果我盖了一栋房子，再把这栋房子租给你，那就是“有 CapEx，也有 revenue”。所以，当然，你通过建设某种资产可以得到租金型收入。

但问题不在于 revenue 会不会上升，而在于 revenue 上升多少。

对 hyperscalers 来说，不只是“我盖了房子，然后收租”。它们实际上是“我盖了房子，然后我还投资给你，好让你能来租我的房子。”

所以，关于 hyperscalers，有一个更大的问题：它们的核心资源是 cash，而它们都在把 cash 用到极致。

我甚至有时候会怀疑，大型 hyperscalers 会不会存在一种“resource curse”。因为它们手上的现金太多了，所以它们天然会被激励去把钱花出去。

但真正决定成败的，也许根本不是 cash，或者说 cash 的作用远没有想象中那么大。

有时候我看这轮 CapEx boom，就会觉得它像是这种 resource curse 的下游结果：我有这么多资源，我必须把这些资源花出去；我又和 Amazon、Microsoft、Google 这些同行一起陷在一场 game theory 里，我们都有 cloud business，而 cloud 又是一个 oligopoly。

这简直是历史上最好的生意之一，是一个最伟大的 oligopoly。它不断吐出现金，于是每个人都不得不跟另一些人竞争。

你顺着这个线头一直扯下去，就会发现，现在这套策略越来越像是“由我手头已有资源决定”，而不是“由我真正想实现的目标决定”。

Alex Kantrowitz：

那对它们来说，替代方案到底是什么？是坐在场外不参与吗？

David Cahn：

这就是我说，如果是我，会怎么做。也许这判断是错的，毕竟我不在那栋楼里，我也不知道它们面对的全部约束。

但我的直觉就是：我会努力去造一个 Nvidia competitor。

TPU 是一个很棒的产品。如果 20 年后我能在 AI chips 市场拿到 50% market share，那已经是非常好的 business 了。

我会给这件事配一个明确的 management team。当然，我自己的内部团队也可以是这个业务的客户，vertical integration 当然也有一些优势。

但过去几年我一直在写 vertical integration。现实是，当你回头看现在和两年前的 ecosystem，对那些 vertically integrated companies 来说，vertical integration 并没有带来它们想象中的 model advantage。

所以，伟大的棋手或者 StarCraft 玩家，有时候也得根据新数据改变策略。现在其实已经有了某种数据：vertical integration 并没有像这些公司原以为的那样，带来模型上的决定性优势。

于是问题来了。也许该换一种打法了。也许你应该一边有团队继续追 AGI，一边认真把 TPU 这个资产 monetization 掉。

然后还有 Search 的问题。某种意义上，如果你照着 Alistair Marn 那套老派技术投资逻辑去看，我很喜欢他，也非常尊重他。他写过一本很棒的书，叫《The Engines That Move Markets》。他的观点是，与其去赌哪条铁路会赢，不如去做空运河。

于是你就会问：Google Search 会不会就是那条“运河”？也就是，这种 ad-driven business 会不会本身才是最脆弱的旧基础设施？

某种程度上，我觉得 Meta 和 Google 这么激进地 all in AI，本质上也是因为它们的 core business 最容易被 AI 伤到。如果大家的时间和眼球都转移到 ChatGPT 这种新界面上，那这些靠广告驱动的生意就会面临很大问题。

所以如果你要问 flanks 暴露在哪里，我会说 ad-driven business 本身就是一个很危险的位置。

当然，整体看它们现在的动作也不是完全不自洽。我只是觉得，大型 hyperscalers 的问题更多。还有一点，也许这就是 founder-run businesses 的优势。

像 Zuck 那种 founder-led 公司，就可以非常鲜明地采取某一种路线。他的策略很清楚，我们等会儿会讲，就是 all in。创始人控制的公司，在行动方式上就是会和 non-founder-led businesses 不一样。

Alex Kantrowitz：

你刚刚说，vertical integration 的公司到目前为止并没有因此做出 leading model。也就是说，那些不是靠“卖 AI 本身”赚钱，而是想把 AI 嵌进别处的公司，比如 Meta 想把它放进 consumer product，Google 想放进 Maps 或 Gmail，它们都想自己训练模型，但都没能像那些必须靠模型本身赚钱的公司那样做出最领先的结果。

你觉得，这种 struggle 的根源到底是什么？

David Cahn：

这事很有意思。好像每隔 10 年，Harvard MBA 教授们就会改一次口风，重新讨论 vertical integration 到底是好还是坏。

如果回到 first principles，我觉得 vertical integration 确实有些场景是好的。你看 Tesla，看硬件供应链，vertical integration 在 hardware supply chain 里往往是好的。因为你的供应商可能不够好，太贵，或者根本做不到你要的水准。

SpaceX 就是这样。你不得不 vertical integrate，因为你的供应商太差，一切都太贵，数学根本不成立。于是 Elon 就是一层一层往下挤：vertical integration、vertical integration、再 vertical integration。

也正因为 Elon 把这件事做得太好了，现在 vertical integration 又重新变得很热。

但我们不妨提出一个假设：software 和 hardware 之间的这层 vertical integration，也就是 chip、data center 和 model 之间这层，并不一定是好事。

也许 data center 更像是 real estate。我完全可以去租，而不是非得买。

当然，这只是一个 hypothesis。我不是在说已经被证明了。最开始这个论点被提出时，我其实觉得挺有说服力。它的逻辑是：如果我控制 data center，我就能做出更好的 model。

这是那个论点。

但看过去两年的 evidence，目前看起来并不支持这个结论。也许原因在于，这些公司实在太大了。做 model 的人在这边，造 data center 的人在那边，他们彼此根本不交流。那他们和两家不同公司也没什么差别。

如果现实中就是这样，那与其自己全包，为什么不直接买市场上最好的 chip？为什么不直接接受 free market 的分工？

反对 vertical integration 的最根本论据，其实就是 capitalism 本身。资本主义之所以有效，就是因为 specialization。绝大多数长期趋势都在说明，你应该专注于自己最擅长、拥有 relative advantage 的环节；而那些你没有 relative advantage 的部分，就让别的玩家去赢。

某种意义上，Apple 反而像是 anti-vertical integration 的典型。Apple 组装 iPhone，这颗 chip 是别人造的，camera 是别人造的，别的零件也是别人造的，而它只负责确保整个产品极其优秀。

Apple 反而会因为“有 30 家公司都在努力为 Apple 造 camera，而 Apple 只要挑最好的那个”而获益。

所以，到目前为止，evidence 更偏向这个方向。当然，现在还不能下 definitive 的结论。

Alex Kantrowitz：

好，我们再快速过几家。

Meta。我的一句话是：commoditize complementary layer，持续空转，等别人做出一个好的 consumer AI application，然后复制它、再用自己的分发能力铺出去。

David Cahn：

我这个人喜欢极致简化，简化到有时候可能是缺点。所以我的概括都很直接。

对 Meta，我的概括就是：买 talent。

他们是一支 mercenary army。只要肯花钱，就把需要的人买过来。

于是问题就变成：一支 mercenary army，能不能打得过 missionary army？

很显然，他们就是一支 mercenary army。他们在买这些公司，在发 golden handcuffs，在给 AI researcher 几十亿、上百亿美元的激励。

我个人判断是，他们买到的人确实都很强，Meta 内部原有的团队也并不差。所以我个人认为，他们的确有不错的概率把这件事做出来。Zuck 这套玩法本身是自洽的。

还是那句话，你要先问：你手里的 resource 是什么？Meta 的 resource 就是 Instagram 和一堆持续吐现金的产品。你能拿这些 cash 做什么？你可以去买 Alex Wang。

但接着在 2026 年就冒出了一个新问题：你的组织会不会因为这种做法出现 cultural dysfunction？你有一个由几万、几十万人组成的大组织，然后又在某个“象牙塔”里供着五十个“真正重要的人”，让他们去做最关键的事。你看那些 leaked press release 或各种流出的消息，显然这种组织失调已经开始出现了。

所以 Meta 的问题在于：接下来会发生什么？

还有一个问题是，我大学毕业那会儿，Meta 是全世界最火的工作去处之一；而今天，它已经不是了。

所以另一个问题是：你是不是正在和 organic talent flow 对抗？你是不是必须先赢得 organic talent flow，才能真正赢？

其实这不只是 Meta 的问题，而是所有 big tech 的问题。因为现在顶尖人才自发流向这些公司的趋势，已经没有了。10 年前，真正厉害的人确实会想去这些公司工作；而今天，它们已经不再被天然视为 leading edge company。

Alex Kantrowitz：

那如果 Meta 真的把这件事做成了，假设一切都朝着它想要的方向走，它是否仍然必须依赖一个大规模 consumer AI application，比如所谓 personal superintelligence，才能真正赢？还是说，只要它能成功完成“买 talent、囤 talent”这步，个人超级智能自然会在过程中出现？

David Cahn：

这还是回到我前面说的：我觉得我们所有人都低估了 AGI，而这些 grandmasters 都是在为 AGI 而下棋。Zuckerberg 显然也是。

至于 AGI 究竟怎么定义，我们可能今天没时间展开。其实也没有一个真正好的统一定义。

但有一个我合伙人常说的定义，我觉得最简单：从今天 1% 的 cognitive labor 由机器完成，走到未来 99% 的 cognitive labor 都由机器完成。这大概是最容易理解的定义，因为工业革命就是这么发生的。最初 99% 的 labor 由人完成，后来 99% 的 labor 由机器完成。

不管未来以哪一种形式到来，只要 Meta 赢下这场 race，Zuck 就会成为一个极其富有的人，shareholders 也会得到巨大回报。

所以，我认为那就是他们正在走的 path。它在逻辑上是自洽的。至于能不能成功，那是另一个问题。

Alex Kantrowitz：

好。接下来是 Microsoft。

我的概括基本是：它会尽量把 OpenAI 和 Anthropic 往 commodity 方向压一压，然后利用自己现有的 enterprise relationships 去收利润。

David Cahn：

我一直都很尊重 Satya Nadella。

而且一直以来，我对 Microsoft 的看法都偏乐观。我觉得大家没有给 Satya 足够的 credit，去认可他实际上持有了 OpenAI 如此大的一部分。

Satya 在做交易这件事上的能力，简直是 unmatched。

Alex Kantrowitz：

大概是 27%？

David Cahn：

现在也许是这个数，最开始应该更高。总之，一开始占比很大。

有一些坊间故事是说，Sam 当时几乎把这个 deal 拿去给了所有 big tech，而真正接住它的人是 Satya。

所以我一直觉得，Satya 没有得到足够的认可。因为如果你仔细看，他实际上一直在下一盘非常非常好的棋。还是回到我前面说的“漂亮的棋手”这个标准，Satya 就是那种你会站在旁边感叹，这个人思考层级跟我们根本不在一个维度的人。

而且某种程度上，我觉得 Microsoft 现在的策略就是：不管谁赢，最后都是我赢。我非常喜欢这种策略。

我最喜欢投资的一类 CEO，就是那种“无论世界怎么变，我都能赢”的人。Alex Wang 就是这种人。无论外部发生什么，他都会赢。因为他们足够灵活，移动够快，适应性强，而且足够 aggressive。

我觉得 Satya 这些年一直在这么做。回头看 2025 年，当他试图收缩 CapEx、让 Oracle 去承担很多 CapEx 时，我当时就觉得那是一个很聪明的战略计算。

而且后来他也很快根据现实更新判断：这件事会拖得比我想象更久，所以我还是得继续在牌桌上。

所以，如果我看哪家公司在“出牌”这件事上做得特别好，Microsoft 肯定是其中之一。

Microsoft 的 distribution machine 非常惊人。

如果 OpenAI 和其他 labs 赢了，而且 frontier models 没有 commoditize，那 Microsoft 会赢。因为它持有其中很大一块。

如果他们真的走到 AGI，那也很好。拥有 AGI 的 20% 已经很不错了。

但如果它没走到那一步，而是 commoditize 了，那么 Microsoft 又会赢 distribution game。

所以我真的很欣赏 Satya。他不是那种天天发推说“我们今天又做了什么新东西”的人。他节奏更慢一点。

如果让我提一点自己的偏好，我可能会说，如果我是他，也许会在 M&A 上更 aggressive 一些。因为他过去一直是个很优秀的买家，也非常会让收购来的公司释放价值。

所以我多少有点惊讶，他们在 M&A 上没有更激进。

不过，说到底，Satya 是比我强得多的 chess player。我认为他脑子里一定有一套非常清楚的 master plan，而且他在执行上既审慎，又足够 aggressive，这一点我非常欣赏。

Alex Kantrowitz：

那接下来是 Amazon。我的概括是：少做点事，卖 compute，赚钱。

David Cahn：

这大概是你说得最接近我会同意的一条了。

Alex Kantrowitz：

太好了，总算对上一条。

David Cahn：

Amazon 的策略到底是什么？某种程度上，还是回到那种“committee 制策略”的问题，所以很难真正说清楚。

但如果你看它最后呈现出的结果，确实像是“少做一点”。

它内部当然也有自己的 AGI lab，但看起来这并不是它的首要优先级。它有一个巨大的 cloud business，而这个 cloud business 在 AI 时代似乎正在逐步被 Azure 和 Google 追赶，甚至丢一些 share。

在 software 时代，AWS 无疑是最强的 cloud business。但到了 AI 时代，它还能不能像以前那样差异化，我并不确定。

所以你看 Amazon，就会觉得你刚才的概括挺准：我们就跟着大部队走，我们不会做特别疯狂的事，我们会做别人都在做的事。我们是全世界最擅长建数据中心的公司，也许这是它最值得强调的真正优势。

它在 earnings call 上基本也一直在讲：“我们特别擅长建 data center，这就是我们的优势。”

当然，我还是想先看到这种优势真正 materialize。它在逻辑上是成立的，但要真正变成结果，还得再看。

也许 10 年后我们回头看，会发现最朴素、最简单的策略反而工作得很好。

只是 Amazon 这种策略在智识上没那么刺激。因为所谓“do nothing”其实一点也不是什么都不做。它们依然在烧几百亿美元、上千亿美元 CapEx。

这也是这些 hyperscalers 很奇怪的地方。它们的 baseline 已经高到离谱，所以你甚至会把“花几百亿美元 CapEx”理解成“没做什么”。这其实是非常疯狂的一件事。那可是把 investors 的 free cash flow 大规模扔进去了。

在这种疯狂周期里，我们对“正常”的感知会被不断上调。于是你就会觉得：哦，几百亿美元 CapEx，只是保守打法而已。其实那已经是 insane 的规模了。

所以我有时会替 Amazon 感到担心。它有点像 heads I lose, tails I lose。

如果这一切真的成了，AGI 发生了，那 Amazon 并没有处在最有利的位置；如果这一切没成，它又和大家一样被埋在自己已经花掉的 CapEx 里。

所以我会问：你的 edge 在哪里？你的 spike 在哪里？哪一点会让我觉得，“哇，这真是一套很棒的策略”？

同样，我相信这些公司内部应该有更完整的战略，只是就外部呈现来看，我更容易看懂 founder-led companies。因为它们更有能力采取鲜明且强硬的立场；而大公司里，则更容易出现 committee wash。

顺便说一句，Apple 才是真正的 do-nothing strategy。

你必须承认，Apple 未来完全有可能被证明像个天才。因为如果最终一切 commoditize 了，Apple 根本没在 CapEx 上花那些钱。Apple 才是真的什么都没做。

当然，investors 今天会因为它这样而惩罚它。但你完全可以想象一个 10 年、20 年后的场景：Apple 反而因为现在的选择，看起来非常漂亮。

从这个意义上说，Apple 其实也是一套非常有观点的策略，而不是没策略。

我觉得 hyperscalers 很难这么有观点，回到前面的 game theory，是因为它们手里都有那只会下金蛋的鹅。它们彼此竞争，但又共享着这个惊人的 oligopoly。

我越来越觉得，竞争里真的存在一种 winner’s curse，或者 resource curse。你反而会被自己的 cash machine 拖住，因为你只能使用你拥有的那个东西。

而过去两年，Anthropic 这种“knife’s edge”状态，反而让它表现得最好。很多人都说，如果它丢了 frontier，它就完了。可人往往就是在刀刃上，才会发挥出最好的状态。我觉得这就是过去两年的经验事实。

Alex Kantrowitz：

Nvidia。我这个概括可能有点太俏皮了：祈祷 inference 不会 commoditize。

David Cahn：

我会说，Nvidia 的策略是：撑起整个 AI ecosystem。

而且这跟 Jensen 的历史是高度一致的。我觉得这其实是一套非常聪明的策略，也应该给他 credit。

Jensen 只需要 AI 这件事能继续成立。只要 AI 不崩，Nvidia 就会处在极其有利的位置。它已经是全球最有价值的公司之一了。

我在 2026 年喜欢讲的一件事是，过去 3 年，所谓 AI trade 的质量其实是在不断“往下传导”的。

2023 年是 Nvidia 的年份。那时候你会觉得，Nvidia 是史上最伟大的公司之一：chip 很惊人，技术很惊人，CUDA 很惊人，Jensen 花了 30 年搭出来这一切。2023 年简直像是 Nvidia 的加冕时刻。

到了 2024 年，Broadcom 进来了。Hock Tan 是商业史上最伟大的 CEO 之一。Broadcom 是半导体领域最顶级的品牌之一，也是最强的 design firm。所以 Broadcom 当然会做得很好。

到了 2025 年，GE Vernova、Vertiv、Siemens 这些 industrial giants 开始进来。它们都是好公司。GE 是美国工业英雄，Siemens 是德国工业英雄。只是如果你纯粹从“惊艳程度”来看，它们终究不像 Nvidia 和 Broadcom 那么强。

到了 2026 年，又轮到 SK Hynix、Micron、Samsung 这些 memory players，处在 right place、right time，通过涨价把 margin 从 hyperscalers 那边挤出来。

所以谈 Nvidia 时，我觉得必须先说一句：这就是人类历史上最伟大的商业之一。

而 Jensen 只需要这件事继续往前走。我认为他的 circular strategy，本质上就是投资所有人、确保所有人都能赢。

某种程度上，我觉得 Jensen 其实是把很多钱主动留在桌子上没拿走。因为在内心深处，他真心希望整件事成。

我觉得这件事应该让他得到更多 credit，但现实里显然没有。

而且你看，今年那些 high-beta AI 公司股价飞来飞去，Nvidia 股价反而没怎么动，尽管它本来完全可以更凶地涨价。Jensen 并没有在 pricing 上发疯。他其实可以更狠，但他没有。他对 ecosystem 是友好的。

所以如果要一句话概括，我会说 Jensen 的核心是：ecosystem first。

而且我觉得他 30 年来一直就是这么做的。

Alex Kantrowitz：

比如他会给 startup GPU，换它们一部分股权。某种意义上，这就是他的策略。只要你有可能在 AI 世界里成事，他就会确保你至少有机会挥棒一次。他愿意拿出现在最稀缺的东西来支持你。

David Cahn：

有时候，人们的 ego 会妨碍他们去做真正对自己最有利的事。Jensen 刚好相反。我觉得他在这件事上是很 low ego 的。

他会想：我就让大家都赢吧。也许我少赚一点，无所谓，大家最后都会很好。AI 会改变世界，每个消费者都会因为 AI 过得更好。

我确实把 Jensen 看成那种“把 pie 做大”的人。其他人都在争 share、争位置、争谁占多少，而 Jensen 更像是只想把 pie 做得足够大。他只想让 AI 成功。

我觉得这也是为什么他那么痴迷 open source。他就是想让这个 pie 变大，想让 AI 真正改善人们的生活。我觉得他的出发点是很好的。

而且你想想，他们为了等到今天这一刻，在 CUDA 上花了多少年。从某种意义上说，Jensen 很早很早以前就已经在押注 AI 了。他是最早那批押 AI 的人之一。

所以我也总是喜欢把讨论拉回到这些人的 personality 和 game theory 上。我的世界模型是这样，他们的世界模型是什么？

一个人到了某个年纪，底层 world model 基本就不会再变了。Jensen 的世界模型就是：你赢，我也赢。

Alex Kantrowitz：

好。那说到 SpaceX。某种意义上，它是不是在执行你理想中的 Google 策略？当然它没有自己的 chip。但它一开始试图自己做 model，用 Grok 去推；后来似乎意识到，靠自己 all in 追 AGI 未必是最优解，于是转而想做 AI cloud，或者说 Neo cloud。这会不会成为它在这里真正的生死线？

David Cahn：

对我来说，SpaceX 更像是一种对金融市场的元评论。

你看，过去 60 年，Silicon Valley 一直在吞掉世界。这个过程非常惊人。我们有 chips，有 Moore’s law，有那么多好事发生。

但最后这些技术能力，很多时候只是导向了 Instagram、TikTok 之类的东西。总觉得那个“对 humanity 的希望”元素，有点缺位。

而 Elon 某种意义上像是在对这件事做一个 meta commentary：如果你真的推动 civilization forward，你就会赚很多钱。但他真正关心的，其实是推动 civilization forward。

我不觉得 Elon 的底层动机是 dollar motivated。我觉得他是 mission motivated。

所以，去太空，殖民别的星球，推进人类文明，AI 也是帮助我们抵达那里的一个手段。我们需要 robots，所以他要做 robots。某种意义上，Elon 正在做所有对文明最重要的事情。我们需要 tunnels，所以就有了 Boring Company；我们需要 Neuralink，所以就有了 Neuralink。

而且他能够聚拢最顶尖的人才。我认为他的领导方式非常 masterful。

他吸引全世界最好的人，让他们愿意做出自己最好的工作。他把所有 blocker 都砍掉。

我前面说过，committee 管理很糟。真正优秀的人不想被一个 committee 管着。真正优秀的人只想让所有障碍滚开，好让自己专注完成 mission。

你去看那些在 Tesla 待了 15 年的 veterans，他们会对自己完成过的事情无比自豪。我的合伙人 Ravi Gupta 有一句话我很喜欢：the meaning of life is earned achievement。

而 Elon 不就是一直在帮助别人得到这种人生意义吗？你曾经是这些公司的一部分，你会觉得那是一种极大的 achievement。

所以在我看来，Elon 一直非常一致。他本质上是在追逐对 humanity 有益的东西，同时把组织里的人类个体逼到能够发挥出最佳状态。

当然，这些组织都很 intense；当然，有人来，也有人走；当然，它们不是完美的。

但 SpaceX 代表的是当下人类面向最大使命的追求。而且它拥有最乐观的未来图景。

我确实觉得 Elon 在很多相关评论上是对的。他是 pro-human 的。他的底层愿景是最乐观、最 pro-progress 的愿景之一。我觉得这也是为什么 retail 最后会站到他那边。

Alex Kantrowitz：

最后我想在这里收尾，而且这个问题会稍微拐一下，跟我们刚才的主线不太一样。但我很高兴你写过这一块，因为我觉得它被谈得太少了。

你写过，AI 可能会如何改变 spirituality。你甚至问过这样的问题：在极端情况下，人类会不会 worship AI？如果会，那会是什么样子？

从历史上看，spirituality 本来就是人类对某种更高力量的崇拜。那如果我们真的发明了 AGI 或 superintelligence，几乎可以肯定会有一些人觉得，这就是某种更高存在的具现化。甚至可以说，仿佛我们造出了造物主本身。

这件事想一想就既疯狂又诡异。

所以我很想听听你对这个问题的看法。以及进一步说，当人类开始追求构建 artificial brain，这件事会如何改变人们对 religion 本身的理解，至少对今天地球上传统宗教的理解。

David Cahn：

这是个很好的问题。线头也很深。我尽量用一个较长回答来覆盖它。

我偶尔会有一些 side quest，而且这种 side quest 往往一拉就是好几年。所以我先把这个前提说出来。side quest 并不一定会回到主线。

主线当然是 technology investing，是我们如何构建 humanity 的未来。而我做很多事的根本动力，是 intellectual interest。

我之所以差不多 10 年前开始进入 AI，最初的驱动力就是对“AI 是什么、它在做什么、它有什么潜力”的智识兴趣。

现在回头想当时也挺有意思。那时候我有一种很朴素的感觉：我们拥有这么多 data，结果却只是拿它来做 dashboard，这不是很奇怪吗？10 年前投资世界对 data 的使用，很多时候真的就停留在那个层面。

而我当时的想法只是：也许我们可以用这些 data 做更多。真的是这么基础的一个洞见。我就这样一路往下扯，然后发现有些线程会特别长，而 AI 这条线显然就是一条特别长的线。它已经拉了 10 年，而且我们还会继续拉很久。

另一条线，更多是 personal interest，而不是 career interest，就是 spirituality、God 和 religion。

我成长于宗教环境，也相信 God。

所以对我来说，会不断问一个问题：God 到底是什么？

我觉得，在投资里，你会努力去投资那些 emotionally mature 的人。而作为个人，我们自己的任务之一，大概也是让自己变得 emotionally mature。

而成为 emotionally mature 的一部分，就是努力理解宇宙。我觉得这也是为什么很多 physicist 最后会走向 AI。因为你本质上是在试图理解宇宙。

在我看来，religion 就是一个持续了几千年的“理解宇宙”的探索。我倾向于相信，5000 年的智慧总不至于毫无成果。人类其实一直在前进。而且我不认为古代人类的 IQ 和今天的人相比有本质差异。人类一直都很聪明。

而人类所做的，就是构造出我们今天称之为 religion 的东西，构造出这些系统，试图去触摸宇宙里的 ground truth。

在我看来，一切都在指向同一个 truth。很多人也会这么相信。你读 Quran，读 Torah，读 Gospels，读 Mahabharata，会感到宇宙里其实存在一个 truth，而很多人一直都在试图接近它。我们把那个 truth 叫作 God。

到这里为止，这其实还是一条 side quest，好像跟 AI 没什么关系。

但它又深刻塑造着我们的日常生活。尤其是在 Valley。Valley 是一个极度缺乏 God 的地方。

如果你继续往下追问：为什么 America，甚至不仅仅是 Valley，而是整个 America，会如此缺乏 godliness？

你很快会一路追到 Freud。

Freud 基本上是在说：“God died。”不是 Freud 杀死了 God，而是他意识到，在西方世界，God 正在死去，religion 正在衰退。

然后 Freud 发明了 therapy。接下来 20、30 年里，你会看到 therapy culture 某种意义上占据了一切。

但你再看统计数据：人们依然孤独、依然 depressed、依然 unhappy。

所以我不觉得这些线程是彼此平行、毫不相干的。不是一边 AI 在发生，一边文化危机在发生，而两者毫无联系。

当然，老实说，人们也未必真想听我谈文化问题。我可以理解。毕竟我只是一个投资 startup 的 VC。

但我确实觉得，这场更大的文化变化，在 AI 世界里有回声。

一种看法是，这是一次 Tower of Babel 式的追求。我们正在试图造 God。而 Tower of Babel 的结局并不好。那么这一次会发生什么？它会怎样展开？

另一种看法则是：God 在 20 世纪早期已经在社会层面死亡了，而现在这些人正试图创造一个新的 God。也许他们真的会成功创造出一个新的 God。也许那又会重新给世界注入某种 spirituality。

在这条路上，一定会有大量争论：这到底是好事还是坏事？老实说，我现在还很难形成一个坚定立场。

我还处在刚开始拉这条线的阶段。就像 10 年前我刚开始拉 AI 那条线一样。现在我也只是处在对这个问题的早期学习阶段。

但我可以说的是，越往下拉，我学到的越多。我认为这是一个极其深的智识领域。已经有很多人写过这方面的东西。

而我现在大概只是在第一局、第二局的阶段，尝试更理解一种我会称为 transcendence 的东西。

spirituality 和 religion 是追求 transcendence 的一种方式。而我觉得我们所有人其实都渴望 transcendence。

在某种意义上，这场 AI quest，恰恰也在满足很多人对 transcendence 的渴望。我甚至怀疑，这可能正是它为什么会变得如此巨大的一部分原因。而我也在想，随着技术继续演化，这种动力最终会如何展开。

Alex Kantrowitz：

是啊，光想想都觉得疯狂。我也觉得你说得对。虽然在 AI development 的公共讨论里，这个角度经常完全不被提，但它其实是躲不开的。

当你试图自己创造 intelligent life 时，不管你信不信 God，其中一定存在某种 spiritual parallel。

David Cahn：

有一个问题其实是我们所有人共同面对的：我们要怎样疗愈 society？

现在的 society 是受伤的。

我们怎么疗愈它？

Alex Kantrowitz：

你觉得 AI 能做到这一点吗？

David Cahn：

我不知道。

我觉得它有些方面是好的，也有些方面是坏的。

我确实会担心，它在某种程度上加剧了 loneliness。technology 当然已经让很多人变得非常孤独。

我们的 communities 正在瓦解。现在这个国家里，很多人已经没有 community sense 了。

那你怎么办？

有一种说法是，回到旧有宗教里去。也许那会奏效。也许。

但作为一个 technology guy，你总会觉得回头走很难。那如果不能回头，我们要怎么往前走？

然后你又会听到 Peter Thiel 这类说法，说它像 Antichrist。那到底呢？

我的答案只能是：我不知道。

这也是为什么我会继续拉这条线。我觉得它很有意思。我也希望，随着我们发展这项技术，最终能得到某种乐观的答案，帮助人们拥有更丰富、更充实的人生。

而且我确实觉得，很多正在造这项技术的人相信，一旦我们从日常 labor 里被解放出来，我们就会拥有更丰富的生活。

在犹太传统里有一句话，大意是：没有 Torah 就没有 work，没有 work 也没有 Torah。

意思是，我们既需要 spiritual quest，也需要被生活里真实的事物所锚定，我们需要做事，需要劳动。

所以从某种意义上说，这种双重追求就是 humanity 的双重追求。你既要赚到自己的 daily bread，又想触碰某种 transcendence。

Alex Kantrowitz：

我希望你继续写这个题目。也再次提醒大家，去订阅 David 的 newsletter，`dcahn.substack.com`。

我很期待继续读你的文章。我知道你并不常上节目，所以这次你能来，我真的非常感激。希望以后还能再见到你，David。谢谢你来。

David Cahn：

谢谢，Alex。谢谢邀请我来。

[音乐]

很有意思的一次对话。

Alex Kantrowitz：

真的很有意思，真的很有意思。我觉得这是我们这里更好的一期节目之一。再次谢谢你。

也谢谢所有收听和收看这期节目的人。我们下次 Big Technology Podcast 再见。
