---
访谈时间: 2026-08-24
访谈时间说明: "无法从公开节目资料独立确认实际录制日期，使用官方 YouTube 发布时间。"
YouTube发布时间: 2026-08-24T23:00:32Z
嘉宾名字: Shafu Elfouly
嘉宾公司名称: Circle
参与嘉宾:
  - 姓名: Robbie Klages
    公司或机构: The Rollup
    职务: 主持人
  - 姓名: Shafu Elfouly
    公司或机构: Circle、Merit Systems
    职务: Staff Software Engineer，负责 x402 与 agentic commerce 基础设施
播客名称: The Rollup
播客url地址: https://www.youtube.com/watch?v=eWKG2hQLFcg
youtube_video_id: eWKG2hQLFcg
字幕来源: YouTube en-orig 原始字幕，结合完整上下文转写为简体中文
全文提及的关键名词:
  - The Rollup
  - Shafu Elfouly
  - Circle
  - USDC
  - x402
  - HTTP 402
  - agentic commerce
  - AI agents
  - agent stack
  - MCP
  - Cloud Code
  - Codex
  - Cursor
  - Poncho
  - Merit Systems
  - XRouter 2
  - XRouter 2 Scan
  - Anthropic
  - OpenAI
  - Coinbase
  - Brian Armstrong
  - Amazon
  - Twitter
  - LinkedIn
  - Apollo
  - Resy
  - 1inch Aqua
  - Dinari
  - Space and Time
  - Relay
  - Zama
  - NEAR
  - stablecoin
  - API
  - wallet
  - on-ramp
companies:
  - Circle
  - Anthropic
  - OpenAI
  - COIN
  - Cursor
industries:
  - 加密
  - 支付
technologies:
  - Agent
  - 稳定币
  - LLM
  - 编程助手
keywords: []
tags:
  - Circle
  - Anthropic
  - OpenAI
  - COIN
  - Cursor
  - 加密
  - 支付
  - Agent
  - 稳定币
  - LLM
  - 编程助手
---

# Circle Head Of AI：Agents Are Already Eating All Of Finance (Writing Is On The Wall)

## Transcript

**Robbie Klages：** 欢迎收看 The Rollup。今天我们讨论 AI agents 如何使用金钱，以及由此形成的 agentic economy。Coinbase 的 Brian Armstrong 之前谈过 AI fi，现在 agentic finance 又出现了新的基础设施。今天的嘉宾是 Shafu Elfouly，他刚加入 Circle，长期思考 agent 如何获得钱包、如何为互联网服务付款，以及 stablecoin 在其中扮演什么角色。Shafu，欢迎来到节目。

**Shafu Elfouly：** 谢谢邀请。我原来是做 AI 的，曾经做过机器学习工程师。2020 年我掉进了 crypto 的兔子洞，开始研究 DAO、DEX 和链上金融。之后我参与过 tokenized bonds 项目，做过以太坊上的去中心化 stablecoin，也在 Erik Voorhees 的 Venice AI 做过智能合约。后来我加入 Merit Systems，搬到纽约。Merit 在一次 pivot 中接触到 XRouter 2，才真正开始深入 agentic commerce。

XRouter 2 是一个开放协议，让支付可以直接通过 HTTP 完成。对非技术用户来说，可以把它理解成 API 原生的支付层。过去一个服务商把 API 放在互联网上，用户通常要先注册、拿 API key、选择月度订阅、预充值，或者让某个中间平台替自己处理计费。XRouter 2 的思路是，服务端可以在请求需要付费时返回 HTTP 402，调用方随后用一个标准化的支付头完成付款，再重新发起请求。付款与服务请求在同一条互联网交互里完成。

在 Merit，我们做了 XRouter 2 Scan。它有点像 XRouter 2 生态的 Etherscan，可以查看哪些服务器支持这一协议、有哪些转账、哪些服务已经开始接受 agent 的按次付款。最早链上只有大约一千笔交易，其中一半还是 Coinbase 的测试。后来相关工具传播开来，几天内交易数量增长到几百万，agent e-commerce 这个概念也因此被更多人看到。

**Robbie Klages：** 对 agent 来说，为什么 HTTP 402 加 stablecoin 会比传统订阅更有意义？

**Shafu Elfouly：** 关键在于 agent 不是一个坐在电脑前、偶尔点击一次的用户。一个 agent 可能需要调用搜索、数据、交易、物流、内容或身份服务。若每个 API 都要求注册一个账户、保存一个 key、接受一个月度方案，agent 就必须管理大量凭证和订阅。对人类来说，这已经很麻烦；对自动化系统来说，凭证管理会成为整个流程的瓶颈。

XRouter 2 把它简化成一次按请求付款。agent 带着钱包和公开密钥访问服务，服务商返回需要支付的金额，agent 用 USDC 完成结算，之后获得数据或执行结果。调用者不必为一个偶尔使用的 API 买整月套餐，也不用提前猜测自己会调用多少次。可以调用 Apollo 的数据，也可以调用 Twitter 的数据；如果一次请求只值一美分，就支付一美分。统一钱包取代了大量账号、API key 和月度订阅。

USDC 很适合这个模型。它可以快速结算，交易费用相对低，资产单位稳定，能够在全球互联网服务之间移动。对于 agent 来说，它不是把信用卡号交给一个陌生网站，也不是由每个服务商分别建立支付系统，而是让 agent 携带一套可编程的美元余额。我的判断是，agentic commerce 目前绝大部分交易都在使用 USDC，这不是因为其他资产没有价值，而是因为 agent 需要一个稳定的记账单位和即时结算工具。

**Robbie Klages：** 这种服务接入需要多长时间？它会不会还是只有大型技术公司才能完成？

**Shafu Elfouly：** 供应侧的接入非常简单。一个服务商可以把现有 API 放到 XRouter 2 后面，保留原来的 API key，然后让协议负责处理付款。Merit 做过实际测试，我们有一次只花了大约一小时，就把一个很小的花卉配送 API 接入。那是一家美国中西部的花店 API，提供商本身没有太多工程资源，但它可以给我们一个 key。我们为它包一层 XRouter 2 服务，之后 Cloud Code 或其他 agent 就能调用这个服务，把花送到美国境内的地址。

也可以由 Twitter、LinkedIn 这样的服务商原生集成。它们只需要投入一部分工程周期，就能把付费请求直接作为产品能力提供出来。对于已经有 API 的公司，真正的工作并不是重写整个后端，而是理解支付挑战、返回付款要求、验证支付并继续执行原来的接口。它的特点是直接、开放、部署快。

**Robbie Klages：** Circle 在整个系统中处于什么位置？这显然会增加 USDC 在 agent economy 中的使用量，但 Circle 如何让这个网络运转，又如何从中获得商业价值？

**Shafu Elfouly：** Circle 正在构建一个 agent stack，面向开发者、消费者和商家。对于商家，它提供把 API 接入 XRouter 2 的基础设施；对于 agent，它可以提供钱包、公开密钥和 USDC 支付能力。目标是同时推进需求侧和供应侧，让更多服务可以接受 agent 的付款，也让更多 agent 能够真正持有并使用 USDC。

这本质上是一个经典的双边市场。一边是能够提供数据和执行能力的商家，另一边是需要这些能力的 agent。没有足够的服务，agent 没有地方花钱；没有足够的 agent，商家也不会花工程时间接入。所以 Circle 的价值不只是发行一个 stablecoin，而是围绕钱包、开发工具、商家接入和支付标准，尽量让交易在 USDC 上发生。

**Robbie Klages：** 目前最大瓶颈在供应侧还是需求侧？

**Shafu Elfouly：** 供应侧已经相对成熟，因为把 API 放到 XRouter 2 后面非常容易。你去 Circle marketplace 或 XRouter 2 Scan 搜索一个知名 API，很可能已经能找到对应的 XRouter 2 server。真正困难的是需求侧。

第一，非技术用户不知道如何配置 Cloud Desktop、MCP 和钱包。他们甚至还不知道 stablecoin 是什么。第二，USDC 的 on-ramp 仍有摩擦。我有德国 debit card，但人在纽约时许多 on-ramp 不能正常使用。企业获得 USDC 也不够容易，尤其是要把资金放入可由软件调用的账户时，开户、合规、支付方式和地区限制都会变成障碍。我们正在改善这些入口，但现在最大的挑战仍然是把 USDC 放到更多人的手里。

一旦钱包和支付入口准备好，体验会非常直接。只要 MCP 支持这些 XRouter 2 资源，用户就可以让 agent 购买商品、购买域名，或调用各种数据 API，而无需分别订阅每一项服务。它从按月付费转为按次付费，从由人先开通权限转为由 agent 在真正需要时完成结算。

**Robbie Klages：** 对不熟悉 MCP 的用户来说，接入过程是什么样？

**Shafu Elfouly：** 可以把一段 skill 复制到终端、Cloud Desktop 或 agent 所在的环境，系统就会开始配置。若用户已经在使用 Cloud Code、Codex 或 Cursor，那么它们可以在原有工作流中调用 XRouter 2 资源。更重要的不是复制几行代码，而是让钱包、支付和服务发现成为 agent 的自然能力。

我们在 Merit 做的另一个产品是 Poncho。它可以理解为把 Cloud Code 放到了网页里，把复杂的 agent 配置、stablecoin 和钱包步骤隐藏起来。用户只需要注册，后台已经有 agent、钱包和 MCP 支付能力。Poncho 的目的不是要求每个人都先成为 crypto 工程师，而是让普通用户先体验开放式 agentic commerce：提出任务，agent 找到服务，按次付款，然后返回结果。

**Robbie Klages：** 如果我只使用 Claude 或 ChatGPT，Circle 是否会直接与 Anthropic 或 OpenAI 合作，把这种支付能力放进订阅里？

**Shafu Elfouly：** 这已经在发生讨论。虽然我在节目录制时还没有正式加入 Circle，但我与团队有接触。Circle 的团队曾向 Anthropic 介绍这一套技术。对于第一次使用 Cloud Code、让 agent 通过它在 Amazon 上完成购买的人来说，体验会有一个很明显的瞬间：原来 agent 不只是回答问题，也能在互联网世界中使用自己的钱包、调用服务并完成付款。

从模型公司的角度看，这确实有潜在收入。假设 agent 每次购买商品、调用数据或执行任务都产生小额交易，模型公司可能在支付或路由上收取少量费用。即使每一笔只增加几个 basis points，当交易量足够大时，也会变成可观的收入。OpenAI 或 Anthropic 如果把这种能力直接放入自己的产品，用户会更容易使用，平台也可能获得新的商业模式。

但我最想避免的是每家公司分别建立自己的 agentic commerce。OpenAI 建一个封闭系统，Anthropic 再建一个封闭系统，用户和商家就要重新接入多个互不兼容的平台。我的愿景是一个开放的公共标准。agent 不应该只在某家公司的围墙里使用某家公司的钱包，而应该能够按照公开协议访问互联网服务。商家也不应该被迫猜测自己必须先接入哪个模型平台。

这和互联网早期很像。AOL 先把互联网包装成一个封闭的服务，但真正产生巨大创新的是开放的互联网协议。agentic commerce 也可能经历同样的路径：大型平台会尝试把用户、钱包、服务和交易全部锁在自己的体系里，但开放标准让任何 agent、钱包和商家都可以互相连接。开放并不意味着没有商业价值，而是意味着价值可以在更广泛的网络中竞争和组合。

**Robbie Klages：** 所以你把它看成开放的双边市场，而不是 Circle 自己控制的支付商城。

**Shafu Elfouly：** 是的。Circle 希望尽可能多地让 agent commerce 使用 USDC，但协议本身应该保持开放。agent 可以从不同入口进入，商家可以用不同工具接入，开发者可以围绕同一套支付能力构建新的产品。Circle 提供的是基础设施和流动性，而不应该成为每一次服务调用的唯一中介。

当然，开放标准不等于没有风险。钱包需要权限控制，agent 需要知道自己在为谁付款，服务商需要确认付款没有被伪造，用户需要能够撤销或限制授权。小额按次付款可以降低订阅浪费，但大量自动调用也可能在错误配置时迅速累积成本。agent 的支付额度、服务范围、身份和审计记录都必须可见，否则方便会变成另一种失控。

**Robbie Klages：** 你能否举一个具体的 agentic commerce 例子？

**Shafu Elfouly：** 一个简单例子是餐厅预订。用户告诉 agent，希望某个时间在某个地点找到餐厅。agent 先查找可用餐厅，再调用 Resy 或其他预订服务。如果这些服务通过 XRouter 2 暴露 API，agent 不需要先分别开通账户或订阅。它可以向服务发送请求，服务返回需要支付的金额，比如几美元或几美分，agent 从钱包中支付 USDC，随后获得预订结果。

另一个例子是数据调用。用户不一定需要购买一个整月的 Apollo 数据，也不需要申请一组长期有效的 Twitter API key。agent 只在完成当前任务时调用一次，按一次请求计费。花卉配送、域名购买、商品购买都可以采用同样的机制。开放 agentic commerce 听起来很宏大，但拆开来看，就是让 agent 按次购买互联网 API。

**Robbie Klages：** 你之前说 agents 会花掉数十亿或更多资金。为什么你对这个趋势这么有信心？

**Shafu Elfouly：** 因为 agent 的活动频率与人的活动频率不同。人一天可能登录几次网站、做几次搜索或购买一次商品。agent 可以持续运行，在后台比较价格、查找数据、执行交易、更新软件、安排日程和调用其他 agent。只要它能够可靠地识别服务、判断价值、获得授权并完成小额支付，互联网上大量原本无法经济化的请求就会变成交易。

现在很多数字服务之所以没有被使用，并不是没有需求，而是接入、认证和计费太麻烦。一个用户可能只想调用一次冷门 API，但为了这一次调用，他要注册、验证邮箱、申请 key、绑定支付方式，再接受月度最低费用。agent 可以把这个过程压缩为一次机器间交易。长期看，服务供应商会发现，自己不仅在卖订阅，也可以直接向 agent 提供细颗粒度能力。

**Robbie Klages：** 这是否意味着每个人都将拥有自己的 agent，并且每个 agent 都拥有钱包？

**Shafu Elfouly：** 我认为会有多种形态。有些人会在自己的 Cloud Code、Codex 或 Cursor 中运行 agent；有些人会使用 Poncho 之类的网页产品；有些企业会在内部部署 agent。无论界面是什么，底层都需要身份、权限、钱包和支付。agent 不一定要拥有完全自由的资金，而应该拥有明确的预算和授权范围。例如一个 agent 可以被允许每次支付一美元、每天支付一百美元，只能调用可信服务，超过额度必须询问用户。

这也会改变我们对账户的理解。今天账户通常属于人或公司，软件只是代表账户发出请求。未来 agent 可能成为一个持续运行的经济参与者，但它仍然需要可追溯到背后的个人、公司或组织。谁授权它？它的余额来自哪里？它调用了哪些服务？如果出现错误，责任由谁承担？这些问题和支付标准同样重要。

**Robbie Klages：** Circle 的 agent stack 是否包括这些更上层的能力？

**Shafu Elfouly：** 目标是为开发者、消费者和商家提供一整套基础设施。商家需要发布服务，开发者需要让 agent 发现服务，消费者需要给 agent 钱包和授权，支付网络需要稳定的 USDC 结算。Circle 会尽量把这些步骤变得简单，但生态中仍然会有专门做钱包、身份、风险控制、服务搜索和工作流编排的公司。

这也是为什么我强调开放标准。不同公司可以在自己的强项上竞争。有人做最好的钱包，有人做最好的服务目录，有人做最好的 agent 编排，有人做最好的合规和风控。如果所有能力都被某个平台封装，创新会受限；如果协议开放，开发者可以自由组合。最终用户关心的不是某个 HTTP 状态码，而是 agent 能否在可靠、可理解、成本可控的情况下完成任务。

**Robbie Klages：** 这会不会让 stablecoin 从金融产品变成互联网的机器货币？

**Shafu Elfouly：** 它至少会让 stablecoin 的一个原生用途变得清晰。过去人们常说 stablecoin 能改善跨境支付、汇款和交易结算，但 agentic commerce 进一步说明了为什么需要一种互联网原生的稳定资产。机器之间的服务调用数量很大、金额很小、频率很高，信用卡的费率、结算时间和人工开户流程并不适合每一次调用。USDC 可以让服务商和 agent 使用同一套稳定单位，并在链上快速完成结算。

这不是说所有金融都会迁移到 agent，也不是说 USDC 会自动赢得整个市场。on-ramp、监管、钱包安全、稳定币流动性和用户信任仍然是现实问题。我们要避免把一个很好的技术概念夸大成已经成熟的商业规模。现在最重要的是把小规模、可审计、低风险的调用做得足够顺畅，让开发者和用户真正看到价值。

**Robbie Klages：** 你对这个领域的最大判断是什么？

**Shafu Elfouly：** 最大判断是，agent 会成为互联网上新的需求侧参与者。它们不只是生成文字，而是会购买计算、数据、软件、商品和现实世界服务。很多服务商今天面对的是人类客户，未来也会面对 agent 客户。服务商需要让 API 可发现、价格可理解、权限可管理、付款可验证。能够完成这些工作的开放基础设施，可能比单纯再造一个聊天界面更重要。

另一个判断是，agent economy 的早期突破点可能不是特别复杂的宏大应用，而是那些按次计费、价值清楚、可以快速验证的服务。一个 agent 调用一次数据 API，支付一美分；调用一次餐厅预订 API，支付一笔费用；为用户买一个域名或一束花。每个用例都不惊天动地，但它们能证明机器可以自主寻找服务、付款并获得结果。当这些小用例组合起来，网络才会逐渐变得有经济活动。

**Robbie Klages：** 也就是说，agentic commerce 最终可以用一句很朴素的话概括：agent 为互联网 API 付费。

**Shafu Elfouly：** 正是如此。开放式 agentic commerce 听起来像一个很大的词，但核心机制非常简单。一个 agent 发现一个服务，服务说明价格，agent 用钱包支付，服务返回结果。x402 把这个流程放到 HTTP 层，USDC 让它有稳定的结算单位，MCP 和 agent 工具让模型能够调用它。真正困难的是把授权、身份、入口、钱包和风控做好。

如果这些基础设施能够逐步成熟，未来的互联网可能不再主要依赖人类点击、注册和订阅。人会给 agent 一个目标、预算和约束，agent 会在开放服务市场里寻找最合适的工具。Circle 希望 USDC 成为这个经济中的重要结算资产，但更大的目标是让机器之间的交易成为一种普通、可组合的互联网能力。

**Robbie Klages：** Shafu，感谢你参加 The Rollup，也祝你在 Circle 的工作顺利。我们会继续观察 agent、stablecoin 和开放支付标准如何发展。

**Shafu Elfouly：** 谢谢邀请。希望很快再回来讨论实际采用情况。
