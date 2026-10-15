---
访谈时间: "2026-07-30"
访谈时间说明: "公开信息未披露实际录制时间，使用 YouTube 发布时间。"
嘉宾名字: "Steijn Pelle; Frédéric Renken; Alex Rampell; Olivia Moore"
嘉宾公司名称: "Lassie; a16z"
参与嘉宾:
  - 姓名: "Steijn Pelle"
    公司或机构: "Lassie"
    职务: "联合创始人"
  - 姓名: "Frédéric Renken"
    公司或机构: "Lassie"
    职务: "联合创始人"
  - 姓名: "Alex Rampell"
    公司或机构: "a16z"
    职务: "普通合伙人（General Partner）"
  - 姓名: "Olivia Moore"
    公司或机构: "a16z"
    职务: "合伙人兼主持人"
播客名称: "a16z"
播客url地址: "https://www.youtube.com/watch?v=Fpg_8aiBxx4"
youtube_video_id: "Fpg_8aiBxx4"
YouTube发布时间: "2026-07-30T14:30:01Z"
字幕来源: "YouTube 原始公开自动字幕 en-orig，结合完整上下文转写为简体中文"
转写说明: "删除妨碍语义重组的字幕断行与时间戳，按官方 RSS 校正 Steijn Pelle、Frédéric Renken、Alex Rampell、Olivia Moore、Lassie、Dr. Quan 等自动字幕误识别；保留 AI agent、ERP、SOP、HIPAA、KYC、ICP、P&L、FDE 等专有词。"
全文提及的关键名词:
  - Lassie
  - Steijn Pelle
  - Frédéric Renken
  - Alex Rampell
  - Olivia Moore
  - a16z
  - Dr. Quan
  - dental practice
  - healthcare administration
  - AI agent
  - autonomous software
  - insurance claim
  - patient billing
  - practice management system
  - Robinhood
  - Superhuman
  - Coinbase
  - Toast
  - Visa
  - Workday
  - NetSuite
  - QuickBooks
  - PeopleSoft
  - Sabre
  - Stripe
  - HIPAA
  - KYC
  - system of record
  - small business
  - labor shortage
  - product-market fit
  - self-serve onboarding
  - software distribution
  - digital payment
companies:
  - HOOD
  - a16z
  - Stripe
  - COIN
  - Visa
industries:
  - 保险
  - 医疗
  - 加密
technologies:
  - Agent
keywords:
  - 创业
  - 合规
  - 人才
tags:
  - HOOD
  - a16z
  - Stripe
  - COIN
  - Visa
  - 保险
  - 医疗
  - 加密
  - Agent
  - 创业
  - 合规
  - 人才
---

# “Every small business should run itself” | Lassie with a16z

## Transcript

**开场旁白：** AI 在 Silicon Valley 被高估，却在 Iowa 被低估。过去的软件只是把纸质档案放进数据库，先通过本地 green-screen computer 提供访问，但真正工作仍要人完成。Lassie 从一位 Yelp 评分第一、每月却花约 200 小时做文书工作的牙医开始。模型参数很大、训练数据很多，却不知道怎样完成这些具体工作。Lassie 先让创始人自己成为 human in the loop，再逐步自动化掉自己的工作。

每家 startup 与 incumbent 的竞争，最终都取决于 startup 能否在 incumbent 获得创新以前先拿到 distribution。Lassie 直接向牙医提供每月数十小时劳动，因此客户把它当作能帮助经营诊所的同事，而不只是一个工具。它不是简单替代员工，而是让小企业主不必同时戴十几顶帽子。很多场景并不存在“AI 抢工作”，而是根本找不到愿意做这些工作的人。

### Lassie 的起点：一位被文书工作困住的牙医

**Olivia Moore：** 欢迎参加节目。Steijn，公司源于你和自己的牙医 Dr. Quan 的一次谈话。他说了什么，让你决定辞去 Robinhood 的工作，亲手替他处理 payments？

**Steijn Pelle：** 我没想到自己的“美国梦”会是这样。当时我在 Robinhood 工作。我从 Amsterdam 搬到 Silicon Valley，已经六年，一直想寻找一个足够难、足够重要的问题创业。

Dr. Quan 是我的牙医，我一年见他两次。他知道我在找问题，就问：“你想看看我是怎样经营这家诊所的吗？”他把我带到后面。我看到一个 Yelp 评分第一、技术设备也很现代的医生，每个月竟然花约 200 小时处理 paperwork 和 busy work。他亲手提交 insurance claims；因为找不到合适员工，还必须自己留下来向 patients 收款。

这让我非常意外。我母亲上世纪 70 年代在医院工作时，就把一袋袋现金带去银行，再手工处理 payments。我原以为几十年后问题早已解决，结果在美国最先进的牙科诊所里仍然存在。

起初我怀疑这只是 Dr. Quan 的个例。但我们继续拜访其他医生，包括 Pennsylvania 的 gastroenterologist，发现他们也在手工完成同样工作。美国有成千上万家小型医疗机构这样运营。我们知道问题很难，却正想寻找这种问题。

**Olivia Moore：** Dr. Quan 提出邀请时，你是不是还躺在牙椅上，嘴里放着器械，只能含糊地答应？

**Steijn Pelle：** 幸运的是我没有蛀牙，没有钻牙。他是在检查结束后把我带到办公室说明情况。

**Olivia Moore：** Lassie 很特别的一点，是你们在真正发布产品前，用数月甚至数年待在客户办公室。你们怎样说服医生让两个科技从业者进入诊所，还查看财务和患者信息？

**Steijn Pelle：** 这听起来确实很奇怪：“你好，我在 Robinhood 做 growth 和 referral program；Frédéric 在 Superhuman 做 product。能否让我们来替你处理 billing 和财务？”

但医生们很快答应，反而是需求真实的第一项证据。大家愿意花几个小时讲述问题，因为这不是可有可无的 vitamin，而是让他们夜里睡不着、甚至想放弃职业的 painkiller。他们学医是为了照顾 patients，不是为了处理表格。

按常理，医生应该质疑我们没有医疗财务经验，也会担心 HIPAA 与 security，不应给陌生人访问敏感数据。Dr. Quan 却说：“每天九点到五点坐在这里，你们可以做这项工作。”Scranton 的一位医生也让我们坐在后台，开放所需系统，几乎像教自己的孩子一样教我们。如此高的信任意愿说明，现有流程已经坏得很严重。

### 2020 年开始建设，等待模型能力追上来

**Olivia Moore：** 公司从 2020 年开始。当时能构建的产品与今天差别很大。Frédéric，你们的 product-building process 怎样变化？

**Frédéric Renken：** 从一开始，我们就想把诊所放到 autopilot，而不是再给员工一个需要操作的工具。这个愿景没有变，变化的是模型能力。早期模型，尤其 reasoning models，远没有今天好。

自动化任何工作都需要三层。第一是 context：牙医诊所的历史数据、patient records 和业务状态。第二是 tools：无论人还是 agent，都需要用工具执行操作。第三才是 intelligence。

我们先把 context layer 与 tools 建好。早期 intelligence 不强，但第一个工作流不需要太复杂推理，基础规则就能自动化一部分。后来模型变好，公司获得巨大 tailwind：已有完整上下文和操作工具，只需替换 intelligence layer，产品就会持续变聪明。我们有一些运气，但核心愿景始终是“替客户完成工作”，不是“让客户用软件完成工作”。

### 软件过去只存数据，AI 开始执行劳动

**Olivia Moore：** Alex，你很早就提出 software 会开始完成 labor。这怎样影响你对 Lassie 的判断？

**Alex Rampell：** 软件最初的本质，是把 filing cabinet 变成 database。航空公司过去把 reservations 放在文件柜里，IBM 与 American Airlines 联合开发 Sabre，把它们搬进计算机。之后每个行业都重复这个过程：HR filing cabinets 变成 PeopleSoft，法律档案变成 LexisNexis，会计档案变成 QuickBooks 和 NetSuite。

Sabre 的名字里之所以有两个“A”，就是因为它是 IBM 与 American Airlines 的联合项目。那个时代的核心创新是，票务员终于不必在纸上擦掉旧预订再重写，而可以在 green-screen terminal 里修改记录。这是很大的使用体验改善，却不等于预订本身已由软件完成。

电子化当然让查询、修改更方便，但人仍要完成工作。企业没有因此少用很多 HR 人员，只是过去要保护纸质档案，后来要增加 IT department 和 CISO 保护数字档案。我是在夸张强调，但效率提升没有想象中那么大。

Alex 明确说，这个判断是为了强调效果而有意夸张，不是说 PeopleSoft 或 Workday 没有价值。他的重点是：纸质档案时代需要人防止他人打开文件柜，数字时代则需要 IT 团队与 CISO 防止别人入侵数据库。信息更易用了，但企业并没有自动获得一支会做 background check、onboarding 和 benefits 解释的团队。AI 的分界点是从“记录状态”走向“改变状态”。

AI 的变化是，software 不再只是 dumb storage，而能修改档案并根据数据采取行动。HR 系统不应只显示员工资料，还应完成 background check、onboarding、解释 benefits；accounting system 不应只列出逾期 invoices，还应主动联系客户追款。

真正的 work 市场，比储存信息的软件市场大几个数量级。早期模型只是 next-word prediction，不足以自主经营诊所或可靠执行 background check；现在能力开始越过门槛，market size 因而大幅扩张。

fintech 已经证明 bundling 能扩大软件市场。Toast 的 restaurant software 在 1985 年技术上也许就能做，但餐厅不会为一套 MS-DOS 订位与菜单系统支付 10 万美元。把 payment processing 捆绑进去、从交易额收约 2%，公司就能有效获得接近 10 万美元收入。fintech 让原本付费意愿不足的软件市场变大。

software 直接完成 labor，比 fintech bundling 的扩张更大。公司不再只卖数据库或支付通道，而是按完成的工作收费，而且成本可能低于人、质量高于人。更重要的是，许多岗位根本找不到人。

我第一位牙医 Dr. Ronald Sloop 后来退休，部分原因是负责 bookkeeping 的核心员工离职，他无法再承受后台工作。他看到 Lassie 发布后说，如果当时已有这类产品，自己就不会退休。这不是 AI 抢走他的员工，而是劳动力缺口迫使医生退出行业。

经济学里，很多潜在需求位于当前供需均衡点右侧：消费者愿意为某项服务支付 1 美元，但人工生产成本是 100 美元，所以市场根本不存在。如果 AI 把成本降到 1 美元，原本不存在的服务就会出现。软件本身已经是万亿美元市场，金融交易是更大的同心圆，labor 则又大几个数量级。

Alex 因此将可服务市场画成三层同心圆。内层是已经巨大的传统 software，收费对象主要是信息存储和操作权限；中层是 fintech 捆绑的资金流，Visa 之类公司的大体量说明交易市场比软件席位费更大；最外层是企业每年真正支付的 labor 和外包成本。当 agent 能对工作结果负责时，它竞争的不再是每人每月几十美元的 SaaS 预算，而是已写在 P&L 里、数额高得多的人员预算。更重要的是，它还会创造原先因成本不合理而根本没有交易的新市场。

因此，这类产品的计价锚不是“用户能看到多少功能”，而是“每月可以稳定交付多少小时的工作”。只有当软件能承担这种结果责任，五位数年费才有与人工成本直接比较的基础。
这也是 Lassie 把自己定义为运行诊所的同事，而不是又一套需要医生亲自操作的工具的原因。

**Alex Rampell：** 可以用一个夸张例子理解新增需求。为什么美国每家牙科前台不同时配一位会说 Dutch 的 receptionist？偶尔确实可能有只讲 Dutch 的患者出现，但为了百分之一的概率，诊所不可能每年花四万美元雇一个人。如果这项能力的边际成本接近零，每家诊所都会愿意拥有。AI 不是只把现有一名员工换成软件，还会把大量过去因成本太高而不存在的服务变成默认配置。

同心圆最里面是储存信息的软件，规模已经约一万亿美元；外面一层是支付与金融交易，因此 Visa 等公司的市值能够很大；再外面才是整个劳动市场。只要软件开始按完成工作收费，收入上限就不再受传统软件席位费约束，而可以进入企业原本的人员与外包预算。

### 每家牙科诊所每年约 20 万美元行政成本

**Steijn Pelle：** 美国约有 16 万家 dental practices，每家每年行政成本大约 20 万美元。我们已经服务数百家，最常见的问题就是找不到人。拥有 Harvard 等顶尖学位的医生会自己工作到午夜，因此越来越讨厌这份职业，而他们真正想做的是照顾 patients。

当 Lassie 说“这个 agent 现在就能提供每月几十小时劳动”，医生会向同学或同行核实，再很快采用。我们的第一个 agent 每月只替代约 30 小时劳动，就已经能按五位数年费收费，因为它来自客户原本的 labor budget。Dr. Sloop 一类诊所每月还有约 200 小时可自动化，空间很大。

医生并不会把这笔支出与另一个每月几十美元的软件订阅比较，而会与招聘、培训和留住后台员工的成本比较。只要 agent 稳定完成固定数量劳动，五位数合同仍可能明显低于人工成本。更重要的是，很多地区的问题并非工资太高，而是根本没有合格候选人。对客户而言，Lassie 既是节省成本，也是补上无法招聘的产能。

但这也提高了技术要求。如果 software 只是工具，最后仍由医生兜底，出错成本有限；如果 agent 真正接管 insurance reconciliation 和 patient billing，就必须可靠工作。Lassie 需要构建 autonomous system，不能假设永远有人逐条审核。也正因为如此，公司花了几年才发布。

Dr. Quan 对我们的评价是，Lassie 不是替代人，而是让人不必同时戴那么多帽子。产品发布视频里，他说自己终于能去执教孩子的 soccer team、观看比赛。真正价值是把时间还给医生。

### 从 human in the loop 到 98% 自动化

**Olivia Moore：** 从“医生想要轻松一点”到“愿意让 AI 控制诊所 payments”，中间有很大信任鸿沟。但你们的增长大多来自 dentists 互相推荐。产品怎样做到约 98% 自动化？

**Frédéric Renken：** 最大原因是我们先在办公室亲自完成工作。如果不知道这个岗位怎样做，就不可能造出真正可靠的产品。

SMB 与 enterprise 的差异是，小企业里通常没有专门员工操作新工具。即使造出 dashboard，最后仍是医生夜里登录。因此，最初我们直接接管全部工作，自己成为 human in the loop，再逐步自动化掉最痛苦的环节。

当自动化率足够高，我们才把剩余少量例外交还给诊所。遇到 agent 不会处理的 case，就从 staff 的反馈学习。我们不会等到某一工作 100% 自动化才做下一项；只要达到至少约 95%、可以真正接管一个 job，就先投入使用，再通过长期尾部案例继续改善。目标是扩大“整个诊所有多少劳动由软件完成”，而不是在一个狭窄任务追求理论满分。

最初的运行方式非常直接：创始团队告诉诊所“这份工作我们替你做”，后台所有尚未自动化的步骤由团队自己执行。每当人需要重复登录 portal、核对字段或发送信息，就把问题变成新的工具和规则。换言之，产品路线不是先想象一套功能清单，而是逐项消灭团队自己每天遇到的劳动。

当软件已经能处理大多数 cases，诊所只看到最后很小一组 exception。工作人员对 exception 的处理又会回流为训练和产品数据。这样的闭环比让客户使用一个全新 dashboard 更有效，因为每一次失败都对应真实业务结果，而不是用户是否点击某个 feature。

**Steijn Pelle：** 对 business owner 而言，最后 2% 不一定是关键。过去每周要更新 200 份 patient ledgers、登录保险 portal、核对 bank account 约 200 次；如果 agent 完成绝大部分，只剩几条 claims 人工处理，就已经节省 10 到 20 小时。

访谈中也回到 Dr. Sloop 的故事开了一个玩笑：既然 Lassie 正在解决迫使他退休的后台问题，也许可以把他“重新激活”，让他回到牙科行业。这个玩笑对应的经济问题很严肃：如果许多医生不是因为治疗能力下降，而是因为丢了关键后台员工而退休，那么自动化不只节省现有诊所的成本，还可能恢复被行政摩擦淘汰的医疗供给。Alex 将它夸张地表述为，如果能让这类医生回归，可能会让更多人获得良好的 dental care。

科技公司也没有让 finance、payroll 和 HR 完全自主运行，但优质工具让小团队比十五年前高效得多。我们的原则是：agent 必须能够 hands-off 地完成绝大多数工作，不能依赖后台人海；但允许极少数边缘情况由诊所处理。数千名 staffers 会告诉我们 agent 还不会什么，帮助覆盖 long tail。

Steijn 来自 Robinhood，Frédéric 来自 Superhuman，因此团队对发布质量的门槛很高。达到可放手使用以前，不会把产品推给客户。

### 接入现有系统，避免让客户更换全部软件

**Olivia Moore：** Lassie 主要连接现有 practice management systems，而不是要求诊所更换整套系统。Alex，你常说 startup 必须在 incumbent 学会创新以前先拿到 distribution。AI 时代这个判断怎样变化？

**Alex Rampell：** 我把它叫 TiVo problem。TiVo 和 ReplayTV 发明了 digital video recorder，创新很好，公司处境却很差。它们要么低价卖给 Comcast 等大分发商，但其他 cable companies 会拒绝使用竞争者拥有的产品；要么 incumbent 几年后做一个更差的复制品，却依靠已有客户取胜；要么 license 给 incumbent，把大部分 economics 让出去。

控制渠道有时带来的不是 control premium，而是 control discount。假设 Comcast 买下 TiVo，其他有线电视运营商就不愿把核心录像体验交给竞争者，收购方也不会按照“整个行业潜在价值”支付价格。创新公司即使技术领先，也可能因为没有直接客户关系，只能接受有限收购或低利润授权。

startup 往往应该先做“无聊的管道”、拥有 customer，再在上面加有趣 feature。我创办 TrialPay 几年后才意识到，应该先做后来类似 Stripe 的 boring payment processing。只有控制支付管道，才有资格叠加利润更高的 offer-based payments。

AI 时代，一方面 incumbent 更容易复制。大公司过去因为工程师效率和流程问题行动慢，AI 会把一般工程师变成更好的工程师，缩短复制时间。例如创业公司想给 Workday 增加 background checks，这显然是好功能，但 Workday 拥有全部客户，也能自己加入。

另一方面，许多 AI labor categories 根本没有 incumbent software，因为过去的 incumbent 是一个叫 Betty 的员工，或者某家 billing agency。牙科后台没有一家类似 Workday 的巨型软件公司能迅速复制完整劳动。startup 不必担心谁来“吃掉午餐”，反而能创建过去不存在的 category。

public markets 现在常把“传统 software”视为过时，把“AI company”视为完全相反的东西；VC 也会追捧 pure-play AI。但 AI 本身就是 software，software 也必然加入 AI。声称做“Workday but AI”或“NetSuite but AI”的公司，最终仍要面对 incumbent distribution；而 incumbent 如果完全不开发 AI，才是真的失职。

过去还有一家为 Microsoft Outlook 提供更好搜索的公司 X1。产品确实比 Outlook 原生搜索优秀，但“替 Outlook 搜索邮件”本身终究是 Microsoft 很容易加入的功能。公司后来被 Yahoo 收购，没能凭单一创新建立独立大市场。这个案例说明，凡是明确附着在 incumbent 产品表面的功能，都要严肃评估对方复制速度与现有分发优势。

AI 让这场竞赛更尖锐：startup 建功能更快，incumbent 的工程团队也因为 AI 提效而复制更快。最后仍是同一个问题，startup 能否先建立足够客户关系、业务数据与工作流深度，使产品从“一个功能”变成难以替换的运营层。

**Steijn Pelle：** Lassie 竞争的旧 incumbent 确实是 Betty 或外包 billing agency，而不是一个能快速复制的巨头。但没有 incumbent 也意味着基础工作全要自己做。

我们必须连接所有 read/write systems，建立跨系统 ontology，让每个平台对 insurance claim 和 patient payment 使用一致 data model，再在上面构建 agents。多年积累形成技术防御：并非接一个模型就能完成。

同一笔 claim 在诊所系统、保险 portal、银行流水与患者账本中，字段名称、状态定义和更新时间都可能不同。agent 若不知道“已提交”“已接受”“已支付”“患者仍欠款”在不同系统中的准确对应，就会重复催款或错误核销。Lassie 必须先建立统一语义，再让 agent 安全读写每一个系统。这个繁琐整合过程正是没有现成 incumbent 时产生的防御壁垒。

go-to-market 同样形成防御。美国有数百万小企业，owner 很忙、不一定懂技术。Dr. Sloop 晚上七点也许还要回诊所处理 emergency patient，回家吃饭后又发现 supplies 需要订购。问题不是客户怀疑 AI，而是怎样在他的日程里找到他、解释价值并完成采用。

### “AI 在 Silicon Valley 被高估，在 Iowa 被低估”

**Olivia Moore：** 这不是从 App Store 下载一个 AI app 就结束。如何 onboarding？如果要派自己的 Betty 去全国每家诊所，商业模式也无法成立。

**Steijn Pelle：** 这是非常重要的 last-mile problem。假设我们能联系到医生并让他愿意试，接下来仍要让产品在繁忙、非技术型的小企业里快速起效。

Robinhood 和 Superhuman 的消费产品经验很有用。用户给你的耐心可能只有 48 小时。如果无法迅速展示 core product value，产品就会被删除。牙医也一样，不会等几个月让一个复杂项目慢慢上线；agent 必须接入后立刻开始工作。

我们因此不只建设 agent，也把设置过程做成接近 self-serve。医生进入类似 Stripe checkout 或 Replit onboarding 的流程：连接诊所 bank account、system of record、接收 claims 的 insurance portals，确认 business information 与在职医生。系统在后台完成大部分配置，只剩一两项仍需人工。我们距离几乎完全 self-serve 只有数月。

产品还要自动判断接入是否完整。例如，某家诊所有多位医生、多个纳税实体和不同 payer portals，系统必须确认每个 provider 的身份、银行账户与 billing relationship，才能避免收入进入错误账户。复杂性不能转嫁给医生，因为 Main Street 客户没有实施团队；如果还要求他们参加数周项目会议，产品就不可能覆盖数十万家企业。

消费级 onboarding 的意义，是在不牺牲后台合规与准确性的情况下，把设置动作压缩成少数可理解步骤。客户只回答自己知道的问题，系统负责完成验证、连接和初始配置。只有做到这一点，“把 AI 带到 Iowa”才不再依赖昂贵现场服务。

Robinhood 早期的重要创新之一，是让用户无需去 Charles Schwab 办公室，就能自行开户。KYC、bank linking 等复杂流程全部藏在消费级界面下面。Lassie 面对的 insurance portals、bank accounts 与 practice systems 也需要同样的抽象。

这就是“AI 在 Silicon Valley 被高估、在 Iowa 被低估”的含义。湾区讨论模型能力，Main Street 真正缺的是把模型接入陈旧系统、可靠完成工作的产品。

### Master plan：先服务牙科，再让每个小企业自己运行

**Olivia Moore：** 牙科还有很多功能可以建设，其他 healthcare practices 也需要 Lassie，范围再扩大则是所有 small businesses。你们怎样排序？为 dentists 建的能力，会让 physical therapists 版本更好吗？

**Steijn Pelle：** 计划分三步。终局是“every small business should run itself”。busy work 由 agents 完成；business agent 会与 consumer 的 personal agent、insurance company agent 及其他交易方互动。

第一步聚焦美国约 16 万家 dental practices。每家约 20 万美元年度行政劳动成本，而且普遍招不到人。只服务这一市场，对 Lassie 而言就可能是约 10 亿美元 recurring-revenue market。必须先把一个垂直做深。

第二步会选择另一类没有被良好服务、TAM 足够大的 doctor office。它同样需要消费级产品质量：agent 不只是约 95% 准确，还要真正可用；onboarding 必须像 Coinbase 或 Stripe 一样简单。

第三步扩展到全球 small businesses。抽象来看，它们都有 system of record，需要读写；都有 customers，医疗行业称为 patients；都有 appointments、payments 与 communication。先在 doctor offices 训练出会经营业务的 agents，最终可以服务 Iowa、Paducah、Amsterdam、Hamburg 等地的普通企业。

跨垂直复用的不是每条牙科保险规则，而是经营小企业的通用结构：理解客户身份与历史、安排服务、发送账单、接收付款、处理异常、更新记录，并与外部机构交互。牙科提供的是一套约束严格、结果可验证的训练场。把这些底层能力做好后，进入物理治疗、其他诊所乃至非医疗行业时，只需替换行业知识和部分工具，而不是从头建设 agent 架构。

团队不会因为终局很大，就同时追逐所有行业。牙科单一市场已经足以支撑大公司，也能迫使产品在可靠性、隐私和支付上达到很高标准。先把一个行业的劳动真正拿掉，再复制方法，比同时发布许多只有演示效果的垂直版本更可持续。

我们会保持 Robinhood 和 Superhuman 式的 laser focus，先把一件事做到非常好，再向外扩张。终局很大，但当前不能分散。

### 2026 年怎样建设公司

**Olivia Moore：** 你们曾参与 Robinhood、Coinbase、Superhuman 等公司的扩张。2026 年创业与过去完全不同。哪些经验仍适用，哪些必须重学？

**Frédéric Renken：** Superhuman 的一些原则仍适用。首先要严格选择 ideal customer profile。Lassie 如果接入不适合自动化的诊所，却承诺替它节省大量劳动，就会陷入无法兑现、又难以 offboard 的关系，代价比旧式工具更高。

其次，onboarding 必须快速到达核心价值。我们把整个过程当作一部有明确情节点的电影，规定每个时间点应到达哪个 checkpoint，并持续测量。

最大的变化是产品定义。过去主要思考“用户能用软件做什么”；现在只问“软件能替用户完成多少 work、节省多少 time”。传统 patient-billing product 也许提供发送 statement、接收 payment 的按钮，但真正耗时的是判断金额是否正确，以及回答患者“为什么欠这笔钱、保险为什么没覆盖”。如果这些沟通仍由诊所完成，工具没有节省多少时间。Lassie 发布 patient billing 时，目标是诊所不必再为这项工作花时间。

这也改变了 product metrics。旧软件可以用登录次数、页面访问或 feature adoption 衡量价值；劳动型软件更应衡量诊所少处理了多少 claims、少花了多少小时、收入是否更快到账，以及 agent 需要人工介入的比例。客户不应因为“更喜欢用 Lassie”而续费，而应因为后台工作确实从日程里消失而续费。

**Steijn Pelle：** 招聘标准一部分没有变化。仍需要学习斜率陡、雄心强、在 engineering 或 selling 达到前 5% 的人。奥运运动员还是要每天训练两次、把身体和心理推到边缘，company building 的基本强度没有消失。

新增标准是 AI-native mindset。候选人是否相信编程方式会完全改变？建设 finance department 时，会不会从第一天就按 AI 时代重构？我们想创建 2026 版本的大组织，同样团队产出两倍、速度快四倍。AI 不只要进入客户业务，也要进入公司自身每个 function。

Steijn 以田径作类比。他曾接近专业运动员水平，一些朋友后来参加 Olympics。新装备不会改变顶级运动员每天训练两次、持续逼近极限的要求；AI 也不会替代 ambition、discipline 和 judgment。它提高的是同样高水平人才能够交付的产出，而不是降低招聘标准。

因此，团队同时寻找两类特征：一是传统意义上的高斜率与强执行，二是愿意彻底重构工作方法。只会调用几个 AI tools 不够，候选人要主动思考哪些流程根本不应再按旧组织方式存在。

未来几年的实验是：多快覆盖全美 dentists、消除每家约 200 小时 busy work，再多快复制到新 vertical，最终帮助所有 small businesses。

### AI 让小企业更容易经营，会不会也让竞争更残酷

**Alex Rampell：** 如果每个人都能“凭空雇到 Betty”，小企业会更容易创办和经营，但也可能更难生存。AI 时代复制一套 software 已经很容易；复制一间实体诊所仍然困难，因为它依赖一组人共同交付服务。AI 如果把人员门槛也降低，small-business moat 会不会被削弱，竞争拥挤到利润消失？

Alex 用 Yogi Berra 那句自相矛盾的名言概括这个担忧：“这里太挤了，所以已经没人来了”（It’s so crowded, nobody goes here anymore）。如果 AI 让组建小企业所需的人手更容易“具象化”，它可能先提高创业和经营成功率，又因大量新供给进场而降低单个经营者的利润。他想问的不是 AI 能否节省一个岗位，而是当“人员集合”不再是进入壁垒时，小企业的结构性 moat 还剩下什么。

**Steijn Pelle：** 这个担忧假设 demand 有上限，但很多本地服务目前供给远低于需求。找一位好 plumber 很难；牙科也是如此。美国可能有两倍未被满足的需求。AI 帮助相同数量医生服务更多 patients，或者让行业容纳 50 万名 dentists，未必会挤压现有需求，反而能让更多人每年获得两次优质 dental care。

如果一间诊所因行政效率提升而多接纳患者，短期未必需要降低治疗价格，因为当前瓶颈是预约难、医生时间不足和后台人员短缺。只有当供给真正追上潜在需求后，竞争才可能压缩利润。在那以前，更便宜的后台主要把无法被服务的人带入市场，并提高医疗资源利用率。

当然，长期看经营门槛下降会增加竞争。Lassie 的观点是，小企业仍要依靠本地信誉、专业技能、患者关系和服务质量，这些不能由一个通用 agent 复制。AI 消除的是无差别行政负担，让竞争更集中于真正的 craft，而不是谁更能忍受夜间做表格。

primary care 也一样。我在 Netherlands 长大，当地家庭医生更了解社区和家庭；美国很多地方很难找到这样的医生。plumbing、烘焙等行业也想服务更多客户，却受 labor 限制。Lassie 释放的是 craft time：让医生看病、面包师烤更多 pie、技术工提供更多服务。

公众担心 AI 会怎样改变世界，但很少有人反对替小企业主清理 busy work。Lassie 是一种偏乐观的应用：技术让人更专注于真正有价值的手艺，而不是退出行业。

### 模型很大，却不知道怎样完成真实工作

**Olivia Moore：** 公司创办于 2020 年，早于 2022 年 11 月 ChatGPT 引发的 generative-AI 浪潮。reasoning models 已经进步很多。要让 software 真正完成 labor，今天最难、仍需技术突破的部分是什么？

她把问题进一步说成“small business 的 AGI”：现在是否已经完成 90%，只剩最后 10%，而这 10% 却又是一套功能能否完整交付的决定因素？她特别说明，这不只是 Lassie 的产品问题，而是所有试图让 software 承担 labor 的公司都要面对的技术曲线：在演示中做对一个任务，与在真实诊所里稳定、可追责地完成整份工作，中间仍有很大距离。

**Frédéric Renken：** 一个反直觉事实是，模型读过海量数据、参数巨大，却不知道怎样完成这些工作。具体 workflows 并没有编码进模型。

例如，我们建设某项产品时，需要收集向不同 insurance payers 提交 claims 的 SOPs 和 documents。大量知识只存在于 office manager 头脑里，互联网没有写下来。我们一度以为新 reasoning models 应该已经知道，实际发现它们不了解每条流程的细节。

一个模型也许知道“牙科保险需要提交 claim”，却不知道某一 payer 对某一 billing code 要求哪种角度的 X-ray、怎样写 narrative、哪些字段必须与 treatment plan 一致，或者拒付后下一步应走哪个 portal。这些知识常常没有公开网页，甚至没有统一手册，只存在经验丰富员工的习惯与历史记录里。

因此，大模型的通用推理只是起点。真正的工作系统还需要可追溯行业知识、当前业务状态、执行权限和失败恢复机制。Lassie 必须把隐性经验转成结构化规则，再让模型在规则无法覆盖的边缘情形中推理，而不能让模型凭语言流畅度猜答案。

Lassie 的优势是拥有大量历史 ERP data，可以从过去操作中推断 workflow。但模型仍需要更快地从少量数据学习。我也期待 smaller models，能够用更少 data、更快适应，让 intelligence 分布到各种设备和场景，甚至像 Pixar lamp 一样拥有个性。

产品层还要解决怎样从 staff 获取偏好和隐性知识，并转换成 agent 可用的 feedback。模型能力只是组成部分，把人的纠正变成稳定学习信号，同样需要大量 UX 设计。

### 当争辩的边际成本降到零

**Alex Rampell：** 我一直在想，当 arguing 的 marginal cost 变成零，世界会怎样变化。我的健康保险公司 Cigna 只寄 paper checks，没有 online enrollment。它可能希望支票丢失或用户忘记存入，形成故意延迟。保险双方长期都有博弈：公司不断 deny，客户也可能夸大损失。现在两边都有几乎免费的 AI，可以无限争辩。牙医的主要 counterparty 又是 insurance carrier，这会怎样改变 payments 与 collections？

**Steijn Pelle：** 牙科保险相对规则化。医生做一颗 crown，只要提供规定的 X-ray 与 narrative，保险文件明确写着应当覆盖。难点是一个人要记住 50、60 甚至 100 个常用 billing codes，以及每家 payer 的要求。

agent 能同时访问规则、相关 X-ray 与 treatment plan，按文档提交，保险公司也必须依照规则处理。它不是无止境制造争辩，而是让诊所第一次有能力稳定满足每项证明要求。

保险公司也需要优秀医生留在 network。每年它要向雇主续约，如果当地没有足够好、可覆盖的 dentists，雇主会换保险商。所以 carrier 并非只有拒付激励，也有保持 provider satisfaction 的需求。

在规则明确的牙科理赔里，AI 可能让双方的争辩减少，而不是无限增加。诊所第一次提交就附齐正确材料，保险商就更难以“信息不足”为由退回；保险商也可以用 agent 快速检查是否符合公开条款。争议会从反复补文件，转向真正存在医学或合同分歧的少数案件。

真正令人震惊的是，很多美国医生仍收 paper checks。我们曾坐在 Dr. Quan 后台，打开邮差送来的信封，把合计约 10 万美元支票存入银行，再逐张处理附带 itemized invoices。那时 filing cabinet 真的还是物理文件柜。

联邦政府随后要求行业逐步提供 direct deposit，并把明细转换成 digital file format。即使五年前已有今天的模型，也无法自动处理还在纸上的钱和凭证。现在监管推动的 digitization 与模型进步同时发生，才创造自动化窗口。

行业仍有约七成付款通过纸张完成，这说明技术可用并不等于转换自动发生。每家诊所要分别联系多个保险商，提交税号和账户资料，再确认电子汇款与电子明细能正确匹配。任何一个环节失败，都可能让钱到账却无法核销，或明细到达却找不到对应付款。

Lassie 建设的“转换引擎”因此也是产品核心：它不仅处理已经数字化的数据，还替客户完成从纸质状态迁移到电子状态。模型进步、监管要求和支付基础设施在同一时间交汇，形成一个过去不存在的自动化机会窗口。

但“切换电子支付”也不是一个按钮。医生可能要花 50 小时分别联系 Cigna、Delta 等保险商，完成账户设置。payments 进入诊所 bank account 后，又不能随意让 staff 看见 rent 等敏感交易。Lassie 因而把转换流程产品化：诊所提供 tax ID 与必要 business information，系统替它完成各 payer 的数字化迁移。

过去 staff 甚至偏好纸张，因为单纯把文件变成 PDF 并没有减少劳动。没有可执行工具时，拿纸逐项处理可能比在多个窗口间切换更方便。只有 AI 能读取、理解并行动以后，digitization 才真正带来效率。

### 怎样找到全美数十万家小企业

**Olivia Moore：** 需要 Lassie 的诊所遍布全国，数量巨大。怎样把 agents 带给 Main Street businesses？

**Steijn Pelle：** 这与 enterprise playbook 完全不同。卖企业产品，也许办几场 steak dinners，就能签下 1,000 万美元 ARR。Lassie 必须找到成千上万、最终数十万家小企业。

我们先绘制全国 dentists：owner 是谁，使用哪些 systems，有没有 hiring intent，例如是否正在 Indeed 招 billing staff。再以真正能穿透噪音的信息联系他们。

面向科技公司销售时，可以在 Clay 找到对象，用 Apollo data 补充，再通过 LinkedIn 判断谁负责采购。Dr. Sloop 通常不在这些数据库里，甚至没有 LinkedIn。因此，Lassie 必须开发一套完全不同的 go-to-market system。

团队会寻找更贴近 Main Street 的 intent signals，例如诊所是否在 Indeed 招聘 billing staff、是否刚更换 practice system、owner 是否公开抱怨人手不足。信息必须直接对应医生的痛点：“我们能替你完成多少小时工作”，而不是泛泛宣传模型能力。

销售触达后，产品的近自助设置又决定获客成本是否成立。如果每签一家诊所都要派实施人员驻场数周，即使需求很强，也无法服务 16 万家客户。发现、说服、设置和持续运行四个环节都必须自动化，才可能建立面向小企业的大规模分发体系。

这既是挑战，也是未被开发的机会。公司不仅在建设能完成工作的 agent，也在回答另一个基础问题：AI 怎样真正进入数十万家普通企业。

**Olivia Moore：** 感谢各位参加。对加入 Lassie、建设一代新公司的机会感兴趣，可以访问 lassie.ai。听说你们正在积极招聘。

**Steijn Pelle：** 是的。

**Frédéric Renken：** 谢谢邀请。
