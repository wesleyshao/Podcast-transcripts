---
访谈时间: 2026-08-18
访谈时间说明: "无法确认实际访谈时间，使用 YouTube 发布时间。"
YouTube发布时间: 2026-08-18T12:00:06Z
youtube_video_id: xH7U7w9Qzlo
嘉宾名字: Rich Sutton、Khurram Javed
嘉宾公司名称: Oak Lab、University of Alberta
参与嘉宾:
  - 姓名: Rich Sutton
    公司或机构: Oak Lab、University of Alberta
    职务: Oak Lab联合创始人、强化学习研究者
  - 姓名: Khurram Javed
    公司或机构: Oak Lab、University of Alberta
    职务: Oak Lab联合创始人、强化学习研究者
播客名称: Sequoia Capital
播客url地址: https://www.youtube.com/watch?v=xH7U7w9Qzlo
字幕来源: YouTube 原始自动字幕（en-orig）
caption_text_path: /Users/wesley/.codex/automations/youtube/caption_cache/xH7U7w9Qzlo.en-orig.source.txt
全文提及的关键名词:
  - Rich Sutton
  - Khurram Javed
  - Oak Lab
  - reinforcement learning
  - The Bitter Lesson
  - continual learning
  - continual deep learning
  - Big World Hypothesis
  - synthetic data
  - large language models
  - AlphaGo
  - AlphaZero
  - Alberta Plan
  - continual backprop
  - catastrophic forgetting
  - abstraction
  - model-based planning
  - University of Alberta
  - Moore's law
companies: []
industries: []
technologies:
  - LLM
  - 强化学习
keywords: []
tags:
  - LLM
  - 强化学习
---

# Rich Sutton and Khurram Javed: Why AI Models Stop Learning, and How to Start It Again

## Transcript

主持人：今天我们很荣幸邀请到 Rich Sutton。Rich 发明了 reinforcement learning，写过这个领域的经典教材，也培养了包括 Dave Silver 在内的一批重要学生。他写的文章《The Bitter Lesson》已经成为这个领域最重要的思想文本之一，持续推动着 AI 研究向前发展。今天 Rich 的搭档是 Khurram Javed，他是 Rich 在 University of Alberta 的学生和合作者。两人现在共同创办 Oak Lab。我们会先讨论《The Bitter Lesson》、今天的大模型，以及 LLM 是否能带我们走到真正的通用智能；随后讨论 Oak Lab 的研究方向和创业计划。

Rich，几十年前你决定把自己的职业生涯投入 reinforcement learning，尤其是 deep reinforcement learning，并把 University of Alberta 建成这个领域的重要基地。当时这个方向还非常早期，是什么让你有这样的信念？

Rich Sutton：还能做什么呢？我们当时想理解 mind，而 learning 是 mind 的核心部分，拥有 goal 也是 mind 和 intelligence 的核心部分。所以我只是在坚持自己一直以来的想法。

主持人：那时候别人觉得你疯了吗？

Sutton：那是 AI winter。时间大约是 2003 年。其实这件事有点疯狂，因为 2003 年我患了很严重的癌症，确实一度濒临死亡。我已经努力了很多年，但又一次缓解之后，我还没有死。于是我想，既然我还没成功死去，既然这件事还会持续一段时间，那不如再找一份工作。于是我去了 Alberta，开始在那里教学。

最后我活了下来，这很不可思议。我现在可以用开玩笑的方式说这件事，但当时非常严肃。更重要的问题是，既然我当时只剩几个月的时间，为什么还继续做研究？Benjamin Franklin 似乎说过，如果你想知道一个人为什么做某件事，通常只有两个原因：habit 或 vanity。也许只是习惯，我一直在做原来的事情；也许是虚荣。但我觉得更多是习惯，因为当时我确实以为自己快要死了。

我一直很容易保持决心。人们有时认为我的观点很激进，会先问我为什么想法和所有人如此不同。但我完全不这么看。我觉得自己只是在用普通方式思考，反而是其他人有一点奇怪。

最近这段 AI 狂热之前，如果你谈 learning，根本不需要加上 continual 这个词。因为没有人会把不是 continual 的 learning 当作正常的 learning。我们一直在行动，也一直在学习。这才是最自然的理解。我并不奇怪，奇怪的是这个领域竟然需要把 learning 叫作 continual learning。它本来就只是 learning。

主持人：可以把“我并不奇怪，是这个领域奇怪”当成生活格言了。很高兴你和这个领域都继续走到了今天。过去二三十年，你是怎么挑选学生的？

Sutton：你给了我一个谦虚的机会。我要说，很多决定只是碰巧发生。我不认为自己特别擅长挑学生，有时幸运，有时不幸运，最后只是遇到了非常优秀的人。David Silver 也许是挑中了我，而不是我挑中了他。

Khurram Javed：我加入 Rich 的过程也很自然。我读完硕士后原本准备去工业界。后来我们在一个项目上合作。项目刚开始时，我做过的一项工作在一次会议上被提到，于是我被拉进了这个合作。我们配合得很好，我非常享受这种合作，Rich 也觉得顺利。六个月以后，我们已经取得了一些进展，于是觉得可以把合作转化成 thesis proposal。这个过程中，我没有正式申请，也没有先问 Rich 是否愿意做我的博士导师，而是先一起工作，然后决定这会是一个不错的 thesis，之后我才申请博士。

主持人：人生往往通过意想不到的方式运作。我们回到 2019 年，你写了《The Bitter Lesson》。那是一个很有意思的时点，ImageNet 的突破在 2009 年，AlphaGo 在 2015 年，而大语言模型的 scaling paradigm 还没有完全启动。是什么让你在 2019 年回头思考并写下这篇文章？

Sutton：这件事酝酿了很久。《The Bitter Lesson》表达的是我几十年来的经验，至少同样来自我亲历的 symbolic AI 浪潮。核心是不要被把人类知识直接装进系统的诱惑分散注意力，而要关注问题本身，以及如何利用 computation 进行扩展。

我至少在正式发表前一年就写过一些版本，也提前做过演讲。它不是对某个当下事件的即时回应，而是我长期观察不同人如何构建 smart systems 后得出的结果。

主持人：能不能用最简洁的话说出《The Bitter Lesson》的本质？

Sutton：我最近尝试把它压缩成 26 个词左右，大意是：不要像传统 AI 那样被 human knowledge 分散注意力，而要专注于能够随着 computation 扩展的 learning methods，例如 search 和 learning。

所以关键是关注 algorithms 和 algorithmic improvement。它不是说 fancy algorithms 没有用。你当然需要好的算法，但应该是能够随 computation 一起 scale 的好算法，而不是只能随着更多人类输入、更多人工规则一起扩展的算法。

主持人：也就是说，不是随着人工输入规模化，而是随着数据和计算规模化？

Sutton：更准确地说，是不要让系统的能力主要取决于 human input。接下来不可避免的问题是，large language models 是否符合这个 lesson？

我认为 LLM 同时是一个正面例子和一个负面例子。首先，LLM 让我们能够大规模地利用 computation。它可以吸收互联网上的海量信息，通过能够扩展的方法让系统变得更强，这是一个非常有力的例子。

但继续往前走时，系统会受到这些信息的限制。互联网是有限的，获取更多高质量例子越来越困难，而现实世界比我们存储在互联网中的内容大得多。最终，LLM 可能成为一个反面例子：我们过度依赖已经积累的人类知识，而这些知识反过来限制了系统。

主持人：现在 foundation model labs 正在用 synthetic data，试图超越已有互联网这个“化石燃料”。Synthetic data 是否仍然属于利用 computation 的通用 scaling 方法？

Sutton：不，这是一个很大的错误，也许它会成为下一个 lesson。这个想法在 Alberta 已经流传了五到十年，我们称它为 Big World perspective 或 Big World Hypothesis。Khurram 后来把它写成了一篇论文。

Big World 的意思是，世界无限大，永远有新的事情可以学习。人类可以生成 synthetic datasets，但世界里永远有更多任务和更多经验。如果系统能够直接从 experience 中学习，不再需要人类处在循环中，那么它最终就能完成各种任务。

关键问题是，谁决定什么是好的 synthetic data，什么是坏的 synthetic data？我可以写一个程序，生成大量 synthetic data，但这些数据可能反而伤害系统。现在仍然是人类在决定。你需要人类专家知道针对某种方法，什么数据有用，什么数据无用。只要需要专家决定生成什么数据，系统就仍然被人类瓶颈限制住了。

主持人：但不是可以看 loss curve，比较用这批数据和另一批数据以后，模型是否变得更好吗？

Sutton：如果 OpenAI、Anthropic 或其他实验室的工程师都去度假，谁来生成 synthetic data？它不会自动来自 agent 的 experience。必须有某个人决定该生成什么数据，而这个决定需要 human expertise。

假设你想做一个很有挑战性的物理任务，例如让一架无人机像蝙蝠一样用 echolocation 定位和飞行。什么才是正确的 synthetic data？你需要先雇佣懂这个领域的人，弄清楚要生成什么，随后系统才可能从中学习。domain expert 必须先存在。

主持人：但可以有无限多个 synthetic worlds，而现实世界是有限的。

Sutton：我们回到蝙蝠的例子。我的目标是让机器人通过 echolocation 定位自己并移动。机器人当然可以通过自身经验产生新的 experience，但无论你生成多少 synthetic data，都不能让它完成这个任务，除非人类先把关键问题想清楚。

Synthetic data 不会自动正确。它生成的是一个 synthetic world，而不是现实世界。现实世界极其复杂，一个生成数据的小程序只会描述一个很小的世界。你甚至无法用 synthetic data 告诉我其他人的 mind 正在发生什么，而人的 mind 对我们很重要。你也无法用 synthetic data 完整描述无人机在现实物理环境中的互动、摩擦、马达磨损和各种未预期情况。

世界的复杂度远超任何一个 agent。世界里还包含许多其他 agents，因此没有任何系统可以声称自己拥有 optimal 或 perfect 的模型。我们只能用 approximation，而且 approximation 必然很严重。我们必须 continual learning，是因为系统会遇到现实世界中某个此前没有见过的部分，需要学习一个适应当前环境的 approximation，而不是为所有环境建立一个完美模型。

主持人：我再追问一次。新一代自动驾驶公司很多主要在 simulation 中训练，之后再做 post-training，使系统能够适应现实世界。这条 pipeline 看起来很有效。

Sutton：更重要的问题是，建造那个 simulation 需要多少工程师？我们是否愿意说，只有能够雇佣一大批工程师先建立 simulation 的问题，才值得解决？我相信这些公司经历了多轮迭代：先做 simulation，在其中训练，发现 sim-to-real gap 无法接受，再由人类修正 simulation。现实世界不断给人类反馈，人类再把 simulation 改好。

主持人：而真正开始驾驶以后，又会出现意外情况。

Sutton：那正是系统需要从 experience 中学习的时候。Simulation 有价值，但 agent 应该从自己的 experience 学会 model，再用这个 model 进行 planning。系统自己学出来的 model 如果不正确，可以通过 continual learning 修正。人类制作的 simulator，只有等人类发现问题以后才会更新。我们可以让 agent 从 simulator 学习，但理想的 simulator 应该由 agent 自己构建和更新。

主持人：我想回到《The Bitter Lesson》里关于移除 human knowledge 的部分。你写道，研究人员为了取得短期进步，往往利用自己的领域知识，但长期真正重要的是利用 computation。你的前学生 Dave Silver 通过 AlphaGo 和 AlphaZero 去除大量 human priors，这是不是一个让你惊喜的结果？

Sutton：当然，这让我非常高兴，也让我觉得自己的判断得到了验证。结果本来可能是另一种方向。Prior knowledge 并没有错。事实上，《The Bitter Lesson》开头就说，prior knowledge 和 learning knowledge 不必互相冲突。你可以把 prior 放进系统，然后继续 learning。它们都是 knowledge，人生就是持续获得和拥有 knowledge。

Nature 和 nurture 也不应该成为敌人。你先有 prior knowledge，然后继续学习；新知识积累以后，又会成为新的 prior knowledge。二者应该互相协作。

实际情况是，喜欢现有 human knowledge 的研究者，常常让它和 learning 对立起来。他们希望已有知识获胜，于是试图减少或排斥 learning。我看起来像是只相信 learning，是因为世界上很多人一直在说“只要放进足够的知识就好，不需要继续学”。

LLM 把大量知识放进系统，运行时却不继续学习。它和人交互，看到新信息，但 weights 永远不变。你不能一边声称系统获得了相当于 PhD 的 experience，一边又让它完全停止 learning。

主持人：你的建议是，让算法运行得更久，持续学习，而不是只在部署前喂给它大量 prior data？

Sutton：两者都重要。但从长期看，必须构建获得和组织新 knowledge 的机制。未来如果我们有 intelligent robots，应该让每个新机器人从互联网重新训练一遍，花费巨额成本，还是直接复制一个已经有基础知识的 agent，再让它从那里继续学习？如果机器人是 digital 的，复制它很容易。Prior knowledge 可以从上一代复制而来，但之后仍要继续学习。

主持人：你认为一个从 experience 学习的 machine 或 computer 会是什么样？

Sutton：它可以是机器人，也可以完全存在于互联网中。比如，一个对经验敏感、随着时间变好的互联网路由系统；一个通过 phone 或 computer 的 user interface 与人互动、逐渐知道你想要什么的 intelligent assistant。关键不是它是否长得像人，而是它是否会因为经验更新自己。

主持人：现在流行的基于 LLM 的 assistant 并不是 experiential learner 或 continual learner。它们也有 memory，也会做 in-context learning，根本差距在哪里？

Sutton：你是认真的吗？它们的 weights 从来没有改变。它们可以记住关于你的 memory，可以在当前 context 中改变状态，但那不等于 model 正在 learning。

继续进行 weight learning 很重要。构建 LLM 时，很多结构和新概念都通过 weight learning 得到。你不能只让这种 learning 发生一次，然后永久冻结。Pre-training 可以很多，post-training 也可以，但模型部署以后仍然应该继续学习。

主持人：那把 fundamental skills 放在共同的 weights 里，把个性化放在 context 中，是不是正确的 mental model？

Sutton：Context 可以放在 state，也可以放在 weights，两者都可以。但你仍然需要更新 weights。人类大脑的可塑性说明了这一点。比如我们有 proprioception，也就是告诉我们身体处于什么位置的内部传感器，我们依靠它走路。有些人会完全失去这种能力，最初因此无法行走，但两三年后，他们可以通过观察自己的脚和利用视觉反馈重新学会走路。

大脑非常有 plasticity。一个持续二十年的事实如果突然不再成立，大脑能够更新原来的结构，消除旧的假设，重新适应。这种能力正是我们希望 AI system 具备的能力。

主持人：我们可以从婴儿和动物的学习方式中获得多少灵感？

Sutton：动物学习是 inspiration，但不是 constraint。AI 不必机械模仿自然系统。自然学习说明了许多可能性，但不意味着我们必须照抄生物机制。

我认为一个显而易见的事实是，动物并不是通过 supervised learning 学会大部分能力的。没有人告诉我们肌肉应该如何抽动，但我们学会了视觉、行走和理解世界。学校是非常特殊的一小部分学习，不是 intelligence 的本质，也不应该成为我们理解 learning 的首要例子。

主持人：但学校里获得的很多知识和技能确实是 supervised learning。

Sutton：从别人那里获得知识当然极其重要，language 也极其重要。但即使在学校里，没人会告诉你如何准确地抽动自己的肌肉。老师告诉你法国的首都是 Paris，但不会告诉你如何用自己的身体发出“Paris”的声音。即便我模仿另一个人的嘴、舌头和声带动作，发出来的声音也会不同。自己的身体只能通过自己的 experience 学会如何完成动作。

主持人：我同意，原始的 sensory-motor 能力需要通过经验学习。但人类的独特能力还包括抽象、计划和想象。人类可以建造火箭、进入太空，而这些事情在发射前没有可直接模仿的经验。如何教机器想象此前不存在的东西？

Sutton：我同意必须能够 plan，也必须能够 imagine。问题是，这种能力仍然应该从 experience 中产生，而不是一开始由人类把所有 abstraction 写进系统。

主持人：一千年前的人类，在还没做过现代社会的大部分事情时，是否和今天一样聪明？

Sutton：过去一万年里，人类的大脑可能没有发生太大变化。机器基本相同，但我们积累了 1 万年的 knowledge。今天的学生通过学校的 supervised learning，在较短时间里获得这些知识，而不是从零开始通过个人 experience 重新发现一切。

所以我们希望 AI 既从 experience 学习，也接触我们的 culture 并学习文化知识。问题在于 paradigm shift。当一个人类积累了大量知识后，通过经验形成新的 abstraction、用新的 abstraction 进行 planning，并发现新知识，这种能力在当前系统中仍然严重缺失。

Khurram Javed：人类和动物都可以通过经验学会很多事情。但人类还能够在发射火箭之前，通过 abstraction 想象它是否可能成功。我们想知道，机器如何学习此前没有出现过的模型，如何从这些模型中计划和推理。

Sutton：你们现在又开始做我说不要做的事情：争论 prior knowledge 重要，还是获得 knowledge 重要。它们不应该互相争夺。机器可以从 culture 获取 prior，也必须继续学习。二者是朋友。

主持人：机器应该怎样知道什么时候需要改变 paradigm？

Sutton：通过自己的 experience。它不能依靠人类告诉它另一种 paradigm，因为人类自己只看到了旧 paradigm。系统需要在 experience 中找到能带来更好预测、更好泛化或其他优势的新方式。

当前领域最大的缺口，是还没有真正实现“学习一个 model，然后用这个 model 进行 planning”。AlphaGo 看起来像一个例子，但游戏的 model 是已知的，棋子如何移动、规则是什么，都已经给定。数学也类似，operators 和 Lean 从一个知识状态转移到下一个证明状态的规则是已知的。

但如果 model 需要系统自己学习，我们目前几乎没有让系统先发现 self-discovered abstractions，再用这些抽象 model 做 planning 的实例。有人会学习下一秒或下一毫秒会发生什么，但那不是我们所说的高层 model。真正的 model 更抽象、更结构化，也更接近系统对世界的理解。

主持人：你们不是只是在讨论问题，而是已经创办了 Oak Lab。2022 年 Rich 提出了 Alberta Plan，一个具体的 12 点 AI research plan。能否介绍一下？

Sutton：我们既有总体想法，也需要把它们拆成更小的步骤。12 个步骤就是把研究目标具体化。其中第二步 continual deep learning 非常重要，几乎可以说是解锁其他步骤的关键。如果系统能 continual deep learning，就能持续更新自己的 world model。

后半部分步骤主要关注如何形成正确的 abstractions。但不存在对所有世界都正确的固定 abstraction。Agent 必须根据自己所处的 world 学会适合自己的 abstraction。因此两个关键点是：学会适当的 abstraction，以及持续进行 deep learning。

Javed：人们都知道需要 model，也需要用 model 做 planning，但 abstraction 决定 model 应该以什么为条件、应该预测什么、行动之后会发生什么。Elite athletes 是很好的例子。如果你问顶级运动员如何完成某个动作，他们可能会使用一些非常细小、非常专业的术语，描述其他人无法察觉的动作。如果他们独自行动，甚至可能没有名字，只是直接做出来。

这些 abstraction 是怎么产生的？这正是 Alberta Plan 后半部分试图回答的问题。

主持人：Continual deep learning 的缺口是 algorithmic gap，还是 deployment infrastructure 和 data privacy 的实践问题？如果只是根据用户互动更新 weights，今天也能做到。

Javed：它绝对是 algorithmic gap。简单地做 naive updating 会带来很多问题。假如你拿一个样本更新整个模型，旧模型里的所有 knowledge 都可能被这个样本破坏。当前的做法通常像 Cursor 一样，使用来自大量用户的大 batch 数据，然后统一更新 policy。这在能收集大批数据时可行，但很多场景只有单一的数据流，naive 方法会摧毁 prior knowledge。

这就是 catastrophic forgetting。但它不是无法治愈的问题，需要正确的 algorithm。第一步是 step-size optimization，让网络中的每个 weight 都有单独的 step size。有些 weight 变化快，有些变化慢。系统通过 meta-learning 学习每个 weight 的 step size，大多数 weights 的 step size 应该很小，这样新样本不会破坏整个网络，而只会改变正确的位置。

第二步是 feature space 中的 generate-and-test。系统要提出新的 features 或 units，而不是只依赖 gradient。Gradient 只有在知道某个方向有帮助时才会沿那个方向移动，过程很慢，也无法自然地让模型不断增长、变得更复杂。

我们有一个叫 continual backprop 的算法。它与 backprop 相似，但会持续加入用随机 weights 初始化的新 units。普通 backprop 只在时间开始时使用随机 weights，之后随机性和多样性会逐渐耗尽；continual backprop 会持续注入一点 randomness，持续 generate，backprop 则负责 test。把这些机制结合起来，就可能得到新一代、能力显著更强的 continual deep learning。

主持人：这些算法能否用于今天的 LLM scaling？

Javed：不能把一个已经训练好的模型拿来直接更新，然后期待它自动解决问题。因为这些算法同时在 meta-learn how to learn。更好的方式是从头训练一个新的 foundation model，同时让它学习 knowledge 和 future learning 的方法。它不是只学会今天的知识，也是在学习以后如何学习新知识。这样才有机会在不发生 catastrophic forgetting 的情况下持续进步。

主持人：你们在 Oak Lab 要做的最激进的事情是什么？

Sutton：我不认为自己激进，其他人可能才奇怪。2016 到 2018 年间，已经有人探索过类似方向，但他们通常在很有限的问题分布里做实验。我们希望从 single stream of experience 出发，让方法在更一般的场景适用。

最有野心的目标，是建立从微小细节到宏大任务的完整 knowledge spectrum。把一架飞机从一个城市送到另一个城市，是一个很大的任务；松鼠解决鸟食器障碍，是更小的任务，但它也在使用 abstraction。我们希望对大事和小事用统一方式处理，并让系统能够自我维护。

真正的大问题是：knowledge-based system 怎样保持 knowledge 正确？LLM 的方式是，人类做大量 post-training，确认它大体正确，然后把模型冻结。但人类的 mind 会持续变化，同时又能保持组织性、一致性，并回到一个稳定状态，而不是不断漂移进疯狂世界。我们想建立一个 self-consistent 的 mind，能够持续训练自己，同时保持 coherent。

主持人：这个 vision 很宏大，似乎要把所有能力统一到一个 mind 中。

Sutton：它在能力范围内。现在是 2026 年，计算机已经很快。我们已经有 vision，也看到了一些步骤的雏形。我不认为它不可达。

主持人：你们还讨论过一个 trillion-parameter model，只消耗 20 watts。这听起来非常激进。

Javed：以当前 technology 看，确实不可能。单纯把一万亿个参数存进 memory，可能就会超过 20 watts。但 computation 正在变得更便宜、更节能。五到十年以后，如果 algorithm 正确，可能就会变得可行。

主持人：按照 Moore's law，十年大约是两个数量级的进步。如果十年后 20 watts 可行，那么今天大约需要 2000 watts。你们现在能用 2000 watts 做到吗？

Javed：有了正确的 algorithm，我认为可能比 2000 watts 更高效。但问题是，很多 research groups 根本不相信这条路径可能成功，因此不会投入时间解决技术问题。

大公司还被现有 product 锁定。新的 algorithmic paradigm 很可能在一开始表现更差，然后才逐步变好。大实验室无法轻易选择一条先退步的路径，因为它们必须持续支持现有产品。我们更像是陷在一个 local minimum 里，必须先接受新方向的短期损失，才能探索更好的方向。

主持人：如果 Oak Lab 一切顺利，公司最后会变成什么？

Sutton：如果我们实现了 architecture，让系统真正 continual learning，并形成 abstraction，从而可以 planning 和 reasoning，就可能得到真正的 intelligence。具体会发生什么很难预言，但世界会变得更令人兴奋，而不是人类变得无关紧要。

LLM 可能会受到影响。它们已经取得了很好的成绩，甚至是一项完全出乎预期的科学突破，是 neural networks 在语言使用上的巨大成功。过去很多人坚持 symbolic methods，认为语言需要这些方法，LLM 彻底改变了这种看法。

但我们不能把 LLM 的成功假装成整个 AI 的成功。流畅、灵活地使用语言，只是 intelligence 的一个子集，可能是 20% 或四分之一。智能还包括感知、行动、持续学习、建立 world model、形成 abstraction、规划以及处理现实世界。

主持人：你们想做的是一个能够从摆动树枝、行动、感知，一直到制造宇宙飞船的单一 mind 吗？

Javed：我们追求的是 single design，而不是只有一个单独的 mind。会有很多不同的 minds，它们使用同一设计，但因为经历不同的 experience，最终学到不同的知识。

Big World Hypothesis 说明，一个 system 不可能学习无限多的事情。即使有两个世界上最大的系统，它们也不可能完整地 model 对方，因为两者同样复杂。最终应该有许多 systems，各自从自己的 experience 学习。

主持人：Oak Lab 招人吗？

Javed：我们在招人。最初的团队大部分已经有明确人选，他们过去长期思考这些问题。我们不会很快扩大规模，因为每个新成员都需要真正理解我们看到的东西，而不是简单地加入一个已经成熟的大团队。我们会从小团队开始，慢慢增加到几个人，再继续发展。团队需要高度一致，才能高效合作并持续推进。

主持人：非常精彩。Rich，你是 reinforcement learning 和 algorithmic design 未来方向上极其深刻的思想者。感谢你们分享正在做的事情。

Sutton、Javed：谢谢，很高兴参加。

Sutton：我要再次强调，所谓“移除 human knowledge”不是拒绝所有已有知识。一个 agent 一开始当然可以拥有 prior，它也需要从文化、语言和其他人的经验中学习。真正的问题是，研究者不能把现有知识当成最终答案，并因此停止让系统自己发现新 knowledge。一个会学习的 mind，会把旧知识作为起点，再把新经验组织成更好的结构。

主持人：这也意味着，模型不能只通过 context 模拟自己知道了某件事。它需要区分当前状态的改变和长期结构的改变。

Javed：对。Context 可以影响下一次预测，但如果 weights 不更新，模型没有真正把新概念纳入自己的能力。人类不会因为暂时看到一张纸条，就永远停留在纸条提供的状态；我们会改变内部模型，之后即使没有纸条，也能利用已经学会的东西。AI 也需要这种从短期状态到长期能力的转换。

Sutton：人类的学习不是一次训练、一次部署、然后冻结。我们每天都通过行动得到反馈，更新自己的理解。我们也不是只在数据上做离线 supervised learning，而是在一个连续的世界里行动、观察、修正，再行动。这个闭环比把更多文本放进 context 更重要。

Javed：Continual learning 还必须解决一个现实问题：新经验不应该轻易破坏旧能力。一个单独的新样本可能只代表一个异常情况，如果它直接更新整个网络，就会发生 catastrophic forgetting。每个 weight 都应该有适合自己的更新速度；对长期稳定的结构，更新幅度很小，对新变化真正相关的部分，更新幅度可以更大。

这也解释了为什么 generate-and-test 很重要。系统不能只沿着已有 gradient 慢慢移动，因为那样很难主动产生全新的 representation。它需要提出新的 units、新的 features 和新的假设，再通过 experience 测试这些假设。Continual backprop 的想法，就是在 backprop 的 tester 旁边，持续注入新的随机种子，让模型拥有不断增长的可能性。

主持人：如果这些方法需要从头训练新的 foundation model，成本会非常高。

Javed：是的，但这不是只比较训练成本的问题。今天的大型实验室已经花费巨大资源做 pre-training 和 post-training，却把 deployment 之后的 learning 关闭。我们要做的是让模型在学习知识的同时，学习如何继续学习。短期成本可能更高，但如果最终得到的是一个不需要每次都从互联网重新训练、能够随着经验改进的系统，长期经济性可能完全不同。

Sutton：而且很多算法方向在一开始不会达到 state of the art。新 paradigm 往往先变差，因为它要解决现有系统没有解决的问题。大公司不愿意承担这种阶段性退步，不代表技术不可能，只说明它们的 product 和组织结构不适合探索这条路。Oak Lab 的意义之一，就是允许小团队长期思考，并在现有范式之外做实验。

主持人：所以你们真正想解决的不是让一个模型记住更多内容，而是让它能在一个复杂世界中形成自己的模型，使用模型做 planning，再通过结果继续修正模型。

Sutton：是的。世界不是一组已经写好的题目，也不是一个可以被小程序完整模拟的封闭环境。Agent 必须面对其他 agents、物理摩擦、社会关系和无法预先列举的情况。只有在真实经验中持续更新，才能形成针对当前世界的合理 approximation。

Javed：这也是为什么我们不把 abstraction 当成一组固定的人类规则。飞行员、运动员、工程师和科学家会根据自己遇到的问题形成不同的概念。好的 abstraction 不是抽象得越多越好，而是能让 agent 更准确地预测、更有效地行动，并在新的经验中继续改变。

Sutton：最终我们想要的是一个能够保持自洽的系统。它既能处理微小的动作，也能处理长距离的计划；既能从别人那里继承知识，也能通过自己的经验发现新知识。它不会因为一次更新就忘记过去，也不会因为过去的知识太多而停止学习。
