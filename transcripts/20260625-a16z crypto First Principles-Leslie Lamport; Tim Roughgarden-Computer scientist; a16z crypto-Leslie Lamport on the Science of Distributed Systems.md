---
访谈时间: "2026-06-25"
访谈时间说明: "未在公开视频元数据中确认单独录制日期，使用 YouTube 发布时间 2026-06-25。"
嘉宾名字: "Leslie Lamport; Tim Roughgarden"
嘉宾公司名称: "Computer scientist; a16z crypto"
播客名称: "a16z crypto First Principles"
播客url地址: "https://www.youtube.com/watch?v=jH05mse8VbQ"
全文提及的关键名词:
  - "Leslie Lamport"
  - "Tim Roughgarden"
  - "distributed systems"
  - "Byzantine Generals Problem"
  - "Paxos"
  - "concurrency"
  - "fault tolerance"
  - "blockchain consensus"
  - "protocol correctness"
  - "DARPA"
  - "theory and practice"
youtube_video_id: "jH05mse8VbQ"
YouTube发布时间: "2026-06-25"
播客标题: "Leslie Lamport on the Science of Distributed Systems"
字幕来源: "YouTube public subtitles: en-orig json3"
---

# Leslie Lamport on the Science of Distributed Systems

## Transcript

[00:00] So, you're going to have a distributed
[00:01] system, some of those computers are
[00:03] going to fail. So, you want to make it
[00:05] fault tolerant. The general problem is
[00:08] really getting multiple processes to all
[00:11] be doing the same thing. There is an
[00:13] unsolvable problem that's being solved.
[00:15] [music] The problem that Axos has is
[00:18] it's implementing a state machine, but
[00:20] that with failures, it could take
[00:22] forever for the computers to come to a
[00:24] decision. I said, "Oh, that doesn't
[00:27] sound very hard." I had the idea that
[00:29] you didn't really need digital
[00:31] signatures. What you needed was a
[00:33] signature that it would be very unlikely
[00:37] for a failed computer to produce.
[00:40] >> Do you have a recipe of how you find
[00:42] problems that are practical where you
[00:44] think you can develop important theory
[00:46] for it?
[00:46] >> Well, one thing that helped me at the
[00:49] beginning was
[00:56] >> [music]
[01:00] >> Hi everyone, and welcome to First
[01:02] Principles, a series by the team at a16z
[01:04] crypto. I'm Tim Roughgarden, head of
[01:06] research at a16z crypto. Our guest today
[01:09] is going to be Dr. Leslie Lamport, the
[01:11] Turing Award-winning computer scientist
[01:13] who, among many other research
[01:15] contributions, first formalized the
[01:17] problem of agreement in distributed
[01:19] systems, the so-called Byzantine
[01:21] Generals Problem, which captures the
[01:23] difficulty of reaching consensus when
[01:25] some participants may fail or act
[01:28] unpredictably.
[01:29] So, through this and his work on logical
[01:32] clocks, state machine replication, and
[01:34] the Paxos consensus protocol, Dr.
[01:36] Lamport helped to lay much of the
[01:38] theoretical groundwork for modern
[01:40] distributed computing, from cloud
[01:42] infrastructure to the consensus layers
[01:45] beneath today's blockchains.
[01:47] So, I'm joined by a16z crypto research
[01:50] partner Etay Abraham as we talk with Dr.
[01:53] Lamport about how these ideas emerged
[01:56] and why careful specification and
[01:58] reasoning remain essential as systems
[02:01] grow more complex.
[02:02] Here's our conversation.
[02:04] Dr. Lamport, welcome and and thanks so
[02:06] much for taking time to speak to us. We
[02:08] we really appreciate it.
[02:09] So, um
[02:11] researchers and engineers who work with
[02:13] blockchain protocols are very familiar
[02:15] with much of your work in distributed
[02:16] algorithms, which is extremely important
[02:18] in that application area.
[02:20] I think that audience may be a little
[02:21] less familiar about the work you were
[02:24] doing that perhaps was a precursor to
[02:26] the work they do know around uh
[02:28] concurrency. And so I thought maybe we
[02:29] could start the conversation um by just
[02:32] setting the stage for what you were
[02:34] thinking about in the early '70s leading
[02:37] up to your work the the initial work in
[02:39] distributed algorithms in the in the mid
[02:40] to late '70s. So, for example, um you
[02:43] know, the time clocks and and the
[02:44] ordering of events paper. Was that sort
[02:47] of a natural segue for you from the work
[02:49] you were doing around concurrency?
[02:52] >> So, I guess the real question is how I
[02:54] got interested in concurrency.
[02:56] And the answer is simple enough.
[02:59] In 1972,
[03:02] I joined the ACM. I think it was
[03:04] probably my first issue of a CACM
[03:08] of had an algorithm for solving the
[03:12] mutual exclusion problem. Basically, uh
[03:15] you have say a bunch of processes in a
[03:19] computer
[03:20] who want to share a resource say a
[03:23] printer.
[03:24] Back in the days when printers were
[03:26] really
[03:27] uh
[03:28] you sent one line at a time to the
[03:30] printer. If two processes were doing
[03:32] that, uh you wouldn't like what you got.
[03:35] So,
[03:35] uh the problem was how to get multiple
[03:38] processes synchronized in such a way
[03:41] that they each has a critical section
[03:43] and at most one process can be in this
[03:46] critical section at the same time.
[03:48] And the problem was originally posed by
[03:52] Edsger Dijkstra,
[03:54] who really started the
[03:57] modern study of concurrency.
[03:59] There was a a solution to that problem
[04:01] uh
[04:02] in CACM, and I thought that, "Well,
[04:06] yeah,
[04:06] that seemed awfully complicated. Should
[04:09] be easier to do." So, I
[04:11] whipped off a uh simple solution for two
[04:13] processes and sent it off to CACM, and a
[04:17] couple of weeks later I got back a
[04:19] letter from the editor uh pointing out
[04:22] where the bug in my algorithm was.
[04:25] And this had two effects.
[04:27] Uh the first was
[04:29] it made me realize how tricky it is uh
[04:32] how concurrency is and how you really
[04:34] have to be
[04:36] uh essentially be able to prove the
[04:37] correctness of a concurrent algorithm.
[04:40] And the second was, you know, I was just
[04:42] going to solve that damn problem.
[04:44] And uh the result of that was the
[04:48] uh
[04:48] bakery algorithm.
[04:51] Now, the thing that interests me about
[04:53] it was that uh
[04:56] I basically started out as a programmer,
[04:57] and I you know, like solving interesting
[04:59] little programming problems.
[05:02] And uh
[05:03] concurrency
[05:04] made problems much more interesting, you
[05:06] know, much more fun. So, it's what I got
[05:09] into.
[05:10] And the bakery algorithm itself,
[05:13] implementing it involved certain
[05:16] problems, but and basically it got me
[05:19] thinking about concurrency.
[05:21] And I'd say that, you know, maybe for
[05:24] the next two or three years, everything
[05:27] that I did directly followed from the
[05:30] bakery algorithm. And that's how I got
[05:32] started.
[05:33] >> And so, what led to uh sort of the
[05:37] either change in scope or sort of the
[05:38] increase in your interests beyond just
[05:41] thinking about multiple processes uh on
[05:43] a single machine to thinking about
[05:45] multiple machines, to thinking about
[05:47] algorithms that uh are distributed.
[05:49] >> Yeah, I think it was 1978.
[05:51] I really discovered that there was no
[05:54] difference between the two for reasons
[05:56] after writing the times clocks paper.
[05:59] It made me think that I had to write a
[06:02] correctness proof for a distributed
[06:04] algorithm.
[06:06] Um
[06:07] and because time clocks made me think
[06:10] that oh, you need to think about
[06:11] distributed systems in a very different
[06:13] way. The way I was doing for you know,
[06:17] multi-process algorithms you know,
[06:19] shouldn't work and you know, I tried a
[06:22] bunch of things
[06:23] and they weren't working
[06:26] and
[06:28] I uh
[06:29] I was writing uh
[06:31] a final report for a project under a
[06:34] government contract that SRI and the
[06:38] promise was we'd write a correctness
[06:41] proof of this distributed algorithm.
[06:43] And finally, I just gave up and said,
[06:46] oh, what the hell, I'll just do it the
[06:47] way I know how to do it for
[06:50] uh
[06:51] uh non-distributed concurrent systems
[06:53] uh and it's not going to be really good,
[06:55] but it'll be
[06:56] you know, I'll get it done. And so, when
[06:59] I did it, I realized that it worked
[07:01] perfectly.
[07:02] And it was exactly the right way to
[07:05] reason about that distributed algorithm.
[07:09] And that's when I learned that there's
[07:11] no basic difference in how you reason
[07:13] about the non-distributed versus
[07:16] distributed concurrent algorithms.
[07:19] >> That's fascinating. Is that distributed
[07:21] algorithm and the correctness proof, is
[07:22] that public domain? Is that from one of
[07:24] your published papers or
[07:26] >> Oh, yeah, I published that algorithm uh
[07:30] I think it's in 1978, but it's something
[07:33] like has a title like correctness proof
[07:35] of a distributed algorithm.
[07:37] >> So, that's the I I I wonder you
[07:39] mentioned multiple times uh
[07:41] proving correctness and thinking about
[07:43] correctness of of algorithms. Can you
[07:44] say a little bit about what what that
[07:46] means? What does it mean that a protocol
[07:48] is correct?
[07:49] >> Basically, it took me
[07:51] uh
[07:52] till about 1990
[07:55] to understand or realize, you know, what
[07:58] correctness means.
[08:00] It started off with properties that was
[08:03] you know, fairly simple like mutual
[08:04] exclusion. Please to state no two
[08:07] processes are ever in their critical
[08:08] section at the same time.
[08:10] And the time clock paper was
[08:15] brought about which started my interest
[08:17] in distributed systems. I never, you
[08:19] know, thought of them particularly
[08:21] when
[08:22] two
[08:23] I guess they'd be called computer
[08:24] scientists. They wrote a paper about uh
[08:27] maintaining consistency in a distributed
[08:30] database.
[08:32] That is when you have uh multiple copies
[08:34] of the database and making sure that all
[08:37] the copies are consistent.
[08:39] One has a general idea of what that
[08:42] means although when you start trying to
[08:45] state, you know, make it really precise
[08:47] it gets a little hard. But at any rate,
[08:50] well, their algorithm I realized
[08:53] didn't satisfy causality in the sense
[08:56] that
[08:57] one command that preceded another
[09:01] command in another part of the system
[09:03] those commands could be executed out of
[09:05] order, you know, out of the order in
[09:08] which they were actually submitted.
[09:10] And
[09:11] um I fixed the algorithm and that was
[09:14] you know, the the algorithm that was in
[09:16] the uh time clocks paper. But I realized
[09:20] and what seemed to me to be completely
[09:22] obvious
[09:23] is that there was nothing special about
[09:26] you know, the particular problem of
[09:27] distributed databases
[09:29] that the general problem is is really
[09:33] getting multiple processes to all be
[09:36] doing the same thing and the
[09:40] obvious way to describe what they were
[09:43] doing was with a state machine.
[09:46] That is all the processes were executing
[09:48] the same state machine and where state
[09:51] machine basically is something that has
[09:53] a state and commands come in and each
[09:55] command produces an output and changes
[09:58] the state. I realized that if you could
[10:02] do that, you can basically implement
[10:04] anything in a distributed system.
[10:07] And in fact, I
[10:09] uh
[10:10] what I realized relatively recently
[10:14] is that abstracting from
[10:17] your duplicate databases
[10:19] to an arbitrary system
[10:22] that involves abstraction.
[10:25] And I happen to be much better at
[10:28] abstraction than most people. It's what
[10:30] Dijkstra wrote a paper with some
[10:32] colleagues colleagues on the concurrent
[10:36] garbage collector.
[10:37] That is a garbage collector that
[10:39] operates in parallel with the program
[10:41] that's creating the garbage.
[10:43] And I made a observation which I thought
[10:46] was pretty obvious that the algorithm
[10:48] could be simplified because it had two
[10:50] data structures, one the data structure
[10:53] that you had to collect garbage from and
[10:55] another one which was the free list.
[10:58] And I realized that it was quite easy to
[11:00] make the free list part of that same
[11:02] structure.
[11:03] Dijkstra
[11:05] made me an an author on the paper for
[11:07] producing that and apparently that was
[11:09] an abstraction that Dijkstra hadn't
[11:11] thought of.
[11:12] And if something that Dijkstra hadn't
[11:15] thought of is not going to be obvious to
[11:17] many people.
[11:18] And in the time clocks paper, I think
[11:20] that really the most important thing
[11:23] uh is that introducing the notion of of
[11:27] implementing a distributed system as a
[11:30] state machine.
[11:31] >> And indeed the the state machine
[11:33] abstraction and just the articulation of
[11:35] state machine replication as a as a
[11:36] problem has been It's very, very central
[11:39] in blockchain protocol design. You can
[11:40] really view modern blockchain protocols
[11:42] like Ethereum and Solana as sort of
[11:44] aspiring to solving
[11:46] uh the general version of state machine
[11:48] replication. So, very, very important
[11:50] work. I'd love to turn a little bit to
[11:52] sort of the next chapters in your work
[11:54] on distributed algorithms. So, for
[11:56] example, the famous Byzantine Generals
[11:57] Problem um paper and then also later the
[12:00] Part-Time Parliament or or Paxos. And in
[12:03] particular, I'd love to hear more about,
[12:05] you know, what led you to introduce the
[12:08] notion of fault tolerance and in
[12:10] particular the notion of Byzantine
[12:12] faults
[12:14] as opposed to perhaps, you know,
[12:15] something like crash faults or some
[12:17] simpler notion of of machine failure.
[12:20] >> Well,
[12:20] again, that seems a very a very obvious
[12:23] thing to do. Uh,
[12:25] you know, having Lamport time clocks,
[12:27] which was an algorithm for implementing
[12:28] a state machine, but with no fault
[12:31] tolerance. And it's obvious that if
[12:34] you're going to have a distributed
[12:35] system, some of those computers are
[12:37] going to fail. So, you want to make it
[12:39] fault tolerant.
[12:41] And as far as Byzantine faults, well, at
[12:44] that time, there was no notion of what a
[12:47] fault might be, you know? And so, I just
[12:50] said, "Well, I'll just take the the most
[12:53] general fault that a uh
[12:56] failed process
[12:58] could do anything."
[13:00] I, you know, I wrote an algorithm that
[13:02] that solved that problem,
[13:04] uh but it uh assumed that digital
[13:07] signatures.
[13:08] Now, I was one of the the few people in
[13:11] the world who happened to have heard
[13:13] about digital signatures
[13:16] because Whitfield Diffie was a friend of
[13:19] mine.
[13:20] Whit was one of the
[13:21] uh founders of modern, I guess you'd
[13:24] call civilian cryptography.
[13:27] We were sitting at uh
[13:29] at a coffeehouse in Berkeley around '76.
[13:32] I don't remember the exact date.
[13:34] He and and Marty Hellman had the problem
[13:36] of, you know, the need for digital
[13:38] signatures.
[13:40] But they didn't have an algorithm for
[13:41] them. And I said, "Oh, that doesn't
[13:44] sound very hard." So I just wrote
[13:47] literally on a napkin and then a simple
[13:49] algorithm uh for writing digital
[13:51] signatures. For the purposes of my
[13:55] of fault tolerance,
[13:57] I had the idea that
[13:59] you didn't really need digital
[14:00] signatures.
[14:02] What you needed was a signature
[14:05] that it would be very unlikely for a
[14:09] failed computer
[14:10] to produce.
[14:12] And I thought that that should be pretty
[14:15] easy simple engineering problem to to do
[14:17] that.
[14:18] Then I went to
[14:20] uh
[14:21] SRI. It was a research project uh for
[14:25] NASA.
[14:26] They knew that future airplanes uh
[14:29] pilots wouldn't be able to fly them that
[14:31] they need a computer because the pilot
[14:33] couldn't react fast enough to what had
[14:36] to be done.
[14:37] And so as a research project, they were
[14:40] building a multiple computer system for
[14:43] flying an airplane.
[14:45] And
[14:46] they figured again, they didn't know
[14:48] what a failed computer could do. So
[14:51] and since they needed real high
[14:52] reliability, they had to assume that it
[14:55] could do anything and therefore they
[14:57] were faced with again the Byzantine
[14:58] generals problem.
[15:00] They they probably hadn't heard of
[15:02] digital signatures at the time.
[15:04] So they came out with an algorithm that
[15:07] didn't need them. I was with digital
[15:09] signatures, you know, you could tolerate
[15:11] n faults with 2n + 1 computers. But
[15:15] without digital signatures, you needed
[15:17] 3n + 1 computers.
[15:20] For reasons that I've never understood,
[15:23] you know, people building airplanes
[15:25] decided that oh, they needed 3N + 1
[15:28] computers
[15:29] because they would seem to think that,
[15:32] you know, digital signatures were
[15:33] impractical.
[15:34] But, I thought they should be practical
[15:36] if you're not worried about malicious
[15:39] opponents, but random failures.
[15:42] The people at SRI when, you know, when
[15:44] they were trying to solve the problem,
[15:46] you know, they
[15:47] tried to come up with solutions
[15:49] that weren't provably correct, but they
[15:52] would say, "Oh, that could not happen in
[15:53] practice."
[15:55] They would be able to construct some
[15:57] kind of failure that
[15:58] was not so implausible that could break
[16:01] the algorithm.
[16:03] And Rob Shostak was one of the people
[16:06] who were working on that, and Marshall
[16:08] Pease, and
[16:10] Michael Melliar-Smith I think were the
[16:12] other ones. So, I don't know who
[16:13] actually came up with the
[16:15] uh algorithm for was hailing a single
[16:17] failure, which required four processors.
[16:20] But, the uh one for the general one for
[16:23] N was discovered by Marshall Pease, and
[16:26] that was uh
[16:28] an amazing uh amazingly brilliant
[16:30] because it was so
[16:33] difficult to understand. Later on, I
[16:36] found a a way to describe
[16:40] uh his algorithm recursively.
[16:43] That is, describe the N process one, you
[16:46] know, recursively in terms of the N - 1
[16:48] process one.
[16:50] Uh and that made it understandable, but
[16:53] he didn't have that that trick. And so,
[16:56] he did it by sheer brainpower. So,
[16:59] anyway, so that's how, you know,
[17:01] Byzantine Generals came to be. And of
[17:03] course,
[17:04] you know, once uh hackers, you know,
[17:07] started appearing on the scene, then it
[17:09] was obvious that really did need to
[17:12] uh
[17:13] Byzantine fault tolerance.
[17:14] >> Absolutely. And 2025 is is literally the
[17:17] right model for how some of these
[17:19] distributed protocols are being
[17:20] attacked. So just again an amazing
[17:23] power of abstraction is ultimately
[17:25] capturing
[17:27] you know exactly what the problem is in
[17:28] in some future generation of the
[17:29] technology.
[17:30] So to wrap up sort of the discussion of
[17:33] of these fundamental works in
[17:34] distributed algorithms, I wanted to chat
[17:36] a little bit about the evolution of how
[17:38] you thought about communication network
[17:40] reliability or message delays and
[17:43] asynchrony, which is something that
[17:45] plays an important role in the Part-Time
[17:48] Parliament paper.
[17:49] So what led you to to to think about
[17:53] more relaxed models of communication
[17:55] between the different the different
[17:56] machines?
[17:57] >> I'm not sure. I mean I I know exactly
[18:00] where Paxos came from.
[18:02] I was working at that time at the
[18:05] Systems Research Center at Digital.
[18:08] And the people there
[18:10] had a a local area network
[18:12] and they
[18:15] believed that failures would just be a
[18:16] computer would just die, would just
[18:18] crash. They weren't worried about
[18:20] Byzantine behavior.
[18:22] I was convinced that
[18:24] well, what they were trying to do was
[18:27] impossible.
[18:28] You know, that there did not exist an
[18:30] algorithm that would have the features
[18:31] that they claimed that their program
[18:33] had. So I started out trying to write an
[18:36] impossibility proof.
[18:38] But instead of an impossibility proof, I
[18:40] wound up with an algorithm.
[18:42] And that's how Paxos
[18:45] came to be.
[18:46] Actually, the problem that was
[18:47] impossible was the impossibility
[18:51] a result of Fisher, Lynch, and Patterson
[18:54] in terms of
[18:56] their paper, you know, there is an
[18:59] unsolvable problem that's being solved.
[19:02] It can't be solved without the use of
[19:04] clocks. And so the the problem that
[19:07] Paxos has is
[19:08] in principle
[19:10] basically it's implementing a state
[19:12] machine, but that with failures, it
[19:15] could take forever
[19:16] for the computers to come to a decision.
[19:20] Uh
[19:21] and what Paxos does
[19:24] is an algorithm that
[19:27] makes it highly unlikely that that will
[19:29] happen.
[19:31] And so, it gives up liveness in
[19:34] principle,
[19:36] but maintains safety.
[19:38] And uh
[19:39] and the probability of not making a
[19:42] decision forever is is just, you know,
[19:44] negligible. And so,
[19:46] it works in practice.
[19:48] >> Yeah, I I I think Paxos went through
[19:49] this uh story about legislators, right?
[19:52] They're trying to
[19:53] reach agreement on uh on a ledger of a
[19:56] >> Yeah, well,
[19:57] I learned something
[19:58] uh
[19:59] years earlier. It's phrased in terms of
[20:02] uh some bunch of philosophers dining a a
[20:07] round a table, and there's one chopstick
[20:09] between each
[20:11] uh pair of of philosophers are sitting
[20:13] around a round table.
[20:15] And it requires two chopsticks in order
[20:17] to eat. Problem was, how do you make a
[20:20] an algorithm that keeps everybody from
[20:23] starving and, you know, lets each person
[20:27] eventually be able to to eat.
[20:30] And I've never found that problem so
[20:33] interesting. I think that people were
[20:37] aware of that problem because it had
[20:39] this story attached to it.
[20:42] And so, when we discovered the the
[20:45] Byzantine
[20:47] uh generals results, I realized that
[20:49] that was important.
[20:51] And to make people
[20:55] aware of it, I thought there would
[20:57] should be a nice story behind it. And
[20:59] that's how the Byzantine generals came
[21:01] about.
[21:03] Uh
[21:04] well, I was successful with that that
[21:06] when Paxos came around, I tried to do
[21:09] the same thing and that was a flop.
[21:12] I just did a a terrible job of it and it
[21:16] just confused people and put them off
[21:18] rather than uh
[21:20] making it uh you know, accessible. And
[21:22] so, the significance of that paper was
[21:25] understood by very few people. One of
[21:27] them was, fortunately, Butler Lampson
[21:30] who went around
[21:31] uh popularizing it.
[21:34] And uh the referee said that this paper,
[21:37] well, it's
[21:39] not very interesting, but it's worth
[21:40] publishing but then you can get rid of
[21:42] all this uh Paxos stuff. And
[21:45] you know, that up- annoyed me, so I just
[21:47] put the paper aside. And uh
[21:51] when it became clear of how, you know,
[21:53] that was important,
[21:55] uh
[21:56] I uh got it published with the Paxos
[21:59] stuff.
[22:00] >> So, so in some sense, the uh the
[22:02] condition for liveness, for success uh
[22:04] in the Paxos algorithm,
[22:06] is that uh all these legislators or a
[22:08] majority of them are actually inside
[22:10] this chamber where communication is
[22:12] synchronous. So, I wonder, was that kind
[22:14] of uh how did you come up with that that
[22:16] abstract? I mean, by the way, that is
[22:17] essentially the abstraction that is now
[22:19] used by uh almost all uh distributed
[22:22] systems.
[22:23] >> You know, there's nothing about that in
[22:25] the paper, you know, talking about
[22:27] synchrony, asynchrony, or anything like
[22:29] that.
[22:30] It's just uh
[22:32] you know, gives the algorithm. And in
[22:34] order for the algorithm to work, you
[22:36] have to have this
[22:38] this condition. And
[22:41] I suppose people
[22:43] >> [snorts]
[22:43] >> you know, gave a name to the condition
[22:45] or whatever, but I don't I don't know
[22:47] how that happened.
[22:48] >> But in some sense, it was kind of you
[22:49] were trying to prove a lower bound
[22:51] saying it's impossible and you said,
[22:52] "Oh,
[22:53] actually, if this thing happens, then I
[22:54] can make progress."
[22:56] Is that kind of how how things evolved?
[22:58] >> I mean, I thought it was impossible
[23:00] maintaining
[23:02] uh safety would be impossible
[23:05] even if you didn't you know
[23:07] worry about liveliness.
[23:09] On the other hand, you know, it was it
[23:10] was sort of
[23:12] clear that with the kinds of failures
[23:14] that people were thinking about, you
[23:16] know, one process just dies and the
[23:20] others keep going and then can
[23:21] communicate reasonably.
[23:24] That was just a natural assumption to
[23:26] make and
[23:27] this was now going to you know just
[23:30] for real engineers to
[23:32] to work uh
[23:33] to
[23:34] to build real systems and
[23:36] you know, real engineers are
[23:39] not worried about the kinds of highly
[23:41] unlikely uh
[23:43] failures that would uh defeat Paxos.
[23:47] >> That may be a good point to um
[23:49] talk a little bit about the interplay
[23:51] between theory and practice through this
[23:53] through the sequence of works cuz you
[23:55] know, Dr. Lamport, you've mentioned you
[23:56] know, enjoying programming puzzles and
[23:58] we've talked a lot about the importance
[24:00] of mathematical formalism and
[24:02] abstraction. At the same time, you've
[24:04] told several stories about talking
[24:06] engineers, looking at existing code at
[24:08] existing attempts at
[24:10] at solving perhaps not yet articulated
[24:12] problems
[24:13] and it's remarkable. You know, a number
[24:16] of your works on the one hand, you look
[24:18] at them and they're in some sense a
[24:19] theory paper, but [snorts] the practical
[24:22] impact has been massive. So,
[24:24] I'm curious if you could speak just a
[24:25] little bit, you know, why have you been
[24:27] so successful in in combining these two
[24:29] things and do you have a do you have a
[24:31] recipe of how you find problems that are
[24:33] practical where you think you can
[24:35] develop important theory for it?
[24:37] What else would you advise the next
[24:38] generation who who wants to do work
[24:41] along those same lines?
[24:42] >> Well, one thing that helped me at
[24:45] certainly at the beginning
[24:48] was a lot of the people
[24:51] you know, who were working in those
[24:52] early days
[24:54] they seem to be thinking in in terms of
[24:57] programming languages
[24:59] or
[25:01] in terms of mathematical theories. And
[25:03] it always seemed to me that since
[25:05] concurrency is in some sense more of a
[25:07] physics problem
[25:09] than either a language or a
[25:11] a mathematical problem.
[25:13] You know, [snorts] like mutual
[25:14] exclusion. You know, two things not
[25:17] happening at the same time. Same time,
[25:19] that's physics.
[25:21] And so
[25:22] I've just really thought in terms of
[25:25] real
[25:27] uh things. For instance, in the early
[25:29] days people would talk say they'd solve
[25:31] the mutual exclusion problem by
[25:33] inventing some language construct that
[25:36] would implement mutual exclusion.
[25:39] And you know
[25:40] that's
[25:41] to me was not solving mutual exclusion.
[25:44] So, I've guess I've always had a sense
[25:47] of whether
[25:48] some problem
[25:50] makes sense in terms of you know
[25:53] real computers, real you know, electrons
[25:56] flowing or whatever.
[25:58] I guess you know, for a problem to
[26:00] interest me, I guess I usually
[26:04] always had some physical situation where
[26:06] it seemed to
[26:08] it to make sense.
[26:09] >> I'm curious if if working largely in the
[26:11] milieu of a industrial research lab
[26:13] played an important role in this as
[26:15] opposed to say being in academia. Was
[26:17] that important?
[26:19] >> Well, I've always used to say so. I
[26:21] mean, I've some problems, you know, came
[26:23] to me because some engineer or
[26:25] programmer, you know, had this problem
[26:26] to solve like uh disk Paxos uh for
[26:30] example, that came because
[26:32] he didn't want to use more than you
[26:33] know, two computers, but you know, he
[26:35] wouldn't be able to use three or four
[26:37] disks.
[26:38] And
[26:39] his autobiography uh Jean Renoir
[26:43] who's the son of August Renoir, the
[26:45] famous painter
[26:47] said that his father had told him
[26:50] that when asked why he went
[26:53] and carrying looking all this stuff
[26:55] instead of painting in the in the studio
[26:58] was that he said
[27:00] well, if I was in my studio and was
[27:02] going to draw a tree, I
[27:04] you know, I might be able to come up
[27:06] with, you know, five or six different
[27:08] kinds of of leaves.
[27:10] But you go out in nature and there are
[27:12] thousands of different kinds of leaves.
[27:15] That's my explanation of why I like the
[27:18] you know, working in a company that's
[27:20] you know, actually building things.
[27:22] >> I think that's an amazing and deep
[27:23] analogy. That's great.
[27:25] >> I think that that distinction between
[27:28] uh academia and industry in terms of you
[27:31] know, practicality and stuff
[27:33] that gap has has has closed uh
[27:37] a lot since the days when I was was
[27:39] doing that stuff.
[27:40] >> So great. So
[27:41] perhaps moving on to the just briefly at
[27:44] least the topic of abstraction and Dr.
[27:46] Lamport you already in some sense
[27:48] alluded to the answer to this, but Don
[27:49] Knuth has said on many occasions that 2%
[27:53] of the population is meant to be
[27:55] programmers.
[27:56] And I'm curious what you think of that
[27:58] quote and perhaps also if we substitute
[28:01] the word abstraction for programming in
[28:03] that quote or alternatively
[28:06] is it something that can to some extent
[28:08] be be taught?
[28:09] >> Well, you know, I've devoted much of
[28:13] the end of my career
[28:15] uh
[28:16] to getting programmers or
[28:19] I would say more system designers than
[28:21] uh you know, average programmers
[28:24] to be able to abstract and you know, to
[28:26] think more abstractly about what they're
[28:28] doing.
[28:29] My understanding of of how one should
[28:33] reason about concurrent programs and
[28:37] concurrent algorithms
[28:38] led me to develop a language called TLA+
[28:43] I will say I've got enough
[28:46] experience to say that
[28:48] very good
[28:50] uh
[28:51] engineers will by using TLA+
[28:55] improve their ability to abstract and
[28:59] make them better designers.
[29:01] >> And so maybe this is a good segue into I
[29:04] believe you have a a coming book, A
[29:06] Science of Concurrent Programs.
[29:08] I would love it if you could speak a
[29:10] little bit about that and and the goals
[29:11] of the book.
[29:12] >> The goal of the book is very simple.
[29:15] I've worked as I said starting
[29:18] well really in some sense starting from
[29:21] uh 1975
[29:23] or so when I
[29:25] wrote this first paper on proving
[29:28] correctness of multiprocess uh
[29:30] programs. You know, I'm figuring out how
[29:34] to a
[29:37] state very precisely what
[29:40] what the problem is, what the you want
[29:42] the algorithm to do
[29:44] and describing the algorithm precisely
[29:48] and being able to show that
[29:50] mathematically and with tools that this
[29:55] algorithm satisfies the correctness
[29:57] property that it should.
[30:00] Basically, the book is putting all that
[30:03] in one place
[30:04] you know, pretty much everything that I
[30:06] learned about the theory uh behind it.
[30:09] It's not about
[30:11] you know, how to use it in practice, but
[30:14] it's about the underlying theory.
[30:16] >> And this is on Cambridge University
[30:17] Press, is that right?
[30:18] >> That's they promised to to uh
[30:20] publish it and the last they said their
[30:23] goal was in March.
[30:25] >> Fantastic. So, Dr. Lamport, thank thank
[30:27] you again for the time. Really
[30:28] appreciate you you speaking to us.
[30:30] >> Okay, it's my pleasure. I had fun uh
[30:33] >> Fantastic.
[30:34] Well, that was pretty amazing hearing
[30:37] from both Leslie Lamport and Barbara
[30:39] Liskov. I thought maybe we could circle
[30:41] back on on something we talked about the
[30:43] power of you know mathematical
[30:44] abstraction of sort of real systems and
[30:47] sort of the feedback loop between
[30:48] practice and and theory. And I I do feel
[30:50] like that came out pretty explicitly in
[30:52] both of the interviews.
[30:54] >> Yeah, I thought both both of them
[30:55] focused on these deep connections
[30:57] between the practical work that they've
[30:59] done and the theoretical underpinning,
[31:02] correctness proofs, and the way that
[31:05] they thought about distributed systems
[31:07] through kind of a mental model that
[31:09] looks a lot like how we think about
[31:11] mathematics sometimes. I think Barbara
[31:13] talked about this mathematical hierarchy
[31:15] of a theorem that has lemmas and sub
[31:17] lemmas and so on. So the analog here is
[31:20] that you look at a system, you don't
[31:21] think about it as a monolithic system,
[31:23] but you kind of look at it as a series
[31:24] of encapsulations and abstractions. And
[31:27] that's extremely important because these
[31:28] distributed systems are very very
[31:29] complicated. So if you just kind of you
[31:31] know just think about this as like a
[31:32] whole lump of of system or of math then
[31:35] it's very very hard to understand what's
[31:36] happening. Yeah.
[31:37] >> Yeah, your head explodes, yeah.
[31:38] >> And they built extremely complicated
[31:40] systems, right? So if you look at PBFT,
[31:42] this is like a huge endeavor and really
[31:44] this power of abstractions what enabled
[31:46] that. And and this pattern, right? Of
[31:48] abstraction and encapsulation is like a
[31:50] core factor of how distributed systems
[31:51] are built today.
[31:52] >> I mean arguably it's like at the very
[31:54] center of computer science as as a
[31:56] discipline.
[31:57] >> Yep, yep.
[31:58] >> I mean in addition to just how the
[32:00] overall themes there were such strong
[32:01] parallels. I mean it was wild how their
[32:03] actual work also converged at least at
[32:06] particular points. We heard from Dr.
[32:08] Lamport about you know Paxos, we heard
[32:11] from Dr. Liskov about
[32:13] you know view stamp replication. It's
[32:15] probably sometimes you know ideas
[32:17] there's just like the right time for
[32:18] them and sometimes it's because you
[32:21] actually lacked kind of the tools to
[32:24] come to the idea. Sometimes sometimes
[32:26] it's an idea that in principle all the
[32:27] tools were available 10 years prior, but
[32:29] somehow
[32:31] it was just there's a right moment in
[32:32] time for this idea to emerge. It's
[32:34] something even you know after 25 or
[32:35] whatever years of of doing this I still
[32:37] find, I must say, a little bit
[32:39] mysterious.
[32:39] >> Yeah, this is kind of a fascinating
[32:41] aspect of the academic world, for sure.
[32:43] >> Another thing that I thought was an
[32:43] interesting parallel, you know, the
[32:45] interplay between theory and practice,
[32:46] but you know, their career paths are on
[32:49] paper somewhat different, right? So,
[32:50] they somehow
[32:52] both really leaned into the synergy
[32:54] between those two things, but in
[32:56] different ways.
[32:57] >> I would say, uh, Barbara Liskov, she was
[32:59] kind of a one of the founders, I guess,
[33:00] of systems research in computer science,
[33:03] I industrial systems. So, you know, she
[33:05] was at at MIT working with a lot of
[33:07] students and and trying to build
[33:09] systems. And kind of on the other side,
[33:11] Leslie Lamport spent his whole career in
[33:13] industrial research. So, he was kind of,
[33:15] you know, doing a a lot of theoretical
[33:17] work, but but being very connected to
[33:19] engineers, uh, and and kind of talking
[33:21] to systems researchers and and people
[33:23] who built, uh, large systems. So, both
[33:26] of them worked on the interface of, I
[33:28] guess, theory and systems, and trying to
[33:30] build things and working with with
[33:31] builders, but both of them came from
[33:33] kind of different very different career
[33:35] paths. Uh, so, it's interesting to see
[33:36] how different influences kind of, uh,
[33:39] push you to different directions.
[33:40] >> Yeah. Though, in both cases, it was, you
[33:43] know, US government funding for
[33:44] different projects that wound up being
[33:46] pretty important, right? So, Dr. Lamport
[33:48] mentioned NASA, he mentioned SRI, and
[33:50] then Dr. Liskov talked about sort of a
[33:53] big DARPA announcement. So, that was
[33:55] sort of a also a common theme for both
[33:57] of them about where some of the problems
[33:58] that they worked on and the motivation
[34:00] for them came from.
[34:01] >> DARPA was kind of this huge, uh, force
[34:03] in the academic world. In the sense, you
[34:05] could think about, uh, the internet,
[34:06] right? As coming from DARPA pushed, uh,
[34:09] use cases, and then maybe flourish
[34:10] through kind of economic, uh,
[34:12] incentives.
[34:13] >> I'm sure as most listeners know, the
[34:14] original internet was actually called
[34:15] the ARPANET because, uh, it was a ARPA
[34:18] project, ARPA being the precursor to to
[34:20] DARPA.
[34:20] >> Yeah, yeah. And, you know, Byzantine
[34:22] agreements might have the same type of
[34:24] path in a way. It was kind of, uh,
[34:25] pushed by DARPA as a focus for
[34:27] survivability. They really cared about
[34:29] this notion of having large-scale
[34:30] distributed systems that survive attacks
[34:33] or would survive failures or would
[34:35] survive even if part of the system, you
[34:36] know, got destroyed or got maliciously
[34:38] attacked. And it's actually fascinating
[34:40] to see that this technology is now being
[34:42] used for in a for economic use, right?
[34:44] In in blockchain technologies. So, it's
[34:47] kind of you know, the same type of
[34:48] pattern of a movement of technology
[34:50] from, I would say, you know, government
[34:52] focused funding to kind of economic
[34:55] value.
[34:55] >> I mean, it also just shows I mean, we've
[34:57] seen this over and over and over again,
[34:58] but I mean, blockchain technology just
[34:59] alone has multiple instances of where
[35:02] the decades long, even kind of half
[35:04] century long time scale is like the one
[35:07] at which sort of really sort of
[35:09] fundamental breakthrough ideas emerge,
[35:11] right? Which is just
[35:13] if you're not sort of working with this
[35:14] stuff day-to-day, it can kind of be
[35:15] sometimes hard to see, okay, where is
[35:17] this going? What's the payoff going to
[35:18] be? But it's it's a very long-term game,
[35:20] fundamental research. And and I think
[35:22] that came through very strongly today.
[35:24] >> Yeah, who knows? Maybe this notion of
[35:25] survivability of systems will actually
[35:27] become very important in the future as
[35:28] well. So, you know, you might see
[35:30] technology go back from,
[35:32] you know, blockchain technologies back
[35:33] to focus on survivability of systems.
[35:35] >> That's a great point cuz that's
[35:36] something again, you know, I mentioned
[35:38] cryptography and SNARKs earlier and
[35:39] that's sort of another example where
[35:41] blockchain technology, I think is really
[35:42] pushing the state of the art with SNARK
[35:45] design, but a lot of the applications of
[35:46] SNARKs are outside of blockchain
[35:47] technology. So, as much as blockchain
[35:49] technology has stood on the shoulders
[35:52] of ideas of other parts of computer
[35:54] science, engineering, I do think it's
[35:56] reaching a maturity state where it's
[35:57] giving gifts back, kind of returning the
[35:59] favor, which has been a very cool
[36:00] development.
[36:01] >> Yeah, absolutely.
[36:02] >> All right. So, it's I thank you for
[36:04] joining us to co-host. Super super fun.
[36:06] >> Thank you for having me. This was this
[36:07] was a lot of fun. This was a lot of fun.
[36:08] Yeah, we should do this more.
[36:09] >> We should. We should. Let's work on
[36:11] that.
[36:11] >> let's do it.
