---
访谈时间: 2026-08-30
访谈时间说明: "使用YouTube发布时间；字幕为完整原始字幕。"
嘉宾名字: Tara Seshan
嘉宾公司名称: OpenAI
参与嘉宾:
  - 姓名: Lenny Rachitsky
    公司或机构: Lenny's Podcast
    职务: 主持人
  - 姓名: Tara Seshan
    公司或机构: OpenAI
    职务: Codex与ChatGPT Work产品负责人
播客名称: Lenny's Podcast
播客url地址: https://www.youtube.com/watch?v=zMvBMfj4cSQ
youtube_video_id: zMvBMfj4cSQ
YouTube发布时间: 2026-08-30T12:30:33Z
字幕来源: YouTube en-orig完整字幕，经上下文转写为简体中文
文字稿来源: "/Users/wesley/.codex/automations/youtube/caption_cache/zMvBMfj4cSQ.en-orig.source.txt"
原始语言: English
全文提及的关键名词:
  - OpenAI
  - ChatGPT
  - ChatGPT Work
  - Codex
  - persistent AI coworker
  - AI agents
  - product management
  - product-market fit
  - Stripe
  - Watershed
  - WorkOS
  - Mercury
  - Sites
  - Visualize
  - writing as thinking
  - writing as reporting
  - Sutter Hill Ventures
  - Mike Speiser
  - Reticle
  - Teal Fellowship
  - Ari Weinstein
  - Sky
  - Dylan Field
  - Figma
  - Anthropic
  - Cursor
  - Sierra
  - Clay
companies:
  - OpenAI
  - Stripe
  - Anthropic
  - Cursor
  - Figma
industries: []
technologies:
  - Agent
  - 编程助手
  - LLM
keywords: []
tags:
  - OpenAI
  - Stripe
  - Anthropic
  - Cursor
  - Figma
  - Agent
  - 编程助手
  - LLM
---

# AI’s third era： the rise of persistent AI coworkers ｜ Tara Seshan (OpenAI’s product lead)

## Transcript

如果把 AI 产品的第一时代理解为 chat，把第二时代理解为和 agents 一起工作，那么即将到来的第三时代，可能是和一个能够与你协作完成事情的 persistent coworker 一起工作。

这里有一个“能力悬置”的概念：AI 能做什么，和我们实际上让它做什么之间存在巨大差距。

未来到底会出现什么，非常难判断。如果你按照模型现在的能力来建设产品，你会失败；如果你按照你认为模型一年后的能力来建设产品，你也会失败。这两种结果同样错误。唯一可行的建设时间尺度是两到三个月。

如果你必须调整自己的 product manager 工作方式，最重要的变化是什么？相比 academic 或 theoretical，prolific 和 empirical 重要得多。与其写一篇很长的 reasoning doc，不如尽快做出能够和用户测试的东西。

AI 不仅让我们能够更加有野心，几乎也要求我们更加有野心。但这对很多人来说并不自然。提升别人的 ambition，提醒他们这里有哪些可能性，会成为 product management role 的重要组成部分。

我很好奇，在 OpenAI 工作的真实体验中，什么最让你意外？

Tara：我加入 OpenAI 时，以为公司里有一个关于 OpenAI secret strategy 的 treasure trove，结果发现 OpenAI 是 open 的。

Lenny：今天的嘉宾是 Tara Seshan。Tara 在 OpenAI 负责 Codex 和 ChatGPT Work 的产品。我认为，ChatGPT Work 是知识工作者中增长最快、也可能是最重要的 AI 产品。

Tara 和上一期来过节目的 Andrew Ambrosino 一起工作，Andrew 是她的 engineering manager。在 OpenAI 之前，Tara 在 Stripe 工作了六年多，是 Stripe 最早的五名 product managers 之一。她在很多年里都被评为整个 Stripe 组织最优秀的三名员工之一。

她还曾在 Watershed 负责产品，是一名 founder，也曾获得 Teal Fellowship。最重要的是，Tara 是 Lenny's Newsletter Fellows 的三位首届成员之一。这个项目是我几年前做的，用来发现和突出最优秀的新生代 product leaders。

看到 Tara 如今承担这个重要而有影响力的职位，我非常兴奋。在开始之前，别忘了访问 lennisproduct.com。Lenny's Newsletter subscribers 可以免费获得一年世界上最热门、设计最精美的 AI products。

Tara，谢谢你来到节目。

Tara：谢谢你，Lenny。我很高兴来这里，见到你真好。

Lenny：我更高兴。你加入 OpenAI 大约一年了。在大多数地方，一年是很短的时间；但按 AI 的时间尺度，一年几乎是一辈子。

Tara：是的。

Lenny：你加入 OpenAI 时，应该已经大概知道在 frontier lab 工作是什么样子。我想知道，真正开始在 OpenAI 工作后，什么最让你意外？好的和不好的都可以说。

Tara：很多东西对我来说其实很熟悉，因为我以前也在高增长、高人才密度、高强度、处于 hyperscaling mode 的公司工作过。同事非常优秀，紧迫感非常强，这些都不让我特别意外。

真正最意外的地方是，我过去工作过的所有公司，都是 founder-led 的。OpenAI 实际上是 founderless。这里的意思是，公司内部几乎每个人，尤其是在自己负责的领域，都在某种程度上像一个 founder。

和我以前工作过的地方相比，OpenAI 的 top-down direction 极其有限。刚加入时，这既让我很开心，也让我感觉很熟悉，因为我自己经历过 founding journey。我可以继续像这个产品领域或这个团队的 founder 一样工作，自己承担责任。

我和市场之间的距离非常、非常薄。在大公司里，你有时会被隔离在用户需求和市场要求之外，但在 OpenAI 完全不会。你会像 founder 一样，完成一切让自己的产品取得 product-market fit 所需要完成的事情。

但更出乎意料的一面是，我加入公司时以为会发现一座 OpenAI secret strategy 的宝库，就像过去进入一家公司时会看到“这就是我们的 payments bible，这就是我们思考 payments 和 operations 的方法”。结果 OpenAI 是 open 的。【笑】

关于世界应该是什么样、产品应该怎样构建、模型应该怎样运作，各种内部想法很快就会成为公开产品的一部分，或成为公开叙事的一部分。这对我来说既是积极的意外，也确实改变了我的工作模式。

Lenny：所以并不存在一个神秘房间，里面运行着 AGI，墙上挂着解决一切问题的 master plan？

Tara：至少我肯定不在那个房间里。但真正鼓舞我的是，OpenAI 做的很多事情会立刻变成用户能够在产品中触摸和感受到的东西。这个循环比我见过的任何地方都快。

【广告：WorkOS】

本期节目由本季 presenting sponsor WorkOS 带来。OpenAI、Anthropic、Cursor、Replit、Sierra、Clay 以及数百家成功公司有什么共同点？它们都由 WorkOS 提供支持。

如果你在为 enterprise 构建产品，就会感受到集成 single sign-on、SCIM、RBAC、audit logs 以及大型企业要求的其他功能有多痛苦。WorkOS 把这些 deal blockers 变成 drop-in APIs，提供专门为 B2B SaaS 打造的现代 developer platform。

我投资的 startup 只要开始向上拓展 enterprise market，最后几乎都会和 WorkOS 合作，因为它是最好的方案。无论你是想赢得第一家 enterprise customer 的 seed-stage startup，还是要在全球扩张的 unicorn，WorkOS 都是成为 enterprise-ready、解除增长阻塞的最快路径。

它基本上就是 enterprise features 的 Stripe。访问 workos.com，或者直接进入它们的 Slack，那里有真正的 engineers 等待回答问题。WorkOS 有好用的 APIs、完整的 docs 和流畅的 developer experience，帮助你更快构建产品。

Lenny：你在很多不同地方做过 PM，也长期担任 PM leader。在这个新世界里，PM 会失去什么？

Tara：当一个市场更稳定、变化更慢时，你有机会做 grand-strategy 式的工作，因为市场更可预测，或者至少你可以理解所有组成部分。

比如 payments 在某种程度上是动态市场，但它也是成熟市场。你可以说：“如果我做这个 bet，竞争对手可能做另一个 bet。”你也可以从 first principles 出发，严谨地推演下一步可能发生的所有事情。

这个市场本身也要求你这样做。赢家必须比其他人更严谨地思考。如果你不够严谨，最终会被看作 careless，因为当时做出的许多决策本来是可以预测的。

但 AI 市场太难判断未来会出现什么。它非常 emergent，变化非常快，也极其动态。最重要的是，你必须紧密地连接 research。

所以，prolific 和 empirical 实际上比 academic 或 theoretical 更重要。我过去工作过的许多公司，都非常 academic、非常 theoretical。来到这里后，我从“写一份很长的 reasoning doc，像写博士论文一样，描述未来一段时间应该采取的计划”，切换成“怎样尽快做出一个可以让用户试用和测试的东西”。

刚开始，这种从 theoretical 到 empirical 的切换非常不适应。我会想：“我是不是没有尽到 due diligence？是不是没有足够周密地思考？难道不应该把所有事情都非常严谨地推演一遍？”

但你必须先尝试，然后尽可能多地学习。这意味着你的思考必须非常明确地聚焦在 core hypothesis 上。定义 hypothesis 是最重要的事情。

借用 Shashir Rahul 的说法，你必须找到那个“最关键的问题”：到底要测试什么最重要的事情？你构造出的其他 grand strategy 都不相关。

Lenny：这很有意思。PM role 有很多东西在变化，但似乎有一件事不仅没有变化，反而变得更重要。请再谈谈人们应该聚焦什么。

Tara：PM role 周围有很多 trappings，比如按时管理 execution、撰写各种 docs 和 presentations。但核心一直是：关于你的产品，你必须提出的最重要问题是什么？决定产品成功或失败的因素是什么？怎样测试它？怎样观察结果？怎样把结果反馈到循环里，继续完善 hypothesis，再次运行测试？

这一直是 PM 的真正工作。

它当然包括理解 users、理解 market、理解你正在建设的 technology，再把三者结合起来，形成尽可能 sharp 的 hypothesis，并让测试尽可能快、尽可能有效。

这件事不但没有变化，反而成为公司里最重要的事情。EMs、engineers、data scientists、designers 都在以这种方式思考。每个人都开始把精力放到非常重要的 problem definition 和 testing loop 上：我们到底在做什么？怎样知道它是否有效？

从 PM 的角度看，这很好，因为 PM 一直以来就应该把这件事做好。它始终是工作的核心，而其他很多工作 trappings 已经逐渐消失。

Lenny：你提到 loop。最近几周，Twitter 上很流行谈 loops，它似乎也继续成为知识工作的主题。我的理解是，loop 大概是这样：AI 得到成功标准，然后自己去构建和解决问题，直到达到目标。

你怎么看 loops 从 software engineering 扩展到 product management，再扩展到所有 knowledge work？这会成为未来吗？

Tara：我确实认为，未来的工作会越来越像 steering，而不是 rowing。

你会和 agents 一起工作，它们承担大量 rowing；而你的角色越来越像驾驶船只，决定要把船指向哪个方向，并持续把它指向正确方向。

这种 steering 可能会越来越高层。过去的 steering 可能是我写下一行 code，然后按 Tab；现在可能是我指挥一个更完整的任务，再往上可能是目标层面，甚至是更高的抽象层面。

但归根结底，仍然需要一个人决定：我们要朝哪个方向前进？获得反馈和更多数据后，下一步应该把它带到哪里？

Steering 的一部分当然由 data 告诉你，但很大一部分是做出有立场的判断。我们有时低估 intuition 的力量，也低估“我希望未来变成什么样”的积极确定性。

你可能会说：“我希望产品朝这个方向发展。”并不是因为相反方向不合理，而是因为你希望世界变成你推动的那个样子。我认为，至少现在，这仍然需要由人来提出 opinion。

所以 loops 很好。让 agents 进入越来越大的 loops，让它们为你承担越来越多 rowing 的 tactical work，这很棒。但现在你仍然需要 steering。

未来的工作也可能是你和其他人一起 steering 一组 agents。把 teammates 带进你和 agent 的互动中，让 agent rowing、你 steering，这同样非常有价值。

Lenny：这是描述方式很有意思。这里有两个想法。第一，如果所有人都能使用同样的工具，真正区分彼此的就是人本身，否则大家会构建同样的东西。

这让我想到 fashion。功能性的衣服人人都可以穿，能够完成基本任务，但你穿什么，也是在表达自己的 individuality，向世界展示你想表达的东西。某件衣服之所以有表达力，往往是因为它和别人穿的不同，或者代表了某个群体。

我们构建的产品也有类似的 opinionated 和 artistic 属性。Patrick Collison，或者也许是 John Collison，有一句很好的话：software 不像 real estate。你不能只是投入 money，然后得到同等的 value。Software 更像 filmmaking。你可以在一部电影里投入很多 money，但这不保证电影会成功或优秀。

其中有一种 authorship、opinion 和 artistry。它要求你或团队对产品有有趣的表达。

Marty Cagan 经常强调，当你有一个 product 或 feature idea 时，最终形成的东西很少就是最初的 idea。你要经历一个过程，弄清楚它真正应该是什么。

你说的似乎也是这个意思：作为人，你需要经历这个过程，理解它到底是什么、用户真正想要什么，而不是说“我已经一开始就完全想清楚了，直接去构建吧”。

Tara：当然。这个 loop 正在越来越快。你形成 intuitions 的能力、获取形成 intuitions 所需信息的能力，以及把 intuitions 和 people、agents 一起付诸行动的能力，都是关键。

Lenny：你认为接下来三到六个月，knowledge workers 的工作方式会发生什么变化？你不仅可以使用最先进的工具，还在世界上最 AI-forward 的人身边工作。哪些内部工作方式可能会变成我们的日常？

Tara：有两个方面。第一，是继续和处于越来越高抽象层级的 agents 一起工作。让 agent 独立完成越来越多事情；你在中间提供 steering，然后让 agent 继续“cook”，在更高层次提供工作结果。

人们越来越把 agents 看成 persistent teammates、persistent coworkers。你可以像和团队成员一起工作那样与它们工作：它们先做大量工作，你提供 input；它们再次工作；你们在不同 cadence 进行同步，互相查看 in-progress work，不断提供反馈。

这种 coworker model 是和 agents 工作的更自然 interface，我们在内部也已经看到很多这种方式。

第二，到目前为止，我和 agents 的工作很多是一对一的。我和自己的 agent 工作，agent 可能再派生 subagents 完成任务，但这和同事使用他们自己的 agents 的方式是分离的。

以前公司内部的人会在 Slack 上互相发送 Codex threads 的 screenshots：“我想和你分享我是怎么得到这个数字的，这是我做的事情。”但这也不是人们一起协作最自然的方式。

随着越来越多工作由 agents 完成，我们是不是应该能和同事的 agents 一起工作？什么是实现这一点最自然的 interface？这正是我们正在思考的事情。

Lenny：我脑海里浮现的是 chat。Tara 有一个 agent，我有一个 agent。她做了一份分析，我可以说：“我的 agent，去检查 Tara 的 agent，确认这份分析是真的，并且符合我理解世界的方式。”

Tara：理想情况下，工作会像 multiplayer game。我们一起完成事情，同时 steering 自己的 agents，而 agents 继续接管越来越多 rowing 的 tactical tasks。

Lenny：这像是信任和认知逐渐变化的过程。我们慢慢意识到这可以成为工作方式：“让它工作更久一点，它能承担更多。”

大家一直在谈 slow takeoff 和 fast takeoff。人们害怕 fast AI takeoff，担心 AI 突然聪明到让我们陷入大麻烦。但我们现在似乎处于 slow takeoff，这很好。我们在逐步迭代，也许并不慢，但至少不是突然出现一个 300 IQ 的 AI。

Tara：模型确实非常聪明。但让我们能够一起和 agents 工作，让 agents 处理越来越高阶的抽象任务，不只取决于 intelligence、执行 long-running tasks 的能力，以及保持专注的时间，也取决于很多非常基础、非常实际的事情。

Agents 在本地运行很方便，因为它们可以访问你机器上的全部 data。要让 cloud agent 成功，需要建设大量 cloud infrastructure。还要解决它访问 systems 的问题：agents 怎样和储存你全部 data 的 third-party systems 对话？

如果你雇了一个 colleague，把他锁在房间里，不让他访问 Google Docs、Slack 和公司 database，他不会很有用。一个被同样隔离的 cloud agent 也不会高效。

所以，要让 agents 真正有用，当然需要 intelligence，但也需要非常 tactical 的 data access、cloud infrastructure 和 reliability。这些问题看起来比 broader intelligence questions 更平凡，却同样决定最终效果。

Lenny：这触及另一个经常出现在节目里的词：ambition。你也经常思考这个问题。AI tools 不仅让我们能够更有野心，几乎也要求我们更有野心。但很多人并不习惯这样。因为简单事情现在极其简单，困难事情也变得容易，人与公司之间的差别，越来越取决于 ambition。

Tara：最有效使用 AI tools 的人，并不是简单地用它自动化 repetitive tasks，而是用它扩大自己能够完成的事情范围。

过去，一个“unicorn person”通常是一个有很强 product sense，同时也是 engineer，可能还是 designer 的人。他们之所以被看作 unicorn hire，是因为他们能压平不同职能之间的 translation layers，很快自己想出、构建并运行一个东西，然后再和团队协作。

我认为，最有吸引力的事情是，AI tools 可以显著扩大所谓“在自己能力范围内”的可能性。你可以把脑海里的更多东西变成现实，像过去那些 jack of all trades 的人一样。

现在我们几乎都拥有这个 superpower。我可以快速做出一组 designs，可以构建 initial prototype，可以找到 pricing model，可以把各种 scenarios model 出来。可能性的范围大幅扩大。

这也意味着，我可以更像一位 film author，在做事情时更充分地实现自己的 vision，达到更高 fidelity。AI 让这些能力进入了你的 reach，所以 ambition 可以被抬高。

你的 ambition 不再受限于你亲自执行或表达的能力，边界可以宽得多。

最难的是扩展自己的思维。Capabilities 扩张得太快，你必须在极短时间内重新思考“什么是可能的”。

Patrick Collison 的网站 patrickzen.com/fast 上有一组项目，它们在过去看起来 ambition 不合理，却在极短时间内完成。现在回看这份名单，真正让我惊讶的是，这些项目都发生在 AI tools 让人几乎立刻学会构建、立刻总结复杂文本和书籍之前。

过去我做不到的事情，比如让我构建一个想法的 CAD model，现在都可以尝试。如果过去的工具条件下已经有人能够快速完成那些项目，那么 AI 带来的能力是不是应该让这类“极短时间、高效果”的项目数量呈指数增长？

Lenny：最难的部分有时只是记得去尝试。你要形成一个新习惯：“Codex 能不能帮我做这件事？”

Tyler Cowen 的网站上有一句话：人们低估了走到别人面前说“你做的事情能不能更有野心？能不能更快？能不能放大十倍？”所带来的影响。

现在，PM role 中非常有效的一部分，就是提升别人的 ambition，提醒大家什么是可能的。当别人说“我们可以用这种方式完成，或者在这个时间点完成，也许这是第一版”时，你的工作之一就是抬高团队的目标：“可能性上限是不是明显更高？我们能不能更有野心？能不能更快？”

这是一个很好的位置。你能构建的东西、可能实现的事情，以及工作的兴奋程度，都会因此提高。

Lenny：Nick Turley 之前来过节目，我记得他有一个内部 meme：Is this maximally accelerated?

Tara：是的。

Lenny：Slack 里好像还有一个 emoji，写着 Is this maximally accelerated？

Tara：这完全是 OpenAI meme。Andrew Ambrosino 和我还喜欢问团队另一个问题：Are you mainlining it yet？也就是，你是否整天、每天都在使用这个产品来完成自己的事情？

这两个问题和“我们是否尽可能有 ambition”结合起来，就是产品开发的三个 memes。

第一，目标范围和规模是否足够有野心？第二，Is this maximally accelerated，也就是我们是否以最快速度推进？第三，Are you mainlining it yet，也就是你是否真正使用它，是否把自己的 taste 用于判断它是否有效、是否是人们真正想要的东西，并尽可能收紧反馈循环？

Lenny：这是新的 dogfooding，只不过不是吃 dog food，而是 mainline it。

Tara：完全正确。这个文化在团队的公开交流里非常明显。大家对产品着迷，不断询问“还能怎样变好？现在什么东西让你不舒服？我们正在构建什么？”

这说明每个人都在把自己的产品当作 founder 来负责。

Lenny：还有其他内部 memes 吗？

Tara：我想想。一个重要的 meme 是 feeling the AGI，或者说持续意识到 AGI 正在到来。

AGI 可能有很多种结果，人们也会有不同看法，但 OpenAI 大多数人加入公司的原因，是相信 AGI beneficial 的 mission，并且愿意做一切让这个结果成为可能的事情：既要实现 AGI，也要确保它对 humanity 有益。

在构建产品时，我还经常提醒自己：我们是不是在为两到三个月后的 models 构建？如果你按照 models 现在的能力建设，你会失败；如果你按照你以为 models 一年后的能力建设，你也会失败。两种结果同样错误。

如果你太早，你会错；如果你围绕过去的 model capabilities 构建，你也完全错。唯一可行的方式，是面向两到三个月后的模型。

你必须假设 models 会显著变好，把 model capability 放在产品中心，同时在 product constructs 上给模型让路。问题是：两到三个月后，模型会有什么能力？你的产品怎样适应它？

Lenny：你怎样知道两到三个月后会是什么样？在指数增长中，这很难判断。靠 gut feeling 吗？研究人员会提供哪些信号？

Tara：和 research 保持非常紧密的沟通极其重要。这些事情并不是完全的 black box。你通常知道研究团队关注哪些方向，比如希望模型在哪些 coding 或 writing 能力上变得更强。

我们确实会围绕特定 capabilities 进行工作。产品开发必须尽可能紧密地连接 research 的 agenda 和 roadmap。

Lenny：Kevin Weil 当时担任 chief product officer 时来过节目。我永远不会忘记他的一句话：现在就是 models 最差的时候。

这句话听起来非常简单，但很难真正理解。现在的模型将是它们有史以来最差的状态。它几乎已经成了 cliché，但确实荒谬地正确。

【广告：Mercury】

本期节目由 Mercury 带来。Mercury 是 radically different 的 banking platform，现在加入了 Spend。我使用 Mercury 多年，已经把所有 business banking 都转到 Mercury，体验非常好。

它像是由 product people 而不是 bankers 构建的 online banking。通过 Spend，你可以给团队成员发 individual cards，为每个人或每个 team 设置 spending limits，expense receipts 还可以自动从 Gmail 或 text 中导入。

你甚至可以给 AI agents 自己的 cards，并为它们设置 limits 和 policies。

大多数 founders 刚开始都一样：公司里所有人共用一张 card。起初没问题，直到某个人超支、receipt 丢失，你需要花两天弄清楚是谁花了多少钱、为什么花。

Spend 把 expense management 直接放进 Mercury。团队的 cards、budgets 和 reimbursements 都在管理 business 的同一个地方。不需要追问，不需要手工审核，也不需要月底混乱，团队可以更快行动，founder 不再成为 bottleneck。

访问 mercury.com 了解更多并注册。Mercury 是 fintech company，不是 FDIC-insured bank。Banking services 由 Choice Financial Group 提供，Choice Financial Group 是 FDIC member。IO card 由 Patriot Bank 提供，并依据 Mastercard International 的许可发行。

Lenny：过去几个月，在 Twitter 上出现了从 Claude Code 转向 Codex 的 vibe shift。虽然 Twitter 是一个 bubble，但很多 tech people 都在那里。除了 Tara 加入并推动产品，你认为内部在三到六个月里发生了什么变化？有什么东西是“我们终于弄明白了”，或者哪些东西被砍掉了？

Tara：有一句话是“启蒙之前，挑水劈柴；启蒙之后，还是挑水劈柴”。Codex app 的团队从一开始就高度关注 users，保持紧密 iteration loop，尽可能 mainline app，把每个细节做好。

外部用户和 Twitter 开始意识到这件事，用户也开始注意到。但团队的工作方式一直没有变化：真正关注 users，保持 iteration，尽可能使用自己的 app。

变化更多是市场终于追上了他们，而不是团队突然改变了。

公司里所有人仍然经常使用这个 app。建设它的人当然是 developer，也用它进行 development。他们不断修复自己的问题，也不断听取公司其他人的问题和用户的问题。

真正显著的是，operating mode 没有改变。我们一直在问：使命是否被充分抬高？进展是否 maximally accelerated？我们是否 mainlining it？

用户和 Twitter 上的人注意到了这一点当然很好，但功劳完全属于团队，因为这种工作方式从未改变。

Lenny：这个答案中最有意思的是它非常 human。是你、Andrew、Tibo 和整个团队对 customer、product 的着迷。不是 AI 本身给出了答案，而是 humans 做出了差异。

Tara：团队应该获得全部 credit。每个人都非常 thoughtful、independent。OpenAI 有很多 founders，尤其是 desktop team，几乎每个人都会像 founder 一样关心每个细节。

当他们发现某个地方应该更好时，就会独立构建起来。内部测试不好、没人使用、大家觉得没用，就继续迭代；测试通过后才对外发布。

这个 loop 完全归功于团队中的每个人。

Lenny：你也提到了 roles overlap。Engineers 在做 PM work，你可能在发 prototypes，甚至把它们推到 production。很多人会问：designer 现在的工作是什么？我负责什么，不负责什么？Marketer 又该做什么？你怎么看？

Tara：我一直最喜欢 startup 的一点是，角色边界非常少。有时我在 startup 工作，startup 意外成长成了大公司，但我主要还是在 startup 工作。

最终，所有事情既是你的 responsibility，也不是你的 responsibility。你要对 success 负责。Stripe 就是这样，engineer、PM、designer 之间没有清晰的边界。每个人都可以做任何事情。

我一直喜欢这种 mentality，现在 capability 终于追上了它。但我最在意的是，必须有人对这些结果承担 core accountability：产品有没有被 users 使用？人们想不想要？质量高不高？是否 effective？

这个人可以是 engineer、designer、PM 或任何其他角色，但必须有一个 DRI。为了实现 outcome，任何人都可以根据自己的兴趣和能力承担工作。

我喜欢的团队不是纠结每个角色的边界，而是所有人都聚焦于把结果做出来。

但另一方面，我也很喜欢 PM craft。PM 有许多 craft 的组成部分，Shreyas、Marty Cagan、Shashir 等人都写过很多很好的内容。

有些人可能会问：“我很喜欢自己所在领域的 craft。如果团队合作更 fluid、更 collaborative，我会不会失去把 craft 做好、把它打磨得更精细的机会？”

我没有答案。我们所有人都在一起经历这件事。模型可能非常有效地完成某些过去属于个人 craft 的工作，甚至比个人做得更好。于是你的 craft 会从“完成过去那项具体任务”，转向把它应用到产品或 discipline 的另一个部分。

但我仍在思考：怎样平衡成为团队一员、使用这些产品、被它们的 effectiveness 吸引，和我对 craft 的喜爱？对 engineer 来说，亲手写 code 很有乐趣，但现在我们不再总是这样做。

Lenny：这正是我想说的。Engineering role 现在变化得不可思议。过去你一整天写 code，那就是你的工作；现在已经不是了。

Tara：是的。很多人会怀念自己亲手写 code 时的 flow state。这是一个艰难的 transition，有人喜欢，有人不喜欢。

Lenny：对于处在 AI frontier 的人，我很想知道，未来 human brains 会在哪里继续有价值？长期无法预测，但在未来几年，人的大脑最有价值的地方是什么？

Tara：首先，是 accountability 的主体。最终是谁拥有这个 outcome？你可以把一起工作的 agent 看成你的 report。最终产品质量高不高？是不是你想让它完成和表达的东西？至少目前，这仍然由人负责。

尤其是在高度 regulated，或者要求 direct human interface 的行业和场景中，这非常明显。

其次，human brain 对 expression 很有价值。我之前说过，software 不像 real estate，更像 film。投入一个大 budget，并不会自动产生伟大的 film。最伟大的 films 也不一定拥有最大的 budgets。

建设 software 有 artistry、opinion 和 expression。你会感受到一个人或一个群体的 authorship。你选择建设什么、它给人的感觉是什么，这些仍然非常 human。

人的大脑还会继续在 caring for each other、和他人建立关系方面有价值。我的工作中，与团队成员交流、一起对某个领域产生 enthusiasm、一起学习和工作、提升彼此的 ambitions，这些都仍然是 human 的事情，而且比过去更重要。

我不能预测 models 最终会怎样，但这些部分在我看来非常、非常 human。

Lenny：你提到了“AI 能力和我们真正使用它之间的 overhang”。很多人觉得最大的 gap 是“我到底应该拿 AI 做什么？”

能不能讲讲你在工作中使用 AI 的方式，让大家产生一些“我没想到可以这样用”的灵感？一类是 PM job 因为 AI 变化最大、你现在固定用 AI 完成的事情；另一类是最近发现的、有趣又有创造力的用法。

Tara：我在工作中最兴奋的一种 AI 用法，是现在经常 build sites。你试过 build sites 吗？

Lenny：没有。先讲讲 sites。

Tara：Sites 是一个非常有趣的产品。你可以在 work 中把它作为 presentational artifact，但我也会用它来做任何事情。

我曾经为团队建过一个 game，让大家使用一个 site 一起玩，因为 site 有 database。最近我去 backpacking，还建了一个 site，记录路线以及沿途 elevation。旅行中的每个人都可以输入自己吃过的 food。

它非常快，也非常有效。Sites 实现了 Alan Kay 在六十年代提出的 personal software 梦想：真正的 personal computer，应该拥有 personal software。

过去我们都梦想创造 personal software。Notion 这类工具尝试通过各种 blocks，让人们配置出自己的软件。Sites 更直接：你只需要 prompt，“请为我构建这个完成某件事情所需的 exact tool”，它就会完成。

Sites 可以分享，可以自动更新，也可以使用内部 data 构建带大量 metrics 的 dashboard。与其辛苦制作 slide deck，不如使用 site 作为更 dynamic 的 presentation surface。

Lenny：使用 site 需要做什么特别的事情吗？是告诉它 create a site？

Tara：你可以在 Codex 里说：“为我的团队创建一个 mafia game site。”它就会做出来。

Lenny：我想确认一下，你说的是 capital S 的 Sites，但这应该不重要？

Tara：它知道 Sites 是什么。

Lenny：以前是“这是 source code，你自己想办法 deploy”，现在是它直接为你 host？

Tara：它会 host。你可以选择 public、只和 team 分享，或者只对自己 private。

过去我的 day-to-day 经常是制作 docs、sheets 和各种 artifacts。现在我经常直接制作 sites。

Lenny：Work、Codex、web 和 mobile 都能做 sites 吗？

Tara：Work 可以，Codex 可以，web 可以，mobile 也可以。任何地方都可以。【笑】

Lenny：我刚刚让它创建一个关于 Tara Seshan 的 site。

Tara：很好。

Lenny：你的姓是这样发音吗？

Tara：Tara Seshan，听起来像 station 的开头。

Lenny：好。我看到它已经做好了。看看这个，变得更 awesome 了。Multi-product，设计很漂亮，是真正的设计。

它还有 quotes：Big conviction，Small teams，Start with the buyer。你觉得这可以作为你的新 website 吗？

Tara：最上面放了一张我大概十九岁时的照片，这很有趣，也有点好笑。除此之外，我很喜欢这个 site。

Lenny：做得好，看起来不错。

Tara：我想那是我在 Stripe 的 badge photo。

Lenny：太棒了。它还围绕你的头像做了一个小设计，很可爱。

Tara：我还很喜欢使用 Codex 里的 Visualize。你用过 slash visualize 吗？

Lenny：没有。

Tara：Slash visualize 非常令人兴奋。你可以输入“visualize my ChatGPT usage until now”，它会调用你过去做过的事情，生成一个很棒的 visualization。

我经常会想，怎样不仅导入很多 charts 和 data，还能把它们用一种易于理解、对我要讲的 story 有用的方式呈现出来。Visualize 让这件事非常简单，使用起来也出乎意料地愉快。

Lenny：这说明这里有巨大的 power，而我们甚至不知道它存在，也不知道如何理解。产品不可能把所有东西都写出来，所以像这样的 podcast 很有用。

我想换一个方向，谈谈 writing。我问了熟悉你的 Brie Wolson 应该问什么。很巧，她之前也给我和 Adam Ward 的节目建议过问题。她说应该问你 writing as thinking。Tara brief 很有名。

是什么让你的 writing 如此 iconic？对于想提高 writing 和 document 能力的人，你有什么建议？

Tara：我非常相信，自己在工作中进行两类 writing。一类是 writing as thinking，另一类是 writing as reporting。

Writing as thinking，是我写 brief，解释为什么应该建设某个产品、为什么应该采取某个 strategy，或者提出一个可能有争议的 take。

Writing as reporting，是总结团队这一周做了什么，发送一份 report，或者写 launch、announcement 的 plan。

Writing as reporting，我很愿意自动化，也一直使用 models，让它尽可能简单。但 writing as thinking，我永远不会自动化。

对我来说，outline 一件事情，把它写成一定程度的 prose，删减、编辑、不断迭代，是让想法变得清晰的最重要步骤之一。

很多人会用很宽的 brush 说：“我永远不会用 models 写作。”或者：“我写作总是用 models。”在我看来，这两种 broad brush 都错了。

你应该尽可能使用 models 完成 writing as reporting；但如果 writing 对你来说也是 thinking 的过程，就不应该让 model 取代你的思考。

过去我的 briefs 很有特点，因为我把 writing 当作 thinking。我会钻进一个 idea 或 product，写一份 brief，花大量时间完善，再把它拿给不同的人，让他们尽可能攻击里面的 idea、找出漏洞、把它变强，然后再交给下一个人重复这个过程。

在 Stripe，我做过很多次这样的工作：启动一个新 product area、建议方向上的重大变化，或者分析问题并提出前进路径。

Stripe 是一个非常重视 writing 的文化。Jeff Weinstein 等很多人都很重视 writing 和分享 briefs。在 Stripe，一份 brief 甚至可能在公司内部 viral。Writing as thinking 在那里非常受重视，我大部分这类工作都是在那里完成的。

在 OpenAI，我仍然经常 writing as thinking，但这里最重要的 sharable artifact 不再是一份很长的 doc，也不再是传统意义上的 proof of work。

部分原因是时代变了。现在，一份很长的 doc 并不能证明你充分思考过，因为你很容易生成一份很长的 doc，反而证明你没有思考。

过去，我会先在 document 中思考，再把思考翻译成 presentational artifact。这个 artifact 表示我已经想清楚了问题，也表示团队接下来要做什么。

现在，我更倾向于 mocks not docs，或者 prototypes not docs。如果有一个东西可以让人尝试、互动，最好还能有真实结果，比如我们做了一个 experiment，跑了一个 A/B test，这就是结果，这就是为什么我认为应该朝这个方向走，那么它比 doc 本身更好的 communication tool。

我现在仍然经常写几百份 docs，但主要是写给自己，不再主要是写给别人。Doc 不再是最好的交流方式，这是我在这个时代相较以前最大的个人变化。

Lenny：你刚才说要让很多人对 doc 提供 feedback。听起来很明显，但一份 iconic brief，往往就是在迭代过程中不断获得反馈，让它越来越强，而不是第一次就完美。

Tara：我以前有一位 manager 告诉我，正确的做法是先把 doc 写到 70% 完成度，再拿给需要 buy-in 的人，让它从 70% 变成 100%。我一直这样做。

很少有优秀的人愿意参与一个已经完美 polished 的 idea。完美的 idea 会让新的想法从表面弹开；有一些凹凸、rough edges 的东西，反而可以让其他人和你一起打磨。

把 people 带进这个 process，并以 doc 作为底层 artifact，是我找到的最佳 collaboration 方式之一。

Lenny：你怎么看 AI brain rot，或者过度依赖 AI？如果我们用 magic 帮自己完成事情，会不会逐渐失去读写长文档的能力？你会刻意避免什么？

Tara：Writing as thinking discipline 是我日常工作中避免 thinking ability 萎缩的主要方式之一。

我会尽可能把 writing as reporting 外包给 model，但 writing as thinking 必须自己完成。我有一个 personal belief：如果我要让别人读我的 document，我至少应该先自己读那么多遍；至少要先投入预计其他人阅读它所花的时间。

Meeting 也是一样。如果我要召集一群人开会，我需要在会前准备好相当于所有人将在会议中花费的 collective time。

为了保持思考能力，我会自己先完成 document 的 writing，确保已经投入了预计别人阅读它的 collective time。我不会主要依赖 model 帮我 polish prose，也不会让它生成 first version。

当然，在 summarization、translation，或者把内容从一种 format 转换成另一种 format 时，我会经常使用 model。

Lenny：所以你的建议是，人类自己写 idea、brief 和 plan，不要从 AI 开始，也不要依赖 AI 来改进 prose。

Tara：至少对我来说，我会自己开始，也自己结束。中间可以用 AI 研究具体元素、加入 data、提取 data，或者帮助 push back on ideas。但 writing 应该由自己开始，也由自己结束，这样不会损害 thinking。

Lenny：最后一个关于 Sutter Hill 的问题。你曾经走过一段很不寻常的职业路径，去找你的 PM founder，然后说：“我想去 Sutter Hill Ventures。”这是一家非常 iconic 的 VC，Snowflake 等很多优秀公司都从那里出来。它有独特的 founding 方式，会 incubate companies。

那段经历是怎样的？你学到了什么？

Tara：Sutter Hill 是一家 iconic firm，而且故意保持 illegible。如果你访问 Sutter Hill 网站，几乎看不到任何东西。它不大声宣传，尽可能低调、尽可能 modest，却 somehow 对 Silicon Valley 最重要的一些成功负责。

它有一个非常独特的 incubation model，由 Mike Speiser 开创，并且一次又一次地获得成功。

对我来说，Sutter Hill 最重要的地方是：人们常常把寻找 product-market fit 或建设一家数百亿美元公司看成 dark art。他们会说这是 luck，是 chance，是很多因素偶然结合。

但 Mike Speiser 已经多次做到这件事，所以这里显然存在一种方法，也存在一份让它成为可能的 roadmap。你可以做一组事情，重复实现这个结果。它不只是 luck，也不只是 dark art，而是一套 playbook。

这套 playbook 在 Sutter Hill 内部。他们不仅知道怎样做 bets、怎样经常正确判断，也知道怎样通过每天不断 compounding 的事情，建设一家成功公司。

比如 enterprise sales team 应该怎样搭建，product 应该怎样定位，initial founding team 应该怎样组建。Sutter Hill 的 recruiting 非常出色，他们有一个叫 Reticle 的 secret tool，里面有他们接触过的每个人，以及这些人接触过的十个最优秀的人。

这让他们在寻找人才方面非常有效。

我去 Sutter Hill，是因为我的职业一直围绕同一个问题：怎样尽可能多次找到 product-market fit？无论作为 founder、在 Stripe 启动新 products，还是加入 Watershed 这样的 startup，我都在重复面对这个问题。

Sutter Hill 已经找到怎样为 B2B products 寻找 product-market fit，所以我想从他们那里学习。

Lenny：除了“他们知道怎样做”，你从那段经历中带走的一件事是什么？

Tara：我在那里学到的最意外的一件事是，product-market fit 当然重要，但我过去严重低估了 product marketing fit。

也就是说，产品如何被描述、如何被 marketing，甚至可以先于产品实际构建。正确的顺序可能是：深入理解 technology，理解 enterprise sales process，再形成 product marketing fit，也就是 narrative 和 positioning。

在构建 product experience 之前，先测试这个 narrative 和 positioning，可能才是正确的事情。你应该先向一百个人 pitch，尽可能完善 pitch，找到这个东西为什么具有 transformative power 的 marketing narrative，然后再决定具体的 product shape。

Mike Speiser 在这方面几乎无人能及。

过去我一直低估 PMM work，觉得它只是不同职能之间的 glue。但后来我意识到，优秀的 product marketing 对公司的结果有多么 transformative，甚至可能直接决定公司成功与否。

Lenny：这个 positioning 观点我非常赞同，我们节目里经常讨论它。

【现场展示：Sites】

Lenny：我来快速展示一下刚才生成的 site。我们聊天时它还在运行。看这个。

Tara：太棒了。

Lenny：我说“make it more awesome”，它真的变得更 awesome 了。Multi-product，很漂亮。这是真正的 design。

Tara：它有 quotes：Big conviction，Small teams，Start with the buyer。

Lenny：如果这成为你的新 website，你感觉怎样？

Tara：最上面那张十九岁左右的照片很有趣，但除此之外我很喜欢这个 site。

Lenny：做好了，看起来不错。

Tara：我想那是我在 Stripe 的 badge photo。

Lenny：太棒了。我已经取消分享了，但我很喜欢它围绕你的头像做了一个完整的小设计。

Lenny：Tara，在 lightning round 之前，还有什么想分享或想谈的吗？

Tara：有一件事我们在 product building 中经常思考，特别是 ChatGPT Work 这个新时代，是 knowledge work 和 coding 在根本上有多么不同。

Coding 非常 output-oriented。当你让它完成一个 coding task 时，你可以用 tests 验证它是否正确，也可以实际运行看看是否有效。你可以根据 output 验证它。

Knowledge work 不一样。你不能只看最后的 deck，然后看到其中的数字，再说：“成功率 90%，所以我相信它。”你必须思考过程、inputs、reasoning，以及它一路是怎样得到结果的。

因此，产品还需要继续适应 knowledge work。我们必须让 ChatGPT 更像一个 collaborator，让用户看到 in-progress work，看到 citations 和 inputs，和 model 一起走完到达最终 output 的 journey。

这样你最后才能知道：“这个东西是对的、质量好、有用。”

这会体现在 product UX 上，也应该体现在 reasoning 和 chain of thought 上。比如，在它到达最终结果的过程中，用户是否应该看到更多 citations？A thread 这种非常适合 coding 的 surface，是否也适合 knowledge work？

这里有很多大的 product questions。随着我们把 human collaborators 带进工作，也需要思考怎样让 model 成为更好的 collaborator，和我们一起完成事情。

Lenny：这点非常好。我想象一个 exec meeting。你要向 executives 介绍计划，说明你认为应该做什么。很多时候，你不仅要给出结论，还要让他们看到你怎样走到结论，做过哪些工作和步骤。

所以，AI 也需要展示它完成的 proof of work。Engineering 不同，工程师通常不需要知道你做过的每一个 architectural decision，只要知道结果怎样、测试是否通过。

这里还涉及 context：它有没有做这件事所需的 context？它能不能看到你的 email 和 Notion docs？

Tara：是的。

Lenny：这个 job 很难。所有这些工作都是一个 product，真的很复杂。

Tara：那我们进入 lightning round。

Lenny：我有五个问题，准备好了吗？

Tara：准备好了。

Lenny：你最常推荐别人读哪两三本书？

Tara：我很推荐 William Finnegan 的 Barbarian Days。它讲一个 New Yorker reporter 的人生，以及他怎样爱上 surfing，并把 surfing 变成自己的 passion。

这本书让我明白，一个人可以极其 passionate、dedicated，把一件事当作 life purpose，即使自己并不擅长它。书中有一种很吸引人的东西：爱上 surfing，追求 excellence 和 perfection，同时知道自己永远无法真正达到。

这对我理解怎样生活有很大影响。

另一本我推荐的是 Anna Karenina。我最近重新读 classics，很喜欢它，因为它是一层一层的书。

我们在新时代需要不断改变自己，去做和过去不同的事情。十三岁读 Anna Karenina 时，我只理解 plot；十七岁再读，我理解了 European history dynamics 和 class warfare；三十岁再读，我想：“这其实是一个关于女人和人类的故事。”

同一本书可以随着你的成长，被不同 lenses 重新理解。这让我想到我们在 career 中也要面对的成长。

Lenny：这两本书都能和我们所在的 AI 时代联系起来。我今年早些时候读了其中一本，之前从没读过，是在一份“世界上最聪明的人读过什么”的书单上看到的。

有人提前告诉了我结局，所以惊喜少了一些，我不想剧透。它也很长。现在我在读 The Power Broker，感觉像是用半生在读它。

Tara：我很喜欢 The Power Broker。还有一个建议：如果有人关注 Simon Hizer 的 Substack，他会 slow read 重要书籍。他读过 War and Peace，也读过或正在读 Hilary Mantel 的 Wolf Hall，一章一章地读。

The Power Broker、War and Peace 甚至 Anna Karenina 这类书，一章一章读可能是最好的方式。

还有一个 99% Invisible book club 讲 The Power Broker，一共十三集，每集一两个小时，每次讲几章。他们邀请 Petey、AOC，以及在那个地区生活过的人，逐章讨论故事，还邀请 Robert Caro 多次参加。

边读边听他们的分析非常有趣。

Lenny：这是个很好的建议。继续 lightning round。最近喜欢的 movie 或 TV show 是什么？

Tara：当然是 The Odyssey。我觉得它是一部非常、非常棒的电影。我的 hot take 是，它其实是一部关于 AI 的电影，或者说是 Christopher Nolan 对 AI 如何改变社会的看法。

我非常喜欢，也强烈推荐。Nolan 是非常出色的 director，他把 artistry 和 commercial success 结合起来，现代导演中几乎没有别人做到同样的程度。

我最近还看了 Akira Kurosawa 的 Rashomon。这是第一次有人用不同人物的 perspectives 讲同一个故事，让你到最后都不知道什么是真相。这个 technique 是 Kurosawa 在电影中开创的。

它提醒我，在 constraints 下也能创造什么。那部电影拍摄于五十年代，是 black and white，可能只有一个人拿着 camera，但它仍然非常完美、非常有 taste、非常 innovative。

我在 iPhone 上拥有他拍电影时一百倍的 power 和 tools，那我还有什么理由不提高 ambition，做出更好的东西？

Lenny：一切又回到了 ambition。我还在努力买 The Odyssey 的票，已经很难买了。我之前没有及时去看，现在一个月内几乎没有座位。

Tara：本周早些时候，Kevin Clark 在晚上十点帮我们买到了 Metreon 的票。电影太棒了。

Lenny：下次叫我，我一定去。我甚至让 bots 帮我找票，还让一个人专门处理，大家都在努力找一张票。

Tara：你一定会喜欢。看完后我很想知道你是否同意我的看法：它讲的是 AI 和 morality 的 collapse。

Lenny：不剧透。节目发布时，希望我已经看过。如果有人有渠道，请告诉我。我想看 IMAX、最强的版本。

Lenny：最近发现的 favorite 或 interesting AI product 是什么？最好不是 OpenAI 的产品，但也可以说 OpenAI。

Tara：当然，我最喜欢的 AI product 是 ChatGPT，也喜欢在 Codex 中使用 Sites 和 Visualize。

在 OpenAI 之外，我最喜欢的 AI products 是朋友为我做的 products，因为现在大家真的可以为朋友做软件。我非常喜欢 cozy software movement：为五个朋友制作工具，然后大家一起使用。

我有一个朋友叫 Sebastian，他做了一个很酷的 AI app，可以把任何东西变成 podcast，再放进一个小 podcast app。它还为我们这群朋友做了一个很棒的 private social network，叫 GATS。

这正是我认为未来应该有的样子：人们为自己和朋友的需求，制作完全贴合的软件。

Lenny：GATS 代表什么？是 inside joke 吗？

Tara：不是，至少如果是 inside joke，我不知道。它有点像一小群朋友的 private Twitter。

Lenny：像 WhatsApp？

Tara：对，差不多。

Lenny：那个 podcast app 很有意思。我想要的版本是，它成为我的 podcast feed，之后我想读的东西会不断被转成新 episodes 加进去。

Tara：它就是这样。它会把内容放进你的 Apple Podcasts feed。

Lenny：太棒了，我想要这个。怎么帮我订阅？

Tara：当然可以。

Lenny：最后两个问题。你有没有经常在生活或工作中回到的一句 life motto？

Tara：我工作中经常回想的是 Tony Morrison 关于 work 的四句话，出自她的 essay The Work You Do, the Person You Are。

第一，无论 work 是什么，都把它做好，不是为了 boss，而是为了自己。

第二，是你塑造 job，而不是 job 塑造你。

第三，你的 real life 是和 family 在一起。

第四，你不是自己所做的 work，你是你这个人。

Lenny：我起鸡皮疙瘩了。

Tara：我把它固定在 Twitter profile 的顶部。每次打开 Twitter，都能再次看到它。

Lenny：这是记住重要事情的好方法。

Lenny：最后一个问题。你以前是 Teal Fellow。是 Teal 还是 Thiel？

Tara：Teal。

Lenny：这个 alumni group 太强了。这个项目很特别。你有没有愿意分享的故事，或者那段时期让你觉得“太疯狂了”的事情？

Tara：Teal Fellowship 是我人生的 inflection point。没有它，我不会走到今天。

有一些关键时刻，别人会告诉你提高 ambition，而你真的听进去了，人生因此改变。那时有人来到我面前，抬高了我的 ambition，告诉我：“你可以做到，不必沿着原来的 path 走。”我一直非常感谢他们。

现在和我一起工作的 Teal Fellow 之一是 Ari Weinstein。他创办了 Sky，后来被 OpenAI 收购。在此之前，他创办过另一家公司，后来被 Apple 收购，并在 Apple 工作了一段时间。

Ari 是我见过最有 creative thinking 的人之一，也是 Mac 上各种 cool things 的专家。现在他在 OpenAI 负责很多 computer use 的工作，已经推出了很多优秀功能。

他的 creativity、做事时的 joy，以及对 craft 的热爱，都非常鼓舞我。他是一个很酷的人。

Lenny：你想故事时，我来为不了解的人解释一下 Teal Fellowship，如果我说错请纠正我。

Peter Thiel 大概是说：“人们不应该去 college。你应该构建自己想要的东西，获得 100,000 美元，不去 college，直接追随自己的 ambition。”这样说大致正确吗？

Tara：完全正确。那时每年有二十个人，因为项目叫 20 Under 20。

Lenny：这个项目持续了多少年？现在还在吗？

Tara：我认为仍然在继续。前四五年左右，每年大概保持二十人的规模。

我那一年非常疯狂的一件事是，项目第二年，他们决定把整个 fellowship 做成 CNBC documentary。所以我参加 fellowship 时的 pitch、站在台上讲自己想做的 idea，全都遗憾地留在 YouTube 上了。

如果你想看一个十九岁的我做一些尴尬的事情，可以去找。

那一批中最成功、最令人惊叹的人之一是 Dylan Field。他不仅非常有 talent，也非常善良。

我很幸运能够和这些人一起工作。

Lenny：Dylan 确实是大家想到 Teal Fellows 时最先想到的人。

Tara：是的。

Lenny：这个 brand 太强了。Tara，今天非常精彩。你想推荐什么吗？听众怎样可以帮助你？

Tara：大家可以使用 ChatGPT desktop app，也可以在 web 上使用 ChatGPT，尝试 Work。现在它还是一个不太显眼的 toggle，但你可以切换到 Work，要求它完成一件有趣的事情，或者让它为你建立一个关于自己的 site。

你也可以让它制作一个 Visualize block，展示你的 ChatGPT usage。这是非常好的入门方式，可以近距离体验这些工具的 power。可以做的事情几乎是无限的。

Lenny：我有一个更好的想法。让它建一个 site，告诉你 Work 能做什么。

Tara：很好。

Lenny：这样就解决所有问题了。

Tara：我本来还想说，大家可以下载 ChatGPT app，在 web 上使用，尤其要试试 mobile。你可以坐一段很长的 subway 或 Muni，甚至在没有 service 的时候让它继续工作。等你走出来，任务已经完成。

这部分非常神奇。你不需要一直打开 laptop，它们终于可以在 cloud 中持续运行，做真正的工作。

Lenny：这正是我想提到的。如今 mobile 上的 cloud piece 被严重低估了，而且不只是 mobile-only feature。

Tara：它到处都可以用。

Lenny：所以，在 mobile app 中，你可以进入 ChatGPT，切换到 Work，让它完成工作。任务不是在手机本地运行，而是在 cloud 中继续运行，直到完成。然后你可以回来和它聊天。

这件事听起来简单，但 power 极其巨大。

Tara：没有其他要补充的了。

Lenny：谢谢你，今天非常精彩。

Tara：谢谢你邀请我来，能和你交谈很开心。

Lenny：从 Teal Fellowship 到今天，真是一段旅程。我会在 intro 里多讲一些。

Tara：谢谢。

Lenny：感谢大家收听。如果你觉得节目有价值，可以在 Apple Podcasts、Spotify 或自己喜欢的 podcast app 订阅。也请给节目评分或留下 review，这会帮助更多听众找到它。

过去的 episodes 和更多节目内容可以在 lennispodcast.com 找到。下期见。
