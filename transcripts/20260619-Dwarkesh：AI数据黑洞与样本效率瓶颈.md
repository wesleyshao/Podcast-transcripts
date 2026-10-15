---
访谈时间: 2026-06-19
访谈时间说明: YouTube 发布时间；未能独立确认访谈录制日期
嘉宾名字: "主持人与嘉宾未确认"
嘉宾公司名称: "Dwarkesh Patel"
播客名称: "Dwarkesh Patel"
播客url地址: "https://www.youtube.com/watch?v=4pG3SJQPAwk"
字幕来源: "YouTube subtitles en"
全文提及的关键名词:
  - AI
  - AGI
  - robotics
  - DeFi
  - The
companies: []
industries:
  - 机器人
  - 加密
technologies:
  - DeFi
keywords:
  - AGI
tags:
  - 机器人
  - 加密
  - DeFi
  - AGI
---

# The data black hole at the center of AI

## Transcript

So one definition of intelligence is sample  efficiency. That is to say, how much data do
you need in a given domain to operate fluently  and competently? And it's actually not clear
that we've made that much progress in training  sample efficiency over the last few years.
It seems more like we've just dramatically  widened and improved the data distribution.
The main way that AIs have been getting  better is from adding more and better data,
and scaling the compute required to develop that  data in the first place. Obviously, RL is the main
way that this has happened. You can think of RL  as basically a kind of synthetic data generation,
where you dump a ton of compute against a  verifier — or a rubric, if you have an LLM
as a judge — in order to find out what the good  data is in the first place. And then you train
your model to predict these correct rollouts,  much in the same way that you might train that
model to predict the next word in internet text. For this process to work, the model must have at
least some prior probability of anticipating the  correct solution in the first place, which is why
you need mind-stretching amounts of human expert  trajectories in every single field and skill that
you want the model to eventually be competent in. It's hard to overstate how task-specific and
bespoke this human expert data is. If you want  some intuition, I recommend checking out the
job descriptions on Mercor or Surge's  websites. There are listings for Word
specialists who will convert legacy documents  into polished Word files, and legal experts who
will write realistic M&A diligence reports or  securities filings, and management consultants
who will write up template market research. And it is not only that the data have to be
so domain-specific, but there has to be  so much of it. Each skill corresponds
to at least hundreds of human experts who are  generating example completions, writing rubrics,
and explaining their chain of thought. There's a reason that the data industry
producing these expert labels, and the RL  environments in which these meticulously
cataloged skills can congeal, is earning billions  a year in revenue, soon to be deca-billions.
Now imagine if it took a couple decades' worth  of courses with hundreds of concurrent professors
and millions of practice tasks for you to  learn how to polish a Word file. Even the
task-count difference here understates the gap,  because the models have to grind through their
far more numerous tasks, each far harder. Whereas a human student might practice a
textbook problem once or twice, with GRPO,  these models are generating hundreds to
thousands of rollouts per task, and they need to  do this to solve the credit assignment problem.
The correct way to think about these models is not  like a human who has learned all these different
skills that you see the models displaying. It's  more like a Frankenstein's monster that has been
built out of a billion grafts of carefully  constructed examples, all sewn together.
Epoch recently reported that open models lag  state-of-the-art frontier models by four months.
I think the reason it is relatively easy  for open source and previous laggards to
catch up to within months of the frontier  is that data is the real driver of progress.
And data can be easily distilled from public  APIs, whereas hyperparameters, training tricks,
and architectural optimizations cannot. If  the latter were driving most of the progress,
then catching up would be far harder  than we are observing it to be.
It is easy to forget how much data these models  are trained on, and how much more it is than what
we humans see in our lifetimes. We see these  AIs as a galaxy glittering with capabilities.
But at their center, invisible to the naked  eye, holding all the constellations together,
is an unimaginably massive black hole of data. I just want to make a couple points of
comparison to illustrate just how big  the sample-efficiency gap is. Here's one.
If a person sees and hears on average, let's say  generously, 2,000 words an hour, then between
the time they're born and the time they're an  adult, they'll see about 200 million tokens.
Now, by contrast, these frontier models  are trained on somewhere between tens to
hundreds of trillions of tokens. That  is close to a millionfold difference.
Here's another point of comparison. If you  wanted to, you could learn to teleoperate
any random humanoid or robot arm within hours.  And if we could get AIs to learn just as fast,
robotics would be a deca-trillion-dollar industry,  and you'd have an endless army of Unitree G1s
doing all kinds of useful work in the world. But the reason we can't do this is that our AIs
learn much less efficiently than we do, and even  with the millions of hours of demonstrations that
we've collected, this is not enough to allow  them to perform complex, open-ended tasks.
And a final point of comparison: a teenager  can learn to drive a car with about 20 hours
of practice. And even if we include their 16  years of growing up and understanding how the
world works and building physical intuition,  that is still three to four orders of magnitude
less data than Waymo and Tesla are using  to train their self-driving car models.
Now I want to deal with a couple of common  responses and objections that people have to
these kinds of comparisons. One thing people will say,
and I think Karpathy said this when he came on  my podcast, is that for humans, many billions
of years of evolution had to go into basically  pretraining us. And so we're being unfair when
we're comparing how little data we see within  our lifetimes to what these cold-started LLMs,
which are just starting off with a totally  random initialization, have to learn from.
I think this is not the right way to think  about it. Our genome is only three gigabytes,
and only one to two percent of it is protein  coding. There is simply not enough space to
store the parameters of this network  that evolution supposedly pretrained.
I think the closer analogy is that evolution  found the right hyperparameters and the right
loss functions, and that within our  lifetime, we are still building up
the connectome in our brain from scratch.  That is to say, the thing analogous to the
weights and parameters of the neural net itself. And even if you granted this comparison and said,
"Yes, the hundreds of trillions of tokens these  models see to get pretrained is similar to just
catching up to evolution," that still doesn't  explain why any new marginal capability that you
want to give these models takes so much data. Once you have been educated, again,
you don't need a hundred different professors  to teach you how to learn a new programming
language. But these AIs, even once they're  pretrained, still require enormous amounts
of data to learn the next marginal skill,  and the next marginal skill after that.
Another objection to this kind of comparison  is that we're not including the multimodal
data that we're seeing in our lifetimes. So if  we include all this sensory information that
we see from birth to adulthood, that's probably  tens to hundreds of billions of tokens of data.
And my response to this objection is simply  that blind or deaf people, who are cut off
from parts of this sensory stream, still have  general intelligence. That suggests to me that
all these billions of sensory tokens are not  really the thing that is making humans smart.
In fact, deaf people who communicate through sign  language and reading, and not through hearing, are
probably ingesting far less than the 200 million  language tokens that we ballparked earlier, which
suggests that even the millionfold difference that  we calculated earlier might be an understatement.
Okay, the third common objection people make  is that we just haven't scaled enough. We
have these scaling laws. They tell us that  bigger models are more sample efficient.
The human brain, we know, is  about 100 trillion synapses,
and we have frontier models that are currently  around five trillion parameters. So maybe we
could just achieve human-level sample  efficiency if we made these models
one to two orders of magnitude bigger. The reason this objection is off-mark
is actually quite interesting. If you look  at the way the scaling-law equations work,
they tell you that the parameter and data  terms are added to the loss independently.
Suppose you have a model, and you've  trained it compute-optimally, and you say,
"I want to be sample efficient. I want to use  as little data as possible, and I'll throw in as
many parameters as necessary to make that happen." Take the constants from the Chinchilla scaling-law
paper. Even if you increased the number  of parameters by infinity, that would only
decrease by a factor of ten the amount of data  that you need in order to keep the same loss.
Humans are somewhere between thousands to  millions of times more sample efficient
than these models. So scaling the size of current  models simply can't make up for that discrepancy,
and this really does suggest that humans  are on a different scaling curve altogether.
Okay, all these nerdy comparisons aside, you might  ask: why do we even care about sample efficiency?
Is this actually necessary for the labs to  achieve the two overarching objectives they
have, which are, one, to automate white-collar  work, and two, to automate AI research itself?
The bet that the labs are making with white-collar  work is that the common tasks that a software
engineer or analyst or accountant needs to do  are common, and as a result, you can bring them
into the training distribution quite easily. If you look at the revenue curves of these
labs over the last few months, it does suggest  that there's an enormous amount of value from
bringing into distribution these kinds of  common tasks, even if we can't replicate
whatever is making human learning so special. And it might be more inefficient to train AIs
to do these kinds of tasks than it is to train  humans, but so what? Human lifespan simply does
not allow for the quantity and the breadth  of training that these models experience.
If you, as a human, had some weird learning  disability where you needed to read through every
public repository on GitHub before you could be a  competent software engineer, then it would simply
not make sense to train you up. You'd be on Social  Security by the early stages of your education,
and even once you were trained, you would  only be able to work on one project at a time.
But AIs can learn these skills by firehosing  gigawatts of training at a time, and what they
learn can be amortized across billions of sessions  at once. So we can be ludicrously inefficient in
training them up and still be wildly in the green. And then there's a question of how much
out-of-distribution thinking white-collar  employees need to do that you simply can't
train for in advance. This is more a question  about the nature of different jobs than it is
a question about AI research, and it also  depends on which job you're talking about.
Some jobs are so mechanical and predictable  that we were able to automate them long before
the modern era of AI, for example, bank tellers  or travel agents. But there are other jobs that
require dealing on a daily basis with problems  that are quite distant from the data distribution.
I think software engineering is probably one such  job. This is the job that AIs are supposed to
take first, but I would be willing to bet that  there's overall more demand for human software
engineers in 2028 than there is right now,  largely due to the complementary input of AI.
The labs' plan for this latter category of  jobs is first to automate AI research and
then have the automated AI researchers  solve the sample-efficiency problem.
So then the question is: can AIs, which  do not have human-level sample efficiency,
nonetheless solve the remaining research  problems that stand in the way of
human-like intelligence and learning? This is a very complicated question,
and I'll have to address it in a much longer  future blog post. But just to tease it a bit,
I think that the way people currently think about  an intelligence explosion is very clumsy, because
either people dismiss the possibility of AIs  speeding up AI progress altogether, or they assume
that some kind of God pops out the other end. They don't reason carefully about what it
looks like to have a period where AI  progress is much faster than usual,
but to have that happen on top of LLMs and the  particular kind of intelligence that LLMs are.
But I'll save that for next time. In the  meantime, if you want to read this blog post,
or all the other blog posts I write, or be alerted  when I write a future blog post, go sign up for my
newsletter at my website, dwarkesh.com. All right, I'll see you later.
