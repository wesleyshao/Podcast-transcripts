---
访谈时间: "2026-08-11"
访谈时间说明: "未确认独立录制日期，使用 YouTube 发布时间 2026-08-11。"
嘉宾名字: "Gabe Pereyra"
嘉宾公司名称: "Harvey"
参与嘉宾:
  - 姓名: "Gabe Pereyra"
    公司或机构: "Harvey"
    职务: "联合创始人；总裁"
播客名称: "Sequoia Capital"
播客url地址: "https://www.youtube.com/watch?v=MGouk8W51v0"
youtube_video_id: "MGouk8W51v0"
全文提及的关键名词:
  - "Gabe Pereyra"
  - "Harvey"
  - "LegalAgentBench"
  - "contracting dataset"
  - "diligence dataset"
  - "RL environment"
  - "synthetic data"
  - "domain experts"
  - "Mercor"
  - "Snorkel"
  - "LangChain"
  - "post-training"
  - "open-source models"
  - "model routing"
  - "model serving"
  - "evaluation"
  - "continual learning"
  - "enterprise search"
  - "legal technology"
文字稿来源: "YouTube public subtitles: en-orig；完整源文本位于 caption_cache/MGouk8W51v0.en-orig.source.txt；官方 Podcast RSS 未提供满足条件的同期公开完整 transcript。"
YouTube发布时间: "2026-08-11T13:00:13Z"
字幕来源: "YouTube public subtitles: en-orig"
companies:
  - Mercor
industries: []
technologies:
  - 后训练
  - 开源模型
keywords:
  - 开源
tags:
  - Mercor
  - 后训练
  - 开源模型
  - 开源
---

# How Harvey Built a Research Lab on a Budget ｜ Gabe Pereyra

## Transcript

Gabe Pereyra：并保护客户数据。

Gabe Pereyra：并始终以生产结果检验研究。

Gabe Pereyra：从窄领域开始，再逐步扩大。

Gabe Pereyra：这是应用层公司建立研究能力的现实起点。

Gabe Pereyra：这条路径必须同时尊重真实工作、客户隐私和模型能力的边界。

Gabe Pereyra：真正的目标是让每个领域客户都能拥有更贴合自己工作的 AI 系统。

Gabe Pereyra：每一步都要有清晰的边界和反馈，才能把研究投入转化为产品能力，而不是转化为脱离客户的演示。

Gabe Pereyra：这也意味着研究实验室不应被理解为只属于大公司的一栋楼，而是一套能力组合：领域知识、数据生成、训练方法、模型服务、评估门禁和生产反馈。应用层团队可以先从最窄、最真实的工作开始，再随着产品使用扩大研究范围。

Gabe Pereyra：这个 playbook 的关键不是某一家公司、某一种模型或某一个供应商，而是把研究链条拆成可以复用的模块。先定义真实任务，再构造可验证的数据；先建立评估和服务基础设施，再决定哪些能力值得 post-training；先用简单的开源替换和 routing 积累生产经验，再把更复杂的模型放进系统。这样应用层公司即使没有无限预算，也能在自己的垂直领域逐步获得 frontier 级的能力。

主持人：接下来我们很荣幸邀请 Gabe Pereyra。Gabe 是 Harvey 的联合创始人和总裁，之前曾在 DeepMind 担任研究科学家，也曾在 Meta 工作。后来，他把 GPT-3 展示给大学室友，两人一起创办了 Harvey。现场很多人都是应用层公司，正在思考怎样开始自己的研究、怎样对模型做 post-training，以及怎样建立自己的研究实验室。Harvey 已经走出了一个很有代表性的路径。今天 Gabe 会讲述 Harvey Labs 是怎样建立起来的。

Gabe Pereyra：这场分享也可以叫作《如何用有限预算建立研究实验室》。如果你是一家应用层公司，想和 frontier labs 竞争，这是一场不公平的比赛。前沿实验室有更多资金、人才、计算基础设施和数据。应用层公司不可能简单复制它们的投入，所以问题是，怎样使用 frontier ecosystem 来竞争。

Gabe Pereyra：Harvey 创办四年前，今天很多基础模型公司还不存在，或者刚刚开始。那时我们要么自己搭建很多东西，要么把注意力放在不同的方向，例如建设 go-to-market 组织和优秀产品。现在情况改变了。应用层公司可以借助前沿生态，获得接近 frontier intelligence 的能力。今天我会讲四件事：怎样建立 benchmark 和训练数据，怎样和 neo labs 合作做 post-training，怎样把这些模型部署进生产，以及怎样从生产反馈中形成循环。

### 先建立 benchmark，再考虑训练

Gabe Pereyra：第一步是建立 benchmark。如果没有好的 benchmark，就无法知道模型训练得好不好；如果无法训练，就没有理由考虑把模型部署到生产环境。今年 Harvey 发布了三套数据集。第一套是 LegalAgentBench，它把大型律所中 associate 会做的工作整理成一套任务分类，覆盖多个业务领域，包括复杂的基金设立文件起草、判例研究等。

Gabe Pereyra：第二套是 contracting dataset，用来训练 agent 像公司内部法务团队一样参与合同谈判。第三套也是我最兴奋的一套，是大型 diligence dataset。它可以被看作一个很大的 RL environment，最大的 data room 包含约 8,000 万个 token，可以用来研究长上下文和复杂任务。这里最值得讨论的不是数据集名称，而是我们怎样构建它们。

### 敏感数据、领域专家与 synthetic data

Gabe Pereyra：Harvey 服务大型律所和企业，客户的法律数据非常敏感，可能涉及保密和法律特权。我们不能用客户数据训练通用模型，甚至不能把它直接放进自己的模型训练流程。因此，问题变成：在没有客户原始数据的情况下，怎样得到足够真实的数据来训练和评估产品。

Gabe Pereyra：今年开始真正有效的一种方法，是让 domain experts 指导 synthetic data generation。Brendan 曾经做过一个很好的类比：就像工程师现在不一定逐行写代码，而是通过 vibe coding 指导 coding model，领域专家也可以指导模型生成符合现实工作的训练数据。我的弟弟是一名律师，在 Harvey 工作。他很早就学会使用 coding models，也训练其他律师一起使用。这样，律师可以生成非常接近真实工作的法律数据，既能用于训练，也能用于评估产品。

Gabe Pereyra：synthetic data 不是终点，它本身未必足够好，但它提供了一个可启动的路径。接下来我们会和 Mercor、Snorkel 等公司合作，把领域专家参与的过程扩大，形成更大规模的训练集。这样做的重点不是让模型凭空编造文件，而是让懂法律的人先定义真实问题、错误类型和评价标准，再让工具扩大生成工作。

Gabe Pereyra：diligence data set 是一个很好的例子。大型并购尽调中，data room 可能有成千上万份合同、邮件和谈判材料，这些输入通常不公开。我们可以从一个 rubric 开始，先写下 data room 中要植入的关键问题，例如合同互相不一致、某份合同缺失、某些条款与其他材料不匹配。然后根据这些问题生成一套完整数据，再让 Mercor 或 Snorkel 等合作方把合同改写得更像真实文件。模型随后生成 diligence memo，我们可以检查它是否发现了预先植入的全部问题。

Gabe Pereyra：过去我们遇到的是一个鸡和蛋的问题。我们去律所说“我们可以用你们的客户数据训练模型”，律所会说“先证明模型有效”，我们又无法要求它们展示敏感数据。现在我们可以用合成 data room 和清晰的 rubric 先证明能力，再和律所讨论如何在它们自己的安全环境中继续做。这为后续合作打开了入口。

### 让 RL environment 更高效，并开放一部分数据

Gabe Pereyra：数据集变大以后，下一步是把它们转化为高效的 RL environment。评估的成本会快速上升。比如 diligence dataset 有超过 1,000 个 unit tests，用 LLM-as-a-judge 给模型输出打分。如果用最大的模型做大量 rollout，成本会非常高。因此，我们还和 LangChain 等团队合作，把环境和评估流程做得更高效。

Gabe Pereyra：当时有一个有些争议的决定，是把部分数据集 open source。理由很简单：除非有很多人实际训练和测试，否则你很难知道一个数据集到底好不好。我过去在 Google Brain 和 DeepMind 做研究时，最有价值的数据集通常是开放的，例如 ImageNet、CIFAR 和 MNIST。大家都使用它们，问题会被发现，社区会提交 pull request、提出建议。现在越来越多实验室会在发布新模型时使用我们的数据集做 benchmark。甚至 Elon Musk 转发过它，这也带来了很大关注。

Gabe Pereyra：开放数据集并不意味着所有有价值的数据都开放。公开的 synthetic data 能帮助整个生态改进，律所和企业的私有数据仍然是更重要、更敏感的部分。我们的长期价值不是把所有客户数据拿出来，而是帮助律所用自己的私有数据训练和定制系统，同时用公开的合成数据推动共同进步。

### 从预训练转向 post-training

Gabe Pereyra：benchmark 建立以后，才有了训练模型的目标。现在令人兴奋的是，open-source models 正变得越来越有竞争力。过去 post-training 的回报有限，因为基础模型的预训练能力提升太快，你刚做出的 post-training 很快就会被下一代预训练模型吸收。现在像 Kimmy 3、GLM 5.2、NeMo-Megatron、Inkling 等开源基础模型已经足够强，应用层公司可以把它们 post-train 到接近 frontier intelligence 的水平，至少在一个具体领域里具有竞争力。

Gabe Pereyra：我们建议的起点是和 neo labs 合作。它们已经有训练基础设施、recipes 和经验，可以帮助你检查训练数据是否真的有效。如果和它们合作后结果完全没有提升，通常意味着你的数据集、rubric 或环境存在问题。这是一个很好的 bootstrap 方法。

Gabe Pereyra：我们和不同的 neo labs 合作，是因为每家公司的研究下注不同。Fireworks 让我们尝试训练 GLM 5.1，并使用 Fable 或 Opus 4.8 这类模型作为 advisor model；Base10 参与了 KB compaction；Ngram 参与 enterprise search 和 firm knowledge；Trajectory 帮助训练 NeMo-Megatron 模型；Applied Compute 则参与 Vault 产品。不同伙伴有不同的研究方式，也有不同的开源模型和基础设施。我们合作得越多，学到的东西越多。

Gabe Pereyra：这不代表 Harvey 永远要把训练交给外部。随着团队扩大，我们会使用 Tinker 等 API，也会使用 Fireworks、Base10 建立的基础设施，在内部做越来越多 post-training。受 Cursor 的启发，我们希望最终形成自己的 Composer 版本，把 synthetic data、Mercor 扩展、neo labs 合作和内部研究整合成一个模型，让它和闭源模型一起服务客户。

### 生产环境中的模型服务

Gabe Pereyra：post-train 一个模型以后，真正把它服务到生产环境并不简单。很多人仍然把应用层公司想成调用单一模型 endpoint 的聊天产品，但 Harvey 在 60 个国家运营，有多个产品界面，不同客户有不同的模型偏好。我们需要服务多个 model family，并在不同 provider 之间安排 fallback，以满足 SLA。现在还可以把 open-source models 通过 Fireworks.ai 放进同一个服务矩阵。

Gabe Pereyra：模型服务基础设施应该在 post-training 之前就建立。每当一个新模型发布，无论它是开源、闭源还是 Harvey 自己 post-train 的模型，我们都要判断是否放进生产，也要判断放进去以后是否继续保留。预生产阶段先跑通用 eval，包括 LegalAgentBench 这样的实验室 benchmark，快速判断一个新模型是否达到前沿水平、在哪些法律任务上强弱不同。然后做人工 side-by-side，把它和其他模型直接比较。

Gabe Pereyra：除此以外，每一个产品界面都需要 critical user journeys 和自动化产品测试。一个模型可能在通用 benchmark 上很强，但并不适合特定产品。我们还会做 human product testing，再结合成本、延迟和地区可用性等启发式规则，决定是否部署。这个基础设施对 post-trained 和非 post-trained 模型都适用，所以不应该等到开始训练以后才建设。

Gabe Pereyra：模型上线后也要持续测试。重大变化要做 A/B test，观察用户参与度是否符合预期；还要跟踪 uptime、token efficiency，以及我半开玩笑称为“生气的客户邮件”的产品反馈。如果用户说某个模型表现奇怪，那也是生产信号。上线不是终点，生产反馈要回到数据集、评估和下一轮模型选择。

### 简单的 open-source switches 和 model routing

Gabe Pereyra：在做复杂 post-training 之前，可以先找产品里能够直接替换开源模型的地方。比如生成 citation 的部分不一定需要最大的模型，可能可以直接换成 GLM 5.2，获得成本或性能收益。这样做的价值不仅是省钱，也是在组织内部建立同时服务开源和闭源模型的肌肉记忆。

Gabe Pereyra：第二个方法是 model routing。有些任务不能简单地把闭源模型换成开源模型，但可以根据特定 query 把一部分流量路由到开源模型。这样公司逐步学会怎样控制质量、成本、延迟和 fallback，之后才有条件把更深的 post-training 放入生产飞轮。

Gabe Pereyra：生产反馈不等于直接训练客户数据。Harvey 不会因为客户使用产品，就把客户的法律材料直接拿去训练通用模型。我们可以从用户测试和其他安全反馈中学习哪些能力需要改进、哪些任务值得构建数据集，但必须保护客户信息和法律特权。

### 研究实验室的全流程和开放问题

Gabe Pereyra：最终的循环是：领域专家定义问题，构建 synthetic data，扩展数据生成，形成高效环境，和 neo labs 做 post-training，把模型放进 serving infrastructure，然后用评估和安全的生产反馈推动下一次数据建设。我认为未来每家公司都会需要成为某种意义上的 AI company，并建立自己的版本。

Gabe Pereyra：目前最大的难题之一，是合成数据的分布和生产数据仍然不完全一致。我们可以生成非常真实的 diligence data room，但 Harvey 的产品并不只用于尽调。模型在 diligence benchmark 上表现好，不代表它在用户让它起草一封邮件时也同样好。因为我们不能直接查看客户数据，所以如何弥合这个分布差距，是数据集方面最重要的开放问题之一。

Gabe Pereyra：另一个问题是超长上下文。最大的 diligence data room 有 8,000 万个 token，现有模型还不擅长在如此复杂的环境中管理上下文。我们需要训练模型选择相关材料、保持中间状态、处理长链任务，而不是简单把更多文本塞进 context window。

Gabe Pereyra：第三个问题是 continual learning。我们的终点不是做出一个“最好的法律模型”，而是帮助每个律所和企业把系统定制到自己正在做的工作。理想状态是，一个大型律所完成每个 client matter 后，AI 系统都能变得更好，同时仍然保护客户数据。这既是技术问题，也是运营、权限和数据治理问题。

### Q&A：如何生成真实的法律数据

听众：大型律所的客户数据非常敏感。你能不能更具体地解释，律师怎样通过 live coding 的方式生成训练数据？

Gabe Pereyra：比如一家大型律所代表客户做并购，律所会拿到被收购公司的 data room，包括大量合同、邮件和谈判会议材料。这些输入都不公开，公开的可能只有最终 purchase agreement，却没有生成它所需要的全部输入。过去让很多律师“做一个假的 data room”很困难，因为它可能有 10,000 份合同，而且每份合同要彼此一致。

Gabe Pereyra：我们的做法是先从 rubric 开始。先写清楚 data room 里要植入哪些问题、在什么场景下检查哪些错误。比如某几份合同不能互相对应、某一份文件故意缺失、某些条款和其他材料不一致。然后根据 rubric 自动生成完整材料，再让领域专家和合作方把文件改得足够真实。模型最后生成 diligence memo，我们检查它有没有发现预先植入的问题。这样不用暴露客户输入，也能建立一套可验证的训练和评估环境。

### Q&A：人才、基础设施与研究能力

听众：应用层公司很难和 Anthropic 等实验室竞争研究人才。你会坚持招 frontier researcher，还是招领域专家和律师？

Gabe Pereyra：这是我早期犯过的错误。我过去在实验室工作，认识很多研究者，曾经邀请他们加入 Harvey，但他们拿到的是一亿美元级别的 package，而公司当时还没有达到能承担这种成本的规模。现在公司更大，我们已经不是在和 frontier labs 的全部人才正面竞争。越来越多博士并不想去大型实验室，也有很多人希望把研究落到具体领域，这扩大了人才池。

Gabe Pereyra：早期研究人才之所以稀缺，不只是因为他们会做 post-training，还因为公司必须自己建设训练、服务和实验基础设施。现在有 Fireworks、Tinker 这类 API 和服务，可以把基础设施的一部分外包或标准化，因此不需要每个研究员都同时是训练系统和 serving 系统的专家。这让领域专家、产品研究者和更多应用型研究人才有机会参与。

### Q&A：如何让 benchmark 挑战 frontier model

听众：领域专家不一定知道模型的弱点，怎样让 rubric 真正区分 frontier model？

Gabe Pereyra：我们的重点不是为了打败模型而编造不现实的题，而是让任务成为客户真实面对的工作。法律领域很适合这样做，因为顶级律所正在处理的真实复杂问题，现有 frontier model 仍然不能稳定完成。我的弟弟是 Harvey 最早的员工之一，他已经和模型工作了四年，对模型行为和数据生成有很强直觉，也训练其他律师使用这些工具。但我们首先仍然要求数据 room 和 rubric 真实，运行模型后再看哪里存在能力缺口。

### Q&A：问题究竟出在数据、研究还是基础设施

听众：从数据生成、环境、算法研究到基础设施，项目不工作时通常是哪一层出了问题？

Gabe Pereyra：没有单一答案。Harvey 能更容易调试，是因为我们先有了 product-market fit，有一个已经在生产环境中被使用多年的产品。早期我们主要使用闭源模型，因此先建立了产品、服务、监控和客户反馈的全流程。后来我们把一个 post-trained model 当成又一个新模型，放进同样的系统中测试，而不是把它当成特殊对象。

Gabe Pereyra：不同阶段有不同 gate。如果模型在 benchmark 上不行，通常不会进入下一步；如果 benchmark 好，但放进产品后用户觉得奇怪，就说明它可能过拟合了 benchmark，或者在分布外任务上失败。所有阶段都要有评估、生产测试和反馈。post-training 只是更大系统中的一个输入，而不是整个系统本身。

### Q&A：为什么开放 benchmark

听众：开放 benchmark 会让实验室反复优化它，但不开源又无法证明它真实。你们怎样权衡？

Gabe Pereyra：在开放之前，我们已经和实验室密切合作，分享数据帮助它们改进模型，而模型变好也会反过来改善我们的产品。法律行业的一个价值是帮助客户理解不同模型在不同任务上的能力。我们早期曾以为只要造出一个最好的模型，客户就会满意，但现实是不同客户有不同偏好，不同模型在不同任务上有不同优势。

Gabe Pereyra：开放数据集还让我们能和更大的 frontier ecosystem 合作。以前有公司来问新技术，我们没有足够 bandwidth 逐一测试。现在可以让它们先在开放数据集上试，如果效果好，再决定是否投入更多资源。真正有价值、涉及客户私有工作的数据仍然要留在安全边界内，开放和保密之间需要平衡。

### Q&A：产品方向和组织级生产力

听众：Harvey 如何与更通用的云端协作产品竞争？

Gabe Pereyra：我们最初的产品和许多通用工作工具，更多关注 individual productivity。现在我们越来越关注 organizational productivity。大型律所的问题不是如何让某个律师单独写得快一点，而是它有 10,000 个客户、成千上万个项目，需要让项目按时、合规并且有利润地完成。

Gabe Pereyra：一个 client project 可能持续六个月，由律所内外的 20 到 30 个人共同参与。核心难点不只是起草一个段落，而是协调人员、客户、外部机构和 agent，让所有工作在同一个项目里推进。因此，我们的基础设施越来越像项目管理，负责编排人和 agent。在组织层面，还要处理资源分配、计费、客户 pitch 和多个项目之间的容量规划。对 Fortune 500 企业来说，它们可能同时和上千家律所合作，内部也有上千名人员，系统协调更复杂。

Gabe Pereyra：应用层公司很难在横向能力上和 frontier labs 竞争，但可以在垂直领域深入。深度理解行业流程、构建真实 benchmark、保护私有数据、把模型放入具体工作机器，这正是通用产品不容易做到的地方。Harvey 的方向是围绕法律和企业工作流做深，而不是试图在所有领域都做一个通用模型。

Gabe Pereyra：谢谢大家。我的核心观点是，应用层公司不必因为没有 frontier lab 的预算就放弃研究。你可以用领域专家生成高质量 synthetic data，用公开 benchmark 和社区验证数据，用 neo labs 和标准化基础设施完成 post-training，再用自己的 serving、评估和生产反馈把模型变成真正可用的产品。只要我们用更少的预算和更合适的团队赢下来，就会改变游戏规则。
