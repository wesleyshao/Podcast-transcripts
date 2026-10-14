---
访谈时间: "2026-06-16"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Chris Gannatti; Elvira Korumshina; Simon Fried"
嘉宾公司名称: "WisdomTree; Classiq"
播客名称: "The Next Big Thing"
播客url地址: "https://www.youtube.com/watch?v=D9C0d5t9bTY"
全文提及的关键名词: 
  - "quantum software"
  - "quantum algorithms"
  - "hybrid quantum-classical workflows"
  - "Classiq"
  - "IonQ"
  - "Cisco"
  - "quantum-ready enterprises"
  - "AI and quantum"
  - "quantum applications"
字幕来源: "automatic_captions:en-orig:English (Original)"
YouTube视频标题: "The software behind the quantum revolution | The Next Big Thing"
---

## Transcript

[00:00:02] Thank you everyone for joining us for
[00:00:05] our newest episode here of the next Big
[00:00:08] Bang [music] podcast. We've been doing a
[00:00:11] lot of great episodes this year. This
[00:00:13] this one here it's
[00:00:15] extremely topical
[00:00:17] in our view. We're recording roughly
[00:00:20] one week after the big announcement made
[00:00:24] by the US government talking about the
[00:00:27] importance [music] and making certain
[00:00:30] strategic investments in quantum
[00:00:32] computing and and quantum computing
[00:00:34] adjacent companies sort of signaling the
[00:00:38] importance of the space to the US as
[00:00:41] well as to the global marketplace. So
[00:00:44] today's episode surprise surprise
[00:00:46] quantum computing is our topic. I'm
[00:00:49] joined by my colleague who works a lot
[00:00:52] with me on quantum computing, Elvira
[00:00:55] Korumshina. She has been on numerous
[00:00:57] episodes so you're you're going to
[00:00:58] recognize her her face on the video, her
[00:01:01] voice, and it's it's exciting because
[00:01:03] she gets to hear a lot of the outside of
[00:01:06] the US quantum computing discussion,
[00:01:08] whereas I hear a lot of the inside the
[00:01:10] US quantum discussions. And then we we
[00:01:14] are also joined with our partner who
[00:01:17] works with us a bit in the index, Simon
[00:01:21] Fried over at Classic. Just to sort of
[00:01:24] define the the relationship here. We at
[00:01:27] Winton Tree have a strategy and
[00:01:29] essentially as we manage and run that
[00:01:32] index Classic has partnered and
[00:01:35] it's excellent to be able to get real
[00:01:39] feedback almost at the practitioner type
[00:01:42] level cuz Elvira and I obviously have
[00:01:44] the more financial and asset management
[00:01:47] type of background, whereas Simon is
[00:01:49] coming at this from
[00:01:51] more inside the quantum computing
[00:01:54] industry. But as we were sort of
[00:01:57] thinking through the plan of this
[00:01:59] episode, I know Elvira had a number of
[00:02:02] questions to kind of kick off the
[00:02:04] discussion. So, what I was going to do
[00:02:06] is actually not my usual. I I think as
[00:02:09] as the audience listens to the journey
[00:02:11] of this episode, I I would I would hope
[00:02:13] they get a better and better sense of
[00:02:16] where are we today in quantum computing
[00:02:18] as we sit here in 2026? What what kinds
[00:02:20] of things is quantum computing or
[00:02:23] quantum-inspired
[00:02:24] algorithms being run on classical
[00:02:26] systems? What are these things doing?
[00:02:28] How are they helpful? Uh, where are they
[00:02:30] being used? What When we say clients,
[00:02:32] what does that ultimately mean? Uh,
[00:02:35] we're we're going to take you on a
[00:02:36] journey today, and at the end of the
[00:02:38] episode, I hope, uh, you have a better
[00:02:40] idea of all of that. But, to to sort of
[00:02:42] kick off our discussion, I was going to
[00:02:45] pass, uh, the microphone over to Elvira.
[00:02:51] >> Thank you, Chris, for this introduction.
[00:02:53] I think it's a very exciting, uh, time
[00:02:55] right now to discuss quantum computing.
[00:02:58] And I actually just wanted to start with
[00:03:00] the following. In the last few months,
[00:03:03] we've been seeing incredible momentum in
[00:03:05] quantum computing.
[00:03:06] Um, several exciting announcements, um,
[00:03:09] around World Quantum Day. I think
[00:03:11] IonQ's, uh, networking breakthrough then
[00:03:14] also followed by Cisco were just very
[00:03:16] important events that further indicate,
[00:03:20] you know, that's, um, useful quantum
[00:03:22] computing might be actually much closer
[00:03:24] than many people think. But, um, at the
[00:03:27] same with all the excitement that we are
[00:03:29] seeing around quantum hardware, because
[00:03:32] this is quite important for, um, further
[00:03:35] breakthroughs for understanding where we
[00:03:37] are in this quantum journey. I think
[00:03:39] it's
[00:03:39] useful also for the audience who is
[00:03:42] listening today
[00:03:43] to explain why quantum software is
[00:03:47] important, and why should people care
[00:03:50] about quantum software, Simon?
[00:03:52] Just from from your own perspective
[00:03:54] here.
[00:03:57] >> Sure. Well, thanks thanks for having me
[00:03:59] and certainly in the classic is is all
[00:04:01] about software.
[00:04:02] And I think probably what we've seen
[00:04:05] as as we saw with you know the classical
[00:04:08] computing back in back in the 60s and
[00:04:10] and and even I think with with
[00:04:12] you know with with cell phones as well
[00:04:14] is that it's very easy and it's very
[00:04:16] concrete and it's very visible to get
[00:04:18] excited about the hardware. And
[00:04:20] obviously the hardware you can't do the
[00:04:22] computation.
[00:04:24] But typically what happens is once that
[00:04:26] hardware starts making itself known,
[00:04:28] people want to do stuff with it. And at
[00:04:30] the end it's the software that gives you
[00:04:32] access to that to that compute power and
[00:04:34] your ability to write programs at all
[00:04:38] and then write them maybe quickly and
[00:04:41] also write them effectively starts to
[00:04:43] get in more and more appealing. And
[00:04:46] essentially in the quantum space what we
[00:04:47] now have is this huge number of
[00:04:49] companies
[00:04:50] working on quantum computers, lots of
[00:04:52] different types of QPUs and modalities.
[00:04:55] And as people start engaging more as
[00:04:57] enterprises start adopting and getting
[00:05:00] on onto their quantum journeys,
[00:05:02] they find that they have this challenge
[00:05:04] which is on the one hand you want to
[00:05:06] program a quantum computer, it's not
[00:05:07] easy.
[00:05:09] It requires a lot of skill. And from
[00:05:11] Classic's perspective, you know, we see
[00:05:13] our job as making that something that
[00:05:15] can be done more easily. How can you get
[00:05:17] those domain experts or that domain
[00:05:19] expertise and be able to deploy that in
[00:05:22] how you program. So software is is not
[00:05:24] really second fiddle to hardware at all.
[00:05:26] You know, they they symbiotically need
[00:05:28] one another
[00:05:29] and you need the best of both.
[00:05:34] >> And thank you, Simon.
[00:05:36] In my own view, I think software is very
[00:05:38] important because it's exactly through
[00:05:40] software that we will realize all the
[00:05:42] potential that quantum computing brings,
[00:05:45] right? And all the potential of quantum
[00:05:47] hardware.
[00:05:49] So, if we're thinking about clients that
[00:05:52] you're engaging with and all the
[00:05:54] developments that have been happening in
[00:05:56] the industry, does it shift the
[00:05:58] conversations that you're having? Does
[00:06:00] it raise awareness
[00:06:03] more around quantum computing? Are more
[00:06:05] companies actually gets engaged and
[00:06:08] interested and exploring quantum?
[00:06:13] >> So, yes. I mean, this is this is a this
[00:06:16] is a really exciting time to be in
[00:06:17] quantum. Obviously, you you guys can see
[00:06:20] the activity in in in the financial
[00:06:22] sector and and and across the board in
[00:06:24] terms of how many different players are
[00:06:26] emerging. At Classic, we essentially,
[00:06:28] because we provide that software layer,
[00:06:30] we engage on the one hand we engage with
[00:06:32] the enterprise customers who actually
[00:06:34] want to write the software, who have
[00:06:35] those applications that they need. And
[00:06:38] then, at the other end, you know, we
[00:06:39] connect to the hardware, so we can
[00:06:40] actually deploy those programs and and
[00:06:43] and start looking at what those results
[00:06:45] mean.
[00:06:46] What we have seen over the last, shall
[00:06:48] we say, a couple of years is is a
[00:06:51] dramatic increase in the number of
[00:06:53] companies that are beginning to engage
[00:06:56] with quantum. We're also seeing those
[00:06:58] that have engaged since some time now
[00:07:01] consistently
[00:07:03] deploying more and more sophisticated
[00:07:05] programs,
[00:07:07] having greater aspirations of the kinds
[00:07:09] of applications that they want to
[00:07:11] develop. And this goes across
[00:07:12] industries. So, we see it from the
[00:07:14] finance sector, the telco sector, in
[00:07:17] chemistry, in pharma, in automotive,
[00:07:20] you know, there are applications and use
[00:07:22] cases
[00:07:24] you know, emerging across all of those
[00:07:26] because the hardware has been doing so
[00:07:27] well because those hardware roadmaps
[00:07:30] have pretty much across the board been
[00:07:31] stuck to.
[00:07:33] This means that there's a great you
[00:07:34] know, there's a great deal of faith in
[00:07:37] how those are going to progress. And
[00:07:38] also a lot of activity in that area of
[00:07:41] hybrid. And quantum is primarily going
[00:07:43] to be a hybrid thing for the you know,
[00:07:45] for the near term. Uh, and there's so
[00:07:48] much movement on the you know, on the
[00:07:49] HPC, on the hyperscalers side as well to
[00:07:52] play their part in in this quantum uh,
[00:07:56] sort of transformation of how you do
[00:07:58] computation. And so you have all these
[00:08:00] pieces coming together. You know, the
[00:08:02] the hyperscalers are coming together
[00:08:03] with with the with the QPU, the quantum
[00:08:05] computers. Uh, you know, the software is
[00:08:08] now more approachable. And companies are
[00:08:10] lining up because you can't spin up you
[00:08:12] know, a good quantum team from one day
[00:08:15] to the next. Uh, you need to start you
[00:08:17] need to start planning today.
[00:08:23] >> So we can say that we are right now in
[00:08:26] the hybrid era of quantum, right? And I
[00:08:29] think this is a very interesting
[00:08:31] takeaway also for investors looking at
[00:08:33] the theme because essentially it's
[00:08:36] validates uh, quantum computing utility
[00:08:38] in the near term and it tells that we
[00:08:41] don't have necessarily to wait for
[00:08:43] quantum era to start. But uh, we can use
[00:08:46] quantum computers already today. And
[00:08:49] this is for example what we are seeing
[00:08:51] um, with um, recent press releases from
[00:08:54] Nvidia, right? Um, at the end of last
[00:08:56] year for example, they released NVQ link
[00:08:58] which essentially allows you exactly to
[00:09:01] combine the power of GPUs directly with
[00:09:03] QPUs. We're seeing first data centers
[00:09:06] where QPUs are being directly into the
[00:09:08] integrated with GPUs so that more people
[00:09:11] actually can research all of those um,
[00:09:14] different quantum applications, right?
[00:09:17] And um, maybe just to clarify also for
[00:09:19] the audience when we're saying hybrid
[00:09:21] era, it's essentially leveraging the
[00:09:22] power of quantum in very specific steps
[00:09:26] within a problem, within an algorithm
[00:09:28] that is not um,
[00:09:30] something that is feasible for classical
[00:09:32] machines.
[00:09:34] And this is um, I think great value
[00:09:36] that's uh, the industry can can bring
[00:09:39] already now in the hybrid era. But in
[00:09:42] terms of the applications that you are
[00:09:44] seeing actually from clients, what are
[00:09:46] the most popular ones and what are the
[00:09:49] most popular maybe algorithms?
[00:09:52] >> Sure. I mean we we see a a broad range
[00:09:55] cuz you know, one of the things with
[00:09:56] quantum I think as as with any adoption
[00:09:59] of a new technology is you have to you
[00:10:01] know, you want to do it strategically,
[00:10:02] you want to do it the right way. Some
[00:10:04] companies are working on quite long-term
[00:10:08] computational challenges. They'll need
[00:10:11] much more developed and stable quantum
[00:10:13] computers than
[00:10:15] they're going to be available in the
[00:10:17] near term. Whereas other companies
[00:10:19] look at use cases that perhaps can have
[00:10:22] impact or maybe smaller impact, but
[00:10:25] nevertheless nearer term impact. And so
[00:10:27] you have this this situation where
[00:10:29] companies are essentially working
[00:10:31] through the strategic plans that they
[00:10:33] have, how to properly develop their
[00:10:36] quantum capabilities, how to make sure
[00:10:38] that they tackle the right thing at the
[00:10:40] right time and they have to keep the
[00:10:41] hardware
[00:10:43] in mind. And the way that often meets
[00:10:46] the HPC sector and
[00:10:48] supercomputers is is really in two ways.
[00:10:51] Firstly, it's it's very common to
[00:10:53] actually simulate execution on on a real
[00:10:57] quantum computer using as for example
[00:11:00] GPU clusters, you know, classic we've
[00:11:02] done that recently with Oracle and with
[00:11:05] with AMD and with with Nvidia. And this
[00:11:07] allows those enterprise users to
[00:11:10] actually simulate
[00:11:12] execution on a quantum computer. It's
[00:11:13] quicker,
[00:11:15] it's cheaper and it's effectively as
[00:11:16] good up to a certain number of qubits
[00:11:18] and and that's one use of you know, of
[00:11:21] HPC in quantum today. And and the other
[00:11:24] one is exactly as you said, you know,
[00:11:27] people should really think a little bit
[00:11:28] about
[00:11:29] about these QPUs, uh quantum computers
[00:11:33] uh in the in a similar way to how you
[00:11:34] think about CPUs and and GPUs. You know,
[00:11:37] each one is good for a particular sort
[00:11:39] of family of of computations. And so,
[00:11:43] whilst we call it hybrid today, in a
[00:11:44] sense, it's likely to remain hybrid for
[00:11:47] the foreseeable future. And what you
[00:11:49] want to make sure is uh the part of your
[00:11:51] compute that is best left to the quantum
[00:11:53] computer should go to the QPU. The part
[00:11:56] of it that is better served by the GPU
[00:11:58] or the CPU should go there. And so,
[00:12:00] one's essentially having this
[00:12:02] multi-processing
[00:12:04] uh capability, and you want to make sure
[00:12:07] you use the right the right processor
[00:12:08] and it for the right part of your
[00:12:10] compute.
[00:12:12] >> And Simon, I I um
[00:12:14] love how you sort of laid that out
[00:12:16] because as as you look at the market
[00:12:18] today,
[00:12:19] there's so much focus on
[00:12:23] AI agents and how AI agents changed the
[00:12:27] equation
[00:12:29] from we need lots and lots of GPUs to
[00:12:33] recognizing exactly what you said. GPUs
[00:12:36] are good at a certain set of tasks. CPUs
[00:12:40] become more necessary because of the way
[00:12:43] agents are set up and work and how you
[00:12:46] have to partition some of the workflow
[00:12:48] and you have to think of a certain order
[00:12:50] and if you do it in one order, you might
[00:12:52] get a valuable result. If you do it in
[00:12:54] another order, you might get nonsense.
[00:12:55] And so,
[00:12:56] GPUs cannot literally do everything.
[00:13:00] They have to kind of work together with
[00:13:02] the CPU. And what we've seen in the
[00:13:03] market is the CPU makers suddenly, "Oh
[00:13:06] my gosh, we have shortages." The share
[00:13:08] prices and it's been off to the races. I
[00:13:12] would love to get your perspective and
[00:13:15] how you and and classic maybe walk
[00:13:18] somebody through the idea of they're
[00:13:21] they're used to working on CPUs and
[00:13:24] possibly GPUs.
[00:13:26] And and how do you explain the
[00:13:28] relationship between what the QPU is
[00:13:31] good at relative to maybe what people
[00:13:33] are more familiar with?
[00:13:36] >> Sure. And and and it kind of boils down
[00:13:38] to you know what what the quantum
[00:13:41] algorithms are good at. So, if you're if
[00:13:44] you're looking at uh for example, you
[00:13:47] know, NP-hard type calculations where
[00:13:50] where you know things get exponentially
[00:13:51] harder to to calculate, that's something
[00:13:54] that doesn't typically gel well with uh
[00:13:57] the ways that that either GPUs or CPUs
[00:13:59] work, but does work uh
[00:14:01] well with some of the some of the the
[00:14:03] quantum algorithms. And so, essentially,
[00:14:06] it comes down to the you know to the
[00:14:07] mathematical approach and the way in
[00:14:09] which uh the processor itself can can
[00:14:11] hold information and how many scenarios
[00:14:14] essentially you can have within your
[00:14:15] computational system at at any one time.
[00:14:18] And that's not always going to be
[00:14:19] advantageous uh for the for the quantum
[00:14:22] machine at all. So, you really does
[00:14:24] require you as a business to look at it
[00:14:28] really through two lenses, you know,
[00:14:29] what what what I typically recommend you
[00:14:31] know enterprises who are looking at uh
[00:14:34] at at getting more deeply engaged with
[00:14:35] quantum is you know, you you need to
[00:14:38] have a
[00:14:39] a meaningful business case. You need to
[00:14:40] have some uh you know, real-world
[00:14:42] potential upside from from exploring
[00:14:45] this new technology. And on the other
[00:14:46] hand, you really need to know the you
[00:14:48] know, the technology readiness level of
[00:14:51] what the quantum technologies can offer
[00:14:53] you at any given time. And so, you need
[00:14:56] to keep in mind you know, does this have
[00:14:58] the right kind of business value?
[00:14:59] Do I am I targeting the right use case
[00:15:02] given the hardware context?
[00:15:04] Um and and then typically what one would
[00:15:08] do is you'll build a team
[00:15:10] uh of of of domain experts who perhaps
[00:15:13] have the business knowledge, but also
[00:15:15] some quantum expertise as well. And you
[00:15:17] essentially look at the toolkit, you
[00:15:19] know, these are very different types of
[00:15:20] algorithms. They work differently, the
[00:15:22] compute works differently to how to how
[00:15:24] classical works. You know, I don't think
[00:15:26] this is this is maybe the right you
[00:15:28] know, the right sort of context to start
[00:15:29] diving into the you know, the underlying
[00:15:32] math. But you're able to essentially in
[00:15:35] certain instances where QPUs have an
[00:15:37] advantage, you'll either get an answer
[00:15:40] more quickly um or maybe within a
[00:15:43] feasible time frame, you'll get an
[00:15:45] answer that is more accurate uh and you
[00:15:48] know, probably down the road you'll find
[00:15:50] ways of getting an answer that is
[00:15:51] perhaps uh you know, cheaper to to to
[00:15:54] calculate. And so you're really looking
[00:15:56] for scenarios where
[00:15:58] you can speed up your calculation, drive
[00:16:01] down the cost of the calculation, or or
[00:16:02] just get a better answer. Sometimes it's
[00:16:05] in the context of things that you could
[00:16:07] never calculate, no matter how many CPUs
[00:16:10] and how many GPUs you have because
[00:16:12] certain calculations would take us you
[00:16:14] know, more or less until you know, until
[00:16:16] the end of time for that kind of regular
[00:16:18] computation where you have to work
[00:16:19] through
[00:16:20] in that sort of serial way that a CPU
[00:16:22] would have to. Uh so it's it's really a
[00:16:25] matter of you know, understanding the
[00:16:26] business, uh understanding the right
[00:16:29] algorithmic approach, and timing it
[00:16:31] correctly so that it has quantum
[00:16:34] hardware that can actually deliver.
[00:16:37] >> And and Simon, I'm I'm curious
[00:16:40] how much time you and your colleagues at
[00:16:44] Classic spend because
[00:16:47] in in many cases as you as you sort of
[00:16:49] dig into this topic uh you might have a
[00:16:52] specific problem. For instance, you you
[00:16:54] might be trying to do a computational
[00:16:57] fluid dynamics simulation that leads you
[00:17:01] to design a better jet engine, a better
[00:17:04] propeller, a better something that has
[00:17:07] to do with blades circulating through
[00:17:10] the wind. And from what I've seen is
[00:17:15] there are different ways that you can
[00:17:17] specify the problem. There are different
[00:17:18] ways that you can set it up and
[00:17:21] depending on how you set it up, it it
[00:17:23] immediately impacts for instance the
[00:17:25] time potential of the computation,
[00:17:27] whether you can do a full optimization
[00:17:30] against all
[00:17:32] global possibilities or if you get sort
[00:17:34] of stuck in a local maxima or local
[00:17:37] minima and and ultimately
[00:17:40] the specification angle and something
[00:17:42] I'm curious about is because in today's
[00:17:44] world again a big thing that you hear is
[00:17:47] oh, people don't need to have
[00:17:50] software expertise anymore because you
[00:17:51] can just vibe code. Like you want the
[00:17:54] computer to do something in the past you
[00:17:56] had to know your C++ or your Python.
[00:17:59] Today you just go into your cloud code
[00:18:02] or your code X or whatever you're using
[00:18:04] and you tell the idea that you're
[00:18:06] looking to achieve and it just converts
[00:18:08] it to computer code and I'm I'm
[00:18:11] wondering if
[00:18:13] AI models even have enough training data
[00:18:16] to be able to take whether it's a
[00:18:18] computational fluid dynamics situation,
[00:18:20] a chemistry situation, an encryption or
[00:18:23] a factoring situation and to to be able
[00:18:27] to in a useful way convert the
[00:18:30] specification of the problem into
[00:18:32] something that could then be dealt with
[00:18:35] through a series of quantum algorithms
[00:18:37] or if in today's world the idea of vibe
[00:18:40] coding and AI really doesn't quite touch
[00:18:43] what we're talking about at least not
[00:18:45] yet.
[00:18:46] >> Yeah. I mean
[00:18:48] CFD computational fluid dynamics is is
[00:18:50] often times you know very large, very
[00:18:54] compute heavy types of calculations.
[00:18:57] Often using classical methods you you
[00:18:59] have to decide how much granularity you
[00:19:02] want to have in that analysis versus the
[00:19:04] computational cost that it gives you and
[00:19:06] it's around those places where that
[00:19:08] computational overload
[00:19:10] you know it as if
[00:19:12] you know, there may be you know,
[00:19:14] quantum algorithms that are actually
[00:19:16] going to allow you to have great
[00:19:18] accuracy. And you could go from having
[00:19:21] what some people would call you know,
[00:19:22] today maybe you have a digital twin.
[00:19:24] And you eventually have quantum twin.
[00:19:28] And sometimes I sort of you know, look
[00:19:29] at it as kind of analogous to and I'll
[00:19:32] age myself here, but you know, when you
[00:19:34] looked at how MP3s were were sort of
[00:19:36] compressed, you know, how much you know,
[00:19:38] how much can your ears pick up on that
[00:19:41] on that spectrum of sound and what can
[00:19:43] you live with and when it comes to how
[00:19:45] much compression? And so, it's maybe a
[00:19:46] little a little bit like that when
[00:19:47] you're doing you know, CFD analysis. You
[00:19:50] know, how much you know, how much
[00:19:51] precision do you need? And as you get
[00:19:53] into those those sort of
[00:19:55] sort of quantum avenues, you can just
[00:19:57] deal with more data, you'll get more
[00:19:59] granularity, you'll get a better
[00:20:01] representation of what the world is. So,
[00:20:03] that's that's what people are aspiring
[00:20:05] to do. The hardware for those really you
[00:20:07] know, really big calculations and this
[00:20:09] is the sort of stuff that you know, that
[00:20:11] we're looking into with with Rolls-Royce
[00:20:13] for example.
[00:20:14] Yeah, those computations are going to be
[00:20:16] some way down the road. That quantum
[00:20:18] hardware isn't what's imminent. You
[00:20:20] know, the inflection point of full
[00:20:22] tolerance which you know, is going to
[00:20:23] come in the next couple of years will
[00:20:25] likely nearer term affect either
[00:20:28] subroutines or smaller problems. And as
[00:20:31] the hardware develops, you know, the
[00:20:32] bigger and bigger challenges will come.
[00:20:35] So, you know, when you're doing
[00:20:36] something like CFD, what you need what
[00:20:38] you need to do is which which you know,
[00:20:40] are we going to do the the all singing
[00:20:42] all dancing thing? You do need to start
[00:20:44] building out that capability over time,
[00:20:45] but it's maybe not imminent.
[00:20:47] Which nearer term subroutines
[00:20:50] could you actually develop so that you
[00:20:52] could do part of your calculation using
[00:20:55] using that quantum approach? And so,
[00:20:58] even within something as as exciting as
[00:21:00] CFD, there's there's a strategic there's
[00:21:03] a more strategic approach to sort of
[00:21:05] break that down into smaller chunks and
[00:21:07] you get some will remain classical for
[00:21:08] some time to come, and certain aspects
[00:21:11] will go quantum somewhat earlier.
[00:21:17] >> Simon, I actually wanted to bring the
[00:21:20] discussion on algorithms into the
[00:21:21] finance realm, and something where I had
[00:21:26] my hands-on experience, and this is
[00:21:29] quantum sorry, Monte Carlo. And then
[00:21:32] obviously, I wanted to ask you to
[00:21:35] introduce what is quantum Monte Carlo
[00:21:37] and how it's different. Maybe just for
[00:21:40] the benefit of the audience here, just
[00:21:41] to clarify what is
[00:21:43] classical Monte Carlo. It's essentially
[00:21:46] you're running a lot of random
[00:21:48] simulations trying to
[00:21:50] get what the expected value or like
[00:21:54] average value of all of those
[00:21:55] simulations could be. What is your
[00:21:57] expected outcome? And one of the
[00:21:59] applications that
[00:22:02] we can give in the finance realm is
[00:22:05] derivatives pricing.
[00:22:06] So this is something that I did myself
[00:22:09] as part of university project, and I'm
[00:22:13] very curious to to hear from you because
[00:22:15] I know that classic
[00:22:17] is actually engaged in in this area,
[00:22:20] and your perspective on quantum Monte
[00:22:23] Carlo and how it can deliver value
[00:22:25] versus classical Monte Carlo.
[00:22:27] >> My expertise in in Monte Carlo is
[00:22:29] probably relatively is relatively second
[00:22:32] secondary to yours, but it's it's it all
[00:22:35] comes back to this notion of you know,
[00:22:37] how much granularity can you have? How
[00:22:38] many scenarios are you able to
[00:22:42] simulate, and how many you know, how
[00:22:44] quickly can you do so? And so it'll
[00:22:46] it'll come down to accuracy, speed of
[00:22:48] compute,
[00:22:49] and what what you can essentially
[00:22:51] achieve that will move things a little
[00:22:53] bit
[00:22:54] compared to compared to the classical
[00:22:56] approaches. And this is what a lot of
[00:22:58] the enterprise folks typically do, where
[00:23:00] you'll take your you know, traditional
[00:23:02] Monte Carlo approach uh and then work
[00:23:05] through an alternate uh quantum Monte
[00:23:07] Carlo approach and essentially look for
[00:23:10] you know, that that compare and contrast
[00:23:13] to see where one may and one may not
[00:23:15] always uh get an advantage, but one is
[00:23:17] looking for an advantage. Um and that
[00:23:20] that is something where probably
[00:23:22] nowadays on the whole you know, it's
[00:23:24] it's it's still not the case that the
[00:23:27] the quantum approaches typically return
[00:23:29] something that is going to be
[00:23:31] better than the best practice in current
[00:23:35] uh current approaches to these kinds of
[00:23:37] things in in finance.
[00:23:39] So, it's it's a it's it's it's this
[00:23:41] period where uh you can work on the
[00:23:44] software, you can deploy those
[00:23:46] algorithms, you're probably not going to
[00:23:48] get uh better computational results in a
[00:23:51] in 2026
[00:23:53] uh but depending on what it is you're
[00:23:54] track you're tackling, you may well find
[00:23:56] that
[00:23:57] you know, 2027, 2028, 2029, these are
[00:24:00] the years where aspects of these
[00:24:03] calculations uh you'll do a side-by-side
[00:24:05] comparison and find at least parts of it
[00:24:08] uh that are advantageous if you follow
[00:24:10] the quantum route.
[00:24:14] >> I'm actually quite curious just to
[00:24:16] clarify here an important point. Um as
[00:24:18] you told that
[00:24:20] the result might not be better in 2026.
[00:24:24] So, is it the limitation of the quantum
[00:24:27] hardware or is it also due to the
[00:24:29] algorithms as well? Because that might
[00:24:31] bring us, you know, like to the topic of
[00:24:33] um
[00:24:34] algorithm discovery and maybe writing
[00:24:36] better quantum algorithms.
[00:24:41] >> Yeah. Well, I mean, it it it's certainly
[00:24:43] without a doubt, you know, that the
[00:24:44] hardware that that isn't that isn't
[00:24:46] ready for, you know, for larger
[00:24:48] calculations. We're still in this NISQ
[00:24:50] era and that certainly makes things, you
[00:24:52] know, hybrid uh and one might find
[00:24:54] certain small subroutines that might be
[00:24:57] better, uh but it it's really a
[00:24:59] combination of the two. So, the hardware
[00:25:01] is going to get better and we see that
[00:25:03] happening, you know, almost, you know,
[00:25:05] quarter by quarter, month by month. Um
[00:25:07] and and then, you know, the algorithmic
[00:25:10] side also needs, you know, to have, you
[00:25:13] know, a lot of work done. So, there are
[00:25:15] core kind of foundational uh and
[00:25:18] algorithms that are very, you know, that
[00:25:19] are very well established in in quantum
[00:25:22] at this point. But, as with, you know,
[00:25:24] as with any sort of algorithmic
[00:25:25] approach, you know, the devil the devil
[00:25:27] is in the in the details of how you use
[00:25:29] those those particular algorithms, uh
[00:25:32] you know, which approaches you decide to
[00:25:33] take for this very specific uh use case
[00:25:36] that a team uh may be working on. And
[00:25:38] so, there's there's, you know, there's
[00:25:41] a clear barrier from the hardware, but
[00:25:43] we find that a lot of these quantum
[00:25:44] teams and they're working on
[00:25:47] uh you know, subsections of these
[00:25:49] computational uh routines they want to
[00:25:51] be able to deploy in the future. And
[00:25:54] this requires, you know, a lot of a lot
[00:25:55] of smart people to do a lot of smart
[00:25:57] thinking. And, you know, back back maybe
[00:25:59] to Chris's uh previous point about, you
[00:26:01] know, how does this meet, you know, how
[00:26:02] does this meet AI and do you actually
[00:26:05] have to know everything? I I think the
[00:26:07] answer is that um what's happened
[00:26:09] recently in quantum is is quite
[00:26:12] remarkable and both on the hardware
[00:26:13] side, but also on software. Um you know,
[00:26:16] not not not wanting to to toot Classics
[00:26:18] horn too much, but Classic was founded
[00:26:20] in in 2020. Then, if you looked at the
[00:26:23] software landscape in quantum then, uh
[00:26:25] we were, you know, very much in the
[00:26:27] scenario where you know, this was quite
[00:26:29] an undeveloped software stack. A lot of
[00:26:31] the coding had to be done at a very very
[00:26:33] low level, which meant that you had to
[00:26:35] be an expert not just on the domain
[00:26:37] issues, you had to be an expert on the
[00:26:39] quantum algorithms, but you also had to
[00:26:41] have deep understanding of the hardware,
[00:26:43] the specific hardware that you wanted to
[00:26:45] execute your your program on. And
[00:26:48] that's, you know, that's pretty low low
[00:26:50] down the stack. That's, you know, for
[00:26:52] folks who are active in in classical
[00:26:55] computing maybe in the you know, 50s,
[00:26:56] 60s, 70s, this is you know, assembly
[00:26:59] language, Fortran kind of kind of
[00:27:01] context. Um and what's happened in the
[00:27:04] in the quantum space on the software
[00:27:05] side
[00:27:06] uh is that probably in the last you
[00:27:07] know, 5 to 6 years uh has happened more
[00:27:11] or less what happened in in the last
[00:27:12] sort of 50 or 60 in classical. And so
[00:27:15] you can now uh engage with quantum
[00:27:17] software using AI uh coding assistants.
[00:27:21] Uh you don't have to know everything
[00:27:23] yourself. You know, Classic we really we
[00:27:25] really made this a a core focus cuz we
[00:27:28] encounter so many domain experts who
[00:27:30] have all these great ideas about exactly
[00:27:32] what they would want to do you know, uh
[00:27:34] with their
[00:27:36] um you know, risk or or sort of pricing
[00:27:38] calculations,
[00:27:40] um and that domain expertise doesn't
[00:27:43] usually reside with the same people that
[00:27:45] have the quantum expertise. Uh and you
[00:27:48] know, so our mission was how can we go
[00:27:51] even further up that quantum stack? How
[00:27:53] can we introduce an agentic approach? So
[00:27:55] go beyond just essentially code snippets
[00:27:58] that maybe or may uh
[00:28:00] maybe won't work on hardware. Because if
[00:28:03] you code at a low level, you have to
[00:28:05] code it for a specific machine and as
[00:28:07] soon as that machine changes, your code
[00:28:09] isn't going to work. And in a context
[00:28:11] like quantum, machines are changing the
[00:28:13] whole time. And if you've developed your
[00:28:15] software for for yesterday's machine,
[00:28:18] rewriting that, you know, with low-level
[00:28:20] code is going to be really, really
[00:28:21] tough.
[00:28:22] Um and so we we recently introduced an
[00:28:24] an agentic approach essentially that
[00:28:26] context that Chris was wondering about.
[00:28:28] Yeah, there isn't a lot of context out
[00:28:29] there, certainly not like there is for
[00:28:31] for classical. So those AI coding uh you
[00:28:34] know, helpers or agents um don't have
[00:28:37] that much uh to go on and it's certainly
[00:28:40] not something that is is going to be
[00:28:42] easy you know, generically for all kinds
[00:28:45] of systems. Um and so we've we've
[00:28:47] actually built our own our own algorithm
[00:28:50] and and application library to give that
[00:28:52] context. Um, but our agentic approach
[00:28:55] relies on what we do downstream as well.
[00:28:57] So, you can use natural language, you
[00:29:01] can express the question you want to ask
[00:29:03] just as you would, you know, of a
[00:29:04] colleague verbally.
[00:29:06] And being able to use that context of
[00:29:08] the algorithm libraries plus the
[00:29:10] application libraries plus them the
[00:29:13] ability to create code that is
[00:29:17] that is hardware independent
[00:29:19] is is now very much what you can do in
[00:29:22] in quantum. So, if you have domain
[00:29:23] expertise and you are comfortable, you
[00:29:27] know, vibe coding essentially, then much
[00:29:31] of that now exists in in quantum and
[00:29:34] certainly via classic you'll know that
[00:29:37] what is produced through that process is
[00:29:39] correct and is implementable and is
[00:29:41] executable.
[00:29:43] And should the hardware change, which it
[00:29:44] does frequently,
[00:29:46] you don't have to redo that from the
[00:29:48] ground up. You have your model, you have
[00:29:50] your asset essentially, which you can
[00:29:52] redeploy. And this is also, you know,
[00:29:54] one of these other things that the the
[00:29:56] quantum teams now struggle with, which
[00:29:58] is because there's so many players, they
[00:30:00] need to benchmark. You know, is there
[00:30:02] something that's going to work better on
[00:30:04] an IonQ machine or a Rigetti machine or
[00:30:06] an IBM machine? They're different
[00:30:07] modalities, they're different providers,
[00:30:10] and they all have their pros and cons,
[00:30:12] and you also don't know who's going to
[00:30:13] be ahead in 12 months time.
[00:30:15] And so this really means that
[00:30:16] portability of your code gets really
[00:30:18] important.
[00:30:19] Your ability to deploy it on various
[00:30:21] backends, but primarily, you know, how
[00:30:24] do you compare and contrast? Not just
[00:30:26] which machine is maybe better absolutely
[00:30:29] at any given time. It might be at the
[00:30:31] algorithmic level that I've developed a
[00:30:33] particular application, and this
[00:30:34] particular application works better on
[00:30:37] the IonQ machine than the IBM machine,
[00:30:39] but the other application that I have
[00:30:42] works better on the IBM machine than the
[00:30:44] IonQ one. And so this, particularly in a
[00:30:46] dynamic environment, you do need to have
[00:30:49] the ability to deploy in these these
[00:30:51] sort of agentic approaches cuz it's it's
[00:30:53] a very very steep learning curve
[00:30:56] if you don't have that kind of assist.
[00:30:59] >> And and Simon, as we as we have this
[00:31:01] conversation, Quantinuum is out there
[00:31:03] doing a road show getting ready for a
[00:31:06] possible IPO documents filed filed with
[00:31:10] the SEC earlier this week as we're
[00:31:13] speaking. And so we're probably going to
[00:31:15] hear more and more about the Quantinuum
[00:31:17] machine and how it compares. So it's it
[00:31:19] is a fascinating world to think in terms
[00:31:22] of the different machines, the different
[00:31:25] modalities. But something you got me
[00:31:27] thinking about as you're explaining sort
[00:31:29] of the proposition that the user of the
[00:31:33] classic software gets is in in the world
[00:31:37] of quantum you you hear a lot and I feel
[00:31:39] like I've IBM has done a great job of
[00:31:41] positioning the Kiskit sort of library.
[00:31:46] Obviously, Nvidia anything Nvidia says
[00:31:49] in 2026 is, you know, trumpeted around
[00:31:52] the world. So if they're talking about
[00:31:54] their Ising model, they're talking about
[00:31:56] CUDA-Q as as Elvira mentioned, NVQ link,
[00:32:00] all these different things,
[00:32:02] you get the impression they would love
[00:32:05] if quantum really takes off or when
[00:32:07] quantum really takes off, you get the
[00:32:09] impression they would love to be
[00:32:11] in the same position where they seem to
[00:32:13] be with AI and CUDA
[00:32:15] and have a version of that going for
[00:32:17] quantum. How how does what classic is
[00:32:21] doing in the in the classic approach
[00:32:22] compared to either say Kiskit or what
[00:32:26] Nvidia is doing that that people cuz in
[00:32:29] in reality people have probably heard
[00:32:30] about Nvidia in some context. And if you
[00:32:34] start looking at quantum particularly
[00:32:35] now after the US government put half of
[00:32:38] the value that they announced investing
[00:32:41] in IBM. IBM is getting a lot of
[00:32:43] attention.
[00:32:44] So how how does what Classen does
[00:32:47] compare to those?
[00:32:49] >> Yeah, um
[00:32:50] In a In a sense, we we we collaborate
[00:32:54] with with both with IBM and and and with
[00:32:57] Nvidia and they're complementarities.
[00:32:59] But I think as as with any sort of
[00:33:01] relatively early stage technology,
[00:33:04] exactly where those those boundaries and
[00:33:06] borders you know end up being drawn
[00:33:09] is is is a bit of a moving feast. But
[00:33:12] you know
[00:33:13] to take your your your sort of question
[00:33:15] around around Kiskit, you know, IBM were
[00:33:18] obviously very very early movers in
[00:33:20] quantum and they've put a great deal of
[00:33:22] effort into it and they they they
[00:33:24] focused I think you could say initially
[00:33:26] on the hardware. And they also, in order
[00:33:29] to make that that hardware usable,
[00:33:31] accessible, they they developed the
[00:33:33] Kiskit language which is by far the most
[00:33:36] established programming language.
[00:33:39] It has its roots
[00:33:41] you know back in the back in the 2010s.
[00:33:44] Um and and it's an amazing tool. It's
[00:33:46] the it's the default learning tool if
[00:33:48] you want to learn quantum computing. But
[00:33:50] you do probably still want to have that
[00:33:52] deep understanding of the of the
[00:33:55] hardware and how that interacts with
[00:33:57] your software. You know, Kiskit is is
[00:33:59] without a doubt the the sort of de facto
[00:34:02] standard
[00:34:04] certainly for education.
[00:34:05] And then as you start getting into you
[00:34:07] know more specific applications, there
[00:34:09] are you know there are various other
[00:34:10] languages and obviously Continuum have
[00:34:12] have their approaches and and some of
[00:34:14] the other hardware providers have have
[00:34:16] their languages as to the as to the as
[00:34:18] to the clouds.
[00:34:19] Um what what Classic essentially is is
[00:34:22] focused on is really taking that
[00:34:24] abstraction journey as far as one can.
[00:34:27] So can you create
[00:34:29] a and it's not
[00:34:32] you know we call it a modeling language.
[00:34:33] So, what we want to allow people to do
[00:34:35] is essentially work in an environment
[00:34:37] that is
[00:34:38] pretty Pythonic. So, if you speak
[00:34:39] Python, you know, you can you can code
[00:34:42] Classics QMod
[00:34:44] uh
[00:34:45] you know, modeling language.
[00:34:46] And we do that for a very specific
[00:34:48] reason, which is that we want to
[00:34:50] separate your modeling, which is how you
[00:34:52] mathematically express the question that
[00:34:55] you want to have answered from the
[00:34:58] implementation of that model, how that
[00:35:01] then gets into code that is executed on
[00:35:04] on a computer. And if you can separate
[00:35:07] on the one hand the model and on the
[00:35:09] other hand the implementation, that
[00:35:11] means that if something happens around
[00:35:14] the back end or you have some preference
[00:35:16] about how that model should be
[00:35:18] implemented, um you know, you don't have
[00:35:20] to change your modeling. If you've got a
[00:35:22] great model, that might be a model for
[00:35:24] life. Whereas, you know, the way you
[00:35:26] choose to run it could change, you know,
[00:35:28] dramatically from uh from period to
[00:35:30] period. And so, Classics essentially has
[00:35:32] these these these two components. One is
[00:35:34] a very high-level modeling language. Um
[00:35:37] and that connects to a
[00:35:40] a form of compilation.
[00:35:42] Essentially, what what our software then
[00:35:44] does is is it automates how you turn
[00:35:47] that into an executable program.
[00:35:49] Uh and this and this is the workflow,
[00:35:51] you know, that that we believe is is the
[00:35:53] right approach for for enterprise users.
[00:35:56] It's all about you know, establishing a
[00:35:58] route from idea through to, you know,
[00:36:01] executable program
[00:36:03] in a way that's as accessible to as many
[00:36:05] people as possible, but is also, you
[00:36:07] know,
[00:36:08] repeatable, correct, um and creates
[00:36:11] assets rather than than one-off
[00:36:13] experiments. So, the the folks that we
[00:36:16] work with, they'll you know, they'll use
[00:36:18] that Agilentic front end. They can use
[00:36:20] natural language. That will create that
[00:36:23] model that
[00:36:24] sort of Pythonically expressed
[00:36:25] mathematical model of what it is we want
[00:36:28] to happen, then compilation
[00:36:31] automatically matches that and
[00:36:33] implements it for a particular hardware.
[00:36:35] So, if you did want that IBM machine or
[00:36:37] that IonQ machine or that Rigetti
[00:36:39] machine or the continuum machine, um
[00:36:42] then you adjust essentially accordingly
[00:36:45] because each one of those has different
[00:36:47] connectivities, is a different modality,
[00:36:50] um and essentially at a you know, at the
[00:36:52] click of a button, you can take your
[00:36:53] model and adjust it for whatever
[00:36:55] hardware is relevant at any given time.
[00:36:57] Uh that makes it a much higher level uh
[00:37:00] modeling environment. It allows you to
[00:37:02] keep things um synthesizable or
[00:37:04] re-compilable every time there's a
[00:37:06] change on the hardware end. Um because
[00:37:09] of that agentic uh approach at the
[00:37:11] beginning, which does have uh both
[00:37:14] algorithm and application context, uh
[00:37:16] you can genuinely start with a natural
[00:37:18] language spoken uh you know, spoken
[00:37:21] instruction.
[00:37:22] You You inevitably, you know, want to
[00:37:24] have You probably And what that means
[00:37:26] from an enterprise perspective is, you
[00:37:28] know, you're still going to want to have
[00:37:29] a uh a quantum PhD somewhere on the
[00:37:32] team, but you can have domain experts
[00:37:35] being those that actually, you know,
[00:37:37] kick things off and ask the questions
[00:37:38] maybe in in a smarter way from the
[00:37:40] perspective of of of the business
[00:37:42] interest.
[00:37:44] >> And And Simon, I'm I'm I'm curious
[00:37:47] because um one of the best aspects of
[00:37:50] sort of sit sitting in the seat that
[00:37:52] Elvira and I get to sit in is you you
[00:37:54] speak to so many different kinds of
[00:37:57] people, and anytime we speak to somebody
[00:38:00] who's kind of in the quantum space uh in
[00:38:04] 2026,
[00:38:05] what you're hearing, and it's come
[00:38:07] through today in a lot of your remarks,
[00:38:09] is a certain degree of strong confidence
[00:38:13] in the road map, that we are on this
[00:38:16] journey, and progress is being made, and
[00:38:19] there there are strong chances, even
[00:38:21] though obviously every issue is not
[00:38:23] fully figured out as we have this
[00:38:25] conversation, there there are strong
[00:38:26] chances that progress continues and
[00:38:29] we're on uh a very positive journey.
[00:38:32] What kinds of
[00:38:35] things, signposts along the way, because
[00:38:37] frequently when we speak to investors,
[00:38:39] they're sitting there going like,
[00:38:41] how do I know if a given announcement is
[00:38:45] truly impactful and exciting and and is
[00:38:47] really going to
[00:38:49] provide something of value? And And you
[00:38:52] think back in recent years, the Google
[00:38:54] making the Willow announcement, that was
[00:38:56] that was obviously impactful and
[00:38:58] exciting. Elvira mentioned the IonQ
[00:39:00] networking uh the two systems together
[00:39:04] uh about 6 weeks ago from as we're
[00:39:06] making this recording, that was
[00:39:07] obviously exciting. So, there are
[00:39:09] certain things that are obviously
[00:39:10] exciting, but as as sort of a
[00:39:12] practitioner and and when you're getting
[00:39:15] together with your your colleagues, what
[00:39:17] kinds of things as you sort of look
[00:39:20] forward through 2026, 2027 and beyond,
[00:39:23] what kinds of things would get you and
[00:39:25] your team excited to see as you're
[00:39:28] you're sort of helping people understand
[00:39:30] how to analyze the just vast amount of
[00:39:33] information that's coming out seemingly
[00:39:35] all the time uh about quantum,
[00:39:37] particularly because the US government's
[00:39:39] announcement last week. I don't know if
[00:39:41] that's going to advance the science
[00:39:43] immediately. I do know that the space is
[00:39:45] now going to get so much more attention,
[00:39:47] there going to be so many more
[00:39:48] headlines. That doesn't mean all the
[00:39:50] headlines are, you know, of equal value
[00:39:52] and parsing through what's truly
[00:39:54] important versus just what's an
[00:39:56] announcement that's just sort of there,
[00:39:58] that may have just gotten uh a little
[00:40:01] bit harder.
[00:40:03] >> Yeah. Um
[00:40:04] look, I I I I think it's inevitable.
[00:40:06] This is Yeah, this is still relatively
[00:40:08] early days for quantum. This This is a
[00:40:11] technology that in all probability is
[00:40:13] going to mature, you know, over decades,
[00:40:15] just as classical computing did. That
[00:40:17] that doesn't mean that the era we're in
[00:40:19] now isn't a very exciting one and isn't
[00:40:21] going to stop
[00:40:23] um and launching all kinds of new ideas
[00:40:26] and new abilities in the near term, but
[00:40:27] this is this is going to take some time
[00:40:30] uh to play out. And I think that yeah
[00:40:33] there are there there are a few things.
[00:40:35] On the one hand, you mentioned the
[00:40:36] government support. I think that's a
[00:40:38] pretty good bellwether uh
[00:40:40] at a at a very kind of high level of uh
[00:40:43] you know, the importance of the sector
[00:40:45] and also the backing that it gets. I
[00:40:46] mean, it wasn't it wasn't just in the
[00:40:48] US, but you actually had similar sums
[00:40:51] announced in the UK and announced in
[00:40:53] France recently. Um and the the the
[00:40:56] majority of, you know, major major
[00:40:59] economies are are putting those kinds of
[00:41:03] uh you know, big big-ticket sums into
[00:41:05] moving quantum along. And and it's also,
[00:41:09] I think,
[00:41:10] visible that that sort of government
[00:41:13] backing, which might originally have
[00:41:15] have been focusing more on on the sort
[00:41:18] of the hard science and and the ability
[00:41:21] to create the the quantum computers at
[00:41:23] all,
[00:41:24] you know, there now aspects that one
[00:41:26] sees are more earmarked for you know,
[00:41:28] application development and workforce
[00:41:30] training and other ways in which you
[00:41:33] know, the rubber really hits the road.
[00:41:35] So, I think there's you know, there's
[00:41:36] this
[00:41:37] significant government backing, but we
[00:41:38] also see it's, you know, it's not just
[00:41:40] about the hardware anymore and that
[00:41:42] goes, I think, across all of these
[00:41:43] jurisdictions. Um the other thing is
[00:41:45] there are loads of QPUs, which is great,
[00:41:47] and they're not all going to win and
[00:41:49] it's probably not that there's going to
[00:41:50] be one one runaway winner either. You
[00:41:53] know, there going to be multiple players
[00:41:54] here. Um and as those roadmaps uh get
[00:41:58] announced and get get uh get stuck uh
[00:42:00] stuck to, which seems to be the case, I
[00:42:03] think it would be a very a very, you
[00:42:05] know, scary moment uh you know, for the
[00:42:08] quantum ecosystem as a whole
[00:42:10] uh to have, you know, one of these
[00:42:12] significant hardware providers, you
[00:42:14] know, dramatically fail on on meeting
[00:42:16] their commitments on the on their road
[00:42:17] maps because I think there's a, you
[00:42:19] know, there's a lot of
[00:42:20] uh, there's a lot of faith that's been
[00:42:22] earned and a lot of trust that's been
[00:42:23] earned by the ways in which this is uh,
[00:42:25] been done so far. Uh, so more more than
[00:42:29] looking for, you know, the maybe one of
[00:42:31] you're looking for
[00:42:32] what, you know, what would give people
[00:42:34] confidence. I think the confidence is
[00:42:35] there. It's that we can't afford to have
[00:42:38] signs that things are slipping. So, I
[00:42:40] think that's, yeah, that's almost how
[00:42:41] we'd look at it the hardware side of
[00:42:42] things. Um, and then and then when it
[00:42:46] comes to announcements and people often
[00:42:48] hear these announcements, there's
[00:42:49] quantum supremacy or there's quantum
[00:42:51] advantage or quantum, you know,
[00:42:53] something that has been expressed. Um,
[00:42:55] and you know, one one always wants to
[00:42:58] take a, you know, kind of sanguine look
[00:43:00] at these things. Fortunately, the
[00:43:01] quantum sector itself is is actually by
[00:43:05] its nature, I think, uh, a little bit
[00:43:08] anti-hype. Um, and is quite
[00:43:10] self-critical and is quite uh, cautious.
[00:43:14] And uh, because you have uh, this
[00:43:17] ecosystem of people who, you know, all
[00:43:19] of these, you know, all of these ships
[00:43:20] will rise and fall to an extent uh, by
[00:43:23] the responsibility this industry shows
[00:43:26] as a whole. Um, it's, you know, it's
[00:43:29] it's it's
[00:43:30] often quite easy after announcements and
[00:43:33] then look around and see how the quantum
[00:43:35] community themselves react to news.
[00:43:37] Because these are these are things that
[00:43:38] are actually often very technical, very
[00:43:40] complex. Um, companies, of course, are
[00:43:43] incentivized to present themselves in
[00:43:45] the best possible light and certain
[00:43:47] things do really matter, you know. Um,
[00:43:50] coherence in in the hardware,
[00:43:52] improvements in that really matter.
[00:43:55] Improvements in error correction can
[00:43:57] dramatically move uh, can dramatically
[00:43:59] move the needle. Um, a yeah, a new way
[00:44:02] of speeding up how an algorithm is
[00:44:04] actually implemented can dramatically
[00:44:06] matter. And all of those types of
[00:44:08] announcements very quickly going to get
[00:44:10] a get a lot of scrutiny
[00:44:12] from from the peers in the ecosystem.
[00:44:15] And I actually think in in many ways
[00:44:18] one needs to you need to look at how the
[00:44:20] industry itself polices itself and
[00:44:22] reacts to one to the other. And I think
[00:44:24] it does a good job of that.
[00:44:30] >> Simon, I believe we are approaching
[00:44:32] actually the end of our episode. Time
[00:44:35] has flown by indeed.
[00:44:37] And I am curious actually to hear the
[00:44:40] key messages that you would want to
[00:44:42] share with two groups. First, the
[00:44:45] companies that are looking to explore
[00:44:48] quantum.
[00:44:49] And then investors who are looking at
[00:44:52] quantum as an investment theme. So
[00:44:54] starting with the first group. What
[00:44:57] would you like to highlight as those
[00:45:00] companies and teams are starting their
[00:45:02] quantum journey. Obviously any quantum
[00:45:04] journey includes quantum software.
[00:45:07] And there are some important
[00:45:08] considerations. For example, do you want
[00:45:11] you know like to use quantum hardware
[00:45:12] directly that access might be quite
[00:45:14] expensive or maybe you can also start
[00:45:16] with quantum simulation to for for
[00:45:19] certain problems and things and maybe
[00:45:21] some some other considerations as well.
[00:45:27] >> Sure. Now I think you know the the
[00:45:29] bottom line is that if you if you are a
[00:45:32] company that has activities
[00:45:35] that are likely to be
[00:45:38] in some ways
[00:45:40] affected by improvements in optimization
[00:45:44] or in simulation for example. If you
[00:45:48] have activities that are exposed
[00:45:51] possibly positively you know to what
[00:45:54] will happen when quantum algorithms and
[00:45:56] quantum hardware start spinning up which
[00:45:58] they will in in the relatively near
[00:46:00] future. You need to have a
[00:46:03] well-thought-through plan of how you
[00:46:06] engage. Now, it's okay if you don't you
[00:46:08] know if you don't have those kinds of
[00:46:09] activities and it's not strategic for
[00:46:11] you, then you should wait.
[00:46:13] Um if on the other hand you do, then you
[00:46:15] should engage and you should engage
[00:46:17] properly. Um and really from the
[00:46:19] enterprise perspective, you know at at
[00:46:21] this point, you don't need to own any
[00:46:23] hardware. You can access everything, you
[00:46:25] know all the hardware is accessible via
[00:46:27] the cloud. You can access it via Azure,
[00:46:30] via AWS bracket, you know
[00:46:33] via via some of the software players
[00:46:35] like like classic directly as well. And
[00:46:37] so it's it's more about if this is
[00:46:40] important,
[00:46:41] it's not going to take you a year or two
[00:46:43] uh to spin up your activities and it's
[00:46:45] certainly going to take consistent
[00:46:47] effort to build a team, to build that um
[00:46:50] talent pool, to build that
[00:46:52] infrastructure of uh of work through our
[00:46:55] applications
[00:46:56] uh because you don't want to be the
[00:46:58] company that wakes up one morning to
[00:47:00] discover that you know your competitors
[00:47:02] are deploying algorithms that are just
[00:47:04] streets ahead of what you have.
[00:47:06] Um and you know now is really the time
[00:47:09] to start doing that given what one sees
[00:47:11] in the hardware context. But you want to
[00:47:13] do it properly. So, you know you want to
[00:47:15] do it uh so that you are able to make
[00:47:18] sure your software is an asset rather
[00:47:20] than an expense. You want to make sure
[00:47:22] that you have you know a process that
[00:47:25] allows you to remain flexible and deal
[00:47:27] with the inherent risk of of change
[00:47:29] within this still emerging technology.
[00:47:31] Uh and so obviously you know that's
[00:47:33] that's what from a classic perspective I
[00:47:35] say that's what we really want to help
[00:47:37] people do which is you know
[00:47:39] operate at a higher level in terms of
[00:47:41] your soft uh software development, and
[00:47:43] be able to implement it automatically,
[00:47:46] have things that are shareable, that are
[00:47:47] transferable, and adjustable you know as
[00:47:50] the as those back ends change.
[00:47:52] Um and that that obviously is my
[00:47:54] interest to say but that's really what
[00:47:55] we built classic to give which is an,
[00:47:57] you know, an enterprise, you know,
[00:47:58] scalable approach uh to turn, you know,
[00:48:01] quantum activity into quantum assets.
[00:48:03] >> So, what would be your key messages for
[00:48:06] investors here?
[00:48:11] >> All right. Well, for investors, you
[00:48:13] know, look look at what's happening in
[00:48:14] the private markets. If you look at the
[00:48:16] amount that's being invested by by by
[00:48:18] VCs, by by corporate venture capital, um
[00:48:22] you know, there's there's there's a
[00:48:23] strong, you know, strong growth and
[00:48:25] uptick in in those kinds of investments.
[00:48:27] There's a lot of support from from
[00:48:29] government, whether that's at the
[00:48:31] national level or at regional or in the
[00:48:33] US at state levels, where again there's
[00:48:36] a lot of activity um supporting this.
[00:48:38] And that goes, you know, it can be seen
[00:48:40] similarly in uh you know, across across
[00:48:42] Europe and in Asia as well. So, clearly,
[00:48:45] you know,
[00:48:46] private government uh money is flowing
[00:48:49] into these directions. That's uh you
[00:48:51] know, partly to help this to grow and to
[00:48:53] continue, but also because
[00:48:55] these, you know, well-informed and and
[00:48:57] and skilled investors who take quite
[00:48:59] some time in their due diligence, you
[00:49:01] know, find this to be, you know, one of
[00:49:03] the key areas
[00:49:04] uh that is exciting uh from an
[00:49:06] investment perspective at the moment. Uh
[00:49:08] so, I would, you know, I'd say to the
[00:49:09] broader investment community, you know,
[00:49:11] this is this is obviously a very rapidly
[00:49:13] moving space. You need to make sure that
[00:49:14] you're, you know, informed or at least,
[00:49:17] you know, relying on people that are
[00:49:18] already informed to to help you. Things
[00:49:20] change, you know, from moment to moment.
[00:49:23] Announcements can can happen and and
[00:49:25] dramatically change the landscape. Uh
[00:49:27] so, I think
[00:49:29] you know, I'm not not here to give
[00:49:30] anybody investment advice, of course,
[00:49:32] but this is a, you know, a very very
[00:49:35] important uh
[00:49:36] um likely to be quite dramatically
[00:49:39] transformative technology. Uh and these
[00:49:42] kinds of things don't come around very
[00:49:43] often. It happens also to be a highly
[00:49:46] technical and complex uh and rapidly
[00:49:49] changing space. Uh and so, one obviously
[00:49:52] needs to tread carefully uh and find you
[00:49:54] know, find people
[00:49:56] that one can rely on to take to inform
[00:49:59] and and and and guide accordingly.
[00:50:04] >> So, I want to thank Simon and Elvira. I
[00:50:07] hope
[00:50:08] everyone in the audience every episode
[00:50:10] we do there's sort of the the key
[00:50:12] statement that sticks in mind. The one
[00:50:14] that Simon made today that's going to
[00:50:15] stick with me is sort of think about how
[00:50:18] the industry, how the actual
[00:50:20] practitioners
[00:50:22] react to different announcements. There
[00:50:25] there was a big announcement.
[00:50:28] If I have the timing right, it was early
[00:50:30] last year February time frame. Microsoft
[00:50:33] was talking about you know, the Majorana
[00:50:36] qubits, the topological qubits.
[00:50:38] Sometimes that's the term that you see.
[00:50:40] And on the one hand, you see the
[00:50:42] Microsoft CEO talking about a chip and
[00:50:45] essentially a million qubits on the
[00:50:46] chip. And as a as a starting point, I
[00:50:49] mean a lot of the the chips that you see
[00:50:51] these days have a few hundred qubits if
[00:50:54] that. And so, initially as a non-expert,
[00:50:57] I'm sitting there going oh my gosh, a
[00:50:59] million qubits on a chip. What what's
[00:51:01] going on? But you saw how the industry
[00:51:04] sort of unpacked those statements. There
[00:51:06] were various articles in nature and
[00:51:08] other places.
[00:51:10] And it's not that topological qubits are
[00:51:13] impossible. It's just that there's still
[00:51:14] a lot that we have to learn, a lot
[00:51:16] that's left to be proven before we can
[00:51:19] really you know, put the full faith into
[00:51:22] that particular approach. And it was a
[00:51:24] great example of again, exactly what
[00:51:25] Simon gave us here, which is see the
[00:51:29] announcement, but then
[00:51:31] try to do your due diligence, try to see
[00:51:32] how the industry itself is reacting. And
[00:51:36] so, as we
[00:51:38] finish our time together today, I do
[00:51:40] have to state to clarify the views and
[00:51:41] opinions expressed in this podcast are
[00:51:44] those of WisdomTree and Classic and are
[00:51:46] subject to change. Anything we present
[00:51:48] in this podcast is not intended to be
[00:51:51] relied upon as a forecast, research, nor
[00:51:54] as investment or tax advice. The
[00:51:56] information and opinions expressed in
[00:51:58] this podcast are not a recommendation,
[00:52:00] offer, or solicitation to buy or sell
[00:52:03] any securities and reliance upon them is
[00:52:04] at the sole discretion of the listener.
[00:52:07] Please remember, past performance is no
[00:52:09] indication of future results. And so,
[00:52:12] with that, I thank everyone for taking
[00:52:14] some time with us today to
[00:52:17] unpack quantum computing. We're going to
[00:52:19] be back. We're going to cover this topic
[00:52:22] many more times because, you know, you
[00:52:24] can't do it justice in just one [music]
[00:52:26] episode. And we look forward to speaking
[00:52:28] again soon. Take care.
