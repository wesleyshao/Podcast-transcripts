---
访谈时间: "2026-08-13"
访谈时间说明: "无法确认实际录制日期，使用 YouTube 发布时间 2026-08-13。"
嘉宾名字: "Vladimir Novakovski"
嘉宾公司名称: "Lighter"
参与嘉宾:
  - 姓名: "Vladimir Novakovski"
    公司或机构: "Lighter"
    职务: "联合创始人兼 CEO"
  - 姓名: "未知"
    公司或机构: "The Rollup"
    职务: "主持人"
播客名称: "The Rollup"
播客url地址: "https://www.youtube.com/watch?v=YJ3iFvRts7c"
youtube_video_id: "YJ3iFvRts7c"
全文提及的关键名词:
  - "Vladimir Novakovski"
  - "Lighter"
  - "Lighter Core"
  - "Robinhood Chain"
  - "Robinhood"
  - "Telegram Wallet"
  - "Ethereum"
  - "Ethereum L2"
  - "ZK proof"
  - "Lighter VM"
  - "Axiom"
  - "Ethereum Foundation"
  - "tokenized stock"
  - "perpetual contract"
  - "market maker"
  - "Citadel"
  - "KYC/KYB"
  - "liquidity layer"
  - "LIT token"
  - "CLARITY"
  - "tokenized equities"
文字稿来源: "YouTube public subtitles: en-orig；完整源文本位于 caption_cache/YJ3iFvRts7c.en-orig.source.txt；官方 Podcast RSS 命中同期节目但未提供满足条件的公开完整 transcript。"
YouTube发布时间: "2026-08-13T23:15:07Z"
字幕来源: "YouTube public subtitles: en-orig"
字幕源备注: "源字幕在嘉宾回答产品公司与基础设施公司定位的问题处提前中断，以下保留已取得的全部源文本语义，不补写未取得内容。"
---

# Lighter CEO: Why Robinhood Chain And Lighter Core Are Built On Ethereum (The Technical Thesis)

## Transcript

**Vladimir Novakovski：** 这就是你必须让规则适应客户所在位置的地方。你仍然希望后端使用 Lighter，并且保持互操作性。问题是，在满足这些限制的同时，能否实现这些规则，并尽可能获得流动性。

**片头：** 就像曼哈顿的街道一样，我会尽快说完。我们超过 70% 的观众还没有订阅。每周我们都会采访金融行业最优秀的一些创业者和投资人。支持频道最简单的方式，就是点击点赞并订阅。现在请放松，开始本期节目。

**主持人：** 我们先从流动性动态、碎片化，以及你们为 Robinhood Chain 构建的新实例的技术架构谈起。为什么你认为，这种方式是进入更受监管、尤其是未来可能在美国境内提供的永续合约市场的更优路径？为什么建立 Lighter 的独立实例是最好的方式？进一步说，你怎么看这些实例之间的流动性和碎片化？

**Vladimir Novakovski：** 架构确实存在取舍。我们正在和很多伙伴合作，其中最大的合作伙伴是 Robinhood 和 Telegram Wallet。两者的结构很不一样。Telegram Wallet 实际使用的是 Lighter Core，Robinhood 使用的是我们新构建的实例。如果你去看 Lithub，也就是名字像 GitHub、但以 L 开头的网站，那里展示了我们已经完成的许多整合和合作。现在合作对象很多样。

就 Robinhood 而言，这种做法对他们很有意义。他们正在发展自己的链，而那条链上已经有很多活动。我认为，这是新链中最成功的启动之一，所以他们押注这条链是合理的。如果 Robinhood Chain 没有获得多少采用，链上唯一有趣的产品又只是永续合约，那么我们可能不会用现在这种方式来构建。但在这条链持续增长的情况下，这种设计就成立。

Robinhood Chain 最终仍然建立在 Ethereum 之上，和 Lighter Core 一样，因此两者具备互操作性。底层技术并不总是容易理解，我们也在持续向用户解释。ZK proof 使做市商能够很容易地在两个实例之间来回转移资金。它们不是彼此隔绝、永远无法互通的两个世界。现在做市商已经可以在几分钟内调动资金，而我们正在推进的 Lighter VM、与 Axiom 的合作，以及和 Ethereum Foundation 一起推动所有 Ethereum L2 更好互操作的工作，未来还会进一步缩短这个时间。

**主持人：** 对交易者来说，这意味着什么？如果你想在 Robinhood Chain 上使用 Lighter 交易 tokenized stock，或者在 Lighter Core 上交易黄金永续合约，只要两边都有流动性，你其实不太关心流动性究竟是怎样到达那里的。但对做市商来说，能够快速平衡账本才是关键。

**Vladimir Novakovski：** 大型做市商会把它看成一个全球统一的大订单簿和一套全球流动性。碎片化不是非黑即白的状态，不是简单地分成“碎片化”或“不碎片化”。你受到的碎片化程度，取决于资金在不同实例之间转移时有多慢。如果资金移动不存在明显延迟，那么你就处在一个非常好的位置。

独立实例的第一个优势，是可以支持不同类型的资产以及不同的客户群。第二个优势来自监管。假设 Robinhood 在美国的核心客户未来通过这套框架交易永续合约，那么如果这是我们和他们正在建设的方向，为这类业务设置一个独立实例就很合理。即使 Lighter Core 和 Robinhood 都取得了相应许可，它们的许可参数和杠杆设置也不会完全相同。传统金融市场也是如此，CME 和 ICE 的全部参数并不完全一致，因为不同平台需要做出不同决定。

因此，基础设施层需要同时提供两种能力：允许每个实例针对自己的资产、客户和监管要求做出灵活选择，又保持互操作性。

**主持人：** 总结一下，你们用运行在数千台 Mac mini 上的 ZK proof 技术，让做市商可以快速在 Lighter Core 和 Robinhood 实例之间切换。这里没有监管障碍，至少技术上是同一个体系。不过，美国用户目前还不能使用，对吗？

**Vladimir Novakovski：** 还不能。

**主持人：** 如果未来 Robinhood 美国核心用户直接在应用中交易永续合约，这些用户会在 Robinhood 的实例上完成 KYC，并拥有该实例上的账户。那在互操作性方面，Lighter Core、Robinhood 当前实例和服务美国用户的实例，能否一起互通？这里的障碍是监管，而不是技术。

**Vladimir Novakovski：** 监管障碍只适用于不愿意完成 KYC 或 KYB 的做市商。那些愿意完成流程的做市商，尤其是很多大型做市商，并不会遇到同样的障碍。

**主持人：** 所以未来可能出现这样的情况：Citadel 同时为多个 Lighter 实例做市。

**Vladimir Novakovski：** Citadel 可能只会参与受监管的实例，但还有一些做市商拥有不同的境内和境外实体，它们可以分别参与两边。链上资金仍然能够快速移动。

**主持人：** 这种实例化愿景是否意味着未来会出现半打左右的 Lighter 实例？

**Vladimir Novakovski：** 只有在拥有很强分发能力的情况下，这个框架才有意义。具备卓越分发能力的平台并不多。不是没有，但也不是成千上万的平台都有这种能力。所以我们会继续观察。Telegram 就是一个拥有强分发能力的例子，但对 Telegram 来说，使用 Lighter Core 反而更合理。我们愿意和这些伙伴合作。

再把问题放大一点。我们已经非常熟悉美国监管，并且在一定程度上参与创新咨询委员会，帮助塑造相关规则。但假设世界上某个司法辖区的规则很特殊，例如交易股票需要 KYC，而交易永续合约却不需要；又假设当地一家新银行希望向客户提供这样的产品。只要它符合当地规则，就需要让客户在自己的监管环境中使用产品，而后端仍然可以采用 Lighter，并保持互操作性。关键在于，在满足当地约束的前提下，能否保留尽可能多的流动性访问能力。

**主持人：** 这让我想到，我们真正看到的可能并不是一个面向大规模分发的永续合约交易前端。随着链上活动增长，以及加密市场重新进入牛市，Lighter.xyz 可能会获得更多网站流量。但更重要的是，你们似乎正在建设一种可以插入现有分发渠道、并提供更好产品的流动性层。你们当然也会为 Lighter Core 的交易者打造好的界面和交易体验，但核心产品其实是一层面向全球消费者前端的永续合约技术底座。

**Vladimir Novakovski：** 这是个很好的问题。我们刚开始创业时，很多早期投资人是 Silicon Valley 的投资人，他们不断问我们：你们究竟是产品公司，还是基础设施公司？

**字幕源中断：** 源字幕在此处结束，未取得后续回答内容。
