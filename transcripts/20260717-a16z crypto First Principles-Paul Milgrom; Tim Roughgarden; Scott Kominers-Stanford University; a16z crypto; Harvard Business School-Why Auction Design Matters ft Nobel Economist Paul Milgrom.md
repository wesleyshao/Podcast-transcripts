---
访谈时间: "2026-07-17"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Paul Milgrom; Tim Roughgarden; Scott Kominers"
嘉宾公司名称: "Stanford University; a16z crypto; Harvard Business School"
播客名称: "a16z crypto First Principles"
播客url地址: "https://www.youtube.com/watch?v=y60fmzaZjsI"
全文提及的关键名词:
  - "Paul Milgrom"
  - "auction theory"
  - "mechanism design"
  - "market microstructure"
  - "Glosten-Milgrom model"
  - "Grossman-Stiglitz paradox"
  - "FCC spectrum auctions"
  - "incentive auction"
  - "price discovery"
  - "prediction markets"
  - "DeFi"
  - "compute futures"
  - "Nvidia"
  - "data centers"
  - "wireless spectrum"
  - "5G"
字幕来源: "automatic_captions:en-orig:English (Original)"
YouTube视频标题: "Why Auction Design Matters (ft. Nobel Economist Paul Milgrom)"
---

# Why Auction Design Matters (ft. Nobel Economist Paul Milgrom)

## Transcript

[00:00] Many of the assumptions that we make in
[00:02] economics are arbitrary for convenience,
[00:05] for simplicity, and they're just wrong.
[00:07] Pacific Bell asked me to look at this
[00:09] proposal by the government. What they
[00:11] had was just a mess [music] and ignored,
[00:13] you know, some obvious problems. The
[00:15] last time I went to the FCC, [music] I
[00:17] said, you know, it isn't that hard.
[00:18] Here's how you could do it with linked
[00:20] Excel spreadsheets, and I just handed
[00:22] them the disk. One of the areas that we
[00:24] will be moving into is creating [music]
[00:27] futures markets for compute. Here's the
[00:29] economic problem we're trying to solve.
[00:31] If it costs you $20 billion to build a
[00:33] data [music] center, why don't you build
[00:36] a $30 billion data center? Well, it's
[00:38] because it's very risky. Suppose [music]
[00:40] that next year Nvidia were to come up
[00:42] with a chip that's 50% faster and uses
[00:45] 30% less electricity. [music]
[00:47] >> It's been a huge theme throughout your
[00:48] career that there's a practical problem
[00:50] that then spawns new theory that then
[00:52] gives rise to new practical designs.
[00:54] What does it feel like? How does it come
[00:55] about?
[00:56] >> are [music] two things you're conflating
[00:57] there, I think. One is that
[01:08] >> Hi everyone, and welcome to First
[01:10] Principles, a series by the team at a16z
[01:13] crypto. I'm Tim Ruffgarden. I'm the head
[01:15] of research at a16z crypto, and today
[01:18] we're talking about how prices form in
[01:20] complex markets and how the rules of the
[01:22] game can shape outcomes. Our guest today
[01:26] is Paul Milgrom, the Nobel laureate in
[01:28] economics whose work on auction theory
[01:30] fundamentally changed how we understand
[01:32] bidding, pricing, and the role of
[01:34] information in markets. Among many
[01:37] accomplishments, he co-designed the FCC
[01:39] spectrum auctions that have enabled many
[01:42] wonderful technologies like 5G wireless,
[01:44] while at the same time generating over
[01:46] $100 billion in revenue for the US
[01:49] government.
[01:50] Paul's ideas have been extremely
[01:51] influential in economics, and in many
[01:53] cases they map directly onto the
[01:56] mechanism design challenges that arise
[01:58] in on-chain markets and decentralized
[02:01] finance.
[02:02] Joining us is Scott Kominers, Harvard
[02:04] Business School professor and research
[02:06] partner at a16z crypto, as we talk with
[02:09] Paul about his foundational
[02:10] contributions to auction theory and what
[02:13] they reveal about designing better
[02:15] markets. Here's our conversation.
[02:18] All right, so Scott, we get to interview
[02:21] Paul Milgrom next. I'm really excited
[02:23] about this. What one very humbling thing
[02:25] to do is just sort of go back over all
[02:28] of the different things. Even let's just
[02:29] restrict to the paper writing. Like
[02:31] let's put aside the practical impact.
[02:32] Just looking at sort of the papers he's
[02:34] written over his career and it's just
[02:36] kind of
[02:37] landmark paper after landmark paper.
[02:39] It's like, how can somebody keep this up
[02:42] for this long? It's just it's it's
[02:43] pretty mind-blowing.
[02:44] >> Well, and I'll tell you, not only has he
[02:47] written, you know, landmark papers in
[02:49] basically everything in economic theory,
[02:52] but every single thing he's ever worked
[02:55] on is the most exciting thing he's ever
[02:57] worked on. I mean, he just has this like
[02:58] incredible energy and like love for all
[03:02] of it.
[03:02] >> I got to ask, so um around the time he
[03:06] won the Nobel Prize along with Bob
[03:08] Wilson, you were actually a co-author uh
[03:10] on sort of a survey basically of of his
[03:13] work as as part of that. So, can you
[03:15] talk a little bit about the process of
[03:16] writing that and just what was it like?
[03:18] >> was so fun. It was so much fun. So, the
[03:21] the Scandinavian Journal of Economics
[03:23] puts out a survey article on the year's
[03:25] economics Nobel laureate or laureates.
[03:28] Tommy Anderson, who who was the handling
[03:31] editor and and co-author and and
[03:33] collaborator with my my friend and and
[03:35] co-author Alex Tadelis, you know, sort
[03:36] of a network of networks, reached out
[03:38] and basically asked whether five of us
[03:41] together, all of whom had in one fashion
[03:44] or another worked with Paul and or Bob,
[03:46] Bob Wilson, uh who who won the prize
[03:48] jointly with Paul,
[03:50] uh would would work together to write a
[03:52] survey, and it was
[03:54] uh, incredible. So,
[03:55] uh, Alex Tadelisboyen, Piotr Dworczak,
[03:57] Mohammad Akbarpour, Shengwu Li, and I
[03:58] sat down to do this.
[03:59] >> That's quite the dream team right there,
[04:01] so.
[04:02] >> Uh,
[04:03] I like I was astounded to be included in
[04:06] the list with those other four.
[04:07] >> [laughter]
[04:08] >> Like,
[04:09] um, it was incredible. So, first of all,
[04:11] like, you know, we we did our homework,
[04:13] right? Like, we tried, I would say, to
[04:15] read all of Paul and Bob's papers,
[04:18] discovering that even though we thought
[04:20] like what are the weird things is like,
[04:21] you know, most of them were were Milgrom
[04:23] and/or Wilson students.
[04:25] Um, all of us had like grown up in grad
[04:27] school like reading their work.
[04:30] And I always felt like I was still
[04:32] discovering I only knew like 25% of it.
[04:34] Even on the topics I'm an expert in,
[04:36] right? It was like, you know, oh wait,
[04:37] like Milgrom introduced that idea in
[04:38] auctions, too? Like, who knew? Like,
[04:40] what? You know, and then we interviewed
[04:42] them. So, we had these long sit-down
[04:43] conversations to hear about the
[04:46] generation of the ideas and how they all
[04:47] fit together. Because one thing that
[04:49] it's possible to look at the body of
[04:51] work and not really understand without
[04:54] the context is they weren't just like
[04:57] writing papers in auction theory, right?
[04:59] Like, Paul Milgrom, yes, he was writing
[05:01] like what are now classics of economic
[05:03] theory on auctions and information and
[05:05] different forms of exchange,
[05:07] but they were in constant dialogue with
[05:10] applied problems. And a lot of the most
[05:13] fundamental ideas in these auction
[05:15] theory papers were coming out of an
[05:18] either a thing he had observed in the
[05:19] field or a question, sort of like a
[05:23] thing that you needed to know in order
[05:25] to be able to take practical market
[05:27] design to the next level,
[05:29] and that we didn't have a theory
[05:31] language to speak about. And so, that,
[05:34] you know, precipitated papers.
[05:35] >> So, I'm I'm sure we'll touch on a a
[05:37] bunch of the things he's worked on, so
[05:38] maybe we should just spend a little time
[05:39] laying some groundwork. One thing I
[05:41] think would be fun to ask about is
[05:43] actually a very important, you know,
[05:45] paper in in effect finance
[05:48] uh, by Glosten and Milgrom
[05:50] >> [snorts]
[05:51] >> and and in particular like the idea it's
[05:53] almost like can you really probe the
[05:57] content of an efficient market
[05:58] hypothesis and really trying to
[06:00] understand kind of in a detailed way how
[06:03] prices form in financial markets.
[06:05] >> One of the things we learned in that
[06:06] survey article when we were writing that
[06:07] survey article was that like why they
[06:09] got into auctions in the first place.
[06:10] Paul was really curious about
[06:13] the mechanisms and mechanics of price
[06:16] formation, right? Like how is it that
[06:18] markets actually achieve prices?
[06:21] >> Which I just have to say that's almost
[06:22] like a very obviously I'm biased I'm
[06:24] trained as a computer scientist but I
[06:25] think of that as like a super computer
[06:26] science-y way and almost critique of
[06:29] like say general equilibrium theory and
[06:31] like the classic economics. So it's just
[06:33] so cool.
[06:33] >> Completely, right? Like you know, most
[06:35] of economics just sort of assumes that
[06:36] prices exist and then reason about them.
[06:38] Most of the way we use prices in markets
[06:41] very much rely on us having to have
[06:42] found them somehow.
[06:44] And a lot of economics sort of at
[06:47] baseline doesn't have a story about how
[06:49] those prices are discovered.
[06:52] Glosten and Milgrom proposed a really
[06:53] simple and incredibly intuitive answer,
[06:56] which is
[06:57] that story forgets that people have
[07:00] different information conditional on
[07:02] being the person who wants to sell
[07:04] versus the person who wants to buy. And
[07:06] so you can actually like you can get
[07:08] price discovery in a world where all the
[07:10] information is aggregated in the market
[07:13] because different people come to the
[07:14] market with different information and
[07:16] that leads them to like take different
[07:18] sides of the transaction.
[07:19] >> And then if someone trades with you, you
[07:21] learn something, right? If someone buys
[07:22] something from you, you're like, "Ooh,
[07:24] maybe it's a little more valuable than I
[07:25] thought." Or if they want to sell
[07:27] >> aggregation in the market comes from the
[07:29] execution of those trades. This one
[07:31] paper was foundational in in information
[07:34] economics and market microstructure and
[07:36] finance. I mean like this one paper is
[07:38] sort of like helped create three
[07:39] different modern economic fields or
[07:41] something and that's like
[07:43] You know, I guess that's like, you know,
[07:44] an afternoon at the office for Paul
[07:46] Milgrom.
[07:47] >> Yeah.
[07:48] So, obviously we have to talk to him
[07:49] about auctions, right? And
[07:51] I think what could be fun is to zoom in
[07:53] on kind of like the early '80s when
[07:56] there was a lot happening in auction
[07:57] theory. I mean, so you know, Vickrey was
[07:58] back in '61, that kind of laid out, you
[08:00] know, how to think about it, properties
[08:01] you might want, second price, first
[08:02] price auctions.
[08:03] You know, Bob Wilson, who we mentioned,
[08:05] tons of work in the '60s, but some
[08:07] really interesting things happened in
[08:08] the early '80s. And one by a different
[08:12] economist, also a Nobel Prize winner,
[08:14] Roger Myerson, wrote a paper optimal
[08:16] auction theory or optimal auctions, I
[08:18] forget the exact title, which asks
[08:20] about, you know, if you're a seller and
[08:22] you're selling an item, what's the way
[08:24] to sell it that will maximize your
[08:26] revenue,
[08:27] framed as an optimization problem, which
[08:29] of course computer scientists love,
[08:31] right? So, computer scientists read the
[08:32] Myerson paper and they're like, this is
[08:34] exactly how I want to think about the
[08:35] problem.
[08:36] >> [laughter]
[08:37] >> And fun fact, economists were initially
[08:38] so, you know, sort of confused by this
[08:41] way of framing the problem that there's
[08:42] a whole follow-up paper that reframes it
[08:44] into economic language.
[08:45] >> [laughter]
[08:46] >> It's a great illustration of like how
[08:48] economics and computer science
[08:49] perspectives work together. Like, it
[08:51] turns out that trying to like
[08:53] deconstruct what's going on in an
[08:55] optimization can lead you to economic
[08:57] insights you would not have found
[08:58] otherwise, and those economic insights
[08:59] have since gone on to like frame lots of
[09:02] new optimization questions. It's
[09:03] actually like seeing early versions of
[09:05] that feedback that we see a lot of
[09:06] today.
[09:07] >> Absolutely.
[09:08] So, this is a landmark paper, um but
[09:10] then simultaneously,
[09:13] Paul was also writing a landmark paper
[09:15] >> Yep.
[09:15] >> with Weber. So, there's this
[09:16] complimentary sort of, you know, equally
[09:19] mind-blowing paper. So, could you talk a
[09:21] little bit about that? What what what
[09:22] Why is the Milgrom and Weber paper so
[09:23] famous?
[09:24] >> One thing I'm sure Paul will talk about,
[09:25] like there are several different ways in
[09:27] which economics papers contribute to our
[09:30] understanding. One of them is through
[09:32] the specific answers and sort of like
[09:34] design insights and and predictions they
[09:36] give. Another is through the framework,
[09:39] the model, the way of thinking about the
[09:41] problem that they produce that then
[09:43] turns out to be useful for thinking
[09:44] about many other many other problems.
[09:46] And
[09:47] you know, Milgrom and Weber gave what
[09:49] has become essentially the single most
[09:52] standard and like
[09:54] viable framework for reasoning about
[09:56] auctions with correlated values in
[09:58] various forms. Um what are called
[10:00] affiliated values.
[10:01] >> And just in case this sounds academic, I
[10:03] mean I mean Scott, how many times have
[10:05] we been in conversations with startups,
[10:07] with founders, and we literally
[10:10] we refer to this paper when we give
[10:12] advice on kind of the details of how to
[10:14] run for example an NFT auction.
[10:16] >> and in particular like, you know, so
[10:19] many auctions in practice. Like this is
[10:21] almost the normal case, right? An
[10:22] auction where there's some sense in
[10:24] which everyone's assessment of the value
[10:27] of the good is informative about what
[10:28] the value of the good actually is.
[10:30] Right?
[10:31] >> So in other words, you can sort of
[10:31] piggyback on others' knowledge about
[10:34] >> Exactly. You can piggyback on others'
[10:35] knowledge. And sort of learn things from
[10:36] their bidding about what your beliefs
[10:40] about the value should be. And like
[10:41] that's not a thing that's relevant in
[10:42] every single auction, but it's relevant
[10:44] in so many auctions. And it's and like
[10:47] and you know, it might be relevant in
[10:48] all crypto auctions, right? Like like
[10:51] >> Yeah.
[10:51] >> you know, in crypto we're usually we're
[10:53] often selling a digital asset as an part
[10:56] of an exercise in a forming a sense of
[10:59] value around that asset. Like you know,
[11:01] you're selling early access to an NFT
[11:04] community. You know, first round NFT
[11:06] minting sale. Or you're you know,
[11:08] selling token units that are then going
[11:10] to be used as the network token of an
[11:11] ecosystem and you're trying to reason
[11:14] about who's going to be participating,
[11:16] how much do we think this ecosystem is
[11:18] going to grow, like who's going to be
[11:19] using it, and how much do we think these
[11:21] tokens really are going to anchor a
[11:22] community. And all of those things
[11:24] you're drawing inferences from seeing
[11:25] other people's bids. And if you can,
[11:27] things from you know, inferences from
[11:29] who's bidding.
[11:30] >> Well, there's a million auction theory
[11:31] papers we could zoom in on. I'm sure
[11:33] we'll touch on some others, but clearly
[11:34] we're going to be talking about that
[11:35] one, Milgrom-Weber. We also have to
[11:37] talk, obviously, about Paul's work on
[11:39] the practical side. He wrote a famous
[11:40] book called Putting Auction Theory to
[11:42] Work. I love that title. You know, the
[11:44] theory is a great starting point, but
[11:45] then of course there's a lot of hard
[11:47] work to do in the trenches.
[11:48] I'd say both to fine-tune how the
[11:51] auctions work to take into account
[11:52] real-world constraints, but then also
[11:54] just the political process of actually,
[11:57] you know, getting all the stakeholders
[11:59] to to be on board with it. And you and I
[12:01] both seen firsthand the work that Paul
[12:03] has put into this, yeah.
[12:04] >> We'll have to ask him some about how the
[12:06] conversations around the first US
[12:09] spectrum auctions worked. Like, you
[12:10] know, how did he collaborate with the
[12:12] Federal Communications Commission? Like,
[12:14] what were all the different parties
[12:15] involved? Because that was sort of,
[12:17] you know, one of the first big like
[12:21] public projects of market design. Sort
[12:23] of the modern brand of using modern
[12:27] economic theory jointly with computer
[12:29] science and operations research and all
[12:31] of these different toolkits to redesign
[12:35] or to design from scratch a marketplace
[12:38] towards a huge public goal. Like, the
[12:40] spectrum auctions are one of the first
[12:42] really big examples.
[12:44] >> Um and I think we got to ask him about
[12:45] the FCC incentive auction, which is more
[12:47] recent, that's maybe maybe eight or nine
[12:49] years ago. I think unquestionably one of
[12:51] the biggest market design triumphs of
[12:53] the 21st century.
[12:55] >> And I teach it in my classes as like,
[12:57] it's market design as entrepreneurship.
[12:59] You know, you are building this thing.
[13:03] You're imagining a major change in the
[13:05] world that you are going to facilitate
[13:07] that at best is going to happen 7 to 10
[13:10] years down the line. Right? Like, you
[13:12] will not know whether you've succeeded.
[13:13] And like, market design entrepreneurship
[13:15] is like this. Like, you don't know
[13:16] whether you're going to succeed until,
[13:20] you know, a huge change in how people do
[13:23] business and how consumers go through
[13:24] their lives.
[13:26] And you have to along the way, like both
[13:28] have the energy and the confidence and
[13:30] the clarity of thought to foresee the
[13:32] problems, to sort of, you know, look
[13:34] downstream and optimize in the moment at
[13:36] the same time, to iterate, to explore,
[13:38] and like, you know, sort of build a
[13:40] coalition around your marketplace design
[13:42] that will enable you to reach that
[13:44] downstream goal, constantly updating
[13:46] even your understanding of what the goal
[13:47] is.
[13:48] You know, and as I said, like every
[13:49] single thing Paul has ever worked on,
[13:51] he's like the most excited he's ever
[13:52] been about anything. It's just like an
[13:54] absolutely wonderful characteristic of
[13:56] him as a human.
[13:57] You know, I would see him, like, you
[13:58] know, he'd come in to Chicago or Harvard
[14:00] to give a seminar or something, like,
[14:01] and we we'd go for a walk and he would
[14:02] tell me about the new impossible problem
[14:05] in the design of the incentive auction.
[14:07] And like every single one of these
[14:09] impossible challenges, he was just like,
[14:10] "And this is going to be so fascinating
[14:12] to solve. Like, here's here's what we're
[14:14] thinking about so far. Here's just
[14:15] constantly treating everything that
[14:18] should have been a totally impossible,
[14:20] unsurmountable roadblock as this like
[14:22] huge opportunity to discover something
[14:24] new."
[14:24] >> Yeah.
[14:25] Amazing attitude. Well, clearly we
[14:27] should ask him about what he's excited
[14:29] about right now [laughter] and feel that
[14:30] enthusiasm first hand. So, having laid
[14:33] that groundwork, let's talk to Paul
[14:34] Milgrom.
[14:35] I thought maybe we could start the
[14:36] conversation talking a bit about auction
[14:38] theory, which obviously has been a a
[14:39] really major theme throughout your
[14:41] career.
[14:41] >> Mhm.
[14:42] >> You know, and I think when a lot of
[14:43] people first encounter auctions, they
[14:44] think, "Oh, yeah, you know, this seems
[14:45] like a
[14:47] reasonable, practical problem and, you
[14:49] know, there's sort of nice solutions."
[14:51] And, you know,
[14:52] one thing I find fascinating is my
[14:54] understanding is your approach when you
[14:56] came to auction theory it was from
[14:58] sort of much deeper intellectual roots,
[15:00] coming from sort of general equilibrium
[15:01] theory and price theory. And that's a
[15:03] story I suspect a lot of our audience
[15:05] doesn't know. So, I wonder if you could
[15:06] start by, you know, just talking a bit
[15:08] about what brought you to auction
[15:09] theory, you know, in the late '70s and
[15:11] what were you trying to achieve in in
[15:13] doing it.
[15:14] >> [snorts]
[15:14] >> So,
[15:15] actually, if I go to what brought me to
[15:17] auction theory, it wasn't any deep
[15:19] intellectual thing like that. I was in
[15:22] an MBA program at Stanford and the
[15:24] faculty recruited me into the graduate
[15:26] program because of, you know, the way I
[15:29] was in class.
[15:30] And I was advised that I should get Bob
[15:33] Wilson to be my PhD advisor.
[15:36] And so I decided I would do that by, um,
[15:39] writing my term paper for his class
[15:40] about something that interested him. So
[15:42] I wrote a paper about auction theory. So
[15:45] it didn't have any deep intellectual
[15:46] roots,
[15:47] um,
[15:48] at the time.
[15:50] But, um, as I continued to take graduate
[15:52] classes at Stanford, the question about
[15:55] how prices emerged and why they had the
[15:58] properties they had, there was, um, at
[16:00] the time this, uh, very puzzling work by
[16:02] Grossman and Stiglitz
[16:04] which had said that people inferred
[16:07] information from prices, but how did the
[16:10] information get into prices before you
[16:12] transacted? And and they had these
[16:15] paradoxical looking results that made it
[16:18] seem that nobody had any incentive to
[16:20] gather information cuz the information
[16:22] was already in the prices, but if nobody
[16:24] gathered information, how did the
[16:25] information get into the prices? So
[16:28] looking at the process of price
[16:29] formation became important. And that led
[16:33] to the paper I did with Larry Glosten
[16:36] where, you know, there's there's a
[16:38] process by which prices are formed.
[16:40] There are bid and ask prices. After the
[16:42] transaction, they came to reveal the
[16:45] information that was used by the
[16:46] transacting party, but not before the
[16:48] transaction. Before the transaction, you
[16:50] didn't know whether the bid price or the
[16:52] ask price was going to apply and it was
[16:55] only after the transaction that you
[16:56] learned which applied and so the
[16:58] transactions prices reflected
[17:00] information. The consumer could then
[17:02] profit from, uh, this information. If
[17:04] the consumer didn't have information, it
[17:06] wouldn't be reflected in the
[17:08] transactions prices. So it was a logical
[17:10] way to account for, uh, these paradoxes
[17:13] of general equilibrium in financial
[17:14] markets.
[17:15] >> I'm glad you brought up the the with
[17:17] Larry Glosten cuz um it's interesting. I
[17:19] mean obviously So that's part of a
[17:21] literature called the market
[17:22] microstructure, which you know, is very
[17:24] famous in the economics and finance
[17:25] world, but actually with blockchain
[17:27] technology, one interesting thing that's
[17:29] happened is there's a new generation of
[17:31] sort of computer scientists and
[17:32] engineers that have now through
[17:34] decentralized finance gotten quite
[17:36] interested in the foundations there. And
[17:38] so I'm hearing about, you know, the
[17:40] Glosten-Milgrom paper now, you know, all
[17:41] the time from groups where historically
[17:43] I hadn't heard as much about it.
[17:45] >> So I'd love to just actually probe a
[17:46] little bit deeper there. Did that kind
[17:48] of come about sort of hand in hand with
[17:50] the work you were doing just in the more
[17:52] pure auction theory side, call it?
[17:54] >> And maybe for the audience just if you
[17:56] can quickly review what the paradox is
[17:58] and what your resolution is cuz it's a
[17:59] really slick and simple insight and I
[18:01] think a lot of people listening, you
[18:02] know, if they're thinking about
[18:03] prediction markets or decentralized
[18:05] finance or whatever, they may not
[18:06] actually know the sort of fundamental
[18:07] paradox yet.
[18:09] >> Well, the paradox has to do with the
[18:10] intellectual history of the way things
[18:12] were modeled. It's only a paradox when
[18:14] you're when you're married to old
[18:16] general equilibrium theory and and in
[18:18] old general equilibrium theory, what
[18:20] happens is people can't influence
[18:22] prices. They think oh, the markets are
[18:24] very big. Prices don't depend on what I
[18:26] do.
[18:27] And they think that prices reflect
[18:29] information.
[18:31] But how do prices come to reflect
[18:33] information if people can't affect them?
[18:36] That's the fundamental paradox. And it
[18:39] was reflected in formal modeling by
[18:42] Grossman and Stiglitz, which showed that
[18:45] if if you made these assumptions, you
[18:48] you could conclude that people had no
[18:51] incentive to gather information since
[18:53] their information was revealed in
[18:55] prices.
[18:57] But then if they didn't have an
[18:58] incentive to get information, how would
[19:00] the how would the prices be informative?
[19:02] That's a very paradoxical result that
[19:04] comes from a very strange modeling.
[19:07] And that sort of opened the door at that
[19:10] time the way the economist thought about
[19:13] prices as well, they didn't think about
[19:15] prices. They said, you know, there's
[19:17] supply and demand and the point where
[19:19] supply and demand crosses is what the
[19:20] price is and we don't talk about how the
[19:23] price emerges. And what option theory
[19:25] was doing and what Bob Wilson's program
[19:28] was was to say, no, actually there's a
[19:30] process behind all of this.
[19:33] And and we should look more deeply at
[19:35] the process.
[19:37] And what Larry and I did said, well, you
[19:39] know, at the time the way specialists
[19:42] ran markets is they quoted a bid price
[19:44] and an ask price.
[19:46] And it turned out in our model that a
[19:49] specialist didn't want to lose money.
[19:50] They knew that some traders were
[19:52] informed. So, they knew that if a trader
[19:54] was buying from them, that was some
[19:57] indication that that trader had positive
[19:59] information that prices should be
[20:01] higher. And they knew that if a trader
[20:03] was selling from them, that was some
[20:05] indication that the price was too high
[20:07] and prices should be lower. So, the bid
[20:10] price and the ask price were separated
[20:12] by this
[20:13] value of information difference.
[20:16] Prior to our work, people thought the
[20:18] difference between the bid price and ask
[20:19] price reflected some costs of inventory
[20:22] that that were being held
[20:25] by the market.
[20:26] >> know that.
[20:26] >> That's wild.
[20:27] >> Oh, yeah. And later on, the empirical
[20:29] work then looked to separate how much of
[20:31] the spread was due to information and
[20:34] how much might be due to some some costs
[20:37] of holding inventory. It turned out a
[20:39] big chunk of the difference really was
[20:41] due to information. That's what the
[20:43] empirical work wound up showing.
[20:46] So, it was a very simple and and it came
[20:49] out to be mathematically quite
[20:50] beautiful. The people in finance had
[20:53] this idea, roughly speaking, that prices
[20:56] formed a martingale. That is that the uh
[20:59] you wanted to predict the price tomorrow
[21:01] in expectation it was the price today.
[21:03] But this was in a model where there was
[21:05] only a single price. And we had a model
[21:08] which there's a bid price and the ask
[21:09] price, but the transaction price is
[21:11] formed a martingale anyway because if
[21:14] the guy bought, then the information
[21:18] that the guy was buying was already in
[21:20] the ask price, and so the the
[21:22] transaction price would reflect the
[21:24] information that actually came into into
[21:27] the market, and we got the martingale
[21:28] property back.
[21:30] Uh
[21:30] and some other uh things as well, things
[21:32] that talked about how markets break down
[21:34] when there's too much asymmetric
[21:36] information uh and a few other uh
[21:39] things.
[21:39] >> Fascinating.
[21:41] This is maybe a little bit of a
[21:42] digression, but let me ask you here
[21:44] anyway. So, anyone who reads papers in
[21:46] the top economics journals, you know, in
[21:48] the '60s, then '70s, then '80s, then
[21:50] '90s, and then into the 21st century, I
[21:52] think observes this evolution of
[21:54] becoming more quantitative, more
[21:57] mathematically rigorous, more precise,
[21:59] and and Paul, certainly, you know,
[22:00] throughout your entire career from the
[22:01] very beginning, I'd say precision and
[22:03] rigor is is there in every single paper
[22:05] that I've that, you know, that you've
[22:06] ever written. I was wondering if you
[22:08] could sort of place your early work in
[22:10] the context of that evolution. Uh like,
[22:12] take us back to, you know, how was, you
[22:15] know, more fine-grained mathematical
[22:16] modeling viewed at that point? Was that
[22:18] in and of itself something relatively
[22:20] new to the um economist profession?
[22:23] >> Well, I think, you know, actually, you
[22:25] can go back to the '50s and find
[22:27] certainly if you read Gerard Debreu's
[22:29] Theory of Value, it's very
[22:31] mathematically uh precise. He lays all
[22:34] the careful mathematical foundations and
[22:37] and seeks high levels of generality.
[22:40] You know, I think part of the reason
[22:42] when you're an economist, when you're
[22:44] looking at these things, sometimes when
[22:46] you're trying to illustrate in a model
[22:47] what's going on, you know that your
[22:49] model's a simplification.
[22:51] So, all you're really trying to
[22:53] illustrate is possibility. And when
[22:55] you're trying to illustrate possibility,
[22:57] you
[22:57] you don't seek maximum generality. It's
[23:01] not really so much as
[23:02] less mathematically uh mathematically
[23:05] rigorous as being less it's less
[23:07] general. That the people are making very
[23:10] specific assumptions which we don't
[23:12] expect to be true in the world in order
[23:14] to illustrate how some effect would
[23:16] emerge. Whereas if if you start
[23:18] following from Arrow and Debreu and
[23:20] those guys, they were looking for
[23:22] generality. They wanted to know
[23:25] how widely can we conclude that a
[23:27] general equilibrium exists or that
[23:30] general equilibrium is efficient or all
[23:32] the other
[23:34] kinds of properties. When you see it
[23:36] being more mathematical, I think part of
[23:38] what you're seeing is attempts at
[23:40] greater generality. And you can see why
[23:43] as we dig deeper into ideas you would
[23:46] seek
[23:47] you know, greater generality because we
[23:49] want to know, okay, how far can we push
[23:52] this idea? And and that's what I think
[23:55] came out more and more starting in the
[23:58] '70s and '80s and moving forward.
[24:00] >> How do you think about the use of math
[24:03] to help search for and understand ideas?
[24:06] Like you know, I've noticed in in
[24:07] working with you like your ability to
[24:09] see the generality is a huge part of
[24:12] what frames the economic sort of the
[24:14] economic space. How do you think about
[24:16] that?
[24:16] >> For me, um
[24:18] I I was always amazed that it worked
[24:20] this way when I got into economics.
[24:23] There was always this back and forth
[24:25] between the
[24:27] the verbal descriptions and the
[24:28] mathematics. That is I wanted to be able
[24:32] to explain what I was doing to say it
[24:35] in in terms of economic concepts.
[24:39] And often the math would teach me
[24:41] something and say, oh, this is the
[24:42] condition I needed for the result to be
[24:45] true. Here's a mathematical condition.
[24:47] What does it mean in the world?
[24:49] >> Let me bring it back to to auction
[24:51] theory for a minute. In particular, I I
[24:53] love to chat a little bit about the you
[24:55] know, famous 1982 paper with Weber.
[24:58] And I'd love to actually before you get
[25:00] into that and and just a little bit
[25:01] about sort of again setting the stage.
[25:03] And in particular, there was another
[25:05] extremely well-known paper that came out
[25:07] the year before by Roger Myerson on
[25:09] optimal auctions. And so I'd love to
[25:11] hear a little bit, you know, what was
[25:12] your reaction to that paper when it came
[25:13] out? And I would say they're very
[25:15] complimentary in my view at least the
[25:17] the Myerson and the Milgrom-Weber paper.
[25:18] So just a little bit about how those fit
[25:20] together.
[25:21] >> We were just sitting two doors apart at
[25:23] the time we were working on that paper.
[25:24] So the papers were growing,
[25:27] you know, more or less simultaneously.
[25:29] You know, Roger's inclusion of some
[25:31] common value was borrowed from the work
[25:34] that Bob Weber and I were doing.
[25:36] Roger was thinking quite orthogonally
[25:38] to, you know, what I was thinking about.
[25:39] Mechanism design was not a
[25:42] a typical way to approach things then.
[25:45] And
[25:46] I was trying to
[25:48] understand
[25:50] these two completely separate threads of
[25:52] auction theory, the one with the common
[25:54] value model that that Wilson had done a
[25:57] lot of work on, and the Vickrey model
[26:00] which was the independent private values
[26:02] model. And I wanted to unify them and
[26:05] see, you know,
[26:08] what could be said, whether Vickrey's
[26:10] results still applied in the unified
[26:11] model, and whether whether Bob's results
[26:15] could be extended. There was also again
[26:17] a mathematical detail that the
[26:20] mathematics, as you point out, was very
[26:21] important to me. I had an undergraduate
[26:23] math degree, and I knew what it meant to
[26:25] be careful. And
[26:28] the people were just writing down these
[26:30] first-order conditions and writing down
[26:32] what the solutions would look like, and
[26:34] I wanted to know whether these were
[26:35] actually equilibria. It turned out we
[26:37] needed affiliation for that. And then
[26:40] affiliation drove some of the other
[26:42] results as well.
[26:43] >> And that that same paper, in addition
[26:45] to, you know, this sort of
[26:46] generalization, you have independent
[26:48] values capturing the common value case
[26:49] and the independent private values case
[26:51] under sort of one general framework.
[26:54] Another big takeaway for me at least
[26:56] from that paper was
[26:57] this kind of relentless focus, you know,
[27:00] on the auction formats that we already
[27:02] know matter. So, rather than just sort
[27:04] of formulating an optimization problem
[27:06] and say, let's see what we get if we
[27:07] solve it, but really let's try to speak
[27:09] to people, you know, give guidance in
[27:11] effect. If someone actually has to make
[27:13] a decision in the real world about, you
[27:14] know, should they run an English auction
[27:16] or should they run a sealed bid auction?
[27:17] Like, what can we as analysts sort of
[27:19] tell them? So, I was curious, like, was
[27:21] that did you have sort of practice in
[27:23] mind, you know, in making those
[27:25] decisions in that paper?
[27:27] >> I didn't really. I mean, remember
[27:29] um I wasn't really making the choice
[27:31] that you've just described because
[27:32] mechanism design was not something we
[27:34] knew about at the time. Um
[27:37] it was totally shocking when Roger
[27:39] formulated
[27:41] the optimal auction principle, the
[27:43] revelation principle. There were
[27:45] versions of it around, but it certainly
[27:47] wasn't widely known at the time.
[27:49] And the idea that you could find an
[27:51] auction that was optimal among all
[27:53] possible mechanisms was was shocking to
[27:57] people. I remember I remember at the
[27:58] time um having a conversation with Sandy
[28:01] Grossman, who was very famous back then,
[28:03] describing that Roger had found an
[28:05] auction that was optimal among all
[28:07] auctions. And
[28:08] Sandy said, "Well, what do you mean all
[28:10] auctions?" I said, "All." I said, you
[28:11] know, he said, "Well, for example,
[28:13] suppose that I have five people and I uh
[28:17] collect bids from them and I take the
[28:19] first and third highest and then put
[28:21] them in a qualifying round or a random,
[28:23] you know, and and then I, you know, he
[28:25] went through a whole series of steps and
[28:27] says, "Does it include that?"
[28:29] I said, "Yes." Um
[28:32] >> [laughter]
[28:33] >> and he he just didn't believe it, right?
[28:35] So, no, I I was not choosing. I was sort
[28:37] of driven by what I understood at the
[28:39] time.
[28:40] >> Yes, maybe just for completeness for the
[28:42] audience, as far as the revelation
[28:43] principle, I would maybe describe it
[28:44] sort of fast forwarding to the
[28:46] equilibrium point. So, in some sense,
[28:48] for the purposes of identifying optimal
[28:50] auctions, really what matters is just
[28:52] sort of allocations and payments at
[28:54] equilibrium as a function of people's
[28:56] willingness to willingness to pay. But,
[28:58] what's what's sort of I think
[29:00] fascinating is Paul, we've also seen
[29:03] really interesting results much more
[29:04] recently last 5 or 10 years, including
[29:06] from your own students, about actually
[29:08] saying, "Well, wait a minute. Wait a
[29:09] minute. Maybe we lose a few things when
[29:11] we just think about the revelation
[29:12] version." Would you care to to you know,
[29:15] speak about the the sort of recent
[29:16] trends about
[29:17] really focusing squarely on indirect
[29:19] mechanisms and the properties you can
[29:20] only articulate at that point?
[29:22] >> I'll start with my own piece of that
[29:24] because it was while we were working on
[29:26] the broadcast incentive auction.
[29:28] >> Mhm.
[29:29] >> And Mohammad Akbarpour and Shengwu Li
[29:31] were both graduate students at Stanford.
[29:34] So, we had to create an auction that
[29:37] worked when checking the feasibility of
[29:39] an allocation was an NP-complete
[29:41] problem. Um so, it was it was hard. And
[29:45] we kept changing the algorithm as Kevin
[29:48] Leyton-Brown was was developing the
[29:49] algorithms uh that were getting better
[29:52] and better at solving a larger fraction
[29:54] of these in in a reasonable amount of
[29:56] time.
[29:57] And I had puzzled to my graduate
[30:00] students that we had always said in in
[30:03] economics that a mechanism is defined by
[30:06] its outcome function. And here we were
[30:08] changing the outcome function and yet um
[30:12] all of these things we knew even without
[30:14] looking even without knowing the outcome
[30:17] even without being able to compute even
[30:18] not without being able to describe the
[30:21] outcome function, we knew that these
[30:22] things were strategy-proof. In fact, it
[30:25] was just obvious that they were
[30:26] strategy-proof.
[30:28] And wasn't that weird? Okay. And Shengwu
[30:31] says that he listened and scratched his
[30:34] head and said, "What could obviously
[30:36] strategy-proof mean?" He was interested
[30:38] in that because he also did behavioral
[30:41] economics and knew that you could have
[30:44] an ascending auction and a strategically
[30:46] equivalent second price auction, and
[30:49] people would play the ascending auction
[30:52] more accurately. They'd be more likely
[30:54] to pick their dominant strategy. And,
[30:57] you know, it in some sense it was
[30:59] clearer to them what a dominant strategy
[31:01] was. So, so he brought in this this
[31:03] behavioral idea, and it turned out to be
[31:06] quite useful. How can we design auctions
[31:10] that are easy for people to bid
[31:13] accurately in,
[31:15] um, that have good properties, and that
[31:17] requires going beyond direct mechanisms.
[31:19] You have to take a look at all the
[31:21] details of how the mechanism works. So,
[31:23] it was pretty interesting.
[31:24] >> You've started alluding a little bit to
[31:25] this feedback between theory and
[31:27] practice and the layering of it, right?
[31:29] That there's a practical problem that
[31:30] then spawns new theory that then gives
[31:32] rise to new practical designs. It's been
[31:34] a huge theme throughout your career.
[31:36] Could you maybe talk us through what it
[31:38] again, what does it feel like? How does
[31:39] it come about? Do you seek it out? Does
[31:41] it find you?
[31:42] >> So, there are two things you're
[31:43] conflating there, I think. One is that I
[31:45] always thought that in writing theory
[31:47] there was always this this feedback
[31:49] between how you would express something.
[31:51] I was teaching myself. I mean, I have no
[31:53] degrees in economics.
[31:55] I I studied in the business school in
[31:57] what was called decision sciences, and I
[32:00] kept trying to explain things in terms
[32:03] that were familiar to economists. So,
[32:05] moving back and forth between the
[32:07] mathematics, what it said, and the
[32:09] economics. Sometimes the economics was
[32:11] more general. When I expressed it in the
[32:13] economic terms, it was more general than
[32:15] the mathematics I had. So, then I'd have
[32:17] to go back to the mathematics and say,
[32:19] "Can I generalize?" And sometimes the
[32:22] mathematics would express things in ways
[32:24] that were surprising to me, and I'd say,
[32:26] "How would I say that using economic
[32:28] concepts? Can I, or does it require new
[32:30] concepts?" So, there was this this
[32:32] feedback always going on between, uh,
[32:35] economic concepts and the mathematics.
[32:39] But, there's also a feedback, the one
[32:40] that that I think you're emphasizing,
[32:43] between theory and practice. And here it
[32:45] was really scary because the very first
[32:48] of my
[32:49] big practical applications, which was
[32:51] the original US spectrum auctions,
[32:54] Pacific Bell, which was the local, uh,
[32:57] telephone company in California back in
[32:59] the early 1990s,
[33:01] asked me to look at this proposal by the
[33:03] government. And I said, "Oh, I I could
[33:05] this is way too hard. This is, you know,
[33:07] for I'm just a theorist. I don't know
[33:09] how to how to do this kind of stuff."
[33:12] And Pacific Bell said, "Well, you know,
[33:14] would you please look at it for us?
[33:15] We'll pay you for your time.
[33:17] Just take a look at it and tell us what
[33:19] you think."
[33:20] So, I studied the proposal that came out
[33:23] of the Federal Communications
[33:24] Commission. And I said, you know, "It's
[33:26] a really hard problem and I don't know
[33:27] what the right thing to do is, but I can
[33:29] do better than that." Cuz what they had
[33:32] was just a mess and ignored, you know,
[33:34] some obvious problems.
[33:36] So, Bob Wilson and I, um, proposed the
[33:39] simultaneous multiple round auction,
[33:42] which ended up being adopted in the US
[33:44] and worldwide, certainly in all the
[33:46] English-speaking countries, but also,
[33:49] you know, also in Germany and Mexico
[33:51] and, you know, other countries as well.
[33:53] And it just took off and and it solved
[33:56] some of the problems.
[33:58] And I was very nervous when we first ran
[33:59] it because I knew how incomplete our
[34:01] analysis was. I had solved some of the
[34:04] problems, but I didn't really know how
[34:05] it would operate in in other respects.
[34:08] So, it was scary, but after that, lots
[34:10] of people came and started asking my
[34:12] advice.
[34:13] After the US, the first place was
[34:15] Australia that came next. And that's
[34:17] when I first became aware, by the way,
[34:19] of the computer science issues
[34:21] because the US had decided that it would
[34:23] break the country up in these pieces,
[34:26] you know, significant chunks of, uh, of
[34:29] geography and significant chunks of
[34:30] spectrum and sell those licenses. And
[34:33] people could decide what combinations of
[34:35] licenses they wanted to buy.
[34:37] One of the Australian regulators said to
[34:39] me, "It's as well, you know, if people
[34:41] are putting together their their own
[34:43] combinations, why would you start with
[34:46] something that big? Why don't we have
[34:48] these what they called postage stamp
[34:50] licenses, which would really small areas
[34:52] with really thin pieces of spectrum, and
[34:55] let them put it together any way they
[34:57] wanted? You know, any combination you
[34:59] want you could bid for." It was
[35:01] obviously an inherently combinatorial
[35:03] problem.
[35:04] And uh I was horrified by the idea that
[35:07] you would try to push the auction that
[35:09] far. Realized that told me how little I
[35:12] understood about how the auction
[35:14] actually worked and when it would work,
[35:16] and then inspired a lot of new work on
[35:18] on theory, but it came from, you know,
[35:20] for me it came from the regulator making
[35:23] a proposal that I knew wouldn't work,
[35:25] but I didn't know what to do about it,
[35:27] right?
[35:28] >> So, Pac Bell got you involved really
[35:29] just to sort of advise them potentially
[35:32] on bidding in this format, but then you
[35:34] said, "No, no, no, no. Let me
[35:36] let me zoom out and advise everybody how
[35:39] this auction should
[35:39] >> Oh, no, no, no, what happened? No, Pac
[35:41] [laughter] Bell, the the government had
[35:43] was deciding what rules to set up, and
[35:45] they had a proposal, and I can't even I
[35:47] could go back and try to tell you the
[35:49] proposal, but it was god-awful. It was
[35:51] really a terrible proposal.
[35:53] And I told Pac Bell, "Not only is it bad
[35:55] it's bad for the government and it's
[35:57] terrible for you because you're going to
[35:59] end up losing the auction to uh
[36:01] companies that want to buy a package of
[36:03] all of the spectrum in the country." And
[36:06] And I said, "You know, we can do better
[36:07] for the government and better for you."
[36:09] So, I ended up making seven trips to
[36:12] Washington, D.C. to talk to the Federal
[36:14] Communications Commission.
[36:16] And um
[36:17] when we did the simultaneous ascending
[36:20] auction, this all came This is something
[36:21] I'm proud of, so I'll tell you this this
[36:23] particular story.
[36:24] >> Absolutely. Absolutely.
[36:26] >> said, "Oh, that's way too complicated.
[36:28] You know, you should just do it like you
[36:30] were Sotheby's or Christie's or
[36:32] something and just sell these pieces one
[36:34] at a time in a particular order that
[36:37] they would work out from maybe what they
[36:38] thought was most valuable to least
[36:40] valuable, something like that." And this
[36:43] is back in 1993
[36:46] that I'm doing this or 1992 or three, I
[36:49] guess.
[36:50] And I said, "Well, it isn't that
[36:51] complicated.
[36:52] Uh and we took and I had my research
[36:55] assistant program these little We had
[36:56] these little 3 and 1/2-in discs. Do you
[36:58] remember those?"
[36:59] Um
[37:00] >> Mhm.
[37:00] >> So, we programmed a series of Excel
[37:02] spreadsheets.
[37:04] And one Excel spreadsheet was the
[37:06] spreadsheet on which you would submit
[37:07] your bid. And it would check whether
[37:10] your bid met the rules. And you'd put
[37:12] your disc in then and your bid could be
[37:14] uploaded by the FCC's Excel spreadsheet,
[37:17] which would then create a combined
[37:19] spreadsheet and then run around and then
[37:21] export the results back to an outcomes
[37:24] file. So, I had all this on a 3 and
[37:26] 1/2-in disc.
[37:28] And I went the last time I went to the
[37:30] FCC, I said, "You know, it isn't that
[37:31] hard. Here's how you could do it with
[37:33] linked Excel spreadsheets." And I just
[37:35] handed them the disc. And Evan Kwerel,
[37:38] who was the guy who was uh being relied
[37:41] on to do this at the FCC, took it home
[37:43] and ran it on his home computer and
[37:46] said, "Actually, it works, right? It
[37:47] must be possible to do this." And uh
[37:50] when the when the chairman of the FCC,
[37:53] Reed Hundt at the time, asked, you know,
[37:55] "You can do whatever you want." "Uh what
[37:57] would it be?"
[37:58] He said, "Well, this is the system we'd
[38:00] want to use."
[38:01] And the chairman said, "It's pretty
[38:03] innovative, though." Yeah, and the turn
[38:04] They said, "Well, I like being
[38:05] innovative." Uh Reed Hundt says, "So,
[38:07] let's do it." So, they adopted this
[38:10] system.
[38:12] And and it spread worldwide and, you
[38:14] know, Bob and I got famous for it. So,
[38:16] there we are.
[38:17] >> Yeah, I I I love this st- It's also just
[38:19] a great example of academic-government
[38:21] collaboration, right? Something that
[38:22] probably doesn't happen enough, but like
[38:24] that's one of the absolute you know,
[38:26] best ever examples of it.
[38:28] What finally convinced them? Like, did
[38:29] you Was it specific examples of how
[38:33] different parties would about the sort
[38:35] of low quality of an allocation you
[38:37] would expect to get from the say a
[38:38] serial sort of mechanism? I'm sure you
[38:41] had to pitch it a few times before they
[38:43] really
[38:44] before you could sell them on it.
[38:45] >> I did it and it wasn't just a matter of
[38:47] them believing or not believing. They
[38:50] hired uh Charlie Plott at Caltech to run
[38:53] some laboratory experiments to see if it
[38:56] would work. They ran some experiments
[38:58] with, you know, Caltech students and
[39:00] they also got me to make some changes to
[39:03] the the activity rule. They said, "Well,
[39:05] what if somebody wanted to screw this
[39:06] up? What's the worst case? How long
[39:08] could it take?" So, the activity rule
[39:10] was to put a floor under how much
[39:12] bidding people could do so that the
[39:15] thing would converge in reasonable time
[39:16] in worst case. The Caltech experiments
[39:19] confirmed our predictions about the what
[39:22] what would go wrong with the alternative
[39:24] uh proposals that were made at the time.
[39:27] So, uh all that went favorably and then
[39:30] they hired somebody to implement that
[39:32] who was incompetent. Um They had
[39:34] software that nobody was sure would
[39:36] work, but they were running it in a very
[39:38] small auction where that the initial
[39:40] task
[39:41] was seven licenses for paging spectrum.
[39:45] And uh nobody was sure it would work and
[39:48] so they set up a a room where there was
[39:51] a blackboard and they were going to If
[39:54] the software didn't work, they were
[39:55] going to run it by by hand. Then it was
[39:58] uh Meanwhile, you know, my reputation
[40:00] was at stake, right? Was this thing too
[40:02] complicated? Could you actually do it?
[40:05] But it worked like a charm and the
[40:06] auction won. We got arbitrage between
[40:09] licenses that were essentially
[40:11] identical, which is what we wanted to
[40:13] get. They all end up selling for exactly
[40:15] the same price. Everything came out in a
[40:18] perfectly reasonable way and they
[40:20] decided, yep, it worked in the lab, it
[40:22] worked according to these theorists, it
[40:24] worked in the first test which was
[40:27] so-called small-scale test only like
[40:29] what was it? A hundred million dollars
[40:31] was our small-scale test remember.
[40:35] The auction four which is what we were
[40:36] really designing for was seven billion
[40:39] dollars. I mean it was a lot bigger. Um
[40:42] So it was a lot of money at stake.
[40:44] Someone got I was fine.
[40:46] I uh
[40:47] I was excited by the whole thing.
[40:51] >> Amazing. So that that's not the end of
[40:53] the story um with your work of spectrum
[40:55] auctions and I do want to you alluded
[40:57] before to the FCC incentive auction from
[40:59] uh I don't know 7-8 years ago. We'll get
[41:00] back to that. So then between these
[41:02] different chapters of of of your
[41:04] spectrum auctions work something
[41:05] interesting happened which was the rise
[41:07] of the internet and of the web and of
[41:09] sort of the digital economy. And so you
[41:11] know, something that we witnessed at
[41:13] that time was auctions going digital and
[41:16] all of a sudden it actually having
[41:18] billions of auctions run every single
[41:20] day. And you had you know, systems like
[41:22] Facebook literally implementing the
[41:24] Vickrey-Clarke-Groves mechanism under
[41:26] the hood. And so I'm just curious, you
[41:27] know, your reflections on that time and
[41:30] um any personal stories you have about
[41:32] how auctions going digital kind of
[41:33] changed
[41:34] how you thought about auction design.
[41:37] >> Well, first of all about Facebook, um
[41:38] that was John Hegeman who was the
[41:40] student in the first undergraduate
[41:42] market design class that I taught. I
[41:45] taught him the Vickrey-Clarke-Groves
[41:46] mechanism.
[41:47] >> Wow.
[41:47] >> And uh John was a terrific student and
[41:51] he entered the graduate program in
[41:53] economics at Stanford and Facebook lured
[41:56] him out of the graduate program to go
[41:58] take over uh that stuff. So I was uh uh
[42:01] a little disappointed to see him leave.
[42:03] And you know, of course we all know
[42:05] about the uh Google's misunderstanding
[42:08] of the second price auction and their
[42:10] generalized second price auction for uh
[42:13] for search advertising.
[42:15] It was all very exciting. And several of
[42:17] my students ended up getting involved.
[42:19] Another one of my students ended up
[42:21] going to Yahoo where they were saying,
[42:23] "Suppose you did search advertising, but
[42:25] the ads aren't all the same size. So,
[42:27] how many ads you can fit on the page
[42:29] depends which kinds of ads you have."
[42:31] So, that was a combinatorial auction cuz
[42:33] you could have different combinations
[42:35] depending on what size ad and then you
[42:37] had bidders who were uh okay, well, in
[42:40] that case, how do they describe their
[42:42] values? How do they compare the values
[42:44] for four-line ad versus a five-line ad?
[42:47] And Google did some, you know, brilliant
[42:50] simplifications. One of the ideas
[42:52] that struck me back then was simplifying
[42:56] the communications. You were paying per
[42:58] click on search advertising and and uh
[43:02] actually a double click as as of 1996, I
[43:05] think it was was already uh uh on a
[43:08] pay-per-click system
[43:10] for uh for advertisers. They had Google
[43:13] running the auction. They were
[43:13] predicting uh click-through rates.
[43:16] So, just making one value per click and
[43:20] predicting click-through rates and
[43:22] running a position auction where you
[43:24] would expect to get fewer clicks. They
[43:26] had a simplified model where the number
[43:28] of clicks that you'd expect to get maybe
[43:31] falls 30% or so with each position you
[43:33] move down the page. They had some uh
[43:36] simplified model that made the reporting
[43:39] very simple.
[43:40] And then I remember having the
[43:42] discussion with Preston McAfee where you
[43:45] know, we started understanding that
[43:47] bidders had different objectives.
[43:49] But they don't all have to use the same
[43:51] language. We could have them describe
[43:54] their objective in different languages.
[43:56] And we were already seeing that that
[43:59] Google was converting cost-per-click
[44:02] information into cost-per-impression
[44:04] information in order to run an auction
[44:07] for uh
[44:08] for advertising slots, you didn't have
[44:10] to be speaking the language of the bids
[44:13] to communicate values, and keeping it
[44:15] simple was important, and that carried
[44:18] over into what we were doing in the
[44:19] incentive auction, too, where I was also
[44:22] very eager to make it easy because, you
[44:26] know, if you're a practical person, one
[44:29] of the early lessons you learn is that
[44:31] perhaps the most important thing you can
[44:33] do in auctions is encourage
[44:35] participation. You need the bidders to
[44:37] come to get a good outcome.
[44:40] And
[44:41] if you make it too complicated they
[44:44] don't show up, right? They just don't
[44:46] participate. They don't know what to do.
[44:48] So, simplicity was also important. All
[44:50] those things were
[44:52] you know, as a practical person, were
[44:54] coming on my together.
[44:56] >> That's so fantastic. So, moving on to
[44:58] the FCC incentive auction, which took
[45:00] place over 2017 and 2018. So,
[45:03] you know, so early '90s was when the
[45:05] spectrum auction work started. This was,
[45:07] you know, now really almost 25 years
[45:09] later, you sort of overseen and
[45:12] innovated many times in that interim.
[45:15] But, definitely there is something
[45:16] very new
[45:18] in the FCC incentive auction. So, maybe
[45:19] you could start just by saying, you
[45:21] know, why was the level of innovation
[45:23] required fundamentally greater than
[45:25] anything since 1993?
[45:28] >> Well, there were two main reasons. The
[45:30] FCC incentive auction was
[45:33] completely different animal from what
[45:35] we'd done before. In all of the auctions
[45:38] until then, as technology advanced, new
[45:42] frequencies which had been unused
[45:45] were being made available for new uses,
[45:48] and the government was selling rights to
[45:50] use frequencies that it controlled.
[45:53] Um before the incentive auction, maybe
[45:55] around 2010 or so on, all the
[45:58] frequencies that were useful with the
[46:00] new technologies had been used up. The
[46:02] reason you couldn't use a higher
[46:05] frequencies for some of the uses was not
[46:08] that you couldn't encode signals on
[46:10] them, but the higher frequencies might
[46:12] not penetrate brick walls or
[46:14] into glass and steel buildings. You
[46:17] know, you could send signals on them,
[46:18] but the signals wouldn't reach the users
[46:20] anymore. So, we were out of the most
[46:23] valuable frequencies at that time. What
[46:27] was required was a reallocation.
[46:30] You needed somebody who already had
[46:32] rights. In this case, it was television
[46:34] broadcasters
[46:35] to give up their rights to use
[46:37] frequencies, and then you needed to
[46:39] reconfigure them. By the way, we won an
[46:42] Emmy award for this, you may know that.
[46:44] I have uh
[46:45] >> I was about to say, I heard you won an
[46:46] Emmy, like, you know.
[46:48] >> I have this little Emmy statuette. Uh it
[46:50] was to auction off the mix that we were
[46:52] a winner
[46:53] of the technical Emmy.
[46:55] Um
[46:56] for reorganizing the television
[46:58] industry. So, what was going on
[47:00] at that time was fewer and fewer people
[47:02] were watching live broadcast television
[47:05] over the air. More was over the
[47:06] internet, satellites, cable. That's how
[47:09] people were seeing their shows. And um
[47:13] so, the value of radio of the spectrum
[47:17] for over the air broadcast had declined.
[47:20] In addition, they were coding more
[47:22] efficiently, so the old analog 6 MHz
[47:24] blocks were more than you needed to code
[47:27] a high-definition signal in the digital
[47:30] format. So, the value had fallen in in
[47:32] over the air broadcast, but for wireless
[47:35] broadband, it was growing demand. This
[47:38] was much more intensive use of wireless
[47:40] data, including video over the internet
[47:42] was coming along.
[47:44] So, we needed a reallocation.
[47:47] And the old licenses couldn't just be
[47:50] turned over. If if Scott over here had a
[47:53] television license to serve Chicago for
[47:56] 6 MHz, you couldn't put a wireless data
[48:00] plan on that. It's very much like zoning
[48:03] and and and which you can think of of
[48:05] zoning real estate uses. You don't want
[48:08] to have a factory sitting next to a
[48:10] house. Doesn't work very well for a lot
[48:12] of reasons. If your television station
[48:14] was broadcasting from the top of the
[48:17] Sears Tower in Chicago, it would send a
[48:19] signal that could be seen for 200 miles.
[48:22] Right around the top of the Sears Tower
[48:24] would be a very strong signal, but at
[48:26] the edges it would be a very weak
[48:28] signal. If you had an adjacent
[48:31] phone that was using adjacent
[48:34] frequencies that was near the Sears
[48:36] Tower, it would be like somebody
[48:38] shouting very loud next to you. Nobody
[48:40] could see the signal. If you had the
[48:42] phone out at the 200-mile limit, then
[48:46] your telephone would block out the
[48:47] television signal. These things just
[48:50] don't go next to each other. So, the
[48:52] sizes of the power that was used and the
[48:55] power limitations, the sizes of the
[48:57] areas that were being served were very
[48:59] different for data and for television.
[49:03] So, the upshot of all of that was that
[49:05] what we wanted to do was to clear a
[49:07] bunch of frequencies. We ended up
[49:08] clearing channels 38 to 51 of all
[49:11] television broadcast and then reusing re
[49:15] rejunking up that spectrum in a way that
[49:18] made sense for wireless data. And then,
[49:21] if you had a television broadcaster who
[49:23] was previously broadcasting on let's say
[49:25] channel 42 and didn't want to go off the
[49:28] air, you might move him to, you know,
[49:30] channel 32. But, you had to do that in a
[49:33] way that didn't interfere with other
[49:36] television broadcast.
[49:38] So, it was a reallocation, and this is
[49:41] the first hard problem, how to do the
[49:43] reallocation. I guess I can describe for
[49:46] you roughly speaking, it's a graph
[49:48] coloring problem, and I'll I'll
[49:50] why.
[49:51] >> Actually, right before you do that, let
[49:52] me quickly flag this is a great
[49:54] illustration of why market design is
[49:56] necessary, right? Like here we have a
[49:57] setting where some level of like
[50:00] first-order, you know, you talked at the
[50:01] beginning about general equilibrium.
[50:02] It's like, "Oh, there's some stations
[50:04] that have licenses. It's not the optimal
[50:06] allocation of the license relative to
[50:08] new wireless applications." Like sort of
[50:10] a naive answer would say like, "Okay,
[50:12] let the market trade." But here, you
[50:14] know, you've already given us
[50:15] constraints that tell us that that's not
[50:17] quite something a market can do easily
[50:20] on its own. Now you're going to tell us
[50:21] that it's going to involve solving an
[50:22] NPR problem.
[50:23] >> Yes, [laughter] right. That's right.
[50:25] >> Actually, if I can piggyback on what
[50:26] what Scott said, because again, like,
[50:28] you know, if you just read auction
[50:29] theory papers, it's like, "Oh, there's
[50:30] some number of items for sale or to
[50:33] procure." Right? And you don't really
[50:35] think about like what that might mean or
[50:36] even like one thing that's amazing about
[50:38] this story is I feel like a huge part of
[50:40] the problem that you solved was even
[50:42] identifying what is being procured,
[50:45] right? So,
[50:46] you know, if a television broadcaster
[50:47] holds a license and is broadcasting on
[50:49] channel 46, you might think that their
[50:51] license gives them the right to be
[50:53] broadcasting in that area on channel 46.
[50:56] But for you to even get started, right,
[50:58] you had to actually clarify what the
[51:01] property rights of those licenses were.
[51:02] Is that right?
[51:03] >> That is absolutely right. By the way,
[51:05] Evan Kwerel at the FCC, the same guy who
[51:08] I worked with in 1993, deserves a lot of
[51:10] credit for this because he understood
[51:13] that if you had to acquire specific
[51:15] licenses, you'd have little local
[51:17] monopolists everywhere. If if all you
[51:20] need to acquire is a certain amount of
[51:23] spectrum in an area, and then you can
[51:26] move everybody into whatever remains,
[51:29] then you could get competition going.
[51:30] So, that was understood by a couple guys
[51:33] at the FCC, and they encouraged Congress
[51:35] to write the law that way. But there was
[51:36] even more that was related to that
[51:38] because
[51:40] when we first started on this problem,
[51:42] it wasn't clear that you wanted to buy
[51:45] and hold television stations. It might
[51:47] be that well, there was a little bit of
[51:50] interference that would be created and
[51:52] maybe I could buy the right to interfere
[51:54] with 5% of your customers. Deciding what
[51:57] the product was was a big deal and we
[52:00] spent a lot of time on that. We decided
[52:01] that that was
[52:03] would be more complicated for the
[52:04] bidders and computationally much harder.
[52:07] The data that was required was also very
[52:09] different. The way we decided what was
[52:11] feasible was as follows. One of the very
[52:13] first steps was a an interference study
[52:16] where the FCC knew where the 2200
[52:19] television stations were in the US and
[52:22] Canada that would be engaged in all of
[52:24] this. And the combination of measurement
[52:27] and modeling worked out their signal
[52:30] strength that pixelated the US into
[52:33] large number of pixels that were 1 km
[52:36] square, looked at the signal strength at
[52:38] the center of each of these pixels,
[52:41] determined whether there'd be
[52:42] interference between two television who
[52:45] was currently serving that area and
[52:46] would there be interference. The
[52:48] eventual way it was done was was this.
[52:52] They would round to whole numbers of
[52:53] percent. So, if you interfered with 0.4%
[52:58] of my customers, that was zero. The
[53:00] criterion was that I couldn't assign two
[53:03] stations to the same channel
[53:06] if they would interfere with any,
[53:10] meaning more than zero, of the which
[53:12] means more than 0.5% really, of the
[53:16] customers.
[53:17] And you know, in in the original thing
[53:19] when we were thinking about total
[53:20] interference, we had a Venn diagram
[53:22] where well, what if two stations
[53:24] interfered with the same area and
[53:26] looking at the sum of the interferences,
[53:28] but this was really computationally
[53:31] simpler because we would just say you
[53:34] either interfere or you don't. So, now
[53:36] we have a graph coloring problem. Here's
[53:38] the problem. Each TV station represents
[53:41] a node in a graph
[53:43] and you draw an edge connecting two
[53:45] stations if they can't both be assigned
[53:48] to the same channel without creating
[53:50] interference.
[53:52] And now you're going to assign a channel
[53:54] to each station or a color to each node,
[53:57] if you will, so that no two connected
[53:59] nodes are the same color, so that no two
[54:01] connected stations are on the same
[54:03] channel.
[54:04] And uh, we have a given set of channels
[54:07] and given some set of stations, you can
[54:10] be asked, is it possible to assign
[54:13] channels to the stations so that there's
[54:15] no interference? And that was going to
[54:17] be the legal requirement that we had to
[54:19] meet with. So, when we were looking at
[54:21] which sets of stations that we could
[54:24] buy, in the end the the auction in
[54:26] effect had considered about 10,000
[54:28] different combinations of stations. And
[54:31] for each of them we had to solve this
[54:34] essentially graph coloring problem to
[54:36] determine is it possible to assign
[54:39] assign um,
[54:41] channels to the stations without
[54:43] creating interference. So, the first and
[54:45] probably biggest challenge was um, how
[54:49] do we do this because as you know, graph
[54:52] coloring, this is an NP-complete
[54:54] problem. There are no algorithms
[54:57] that at the scale we are working would
[55:00] solve this, if I understand correctly
[55:02] formulated that way was something like
[55:04] 130,000 constraints. Uh, which is too
[55:07] big a number to stick it in an exponent
[55:09] of the uh,
[55:10] you know, so anyway,
[55:12] >> Little bit. Little bit too big. Little
[55:13] bit too big, yeah.
[55:15] >> Exactly. [laughter] Like
[55:17] By by a few zeros, yeah.
[55:20] >> So, we weren't going to be able to solve
[55:22] all of these problems, but I became
[55:24] convinced from Kevin's early work that
[55:27] he was going to be able to solve them
[55:29] well and that we could design an auction
[55:33] in which we could assume that 99% of the
[55:36] problems we would we would be able to
[55:38] answer. Um 1% we wouldn't be able to you
[55:41] know, the computer would time out.
[55:43] That's what we were hoping for and
[55:45] that's pretty much what Kevin achieved
[55:46] with the uh software they developed. So
[55:49] then we needed an auction that worked in
[55:51] that setting where the computer might
[55:53] sometimes be unable to solve the
[55:55] problem, you know, so there was a little
[55:57] bit of that. Then the other big problem
[56:00] is that this was a two-sided auction. We
[56:02] didn't have money allocated by Congress
[56:04] to buy these stations. We had to then
[56:07] sell wireless broadband licenses that
[56:10] would raise enough revenue
[56:12] to cover the cost of buying the stations
[56:14] plus the stations that were moved, we
[56:16] had to cover the retuning costs.
[56:18] There were uh certain other costs that
[56:20] we had to cover.
[56:21] So it was going to be about $7 billion
[56:23] worth of costs and and we needed the
[56:26] revenues from the uh sale would exceed
[56:30] the costs of the purchase. So we needed
[56:33] two linked auctions where the whole
[56:35] process would be budget balanced as well
[56:37] and that was also novel. You know, no
[56:40] way of knowing what what these things
[56:41] were going to cost, what the revenues
[56:43] would come in. Computations were
[56:45] incredibly hard. One of the premises
[56:47] that I used in in um guiding the design
[56:51] is that we didn't expect to be able to
[56:54] buy a large number of CBS affiliates,
[56:57] for example. We thought that, you know,
[56:59] the mom and pop stations, your your
[57:01] grandfather founded a a channel in
[57:05] Topeka, Kansas in 1958
[57:08] and um
[57:09] that those were the guys who were going
[57:10] to have the low-value uh stations that
[57:13] were going to be willing to sell. So we
[57:15] needed those guys to participate. So the
[57:17] auction had to be simple enough.
[57:19] You know, here we're doing these
[57:20] horrendously complicated calculations
[57:22] and the auction had to look simple to
[57:24] the participants. So that was a
[57:26] challenge, right? And and so we settled
[57:29] on this this clock auction. If you're a
[57:32] participant, here's how it looks to you.
[57:34] You, Tim, by the way, have looked at
[57:36] your station and done some evaluation.
[57:38] You figure it's worth around $12
[57:40] million. And I say, "Tim, um And I say,
[57:42] "Tim, um it's first round of the
[57:44] auction.
[57:45] We might be willing to pay you as much
[57:47] as $100 million for your station. Would
[57:49] you accept it?"
[57:50] >> I think I know the answer to this one. I
[57:51] know the answer. So
[57:53] >> [laughter]
[57:53] >> Very good. The idea was to make it
[57:55] obvious, right? So you would say, "You
[57:58] know, and and we say you can say yes or
[58:00] no."
[58:01] And here are the cuts. Here are the
[58:02] rules.
[58:03] If you say no,
[58:05] you're out and you don't sell your
[58:06] station and that's fine.
[58:08] If you say yes and we offer you this
[58:10] $100 million, you have to sell.
[58:13] Then I go around and say, "Tim, you
[58:14] know, I I've looked and you know, Scott
[58:16] is in your area. He's also willing to
[58:18] sell and you know, I got a bunch of
[58:19] people who are happy to sell at my
[58:21] opening offer. So I'm only going to
[58:23] offer you the most I'm going to offer
[58:25] you is $95 million.
[58:28] Would you still be willing to sell?" And
[58:29] you can say yes or no. And if you know,
[58:31] you're out. If you say yes, we might
[58:33] offer you $95 million or you
[58:35] you know, or or we might come back to
[58:37] you with a lower offer. So those are the
[58:38] rules.
[58:40] And the idea is for you, it's really
[58:42] easy. I'm offered $100 million, $95
[58:44] million. Well, you know what your answer
[58:46] is. If I offer you less than your $12
[58:48] million, you know what your answer is to
[58:49] to that, too. So this was an auction
[58:53] that as Shen Wu would have us say now,
[58:56] was obviously strategy proof. That is
[58:58] the choices you make are obvious at
[59:00] every point in time.
[59:02] And that's written down in a technical
[59:04] way that defines obviousness, but it's
[59:06] clear I think to your listeners why the
[59:09] these choices were were obvious.
[59:12] And the way the auction proceeded on the
[59:14] reverse auction side, let's fix for a
[59:17] moment the amount of spectrum we're
[59:19] trying to clear. What we do is we say,
[59:22] "Okay, we we're going to have a certain
[59:25] a of channels that we're going to use
[59:26] for broadcast television.
[59:28] Then when I go to Tim, I I ask myself,
[59:31] "Hmm, given the promises that I've
[59:33] already made to Scott and others, um
[59:36] is it possible that if Tim says no, I
[59:38] have to give him a channel?" Is it
[59:40] possible that I can give him a channel?
[59:42] That involves solving this graph
[59:43] coloring problem to figure out whether
[59:45] it's possible.
[59:47] And um
[59:48] if the answer is no,
[59:50] then I say, "Okay, Tim, I offer you $95
[59:53] million and that's what you're getting,
[59:55] $95 million. But if I have room for your
[59:58] station, then I'll say, 'No, I'm going
[01:00:00] to actually offer you $90 million now
[01:00:02] cuz you say no, I do have somewhere to
[01:00:05] put you.'"
[01:00:06] So that's how the uh reverse auction
[01:00:08] worked with the fixed set of channels.
[01:00:11] But then we didn't know how many
[01:00:12] channels we were going to have because
[01:00:14] how many channels we could afford to
[01:00:15] clear depended on the revenue we would
[01:00:18] raise in the forward auction, the
[01:00:20] auction where people are buying.
[01:00:22] So we had this back and forth where we
[01:00:24] would lower prices to a certain point.
[01:00:27] We didn't actually say to you when the
[01:00:29] price got to 90 million that we were
[01:00:30] going to buy your station at 90 million.
[01:00:33] We're we're just not lowering your offer
[01:00:35] yet. Um and now if we raised enough
[01:00:37] money to pay all these things, then we
[01:00:40] would offer you the 90 million. But if
[01:00:42] we didn't raise enough money, then we'd
[01:00:44] say, "Okay, well, we can't afford to
[01:00:45] clear that many channels. So we now have
[01:00:48] more channels that are available and now
[01:00:50] there's room to place you. So now we'll
[01:00:53] offer you we'll lower your price to 85
[01:00:55] million." So from your point of view,
[01:00:56] the price can only go down from round to
[01:00:58] round. And the whole process is designed
[01:01:02] so that the number of channels we're
[01:01:04] trying to clear um can only go down
[01:01:07] during the course of the auction. And
[01:01:09] that means for the bidders in the
[01:01:10] forward auction, if they're selling some
[01:01:13] amount of spectrum and we decide we
[01:01:16] don't have that many channels to give to
[01:01:18] those guys anymore, we reduce the number
[01:01:20] of channels and we say, "Well, we've got
[01:01:22] some more competition in the auction now
[01:01:24] because we're not going to sell as many
[01:01:26] channels, so the prices per unit go up
[01:01:29] in the forward auction and they go down
[01:01:31] in the reverse auction until we reach a
[01:01:33] point
[01:01:34] where
[01:01:35] there is enough revenue
[01:01:37] from the forward auction to cover what
[01:01:41] we need to pay as a result of the
[01:01:42] reverse auction and then the auction
[01:01:45] ends. And And anyway, that was the
[01:01:46] design. It turned out that the bidders
[01:01:49] did consider it easy.
[01:01:51] And I've got some more stories to tell
[01:01:53] you. Can I tell you some more stories?
[01:01:55] Because
[01:01:55] >> Always.
[01:01:56] >> Absolutely.
[01:01:56] >> Because this this is coming up these
[01:01:58] days for the next applications. We were
[01:02:00] told, "Look, you're going to have a
[01:02:02] really hard time getting
[01:02:04] to participate." I mean, think about the
[01:02:06] spectrum out there. You know, we got
[01:02:08] these religious broadcasters. They're
[01:02:10] not-for-profit broadcasters. They have a
[01:02:12] mission and they're not going to sell
[01:02:14] their stations. We've got public
[01:02:16] television stations like here in the Bay
[01:02:18] Area, KQED. And, you know, they're
[01:02:21] not-for-profit.
[01:02:22] They are
[01:02:23] >> Excellent choice of call sign.
[01:02:25] >> Excellent choice of call sign, KQED. I
[01:02:27] somehow never even realized that, even
[01:02:29] though I grew up in the Bay Area with
[01:02:31] that station. Wow.
[01:02:33] >> I hadn't realized that either. There we
[01:02:35] go. It's God's station.
[01:02:37] After the deity. [laughter]
[01:02:39] Amazing over there.
[01:02:40] >> Amazing.
[01:02:41] >> It's God's station, absolutely. So, KQED
[01:02:44] had You know, they're never going to
[01:02:46] sell their stations, we were told. Well,
[01:02:48] haha. But, it turns out KQED had three
[01:02:53] broadcast stations and it was using
[01:02:55] rather old technology and it discovered
[01:02:58] that by upgrading its technology, it
[01:03:01] could serve its entire population using
[01:03:03] two of the stations and it sold the
[01:03:06] third one for $95 million,
[01:03:08] which he added nicely to its endowment.
[01:03:11] And the highest-paid station in the
[01:03:14] auction was a religious broadcaster in
[01:03:16] Chicago that got half a billion dollars
[01:03:19] approximately for its station said it
[01:03:22] could save a lot of souls
[01:03:24] for a half a billion dollars. And
[01:03:26] besides getting cash, it also got a VHF
[01:03:30] station which the broadcast quality
[01:03:32] isn't quite as good.
[01:03:34] But it stayed on the air with a VHF over
[01:03:37] the air station plus a half a billion
[01:03:39] dollars. Decided that was a good deal
[01:03:41] even though it was a religious
[01:03:42] broadcaster.
[01:03:44] So um
[01:03:45] you know, money talks. These are big
[01:03:47] sums. And we were able to, you know,
[01:03:50] clear 70 megahertz of spectrum this way
[01:03:52] which is a lot for, you know, modern
[01:03:54] data services.
[01:03:56] >> And in fact many of our listeners are
[01:03:57] literally using the spectrum you
[01:03:59] >> I was about to say that literally like
[01:04:01] on their phones or whatever to listen to
[01:04:02] this podcast.
[01:04:04] >> Yeah.
[01:04:04] >> Let me add a quick footnote in there cuz
[01:04:06] there's a there's a little it's not
[01:04:08] slight of hand because you declared it
[01:04:09] but but the trick of how you managed to
[01:04:13] get a form of price discovery with these
[01:04:15] interference in the background is really
[01:04:17] subtle and clever. So I just want to
[01:04:18] like make sure that we highlight it.
[01:04:19] Like as you said you're going to lower
[01:04:21] the price when you have an opportunity
[01:04:24] to repack a given station. But if you
[01:04:27] can't find a repacking then then you
[01:04:30] don't. And that could be because you
[01:04:32] know, the graph coloring problem has no
[01:04:33] solution or just because the the the
[01:04:35] algorithms can't find it quickly enough.
[01:04:37] >> Right.
[01:04:38] >> And so you're discovering prices
[01:04:41] accurately in a sense except you know,
[01:04:43] up to the small failure rate of the
[01:04:45] ability to find the colorings. And so
[01:04:47] everything if I understand correctly
[01:04:49] then everything actually like comes down
[01:04:51] to the better you can make that sort of
[01:04:53] interference constraint solver the the
[01:04:56] more accurately the market can clear.
[01:04:58] >> I've heard Kevin say that there may
[01:05:00] never have been a more direct
[01:05:01] relationship between the speed of an
[01:05:03] algorithm and that's like piles of cash.
[01:05:05] Right? Because
[01:05:07] if it times out it's literally making a
[01:05:09] higher offer perhaps than you strictly
[01:05:11] needed to
[01:05:12] >> Millions of dollars higher if it times
[01:05:13] out. That's right. It times
[01:05:16] It times out when the answer would have
[01:05:18] been yes. He figures that he saved a
[01:05:20] couple of billion dollars for the
[01:05:22] government. But they you you don't have
[01:05:24] it quite right. Um
[01:05:25] >> Okay, good. Correct. Correct.
[01:05:27] >> There's several things I want to say at
[01:05:28] this point. One is First of all, this
[01:05:30] algorithm, if you think about it for a
[01:05:32] while, is a greedy algorithm. What we're
[01:05:34] actually doing is we're putting stations
[01:05:39] on the air which have the one by one
[01:05:42] which have the highest values, roughly
[01:05:44] speaking. And as long as there's room to
[01:05:46] put them. And if there's not room to put
[01:05:48] them, then we find somebody else that,
[01:05:50] you know, to put in those stations. So,
[01:05:52] it's a greedy algorithm. And it's a
[01:05:54] greedy algorithm it we're we're solving
[01:05:57] an NP-hard problem. The actual problem
[01:05:59] of optimizing the value of the stations
[01:06:02] is one near. So, so even if we could
[01:06:05] solve all of these questions, all these
[01:06:07] things perfectly, we still don't expect
[01:06:09] to achieve the optimum.
[01:06:12] And we did a bunch of simulations to see
[01:06:14] how good it was. It's pretty good,
[01:06:15] actually. But the uh
[01:06:17] But you know, it could have been better.
[01:06:18] We did some work afterwards where we
[01:06:20] discovered
[01:06:21] ways we could have done that better. And
[01:06:23] the other thing I wanted to do because I
[01:06:25] I told you I gave you those examples for
[01:06:27] a reason.
[01:06:28] So, we were looking at other repurchase
[01:06:31] sorts of auctions, auctions where you're
[01:06:33] repurchasing the existing rights. So,
[01:06:36] right now, one of my former students
[01:06:39] is uh looking at repurchasing water
[01:06:42] rights around the Great Salt Lake, which
[01:06:44] is drying up because too much of the
[01:06:46] stream flow is being taken. There's an
[01:06:48] environmental disaster pending in the
[01:06:50] Great Salt Lake unless they can reduce
[01:06:52] the water use by local farmers. That
[01:06:55] also has some complexities associated
[01:06:57] with it. But the people there say the
[01:07:00] auction's too complicated. Farmers don't
[01:07:02] want to bid in an auction. They won't
[01:07:05] participate.
[01:07:06] And these stories that I have from the
[01:07:09] FCC, I think are really quite helpful in
[01:07:12] a setting like that. You know, you don't
[01:07:14] know who's going to participate. Money
[01:07:16] talks. We'll start out with a high price
[01:07:18] and we'll pay whatever we have to and
[01:07:20] guess what? There're going to be people
[01:07:21] who participate. So, we're we're hoping
[01:07:23] to be able to take variations
[01:07:26] of what we did and put them to other
[01:07:29] uses.
[01:07:30] >> As part of this, you touched on
[01:07:32] um how
[01:07:33] you couldn't be a a mere economist to uh
[01:07:37] design the FCC incentive auction. There
[01:07:39] was no choice but to sort of grapple
[01:07:40] with the computational intractability
[01:07:42] that was inherent Yeah. Um both in the
[01:07:45] repacking problem and then as you say,
[01:07:46] even given a perfect oracle for the
[01:07:48] repacking problem, there's this NP-hard
[01:07:50] welfare maximization sort of
[01:07:52] optimization problem on top of it.
[01:07:54] I think of you as a relatively early
[01:07:56] adopter among the economics community
[01:07:58] with respect to, you know, computer
[01:07:59] scientists and and sort of the
[01:08:01] techniques.
[01:08:03] Having now a a decade-plus, I'd say, of
[01:08:05] experience with that community, do the
[01:08:07] two communities have things to learn
[01:08:08] from each other, do you think? I mean,
[01:08:10] either in terms of, you know, bringing
[01:08:13] theory to practice or perhaps even just
[01:08:15] sort of intellectually as far as the
[01:08:17] sort of strengths and and weaknesses of
[01:08:19] each of those communities, computer
[01:08:20] science and and economics?
[01:08:22] >> So, let me start with a compliment for
[01:08:24] you, Tim. Back then, you know, the the
[01:08:27] you were on leave at Columbia, I
[01:08:29] believe. I'd asked around about people
[01:08:32] to include on the team
[01:08:34] and I wanted people who both were really
[01:08:36] good at this as computer science and
[01:08:37] also really excellent teachers and uh
[01:08:40] the two names I came down to were you
[01:08:42] and Kevin.
[01:08:43] And um
[01:08:45] I I tried calling over you and
[01:08:47] discovered that you were on leave.
[01:08:49] That's So, that's I ended up with Kevin,
[01:08:51] who was great, by the way. Kevin,
[01:08:53] terrific, but you would have been
[01:08:54] terrific, too, I'm sure. One of the
[01:08:56] things I found when I got into this was
[01:08:59] the simple, you know, clarity with which
[01:09:01] you and Kevin both Kevin taught me about
[01:09:04] sat solving algorithms while we were
[01:09:06] sitting in a hot tub in the Sierras,
[01:09:08] right? The
[01:09:10] you know, we
[01:09:10] >> [laughter]
[01:09:11] >> we had a retreat to you know, try and I
[01:09:13] was trying to figure out we hadn't
[01:09:15] settled on an auction algorithm yet
[01:09:17] because it depended on you know, what
[01:09:19] computations we could do and we were
[01:09:21] still talking about you know, whether to
[01:09:24] buy interference rights or whether to
[01:09:27] take a station off the air. The products
[01:09:29] hadn't been decided up and hadn't been
[01:09:31] decided and I needed to know what you
[01:09:33] could compute. Kevin explained to me
[01:09:36] well explained to me a lot taught me a
[01:09:38] lot about algorithms. It became clear to
[01:09:41] me that many of the assumptions that we
[01:09:45] make in economics
[01:09:47] are you know, the arbitrary for
[01:09:48] convenience for simplicity and they're
[01:09:50] just wrong, right? You know, we have all
[01:09:52] these
[01:09:53] convexity assumptions that make a lot of
[01:09:56] problems look very simple and sometimes
[01:09:58] they are some
[01:09:59] and I started wondering well, when are
[01:10:02] problems simple? What's really going on
[01:10:04] here and a lot of economics is about
[01:10:06] decentralization
[01:10:07] that is about the we imagine that
[01:10:09] information is spread throughout the
[01:10:12] economy and how do you get that stuff
[01:10:14] working? That's something that I think
[01:10:17] is something that both economists and
[01:10:19] and some group of computer scientists
[01:10:21] are interested in.
[01:10:22] In data analysis too, I know that the
[01:10:24] computer scientists learned a lot about
[01:10:26] causal inference from people like Guido
[01:10:29] and Bentsen others and Susan Athey who
[01:10:32] said yeah, yes, you're very good at
[01:10:34] forecasting but forecasting is not the
[01:10:36] same as causal inference.
[01:10:38] Um so there has been communication
[01:10:40] across that boundary. I think computer
[01:10:43] scientists have been great at absorbing
[01:10:45] a lot of these ideas from economics. I
[01:10:46] think economics has been less good at
[01:10:49] absorbing ideas from computer science.
[01:10:52] Our frameworks are pretty rigid and
[01:10:54] fragile a lot of them and it's been hard
[01:10:57] to absorb um um
[01:11:00] The incentive auction was really an
[01:11:01] exception.
[01:11:02] >> I will say though, just almost all pairs
[01:11:04] of disciplines I've ever observed when
[01:11:06] they start overlapping in interests,
[01:11:08] they kind of tend to behave with a
[01:11:11] mixture of like territorial nature and
[01:11:13] fear, and I feel like it's been kind of
[01:11:15] the opposite of that with computer
[01:11:17] science and economics. It's It's
[01:11:18] literally one of the most, you know,
[01:11:20] as you say, Paul, I mean,
[01:11:22] we should aspire toward, you know, still
[01:11:23] more applications of the impact of the
[01:11:25] FCC incentive auction, but as far as
[01:11:27] just the exchange of ideas, I actually
[01:11:29] think it's been, for the most part,
[01:11:30] extremely constructive, and one of the
[01:11:32] more positive ones I've seen in my
[01:11:34] career between two pairs of fields.
[01:11:36] >> Well, good. Again, I think that computer
[01:11:38] scientists have done a great job of
[01:11:39] take, you know, game theory right now in
[01:11:41] the Journal of Games and Economic
[01:11:43] Behavior, which used to be a a journal
[01:11:45] that was dominated by economic
[01:11:47] publications, it's now mostly computer
[01:11:50] scientists publishing in in yeah, game
[01:11:53] theory and mechanism design. One of the
[01:11:55] things that happens in economics, as you
[01:11:57] know, is that certain ideas get rather
[01:11:59] thoroughly examined, and we move on.
[01:12:01] There's very little research in general
[01:12:03] equilibrium theory anymore. Yeah,
[01:12:05] economists worked on game theory for a
[01:12:06] while, and it exhausted most of the
[01:12:09] economic ideas that were relevant to
[01:12:12] game theory, but computer scientists
[01:12:13] have these other ideas for how to
[01:12:15] approach game theory, and so game
[01:12:17] theory, that area has
[01:12:19] is alive again with ideas that come from
[01:12:21] computer science rather than the ones
[01:12:23] that came, you know, in previous decades
[01:12:25] from economics.
[01:12:26] >> I have to say, Paul, I mean, when you
[01:12:28] made it clear
[01:12:30] um, you know, publicly that you thought
[01:12:31] there was sort of value in these
[01:12:33] collaborations and in the computer
[01:12:34] science ideas, I mean, just by nature of
[01:12:36] your stature, that had a huge positive
[01:12:38] effect in a larger group of economists
[01:12:41] taking notice. So, I mean, the fact that
[01:12:43] you were on board early, I think it's
[01:12:44] been very helpful on the computer
[01:12:46] science side.
[01:12:47] >> Well, good. Well, thank you.
[01:12:48] >> And you've you've also been influential
[01:12:49] through your students. Like, so many
[01:12:51] people who have worked with you have
[01:12:52] gone on to work at the intersection of
[01:12:54] the two fields in in various ways.
[01:12:56] >> Yeah.
[01:12:56] >> You just mentioned causal inference. So
[01:12:58] like you know, all I've just claimed is
[01:12:59] an association, but I'll I'll bet it's a
[01:13:01] causal treatment effect just based on my
[01:13:03] own observational data.
[01:13:05] >> [laughter]
[01:13:06] >> Perfect.
[01:13:07] >> You did mention, you know, sort of ideas
[01:13:10] and new and and you know, you talked
[01:13:11] about water rights. You always have, you
[01:13:13] know, a dozen things that are super
[01:13:15] exciting that you're thinking about. Any
[01:13:17] previews and and slash, you know, sort
[01:13:18] of things that you would tell our you
[01:13:20] know, our listeners that they should go
[01:13:21] think about, too.
[01:13:22] >> You might have noticed on LinkedIn that
[01:13:24] the 1 Chronos and Optix partnership. Did
[01:13:26] you see that?
[01:13:27] >> Yeah, of course.
[01:13:29] >> Uh so, you know, so 1 Chronos is using a
[01:13:34] combinatorial auctions in in security
[01:13:37] exchange. Relatively simple ones cuz
[01:13:39] they happen happen they have to happen
[01:13:41] very fast. One of the areas that we will
[01:13:44] be moving into with
[01:13:47] 1 Chronos and Optix
[01:13:50] is creating futures markets for compute.
[01:13:53] Here's the economic problem we're trying
[01:13:54] to solve, okay? So if you were to um
[01:13:57] to ask Nvidia, for example, what limits
[01:14:00] their sales. Everybody's buying as many
[01:14:02] of these chips as they can afford. When
[01:14:05] you build a data center, if it costs you
[01:14:07] $20 billion to build a data center,
[01:14:10] somebody asked, "Well, why don't you
[01:14:12] build a $30 billion data center?"
[01:14:15] Say, "Well, because I can't get that
[01:14:17] much money." is what you say, right? And
[01:14:19] why can't you get that much money? Why
[01:14:21] can't you borrow it from the bank in an
[01:14:23] environment like this?
[01:14:25] Well, it's because it's very risky.
[01:14:27] Suppose that the bank were to lend you
[01:14:30] $10 billion and you were to build a
[01:14:32] bunch of systems and next year Nvidia
[01:14:35] were to come up with a chip that's 50%
[01:14:38] faster and uses 30% less electricity.
[01:14:41] You know,
[01:14:41] >> Right.
[01:14:42] >> what is the security worth on what
[01:14:44] you've done? And so that makes it hard
[01:14:47] for a traditional for debt financing.
[01:14:49] But if you can spread this risk if you
[01:14:51] have a futures market on the let's say
[01:14:54] rental price of compute for example, if
[01:14:56] you have a futures market on that then
[01:14:59] then those risks can be hedged. And once
[01:15:02] those risks can be hedged, you can
[01:15:03] spread the risk more widely, you can
[01:15:05] support more debt financing,
[01:15:08] you can sell more chips. So there's you
[01:15:10] know the wide demand for this. So one of
[01:15:12] the things we're working on.
[01:15:13] >> One last question, you know,
[01:15:14] forward-looking advice for people who
[01:15:17] are interested in doing market design in
[01:15:19] many forms and shapes and sizes. What
[01:15:21] would you What would you tell them?
[01:15:23] >> Oh goodness, you know, the future is so
[01:15:25] uncertain. What I would say to my
[01:15:26] undergraduates, I want them to be
[01:15:29] rigorously technically trained.
[01:15:31] Um I I can't tell them what knowledge
[01:15:33] they're going to need in particular,
[01:15:36] but uh setting high standards of
[01:15:39] evidence and logic in their thinking by
[01:15:42] studying a discipline that demands it,
[01:15:44] which there are several.
[01:15:46] And then you know, there's some things
[01:15:47] that are just obviously going to grow in
[01:15:49] importance. Artificial intelligence, we
[01:15:51] don't know what it's going to be, but we
[01:15:53] know it's going to be important and even
[01:15:54] more important than it is now. Learning
[01:15:57] something about that would be things to
[01:15:59] do and then beyond that, I'm you know,
[01:16:02] you place your bets, you take your
[01:16:03] chances, but being flexible and being
[01:16:05] ready to adapt to whatever is coming,
[01:16:08] that that's what the students need to be
[01:16:10] doing.
[01:16:11] >> Yeah, that should be printed on a poster
[01:16:13] so that we can
[01:16:13] >> Yeah, exactly. I was going to say
[01:16:15] >> Awesome. [laughter]
[01:16:17] I think I'm going to run that by my
[01:16:18] five-year-old tonight and see if see if
[01:16:20] see if see if it sinks in. So yeah.
[01:16:23] >> Okay. Well, great. Thank you guys. This
[01:16:25] has been wonderful.
[01:16:25] >> you so much for taking the time, Paul.
[01:16:27] Really appreciate it. Fantastic
[01:16:28] conversation.
[01:16:30] Wow. So um
[01:16:32] amazing conversation with Paul Milgrom.
[01:16:34] >> As expected, but still above
[01:16:35] expectations.
[01:16:37] >> [laughter]
[01:16:37] >> I do want to sort of talk about my maybe
[01:16:39] favorite two moments from that interview
[01:16:42] just to reflect on it. My second
[01:16:44] favorite moment, you know, we talked a
[01:16:45] lot about sort of theory and practice
[01:16:46] and so on the back and forth there, but
[01:16:48] at one point he talked about back and
[01:16:50] forth between mathematics and economics.
[01:16:54] And I was fascinated by the way he
[01:16:56] described that. His papers do exhibit a
[01:16:58] sort of mathematical elegance and a
[01:17:00] certain aesthetic, which is a little
[01:17:02] unusual, I'd say, uh, quite unusual in
[01:17:05] in economics papers. He said,
[01:17:07] "You know, I think I understand the
[01:17:08] economics, and then the struggle is just
[01:17:10] how do I get the mathematics to
[01:17:12] articulate what I believe I understand
[01:17:15] about the economics." But then sometimes
[01:17:17] actually the mathematics winds up
[01:17:18] teaching you that you didn't have the
[01:17:20] economics quite right and refines your
[01:17:22] understanding of the economics. So, I
[01:17:24] thought that was my second favorite
[01:17:25] moment. I thought that was I thought
[01:17:26] that was beautiful.
[01:17:28] My top favorite moment has to be the new
[01:17:30] appreciation I have for the call letters
[01:17:33] of the PBS station I grew up listening
[01:17:35] to my entire life, KQED.
[01:17:38] >> [laughter]
[01:17:38] >> Totally amazing. So.
[01:17:41] >> Look, I I can't I can't follow Paul
[01:17:43] Milgrom and then that. We'll just say
[01:17:44] QED.
[01:17:45] >> [laughter]
[01:17:46] >> All right.
[01:17:47] Always a pleasure, Scott. Thanks so
[01:17:48] much.
[01:17:49] >> Thank you. QED.
