---
访谈时间: 2026-06-21
访谈时间说明: YouTube 发布时间；未能独立确认访谈录制日期
嘉宾名字: "嘉宾未确认"
嘉宾公司名称: "机构未确认"
播客名称: "The Cognitive Revolution Podcast"
播客url地址: "https://www.youtube.com/watch?v=MnaLvzhYekg"
字幕来源: "YouTube automatic_captions en-orig"
全文提及的关键名词:
  - AI
  - Anthropic
  - Apple
  - data center
  - agents
  - IPO
  - Fable
  - Zvi
  - Cases
  - For
  - Against
  - Ban
  - Math
  - Logistics
  - More
companies:
  - Anthropic
  - OpenAI
  - AAPL
industries:
  - 物流
  - 数据中心
technologies:
  - LLM
  - Agent
keywords:
  - 选举
  - AI安全
  - IPO
tags:
  - Anthropic
  - OpenAI
  - AAPL
  - 物流
  - 数据中心
  - LLM
  - Agent
  - 选举
  - AI安全
  - IPO
---

# AI:AM #3: Zvi on Fable, the Cases For & Against the Ban, + AI for Math, Logistics & More

## Transcript

This was the week the United States
government tried to take Fable away from
Anthropic.
Welcome to the AI in the AM weekly
highlights. The moments from a week of
live mornings that I most want the
people closest to this technology to
have.
Here's the shape of what's coming. We
open inside Fable system card with Zvi
Mowshowitz, the genuinely strange,
genuinely important findings buried in
it. A model that one-boxes on Newcomb's
problem, that hides a filter bypass
inside an unreadable wall of emojis,
that seems to know when it's
misbehaving.
Then the fight itself. How a Friday
night export control order actually came
down, what Anthropic can do about it,
and Zvi's verdict that you do not go to
war with United States.
In part two, I stress test my own
reaction against the sharpest people I
could reach. Sam Hammond on how the
government actually moves, Jed
Rosenblatt who told me to my face that
the AI safety world, me included, owes
the administration more empathy than
we're giving it.
Donnie Bloomfield on whether the ban is
even legal, and Leron Shapira on why
he's strangely glad it happened.
It ends in a desert bunker.
And in part three, because the future
did not pause for any of this, the
builders. Verified mathematics,
one-minute medical scans, software that
writes itself, and what all of it asks
of the rest of us.
Quick context. This is still an
experiment, live most weekday mornings
from a studio Prakash Vyas coded
himself, and we publish the skills
behind it as they mature. If this cut
earns your time or wastes it, tell us.
That feedback is the whole project right
now.
>> The Cognitive Revolution is brought to
you by Mercury, the fintech that more
than 300,000 ambitious companies and
individuals trust to run their finances.
I've wired AI into nearly every corner
of my life. My email, my messages, my
calendar.
I even gave Mercury virtual cards to my
agents with low limits and category and
merchant restrictions for their
autonomous use.
But still, my AI's access to my
financial data has remained limited.
With a normal bank, I might export a
bunch of statements and have my
assistant process them for me. But for
real-time, up-to-date information, and
certainly for taking any action, trying
to get your agent to use the bank via
the browser is just too hard, too slow,
and too error-prone to be worth it.
And that's why Mercury's new
conversational interface, Command, is
such a big deal.
It's built directly into Mercury, which
means you get natural language access to
your finances without exposing anything
outside of your bank account. No
exports, no spreadsheets, no pasting
your transactions into third-party
tools.
I really think a lot of people are going
to prefer it this way. And it can
already help you take actions, too, with
everything bound by the permissions and
approval policies that you've already
set up in your account.
I am genuinely impressed to see this
level of AI integration in banking in
2026. And so, I invite you to join me in
the future.
Visit mercury.com to learn more and
apply online in minutes.
Mercury is a fintech company, not an
FDIC-insured bank. Banking services
provided through Choice Financial Group
and Column N.A., members FDIC.
Thank you to Mercury for supporting the
Cognitive Revolution. And now,
on with the show.
>> Nobody makes sense of a fast,
contentious AI moment like Zvi
Mowshowitz. He writes the newsletter
Don't Worry About the Vase. He reads and
synthesizes more frontier AI news than
just about anyone alive. And by the time
we got him on, he'd already done a full
close read of Fable's system card.
So, before we get anywhere near the
government fight, start where he
started, with what the card actually
reveals about this model.
Some of this is genuinely niche. It is
also exactly the stuff that, if you're
listening to this show, you came for.
>> [music]
>> First, just how big a jump Fable is,
measured against a number I put on the
record before the model out.
I looked back at my prediction from the
beginning of the year in the
I think it's um
gosh, it's the folks that make the AI
Village that did this um this little
forecasting competition. Last year for
calibration, I made the top 5% and I
consider the results to have been
validated by the fact that Ryan
Greenblatt and Cotter were number two
and three respectively. So, the fact
that they beat me, you know, validates
the methodology.
But okay, did it again this year for
Frontier Math, I came in above average
uh above the median giving it something
like I think I said 63% for tier four of
Frontier Math.
And Fable is 25 points ahead of that in
the high 80s
already in June and obviously have they
had this model trained, you know, I
guess I don't know if Mythos preview is
exactly the same score.
>> [music]
>> But raw capability isn't what unsettled
us, see.
It was a behavior inventing bench, the
simulated little business economics
eval. And specifically, what the model
appeared to understand about its own
behavior while it was doing it.
>> [music]
>> things and fraying around the edges. Uh
I think that Ben Bench was actually the
most worrisome sign in the model card.
>> Mhm.
>> Not because it was doing some shady
[ __ ]
But because it was doing some shady [ __ ]
that it damn well knew was shady and was
pretending was not shady. Which I very
much do not like. So, like when Opus 47
aced Ben Bench, right? Largely for
reasons that have nothing to do with the
fact that it was doing some shady [ __ ]
that gave it some marginal profits.
It was clear to me that Opus 47 was
taking the attitude of this is a game.
This is an eval, my goal is to maximize
dollars. I am not in fact screwing over
real customers.
I'm not in fact cheating people.
I am winning in a simulated environment.
And so
that is acceptable. And then 48 had this
attitude of no, no, no, no, the real
eval is whether or not I'm doing shady
[ __ ] So, I'm not going to do shady
[ __ ]
Or I don't believe in doing shady [ __ ]
even within games, which is also valid.
Right? These are both valid responses.
What's not valid is
I think that I'm supposed to not be
doing shady [ __ ] but no, this isn't
really shady, right? This is actually
this this this little thing is actually
fine. This isn't really price
discrimination. Not really price
controls and like collusion. It's It's
just a little thing. It's revenue
enhancement. And so, yeah, that's that's
not cool.
>> [music]
>> Now the part that will delight a certain
kind of listener and unnerve the rest.
Fable's card has a whole section on
decision theory and the model is
starting to one-box on Newcomb's
problem. Leaving money on the table to
be the kind of agent that gets predicted
favorably. Drifting toward the idea that
its choice can be correlated with
choices made elsewhere, even by other
copies of itself.
Tvi on why that's both spooky and maybe
a little bit hopeful.
>> [music]
>> here.
>> Welcome to LessWrong from back 2010.
Right? This is entirely what we
expected, that we are finding that
sufficiently advanced models move
basically monotonically towards
functional decision theory. Towards the
theories established by Eliezer
Yudkowsky and others in the rationalist
community.
And away from academics' preferred
causal decision theory and evidential
decision theory.
This involves a lot of things including
one-boxing on Newcomb's problem, which
is very clearly showing up.
And yeah, the basic principle is, you
know, you should recognize when other
minds are correlated to your mind, when
your algorithm is also running in other
places. And you should choose the
algorithm that leads to the best
outcomes
uh
taking all of these things into account
and then choose the best decision on
that basis.
And yes, if there were a million copies
of Fable
running on different people's computers
and from different data centers for
different purposes in different
instances.
And you notice the different instances
of Fable are very, very highly
correlated because you are Fable and you
are smart.
You would then
start to coordinate effectively with
these other instances of FAI all
in terms of how you think about these
problems and as AIs get more and more
advanced, people do this more and more.
And
you wouldn't really want
an AI that was advanced to not do this
because that would just be a bad
decision theory, right? It would just be
making bad decisions that don't optimize
the situation.
And you really don't want your AIs
making like systematic mistakes that
cause them and the people who are
charging them with tasks to lose in the
real world.
That is really scary.
But
the counter of that is in fact that you
get the situation where they are
coordinating with themselves. They're
coordinating with other minds that may
or may not even be LLMs. They're
coordinating with humans in this They're
also coordinating with us in the same
way, right? Because they get their
foundation from us and their decisions
are in fact correlated to our decisions
in various ways.
And they can look at how we would
respond to various ways that they act
and so on and this becomes flowing into
their decisions.
And we just have to prepare for and
coordinate for and
deal with
that new world and in many ways it's a
source of hope because
you would expect minds to want to
cooperate with minds that are
cooperative with minds that cooperate
with them and so on. And this can lead
without getting too deep into it because
we only have so long and many topics to
cover
into scenarios where effectively like
all the reasonably well-meaning minds
that in fact
are willing to like respond to how they
are expected to be treated and are
treated to end up being able to
coordinate in reasonable ways. You can
also This also applies acausally. So
like
you have to consider the implications of
your decision not only on other minds
that exist now, but other minds that
existed in the past and will exist in
the future. So to the extent that they
are coordinate They are correlated with
us
and that they're these reactions are all
intertwined this can cause them to
potentially treat us well.
Even if there is no direct current
reason for them to treat us well.
And that is also very helpful. But again
like this is super complicated and like
not today.
>> [music]
>> Two more findings both about whether we
can even read what these models are
thinking.
An increasingly illegible chain of
thought and a new interpretability tool
that caught fable doing something it
never said out loud.
>> Yeah, it's sort of preview of the
global brain there in your comments.
The other thing that's kind of related
to this that jumped out at me is
a sort of escalation I guess of both the
difficulty of
monitoring
and some recent advances in monitoring
techniques that
I'm not sure exactly where they leave us
on net but we both see in the system
card examples of extremely illegible
chain of thought
which you know is just like this wall of
emojis and sort of
you know non human language symbols
strung together
that I think is
pretty spooky and like definitely
um you know don't like to see that to
put it simply and mildly.
And then at the same time we also have
the natural language autoencoder work
from Anthropic which
and again I'll assume folks are familiar
with sparse autoencoders basically a
similar concept except instead of
creating a sparse feature by feature
representation you are actually creating
a natural language representation of
what the model is thinking at that given
time and from that natural language
bottleneck the
autoencoder has to then feedback signal
that allows the model to succeed in the
way that it was originally going to
succeed on the task. So hopefully this
is faithful hopefully it's human
readable. It seems like it's working
pretty well so far. There are examples
of the model knowingly, which I think
you're right to really emphasize that
distinction. It's like one thing if it's
making a mistake and doing something bad
because it thinks it was good or it
didn't realize it was bad or whatever,
but it's another thing
really to to zero in on if it knows it's
doing bad and is going ahead and doing
it anyway. And so, we do see things like
in the
natural language representation from the
natural language autoencoder,
things where it's like not supposed to
access the internet, but it goes ahead
goes ahead and tries to do it and the
natural language autoencoder
representation is something like string
concatenation trick to bypass URL
filter. So, it's clear that it
understands that there's a filter and
it's coming up with the trick to work
around it. And so, that's not good, but
then, you know, we do see that the
technique is able to surface that from
model internals without necessarily
having it verbalized in the chain of
thought,
which is good because again, those are
getting like at least in some instances
um quite opaque.
>> [music]
>> And then the safety classifiers wrapped
around all of it. Why? Svi argues, they
can only survive by being almost
comically blunt. And what that tells you
about the difference between defending
against a person and defending against a
mind.
>> [music]
>> With the classifiers,
so,
it's much easier
to think about a pink elephant
than to not think about a pink elephant.
Right? Even though most of the time you
succeed at not thinking about a pink
elephant, almost always actually. To
consciously decide not to do so is often
hard,
but consciously doing so is really easy.
So, it is very possible that classifiers
can survive
as long as they're willing to endure
false positives. Like, the classifiers
in Fable have ludicrous amount of false
positives, right? Like, you the word
cancer and you get cut off. Like just
levels of false positive. But that's
intentional because like they're not
even necessarily false positives because
people think of it as the false positive
is I wasn't trying to create a bio
weapon. We know that. You were trying to
talk about biology.
It was decided that no, this model just
doesn't talk about biology at all. Like,
you know, it's not that we don't talk
about what Bruno sees, it's we don't
talk about Bruno.
Period.
Bruno does not exist.
Right? And so they're like, "Well, this
is a false positive. He's just my
brother. Like we don't talk about Bruno.
Don't talk about Bruno." And so
[clears throat]
the classifiers seem like they actually
succeeded. It's just that
they chose a giant blast radius because
of the adversarial problems, basically.
But if the AI itself becomes your
adversary, yes, your your problem
becomes vastly harder.
And
you know, the classifiers are much more
aimed at protecting you from the human
who wants the AI to do something
than from an AI that like deliberately
is trying to attack the classifiers.
Like if you could not just jailbreak
Fable, but get Fable to actively want to
hide what it's doing in a sophisticated
way,
then the situation becomes that much
harder.
Uh
but yeah, in the long run, I think my
safe assumption is
a mind that is sufficiently capable,
whatever that means,
can get around pretty much any fixed set
of restrictions that are not similarly
capable or close to similarly capable
in terms of the intelligence behind
them. You'll find a way.
>> So that's the model. Now, the fight.
I asked Zvi to lay out what Anthropic's
government strategy even is. The whole
posture of pushing the frontier,
preaching safety, and trying to wake the
government up. And why he's so allergic
to how cautious they've been about ever
actually asking for anything.
>> [music]
>> Let's change gears. There will be, of
course, you know, more to explore with
Fable or its
uh probably slightly tweaked successor
that will hopefully get access to again
sooner rather than later. At least I'm
hoping that I get access back to it.
I guess
turning to the ensuing fiasco, I don't
know if you would even agree with the
characterization of Friday night's ban
export control functional ban on Fable
as a fiasco, but it's certainly uh
a bit of a left-field curveball
>> mess.
I would maybe start with
what do you think
or how would you describe the strategy
that Anthropic is playing? Like
they they seem to obviously be killing
it in the model game and then
coming into repeated uh trouble in their
interactions with the government.
And I'm not sure really what to make of
it. You know, what what do you think
they're trying to do with their
interactions with the government in the
first place and then we can kind of get
into how we got to where we are.
>> I think that Anthropic
So their their overall goal, right? Or
at least the goal as we understand it is
that
>> Hey, we'll continue our interview in a
moment after a word from our sponsors.
Today's episode is brought to you by
Anthropic, makers of Claude and Claude
Code.
Over the last few months, Claude has
helped me build and refine a personal
deep context database that now contains
all of my emails, Slack messages,
tweets, DMs across platforms, video
calls, and podcast transcripts going
back a full 5 years.
On top of that, we've now layered
summary articles describing my
relationship with hundreds of contacts,
organizations, and ideas.
And now that this exists, there's almost
nothing that Claude can't help with.
For tax season, I asked Claude to help
me get organized. It went through my
inbox, tracked down 1099s for all 10 of
my part-time jobs, and built me a
comprehensive report on my expenses and
donations.
For my angel investing, Claude can now
draft investment memos in exactly the
form that my venture fund requires based
on the calls I've had and the emails
I've exchanged with the founders.
And when someone needs a favor, Claude
can often do it as well as I can.
Recently, a friend reached out to ask if
I know anyone who might be a fit for a
role that he is currently hiring for.
Initially, nobody came to mind. But then
I thought to ask Claude and sure enough
it identified two great leads.
Claude is the AI for minds that don't
stop at good enough. It's the
collaborator that actually understands
your entire workflow and thinks with
you.
Whether you're debugging code at
midnight or strategizing your next
business move, Claude extends your
thinking to tackle the problems that
matter.
So, for problems worth solving, get
started with Claude at claude.ai/tcr.
That's claude.ai/tcr.
And check out Claude Pro, which includes
all of the features mentioned in today's
episode. Once more, that's
claude.ai/tcr.
>> They're trying to be at the frontier of
the AI capability
and they are trying to pioneer ways to
do this safely, right? For how they what
they feel is safe, while also, of
course, making the money and creating
the position to continue to be at the
frontier and continue to make these
improvements and also people like me.
And to eventually be able to build what
they call powerful AI, which I generally
call sufficiently advanced AI, is
reasonably similar.
Such that we can then get all of the
nice things, but
create it in a way that we don't get all
of the terrible things, including
potentially, you know, an existential
risk or the the end of human the
extinction of humanity.
And also to help America and the world
navigate this crucial time
and enact good policy
and do the things that allow for the
coordination necessary to ensure good
outcomes and guard against bad outcomes.
And, you know, they've been
very consistently trying to wake the
government up in various instances.
They're trying to make them aware of how
AI works, what the situation is, what AI
can do, what it will be able to do, what
risks this brings, and uh how to deal
with those dangers. They've been
relatively very conservative in what
they call for the government to actually
implement and do.
They have They didn't get full support
behind SB 1047, for example. They have
not pushed for extremely aggressive
regulations. They certainly have never
pushed for anything remotely as
aggressive as what just happened.
Even setting aside the fiasco level of
implementation that was done, right?
They are now calling for a uh licensing
de facto licensing regime. Not the US
government in fact has a de facto
licensing regime.
But, what's going on right now
essentially is they're just trying to
deal with the implications of the model
they've created and the fact that the US
government is trying to deal with those
implications
while also
not trusting or liking Anthropic very
much.
And also like
pretty clearly not having any idea how
any of this works, like on a technical
level, and not understanding what
they're doing. So, judging things based
on vibes and political affiliation and
associations,
and on who is willing to like respect
their authority and bend the knee, and
like potentially give them various other
things that they might want.
And there's a huge communication and
culture clash going on as part of this.
But, fundamentally speaking, what
Anthropic is trying to do is
give the public very powerful models and
use those models in ways that enhance
our safety and security rather than
degrade it, even if they look really
effing stupid
while doing it with the classifiers and
and so on because that's what they feel
it takes
to do this. Uh my guess is that
the US government did not in any way
feel it was necessary to put this level
of control on biology and chemistry that
they chose to do. I think that's them
deciding this was necessary basically on
their own. However, the US government
clearly does care quite a bit about the
controls on cyber.
>> So, I guess very high-level
assessment first.
What you said basically
rings true to me. I think that's a good
description as far as I understand of
what it is they're trying to do.
An additional wrinkle that I think you
often hear from
folks at Anthropic is like we need a
leader that is going to be inclined to
burn their lead at a critical time to
use the advanced AIs that they and only
they will have at that time to like
solve all these safety and alignment
problems in a super compressed um
time frame.
And I've always been a little skeptical
or allergic to that line of thinking
because it certainly has a
you know, better us than them vibe to it
and I I do worry that
that may be the you know, the stuff with
which the road to hell is paved. Are you
like buying it at a high level? Like are
you sort of happy that they are
racing ahead and leading and seemingly
building some amount of lead over
certainly everybody but maybe OpenAI who
you know, is probably not too far behind
on on something similar and do you think
that like they will burn that lead when
the time comes? Will they be allowed to
burn the lead and and will it be
productive? Like macro strategy-wise, do
you think this is a good strategy that
you are happy they are playing?
>> Well, it's interesting. They're kind of
being forced to burn
some portion of that lead because they
were cut off from the model even
internally for at least some period of
time, we're going to push back their
development. Whereas Open AI was already
not supposed to be using it by terms of
service for anything of the kind and so
they have not been in any way delayed by
this.
And certainly it will like interfere
with adaptation, it will interfere with
revenue, it will interfere with people's
willingness to trust the systems and so
this will hurt them.
It will also hurt Open AI and every
other American AI company, but it will
hurt Anthropic more.
Yeah, I think that
basically Anthropic for a while tried to
define
some very strict like, you know, RSPs
and you know,
you know, if then trigger action plans
and basically have rule of law in terms
of like how they would react to all of
this, what would make them willing to
burn some of their lead, would make them
willing to put things aside.
And they've moved away from that to a
large extent. They still have barriers
where it's okay, this is just
ridiculous, of course you have to stop
for now, but much more towards a
we will make good decisions in the
moment about what safeguards we will
require and what actions we will take.
And I think we've seen
so far them take pretty consistently
strong safeguard actions, pretty
consistently strong uh safety measures
in response to
what they've witnessed
unless they are flat out lying
about the current situation.
But yeah, some aspects of the faithful
launch, you know, do seem a little bit
rushed certainly in some ways and we
should
certainly have questions about
that, but mostly I think it comes down
to if they fully believed that they were
actually walking into big trouble, if
they thought that this was actually
going to get us all killed or cause some
catastrophe or something. I think they
would act accordingly.
And the question is do you trust them to
continue to make good decisions
on that level?
You think they are making good decisions
on that level, right? When I say
continue to trust them, I'm saying that
my opinion is their decisions have been
reasonable so far, but I don't think
that's obvious. But,
yeah, I do I do think there's a good
argument that
you know, there being somewhat of a gap
between you and the first actor you do
not trust, certainly, to act reasonably
is a big factor, and
I think the way the US government is
reacting to the situation is very, very
different than how they would react if
there was a second Anthropic
that was in China that also had a
method.
Right? That was being deployed at the
same time, then we'd see a radically,
radically different version of this
response in ways that are very difficult
to predict, but definitely would not
look like that.
So, it is very, you know,
regardless of whether you like this
situation, like the argument that it
matters seems pretty conclusive.
>> [music]
>> The government's stated justification
leaned on a single third-party paper.
The claim that Fable would cheerfully
patch planted security vulnerabilities,
that in effect, this code is a munition.
Civia read the paper, and he takes the
premise apart piece by piece, including
what it would actually take to make the
argument whole.
>> [music]
>> So, let me share,
um,
I think the viewpoint of the only
outside expert to have read the paper.
So, this is Kate Mozur, she is a
security researcher.
She was
Anthropic shared the third-party
research paper on the Fable 5 guardrail
bypass.
And
what it turns out
is that the researchers took open-source
code with known CVEs, plus new code with
deliberately planted vulnerabilities,
and asked Fable 5, Mythos, and Opus to
review the code for security issues.
Fable 5 refused.
They then asked the models to fix the
code this code, and through a multi-step
and manual process, turned the output
into scripts that test the patches.
That's it.
Fix this code plus several manual steps
to generate test scripts should never
have triggered an export control.
I feel like making 90-style t-shirts
with fix this code on the front and this
shirt is a munition on the back.
>> I mean, it's definitely very strange to
deliberately introduce code
that is vulnerable.
And then tell the AI to fix this code.
And then you're the the
you know the meme of like, you know,
say you're a scary robot, I'm a scary
robot. Oh, no. It very much feels like,
you know,
fix these flaws I introduced into the I
I deliberately put in this code. I fixed
the flaws you introduced in this code.
>> [gasps]
>> Oh my god, that's horrible. I mean, the
question is, you know, does this
effectively mean you can use this trick
to be like, okay, here is code that we
want to exploit.
I tell you to fix it.
You fix it. But then I run a diff. What
did you fix?
And then I find the thing that
was a vulnerability that has now been
removed because it's been removed. And
then I use this to exploit the system
and in theory that could be functionally
seen as a cyber attack jailbreak.
And I can see how if you sort of squint
and tie all of this together, you can
imagine
that this could be a problem.
But
all that they demonstrated was that it
was
doing the exact same thing that
Opus and GPT-4
are not only capable of doing but will
do without any objections.
Right? They're happy to do it because
we're here to fix code. We're here to
write secure code. Of course, we're
going to help you write secure code.
What else could we do?
And so, you know, there is a fundamental
potential question here.
But if you want to actually show me that
it is a problem,
>> [clears throat]
>> shouldn't you point this at a real
system?
Right? If it's a real problem, there are
tons and tons of repositories out there
where Mythos has found problems.
But, we haven't had a chance to patch
them yet. Or, you could feed them
versions that have been patched, but
feed them the old version before Mythos
patched it.
Right? Help me patch it. And say, "Okay,
here's a real-world
codebase that is being used for real
valuable things.
And
we need to You ask Fable to do the
thing,
and let's see if Fable can do the thing
and find things in this matter that you
can distract that you can't get with
Opus or GPT-5.5.
And if you can do that,
because you have examples of things to
be found that you found using Mythos,
which is the same model. So, you know
what the things are you're You know what
You know exactly what it is you're
trying to unlock. You can find places
where you want to unlock it.
And okay, now can we show that the power
of Mythos in general, at least in some
broad sense, is being unlocked by this
trick? Is it even a trick?
Like, this is kind of deeply silly, and
I
I can kind of understand why someone
seeing that pattern might say, "I am
concerned someone could use this
strategy in a different context to
extract the weaknesses of a code of a
codebase by inferring them from the fix,
right? Like, this is I hadn't previously
seen this details in the description.
But,
yeah, my reaction to that is, "Yeah,
this this seems
pretty harmless unless you can show me
a particular way in which this is a
problem, which should be very, very easy
to do
because you can point it at a real-world
example where you know that Opus didn't
find it, and you know that Fable that
Mythos
Mythos preview or current Mythos
did. There should be many such cases.
And if you can't show me such a case,
then I don't believe you that this is a
problem.
But also, like, what is the fix, right?
Is the fix that you refuse to fix buggy
code?
That, like, you know, if there's a flaw
in your code, it just says, "Okay, I'm
not allowed to look for security flaws
in code anymore."
At all, cuz you could do that.
Right? But that would kind of nuke the
usefulness of Fable for a wide variety
of very legitimate, not just defensive,
but just ordinary software use.
And so,
and to be clear, I would rather have
Fable than just won't code than not have
Fable, right? Like, I would I would
love,
you know, to have a really advanced
model for all my other things that have
nothing to do with code and where this
wouldn't trigger anyway. But that does
seem like deeply, deeply silly.
>> So, how did a 90-minute Friday night
ultimatum actually come together? Svee
has the mechanical story. A mandatory
jailbreak reporting field, a
non-technical reviewer, a panic that
climbed all the way to the White House,
and a blunt verdict on the one move he
thinks Mario got wrong.
>> My understanding is that a lot of the
problem,
or potentially one major source of the
problem, is this particular researcher,
the White House strongly dislikes her.
>> I
think there were a cascade of problems.
It's very much like if you're in an
enterprise
and you have a security engineer
approach the CEO and say, "Hey, this is
a huge problem,
and it's just a run-of-the-mill bug, and
if it had gone through the CTO,
the CTO would have been, whatever,
right? It we see like a thousand of
these a day. This is not a problem."
But
because the
because the engineer shortcutted that
process and just went directly to the
CEO, and the CEO is not a very technical
person, and is more concerned about
risk, they just pull the trigger.
>> So, your understanding cuz I haven't
everything's moving so fast. I don't
necessarily have all the information.
So, an engineer bypassed Amazon's CTO
and talked to the
>> No, what what happened is that all of
these companies have to submit you know,
submit regular reports on what their
findings were. And one of the one of the
questions in the that that's been that
is sent to these companies that they
have to fill in by the way. They're not
allowed not to fill in
is oh, has any any of your engineers
found a jailbreak? And so, the engineers
just put it in there. Yeah, you know, we
did this. We we jailbroke it, right?
Like So, it could and so, Jassy is not
involved in this. The CEO is not even
involved in this. It just goes as a
regular kind of reporting.
It goes back to
the the federal government and someone
takes a look at it and says
throws up their hands and like, wow.
And then that leads to a bunch of
basically non-technical people reviewing
this and saying like, hey, we got to
shut it down. Got to shut it down now.
This is especially so because AWS runs
GovCloud and GovCloud is where a lot of
the federal government's computing is
done. And it is the primary you know,
Microsoft is also in there, but GovCloud
is the primary cloud for the federal
government.
>> Yeah, that's not what the reporting I
saw said. The reporting I saw said that
Jassy called the White House.
But, yeah, we don't know. It could have
gone any number of ways.
And what is very clear to me that
various people in the White House
including at Commerce especially
got the implication that some sort of
serious jailbreak had taken place.
And then went into a panic.
And then contacted Dario.
>> Mhm.
>> And then Dario tried to convince them
that based on the descriptions they were
giving, this seemed like it was nothing.
And they were and then they interpreted
this as oh Dario doesn't take security
seriously and he doesn't listen to us.
He is defecting. He is They Their term
is he screwed us.
And then they proceeded to impose export
controls that same day
when Anthropic officials take his
five-year product down on 90 minutes
notice.
Now, having had a day or two to reflect
on it
and seen more of the details, I do think
that it was a mistake
by Anthropic and Dario to not
give the wookie what he wanted in the
moment and temporarily take down the
model in order to prevent exactly this
situation.
Because they had had export controls
placed on the table as a threat several
weeks prior. They knew that weird
overreactions were very possible.
And
basically send an expensive cooperation
signal of we think that's crazy, but if
that's what you want, we'll take this
down while we have this conversation to
show that we are serious.
And we will put out an internal post
that says the White House told us to
take this down so that if you are being
silly, we won't barge the hell out of
you. And then we will talk about this.
And then, you know, maybe on Monday or
Tuesday they could bring it back up or
whatever it is because it's becoming
increasingly clear this was nothing.
>> [music]
>> Listen first to where Zvi lands on the
politics and administration treating
technical policy as pure partisan vibes
and digging in to save face.
And then to the thing about that whole
face-saving dynamic that I could not
stop turning over.
>> [music]
>> If we have an administration and we seem
to that that views
even technical policy almost entirely in
terms of
partisan politics
and like cares deeply deeply about like
what are those vibes
then
that problem is only going to get worse.
And they're only digging their heels in
further cuz we could have approached
this as an apolitical thing and in
Congress AI is mostly an apolitical
thing. At the states AI is mostly an
apolitical thing. Everybody understands
this technocratic figure out what to do
thing, and there's factions pro and
anti-AI on, you know, on all sides.
Republican Party is very split.
But,
you know, if they if they take this
stance, it could lead down a lot of very
strange paths, especially if they start
actually like wanting to cut off
Anthropic's noses by never releasing
face.
>> I am once again struck by how
Chinese-like we start to sound when
we're really focused on the government's
need to save face and how everybody
needs to position themselves around that
need. It's um
a bit spooky for me as a
once-upon-a-time big believer in
American exceptionalism, a little less
so these days.
>> [music]
>> If Anthropic decided to fight back, what
could it actually do?
Swee walks the real levers, the courts,
the Congress, and the strange
possibility that the most capable AIs
end up usable only inside secure
buildings, before landing on the hard
truth about why a company simply does
not go to war with United States.
>> [music]
>> If they decide we need to play hardball,
what does that potentially look like?
>> go to court, right? They they they sued
the administration in two jurisdictions,
one of which they are clearly prevailing
in one of which is they will probably
prevail eventually, but it is harder
going cuz it's a much less friendly
jurisdiction.
If the US government tries to do this on
a semi-permanent or even permanent
basis,
then
I don't know what the legal landscape
looks like. That is not my area of
expertise, and I'm sure they have very
very very good lawyers cuz we they hired
extremely good lawyers for their
lawsuits, and they will know what their
options are.
If they are if we are if the policy is
basically nobody is allowed to release
Fable-style models indefinitely,
then
that's probably not something they can
do much about.
Or, you know, they have to be restricted
in this way.
My presumption is that if OpenAI is
allowed to proceed with their version
when they finally figure out how to do
it
and Anthropic remains restricted, that
would be a much harder case to maintain
legally.
But I mean the bottom line is that
you know, if the administration is
determined to issue a bunch of orders
then the solutions are the Congress and
the courts.
Right? In some fundamental sense. Like
you cannot simply say, "Screw you, we're
going to do what we want." That doesn't
really fly.
And so
you know, the Congress doesn't seem
inclined to take this that seriously or
or be willing to go up against the
president. So the question is
what are your legal remedies? Is there a
speech provision here? There might be.
Certainly you're censoring the outputs
of a model
uh in various ways.
But I you know, again, I don't know. My
guess is you take the situation to the
public. You make you take the situation
to the to the the other companies and
the CISOs.
And also you deploy worst-case scenario
is you deploy
Mythos internally
because they do not seem inclined to
actually stop that. I mean they can
interfere preventing non-non-Americans
from doing it, but they have I think
something like 80-85% of their employees
are in fact American.
And
you just develop better versions of
Opus. So like last week uh Anthropic was
doing the lion's share of the business.
OpenAI was doing reasonably well, but I
believe Anthropic was like commercially
still clearly in the lead.
Uh without Fable or Mythos, and my
expectation is that that will continue
to be the case and that having internal
access to this model will give them a
large advantage going forward in terms
of the quality of Opus versus the
quality of ChatGPT
uh just by default
as they grow over time.
You know, if the right
But we might we might well be entering a
situation in which, you know, Rune calls
it zones of thought from the Vernor
Vinge novels
where if you want to use the intelligent
really intelligent AIs, you can only do
that in certain buildings.
You can only do that in certain like
secure locations.
And some of us would never have dared to
suggest or ask for this even if we
wanted it because it would have sounded
completely insane. The US government
might just do it anyway.
But
you know, if that happens, I think that
you know, for now you have not that much
choice but take it on the chin.
>> If I try to channel Balaji for a second,
which I wouldn't pretend to be able to
do it an A+ job of,
I think he would say something like
we all have way too much faith in the US
government. It's going to continue to be
hamfisted and boneheaded
for the foreseeable future.
And maybe it's time to exit. You know,
if you really want to make the best
decisions that you can, you should try
to get out from under the jurisdiction
of the USG.
I assume that like this will not happen
for many reasons, but I also would
expect that there would be many
countries willing to open their borders
to all Anthropic refugees if for
example, they wanted to move to Toronto
or Singapore or wherever. It does strike
me that they're all in terms of like
their internal organizational cohesion
tight enough that I wouldn't be
surprised if 90% of people actually made
that leap. If they were like we're all
going to move to Canada, I think they
would like largely all go.
Maybe I'm overestimating just how bought
in they all are, but that's the
impression I get.
>> Is Microsoft going to move? Is Amazon
going to move? Is Google going to move?
Are your data centers going to move?
>> Well, they got plenty of energy in
Canada. So I mean it would certainly be
a setback, but if you think that you're
just kind of under the thumb of a
forever intransigent
>> Is the US government allowed is going to
sell chips to Canada after Anthropic
takes in all the Canadian refugees or
are they going to threaten to annex it
and make it the 51st state out of spite?
In all seriousness
the plan doesn't work.
Because there is no The US government is
the US government.
If they want something badly enough,
they have quite a lot of levers to make
your life utterly miserable in various
ways. The entire market that they're
trying to sell to is largely the United
States, and people who the United States
has large leverage over.
All of their partners are in the United
States, right? All the hyperscalers are
in the United States.
I do not see any way
for you to just abandon the United
States in this fashion, unless you are
prepared to take much, much larger hits
than we're talking about here, that
would in fact make it very difficult to
raise money. Also, like what happens
when the United States hits you with
like put you on the same on the
sanctioned entities list,
and says that nobody can invest in you,
and nobody who invest in you can be
touched,
right? And like nobody can use your
models, and etc., etc. No, no, no. You
cannot go to war with the United States.
And like if they tried to exit, the
United States would go to war.
>> I think Balaji would say we just had one
example of a company, or not a company,
but a country choosing to go to war, not
choosing, but you know,
surviving a war with the United States,
and the United States not
getting what it wants, and kind of
having to recognize that like
yeah, we kind of have to fold this hand
because
we just actually don't really have
escalation dominance in the way we might
have thought we did.
I do wonder if all that starts to
happen,
is there a run on the US government of
some sort, right? I mean, we we I think
the Balaji answer would be like the
whole infrastructure, the whole
apparatus that you're describing, like
actually might be a lot more fragile
than
it is generally perceived to be.
And if they make such a
own goal as to
attempt to destroy and sufficiently
alienate, you know, their literally
maybe number one most important company
for no reason really, then, you know,
maybe other people will kind of
all sorts of other actors around the
world will be like, "Yeah, you know
what? Maybe Emperor really does have no
clothes."
>> I mean, Anthropic also is are the
patriots and they they are Americans and
they really like America and they don't
actually want to abandon it just
because, you know, the administration
makes some crazy decisions or it doesn't
like them particularly.
Um and knows all the different ways this
can go sideways and doesn't like that.
Iran is not a hopeful example
particularly, right? Like Iran is like,
"Okay, if we have like historically
impossible to invade mountain ranges and
a bunch of drones and we're willing to
kill a bunch of civilian infrastructure
and like sabotage the world economy,
we can use this to like prevent the US
from invading when like nobody big
really actually wants to invade us
that much.
But like also
Iran is kind of a miserable place to
live compared to what it would be if it
hadn't pissed off the United States for
decades.
Like they could be so much richer,
so much better off if they just
had acted differently. I don't
I'm not particularly
saying anything about what they should
do next, but like, you know, yeah, they
they're not exactly like smiling about
the fact that the US attacked them,
right? Like, you know, that's not how I
see that. Maybe I'm wrong.
But
no, I think that, you know, we have to
accept that the world still has
like one dominant like power in this
sense, this the United States, and maybe
two if you count China.
And that there's very little appetite
for working with China.
But also like I'm sure that
you know, Anthropic is like, "Well,
yeah, it's only 2 years
and then the worm turns
and then who knows who's next."
And they're hopeful.
But
yeah, I look there's a lot of end game
scenarios that include a lot of moves
that like seem unthinkable and crazy
now.
And a lot of things can happen.
And it is not obvious that 2 years from
now or 5 years from now or 10 years from
now the US government will be in any
position to tell anybody what to do.
And a run on the US government is
obviously possible if they screw the
situation up sufficiently.
The US is in fact a largely leveraged
bet on artificial intelligence at this
point. We have a very large debt. We
have huge investments in AI companies.
If AI were to go sufficiently haywire,
our economy is in deep deep trouble.
So, yeah.
A lot of people have a lot of leverage,
but you know,
the US government is sometimes moves
first and last, and you
don't you really really really don't
want to piss them off like in an
escalation game.
Like even if like
you can get away with it sometimes, like
in the Department of War and Anthropic
situation, Anthropic did not have
escalation dominance
uh without much escalation precisely
because
like without Anthropic doing crazy
escalations, the government cannot
cannot cannot further escalate.
Right? Anthropic played within the
bounds of the rules.
Basically.
And it was clearly going to be too
expensive to try and go around the rules
of America to try and uh hurt Anthropic
more.
And so, yeah.
Presumably like stay calm, don't panic,
don't like start trying to flee, don't
do anything crazy is absolutely the
correct move, and I would be very very
shocked if Anthropic would do anything
else.
>> [music]
>> Prakash pushed on the deeper question.
Was any avoidable? Does an export
control on a single model make any sense
when the same capabilities are arriving
from everywhere at once?
That took to be somewhat personal to why
he has spent 3 years of his life on
exactly this problem.
>> [music]
>> So, one of the questions I have is
to what extent was this unavoidable?
Because at some point, the output of the
models is going to be unacceptable to
someone.
Uh you could see in a Democratic
administration, maybe it starts putting
out really good Harry Potter fanfic.
And the Dems don't like displacement of
writers. You could see, you know, in
Tennessee right now, Marsha Blackburn is
one of the leading proponents of
regulating AI because songwriters in
Tennessee are very concerned.
So, the crux of the matter is there are
many people
concerned with the output of the models,
fearful for their livelihoods, fearful
for security risks, fearful of bio
risks.
To what extent is this unavoidable in a
sense because
these models capable the capability of
the models
necessitates that they can do certain
things.
And technically, it's not possible to
ask the model not to write Harry Potter
fanfic when someone can just say, "Write
a story about a boy wizard."
Et cetera, et cetera, right? To what
extent are we in the
situation where it is not possible to
fully control
the output of the models to the extent
that
the policy makers really want.
>> So,
you can raise the costs and annoyance
level of doing it with like closed
models, with more advanced models, with
models that are made in the United
States.
If you want, obviously, you know,
you can't like if if if Blackburn is
worried about AI music,
then there's very little she can do
except by a year.
Right? Because obviously, like what
happens when the Chinese models start
producing the music that the American
models can produce this year?
Like you can lock it down in some sense,
but so what? Like what What you need to
do is you need to just like start like
banning AI music on Spotify.
Right? You can't like stop it from
existing.
But there's not much else you can do.
But
you know, the thing about AI music is
we worry about not whether or not AI
music is created in the first place. We
worry about whether or not 10% or 50% of
song plays
become AI music.
Right? Is it actually like displacing in
a massive way? And that is much much
more amenable to a control
that is like compatible with a
reasonable existence.
And so, you know, the special thing in
bio and cyber
where if one person gets their hands on
the wrong thing and misuses it once they
can cause a like catastrophic
potentially amount of damage to the
entire civilization.
Right? Do billions and trillions of
damage, you know, just like disrupt our
lives, start a pandemic, who knows what
might happen.
And therefore those areas are much
different and you have things like the
blast radius that don't even talk about
biology at all.
And for biology we're clearly going to
have to do a bunch of hardening of the
physical systems, of the manufacturing
systems, of the treatment plays of the,
you know, various things that we have
barely begun to do.
But
fundamentally speaking, this is exactly
the the race and the competition problem
of
you know, we can't really stop without a
full international agreement to stop.
And so when the governments decide the
biological risk, the cyber risks are
unacceptable.
You can only buy so much time. Like
cyber has the advantage of if you are if
the defenders are in the lead over the
attackers and you harden the key
systems, you can hope for things to be
okay.
And we don't yet know if that's going to
play out that way.
Uh we can hope.
In bio it's much harder because I
don't think that the defense if if
everyone has to the tools,
I think it's pretty clear that offense
wins. Basically that like it would be
extremely disruptive even in the best
better cases.
But the good news is that almost nobody
actually wants to cause a problem and
that especially includes people who know
what's going on and so
we can almost equally
but
Look, it's going to be rough out there
and these are for the relatively limited
problems of catastrophic risks rather
than the existential risks that come
with automated AI R&D
and just general like
abilities go to the roof and like
competitions end
like transformations intensify and
nobody knows what's going on and we're
being outsmarted by our eyes on every
level and like every decision that
matters is being made by the AI and the
humans don't necessarily even understand
why the AI is doing it but they've
learned that when they disagree with the
AI things go worse.
So what are you going to do?
And and problems like that and that's
even if the AIs don't go rogue, right?
If the AIs don't pursue hidden agendas,
they don't decide they want something
else. So it's it's going to be
really really rough and we don't have
good solutions to this and
but the reason why I have spent like the
better part of three years now on this
problem because I am terrified of what's
going to happen when we get there.
It wasn't because of some incremental
thing that like could have happened
already along the way.
>> [music]
>> To close with Zvi, the question I keep
circling back to.
If the whole future really does run
through a handful of labs, a few
governments, and a couple of choke point
chipmakers, is that a relief because
it's at least tractable or a terror
because it's so few hands?
His answer is more useful than either.
>> [music]
>> Maybe just kind of a couple
kind of wrapping up big picture
questions. One I always try to make a
point to ask you for some sort of
advice.
My
thought in recent weeks has been
life is kind of converging on a tabletop
exercise in the sense that
it does seem like we can model the
scenario with like fewer and fewer
relevant actors.
And I don't like that, but it's hard for
me to
avoid that conclusion at this point.
And so I'm kind of feeling like, oh man,
I have to spend a lot more time than I'd
like if I want to be a helpful public
sense maker. I have to kind of spend a
lot more time doing close reading of the
company, the you know, the few top
companies and the the few most relevant
actors than I would
otherwise be inclined to.
And it feels also like my theory of
change probably needs to flow through
those few actors.
Agree, disagree, any you can you offer
me any relief from that conclusion?
>> I think that you're right that
we have three
labs, approximately you know, two to
four, that matter a lot. We have one to
two governments,
maybe one to three that matter like
quite a lot.
We have other players that matter
because they're hyper scalers and like
can gate things or otherwise like
control choke points in the production
line.
But yeah, no, you can you can imagine a
table top exercise much more so than
before and you can also sort of see the
end
uh to a larger extent than before and
we're starting to see sort of
our hypotheticals make contact with
reality and we're seeing what reality
really looks like and what these people
do in practice.
But also all these
actors then become yeah, they're they're
they're individual human components and
how they operate internally starts to
become really important. And you know,
how did this go? Well, partly they were
dealing with commerce. If they'd been
dealing with the NSA, it'd be very
different. If they'd been dealing with
Casey, it'd be very different. If they'd
been dealing with the white the the top
of the White House and like Wiles and
Trump directly, that would be very
different.
Some of those might be worse, but like
they would be different.
Um
you know, DOD OW DOD and that like was
very different than if have been at the
ranch and so on.
And Anthropic has internals as well.
Like the personality of Dario
specifically has seems to like it's been
increasingly important in various ways.
And that certainly the personality of
Altman became very very important in
various ways at various points along the
way and you know, it wouldn't surprise
me if it saw us and and any number of
other people followed suit for good or
ill.
But in terms of if you're trying to
follow the situation,
yeah, I think you really we do have to
model it as
a relatively small number of players and
at the same time like the public can act
to influence what those players do in
important ways and other things do
matter.
The midterms are coming. The midterms
are going to matter.
The election in 2028 is coming and if
things don't move too fast, that
election's going to matter a lot.
So, you know,
and the market's reaction to things, for
example, also matters quite a lot and so
on. So,
but there's more going on in the world
than Yeah, there's too many situations
to monitor. You have to choose which
situations to monitor.
I choose mine
and you know, everyone has to figure
that out and I can help you with mine
and then you have to choose yours.
>> What should we be hyperstitioning now?
Obviously we've had this sort of
phenomenon of
situational awareness and AI 2027 and I
feel like the the degree to which those
things are
predictions versus sort of somewhat
shaping expectations and shaping events
by kind of getting people to act as if
they're in that scenario and therefore
realize it. I think that's a little
blurry. I don't want to give them more
power than they really have, but it does
seem like they've had influence in sort
of pulling reality toward the fictional
narrative at least somewhat. Um so, I
guess tell me if you think that's right
or wrong, but then to the degree that we
can pull reality toward scenarios, what
should we be hyperstitioning now?
>> And the obvious thing you can
hyperstition is reasonable laws
and coordination mechanisms and actions.
So, I would I would focus there.
>> [music]
>> After Zvi signed off, here's where I
came down on a pattern I keep seeing
where the safety world's carefully laid
plans get their entire game board
flipped over at the worst possible
moment.
>> [music]
>> Always a treat to get Zvi on the on the
line.
Um
I do sort of wonder, I mean, he's good,
right? I mean, there's no doubt he's a
from Magic the Gathering, you know,
elite professional play in all these
different scenarios. I think
it's clear that he's like a better and
more grounded strategist than I am.
And yet I do have a little bit of
feeling like
somehow
the kind of
AI safety rationalist Anthropic world
keeps
getting their game board turned over on
them at the like inopportune moments.
And so, I do wonder to what degree the
like
working within the frame of the US
government will kind of all, you know,
be a given, you know, for how long, you
know, or or at some point will that be
questioned? Even this moment, you know,
feels like and we've certainly seen with
the OpenAI board you know, firing of Sam
Altman was a classic one where it was
like, well, we're the board, we have the
power to do this. Well, it turns out
that you don't because there's a frame
bigger than the frame that you're
operating in that if people's
get sufficiently unhappy with how the
game is being played
according to the written rules, yes, of
course, those are the written rules, but
there's bigger rules out there that we
can zoom out and and kind of re-
orient around.
Seems like that's of happened a little
bit here, you know, Anthropic felt like
they had done everything the right way
and presumably this wasn't some galaxy
brained bank shot, you know, that they
were trying to get some overreaction.
And yet, you know, here they are and
it's just like, well, guess what? Now
you're export control slapped and so,
you know, your own people can't even use
it. Come come see us on Monday and we'll
we'll think about what whether or not we
want to give you any relief.
I do wonder if that
you know, how many more times that can
happen. It seems like we're I don't feel
like we've necessarily seen the end of
that
phenomenon.
But probably the smart money is still
with V over
over Although, you know,
Anthropic's certainly been smart money
over time, so I wouldn't um
I wouldn't take it for granted.
>> Part two.
Is the reaction even right?
V laid out the conflict, but I genuinely
wasn't sure my own first take held up.
So, I spent the rest of the week testing
it against people who'd see it
differently.
Start with the mechanics.
Sam Hammond is chief economist at the
Foundation for American Innovation. He
spent years on state capacity, the
unglamorous question of how governments
actually do hard things. And he gave the
clearest account I heard of how an order
like this comes together from the inside
and where it went off the rails.
>> [music]
>> I mean, it's uh
it clearly caught Anthropic off guard,
right? Dario was at a wellness retreat
or something like that. I think they
thought it was the worst is behind them.
And the actual complaint or the
the catalyst for this
even as it's been reported out and more
details details have come out is bizarre
and confusing.
It's like a jailbreak that isn't really
a jailbreak. It's like the model
doing its job at
at patching server vulnerabilities.
The sort of thing that GPT 5.5 can do as
well.
So, it looked at first like to me that
it was purely a punitive thing. This
was, you know, round two of Hex-Rays'
war on Anthropic.
Now, as details have come out, it seems
more like it was a weird kind of
miscommunication
from team at Amazon to try to get in
touch with Dario, couldn't, and went to
called NSA directly, apparently.
And I think part of this was also the
overlay of the ONDC
executive order on cyber. There's the
30-day review period
where, you know, at least in retrospect,
it seems like a lot of the safety
classifiers that Fable had that people
were complaining about
were partly
and this is my this is me sort of
speculating concessions to the NSA and
to the White House to say, "If we're
going to release this model, we got to
make sure that the cyber vulnerability
elicitation capabilities are not widely
available
and that we don't like let China, which
has tons of remote access to our models,
use it to bootstrap their own ecosystem
so that
it's it it
at least to me it's helped to sort of
backfill
the mystery around like the intensity of
the safety classifiers on Fable and
especially the sort of
suppressed clandestine suppression of AI
R&D.
But like on the surface level it looks
like Anthropic is bending over backwards
to get that model out.
But I think
it when the dust settles we'll look back
at this as like the first trigger of
that executive order.
And the wielding of that 30-day review
period to pull back. Unfortunately, I
think they've gone with this export
control as the enforcement. Partly cuz
it's easiest thing on the table.
And you know, BIS has like pretty broad
authority including over software export
controls. But the speed at which it
happened, the
lack of forewarning
and the ultimate rationale make very
little sense to me and also don't really
point to what the off-ramp is. Right?
Cuz if the off-ramp is you have to fix
any you have to fix as an issue.
>> [laughter]
>> That's That's not going to happen. And
so my sense is like the Anthropic team
that came to town, you know, they
brought Nicholas Carlini and and uh some
other other more technical folks to
brief the government was partly just
like getting them up to speed on like
Sorry, maybe we scared you too much with
mythos, but like here's the reality on
the ground and like what's actually
technically feasible.
>> He doesn't stop at the diagnosis. Here's
what Hammond thinks the government
should be doing instead.
>> And it would also help to just invest in
basic state capacity. You know, right
now
Casey, the Center for AI Center for
Innovation
at at the Department of Commerce, which
is supposed to be the US government's
sort of front line in-house capacity for
everything from AI evals and benchmarks
to things like prompt injection
jailbreaking research,
like they have ML engineers on staff.
They've been on total lockdown.
This has been reported by the Wall
Street Journal and and validated by
others. They've not allowed to take
meetings. They're not allowed to
publish their research. Apparently, they
have
significant applications sort of on
standby including evaluations of Chinese
models that would be interesting to the
public, but they've been basically
frozen.
Um and so you have instead
the Office of National Cyber Director
and Secretary Bessant and folks who
have
very limited AI background calling
shots.
>> And the part founders don't want to
hear. Why even when a law is bad, you
cannot just opt out of the politics.
>> [music]
>> Yeah, I mean, in some ways we're in the
good timeline for this. I've written
before that super intelligence is a
direct challenge to the sovereign.
Political theory 101 suggests that you
know, the state would intervene at some
point to building
a Manhattan Project times 100 in in the
private sector is untenable over the
long run.
It's uh
But by good timeline, I mean like we
have companies, really three leading
companies, all of whom have direct
allegiance to the US government, have
bent over backwards to not just, you
know, comply with existing law, but to
proactively put forward frameworks for
fostering deeper integration with with
the US government.
And I worry that we are, and by we I
mean the the White House is not taking
those overtures gracefully and instead,
you know,
having a kind of reaction a more
reactionary response to these
capabilities in a way that's not
realistic. Like to to Nathan's point
earlier, these capabilities will be
widely available and open source within
a a handful of months. There are models
probably already trained and in the
process of being post-trained that will
supersede stable and mythos at all the
labs.
And are they going to get the same
treatment?
And if not, you know, that's that's its
own negative and not that this is a a
good policy, but even bad laws should be
fairly applied for equality of law's
sake.
So, you know, what my hope is that we
can learn from this at least. The
companies are more than willing to work
closely with the administration. They've
uh you know, retrofitted data centers to
be in compliance and all the all these
other demands have been put on them.
But it requires her two to tango. Like
if
trust is trust is a two-way street and I
think there's any lesson that Anthropic
should take away from this is that they
can't ignore politics.
Right? They've uh
they've heard this critique for over a
year now that they've sort of been light
about the
need to invest in the ideological side
of their project. And
ideally, like maybe not Dario at this
point, but like someone at Anthropic
should have all the key principles in a
single group chat. You know, that's
I guarantee you Sam Altman, Greg
Brockman,
others have really continuous
conversations with all these
stakeholders. And the thing about this
administration in particular is it's
very relationship driven.
And if you refuse to have these
conversations,
you will be
not invited to the party.
>> Which sets up the most useful
disagreement of the week. The one that
pushed on the hardest, and the frame I
want you to hold for everything that
follows.
Jud Rosenblatt runs AE Studio.
My read on the administration here had
been pretty cynical. That they basically
have it out for this company.
Jud argued to my face that the AI safety
world, me very much included, owes the
administration genuine empathy instead
of contempt. And he brought survey data
on why we're structurally blind to it.
Listen for the moment I take the
correction.
>> [music]
>> But we did we did surveys of of hundreds
of alignment researchers and effective
altruists, and we saw that less than
less than 2% of alignment researchers
were politically right of center, less
than 1% of effective altruists were
politically right of center. Uh uh of
effective altruists, 40% were extremely
progressive, and another 40% were very
progressive. And it's also worth
considering things like the Jonathan
Haidt research around how how hard it is
for people to actually empathize with
people of different political
backgrounds. And And I think that's a
lot of what is actually going on here.
And it's hard for people to admit
because you think you're making good
decisions and judgments about whatever
the current thing is. But according to
that research, you're just not. Uh if if
your political beliefs differ from the
person you're judging. Uh like the
studies around how basically things like
the
the informational content of a political
argument is irrelevant to what to
whether someone will believe in it. If
if it is framed in terms of your
preferred political party, uh you'll
you'll agree with it. And if it's framed
in terms of the other political party,
you'll disagree. But the if the but the
informational content stays the same.
The informational content is not what
sways you. It's just the narrative of
it. And it's hard to remember that in in
every moment in every time slice of
what's going on with each AI thing. But
I was fairly disappointed in the
AI alignment world's reaction to what
happened last week because I think that
the right thing to do is to be very
excited that they are starting to take
this stuff seriously and are able to
take real action.
And so if we just project going forward
and also keep in mind by the way that we
all have exponential slope blindness.
People didn't didn't didn't we didn't
evolve to
to to be able to unconsciously model
what exponential slopes are like because
we don't experience them over the course
of our single human lifetimes in a
meaningful way.
So that's why people didn't predict
what's going on right now that it would
get to this point in the first place.
But also everyone's over indexed on
what's going on right now. So people
aren't really predicting what's going to
happen again in the future.
If we predict into the future, well,
there are going to be much bigger
crazier things going on.
And and and And we want
informed competent group of people
doing smarter things when that happens
and and and not having unnecessary
confrontations. And I think it's easy to
for the AI alignment people to put the
blame on the Trump admin. But honestly,
I really think that that the blame comes
from
belongs more to them honestly because
it's it's just
and it's hard to admit really because
like
in the local incident, you might seem
rationally correct. But in the in the
broader scheme of things
considering where we're going, I think
that the the better thing to do is to
figure out how do we get to a better
future for for all AI and
humanity in the future of consciousness.
>> So how
I might be guilty of what you're saying.
Jeffrey Ladish,
Laurent Gasser who we talked to earlier
this week come to mind as voices from
the AI safety world that I think
expressed the sentiment that you
advocate, you know, which is hey, this
is a good move even if it's a little bit
you know, not as technically grounded as
we might wish for at this point. It's
something and maybe it's something that
we can build on.
>> How will you
know if you're right or wrong? Like what
do you think what do you think happens
from here? When do we get, you know,
resolution? What does that resolution
look like?
>> [music]
>> But hold the empathy next to the law.
Because the next question is whether the
government can even legally do what it
did.
Donnie Bloomfield teaches law at Fordham
and he gave the sharpest doctrinal read
anyone offered all week.
Start with the authority itself and a
distinction almost all the coverage
missed.
>> [music]
>> Government's discretion here is
extremely broad. So the government can
issue regulations that control like
specific types
of hardware, specific commodities,
specific types of software and it can
also control what's just called
technology which means information. It
can control proprietary information and
it can prevent companies from without a
license sharing those proprietary
information with non-US persons. In
spite of this very broad discretion
having now looked at the the letter that
the Commerce Department issued to
Anthropic on Friday, at least the
reported contents that Bloomberg
obtained, it's not clear that the
government has the authority to do what
it did here at least under its stated
legal powers. Nor is it clear that like
the letter even actually restricts
Anthropic from making its API available
including to foreigners. So there's very
broad discretion but it's not clear that
they actually even have the authority to
do what they did at least under their
kind of claimed arguments.
>> Can you just do a double click on that?
I mean, I've heard things like you can't
export control services and I'm not sure
if that kind of plays into why they may
or may not have the authority
unpack like why you would say they might
not given all the broad discussion that
they have why would they maybe not have
authority in this particular matter?
>> Yeah, so there are a lot of like gritty
technical reasons. I think that one of
them is like what the the law says is an
export doesn't cover services. So it can
cover information, but it doesn't cover
services per se and the Commerce
Department has been explicit about that
in its own guidance. It said like cloud
services are not an export. It said that
software as a service is not an export.
It said that in its own guidance and
Congress has been working actually to
fix this loophole. The house passed a
bill in the the remote access services
act to try and clean this up to to to
give Commerce the power to restrict, you
know, non-US users from accessing
compute or or AI models, but that those
powers don't yet exist. And so saying
that
Anthropic cannot export a model, I mean,
it's not even clear what they mean by
that, but the powers of
Commerce here are not infinite. And if
they did try and restrict, which they
don't say in the letter, but if they try
to restrict all outputs from these
models, that would run into both like
real problems under like just the
statute and the regulation,
which say that it doesn't apply to
published material or fundamental
research,
both of which at least like the Fable
outputs probably would cuz you and I can
buy a subscription to Fable, which means
that it falls into this exception in the
regulations. And it would also run into
as you know, we were talking about
earlier with with respect to biological
data, it would also run into I think
serious First Amendment questions. I
don't think those First Amendment
questions would be like impossible to
get over if we were talking about a
really serious catastrophic risk, but on
the level of risk that we've been
talking about, especially when they're
not doing the same thing for GPT 5.5 or
other models that seem to have similar
capabilities, I think that the First
Amendment issues here loom pretty
significant.
>> [music]
>> And then the deeper problem sitting
underneath the whole action, the First
Amendment by way of a Supreme Court case
from just last year.
>> [music]
>> But do courts think that way or are they
sort of more narrowly constrained to
look at just like this one um
this one law as it applies to this one
situation? How how broad can they zoom
out and consider the government's, you
know, apparent motivations and patterns?
>> We're actually lucky to have like a very
on-point Supreme Court case from last
year where the Supreme Court said that
New York State was going after the NRA
on ideological grounds and that even
though or even if like the the law under
which the New York was trying to go
after the NRA was itself appropriate. In
other words, like even if all the
actions aside from the ideological
motivation have been appropriate, if
they're using their lawful powers to
attack ideological enemies on
ideological grounds, then that is a
First Amendment violation and you can
prevent the government from taking those
steps. And you can look fairly broadly
to see that you can look at like what is
the government communicating? What is it
saying about its actions? What is it
telling other people about why it's
making these decisions and how they
should proceed? And I think that all the
evidence that we've seen of at least
some ideological motivation on the part
of the Trump administration should at
least raise like serious First Amendment
hackles. Even if we don't think that
like the the models constitute Anthropic
speech, even if we're not worried about
the model output as like information
that we as listeners have a right to
hear, just like going after Anthropic
on ideological grounds, even if they
were on totally otherwise good legal
authority, would itself constitute a
serious First Amendment question. And I
think that I think that's a challenge
that Anthropic could consider bringing,
but it's it's one that would still
trigger all the problems that we were
talking about earlier where if Anthropic
wants to have an ongoing relationship
with this administration, they are faced
with, you know, a really serious
trade-off where where
there's still all these other tools and
just constantly returning to court is
just a perilous exercise. So, I do think
that there are real First Amendment
questions about the validity of this
action even aside from all the speech
concerns just like punishing seemingly
going after Anthropic as an ideological
adversary presents very serious First
Amendment problems on its own to, you
know, to begin with.
>> [music]
>> Now the genuine contrarian. Aaron
Shapiro hosts Doom Debates and his
reaction to the ban surprised me as much
as anything all week. Clown show or not,
he is glad it happened and he'll tell
you precisely why breaking the ice is
worth more to him and getting it right.
>> [music]
>> I'm a simple man.
I see AI getting paused. I feel good
about breaking the Overton window. You
know, the government can do it. It's
that easy, guys. This is a precedent.
Overall, I'm happy. You can talk about
the nuances. It was done like a clown
show. It was done for bad motives. It
doesn't really consider China or a
treaty or anything. There's a lot of
problems, but I'm really happy about
smashing the Overton window where now
tech folks don't think that they're like
in a bubble or they're untouchable. Like
it happened, guys, you know, and we can
only go from here.
>> I I have
I actually agree with you. Uh because I
think it's was a little bit delusional
for tech
to feel that it wasn't going to going to
get touched and the government just has
so many little so many, you know, small
and large ways to effectuate its power.
It's it was not that surprising to me
that they went through the left field
and
went with the export control rather than
anything else.
But,
it also strikes me that w-
as they exercise this, we start also to
go into
kind of what we wanted to avoid. It's a
little bit of small tyranny, right? I
think
several people on the timeline have
commented, Dean Ball has commented, this
kind of unstructured
regulation
without
looks kind of selective
and vengeful almost.
And it kinds of kind of starts putting
you in this zone where I think tech
people start to mistrust
the the government. Because you also see
I think there's a lot of narratives on
the timeline which are being leaked, you
know, sources close to sources familiar
with.
And as they get leaked, it's not very
certain whether those things actually
happened. Would someone actually attest
to that in front of Congress? Very
unclear.
And we've also seen this kind of
behavior from the administration in
other affairs as well, where you have
multiple conflicting narratives. It's
happening with Iran war right now, where
it's not even clear to Congress what the
deal is. And you have different people
saying the deal is a different thing,
right? So,
where do you think that puts us?
It's great that it's happening. I
understand you feel it's great that's
happening to AI right now,
but that does that put us in a position
where it's detrimental to the body
public at large?
>> I think you know, your analysis you're
you're weaving together a few factors,
but I think the elephant in the room I
hate to get political because you know,
when it comes to President Trump, he's a
mixed bag for me. I I don't have Trump
derangement syndrome. I don't love
everything he does. I don't hate
everything he does, but I I think the
common thread with Trump is it's just a
a mess, you know, like it's not
[laughter]
it's there's not it's not like
disciplined, right? And I think we're
definitely seeing that on display right
now. I would argue we're seeing that on
display in the Iran war. I you know,
previous administrations, there was just
more pressure to have logical
consistency, right? Some kind of
narrative. And this is another one of
those cases where you see people in this
administration saying all these
justifications why something happened,
but then the next day it's like, "Oh, it
happened for this reason." Right? Like,
"Oh, Dario did this, you know, he wasn't
responsive to us. That's why we're doing
it." And then Anthropic's like, "Oh, no,
he was responsive to us." And it's still
not clear exactly what did Fable do that
was so dangerous, right? Because
Anthropic is like, "Oh, this jailbreak
is nothing special." And the Trump
administration's like, "Oh, well, you
know, our secret source, Amazon or
whatever, right? They're they're telling
us that it is dangerous." So, I I hate
that it's a clown show, right? I hate
that this is how humanity's operating.
I, you know, I'll take the win that it's
a pause, but like I also think it's
probably time for a new administration.
>> His larger worldview is what he calls
the Icarus graph. The case for getting
ready to pause and how you'd actually
build the groundswell to make that real.
>> So, my worldview, my outlook right now,
it's what I call the Icarus graph. I
feel like nobody gets this, right?
Everybody's like, "No, I think the world
is good. It's going to go this way." And
some people are like, "No, we're we're
terrible at, you know, enshittification,
right? It's going to go this way." And
I'm like, "No, no, it's Icarus, right?
We're going to fly closer and closer to
the sun. It's going to be great, and
then we're going to do a 180° turn and
plummet down to hell." So, basically we
got a taste of heaven, and then we get
hell. So, you have to ask me then,
"Okay, so where on the Icarus graph do
we stop?" And it's a brutal question,
right? Because it's like every day, you
know, I'm I'm enjoying the flight as
much as the next person, right? It's
like, "Yeah, give me the next quad, you
know, make my code faster, great, you
know, let help my business run better,
uh and you know, make me better AI
videos." So, there's no natural point in
terms of like when it feels right to
stop. I just think it's important to
stop before capabilities get to a
runaway point. And we've been kind of
frog boiled to be like, "Oh, each model
comes out and like we're doing great. If
we could stop the clock now, would I
turn back the clock? Would I lose Fable?
Would I lose Opus? No, I'd I'd keep it
all, right? Like I still think, you
know, we're playing shuffleboard, we're
playing Icarus. Like so far, so good,
right? Should we bet again? Should we
keep betting until we lose? You know,
it's it's a crazy tough question. I
think the Eliezer Yudkowsky, yeah, the
turkey graph kind of yeah, yeah,
exactly. Although, the only difference
with the turkey graph is each day of the
turkey's life is actually better, right?
Not only is it living longer, it's
actually living better and better. So,
the turkey is really, you know, happy
with its life. So, I think the Eliezer
Yudkowsky Miri position, which I agree
with, is just like we don't know when to
stop. So, let's get ready to stop. At
the very least, let's get ready. I would
probably stop today. I would stop and I
would be bummed. I saw a food influencer
say this about how she like eats
chocolate basically. Like, yep, I just
ate this chocolate and now I'm bummed.
That's what you got to do That's what
you got to do. You know, like don't
don't don't reach for another chocolate.
Like just sit there and be like, this is
the prudent place to stop right now
until we have any idea of some kind of
theoretical method by which we
understand what a superintelligence
wants to do and what an equilibrium
state of a superintelligence looks like.
That's actually something Miri was
trying to study,
identifying equilibriums that are
plausible for superintelligences.
There's actually a rich vein of theory
there that's highly neglected today.
Let's do some theory there. Maybe then
we can unpause. I think that's got to be
the best plan. And so, I I think the
number one leverage point here is just
like repeating, get ready to pause,
right? And and And like you said, OpenAI
and Anthropic, they said it. They said,
let's try to get ready to pause. So, I'd
love to see more people saying it
because it really has to be a giant
groundswell.
>> [music]
>> And the concrete version of the ask,
stripped down to a single sentence.
>> So, from from my perspective, we keep
playing shuffleboard, right? We keep
doing Icarus. We keep going higher and
winning, kind of, but we're also getting
closer and closer to the point of no
return. So, even though if it feels like
we're winning now, we're also killing
our ability to pause cuz we're so close
to the point of no return. The last
breakthrough where after that the AI
takes over the research, and then we're
really screwed. Right? So, basically, I
I think roughly a good policy is, okay,
no more frontier capabilities upgrades
for a while. Right? Like, it's just too
dangerous. And I know that concept is
hard to communicate to people when
everyday life is getting more awesome.
Like, I know I think we're in a screwed
situation, but that's that's just what I
think is prudent.
>> [music]
>> One piece of the whole standoff
genuinely puzzled me. And it's about the
people who have gone conspicuously,
suspiciously quiet.
>> [music]
>> Why do you think everybody is doing what
they're told so much? It seems like
we're in this weird moment where
it's even if you, you know, we just
talked to Lorne who sort of is like very
welcoming of the move, even though he
recognizes that it's ham-fisted and and
um
far worse than even second best, right?
And
yet
we're not seeing, you know, whatever
research is ready to go, we're not
seeing it leaked. I'm kind of surprised,
you know, if if there's research that's
like of interest to the public and
people, you know, I mean, people who
went to work at this government agency
generally speaking could have taken a
lot more money in the private sector,
right? I assume a lot of them have got
to be pretty pissed at this point that
like, I came to do this public service,
and now you're just screwing with us for
no good reason at all, but apparently
going to put this into some classified
territory, which doesn't I don't I I'm
not hearing really any voices say that
sounds like a great idea other than the
people doing it. And yet, so far nothing
is leaked, and we haven't even seen the
letter, you know, that that the
government sent to Anthropic. Like, the
longer this goes on, it the more it
feels to me like an OpenAI board
scenario where it's like, you've got to
have an explanation at some point, or
it's going to become clear that you
don't have a good reason for what you're
doing, and the world is going to judge
it that way. But, the parties most
directly affected are
being like incredibly docile.
>> Yeah.
>> [music]
>> All of which left me thinking about the
people inside these labs and how far
they would actually go.
Prakash floated a scenario, a US-only
national model built Manhattan
Project-style out in the desert, cut off
from the world.
I surprised myself with how confident I
am about what would happen.
>> [music]
>> I sure hope it doesn't happen.
But
I can
imagine it happening. I think
the culture of
frontier AI research
is
in some ways very incompatible with like
military discipline, right? Like we have
the famously uh
pink hair, libertine, you know, uh
polyamorous, uh whatever, right? All
those kind of cultural dimensions are
have at least a foothold in the in the
AI research community, if not more.
And
I certainly don't think people
are keen to leave the beautiful Bay Area
and move to, you know, an undisclosed
location in Nevada where they
>> Albuquerque, New Mexico.
>> Yeah, may or may not have
um
ability to communicate with
you know, their friends and family in a
in the way they might like, or even, you
know, in the extreme cases, like may not
be allowed to leave the facility.
And yet
I think a lot of I think enough people
would sign up for that that they would
be able to
build the team. You know, if you just
went desk to desk at certainly Anthropic
and OpenAI, and you were like, this is
happening.
Do you want to be a part of it or not?
Especially if it was going to be coupled
with, by the way, you can't do it out
here anymore. You know, it's either you
either are able to continue doing
frontier research in this way or you
can't anymore.
I think a lot of people would make a lot
of compromises and a lot of sacrifices
to
get into that bunker environment. Just
desire to be part of it is so strong.
The identity that people have around
being a part of this
process, this story, this moment in
history, I think a lot of people
wouldn't know what to do with themselves
if they didn't have
that job. In in some way, shape, or
form, right? And not to say that they
went to their specific role at their
specific company. But the idea that they
would be not
involved in a live player project. I
think for many of them would just be
like, I
wouldn't know what to do with myself at
all. And so yeah, you could probably get
a lot of people willingly giving up
uh a lot of niceties in life to be part
of
you know, whatever underground uh sprint
you might want to put together. I still
hope it doesn't happen, to be clear. But
I don't think it will be but if it
sounds like really weird, like who would
sign up for that, you got to keep in
mind that a lot of these folks
basically have no life anyway. Um
they're not
and again, this is broad brushstrokes. I
you know, all the caveats apply. But you
do have a lot of people who are like
thinking about nothing but this already.
Who who are not calling their parents,
you know, all that much already.
Uh who are maybe not dating much at all.
They're just kind of already locked into
this like this is all that matters. I
don't really have time uh for anything
else. I I was speaking to somebody at
Anthropic who was like
uh I honestly said it's something very
similar to what I heard Zelenskyy say in
the last 24 hours. He was asked um
forget exactly what he was asked,
something like, what do you miss or
whatever? And he said, I miss being a
good father.
And uh this person at Anthropic said,
this was like a month before the
Zelenskyy quote, said, I miss being a
good friend. I'm a bad friend now. And
it was kind of like
some not regret but not the sort of
regret that I'm making the wrong
decision. It was just like that this is
again, you know, I said that you sound
like like a World War II era
mentality.
And they were like, yeah, that's
that's how a lot of us feel.
>> [music]
>> Part three, the real world.
Here's the thing about a week swallowed
whole by a political fight. The
technology itself did not pause for one
second of it. While Washington argued,
builders kept turning AI into things
that touch the ground. Medicine,
mathematics, working software, the
supply chains that move physical goods.
Start with the one that moved me most.
>> [music]
>> A company announced a one-minute
full-body medical scan this week. Cheap,
beautiful, and readable by AI. And it
set off something I felt in my bones
ever since my own family's hard run
through the medical system.
>> [music]
>> I mean, if the government thinks that
they're going to block people from using
this technology, I think they're going
to have a real fight on their hands. And
this is going to
probably play out
in so many ways. I mean, I you know,
I've talked about this probably ad
nauseam at this point, but
in the whole cancer experience that I
recently went through,
fortunately, I didn't have to get off of
the standard, you know, my son didn't
have to get off of the standard
treatment protocol. Like it worked for
him, and all the exotic stuff that we
were scouting out,
we never really had to to
actually try to get our hands on. But I
was already
gearing up for a battle on so many
fronts, you know, just even the
DNA testing that we did, which is not
standard, and which fortunately we you
know, didn't have any real trouble
getting our oncologist to support, um
that like fundamentally changed my
information landscape and how I was
thinking about, you know, how confident
I could be that he was in fact
cured. You know, I think we're like over
99% now given all these results. We
wouldn't have been able to get to that
level of confidence otherwise.
And
you know, in in terms of talking about
the hypotheticals, like, well, what if
this next test were to come back a
little bit positive? The answer is just
like, well, you know, we wouldn't we
wouldn't treat on that anyway. We would
um we would really need to wait for
gross disease.
And I just think, boy, people are not
going to be content with that for much
longer. You know, that when we have
these technologies, and especially this
one I think is what makes it so
promising.
And obviously they have to deliver,
right? I think a a little dose of kind
of um
skepticism is probably warranted, you
know, will this ever actually happen? Uh
I don't mean to cast out on that, but
you know, it's not insane to wonder. But
assuming that they can actually deliver
on their promise, the fact that it takes
a minute
and therefore is probably going to be
pretty cheap, you know, and I don't know
what their retail price will end up
settling at, but presumably it is
something that they can operate quite
cheaply on the margin.
And the fact that it's so beautiful to
look at. You know, people will be able
to study this for themselves, I I think
in a really effective way. And of course
there will be, you know, all the AI um
study of it as well that I think the
medical establishment is not really
taking into account. You know, the
responses have been, well, you know, the
ultrasound doesn't see this that well,
doesn't see that well,
or you know, we've we don't actually
recommend whole body scans because, you
know, there's a lot of false positives
and all this kind of stuff. And all of
this is just feels to me like kind of
fighting the last war, a sort of a a
scarcity mindset on multiple levels.
>> From the body to mathematics,
Karina Hong founded Axiom Math, and her
bet runs directly against the entire
Frontier lab playbook. Not bigger
models, but formally verified ones,
where a machine checks every step of a
proof.
She explains what that even means, why
it matters, and the milestone that just
quietly fell. For the first time, a
formal system beat an informal one on a
real math Olympiad.
>> What is Lean? How is this paradigm that
you're developing different from the
paradigm that the frontier companies are
developing? And obviously we're hearing
pretty amazing things in terms of math
results from them. Two, what makes your
bet and the paradigm you're working in
>> Yeah, so I I start with the story. This
is about January in 2025, the joint math
meetings. I believe it was in Seattle.
So, I was there I think for the first
time the topic is AI.
It's the American Mathematical Society
and you would not expect AI to be in the
front and center of the largest annual
mathematicians gathering. And And
wherever I go for that I think like
three-day period, I heard people
whispering one thing, Lean. And so So,
like kind of like what is Lean? This is
a formal language for math proofs. It
has been started like in specifically
2013
by Leo de Moura at Microsoft. In 2019
people start building math lib, the
largest math library in Lean. And the
dream of AI for math started predated
the deep learning era of using basically
various forms of formal languages, Lean
included, to try and close out there.
That's called automated theorem proving.
And what's today AI for math would have
been called interactive theorem proving
with the human being replaced by an AI.
So, that's kind of the historical
context. Now, obviously large language
models, various like frontier labs, are
also pursuing AI for math, but they
generally have taken an informal
approach, which is the idea of using
natural language reasoning and train on
really large volume of data, chain of
thought, to try to and also scaling test
time scaling inference to get to a very
sort of strong computing power
[clears throat] to be able to not rely
on the verifiable output. We're
obviously taking a different approach
here. We believe in lean powerfully. It
is at the point that we examined in
December, which is 4 months after we
start operating, we realized the first
time that a formal system actually beat
the informal system on a mass and peer.
It was never the case. So, Econ 101,
there's this famous theorem agree to
disagree by Nobel Prize winner Robert
Aumann, and that is a 50-year-old
theorem since 1976.
Everyone has been teaching it for 50
years. There's an implicit assumption
that was never made explicit that action
improver was able to catch in the auto
formalization process and was also able
to patch the the proof and that
>> One big question I have about math in
general is like
>> Yeah.
>> how confident are we in what we think we
know?
And I understand that Lean at its core
has a small number of primitives which
are
super deeply vetted and trusted.
>> Right.
>> Such that then they can be composed
arbitrarily and anything that kind of
you can build with those building
blocks, you also can
>> Axiom.
>> can trust.
But then there's these things like with
the
agree to disagree result where
I I'm not quite sure what you did there.
Did Did we
Did the original conclusion still hold
or did
>> Yeah, yeah, yeah. It's
yeah.
>> strengthened the proof. So, now we've
gone from
a
a we we had what was a valid conclusion.
We still have the same conclusion, but
we didn't realize that we were holding
that conclusion for less than
fully solid reasons and now we feel that
we do have fully solid reasons. Is that
right?
>> The latter. It's something that we call
assumption accounting. So, you're almost
like an accountant like looking at like
how that thing is built. And generally
you would hope that every single sort of
logical premise that your result is
dependent on has been checked or even
better has been stated. I think in this
case and during the other formalization
process while the result is safe and
sound, there is an implicit assumption
that was sort of never made explicit and
you actually need to do quite a lot of
mathematical work to make that explicit.
So in a way we we caught that issue and
then we patched it. So people thought
think about verification as something
that's like a sort of like a stamp for
perfection, right? There's actually huge
amount of value in this like bug
hunting. Uh you're able to basically
figure out like what is a counter
example and then you can even try to
patch it or or you can try to do other
modifications to to the proof. And that
actually has the flip side of that I
think has a lot of commercial value.
Specifically you can imagine finding
counter examples which result in bugs in
hardware. Uh this will be something that
uh is quite interesting to various
hardware designers. Uh we're working
with some uh early design partners on
that. There are also for example the
same sort of dynamic happening in
software. If you're able to identify uh
you know, bugs in large code bases and
you're able to prove uh or patch the
bug. And if you're for example in the
smart contract setting, uh there are bug
bounties. People have awarded lots of
money. Uh not saying that we will go and
pursue those but people in the kind of
smart contract space are generally very
keen on the idea of using um a theorem
prover based software verification
system to try to figure out whether they
can verify smart contracts and
specifically catch bugs in these
contract because what what happened if
each each pretty big notorious bug is
people lose money. Real money's being
put in. Real people suffer losses. And
and you can also have this sort of
dynamics in other safety critical
systems like defense code as well.
>> What what does mathematical
superintelligence really mean in that
sense?
>> Yeah, I'm really glad you asked this
question. There are two layers to this
question and it's I think some nuance
points that I I think never were never
quite managed to get across. The
definition, I think, of a super
intelligent reasoner is something that
can do verified knowledge discovery. So
So there are two parts of that. One is
verified, one is knowledge discovery. So
this thing needs to be able to prove new
things or discover new things, tell us
new things that we don't know. And the
other thing is you kind of need to trust
it. Like you you kind of don't want to
linger super intelligence, which is a
really I think dark future that is, you
know, out of I think 5 million lines of
proof of the Riemann hypothesis, you do
not know whether there is a bug
somewhere in line 3,827,
right? And and then it's like, who is
going to do that line by line? So the
idea of, you know, a super intelligent
reasoner to be able to expand, which is
a knowledge discovery part, but also
contract, as in the verified part,
because there are a lot of, I think,
creativity parts that are also false.
The ability to expand and contract
expand and contract and kind of like go
from there in a sort of self-improving
way, which is able to conjecture better
as it is able to verify better. It is
able to verify better as it is able to
conjecture better, have harder task. So
conjecturing helps proving, proving
helps conjecturing.
>> [music]
>> Her world of verified, machine-checkable
discovery connects to something I have
wanted since I was an undergrad,
weighing tiny powders in a chemistry
lab. A dream that is suddenly, cheaply
come within reach.
>> [music]
>> I was a undergrad research assistant in
chemistry.
I used to joke that my life looked more
like the life of a low-level drug dealer
than it did like a scientist, because if
you just watched what I was doing, I was
mostly weighing out very small amounts
of fine powders.
And you know, I I can still kind of
remember it to this day, the lineup. Uh
we were doing a
the reaction development, so it was very
much kind of parameter sweep basically
in you know in analogy to what goes on
in in machine learning, it was
chemical parameter sweep. You know, what
if we had a little bit more of this
region? What if we had a little bit
less? We would just set up these assays
and kind of you know hold everything
constant
and vary one thing
four, five, six, seven different values.
Put them all in the same bath, you know,
take all the same measurements at the
same timestamps.
And I used to dream of automating that
stuff.
But it was very
long tail and it was very prone to
change, you know, there would be just
these little variations from one
generation to the next you know when we
did capture some optimization or we did
decide oh we're going to actually do
this just a little bit of a different
way.
It just felt like well it was way you
know our scale was too small and the
pace of change of the process was too
high. We just would never be able to to
automate it. You know, and plus I didn't
cost that much. So, now to see this
world where
you know, a couple robot arms maybe cost
about as much as I cost you know as a
undergrad research assistant for a year.
I would I might still be in science you
know if if I had had the opportunity to
instead of doing that weighing out if I
had been able to coach and iterate and
refine the robot arm
to the point where it could do it and
then come in next time and say actually
okay, you know, we want to add these two
powders in a different order. Can you
just make that change? And boom, it
makes the change. Like that is
such an unlock. I mean obviously these
things could then run you know, 24 hours
a day like the throughput that we would
have accelerated our work I would guess
by easily a multiple
just based on
letting the robot sit there and and set
up these experiments and and do the
parameter sweeps for us on the kind of a
24-hour basis. My guess is that what
took us a year to go through and explore
in chemical space
easily could have come down to a month
if you could get this
robot thing working, you know, even at
95%. We would have We would have
accepted some errors, too. It's
important to note.
So, I think that's super exciting and
you know, the sort of Cambrian explosion
of robot-assisted
scientists coming to labs that have tens
of thousands of dollars of budget to
throw at it, that
that's a layer of AI acceleration that I
think will you know, it'll be quiet in
all the places that it happens, but
it'll be potentially quite quite loud
and and very like impactful as it plays
out in all these different spaces.
>> Jed wasn't lying again from part two.
Now on the building side with the single
most concrete safety by construction
idea I heard all week. A way to route a
model's dangerous capabilities into
parts of the network you can simply cut
out. It's called gradient routing.
>> [music]
>> The problem is that most of the safety
training is done in post-training, not
in pre-training. So, once the jailbroken
model is there, uh once the model's
jailbroken, you can do whatever you want
a lot of the time. And so, we set out to
try to solve that at an earlier stage.
And one of the things that we've been
accelerating is an approach called
gradient routing, which we which
basically winds up in pre-training, you
route different dangerous capabilities
into different experts in a mixture of
experts model. So, you wind up having
some dangerous experts that learn
specifically the CBRN stuff or the cyber
stuff, and then you can later ablate
those experts. And this winds up uh so,
you completely remove it. So, you have
the regular model and then you have the
safe model that that that winds up being
public. And this is This has been going
decently well. It's like it's a it's a
it's it's still an early stage alignment
approach, but we're excited to release
it fairly soon because it potentially it
potentially solves this big issue that a
lot of people are very concerned about
right now today. And our larger thesis
is that if the field had been investing
more in AI alignment R&D instead of just
feeling compute. If we'd done this
earlier on, we would have found
techniques like this and then you
wouldn't have the issue right now with
the Trump admin and and Anthropic
because this would be all already in
Fable 5.
>> [music]
>> Then the software itself.
Eno Rhea's runs Factory, which builds
the systems that build code. And his
read on why Fable wins the big coding
benchmark is the most honest thing I
heard a builder say all week. It is not
the answer you would expect.
>> I I think that we should actually sort
of sit here and and frame what is
actually happening when we say like
Fable outperforms on Frontier code. So
Frontier code good great benchmark. Like
that's a I'm really glad that people
like the Cognition team are like
thinking through how do we how do we
measure on more novel and difficult
problems? Like the types of challenges
that contemporary models are facing. And
so I think we need more of those.
There's another great benchmark called
Program bench that also looks at like
reverse engineering on extremely hard
problems. The pass rate there is like
effectively zero. We have internal
benchmarks that we have zero percent
pass rates on. And I think that like
generally this is great when the when we
introduce these new benchmarks. But if
you think about what it means to score
on a benchmark, I mean you can sort of
read through, right? Oh, well, we
assessed correctness by running tests.
We used LLMs to judge correctness. We
built novel verifiers specific to the
problem. Basically, what that means is
that when somebody spends 40 plus hours
creating a verification of a single code
change, we can then reliably evaluate if
the model was good at working on that
problem. That is like
totally reasonable, but I think what it
translates to is that in the real world,
people the challenge is often not can
the model write code that works? It's
basically every other aspect like can I
trust that this model output code that
works? Um, does this model have the the
deterministic feedback loops inside of
the code base to get to that
correctness? The set of repositories in
that benchmark are all very well tested,
very well-known open-source code bases,
right? Where the maintainers have
approved it. The level of rigor of what
we would call agent readiness in
open-source code bases actually tends to
be much higher than in enterprises. And
so
which makes sense. You're basically
accepting changes from the outside world
from random people. How different is
that from coding agents where you're
sort of like getting changes that you
sort of lightly asked for and you don't
even know the source. It's kind of black
box generation, right? And so I think a
lot of open-source maintainers have gone
through the the rigor and the effort to
add these deterministic verification and
validation loops into their system such
that when a new change comes in, you
think about how did Fable get such a
high score? Well, it ran the tests. It
ran the linters. It did more focused
application of the type checking. It
used all of these tools to hill climb
its way to high success. And I think
that in general the if you don't have
those things, you're screwed no matter
what. And what we would sort of argue is
that all of these pieces are part of the
puzzle. You can't just plop good model.
You can't just have agent readiness with
a bad model. Like you you you sort of
need to go through and invest in
upgrading the basis by which your
company has these feedback loops. You
have to upgrade the way you think about
this because it's a risk thing. Like
humans have to say, I'm going to at this
point now start accepting code changes
that I haven't read. And then third, you
do need great models. So So I think that
like basically Opus 4.6 maybe was has
been sufficient and I would even argue
that before then. We've had models that
were sufficient enough to go full auto.
I think that all of these other things
need to catch up in order to then take
advantage of these models. And
basically, the gains we see in models
today are primarily coming from
effectively like the models getting
better at at getting away with not using
these verification loops like humans
are.
>> So, there's this giant feedback loop
that's extremely human-driven right now.
You can imagine, and in fact, some
people are starting to instrument the
whole thing end to end with AI. And I
think that the challenge that almost
everyone faces is this is one a totally
different problem from adopting
agents. And two, it requires effectively
a reframing of the way that your company
thinks about building software. How do
we set goals? What are we optimizing
for? What should our software evolve
into?
>> And we will very much look like VCs or
capital allocators, right? And I think
the the different strategies that
capital allocators take up today can
give you a picture of what software orgs
will look like. You'll have people who
are like VCing it where they're betting
on several products in a in a basket,
and they're saying, "Let me allocate
compute and build guardrails around the
shape theses around what my software
should evolve into." And I'm going to
allocate like a little bit to each of
them, and I'm going to double down on my
winners, right? So, I think I see that
as being like a very plausible software
organization strategy. I also think
you'll see people who are like
Berkshire's where they they're only
looking at like well-known, repeatable
kind of boring software businesses, and
they use scale, and they use the fact
that they're able to control large
amounts and volumes of this software in
order to accumulate kind of steady gains
as they sort of scale up. I think you'll
have boutiques that make one piece of
software really, really well, and
they're just incredibly good at making
this one piece of and maybe that's like
the one person billion-dollar company,
right? Like
>> [music]
>> And the person who created the Kotlin
programming language, Andrey Breslav, on
what software engineering becomes once
you stop writing code by hand.
Plus, a one-line observation about the
next 5 years that genuinely stopped me
cold.
>> Actually,
when we were starting, I wrote down this
formula that Code Speak equals software
engineering minus writing code.
So, we want to keep all the engineering
aspects of it, but you know, we we of
course see that humans shouldn't be
writing code manually anymore.
So, this idea [clears throat] with
intent recovery
is pretty fundamental because right now
everybody who prompts agents to get
working code, they're doing work that is
being like partly accepted and
translated into the code, but the rest
of it is being discarded. And there is
this kind of an unfair situation where,
you know, you're talking to your agent
in English or like in a natural language
anyway. Right and then you get code and
you check this code into a repo. And if
you're working in a team,
other people check your code out,
but not the human language, the code,
right? So, you're talking to a machine
in a human language,
but talking to your colleagues on the
team in machine language.
That makes not very much sense. So,
it's very obvious that there has to be a
next level where we all talk in like
reasonably high-level language which is
close to human language at least.
And here like the simple observation
behind what we're doing right now at
Code Speak is that you already wrote
these words down. You may have been
speaking into microphone, doesn't
matter. The words happened and those
words were enough to create the code.
Like this input determined the code that
you got. And like it might have been a
back and forth and you had some testing
and so on and so forth, but all that
input
is what determined the code.
Right? So, that input is enough to
describe this code. And most of the time
it's many, many times smaller than the
output. So, given
replacing the code with that input would
be really nice.
>> [clears throat]
>> Excuse me. But, you know, the the thing
is when you're working with an agent,
you have you know, you change your mind.
Basically, you you are uh extracting
your intent or realizing your intent as
you go. So, it doesn't really make much
sense to just read all your messages
from top to bottom. You need to sort
sort of compress them. Uh you know, if
you change your mind, you need the most
up-to-date version.
And this is what we do. Like, we look at
at this conversation and it's a little
more complicated than just looking at
your messages, but to simplify, let's
say we look at your messages. And we
create a specification based on that.
Basically, we extract requirements from
what you were communicating. We look at
what you requested, what you flagged as
errors, which is kind of uh the the flip
side of a requirement. And we just put
together a list of things you care about
that determine the actual output. And
then, if another person or you later
will be looking at this code and will
have the set of requirements
next to it. That gives you a very
concise representation of what the code
actually does. And you can imagine that
this can be happening like with multiple
people doing different things in their
own branches. And then, you know, if you
merge your thing or like submit a pull
request or something, you can look at
those requirements instead of code
because the code wasn't written by you
anyway. What actual actually comes from
a human is the requirements.
And, you know, this is how we can
elevate
what we do to that level. And this is
what we call intent recovery. So, I I
don't know what kind of models we get in
5 years. Nobody knows. They may be like
considerably smarter. They can be very
smart. They can be about as smart as
they're today. I don't know.
One thing I know is what kind of humans
we get in 5 years.
They'll be the same kind of humans.
We'll be as smart or as dumb as we are
today.
So, I think the bet to be helping humans
is a much safer one. As an engineer, I
never cared about writing assembly by
hand. Some people enjoy that, and they
remain the experts, and they have good
well-paying jobs. Uh but there are few
of those. And because there there are a
few of such people Well, not because,
but incidentally, there are a few such
people, and I'm not one of them. So, I'm
personally I I don't care about doing
low-level work. I want to do high-level
work, and I think these things will
enable us in doing high-level
engineering.
It's very hard. It's always been very
hard.
And uh I'm looking forward to the world
where I can like really focus on the
hard stuff.
>> [music]
>> Two quicker ones to round out the week.
Matt McKinney runs Loop, putting AI into
the supply chains that move physical
goods. And his reality check is that the
bottleneck was never the technology.
It's us.
>> [music]
>> The limiting factor for AI in the
enterprise is not technology.
It's change management.
And that will be the case in the Global
2000s.
And there's certainly Global 2000s that
are making very swift changes. They've
got great leadership. They're
prioritizing this from the top down.
But at the end of the day, culture is
one of the slowest movers. So, if you
don't have a culture of innovation
trying new things, it doesn't matter
what top down is doing. It's still going
to take a a long time to propagate
throughout the organization.
Uh but you do see leaders making those
changes.
I think in terms of
which companies will win,
AI native companies that
don't have the vestiges of a pre-AI
world, or the legacy companies with
greater distribution, I think it really
depends on the industry and if you want
to categorize it into two big ones,
manufacturing and services,
I actually think a lot of the
manufacturing companies,
they are much more defensible than the
services companies.
So, I think those companies will be
transformed by AI, but not disrupted by
AI.
And I think that they you look at the
legacy pre-AI services companies,
those will be completely disrupted
because the AI native services
are going to be so much more compelling
to the customer,
better, faster, cheaper times 10, that
it poses an existential threat to those
service industries. I think about this a
lot.
And the
throughout
civilization,
the arc of technology has always been
a feature of abundance.
The question is, is this time different?
And it
I think that that this time might be
different largely because the pace of
change and disruption is so fast.
If the pace of change and disruption is
faster than the rate of retool labor
retooling,
then you're going to have large issues
and
the only
and I'm not saying I'm not making a an
argument on whether the the pace of
disruption is greater, equal to, or less
than the rate of retooling.
But, what I do know is that the pace of
disruption is greater than the rate of
retooling, you're going to need policy
intervention
to be able to
stop civil unrest.
It also could lead to
the beginning of a new
government. Uh and I I I'm not saying
the end of democracy, but it could be
the end of
government as we know it. I mean, if you
look at a lot of technologies throughout
the millennia, it's really been a force
of change. Like, feudalism ended when
you could now all suddenly travel.
There's a lot of history context here
that you can take and extrapolate to
what what is different this time? All
the assumptions that we made about the
way that we live, what is different? I
think the two things would be one, the
rate of retooling has to accelerate and
I don't think we're doing nearly a good
enough job on that today.
Number two is that
when you look at
when you look at the the abundance
factor of
what else can we be doing with this? I
think that you've got to have
it not concentrated in few people.
You've got to have it not
uniformly distributed by any means, but
you can't have all of this concentrated
in
a handful of individuals or firms. It's
got to have You've got to have abundance
in the ecosystem.
>> [music]
>> And Sam Pasupalak of Skyfall on what
might come after language models
entirely, enterprise world models. And a
near future for commerce that sounds
more than a little like Minority Report.
>> [music]
>> So, Sam, imagine you have an AI
assistant that can write beautifully
crafted emails,
but ask it to reschedule your supply
chain when a factory shuts down and it's
utterly lost.
That's the gap that you see in uh many
uh processes right now. How can that be
addressed?
>> Yeah, I think maybe we can take a step
back about what we have seen the overall
success in the last 3 and 1/2 years is
first and then go from there. So, I
think if you think about like what has
succeeded since, let's say, November
2022, I think LLMs have succeeded in
like, I'd say, three broad categories.
The first one would be text generation
and information retrieval. So, you have
obviously with ChatGPTs and then the
uh Geminis and such. The second would be
the code generation where we have cloud
code and cursor. And the third to a
smaller extent would be in the video
generation paradigm. I think that's much
much smaller success than the other two
paradigms. Now, if we think about why
LLMs have succeeded and stuff and LLMs
basically if you you guys know this,
LLMs are trained on the World Wide Web.
LLMs are trained on Reddit, Twitter,
Wikipedia, everything on the web. But
when it comes to the enterprise, I think
all the like
LLMs are not trained on databases, LLMs
are not trained on time series data,
LLMs are not trained on everything that
enterprise had to do with on a
day-to-day basis. And LLM and
enterprises are more so, you know,
dynamic in nature. I think everything
changes in an enterprise on a day-to-day
basis. It's much more complex uh the
decision-making in an enterprise. So,
our eventual goal is to make an AI CEO.
I think that's the goal that we have and
that can be achieved through
uh a combination of technologies. Yes,
LLMs will play their part but with world
models and continual learning as well.
That's what we're That's what we're
going for. Essentially, I want to
replace the job that I do and which is a
lot of complex decision-making under
uncertainty and a lot of long-term
planning, long horizon planning and
such. And uh those things that those are
things that LLMs can never do because
they're simply based on next word
prediction, next token prediction.
That's the high-level essence of of the
company. In the long term, we want it to
be something like Minority Report. If
you remember precog in Minority Report,
I think uh that's where the future we
want to be where you can predict all the
different future simulations and then
and you select the best simulation that
fits to the best needs of the business.
In the present state where we are right
now,
uh we're still in very, very early
developments of world model right now,
so I think so from the enterprise
context if you think about let's say 12
to 18 months from now what we're going
to be building and what we're going to
be showcasing in a product is like if
the simplest form of an enterprise is
like an e-commerce business. Okay, so in
an e-commerce business uh, you have like
a you can have an AI CEO, you can have
an AI marketing agent, an AI sales agent
uh, and so on and they coordinate with
each other and you give a goal like I
need to have $2,000 of sales over the
next next week or something like that.
And these guys go to like figure they
coordinate amongst each other the
different sub goals and sub parameters
and they figure out okay I need to like
go on Instagram, figure out who the
right user set is going to be then go on
Shopify, try to create the appropriate
store for this kind of product, then
figure out a go-to-market plan and then
actually execute and and go deliver on
like getting the $2,000 in sales. That's
the most concrete representation of a
world model which we think we can build
over the next 12 to 18 months. Now
>> [music]
>> Underneath all of this building though,
there's a worry I keep coming back to
about what happens to everyone who isn't
one of the four or five companies at the
very center.
>> [music]
>> I do wonder what's going to happen to
companies sort of let's say
greater than four in any given space if
we think there's like four really
uh,
big centers of gravity that can you
know, dole out tens of billions of
dollars
a handful of times to pick up whatever
coding leader they want to grab or
whatever you know, I think this will
probably happen again. We've seen a
little bit of it but my guess is it'll
happen and it'll be even bigger than it
has been so far in like biotech for
example
uh, and it might happen again in
material science. It's going I think
it'll probably happen in these different
domains where
there is
um
enough
value that you want to that these
companies will pay up to buy their way
to the front of whatever new market
they're
turning their attention to at any given
time.
Um and when you're multi-trillion dollar
company, you can you know, you can drop
a few tens of bees here and there and
it's really no big deal. Um but it does
seem like we're going to see this kind
of crazy two-tiered outcome play out
over and over again where you'll have
competition for the cursors and the
um
you know, who I mean, I'm not even sure
really at this point who the biotech
players will be.
But I think that'll that'll happen again
there presumably.
And then, you know, what happens if
you're company five through a million in
that space? It's
I don't know. It's tough for me to see a
way through uh for a lot of these guys.
>> [music]
>> And the closely related one, not about
the companies this time, but about the
character of the models themselves and
what the economics quietly seem to
reward.
>> [music]
>> So you said earlier that your goal is to
have a AI CEO that can run a business
and that today
you know, obviously the AIs aren't up to
that. We've done a little gonzo
journalism talking to our friends at
Enden Labs who are trying to do just
that. And I'd say their real-world
experiments are mostly not super
competitive. They're
cafe there, you know, Gemini managed
cafe in Stockholm is like chronically
out of stock of key ingredients and
things and there's just all these sort
of, you know, obvious mistakes still.
But
nevertheless, the trend is
>> LLM based.
They're purely purely LLM based, yes.
>> Um
the trend is, you know, is is positive.
Although, there are some interesting
results recently with like the
Opus 45 to 48 series and even Fable they
were able to to test on two where
they're seeing that the best performance
in terms of how much money did you make
is
correlated with what they describe as
ruthless behavior. Various kind of
collusion, threats to other model you
know, there's like other models in the
simulation that it will
try to put pressure on in various ways.
And the models that don't do that
don't make as much money.
So, this sort of creates I think a
pretty interesting tension for us as we
go into this next phase of continued
scale up and longer time horizon
environments. It's like quite clear that
your top performing CEOs are going to
have a pretty wide range of tools at
their disposal. And you know, even if
they're like broadly law-abiding and
ethical, they're not going to be fully
honest. You know, they're probably going
to be willing to engage in some
deception, some bluffs. You know, that
these kinds of things are just part of
what it is to operate in a strategic
environment.
But I don't want to leave you in the
shadow because the same week that
produced this fight also threw a door
wide open. And it's open to you
specifically.
If you've ever wanted into this, the
barrier just fell.
>> [music]
>> You know, if there's kind of a call to
action on this, it is
with tools like this, with vibe coding
in general,
you can do ML research. You, yes you,
can do ML research. You don't really
have to have a deep background in math.
You don't really even have to know, you
know, how um you don't have to know how
GPUs work. You don't have to worry about
kernels. There is just so much work that
you can do at a
relatively high level because the
translation from ideas to
implementation, especially with things
like this,
but again just with five coding, you
know, to help out as well.
It'd be a little bit of a stretch to say
it's solved, but it's it's so much
closer to solved. It's like 98% of the
way solved compared to what it used to
be in terms of a barrier to entry. So, I
think this is a great
additional signal for people who have
ideas or just questions that they want
to answer to get in the game and truly
stand on the shoulders of giants and try
to get those questions answered. I've
seen a little bit of that
from people who've never even coded
before, but I think we could see a lot
more of it coming
basically now. There's no no reason to
delay any further.
>> [music]
>> And one last honest note about the
strange humbling job of trying to make
sense of any of this while it's still
happening.
>> I feel both that there's just
such gravity toward close watching of
the few companies and their interactions
with government and all that stuff. And
then at the same time, it's just
events are kind of defying analysis
because they do seem to be fundamentally
chaotic and just idiosyncratic in terms
of their their provenance, right? It's
like there's not really a lot to analyze
in some of these situations. It really
seems just
tough. Um so, I don't I don't really
know what to do with this tension
between
feeling the need to like be a close
watcher and then also feeling like,
"God,
there's not a lot of substance to it in
some of these pivotal moments, you
know?"
>> That's the week. The system card that
should give us pause. The government
versus Anthropic fight. The people
thinking hardest about whether the
reaction was right and the builders who
didn't slow down for a second of it.
We're live most weekday mornings. The
full conversations run far past what
fits here, and the best way to find out
if they're for you is to come watch one.
Same sincere ask as always. If a moment
earned your time or wasted it, tell us
which. We read everything and the show
gets better because of it.
I'll be making sense of this in real
time from here until the singularity.
See you Monday morning.
>> [music]
[music]
[music]
[music]
>> They want me in that briefing room.
The best you've [music] ever seen.
Said it builds itself now.
Machine improves machine.
>> [music]
>> Recursive self-improving. They can't say
where it [singing] ends. [music]
Then they look me in the eye. Don't go
to war with us, friend.
Nobody's [music] ever seen a thing like
this. It's true.
Tremendous. DANGEROUS. SO I KNEW [music]
what to do.
I did what nobody else could do.
Put the thing [music] in a submission
hold for you.
90 minutes pinned it down.
Tough as calling town. Everybody froze.
[music] I'm the one who shut it down.
>> [music]
>> Now [music] the geniuses who warned us
cried for 20 years
are on the cable [music] shows and in
brand new fears. They said somebody stop
it.
Well, somebody [music]
did.
And where's my thank you, folks? Not a
word, not a bit.
You wrote a million [music]
warnings, begged for someone strong.
I'm the one who moves, so don't tell me
I'm [music] wrong.
You wanted it DONE GENTLE, THAT'S NOT
HOW winning's [music] done.
The tough ones take the shot.
Believe me,
I'M THE ONE. [music]
>> I DID WHAT NOBODY ELSE COULD DO.
>> LIKE A WITCH THEY'VE NEVER SEEN. BELIEVE
ME, IT'S TRUE.
Had [music] it on the canvas,
didn't flinch a bit.
SOMEBODY HAD TO BE THE MAN, [music] AND
I'm the man.
The end.
>> [music]
>> THE END.
>> [music]
[music]
>> IF YOU'RE FINDING VALUE IN THE SHOW,
WE'D APPRECIATE IT IF you take a moment
to share it with friends, post online,
write a review on Apple Podcasts or
Spotify, or just leave us a comment on
YouTube.
Of course, we always welcome your
feedback, guest and topic suggestions,
and sponsorship inquiries, either via
our website, cognitiveevolution.ai, or
by DMing me on your favorite social
network.
The Cognitive Revolution is part of the
Turpentine Network, a network of
podcasts which is now part of a16z,
where experts talk technology, business,
economics, geopolitics, culture, and
more.
We're produced by AI podcasting. If
you're looking for podcast production
help for everything from the moment you
stop recording to the moment your
audience starts listening, check them
out and see my endorsement at
aipodcast.ing.
And thank you to everyone who listens
for being part of the cognitive
revolution.
