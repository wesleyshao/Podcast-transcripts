---
访谈时间: 2026-08-05
访谈时间说明: 无法确认实际访谈日期，按 YouTube 发布时间 2026-08-05 使用
YouTube发布时间: "2026-08-05T14:00:08Z"
嘉宾名字: "Philip Johnston"
嘉宾公司名称: "Starcloud"
参与嘉宾:
  - 姓名: "Philip Johnston"
    公司或机构: "Starcloud"
    职务: "联合创始人兼 CEO"
  - 姓名: "Garry Tan"
    公司或机构: "Y Combinator"
    职务: "The Lightcone 主持人，具体职务未知"
  - 姓名: "Harj Taggar"
    公司或机构: "Y Combinator"
    职务: "The Lightcone 主持人，具体职务未知"
  - 姓名: "Jared Friedman"
    公司或机构: "Y Combinator"
    职务: "The Lightcone 主持人，具体职务未知"
  - 姓名: "Diana Hu"
    公司或机构: "Y Combinator"
    职务: "The Lightcone 主持人，具体职务未知"
播客名称: "The Lightcone"
播客url地址: "https://www.youtube.com/watch?v=A9JDkiYEhfY"
youtube_video_id: "A9JDkiYEhfY"
字幕来源: "YC Root Access 官方文章公开完整 transcript"
公开文字稿地址: "https://www.ycrootaccess.com/p/starcloud-solving-ais-energy-problem"
原始语言: "English"
全文提及的关键名词:
  - "Starcloud"
  - "Lumen Orbit"
  - "Starcloud-1"
  - "Starcloud-2"
  - "Starcloud-3"
  - "Starcloud-4"
  - "NVIDIA H100"
  - "NVIDIA H200"
  - "NVIDIA B200"
  - "NVIDIA Jetson"
  - "Blackwell"
  - "ARM"
  - "SpaceX"
  - "Falcon 9"
  - "Starship"
  - "Starbase"
  - "FCC"
  - "Benchmark"
  - "YC"
  - "GTC"
  - "solar"
  - "launch cost"
  - "$50 per kilogram breakeven"
  - "$500 per kilogram breakeven"
  - "20GW"
  - "10 terawatts"
  - "88,000 satellites"
  - "radiation"
  - "heat rejection"
  - "radiator"
  - "GPU"
  - "AI data center"
  - "optical communication"
  - "Bitcoin mining"
  - "ASIC"
  - "automotive-grade components"
  - "particle accelerator"
  - "Brookhaven National Lab"
  - "Knoxville cyclotron"
  - "heavy ions"
  - "protons"
  - "phase change material"
  - "immersion cooling"
  - "DC-to-DC converter"
  - "AC-to-DC converter"
  - "Starlink laser terminal"
  - "synthetic aperture radar"
  - "SAR"
  - "DOD"
  - "Space Rubin-1"
  - "AWS Outposts"
  - "EC2"
  - "Space Force"
  - "Golden Dome"
  - "McKinsey"
  - "NASA"
  - "Varda"
  - "AstroForge"
  - "Asimov"
  - "Gemini"
  - "Stoke Space"
  - "Nova Rocket"
  - "Rocket Lab"
  - "Neutron"
  - "Blue Origin"
  - "New Glenn"
  - "LEO"
  - "GEO"
  - "ISS"
  - "International Space Station"
  - "natural gas generators"
companies:
  - SpaceX
  - NVDA
  - GOOGL
  - AMZN
  - BlueOrigin
industries:
  - 数据中心
  - 商业航天
  - 半导体
technologies:
  - 可回收火箭
  - GPU
  - 比特币
  - ASIC
keywords:
  - 融资
tags:
  - SpaceX
  - NVDA
  - GOOGL
  - AMZN
  - BlueOrigin
  - 数据中心
  - 商业航天
  - 半导体
  - 可回收火箭
  - GPU
  - 比特币
  - ASIC
  - 融资
---

# The Case for Data Centers in Space

## Transcript

Philip Johnston：每一家太空公司第一件该做的事，就是先把自己能拿到的第一个发射名额订下来。

Jared Friedman：在他们真正把要发射的东西造出来之前？

Philip Johnston：对，在东西还没造出来之前，甚至可能在你都还不知道自己到底要发什么之前。先把发射订下来，对太空公司来说是一个极强的 forcing function。我们是 2024 年 1 月 1 日创立公司的，1 月 2 日就订下了 SpaceX 最早可用的 rideshare 发射。我们当时的想法就是，好，反正那枚火箭上一定会有某个东西是我们的。我还不能百分之百确定那到底是什么，但一定会有东西上去，一定会发生点什么。

Diana Hu：听起来这和所有软件公司的建议一样，你就是得不停上线、再上线，本质上是同一回事。

Garry Tan：欢迎回到新一期 The Lightcone。今天我们请到的是 Starcloud 联合创始人兼 CEO Philip Johnston。Starcloud 正在把 data center 建到太空里，以解决 AI 在地球上制造出来的能源瓶颈。今年早些时候，他们完成了由 Benchmark 领投的 1.7 亿美元融资，并在 Demo Day 后仅 17 个月就成为 YC 历史上增长最快的独角兽。Philip，欢迎来到 The Lightcone。

Philip Johnston：非常感谢邀请。

Garry Tan：那我们就直接开始，为什么是太空 data center？

Philip Johnston：Starcloud 做的是太空 data center，目标是解决 AI 的能源瓶颈。我们很快就会撞上一个现实约束，就是在地面上还能在哪里继续建设新型能源项目。把这些东西建到太空里，我们就能获得几乎无限、而且低成本的能源，形式就是 solar。当然，太空里也有别的成本，比如 launch cost。但 launch cost 正在非常快地下行，新的运载工具不断上线，Falcon 9 已经成熟，Starship 也快来了。这就是我们为什么要在太空里建 data center。

Harj Taggar：这个想法你是怎么想到的？这可不是普通人会冒出来的那种点子。

Philip Johnston：我之前在 McKinsey 做了几年，和不同国家政府的 space agency 一起工作。那时候我已经能看出来，launch cost 正在非常快地下行。2023 年初的时候，我某个周末心血来潮，跑去了一趟德州 Starbase，看他们在那边搭 Starship 发射体系，那会儿连第一次发射都还没发生，当时根本没多少人在关注。我在那里看到的是，他们在建设极其夸张的产能。他们在造两座 Starship gigafactory，目标产能差不多是一天造三艘 Starship。由于 Starship 还是可复用的，如果拉长到三四年的时间尺度看，这意味着我们把东西送上太空的能力可能会比今天高出几千倍。所以我就开始想，如果把时间往前拨一拨，假设 launch cost 只有现在的十分之一，发射能力又是现在的一千倍，那今天看起来不成立、未来会成立的事情到底是什么？

Philip Johnston：于是我开始回想小时候看 sci-fi 时接触到的那些概念，比如 space-based solar，在太空里铺巨大的太阳能板，然后把电打回地球。我联系了几个认识的太空行业朋友，又被介绍给更多人，开始一起想，如果 launch cost 真的比今天低得多，到底什么会变得可行？

Jared Friedman：我很好奇，在你做这个推演的过程中，除了现在这个方向之外，还有没有别的想法也冒出来？如果太空真的变便宜了，人们还能在上面造什么？

Philip Johnston：当然有，一大堆。我们认真看过太空制造，对应的例子就是 Varda；也看过 asteroid mining，YC 里就有 AstroForge；还看过太空酒店，总之就是所有那些在 launch cost 大幅下降后有可能成立的事情，我们几乎都扫过一遍。

Jared Friedman：那为什么最后 data center 是最好的选择？

Philip Johnston：因为 data center 很适合作为第一件做的事，它不需要把产品再送回地球。像 asteroid mining、太空制造、太空酒店这些方向，都绕不过一个非常昂贵的 reentry 过程。我们最开始其实真的是在做 space-based solar，也就是巨大的 solar 面板，发电后再把能量打回地面。这其实是 1960 年代就有的概念，Asimov 在 1940 年代的文字里都写过。问题在于，space-based solar 在把能量从太空传回地球时，会损失 95% 的能量。所以公司前两个月我们干的真就是这个，因此那时候公司名字叫 Lumen Orbit，意思也是 orbit 里的光。后来我们开始问自己，假设真把这股电送到了地球，它最终是拿来干嘛的？其实早在 2023 年，大多数新建能源项目的主要需求方就已经是 data center 了。

Philip Johnston：所以我们就想，好，那不管直接还是间接，这些电最后都会流进 data center。那就把数学重新算一遍。我们最早算的是，space-based solar 要在什么样的 launch cost 下才能 breakeven，算出来差不多是每公斤 50 美元，也就是 $50 per kilogram breakeven。然后我们又花了一个月，认真去算如果是把 data center 直接放到太空里，launch cost 的 breakeven 要多少，结果得到的是一个离现实近得多的数字，大约每公斤 500 美元，也就是 $500 per kilogram breakeven。我们现在依然认为这就是那个关键平衡点，于是公司很快就转向了这个方向。

Garry Tan：Philip，你们在 2025 年 11 月发射了 Starcloud-1，那显然是一个情绪很强烈的时刻。你能讲讲那到底是什么感觉吗？

Philip Johnston：太夸张了，真的很不可思议。先给大家一点 Starcloud-1 的背景。我们先定下了一个 18 个月后的发射日期，然后一开始准备做的东西其实挺不惊艳的。最早打算带几颗 NVIDIA Jetson 上去，这类芯片以前在太空里飞过，我们想做一些新的 workload。后来 Adi 加入后说，不行，这也太普通了，我们得做一件酷得多的事。最后我们真往上放了 5 块 GPU，3 块来自 NVIDIA，2 块来自 ARM。但最有意思的是那块 NVIDIA H100。我们做了很多很疯的事。比如它需要做 thermal cycling，可我们根本没时间。我们本来预约了 thermal vacuum chamber，可那之前我们必须先知道，如果把这块东西里面的 phase change material 一次次加热、冷却、再加热、再冷却，会不会把什么东西裂掉。

Philip Johnston：结果到了要把设备运走的那天凌晨 5 点，我们还在通宵干活。Adi 和 Ezra 把这玩意儿整个泡进冰水里降温，我看着都傻了，问他们，你们确定电子设备这么搞没问题？他们说别担心，完全没事。然后把它从冰水里捞出来，再拿吹风枪把它加热，把里面那些蜡全融掉，再丢回冰水里。说实话，这东西最后能工作，简直是个奇迹。

Garry Tan：你们这种公司，真的是想干就能干。

Philip Johnston：确实，想干就能干。这类事也只有 startup 能这么干。因为我们其实拿到过一家传统 prime contractor 的报价，问他们如果按他们的方式做 Starcloud-1 要多少钱，他们给的数字是 7500 万到 1 亿美元。结果我们把整个 Starcloud-2 连同发射一起做下来，只花了 200 万美元。所以发射前那段时间其实特别疯狂。

Philip Johnston：而且我们还拿到了我见过最震撼的分离视频。我想我们现在可能会播出来。它分离的时候，一半概率是在地球阴影后面，你什么也看不见；另一半概率则不是背着地球轮廓分离，就能看到极其完美的画面。那真的是我见过最漂亮的部署视频。后来 Jensen 在今年 GTC 上走上舞台时，背后那块五层楼高的大屏幕上放的就是 Starcloud-1 的分离视频，太夸张了。所以是的，看着它在轨展开，那个感觉真的难以形容。

Jared Friedman：发射那次团队人都在哪？你们全员都去了？

Philip Johnston：对，我们把全团队都带去了。当时 Starcloud-1 发射时团队总共也只有 12 个人，所以我们整个团队都去了佛州。现场还有 100 个左右的朋友、家人和投资人，有些同事还把孩子也带过去了。那真是很美好的一天。我们之后会发一个幕后视频，里面会有不少家人相关的片段。

Jared Friedman：从火箭升空，到卫星部署，再到第一次上电并确认这东西真的能用，这中间具体隔了多久？

Philip Johnston：火箭大概是午夜升空的。我们当时都在所谓的 banana bleachers 上看，那是 Apollo 时代就很有名的观看区，不过那次是在半夜。升空后到了凌晨 1 点左右，看台关闭，所有人都得上大巴离开。我们当时还想，靠，我还以为能现场看到部署。结果我坐在出租车后排，拿手机看 spacex.com 的直播，突然看到它开始部署了，我整个人都惊了。之后差不多过了 12 个小时，我们完成了 first contact。其实这已经算不错了，通常至少要 24 小时才能 first contact。再往后还有大概两周的 commissioning period，而我们在软件上遇到了一堆问题。

Philip Johnston：整个卫星每两个小时就会重启一次。原因是系统里大概有 20 种不同的 failure trigger，其中某一个在不停触发，但我们不知道是哪一个。更麻烦的是，地面站 pass 最快也要一个半小时才来一次，有时更久。所以我们只能一次手动关闭一个触发器，其他都打开，然后等下一次地面站经过，看看是不是还重启，以此排查。光这个软件问题就花了三天。再过了两周，我们才陆续开始给不同 payload 做 commissioning、逐个开启。之后我们训练了第一个模型，跑了第一个版本的 Gemini，做了第一次在轨模型 fine-tuning，还做了第一次针对卫星影像的高功率 inference，诸如此类。

Garry Tan：我们现在说话的这一刻，Starcloud-1 刚刚飞离中国上空，好像正要进入日本。看起来它飞得真的非常快。

Philip Johnston：对，它的速度大概是每小时 17000 英里，绕地球一圈大概只要一个半小时。

Garry Tan：所以等到 Starcloud-4 左右的时候，它就不会只是单颗了，而会变成一个真正覆盖地球的巨大网络。

Philip Johnston：对。从 Starcloud-3 开始，我们的规模会到 88,000 颗，它们都会飞起来。现在这颗走的是所谓的 mid-inclination orbit，所以不会飞越两极。这也说明这颗验证星到底有多 janky，它连正确的轨道都没上，但至少足够让我们测试硬件。下一颗会飞越两极，那样我们就能做到 24 小时持续在太阳下。

Jared Friedman：要做到那一点，你们是不是得在卫星上装推进器，把它推到那个轨道？

Philip Johnston：最终量产状态下会直接部署到那个轨道上，但无论如何还是需要推进器，因为高层大气依然会产生 drag，你得不断维持轨道。

Diana Hu：要让这一切成立，你们到底要做哪些工程和物理层面的取舍？你们做的事情本质上像是在拿无限能源，因为太阳本来就是天然的 fusion reactor，一个巨大的天体不断发生核反应。你们在太空里有几乎无限的能量，也有大量空间，而这些恰好是地球上最稀缺的东西。但换来的代价就是另一组极难的问题，比如 interconnect，数据要怎么和地面来回传；比如 cooling，很多人以为空间是冷的，但实际上不像地球上有空气可以对流带走热量，所以散热反而需要很疯狂的解法；还有 radiation，会导致处理器 bit flip；再往外还有 solar panel 怎么做得足够大、怎么展开，等等。

Diana Hu：这些只是我马上能想到的，真正困难的地方肯定还有很多，太多东西都极难做。

Philip Johnston：对，你说得没错，确实有很多工程挑战。现在最核心、而且仍然最关键的两件事，也是我们工程团队几乎一分为二在做的两条主线，第一就是你刚才说的，在真空里怎么把热排掉，也就是 heat rejection；第二是在更高 radiation 环境下，怎么让芯片正常工作。其他一些问题已经有人在解决，比如 interconnect 方面，我们刚和 SpaceX 签了合同，下一批 20 颗卫星会装 Starlink laser terminal，这能提供高带宽、低延迟连接。别的一些问题也有人在解决。真正由我们自己啃的，是散热和 radiation 这两件事。所以在 thermal management 这一侧，我们正在做一种很大的、低成本、低质量的可展开 radiator。

Philip Johnston：radiator 这个东西在太空里并不新，不是什么新物理。更像是制造与工程挑战，因为 International Space Station 早就有能排掉大量热量的 radiator 了，机制非常类似，本质上就是液体回路把热带走。难点在于既要便宜，又要轻。我们的 radiator 在每瓦散热对应的质量上，至少比 ISS radiator 低 10 倍；在每瓦散热对应的成本上，至少比 ISS radiator 低 500 倍。所以拿 ISS 当 benchmark，在成本上其实非常容易超越。至于 radiation，我们的办法就是做大量地面测试，在不同 particle accelerator 里测。我们已经在 Brookhaven National Lab Particle Accelerator 做了好几轮 heavy ions 测试，也去 Knoxville 那边的 cyclotron 做高速度 proton 测试。我们会把所有硬件都运过去，我的联合创始人 Adi 还会穿着防护装备进进出出地折腾。

Philip Johnston：基本上，你会在 24 小时内把设备暴露在相当于五年任务期的 radiation dose 下。然后所有 telemetry data 会反过来指导我们做 shielding 和软件层面的 bitflip 缓解。我认为现在全世界可能只有我们知道，如果你拿高速度 proton 和 heavy ions 去轰一颗 H100、B200、H200，它们分别会在什么条件下失效。

Jared Friedman：所以你们需要改底层电子设计吗，还是说主要是在外面做 shielding 就够了？

Philip Johnston：两者都要。我们确实会加 shielding，但很多时候核心其实是 component selection。比如所有 SSD、整个 power delivery system、各种 power converter，我们通常会一口气测 10 个不同组件，最后选表现最好的那个。我们的策略是尽量不用 space-grade、rad-hard 那类元件，而是优先采用现成的 automotive-style components，因为便宜得多。而且大多数人从来没把这些东西拿去 radiation chamber 里认真测过。

Diana Hu：我觉得这其实就是 SpaceX 能把很多卫星成本打下来的秘密之一。他们不是去用那些贵得离谱的 space-graded electronics，而是用普通供应链里随处可得的器件，把测试做透，只要能工作就行。我记得 Astranis 也是类似思路，这样他们的通信卫星才能真正跑起来。因为他们是在 GEO，radiation 更强。你们也是 GEO 吗？

Philip Johnston：不是，我们在 LEO。

Diana Hu：明白。

Jared Friedman：你们刚开始和别人说，要把 data center 放进太空时，别人一般是什么反应？

Philip Johnston：很长一段时间里，别人的反应都是，这大概是我听过最蠢的想法。所以是的，我们其实曾经申请过一次 YC，然后去融资，想按 1000 万 post-money 的 SAFE 融 200 万美元。结果花了三个月，至少被 100 家 VC 拒了。哪怕进了 YC 之后，我们在 Demo Day 后出去融下一轮，我记得在拿到第一张支票前也至少被 20 家 VC 拒掉。

Jared Friedman：这是那种对投资人来说极不受欢迎的点子之一。如果你真的把他们说的话都听进去，你可能早就放弃了。我很好奇，他们不投的理由主要是什么？他们到底看错了什么？

Philip Johnston：很多人很难想象一个低 launch cost 的世界。公平地说，我们今天也还没完全走出那片林子，Starship 项目还有很多事必须做对，这套逻辑才会真正成立。所以这是一方面。另一方面，这个故事听起来太像 sci-fi 了。要让这件事成立，其实要两股力量同时收敛。第一是 launch cost 真的往下掉，而且你得相信它会继续掉；第二是在地面上建东西变得越来越难。可能两年前，这第二件事还没有今天这么明显。现在人们会说，好吧，纽约已经在禁止新 data center 建设了，接下来还会有另外七个州禁。等这两件事叠到一起，这个故事在投资上就明显更可投了。

Diana Hu：而且我觉得还有一点，在听你把整个工程和物理问题解释完以后，这件事其实是做得出来的。它不是那种用第一性原理一推就散掉的 sci-fi，它真的能造。

Philip Johnston：我之所以一直有信心，核心原因是我们的工程团队非常强。如果全世界最好的太空工程师告诉你这件事能做，而且坦白说，我自己的背景并不是太空工程，但我的两位联合创始人，一个来自 SpaceX，一个之前在给 NASA 造卫星，如果他们都说能做，那对我来说就足够了。

Harj Taggar：你们有了点子以后，尤其是进了 YC 之后，是怎么把这个大问题拆成执行计划的？做软件的人会想 MVP，尽快上线、拿反馈，但你们这是太空 data center，没法按普通软件那一套来。

Philip Johnston：我对所有太空公司都有一个非常具体的建议，第一件事就是把最早能拿到的发射订下来。

Jared Friedman：在真正把要发的东西造出来之前。

Philip Johnston：对，在东西还没造出来之前，甚至还不知道到底要发什么之前。先订发射，对太空公司是一个极强的 forcing function。我们 2024 年 1 月 1 日成立公司，1 月 2 日就订了 SpaceX 最早的 rideshare 发射，而且很便宜，大概 30 万美元。

Jared Friedman：那个发射当时离你们有多远？

Philip Johnston：一开始是 18 个月后，后来又推迟到了 21 个月。我们当时就想，好，不管怎样，那枚火箭上一定会有东西属于我们。我还不能完全确定到底是什么，但一定会有东西飞上去。这一点很有意思。

Diana Hu：听起来真的和软件公司一样，就是一直 launch、一直 launch。

Philip Johnston：对。其实我们最早打算发的东西非常不惊艳，本来是想放一颗 Jetson 芯片上去。这种芯片以前很多卫星都飞过，我们只是想拿它做 edge processing 之类的事。后来我们很早就经历了一次联合创始人变化，Adi 从 SpaceX 加入。他当时的反应是，这也太 lame 了，干脆直接上 H100。我们说，Adi，你不可能把 H100 放上卫星。他说，当然可以。那时候无数人都说，这是物理上不可能实现的。大家普遍认为，data center 级别、功耗密度这么高的 GPU，不可能在轨运行。

Jared Friedman：他们为什么会觉得不可能？

Philip Johnston：有两个原因。第一是 thermal 问题，这类芯片功率密度极高，会产生大量热。第二是它们从来没在太空 radiation 环境里被认真测试过。第一个问题我们用了一个很离谱的解法：把整个系统浸没在一种 phase change material 里。Starcloud-1 上所有东西都浸在这个材料里，所有组件、供电、内存，全部如此。你可以把它理解成 immersion cooling，但对象是整颗系统。以前没有人想过在太空里这么干。这不是一个特别 scalable 的方案，因为 duty cycle 会比较低，你要等它融化，然后过一段时间它又会重新凝固。但它足以证明，H100 在太空里是可以跑起来的。下一代我们会换成 directed chip liquid cooling 架构，那样就能持续运行。

Philip Johnston：不过这一点我要把功劳完全给我的联合创始人 Adi，这些相当离谱、也相当疯狂的思路很多都是他提出来的。

Jared Friedman：如果要走到真正 commercial scale 的 data center，做到能赚钱、能盈利，显然中间还有很多步。你们当时是怎么规划这个路径顺序的？

Philip Johnston：我前面说的第一步，就是先订最早那次发射，做出我们能做的最低可行版本。第二步，是造出一个可以卖给客户的产品，那就是 Starcloud-2。这是一台 10 kilowatt 的 spacecraft，我们可以把算力卖给政府和军用卫星。第三步，才是能够卖给 hyperscale data center 客户的产品，也就是 Starcloud-3。它是一台 200 kilowatt、3 吨重、长度大约 6 米的 spacecraft。用这种规格，每一艘 Starship 可以装下 50 台，也就是每艘 Starship 能带来大约 10 megawatts 的新增算力容量。我们已经向 FCC 提交了一份由 88,000 颗组成的 constellation 申请。换算下来，就是 20GW 级别的新增计算容量。

Diana Hu：哇。

Philip Johnston：而且在 dawn-dusk synchronous orbit 这种轨道上，我们理论上最多能塞到 10 terawatts，差不多是整个美国电网总功率的 20 倍。

Diana Hu：给大家一点背景，地球上今天最大的 data center deployment 有多大？你刚刚说的是 20 多 gigawatts，这太夸张了。今天地面最大的单体规模大概是什么级别？

Philip Johnston：大概 1 gigawatt，这已经算最大的了。

Jared Friedman：那这一切要多久才会变成现实？

Philip Johnston：这件事非常依赖 launch cost。按 Elon 的说法，Starship 可能今年底就能到位；保守一点说，也可能要到明年年底，或者 2028 年初，Starship 才开始真正部署并把发射频率拉起来。他们事实上也在逐步淘汰 Falcon 9，会把商业客户慢慢迁到 Starship 上。另外还有一批新运载火箭也在上线，比如 Stoke Space 的 Nova Rocket、Rocket Lab 的 Neutron、Blue Origin 的 New Glenn。所以我会说，真正和地面 data center 直接竞争的阶段，大概会在 2020 年代末开始加速。

Garry Tan：所以你们的客户，本质上就是任何想买算力的人。只不过最开始是……

Philip Johnston：最开始会是政府和军方。未来两三年我们已经拿到了 4 个来自不同 DOD 和政府机构的合同。

Garry Tan：而且最初的一批客户，也会是那些想把算力用在太空业务上的人，对吧？

Philip Johnston：对，完全正确。现在很多卫星真正的瓶颈，是它们能 downlink 回地面的数据量太少。所以我们会在第二颗卫星上装 3 个 optical terminal，它们能把极大量的原始卫星影像以及 SAR，也就是 synthetic aperture radar 数据，传给我们。我们在轨把这些数据处理完，再把处理后的 insight 快速 downlink 回地面。这个 insight 可能就是一艘船的坐标，类似这样。

Garry Tan：说到 NVIDIA，你们现在和他们在 chip design 上是怎么合作的？随着规模扩大，你们是不是得在设计层面做一些变化，比如让芯片更抗 radiation，还是别的什么？

Philip Johnston：对，我们和 NVIDIA 合作得非常紧密。我们最近刚宣布了一个正在与他们共同推进的 Space Rubin-1 芯片，它就是为太空环境设计的。我们为了让 H100 能在太空里工作，对它做了非常重度的修改。为了减重，我们拆掉了很多东西，比如 AC-to-DC converter、cold plate 等等，全都剥掉了；然后我们把板子做得更 stiff，也让它具备 radiation tolerance。正因为如此，NVIDIA 现在非常关心，到底有没有人掌握高功率 GPU 在太空环境中的运行数据。所以我们现在和他们非常紧密地合作，设计这颗新的太空芯片。事实上，有很多非常简单的改动，就能让这类芯片在太空里运行得好得多。我们现在就在做这些事情。

Diana Hu：我觉得一个很重要的点是，让 GPU 原生跑在 DC 上，就可以绕开 AC 转 DC 这一步。因为 solar panel 本来最怕的就是中间那一层转换损耗，会损失很多能量。

Philip Johnston：完全正确，而且那一步很难做。我们的 solar panel 直接产出的就是 DC，所以根本没必要先转成别的。我们只需要 DC-to-DC converter，这要比 AC-to-DC converter 好得多。

Diana Hu：那其实这也会给很多别的公司打开机会，比如无论在太空、水下还是地面，只要能直接吃 solar 的 DPU data center，理论上都能受益。

Philip Johnston：对，这项技术当然也可以被别人用在别的场景里。

Garry Tan：你多讲讲 Starcloud-2 吧。里面真的还会放一个 Bitcoin miner 吗？

Philip Johnston：会。明年我们会带一颗用于 Bitcoin mining 的 ASIC 上去，crypto 社区对此兴奋得超出我的预期，老实说我之前没想到他们会这么激动。

Harj Taggar：crypto 社区确实很爱这种叙事。

Philip Johnston：想让我发 Starcoin 的人多到你无法想象。外面好像甚至已经有一个 Starcloud meme coin 了。

Garry Tan：对，别买。那不是官方的，不要去买。

Philip Johnston：那个 Starcloud……

Garry Tan：meme coin。

Philip Johnston：所以是的，我们会带一个那样的东西上去。还会带更多 H100，也会带 Blackwell 芯片。我们还在和 AWS 合作，把他们的 Outposts 硬件发上去。那是他们给客户在本地部署 EC2 实例用的 on-premises server blade，这对我们的军用客户尤其有用。

Harj Taggar：我们之前聊到一个话题。过去几年在 YC，我们明显感觉 hard tech 公司融资很难，投资人的胃口并不大。但过去 6 个月好像突然变了，这当然是好消息。我很好奇，从你的角度看，在 YC 期间融 seed，以及后来从 Benchmark 融这么大一轮，背后的真实过程是什么？今天做 hard tech 创始人融资到底是什么感觉？

Philip Johnston：我们最早在 2023 年底融资时，想融的是 200 万美元，10 million post。结果足足花了三个月，差不多 100 家 VC 说了不。那时候 deep tech、hard tech、space 都不是大家眼里的热门方向。YC 之后，我们的融资也花了挺久。我记得在 Demo Day 那轮里，我们至少又被 20 家 VC 拒过，才拿到第一张支票。后来风向确实彻底变了，deep tech 现在好融多了。我觉得原因有几个，其中一个就是很多人开始觉得软件已经没有 moat 了，我认为这大概率是对的。

Harj Taggar：很好笑的是，整个 hive mind 几乎是一瞬间就切换了。

Philip Johnston：看起来确实是这样。

Harj Taggar：速度快得惊人。像 SaaS 股票那次，Claude code 一出来，SaaS 上市公司股票就都往下掉。然后突然之间，我觉得这是我见过公共市场影响 Demo Day 最快的一次，所有人一下子都变成，好，我们现在得投 hard tech。

Philip Johnston：对，这很有意思。我觉得大家现在就是更愿意投 hard tech 了。我们好像还是 Benchmark 投的第一家太空公司。

Harj Taggar：如果有些细节你能讲的话，这轮到底是怎么拼起来的？你觉得 Benchmark 到底看中了你们什么？

Philip Johnston：坦白讲，那轮融资从外面看上去比实际容易得多。很多 VC 手里本来就有很大的 SpaceX 仓位。融资进行到一半时，SpaceX 对外放出消息说他们也在做和我们一样的事情，而那在之前其实并不公开。所以凡是内部有 conflict policy 的机构，立刻就会觉得，好，这轮我们 conflict out 了。不过到了后半段，速度确实明显快起来。我不想乱替别人下定义，但我们的 partner 是 Chetan，Chetan 非常棒。

Garry Tan：顶级投资人。

Philip Johnston：对，他很厉害。我觉得他本质上看到的是，一个极其强的技术团队正在做一件如果做成会非常惊人的事。而且他来我们这边看时，花了很多时间做 DD，不只是看项目，也看整个团队的背景。我们在 Redmond 这支团队，说真的，就是世界上最强的工程团队之一，一半来自 SpaceX，一半来自几个 hyperscaler。所以他花了很多时间看团队。我不觉得如果他读到一份报告，说在太空里 cooling 根本不可能，他就会被劝退。我觉得他的判断是，这支团队够强，他们能把它做出来。

Jared Friedman：那你是怎么把这么强的团队组起来的？

Philip Johnston：我的联合创始人是 Adi 和 Ezra。至于 Ezra，是我去过德州 Starbase 之后联系到他的。我当时问他，如果 launch cost 比今天低 10 倍，有没有什么能赚钱的点子？我们最开始就是围绕 space-based solar 想出来的。Adi 则是通过朋友介绍认识的。实际上他自己早就在想类似的事了，甚至以前都已经注册过 stellarcloud.com 这个域名。至于团队建设，我们在招聘上简直是残忍地慢、也残忍地挑。YC 之后我们融资拿到了 1100 万美元，估值是 4000 万，这在 YC 里已经算不错的一轮了。即便如此，我们还是花了整整 6 个月才招到第一个人，而第一个人就是一位极强的太空工程师。我们现在已经融了很多钱，就连我们 3 月份官宣的那轮之后，我们又融了一轮更大的。

Philip Johnston：但即便这样，我们现在也只有 20 个工程师。商业侧只有 1 个人，他之前在 Space Force，做的是 Golden Dome。我们对招聘要求高到让人沮丧，但这就是全部游戏。全部游戏就是，你必须拥有一支极强的工程团队。

Garry Tan：你最初提出这个想法时，很多人都不理解，甚至嗤之以鼻。后来却出现了更强的商业验证，Google、SpaceX 以及整个行业里很多最老牌的参与者都开始接受这个方向，意识到未来很大比例的 data center 很可能会在太空里。你自己看到这种风向变化，看到自己站得这么早，那是什么感觉？

Philip Johnston：很超现实。如果你翻我的 Twitter，过去三年我几乎每天都在屋顶上喊这件事。就是那种 contrarian, but right 的状态。我几乎每天都会发一些东西，解释为什么太空 data center 最终会成立。然后慢慢地，越来越多的人开始有意无意地透露类似信号。比如 Elon 有一次说，太阳系里 99.999% 的能量都来自太阳。我当时立刻转发，然后配文说，我们需要在太空里建 data center。总之，只要找到一个钩子，我就会拿来重复这个观点。

Diana Hu：我觉得这正是所有最好的 hard tech 创始人身上的特质。你们本质上像是活在未来里的人，几乎像先知一样，把未来提前带回给还待在地球上的我们这些普通人，我们一开始确实看不懂。

Philip Johnston：我要回去告诉我那个很虔诚的妈妈，你刚刚说我是先知。

Diana Hu：但这确实很酷。另一个让我觉得很有意思的地方是，如果有人去看你的 LinkedIn，会发现你的履历并不直观地让人觉得，你最后会跑去做太空。你之前的背景更像是软件、物理，然后又转到商业端，但表面看都不像典型的太空履历。

Philip Johnston：对，如果大家不了解我的背景，我职业生涯前五年其实做的是软件侧工程师，再之前本硕读的是数学和物理。后来我去了 McKinsey，更多做商业和产品方向。但我后来确实参与了几个和国家级 space agency 相关的项目，涉及不同卫星任务，那也是我第一次真正注意到 launch cost 正在非常快地下滑。在这家公司之前，我还做过另一家 startup。离开那家公司后，我就想，如果我要再做一次创业，它必须是我真正有激情的东西。而我一生都对太空非常着迷。因为我自己没有太空工程背景，所以我意识到，好，那我就必须把世界上最能打的太空工程师拉进来。说到这点，我其实很感谢 YC。

Philip Johnston：因为我当时几乎是在盲目执行 YC 的建议。我想的就是，在真正想清楚具体做什么之前，第一步先把世界上最厉害的太空工程师聚到团队里。

Jared Friedman：那时候你甚至还不知道自己在太空里到底要做什么。你只知道 launch cost 会大幅下降，太空里会出现一些很酷的新机会，所以你想先找到一些做太空的人，和他们一起想。

Philip Johnston：完全就是这样。

Garry Tan：而且你的方式也不是那种“求求你们帮我实现这个疯狂点子”的姿态，反而几乎是反过来的。你是在说，我来把商业这一侧搞定。

Philip Johnston：对，正是这样。我给 Adi 和 Ezra 的 pitch 基本就是，如果你们有任何一个点子，是建立在 launch cost 比今天低 10 倍的前提下会成立的，那除了造卫星本身，其他一切我都能想办法搞定。

Jared Friedman：那你是怎么找到他们、怎么把他们招进来的？

Philip Johnston：Ezra 和我在英国同一个地方长大。坦白说，我给很多太空工程师都发过消息，也许有 10 个人愿意接电话，最后有 2 个人说了 yes。我觉得这就够了。

Garry Tan：对，你不需要一百个人才开始做，你只需要一两个。

Jared Friedman：Philip，在 batch 期间，我对 Starcloud 的理解一直是，只有当你们的每单位算力成本比地面算力更低时，这公司才真正成立。我现在依然觉得你们最终会做到，但后来我慢慢发现，也许这件事甚至不再是 Starcloud 成功的必要条件。我很好奇你是否也这么看。因为从 batch 之后到现在，我们已经看到 AI data center 在政治上正迅速变得极不受欢迎。我甚至觉得，在一个讲民主政治的国家里，要继续建设 AI data center，很快可能会在事实层面变得几乎不可能。我想知道你怎么看这件事，它会如何影响你们的公司规划。

Philip Johnston：百分之百同意。而且这件事的发展速度比我原先预期的还快。我们已经看到纽约因为一些根本不太建立在科学之上的理由，开始阻拦 data center 建设，感觉更像是一些氛围式判断，而不是硬事实。从监管角度看，把这些东西建到太空里，肯定会容易得多。

Garry Tan：那我们来做一点 myth busting。围绕 data center，尤其是水和电这两个问题，现在外界有很多误解。你脑子里最典型的误解有哪些？

Philip Johnston：先说水。水的问题本质上其实只是 power 的函数。如果你愿意往里面继续砸更多电，你完全可以把 data center 设计成日常运行几乎不消耗水的 closed-loop system。现在各家 data center 公司实际上也都是这么提方案的。几乎不太可能有哪个公司今天还会去提一个每天持续大量消耗水的 data center 方案。

Garry Tan：而且确实有证据表明，closed loop system 可以把耗水量压得非常低。一个很形象的类比是，如果你开一家汉堡店，一个规模相当大的、几百 megawatt 的 data center，用水量大概也就和一家麦当劳差不多。所以这根本不是问题，但不可思议的是，外界居然一直反复拿这个点说事。

Philip Johnston：对，不过它们确实会耗很多电。所以现在很多给 data center 配的新电力项目，实际上是直接配 natural gas generators。这一点确实会引起一部分人的反对。

Garry Tan：还有一个说法是，data center 一建起来就会去跟整个电网抢电，这也不对。实际上大家通常……

Philip Johnston：通常都是为它单独新建一个 power project。

Garry Tan：对，一般就是这样。因为你本来也不可能单纯从现有电网里拿到足够的电。甚至还有一些证据表明，增加 data center 反而会提升整个电网的容量，长期看价格可能还会下降。话虽如此，现在确实像一场完美风暴。我们需要 intelligence，需要 data center，而对美国和整个西方来说，能不能拥有 intelligence 基本已经成了 national security 问题，这是未来一百年最重要的一条 tech tree。如果技术政策把我们重新推回石器时代，甚至让我们在这场竞争里输掉，那 Starcloud 在 bring compute、AI 和 power online 这件事上的位置就会完全不同。

Philip Johnston：对，毫无疑问。那样一来，我们就会非常明确地被归入 national security 这个 bucket。

Garry Tan：那就谢谢你们在为西方而战了。

Philip Johnston：我们尽力而为。

Garry Tan：作为 YC 历史上增长最快的独角兽之一，而且还是一家硬件公司，你最后有没有什么收尾建议，想给那些现在正在看太空、看 hard tech、也想投身其中的人？你一路走到今天，学到的最重要的东西是什么？如果你能回去跟刚开始创业时的自己说句话，你会说什么？

Philip Johnston：我觉得太空领域接下来会出现巨大的机会。我们现在真的还处在这个庞大太空产业的极早期阶段。未来五年将要上线的运力和发射能力，规模大到让人头皮发麻。所以我会非常明确地鼓励更多人进入这个领域。至于建议，YC 那套建议依然成立。首先要解决的是技术人才和 founding team，其他所有事情都排在后面。

Garry Tan：Philip，非常感谢你来做客 The Lightcone。

Philip Johnston：谢谢邀请，很高兴来到这里。
