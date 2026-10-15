---
访谈时间: 2026-08-06
访谈时间说明: "无法确认独立录制日期，使用 YouTube 发布时间。"
YouTube发布时间: "2026-08-06T12:39:30Z"
嘉宾名字: "Mitchell Troyanovsky；Matt Turck"
嘉宾公司名称: "Basis；FirstMark Capital"
参与嘉宾:
  - 姓名: "Mitchell Troyanovsky"
    公司或机构: "Basis"
    职务: "联合创始人"
  - 姓名: "Matt Turck"
    公司或机构: "FirstMark Capital"
    职务: "General Partner、The MAD Podcast 主持人"
播客名称: "The MAD Podcast with Matt Turck"
播客标题: "How to Build Autonomous, Long-Horizon AI Agents | Basis"
播客url地址: "https://www.youtube.com/watch?v=54pwkcp48Lg"
全文提及的关键名词:
  - "Basis"
  - "long-horizon agent"
  - "autonomous agent"
  - "ReAct"
  - "AutoGPT"
  - "BabyAGI"
  - "Claude Opus 3"
  - "OpenAI o1"
  - "OpenAI o3"
  - "RLVR"
  - "process supervision"
  - "outcome reward"
  - "verifiable reward"
  - "behavior spec"
  - "judge-as-agent"
  - "runtime training data"
  - "context engineering"
  - "ontology"
  - "canonical documentation"
  - "Language Architect"
  - "deployed intelligence"
  - "reinforcement learning"
  - "Bitter Lesson"
  - "Braintrust"
  - "tax return"
  - "Form 1065"
youtube_video_id: "54pwkcp48Lg"
字幕来源: "YouTube en-orig 原始字幕，结合完整上下文转写为简体中文"
原始语言: "English"
转写说明: "完整读取原始字幕后按上下文转写；对自动字幕中的同音词和产品名结合节目说明校正，保留完整技术论证、限定条件与反例。"
companies:
  - OpenAI
  - Anthropic
industries: []
technologies:
  - Agent
  - LLM
  - 强化学习
  - 推理
keywords: []
tags:
  - OpenAI
  - Anthropic
  - Agent
  - LLM
  - 强化学习
  - 推理
---

# How to Build Autonomous, Long-Horizon AI Agents | Basis

## Transcript

【冷开场】

**Mitchell Troyanovsky：** 人类早已习惯与非确定性系统合作，只是过去那些系统通常是同事，而不是计算机。公司和流程的很多设计，本质上都在解决同一个问题：怎样让多个非确定性主体协调行动、共同完成任务。一旦意识到这一点，你会发现它与 agent design 非常相似。

假设你有 100 个 eval，全部通过，看起来很好。你能因此确信系统在真实生产环境中也能泛化吗？我们的答案是否定的。哪怕一个人连续 100 次给出正确答案，如果他只是从 Wikipedia 抄来的，会计师事务所也不会录用他，同样也不应该录用我们的 agent。

我还看到很多人会因为代码文件没有正确抽象而抓狂，自己的 context 却一团糟。实际上，English context 更珍贵，因为 English 会直接影响运行性能，而代码的组织方式在逻辑不变时并不会改变模型性能。

【节目开场】

**Matt Turck：** 大家好，我是 Matt，欢迎收听 The MAD Podcast。所有人都在构建 AI agents，但在 coding 以外，大多数 agent 仍不能可靠地完成真实工作。今天的嘉宾正处在解决这个问题的前沿。

Mitchell Troyanovsky 是 Basis 联合创始人。Basis 已成为一家 unicorn AI company，其 agents 可以自主运行数小时，有时甚至数天，并已经能够端到端完成整份复杂 tax return。这是一场关于如何构建 long-horizon autonomous agents 的参考型对话。Mitch 会分享大量亲自踩过坑后总结出的经验。下面开始这场对话。

## 为什么 Basis 工程师对着麦克风低声说话

**Matt Turck：** 我准备节目时看到 The Information 的 Stephanie Palazzolo 拍的一段视频。她走进 Basis 办公室，发现很多人都在非常小声地对着麦克风说话。对最前沿的 AI builders 或者时时刻刻盯着 X 的人来说，这也许不新鲜，但绝大多数人并不知道你们在做什么。请解释一下，为什么大家都对着麦克风低声说话？

**Mitchell Troyanovsky：** 关于 agent，甚至关于所有 AI 工具，我能给出的最好建议之一，是尽可能多地提供 context。因为按照定义，AI 总会在某些方面缺少 context。

说话比写字快得多。写东西时，你其实是在努力把脑中大量杂乱想法先压缩成摘要，所以很耗时间。人与人之间需要这样做，因为如果有人不加整理地说一大段，再把原始录音当作 Slack DM 发给你，会显得很失礼。但 agent 不介意，甚至更喜欢原始、丰富的信息。

因此，把自己的思路直接低声说出来会高效得多。你又不想在办公室里大喊，于是现在有一些麦克风，可以在你声音非常小的时候仍保持完整清晰度。新员工刚进公司时会觉得有点怪，但一个月后就再也回不去了。

**Matt Turck：** 你们是对 Cursor 说，还是对什么工具说？

**Mitchell Troyanovsky：** 大家用的工具不同，可以是 Codex、Claude、Cursor 或其他工具，而且不仅限于 engineering。任何职能，只要你想完成工作、描述需求，就可以这样做。

## Basis 为什么选择会计

**Matt Turck：** 今天我希望围绕 long-horizon agent 做一场参考型对话。一部分依据来自你在 X 上写的长帖，更重要的是你们刚刚与 Braintrust 合作发布的开源项目。正式进入技术前，先用两三句话介绍 Basis。

**Mitchell Troyanovsky：** Basis 构建能够端到端完成会计工作的 agents。会计很难，它不是纯粹的 text-in、text-out。AI 必须在很长时间里执行大量动作，并在全过程中保持一致，最终才可能得到可靠结果。因此，我们一直专注于怎样构建能够扩展到真实会计工作的 agent。

**Matt Turck：** 你是因为 agent 技术问题有趣才选择会计，还是先选择会计，再遇到 agent 问题？

**Mitchell Troyanovsky：** 大概是后者，但会计从 agent 视角看确实非常有意思。它是美国规模最大，甚至可能就是最大的 knowledge-work profession 之一。美国会计相关从业者合计超过 300 万人。

更有意思的是，多数人从未认真想过会计为什么存在。让我用 30 秒解释一下它为何重要。现实世界每时每刻都在发生大量经济活动。比如我刚才喝了一瓶水，装瓶公司曾决定向哪家工厂或供应商采购，是否新开门店，是否招聘销售人员。这些都是建立在理解现实世界之上的经济决策。

现实中，资金易手、合同签署、库存交付，各类事件不断发生。现代资本主义依赖很多主体根据这些事件做决定：公司的 CEO、决定征多少税的 IRS、决定是否放贷的银行，以及投资者。所有人都关心真实世界，却无法直接理解它，因为现实规模太大，而且包含海量非结构化、难以解析的信息。

会计就是把这一切压缩成结构化信息的艺术，让人们能够阅读、理解并据此决策。从更抽象的角度说，会计像是覆盖整个经济系统的一层 intelligence，因为它的核心工作就是压缩现实中存在的全部信息。这是一个非常酷的问题。

## 什么是 long-horizon agent

**Matt Turck：** “long horizon”的边界一直在变化。今天什么样的任务才算 long horizon？

**Mitchell Troyanovsky：** 我先给 agent 一个简短定义。agent 是一次 AI inference，它获得一定 agency，可以自行决定采取哪些动作。agency 天然是一条连续光谱，因为可行动程度取决于你把它放进什么环境、给它什么约束。

long horizon 同样是一条光谱。你允许 agent 作出更多决定，从而在更长时间里维持 coherence。比如让 agent 查询天气，它也可能算 agent，因为它能决定调用哪个工具、输入什么 Google search，但任务很短，不需要长时间保持一致。

如果让 agent 在 repo 中实现一整项 feature，或者制作一个大型 Excel workbook，运行时间就可能从一分钟扩展到 10 分钟、20 分钟、30 分钟，甚至更久。一旦进入这个尺度，就会撞上 LLM 的基本限制。

我常说，LM 拥有非常大的 working memory，但默认没有真正的 short-term memory 或 long-term memory。你必须利用它工作记忆强大的优点，弥补它没有持续记忆的缺点。harness 和其他技术进展，就是为了让模型跨越更长时间仍保持 coherence。当任务超过单个 working-memory 范围，构建者必须主动解决一致性问题时，我会称之为 long horizon。

## 一份 tax return 如何由 agent 自主完成

**Matt Turck：** 我们这里讨论的是 autonomous agent。Basis 已能让 agent 端到端处理 tax return。请从高层解释任务包括哪些步骤，以及“自主”具体意味着什么。

**Mitchell Troyanovsky：** 以复杂的 Form 1065 为例。开始时，你可能拿到公司不同的 K-1、W-2、1099、K-3 和其他文件，也可能已经有 trial balance，或者账簿还没有完成。agent 必须根据这些材料决定怎样推进、哪些事情可以完成。

这立刻会涉及“好的做法是什么”。怎样得到可靠的 trial balance？怎样正确提取 K-1 和 K-3，才足以对结果有信心？自主意味着 agent 不会不断回头问用户：“这个对吗？那个对吗？我还缺这个，我还缺那个。”它从开始任务一直运行到“完成”。

但这里的“完成”并不是点击按钮后再也没人检查，恰恰相反。它更接近一名 preparer 或 junior engineer 完成第一轮工作后交接：我做了哪些重大决定，采用了哪些假设，哪些地方需要你重点查看，现在我们一起 review。

软件工程里，没有人喜欢收到一份 1,000 行的 PR，再听对方说“已经完成，相信我”。更好的交付，是把改动合理拆成一组容易理解的 stack，清楚说明每个 diff 做什么，哪里采用了重要 architectural assumption，以及为什么这样做。系统不仅要完成任务，还要优化 reviewer 理解决策的成本。这个原则适用于 software engineering，也适用于大多数专业工作，尤其适用于会计。这就是我理解的 autonomy。

## 从 ReAct 到长程 coherence

**Matt Turck：** 我们回顾一下 agent 的历史。2022 年的 ReAct，也就是 reasoning and acting 框架，提出 agent 是推理与行动的组合。今天叠加了大量复杂技术后，底层理论仍然是这个吗？

**Mitchell Troyanovsky：** 在现代 LM 范式内，基本还是如此，但 reasoning 的作用已经扩展。它不仅用来判断某项任务该走哪条路径，还要调节模型自己的状态，确保下一次 inference step 拥有正确的信息。

我喜欢用 Christopher Nolan 的电影 Memento 作比喻。主人公患有短期记忆障碍。每天醒来时，他知道自己是谁，也知道基本常识，却不知道过去几年发生了什么。为了完成买菜、复仇等目标，他必须给自己留下笔记。第二天醒来后，他读取笔记，再在此基础上继续积累知识。

**Matt Turck：** 那是 Christopher Nolan 的早期作品。现在所有人都在谈 The Odyssey，但 Memento 是他很早的电影。

**Mitchell Troyanovsky：** 是的。不过我仍觉得 The Prestige 是 Nolan 最好的电影。

回到 agent，reasoning 一方面用于判断怎样处理 tax 等具体任务，另一方面必须思考：怎样确保下一次 inference 有足够信息与世界交互。短任务停留在 context window 内，这很容易；长任务超过 context window 或出现 context rot 后，模型必须通过 sub-agent、compaction 等方式主动组织自己的环境。reasoning 在这里变得极其重要。

## AutoGPT、BabyAGI 为什么失败

**Matt Turck：** 2023 年的下一阶段是 AutoGPT、BabyAGI。当时人们把它们视为巨大进步，但最终没有真正落地。原因主要是多步骤任务中的错误复利吗？

**Mitchell Troyanovsky：** 当时使用的大概是 GPT-4 或 GPT-4 Turbo。首先，早期 context window 很小，连组织自身环境所需的信息都装不下。后来 context window 变大，但模型在超过大约 20,000 tokens 后并不能保持良好 attention，实际上就不聪明了。直到 Claude Opus 3，模型才开始能在 100,000 tokens 左右真正理解上下文。

BabyAGI 没有这些能力，而且当时模型也不擅长 reasoning。不擅长推理就一定会产生 compounding errors：某一次 token generation 出错，后续步骤不断沿着错误继续走，而模型没有足够 self-awareness 去发现并自我修复。

## Opus 3、o1 与 o3 三次范式变化

**Matt Turck：** 真正的突破因此是 reasoning model？

**Mitchell Troyanovsky：** 对我个人而言，真正造成 paradigm shift 的时刻并不多。第一个是 Claude Opus 3。它经常被低估，但我认为它是第一个真正理解 long context 的模型。此前把 80,000 tokens 塞进 GPT-4 Turbo，它无法真正理解；Opus 3 做到了，这很惊人。

第二个当然是 OpenAI o1。第三个是 o3。o1 证明 inference-time reasoning 可以随投入算力扩展；o3 进一步证明，通过更好的 training、更多 compute、更好的 data 与 post-training，可以提高 reasoning 的质量和效率。模型在 inference time 每多花一个 token，得到的推理质量也更高。这一点在 o1 发布时并不显然。

**Matt Turck：** reasoning models 像 agent 一样在 loop 中训练，会尝试、回退再尝试。这是不是它们更适合 agent 的根本原因？

**Mitchell Troyanovsky：** 原因有几个。模型能够按具体步骤的难度调节投入的 compute。任何 trajectory 中都有很难的决定和很容易的决定。让一个巨大而昂贵的模型在每个 inference step 都用满全部算力，并不可行。

reasoning 让系统可以按需分配算力。现代 reasoning model 在简单步骤和困难步骤上消耗的 compute 相差很大。一个优秀 reasoner 如果愿意暂停、检查并思考，而不是像普通逐 token generation 那样完全依靠“直觉”，也会更擅长 self-healing。

## process reward 与 outcome reward

**Matt Turck：** 你在 X 帖子里提到 OpenAI 2023 年的论文 Let's Verify Step by Step，当时由人类标注约 80 万个 reasoning steps。那项工作的目的是什么？

**Mitchell Troyanovsky：** 当时有很多关于 Strawberry 能解决数学问题的传闻。研究界逐渐意识到，可验证的数学问题也许适合用来训练模型完成不同任务。机器学习历史上长期存在一个分歧：reward 应该只看最终答案是否正确，还是也看模型有没有像优秀数学家那样使用正确过程。

Let's Verify Step by Step 显示，在其样本中，根据过程而不是只根据结果给 reward，效果更好。但代价很高，因为必须让数学家逐步评价解题方法。

再往后看 DeepSeek R1 论文，它公开了当时很多实验室所采用的 RLVR，也就是 reinforcement learning from verifiable rewards。这个方案几乎没有 process supervision，而是问“最终答案对不对”，对了就奖励，再把规模做大，结果也确实不错。

## METR 曲线、理论自我认知与 runtime verification

**Matt Turck：** 去年广为传播的 METR 图表显示，long-horizon agent 的能力大约每七个月翻倍。2026 年你还观察到这种趋势吗？

**Mitchell Troyanovsky：** 绝对如此。不过 METR 曲线今天可能不够准确，因为这件事太难测量。我对其数据集细节不算熟悉，但样本量似乎较小，门槛也不高。

从实际体感看，模型确实因为变聪明而能维持更长时间的 coherence。现在它们还被专门训练去做这件事。模型必须对自己形成 theory of mind。比如它要把工作交给 sub-agent，或者给未来的自己写笔记。回到 Memento 的比喻：你知道明天醒来后会读今天留下的笔记，就必须思考怎样用信息密度最高的方式写，让未来的自己准确理解。这需要对未来的自己建立 theory of mind。

人类通常不需要刻意做这些事，因为大脑会替我们维持连续性。模型却必须学习这种非常不“人类”的工作方式。随着它们越来越多地接受这类训练，long-horizon 能力还会继续扩展。从 Claude 5、5.6 Sonnet 等进展看，这个阶段仍然很早。

**Matt Turck：** 2026 年 agent 向 autonomy 演进的讨论，不能缺少 verifiable rewards。它在整体图景中是什么位置？为什么 coding 成为第一个成功的 autonomous-agent 场景？

**Mitchell Troyanovsky：** 人们对这件事的理解有一点偏差。coding 确实可验证，可以检查代码是否通过，因此可以用结果对模型进行训练。但模型擅长 coding，不仅仅因为这一点。

第一，coding 可以在 runtime 被验证，这极其重要。agent 需要在运行中得到关于自身表现的信号。假设一名顶尖工程师写完代码后永远不能运行，他迟早也会留下一处 syntax error。coding 的很多部分可以在 runtime 容易、低成本地检查，而且环境高度 text-based，在本地电脑上就能运行。

第二，早期 coding agent 能实现指定功能，却缺乏判断“什么是好软件”的 taste。通过所有 unit tests，并不代表 app 架构正确、database 设计良好，或文件拆分合理。coding 最终仍有主观性，是一门 art。只靠 verifiable rewards 无法解决艺术判断。

模型今天不仅会写代码，也开始真正会做 engineering，另一个重要原因是训练数据的数量和质量。实验室里有大量工程师，coding 又是其战略重点，因此它们显然投入很多精力，保证 pre-training 和 post-training 数据包含高质量代码。verifiable rewards 只是让后续进展得以发生的起点，其他因素至少同样重要，甚至更重要。

## coding 以外的 agent 为什么更难

**Matt Turck：** 这就进入你们的核心工作：为真实经济构建 coding 以外的 long-horizon autonomous agents。它们为什么困难？

**Mitchell Troyanovsky：** 原因很多。第一，agent 不一定知道“好”的样子。第二，它在 runtime 不一定容易验证自己。第三，这也许更像 UX 问题：工程师本人深度参与代码，愿意容忍较低的自动化质量门槛；如果使用者离过程很远，系统就必须达到更高质量。

即便在 coding 领域，agent 也远未达到人类在长时间保持 coherence 的水平。它不能像 junior engineer 那样在一个项目上连续工作两周，因此起点仍比人差。

**Matt Turck：** tax return 不需要像代码那样 compile。你们如何定义“测试通过”？

**Mitchell Troyanovsky：** 好消息是，会计中仍有一部分东西可以“编译”。

**Matt Turck：** 要么被起诉，要么没被起诉？

**Mitchell Troyanovsky：** 更实际的办法是观察人类怎样组织工作。会计师必须努力做到正确，其中又包含大量 judgment 和 process。

我们常说：人类已经习惯与非确定性系统合作，只是那些系统过去是同事，不是计算机。公司和流程的意义，正是让人类这些 nondeterministic entities 协调行动、共同解决问题。换个角度看，这本来就很像 agent design。

如果想知道怎样设计 agent、哪些东西能够验证，就观察人类怎样组织 tax return。人类设置多层 verification 和 independent review，也使用 deterministic checks。比如 trial balance 是否加总为零，Excel 是否包含错误，都是明显可验证的项目。对人类显而易见的检查，也必须被明确编码进系统。

另一些错误不能被完全 deterministic 地验证，却会让会计师一眼发现：比如 agent 删除了 Excel 中某个 tab，或研究结论没有引用来源。这时可以构建 verifier、judge 或其他验证机制，在 eval 和 runtime 中提供信号。

## 数据稀缺、synthetic artifact 与超长反馈回路

**Matt Turck：** 你还指出一个问题：数据稀缺。

**Mitchell Troyanovsky：** 假设不考虑隐私，你拿到了全美国每一份真实 tax return，把它们用于验证 agent。数据规模与可以自动生成几十万、几百万道数学题相比，仍小得多。即使拥有全部真实数据，也无法把数量扩展到模型训练需要的层级，因此必须考虑 synthetic generation。

但合成会计数据极难，因为你生成的不是一段 text，而是必须真实、多样、内部一致的 artifacts。它会遇到数据多样性等所有老问题。这个问题迟早会被解决，但今天还没有。于是，数据生成能力与模型已经拥有的 latent capabilities 之间存在缺口。

**Matt Turck：** feedback loop 的长度呢？

**Mitchell Troyanovsky：** 它可能非常长。一个人完成一份 Form 1065，实际坐下来工作的时间很容易超过 20 小时，复杂 return 还会更久。即使拥有全部数据，也无法获得足够快速的 feedback loop，去运行持续改进 agent 所需的循环。

一份 return 可能包含 500 到 1,000 份文件。系统必须理解文件之间如何映射、哪些内容重要，对不同文件分别研究，再把结果编入特定 workbook，也就是大型 Excel。按 inference steps 计算，很容易达到几千步。

如果系统为不同任务派生 sub-agents，步骤数还会更多。还可以增加 test-time compute：遇到极难的 tax question，不只让一个 sub-agent 回答，而是同时派出五个，让它们投票。具体怎样构建系统，会显著改变总计算量。

## 为什么 100 个 outcome eval 全过仍不够

**Matt Turck：** 总结一下：流程包含几千步，数据不足，什么算正确也不总是清楚，只有一部分能确定验证。因此不能只依赖 outcome，还要监督 process。只看 outcome 究竟有什么问题？

**Mitchell Troyanovsky：** 对一条几千步，甚至只是一小时的 trajectory，你会设置 eval 来判断最终结果。某些指标完全可验证，例如数字是否一致；另一些可能用 LM-as-a-judge，根据 rubric 评价。

假设有 100 个 eval 全部通过，你仍不能确信系统会泛化到 production。工程师说 end-to-end tests、unit tests 全过，并不等于 database architecture 正确。达到某个 outcome 的路径很多，其中不少路径并没有遵循正确过程。

人类组织长期积累了大量工作方法，不应该因为一句 Bitter Lesson 就把这些经验全部扔掉，指望 agent 在 runtime 临时发明一套全新的 tax-return 方法，并自动超越几百年积累的流程。未来也许能做到。如果有足够 data 和 compute，纯 outcome-based process 最终可能成功，但不会很快发生。

今天模型已有很强 latent potential，现实做法是吸收人类对良好流程的认识，再翻译为适合 agent 的行为。不能原样复制人类流程，因为模型在 long horizon 中保持 coherence 仍需要大量 agent-specific design。之后可以建立 eval，未来甚至建立 reward functions，检查 agent 是否遵循过程。

例如回答 tax research 问题，agent 可能凭 pre-training knowledge 给出正确答案，也可能从某个 blog 找到答案。但真正的 accountant 不会信任这种做法，他要求引用 primary source。即使系统连续 100 次答对，如果依据都来自 Wikipedia，会计师事务所仍不会录用这个人，也不应采用这样的 agent。

因此，Basis 要求 agent 不依靠模糊的 pre-training knowledge 或普通 blog，而要查看实际 tax code，并用 primary source 验证结论。理想情况下，真实 tax accountant 也应这样做。

## behavior specs：把期望行为写成可执行的规范

**Matt Turck：** 你们因此提出 behavior specs。它在实践中是什么，是一个 Markdown 文件吗？

**Mitchell Troyanovsky：** 这个想法是我的联合创始人 Matt 大约两年前提出的。当时 agent 还不像今天这样充分 agentic，可选动作受到限制，但系统走到岔路口时，你仍要定义希望它作出哪类选择。

我们内部最早叫它 meta behaviors。你定义的是某个行为，但它处在更高层次，要跨越 agent 在不同 trajectories 中的所有行为。写 prompt 之前，团队必须先就 meta behavior 达成一致。后来为简化名称，我们直接叫 behaviors。

具体形式就是一个 Markdown 文件，在其中写明你希望 agent 怎样行动，粒度可以不同。比如要求研究时查 primary source，也可以更具体地要求始终查 IRS website。又比如让 agent 制作 PowerPoint，可以规定它提交前必须先把 slide 渲染为图片，检查是否存在 formatting issue。

这份 Markdown 最好 self-contained。人类可以阅读并确认“这就是产品应有的行为”，因为 behavior 本身带有主观判断，它既是 intelligence 问题，也是 product 问题。judge 也可以读取 trajectory，判断触发行为的条件是否出现；如果出现，agent 是否真的表现出规定行为，再据此评分。

**Matt Turck：** 谁来写 Markdown，或者监督这个过程？是 accountants 吗？

**Mitchell Troyanovsky：** 需要 accountants 与 applied ML researchers 共同完成。行为不只是“去某个网站”。你可能规定：对于某类研究，应派生一个携带完整历史的 sub-agent，因为它需要逐步建立 context。这里会涉及很多 agent machinery。

人类专业流程必须被翻译成 agent language，再与 agent mechanics 结合。Basis 有一支 Accounting Product Operations 团队，由 accountants 与 research teams 紧密协作，同时构建 outcome-based rubrics 和 behaviors。

**Matt Turck：** 如何平衡精确性与 brittleness？今天规定去 IRS website，也许两年后信息迁移到另一个位置。

**Mitchell Troyanovsky：** 这是非常好的问题，也正是 behaviors 不会直接展示给 agent 的原因。behavior 可以写“应该去 IRS website”，但不代表 prompt 一定命令 agent 去那里。是否把规则暴露给 agent，要由系统设计决定。

在边际上，最好提供 principles、原因和更多 context，让 agent 自己判断，而不是枚举所有可能情况。behavior spec 的意义，是构建者明确选择少数真正重要、可泛化的东西进行评分。

例如 PowerPoint 在交付前渲染成图片，通常能发现问题。但 product trade-off 仍然存在：一个原本 30 秒完成任务的超快 agent，如果渲染让时间变成一分钟，也许不值得；一个本来运行 20 分钟的 agent，多花 30 秒则应该每次都做。具体程度取决于目标 outcome 能否泛化到全部情形。这是一项主观 product design，而不仅是 intelligence design。

## context 是 runtime training data

**Matt Turck：** 2023 年 OpenAI 的工作需要 80 万个人工 labels。你们 2026 年的做法有什么不同？

**Mitchell Troyanovsky：** 至少今天，我们没有用 behavior reward 主动训练底层模型，也没有根据过程对自有模型做 post-training。这个方向很有研究价值，我们也在单独研究，但还不是当前 production 方法。

理解差异的一个好办法，是把 agent building 和 context engineering 类比为直接训练模型。人们谈 prompt、context 时，常用的心智模型只是“我写了一段 English，告诉模型该做什么”。我认为这是错误框架。更准确的理解是：context 就是 training data，只不过它在 runtime 训练模型。

模型在 inference time 进行学习，因此整个系统能提供的 runtime training data，远少于真正 post-train 一个模型所用的数据。agent 沿 trajectory 逐步发现并学习的全部 context，比 post-training 数据低几个数量级。构建者必须保证这些数据质量尽可能高，才能让 agent 表现出想要的 behaviors。

data 当然只是系统的一部分。还有 harness、tools、capabilities、environment，以及选用哪个 model。我们当前利用 behavior signal 改进的是整个 agent system，而不是把 signal 直接作为 RL reward 写回底层 weights。改进系统所需的数据规模，远小于训练模型。

## judge 本身也是 agent

**Matt Turck：** 你几次提到 judge。怎样训练或 instruct judge？更直接的问题是，谁来判断 judge 是否正确？

**Mitchell Troyanovsky：** 这不仅适用于 behavior eval，也适用于所有 outcome-based eval。我们没有无限时间和资源去把每个 judge 打磨到完美。高层原则是先建立对 judge taste 是否正确的直觉。怎样对 judge 做 post-training、怎样提升 taste，都是值得研究的方向。

今天首先要确保 judge 拥有作决定所需的信息、正确的判断框架，以及适合该任务的数据和心态。behavior judging 目前相当昂贵，因为这里的 judge 本身也是一个 advanced agent，而不是传统意义上看一段输出就打分的 classifier。

它必须阅读整个 trajectory。未来可以先更好地标注 trajectories，只筛出可能相关的部分交给 judge，而不是让它读取全部历史。Braintrust 等团队已经开始思考这个问题。

long-horizon trajectory 可能包含大量 sub-agents。若系统递归深度达到七层，就可能真的存在七层 agents。judge 必须知道自己该去 trajectory 的什么位置，判断的是 root agent 还是某一层 sub-agent。它需要一张 trajectory map，还要理解 behavior 的触发条件、应该观察谁，以及怎样判断行为是否发生。因此，judge 本身也要被正确 prompt，未来可能还要 tune。

## 为什么可靠性比 Move 37 更重要

**Matt Turck：** 这种方法有什么 trade-off？人类验证过的流程能提高严谨性、降低失败概率，但也可能错过类似 AlphaGo Move 37 的突破。AI 也许跳过几步，反而做得更好、更高效。

**Mitchell Troyanovsky：** 首先，把一项 behavior 写下来有真实成本。它意味着你开始保存 state，必须持续更新。如果又通过 context 让 agent 执行同一 behavior，系统里还可能出现 duplicate state。维护负担决定了 behavior 应该越少越好。

我们不是把 tax return 所有 best practices 全部写下来，再逐项监控，而是挑选最重要、最能泛化到 production、影响最大的几项。其他部分仍保留 agent 发现 Move 37 的空间。

更重要的是，客户到底在购买什么。假设一家公司规定工程流程：先画 architecture diagram，与 CTO 讨论并获得批准，把 1,000 行改动拆成 10 个小 PR，完成 end-to-end tests 后再部署。一名工程师却直接提交 1,000 行 PR，说要马上 merge production。它有可能是一记 Move 37，甚至比 CTO 的方案更好，但公司仍不会认为这是良好结果。

工作价值不是来自某一单元任务偶尔达到惊人最优，而是来自它能扩展成公司、系统和组织。客户购买 Basis，并不是为了得到“史上最漂亮的一份 tax return”，而是购买 consistent、reliable、trustworthy 的工作。

就像管理人类员工一样，客户先建立信任，再逐步扩大 agent 的 agency。要部署进真实经济，需要的是 reliability，而不是 Move 37。后者适合 Olympiad 数学竞赛，不适合日常经济工作。

## 把模型看作 magic box

**Matt Turck：** 你们做这一切时，并不了解底层模型内部究竟怎样工作，只能根据 artifacts、tool calls 和行为推断。每当新模型发布，是否必须重新审查整个系统？

**Mitchell Troyanovsky：** 构建 agent，尤其围绕它建立公司时，不应该经常感到意外。你必须有一套 world model，外部变化时更新它；但如果总在彻底改写 world model，说明最初的理解不够对。要成功，你至少得在一些根本问题上判断正确。

暂时忘掉 LM 内部实现。把它想象成一个 magic box，或者我有时说的 alien。你可以向这个 box 输入海量 data，它会在 inference time reasoning 和 learning，再给出 output。今天 tool calling 已经可用，因此 output 可以接入系统其他部分。理解这一点，已经足够推导很多设计结论。

如果一个 magic box 能做到这些，它能否决定调用另一个 magic box？能否把多个 boxes 串起来？单次 trajectory 会形成 activation state，KV cache 正来自这种状态，因此它会对当前 trajectory 产生偏置。做 review 时，也许应该启用一条不相关的新 trajectory，让另一个同样聪明但没有同样偏置的 box 检查。

把这些 LM intuition 与 organizational design、management 的基本原则结合起来，就开始接近 agent-building frontier。

**Matt Turck：** 怎样建立这种 LM intuition？一直读论文、和 researchers 交流，还是跟踪 state of the art？

**Mitchell Troyanovsky：** 最主要的办法其实都不是这些。看 Twitter、理解新进展有用，但很多人过度依赖它。如果没有对系统机制和能力边界的根本理解，就会觉得世界每天都在剧烈变化，实际上并没有。

从 o3 至今，没有发生新的 paradigm shift。并不是说我提前知道每条技术曲线，而是之后的变化基本都还处于同一范式。

建立直觉最好的办法，是在自己的工作里大量使用 agent，尤其是 coding。让 agent 实现某项 feature 却没有按预期完成时，不要停在“模型不好用”，而要像分析系统瓶颈一样问：真正的 limiting factor 是什么？它真的不够聪明吗？多数时候不是，模型已经聪明很久了。

我在招聘中也看到，agent intuition 最好的人不一定有 ML background。很多人只是非常擅长自动化自己的工作，擅长把问题拆成系统，并持续追问“应该构建什么环境”。真正重要的不是怎样 prompt 一个 model，而是怎样 build a system。主动思考 repo 中 data ontology 的人，通常会形成很好的 agent intuition。

## 与 Braintrust 开源 behavior spec 标准

**Matt Turck：** 具体说说你们与 Braintrust 开源了什么，项目从哪里来，为什么与 Braintrust 合作？

**Mitchell Troyanovsky：** behavior Markdown 同时是 spec 和 rubric。有人问它是不是 rubric，答案是两者都是。它不仅用于 grade 或未来 reward agent，也用于让人类先达成一致。

希望 agent 怎样表现，本身是主观问题。团队需要形成内部流程，共同确认“这就是我们要做的 product”。例如 PowerPoint 是否必须做图像验证，就是产品选择。标准的作用，是把这些选择写下来。

项目来自我和 Braintrust CEO Ankur 共进咖啡的一次交流。我忘了当时为什么谈到 behavior，但我向他解释 Basis 内部已经在做的事情，他立刻觉得很有意思。

Basis 做了很多 cutting-edge work，却很少公开讨论，因为我们一直在工作。就在录制前，我还给 Matt 看了联合创始人凌晨 4 点发给我的 prompt refactor Slack，我早上 6 点回复。那是星期日晚上。

**Matt Turck：** Basis 联合创始人的 996 正在全面运行。

**Mitchell Troyanovsky：** 对 Matt 和我来说不是 996，是 24/7。公司其他人工作很努力，但并不是 996。

我们希望更多分享，又没有大量资源做传播。behavior spec 如果成为标准，就可以被 observability 和 monitoring platforms 自动读取。对经验较少的团队，它还可以附带 out-of-the-box judges：用户只定义 behavior，不必先构建自己的 judge，就能看到评价结果。Ankur 因此很兴奋，合作由此开始。

开源 repo 中有几个小型示例、一个可直接使用的 example judge，以及一些已经写好的 behaviors，开发者可以据此构建自己的规范。

比采用某个具体标准更重要的是采用这种 mindset：运行 10 小时的 agent 并不是 black box。trajectory 中存在海量 data。如果你不了解 agent 怎样完成工作，可能是在损害客户利益。

**Matt Turck：** 你希望大家怎样参与？贡献、在自己的系统中使用，还是共同把它变成 industry standard？

**Mitchell Troyanovsky：** 最理想的是大家贡献想法。现在只是起点，仍有大量工作：怎样制造 good judge；怎样标注和拆解 trajectory，让 judge 更容易理解；怎样降低成本。按今天的计算费用，还不能在 production 中对每一条 trajectory 都运行这种 judge。

标准被刻意设计得很灵活，和 skills 有点像。它只是 Markdown，不要求必须出现五个固定词。behavior 可以写得宽泛，也可以非常具体。唯一硬要求是 self-contained：judge 读完后必须能够判断触发条件是否满足；若满足，行为究竟有没有发生。在这个边界内应保留足够自由度。

## ontology：为 agent 定义一个可居住的世界

**Matt Turck：** 除了 judges 和 behaviors，构建 long-horizon autonomous agents 还应考虑什么？你曾把 ontology 称为“agent 居住的世界”。它在整体系统中处于什么位置？

**Mitchell Troyanovsky：** ontology 极其重要。许多人一听 agent，心智模型就自动切换到 coding agent，因为这是技术从业者最熟悉的例子。

coding agent 随产品带有 harness、tools，也在 context 中编码了某些 behaviors。Codex 是 open source，我很建议开发者查看它的 repo。但 coding agent 并不控制自己的 runtime training data，因为它运行时的数据就是当前 codebase。

同一个 Codex agent 在一个 codebase 中可能表现一般，在另一个 codebase 中却极好，原因可能只是后者的 runtime training data 更优：skills 更清楚，操作 context 更完整，没有相互矛盾和令人困惑的规则。

codebase ontology 对人类工程师一直重要，对高质量 agent 同样重要，甚至更重要。到了 non-coding agent，问题又上升一层。coding 产品通常不拥有客户 repo；Basis 却拥有 Basis agent 看到的绝大多数数据，因此必须确保这些“训练数据”结构良好。这里的 training data，指手写 context 或 progressive disclosure 中的其他信息。

agent 每次都从零开始，ontology 必须让它容易使用。既包括 skills 等相对静态、所有 agents 都能访问的数据，也包括 long-horizon agent 给自己留下的历史。

如果运行几小时，历史也许只有几条 notes；如果一个 stateful agent 连续运行数天乃至数月，历史就会变成完整 folders。里面保存的是 agent 的 lived experiences。一个新启动、只带高度压缩 context 的实例，必须从这些材料中恢复自己完整的 state of mind。让这种恢复变得容易的 ontology，以及确保它执行恢复过程的 behaviors，是 long-horizon 系统能否真正工作的关键。

**Matt Turck：** 实际上怎样设计 ontology？它是 graph database，还是一组 relationships？

**Mitchell Troyanovsky：** 形式很多。最简单的理解就是 file system，其中包含某种结构。通常可以采用 virtual file system，给 files 和 folders 附加 metadata；也可以在 graph 中建立 connectors 和 nodes，或者增加 embeddings。

随着模型越来越便宜，更多工作可以直接用 inference 完成，而不一定依赖 deterministic graph 或 embedding。假设 inference 近乎免费，就可以让小模型遍历整个 ontology，为 agent 总结信息。

ontology 也不仅是 folder structure。传统意义上，它还包括 language：系统中有哪些 objects 和 concepts。既然 agent 在 runtime 接受训练，就必须避免把概念混在一起，并让整个世界保持一般意义上的一致。所谓“定义世界”，就是规定 agent 在探索环境时预期会遇到什么。

## 文档必须像 codebase 一样维护

**Matt Turck：** 你说过，面向 agents 的内部文档必须像 codebase 一样对待。删掉一个关键段落，就像删掉一行代码，会直接破坏 agent。这里的文档是 ontology 外部、由 agent 通过 tool call 搜索的东西吗？最佳实践是什么？

**Mitchell Troyanovsky：** 先区分两种情形。刚才的 ontology 主要指 Basis product 内部，也就是 production agent 使用的世界。企业内部使用 coding agent 或其他 agents 时，environment 的控制程度更低，因为它们还要访问 Linear、Gong、Pylon 等系统。

内部 agent 的关键，是清楚区分 canonical 与 non-canonical。一个新加入组织的人可以听完所有 Gong calls，但如果他想知道公司今天的 sales strategy，只听两年前的 calls 只会得到历史 context，不会知道当前策略。必须存在一份 canonical documentation。

人类常通过聊天逐渐学会这些隐性知识，agent 很难做到。更重要的是，真正的 organizational intelligence 不能让 agent 从不同人那里听到不同说法，或者在多个互相冲突的文字记录中猜测：当前 sales pitch 是什么，deck 怎样制作，email 应该怎么写。每件重要事情都要有一个 canonical source。

真正 agent-native 的公司必须明确自己的 company canon，用合理 ontology 组织，并像维护 code 一样持续更新。今天还很早，但未来这会成为员工最重要的工作之一。

## Language Architects 与系统思维

**Matt Turck：** Basis 正在招聘两年前根本不存在的职位，例如 Language Architect、agent manager。这些人做什么，什么背景适合？

**Mitchell Troyanovsky：** 我们需要很多这样的人。愿意加入的听众请联系我。坦率说，我们也仍在摸索。

我确定的一点是，systems thinking 很重要。它来自这样的经历：你必须对某种 abstraction 或 system 进行设计，使它能在大量不同场景中保持有效。

优秀 engineering 是 systems thinking，尤其是那些需要设计整体架构、寻找正确 abstraction 的困难工作。但历史上多数 engineering 更偏 execution，不一定真的锻炼系统思维。

law 也很类似。我甚至觉得美国 Founding Fathers 会成为优秀的 context engineers 或 agent managers。他们必须写出一段 English，让 lawyers、judges 在未来 runtime 中解释几百万次。认真写一部 law，就是在刚好的 abstraction level 上覆盖整个可能情形空间，还要对 judicial system 建立 theory of mind，预判它会怎样解释文本。

一些机场标牌会列出“不要带 gun、不要带 sword”，再罗列 30 种东西。这与 brittle rules 相同。你可以列出 50 条脆弱规则，也可以找到一个恰到好处、覆盖全部情形的 abstraction。

任何要求用 abstraction 思考的职业，都可能培养优秀 systems engineer。管理世界上最复杂 Excel models 的人也不例外，因此潜在背景非常广。

## Deployed Intelligence：帮助事务所接纳 300 名“外星员工”

**Matt Turck：** 你曾说，把 agents 部署到一家公司，就像一次 onboarding 300 名聪明但毫无 context 的 alien employees，因此 Basis 设立 Deployed Intelligence 团队。这个概念还在吗？

**Mitchell Troyanovsky：** 当然，DI team 非常出色。我得查一下，但我认为 Basis 确实首先使用了 Deployed Intelligence 这个名字。Google 搜索时，我们是第一家出现的公司。这个名称目前还没有广泛流行。

DI 不是 FDE，不是工程师进入客户现场为其定制系统；也不是一些公司所谓的 agent PM，用 agent builder 半定制地给客户“造一个 agent”。

这些人深刻理解会计行业，理解怎样建立良好流程，也能同理从业者突然把部分工作交给 agents 后会面对什么。DI team 与 accounting firms 合作，帮助它们过渡到新时期。

我们给客户的是一种 magic，但还必须教他们怎样使用。它不仅改变日常工作，也会改变事务所能承接什么业务、应招聘什么人才，以及怎样扩展为未来理想中的 firm。要求客户完全靠自己摸索并不公平。

客户贡献对自身 firm、历史流程和人员的知识，Basis 贡献部署 agents 的经验，两者结合，才可能建成真正 frontier accounting firm。

## closed loop 与 agent 系统的自我改进

**Matt Turck：** 2026 年一个重要话题是 self-improvement。它在 Basis 和 autonomous-agent 图景中是什么样？你也谈到 agents 对其他 agents 形成 theory of mind。

**Mitchell Troyanovsky：** Basis 的一个主要研究方向是“close the loop”：从发现 agent 犯错、表现不好，走到真正改进系统。这个闭环会很快接近完成。整个 loop 能否在年底彻底关闭我不确定，但届时应该已经非常接近。

随着 agents 对自己、进而对其他 agents 的 theory of mind 提高，会同时发生两件事。第一，它们在 runtime 更善于 orchestrate sub-agents，也更善于为自己调节 environment。第二，它们会成为更好的 context engineers 和 harness engineers。

今天，agent 设计 agent system 的能力，远差于它编写普通 software 的能力。这个领域太新，training data 中几乎没有足够样本，因此模型缺乏直觉。

很多 agent builders 还有一种奇怪偏见：context 中的 slop 似乎比 code 中的 slop 更能接受。他们会因 code file 抽象不正确而抓狂，却允许 context 一团糟。这很荒谬，因为 context 会直接改变 runtime performance；只要 logic 相同，code organization 不会改变 runtime 的模型性能。

工程师长期形成了珍惜 code 的习惯，但在 agent system 中，English context 反而更珍贵。agent 逐渐学会这类 engineering 后，才可能 close the loop。

关闭 loop 需要从运行中获得足够 signal。只使用 outcome-based eval，signal 非常稀疏；behavior 的价值之一，就是提供更多过程信号。之后可以让 agent 把这些 signal 传播到系统各处：更新 context、改变 tool、调整 harness。

今天也能做自动更新，但很容易 overfit 某个 signal。若希望改进能够 generalize，agents 仍需继续变强，系统研究也还有工作要做。

## reward function、credit assignment 与是否更新 weights

**Matt Turck：** model level 的 self-improvement 呢？你们目前主要做 harness，没有大量 reinforcement learning。下一项大赌注会不会是根据 behavior adherence 直接做 RL？

**Mitchell Troyanovsky：** reinforcement learning 最难的是决定 reward function，以及怎样把 reward 分配给 trajectory 中发生的不同事件，也就是 credit assignment。

这正是我们当前研究的核心。behaviors、production monitoring 和 eval 都是 signal sources，可以用于构造 reward function。怎样在无法完美验证的 domain 中建立可靠 signal，是最难的工作。

得到 signal 后，是通过正式 RL 把它传播到 weights，还是通过 harness engineering 这种“非正式 RL”传播到 context、tools 和 system，是另一个问题。signal development 才是困难部分。

今天我们不直接更新 weights，主要因为 model 在 self-orchestration 上的持续进步，带来的 performance gains 远大于我们自行更新模型可能获得的收益。未来是否改变还要观察，我们也会研究这个方向。

但要让模型在真实经济中可靠工作，最终一定需要类似过程信号。单纯增加 pre-training compute，再扩大 perfectly verifiable rewards 的 post-training，不会自然产出一台能可靠完成 tax return 的 model。它也许偶尔做出一份很优秀的 return，但真正的问题是：能否达到客户所要求的 quality、reliability 和 scalability。

## Bitter Lesson 最终会吞掉 harness，但不是现在

**Matt Turck：** 你担不担心 Bitter Lesson？Basis 和其他团队在 harness 层做的出色工作，会不会最终被 model 吞掉？

**Mitchell Troyanovsky：** 我假设它一定会被吞掉，因此并不担心。这就是未来。

我在帖子里故意留下一个提示：behaviors “尚未”展示给 agents。真正遵循 Bitter Lesson 的未来，也许所有 context engineering 都会消失。构建者只需说“我希望出现这些 behaviors”，系统就能自动做到。

它需要多久？我不知道精确答案。我估计少于五年，但不会少于两年，大概落在两到五年之间。

Basis 处于 hyperscale mode。我们不能等 Bitter Lesson 到来后才准确完成 tax return，所以今天必须做这些工作。

我也怀疑，process reward 可能长期仍对实验室优化 compute 很重要。经济中的每一种职业都已经积累大量流程经验，未必值得让模型在每个领域都重新寻找一次 Move 37。

## 技术不是长期 moat，业务嵌入才是

**Matt Turck：** 自己做 RL 能否成为防止模型能力吞噬应用层的 moat？未来 applied AI companies 是否都会成为某种 RL lab？

**Mitchell Troyanovsky：** 对正在创业的人，我建议这样思考：technical moats 不是真正的长期 moats。Basis 的 terminal value 不会来自某种只有我们发现的秘密 RL trick，那不重要。

重要的是，我们现在很擅长构建可靠并能部署进 production 的 long-horizon agents，而且会继续保持领先。这种能力让我们赢得 market share、深入嵌入客户。我们快速行动，是为了在所谓 AGI 到来前尽可能扩大部署。

未来多数 moats 会是 business moats。在 AGI 时代如此，在此前同样如此。Salesforce 的 moat 不是它能比别人写出更好的 SQL query，而是 business position、powers、所拥有的 workflows，以及深度嵌入客户后形成的各种优势。

technology 是一次暂时性 dislodgement，让三年半前还不存在的 Basis 得以进入市场、完成过去做不到的工作，但它本身不是长期价值来源。

这也不意味着专业能力会迅速完全 commodity 化。一群天才人类并不会同样擅长做 tax return，因为这项工作包含大量 subjective requirements。Basis 在具体会计工作中积累 competency，仍会在可预见时期决定交付质量。

## 给 AI builders 的最后建议

**Matt Turck：** 最后，请给今天构建 agents 的 AI builders 一些建议。最重要的 dos、don'ts 或 lessons learned 是什么？

**Mitchell Troyanovsky：** 最大教训是，不要因为世界变化很快，就丧失作出 first-principles decisions 的能力。Twitter 像 ADHD 一样不断跳转，中国实验室似乎每天都发布新东西，人很容易觉得自己无法判断方向。

更好的方式，是把今天的变化理解成一次 underlying paradigm shift，就像 cloud 带来的转变。然后从基本条件向外推演：如果 intelligence 变强 X 倍会怎样，如果没有变强又会怎样。

这样构建出的系统会更 coherent，技术和商业层面的 strategic bets 也会更好。事情确实在变化，但底层 paradigm 并没有每天重写，至少没有那么剧烈。真正理解当前范式，是在这个世界里持续建设的关键。

**Matt Turck：** Mitch，这场对话非常精彩。感谢你分享所有这些经验。

**Mitchell Troyanovsky：** 谢谢邀请。

【节目结尾】

**Matt Turck：** 感谢收听本期 The MAD Podcast。如果你喜欢这期节目，请考虑订阅，并在收听或观看平台留下积极评价或评论。这会帮助我们继续建设节目、邀请优秀嘉宾。下期再见。

