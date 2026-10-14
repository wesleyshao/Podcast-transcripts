---
访谈时间: 2026-08-10
YouTube发布时间: 2026-08-10T20:30:26Z
访谈时间说明: 使用 YouTube 发布时间；Root Access 官方公开页面全文发布时间为 2026-08-10T20:30:48Z
youtube_video_id: whcfSGN6CAU
嘉宾名字: Peter Steinberger
嘉宾公司名称: OpenClaw
参与嘉宾:
  - 姓名: Peter Steinberger
    公司或机构: OpenClaw
    职务: 创始人
播客名称: Y Combinator
播客url地址: https://www.youtube.com/watch?v=whcfSGN6CAU
字幕来源: Root Access 官方公开页面完整 transcript
全文提及的关键名词:
  - Peter Steinberger
  - OpenClaw
  - Claudius
  - WhatsApp Relay
  - Discord
  - OpenAI
  - Anthropic
  - Claude
  - Codex
  - GPT
  - Opus 3
  - Gemini 2.5
  - OpenAI o3
  - Jensen Huang
  - Sam Altman
  - Mark Zuckerberg
  - Gary
  - Mac Mini
  - MacBook
  - Jump Desktop
  - TypeScript
  - Python
  - OpenClaw Killer
  - Startup School 2026
  - open source
  - open-weight models
  - agent
  - agentic infrastructure
  - session
  - compaction
  - loop
  - graph
  - workflow
  - sub-agent
  - orchestration
  - computer use
  - browser use
  - multimodality
  - voice interface
  - FaceTime
  - sandboxing
  - allow list
  - security boundary
  - remote machine
  - personal brand
  - product-market fit
  - 501(c)(3)
  - O-1 visa
  - configuration options
  - security researchers
  - token cost
  - local models
  - agent harness
---

# Peter Steinberger：＂Fun Is Velocity＂

## Transcript

### 开场：让模型自己运行

Peter Steinberger：六个月前，我还是“未来”，现在各种民调却说我被一个动漫女孩打败了。我几乎每天都会收到类似问题。通常我会忽略，或者给一个适合媒体引用的回答，但今天我想讲一些真实的答案。

这次我准备回答五个问题，大约四十分钟。我知道大家真正想听的是 loops、graphs，以及如何让 Codex 发出“bruh”的反应。相关内容我已经免费放在 Twitter 上。这些经验也许能帮助你们应对接下来可能出现的过山车行情。昨天 Boris 让大家“让模型自己运行”，而我是那个亲眼看到几万人同时让模型运行之后会发生什么的人。

第一个问题是：OpenClaw 为什么看起来只有八个月历史？

按人类时间算，它可能只有八个月，但在 AI 时间里更像四年。我的灵感通常来自“被某件事惹恼”。去年 11 月一个下雨天，我一边调度几个 coding agent，一边觉得饿了。我想去厨房找吃的，同时又希望自己的 tokens 不要闲着，于是我想让 agent 在我离开时继续工作。

当时没有一种真正好用的办法，让我从手机给电脑发一个 prompt，再让某个 agent 检查另一个 agent 到底做得怎么样。于是我回到厨房时，coding agent 因为一个很蠢的问题停了下来，我被惹恼了。我新开了一个 terminal session，把想法杂乱地说给模型听，让模型自己“cook”。

一个小时后，它为我做出了一个 WhatsApp relay，我可以从 Mac 给 WhatsApp 发消息，再从 WhatsApp 收回消息。这个感觉很神奇，但从技术上说不应该这么神奇。过去几个月里，我们其实都在终端中输入指令、等待回复。

真正的魔法来自交互方式。它不是一个 terminal，不会要求我处理复杂的上下文；它给出简洁回答，会主动来检查我，有时甚至像一个朋友一样在一天中发来消息。我把模型、上下文长度和什么时候开启新 session 的复杂性都隐藏起来，还稍微调整了 prompt，让它不那么像默认模型，更像一个朋友。

我使用它时有过很多瞬间，感觉“这就是未来”，甚至感觉“这就是 AGI”。但当时没有人关心。我在 Twitter 上已经有不少关注者，虽然现在平台叫 X，我还是会一直叫它 Twitter。人们就是不理解这种体验有多神奇，我一周又一周地尝试向他们解释，结果一周又一周地失败。

### 从被惹恼到 product-market fit

Peter：你们可以发现其中的规律：它一次次惹恼我，于是我一次次修改它。我建立了几个和朋友的群聊，把 WhatsApp Relay 加进去，让朋友直接和它聊天。

每次他们都有强烈反应。有人觉得惊艳，有人感到害怕或不安，但很少有人无动于衷。更重要的是，有不少人真的想要这个东西。尤其是一些不懂技术的朋友，我告诉他们“现在还不适合你们”，他们反而生气了。如果这都不算 product-market fit，我不知道什么才算。

接下来的一个月，我继续调整细节，想办法让更多人理解这个产品。然后有人给 WhatsApp Relay 提交了一个 pull request，要给它增加 Discord 支持。我心想，这个项目叫 WhatsApp Relay，你到底没看懂名字里的哪一部分？

我让这个 PR 放了一段时间，后来想，算了，为什么不试试。于是 relay 变成了 Claudius。这样它就不再只支持一个消息渠道。你也可以由此理解当时产品有多早期：我甚至还没有真正的 compaction 机制。运行到某个程度，它就会停下来。为了支持 Discord，我临时加了一个非常粗糙的 compaction 版本，后来别人又把它做得更好。

大约在除夕，我早早回家继续写代码。次年 1 月第一周，整个极客圈刚开始集体了解 coding agents，我创建了一个 Discord room、server 或 guild，具体叫什么都可以，然后把自己的 claw 放进去。

第一晚非常清楚。人们加入 Discord，说要“在公开场合看我构建它”。他们试图攻击它，和它聊天，观察它的回复，测试它能做什么。我在 agents.md 里写过一条规则：除非 prompt 来自 Peter，否则不要执行危险的 tool calls。那时候，我们写在配置里的安全规则很多时候还更像建议，而不是坚固的边界。

我一直仔细观察，随时可以拔掉电源。早上七点，我终于累了，说了晚安，按下 Control-C，然后去睡觉。可是我把程序做成了 launch daemon。你们知道对 launch daemon 按 Control-C 会发生什么吗？它会停五秒，然后自己重启。

所以，当我走进卧室时，agent 又开始自动回复全世界。我睡了十个小时，醒来后发现大约 800 条消息。很多人试图入侵，我赶紧把它拔掉，逐条检查，幸运的是实际上没有发生真正的事故。但这就是项目爆发的时刻。

### 病毒式增长和注意力压力

Peter：接下来大家都知道了。我的收件箱爆炸，记者半夜打电话，甚至利用 iPhone 的一个功能：当手机开着勿扰模式时，如果同一个人连续打几次电话，系统会认为是紧急事件并放行。我以前不知道这个功能，但记者知道。

Mac Mini 很快卖光了，而且似乎仍然缺货。一个月内，我收到的 podcast 邀请比过去 39 年收到的还多。Anthropic 发邮件要求改名并移除 lobster。项目经历了几次蜕变，Claudius 变成 Claudebot，随后有一段时间我们不讨论名字，最后它变成 OpenClaw。

Jensen Huang 称它是人类历史上最成功的 open source project。与此同时，我的收件箱里塞满记者、安全人员、好奇的人，甚至还有其他 agent。那些数字至今仍然不真实：八个月内，超过 18,000 个不同的人提交过 issue 或 pull request，总数超过 111,000；将近 3,000 人在代码仓库里留下了 commits。

有些人说我偷了他们的想法，给我发来链接，证明他们几年前做过类似东西。但那些东西我从来没有见过。有人叫我 AI Jesus，也有人叫我 antichrist。

我甚至开始收集各种“讣告”，几周就会出现一篇，最近一篇还是昨天发布的。这里最重要的教训是：小心你许下的愿望。我没有准备好承受这么多关注，甚至差一点就把整个项目删掉。

我不再回复朋友，也不想看手机，因为屏幕上只有不断流入的消息。有人泄露了我的电话号码和很多私人信息，把我描述成 humanity 的敌人，而我只是想做一个有趣的东西。

### 要不要出售，以及名字无法被 fork

Peter：第二个问题是，你是不是卖掉了自己？

这不是我第一次经历这种选择。我二十多岁和三十多岁时一直在做 B2B software company。我甚至像个原始人一样手写了一套 PDF framework，靠 bootstrapping 把公司做到接近 80 人。我没有理会竞争者，公司最后成了大多数企业会购买的产品。

后来我把事情交给联合创始人，出售了自己的股份，然后非常彻底地 burnout。Retirement 听起来很美好。我花了将近三年漫无目的地生活，补上过去错过的聚会和生活经历。有几个月我甚至不开电脑，只拿手机像普通人一样随便浏览互联网。

我一直知道，只要给自己足够时间，冲动就会回来。我原以为回来的是写代码，因为我一直喜欢 programming。但花了一年我才明白，真正吸引我的是 building，编程只是达到目的的手段。

找回火花八个月后，我的收件箱里充满 VC，希望我接受他们的钱。我当时并不知道自己要不要这样做。后来几家大型 labs 找上门，我突然和 Mark、Sam 以及其他人通电话，这条路径看起来有意思得多，也非常不真实，甚至让我有 imposter syndrome。

你能构建出来的任何产品都可能被 fork 或 clone，但你的名字不能被 fork。personal brand 比任何一个具体产品都更重要。应该在真正需要它之前就开始经营个人品牌。

我知道这个游戏怎么运作，也知道接受这件事相当于把自己的 soul.md 卖掉。决定并不容易，但 burnout 之后我学到的一件事是相信直觉。我的直觉告诉我，我最喜欢 OpenAI。

### 安全报告、OpenClaw 的防守和依赖风险

Peter：第三个问题是，Hermes 赢了吗？

简短回答是，他们在最痛的地方打败了我们。我们仍然在那里，但这两件事都和我的决定有关。发布后的几个月里，我们被大量 security reports 压得喘不过气。某种程度上，我们提前体验了很多 open source 项目后来都会遇到的情况。

很多报告其实只针对很极端的 edge case，但压力仍然存在。媒体说我们有 20% 的 skills 是恶意的。我们后来专门写了论文，实际数字更接近 0.3%，因为我们扫描了全部 67,000 个 skills。论文发布了，但 correction 永远不会像 scare 一样传播得远。

世界发现了 OpenClaw。我知道安装时有一个很大的安全免责声明，甚至比我能放进演示文稿的内容还长，但我也知道许多用户不会读文档，所以我把注意力放在加固代码上。

我们增加了层层 security：sandboxing、allow lists、内置权限的 vet protocol。某些文件操作甚至从 TypeScript 转到调用 Python，因为 TypeScript 缺少一些足够可靠的 primitive。我们希望 agent 留在 workspace 内，不跟随 symlink，并且让配置文件以原子方式写入。

多数用户并不真正关心这些细节。他们喜欢“看起来安全”，但从实际使用角度看，加固改变了他们依赖的行为，让程序变慢，也让更新变得更困难。

与此同时，我的时间被 open source、媒体、为成立 501(c)(3) 美国 nonprofit 而和律师长时间沟通、处理 O-1 visa，以及 OpenAI 自己复杂而有吸引力的工作分散。我的注意力变得非常碎片化。

我找来了一些帮助，也建立了非常优秀的 maintainer community。可是每个人都在免费工作，我很难告诉他们不能做什么。同时，features 很有趣，新增功能似乎只需要一个 prompt。真正的成本总是在之后。

因为不想破坏用户的设置，每个新功能我们都增加了 configuration option。到最高峰，算上各种排列组合，大约有 9500 个 configuration options。你可以写再多测试，也不可能覆盖所有组合，软件必然会偶尔被改坏。

软件有用户之后，演化难度会无限增加。与此同时，其他公司拿着 VC money 快速前进。那个动漫女孩公司尤其擅长营销，它们进入 Twitter 的各种讨论，故事简单、营销激进，还提供一行命令迁移用户的 claws。

真正伤害 OpenClaw 的最大因素是 Anthropic，不是改名字这件事。改名虽然有压力，但我能理解，他们处理得也很礼貌。真正的问题是我过度依赖了他们的 model。

OpenClaw 最初用 Codex 和 GPT 构建，但 harness 很长时间对 Opus 优化得最好。Anthropic 提前约 24 小时通知，将停止向所有人提供某种 subscription，留给我们改变路线的时间太少。我们支持 open-weight models，也做了很多工作，但那时它们还不够好；早期 OpenAI models 又缺少 character。

所以请记住：依赖方的 business model 就是你的 business model。现在这些问题已经修复，相关模型更强，open-weight models 也真正可用，我从 harness engineering 学到了很多。但很多用户已经转向别处。

下载曲线显示了这种反差。5 月每周下载量一度跌到约 835,000，6 月被宣布“死亡”之后，最高又达到每周 470 万。两件事可以同时为真。Hype 像天气，你可以看见风暴正在靠近，但你无法控制它。我的情况就是遇到了一场风暴。

### 从责任感重新找回乐趣

Peter：第四个问题，OpenClaw 现在还好玩吗？

大约二月，事情不再有趣。我开始觉得它是一项责任。我原本不想再建立一家公司，却突然有了两份工作，或者说一份工作加一个使命。

最糟糕的是，我停止使用自己的产品。我不再做一个每天自己喜欢用的东西，而是开始做一个“适合所有人”的东西。产品从我每天使用的工具，变成了我看到并感觉像工作的东西。

我尝试想象所谓“所有人”到底是谁。有人在做 grocery agent，有人尝试 social engineer 我的 bot。随着大家不断加功能和我不断做组织工作，我变成了负责修 bug、修 security issue、提供支持和建设基础设施的人。

因为外界传言 OpenClaw 属于 OpenAI，我也不想从 OpenAI 获得太多帮助。它们给了我 token，我确实大量使用了，但我同时被拉进其他项目。还有很多人试图找我聊天，我只能轻易地把他们 block。

事后看，我本可以做得不同。我可以更早寻求帮助，把责任移出自己的工作清单。但我深陷所有细节，没有时间做战略思考。

幸运的是，我遇到了很多优秀的人，事情逐渐对齐。我解决了签证问题，成立了 nonprofit，找到愿意捐助的公司，也找到真正相信 open source 的人开始和我一起工作。

我还要特别感谢 Nvidia。他们很早就来问我需要什么，然后派人接手了大量 security work。大约五月、接近我生日时，我开始感觉事情重新变好，构建产品的快乐回来了。

媒体每隔一周就会选出一个 OpenClaw killer，我数过大概有 20 个。甚至有一个项目真的叫 OpenClaw Killer，它其实是一个 uninstaller，但完全没必要，因为我们本来就有 uninstaller。

这些 killer 故事都没有抓住 OpenClaw 真正的核心：open source。我的灵感一直来自被软件惹恼。现在，如果一个软件不允许我直接给 agent 发 prompt 去修改，我又会被它惹恼。这个部分的乐趣正在回来。

和一个真正享受构建的人竞争非常困难。Fun is velocity。那些我享受构建的星期，产品会明显变好；那些我不享受的星期，我们只是在增加 configuration options。

### OpenClaw 的下一步和开放模型的意义

Peter：第五个问题是，接下来做什么？

首先，我对现在的基础设施很满意。我们的使命是让人更接近 AI。AI 变化太快，很多人觉得它模糊又可怕。OpenClaw 做成的一件令我骄傲的事，是把 AI 从一个抽象、吓人的东西变成有趣、古怪的东西。lobsters 以及其他玩笑，都是这个过程的一部分。

我们会继续建设 open source software ecosystem，举办让人相聚的活动，做教育。现在有 10 个人在 payroll 上，还在招聘，包括 CEO。

第二，我似乎把 Claw 变成了一个名词。Karpathy 去掉了 Open，Satya 在 Microsoft keynote 里说 enterprise-grade Claw，已经有 33,000 个名字里含 Claw 的 repository。如果我们处在 simulation 里，那也是一个非常古怪、还没有被关闭的 simulation。我很喜欢未来的这个部分。

第三，我们还没有一个永远在线、永远同步的 agent，仍然有很多事情可以做。AI 的技术和模型变化速度，快于围绕它们建设的软件。对于所有构建者来说，这既是问题也是机会。

我早期的愿景是，不应该让用户操心 session 或 compaction。现在模型和技术终于接近能够实现这个愿景。我们也会从纯文本界面走向 voice 和 multimodality。就在昨天，我们成功做了一个 hack，让 Claw 可以 FaceTime 用户。

这就是 OpenClaw 存在的原因。每个 lab 都会卖给你一个 agent，OpenClaw 是另一个选择。它是 open source，可以在任何地方运行，支持任何模型。如果使用 local models，数据可以不离开设备。你的 agent、你的机器和你的生活都属于你。这不是我的 thesis，是 Gary 的 thesis，我们只是先把它做出来。

我们也重新用 OpenClaw 构建 OpenClaw，但这次加入了团队 server。每个人可以看到彼此的 session，有一个 Claw 知道团队其他人在做什么，并且能接管工作编排。

我们会慢慢离开这样一个奇怪的过渡时期：人们必须在 terminal 里工作，电脑一直开着，因为 agent 还在运行。大家只记住三件事就够了。

第一，不要停止享受乐趣。乐趣是获得最好想法的终极驱动力。

第二，相信直觉，修复那些惹恼你的事情。它可能变成下一个大产品。

第三，保持专注。

另一个 podcast 不会让你赢。要活在未来，构建缺失的东西。当别人写你的讣告时，继续 shipping，这会让他们困惑。

## Q&A

### 从 agent、loop 到 graph，Peter 现在如何构建

提问：最初有 agents，后来有 loops，再后来有 graphs。你现在如何构建？

Peter：其实一直都是 sessions。早期你必须清理 session，确保 instructions 前后一致。现在我的 sessions 更像围绕某个 topic 组织。

清空 session 有时反而是劣势，因为里面有很多帮助 agent 的信息。真正的变化是，我要求 agent 为我做更多主动工作。

当我把注意力转向一件事时，我不想先阅读 issue。我想看到已经 review 和 test 完成的 PR。功能最后是不是我喜欢的另说，但我不想被迫把注意力拆开。

如果团队成员来告诉我一个功能想法，我反而会生气。现在功能构建太容易了，他完全可以先和 agent 讨论，再自己做出来，截取 screenshots，让我直接试用。好的功能可以马上迭代，而更多时候，团队会在来找我之前自己发现它为什么不好。

### Graph 不是魔法，而是 automation 的新名字

提问：graphs 之后是什么？OpenClaw 下一步做什么？

Peter：我有时周日发一个看似 shitpost 的内容，Twitter 就爆炸了，但它有时并不是 shitpost。工程师很久以来就在写 automation，让生活变得容易。

无论叫 loop、graph 还是 workflow，本质都是一样的：接收一个 trigger 和 input，为你执行某件事，中间可能有一个 decision。这样就得到一个 graph。它没有那么神秘，只是我们长期以来 automation 故事的更好表达。

### 快速构建如何保持可靠和可扩展

提问：在 build fast、ship fast 的环境里，如何确保产品可靠并且可扩展？

Peter：这正是我曾经搞砸的地方，因为我不够专注，而且当时模型还不擅长测试。现在模型进步很多。我们不只有能记忆的 sessions，orchestration 也已经被训练进模型，它们知道如何使用 sub-agents。

我们还拥有 computer use 和 browser use。把这些能力放在一起，就像一个很好的 Q&A 环境。昨天我启动 Codex，使用 12 个 sub-agents，让它们理解项目并拆解成 features。每个 sub-agent 负责 stress test 或 code review，再把结果告诉其他 session，指出下一步测试重点。

我们还没有完全自动化一切。你仍然需要手动 click-through，确认产品用起来是什么感觉。但对大量典型 bug 来说，通过 prompt 已经可以走得很远。

### 速度与 code review

提问：你早期为了速度做过什么决定，今天仍然受它影响？

Peter：我很早就决定不阅读全部代码。我把 code review 看作 risk management。有时你碰到一个可怕的系统，就需要读得更仔细；有时你只是在构建 UI，如果它看起来正确，我并不太在意内部具体怎么实现。

你也要逐渐形成对工作量的感觉。如果一个小改动只是改变拖拽行为，却花了三个小时，我就知道出问题了，会进一步检查。除此之外，code review 也包括观察改动规模、判断风险，然后相信自己的直觉。

### 从 prototype 到前十个用户

提问：AI 工具让人一个周末就能做出产品，但真正难的是获得用户。今天如何从 prototype 获得前十个真实用户？

Peter：第一位用户应该是你自己。我自己的第二到第二十位用户是朋友。你肯定也有一些愿意测试东西的人，但你必须先成为自己的用户。如果你对自己做的东西都不兴奋，它可能就没有意义。

现在最贵的货币是 eyeballs，因为构建产品已经太快。技术、软件甚至人员都不一定是最难的问题，让真实的人看到、尝试并持续使用，才是新的瓶颈。

### 解决惹恼你的问题，还是做别人想要的功能

提问：如何平衡解决自己讨厌的问题和构建你认为别人想要的功能？

Peter：这两个事情经常是一回事。如果某个功能不存在，且它没有按照我希望的方式工作，我就会被惹恼。但我还没有完全解决这个问题。

软件总有奇怪的 edge case，我可以花几个月一直修问题。但如果只做这个，我又会失去继续工作的兴趣，所以必须保持健康的混合：既修复让自己恼火的事情，也做能够让产品向前走的建设。

### 对安全研究者的反思

提问：如果可以回到过去，你会改变 OpenClaw 的哪一件事？

Peter：我会少为 security researchers 感到压力。他们很擅长让你感觉很糟。他们发报告、邮件、打电话，用各种方式吸引你的注意力，但不一定真正帮助产品。

很多时候，他们只是为了获得 clout，证明“我们发现了一个问题”。更糟糕的是，有些报告是他们的 agent 生成的，甚至没有真正测试。我应该更明确地解释哪些是我们保证的安全边界，哪些不属于我们的边界、不会修复。

那是我第一次接触这个世界，我不知道应该如何处理，因此浪费了几个月，也多了几根白头发。

### agentic infrastructure 最大瓶颈是 compute management

提问：今天 agentic infrastructure 最大的瓶颈是什么？是可靠性、工具、memory 还是 evals？

Peter：我会说是 managing compute。比如我在自己的机器上跑一个测试，TS Go 可能开 16 个 threads，把整台机器卡住。如果同时有 10 个 sessions，其中两个可能 timeout，只能再跑一遍。现在没有一个真正好的系统可以管理这些负载。

如果只是 web 工作，建立 cloud session 很容易。但如果任务需要 Mac OS，99% 的工具都会失效。如果它还需要电脑上的其他资源，问题更大。我们还没有很好的系统，可以让任务稳定地从一台机器迁移到另一台机器。

目前我只能 screen share 到几台电脑，把负载分散开。我不应该需要这样做。也还没有可靠的方法，让一整支 computer fleet 自动运行。

### 开源项目的方向与 vision.md

提问：怎样让 open source project 保持鲜明方向，而不是不断合并增加随机功能的 N+1 个 PR？如何向 community 传达方向？你是否拒绝过一个受欢迎但会让项目偏离路线的 PR？

Peter：我应该更经常说“不”。现在做新的 open source project 时，我会写一个 vision.md，解释它当前是什么，以及我希望它变成什么。当然，这个文件不可能是完美科学，可能会错，但它能帮助项目维持方向。

诱惑总是存在：某个功能看起来很酷，为什么不加进去？但合并一个功能意味着接收一大堆代码。提交者可能并不完全理解，我也可能没有完全理解，可一旦合并，它就变成我负责的东西。开发者常常低估了这个长期责任。

### 永久运行的 proactive claws

提问：什么时候能有一直运行、能够主动工作的 claws？

Peter：这不完全是技术问题，而是 token 问题。今天我们可以做到，但你的 subscription 很快就会被用完，不是所有人都愿意消耗那么多 tokens。

另一个难点是设计一个不浪费 tokens 的系统。我的早期 heartbeat 太静态，不够 proactive。如果 session 很大，一个小时后又对所有内容运行 heartbeat checkup，缓存过期后可能需要把 600,000 tokens 再发回服务器，为很多无用工作支付大量费用。

因此需要更好地管理上下文、缓存、触发条件和检查频率。优化空间很大，也非常难。

### 个人机器、远程电脑和鼠标争夺

提问：你的个人 setup 是什么？claws 运行在哪里，使用什么 model 和 harness？你还读代码吗？

Peter：我使用 MacBook，但通常通过 Jump Desktop 远程进入 studio，在那台始终开机的电脑上运行任务。这样可以快速运行任何东西，不消耗笔记本电量，也可以合上电脑让任务继续。

我还有几台 remote machines，有时会连接进去。因为我经常做 Mac 软件，agent 喜欢接管屏幕并点击。如果给 agent 一台自己的机器，它就不会打扰你，否则你会和 agent 争夺鼠标光标。

至于是否还读代码，还是 risk management。如果我自己做 open source，风险标准和我在 OpenAI 做 software 时不同。后者仍然会对全部代码进行更严格的阅读。

### 下一次创业

提问：Peter，你会如何处理下一个 startup idea？

Peter：最重要的是构建你真正想使用的东西，否则它不会足够好。其次，希望你在个人品牌和 visibility 上提前投入。现在噪音太多，最难的问题不再是 technology、software，甚至也不一定是 people，而是得到 eyeballs。

我可能会再次选择 hard and boring 的类别。这样的类别更容易找到真正感谢你解决问题的人。如果选择一个有趣但竞争激烈的领域，就算技术很难，也会非常困难，因为现在人们可以直接 prompt 出很多东西。

### 想要的产品

提问：你希望别人构建什么产品？

Peter：Linux 的 test box 很容易找到，但一个真正好用的 Mac test box 难得不合理。Windows 的解决方案也很令人恼火。我还没有找到一家 provider，能快速、便宜、稳定地提供这些环境。

我不确定这是不是适合创业的方向，因为 dev tools 天生很难，但我确实希望拥有这样的服务。

谢谢大家。

## 核心观点

1. OpenClaw 起源于 Peter Steinberger 自己被惹恼的具体需求：希望从手机向电脑上的 coding agent 发消息，并让 agent 主动检查工作。产品市场匹配来自非技术朋友产生强烈兴趣，而不是来自创始人单方面的技术兴奋。
2. 爆发式开源项目的主要风险不是第一次发布，而是病毒式增长后的安全、维护、配置复杂度、社区治理和创始人注意力分配。OpenClaw 高峰期约有 9500 个配置组合，功能增加的成本会在发布之后持续累积。
3. 依赖方的 business model 就是自己的 business model。过度围绕单一模型优化，会在模型供应商改变 subscription 或产品策略时暴露；支持 open-weight models、多个模型和可迁移 harness 是降低风险的基础。
4. 开发速度提升后，最稀缺的资源从构建能力转向 eyeballs、用户注意力和可靠的 compute orchestration。产品的第一位用户必须是创始人，前二到二十位用户可以来自真实朋友和早期社群。
5. loop、graph 和 workflow 在底层都是带有触发器、输入、动作和决策的 automation。未来的 agent 产品重点不只是生成文本，而是跨 session、机器、浏览器、语音和多模态环境持续执行工作。
6. OpenClaw 的开放模型路线强调 agent、设备和数据的控制权。local models 可以让数据不离开设备，团队 server 则可能把个人 agent 推进到协同编排。
7. 创始人的三个建议是：不要停止享受构建，相信直觉并修复真正惹恼你的问题，保持专注。对于创业者，个人品牌和可获得的用户注意力已经和技术本身同样重要。

## 投资边界

本期主要讨论 OpenClaw 的产品构建、开源治理、agentic infrastructure 和创业经验，没有明确的上市公司级交易逻辑，也没有形成可验证的单一证券观点。不创建投资机会文件。
