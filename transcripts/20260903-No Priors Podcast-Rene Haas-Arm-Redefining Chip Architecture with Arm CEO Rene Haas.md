---
访谈时间: 2026-09-03
访谈时间说明: 无法确认实际访谈时间，使用 YouTube 发布时间
嘉宾名字: Rene Haas
嘉宾公司名称: Arm
参与嘉宾:
  - 姓名: Elad Gil
    公司或机构: No Priors Podcast
    职务: 主持人
  - 姓名: Sarah Guo
    公司或机构: No Priors Podcast
    职务: 主持人
  - 姓名: Rene Haas
    公司或机构: Arm
    职务: CEO；SoftBank Group International负责人
播客名称: No Priors Podcast
播客标题: Redefining Chip Architecture with Arm CEO Rene Haas
播客url地址: https://www.youtube.com/watch?v=85Y6h_jbRfs
youtube_video_id: 85Y6h_jbRfs
YouTube发布时间: 2026-09-03T10:00:26Z
字幕来源: YouTube公开英文原始字幕（en-orig），经完整上下文转写为简体中文
原始语言: English
全文提及的关键名词:
  - Arm
  - Rene Haas
  - Arm AGI CPU
  - CPU
  - GPU
  - IP licensing
  - compute subsystem
  - RTL
  - GDS2
  - AI
  - LLM
  - Transformer
  - token
  - verification
  - validation
  - debug
  - TSMC
  - Samsung
  - Micron
  - SK Hynix
  - Nvidia
  - Qualcomm
  - Amazon
  - Microsoft
  - Google
  - Meta
  - SoftBank
  - SoftBank Neo
  - Ampere
  - Graphcore
  - Stack AV
  - OpenAI
  - robotics
  - humanoid robots
  - data center
  - memory
  - substrates
  - advanced packaging
  - export controls
  - Semitech
  - Intel
  - national security
  - energy efficiency
  - edge computing

---

# Redefining Chip Architecture with Arm CEO Rene Haas

## Transcript

**Elad Gil：** 欢迎回到《No Priors》。今天我们邀请到Arm CEO，同时负责SoftBank Group International的Rene Haas。我们会讨论Arm在芯片产业链中的位置、芯片创新再次受到关注的原因、供应链挑战、robotics、能源、SoftBank生态，以及未来计算工作负载怎样变化。

**Rene Haas：** 很高兴参加节目。

**Sarah Guo：** 先祝贺你们在Hot Chips上的芯片发布。最近技术行业和软件行业都很想弄清楚芯片供应链到底发生了什么。对还不熟悉Arm的人来说，Arm处于产业链的什么位置？

**Rene Haas：** 我们在芯片供应链里有两个位置。主要业务仍然是授权IP。我们的CPU core会进入smartphone、data center、汽车和很多其他设备。客户有的自己生产芯片，比如拥有fab的Samsung；更多客户会完成芯片设计，然后把设计交给TSMC tape out。

**Rene Haas：** Arm覆盖的市场很广，所以能够从多个角度观察供应链。我们能看到汽车、data center和smartphone的需求变化，也能看到不同客户遇到的限制。去年3月，我们又发布了第一款实体产品，也就是在Hot Chips上介绍的Arm AGI CPU。现在我们不只是向别人提供IP，还要自己面对substrates、wafers、memory等采购和分配问题。

**Elad Gil：** Arm过去几十年主要做IP，为什么现在开始做自己的CPU？

**Rene Haas：** 这是一个逐步演化的过程。早期我们提供CPU IP、GPU IP、system IP等独立组件。后来我们发现，产品周期没有变慢，芯片制造时间反而在延长，客户越来越需要更快拿出完整解决方案。因此，我们从独立组件进一步做成compute subsystems。

**Rene Haas：** 我在几年前路演时用过Lego的比喻。独立IP像一块块积木，compute subsystem则是告诉客户怎样把积木拼在一起的蓝图。很多人一开始认为芯片设计公司不会需要这类产品，因为拼装本来就是它们的工作。但事实是，这种方式可以节约time to market，也能减少成本和工程复杂度，需求非常强。

**Rene Haas：** 实体芯片是再往前走一步。有些客户拥有足够能力，能直接基于Arm IP完成产品；但也有很多公司希望使用Arm，却没有能力或意愿自己完成整个产品。Meta就是第一个例子。它需要一款general-purpose agentic CPU，却找不到可以直接提供产品的厂商，于是双方开始合作。

**Sarah Guo：** 这会不会让其他客户担心Arm与某一个客户竞争？

**Rene Haas：** 我们很谨慎，先和生态系统沟通。CPU IP的价值取决于生态系统，既包括芯片公司，也包括软件开发者和围绕它构建产品的人。我们逐一询问客户是否接受这个方向，得到的反对比预想少得多。

**Rene Haas：** 原因是，市场上可用的软件越多，无论是proprietary还是open source，Arm生态和所有客户都会受益。Nvidia、Amazon、Microsoft、Google等基于Arm构建server chip的公司都支持这个方向。我们发布产品时，Jensen Huang、Renee James、Amin Vahdat、James Hamilton等客户和生态伙伴都公开表示祝贺，这算是很好的验证。

**Elad Gil：** 从授权IP转向实体芯片，需要增加哪些能力？

**Rene Haas：** 我们是一家fabless semiconductor company，没有fab，也没有建fab的计划，但要交付实体产品，就必须增加supply chain operations。我们要和TSMC、Samsung合作，还要与Samsung、Micron、SK Hynix协商memory allocation。工程方面也增加了很多能力，包括back-end、layout、implementation、bring-up labs和其他物理工作。

**Rene Haas：** 我2013年加入Arm时，最喜欢的就是没有inventory、没有RMA、没有scrap。那种业务的gross margin曾经达到98.5%，非常漂亮。现在做实体产品，就必须面对库存、物料、良率和交付的现实。不过我们的管理团队里有Broadcom、Qualcomm、Nvidia等公司来的负责人，他们以前做过这些事情，所以组织能力建立得比较快。

**Sarah Guo：** Arm内部如何采用AI？芯片设计会不会因为AI工具而明显缩短？

**Rene Haas：** 我非常相信AI会成为所有行业的utility，医疗、基础设施、robotics以及其他行业都会使用它。Arm内部非工程工作已经大量使用AI，工程侧的收益也很大。芯片设计通常需要24到36个月，真正耗时最多的并不是架构设计和RTL generation，而是verification、validation、debug和documentation。AI非常擅长这些工作。

**Rene Haas：** 今天Arm大约80%到90%的工程师每天使用AI。如果突然关闭这些工具，感觉就像回到1990年代，明明已经有internet，却规定每天只能在两点到四点使用。之后还要去走廊尽头的library查书，大家会觉得不可接受。工具一旦成为日常基础设施，就很难退回去。

**Elad Gil：** 哪些部分还没有成熟到可以完全交给AI？

**Rene Haas：** RTL generation、physical design和implementation仍然有明显限制。模型主要基于公开可用的信息训练，而芯片公司最有价值的设计资料通常是proprietary。不过Arm的优势是，我们不仅有丰富的IP，还有documentation、test benches和使用这些IP的完整方法。

**Rene Haas：** 有些公司说自己的IP很有价值，但拿到手后没有文档、没有解释、没有测试方法。不可用、不可测试的IP，也就不可用于训练AI。Arm已经积累了这些材料，所以我们正在和model makers合作，探索怎样把专有工程知识更好地用于工具训练。

**Sarah Guo：** 假如把时间拉到两三年后，芯片设计周期会从24到36个月缩短到一年、六个月，还是变化没有那么大？

**Rene Haas：** 我不确定两三年内会发生什么，但五年以上的时间尺度上，对于某些更直接的设计，从想法到GDS2 file可能真的会大幅加速。GDS2 file就是最终送到fab制造的文件。AI可能同时压缩设计和verification的时间。

**Rene Haas：** 但如果你让工具一次性设计一个比Verano快10%、比Rubin便宜20%、在某个模型上效率高30%的芯片，它不会简单到按一下按钮就完成。目标、约束和验证都很复杂。不过五到十年后，芯片设计方式大概率会非常不同。

**Elad Gil：** 现在越来越多公司想做自己的AI chip，客户从Vera、Graviton到各种新公司都使用Arm。客户数量分散，对Arm意味着什么？

**Rene Haas：** 这总体是好事，但关键在于供应链能力。年轻公司可以有优秀的AI chip设计，拿到很多融资，却仍然需要memory vendors、substrate vendors、先进制程和advanced packaging。它们不仅要拿到3-nanometer或16-nanometer产能，还要拿到合适的封装和各种配套资源。

**Rene Haas：** 我认为这种受限环境至少还会持续三到五年。只要Transformer仍然是生成和推理AI的主要计算单元，系统就会非常compute-intensive、memory-intensive。瓶颈会从packaging转向memory，再转向data center buildout，可能是层层传递，而不是某一个环节突然彻底解决。

**Sarah Guo：** data center建设会成为下一个瓶颈吗？

**Rene Haas：** 很可能。现在很多项目没有按期完成，也没有像预想那样少用labor。再加上美国不同地区出现限制data center建设的政治和社区讨论，基础设施建设可能成为headwind。即使wafer和memory产能增加，能源、许可、施工、冷却和连接都需要时间。

**Rene Haas：** 这不代表AI需求接近饱和。我经常被问AI bubble什么时候结束。如果说的是估值泡沫，那是股票市场的问题；如果说供给是否已经超过需求，我认为远远没有。模型的工作方式决定了需求仍然非常强，只是需求会受到基础设施、资本和建设速度的约束。

**Elad Gil：** 你如何看待SoftBank对资本和生态的使用？

**Rene Haas：** Arm有一个很大的单一股东SoftBank，这带来很多可以共同推进的事情。对年轻公司来说，我的建议是尽早建立strategic partnerships，不要只依赖单一客户或单一融资渠道。伙伴可以来自supply chain、private equity、银行或产业公司。

**Rene Haas：** 半导体startup重新得到投资者关注，但资本需求非常巨大，access to capital可能决定它能不能活下来。公司需要更有创造力地使用生态关系。SoftBank也会观察那些可以被纳入portfolio、并且能获得资源帮助的公司。SoftBank近期宣布SoftBank Neo，目标是成为neocloud，这可能为拥有芯片技术但还难以获得Microsoft或Google design win的年轻公司提供另一个落点。

**Sarah Guo：** 你在SoftBank Group International负责哪些业务？

**Rene Haas：** SoftBank Group在日本由Masa领导，下面有很多operating companies，包括SoftBank Corp和mobile业务，也有SoftBank Vision Fund以及SoftBank Group International的投资活动。Masa公开谈到的重点包括robotics、OpenAI、infrastructure和Arm。我会参与许多相关讨论，帮助形成策略，更重要的是推动执行。

**Rene Haas：** 我目前关注Ampere、Graphcore和Stack AV等公司。Stack AV涉及autonomous systems。更准确地说，我不仅关注Arm本身，也会参与SoftBank生态中很多关于robotics、energy、data center infrastructure和AI的讨论。

**Elad Gil：** 这种生态视角怎样改变Arm？

**Rene Haas：** 它让我们从更高的位置看到infrastructure、capital和energy，也可能为Arm产品找到应用场景。SoftBank参与robotics、energy和data center infrastructure，而Arm的CPU和其他产品可能在这些领域发挥作用。这不一定意味着Arm会进入广泛的merchant chip business，也可能只是为SoftBank生态做特定产品。

**Sarah Guo：** robotics现在还在早期。你怎么看市场的机会？

**Rene Haas：** 无论是humanoid，还是可以重新训练、执行特定任务的专用机器，市场都可能很大。过去的robotics更像robotics 1.0，每条生产线都有为特定任务设计的机械结构和软件。换一条汽车生产线，旧机器人可能就无法继续使用，改造成本很高。

**Rene Haas：** 如果机器人可以通过训练和观察学习，又有足够general-purpose的机械结构，再加上成本下降，能做的事情会非常多。construction、infrastructure、service和security都可能采用。机器人体育比赛也许有爱好者观看，但更大的价值在于替代或增强大量human labor tasks。

**Elad Gil：** humanoid和task-specific form factor，哪一种会赢？

**Rene Haas：** 两者都会存在。很多工作环境是按六英尺高的人、固定的手臂长度和现有工具设计的，所以humanoid可以直接进入这些空间。但有些任务没有必要复制人类形状，专用机器人更高效。真正关键的是机器人是否足够smart、能否学习，以及成本和business model能否成立。

**Rene Haas：** Arm在robotics里会非常普遍。我们在real-time sensing和microprocessor方面有丰富技术，可以把芯片放在机器人手指等末端，用于perception和sensing。今天许多humanoid的“大脑”已经运行在Arm架构上，Nvidia和Qualcomm参与的方案也是如此。

**Sarah Guo：** 哪些robotics应用可能最早落地？

**Rene Haas：** 现在还早，因为business model尚未完全确定。机器人的购买成本很高，企业会问它到底能否替代工作、多久回本。汽车、部分surgical robots、distribution centers是较明确的应用。factory automation、delivery和distribution很可能较早实现自动化，甚至一辆autonomous truck也可以被看作某种robot。

**Elad Gil：** 如何看待芯片、robotics和data center相关的政策限制与export controls？

**Rene Haas：** 我以美国公民和半导体从业者的身份回答。Arm是全球公司，总部在英国，员工大约30%在美国、40%在英国、30%在亚洲，但美国市场对我们非常重要。我记得1980年代美国曾经是半导体领导者，Japan Inc.在memory价格和市场份额上变得很强，美国后来推动Semitech，加强本土半导体产业。我认为当时的方向是正确的。

**Rene Haas：** 后来internet和SaaS变成热点，很多人忘记semiconductors是战略资产。美国需要更多本土fabs，这既关系到national security，也关系到supply chain diversification。Intel、Micron以及其他制造能力对美国很重要。英国规模小一些，但保持关键技术能力同样有价值。

**Rene Haas：** 至于export controls，我不认为这是一场简单的“谁赢得比赛”。技术是一个infinite game，不会有某一天宣布唯一赢家。真正危险的是，如果关键技术全部转移到美国之外，那既不利于经济，也不利于安全。一个国家要保持创新和生态领先，就必须让产业链的一部分留在本土。

**Sarah Guo：** 有些人反对data center，担心它们不创造工作，或者会消耗社区资源。

**Rene Haas：** 我不认为“data center没有工作”是正确的。人们看到一个像Costco仓库的大盒子，里面没有很多人，就以为它不会创造就业。但data center需要energy、liquid cooling、施工、电气、网络、维护和设备供应链。electrician是高度熟练、需要培训和认证的工作，行业非常需要他们。

**Rene Haas：** 反对声一部分来自对AI失业的恐惧。很多人的工资没有明显增加，看到AI又担心自己的机会减少，于是data center成了所有焦虑的靶子。社区和行业应该更好地沟通真实的资源消耗和就业影响，但不能因为恐惧就假设技术只会带来坏处。

**Rene Haas：** 从smartphone、internet到personal computer，成为技术领导者没有根本性坏处。确实会有二阶、三阶影响，需要治理，但成为落后者意味着别人会替你写规则。数据中心、能源、冷却和芯片产业如果在本土发展，会形成类似1950年代Detroit汽车生态那样的供应商网络和技能体系。

**Elad Gil：** 回到Arm，未来一两年什么最让你兴奋？

**Rene Haas：** 我很幸运Arm处在这些变化的中心。AI需要compute，而Arm擅长power-efficient compute。过去我会纠结下一个产品是不是另一款tablet、屏幕是8.9英寸还是9.2英寸；现在AI带来的工作负载变化创造了大量创新机会。我们可以参与生态，帮助领先公司开发产品，也能从广泛的市场中看到需求变化。

**Sarah Guo：** 许多人在accelerator之外低估了CPU。你怎么看CPU在AI时代的机会？

**Rene Haas：** 所有计算问题都使用或可以使用microprocessor。CPU是整个系统的核心，负责orchestration、arbitration和decision，决定token往哪里走。过去ChatGPT带来accelerator热潮时，人们好像认为任何问题的答案都是accelerator，但accelerator生产token以后，需要CPU来组织、调度和把token交给用户。

**Rene Haas：** 训练很重要，也会涉及recursive learning和reinforcement learning；但越来越多数据和工作会进入inference。Inference过程中，系统要处理信息、安排调用、管理软件和决定下一步。CPU不会因为accelerator变强就消失，它和accelerator、memory一起构成完整系统。

**Rene Haas：** 这不仅适用于data center，也适用于汽车、robot、phone和wearables。在edge device里，CPU本来就是table stakes，还要在有限功耗下完成更多AI处理。你不能把一个50-watt GPU戴在头上，所以很多AI能力需要在本地、低功耗地运行，这正是Arm架构的优势。

**Elad Gil：** 工作负载变化会怎样影响芯片产业？

**Rene Haas：** 未来几年会同时出现更多data center CPU、edge CPU、agent sandbox以及运行现有software和API tools的设备。芯片需求来自工作负载的持续变化，而不是只来自某一个模型。只要有人在做新的AI应用、robotics和基础设施，就会需要不同类型的compute。

**Rene Haas：** 最终我认为，CPU、accelerator和memory都要协同设计。token factory可以不断生成token，但必须有“卡车”把token运走、交给使用者。CPU就是承担这一类系统组织工作的核心。Arm的机会在于，我们的架构既覆盖data center，也覆盖边缘设备和未来机器人。

**Elad Gil：** 你刚才说供应链能力会成为芯片公司的新肌肉。对于一个只擅长设计的创业团队，最容易低估的环节是什么？

**Rene Haas：** 它们常常先想到架构和演示结果，却没有把量产路径放进最早的计划。你需要提前和晶圆厂讨论产能，和memory供应商讨论分配，和substrate以及封装供应商确认规格，还要知道什么时间可以拿到样品、什么时候完成验证、什么时候能够稳定出货。只要其中一个环节没有排上，优秀设计也可能停在实验室里。

**Rene Haas：** 资本也不是简单地“有钱就够”。资本必须在正确的时间到位，才能支付工程团队、验证设备、晶圆、封装和库存。公司还要管理客户承诺与实际订单之间的时间差。如果没有清楚的客户需求、供应链伙伴和现金流计划，融资额越大，错误也可能被放大得越快。

**Sarah Guo：** 所以你认为创业者要更早把产业伙伴纳入公司，而不是等设计完成后再找供应链？

**Rene Haas：** 是的。战略伙伴关系应该尽早建立。它可以是晶圆厂、memory供应商、封装厂、银行、私募基金，也可以是能够提供真实产品验证场景的客户。半导体的设计周期和投入都很长，不能把供应链当作最后一步采购。伙伴越早参与，越可能一起解决规格、产能和交付的问题。

**Elad Gil：** Arm做实体芯片后，内部怎样判断哪些事情自己做，哪些事情留给生态伙伴？

**Rene Haas：** 我们不会因为能做一件事，就把所有事情都自己做。Arm最强的基础仍然是架构、IP、软件生态和能效。对于某些客户来说，完整的CPU产品可以帮助它们更快得到结果；但这不意味着我们要覆盖所有芯片品类。我们要判断客户真正缺什么，以及哪一段工作能让整个生态更快交付。

**Rene Haas：** Meta的案例说明，有时客户需要的不是更多一块IP，而是一个可以直接投入系统的通用CPU。这个产品需要和客户共同定义，也需要Arm承担物料、验证和交付责任。只要边界清楚，实体产品可以扩大IP的价值，而不是破坏客户关系。

**Sarah Guo：** 你提到Arm的文档和测试资产很重要。为什么它们对AI工具特别关键？

**Rene Haas：** 因为AI工具不能只学习一个抽象的设计结果，还要学习为什么这样设计、如何使用、怎样验证以及出现错误时怎么定位。没有说明文档的IP就像没有接口说明的零件，模型不知道输入输出、边界条件和失败模式。没有test bench，模型也无法判断自己生成的结果是否正确。

**Rene Haas：** Arm长期维护IP、文档、测试和开发流程，这些资产形成了可以用于训练和验证的材料。随着模型制造商和芯片公司的合作加深，AI可能从辅助工程师查资料，进一步参与验证、调试、生成代码和安排测试。但最终仍然需要工程师对设计负责，尤其是在安全、功耗、时序和量产条件上。

**Elad Gil：** 这是不是意味着验证工程师的价值会下降？

**Rene Haas：** 更可能是工作内容变化。重复查找、生成测试、比对结果和整理文档的工作可以大量自动化，工程师就能把更多时间放在架构取舍、边界条件和系统级判断上。AI不是取消所有工程，而是让团队能在同样时间里验证更多方案。芯片制造仍然有真实的物理限制，工具不能凭空消除这些限制。

**Sarah Guo：** 当AI让更多公司可以设计芯片时，会不会反而让供应链更加拥堵？

**Rene Haas：** 这是很现实的可能性。设计门槛下降后，更多项目会争夺同样的晶圆、memory、封装、能源和data center资源。供给不可能在几个月内同步增加，所以好的想法会继续面临排队。技术创新和产业执行必须同时进步，否则设计速度越快，等待时间越长。

**Rene Haas：** 这也解释了为什么我不认为需求泡沫已经接近结束。限制需求的可能是能不能建成data center、能不能接入电力、能不能拿到先进制程和memory，而不是用户已经不需要AI。未来几年，产业竞争既是模型和芯片的竞争，也是施工、能源、冷却、网络和资本的竞争。

**Elad Gil：** 你对data center建设的看法，和很多只看到电力消耗的人不一样。你认为应当怎样讨论它？

**Rene Haas：** 要把成本和收益放在同一张表里。data center确实需要电力、水、土地和网络，也必须遵守环境与社区规则。但它同时需要电工、机械工程师、冷却系统、设备制造、维护、软件和安全服务。社区应该要求透明数据和合理规划，而不是把所有建设都当成没有就业和价值的盒子。

**Rene Haas：** 如果一个国家因为害怕争议而停止建设，需求不会消失，只会转移到别的地方。那样本地既失去产业链和工作，也失去制定规则和积累能力的机会。我的观点不是每个项目都应该批准，而是政策需要在安全、环境、能源和技术领导力之间作出有信息基础的选择。

**Sarah Guo：** 回到robotics，成本下降之前，哪些项目最可能先形成正向商业回报？

**Rene Haas：** 先看任务是否重复、环境是否相对结构化、人工成本是否高，以及机器人是否能带来连续的生产率提升。仓库分拣、工厂搬运、配送和部分汽车生产线符合这些条件。手术机器人和专业设备也可能继续增长，但它们需要更高的可靠性和认证。泛化能力很有吸引力，可是企业最后仍然要问每小时产出、维护成本和投资回收时间。

**Rene Haas：** Humanoid的优势是能使用已经为人设计的空间和工具，专用机器人的优势是可以围绕一个任务做到更低成本。两者不会互相排斥。真正决定采用速度的，是软件能否让机器人适应变化，硬件能否稳定工作，以及整个方案是否比人工或传统自动化更划算。

**Elad Gil：** Arm在这些机器人系统里，除了主CPU，还有哪些位置？

**Rene Haas：** 机器人需要中央计算，也需要分布在手指、关节、摄像头和传感器附近的实时处理。末端设备必须快速感知触碰、压力、位置和环境，不能每个信号都先传到远处再回来。Arm在低功耗微处理器、实时系统和广泛软件生态方面有基础，因此可以从“大脑”一直延伸到各个传感节点。

**Rene Haas：** 未来机器人会同时使用CPU、accelerator和memory。CPU负责协调任务和控制系统，accelerator负责特定模型，memory保存上下文和状态。一个机器人要走路、看东西、抓取、规划并和人协作，不能只看某一块芯片的峰值速度，要看全系统的功耗、延迟、可靠性和成本。

**Sarah Guo：** 这似乎也是你为什么反复强调CPU。AI讨论容易只看生成token的加速器。

**Rene Haas：** 正是如此。accelerator很重要，但它只是系统的一部分。大量token生成以后，系统要把它们放进正确的上下文，决定调用哪个工具，管理内存，回应用户，再把结果交给下一步。CPU负责很多编排和仲裁工作。只要计算系统还需要组织信息，CPU就仍然是基础设施。

**Rene Haas：** 在data center里，CPU连接accelerator、memory和网络；在汽车里，CPU处理控制和感知；在手机、wearables和机器人里，它还要在严格功耗约束下完成本地推理。边缘设备不可能把所有数据都送到远端，所以低功耗和高效率会越来越重要。这是Arm长期积累的能力，也是AI时代仍然有价值的原因。

**Elad Gil：** 听起来你对Arm未来的判断，不是押注一个单独的AI产品，而是押注计算系统会继续扩张。

**Rene Haas：** 我更愿意这样表达。我们不需要猜某个设备最终会长什么样，但可以观察所有设备都需要计算、软件和能效。新的工作负载会不断出现，芯片会进入新的场景，Arm可以凭借架构、IP、生态和能效参与其中。机会很多，但我们仍要尊重供应链、客户边界和交付现实。

**节目片尾：** 感谢收听《No Priors》。欢迎在No Priors网站查找每期节目的transcript，也可以在YouTube、Apple Podcasts、Spotify等平台订阅节目。
