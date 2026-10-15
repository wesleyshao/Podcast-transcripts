---
访谈时间: "2026-07-09"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Dylan Patel; Klay Hyman"
嘉宾公司名称: "SemiAnalysis; WisdomTree"
播客名称: "The Next Big Thing"
播客url地址: "https://www.youtube.com/watch?v=lHnxU9f-rwc"
全文提及的关键名词: 
  - "AI infrastructure"
  - "GPUs"
  - "memory"
  - "networking"
  - "data centers"
  - "energy"
  - "power constraints"
  - "AI agents"
  - "CPUs"
  - "semiconductor ecosystem"
字幕来源: "automatic_captions:en-orig:English (Original)"
YouTube视频标题: "Dylan Patel on the infrastructure powering the AI revolution | The Next Big Thing"
companies:
  - WisdomTree
  - SemiAnalysis
  - AMD
  - Anthropic
  - NVDA
industries:
  - 数据中心
  - 半导体
  - 电池
technologies:
  - Agent
  - GPU
  - LLM
  - 推理
keywords:
  - 能源瓶颈
tags:
  - WisdomTree
  - SemiAnalysis
  - AMD
  - Anthropic
  - NVDA
  - 数据中心
  - 半导体
  - 电池
  - Agent
  - GPU
  - LLM
  - 推理
  - 能源瓶颈
---

## Transcript

[00:00:01] All right. Hello everyone and welcome
[00:00:03] back [music] to our next episode of the
[00:00:06] next big thing podcast here. Uh I'm
[00:00:08] joined by my colleague Klay Hyman and uh
[00:00:11] Dylan Patel, our uh our our new partner
[00:00:15] uh founder of Semi analysis uh the
[00:00:18] research group. It's an exciting day
[00:00:20] that we get to sort of go through the
[00:00:23] current state of the AI infrastructure
[00:00:26] landscape uh with Dylan. You you've
[00:00:28] probably heard Dylan on many different
[00:00:29] podcasts. I I follow his content all the
[00:00:32] time as well as the newsletter on the
[00:00:34] semi analysis site. Uh mo most recently,
[00:00:37] one of the ones I saw was about data
[00:00:39] centers in space. So if anyone is uh
[00:00:41] interested in that topic, uh they have
[00:00:43] they have a great piece a lot of detail
[00:00:44] out on that. But um Dylan, I would love
[00:00:49] to hear a bit about where the idea for
[00:00:52] semi analysis sort of uh came from. I I
[00:00:55] know on the in the Substack community
[00:00:56] these days, people are talking a lot
[00:00:58] about the revenue of the firm and the
[00:01:00] success the firm has uh achieved, but
[00:01:02] but I I feel like a lot of a lot of
[00:01:04] times you you uh you know sometimes see
[00:01:07] the current level of success and and
[00:01:09] forget about the journey and and the
[00:01:10] origins and how much work probably uh
[00:01:12] went into all of it.
[00:01:14] >> Yeah. So I think the origin of semi
[00:01:16] analysis really comes from ship posting
[00:01:19] um posting online you know in in let's
[00:01:22] say a less serious manner, right? So
[00:01:24] when I when I go back to what were my
[00:01:26] first posts about semiconductors uh they
[00:01:29] were they were when I was uh in my tween
[00:01:32] right um you know and I was just posting
[00:01:34] on the internet about chips about uh
[00:01:36] smartphones about you know smartphone
[00:01:38] displays and smartphone SOC's and and
[00:01:40] all these other things before I ever
[00:01:42] even had a smartphone I was just
[00:01:43] obsessed with them and same with gaming
[00:01:45] hardware right PC hardware console
[00:01:47] hardware I was just posting about this
[00:01:48] stuff all the time on the internet on
[00:01:50] various forums and by the time I was 12
[00:01:52] I was moderating creating a lot of
[00:01:54] forums related to, you know, Android and
[00:01:56] Apple and Google and Intel, Nvidia, AMD,
[00:01:59] like, you know, the hardware topics of
[00:02:01] the world, various forums on Reddit
[00:02:03] related to these things. Um, and so
[00:02:05] that's sort of where the origin of it
[00:02:06] all comes from is I was just I've always
[00:02:08] been a poster. I've always posted my
[00:02:10] opinion. I've always replied, I've
[00:02:11] always thought, taken comments. And you
[00:02:13] know, I think one of the things the
[00:02:15] people in my team who, you know, now
[00:02:16] we're a 90 person organization, so I
[00:02:17] actually have like, you know, people in
[00:02:19] marketing, they're like, Dylan, stop
[00:02:20] replying to random bozos on the
[00:02:22] internet. like you're making us look
[00:02:23] bad. It's like it's like I I just have
[00:02:25] that burning desire to respond to anyone
[00:02:27] on the internet when they try and
[00:02:28] criticize me. And so that's the you know
[00:02:30] maybe maybe it's a bad thing but um
[00:02:32] basically you know throughout my teenage
[00:02:34] years I was moderating these forums. You
[00:02:36] know I started investing uh as soon as I
[00:02:38] started making money in my later teenage
[00:02:39] years. Um I was a quant for two years
[00:02:42] and then I started my firm but the whole
[00:02:44] time I was posting posting posting
[00:02:45] posting posting. I had anonymous blogs.
[00:02:48] I had anonymous posts. Uh but then in
[00:02:50] 2020, you know, sort of I got fed up
[00:02:53] with my job. Disillusionment of sort of
[00:02:55] like being a quan is, you know, not as
[00:02:57] amazing as it seems. Yes, you make
[00:02:58] money, but it's not as amazing as it
[00:03:00] seems. Um and I kind of quite quit my
[00:03:02] job and started my company. Um, and I
[00:03:05] wasn't exactly sure it was going to go,
[00:03:07] but I was posting on a WordPress website
[00:03:10] um, that I made and I was posting under
[00:03:12] my real name and I was posting sort of
[00:03:13] this mix of technology, business,
[00:03:15] finance, supply chain, sort of the
[00:03:18] things I was most interested in because
[00:03:19] I I grew up in a small business, right?
[00:03:21] I grew up in a motel. My parents owned a
[00:03:22] motel in rural Georgia and we lived in
[00:03:24] it and I kind of just know business. We
[00:03:27] we later had gas stations too and so
[00:03:29] sort of lived in it, grew up in it. So,
[00:03:30] I always loved business. Uh supply chain
[00:03:32] was always interesting from the
[00:03:34] perspective of investing from the
[00:03:35] perspective of how things are made. I
[00:03:37] think that's always just been a knack
[00:03:38] like how are things made um you know
[00:03:40] technology aspect of course is super
[00:03:41] exciting and the finance aspect are
[00:03:43] super exciting. So, you know, taking the
[00:03:44] combo of that, you know, my first post
[00:03:46] were things like um you know, at the
[00:03:49] time, China was banning or or the US was
[00:03:51] banning Huawei from access to TSMC and I
[00:03:54] was and then so my first post was
[00:03:56] actually about how uh MediaTek was the
[00:03:58] biggest winner. Um because Huawei was
[00:04:00] number one market share in China for
[00:04:02] smartphone chips and smartphones in
[00:04:03] general. Obviously, that was going to
[00:04:05] tank because they no longer had access
[00:04:06] to TSMC and and so the US market
[00:04:09] thought, oh, Qualcomm's going to win.
[00:04:10] But MediaTek, which is the Taiwanese
[00:04:12] firm, we thought I thought, you know,
[00:04:13] they're actually going to win a lot more
[00:04:14] share because, you know, it turns out
[00:04:16] geopolitically China would rather buy
[00:04:18] from a Taiwanese firm than from a US
[00:04:19] firm given we just banned Huawei. And so
[00:04:21] both firms benefited, but MediaTek
[00:04:23] benefited a lot more. So it was that
[00:04:25] like mix of like technology, uh, supply
[00:04:28] chain, you know, finance, geopolitics,
[00:04:30] all these things sort of melded
[00:04:31] together. And you know over the coming
[00:04:33] years sort of I converted my WordPress
[00:04:35] into a substack um at one point um
[00:04:38] started charging for it and I was
[00:04:40] writing about all these topics across
[00:04:42] the entire semiconductor and AI supply
[00:04:43] chains. Um you know given you know I
[00:04:46] followed AI a lot. I did a little bit of
[00:04:47] AI when I was a quant as well as you
[00:04:48] know following semiconductors out of a
[00:04:49] passion. Um and that just grew and grew
[00:04:52] and grew and grew. Um for four years I
[00:04:56] traveled all around the world and I went
[00:04:58] to every conference in the world. I was
[00:04:59] going to 40 conferences a year. um you
[00:05:02] know I didn't live anywhere I was just
[00:05:03] going to every conference I could
[00:05:04] whether it be you know an AI conference
[00:05:07] like Nurips um ICML ilear so these are
[00:05:11] sort of AI researcher conferences mostly
[00:05:13] researchers and some companies uh go go
[00:05:15] there and present their research all the
[00:05:16] way downstream to random conferences for
[00:05:19] let's say chemicals that are inputs into
[00:05:21] the semiconductor supply chain so I'd go
[00:05:23] up and down the stack whether it be
[00:05:24] servers networking you know fabrication
[00:05:28] um AI you know just all up and down the
[00:05:30] stack I'd go to 40 conferences a year.
[00:05:31] You know, there'd be some that are super
[00:05:33] niche and there'd be 300 people there
[00:05:34] and they only spoke Japanese except for
[00:05:36] like five people and I'd be like, "Well,
[00:05:38] whatever, right? That is what it
[00:05:40] is." And then there'd be others where
[00:05:41] it'd be 10,000 20,000 people and it'd be
[00:05:43] huge, right? And it'd be the whole
[00:05:45] spectrum and continuum. And so I was
[00:05:46] able to go across the whole ecosystem.
[00:05:48] You know, you go to a conference three
[00:05:50] times, you actually know the language
[00:05:51] now. you know people there you can you
[00:05:53] build all these contexts so you can ask
[00:05:54] them questions and sort of you you know
[00:05:56] I developed this whole ecosystem and
[00:05:58] learnings and I was covering you know
[00:05:59] the inflections at each of these right I
[00:06:01] was very curious technologically but
[00:06:04] then once something stood out whether it
[00:06:05] be technology or supply chain I learned
[00:06:07] from a conference I knew where it would
[00:06:09] lead to on a supply chain or finance
[00:06:11] basis and so I was writing about like
[00:06:13] the whole mix sometimes reports would be
[00:06:15] centered around technology and no one in
[00:06:17] finance would care and other times
[00:06:18] they'd be like wow this is the
[00:06:20] bottleneck or this is the inflection
[00:06:21] that's happening or this company is
[00:06:22] going to gain a ton of market share
[00:06:24] because they're next generation
[00:06:25] technology and I would call it before
[00:06:27] anyone else on the street before any
[00:06:29] hedge fund before anyone. And so sort of
[00:06:31] that was that was like the start and
[00:06:33] then as that substack grew and grew in
[00:06:35] 2022 I started hiring people. My first
[00:06:37] two hires were people I knew from
[00:06:38] Discord for years. Um but then after
[00:06:41] that my third hire was Myin and he
[00:06:43] worked at a hedge fund before and he was
[00:06:45] moving to Japan to live with his wife
[00:06:47] there and so he was he was sort of a
[00:06:49] free agent. I'd put in a post about how
[00:06:51] uh you know it's interesting this is a
[00:06:53] very interesting post at the time um in
[00:06:55] early 23 memory was the biggest loser
[00:06:57] from AI and the reason was because the
[00:07:00] amount of memory that AI chips used uh
[00:07:02] and AI servers used versus regular
[00:07:04] servers was a lot less right regular
[00:07:06] servers about half the bomb was AI chip
[00:07:09] was memory in AI servers it was much
[00:07:11] less part of that was Nvidia's margins
[00:07:13] are much higher part of that was you
[00:07:15] know there's a couple different factors
[00:07:16] um of course Nvidia's next generation
[00:07:18] chips have increased the memory content
[00:07:20] dramatically. Um, and now it's like, you
[00:07:22] know, way more. But at the time it was
[00:07:23] saying memory is the biggest loser. And
[00:07:25] in the paid section, I said, "Hey, I'm
[00:07:27] hiring." Um, and Myin reached out and he
[00:07:29] was the first person from a hedge fund
[00:07:31] background, right? The other two people
[00:07:32] were technical backgrounds. And so as
[00:07:33] soon as he joined the firm, we started
[00:07:34] making all these models and we really
[00:07:36] converted the business from, you know,
[00:07:38] we still do the newsletter, we still
[00:07:39] post a lot of amazing content there more
[00:07:41] than ever before. But we converted it
[00:07:43] from that to being one around uh selling
[00:07:45] information services, you know, selling
[00:07:47] these reports, selling these data sets.
[00:07:49] Um, and and that sort of as that started
[00:07:51] to happen, the ball started tumbling
[00:07:52] down the hill. And from 2023 to 2024, I
[00:07:56] went from, you know, 2 to 7. And then
[00:07:59] from 24 to end to 25 uh to beginning at
[00:08:02] 25 I went from seven to 20. Uh and from
[00:08:05] 25 to 26 I went from 20 to 60. And now
[00:08:08] this year we're at 90. Uh so we've added
[00:08:10] 30 people this year. So it's just been a
[00:08:12] ball tumbling down the hill and we've
[00:08:14] just added sectors. Um you know I've
[00:08:16] always been interested in everything but
[00:08:17] now I've been able to add people that
[00:08:19] are experts. So you know I think the the
[00:08:20] most exciting thing about semi- analysis
[00:08:22] is I don't know another firm that has
[00:08:24] the level of expertise and a
[00:08:25] concentration we do right. I have people
[00:08:27] who have worked at ASML, Applied
[00:08:29] Materials, Lamb Research, the equipment
[00:08:31] companies that build wafers, all the way
[00:08:33] upstream to people who have worked at
[00:08:34] Intel and TSMC and Nvidia and Microsoft
[00:08:36] and Amazon of course, but also people
[00:08:38] who have worked at, you know, worked at
[00:08:41] OpenAI on model, someone who's worked at
[00:08:42] OpenAI on model, someone who's worked at
[00:08:44] Tesla and FSD, someone who's worked at
[00:08:45] Coher sort of we've got people who
[00:08:47] worked on the model layer and then on on
[00:08:48] another vertical we've had people who
[00:08:49] have worked on data centers. There's
[00:08:51] someone at my company who built a power
[00:08:52] plant in Kazakhstan, right? It's like we
[00:08:54] just have this most insane talent
[00:08:56] density that's like awesome. So like you
[00:08:58] know half the firm is is sort of like
[00:09:00] people who have done engineering across
[00:09:01] the industry and then the other half the
[00:09:02] firm is either ex hedge fun or ex just
[00:09:05] like random people from the internet who
[00:09:07] are super passionate. you know, I found
[00:09:08] them on Twitter or Discord and I'm like,
[00:09:10] you're smart. Come work for me. And and
[00:09:11] it works. And so this is sort of like,
[00:09:13] you know, what's built up and now semi
[00:09:15] analysis is like got many different
[00:09:16] lines of businesses. You know, obviously
[00:09:18] data services, consulting, um
[00:09:20] information services, um you know, we
[00:09:23] have the newsletter. We're we're doing
[00:09:25] all these media. We're having a
[00:09:26] conference soon that's going to be big.
[00:09:27] And you know, all sorts of different
[00:09:29] stuff that we do. And it's it's just a
[00:09:30] hell of a ride.
[00:09:32] And and speaking of the ride, I had a
[00:09:34] moment uh Dylan where so wi wisdom tree
[00:09:38] and semi analysis have been on this
[00:09:39] journey for um a number of months
[00:09:42] working together. And so uh Nvidia GTC
[00:09:45] happens uh in March as it does every
[00:09:48] year. And I'm sitting watching the live
[00:09:50] stream here in Charlotte, North
[00:09:52] Carolina. And I think there's 55,000
[00:09:54] other people watching the live stream.
[00:09:56] And suddenly
[00:09:57] >> and there's 20,000 people in a stadium.
[00:09:59] There's 20,000 people in the stadium,
[00:10:01] dude.
[00:10:02] >> And and he's referring to you directly
[00:10:04] that you were like sandbag, you said he
[00:10:06] was sandbagging a certain number and
[00:10:07] your charts like right up on the stage.
[00:10:10] And so admittedly, I I had a moment I I
[00:10:12] guess probably on your behalf basically
[00:10:14] watching the CEO of the biggest company
[00:10:16] in the world basically refer to your
[00:10:18] research and and how you were
[00:10:20] criticizing uh you know his uh his take
[00:10:22] on some of the numbers. I I'd love for
[00:10:24] you to sort of I guess you were in the
[00:10:26] stadium from what it sounds like there.
[00:10:28] >> Yeah. Yeah. So that moment was quite
[00:10:30] surreal, right? So basically one of the
[00:10:32] things that semi analysis does is we
[00:10:34] actually have a number of engineers and
[00:10:35] we do open- source benchmarking of all
[00:10:37] the uh AI models that are open source as
[00:10:40] well as all the hardware. Um it's a
[00:10:42] pretty awesome effort. Um so there's a
[00:10:43] number of engineers on my side, but we
[00:10:45] collaborate with the industry heavily.
[00:10:47] Um, so we get hardware, you know, so we
[00:10:49] have over $50 million of hardware
[00:10:50] donated to us from companies like um,
[00:10:53] OpenAI, Microsoft, Amazon, Google, Core,
[00:10:56] Reweave, Nebius, Crusoe, um, you know,
[00:10:59] all of the major clouds you can think of
[00:11:01] that have donated us. Oracle have
[00:11:02] donated us hardware um, that we run
[00:11:05] these benchmarks on. And so we have we
[00:11:07] have uh, you know, we have eight
[00:11:09] different kinds of GPUs, you know, all
[00:11:10] H100s, H200s, Blackwell, you know, AMD's
[00:11:13] various GPUs. In addition, we have TPUs
[00:11:15] from Google and Tranium from Amazon. And
[00:11:17] what we do is we run benchmarks on the
[00:11:20] latest version of software every single
[00:11:22] day. And so why why that is is because
[00:11:23] every night a CUDA version could
[00:11:25] release, a PyTorch version could
[00:11:26] release, a driver update could release,
[00:11:28] inference engine VLM lang version could
[00:11:30] uh release um etc. And so we run these
[00:11:33] benchmarks every single night on the
[00:11:35] entire curve of you know how fast do you
[00:11:37] want the tokens versus how
[00:11:38] cost-effective do you want them on the
[00:11:40] optimal scenarios. And we run all of
[00:11:42] this every single day. It's it's like an
[00:11:44] automated benchmarking suite that runs
[00:11:47] and you know bench you know Jensen when
[00:11:49] he originally launched Blackwell had
[00:11:51] claimed it would be a 25x improvement.
[00:11:54] Um, and at the time no one believed him,
[00:11:56] right? It's Jensen, right? He's
[00:11:57] marketing. Um, and and even us at the
[00:12:00] time were like, "Oh, okay." We were like
[00:12:02] more bullish than ever. Like, we think
[00:12:03] it could be like a 15 to 20x improvement
[00:12:05] based on some of the simulations we were
[00:12:07] running. Uh, because we had a simulator,
[00:12:09] uh, we have a simulator for performance.
[00:12:10] But, you know, as we built out this
[00:12:12] inference benchmarking called inference
[00:12:14] X, uh, we got to the point where
[00:12:16] actually, oh wow, in DeepSeek V3,
[00:12:19] Blackwell is 30x faster than Hopper on
[00:12:22] on somewhere on the continuum. And so
[00:12:23] then you end up ended up with this like
[00:12:25] you know I I I emailed him as soon as we
[00:12:27] had the results and they you know they
[00:12:29] automatically published onto the open
[00:12:30] source GitHub sort of it's a open source
[00:12:32] collaboration Nvidia people helped and
[00:12:34] they knew but I highlighted to him I was
[00:12:35] like hey Jensen you know I emailed him I
[00:12:37] was like hey Jensen you know back in
[00:12:39] 2024 you said uh or back when you
[00:12:41] launched Blackwell you said 20 uh 25x
[00:12:44] and everyone gave you crap. Here's all
[00:12:45] the people that gave you crap. Even I
[00:12:47] gave you crap. I was like there's no way
[00:12:48] it's 25x. It's maybe 15 to 20x and and
[00:12:51] and a lot of people were like, "No, no,
[00:12:52] no, it's like 3x." Um, so we were we
[00:12:55] were quite bullish, but Jensen, I was
[00:12:57] wrong. You were sandbagging it. It was
[00:12:59] 30x and and and so and so he he he took
[00:13:03] that and and you know, he I didn't know
[00:13:06] that he was doing anything with it. I'd
[00:13:07] heard from a couple customers. Uh
[00:13:09] someone at Meta told me there was a
[00:13:10] meeting they had and Jensen was using
[00:13:12] that as proof that he doesn't sandbag
[00:13:14] numbers. He was like cuz he was telling
[00:13:16] about the next generation chip and and
[00:13:18] anyways this this all happened and and
[00:13:20] anyways I I didn't expect it to happen
[00:13:21] on stage. Uh you know in addition in
[00:13:24] inference X uh we created this belt. It
[00:13:26] looks like a WWE belt you know it's a
[00:13:28] WWE belt like sort of and it says
[00:13:30] inference king and we sent it to all of
[00:13:31] our collaborators. We sent it to our
[00:13:33] collaborators. We sent it to Nvidia. We
[00:13:34] sent it to AMD. We sent it to uh you
[00:13:37] know some of the other folks SG Lang
[00:13:38] VLM. All these different people who
[00:13:39] helped us help us with the benchmark
[00:13:41] people donated hardware whatever. um you
[00:13:43] know because it's an open source effort
[00:13:45] where I'm spending you know a couple
[00:13:47] million dollars a year on engineer
[00:13:48] salaries and then other people are
[00:13:49] spending millions on hardware and
[00:13:50] donating it or millions on engineer
[00:13:52] salaries and donating it towards this
[00:13:53] open source effort that we run. Um, and
[00:13:56] and I sent them this this belt and he
[00:13:58] has this belt on the on the slide. Uh,
[00:14:00] and he hel he he had held it up and then
[00:14:02] there were our charts and he's on the
[00:14:04] slide for five minutes talking about
[00:14:05] how, you know, Dylan said I was
[00:14:06] sandbagging but I wasn't, you know, and
[00:14:09] and our performance is the best and it
[00:14:11] was just it was such a surreal moment.
[00:14:13] >> Um, he talked about he talked about us
[00:14:15] longer than anyone else in the entire
[00:14:18] presentation. Um the only other person
[00:14:20] who even talked about as much was
[00:14:21] OpenClaw uh which is you know obviously
[00:14:23] taking this world by storm.
[00:14:25] >> So it was an incredible moment.
[00:14:27] >> Yeah Dylan so you mentioned a couple
[00:14:29] things there. Um I think it's quite
[00:14:30] interesting that you mentioned open
[00:14:31] source and now that there's kind of you
[00:14:33] know maybe transitioning a bit towards
[00:14:35] um I'll say some of the recent
[00:14:36] developments and maybe a bit of I'll say
[00:14:39] the markets. Um there's been kind of
[00:14:42] these these discussions around the
[00:14:44] actual inference efficiency of some of
[00:14:46] the open source models versus the closed
[00:14:48] source models. And there's also even you
[00:14:50] know still to this day a lot of
[00:14:51] investors that are like questioning say
[00:14:53] the ROI on all of this. I mean, just in
[00:14:55] the last week or two, we had some I
[00:14:57] think it was a Bloomberg economist kind
[00:14:59] of talk through um you know, how a lot
[00:15:02] of these AI initiatives may be uh you
[00:15:05] know, I'll say potentially failing at
[00:15:08] some of the firms out there and I know
[00:15:10] you've highlighted how your firm is
[00:15:12] using AI extensively and really leaning
[00:15:14] into, you know, giving lots of giving
[00:15:17] your employees lots of access to tokens.
[00:15:20] Um and then obviously you just
[00:15:21] highlighted that you're hiring. So I'm
[00:15:22] just curious kind of what's your take on
[00:15:25] this kind of like end demand the you
[00:15:27] know and kind of this the fact that this
[00:15:30] end demand really does uh drive I'll say
[00:15:33] this big buildout that we're seeing that
[00:15:34] is kind of full of all these um
[00:15:36] constraints that have been at least over
[00:15:38] the last month besides the most recent
[00:15:41] couple days in the markets driving up a
[00:15:43] lot of the I'll say different stocks
[00:15:46] tied to tied to some of these themes.
[00:15:49] >> Yes. I would say a few things, right?
[00:15:50] When you look at um you know the the the
[00:15:53] overarching question here sort of ROI
[00:15:55] and are people are the companies making
[00:15:56] enough money from AI? Is this going to
[00:15:58] continue? Um are the comp people using
[00:16:01] AI actually getting value out of it?
[00:16:02] It's it's this overarching question that
[00:16:04] a lot of people have. Um
[00:16:06] and when I look at it and when I think
[00:16:08] about it right there's there's a few
[00:16:09] ways to dissect it, right? One first and
[00:16:11] foremost is you know anthropic is free
[00:16:13] cash flow positive and they are
[00:16:15] profitable in Q2. Um, even in April, in
[00:16:18] April, they closed April's books. They
[00:16:20] were profitable. They were free cash
[00:16:21] flow positive. In in uh in May, they
[00:16:24] were free cash flow positive. They were
[00:16:25] profitable. Uh, June looks like it's
[00:16:28] going to be the same way. It's not fully
[00:16:29] closed yet, but at least for two of the
[00:16:31] three months, they've been free cash
[00:16:32] flow positive and profitable. Um, you
[00:16:34] know, their their reoccurring revenue is
[00:16:36] is soared past $50 billion ARR. Um, and
[00:16:39] they're doing fantastic, but you know, I
[00:16:41] think I think that's that's one side of
[00:16:43] the coin is anthropic is printing. Um,
[00:16:45] obviously there are a lot of companies
[00:16:46] that aren't printing, but they're
[00:16:47] getting there, right? And OpenAI's
[00:16:49] revenue has started to inflect as
[00:16:50] Codex's adoption has grown and others as
[00:16:53] well. Um, so, so these companies are all
[00:16:55] getting much more profitable. Anthropic
[00:16:57] gross margins are really, really high.
[00:16:59] They're, uh, they're above 70%. Um, but
[00:17:02] ultimately, um, you know, when
[00:17:05] ultimately, you know, that's one side of
[00:17:07] the coin, the side of the coin that
[00:17:08] people are starting to and you were
[00:17:09] alluding to is sort of what about the
[00:17:10] company's spending on AI, right? um at
[00:17:12] least at semi- analysis we went from our
[00:17:15] annual you know I call I like to call it
[00:17:16] like you know it's not an ARR annual
[00:17:18] reoccurring revenue it's ARS right uh
[00:17:21] annual reoccurring spend and so my
[00:17:23] annual reoccurring spend in December and
[00:17:25] in November before uh cloud code cloud
[00:17:28] code really started to take off in
[00:17:29] December for us um last year but our re
[00:17:32] annual reoccurring spend in November was
[00:17:34] less than 100k right what we had was
[00:17:36] that we had a subscription to every
[00:17:38] model or we had a subscription to the
[00:17:40] $200 tier for a chat uh GPT for every
[00:17:43] user, right? Uh and and that was, you
[00:17:45] know, like about it. Um so we were
[00:17:47] spending less than $100,000 on, you
[00:17:49] know, if people wanted XAI or Claude,
[00:17:51] we'd give it to them as well. Uh but
[00:17:53] standard was giving everyone the $200
[00:17:55] OpenAI subscription. And that's what
[00:17:57] that's what was the state in November,
[00:17:58] which was, you know, I think we were on
[00:17:59] the bleeding edge even then. But then
[00:18:01] cloud code really started to hit its
[00:18:03] inflection point with cloud opus 4.5 and
[00:18:05] 4.6 and so on and so forth. And by the
[00:18:08] end of January, our ARCs, right, our our
[00:18:11] our annual recurring spend had hit $4
[00:18:13] million. And that's because people were
[00:18:16] using cloud code. Now today, it's about
[00:18:18] $11 million. And the highest uh you
[00:18:21] know, day on, if we take the week and
[00:18:23] multiply it by 52, a week of spend
[00:18:25] multiplied by 52, that we're at 11. Uh
[00:18:27] the highest we've ever had was 14. Um
[00:18:29] so, you know, we've it oscillates a lot
[00:18:31] based on what work people are doing. Uh
[00:18:33] but right now the average looks to be
[00:18:35] about $1 million of spend a year for a
[00:18:37] 90 person firm. That's freaking insane,
[00:18:39] right? I just want to be clear. Um we're
[00:18:41] spending you know more like you know
[00:18:43] more than a third of the spend uh you
[00:18:45] know employee spend a third of it is
[00:18:47] also on top of that is AI. Um and we'll
[00:18:49] probably get to half half or uh you know
[00:18:51] by the end of the year depending on how
[00:18:52] Methos and other models start coming out
[00:18:54] get better and better and better. Um
[00:18:57] that's that's a huge amount of spend.
[00:18:59] Now the question is what's the ROI? Um,
[00:19:01] I think there's been huge ROI because
[00:19:02] we've been able to build product. We've
[00:19:04] been able to, you know, sell more. We've
[00:19:05] been able to increase the efficiency of
[00:19:07] everyone in the company. Um, and and so
[00:19:09] I see the ROI, but I think a lot of
[00:19:11] companies are questioning, hey, if I'm
[00:19:13] spending hundreds of, you know, you
[00:19:14] know, if if I take a really good
[00:19:16] developer and they make, you know, call
[00:19:17] it $300,000 a year or more, right? If I
[00:19:20] take a good developer, they make
[00:19:21] $300,000 a year. Uh, there's a lot of de
[00:19:23] devs who make a lot more, of course. Um,
[00:19:26] their spend on AI is starting to
[00:19:28] approach, you know, one to one. um for
[00:19:30] for good developers and then for
[00:19:32] non-developers you know the spend ranges
[00:19:34] it can be lower but even you know at
[00:19:36] least at semi- analysis a lot of our
[00:19:38] biggest spenders are people who don't
[00:19:39] know how to code um and they just kind
[00:19:41] of tell the model what they want and
[00:19:42] then they like iterate iterate iterate
[00:19:44] and they get what they want um and and
[00:19:46] so you see this soaring spend per
[00:19:48] employee um and and a lot of companies
[00:19:51] are now rightfully asking like hey our
[00:19:54] entire AI budget we blew through it in
[00:19:56] Q1 Q2 right for the year we blew through
[00:19:58] it already now what do we do? And the
[00:20:00] question is, well, do we cut spend or do
[00:20:02] we cut elsewhere? And a lot of companies
[00:20:04] are saying, oh, maybe we need to slow
[00:20:05] down on spend on AI. Uh, but a lot of
[00:20:08] companies I've seen are starting to cut
[00:20:09] elsewhere, right? They're cutting other
[00:20:12] SAS products that they have used
[00:20:13] historically. They're saying, "Hey, we
[00:20:15] can grow faster, so we'll just do it."
[00:20:17] They're saying, "Hey, it's okay to spend
[00:20:19] on AI. We'll take the hit temporarily.
[00:20:22] AI keeps getting cheaper." You know, as
[00:20:23] adoption sores, uh, you know, for what I
[00:20:26] used to do six months ago, AI is much
[00:20:28] cheaper today. Of course, what I'm doing
[00:20:30] with AI today is much more extensive
[00:20:32] than what I did six months ago. There's
[00:20:33] a variety of different approaches people
[00:20:35] are taking. Some people are uh even
[00:20:37] cutting on employees instead of cutting
[00:20:38] on AI. And some people are clamping down
[00:20:40] on AI, but those companies are going to
[00:20:42] get left in the dust in terms of
[00:20:43] productivity gains and and what they're
[00:20:44] able to build.
[00:20:46] >> Gotcha. And then one of the So, one of
[00:20:49] the I'll say ways to kind of mitigate
[00:20:51] some of the incremental cost is choosing
[00:20:54] cheaper maybe sometimes, you know, less
[00:20:56] intelligent models. maybe not always
[00:20:58] being at the the leading edge there. Um,
[00:21:01] and now I I've like I've said I've just
[00:21:04] it's very early I think in terms of some
[00:21:06] of the rumblings there, but I I'm
[00:21:07] curious like is there a point where you
[00:21:10] know firms you know like yours kind of
[00:21:12] decide you know there's some use cases
[00:21:14] that are more optimal for using you know
[00:21:16] a deepseek v4 type of model for a
[00:21:20] certain type of work and then obviously
[00:21:22] you might need to rely on things that
[00:21:23] cost a bit more for um you know I'll say
[00:21:26] things that require a lot more
[00:21:27] intelligence. Is is that part of the the
[00:21:30] calculus here?
[00:21:32] >> I think that's absolutely part of the
[00:21:33] calculus for some folks. Um or and and
[00:21:35] and you have to sort of break out AI
[00:21:37] workloads into two types, right? One is,
[00:21:40] hey, this is AI integrated into a
[00:21:42] process that I have. Um and in those
[00:21:45] cases, right, it's like, oh, when a
[00:21:47] customer sends me a document, I check it
[00:21:49] for XYZ. Um and I put it into the model
[00:21:52] and the model checks it and it's done.
[00:21:54] Um, and there I just need to hit some
[00:21:56] level of quality and then from there I
[00:21:58] can stop improving the model and I can
[00:22:00] start decreasing on cost by waiting for
[00:22:02] newer models or cheaper models or the
[00:22:03] cost efficiency, right? And we've seen
[00:22:05] we've seen AI models uh improve at a
[00:22:07] rate of about 60x per year in cost. Um,
[00:22:10] you know, you take a quality level and
[00:22:12] then a year later it's 60x cheaper. Uh,
[00:22:15] you know, people freaked out about
[00:22:16] DeepSeek uh because it was 600 times
[00:22:18] cheaper than GPD4. um you know so that's
[00:22:21] that's actually it was it was about 2
[00:22:23] years after GBD4 so 360x uh 60x and time
[00:22:27] 60x 360x uh and it actually ended up
[00:22:30] being 600x cheaper so somewhere on the
[00:22:32] curve is you know 60 whether it's 60x a
[00:22:34] year cheaper or you know 90x cheaper a
[00:22:36] year you know there's somewhere on the
[00:22:37] curve is is is how much cheaper it's
[00:22:39] getting a year but deepseek you know v3
[00:22:41] versus GP4 was 600x in two years um and
[00:22:45] as you as you step forward it's
[00:22:47] somewhere in that range and so if you
[00:22:48] have a workflow and you integrate AI
[00:22:50] into that workflow, then it's, you know,
[00:22:53] you you get to a quality level, then you
[00:22:54] go cheaper. The other range of work is
[00:22:57] AI assistant, right? And that's where I
[00:22:59] think it's it's sort of there's actually
[00:23:00] a bit of a misnomer. You don't, you
[00:23:02] know, if if I am doing my day-to-day
[00:23:04] work and I'm asking the model to help me
[00:23:06] with this, help me find this, help me
[00:23:08] figure out that. Cost optimization is
[00:23:11] not actually going to a cheaper model.
[00:23:12] cost optimization is oftent times taking
[00:23:16] the newest model because the newest
[00:23:17] model whereas uh you know claude 4.6
[00:23:21] opus would take a 100,000 tokens to do a
[00:23:24] task and it might it might take a couple
[00:23:27] turns right me talking to it back and
[00:23:29] forth so it might take 100,000 tokens
[00:23:31] and you know uh 10 minutes of my time
[00:23:34] cloud 4.8 Opus can do it in a quarter of
[00:23:37] the tokens, 25,000 tokens, and it might
[00:23:39] only take one back and forth, right? And
[00:23:41] so the the cost is actually less because
[00:23:44] the number of tokens being generated is
[00:23:46] less. And the amount of time I'm using
[00:23:48] is less. And so when I look at a
[00:23:50] developer or I look at uh someone who is
[00:23:52] doing intelligence work, how do I how do
[00:23:54] I reduce the cost is actually not by
[00:23:56] using a cheaper model. It's by taking an
[00:23:59] existing task that could be done
[00:24:00] sometimes with the model after fighting
[00:24:02] with it and and going to newer and newer
[00:24:04] models and now it's able to either just
[00:24:06] one iteration or oneshot the entire uh
[00:24:09] workflow. It's able to do it in fewer
[00:24:11] tokens. And so what we've seen from 4.6
[00:24:13] opus to when 4.7 opus my cost actually
[00:24:16] fell for a week before it soared back up
[00:24:19] because people were using it more and
[00:24:20] more. And now why did it sore back up is
[00:24:22] because people you know they were like
[00:24:23] okay they have to adjust to the new
[00:24:25] workflow right which is okay the work I
[00:24:26] was doing is done let me do more right
[00:24:29] and so it goes back up and and and
[00:24:31] likewise when 4.7 came out to 4.8 Hey,
[00:24:33] the cost fell for about a week, a week
[00:24:36] and a half, and then it soared back up
[00:24:38] because people were like, "Oh, yeah, now
[00:24:39] I can do more work." And so, you know,
[00:24:41] you have to measure the productivity
[00:24:42] alongside the cost. And when it's an AI
[00:24:44] assistant, actually, token efficiency is
[00:24:46] really important. And so, this is this
[00:24:48] is sort of uh why Anthropic has been
[00:24:51] beating OpenAI is because their models
[00:24:53] are more token efficient than OpenAI.
[00:24:55] Actually open eyes models uh on the edge
[00:24:58] edge cases right in terms of leading
[00:25:00] science leading math leading code oftent
[00:25:02] times can do a task that enthropic
[00:25:05] models cannot but they take you know 3x
[00:25:09] as long and 4x as many tokens and
[00:25:11] therefore it costs a lot more and the
[00:25:13] feedback loop of human and AI is not as
[00:25:16] rapid and therefore it actually ends up
[00:25:18] being worse uh on a customer perception
[00:25:21] basis because it's one thing to say hey
[00:25:23] model do this task
[00:25:25] and then you come back and you check if
[00:25:26] the task is done. It's another thing to
[00:25:28] say, hey, I have four hours to do this
[00:25:30] task and you know whether it's one call
[00:25:32] to the model and it does work for four
[00:25:34] hours or if it's four calls to the model
[00:25:36] and it goes back and forth which one
[00:25:38] does it better it turns out enthropic
[00:25:39] when you have this human in the loop
[00:25:41] feedback loop is actually way faster and
[00:25:43] better because it's more token efficient
[00:25:45] and and so you end up with that's the
[00:25:46] main reason why we still remain a
[00:25:48] majority enthropic shop. Some tasks
[00:25:51] people do use OpenAI and oftent times
[00:25:53] you know the tasks that they let running
[00:25:55] overnight are the ones that they give to
[00:25:56] OpenAI uh codecs um but most tasks they
[00:25:59] keep with cloud code and so this is sort
[00:26:02] of one of the interesting factors of
[00:26:05] you know what's going on with sort of
[00:26:06] the models and token efficiency is is
[00:26:09] cost is is a bit of a uh you know it's
[00:26:12] hard to pair it out but you know some
[00:26:14] tasks it's you know freeze the model
[00:26:16] quality and and you wait for the models
[00:26:17] to get cheaper and others it's actually
[00:26:19] I just want the smartest model because
[00:26:21] it is cheaper.
[00:26:24] >> Dylan, I um was curious on your thoughts
[00:26:28] shifting it a bit to the hardware side
[00:26:32] and I know earlier this year uh one of
[00:26:34] the newsletter uh I'm I'm a big I've
[00:26:36] been a big newsletter fan for multiple
[00:26:38] years if the audience hasn't realized it
[00:26:40] but um there was an article talking
[00:26:43] about memory. memory has usually been a
[00:26:47] cycle. Meaning may maybe it's 18 to 24
[00:26:50] months you you go up, 18 to 24 months
[00:26:52] you go down. And we we know that it
[00:26:56] feels like almost everything is in
[00:26:57] shortage. Like if you're involved in a
[00:27:00] component that goes into a data center,
[00:27:02] it feels like it's not a question of can
[00:27:04] you even get the component. It's more
[00:27:06] okay, how long are you going to have to
[00:27:07] wait because it feels like in the world
[00:27:09] today you can barely get any any
[00:27:11] component. So with your experience
[00:27:14] having looked across the hardware side,
[00:27:17] what's what what do you expect is going
[00:27:19] to be changing with something like
[00:27:21] memory which used to always be this just
[00:27:23] commoditized product. You you ride the
[00:27:25] upswing, you go through the downswing
[00:27:27] and it it just repeats uh going back the
[00:27:30] last 40 years.
[00:27:32] >> Yeah. So so I'm not saying there's not
[00:27:33] going to be cycles anymore. You know, I
[00:27:35] think cycles will happen. Obviously,
[00:27:37] we're in a super cycle where the upswing
[00:27:40] is crazy and and you know, there will be
[00:27:41] some downswing and it'll be brutal as
[00:27:43] well. Um, but the downswing obviously,
[00:27:46] you know, trough to trough, there's
[00:27:47] still a lot of growth, right? Um,
[00:27:50] you know, even if you know, you're in an
[00:27:51] upcycle and um, so I think what's what's
[00:27:54] relevant now about memory um, and other
[00:27:56] components is is the shifting faces of
[00:27:59] what's happening, right? Um historically
[00:28:02] we had you know upcycles would be you
[00:28:05] know you know up 50% you know for the
[00:28:07] end market and therefore you know for
[00:28:09] commodity markets like memory where
[00:28:12] pricing power you know pricing is more
[00:28:13] elastic and things like that you'd end
[00:28:15] up with oh those stocks 2 3x uh but what
[00:28:18] we've gotten today is instead of up 50%.
[00:28:20] we've gotten over just the last uh few
[00:28:22] years, we've gotten uh spend has has you
[00:28:25] know already doubled um and it's going
[00:28:27] to double again, right? And and so what
[00:28:29] we've got is total spend has doubled and
[00:28:30] then when you look at the elasticity of
[00:28:32] different end markets um memory
[00:28:36] we've had the pricing, you know, go up
[00:28:37] like 4x and it's going to go up another
[00:28:39] 2x 3x again um in addition to capacity
[00:28:41] growth. And so you've got the stocks
[00:28:43] just like ripping like crazy um before
[00:28:45] going back down. And so I think you know
[00:28:47] what's really really exciting um about
[00:28:50] memory is it's not just an endmarket
[00:28:53] thing right it's not just oh the
[00:28:54] market's ripping and it's a very elastic
[00:28:56] good and and memor is a commodity and
[00:28:58] therefore uh the pricing of it is very
[00:29:00] elastic uh with the end market demand
[00:29:02] what's actually interesting and this is
[00:29:03] something we wrote in 2024 when 01 came
[00:29:06] out openai released 01 which was the
[00:29:08] first reasoning model um and it and it
[00:29:10] created a new boom of sort of reasoning
[00:29:12] models that you know openai anthropic
[00:29:14] deepseeek and many others have been
[00:29:15] exploiting uh to get the models to go
[00:29:18] long horizon agent tasks. Um so when we
[00:29:21] look at that what's interesting is when
[00:29:23] we when 01 came out the immediate thing
[00:29:25] we noticed is the workload changed
[00:29:27] dramatically. See when we were doing
[00:29:29] chat right when you're talking to chat
[00:29:30] GPT you may send a prompt that is you
[00:29:33] know it might be 50 words it might be
[00:29:34] 500 words but you're going to send a
[00:29:35] prompt and it's going to give you a
[00:29:36] response back and that ratio the context
[00:29:39] length is is you know a few thousand. So
[00:29:41] you might have a context length of let's
[00:29:43] call it 2,000. And what that means is,
[00:29:46] you know, when you're running inference,
[00:29:47] you you every time you generate a token,
[00:29:50] you read all the weights into the chip,
[00:29:52] you read all the context into the chip,
[00:29:54] you process a token, and then you and
[00:29:56] then you iterate again. You you read all
[00:29:58] the uh tokens uh the context and
[00:30:00] weights. And the context is called the
[00:30:01] KV cache, right? It creates this
[00:30:03] relationship between all these tokens.
[00:30:05] What's interesting is, you know, when
[00:30:07] you're when you're running a model
[00:30:09] inference on the weights side, if it's
[00:30:11] the context length is a thousand or if
[00:30:13] the context length is 100,000, you still
[00:30:15] have to read all the weights. So, memory
[00:30:16] intensity on inference is the same on
[00:30:19] the side of the weights, but on the side
[00:30:21] of the KV cache, right, the context your
[00:30:23] your memory when you have a thousand
[00:30:26] tokens that you're reading in versus
[00:30:27] 100,000 tokens is a humongous difference
[00:30:29] even though the compute amount is
[00:30:30] roughly the same. um you know the
[00:30:32] compute amount is you know because of KB
[00:30:34] cache uh uh caching on on memory and
[00:30:37] things like that you can you could sort
[00:30:38] of get away with your me your compute
[00:30:40] costs don't soar but your your memory
[00:30:43] costs sore and so what we highlighted in
[00:30:45] our 01 note was um in when in December
[00:30:48] of 2024 we talked about the scaling laws
[00:30:50] and how pre-training scaling laws were
[00:30:52] giving way to reasoning scaling laws and
[00:30:54] and 01 was a big uh step function change
[00:30:57] we talked about how KVach was going to
[00:30:59] explode because of reasoning and
[00:31:01] Therefore, memory was going to be the
[00:31:02] biggest winner. And so, we did that in
[00:31:04] December 24. And multiple times in 25,
[00:31:06] we were really excited about memory. But
[00:31:08] really in in in I think January of 26 is
[00:31:10] when we wrote the note which was talking
[00:31:12] about, you know, at the time people were
[00:31:13] like, okay, memory has gone up 50%. You
[00:31:15] know, is it the top of the cycle? Do we
[00:31:17] need to keep going? And we wrote a note
[00:31:18] that was basically like, no, no, no. Uh,
[00:31:20] I don't think you guys get it, right?
[00:31:22] Memory capacity is only growing 20, 30%
[00:31:24] a year for the next three years. And
[00:31:26] yet, demand is doubling, is doubling.
[00:31:28] And so what's going to end up happening
[00:31:30] is memory prices are going to keep
[00:31:31] soaring. Users of memory who are less
[00:31:34] elastic or less capable of uh adapting
[00:31:37] to the elasticity of pricing will drop
[00:31:39] out of the market. Uh smartphones,
[00:31:41] laptops because the costs are going to
[00:31:43] sore so much, they're going to drop out
[00:31:44] of the market and that's going to all
[00:31:46] give way to AI. Um and what that means
[00:31:48] is the price is just going to have to
[00:31:49] soar and soar and sore until that
[00:31:51] happens um to because capacity is not
[00:31:53] going up enough. And so ultimately our
[00:31:55] our point there was memory isn't a
[00:31:57] shortage and this is not a short-term
[00:31:59] shortage. It's a shortage that's going
[00:32:00] to last years. And and and so what we've
[00:32:03] seen so far over the last over the you
[00:32:05] know Q rest of Q1 and and now Q2 is is
[00:32:08] memory just been gang busters. It's been
[00:32:10] soaring. Uh there have been you know
[00:32:11] days where it's gone down 7 8% for some
[00:32:14] random reason. Uh but ultimately the
[00:32:16] chart has been up and to the right and
[00:32:18] you know where we where we uh not
[00:32:19] investment advice but where we see it
[00:32:21] continuing to go is is it's going to
[00:32:23] continue to soar because pricing
[00:32:24] continues to go up because we still
[00:32:27] haven't had we've had uh Chinese some of
[00:32:29] the Chinese uh smartphone makers in the
[00:32:31] mid-range and low end uh like Xiaomi say
[00:32:34] their their their shipments are down
[00:32:35] 40%. But we haven't seen the high-end
[00:32:37] market get impacted yet. And next year
[00:32:40] iPhone prices have to go up. Next year
[00:32:42] MacBook prices have to go up. And right
[00:32:44] now, you know, if MacBook prices or
[00:32:46] iPhone prices go up a hundred bucks,
[00:32:48] that market's not going to adjust too
[00:32:49] much. Uh, but that memory is going to
[00:32:51] keep getting more and more expensive
[00:32:53] until AI gets its fill. Um, and which
[00:32:55] which means, you know, smartphone prices
[00:32:57] aren't just going to go up 100 bucks.
[00:32:58] They're going to have to go up a few
[00:32:59] hundred bucks. And so, this is this is
[00:33:00] just the and and at some point there's
[00:33:02] going to be an equilibrium where AI gets
[00:33:04] the demand it needs and and and mobile
[00:33:06] and consumer hardware, you know, gets
[00:33:08] shucked pushed down enough, but
[00:33:09] obviously at some point people still
[00:33:11] need new phones and new laptops, so
[00:33:12] they'll still buy. So that we're going
[00:33:13] to have to reach a new equilibrium
[00:33:14] because this end market uh capacity of
[00:33:16] memory doesn't grow fast enough. And as
[00:33:18] we extend across the ecosystem, what
[00:33:20] really matters is hey a lot of different
[00:33:23] components are in shortage. Who is
[00:33:25] taking elastic? Who has an elastic price
[00:33:27] and who doesn't right an example is TSMC
[00:33:29] is not elastic on pricing, right?
[00:33:31] They're pretty they're a pretty good
[00:33:33] company, pretty fair with their
[00:33:34] customers partner long term. They're
[00:33:36] like we'll take up price 5 10%. Memory
[00:33:38] companies, they're in a commodity
[00:33:39] market. They're they let the spot market
[00:33:41] and contract market, you know, sort of
[00:33:42] supply demand balance really adjust
[00:33:44] pricing. And so you see these two three
[00:33:45] axes in pricing and and someday you'll
[00:33:48] see pricing half, right? Um you know,
[00:33:50] because memory necessarily doesn't
[00:33:52] deserve a margin of 85%. Right? Which is
[00:33:55] where it's headed to though, right? We
[00:33:56] are we're still not at 85 90% gross
[00:33:58] margins for memory, but we'll get there.
[00:33:59] And then at some point from there, it'll
[00:34:01] also half down back to like 70s or maybe
[00:34:03] even lower. Um and and so we'll see this
[00:34:06] oscillation in memory. In in in TSMC,
[00:34:08] you don't see so much oscillation. In
[00:34:10] other areas like ASML, we don't see much
[00:34:12] oscillation on the pricing, right? They
[00:34:14] make equipment, but different parts of
[00:34:15] the ecosystem will oscillate differently
[00:34:17] based on one, how much of the end AI
[00:34:20] demand flows through to them, right?
[00:34:23] Different parts of the supply chain are
[00:34:24] going to have, you know, for every
[00:34:26] dollar spent on AI, it might be one cent
[00:34:28] on this product, but it might be 5 cents
[00:34:29] on this product. And so, obviously,
[00:34:31] there's uh in in this end market, right,
[00:34:33] memory versus something else. Um and so
[00:34:35] ultimately different end markets in the
[00:34:38] infrastructure supply chain will benefit
[00:34:40] differently. But then in in terms of
[00:34:42] demand, but in addition, what are the
[00:34:44] market dynamics there? Is it one where
[00:34:46] there's a monopoly or an oligopy? Is
[00:34:48] there one where there's a very
[00:34:49] competitive large market? Is there one
[00:34:50] where the pricing is pretty stable and
[00:34:52] it's a lot of long-term agreements? Or
[00:34:54] is there one where it's it's quite a
[00:34:55] commodity market and pricing is based on
[00:34:57] supply demand? And so all of these
[00:34:59] factors determine whether a specific end
[00:35:02] market, whether it be memory or now
[00:35:04] people are talking about shortages of uh
[00:35:06] MLCC's or you know PCB drill bits or or
[00:35:10] PCB foil, copper foil or all these
[00:35:12] random components. You'll go online and
[00:35:14] see this is the next shortage. This is
[00:35:16] the next shortage. Um you you'll see all
[00:35:18] these different things, but what matters
[00:35:19] is how much flowthrough of demand is
[00:35:22] there actually. Is this end market
[00:35:23] doubling? Is it going up 50% or is it
[00:35:25] quadrupling? Right? um is how much is
[00:35:28] the pricing going to go up based on the
[00:35:29] market structure. These are what really
[00:35:31] determines what happens in the
[00:35:32] infrastructure supply chain
[00:35:34] >> and if you take that framework because
[00:35:37] it feels like yearbyear the market wakes
[00:35:39] up to exactly what you said a new quote
[00:35:42] unquote potential shortage. So earlier
[00:35:45] this year we have the open claw uh
[00:35:48] virality uh on various uh sites awakens
[00:35:52] people to the world of AI agents and all
[00:35:55] the possibility take the framework that
[00:35:57] you just described and I'd be curious to
[00:36:00] hear your take on the CPU market which
[00:36:03] for the first three years of AI I don't
[00:36:05] think I heard the word CPU and this year
[00:36:08] I'm hearing CPU everywhere.
[00:36:11] >> Yeah. Yeah. So um on on the side of
[00:36:13] CPUs, what's interesting is uh in some
[00:36:16] of our institutional research for our
[00:36:17] clients um in November last year, we
[00:36:21] started talking a lot about it and
[00:36:22] that's because OpenAI and Anthropic had
[00:36:24] started striking deals with Amazon,
[00:36:25] Google, uh Microsoft, etc. on buying all
[00:36:28] the CPUs they had in their fleets, uh
[00:36:30] renting them out. Um and then over the
[00:36:33] course of uh you know, uh late last year
[00:36:36] and and now this year, CPU demand has
[00:36:38] just been inflecting. And the reason
[00:36:39] why, right, let's talk about the reason
[00:36:41] first. So AI initially when it was
[00:36:43] training and inference um and inference
[00:36:45] was mostly a short context thing um it
[00:36:48] was it was mostly just predicated on
[00:36:50] compute and networking right but as
[00:36:53] training you know as pre-training
[00:36:55] shifted to reinforcement learning right
[00:36:57] and as uh you know chat style inference
[00:37:00] turned into agentic you know we had this
[00:37:02] big inflection of now CPUs are demanded
[00:37:04] more now why is that in the case of
[00:37:06] pre-training to reinforcement learning
[00:37:07] pre-training is all about like training
[00:37:09] the entire web data set on you know into
[00:37:12] your model. Whereas reinforcement
[00:37:13] learning is the model generates some
[00:37:15] synthetic data or generates a reasoning
[00:37:18] trace and then it checks it against an
[00:37:20] environment. That environment may be you
[00:37:22] know running unit tests on code. That
[00:37:24] environment may be you know a sandbox
[00:37:26] that looks like a website. Uh that
[00:37:28] environment may be you know a sandbox
[00:37:30] that looks like an engineering system or
[00:37:32] some other platform that you would use.
[00:37:34] Um whether it be like a website or
[00:37:36] shopping site or what have you. um it
[00:37:38] would be something that you utilize on
[00:37:40] the internet might be compiling the code
[00:37:41] and those environments require a lot of
[00:37:44] CPUs whereas before pre-training the
[00:37:46] actual processing of tokens didn't
[00:37:48] require much CPU it was all the
[00:37:50] environment checking right okay I've
[00:37:51] generated these tokens now are they
[00:37:53] valid what do they look like inside an e
[00:37:55] a whether it be a python you know or a C
[00:37:58] compiler or within a website if I'm
[00:38:01] trying to buy something you know
[00:38:02] e-commerce whatever it is as an agentic
[00:38:04] workflow I'm testing these things
[00:38:06] constantly that requires a lot of CPU
[00:38:08] And then the flip side is when you're
[00:38:09] doing live inference now when you're
[00:38:10] doing chat it's like okay I tell it
[00:38:12] something it gives me an answer back
[00:38:14] done okay I might ask it a few more
[00:38:16] questions but that's it but now when I
[00:38:17] talk about agentic workflows where the
[00:38:20] model is making tool calls right so it's
[00:38:22] like okay I'm going to go search for
[00:38:23] this it's like oh I'm going to look this
[00:38:25] up in a database oh I'm going to go uh
[00:38:27] ask uh the Python interpreter and I'm
[00:38:29] going to I'm going to write a little bit
[00:38:30] of code to check my work um oh I'm going
[00:38:32] to write some code and I'm going to
[00:38:33] compile it and and deploy it right these
[00:38:35] agentic flows end up requiring more and
[00:38:38] more and more CPU because they have to
[00:38:40] actually interact with the regular
[00:38:42] world, right? It was one thing if the
[00:38:43] human is interacting with the model
[00:38:45] where I'm telling the model something,
[00:38:46] the model gives me a response, I read
[00:38:47] it, I'm like, "Okay, copy and paste into
[00:38:49] whatever it is." It's a different thing
[00:38:51] when it's the model reacting with the
[00:38:53] internet world, right? And there there
[00:38:54] ends up being a lot more uh you know,
[00:38:56] compute in the loop, a lot more AI in
[00:38:58] the loop, uh or a lot more CPUs in the
[00:39:00] loop, sorry. Uh that are that are
[00:39:02] bouncing back and forth the answers. And
[00:39:04] so both of these whether it be
[00:39:05] reinforcement learning or agentic
[00:39:06] workflows need a lot of CPU. Now what
[00:39:09] has ended up happening now because okay
[00:39:11] we need a lot of CPU but let's let's
[00:39:13] evaluate the prior things in our
[00:39:14] framework right what is the market
[00:39:16] structure well okay so there's a few
[00:39:18] people in the market there's Intel and
[00:39:20] AMD uh you know there's ARM now
[00:39:22] releasing a CPU so ARM stock has has
[00:39:25] gone gang busters because of that
[00:39:26] because they're a new entrant into the
[00:39:28] market that looks pretty um competitive
[00:39:30] and then you've got you've got Amazon um
[00:39:33] who's the leader of this but also
[00:39:34] Microsoft and Google releasing their own
[00:39:36] CPUs that they've developed internally
[00:39:38] And then you've got Nvidia who's
[00:39:39] releasing their own CPU. And so you've
[00:39:41] got um you've got a lot of different
[00:39:43] competitors in the market, but really uh
[00:39:46] up until up until two years ago, all of
[00:39:48] the market was Intel and AMD. And now,
[00:39:50] you know, Amazon's gotten a good amount
[00:39:51] of share. Now Nvidia and a and ARM are
[00:39:55] starting to get more share. Um but
[00:39:57] ultimately what happens in the end
[00:39:58] market is well, Intel's actually able to
[00:40:00] increase their price. AMD is Apple
[00:40:02] actually able to increase their price.
[00:40:03] And so they've both increased their
[00:40:04] pricing. They've obviously gotten demand
[00:40:06] to go up a lot. Amazon is able to, you
[00:40:09] know, extract incredible margins out of
[00:40:10] CPUs because they don't make them and
[00:40:13] sell them. They make them and rent them.
[00:40:14] And so, you know, their Graviton CPUs
[00:40:16] are renting like crazy. Um, and they've
[00:40:18] they've increased the orders like
[00:40:20] massively. Nvidia, who was previously
[00:40:22] only selling CPUs attached to their
[00:40:24] GPUs, is now selling CPUs standalone,
[00:40:26] right, with Vera. And so, they they've
[00:40:27] given the guidance of uh 20 billion
[00:40:30] dollars of CPU revenue. Now for Nvidia
[00:40:32] that doesn't really scratch the surface
[00:40:33] of you know it's like okay that's like
[00:40:35] you know few percentage growth. No I'm
[00:40:37] just kidding. Um but you know I think I
[00:40:39] think you know when you look at other
[00:40:40] companies like Intel, AMD, ARM um Amazon
[00:40:43] you know who gets the the revenue
[00:40:45] instead of the just uh you know sales
[00:40:47] revenue there's there's huge things
[00:40:50] happening there. Dylan, maybe on the
[00:40:52] back of that um with CPUs now, some of
[00:40:55] the discussion at least that I've heard
[00:40:57] has been that it the the CPUs for agents
[00:41:02] are different than say the historical
[00:41:04] CPUs in some some regards. So the the
[00:41:06] cores are more optimized for agentic
[00:41:08] activity is uh what I remember hearing
[00:41:11] Jensen kind of saying or implying around
[00:41:13] the Vera CPU. Um and then there's also a
[00:41:16] lot of discussion around this GPU to CPU
[00:41:18] ratio which obviously you know
[00:41:20] highlights you know maybe the direction
[00:41:22] of uh of the demand and need for for
[00:41:25] CPUs. Can you maybe give us a little bit
[00:41:27] more color on you know each of those
[00:41:29] topics because I think you know it the
[00:41:32] concept I think makes a lot of sense at
[00:41:34] the high level to people but then there
[00:41:35] is I'll say some of the technical things
[00:41:37] that are I think are probably um maybe
[00:41:40] kind of pushed under the rug if if there
[00:41:42] are any. I'm not sure if it's just
[00:41:43] marketing or if there's a reality to
[00:41:45] this.
[00:41:46] >> So when it comes to agentic workflows,
[00:41:49] uh use of CPUs varies a lot, right? You
[00:41:51] have um you have some workflows in
[00:41:53] Agentic, it's like, okay, if my model's
[00:41:56] running and then I send a response to,
[00:41:58] you know, send all the tokens to some
[00:42:00] CPU workflow
[00:42:02] and and then I'm waiting on the CPU to
[00:42:03] do something and then I send it back to
[00:42:05] the model and the model works some more.
[00:42:07] The question is a did the mo did the
[00:42:09] compute that the model's running on
[00:42:10] stall while you're waiting for the CPU
[00:42:12] and in some cases it does in some cases
[00:42:14] it doesn't and in the cases where it
[00:42:16] does stall right the compute that's
[00:42:17] running the model just stalls waiting
[00:42:19] for the CPU's response then the CPU
[00:42:21] needs to be very architected very
[00:42:23] differently right um you know you know
[00:42:25] the basic concept is do I want more
[00:42:27] cores or do I want faster cores and you
[00:42:30] know there's sort of there's sort of
[00:42:31] like a a law within you know CPU
[00:42:33] architecture which is basically if you
[00:42:35] make the CPU core twice as big, right?
[00:42:37] Which means I have half as many CPU
[00:42:39] cores on the chip. My performance
[00:42:41] doesn't go up 2x per CPU core. My per
[00:42:44] CPU core performance may only go up 50%.
[00:42:46] Um, obviously there's a lot of
[00:42:47] engineering and that that that the
[00:42:49] trade-off is not that simple, but you
[00:42:51] know, to to simplify simplify, that's a
[00:42:53] simple way to think about it. So, if I
[00:42:54] look at an Nvidia CPU for Vera, right,
[00:42:58] it has less than 100 cores, but those
[00:43:00] cores are faster than the AMD cores.
[00:43:03] AMD's leading CPU has 256 cores. So
[00:43:05] you've got this big delta number of CPU
[00:43:07] cores, but the a the Nvidia core is
[00:43:10] faster, but it's not twice as fast,
[00:43:13] right? It's not twice as fast as AMD CPU
[00:43:15] core. And so there's this sort of
[00:43:16] trade-off that people are making on the
[00:43:18] design space. And for some workloads
[00:43:20] where the the AI compute has to stall
[00:43:23] while waiting for the CPU, then you need
[00:43:25] you know what, who cares if I spend, you
[00:43:28] know, if I have half as many cores and
[00:43:29] they're only 50% faster. And so in total
[00:43:31] the performance of the CPUs is less but
[00:43:34] the per core performance is higher and
[00:43:36] therefore I'm never I'm not waiting on
[00:43:37] the CPU cores as often right I don't
[00:43:39] need a super parallel workload what I
[00:43:41] really need is this one workload done
[00:43:43] now right and and so you know in that
[00:43:45] case where the AI compute is stalling I
[00:43:48] want to have the fastest core possible
[00:43:50] and I'm willing to sacrifice multi-core
[00:43:52] performance and so that's some types of
[00:43:54] agentic workflows other types of agentic
[00:43:56] workflows right if I talk about how I
[00:43:58] use claude uh day-to-day or how the team
[00:44:00] uses is Claude. How we spend $11 million
[00:44:02] a year on Claude on a ARS basis. Um what
[00:44:05] is that? Well, I'm calling Claude.
[00:44:08] Claude is processing a bunch of tokens,
[00:44:09] but they're not just using only me.
[00:44:11] They're batching, you know, hundreds of
[00:44:12] thousands of users together, right,
[00:44:14] across all of their compute. And so if
[00:44:17] if I get the response back and now it's
[00:44:19] waiting on me to implement it, whether
[00:44:21] it's waiting on me or a CPU core to
[00:44:23] implement it somewhere, you know, you
[00:44:24] end up with this um that's okay because
[00:44:27] the computer is still running, just not
[00:44:28] for me. it's running for other people,
[00:44:30] right? So, so if the CPU is slower but I
[00:44:33] get way more of them, it's a different
[00:44:35] sort of task, you know, and and another
[00:44:37] one is sort of like is it the active use
[00:44:39] of AI or is it the use of is it what's
[00:44:41] AI generated and then you're taking what
[00:44:43] AI generated and deploying it, right?
[00:44:45] The beauty is uh you know, if we look at
[00:44:47] GitHub commits globally, they're up
[00:44:49] multiplefold versus last year, right?
[00:44:52] Not just it's not just like a oh total
[00:44:54] GitHub commits are 10% up or 50% up. No,
[00:44:57] no, no. They're up like multiple X. And
[00:44:59] what that means is all this code is
[00:45:00] being generated to the world and people
[00:45:02] are deploying a lot of the code. A lot
[00:45:03] of the code is sloped, but a lot of code
[00:45:04] is being deployed. And when it gets
[00:45:06] deployed, it's being put on CPUs. And
[00:45:08] it's standard code, right? It might just
[00:45:09] be like a web scraper. It might be like
[00:45:10] some analytical engine. It may be some
[00:45:12] business process automation. That
[00:45:14] doesn't necessarily need to be on a
[00:45:16] super fast CPU core. It can be on a
[00:45:18] cost-effective CPU core. And so when you
[00:45:20] look at the continuum, right, Nvidia has
[00:45:22] built the highest performance CPU core,
[00:45:25] but it's not necessarily giving you, you
[00:45:27] know, if I have AC a chip, what is the
[00:45:29] maximum number of CPU cores times the
[00:45:31] performance per core, right? They're
[00:45:33] actually not so great at that. Whereas
[00:45:34] if I look at AMD and Amazon, right, they
[00:45:37] have they have a lot more cores, right?
[00:45:39] Hundreds, but they have less per core
[00:45:42] performance. And so you end up with this
[00:45:43] like trade-off of um you know, and and
[00:45:46] ARM is on that end too, right? And so
[00:45:48] where in that continuum do you want to
[00:45:49] go? And for some workloads you do want
[00:45:51] Vera and for some workloads you want the
[00:45:52] Graviton or the AMD CPU. And I I
[00:45:55] wouldn't say it's as simple. Now as far
[00:45:56] as the other question you mentioned
[00:45:57] which is ratio. Um it is indisputable
[00:46:00] that CPU demand is going up. We were the
[00:46:02] first to call it out uh late last year
[00:46:04] in our institutional research and and in
[00:46:05] January this year in our in our
[00:46:07] newsletter and since since we published
[00:46:09] that some of these CPU stocks have
[00:46:11] ripped. ARM has gone up multiple X
[00:46:13] right. Um Intel, Nvidia, uh Intel's gone
[00:46:15] up multiple X. Um AMD's ripped. Uh these
[00:46:18] stocks have ripped. But now the sellside
[00:46:20] who doesn't really understand technology
[00:46:22] at all is just making up stuff. Um and
[00:46:25] is getting to the point where the ratio
[00:46:26] of CPUs to GPUs or ratio of CPUs to uh
[00:46:29] AI compute is getting lopsided to the
[00:46:31] point where it's more in the favor of
[00:46:32] CPUs than it is AI compute. That's
[00:46:34] false, right? Um you know, just to
[00:46:37] reiterate, right, if you look at a
[00:46:38] Blackwell full allout Blackwell, it's
[00:46:40] like 50 something thousand per chip. If
[00:46:43] you had a one:1 ratio, CPUs cost like
[00:46:45] $5,000, right? And so you end up with,
[00:46:48] okay, well then for $300 billion of
[00:46:50] Blackwell to sell or $500 billion of
[00:46:52] Blackwell to sell, you would only get,
[00:46:54] you know, you know, uh, you know, you'd
[00:46:57] get 30 billion or $50 billion of CPU
[00:46:59] sales, right? And so that's sort of like
[00:47:01] another thing that people are start
[00:47:02] missing. Like yes, this end market is
[00:47:04] ripping. Ultimately, the majority of the
[00:47:06] dollars are still going to AI compute
[00:47:08] and memory. uh this market was
[00:47:09] underpriced
[00:47:11] and it's more fairly priced now, right?
[00:47:13] And I think that's something that people
[00:47:14] need to recognize is it's not like CPUs
[00:47:17] CPUs are going to like keep growing and
[00:47:18] growing in demand beyond that of AI AS6.
[00:47:21] It's it's a bit of a like a right
[00:47:23] sizing, right? So basically in 23 24
[00:47:26] there were years of selling millions of
[00:47:28] AI chips and very few CPUs. Now all of a
[00:47:30] sudden the CPU demand is inflected to
[00:47:32] now the ratio shouldn't be here, it
[00:47:34] should be here. And people are in
[00:47:35] catch-up mode. And so now I need to buy
[00:47:37] a bunch of CPUs to catch up all the
[00:47:39] compute I've historically bought as well
[00:47:41] as in addition to the compute I'm
[00:47:42] currently buying. Well, once I catch up
[00:47:44] that, you know, backlog of all these AI
[00:47:46] chips that I had bought previously and I
[00:47:48] catch them up for CPUs. Well, that
[00:47:51] demand isn't there anymore, right? I've
[00:47:52] already caught it up and now it's only
[00:47:53] the incremental. And so, you know, if
[00:47:55] you if you think about it, right? um if
[00:47:57] there's a ratio, you know, of let's say
[00:47:59] one to two, one G, one CPU to two GPUs,
[00:48:03] um and each of those GPUs cost, let's
[00:48:05] say, $50,000 and each of those CPUs cost
[00:48:07] $5,000. Well, then for every $100,000
[00:48:10] I'm spending on GPUs, I'm spending
[00:48:11] $5,000 on CPUs. And and that's actually
[00:48:14] not that great of a market dynamic. Uh
[00:48:16] in terms of CPU growth, it's still great
[00:48:18] for CPUs. It's way better than it used
[00:48:19] to be. But if you flip back to, oh well,
[00:48:22] what happens if, you know, I have 10
[00:48:24] million GPUs in AI6 that I shipped over
[00:48:27] the last three years that don't have any
[00:48:28] CPU attached really. Okay. Well, now
[00:48:30] that one that 5,000 has a huge catch-up,
[00:48:33] right? And so that's what we're
[00:48:34] experiencing right now is a huge
[00:48:35] catch-up as well as the the ratio has
[00:48:37] shifted up and then that huge backlog is
[00:48:39] getting caught up and and so you're
[00:48:41] seeing like demand be ridiculous, but it
[00:48:43] will it'll it will sort of subsume and
[00:48:45] then it'll be at a steady state, right?
[00:48:46] We're in sort of a mini cycle of CPU.
[00:48:49] No, that's that's excellent context.
[00:48:51] Really really helpful. Um, and then
[00:48:53] maybe just moving to networking to kind
[00:48:55] of, you know, move into another, you
[00:48:57] know, area of the stack. I think this is
[00:48:59] one that's come to a lot of investors
[00:49:01] attention, uh, particularly as they dive
[00:49:03] down, you know, I'll say the optics
[00:49:05] supply chain and some of the constraints
[00:49:07] there. Um, and we're seeing some
[00:49:09] estimates that, you know, co-acked
[00:49:11] optics is maybe something that's talked
[00:49:13] about a lot, but is really probably
[00:49:15] going to be deployed um, 2028 or so,
[00:49:19] 2027, 2028. Um, as you think about the
[00:49:23] I'll say there's obviously this u, you
[00:49:26] know, the concept of, you know, you
[00:49:29] know, using copper when you can, optics
[00:49:31] when you must, and this kind of
[00:49:33] transition um, from optics to copper.
[00:49:36] And then we also had uh Jensen um
[00:49:39] talking a lot about it at Computex as
[00:49:41] well. Um and you know a lot of other
[00:49:43] discussions in propping up um or at
[00:49:45] least bringing a lot of attention to
[00:49:47] firms like Marll. Um is there I mean is
[00:49:50] there any I guess additional thoughts
[00:49:52] you have around you know optics and kind
[00:49:54] of how you see the architecture of the
[00:49:56] data center within the networking domain
[00:49:58] evolving over the next two years.
[00:50:00] Yeah, I mean it's it's pretty clear um
[00:50:03] as models get bigger, how do we run them
[00:50:05] across models? As how do we train
[00:50:07] models? Uh there's a lot of different
[00:50:08] domains within the optical stack, right?
[00:50:11] There's telecom optics, you know,
[00:50:12] companies like Sienna have been ripping
[00:50:14] um and many of the constituent supply
[00:50:16] chains around them. Um you know, you
[00:50:18] look at you look at datacom, right? chip
[00:50:20] to chip communications that's, you know,
[00:50:22] got a copper domain that's got optics
[00:50:23] domain today and those are all ripping
[00:50:25] because the growth of networking content
[00:50:26] is faster than the growth of any other
[00:50:29] content um you know in terms of
[00:50:31] percentage right networking is going
[00:50:33] from you know sub 10% to above 10% of
[00:50:36] spend associated with AI chips and when
[00:50:38] we get to CPO networking grows even
[00:50:41] further it's like 20 30% right so we've
[00:50:43] got this huge uplift in networking
[00:50:44] content but you know on the flip side is
[00:50:47] you know CPO is such a huge step
[00:50:50] function change in the industry and
[00:50:51] everyone sort of recognizes CPO now. Um
[00:50:55] but it's it's you know I think people
[00:50:56] are getting a little exuberant today.
[00:50:57] Currently there's a little bit of I
[00:50:58] would say currently people are a little
[00:51:00] bit too excited on CPO. Um it's not
[00:51:02] coming in 27 in my view. Um really in
[00:51:05] the tail end of 28 but 29 is the real
[00:51:08] ramp for scale up co- package optics. Uh
[00:51:12] there's been a lot of problems. It's
[00:51:13] it's it's a manufacturing thing right.
[00:51:15] If we could deploy it today at good cost
[00:51:17] amazing everyone would do it. But it's
[00:51:19] it's really hard. The manufacturing
[00:51:20] volumes are not there. The yields aren't
[00:51:22] there. Uh the chips aren't really
[00:51:24] designed there yet. It's like it's a
[00:51:25] very complex, difficult thing to ramp.
[00:51:27] And so people are going to stay in
[00:51:28] copper as long as they can. And that
[00:51:30] means, you know, uh Reuben is all
[00:51:32] copper. Uh Fineman on the GPU is still
[00:51:35] copper, right? Which is next generation
[00:51:37] Nvidia GPU. After Ruben, Reuben Ultra,
[00:51:39] then Fineman. Uh and we're not even at
[00:51:40] Ruben shipping yet. Um so sort of Reuben
[00:51:43] just starting to ship. So sort of we've
[00:51:44] got a few generations of chips before we
[00:51:47] get to co-ackage optics on the GPU.
[00:51:49] There's co-ackage optics on switches
[00:51:51] which is coming earlier than on the GPU
[00:51:52] or the AIS. Um but ultimately that's
[00:51:56] sort of you know I would say even
[00:51:58] without that though right as the cluster
[00:52:00] size gets bigger you need more optics
[00:52:02] per GPU and so or or more uh active
[00:52:04] electrical cables and things like that.
[00:52:06] So we've what we've seen is this big
[00:52:07] dynamic and shift and so like uh
[00:52:09] actually on Monday um we released a note
[00:52:13] uh at semi- analysis for our
[00:52:14] institutional research subscribers which
[00:52:16] was on a localized time you know not
[00:52:18] saying end market right obviously the
[00:52:19] technology our our agreement of CPO is
[00:52:21] going to happen we've been pushing that
[00:52:22] for a long time our agreement is you
[00:52:24] know copper will subsume over time but
[00:52:27] on a medium-term basis we're actually
[00:52:29] very bullish copper and we're very
[00:52:30] bullish optics that aren't CPO and we're
[00:52:33] actually kind of bearish on CPO um
[00:52:36] because of certain delays on chips that
[00:52:38] we see downstream, right? fine men not
[00:52:40] being full of CPO um you know and and
[00:52:43] other things like that uh that we've
[00:52:45] seen uh where copper names like Amphanol
[00:52:48] right who make all the backplane
[00:52:49] connectors and and cables are actually
[00:52:51] going to do way better over the next few
[00:52:53] years than previously expected because
[00:52:54] we previously thought CPO would ramp
[00:52:56] sooner but now it's delayed out and so
[00:52:58] things like this happen in the supply
[00:52:59] chain but ultimately
[00:53:02] optics is one which if you close your
[00:53:04] eyes today and open it 5 years from now
[00:53:06] it's going to be way bigger um a lot of
[00:53:08] that is priced into stocks. A lot of
[00:53:09] that isn't and I'd say there's some
[00:53:11] local disjunctions. Um, but this is sort
[00:53:13] of like part of the the research that we
[00:53:15] kind of do and and uh work that we've
[00:53:17] been doing with you folks as well is is
[00:53:19] how do we weight that, right? How do we
[00:53:20] weight, you know, what amount is is, you
[00:53:22] know, CPO favored optics versus nonCPO
[00:53:24] optics, right? Typical optical
[00:53:26] transceivers versus copper, right?
[00:53:28] Because copper has actually got a long
[00:53:29] ways to go. Uh, there's a lot of things
[00:53:32] happening in the copper industry that
[00:53:33] are innovating and pushing back CPO,
[00:53:36] right? It's like why would I do CPO?
[00:53:37] because at the end of the day,
[00:53:38] integrating optics is so much more
[00:53:40] expensive than sending something
[00:53:41] electrically. Except if I have to send
[00:53:43] something electrically, I can't go that
[00:53:44] far unless I add repeaters or optics.
[00:53:46] And so there's like this this trade-off
[00:53:48] and continuum and and CPO will happen,
[00:53:50] but it looks like it's getting pushed
[00:53:52] out a little bit.
[00:53:53] >> And and Dylan, as as we sort of go into
[00:53:56] our probably uh we we probably have time
[00:53:58] for our last overall topic, we we've
[00:54:00] done models, GPUs, CPUs, memory,
[00:54:04] networking.
[00:54:06] uh we'd probably be remiss to not
[00:54:08] mention uh the elephant in the room at
[00:54:10] any data center which is how how are you
[00:54:13] getting the electricity and and how are
[00:54:15] you sort of getting that electricity
[00:54:17] into the the form and I know you you've
[00:54:19] you've written through the newsletter at
[00:54:21] least certain things about direct
[00:54:22] current versus alternating current and
[00:54:25] uh c certain elements that in theory
[00:54:28] when you when you see the hyperscalers
[00:54:30] spending all this money building these
[00:54:31] data centers potentially even putting
[00:54:33] the power plants on site behind in the
[00:54:36] meter. H how are we to think about the
[00:54:40] electrical demand sort of the grid
[00:54:43] versus non-grid? And I know I know it's
[00:54:44] a big topic, but I feel like we'd be
[00:54:46] remiss to not at least mention it here.
[00:54:49] >> Yeah. So, I would say um you know, data
[00:54:52] center growth is massive. This year
[00:54:54] we're deploying 20 gigawatts of data
[00:54:56] centers. Um next year that number goes
[00:54:58] up 50 gawatts or 50% sorry uh 50% sorry
[00:55:02] uh 50 g 30 g 30 gigawatts um and then
[00:55:06] and then and then it'll be 50 gawatts
[00:55:08] the year after that. The the growth in
[00:55:09] data center capacity is massive. Um
[00:55:12] there's a lot of like local disjunctions
[00:55:14] that people are having to deal with
[00:55:15] right and so sort of I would say energy
[00:55:18] is one of the biggest ones. The other
[00:55:19] one is sort of political um and third is
[00:55:22] like sort of construction. Building data
[00:55:23] centers and getting permits and filings
[00:55:24] is kind of tough politically. people are
[00:55:26] trying to stop it, but the primary
[00:55:28] factor gating it is really um the energy
[00:55:31] at the end of the day, right? And and
[00:55:32] and so what's what's happening there is
[00:55:34] energy you can break down into a few
[00:55:35] things, right? There's generation,
[00:55:37] right? Where do I generate the electrons
[00:55:38] from? There's transmission. How do I
[00:55:40] transmit the electrons from where it was
[00:55:42] generated to the data center? And then
[00:55:43] there's conversion, right? Because the
[00:55:44] power that it gets transmitted at is at
[00:55:47] a is a form factor that the chips cannot
[00:55:49] consume. And so the chips need to
[00:55:51] consume it at a different form factor.
[00:55:52] What does that conversion pipeline look
[00:55:53] like? And I think in all three of these
[00:55:56] there are very bullish aspects right in
[00:55:58] the transmission side uh that's the one
[00:56:00] that's the hardest to be bullish on
[00:56:01] because um you know the the regulatory
[00:56:04] and political difficulties with building
[00:56:06] more uh transmission capacity and the
[00:56:08] way local monopolies of utilities work
[00:56:10] and how if they build a utility line
[00:56:12] they have to amortize it across all
[00:56:14] users not just individual user. there's
[00:56:15] all these various weird dislocations
[00:56:17] with transmitting power and so building
[00:56:19] more grid capacity is kind of difficult
[00:56:21] on a transmission basis. But
[00:56:23] generationwise and convergence wise
[00:56:25] there are two interesting things. So
[00:56:26] generation wise obviously there's more
[00:56:28] generation happening on the grid.
[00:56:30] There's also this big shift to
[00:56:31] generating for the data center. So we
[00:56:33] were predict in in a couple years half
[00:56:35] of the power for data centers for
[00:56:37] incremental new power for data centers
[00:56:38] will be generated on-site not offsite.
[00:56:41] Um and so behind the meter is soaring.
[00:56:43] Um, and we see this, you know, with the
[00:56:45] behind the meter tracker we have in our
[00:56:46] data center and energy models. Um, with,
[00:56:48] you know, I mentioned, you know, someone
[00:56:49] in our team, she she she built a power
[00:56:51] plant in Kazakhstan. She's leading our
[00:56:53] energy model, um, Ellie. And so, she she
[00:56:56] sort of been tracking and we've been
[00:56:57] building this model, the entire grid,
[00:56:58] every generation asset, every
[00:57:00] transmission asset, um, all the load
[00:57:02] assets as well as all the um, you know,
[00:57:04] behind the meter work. And what's
[00:57:05] interesting is we've seen this huge boom
[00:57:07] in behind the meter. Um, there's been a
[00:57:09] lot to fight the permitting and
[00:57:10] regulatory side there. um you know
[00:57:12] whether it be people not wanting to
[00:57:14] allow air permits or people wanting to
[00:57:16] have um you know uh not allowing the gas
[00:57:20] pipeline to be built to the side or
[00:57:22] things like that. We've seen that with
[00:57:23] an Oracle data center. Uh there's a lot
[00:57:25] of different aspects of this that are
[00:57:26] happening but ultimately the end state
[00:57:28] of it is that behind the meter is
[00:57:30] soaring right and a lot of that is um
[00:57:32] gas you know you know lot a lot of it
[00:57:35] was you know dual combine cycle gas uh
[00:57:37] reactors from GE Vernovar Mitsubishi
[00:57:41] um or Seammens but beyond that there's
[00:57:43] also been a lot of different types of
[00:57:44] energy sources right there's
[00:57:46] reciprocating engines there's industrial
[00:57:48] gas turbines um there's various types of
[00:57:51] diesel engines uh there's train engines
[00:57:54] People have taken train engines, people
[00:57:55] have taken boat engines, people have
[00:57:57] taken uh truck engines and converted
[00:57:59] them into power generation for data
[00:58:01] centers. So we see a sea of innovation
[00:58:02] happening there. It's not like we don't
[00:58:04] have the industrial capacity, right? Um
[00:58:06] you know the US is has makes millions
[00:58:08] can make millions of industrial uh uh
[00:58:11] sorry reciprocating engines a year,
[00:58:12] right? This is just engines that burn
[00:58:14] fuel and spin. Um and it's pretty
[00:58:16] trivial to retool those to be for gas
[00:58:18] rather than diesel. But even if it's
[00:58:19] diesel, that's fine. Um, and then you
[00:58:22] stick a you you you stick a um
[00:58:24] electrical engine on it and and
[00:58:26] basically back back drive it and then
[00:58:28] that generates electricity. And so then
[00:58:30] you can do this in like large large
[00:58:32] volumes to generate power. Um and so we
[00:58:34] see you know 10 gawatts plus of data
[00:58:36] centers that are going to be built with
[00:58:38] technologies like this right taking
[00:58:39] diesel truck engines converting them to
[00:58:41] gas uh which can be done at the time of
[00:58:43] production very simple um put back back
[00:58:45] driving a electrical motor um and then
[00:58:48] sticking them on site on a data center
[00:58:49] and you have hundreds of these backing a
[00:58:51] data center and then you hire a bunch of
[00:58:52] people from car mechanic shops and if
[00:58:55] you know these things need to be
[00:58:56] serviced right and so they just run
[00:58:57] around servicing these diesel engines
[00:58:58] all day um you know and and and so you
[00:59:01] have some buffer so that you don't like
[00:59:03] you know you know when they go down you
[00:59:04] you can service them and keep them going
[00:59:06] and have the max power and obviously you
[00:59:08] need some batteries in between because
[00:59:10] you don't want the you know the up and
[00:59:12] down of the data center uh to mess with
[00:59:14] to blow up the engines that you've got.
[00:59:16] Um and so you've got like this entire
[00:59:18] supply chain of behind the meter uh
[00:59:19] which is exciting but in addition you've
[00:59:21] got you know over you know in about 2
[00:59:23] years uh solar plus battery will be
[00:59:25] cheaper than gas. Uh now supply chains
[00:59:29] for solar plus battery are difficult. Um
[00:59:31] and it depends on what level of
[00:59:32] reliability you want. If you're if you
[00:59:35] have just enough battery for to get
[00:59:36] through the night, it's cheaper. But
[00:59:37] what if you you need enough batteries to
[00:59:39] get through the night? Three three days,
[00:59:41] right? Because it might rain for two
[00:59:42] days. You know, things like this, you
[00:59:43] know, how many nines of reliability do
[00:59:45] you want? But solar plus battery are
[00:59:47] getting cheaper and cheaper at an
[00:59:48] incredible pace because of China's
[00:59:49] manufacturing excellence. Um and and
[00:59:51] some of the subsidies too. um that you
[00:59:53] know it's going to get cheaper at one
[00:59:55] point to uh at some point to do solar
[00:59:57] plus battery. Um and then you've got
[00:59:59] space data centers, right, where you
[01:00:00] don't even need a battery, you just
[01:00:01] stick it in space and you've got a solar
[01:00:02] panel and that's it, right? Um and so
[01:00:04] you've got this whole continuum of ways
[01:00:06] to generate power. Um whether it be all
[01:00:09] the way, you know, taking diesel engines
[01:00:11] and making them gas engines or, you
[01:00:13] know, using dual combine cycle engines
[01:00:15] all the way downstream to, you know,
[01:00:16] let's just ship the chips into space
[01:00:18] instead, right? So there's the whole
[01:00:20] continuum. Um and and there's a lot of
[01:00:22] money to be made there. There's a lot of
[01:00:24] interesting dynamic things to do there.
[01:00:25] That's why you know um actually the
[01:00:27] largest uh data set and uh research
[01:00:30] vertical for semi analysis which you
[01:00:32] think is semiconductors is actually data
[01:00:34] centers and energy. It's data centers
[01:00:35] industrials and energy. It's we call it
[01:00:37] the DEI team. The data center energy
[01:00:39] industrial. It's it's a pun internally.
[01:00:42] You know the tag is at DEI team. Um so
[01:00:44] Jeremy he leads that team. He came up
[01:00:46] with the name. Um but anyways, so data
[01:00:49] centers, energy and industrials, uh
[01:00:51] that's actually our biggest research
[01:00:52] vertical because we're tracking every
[01:00:54] data center in every power plant. And so
[01:00:56] the market, you know, when we when we
[01:00:57] identify like a delay or this is
[01:00:59] happening or there's going to be this
[01:01:00] build or this company's going to have
[01:01:02] this many data centers go online in this
[01:01:03] quarter, it's something that no one else
[01:01:05] in the industry can do. And that's sort
[01:01:06] of like why it's one of our biggest um
[01:01:08] verticals and and everyone's interested
[01:01:09] in that, right? Google's interested in
[01:01:11] what Meta is able to deploy. Meta's
[01:01:12] interested in what OpenAI is able to
[01:01:14] deploy, but also all of these guys are
[01:01:16] looking at what the supply chain is able
[01:01:17] and who has capacity and then also all
[01:01:19] the investors are looking. So that's
[01:01:20] like our biggest data set. But I would
[01:01:22] say it's one where it's a market where
[01:01:24] it's very decentralized, right? In the
[01:01:27] case of like memory, there's three
[01:01:28] names. You know, it's pretty simple. In
[01:01:30] the case of like, you know,
[01:01:31] accelerators, there's just a few names.
[01:01:33] In the case of like uh semiconductor
[01:01:35] wafer fabrication equipment, there's
[01:01:36] just a few names. In the case of this,
[01:01:38] there are hundreds of names in the
[01:01:40] supply chain, you know, making all these
[01:01:42] random little widgets. There's dozens of
[01:01:44] companies building data centers. Um, you
[01:01:46] know, and and there's dozens of
[01:01:48] companies trying to do whether you're
[01:01:49] being an indust IP as power producer or
[01:01:52] you're doing it behind the meter, you're
[01:01:53] offering some sort of battery service or
[01:01:55] all these different things. It's a very
[01:01:56] complex supply chain. Uh, but one that
[01:01:59] has a lot of dynamicism and ultimately I
[01:02:02] think there's a lot of innovation
[01:02:03] happening. And so while data centers
[01:02:05] will continue to be a constraint of
[01:02:07] sorts, they will also not be a
[01:02:09] constraint because, you know, it depends
[01:02:11] on how crazy you're willing to go. But
[01:02:13] like I said, you can just take truck
[01:02:16] engines and convert them and and hire a
[01:02:18] bunch of mechanics and and run a site
[01:02:20] like that. It's not going to be the
[01:02:22] best. You know, a lot of people say,
[01:02:24] "Uh, that's disgusting. How reliable is
[01:02:26] that going to be?" You know, "Oh, that's
[01:02:27] going to be really annoying to do." But
[01:02:28] people are doing it and it will work and
[01:02:31] it's a pain in the ass, but it will
[01:02:33] work. You know, all the way to like I'm
[01:02:34] going to ship shoot it into space. It's
[01:02:37] going to be a pain in the ass. It's
[01:02:38] going to be really hard to make it work,
[01:02:39] but it will work. And so, you know,
[01:02:41] you've got solutions to the data center
[01:02:43] problem, whether it be, you know, going
[01:02:45] full dirty or going fully into space. Um
[01:02:49] whereas other parts of the supply chain,
[01:02:50] you don't. And so, I think that's what
[01:02:52] makes this market so dynamic is you're
[01:02:53] going to see people go up and down a
[01:02:54] lot. Um Yeah. And then and then I guess
[01:02:58] the other part so that's on the
[01:02:59] generation and transmission side but on
[01:03:01] the conversion side is the other thing
[01:03:02] right how do you get the power from
[01:03:04] where it is uh you know what it gets
[01:03:06] generated at or it gets transmitted at
[01:03:08] to what the chips want and there's an
[01:03:09] entire supply chain of you know stuff
[01:03:11] going on there whether it be IGBT
[01:03:13] silicon carbide uh you know various
[01:03:16] types of MOSFETs um GAN gallium nitride
[01:03:19] MOSFETs all the names there you know
[01:03:21] what happens when we go from 12 volt to
[01:03:23] 54 volt to 800 volt DC and the
[01:03:26] conversion supply chain in there. What
[01:03:27] happens with solid state transformers as
[01:03:29] those get innovated? All these things
[01:03:31] are happening in the space. What happens
[01:03:32] with UPS's you know uh universal power
[01:03:35] uh supply? Is it universal power supply?
[01:03:37] Battery backups and super capacitors and
[01:03:40] all these other different ways to smooth
[01:03:42] out the power make it make it from you
[01:03:44] know the dirty uh variable power that
[01:03:47] gets created on the left side to the
[01:03:50] super clean power but also variable
[01:03:51] usage of it on the right side. How do
[01:03:53] you match that? that entire conversion
[01:03:55] pipeline is one that's super super
[01:03:56] exciting. And so we had a blog on that
[01:03:58] and 800 volt just last week. Um and
[01:04:01] we've talked about more recently to our
[01:04:02] institutional subscribers some um delays
[01:04:04] that are happening there um on the uh
[01:04:07] side of Nvidia as they delay it out of
[01:04:09] uh Kyber. Reuben Ultra Kyber doesn't
[01:04:11] have 800 volt anymore. And so what does
[01:04:13] that mean for the supply chain? Well, it
[01:04:14] gets pushed out a little bit.
[01:04:17] >> So Dylan, I want to uh thank you
[01:04:20] profusely uh on our side. This is this
[01:04:22] is the first episode if we think in
[01:04:25] terms of of chapters. Uh this this will
[01:04:27] be the first time uh we've had Dylan on
[01:04:29] the podcast, but but certainly not the
[01:04:31] last uh because there's a lot more
[01:04:34] information and like he said uh directly
[01:04:36] numerous times across uh the entire
[01:04:38] stack. Everything's changing all the
[01:04:40] time. It's uh it's a bear to to keep
[01:04:43] track. But um as as many people
[01:04:46] [laughter]
[01:04:48] >> the other thing I would say is this
[01:04:49] supply chain is so freaking crazy. Um
[01:04:52] and and and you know a lot of times we
[01:04:53] talk about the big ones right memory
[01:04:56] CPUs you know data centers but actually
[01:04:58] when you drill down to the supply chain
[01:05:00] the local bumps are very small and many
[01:05:03] right uh you know for a couple months we
[01:05:05] were talking about PCB drill bits right
[01:05:07] the drill bits that drill into PCBs for
[01:05:08] the holes for for uh you know it's like
[01:05:10] it's like random like copper foil that
[01:05:12] goes on PCBs there's all these random um
[01:05:15] you know small things in the supply
[01:05:16] chain that also have these dislocations
[01:05:18] and also the companies that exist in
[01:05:20] them are all over the They could be
[01:05:21] trading in Taiwan. They could be trading
[01:05:23] in Japan. They could be trading in
[01:05:24] Korea. They could be trading in, you
[01:05:26] know, um, in all parts of the world.
[01:05:27] It's not just easily accessible to
[01:05:29] investors. And so, I think that's what's
[01:05:31] really exciting about, you know, our
[01:05:32] partnership and the way we're working
[01:05:33] together is, you know, we we get to we
[01:05:35] get to influence sort of, you know,
[01:05:37] what's going on. We get to talk a lot
[01:05:38] about these these supply chain
[01:05:40] disruptions, but also what's what's
[01:05:42] really interesting in the framework that
[01:05:44] I laid out earlier and and the entire
[01:05:46] landscape that we're trying to cover. Um
[01:05:48] and so you know looking forward to
[01:05:49] coming back on the show more and our
[01:05:50] other collaborations.
[01:05:52] >> Absolutely. And with that I do have to
[01:05:56] state one thing here uh for our
[01:05:58] compliance team to clarify the views and
[01:06:00] opinions expressed in this podcast or
[01:06:02] those of wisdom tree and are subject to
[01:06:04] change. Anything we present in this
[01:06:06] podcast is not intended to be relied
[01:06:08] upon as a forecast research nor as
[01:06:11] investment or tax advice. The
[01:06:13] information and opinions expressed in
[01:06:14] this podcast are not a recommendation,
[01:06:16] offer or solicitation to buy or sell any
[01:06:18] securities and reliance upon them is at
[01:06:20] the sole discretion of the listener.
[01:06:22] Please remember past performance is no
[01:06:24] indication of future results. Thank you
[01:06:26] everyone for taking some time with us
[01:06:28] today and we look forward to coming back
[01:06:30] in the future. Take care.
