---
访谈时间: 2026-07-11
访谈时间说明: "无法从公开信息确认独立访谈录制日期，使用 YouTube 发布时间。"
YouTube发布时间: 2026-07-11
嘉宾名字: "Alvin Roth; Tim Roughgarden; Scott Kominers"
嘉宾公司名称: "Stanford University; a16z crypto; Harvard Business School"
播客名称: "a16z crypto First Principles"
播客url地址: "https://www.youtube.com/watch?v=mtsscntr1Cs"
全文提及的关键名词:
  - "market design"
  - "matching markets"
  - "kidney exchange"
  - "medical residency match"
  - "NYC school admissions"
  - "congestion"
  - "preference signals"
  - "repugnant transactions"
  - "crypto networks"
  - "mechanism design"
字幕来源: "YouTube 公开字幕 json3，automatic_captions/en-orig"
companies:
  - UBER
  - ABNB
industries:
  - 加密
technologies: []
keywords:
  - 就业
tags:
  - UBER
  - ABNB
  - 加密
  - 就业
---

# Why markets fail — and how to fix them (ft. Nobel  economist Alvin Roth)

## Transcript

[00:00] One of the things about market design is
[00:02] you think in advance about what you're
[00:03] going to do.
[00:04] >> A lot of economics asks how does the
[00:06] world work? And market design gives the
[00:08] opportunity to ask how should the world
[00:10] work.
[00:10] >> Many systems from kidney exchange to
[00:13] school choice would fall apart without
[00:15] good market design.
[00:16] >> There's 130,000 people who experience
[00:19] for the first time kidney failure each
[00:21] year, but we only do about under 30,000
[00:24] transplants a year. Most people who need
[00:25] a transplant die without getting one.
[00:27] The challenge is to build systems that
[00:29] produce good outcomes even when
[00:31] participants have competing incentives.
[00:34] A lot of kidney exchanges now are done
[00:36] nonsimultaneously
[00:38] in nondirected donor chains. People who
[00:42] wanted to give a kidney to someone and
[00:43] didn't have anyone particular in mind.
[00:45] And so they allow us to organize a chain
[00:47] that doesn't have to loop back to the
[00:49] beginning. And in that chain, every
[00:51] patient donor pair can get a kidney
[00:53] before they give one.
[01:04] Hi everyone and welcome to First
[01:06] Principles, a series by the team at A16Z
[01:09] Crypto. I'm Tim Ruffgard. I'm the head
[01:11] of research at A6Z Crypto and today
[01:14] we're talking about market design, the
[01:17] careful engineering of efficient
[01:18] marketplaces. Many systems from kidney
[01:21] exchange to school choice would fall
[01:24] apart without good market design. The
[01:26] challenge is to build systems that
[01:28] produce good outcomes even when
[01:30] participants have competing incentives,
[01:33] a problem that's central to markets,
[01:35] including those familiar to us in
[01:37] crypto. Our guest is Dr. Alvin Roth, the
[01:40] Nobel laurate in economics and Stanford
[01:42] professor who is one of the pioneers of
[01:45] market design. And I'm also joined by
[01:47] Scott Commoners, a professor at Harvard
[01:49] Business School and a research partner
[01:51] here at A6Z crypto and as it happens a
[01:54] former student of ALS. Together, we
[01:57] explore how economic theory becomes
[01:59] practical market design. From New York
[02:02] City high school admissions to kidney
[02:04] exchange and how technology changes
[02:07] marketplaces, as well as the idea of
[02:10] repugnant transactions, which is a theme
[02:12] in Al's soontobe published book, Moral
[02:14] Economics. Here's our conversation.
[02:17] So, Scott, we get to interview Al Roth,
[02:20] which is very exciting. I imagine this
[02:22] is sort of particularly meaningful for
[02:24] you given that you know you were a PhD
[02:26] advice advis back in the Harvard days.
[02:28] >> Oh yeah and in fact I mean I I first met
[02:30] him as an undergraduate the summer
[02:32] before I took his market design class
[02:35] you know I was reviewing papers for this
[02:37] uh central blot math. It's one of these
[02:39] you know sort of like largecale math
[02:41] reviewing programs where they're trying
[02:42] to summarize every single math paper
[02:44] ever written. It's an incredible
[02:46] herculean project and I was at the time
[02:48] one of the people who was you know
[02:49] writing summaries for this one of the
[02:50] like thousands and thousands. I was
[02:52] reviewing number theory papers and some
[02:53] of those were like you know sort of very
[02:54] run-of-the-mill. I was getting like the
[02:56] tier one game theory paper sent and I
[02:58] got this article I think it was deferred
[02:59] acceptance algorithms history theory
[03:01] practice and open questions. It was a
[03:03] survey article that had come out earlier
[03:04] that year and was about the use of this
[03:08] thing called the deferred acceptance
[03:09] algorithm which is an algorithm for
[03:11] finding stable matchings. matchings
[03:13] where nobody has any incentive to try
[03:15] and recontract after the fact. And the
[03:17] article took you through this beautiful
[03:19] mathematical theory and then into
[03:21] practice, how this was used in the
[03:23] assignment of doctors to their medical
[03:25] residencies, how it was starting to be
[03:27] used in school choice and it, you know,
[03:29] and and tangentially sort of like how it
[03:31] also related to organ allocation and
[03:33] saving lives through kidney exchange,
[03:34] you know, all this incredible stuff. And
[03:37] I was like, "Oh my god, this is the
[03:38] coolest thing ever. I have to learn more
[03:39] about it." And then I realized that the
[03:42] author taught at Harvard. It was Al
[03:44] Roth. Uh he's at Stanford now, but at
[03:46] the time he was at Harvard. And I had
[03:48] never heard of him. I didn't know
[03:49] anything about this. Um but I checked
[03:52] the courses of instruction and lo and
[03:54] behold, he was teaching a graduate
[03:55] market design seminar that fall. So I
[03:57] walked in and I tell you the the first
[04:00] like 45 minutes of that class, I knew
[04:03] this was what I was going to do. and Al
[04:06] crystallized this set of ideas with like
[04:09] what in retrospect was like the simplest
[04:11] but like to me has always been like the
[04:12] most profound thing I I think I've ever
[04:14] learned about economics which is that
[04:18] economics is a way of thinking about the
[04:21] world right economics is a descriptive
[04:23] science and a toolkit for reasoning
[04:25] about incentives and markets and
[04:27] behavior
[04:29] and market design is a way of thinking
[04:31] about economics like a lot of economics
[04:33] asks how does the world work and market
[04:36] design gives the opportunity to ask how
[04:39] should the world work? What is the the
[04:41] way in which we can use economic theory
[04:44] and analysis to build practical
[04:45] solutions to real world problems? That
[04:48] idea was just so like I was I was primed
[04:51] to hear it and it hit so hard. I was
[04:54] like wow this is what economics can do.
[04:57] And then I was a market designer. I mean
[04:59] even even even that phrase right market
[05:02] design I mean I uh another variant of
[05:04] that is Although has a famous paper
[05:06] called the economist as engineer right
[05:08] and so and really if you look at all of
[05:10] the collaboration between computer
[05:12] scientists and economists now market
[05:14] design I think is sort of in many ways
[05:16] led the way it's really combining
[05:18] >> sort of the practical you know building
[05:21] and problem solving skills that
[05:22] engineers often pride themselves in with
[05:25] the sort of deep insights of incentives
[05:27] that economics gives
[05:29] And even that so that phrase market I
[05:31] mean is even that phrase sort of
[05:32] attributable to to Al Roth.
[05:34] >> Yeah. I mean I think Al has really been
[05:36] heavily involved in essentially like the
[05:38] the the branding and the and the
[05:40] codifying of like what it is to be a
[05:42] market designer and you know the paper
[05:43] you mentioned the economist as engineer.
[05:45] was really like a seminal work and it it
[05:48] took as case studies different instances
[05:51] in which people had used economics in
[05:55] combination with other types of what
[05:56] we'd call like engineering interventions
[05:58] whether you know whether it's specific
[06:00] design features that that make an
[06:03] abstract auction actually work in a
[06:05] specific context or the theory doesn't
[06:08] actually quite tell you you know what's
[06:10] going to happen you know stable matching
[06:12] theory started as a you know Gail and
[06:13] Shappley with this paper on on stable
[06:15] marriages and stable college admissions
[06:17] assignments.
[06:17] >> So when you talked about the deferred
[06:19] acceptance algorithm earlier, is that
[06:20] the same as the Gail Shappley algorithm
[06:21] or
[06:22] >> Yeah, Gail and Shappley introduced this
[06:23] deferred acceptance algorithm which is a
[06:25] way of finding a stable assignment of
[06:26] partners and and they first talk about
[06:28] these are both abstractions. They talk
[06:30] about a marriage market and then a
[06:31] college admissions market. But what you
[06:32] should really be thinking about is you
[06:34] know the matching of doctors to their
[06:36] medical residencies or perhaps you know
[06:38] students to schools. you know, stable
[06:40] matching theory doesn't
[06:43] give a, you know, a way in general to
[06:46] ensure that you can do stable matching
[06:48] when some people enter the market as
[06:50] couples trying to match to the same
[06:51] location. It's an example of what's
[06:53] called matching with complimentarities
[06:55] and it's not guaranteed to work. But as
[06:58] Al showed in work with Elliot Parinson
[07:01] when they redesigned the national
[07:02] resident matching program along with the
[07:04] American medical associations in
[07:06] practice
[07:07] for the context of the medical residency
[07:10] match. It turns out that matching with
[07:12] couples was always possible and they had
[07:14] to like you know design an algorithm.
[07:15] They had to sort of like adapt deferred
[07:17] acceptance which assumes that there are
[07:19] no couples or at least in sort of the
[07:20] native form assumes that there are no
[07:21] couples. um to incorporate couples like
[07:24] how do you change the way the system
[07:27] works in a way that respects the theory
[07:28] and respects the objective of stable
[07:30] matching, right? You still want to have
[07:32] this outcome where no one has any
[07:34] incentive to recontract after the fact.
[07:36] How do you do that in a way that also
[07:39] incorporates this other very important
[07:41] real world component? And that way of
[07:44] thinking about the role of economic
[07:46] theory, you know, sort of Al was really
[07:49] a pioneer in translating and sort of
[07:51] building a toolkit for how to do that
[07:53] then other people built around.
[07:54] >> Amazing. Well, this is you mean just
[07:57] talking about this, you know, from afar
[07:59] is incredibly inspiring. I can't wait to
[08:01] actually talk to the man himself
[08:03] >> and and also I mean he's just it'll be
[08:05] fun.
[08:06] >> Yeah. Yeah. All right, let's do it.
[08:09] Great. So Al, welcome. I thought maybe
[08:11] we could chat about the role of sort of
[08:14] translating theory into practice, right?
[08:16] cuz you know over over your career uh at
[08:19] least my understanding is you know early
[08:21] on it was really more focused on sort of
[08:23] the foundations on getting the um
[08:25] mathematics right u but obviously you
[08:27] know at this stage you're rightfully uh
[08:30] celebrated for your practical market
[08:31] design work and so I just love if you
[08:34] could take take us through a little bit
[08:35] about your evolution from more the
[08:38] primary focus being working on papers to
[08:40] the focus really being on helping real
[08:42] people
[08:43] >> well so the joke about theory and
[08:45] practice is correct its punch line is
[08:47] right right on target. You know, in
[08:50] theory, theory and practice are the
[08:51] same, but in practice they're not. Yeah.
[08:53] And it turns out there are complexities
[08:55] in the world that we that we uh leave
[08:57] out of our simple models, but that are
[08:59] important in the world. So, um so I
[09:02] spent a lot of time studying
[09:04] um the labor market for for doctors. You
[09:08] know, it was an interesting problem for
[09:10] me to study and I I studied it. It had
[09:12] some mathematical background, important
[09:13] mathematical background and it had some
[09:15] complexities and I wrote a paper about
[09:17] it in which sort of the final u line was
[09:21] something like they have a hard problem
[09:24] here and when you're writing a theory
[09:25] paper that's a fine conclusion. You know
[09:27] I showed that couples were were
[09:29] difficult to handle in a in a labor
[09:32] market. You know two career households
[09:33] are tough. And then years later they
[09:36] called me up. my phone rang at the
[09:38] University of Pittsburgh and they said,
[09:39] "Would you uh lead a redesign of of the
[09:42] market?" I still remember that phone
[09:44] call with, you know, a visceral feeling
[09:46] of I was sort of sorry I'd picked up the
[09:48] phone, but I knew why they called me,
[09:50] which is because I'd written a book on
[09:51] matching. But I also knew that the only
[09:53] parts of the book that directly applied
[09:56] to the problem that I was about to take
[09:59] were the counter examples because the
[10:00] book is full of simple theorems. And
[10:03] then you say but of course if they were
[10:04] compliment parodies these theorems you
[10:06] know you couldn't rely on them and
[10:08] indeed you couldn't but the theorems
[10:10] proved to be a surprisingly good guide
[10:12] for what was out there. So that was
[10:13] really the beginning of my career as a
[10:15] practical market designer when I when I
[10:18] agreed that their hard problems would
[10:19] become my problem. You say the theorems
[10:22] were a guide, right? These sort of like
[10:24] these these negative results, these
[10:25] counter examples and and for people in
[10:27] the audience who don't know like you
[10:28] know there's this concept of
[10:30] substitutability versus complimentarity
[10:32] and couples are sort of the the simplest
[10:34] case of complimentarity and it and it
[10:36] turns out that under complimentarity
[10:37] stable matchings often don't exist. And
[10:39] so if you were trying to do a you know
[10:41] centralized matching mechanism with
[10:43] couples hard how do theorems guide us
[10:46] even when they tell us that what you're
[10:49] trying to do can't be done in general.
[10:51] Well so so the the phrase in general is
[10:54] key there because what you said was uh
[10:56] with complimentarities stable matchings
[10:59] often don't exist and and we actually
[11:01] didn't know that and it's actually not
[11:03] true in the application. It's that they
[11:05] can not exist but that happens only
[11:08] seldom. So in my book all the theorems
[11:11] had the grammatical form the following
[11:13] thing always happens. You know stable
[11:16] matchings always exist when you have a
[11:17] simple matching market. Another
[11:19] grammatical form of theorem was some
[11:22] things are impossible. You can never get
[11:24] a stable matching mechanism that always
[11:26] makes it a good idea to state your true
[11:30] preferences. But we didn't have any
[11:32] theorems that said how often those
[11:34] problems are likely to crop up. And it
[11:37] turns out that those in in a market like
[11:39] the market for new American doctors,
[11:42] those problems crop up very seldom. And
[11:45] therefore, we could start by treating
[11:48] the problem as if couples didn't matter
[11:51] too much. And then we could fix the
[11:54] couples because of course the couples
[11:55] matter a lot to the couples. U but but
[11:58] that's sort of what we could do. We
[12:00] could say let's let's ignore them until
[12:02] we see the problem appear and then we'll
[12:04] fix the problem if we can. And so far we
[12:08] always can because it's rare that stable
[12:11] matchings don't exist in a in a market
[12:13] with
[12:15] uh 45,000 applicants and 35,000 jobs and
[12:19] 2,000 couples.
[12:20] >> You know, the the labor market for
[12:22] doctors is an interesting one in that
[12:23] you know the use of stable matching
[12:25] there goes way way way back, right? sort
[12:27] of farther than the start of your
[12:29] career, Al. I mean, even sort of I say
[12:31] this fully knowing that I'm on a call
[12:33] with two people that know literally a
[12:34] hundred times more about matching theory
[12:35] than I do, but my understanding is that
[12:37] that even the algorithm predates the
[12:39] Gail Shappley paper as far as the as far
[12:41] as the implementation. So, since that
[12:43] work, we're seeing these matching
[12:45] techniques used in the field more and
[12:47] more and more and more applications. So,
[12:49] I'm curious about that, how that story
[12:50] went. Was it that once people saw the
[12:53] practical matching work you were doing
[12:56] uh in the doctor labor market then other
[12:58] opportunities arose and then you saw
[13:00] more places where this these ideas could
[13:01] be used or or how did that how did that
[13:03] happen?
[13:04] >> Well, a couple of things happened and
[13:05] one of them was that those ideas were
[13:08] already in use without knowing about
[13:10] Alen Chapley uh in a bunch of medical
[13:14] labor markets and and so fixing it in in
[13:17] the big one just diffused it to the
[13:19] others. And there's a a point that
[13:22] computer scientists will appreciate it,
[13:23] which is that the deferred acceptance
[13:25] algorithm hadn't exactly been
[13:27] rediscovered many times, but mechanisms
[13:30] equivalent to it had. So things that if
[13:32] you put in the same inputs would give
[13:33] you the same outputs as the deferred
[13:35] acceptance algorithm had been
[13:36] discovered. And that was the case with
[13:38] the medical match from the 1950s when in
[13:41] the 1950s they had a simple problem.
[13:43] There weren't any two career households
[13:44] because all American medical graduates
[13:46] in 1950 almost all were men. Uh so they
[13:50] weren't married to other doctors. Uh but
[13:52] by 1970 there were already you know 10%
[13:55] women and today it's a little over 50%.
[13:58] So there are lots of married couples and
[13:59] they they have to look for two jobs not
[14:03] just one. And that's the complimentarity
[14:04] that that Scott is talking about. When
[14:06] you're a couple you care not just about
[14:09] what job you have but what job your
[14:10] spouse got because of the iron law of
[14:13] marriage which is that you can't be
[14:14] happier than your spouse.
[14:16] >> Good good practical advice.
[14:17] >> I remember this iron law. This is, you
[14:19] know, this is this is perhaps one of my
[14:22] most quotable like, you know, Al Roth
[14:24] facts, the uh, you know, the the iron
[14:26] law of marriage matching.
[14:28] >> I want to go back in history one more
[14:30] step because we've talked about the
[14:31] medical match and its fix, but actually
[14:33] like the story of how it came to be is
[14:35] also instructive. Can you tell us just
[14:37] quickly like talk us through what
[14:38] problem it was solving and how it
[14:40] evolved to the form that you were
[14:41] working on?
[14:42] >> So, the medical match was unraveled.
[14:45] Before they had the match, they had had
[14:46] a long period where doctors were getting
[14:48] hired for their first job after
[14:50] graduating from medical school after
[14:52] four years of medical school. They were
[14:54] getting hired in the summer after their
[14:56] second year and that caused lots of
[14:57] problems. That's too early in some
[14:59] sense. There was lots of information
[15:00] missing on both sides and then later
[15:03] they had some some other problems as
[15:05] they tried to fix it. Some problems of
[15:06] exploding offers and congestion. But
[15:08] those problems turn out to be quite
[15:10] common today even in many markets like
[15:13] markets for lawyers like markets in
[15:15] private equity. You guys might know
[15:17] about some of those markets. I don't
[15:19] know how
[15:20] >> certainly on campus the private equity
[15:22] interview dates keep moving earlier and
[15:23] earlier.
[15:24] >> Well and private equity interviews
[15:26] people who have just taken jobs with
[15:28] investment banks for two years later
[15:30] which also you know has conflict of
[15:32] interest problems. So having markets
[15:35] unravel is a tough problem and not all
[15:37] markets can solve it with a clearing
[15:38] house. There are markets like the like
[15:41] the law school markets and the markets
[15:42] for uh appellet court clerks that
[15:45] wrestle with those problems and just
[15:47] suffer from their consequences. Actually
[15:49] I'd love to ask a follow-up on that and
[15:51] I think this may be one of the themes of
[15:53] the conversation. you know, when when
[15:55] our market failure is, you know,
[15:56] amendable to being fixed and and and not
[15:59] would you say there's something
[16:01] fundamental about say the market for
[16:02] lawyers such that, you know, it's just
[16:04] not practical to actually have a
[16:05] clearing house or is it just a
[16:07] coordination problem of having all the
[16:08] relevant parties agree to sort of switch
[16:10] over to a clearing house?
[16:11] >> That's a good question. Market failure
[16:13] means lots of different things to
[16:15] economists. So, I've and I use those
[16:17] terms in my early papers, but but now I
[16:19] like to talk about marketplace failures.
[16:21] You know, I think of marketplaces as
[16:23] small parts of big economic environment,
[16:25] small parts of markets. Uh, so these are
[16:28] marketplace failures. The marketplace is
[16:30] failing to serve the market in an
[16:31] efficient way, things like that. Uh, but
[16:34] one of the problems for lawyers is that
[16:36] they are able to promiscuously make
[16:39] binding verbal contracts. So just by
[16:43] talking to you, I might be entrapped
[16:45] into working for you under some
[16:47] circumstances. For instance, if you're a
[16:49] federal appellet judge and I'm a law
[16:50] student and you say, you know, you'd be
[16:53] a good clerk. I'm going to hire you. And
[16:55] the only grammatically correct answer in
[16:57] that circumstance is yes, sir. Thank
[16:58] you, sir. Uh and and then we're we're
[17:01] done. You know, the the job market is
[17:03] over for me. So, that makes it hard to
[17:06] have a centralized clearing house
[17:07] because you could say that to me before
[17:09] the centralized clearing house, too. I
[17:10] think that's the main problem for for
[17:12] lawyers. And that's a very interesting
[17:13] one because often economists talk about
[17:15] the inefficiencies that result from the
[17:18] inability to make contracts. Right? If
[17:20] we can't make contracts, then I can't
[17:22] send you, you know, 5,000 bushels of
[17:24] wheat with 60 days payable, uh, you
[17:28] know, on delivery. But if we can
[17:29] promiscuously make contracts, then you
[17:31] can hire me before I have a chance to
[17:34] interview at the other places that are
[17:36] interested in hiring me.
[17:38] >> This happens in crypto markets,
[17:39] incidentally, right? You can write smart
[17:41] contracts which are these you know
[17:42] software programs that have immutable
[17:44] function. You can basically write a
[17:45] smart contract to commit to an outcome
[17:46] upfront before you participate in a
[17:49] marketplace and sometimes you know the
[17:51] incentives are such that people would in
[17:52] equilibrium choose to do so even if it
[17:54] means they're giving up rights to things
[17:55] they might later want from the
[17:56] marketplace protocol.
[17:58] >> So Al so moving on to other application
[18:00] domains. I wonder if we could talk about
[18:01] school choice a little bit um and how
[18:03] you got involved there and the work
[18:06] taken to you know convince the relevant
[18:08] decision makers um that your ideas were
[18:11] were worth putting into practice.
[18:12] >> Okay. Uh let me ask do you have by any
[18:14] chance kids in the New York City school
[18:16] system?
[18:17] >> I do. My uh my son is in kindergarten.
[18:19] Yeah. And at the local neighborhood
[18:21] public school.
[18:22] >> Well, in that case maybe let me
[18:23] emphasize that uh you know Parag and
[18:25] Attilla and I didn't design the
[18:27] kindergarten entry process. We just
[18:29] designed a high school entry process.
[18:30] >> I I've made I made a mental note to be
[18:32] in touch in about 8 years. Sounds good.
[18:33] Sounds great. So
[18:34] >> eight years that's precocious, but okay.
[18:36] Uh well that's right. You get at 8th
[18:39] grade you go into nth grade and go
[18:41] through the process uh which has been
[18:43] modified. It was modified under um the
[18:46] predecessor to Adams
[18:47] >> Delasio.
[18:48] >> Yes. So he sort of vandalized the
[18:50] algorithm a little bit. But what
[18:52] happened there is um Mayor Bloomberg
[18:56] when in his first term decided to claw
[18:59] back centralized authority for the
[19:01] school system which had been widely
[19:03] diffused into what was called community
[19:05] control. So there were lots of little
[19:07] school boards that were doing everything
[19:09] for the schools and Bloomberg decided
[19:11] that New York City public schools should
[19:13] do that. You know the department of
[19:14] education. So that was the second time
[19:16] where my phone rang and there was a guy
[19:18] on the other end who said we have this
[19:20] problem. Uh 30,000 of our students have
[19:24] to be administratively assigned. We've
[19:26] tried to go through a choice process
[19:28] have to be administratively assigned to
[19:30] a school that they didn't list any
[19:33] preferences for because we just run out
[19:35] of time to to match them. But he knew
[19:39] about the resonant match and he said
[19:41] this seems to me, you know, he was doing
[19:42] some of the market design there. He
[19:43] said, "This seems to me like like a
[19:45] problem you've already solved. Can you
[19:46] help us?" And at that time, Parag Pak
[19:51] was a graduate student looking for a
[19:52] problem. And he came into my office one
[19:55] day and he said, you know, I went to
[19:56] Tulus and I I, you know, studied a lot
[19:59] of theory and I sort of thought maybe
[20:00] I'd like to get into something more
[20:02] applied. And I I said to him, how about
[20:04] New York City public schools? And, you
[20:07] know, he's run with that. So much of
[20:09] what I tell you about what what's now
[20:11] known about what he and Attilla and I
[20:13] did is known because of his subsequent
[20:15] research. So their problem was they had
[20:18] a a system that worked through the mail,
[20:21] right? And it had some other problems
[20:23] too, but basically the Department of
[20:25] Education sent out a letter to all
[20:28] 90,000 applicants and said, uh, tell us
[20:31] where you'd like to go. And the people
[20:34] applied and they and they listed five
[20:36] schools in order and their
[20:40] their application was xeroxed and sent
[20:42] to the schools they'd listed and that
[20:44] was their application. So that has a lot
[20:46] of problems right there. As a principal,
[20:47] you could see that you're my third
[20:50] choice. And you might decide
[20:52] >> this is in the 2000s, right? Just to be
[20:54] clear, just the timing. This is in the
[20:55] 2000s and they were still using a
[20:57] process like this. Yeah.
[20:58] >> Yes. And that would show you that that
[21:00] you were my third choice. and you might
[21:02] decide, you know, I have a great high
[21:03] school. I'm only going to consider
[21:04] people who list me as their first
[21:05] choice. So, right away, there were
[21:07] reasons to have to strategize and think
[21:10] about what my first choice should be.
[21:13] But also then the high schools made
[21:15] their decisions. They forwarded them to
[21:17] the New York City Department of
[21:18] Education, which sent letters to all the
[21:21] lucky people who had been admitted to at
[21:23] least one high school. And some of those
[21:25] letters said, "You've been admitted to
[21:27] three high schools. Choose the one you
[21:29] want." and they waited for the decisions
[21:31] to come back and then they sent them to
[21:33] the schools and the schools made new
[21:35] admissions offers. They only had time to
[21:37] do that three times. It was August by
[21:39] that time and 30,000 students were still
[21:41] unmatched and they just, you know, if
[21:43] you're 14 years old, you have to go to
[21:45] school of New York. So, they assigned
[21:47] them to the nearest school that had an
[21:49] empty seat. And people were very unhappy
[21:51] with that system for good reasons. It's
[21:53] like chess by mail except it's deferred
[21:55] acceptance by mail with like you know
[21:56] truncation and
[21:58] >> it's deferred acceptance by mail with a
[21:59] very short time clock
[22:01] >> with a very short time list short list
[22:03] time short time
[22:03] >> the games all end before checkmate
[22:07] >> right
[22:08] exactly ch three move chess by mail
[22:11] >> yes so we looked into it we wanted to
[22:14] make sure that we weren't going to be
[22:16] the the economists who drove the last
[22:18] middle class students out of the New
[22:19] York City public school system things
[22:21] like that we we did a lot of talking to
[22:25] educators and but eventually we we built
[22:28] for them a uh deferred acceptance
[22:30] algorithm that met their needs and
[22:32] they've been using it since then. The
[22:34] part that got vandalized by Mayor
[22:36] Delasio was even when you have a
[22:38] deferred acceptance algorithm instead of
[22:40] having 30,000 students who you can't
[22:42] match, you have about 3,000 and they're
[22:44] often students who didn't have good
[22:46] communication with the Department of
[22:47] Education. They may not have uh
[22:49] submitted preference lists. to get down
[22:51] to 3,000. We had maybe 10,000 students
[22:55] who didn't match to one of the places
[22:56] they'd listed and we gave them another
[22:59] opportunity to submit lists. And that
[23:02] part has been truncated and replaced
[23:04] with waiting lists which are not well
[23:06] defined and I believe have their
[23:08] procedures have changed each year.
[23:10] That's part of the story about not being
[23:12] well defined how the waiting lists are
[23:13] run. But the main match there were three
[23:16] parts of the match. one was to the exam
[23:18] schools because there are regulations
[23:20] that make it sensible to do them first.
[23:23] Uh then there was the the main match
[23:26] that most students get matched in. And
[23:27] then there was the the supplementary
[23:30] match in which uh people who didn't get
[23:32] any of their listed applicants got
[23:34] another chance at at schools that were
[23:36] still had at had empty spots. And I
[23:39] believe now only the first two parts are
[23:41] operating. And then there's something
[23:43] happening in that third part to get
[23:45] those students into schools.
[23:47] >> I'm curious, what was the alleged reason
[23:49] for doing away with a supple
[23:50] supplementary match that you mentioned?
[23:52] >> There wasn't a good reason. They never
[23:54] said what they were going to do. I think
[23:55] there was generally some anxiety about
[23:58] about going into the the third match. I
[24:01] mean, for sure going into the third
[24:02] match was bad news. It meant you hadn't
[24:03] matched any place you'd listed. And they
[24:05] decided that since it was bad news, they
[24:07] were going to do away with it. And I
[24:08] believe they hadn't thought about what
[24:09] they were going to do because because
[24:11] they've changed it each year since. You
[24:13] know, one one of the things about market
[24:15] design is you think in advance about
[24:17] what you're going to do.
[24:18] >> I have a quick footnote because you
[24:19] mentioned it a couple of times. The blog
[24:22] you started that when I was taking the
[24:24] market design class in 2009 I or fall
[24:27] 2008 rather and it has continued
[24:30] essentially daily ever since then. First
[24:33] of all, we we should plug it because
[24:34] it's awesome. Like you know if you're
[24:35] not if you're not following
[24:36] marketdesigner.blog blogspot.com. Al
[24:39] won't advertise it, but I'll tell you
[24:40] you should go look at it. But also, can
[24:42] you talk about how it's related, like
[24:44] how it's linked in with your work?
[24:45] >> So, I started it for my class in market
[24:48] design. I wanted people to know that
[24:50] market design problems don't just occur
[24:52] to you when you're reading papers in
[24:54] econometric. They can also occur to you
[24:56] when you're reading the newspaper about
[24:58] markets that are having problems. Also,
[25:00] market design has lots of different uh
[25:04] applications and and you know, markets
[25:06] can have lots of different problems.
[25:08] There are lots of themes. It became a
[25:10] habit and and so now I you know, I just
[25:12] do it. But it's it's a source of ideas
[25:14] and it's a source of memory. It used to
[25:16] be that if I read an interesting New
[25:17] York Times story, I would forward it to
[25:20] you if I thought you would be interested
[25:21] and I'd copy it to myself and I would
[25:23] hope that when I wanted to remember it,
[25:25] I would find it in my emails. And that
[25:26] didn't work. uh but now I can find it in
[25:29] the blog. So I've just written a book I
[25:31] have a book coming out called moral
[25:33] economics. It's about repugnant
[25:35] transactions and you know so
[25:36] controversial markets and a lot of it is
[25:39] I I've been blogging about controversial
[25:41] markets for years and when I think of
[25:44] something I want to write about I look
[25:45] to see whether I've blogged about it and
[25:46] often I have and that reminds me and
[25:48] helps me get going. This is funny. I
[25:51] will say I also use your blog as an
[25:53] index of market design problems and
[25:55] information about them. So I guess it's
[25:58] heartening to learn that you do this as
[25:59] well because I just sort of assumed you
[26:01] had it all in RAM all the time.
[26:02] >> All the time. Absolutely. Remember
[26:04] everything.
[26:05] >> We'll return to Republican markets and
[26:07] in the new book. But let me just let me
[26:09] stay a little bit longer with the school
[26:10] choice application in particular. you
[26:12] know when you speak about the economist
[26:13] as engineer you speak about the
[26:15] importance of spending time in the
[26:16] trenches really studying the specific
[26:18] details of the application and just you
[26:20] know quick personal story I mean I had
[26:22] that very front in my mind actually when
[26:24] I started doing research in the sort of
[26:26] blockchain protocol space it's one of
[26:29] the many benefits I get from my
[26:30] association with A16Z is really seeing
[26:32] what's in the trenches and having that
[26:34] inform my research and and really talks
[26:36] I've seen you give over the past you
[26:37] know 15 years are are in my mind you
[26:40] know when I think about the time that I
[26:41] spend that Okay. So, you know, return
[26:43] returning to school choice. What were
[26:45] the application specific details that
[26:47] were really important there? What made
[26:49] the problem different for example than
[26:51] the work you did matching doctors to
[26:52] hospitals?
[26:53] >> So, some students were getting multiple
[26:55] offers and we wanted to know whether
[26:58] maybe that was important to them and
[27:00] that if we ended up just giving them the
[27:02] best offer that they could have gotten
[27:04] according to their preferences submitted
[27:06] beforehand, whether that would do them
[27:08] harm. So we looked at where they went,
[27:10] the students who got multiple offers,
[27:12] and mostly they went to the place that
[27:14] they had said they like best. And so we
[27:16] decided that we wouldn't harm them by by
[27:18] taking that away from them. And one of
[27:21] the things that speeds up the process,
[27:23] it's not just that it works on a
[27:25] computer, although that is faster than
[27:26] the mail. It's that we ask them for
[27:29] their decision before they begin. That
[27:32] is we ask them to submit preference
[27:33] lists and those those are their
[27:34] decisions. And what was taking time I
[27:37] think in the letters was not the mail
[27:38] but the decisions. So only 17,000
[27:41] students got multiple offers if I
[27:43] remember correctly. But those 17,000
[27:46] what a relief. You know you applied to
[27:47] high schools you got in not just to one
[27:49] but three. The neighbors should know
[27:51] your friends should know. You should
[27:53] talk to everyone about it. You should
[27:54] think what to do even though you'd
[27:55] already had a rank order list. And I
[27:57] think that took takes time. And having
[27:59] that those decisions made first speeds
[28:02] it up. You still need computers. I mean
[28:05] uh there's congestion is a really
[28:07] important part of markets and I've
[28:09] studied markets that tried to do
[28:11] deferred acceptance by telephone and
[28:14] that turns out to be very hard just
[28:15] because of the the way uh rejection
[28:18] chains propagate.
[28:19] >> So actually maybe for the audience could
[28:21] you elaborate a bit on when when you say
[28:22] congestion?
[28:23] >> So congestion has to do with not having
[28:27] enough time to evaluate or transact or
[28:30] do all the things you have to do in the
[28:31] market. So the nice thing about a
[28:34] centralized clearing house like the
[28:35] medical resident match is you make a
[28:37] bunch of decisions up front and then
[28:39] everything happens algorithmically. But
[28:41] if you were trying to do that by
[28:43] telephone, I studied a telephone market
[28:45] for for uh professional psychologists
[28:48] and they tried to implement the deferred
[28:51] acceptance algorithm by telephone. So at
[28:53] 9:00 a.m. on selection day, all the
[28:55] phones are ringing uh as as employers
[28:58] are making offers to applicants. But by
[29:01] 9:30, most of the phones are silent
[29:03] because most of the applicants are have
[29:05] received an offer, but they're waiting
[29:07] to see if they receive a better offer.
[29:09] Now, how do they receive a better offer?
[29:10] Well, somewhere in the country, someone
[29:13] uh gets a better offer, and then he
[29:15] calls back the place that made him the
[29:18] offer he was holding and he says, "I got
[29:20] a better offer. You know, thank you so
[29:21] much. I'm not going to come." And they
[29:23] have to put down the phone and call
[29:25] someone else. And in the market we
[29:27] studied, they were so experienced and
[29:29] fast at that that that exchange took
[29:31] only 6 minutes. About a minute for me to
[29:33] say, "No, thank you. I'm not coming. You
[29:35] know, it was really nice of you to make
[29:36] me an offer." And about 5 minutes for
[29:38] you to call Scott and say, "Scott, we've
[29:40] been thinking about you all morning. Um,
[29:43] you know, we'd like to make you an
[29:44] offer." And he already knows the nature
[29:46] of the offer. You know, all that stuff
[29:47] has been. So, you're just saying to him,
[29:49] >> now we're making an offer. And he says
[29:51] to you, "That's great. You know, you're
[29:52] you're one of my top choices. I'll get
[29:53] back to you later today." you both hang
[29:55] up and now he has to call someone and do
[29:58] another thing that takes 6 minutes. And
[30:00] so you can only do 10 of those an hour.
[30:02] That's the rejection chain that's taking
[30:04] time even though each transaction is
[30:07] very very fast in the world of of labor
[30:10] markets. Uh you can't do a whole
[30:12] country's labor market by phone.
[30:16] >> This one has so many resonances in um
[30:18] different contexts. I mean I at least
[30:20] have have done market design in you know
[30:22] both in cryptoland and outside right
[30:24] like you know with crosscountry vaccine
[30:26] allocation you face versions of this
[30:27] right like you know vaccines expire in
[30:30] crypto often there is literal latency in
[30:33] the system because of the way the
[30:34] computational you know time and and
[30:36] power is rationed by the system you
[30:39] literally can't do more than a certain
[30:40] number of computations per block which
[30:42] then means that you can't do more than a
[30:44] certain number of market operations per
[30:46] unit time right I was a customer in some
[30:48] NFT
[30:49] that had to space out over time because
[30:52] there were so many individual
[30:53] transactions people were doing it was
[30:54] actually like running you know it was
[30:56] causing running out of block space
[30:58] is a way of both undoing congestion and
[31:02] sort of um sorry unnoding I'll say
[31:05] instead of unraveling because unraveling
[31:06] is bad you know unnoding the congest
[31:08] decongesting
[31:10] >> it's like um it's a it's a like you know
[31:12] sinus decongestion good what's the
[31:15] framework for that how do you go about
[31:17] it as you know sort of and And on the
[31:19] theory to practice theme, I know this is
[31:21] one of the places where the theory and
[31:22] the practice sort of sometimes dovetail
[31:23] and sometimes practice requires
[31:25] engineering on top of theory.
[31:27] >> Well, there's lots of ways to to
[31:29] decongest markets because markets that
[31:32] fail to do that don't get very large. Uh
[31:36] so think about Amazon. There was a time
[31:38] when Amazon sold only books and it's
[31:40] conceivable that you could type in an
[31:42] author or browse by topic. I mean like
[31:45] you know maybe the Dewey decimal system.
[31:46] But now Amazon sells everything. If you
[31:48] had to look in alphabetical order at all
[31:51] the things they offered before you could
[31:53] buy something, you wouldn't be able to
[31:54] buy anything. But there's search, right?
[31:57] So that decongests Amazon. You can
[31:59] quickly find what you want to buy among
[32:02] their vast inventory. Think about
[32:05] Airbnb. When Airbnb started, you had to
[32:09] try to reserve a room that other people
[32:11] might also be trying to reserve.
[32:13] Supposing you were trying to reserve a
[32:14] room in my house, you know, our guest
[32:16] room. Supposing we put it on Airbnb. In
[32:19] the old days, you know, I would post it
[32:20] in the morning and then I'd go off to
[32:22] work and then I'd come back from work
[32:23] and look at my my computer, my home
[32:25] computer, and see if anyone had applied
[32:27] to to reserve our room for for tomorrow.
[32:30] And if four people had applied and you
[32:33] weren't the first, I would write you and
[32:34] say, "I'm so sorry. The the room is
[32:35] taken." And so you would have wasted a
[32:38] day and now have to try to get a room
[32:40] again. Well, that was fine when they
[32:42] were competing with other websites like
[32:44] Crash Patter in London, but today they
[32:46] compete with Hilton Hotels. And that
[32:48] isn't the way Hilton Hotels works. When
[32:50] you call up Hilton Hotels, you say, "Can
[32:52] I have a room tomorrow night?" They
[32:53] don't say which room. They can tell you
[32:55] pretty quickly whether they've got a
[32:57] room. And if they said to you which
[32:58] room, you you'd be astonished. You say,
[32:59] "Well, how about room 212?" And they
[33:01] say, "I'm so sorry. You know, that room
[33:03] is taken." They hang up and and then you
[33:05] call back and say, "How about room
[33:06] 2111?" They say, "Oh, yeah, sure." Uh,
[33:09] but that was how Airbnb worked. You
[33:11] know, you didn't get my room, you had to
[33:13] get someone else's room. Well, Airbnb
[33:14] has done a lot of stuff since then.
[33:16] First of all, if you have a high
[33:17] reputation, and if I'm willing to take
[33:19] people with high reputation, then you
[33:20] could just click and not wait for me to
[33:23] uh to confirm your reservation. But even
[33:25] if I want to confirm reservations, once
[33:27] someone is online, they take my listing
[33:30] away from your web page. So, you know,
[33:32] your app, you won't get second in line.
[33:35] You'll only see places that you could
[33:36] get. So, they've gotten rid of a lot of
[33:38] congestion and indeed they compete with
[33:39] hotels now. Uh, but they had to do that
[33:42] in order to compete with hotels because
[33:44] all of a sudden they had a lot of rooms
[33:46] and congestion would take time to be
[33:48] rejected from one room and apply for
[33:50] another. It's interesting that in both
[33:52] this and the school choice context,
[33:54] resolving sequencing issues up front,
[33:57] right? sort of like agreeing on a fixed
[33:58] order given what's available actually
[34:00] was the was the core congestion
[34:02] mitigation which is definitely also of
[34:04] course you know sort of familiar to to
[34:05] our our blockchain listeners.
[34:06] >> We're dealing with a big congestion
[34:08] problem right now in u allocating
[34:11] deceased donor organs to transplant
[34:14] because organs don't last that long
[34:16] after they've been recovered but it
[34:18] takes time for people to decide whether
[34:21] you know you make an offer to a
[34:22] transplant center for a particular
[34:23] patient. There's a big controversy over
[34:25] what are called outofsequence offers,
[34:28] which is when the organ procurement
[34:30] organization starts getting worried that
[34:31] maybe this organ isn't going to find a
[34:33] home while it's still viable because
[34:35] being on ice isn't good for it. Uh they
[34:38] start making offers out of out of
[34:41] sequence. There was some initially
[34:43] agreed on sequence, but they sort of say
[34:45] we better get this organ transplanted
[34:47] quick and they jump ahead to some place
[34:48] that they think will fit. And actually I
[34:50] think that comment is a great excuse to
[34:51] zoom out a bit and talk about kidney
[34:53] exchange because some of our listeners
[34:54] may not even you know be aware that uh a
[34:57] large number of kidney transplants are
[34:58] actually sort of the product of a market
[35:00] which you helped design. So I know
[35:02] you've told the story many times but you
[35:04] know just it still be great to hear the
[35:05] hear the background again. So
[35:07] >> well one part of the background is you
[35:09] can get a kidney transplant from a
[35:12] deceased donor or from a living donor
[35:14] because healthy people have two kidneys
[35:17] and can remain healthy with one. Another
[35:19] part is you can't pay a donor for a
[35:22] kidney. That's or a pregnant transaction
[35:25] that's against the law almost everywhere
[35:26] in the world with the singular exception
[35:29] of the Islamic Republic of Iran where
[35:31] you can pay a donor for a kidney. Uh
[35:34] there are black markets but mostly and
[35:37] certainly in the United States uh
[35:39] kidneys are gifts. Their price is zero
[35:41] and they're very scarce. Therefore uh
[35:44] there are half a million people on
[35:46] dialysis in the US. There's 130,000
[35:49] people who experience for the first time
[35:51] kidney failure each year, but we only do
[35:53] about under 30,000 transplants a year.
[35:56] So we have 130,000 new cases. We do
[35:58] 30,000 transplants. Most people who need
[36:01] a transplant die without getting one.
[36:04] One of the ways you can get a transplant
[36:05] is someone healthy enough to give a
[36:07] kidney loves you enough to give you a
[36:09] kidney. And there's lots of living donor
[36:12] transplants, but often you can't give a
[36:14] kidney to the person you love, even if
[36:16] you're healthy enough to give someone a
[36:17] kidney because kidneys have to be well
[36:19] matched to the patient. So, you could be
[36:22] in the situation where you want to give
[36:24] a kidney to one of your kids, but you
[36:26] can't. And I want to give a kidney to
[36:28] one of my kids, but I can't. Uh, but
[36:31] maybe I could give a kidney to your kid,
[36:32] and you could give a kidney to my kid.
[36:33] That's a kidney exchange. And that
[36:35] increases the availability of living
[36:37] donor transplants. And now we do about a
[36:41] third of the living donor transplants
[36:43] through exchange often more complicated
[36:46] exchanges than than just between two
[36:47] pairs. So that's a matching problem. It
[36:50] doesn't use deferred acceptance
[36:51] algorithm for you know for you matching
[36:53] guys out there. It it doesn't use top
[36:55] trading cycles either although that was
[36:57] what we originally proposed. It uses uh
[36:59] integer programming to find cycles and
[37:02] chains that that do the job. Those are
[37:06] computationally hard problems and and
[37:08] some of the instances are
[37:09] computationally demanding. They can run
[37:11] a long time. It's not that the worst
[37:12] case is computationally hard, but but
[37:14] you never meet a hard problem, but we've
[37:16] never met one that we couldn't solve.
[37:18] So, you computer scientists can help us
[37:20] out by enlarging the the complexity
[37:23] literature to not just deal with worst
[37:25] cases.
[37:26] >> I mean, Tim Tim has done a lot of that
[37:29] actually.
[37:30] >> Yeah. Looking at you, Tim.
[37:32] Well, you know, the good news is is area
[37:34] I like to call beyond worst case
[37:35] analysis has been a really very major
[37:37] theme in in computer science algorithms
[37:39] research over the past decade or so. Um,
[37:42] and you know, in addition to more quote
[37:44] unquote traditional applications, you
[37:46] know, like integer programming, like you
[37:47] say, Al, I mean, if you can imagine
[37:48] like, you know, the the rise of uh
[37:51] success in machine learning first with
[37:52] the deep learning wave last decade, but
[37:54] then of course also with the genai this
[37:56] decade. I mean that in some sense throws
[37:58] the gauntlet to computer science
[38:00] analysts more than ever to explain how
[38:02] we're sort of solving problems that the
[38:04] traditional theory says uh should be
[38:06] unsolvable. So lots of very smart people
[38:08] uh working hard on these kinds of
[38:09] questions. I'm happy happy to report you
[38:12] know I'd love to linger on King Exchange
[38:13] a little bit longer because I I you know
[38:14] I know you have a a deep book of amazing
[38:18] war stories from um you know this work.
[38:22] So, one idea would just be some of the
[38:25] challenges that came up in getting your
[38:27] ideas accepted, right? I mean, even the
[38:29] idea that you would have a quote unquote
[38:30] market for kidneys, right? I mean, that
[38:32] has to take a lot of socialization to
[38:34] get people people even comfortable with
[38:35] that idea in the first place.
[38:36] >> Literally required legislation, right?
[38:38] >> Well, we we went ahead without the
[38:40] legislation, but then we got
[38:42] legislation. The American law that says
[38:45] you can't pay for a kidney is a little
[38:47] obscure. It says you can't give valuable
[38:50] consideration to a donor of an organ for
[38:53] transplant. So the question is what's
[38:55] valuable consideration? When I just told
[38:57] you about kidney exchange, something
[38:59] valuable is being exchanged where we're
[39:01] where, you know, I'm giving a kidney to
[39:02] your patient, you're giving a kidney to
[39:04] my patient. That's that's very valuable.
[39:06] But the Department of Justice wouldn't
[39:08] write us a memo saying that that wasn't
[39:10] what they meant by that legislation,
[39:11] which is called the National Organ
[39:13] Transplant Act of 1984. So, there was a
[39:16] southern congressman named Charlie
[39:18] Norwood who proposed an amendment to the
[39:21] National Organ Transplant Act that said,
[39:24] uh, those words, valuable consideration,
[39:26] don't apply to kidney exchange. And we
[39:29] were already doing kidney exchange at
[39:31] that point, but we're doing it without,
[39:34] you know, clear legal guidance. And one
[39:37] of the heroes of kidney exchanges, my
[39:39] colleague Mike Reese, who's done a lot
[39:40] of innovation in kidney exchange. And he
[39:42] said something like, you know, one of my
[39:44] patients was a US attorney uh for the
[39:47] Southern District of Ohio, you know,
[39:48] something like that. I could have him
[39:49] sue me and then we'd establish in court
[39:51] that this is legal, you know, and
[39:53] everyone who loves Mike said, "Don't do
[39:54] that. Don't do that. I can never tell
[39:56] what would happen." It
[39:57] >> doesn't seem like that. But the
[40:00] amendment failed to pass in the first
[40:03] Congress. It was introduced and it
[40:05] failed to pass in the second Congress.
[40:07] And in the third Congress, Charlie
[40:08] Norwood who had had a transplant, he
[40:10] died of a amunosuppressive related
[40:12] disease and his colleagues named the act
[40:15] after him and passed it unanimously. So
[40:18] kidney exchange, which doesn't involve
[40:20] any payments between patients and
[40:22] donors, uh is is legal in the United
[40:25] States. But just to be sure in the
[40:28] legislation it's not called kidney
[40:29] exchange it's called kidney paired
[40:31] donation which is a term of art that
[40:33] keeps the word exchange out of the
[40:35] description and what made it take off
[40:38] was non-simultaneous chains right so the
[40:42] exchange I described to you between two
[40:44] pairs we always do those simultaneously
[40:46] because one thing that
[40:48] not being allowed to give valuable
[40:50] consideration means consideration is a
[40:52] contract term means you can't write a
[40:54] contract a legally enforceable contract
[40:56] that says you guys give us a kidney on
[40:58] Monday and we promise to give you a
[40:59] kidney on Tuesday. So when we do
[41:02] pairwise exchange we do all four
[41:04] operations two nefrectomies and two
[41:06] transplants simultaneously and that
[41:09] requires four operating rooms and four
[41:12] surgical teams. So it's so there's
[41:13] congestion in the market that is it
[41:15] takes resources. It's hard to to do
[41:18] these. So a lot of kidney exchanges now
[41:20] are done nonsimultaneously
[41:23] in nondirected donor chains. So last
[41:26] year we had 500 some odd nondirected
[41:30] kidney donors in the United States.
[41:32] People who wanted to give a kidney to
[41:34] someone and didn't have anyone
[41:35] particular in mind. And so they allow us
[41:38] to organize a chain that doesn't have to
[41:40] loop back to the beginning. And in that
[41:42] chain every patient donor pair can get a
[41:45] kidney before they give one. And so if
[41:48] the chain breaks, it's not a tragedy
[41:50] where some pair has lost a kidney but
[41:53] not gotten one and no longer has one to
[41:55] participate in exchange with. So it
[41:58] turns out you can make economic models
[42:01] in which that doesn't work at all
[42:03] because people people reneg on their
[42:07] agreement. But this is one of those
[42:09] behavioral things. It turns out we human
[42:12] beings are a lot nicer than economists
[42:14] often give us credit for. And so that
[42:16] turns out to be a rare problem. And
[42:18] consequently, non-directed donor chains
[42:21] are a very productive way to get bunches
[42:24] of kidney transplants, including
[42:26] transplants for the hardest to match
[42:27] patients for graph theoretical reasons
[42:30] that you guys will understand if if
[42:33] we're hard to match. And I don't know
[42:34] who listens to your bot, but think of
[42:36] sort of Erdogeni kind of graphs going to
[42:38] infinity. Uh if
[42:39] >> they'll that that'll that's on topic.
[42:41] >> Yeah, that's that's what I thought. I
[42:43] mean, almost all of your your listeners
[42:45] will will now know what I want to say.
[42:47] There's uh a way of of looking at graphs
[42:51] that says if graphs are closely
[42:53] connected, if if there are lots of
[42:56] possible transplants for every pair,
[42:59] then it'll be easy to take care of
[43:00] everyone. But if some people remain in
[43:03] sparse parts of the graph, that is it's
[43:05] really hard for them to find a kidney,
[43:06] then it's especially hard for them to
[43:08] find a two-way exchange because the it
[43:11] it's only a rare pair that can give them
[43:13] a kidney and it's only rare that they
[43:16] can give one back. So uh but if you have
[43:19] chains so suppose we're all hard to
[43:21] match pairs then the chance that we can
[43:23] do exchanges with each other is hard is
[43:24] very small because the chance that I can
[43:27] take a kidney from you is very small cuz
[43:29] my pair is hard to match and the chance
[43:30] that you can take a kidney from us is
[43:32] very small cuz your pair is hard to
[43:33] match. But if we have a big data set if
[43:35] we have a thick market then the chance
[43:37] we can give someone a kidney is not so
[43:39] small. Chance that they can give it back
[43:41] to us is very small but the chance that
[43:42] they can give it to someone else isn't
[43:44] so small. And so we can construct a
[43:47] chain that includes very hard to match
[43:49] pairs. So that's been a big development.
[43:51] I just came back from a conference in
[43:53] Egypt in which it turns out there's a
[43:56] long-standing dogma of the World Health
[43:58] Organization that says countries should
[44:00] be self-sufficient in transplantation.
[44:03] And that essentially prevents small
[44:05] countries from having kidney exchange
[44:07] and
[44:07] >> from having transplants, right?
[44:08] >> Right. From having transplants. It
[44:10] protects them from certain kinds of
[44:11] medical care because they're worried
[44:13] about black markets. But I co-chared a
[44:15] consensus working group that got a a
[44:18] consensus statement. The conference
[44:20] voted on it uh that said that countries
[44:22] should be able to cross borders in in
[44:24] kidney exchange and you know in
[44:27] particular small countries working with
[44:28] large countries has some advantages for
[44:30] everybody concerned. We'll see if that
[44:33] happens. We have to write a paper. We
[44:34] have to this is part of market design on
[44:36] a on a sort of diplomatic scale.
[44:39] >> Well, that sounds like very important
[44:40] work. Uh, and just, yeah, it goes to
[44:42] show there's the theory and then there's
[44:43] the 100 steps involving humans after
[44:46] that of actually um, you know, getting
[44:48] people com comfortable with it and
[44:49] getting it done. I'd love to circle
[44:51] back. So, you know, you you brought up
[44:52] Amazon, you brought up congestion uh,
[44:56] and how technology can increase or
[44:59] decrease congestion. So, maybe I'd love
[45:01] to just get your thoughts um, on how
[45:04] technology has changed, you know, both
[45:06] the the theory and practice of market
[45:08] design, right? you you got to witness,
[45:10] you know, the rise of the internet in
[45:12] the late '9s and then the 2000s. Um, you
[45:15] know, I know you've um, you know, I
[45:17] think have done some work with eBay at
[45:19] that time. So, yeah, just a little bit
[45:21] about the internet, the web technology,
[45:23] market design. What role has it played?
[45:26] >> You know, computationally assisted
[45:27] markets are sort of something new. Uh,
[45:31] and and we've seen a little bit of that.
[45:32] You know, when I was young, uh, a cash
[45:35] register was a a mechanical machine. you
[45:38] know, you you typed dollars and cents on
[45:40] it and a a cash drawer opened up and you
[45:42] made change. But now, uh, long before
[45:45] the internet, uh, cash register was a
[45:48] laptop that had, you know, cash register
[45:50] inputs and it also kept track of your
[45:52] inventory. It remembered what you just
[45:54] sold so you could figure out that you
[45:56] didn't you needed to reorder it, things
[45:57] like that. So, that was already adding
[46:00] some computation to markets and
[46:02] marketplaces at the local level. And
[46:04] then the internet came along and all of
[46:06] a sudden markets became global. You
[46:09] know, eBay, you could sell stuff on eBay
[46:11] to people far across the world. One of
[46:15] Scott's colleagues once sold his
[46:17] collection of Pokemon cards to a dealer
[46:20] in Finland that way uh when he was uh
[46:23] quite a bit younger than he was.
[46:24] >> Wait, I'm not totally sure I know which
[46:25] colleague this is, and I want to know
[46:26] why he didn't sell me the Pokemon cards.
[46:29] >> You were also a child at that time.
[46:31] >> I see.
[46:34] Fair enough.
[46:35] >> So, you know, all of a sudden a kid
[46:37] could sell his collection of cards to a
[46:39] to a store in Finland. You know, that's
[46:42] pretty remarkable. So, that's also
[46:44] computationally aided markets, right? I
[46:46] mean, the internet allowed him to do
[46:47] that. And of course, computationally
[46:50] aided markets can do all sorts of
[46:52] computations, including
[46:54] computationally difficult computations.
[46:56] But but the resident match I mean when
[46:58] it it actually began you know as as you
[47:01] said at the beginning long before my
[47:02] involvement began in the early 1950s and
[47:05] it worked on card sorting machines. So
[47:07] it was doing something that could be
[47:09] done with card sorting physical card
[47:11] sorting and I guess it's still doing
[47:14] something that could be done with
[47:15] physical card sorting but that wouldn't
[47:16] be the way to do it because now there
[47:17] are 45,000 applicants and you know
[47:20] thousands of jobs. So doing it digitally
[47:23] happens very fast you know. So medical
[47:25] students have to wait. they they submit
[47:26] their preferences, the the hospitals
[47:28] submit their preferences, and then
[47:29] there's a waiting time. A lot of that
[47:31] waiting time is checking, you know,
[47:32] making sure you're now a medical
[47:34] student. If you have a funny uh
[47:37] preference list, funny in the sense that
[47:39] you seem to have applied to places that
[47:40] didn't interview you, didn't list you,
[47:43] they'll call you up and they'll say, you
[47:44] know, you sure you haven't clicked on
[47:46] the wrong things? You know, we want to
[47:47] make sure that when we run the match,
[47:49] we're running them on your actual
[47:50] preferences. So they do a lot of
[47:52] checking of that sort to make sure that
[47:53] the inputs are correct which takes time
[47:56] but but once they are uh you know the
[47:59] algorithm itself runs very fast. Now you
[48:02] know those are smart markets they do
[48:03] computations and we're going to see even
[48:05] smarter markets. That's what we're
[48:06] seeing with AI, right? I mean uh
[48:09] possibly some of the checking can be
[48:10] done automatically including
[48:12] communicating with with people. You know
[48:14] we notice something funny about your
[48:15] preferences. Would you confirm that that
[48:17] you've submitted the correct preference
[48:18] list? you know, we're going to see more
[48:20] smart markets. People are going to
[48:22] depend on them for matches with more or
[48:26] less understanding of what's going on
[48:28] and with the market eliciting more or
[48:30] less information. So, just as example,
[48:32] we already talked about Airbnb. Let's
[48:34] talk about Uber for a minute. First,
[48:37] those come at very different
[48:38] technological stages, right? Airbnb
[48:40] could come when the internet was
[48:41] invented. Airbnb became possible, but
[48:44] you couldn't run Uber on the internet,
[48:46] you know, on your desktop computer. Uber
[48:48] needs a smartphone. It needs to know
[48:50] where you are and you have to be able to
[48:52] communicate with it wherever you are.
[48:54] You're typically not at your desk when
[48:55] you want an Uber.
[48:57] >> Uh but their matching algorithm, your
[48:59] desires are pretty simple. Once they
[49:01] know your location and maybe where
[49:03] you're going, they can pretty much guess
[49:06] what you want. You want is a car that
[49:07] will come quickly to where you are now
[49:09] and will take you to where you're going.
[49:11] That's a much simpler problem than
[49:13] Airbnb has. They they can't just ask
[49:15] what city you're going to, what where's
[49:16] your convention. They have to show you
[49:18] pictures because you might like the the
[49:21] house that has a view of the bay or you
[49:23] might like an ocean view. So Uber knows
[49:26] to a good approximation what you want.
[49:28] You want somebody to play fast. And the
[49:30] drivers, we we can think about their
[49:32] preferences. So Uber just doesn't ask
[49:35] you any questions except, you know, do
[49:37] you want it more expensive or less
[49:38] expensive? Do you want it quicker or
[49:40] slower? I mean, they they have a couple
[49:41] of questions, but but they they really
[49:42] know what you want. They know the shape
[49:43] of your preferences
[49:44] >> and and quasi conversely the Uber
[49:46] competitor that did ask you a lot of
[49:48] details right that actually had you try
[49:49] and choose between different drivers
[49:51] this was sidecar like you know it went
[49:52] out of business
[49:53] >> there you go that's congestion for you
[49:56] now Uber suffers from congestion too
[49:58] that that is if you go to San Francisco
[49:59] airport there's a bunch of Ubers waiting
[50:01] for the next call and like
[50:06] potential transplant recipients who have
[50:08] waited long enough to be high priority
[50:10] they're going to get many offers. So if
[50:12] you don't want to go to San Francisco,
[50:13] if you for some obscure reason want to
[50:15] go to Palo Alto from San Francisco
[50:17] airport, the first Uber driver online
[50:20] might not want to take you there. He
[50:21] might want to go back to San Francisco.
[50:22] That's where he gets most of his
[50:24] business. So you might have to wait a
[50:26] little bit during which time you might
[50:27] look at Lyft and take a lift. So So one
[50:31] of the problems Uber has is a little bit
[50:33] like the problem of deceased donor
[50:36] transplants is the the patients don't
[50:39] wait around. you know the the the rides
[50:41] the organs don't wait around they get
[50:42] cold and and become unviable. So the
[50:45] problem that Uber has of congestion it
[50:47] takes time for for the match to be made
[50:51] uh is also very similar mathematically
[50:53] to the problem we have in in deceased
[50:56] organ allocation. Um but Airbnb has a
[50:58] very different problem. They they have
[51:00] to show you pictures. They have to sort
[51:02] of tell you a story. you know, this is
[51:03] where you'd be. And they don't like to
[51:05] tell you exactly where you'd be because
[51:06] they don't want to be uh worked around,
[51:09] >> disintermediated. Yeah,
[51:10] >> disintermediated. Thank you. But they
[51:12] have to tell you quite a bit. Otherwise,
[51:13] you can't form an opinion about whether
[51:16] which which apartment you want. So,
[51:18] those are two markets that will evolve
[51:20] differently as markets get smarter. Uh
[51:23] you know, maybe your AI agent will know
[51:25] what apartment you like eventually, but
[51:27] somebody has to know what apartment you
[51:28] like. Whereas for Uber, we we sort of
[51:30] know what you like. So earlier this idea
[51:33] of um repugnant markets came up, right?
[51:36] So I guess the question here would be is
[51:38] it ever inappropriate to solve a problem
[51:41] with the market.
[51:42] >> Well, people people think it is some
[51:44] some people think some problems are
[51:46] inappropriate to solve with market. I
[51:48] already indicated that it's against the
[51:50] law in the United States to pay someone
[51:52] to give you a kidney. So it doesn't
[51:54] surprise economists that kidneys are in
[51:55] short supply. You know, you can't use
[51:57] prices to increase supply. Kidneys have
[51:59] to be a gift. the price has to be zero.
[52:01] You mentioned Iran earlier as the as the
[52:03] one place where there is a market and I
[52:05] assume the weight times there are not so
[52:07] high or lower than in
[52:08] >> so I think that's right but it's very
[52:10] hard to tell because I know much less
[52:12] about and there's much less data about
[52:14] what's the incidence of diabetes and of
[52:16] kidney failure and things like that so I
[52:18] don't have all the comparative stuff uh
[52:20] it's controversial in Iran too before co
[52:22] I once gave a talk in Berlin about
[52:24] controversial markets and I talked about
[52:28] kidney exchange and surrogacy
[52:30] and prostitution. And the reason those
[52:33] were three good markets for me to talk
[52:35] about in Germany, three controversial
[52:38] markets, is that the German laws are
[52:40] exactly the opposite of the American
[52:42] laws. In Germany, the only one of those
[52:44] three that's legal is prostitution. And
[52:47] surrogacy and kidney exchange are not
[52:50] legal. Although kidney exchange, there's
[52:52] legislation moving forward. Uh, so there
[52:55] isn't kidney exchange in Germany and
[52:56] there's not surrogacy in Germany, but of
[52:58] course surrogacy is legal in California
[53:01] and in New York and in Massachusetts. So
[53:04] German couples that need a surrogate can
[53:06] come to the United States. And then the
[53:08] German courts have to figure out how to
[53:11] repatriate the baby who is not legally
[53:14] recognized as belonging to this couple.
[53:17] But what the courts have had to do is
[53:19] figure out how to let the German couple
[53:22] adopt their own baby which you know
[53:24] constitutional courts think of high
[53:26] level things you know is this something
[53:28] we want to support as a society but
[53:30] family courts have to think about who
[53:32] takes home the baby and one good answer
[53:36] is how about the baby's parents. So uh
[53:39] so it turns out just like markets need
[53:42] social support, bans on markets need
[53:44] social support otherwise they'll be
[53:47] subverted by people who need surrogate
[53:49] help to start their family for instance.
[53:51] And and you know remember we're all
[53:53] descended from long lines of people who
[53:56] never in any generation forgot to have
[53:59] children.
[54:00] So the urge can be very strong. Right?
[54:05] making it against the law to have
[54:06] children the only way you might be able
[54:08] to doesn't always stop people from
[54:10] having children that way. So what what
[54:12] my new book is about is about
[54:14] controversial markets and and morally
[54:16] contested transactions. You know what
[54:18] happens when you when you start to try
[54:20] to design these markets and sometimes
[54:23] inadvertently design the black market
[54:25] that that replaces them.
[54:27] >> So So let's let's talk about uh moral
[54:29] economics a little bit. What would you
[54:30] say are some of the key themes or a
[54:33] favorite story from it that you think
[54:34] would resonate with the audience?
[54:36] >> Most of the legislators legislatures in
[54:39] Western Europe uh where Sargacy is
[54:42] widely illegal that is they don't
[54:44] recognize parentage through surrogacy.
[54:46] They worry that it exploits women and
[54:48] they want to prevent exploitation. They
[54:50] want to protect vulnerable people. On
[54:53] the other hand, when bans on surrogacy
[54:56] are permeable, as they are, because you
[54:58] can come to the US, you used to be able
[55:00] to go to Ukraine. That was a big market
[55:01] for surrogates. When they're permeable,
[55:03] it means there are going to be babies
[55:06] and there's no one more vulnerable than
[55:08] a baby. So,
[55:10] Italy is trying to criminalize
[55:14] coming to the United States to have a
[55:16] surrogate. But these other places that
[55:19] where surrogacy isn't legal, they're
[55:20] trying to figure out ways to get the
[55:22] babies home. And in places like Britain
[55:24] and Canada, surrogacy is legal in the
[55:27] sense that they acknowledge parenthood,
[55:29] but you can't pay the surrogate. In
[55:30] Britain and Canada, having a surrogate
[55:33] is like having a kidney donor. You you
[55:35] can't pay for it. So So there are
[55:37] surrogates in Britain and Canada, but
[55:38] not nearly as many as as you would
[55:40] think, given Well, maybe just as many as
[55:42] you would think. I mean, not as many as
[55:44] many as you think given the price is
[55:45] fixed at zero.
[55:45] >> Yes. Yes. So they come to the US and and
[55:48] the British law is it's legal to come to
[55:49] the US. It's legal in the US. You can
[55:51] come home with your with your British
[55:53] baby, you know. So that's the kind of
[55:55] thing that that I think about, you know,
[55:56] what can you accomplish? What can you
[55:59] not accomplish by regulation? I also
[56:01] think a little bit about maybe what we
[56:03] should want, you know, should we be
[56:04] trying to prevent surrogacy? Now,
[56:06] American surrogates, you know,
[56:09] >> might feel differently.
[56:10] >> Yeah. They they get paid around $50,000
[56:12] for a surrogate birth. They're all
[56:15] already mothers, so they know what
[56:16] they're getting into. Uh it turns out
[56:18] not to be a terrible job for a woman
[56:20] with small children in the house, uh
[56:23] being pregnant. So, you know, we think
[56:25] it's okay. There there are other markets
[56:27] like that, like the market for blood
[56:29] plasma, right? Plasma is an essential
[56:33] source of pharmaceuticals, particularly
[56:35] having to do with with immunology,
[56:37] antibodies, things like that, but also
[56:39] clotting factor for people who don't
[56:41] have it, who are hemophiliac, uh, and
[56:43] and a bunch of things. And it's on the
[56:45] World Health Organization's list of
[56:47] essential medicines. If you want to
[56:50] provision a hospital anywhere in the
[56:52] world, your pharmacopia has to have
[56:55] plasma products because you can't run a
[56:57] a modern hospital without them. But the
[57:00] World Health Organization and the
[57:02] European Union believe that you have to
[57:05] be self-sufficient in plasma from unpaid
[57:08] donors. And it turns out no one has been
[57:10] able to do that. And so fortunately, you
[57:13] don't have to do it. You you can believe
[57:15] it's immoral to pay donors in your
[57:17] country and you don't have to because
[57:18] you can buy all you need from the United
[57:20] States because we are the Saudi Arabia
[57:23] blood plasma. We pay plasma donors and
[57:26] we export 70% of the world's plasma. Uh
[57:29] and that's why there are
[57:31] millions of deaths in Europe due to
[57:34] shortage of plasma products.
[57:35] >> And it's interesting that these
[57:36] different rules regimes can coexist at
[57:39] the same time in different locations.
[57:41] >> Right? So think about marijuana in
[57:43] American states, right? Marijuana was
[57:45] once widely illegal, but I'm guessing
[57:48] that when it was illegal everywhere,
[57:50] there's some chance that you guys knew
[57:52] someone who would know where you could
[57:54] get some. That is, there was a a a
[57:57] pretty big black market in marijuana
[57:59] among people of certain age and
[58:01] socioeconomic status and education. Uh
[58:04] but now, if you're in the state of
[58:07] Idaho, where it's still completely
[58:09] illegal, you're surrounded by states
[58:11] where it's legal. So, I'm predicting
[58:13] that eventually it's going to be legal
[58:15] everywhere in the US, even though it's
[58:16] still a federal schedule one drug. It's
[58:19] treated like heroin as a, you know, a
[58:21] very dangerous substance with no medical
[58:23] uses. Of course, it starts to have
[58:25] medical uses. Uh, but there's also, you
[58:28] know, becoming widely available legally
[58:30] for recreational purposes. So, if you
[58:33] were a state of Idaho highway patrolman,
[58:38] there was a time where you could have
[58:39] stopped a car on the highway and made an
[58:41] arrest for somebody who had marijuana in
[58:43] their car. And when you got back to the
[58:45] police barracks, the state police
[58:46] barracks, they they'd clap you on the
[58:47] back and say, you know, good arrest. You
[58:50] know, you you stopped someone bringing
[58:53] drugs into Idaho. But now they're going
[58:55] to say to you, someone didn't finish
[58:57] their magic brownies that they bought
[58:59] legally in Washington and you know
[59:01] they're on their way east where they're
[59:02] going to eat them at dinner after dinner
[59:06] and you arrested them. You know, why
[59:07] can't you be chasing bank robbers and
[59:09] murderers? You know, the we have real
[59:11] problems in Idaho. Uh so I think that
[59:13] it's going to get harder and harder for
[59:16] Idaho juries to be presented with cases
[59:18] they want to convict when when marijuana
[59:21] purchases are legal. There's also the
[59:23] problem of crime. You don't want your
[59:25] market to be just run by criminals. Uh
[59:27] and of course in the United States, we
[59:28] had an experience like that in the 1920s
[59:31] and early 30s with prohibition of
[59:33] alcohol. And we prohibited alcohol. It
[59:36] didn't reduce alcohol consumption to
[59:39] zero by it. It was far from that. It
[59:41] created a lot of organized crime. We we
[59:44] created the prohibition with a
[59:45] constitutional amendment and we ended it
[59:47] with another constitutional amendment.
[59:49] So there are now legal markets for
[59:51] alcohol. We haven't solved the problem
[59:53] of alcoholism. It's not that alcohol is
[59:55] unproatic,
[59:57] but you can't buy moonshine whiskey from
[01:00:00] gangsters anymore. They're outco
[01:00:02] competed by the the fancy wine and
[01:00:05] liquor stores. It's not that wanting to
[01:00:07] ban alcohol was a crazy thing, right?
[01:00:09] And and we we still deal with those
[01:00:11] problems. You know, Alcoholics Anonymous
[01:00:13] was founded around the time that
[01:00:14] Prohibition ended. Uh now we have, you
[01:00:17] know, Sports Gambling and Gamblers
[01:00:18] Anonymous. marijuana is going to be
[01:00:20] problematic and it always was. But we
[01:00:22] didn't succeed in in preventing
[01:00:24] marijuana and we we created criminal
[01:00:27] organizations that sometimes
[01:00:30] also deal in other drugs. You know, I
[01:00:32] think it's going to go the way of
[01:00:32] prohibition once once it's fully
[01:00:36] digested how we're how we're dealing
[01:00:37] with it in the United States. So,
[01:00:39] repugnant transactions are important.
[01:00:41] Let let me sort of add with a note that
[01:00:44] we're not out of the woods for
[01:00:45] artificial intelligence. Right. Right.
[01:00:47] At at Stanford, we are not allowed to
[01:00:50] use artificial intelligence to vet
[01:00:54] admissions. I don't know about I mean,
[01:00:55] I'm sure it's true for undergraduate
[01:00:56] admissions, but for for PhD admissions,
[01:00:59] we're not allowed to upload all the
[01:01:01] dossas we get for students into into a
[01:01:04] large language model and ask it
[01:01:06] questions. Okay. So Stanford is somewhat
[01:01:08] concerned that maybe we'd be uploading
[01:01:11] something with implicit biases that we
[01:01:12] didn't know about or maybe they're
[01:01:14] concerned about what the newspapers
[01:01:15] would say if they heard that that's what
[01:01:16] we were doing. But you can imagine that
[01:01:18] that we're not too many
[01:01:21] terrible incidents away from having
[01:01:23] regulations that will that will say a
[01:01:25] lot of the things that you think are
[01:01:26] going to be good about AI shouldn't be
[01:01:28] allowed to happen. So we're not out of
[01:01:30] the woods. You know, markets need social
[01:01:32] support. That's something that
[01:01:33] economists haven't studied enough. I
[01:01:36] wish I understood it better than I do.
[01:01:38] And one reason I'm writing a book about
[01:01:39] this is to to say this is something to
[01:01:42] study. This is part of market design.
[01:01:43] It's just like you can't expect the
[01:01:46] world to read econometrica and and
[01:01:48] figure out how to implement the papers
[01:01:49] in it. Neither can you expect everyone
[01:01:51] to say, "Oh, well, if an economist
[01:01:53] thinks this is a good idea, it must be a
[01:01:54] good idea. Let's let's do it."
[01:01:56] >> Or or to know to switch to an
[01:01:57] infrastructure layer like, you know,
[01:01:59] sort of think again cryptoland, right?
[01:02:00] We have all of these infrastructure
[01:02:02] tools. We actually need to solve a
[01:02:03] coordination problem to get people to
[01:02:04] use them. It's another version of that,
[01:02:06] right? But so with your examples of, you
[01:02:08] know, kidney markets on one side and
[01:02:10] then contexts like marijuana on another
[01:02:13] and then maybe surrogacy somewhere in
[01:02:14] the middle, do you have a sense of when
[01:02:17] markets are ready to move into design
[01:02:20] space versus when they're sort of just
[01:02:22] impenetrable, like you know, you're
[01:02:24] going to be banging your head against a,
[01:02:25] you know, a marketplace wall. I should
[01:02:27] be careful what I say here, but I but
[01:02:28] but I think there has to be widespread
[01:02:31] dysfunction that affects lots of people
[01:02:33] so that there's at least the hope of
[01:02:36] making a paro improvement. You know,
[01:02:37] when markets are really working badly,
[01:02:39] there's some chance that a better design
[01:02:41] will make everyone or almost everyone
[01:02:43] better off. But until that time, there's
[01:02:45] a distribution question and there's
[01:02:47] therefore a uh you know entrenched
[01:02:49] interest. So I think this business with
[01:02:51] self-sufficiency in transplants for
[01:02:53] instance the reason this conference I
[01:02:54] just went to it was an international
[01:02:56] conference but it was in Egypt and the
[01:02:58] reason it was in Egypt is these rules
[01:03:00] about self-sufficiency are working
[01:03:02] against low and middle inome countries
[01:03:04] to to get transplants they should be
[01:03:06] able to cooperate with each other and
[01:03:07] pull their resources and find ways to
[01:03:09] match hard to match patients things like
[01:03:11] that it seemed like a great idea that
[01:03:14] countries should be self-sufficient in
[01:03:15] rich countries even though no countries
[01:03:17] are self-sufficient in transplantation
[01:03:19] We just don't serve the need, right?
[01:03:21] People people who need transplants to
[01:03:23] die without them. But still, it made
[01:03:25] some sense for rich countries to say,
[01:03:27] you know, everyone should act like us.
[01:03:29] We worry about bad things that could
[01:03:30] happen. So, we refrain from allowing
[01:03:33] them to happen. And at the same time,
[01:03:35] that means we refrain from caring for a
[01:03:37] lot of patients, but those patients,
[01:03:38] many of them, many, many, many of them
[01:03:40] are not in rich countries. So, in Egypt,
[01:03:43] people understood that that these rules
[01:03:45] are are working against our patients.
[01:03:48] and we'll see what we can do about
[01:03:50] cooperating and getting cooperation
[01:03:52] between poor countries and rich
[01:03:53] countries, you know, in in lots of
[01:03:56] global trade. That's that's what makes
[01:03:58] sense in trade. But the idea is that the
[01:04:00] shortage is so bad in transplants that
[01:04:03] you can that you can start to form a
[01:04:05] broad coalition. You know, one one thing
[01:04:07] people sometimes ask me is why don't we
[01:04:09] have something like the medical clearing
[01:04:11] house or a New York City public schools
[01:04:14] clearing house for college admissions?
[01:04:16] because college admissions is
[01:04:18] complicated and it's congested. So
[01:04:20] there's problems in in college
[01:04:21] admissions for both for applicants and
[01:04:24] for colleges. But I think the colleges
[01:04:26] aren't yet feeling the pain enough that
[01:04:29] that they'd be really open to uh
[01:04:32] coordinating with each other for for a
[01:04:34] centralized market.
[01:04:35] >> Not to mention there I guess the costs
[01:04:36] of preference formation are really high,
[01:04:38] right? So the coordination problem is
[01:04:40] there's both little demand absolute but
[01:04:42] maybe also little demand relative to the
[01:04:44] cost of the switch,
[01:04:45] >> right? Although there's there's lots of
[01:04:46] information about schools and there'd
[01:04:48] still be visits and things like that,
[01:04:49] you know. So, one of the questions is
[01:04:50] how many places do you have to apply to?
[01:04:52] And that's sort of a prisoners dilemma
[01:04:54] problem. The more the congestion
[01:04:56] actually supports a need to apply to
[01:04:57] many.
[01:04:58] >> Yeah. And so, one of the things we're
[01:04:59] seeing in these congested markets is the
[01:05:01] growth of preference signaling, which we
[01:05:03] pioneered in economics. That is there's
[01:05:06] lots of signaling in labor markets, but
[01:05:08] it's signaling often it's it's
[01:05:11] spent signaling. It's signaling of your
[01:05:13] quality. that is you go to college to
[01:05:16] show that you can learn the kind of
[01:05:17] things that college can teach you and
[01:05:18] then you go get a PhD to show that
[01:05:20] you're the kind of person who can learn
[01:05:22] the kind of things that that you need to
[01:05:23] get a PhD and you write a dissertation
[01:05:25] and you get letters of reference you're
[01:05:26] sending lots of signals that say I'm
[01:05:28] smart but when people are making lots of
[01:05:30] applications it turns out it also helps
[01:05:33] to send signals that say I'm interested
[01:05:34] in you so if you were to take the
[01:05:37] trouble to interview me you'd have a
[01:05:39] chance of hiring me and you know when
[01:05:42] you're getting hundreds of applications
[01:05:43] for every position vision and can only
[01:05:44] have the time to interview a fraction of
[01:05:46] those people, then you value those
[01:05:49] signals that say, "Here's someone who
[01:05:51] looks interested in us." And that's one
[01:05:52] reason why colleges look for expressions
[01:05:55] of interest. You know, if if you're ever
[01:05:56] going to take your kid to uh look at
[01:05:58] college campuses, you should register at
[01:06:00] the admissions office and take the tour
[01:06:02] so that they'll know that you took the
[01:06:03] trouble of visiting them and you might
[01:06:05] be interested in their college. You
[01:06:06] shouldn't just park your car in a
[01:06:08] visitor lot and look around. But there
[01:06:10] are now more formal ways of sending
[01:06:12] signals and you have to think about how
[01:06:13] to design those so that the signal is
[01:06:15] informative. So you have to put a
[01:06:16] restriction on the number of signals you
[01:06:18] can send things like that. You see that
[01:06:20] in dating sites too.
[01:06:21] >> Would you like to speak briefly about uh
[01:06:23] how it works in the economic sort of
[01:06:25] professor market? My understanding is
[01:06:27] you were one of the designers of of the
[01:06:29] way it works to this day. Is that right?
[01:06:30] >> I was. Um, so the American Economic
[01:06:33] Association allows new PhDs in economics
[01:06:37] who well they allow anyone but they
[01:06:39] allow new PhDs in economics who are
[01:06:41] applying for jobs listed in the job
[01:06:42] openings for economic economists
[01:06:44] bulletins. They allow them to send
[01:06:47] signals of particular interest to two of
[01:06:49] those jobs before interviews are
[01:06:51] scheduled. So what does it mean two
[01:06:53] jobs? You you might apply like other
[01:06:55] people do. You might apply to a 100 jobs
[01:06:57] and you shouldn't signal Harvard or
[01:07:00] Stanford because we're fancy places. We
[01:07:03] assume that if we would offer you a job,
[01:07:05] you'd be at least interested in
[01:07:06] considering it. But I used to work at
[01:07:09] the University of Pittsburgh and that's
[01:07:11] a great American university, but it
[01:07:14] doesn't have the same cache as Harvard
[01:07:16] or Stanford. And so we understood that
[01:07:18] we couldn't earn our living by just
[01:07:19] interviewing the same people who Harvard
[01:07:21] and Stanford interviewed because we like
[01:07:23] the same people, but we needed people
[01:07:24] who might not get jobs at Harvard and
[01:07:26] Stanford, but would still be exciting
[01:07:28] and would be excited about us. So
[01:07:30] allowing someone to send a signal to
[01:07:32] Pittsburgh says, I know that Pittsburgh
[01:07:35] is a fine place, and if I don't get that
[01:07:38] job at Harvard that I've applied for,
[01:07:41] I'd be interested in Pittsburgh. and
[01:07:42] that distinguishes them from the people
[01:07:44] who are otherwise similar but would be
[01:07:45] interested in Ohio State instead of
[01:07:47] Pittsburgh. Right? So, it would help us
[01:07:50] um organize our interviews and include
[01:07:53] some interviews that had more
[01:07:55] probability of turning into hires than
[01:07:57] ones that that didn't have signals. And
[01:07:59] among the places that like signals, for
[01:08:01] instance, are uh universities in England
[01:08:03] because the thing about English
[01:08:04] universities, they get lots of North
[01:08:06] American applications and they they hire
[01:08:08] lots of North American PhDs. But every
[01:08:10] North American PhD could teach in
[01:08:12] England because of the language of
[01:08:14] instruction there. And so the the job
[01:08:17] for Oxford is or or for LSSE or for
[01:08:20] Royal Holloway is to figure out is this
[01:08:23] a person who knows that we're an
[01:08:24] excellent university and if they don't
[01:08:26] get a top job in North America, they
[01:08:28] might like to come here or is this a
[01:08:30] person who really wants a job in North
[01:08:32] America, but since it's so easy to add
[01:08:34] another application, they've added LSE
[01:08:36] even though they prefer an
[01:08:37] undistinguished job in the US. And if
[01:08:39] they can distinguish those, then they
[01:08:41] can start to figure out which Americans
[01:08:42] to invite for interviews. There's this
[01:08:45] question of how do you signal interest?
[01:08:47] You know, it's not just the peacock
[01:08:48] feathers which say I'm a I'm a healthy
[01:08:50] male. I can carry around this fan and
[01:08:53] not get eaten by foxes. It's not just
[01:08:56] you should be interested in me. That's
[01:08:57] the conventional signal. It's I'm
[01:08:59] interested in you. Given that you're
[01:09:01] facing congestion, you don't have time
[01:09:02] to interview everyone who applies to
[01:09:05] you. It might pay to interview me.
[01:09:07] >> So why two? Why two signals?
[01:09:09] >> That's a good question. The deep
[01:09:11] theoretical answer is we knew that one
[01:09:13] would help and a 100 would hurt. If we
[01:09:17] had a 100 signals, then the fact that I
[01:09:19] didn't send you a signal would be really
[01:09:21] informative. You'd say you had 100
[01:09:23] signals and you didn't send me one, you
[01:09:24] wouldn't even think about me. So, we
[01:09:26] picked two because it was bigger than
[01:09:28] one and smaller than 100 and closer to
[01:09:30] one. But we're seeing a natural
[01:09:32] experiment uh play out in medicine
[01:09:35] because the medical specialties which
[01:09:37] are facing an influx of lots of
[01:09:39] applications for residencies. They all
[01:09:42] have written position papers saying
[01:09:44] we're going to do what the economists
[01:09:45] do. We're going to have signals of
[01:09:47] interest. And some of them do what the
[01:09:49] economists have done and have relatively
[01:09:51] few signals of interest which in a
[01:09:52] medical context means a handful five or
[01:09:55] six. But some of them obstetrics and
[01:09:59] gynecology uh orthopedic surgery
[01:10:02] otoarendology
[01:10:03] some of them allow 30 signals and 30
[01:10:07] signals we're starting to see are acting
[01:10:09] as a soft cap on the number of
[01:10:11] applications because indeed if I don't
[01:10:13] send you a signal you won't interview me
[01:10:14] because I had 30. So that's going to
[01:10:16] play out in a different way.
[01:10:18] >> Cutting down congestion in a different
[01:10:19] way maybe.
[01:10:20] >> Yeah. Yes. So we're going to see why two
[01:10:22] and not 30 or maybe maybe 30 would be
[01:10:24] better. But uh but that's going to play
[01:10:27] out in in similar labor markets. Market
[01:10:30] places have to help markets be thick.
[01:10:32] Once they're thick, they're going to
[01:10:33] have to deal with congestion. You know,
[01:10:34] once you have a lot of transactions you
[01:10:36] can look at and then you have to make
[01:10:37] them safe and trustworthy and reliable.
[01:10:39] So, you know, these are just principles
[01:10:42] of marketplace design that that are
[01:10:45] pretty general, I think, even though
[01:10:47] marketplaces and markets are very
[01:10:48] different one from another.
[01:10:49] >> And maybe just to connect a couple of
[01:10:51] the other dots from the from the
[01:10:52] conversation so far. So, I loved what
[01:10:54] you said a few minutes ago about, you
[01:10:56] know, the big opportunities for new
[01:10:59] market design is where there's a
[01:11:01] plausible possibility of a paro
[01:11:03] improvement, meaning everybody's worse
[01:11:04] off.
[01:11:05] >> Yeah. Everyone's worse off under the
[01:11:06] current situation. They're better off
[01:11:07] after the design.
[01:11:08] >> Exactly. So, everybody should sort of be
[01:11:09] in favor of the new design and and it's
[01:11:11] largely a coordination problem. And as
[01:11:13] you were telling that story, I again I
[01:11:15] sort of circled back to the example of
[01:11:16] doctors and hospitals because actually I
[01:11:18] learned from your first book, Who gets
[01:11:20] what and why, but I remember you talked
[01:11:22] about what things were like before, you
[01:11:25] know, stable matching was implemented
[01:11:27] and you talked about, you know, doctors
[01:11:29] in the beginning of their second year of
[01:11:30] med school, you know, before you even
[01:11:32] really know they know what specialty
[01:11:34] they want, right? They're already
[01:11:35] getting sort of offers at that point. So
[01:11:37] all of this just sort of connects and
[01:11:38] makes so much sense to hear you to hear
[01:11:40] to hear you say this.
[01:11:41] >> No, no. unraveling is is a big problem.
[01:11:43] You know, economists over the years have
[01:11:45] spent a lot of time thinking about the
[01:11:48] price of transactions without always
[01:11:50] thinking about the other dimensions of
[01:11:52] transactions like their timing.
[01:11:54] Incidentally, I mean, you know, matching
[01:11:56] wasn't always a big topic in economics.
[01:12:00] There was this idea that that you could
[01:12:02] sort of model everything like a
[01:12:04] commodity market, including labor
[01:12:05] markets. It's just that the trouble with
[01:12:08] that in labor markets is instead of
[01:12:09] having some small vector of prices, one
[01:12:12] for each commodity, you had all these
[01:12:14] personalized prices. You know, the the
[01:12:16] wage that you all offer to hire me is
[01:12:18] different from the wage that you would
[01:12:19] offer. And the wage that I would demand
[01:12:20] to work in one job is different from in
[01:12:23] another job. So so all of a sudden the
[01:12:24] prices don't do the work that that we
[01:12:26] think of prices as doing of giving us a
[01:12:28] a lowdimensional vector that that
[01:12:30] coordinates lots of actions. So
[01:12:33] matching, you know, you care who you're
[01:12:36] matched to and so you can't just choose
[01:12:37] what you want. You also have to be
[01:12:39] chosen.
[01:12:40] >> So Scott, as as a as a former student of
[01:12:42] ours, you've gotten lots of advice from
[01:12:44] him. I know you wanted to maybe ask a
[01:12:46] little bit about for about the next
[01:12:47] generation of students.
[01:12:48] >> Yeah, look, I mean, let me just also
[01:12:51] again like, you know, shout out the
[01:12:52] blog. I should shout out Al, too. I
[01:12:54] mean, he's just like an absolutely
[01:12:55] incredible mentor and and adviser
[01:12:57] throughout. Kind of like, you know, Tim
[01:12:58] has been, you know, at A6Z crypto. I
[01:13:00] will add, you know, as you're thinking
[01:13:02] about students today, both both people
[01:13:04] who are going to be scholars of
[01:13:06] marketplaces and and marketplace design
[01:13:08] and also practitioners, right? You know,
[01:13:10] sort of people are going to go out and
[01:13:11] build marketplaces in the field and
[01:13:13] maybe coordinate and collaborate with
[01:13:14] with economists and other scholars, what
[01:13:16] would you push them to think about and
[01:13:19] how would you, you know, how would you
[01:13:20] advise them?
[01:13:21] >> Well, I mean, you have to think about
[01:13:22] markets in general and also in
[01:13:25] particular, right? So, so different
[01:13:27] marketplaces are different. One of the
[01:13:29] nice things about market design coffee
[01:13:30] at Stanford is, you know, we have people
[01:13:33] from Uber or Airbnb or Carta or Scale
[01:13:37] AI, you know, come join us at coffee and
[01:13:39] they all have different uh market design
[01:13:41] problems. But there are some principles
[01:13:44] of design that you can think of and one
[01:13:45] of them is that incentives matter. You
[01:13:47] know, many of many companies don't
[01:13:48] really think about that. Also the thing
[01:13:50] about doing experiments uh how to
[01:13:52] evaluate experiments you know there's a
[01:13:54] temptation on the web to do experiments
[01:13:56] sort of AB comparisons and you do them
[01:13:58] on a tiny fraction of your transactions
[01:14:00] and if you know if treatment A is better
[01:14:02] than treatment B someone in marketing is
[01:14:04] going to say why don't we go all to
[01:14:05] treatment A but if you have an economist
[01:14:07] on the team they'll say wait a minute
[01:14:08] you know no one noticed we were doing
[01:14:09] this experiment but once we give
[01:14:10] treatment A to everyone they're going to
[01:14:12] know that that's how we're organizing
[01:14:14] the market and they're going to think
[01:14:15] about how to react and we should think
[01:14:17] about that too. So, lots of people don't
[01:14:19] think about equilibrium and economists
[01:14:21] think a lot about equilibrium, but
[01:14:23] sometimes we don't think enough about
[01:14:24] equilibration. How are we going to get
[01:14:26] to the equilibrium? You know, can we fix
[01:14:28] this thing that we're worried about
[01:14:29] without breaking it? So, there's lots of
[01:14:31] things to think about and I don't know
[01:14:34] how the academic discipline is going to
[01:14:38] evolve. You know, my first half dozen
[01:14:40] papers on kidney exchange were in
[01:14:42] economics journals, but my most recent
[01:14:45] half dozen papers on kidney exchange
[01:14:46] were in medical journals because we're
[01:14:49] trying to convince surgeons to do things
[01:14:51] the way we think they should do them.
[01:14:53] Um, and I think that's a natural
[01:14:55] evolution. You know, I'm happy to have a
[01:14:57] platform in medical journals. You know,
[01:14:58] you think about engineering. Engineering
[01:15:00] is just applications of physics, but
[01:15:03] they have their own journals. You know,
[01:15:05] we were at a conference, a matching
[01:15:07] conference in Sicily this summer and we
[01:15:09] visited before and we visited Syracuse
[01:15:11] where Archimedes lived. And when
[01:15:14] Archimedes lived there, you know, the
[01:15:16] physicists and the engineers, they were
[01:15:17] the same guy. But now engineering is
[01:15:20] still about physics, but the the civil
[01:15:22] engineers don't publish about bridges in
[01:15:24] physics journals and the aeronautical
[01:15:26] engineers don't publish in civil
[01:15:28] engineering journals. And they're both
[01:15:30] using the same physics with which we
[01:15:32] know God created the heavens and the
[01:15:34] earth. But they have to emphasize
[01:15:36] different things. If you're building a
[01:15:37] bridge and there's some problem, you can
[01:15:39] often solve it by making the bridge
[01:15:41] heavier and stronger. But that's not the
[01:15:43] way to solve problems for airplanes. So
[01:15:45] I'm not sure that when as we educate
[01:15:47] economists in market design that we'll
[01:15:50] be just sending them off to economics
[01:15:52] department. And indeed I have a student
[01:15:54] Kurt Sweat from two years ago who's in a
[01:15:56] medical school now. We study heart
[01:15:57] transplants.
[01:15:58] >> And conversely, you know, economics
[01:16:00] departments are sometimes hiring
[01:16:01] computer scientists because they have
[01:16:02] the, you know, adjacent market design
[01:16:04] toolkit. Same story.
[01:16:05] >> We certainly should. We're we're a
[01:16:07] little slow on that, but it happened in
[01:16:09] my generation with game theorists,
[01:16:10] right? A lot of the game theorists of my
[01:16:12] generation don't have PhDs in economics,
[01:16:14] but economics swept over us and was very
[01:16:16] welcoming. And I'm I'm still waiting for
[01:16:18] that to happen with computer science.
[01:16:20] I'm just pleased we've made a dent at
[01:16:22] all so far given the given how sort of
[01:16:24] traditional I think uh especially top
[01:16:26] economics departments are. So I I'm
[01:16:28] going to focus on the positive. I'm
[01:16:30] optimistic it's directionally going the
[01:16:32] right way. I don't see why it would stop
[01:16:33] now.
[01:16:34] >> Yeah. Exactly. And and maybe one you
[01:16:36] know one thing I take away from what
[01:16:37] what you just said Al was uh kind of the
[01:16:40] importance if you want to have impact if
[01:16:41] you want your work to have impact like
[01:16:43] >> know who your audience is and go to them
[01:16:46] like meet them where they are. And if
[01:16:47] that means publishing somewhere where
[01:16:49] you're not accustomed to, go do it. If
[01:16:51] that means spending time, you know, in
[01:16:54] your case, like in doctor's offices or,
[01:16:56] you know, in office, whatever it is.
[01:16:59] >> Yeah. Exactly. So, um,
[01:17:01] >> yeah. No, absolutely. We economists
[01:17:03] speak to each other in models. No one
[01:17:04] else speaks in models or at least in our
[01:17:06] kind of models. So, you have to learn
[01:17:08] their language so you can speak to them.
[01:17:11] And you often have I mean one reason I
[01:17:13] wrote the the my previous book who gets
[01:17:16] what and why was market design is an
[01:17:18] outward-f facing part of economics. So
[01:17:20] I've had many conversations in my life
[01:17:22] where I explain to people who are in a
[01:17:24] marketplace that's having some problem
[01:17:26] why they should be listening to an
[01:17:27] economist. So I thought writing a book
[01:17:29] about that might might lower the
[01:17:31] barriers to entry.
[01:17:32] >> Scott, I'm sure this resonates with you
[01:17:33] even more than me, but the work we do at
[01:17:35] A16Z Crypto, we we we face that similar
[01:17:38] issue every day. Right. So,
[01:17:41] >> I mean, look, this has been utterly
[01:17:43] incredible. Maybe if we could spend a
[01:17:45] minute on your outlook for the future.
[01:17:47] Like, what are you most excited about in
[01:17:50] the, you know, in the future we're going
[01:17:51] to see or that you hope we see?
[01:17:53] >> Well, I'm excited about AI. I remain
[01:17:56] excited about democracy. I hope it's
[01:17:58] we're going to keep having it. I'm
[01:18:01] excited about the young generation of
[01:18:02] economists and computer scientists who
[01:18:04] more and more talk to each other. I used
[01:18:06] to never go to computer science talks
[01:18:09] but now the reason I don't go to them is
[01:18:10] we have competing economics talks and
[01:18:13] medical talks at the same time at
[01:18:14] Stanford. So uh so I think this is an
[01:18:19] exciting time for for scientists
[01:18:21] interested in markets and of course some
[01:18:25] of that work for various reasons is
[01:18:27] moving out of universities into giant
[01:18:29] tech companies right the parts that
[01:18:31] involve training large language models
[01:18:33] but but other parts as well. Uh
[01:18:36] nevertheless I'm I'm cautiously
[01:18:38] optimistic that American universities
[01:18:40] are going to remain the center of
[01:18:41] research in for a lot of these things
[01:18:43] around the world. I'm a little worried
[01:18:45] about that too. Um, you know, we've been
[01:18:47] a a big exporter of education, which
[01:18:50] involves having lots of international
[01:18:51] students come to American universities.
[01:18:53] So, we'll see how that develops. One of
[01:18:55] the matching markets that I think we
[01:18:57] need to pay more attention to is uh
[01:19:00] resettling refugees and and other kinds
[01:19:01] of migrants. Right. Right now, that's
[01:19:03] clearly a broken market. You know, when
[01:19:05] I go to Europe, I land at a European
[01:19:07] airport having flown across the water
[01:19:09] and I get off with my shoes dry. A lot
[01:19:12] of people are trying to get to Europe in
[01:19:14] little boats over the Mediterranean and
[01:19:16] trying to get to the US across the land
[01:19:18] border and and you know it's a matching
[01:19:21] problem. They can't just choose where
[01:19:23] where they'll be given asylum and we
[01:19:25] can't just choose who will cross the
[01:19:26] borders. So we have to do that a lot
[01:19:28] better. It's obviously a real mess
[01:19:30] around the world, not just in the US on
[01:19:31] our on our southern border. Um, so
[01:19:34] that's a matching problem we have to
[01:19:36] deal with because if if the water
[01:19:38] continues to rise, there are going to be
[01:19:40] lots of human migrants around the world,
[01:19:43] internal migrants and external. I mean,
[01:19:45] those are political questions, but going
[01:19:47] to have to think about how to deal with
[01:19:48] with people moving around from where
[01:19:50] they are to where they'd like to be and
[01:19:52] whether we want them to come. I mean, so
[01:19:54] this whole question of what more kids
[01:19:56] have social supports is going to be very
[01:19:57] big there. It's going to be big on uh
[01:19:59] AI. You know, the think about things
[01:20:01] like facial recognition, right? The city
[01:20:04] of San Francisco doesn't let the police
[01:20:06] use facial recognition. You could
[01:20:08] imagine that if AI somehow makes an
[01:20:12] early wrong step of a highly publicized
[01:20:14] sort that will have regulations that say
[01:20:16] you can't use AI for things. Or you
[01:20:19] could imagine that AI will be beneficent
[01:20:22] and and you know, augment jobs rather
[01:20:24] than replacing them. and you know all
[01:20:26] sorts of good things will happen. It's
[01:20:28] going to be fun to to watch. And and let
[01:20:30] me just note one of the things that I
[01:20:31] learned from you very early like one of
[01:20:33] the very first insights of your class
[01:20:35] like when I took it gosh a decade and a
[01:20:37] half ago was you know is that that
[01:20:39] outcome is indogenous right it's not
[01:20:41] that these things are just you know good
[01:20:43] or like these markets are are good or
[01:20:44] bad right it's that through proper and
[01:20:47] social welfare you know sort of
[01:20:49] maximizing or attuned you know
[01:20:50] marketplace design you can actually get
[01:20:52] yourself into the equilibrium that has
[01:20:54] the better outcome
[01:20:55] >> certainly try you can work at it and
[01:20:56] that's part of market design. Exactly.
[01:20:59] It's not it's not static, right? It's
[01:21:01] not like the the answer is a yes or no.
[01:21:03] These things are useful or or harmful.
[01:21:05] It's that we can think about the rules
[01:21:07] that govern the architecture of
[01:21:09] marketplaces to to make them work
[01:21:10] better.
[01:21:10] >> And we have to think about the
[01:21:12] transition too. Not just about the
[01:21:13] equilibrium, but about equilibrium.
[01:21:15] >> So you guys are
[01:21:16] >> Yeah.
[01:21:16] >> taking on a big responsibility.
[01:21:19] >> We stand on the shoulders of giants, Al.
[01:21:21] So
[01:21:21] >> there you go.
[01:21:23] >> Exactly.
[01:21:24] You you give an Ashley dinner talk at
[01:21:26] the Nobel ceremony and mine had a
[01:21:28] metaphor of a a pyramid of acrobats, you
[01:21:30] know, each standing on each other's
[01:21:32] shoulders and lifting each other up.
[01:21:34] >> That's a beautiful picture.
[01:21:35] >> Excellent.
[01:21:36] >> Fantastic. Thank you so much, Al, as
[01:21:38] always.
[01:21:39] >> Super inspiring to talk to you.
[01:21:40] >> Incredible. Yeah, nice to talk to you
[01:21:42] guys.
[01:21:43] >> Wow. Well, that was uh that was quite
[01:21:45] the honor getting to spend time with
[01:21:46] with Al Roth. Totally inspiring
[01:21:48] conversation. toward the end we started
[01:21:50] talking about this notion of repugnant
[01:21:53] goods, repugnant markets and moral
[01:21:54] economics, a sort of new book. Um, you
[01:21:57] know, so going back to when you were
[01:21:58] there at Harvard, was that already kind
[01:22:00] of something he was thinking about at
[01:22:01] that time or
[01:22:02] >> Yeah, it's funny. I mean, he has this um
[01:22:05] very well-known paper in the Journal of
[01:22:07] Economic Perspectives called Repugnance
[01:22:09] as a constraint on markets. He's been
[01:22:11] thinking about repugnance for years and
[01:22:13] years and years. And like the example
[01:22:15] you talked about with having to amend
[01:22:18] the National Organ Transplantation Act
[01:22:21] in order to enable kidney exchange,
[01:22:23] right? Like you know, it comes up in so
[01:22:25] many of the contexts that he's been
[01:22:27] working on because when you're going in
[01:22:29] to change the way a market functions,
[01:22:32] you know, you're you're going to go in
[01:22:33] and build a marketplace of one form or
[01:22:35] another, you need buyin from
[01:22:37] participants. There are lots of things
[01:22:38] that economists would like to say, oh,
[01:22:40] you know, we we should just solve this.
[01:22:42] You know, design a market like let it
[01:22:43] go, we'll be done. But actually like
[01:22:45] people are unwilling to do that. By the
[01:22:48] way, crypto listeners like listen up.
[01:22:50] This is like a huge part of how we have
[01:22:52] to think about building marketplace
[01:22:54] design in cryptoland, right? Like part
[01:22:56] of the challenge when you're designing a
[01:22:58] market or a marketplace is it doesn't
[01:23:01] just have to work, but it has to work in
[01:23:04] a way that appeals to the prospective
[01:23:06] participants. Right? it has to, you
[01:23:08] know, enter into the sort of existing
[01:23:11] system in a way that participants are
[01:23:14] willing to adapt around your solution.
[01:23:17] And so Al has all these stories and they
[01:23:20] would come up in like almost every
[01:23:21] session of like something that made
[01:23:23] sense to do or would have in principle
[01:23:25] made sense to do and was repugnant,
[01:23:28] right? It just for whatever reason the
[01:23:29] market participants said, "No, no, no,
[01:23:30] no, no. You can't do that." One thing
[01:23:32] I'm really excited about with this book
[01:23:34] is that it's something he's been talking
[01:23:35] about and running into for years and
[01:23:38] years, but has never really had a
[01:23:41] concrete framework, right? There's never
[01:23:42] been a way to think about like how you
[01:23:45] interact with repugnance. And it sounds
[01:23:47] like this book is going to give like the
[01:23:50] meat to the question of how do we reason
[01:23:53] about what is repugnant? How do we
[01:23:55] reason about what you need to do to like
[01:23:57] work around it? and like when it's a
[01:23:59] hard constraint versus when it's a soft
[01:24:00] constraint and again you know sort of as
[01:24:02] I say like this is something we need to
[01:24:04] do a lot of in cryptoland
[01:24:05] >> I mean one thing that's amazing just you
[01:24:07] know his original theory work was in
[01:24:09] sort of the classic models right so you
[01:24:10] talked about stable matching which for
[01:24:12] example did not have this idea of like
[01:24:13] constraints on couples and then I kind
[01:24:16] of feel like a lot of his journey has
[01:24:17] been the back and forth between the
[01:24:18] theory and the practice and you go out
[01:24:20] the practice you're like oh couples are
[01:24:22] really important solve the problem in
[01:24:23] practice but then don't stop there
[01:24:25] >> right don't stop there right the theory
[01:24:27] that explains what's going on. Yep.
[01:24:29] >> Enrich the theory, take it to the next
[01:24:30] level. And so perhaps like with
[01:24:31] repugnance, this is again what we're
[01:24:33] seeing like you first encounter it out
[01:24:34] in the wild where markets that the
[01:24:36] papers tell you you should design, you
[01:24:38] can't, and then you come back and you
[01:24:39] say, "How can we update the theory so
[01:24:41] that we can sort of think clearly about
[01:24:42] about these issues?"
[01:24:43] >> Absolutely. No, totally. I often
[01:24:45] describe it as like there's a diagram
[01:24:47] theory to practice to evaluation and
[01:24:50] then the evaluation sort of like points
[01:24:51] back to practice, but also points back
[01:24:53] to theory and you get, it's kind of hard
[01:24:55] to see in this visual, but it looks like
[01:24:56] a nautilus, right? like you get this
[01:24:58] like sort of like golden section type
[01:24:59] like spiral that constantly makes the
[01:25:02] marketplace designs deeper and and sort
[01:25:04] of both more impactful and more
[01:25:06] intellectually fascinating.
[01:25:07] >> All right. Well, I think that's a great
[01:25:08] note to to wrap up on. So, Scott, thanks
[01:25:11] so much for the co-host. Fantastic
[01:25:13] conversation.
[01:25:13] >> Tim, thanks so much. This was awesome.
