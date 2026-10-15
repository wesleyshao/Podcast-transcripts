---
访谈时间: 2026-06-16
访谈时间说明: YouTube 发布时间；未能独立确认访谈录制日期
嘉宾名字: "Joon Sung Park"
嘉宾公司名称: "Simile"
播客名称: "Sequoia Capital"
播客url地址: "https://www.youtube.com/watch?v=lfhFmwcESRw"
字幕来源: "YouTube automatic_captions en-orig"
全文提及的关键名词:
  - AI
  - agents
  - AGI
  - DeFi
  - Simulating
  - Humans
  - Scale
  - Simile
  - Joon
  - Sung
  - Park
companies: []
industries:
  - 加密
technologies:
  - Agent
  - DeFi
keywords:
  - AGI
tags:
  - 加密
  - Agent
  - DeFi
  - AGI
---

# Simulating Humans at Scale: Simile's Joon Sung Park

## Transcript

I am somebody who is quite inspired by
science fiction. And when you read
science fiction uh that covers societies
that have progressed far enough in its
technological maturity, you always see
two pillars. You have some version of
AGI and you have some version of
simulations that really help guide the
society. I do see an opportunity today
to really take the first crack at
building the simulation. I would not
have said that even 5 years ago, but
that is a conviction that we have built
up over the years as we are going deep
into this research.
Today we're delighted to have Jun uh
founder and CEO of Simile. Uh, Similey
is building an applied AI lab simulating
human behavior and societies and I'm
very excited to have you here to discuss
what you're building.
>> Same here. Thank you for having me.
>> Okay, take me back to April 2023,
Stanford, California, specifically
Smallville, Stanford, California. What
was what was that? So, Smovville was a
project that we were running at Stanford
where the idea was that we made this
observation that large lynch models can
now encode a lot of human behavior that
is embedded in its training data from
the web and social media and so forth
that if you sort of prove at the right
angle, you can actually get a lot of
micro behaviors out of these models. So,
given a very specific demonstration or
description of a situation, what would
person X do? And it would actually
generate really interesting behaviors.
We found that to be so interesting and
we found that to be the ingredient that
we had been waiting for for creating
really complex agentic behaviors. So
small bit actually was an experiment
where we decided that if we pushed this
as far as possible what would a society
that is created by these agents look
like. So we basically created generative
agents that is paired with generative AI
model with memory planning and
reflection to basically create this
lived experience of agents living in the
small town. So smallville was basically
a game town of 25 agents living in it.
Individual agents had a description of
persona but they would actually wake up
in the morning do their routines go to
work actually have relationship sort of
like people would and they would
actually have emergent phenomena like
having parties and so forth. So that was
the experiment that we ran.
>> What was the most surprising things to
come out of the experiment?
So one of the surprising things was so
the experiment the simulation itself
actually sets place the day before a
Valentine's Day. So you actually see
these agents one of the agents actually
thinking well I run a cafe. So she's a
cafe owner. Her name's Isabella. She
goes and thinks it would be great if I
can do a Valentine's Day party where we
invite a lot of friends, customers. So
you actually see her on the day before
Valentine's Day going around actually
gathering materials for the party,
actually telling her customers, hey,
we're going to have this party. Please
come. And on the day of Valentine's, you
actually see this immersion party that
actually get formed with all these
agents coming to the to the basically
cafe.
>> Did anyone not get invited?
>> Well, some of the people did get the
invite invitation, but they forgot.
That's one thing that did happen. Uh
some of the agents did not explicitly
get invited, but we had one agent who
got the invite, Claus, who decided to
ask his crush out on a date. So he would
actually bring in the date. They would
actually have a party at this cafe. So
quite surreal.
>> So how did you end up building
Smallville in the first place? Like were
you studying kind of human psychology
and social behavior or was this coming
from was this coming from the kind of
customer back or was it coming from the
technology out? So my particular team
has been excited about simulations and
we saw the vision of simulation failure
early on. So my career as a researcher
at Stanford really started back in 2020.
That was the year when GPT3 was about to
come out. It wasn't quite there yet but
it was just about to come out. We
started to get its first demos. And my
first year uh we wrote this paper called
opportunities and risks of foundation
model alongside many of the Stanford
researchers and was led by one of my
co-founders Perc Leang who is now the
head of the center for foundation model
at Stanford and when we were writing
that the part that I was really focused
on was well here's a new class of models
that we have not seen in the past that
these models that can be very
generalizable in ways we didn't quite
have in the past and I got into thinking
well if we can imagine the kind of
interaction we can create with these
models, what would that be? And many of
my colleagues back then were surprised
that these agents or these models can do
classification or simple generation. And
that was really incredible to see
because these models didn't really know
or didn't really wasn't really taught to
do that. But the part that was
surprising to me wasn't that these
models can do that because from
interaction perspective, we've known how
to do this for a long time. The
interesting part was well, these models
can actually encode human behavior. What
does that mean if we were to push this
as far as possible? So part of the
tradition I come from research included
what we call social computing and social
computing within human computer
interaction really has to do with this
idea of how can we build a better techn
technological platform that would enable
social interactions and collaboration.
One of the most difficult challenges of
building a social platform is not
necessarily testing the UIU UX of the
system, but it's more about when you
have tens of people, millions of people,
and down the line billions of people.
How do all these people come together to
create the immersion phenomenon that's
both good and bad and how can we design
for a scale? And so far, we didn't
really have a tool that would enable us
to test for that. The only way we test
it today is you basically field test it.
You release your prototype, see what
happens. And sometimes it actually comes
at a real cost. Obviously, it's high
cost in terms of human hours and the
time it takes. But at the same time, if
you have a bad design, imagine you have
a feed on social media that is more
likely to propagate certain emotion that
is negative. Then obviously that is
something that we want to avoid. But
this now gets tested in the in the
field. So we wanted to see whether we
can actually create a simulation that
would actually let you test for this. So
2022 this was actually a year before
generative agents we worked on a paper
called social similacra which actually
really was the precursor to the agent
paper that we ended up writing. The core
thesis was imagine you're building a
subreddit. You're a designer on a
subreddit. You want to see what people
might do in the subreddit which is
surprisingly hard task even for practice
designers. And we basically decided,
hey, we have this model seems unique.
Let's use this model to create
simulations of the entire subreddit. So
you define the goal, you define the
moderation strategies, and you populate
it with thousands of what back then we
didn't call them agents, but we call
them personas, but populated with
thousands of personas.
>> This is basically 22 uh version of
mobook, which is quite interesting that
it actually came back. And when we saw
that, we actually got a lot of really
important insights out of this. What are
the good behaviors? We actually
simulated a community where the entire
idea was for people to discuss with each
other the sight sing uh places to
sightsee in Pittsburgh. And all of a
sudden, you start to see this personas
actually collaborate to actually
discuss, hey, XYZ places are amazing. Do
you want to actually go to a trip
together and actually plan those trips
live in the simulated subreddit? So
that's how we got excited. So we saw the
vision and the excitement and the
potential applications failure early on.
But then the work that we had to do was
then demonstrating how can we go beyond
simple personas to create complex agents
that actually can think over time
because we want to simulate the
longitudinal aspect of the our society
and then actually validating that these
simulations are actually accurate in
practice. Was there a point of model
evolution at which you felt like okay
we're there the the models are good
enough for us to actually have a you
know faithful representation of human
society.
>> So Gypty 3 when it came out and social
similar was built with GP3 and it was
very janky. It didn't do any instruction
tuning. It did not follow your
instructions. So just to have it to
listen to you and do what you wanted to
do, you had to do some weird tricks with
prompting and so forth. But you could
actually see the promise. The model
actually have encoded a lot of human
behavior and you could actually see the
trajectory and when we had the
generative agents paper wasn't quite
tragic but we now had instruction
tuning. So we could actually build much
more complex agents that can reason
about its memory that wasn't really
possible when we did social similar and
since then of course the models have
improved. So where we are today is the
models at its foundational level have
reached a point where we can actually
imagine building these kind of
applications. Now the part that actually
I do think however that's quite
interesting here today if you look at
many of the large linkage model
companies whether it's open AAI
anthropic and many of the neolabs that
are getting formed the models they are
creating are models that I would
consider to be their north start to be
something that is similar to let's build
a super intelligent machines. These
machines are meant to be rational and
these machines are supposed to be really
amazing at technique problems that have
an objective answer.
>> So maybe that's not even the best
simulation of
true human society. Then
>> turns out,
>> yeah,
>> people are irrational. Yeah.
>> Right. We have a lot of subjective
values, preferences, and taste.
>> So you actually start to see divergence
in moral science going up and the
performance in its ability to predict
and simulate human behavior. So we have
sort of plateaued with current modeling
paradigm our ability to really simulate
humans. So it is sort of at the starting
good foundational level but to make it
really amazing we do need the next
frontier that is more geared towards
actually modeling people's diversity.
>> Very interesting. At what point did you
realize that you know what you did with
Smallville could become a company?
>> Right. So again the promise of
application was something that I was
very much inspired by early on by
simulation with social similacra and so
forth. But the part that I realized over
time is research and a company have very
different function. Research is an
amazing vehicle if you want to basically
do breath research. You are in a lab
surrounded by really smart set of people
and each of our each of the researchers
own a small piece of thesis and they go
explore some of those thesis blossom
into amazing research product but we're
not necessarily known for finishing our
job. We're not usually the one to bring
that research impact to the real world.
Company is a machine for depth for
search. You have a conviction on an
area. You find a hill that you want to
climb. This is the vehicle that let you
put together resources and an amazing
group of people to go after a singular
vision without hesitation. And we got
that conviction I would say about half
year after generative agents after the
original generative agents paper. We got
so much inbound interest initially from
actually social scientists who wanted to
run their experiments and all the RC
RCTs on our platform. Then very soon
after many of the Fortune 500 companies
who saw this demo and their board
members and CEOs who sometime visits
Stanford saw that and they start asking
well we go run all these surveys and
experiments and there's so many research
questions about the market that we
cannot answer today. Can we run that in
simulation? That started to really
intrigue me because that showed a clear
line towards a real world impact for
research which is not always the case
that we have that kind of opportunity.
So that is when we decided we actually
want to validate the simulations are
accurate. So we went out and actually
created simulations of thousand people
of the US population. We demonstrated
that using our architecture and the
models we can actually predict people's
behaviors 85% as accurately as people
replicate their own. When we saw that we
thought okay this is something that we
feel comfortable providing to our users
as a platform for simulating their
really important decisions. So that's
when the co-founders myself Percy as
well as Micah Bernstein was a researcher
and my adviser at Stanford. Both of them
were actually my adviserss. So the three
of us have been working together for
five years and now at this point it's
similarly six years but that's when we
got together to have the initial
conversation of can this be a company.
>> Got it. Amazing. Um maybe walk me
through a customer engagement end uh
today like who's a canonical customer
and which department and they come to
you what are they asking you uh and you
know what product do you or service do
you deliver to them
>> right so maybe an example that I can
give uh to make this concrete um so CVS
has been partnering with similarly for
the past I would say nearly half a year
uh and they they've been an amazing
partner the way we initially got in
touch with so our main buyer at CVS is
the lead uh it's a senior VP who leads
human insights and original story there
was he was he basically read my paper
that validated the age and simulations
and thought we have to bring this to CBS
because today we are bottlenecked by the
number of questions we can field test
and we're also bottlenecked by truly the
physics of human society. It's one thing
to ask surveys and experiments. Totally
different thing if down the line you
actually want to simulate the entire
market and actually map out all the
second order impact of the decisions you
suggest to your leadership. So he's been
looking around for that solution and his
cousin happened to know me and basically
told uh our buyer shri that the authors
of the paper are actually looking to
start something. So that's how we got
connected and in this particular
engagement usually the way this goes is
our customers are very much used to
working with polling companies or panel
companies today and there they go and
basically ask these companies XYZ are
the populations that we are interested
in better understanding can we go run a
research study of these topics
that initial stage looks very similar
for simile so our buyers come and They
tell us we want to better understand XYZ
population. Then similarly goes out and
we have through our partnership with
vendors. We have a strategic partnership
now with Gallup for instance who is a
polling and panel company where we go
out work with our vendors to actually
reach out to real humans. So these
simulations are grounded in real data
but reach out to those people collect
data that we believe are efficient and
generalizable about that person. So
imagine you have 15 minutes. what are
the magical questions you can answer or
you can ask these people during that
time. We collect that data, use that
data to create agents or simulations of
these people that can basically be used
to answer a large number of questions
that goes way beyond the original
domain. We load that onto our platform
and it's basically a SAS product. Our
customers come and they can basically
ask any questions about the group of
people of their interest.
>> So interesting. It reminds me of um in
autonomous vehicles, you know, you go
and collect a bunch of data from the
road and then you're able to augment it
with simulation. Is this similar concept
or are there big differences to to what
you're doing here?
>> It is similar concept in the sense that
of course you with the self-driving
vehicles. You want to create model that
is based on real world physics, but you
want to create a model that is
generalizable beyond your training data.
It needs to be generalizable into
different locations with different
weather conditions. Very similar concept
where what we want to create is we want
to reach out to real people and for
these people want to understand
something fundamental about these people
in a way that we can encode into the
model.
>> I would thought that the large language
models would be such a good
representation of you know the whole
world. Yeah.
>> That you could almost narrow it down.
you could tell Claude, you are a 34 year
old woman living in a you know by
coastal metropolitan area and you know
it would be able to have faithful
representation. So I'm actually
surprised that you go out to Gallup
maybe. Can you just explain why you have
to go out and collect any real world
data at all?
>> Yeah, one of the big questions here is
the question around say do gap. There
are things that people say and then
there are people there are things that
people actually do and the gap there is
real and a lot of the large language
models are trained on edit data
fundamentally it is the things that
people have said online that does cover
a large quantity of its training data.
So one of the things that simul
simulation platform does is actually
closing that gap. So a lot of the data
that we end up collecting by nature are
behavioral.
It also includes data that actually goes
into literally questions like just tell
me the story of your life. Turns out if
we understand the person's story of your
life, the kind of data you get from it
is what we consider to be the longtail
information about this person. It's not
about um what you've done in this
particular moment. It's not about very
broad questions like what's your view on
politics. It's about where you grew up,
what you what were some of the difficult
decisions you had to make in in life.
And what's interesting about this data
is it's an amazing way to build a
translational layer between attitudes
and behavior. So we combine these kind
of data sets but fundamentally that's
the gap that we want to close.
>> What sort of behavioral data do you
have?
>> So similarly does run a lot of
experiments. So kind of models that we
have trained for instance we have a huge
repo of RCTs. So randomized control
trials that were run in social
scientific context that were run around
pricing studies. So one of the models
that we are training is basically the
foundation model of human behavior in
quite a literal sense. We have all the
behavioral signal from RCTs. Can we
actually encode that into the model so
that the end outcome is a model that can
basically predict the results of any
RCTs?
At the same time, uh, one of the
conversations that we keep on having
with our customers that we're very
excited by is our customers then come
in, see that potential and their mind
goes to, wow, we have 90 million
customers, let's say here at CVS. How
can we leverage this kind of data to
create better simulations? So there's
also conversation around how can we in a
responsible and ethical way leverage
existing data that is also inhouse for
our customers then use that to create
augmented version of simile model. So
that of course is going to be more
fine-tuned specific to the population of
these customers.
>> Yeah.
>> But that's the kind of data that we will
be leveraging.
>> I see. And are you doing these
interviews typically by voice? Is it is
it a survey that you fill out? like
what's the modality?
>> So, it's a huge breath. Uh the quick
answer here is it's both. Um interviews
are fantastic if you want to get the
longtail information about people. So,
we actually do in the original study
that I conducted uh back in 2024, we
literally ask a question, tell me the
story of your life. Now, the way we do
it is we are training our own model. So,
it's a reinforcement learning loop.
Basically imagine the objective function
here is how can you spend the minimum
amount of time to get the maximum amount
about visibility about this person. So
that is one of the things that we do. So
basically training an interviewer that
is not really asking for factual
information or an experience about a
particular platform but just what are
the life story that people have that can
be used to train our own model for these
agents. And then for the more factual or
sort of a more discrete choices uh
choice questions surveys and so forth.
These are also very efficient. These are
time and data efficient because people
can fill out many of the questions in
short periods of time. So for those we
actually do leverage them in for
instance if you want to just have a
broad understanding of people's
viewpoints on certain topics, certain
policies and things like that.
>> You describe yourself as an applied AI
lab.
>> How do you think about where you want to
build your own models versus where you
want to rely on other existing models?
So in terms of building our own model
really the core thesis here is there is
an amazing model to be built that really
uncodes the diversity of people's values
preferences and taste in ways that
simply a rational model cannot do. So
one way I actually post this we're sort
of building. So imagine the current
today's model are akin to the CPU of
intelligence unit. It's a single model
trained on amazingly rational data that
is amazing at solving very complex
objective questions.
Simile's model is much more akin to
developing something that is close
closer to the GPU of the intelligence
unit where the idea here is we don't
actually need a model that is superhuman
at simile. In fact, we want model that's
as human as possible, but we want to
make sure that these models at the sort
of individual subunits can represent the
real viewpoints of different
populations. So where we see that gap,
that's when we go develop our own model.
But at the same time, we do leverage
volunteer models for instance as a way
to coordinate the research. Frontier
models are amazing at coming up with a
research plan. So that's where those
models actually do get leveraged.
>> Very interesting. Um, are people
typically coming to you with questions
around new product launches,
uh, you know, how they should be
marketing their companies,
pricing, all of the above?
>> So, it's it is all of the above.
>> Okay.
>> Our customer journey usually does
however start with a very concrete use
cases and problems they are trying to
solve. Uh, concept testing is a big one.
It's also a very straightforward one. So
they have a new concept, new product
idea, new market message they want to
test and they want to hear from their
users what they would think about XYZ.
This is one way for them to quickly test
those ideas. And then the promise they
quickly see is well right now we're very
much in the practice of testing five to
10 different ideas. But what does it
look like for us to test instantly
thousand different ideas across thousand
different sub populations? That's the
initial vision they see.
Then we really get into the nitty-gritty
uh details of well where the simulation
go from here. They then pretty soon
start asking well can this be used to do
product testing but not just simply
submitting like an image but imagine
basically asking these agents go
experience this product for 10 minutes
and tell us about what you experienced
what you saw. So you're basically adding
temporal dimension. Then you go into
things like multi- aent simulation.
Some of our customers very routinely
actually ask us to simulate their
earnings goal. This is actually a use
case that both surprised me at first but
this is also surprisingly a common ask
because of course the CEOs and board
members always need to think about hey
how are we going to design our earnings
call? How would the the audience react
>> so that is something that we also do and
this is very much multi- aent
simulation. you know, it seems like
there's so many use cases that could
potentially be tested once you have like
a simulated almost customer population,
right? Yeah. Um I'm curious
>> the value of research and testing in SIM
versus just like let's say you have a
new product concept that you want to
test. Why not just go run a thousand
Facebook ads and like you actually get
the click-through rates on this stuff?
Isn't that real world data almost more
useful than the simulated data on how
people might behave that you then
correct for with your own models?
>> So it's a great question and I think to
some extent here the answer has to do
with initially scale and then down the
line truly the new capability that comes
because you can simulate the
interactions. The scale question here is
actually quite straightforward where
yes, you can absolutely run Facebook ads
and Facebook testing. But the kind of
experiments that you can run in
simulation is actual behavior simulation
at scale, right? So you can basically
pull in any number of users doesn't even
have to be bounded by the number of
population that's available on Facebook.
And it's also much more representative
because only certain groups of people
will actually respond to the online
experiments. But similarly the model
that we are creating one of the key
promises is that it is representative.
We do the hard work of actually gaining
the representative set of people and
then collecting the data that would
actually represent them properly. So the
scale representativeness is something
that many of our users do not have easy
access to. This is actually one of the
common ask also that we do get or common
sort of pain points that we have heard
where the question that many of these
people have isn't about like what
questions do we ask these people but
it's about in the first place how can we
get to the population that we're excited
to talk to that's a huge bottleneck.
Then down the line you can actually
really start to imagine and this is
something that our customers and some of
the most forwardlooking customers are
now going into which is what are all the
downstream implication of the decisions
you make. It's not just about whether
imagine you have this particular product
will do you like it or do you not like
it? Would you pay for this not pay for
this? It's not necessarily the just that
initial questions that we want to answer
and finish but we want to understand
imagine you're a car company. You
launched an electric vehicle in this
market. Maybe the electric vehicle does
really really well. So we can help you
do concept testing around marketing and
the product around the electric vehicle.
But what does that do to the perception
of let's say non electric vehicle? Does
that change the market perception? Then
what does that mean for the rest of the
product line? And how do you balance
those kind of second order impact of
your decision in a way that is more
evidence-based today? There's no way to
test for this.
>> Yeah,
>> you can run this in simulation. So
really going beyond simply asking one
question at a time, but then to think
about what are the long-term
implications of your decisions is
something that our customers are quite
excited by.
>> I'd love to understand how you think
about how predictive your model is in
actually simulating real human behavior.
I imagine you have a lot of eval. I
guess what is your northstar metric? How
do you guys do on that? Um and you know
what do you think is the theoretical
limit?
>> It's a great question. So theoretical
limit and let me just start from there.
certainly does exist in the sense that
humans are genuinely there's a lot of
randomness that if you ask me the same
question I actually answer the question
slightly differently. So there is
certainly that degree of randomness in
human behavior. However, there's a lot
of gains in performance that we can have
even today in the way we're predicting
people. So the measurement that we do is
so at the level of population we measure
the distribution of responses if it is
more quantitative. So we actually
measure total various distance which
basically shows how close are the
distributions of the ground truth versus
the simulated information
and that is a metric that we run across
all the use cases that our customers
have and we have certain threshold that
we believe is good enough for decision-
making. So a TVD of let's say less than
0.15 we believe is actually quite strong
evidence for making decision. So that is
a northster state that we want to hit
for this class of use cases that are
more quantitative that's more question
and answers. This also does cover RCTs
which is many of the core use cases our
customers have. Now there's actually a
really interesting then question to ask
around well what about multi- aent
simulation? What about all the
downstream implications we're going to
be simulating? What does the evaluation
of those look like?
>> Yeah. And then do you daisy chain errors
as you kind of you know if this one is
85% accurate and then this agent is
telling another agent something and you
know like do you accumulate errors as
you go as you go towards multi- aents
>> exactly and one of the core thesis here
is we basically see two categories of
simulations one simulation is what I
would consider to be simulations that
converge the other categories of
simulations are the simulations that
diverge and sometimes they actually
coexist and it's really about what
research questions do you have questions
that converge
doesn't actually matter if you have a
little bit of error. Now the error
cannot be obviously so dramatic that it
sort of is completely detached from
reality but you actually are okay even
if the errors do compound over time
because the pool towards of convergence
is strong enough that you'll actually
understand where everything would fall.
A good example here actually is if you
simulate a network of people then that
network will always have a hub that gets
formed. This is what sort of network
scientists would call the skillfree
network. For instance, this is actually
what powered Google too. One of the core
observation of page rank was doesn't
matter how these networks actually get
formulated, you actually see some web
pages that get exponentially more links
that are attached to it. This is a very
fundamental uh behavior in humans that
we also see in simulated networks and
that convergence always happens as long
as you are replicating human behavior
with certain threshold accuracy. Now
there are then questions that generally
do diverge. It's like your classical
questions like was World War I
inevitable or was it not?
And there it is sometimes difficult to
run the same simulation over time and
get the same exact outcome. Imagine
you're running a this is not something
that necessarily similarly right now is
going into but imagine you're running a
simulation of an election. Will the same
person win the election every time?
There are a lot of downstream
implications of every single decision
that does happen. So it does diverge
there. The core evaluation is around
confidence. So imagine you run the
simulation 100 times. How many of those
times do the results come out to be X?
And how can we actually use that to
basically create a bootstraps resembling
to calculate the confidence around the
simulations. Those are some of the
questions that we do ask. And a huge
part of this also of the power of
simulation is then to show when it
diverges to show the diversity of
possible outcomes so that people can
actually look understand the cause or
mechanism of how we got to those
outcomes and prepare for those futures.
So those are some of the implications of
divergence in simulations.
>> Are there any mathematical descriptions
of like why something would converge or
diverge? Like I imagine if you have like
an average function maybe you converge
and then if it's like a you know you're
splitting outcomes to a binary then you
might maybe diverge but
>> yeah so the intuition I think is close
uh and technically this is also a
research topic so similarly is a
certainly a company where we do go deep
into this research topic in the sense
that I see simulation as a field as akin
to developing your day one of inferial
statistics. you know inferial statistic
scientists actually had to do a lot of
discussion and research over time to
decide that P less than 0.05 is actually
evidence that is strong enough for
science. Similarly is working on setting
the same kind of threshold and standards
for the rest of the field. So those are
the intuition. I think that's exactly
the right intuition in terms of actually
how to make a robust mathematical
equation around when it's going like
what's going to happen when it is a real
research frontier for simulations.
>> Thank you for being nice about my vibe
mathing. Um I'm curious you know it
seems like so a lot of force 500s coming
to you. I'm wondering whether there are
you know non-existing corporate use
cases that might you know the like great
mysteries of our society that might
become solved. And for example, I'm
wondering about economics. You know,
central bank decisions oftentimes like,
you know, I've I personally believe in
that macro. Nobody's nobody knows
nothing. Uh and oftentimes a lot of the
issues come about from human psychology.
Um so to me, macroeconomics is a
function of simulating human behavior at
scale.
>> You know, I'm thinking even in the
venture capital use case, we we often
debate internally, you know, does value
acrue to this company or not? you could
you could you could run the simulation
of all the different layers of the AI
stack and and almost figure out where
durability and value value occurs like
you had a kind of perfect simulator of
human behavior there's so much more you
could do than serving the Fortune 500 do
you agree with that and then if so are
you serving governments
uh you know the like
>> yeah so it's interesting um when we were
still researching in this area the way I
actually uh back then my adviserss
Michael and Percy excited about this was
I basically told them look we do this
right there's a Nobel Prize to be won
there and I truly believe that and it's
also not surprising in that your
classical economics uh simulations
things like Asian based models that
really pioneered our understanding of
back in the day the kind of topic they
studied was how does segregation happen
what are the causal mechanism for
segregation
So scholars like Thomas Shelling would
actually build agent-based models that
are extremely simple and rudimentary but
that showed something deep about human
macro behaviors and he of course went on
to win a Nobel Prize. I see the same
opportunity here but in an augmented way
where back in the day the agent-based
models were very much deterministic in
some sense where you basically in this
simulation of let's say like motor of
segregation from like 30 years ago
individual agent was simply red dot or
blue dot and every game iteration they
would look around its corner see how
many of its neighbors are of the same
color and if that threshold goes below
certain threshold then they will decide
to move to a new location that was it
but Now we can actually create real
agents that replicate the full richness
of individuals and run the same kind of
simulations. So the kind of questions
that we can ask that goes beyond simply
the commercial use cases for instance in
the in the context of macroeconomics
actually the questions that I actually
did get asked from economist uh were
things like when does bankr run happen
or questions like climate change one of
the sort of core blocker of climate like
solving that issue is the collective
action problem of many nations. Can we
actually simulate that? Or what are the
signals of a democracy that is about to
collapse? Can we understand the origin
story of the monetary system? These are
the kind of simulations that I do
believe ought to be the northstar state
of this field. And it is sort of
interesting to imagine like what that
would actually look like in practice,
right? Because these would involve very
large scale simulations with many agents
interacting with each other. I do see a
future where today this is certainly not
the case. Uh today a simulation is quick
and fast to run. But what about
simulation that takes actually a$und00
million to run once and could take many
months to run but when we run it it
solves one of the fundamental questions
of our society. That I do think is
genuinely a very exciting possibility
for this field. I agree.
>> I'm even thinking like politics for
example could be forever changed of say
everyone has an agenda of how they say
>> some policy change will will impact
things. Why don't we just run the
simulation
>> and understand all the downstream
implications.
>> Yeah.
>> And not just what's going to happen this
year but what does it mean in the next 5
to 10 years.
>> Exactly. Fascinating. I was going to
close by asking you what makes you
excited about the future. Is it what we
just talked about or is it something
else?
>> I am somebody who is quite inspired by
science fiction and when you read
science fiction uh that cover societies
that have progressed far enough in its
technological maturity, you always see
two pillars. You have some version of
AGI and you have some version of
simulations that really help guide the
society.
I do see an opportunity today to really
take the first crack at building the
simulation. I would not have said that
even five years ago, but that is a
conviction that we have built up over
the years as we are going deep into this
research. And what's exciting is there's
a clear use case today that can serve
our users. But then there's a lot of
innovation that is yet to come that I do
think will build up to actually building
simulator that's akin to the CERN of
human society.
And one of the things that my one of my
my co-founder Percy sometimes say is you
look at the greatest scientific
innovation they often start from an
amazing measurement. Hubble telescope
really change the trajectory of how we
understand the universe. Simulation can
be that for human society. So the thing
that does excite me there's a lot of
focus on natural sciences but how can
social how can simulation really unlock
our understanding of humanity and social
sciences and how can we actually use it
to make our society be a better place
that's exciting
>> I remember reading somebody was excited
about you know there's a small but you
know breathtaking chance that you know
the field of economics as we know it may
actually become solved by simulation and
I'd extend that not just to be economics
but kind of everything that deals with
uh human behavior uh and social sciences
which ultimately is everything around
us.
>> Truly
>> wonderful. Thank you so much for joining
today and sharing the story of both
Smallville and what you're now up to at
Simil. I really enjoyed the
conversation.
>> Same here. Thank you for having me.
