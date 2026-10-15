---
访谈时间: 2026-06-19
访谈时间说明: YouTube 发布时间；未能独立确认访谈录制日期
嘉宾名字: "Barbara Liskov; Tim Roughgarden"
嘉宾公司名称: "MIT; a16z crypto"
播客名称: "a16z crypto"
播客url地址: "https://www.youtube.com/watch?v=5N2MGCh2zzI"
字幕来源: "YouTube automatic_captions en-orig"
全文提及的关键名词:
  - AI
  - Bitcoin
  - crypto
  - Before
  - Blockchains
  - There
  - Was
  - State
  - Machine
  - Replication
  - Barbara
  - Liskov
  - Tim
  - Roughgarden
companies: []
industries:
  - 加密
technologies:
  - 区块链
  - 分布式系统
  - 比特币
keywords: []
tags:
  - 加密
  - 区块链
  - 分布式系统
  - 比特币
---

# Before Blockchains, There Was State Machine Replication (ft. Barbara Liskov and Tim Roughgarden)

## Transcript

DARPA had recognized that this was a
serious problem, the problem of
malicious attacks, and was looking for
research in that area. I had a student,
[music] Miguel Castro, who came to me
and he said, "Why don't we see whether
we can figure [music] out a way to do
replication that handles these malicious
attacks?" And that seemed like a great
idea. If the primary If the primary
[music] that was running the protocol,
the whole thing came to a crashing halt.
We came up with a protocol that if
[music] the primary seemed to not be
doing its job, the backups then carried
out another protocol in which a
different replica became the primary. We
thought that at some point people would
start to use this. And then along came
blockchains.
And
>> [music]
>> well, that was very funny.
>> Someone who loves computer science,
loves research,
>> [music]
>> wants to do important work, must have an
impact. What would you suggest as kind
of a mindset as an approach?
>> Computer science [music] is in a very
strange place right now. With the advent
of AI, I think that [music] as far as
research is concerned,
>> [music]
>> Hi everyone, and welcome to First
Principles, a series by the team at a16z
crypto. I'm Tim Roughgarden. I'm the
head of research at a16z crypto, and
today we're exploring a core challenge
in distributed computing. How can a
system remain reliable when some of its
parts fail or behave maliciously?
In this episode, we're going to speak
with the Turing Award-winning computer
scientist whose work helped answer this
question, Dr. Barbara Liskov. She's
famous for many things, but today we're
going to focus on her work that laid the
foundations for modern blockchain
systems. For example, from Viewstamped
Replication from the 1980s to Practical
Byzantine Fault Tolerance or PBFT a
decade later.
a16z crypto research partner Ittai
Abraham joins me as we talk with Dr.
Liskov about her path from programming
languages to distributed systems, the
evolution of practical replication
protocols, the state machine replication
paradigm underlying blockchains, and how
emerging technologies like AI are
reshaping systems research. Here's our
conversation.
Professor Liskov, thanks so much for
joining us for the conversation today.
Really appreciate you you taking the
time.
>> Sure.
>> I thought maybe it would be fun to start
to just discuss a little bit about how
you got into distributed systems
research, which my understanding was
maybe around 1980 or so, especially
given that, you know, throughout the
1970s you did a lot of extremely
important work on other topics,
operating systems, programming
languages,
data abstraction. So, why the sort of
segue into distributed systems around
that time?
>> So, what happened was I had finished
working on Clue, which was the
programming language that
um I developed with my group to provide
access to data abstraction as a way of
building programs.
And I had thought a little bit about
maybe starting a company to market the
language,
but I realized that
um I was much more interested in
research.
And I also thought that I had sort of
done as much programming language
research as I had anything interesting
to do at that point, and I started
looking around. And I read um
paper by Bob Kahn in which he talked
about the dream of distributed
computing.
And how there would be distributed
programs that had components at
different nodes in a network and
communicated over the network, and only
nobody knew how to build them.
And so I thought, there's a great
problem.
So I jumped into distributed computing.
>> Wow, fantastic.
>> was a great yeah, great move.
>> Well, it was great for computer science
that that happened. Let's think about
it. Um, I'm curious, did did it feel
like a pivot at the time? Like you were
really changing your research field? And
maybe a related question would be, you
know, how much did sort of the the
mindset and the approach to abstraction
that you developed early in your career,
how much did that port over versus how
much did you need to really have a new
sort of toolbox for working on those
problems?
>> Well, it I I may have thought of it as a
pivot, but my first project there was a
programming language.
And that programming language was really
an extension of the language I'd already
developed. We had this language called
Clu, it supported abstract data types
and objects. And in Argus, which was the
new language, we had abstract data types
and then we had one additional feature,
this new kind of object which we called
a guardian.
And the idea with the guardian was it it
resided at one node of a network. It
provided operations that could be called
from other nodes. And so the idea was a
distributed program consisted of all
these guardians, each running on its
node, communicating with each other.
And so really, it wasn't that much of a
pivot at all. It was in fact
picking up something I'd had to leave
behind for Clu, which was parallel
computing.
I had decided in Clu that that was going
to be a sequential language because I
felt we had enough stuff going on that I
didn't want to complicate it by adding
concurrency as well.
And so now I was able to pick up
concurrency, but in this more
interesting world where concurrency
wasn't just that you had a for loop
where you ran a bunch of threads in
parallel, but instead you had multiple
users and they might be making requests
in parallel and stuff like that. And one
of the interesting things about Argus
was that we had to worry not just about
concurrency, but also failures. And we
had computations there
that would visit several nodes of the
network. And then at the end, we had to
make sure that such a computation either
happened completely or had no impact
whatsoever.
And so, of course, we picked up
transactions from database systems, and
[snorts] we ran those computations as
atomic transactions. And we had a
two-phase commit protocol going on.
It seemed like a continuation in a more
evolved or complicated environment. So,
it should allow me to look at additional
problems.
>> Yeah, I was I was just on a personal
note. It was It was very cool for me to
sort of read all that backstory because
when I'm explaining blockchain execution
to sort of undergrads in my class, you
know, I had taken to using
object-oriented programming as kind of
the mental model they could kind of fit
it into as far as the sort of
interoperability between different parts
of the state. And so then, you know, to
see that indeed that's exactly sort of
the roots of of sort of your thinking
about it in those early systems, I
thought was really really cool to see.
So.
>> I would [clears throat] say that
modularity is everything
in building large programs.
And
it was only many years later that I
started to think of modularity and
theorems as being similar.
But it seems very clear that they are
because in a theorem, you start off with
the statement of what is supposed to be
true. You want to reason about this. But
of course, you don't do it as one big
blob.
Which by the way, was kind of how
programs were written back in the '60s
and '70s.
Uh instead, you have to have lemmas, and
the lemmas each have a statement of what
they are, and then you prove their
correctness independently, and you can
reason about each piece of the theorem
as a separate unit.
And this is exactly what's going on in a
modular program. You know, you have each
module, it's got a specification.
You can do a proof of the correctness of
the code that implements the module
without having to look at any other
modules code. You just look at the
specifications of other modules. And
that's very similar to a theorem with
limits and so forth.
And um I just think looking back that
since I was a math major in college uh
it was just a very natural way of
thinking about things to me even if I
hadn't had it in the front of my mind
what I was working on the original work
on modularity.
>> So your your uh early work on
distributed computing view stamp
replication you were kind of uh trying
to to merge this object-oriented
approach with handling failures.
So I wonder what what was kind of the
main motivation for thinking about uh
you know handling failures in in the
distributed system.
>> You know, I don't think it had anything
to do with object-oriented. I think
it was a question that was of great
interest in the systems community at
that time.
We could all see
that it would be really nice to have a
file system
that was you know, implemented at many
replicas and where lots of people could
be using the same files. In those days,
if you wanted to write a paper or do
other work with somebody else, you had
to use file transfer. And you know, you
couldn't access their file system. What
you could do is communicate by email in
a sort of an you know, not terribly
attractive way. And of course, you had
the problem that if your computer was
down, you had no access to your files
and wouldn't it be nice if we could have
a replicated system where the stuff was
always there and so forth. So this was a
problem that was sitting there in the
systems area that people were interested
in. And so I got interested in it.
And um I had a student Brian Oki who was
looking for a thesis topic and so the
idea of a replicated file system seemed
like a really interesting thesis topic.
This is in the mid-80s.
>> So this is maybe a little bit of a a of
a digression, but I'm just curious which
is a little bit about what systems
research was like at that time as a as a
community. So, my career started kind of
around 2000 or so and for much of my
career the field of systems is so large,
it feels a little bit fragmented to me.
Like you've got conferences devoted to
databases, multiple multiple on
networking, multiple on operating
systems. Meanwhile, you've already
talked about the idea that it was
obvious throughout the systems community
as if it was one community. You also
talked about how just, you know, the
proximity to different areas meant that,
you know, two-phase commit protocols and
transactions and atomicity. You
recognize that immediately as things you
were going to need in the distributed
systems context. So, what what were
things like back then?
>> Um they were very nice.
>> [laughter]
>> So, it used to be SOSP was the main
conference. And I remember going to SOSP
and the people you think of in the
systems area like Butler Lampson and so
forth were there. But so was Jim Gray,
so was Bruce Lindsay. All the top
database people were all there. And the
conference was small enough that we used
to have it at Asilomar.
>> Wow.
>> Which is
>> In Monterey.
>> a site in Monterey.
>> Yeah.
>> But the conference was small. Uh in
those days there may have been other
specialized conferences, but mostly we
were together and so it was easy for us
to
to see the sort of field as a whole.
>> Sounds like a magical time. Sounds
amazing.
>> It was a good time.
>> So, to bring it back to kind of um your
research. So, so entering distributed
systems, working on Argus, beginning of
the '80s. And then at some point you
decided to focus specifically on
replication, right? And you know, it's I
mentioned the view stamp replication
protocol. So, so could you talk a bit
about what led you to focus on that
problem at that time?
>> It just seemed like a really interesting
problem. I always like to work on stuff
that looks important. So, it was clearly
something that was coming and it it was
clearly something we needed and we
really didn't understand how to
implement a system like that. The view
in the systems community at that point
was mainly to think about this using
locking. So, the idea was you had the
users, and they would lock the replicas
so that they could have control. So,
that way you were going to make sure
that you didn't have concurrency
problems. And to me, that seemed like a
very bad solution because that means you
have to re-depend on these other users
at far-flung sites to do their job, and
[snorts] they might not do it. So,
I thought, let's switch the work to the
replicas. And I think in retrospect,
this is because of the work I did in
Argus, where I was already using atomic
transactions, and it was already sort of
natural to think of having a group of
replicas that were in charge of things.
Although, I didn't have that insight at
the time. It just seemed like this
looked like a good approach.
So, Brian and I dug into it, and there
was work in theoretical computer
science. I mean, they understood then
that you needed 2F + 1 replicas to
survive F failures,
and there may even have been a protocol,
but our focus was different because we
were always interested in practical
protocols that you could really use that
were efficient. And we based our work on
two-phase commit.
Um
but of course, two-phase commit didn't
actually solve the problem because
two-phase commit had what was in it
called the embarrassing pause,
or the window of vulnerability, where if
the primary failed, the primary that was
running in the protocol, the whole thing
would came to a crashing halt. And there
was even some concern about whether you
get it going again in the right way. And
so, we had to figure out how to solve
that problem. And that was the
contribution of Viewstamped Replication.
We come up with a protocol that it had
what we called the primary and the
primary was telling the backups what to
do
and we were carrying out a protocol that
was similar to two-phase commit to have
make this happen but if the primary
seemed to not be doing its job the
backups then carried out another
protocol where they moved to what we
called a new view in which a different
replica became the primary and of course
this had to happen in a way that
guaranteed that everything that had
reached the commit point in the previous
view made it into the new view with the
history was exactly the same as what it
had been before the primary failed and
so in that sense we were building a
ledger we didn't use that terminology we
thought of this more like a log because
that's what we used to call it in the
systems community when we were talking
about a single machine where you were
always writing stuff to the log so that
if the machine failed you could come
back up again and pick up where you left
off so now it was a log based in a
distributed system and we were really
thinking in terms of a file system but
the protocol didn't have anything to do
with the application we were really
building a ledger and doing so in a way
that guaranteed that the history going
forward was always preserved but a very
important point is we only thought about
what we referred to as benign failures
these were failures where machines were
either running or they were completely
silent
and messages might arrive they might not
arrive at all or they might arrive
corrupted but if they were corrupted you
could tell
so we didn't worry about
Byzantine failures we only worried about
these simple failures which were in fact
the main failures that happened at that
time because it was just the days of the
ARPANET and we were all friends
and we didn't have the malicious attacks
that showed up in the '90s once we had
an internet.
>> I think this was like a really great
that description of of of Byzantine
replication and and so in some sense
like this whole idea of of moving from
one view with one primary to a a new
view with the new primary
gave this birth to these view change
protocols which I think are now
everybody's using them but it's it's
it's quite amazing to see that you know
basically they they come from the early
'80s
anyway, right?
>> And this may be another little bit of a
digression but Professor Liskov you
mentioned that there was sort of in the
background there had been some work on
the on the theory side you know just
identifying what is the in principle
kind of you know best possible fault
tolerance one could perhaps achieve. And
so I I'd love to just hear your thoughts
on kind of theory versus practice theory
versus systems you know maybe both at
that time and how it's evolved over the
years and and how you see the the flow
of influence like in what ways is kind
of the work on the theoretical side
informed your work or other work on the
practical side and and vice versa.
>> Well, I don't know that I should talk
about the practical side and how it
influences theory.
But in my group I always told my my I
always told my graduate students they
should take theory courses.
You know theoretical computer science is
is the backbone of our field. We always
wanted to track what was going on in
there. The main thing that was impacting
my work was always understanding you
know understanding what they were doing
and also uh things like cryptography and
so forth which came to be so important
in not in those days so much but in
later work. And of course I was
fortunate to be at a place where Ron
Rivest was
and his colleagues you know and so
forth.
>> And I was going to ask about that
actually which was how how important was
the milieu of MIT for the for the work
that you did? Do you think if you'd been
in another strong department things
would have played it out in a similar
way or is the MIT imprint very strong in
some way?
>> Well, I I I can't answer that question,
but I really think you know, we have
many strong places and I think all the
top institutions could have done this
work.
But MIT is a wonderful place and we also
took teaching very seriously and I do
think teaching and research are very
closely connected because
when you teach well, you teach from
first principles
and when you do good research, you have
to truly understand. So, you're really
doing research from first principles and
it's also very important in research to
understand what you don't understand. I
always tell my students that there's
where you get the insight into where you
have to move and you don't want to have
an incomplete understanding of why
something works.
You know, you have to really understand
it completely and we always tried to
prove the correctness of these as we got
to these more complicated protocols. You
really you have to reason about them
carefully to make sure they really work.
>> I'm glad to hear you say that. I I I
couldn't agree more. You know, what
you're talking about teaching and
research, I sometimes describe teaching
as
increasing the number of people who
understand something from a smaller
number K to a bigger number N
>> Yeah.
>> and research is the special case where K
equals zero
where for the first time people are
understanding it sort of deeply.
>> [laughter]
>> That's a good way of looking at it.
>> So, I view them I I completely agree
with you, very synergistic activities
and and you know, that's kind of the
twin pillars of the the professor's
role, I think really.
>> Yeah.
>> So, returning to the to the research
side. So, Viewstamped replication came
out in the late '80s
and then there was sort of a period
where I think the focus of your group
turned away from replication to some
extent, still partly in distributed
systems.
>> We finished Viewstamped replication, we
published it at sometime in the late
'80s. That was when I came up with what
came to be called the Liskov
substitution principle,
but we had put that aside. Of course, it
was early days. It was not in any
commercial
uh environment yet. And also, you know,
Leslie Lamport
was working on Paxos,
and I actually heard him give a talk in
the '80s about Paxos, and I didn't
understand what he was talking about,
and I had certainly no idea it was the
same thing. But this was a mutual lack
of understanding.
>> Yeah.
>> The story I heard was well, in the late
in the '90s, the Google file system
paper was published,
and that paper used replication and
talked about using Paxos, and I was kind
of peeved because one of my students was
working there, and I thought he could
have talked about view stamp
replication. But the story I heard was
that Bill Weihl, who had been a student
of mine in the '80s, happened to be at
Google, and he was looking at what was
going on in the Google file system, and
he said, "Oh," he said, "that's view
stamp replication."
>> Mhm.
>> [clears throat]
>> And they really were the same protocol
developed in two different places.
It was just funny how we kind of
couldn't see that for that period.
>> Fascinating. It's interesting how there
there's sometimes just moments in time
where it feels like the right time for
certain work to be done, and often it
happens at sort of multiple different
sort of groups doing it at
>> in
two places, and the same idea does get
discovered discovered more than once.
Yes.
>> Yeah. So that seems like a great great
example of that.
>> [snorts]
>> But then you did get in the late '90s,
you did get pulled back into
replication, right? In the famous PBFT,
practical Byzantine fault tolerance, um
protocol. And my understanding is that
was at least in part inspired by DARPA
uh BAA, you know, a sort of request for
proposals. So would love to hear a
little bit about that story, and and
then they maybe relatedly just perhaps
the importance of collaboration outside
of academia, whether it's with, you
know, kind of government funding
agencies or industry and how maybe
that's
if that's been important in your work,
how that's been important.
>> Well,
the way
PBFT came about, practical Byzantine
fault tolerance, is I had a student,
Miguel Castro, who was looking for a PhD
thesis,
and I suggested to Miguel that he look
at the RFPs that DARPA had put out
and see if anything interested him,
and he found an RFP that was looking for
ways to handle the malicious attacks
that were going on on the internet. And
so, he came to me and he said, "Why
don't we see whether we can figure out a
way to do replication
that handles these malicious attacks?"
And that seemed like a great idea.
I mean, I'm not saying it wouldn't have
happened anyway, but the fact that DARPA
had recognized that this was a serious
problem, the problem of malicious
attacks, and was looking for research in
that area,
certainly was something that caused this
work to happen in my group at that time.
And I think that DARPA was a very
important between DARPA and NSF. I mean,
they were the reasons that research was
getting funded all those years. They are
one of the very important backbones of
why we have the internet that we have
today. Without that research funding, it
would have been much more difficult to
have done all that work. So, that's how
we got started on Byzantine fault
tolerance.
And then, what we did was we simply
started from viewstamped replication. My
group all knew what viewstamped
replication was, and I don't think it
was understood at other places. And so,
we had that stepping stone that other
people didn't have, and we used it. It
just seemed like it was a natural thing
to do. We had this algorithm that worked
in for benign failures, okay, let's add
Byzantine failures and see what happens.
And we also knew from the theoretical
work that we were going to need 3f + 1
replicas instead of 2f + 1. But again,
we're looking for a practical protocol
that people will really use in practice.
So, we started from Viewstamped
replication, but it's a very different
problem once you add those Byzantine
failures because
you have to be prepared for replicas
that lie. And of course, you also have
to worry about malicious attack on the
content of messages.
For that, of course, we immediately
started using cryptography because that
was the way to make sure the messages
can get from here to there and you knew
who they were coming from and you knew
whether they were correct or not.
The bigger problem that we were dealing
with was the replicas that lie.
And of course, that's why you need 3f +
1 replicas instead of 2f + 1. And the
biggest problem you have there is that
the primary might lie.
It felt to me like we were in a funhouse
full of these distorting mirrors. And
you had And you had to really think
about things in an odd way to come to
grips with this. But in the end, the
solution was a protocol that was
strongly based on Viewstamped
replication. It had one more um phase in
the replication protocol because the way
you handle the problem is you never
trust an individual replica. You only
trust the group.
And the group has to consist of a
sufficient number of replicas to be able
to prove that this is what really
happened.
And of course, we need a way that this
proof can be offered at a later point in
time. And for that, we use certificates.
So, a certificate consisted of 2f + 1
signed messages all stating the same
thing. And that would be a proof that
you got to a particular point in the
protocol.
And the extra step happened because the
primary could only suggest the next
step.
Then 2f + 1 replicas together have to
produce a protocol that says we're doing
this next and putting this next in the
ledger.
And then you have to do another phase to
actually commit that step.
And that's how you get this this
protocol.
But you know, it's easier in hindsight
to see it than it was at the time. It
took quite a bit of thinking to come out
with it. But that was still it was the
underpinning of how we came up with
PBFT.
>> Yeah, and just
for audience's benefit, I mean this idea
of sort of certificates of 2f + 1
signatures, I mean this has been a very
very influential idea in many of today's
major blockchain protocols. Indeed, this
is
this is how they prove you know, the
ordering of their transactions to to
others.
>> But of course, we didn't invent
certificates. They were coming out of
theoretical work.
>> That's right. Correct if I'm wrong, but
PBFT to me felt like the bridge from
that theoretical work
to practical systems, right? I mean my
sense just, you know, from reading the
PBFT paper and all of the reactions
around it
was perhaps there was this aha moment.
It's like, oh wait a minute, this isn't
just to prove the theorems. Like we can
actually sort of build a system where
this is really how it's going to work.
Is Was that what happened or
>> I mean, we were just, you know, picking
up stuff from theoretical computer
science and using it as we needed it.
But it [snorts] you may be right that it
was thought of as this work is
interesting, but you know, who cares?
>> [laughter]
>> Um the theoretical works and now you
could see how it really fit right into a
practical system. We were happy that
there were techniques that people had
developed that served our needs. Still,
you can see the bridge between theory
and practice. If we hadn't been aware of
the theory,
then, you know, we would have been real
really stymied in what we were doing.
>> Yeah, I I wanted to add that sometimes,
you know, good systems work that have
benchmarks that show, you know, good
actual practical results. They change
people's mind. They say, "Oh, this this
technology can actually be used."
There's a difference between having a
theoretical paper saying it's possible
and seeing, you know, good benchmarks.
>> what you're saying.
>> Saying that the you know, file system
works well.
>> I I was never worried about that, I see.
But of course
>> [laughter]
>> I was just the one who wanted to find
the stuff that would make the system
work.
And it it was hard, but it was a lot of
fun.
>> So being a certificate actually has been
a very cool line of work in the last
maybe five to seven years or so in
distributed computing around
accountability, which is when something
goes wrong, can you tell if it went
wrong and who might be responsible for
it. And so in in particular, like if you
want to think about Byzantine fault
tolerant systems
and say, "Well, what would happen if
actually you did have too many malicious
actors, right? What could happen?" And
you could have a consistency violation.
But accountability says the only way to
create a consistency violation is by
signing lots of inconsistent things. And
then through inspection, you can
actually identify bad actors who double
signed on different conflicting states.
I could imagine this being developed
maybe 20 years ago, but it's mostly been
developed in the last five to seven
years.
So analyzing PBFT style protocols not
just in the regime where the number of
faulty nodes is small, but also where
it's actually bigger than the than the
threshold. So
>> You know, I'm not aware of that work,
but it does sound interesting.
>> Yeah, it's very cool.
>> The other thing I wanted to ask you
about PBFT or one of the things that I
really was very helpful for me when I
read these papers
is not only the uh replication protocol
itself that has certificates and 2f + 1
that we talked about. Um but also kind
of this observation that once you have a
consensus protocol or a replication
protocol, you can actually run different
types of execution engines. So you
mentioned a file system as one example,
but you could run other types of uh
services.
Um so maybe you could talk a little bit
about kind of this uh view of a generic
service as a replicated service.
>> Well, I think that's
I mean that was there from the start. Of
course, we were thinking about a file
system when we did view stamp
replication, but it was always clear
that we really weren't the application.
We were actually the piece that gave the
application the right information. And
so, we didn't really care
we we just wrote into the ledger, you
know, what the operation was that was
being requested, but we were not in the
least bit interested in what it meant to
execute that operation.
So, it just seemed like a good
separation of concerns. And I think even
in the beginning we understood that you
wanted to look at it that way because
you didn't want to limit yourself to one
application. You wanted to find this
generic thing that would work for many
applications.
>> It's another variant of the modularity
principle that you were proposing
earlier, perhaps.
>> I I think it was
I think it was just sort of
in a way obvious that you wanted, you
know, you mentioned state machine
replication in the in the email you sent
me and we knew we were working on state
machine replication. And state machine
replication has the idea that whatever
it is that you're doing, that's just the
thing, you know, and you instead just
think about the order and this is
operation number 25 or something like
that. So, I think it was very
fundamental even in view stamp
replication to what we were doing.
>> Yeah.
>> today is a very common understanding,
right? This this separation of different
layers of consensus and execution. And
it's it's really cool to see that these
are kind of ideas that again evolved
from from these these work from the '80s
and '90s. Yeah.
>> And then even more so, I mean,
I would say Turing complete blockchain
protocols like, you know, Ethereum,
Solana, etc. They're they're almost like
literal implementations of the fully
general state machine replication
problem. Right? They're not trying to be
kind of a specific application of state
machine application, they're trying to
actually just implement it in full so
that then a specific smart contract can
then be, you know, in some sense a
special case, a special instance run in
the general sort of SMR protocol. So,
these blockchain protocols are in some
sense, you know, one of the more literal
embodiments, I think, of the general
state machine application problem that
we've seen today. Just super
interesting. So.
>> I think it it was when Miguel and I
finished the work on practical Byzantine
fault tolerance, we thought
that at some point people would start to
use this.
Of course, for view stamp replication,
it was a delay of about 10 years before
people started to use it.
And then along came blockchains.
>> [laughter]
>> And
Well, that [snorts] was very funny.
>> There was a long period of time, I mean,
so right, so blockchains were sort of
launched with Bitcoin protocol, which
actually looks
rather different than PBFT and and most
of the other consensus protocols anyone
had thought about to that time. And it
took, I think, you know, the the
blockchain community a number of years
to realize that PBFT and and the the
sort of subsequent protocols in that
family were exactly the right tool for a
lot of the problems that they're trying
to solve. But at this point, 2025, it
is, I think, very well understood among
blockchain practitioners and researchers
that really PBFT and protocols like it
are the foundation for what those
protocols are trying to do.
>> One other thing I'd love to talk a
little bit about is just um do you have
advice for the younger generation? So,
what's someone who loves computer
science, loves research,
you know, maybe maybe distributed
systems, maybe more broadly, thinking
about computer science, you know, wants
to do important work, wants to have an
impact. What would you suggest as kind
of a mindset as an approach?
How to get started?
>> Computer science is in a very strange
place right now with the advent of AI
and not really understanding
uh where we're all going with this.
I think that as far as research is
concerned, there's a huge amounts of
research to be done. And I can't help
but think about all the systems research
that's lying under all the AI stuff.
And all the problems that are coming up
that make for very interesting systems
research. So, I don't think research is
in trouble. I am a little worried about
computer science as a as a field for
young young people going to college and
should they major in computer science
and so forth.
And I don't understand the limits of
what AI can do. I can easily see how AI
can write a little program for you if
you give it a specification.
I can easily see how that program might
be wrong.
And it's very easy to see that we're
going to need a lot of verification
tools in order to make sure that program
is right.
There was a letter in The New York Times
recently by Mary Shaw and somebody else
about what's the future for coders
that made the point that um
the students really need to understand
how to write those programs themselves
or otherwise how will they know that AI
didn't them right or wrong.
And that's correct. I think, you know,
there's going to be a lot of research
going on whether this is a field that
you can get a good job in and do the
kind of coding work that people used to
do.
What Mary was saying, you know, is
you're now managing more the coding and
you're working at a higher level. That's
that's a good job. The course that I
developed at MIT in the 19 starting in
the late 70s with John Guttag, which was
a course about how do you build big
programs. And it was all about design
and modularity and specifications and
verification.
Maybe that's exactly what we're talking
about as the future for coders. They
have to be working at that level, not at
the how do I write that little for loop
with the
you know,
>> Yeah. Is it a semicolon or a comma, or
yeah. Exactly.
>> So, I I still think computer science is
a great field and I think there's a lot
to be done. And the the problems that we
solve will change as the future goes
forward. I am very worried about all the
bad behavior that we
uh enable, but then bad behavior is
enabled by most anything, so uh
>> [laughter]
>> it's not really our fault, but it
worries me and I really think to the
extent that we can figure out ways to
modify or con- contain the bad behavior,
that's another good research area.
So, what am I saying? I've said there's
great research to be done.
And a lot of it's in the systems area.
>> I couldn't agree more. I think that's a
that's a great uh
great note
>> note to close on, I think. Yeah.
>> Okay, good. I'm glad to hear it. Anyway,
so I mean, this has been fun.
>> It's been an honor to have you,
Professor Liskov. Thanks so much for
Thanks so much for taking the time.
>> You're welcome. And nice to talk to you.
>> Take care.
