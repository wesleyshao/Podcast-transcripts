---
访谈时间: 2026-08-03
访谈时间说明: "本期为博客文章的视频版，不存在独立访谈日期，使用 YouTube 发布时间作为记录日期。"
YouTube发布时间: 2026-08-03T17:36:16Z
嘉宾名字: "Dwarkesh Patel"
嘉宾公司名称: "Dwarkesh Podcast"
参与嘉宾:
  - 姓名: "Dwarkesh Patel"
    公司或机构: "Dwarkesh Podcast"
    职务: "主持人、作者"
播客名称: "Dwarkesh Podcast"
播客url地址: "https://www.youtube.com/watch?v=oZBGAuANX6I"
youtube_video_id: "oZBGAuANX6I"
字幕来源: "Dwarkesh Patel 官方网站公开完整原文，结合 YouTube RSS 赞助说明转写为简体中文"
公开文字稿来源: "https://www.dwarkesh.com/p/why-compute-might-get-10x-more-expensive"
原始语言: "English"
全文提及的关键名词:
  - "Anthropic"
  - "OpenAI"
  - "Fable"
  - "inference"
  - "training"
  - "AI lab"
  - "compute"
  - "GPU"
  - "H100"
  - "GB200"
  - "GB300"
  - "Google"
  - "SpaceX"
  - "frontier lab"
  - "software engineer"
  - "lump of labor fallacy"
  - "Alchian-Allen effect"
  - "Simon-Ehrlich wager"
  - "Moore's Law"
  - "fab"
  - "EUV"
  - "N3"
  - "wafer allocation"
  - "economies of scale"
  - "Mercury Command"
  - "QuickBooks"
companies:
  - Anthropic
  - GOOGL
  - OpenAI
  - SpaceX
industries:
  - 商业航天
technologies:
  - 推理
  - LLM
  - 可回收火箭
  - GPU
keywords: []
tags:
  - Anthropic
  - GOOGL
  - OpenAI
  - SpaceX
  - 商业航天
  - 推理
  - LLM
  - 可回收火箭
  - GPU
---

# Why smarter AI models could drive up compute prices 10x

## Transcript

### 核心假设

**Dwarkesh Patel：**

如果一个达到人类水平的软件工程师可以在一张相当于 H100 的 GPU 上运行，那么按照当前软件工程师的市场薪酬，这张 H100 每年的租金应该超过 25 万美元，约为今天现货价格的十五倍。

我想试一种非常快的博客写法，把写作时间限制在两小时。这样不可能把许多重要的子问题全部钉死，但另一个选择，是对很多令我好奇的话题始终没有任何推进。

今天我想讨论未来几年 AI labs 面临的 compute 局面。

Anthropic 的收入同比增长了十倍。它今年结束时的收入很可能达到约 1,000 亿至 1,500 亿美元。若要延续这条趋势，Anthropic 到明年年底就必须实现 1 万亿美元收入。没有什么深层理由要求趋势必须延续，它完全可能中断，最终取决于 AI capabilities。但先假设它真的延续下去，那么那个世界必须满足什么条件？

### 收入增长与算力增长之间的缺口

AI lab 的 compute 每年大约增长三倍。如果一家 lab 的收入增长十倍，而 compute 仍只增长三倍，那么以下三件事中必须出现某种组合：

1. lab 的利润率提高；
2. compute 价格上涨；
3. lab 把更大比例的 compute 用于 inference。

据我理解，这三件事基本都在发生。

第一，Anthropic 的 Fable inference 利润率从 2025 年的 40% 提高到今年可能超过 80%，尽管新增边际 compute 未必能达到这个水平。第二，compute 现货价格较 2 月低点上涨了 40% 以上，而这很可能仍低估了 labs 实际需要支付的涨幅。第三，根据 Epoch 的数据，OpenAI 在 2024 年约四分之一的 compute 支出用于 inference，现在这个比例肯定更接近 50%，甚至更高。

Labs 其实不愿意让第三种情况持续，也就是不希望把越来越高比例的 compute 花在 inference 上。有人开玩笑说，inference 收入的作用，是说服投资者再给你更多钱，让你购买更多 compute，训练更大的模型。

如果绝大多数 compute 都被用于 inference，某种意义上你是在宣告 AI 进步已经停滞，因为继续投资 training 已经不值得，而你的业务本质上变成了一家 cloud provider。Labs 并不相信事情会这样发展。他们认为，自己现在提供的模型一年后看起来会非常糟糕，而眼下商业化的目的，是建立继续训练更聪明模型所需的商业依据。

于是还剩两种主要解释：lab 的利润率继续提高，或者 compute 变得更贵。

如果领先的一两家 labs 显著领先竞争者，第一种力量会更强。在市场中，你的利润率由自己相对次优替代品好多少决定。若要仅靠利润率解释前述增长，labs 到明年年底的利润率必须升至 95% 左右。我觉得这听起来相当疯狂。但我确实认为，AI lab 的收入继续以惊人速度增长是可信的。

### Labs 真正需要的 compute 已经更贵

因此，要解释明年年底收入可能达到 1 万亿美元的疯狂世界，还剩一个重要效应：compute 会贵很多。这已经开始发生。

如果只看 labs 真正需要的那一档 compute，价格涨幅更明显。Labs 显然不能依赖临时现货实例。他们需要保障模型权重和客户信息的安全，也需要足够大的规模，以实现良好利用率和灵活性。

观察这一档市场有多疯狂，可以看 Google 和 Anthropic 向 SpaceX 租用 compute 的价格。据报道，Google 每月支付 9 亿美元，租用 11 万张由 GB200 和 GB300 混合组成的 GPU。按每张 GPU 每小时计算，这大约是现货价格的两倍，而当前现货价格本身已经比 2 月高出 40%。

这里最关键的结论是：随着 AI 模型变得更聪明，它们可以用同样数量的 compute 变现更多价值。

假如真正达到人类水平的软件工程师能够在一张相当于 H100 的 GPU 上运行，按今天软件工程师的市场薪酬计算，这张 H100 每年的租金应该超过 25 万美元，是今天现货价格的十五倍。

### 软件工程师供给增加会不会压低价值

当然，你可能会认为，如果突然多出一千万名软件工程师，边际软件工程师的价值就会下降，因此 H100 未必能创造今天十五倍的收入。但我并不知道这个判断是否正确。

如果把同一论点用于人类劳动而不是 AI，它就是经典的“固定工作总量谬误”（lump of labor fallacy）。经济学家通常认为，高技能移民不会在长期压低工资，因为专业化与创新会提高劳动价值。

这一次的劳动供给冲击或许大到、快到足以让传统经验失效。但如果我们相信标准经济学关于劳动的判断，那么劳动的边际价值，以及相应的 compute 边际价格，仍应维持在惊人的高位。

### 这个世界的五个后果

**Dwarkesh Patel：**

第一，头部模型越擅长用 compute 赚钱，后来者追赶就越困难。

假如到 2028 年软件工程已经实现自动化，而 compute 价格涨到现在的十五倍，那么一个没有收入的挑战者，要与 frontier labs 争夺 compute 会困难得多。

第二，谁能训练出最优秀、效率最高的模型，谁就能收取远高于今天的利润率。

这符合 Alchian-Allen effect：当两种不同品质的商品都叠加一项固定成本后，高品质商品相对变得更便宜，需求会向高品质商品转移。

如果 H100 每小时要 20 美元，使用一个较弱、效率较低的模型会既昂贵又愚蠢，因为为了得到同样结果，它会在昂贵 compute 上消耗更多 token。如果一家 lab 训练出的模型更能节约这种稀缺资源，它就能收取很高的溢价。

既然用户无论如何都要直接或间接支付高昂的底层 compute 费用，那么再多付一点，使用在相同 compute 上运行的最佳、最高效模型，就会变得合理。

第三，许多今天流行的 AI 应用会因为成本上涨而被挤出市场。

AI 今天相对便宜，至少与人类劳动相比相对便宜，部分原因是它还做不了顶尖人类能做的很多事情。未来某个时点，这一点将不再成立。届时，用 GPU 制作低质量短视频内容，很可能会被更高价值的用途挤出去。

第四，这种预测也很像历史上对稀缺性判断错误的那些案例。

Simon-Ehrlich wager 就是一个例子。Paul Ehrlich 曾下注，截至 1990 年前十年，一篮子大宗商品的成本会升高而不是下降。这场赌局在大众经济学讨论中很有名，因为它常被用来说明 Ehrlich 的 Malthusian 世界观被证伪。他低估了市场信号和人类创造力可以怎样节约稀缺投入。不过，另一些分析显示，如果赌局发生在不同十年，Ehrlich 也可能获胜。

我猜 Simon-Ehrlich 所用的大宗商品篮子，并不是 compute 的正确参照类别。Compute 供给的弹性小得多，吸收大规模需求冲击的能力也弱得多，可替代手段也不像开采不同金属那样丰富。

当前每年约三倍的 compute capacity 增长，可以拆成三个倍数相乘：Moore's Law 贡献约 1.4 倍；新建 fab 贡献约 1.2 倍，而至少到 2030 年仍会受到 EUV 设备供给限制；AI 从其它设备手中取得 leading-edge wafer allocation，贡献约 1.8 倍。

最后一项也会撞墙。到 2027 年底，AI 在 N3 wafer allocation 中的占比预计会从 60% 升至 86%，届时可继续转移的空间已经很小。很难让这三个输入中的任何一个显著加速，而且 wafer allocation 在一两年内就会趋于饱和。

第五，compute 最终仍会重新变便宜，但不是在当前阶段。

未来某个时点，机器人将能够把海岸上的 silica sand 和矿山里的 copper 转化为计算机。届时 compute 价格应更接近原材料和工具成本。

我讨论的只是当前这个阶段：AI compute 每年只增长三倍，还不足以抵消 AI 每年变得更有用所带来的价格上涨效应。

### 模型业务的规模经济与权力集中

**Dwarkesh Patel：**

顺便说，Anthropic 收入每年增长十倍，而 compute 只增长三倍，说明模型业务中存在非常强的 economies of scale。

从逻辑上看这很合理。训练模型时，你只需支付一次性成本，让模型学会各种技能，之后可以把这笔成本分摊到所有用户身上。这与人类劳动不同，每一个新的人类实例都必须从头训练。

我并不希望自己生活在一个 intelligence 具有如此强规模经济的世界里，因为我担心权力集中。但现实似乎正是如此。

关于前面使用的利润率数字，再补充一点：混合 inference 利润率已经超过 70%，因此我猜 Fable API 的利润率超过 80%。这只是一个凭直觉提出的估计，不是经过严密验证的结论。

### 赞助信息：Mercury Command

**Dwarkesh Patel：**

感谢 Mercury 赞助这篇文章的视频版。Mercury 内置的 AI 工具 Command 可以帮助我完成月末结账，节省大量时间。每个月底，Command 会把交易自动分类，并解释每一个选择的理由。我只需检查、修正不准确之处并批准，随后 Mercury 就会把所有内容同步到 QuickBooks。可以访问 mercury.com/command 开始使用。
