---
访谈时间: "2026-07-17"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。YouTube 字幕抓取返回 HTTP 429，改用视频简介指向的公开 Substack transcript。"
嘉宾名字: "Ankit Gupta; Francois Chaubard"
嘉宾公司名称: "Y Combinator; Google DeepMind"
播客名称: "Y Combinator"
播客url地址: "https://www.youtube.com/watch?v=qz4GQ0zUFRw"
全文提及的关键名词:
  - "world models"
  - "sample efficiency"
  - "intelligence per watt"
  - "intelligence per sample"
  - "ARC-AGI"
  - "Newtonian mechanics"
  - "model predictive control"
  - "control theory"
  - "deterministic differentiable control"
  - "Monte Carlo tree search"
  - "AlphaGo"
  - "robotics"
  - "self-driving"
  - "model-based reinforcement learning"
  - "model-free reinforcement learning"
  - "Dreamer"
  - "physics-informed neural networks"
  - "tactile sensing"
  - "neocortex"
  - "hippocampus"
字幕来源: "public transcript: https://ycrootaccess.substack.com/p/world-models-an-intuitive-introduction"
YouTube视频标题: "The Key Thing Human Brains Have That AI Is Trying To Learn"
---

# The Key Thing Human Brains Have That AI Is Trying To Learn

## Transcript

#### 00:00 — Intro

**Ankit Gupta**

One of the biggest open problems in AI right now is how to solve sample efficiency. That is, how do you get models to quickly learn new tasks or skills from relatively small amounts of training data?

**Francois Chaubard**

Humans do this incredibly well. We can learn new games, concepts, and skills, often after just a handful of tries. Our best models, on the other hand, often need tens of thousands of data points just to learn.

**Ankit Gupta**

So today we’re going to discuss what many top researchers believe is the most promising path to closing that gap, world models.

**Francois Chaubard**

We’re going to discuss the motivation and math behind world models, current applications, and why this approach might be the key to unlocking AGI.

**Ankit Gupta**

You and I have talked a lot about the various ways people are creating models and the sample efficiency of them. Why don’t we start by just defining sample efficiency and how we intuitively think about it as humans?

**Francois Chaubard**

Yeah. So I think from my perspective, the two major problems that we haven’t left to solve is intelligence per watt and intelligence per sample. Intelligence per watt is how many valve perplexity points we get per watt of spend. And then intelligence per sample is basically if I have one additional sample in my dataset, how much more intelligent am I getting? And so if I imagine I have a new tasks like ARC-AGI, For example, I think really François Chollet has been on the forefront of this thinking and talking about intelligence as a rate of skill acquisition versus skill acquisition and that’s very different. And so how fast do we get smarter with more and more samples? And these things are incredibly poor at getting smarter with fewer and fewer samples.

**Ankit Gupta**

And for context, the ARC-AGI test sets are a really good example of cases where humans are intuitively very good at them. Most humans can intuitively solve those puzzles with some amount of thinking and effort. But our current state-of-the-art AI systems, what people consider frontier intelligence, basically can’t do them.

#### 01:45 — What would perfect efficiency look like?

**Francois Chaubard**

Right. I mean, we come into new problems with such inductive bias from K through 12, all this math in school that we’ve had, that these models are kind of getting from compressing the entire internet. And so when we come in, we’re not coming in tabula rasa or bare bones, but even so that they have... I don’t know what percent of the internet you’ve read. I’ve read very little percent of the internet, but despite that and having read the entire internet, it still can’t really do well and generalizing to these new tasks.

**Ankit Gupta**

So now let’s think about this in the extreme cases. In the extreme case where let’s say we were perfectly sample efficient, we were as sample efficient as possible, what would that mean in terms of a model that is taking a set of actions in the world?

**Francois Chaubard**

Well, I guess the perfect sample efficiency would be zero samples. And there are examples of this, and that sounds absurd to say. And the example, the hypothetical I’ll give on this is imagine I had a perfect world model, then I should never go to the environment to go and collect samples to train on. And well, that can’t possibly happen for us. No, it actually can happen. We do it all the time. It’s called Newton’s Second Law of Motion. In Newtonian mechanics, we basically know how to get an object from point A to point B with a rocket quite easily just by following Newton’s laws of motion.

**Ankit Gupta**

Yeah. When NASA plans to intercept an asteroid and is planning it years in advance and can set it off in a trajectory where it just glides to the right thing and intersects to the right point, that is an example of a perfect world model we’ve built where we’re then just letting that world model act. And that system does not need to intelligently collect new samples from the environment to decide which direction to go next. It’s already been pre-programmed and it can perfectly do it.

**Francois Chaubard**

Yeah. Can you imagine if we needed to collect a one million training examples of us shooting spaceships to the moon to know how to do it? We definitely wouldn’t have the Apollo missions, right? But we do have that ability because the real world is differentiable and we can do something called model predictive control that we’re going to talk about in a little bit. But even in our own brain, I was just thinking about this on the drive up, but there’s so many ways that I can basically think about the things that you are going to say or what a VC is going to say when I was pitching them or what-

**Ankit Gupta**

A customer might say.

**Francois Chaubard**

... a customer might say. And even product, having taste, what is taste? It’s predicting that other people are going to like this thing. And so we’ve built this world model over years of entrepreneurship, 10 years of getting it wrong, that maybe Bill Gates, Steve Jobs and Jensen have 50 years of world modeling experience to know what people want. And basically this is actually proven in the 1967 Cog-Sci study by Richardson that basically showed that if you take a cohort of three groups of people and you have one go practice layups in basketball and they go and they shoot, for one hour they improve by I think it was like 24% or something like that. And then if you take the other one and they just blindfold them and they imagine laying up a basketball, they improve at 23%-

**Ankit Gupta**

Interesting.

#### 05:10 — World models in the human brain

**Francois Chaubard**

... against the control. I mean, that’s insane. It means that we have this crazy good world model and there’s this neuroscientist at Stanford named Shaul Druckmann who basically is of the view that the entire point of the growing neocortex during the great critical expansion 10 million years ago was to get better and better and better and better at world modeling. And having just like my little VLA, which we’ll define of predicting the next action is not as good as having a world model to lean on either for training purposes or for test time adaptation.

**Ankit Gupta**

Yeah. What it fundamentally comes down to is we as humans, we think about our intuitive ability to think as coming from some implicit world model we have in our heads, encoded by genetics and our ability to learn and whatever else. It seems like models can do surprisingly intelligent things despite not having an explicit world model when it comes to natural language. When they’re just talking, it seems like maybe under the hood, deep inside the weight somewhere, there’s some kind of implicit understanding of the world, but there isn’t an explicit representation of that. But it seems like in certain domains, especially in robotics and self-driving as we’ll talk about, that sort of breaks down. And maybe it would be helpful now to just think a little bit about and just sort of define some of the pieces of what makes it challenging in these different domains, and then we can use that to build up to why it’s particularly hard in things like self-driving and robotics to get these types of predictive models to work.

**Francois Chaubard**

Yeah, let’s do it. So let’s actually take a step back and just talk about control, reinforcement learning and define some common terms. So typically we teach a course called Decision Making Under Uncertainty, which is the main reinforcement learning course at Stanford. I like to show a specific example of let’s say I have some drone and this is my poor little drone here and it has some mass.

**Ankit Gupta**

Helicopter.

**Francois Chaubard**

And we know that gravity G is pulling down on it and it’s currently at position T with velocity T, which we will collectively call the state. And to be really clear, this is going to be PX, PY, PZ, and VX, VY, VZ.

**Ankit Gupta**

It’s like the six-dimensional state vector.

**Francois Chaubard**

Yep. And we have some thrust vector U that we control and we’re trying to get to some point P-star and V-star, which is V-star is typically zero. And so you have some platform that I want this drone to land on. So this is this control problem, right? And so let’s say this is like, and we’ll go through optimal.

**Ankit Gupta**

Optimal, yeah.

**Francois Chaubard**

Optimal control. So how would I actually solve this? So the first thing I need to know is my transition function. And so this is my state transition function, which is ST+1.

**Ankit Gupta**

Given the previous.

**Francois Chaubard**

Given ST and my action, which I control is UT. And so this is my state transition or dynamics function or a world model. This is a world model.

**Ankit Gupta**

This is a very fundamental for context, this equivalent to a transition function you would think about in RL in general.

**Francois Chaubard**

Exactly. And then what I’m trying to learn is something called a policy, which is like what UT should I emit given some ST. And so this is the ultimate question, what should I do? What action should I take given some state ST? And so the way that we’ll solve this and luckily we have a world model that is perfect and it’s called-

**Ankit Gupta**

It’s Newtonian physics.

**Francois Chaubard**

Newtonian physics. This is new and second law of motion, which is F equals MA. And so we know that the position PT plus one is going to equal PT plus delta TVT plus one half delta T squared. So everyone’s taking high school physics. And the same thing for the velocity, blah, blah, blah.

**Ankit Gupta**

Delta TA.

#### 09:20 — Control theory & the drone example

**Francois Chaubard**

And then my acceleration is sum of the forces, which is going to be my UT. I think I divide by the mass and G. And so that’s it. And now I have my transition function. Now, how do I get to a policy? And I’m going to apply something called model predictive control or real-time model predictive control, which is the way that SpaceX lands the rocket on some platform in the ocean. And what you’re going to do is you’re going to set up your loss function. You’re going to minimize sum over all T. You have UT to infinity, and I’m going to minimize my P-star minus PT plus V-star minus VT. And usually you add this little lambda UT, which is how much energy you’re exerting. And you can’t have infinite thrust. So you typically will have to say UTU max thrust that can be achieved. And so this is easily solvable with comics optimization. And so this is convex, this is convex, this is convex. The sum of convex functions is convex. This is a convex constraint. And so DCP, discipline convex programming means that I can put this into a CVX pie and it will just give me out my policy, which will be the solution will be the optimal UT plus one all the way to infinity.

**Ankit Gupta**

So we can solve this in closed form basically.

**Francois Chaubard**

Exactly.

**Ankit Gupta**

Because we have this world model of Newtonian physics, we can say at every step exactly how this drone should fly so that it lands on the appropriate thing under a set of constraints like max thrust available.

**Francois Chaubard**

Exactly. You’ll run your log barrier or enter a point, whatever to some solver on this and it will give me my optimal... Then this will be literally the optimal path that this thing can take to get to this state. And that will minimize and I can increase this if I want it to do the least energy path and I make that zero if I want it to be the fastest. And so that’s typically the way that you would do what I’ll call deterministic differentiable control. And why differentiable? Because I can form the Lagrangian by taking this minus this constraint and take the grading of it. And I can do mono-robins.

**Ankit Gupta**

You use the fact that it’s differentiable to do the optimization.

**Francois Chaubard**

Exactly. If this is non-differentiable, you cannot do convex optimization and you cannot do SGD. Even if it’s non-convex, you could still solve and get a pretty good solution as we do in deep learning. But if it’s non-differentiable, you can and can’t. There’s nothing you can do.

**Ankit Gupta**

So yeah, let’s have an example then of how you could make this non-differentiable. What’s a scenario I guess even in this drone scenario where it now becomes non-differentiable?

**Francois Chaubard**

Yeah. So I’ll put this adversary named Ankit. And your job is to, you have another drone, let’s say. Ankit’s drone is to try to hit me and stop me from getting there.

**Ankit Gupta**

Now from the position of your drone, you don’t know what actions I’m going to take.

**Francois Chaubard**

Right. And so now let’s just call this the, this would be now we’re definitely not deterministic, we’re stochastic. And stochastic and non-differentiable. And in this case, my state transition, what is ST plus one? It’s going to be say I’m in now, my thrust and what Ankit’s going to do.

**Ankit Gupta**

Right. And it was all differentiable until this new variable.

**Francois Chaubard**

Yeah. And I can’t backprop through your brain to say what you’re going to do with your little drone controller, right? It’s completely non-differentiable now. And I’m resorting and I have to resort to this awful area called reinforcement learning, which is just super brutal and it’s sprawling and there’s so many different things. And you’ll hear things like when you study initial reinforcement learning called value iteration or policy iteration. And there’s DQN or deep Q learning or just Q learning. There’s actor critic. There’s all this mega stuff.

**Ankit Gupta**

And all of this stuff ultimately comes down to ways to estimate, to model this non-differentiable stochastic process.

**Francois Chaubard**

Exactly. Yeah. And so that’s basically the main thing is you’re going to start talking about this as a model where I’m going to introduce this SI to say that this is going to be some model that’s going to take in these things and then output this and that we’re going to train it over many, many instantiations of this. And that’s so it’d get a better and better world model. And then I need to train some policy, AT/ST. And then typically you also need a value function. And that is the value of some state. And to discern between the value of different states. And in this case, I don’t know what a valid state is, but let’s just say I was doing the SpaceX with launching rockets.

#### 14:30 — When physics breaks down

**Ankit Gupta**

Landing the rocket.

**Francois Chaubard**

And landing rockets in Florida. Let’s just say that there’s different... If I have my launchpad here and I have a whole bunch of houses here, let’s just say, the path going from here to here, I may think that doing this and then coming across here and burning all these houses alive may be not highly valued. So I might say as an example, they typically call this some kind of a cone here, and I might say it’s low value to be here and it’s very high value to be in this cone or something as an example.

**Ankit Gupta**

Yes, right. But in a sense, a value gives you some expectation of future rewards, like the sum of future rewards you’re getting. And so if you’re in a bad space, you would set the value to zero or negative infinity or something like that.

**Francois Chaubard**

Yeah, so we should introduce RT as well. And so typically if you’re playing go or chess, winning the game, you can say winning the game is plus one minus one for losing, draw zero, that’s what’s done in AlphaGo. In chess, we have these heuristics, like a pawn is worth one point, a rook is worth five, et cetera, et cetera. Et cetera. So you can already have reward is the difference in board state. And then this, yes, will be the sum of my discount. Should just do T of RT given. And it’s important also to use this nomenclature, V pi. And the reason why that’s important is because what’s actually happening here is this is the discounted reward following policy pi.

**Ankit Gupta**

Correct.

**Francois Chaubard**

And that means that when I’m in this state, I will take this action and then I’ll end up in this to SC plus one and then I’ll take this action and taking it greedy. And so that’s the value with respect to pi.

**Ankit Gupta**

And so ultimately what it comes down to is we are trying to still find a new policy pi. And along the way we will use machine learning models in various capacities, this is standard RL, to estimate the value function given the rewards we’re receiving. And then where world models come in is a way of incorporating all of those into some sort of joint modeling of the state and action distribution so that we can make more intelligent policies off of it.

**Francois Chaubard**

Right. And so your standard setup for this is what I’m always trying to get to at the end of the day is some joint distribution, which would be ST plus one given where I’m at now. And then this factorizes with chain rule simply to my pi, my policy, AT given ST, and my world model. And I’ll give this, this is usually represented with theta. And this is my world model, which would be ST plus one given ST and AT. And these are typically learned separately. And you can imagine, in fact, actually you can actually learn this. This a video generation model and I have the frame ST, and I predict the next frame ST plus one. And we’ll get into this.

**Ankit Gupta**

Yeah. For those of us who saw our diffusion model series, often people these days use video diffusion for exactly this.

#### 17:45 — Chess, Go & the action space problem

**Francois Chaubard**

Yeah. And then what you can do, and this is the in vogue thing to do since Danijar and the Dreamer paper series from V1 to V4 is do action conditioning later. Similar to Clip where we will inject this input head or input tail to come into the model to influence and enable the world model to have embodiment. What does that mean? It means that not only can I predict as a plant or tree growing on the side of the building, I can see the world passing by, but I can actually influence it and I can change the world and I can learn that with AT. And it’s far fewer samples to do this post action conditioning if I already have a really good ST to ST plus one world model.

**Ankit Gupta**

And so here you’re saying what’s also in vogue now is jointly training these versus separately training them.

**Francois Chaubard**

Exactly. So that is called the world action model where some of the issues here is one, there’s all these training dynamics if these things are disparate, training on different sets and things like that. The other issue is plainly obvious what I have to do to actually do test time planning is I’ll have to sample with model one, invoke theta, and then pass that sampled action into here and then roll it out to ST+1. And it’s very expensive and it’s a very not real time. Two major issues and why can’t we just scale up AlphaGo to solve all the problems is because of this property. If I have one invocation to the model and it gives me both, here’s the action I should take and here’s the ST plus one, that’ll end up much, much cheaper and much, much faster.

**Ankit Gupta**

Okay. So I think that’s a really good segue. I think why don’t we now motivate everything we just described through a series of increasingly complex environments? So I’ll contend that I think the right set of environments for us to consider is chess followed by go, followed by self-driving, followed by robotics.

**Francois Chaubard**

All right, so let’s go through a couple examples of problems that we want to apply reinforcement learning to. So chess is a pretty easy one. There’s an 8x8 grid. And so typically when you approach any RL problem, you’re going to look at star. And so the size of the state, the number of states I can be in. So if I have these eight here and these eight, so this would be 8, 16, 32. So it’d be 32 to the 64.

**Ankit Gupta**

Yes, quite large.

**Francois Chaubard**

Quite large. Then my transition function is stochastic and non-differentiable because you can-

**Ankit Gupta**

You don’t know what the other player’s going to do.

**Francois Chaubard**

I don’t know what you’re going to do. So if I’m playing chess.com at my house, I move and then something happens and it comes back and then now you moved and the board has changed. So I can’t really differentiate through what the other player is doing. The car line in my action space is actually quite small. Even though there’s 32 pieces and all that stuff, there’s only eight possible moves in expectation that are legit moves. So any-

**Ankit Gupta**

In any given state, there’s only eight-ish moves you could do.

**Francois Chaubard**

Yeah. Let’s just say in the beginning, I can move all my pawns, I can move my horses. So that’s 10. That’s not that much. So this is extremely small. And then my reward, we can use the heuristic-based approach or we can just say plus one, zero, or minus one if I lose, plus one if I win. And so this is very tractable.

**Ankit Gupta**

You say it’s tractable even though there’s a really big state space here.

**Francois Chaubard**

Yeah.

**Ankit Gupta**

But why don’t we talk about that for just a second. I think this is a really important point. I think when you say it’s tractable, you’re specifically referring to the action space being small because it affects the combinatorial expansion here. Should we talk about that for just a second?

**Francois Chaubard**

Yeah.

**Ankit Gupta**

Or maybe we can add go and then contrast the two.

**Francois Chaubard**

Yeah. So why don’t we do that? Because I want to get to the AlphaGo, the way that they solve this. And you’re right. So if I were to do this naively and I just took my ST plus one and I want to do look aheads, what I would do is I would take all of the actions I can take. So there’s eight. So I would do action one, action two, action eight. And then each one of these, I need to expand it for all possible states. And so now I need to do carnality S, which we just said is this huge freaking number. And so I have to do that eight times and I have to do it again. I have to do it again. So just looking forward, one move is quite intractable.

**Ankit Gupta**

Although at the same time, everyone starts at the same starting position. And while it is a really large space, there isn’t an infinity number of potential... There’s actually a really small number of game boards, even four moves into the game as opposed to a game where you could start in any permutation, for example, of initial game state and what a few states down look like.

**Francois Chaubard**

So this is definitely overdone because it’s much, much less than this in practice. But just naively looking at what possible game states could be as a rough math here. But this is roughly the idea. And then each one of these leaves, I need to invoke my value function, which is the value of that state T plus one. And so I have to do that all many times. And we’ll get this with AlphaGo, but this ends up being estimating the leaf node because at the end of the day, my policy AT/ST, I want to pick, I want the ARG max of the value of the following-

**Ankit Gupta**

The ARG max action, I guess it would be an A here.

**Francois Chaubard**

Yeah, A, exactly. Yeah. The ARG max over A of the value of the N state, ST plus N, let’s say. That’s the main goal here. And so for me to do that, I need to roll all this out, estimate the value, and then pick the best one. And so this quickly grows. However, and we’ll see this with AlphaGo, which actually has an even bigger state space. So I think it’s 19 by 19. Correct me if I’m wrong.

**Ankit Gupta**

I think it’s about right now.

**Francois Chaubard**

So yeah, there’s 19 by 19 grid. In each one, it can be black, white, or nothing there. So I have three. So let’s do our star again. So the cardinality of the state I think is going to be S3 itinerary thing here.

#### 24:10 — Why AlphaGo can’t scale

**Ankit Gupta**

19 squared, I guess.

**Francois Chaubard**

19 squared. I think it’s 361.

**Ankit Gupta**

381? Yeah, 361.

**Francois Chaubard**

1. My transition, same issue. I don’t know. My action space is going to be 361, let’s say.

**Ankit Gupta**

So it’s a good amount bigger than chess.

**Francois Chaubard**

Much bigger.

**Ankit Gupta**

But it’s still not enormous.

**Francois Chaubard**

Yeah.

**Ankit Gupta**

As we’ll see in a second.

**Francois Chaubard**

Yeah. And so basically what they do, they call this Z, which is kind of annoying, but let’s call it R. And it’s the terminal when they won the game. And they basically, you have your trajectory, which is S0, A0, R0, then all the way to the end of the game, SN, AN, RN. And if you won, then all the moves that... If black won, all the moves that black did get plus, all the moves that white did were minus one. And that’s how they create their rollouts.

**Ankit Gupta**

Rollout refers to a taking end steps of play of all players one after another, of moves under a specific policy at the particular instantiation of it.

**Francois Chaubard**

Right, right. So let’s probably under this policy P, theta T. And we’re going to overload T, but this is that instantiation.

**Ankit Gupta**

At that model.

**Francois Chaubard**

We froze that model and we play I think it’s like 70 games and we treat all of those and we’re going to sub-sample a bunch of these state action results, state action results to update our policy in our world model, our transition model. And what it’s actually doing is we take in an ST, we give it to some theta, and then it wants to output the probability of ST plus one being played, which is our transition function and the value of the current state, the ST.

**Ankit Gupta**

And how do we get the value.

**Francois Chaubard**

And so the value of the current state, well, both of them are coming out of the model, but basically the loss function, L theta is going to equal, and it’s going to be eerily close to this control problem one, is we have some V theta minus this Z, which we’ll just call it R here squared. And then plus... Actually, sorry, it’s minus this pi, which I’ll explain in a second log P theta. And I think everyone includes this, but they include it in the paper, so I’ll include it there as well, which is the weight decay. So this is basically what our loss function is. Then we’ll play a bunch of these games. Let’s try to be a little bit organized here. And so this is our setup, this is architecture. And now once we train this thing, we do an insanely expensive task of test time planning. And so this trend in RL is just called test time planning.

**Ankit Gupta**

And the specific algorithm they use here for this is Monte Carlo tree search.

**Francois Chaubard**

It’s called MCTS. And so this is one of the possible things that you could do. It ends up working extremely well if you have small action spaces.

**Ankit Gupta**

Yeah. So let’s just very intuitively talk about what MCTS does.

**Francois Chaubard**

Sure.

**Ankit Gupta**

A lot of people have heard about Monte Carlo tree search because AlphaGo was such a big moment, but how exactly does that map into our star in value function and policy?

#### 28:00 — Monte Carlo tree search explained

**Francois Chaubard**

Yep. So I’ll take this ST. This will give me 361 numbers that sum to one. And so I’ll have some probability of where these things are going to go of where my opponent will play here.

**Ankit Gupta**

So these are the sets of actions.

**Francois Chaubard**

Yeah. So I’m here so that I have all my ST plus ones. I’ll have 361 of these things. And then-

**Ankit Gupta**

And to be clear, this is action one, action two all the way to action 361.

**Francois Chaubard**

Yeah. Exactly. Yeah. And we have to estimate the value of each one of these. And so then we have to invoke the model all 361 times to give me values for each one of these things. And then I’ll select it based on the UCB, the upper confidence bound, which is this equation that is roughly something like balancing my value function of ST plus one, which in the literature it’d be called a Q value because it’s actually the difference between a value function and a Q value is just that I have the action as well. So it’d be ST, then AT. So we’ll just call that Q value, which is my exploitation term. And then my exploration term will be something like it’s this funky square root of N. So it’s the ARG max of A of my Q. And then I have this, which is the probability of this move being played, which we have from here of S, let’s just call it ST plus one. And then I have this term, which is this sum over NSB divided by NSA.

**Ankit Gupta**

What the \[inaudible 00:29:59\] on this term.

**Francois Chaubard**

So these ends is the visit count during my MCTS process. So this whole tree I’m going to...

**Ankit Gupta**

So this tree could get really big. It’s 361 per thing.

**Francois Chaubard**

And it’s depth of 30.

**Ankit Gupta**

So you can’t visit every single leaf node.

**Francois Chaubard**

Exactly. And so you want to keep track of which state did you end up in and what action did you take when you were in that state? And you want to make sure that you have good exploration, right? And so the way you ensure that you have good exploration is you want to not just be greedy and always pick the highest value one because that could be very myopic. And so what you’ll do is during this MCTS process, you’ll start this dictionary, which will be all zeros of the visit count of being in this state and taking this action. And then once you go through your first rollout, you’ll go here, all these things will be added to zero, you’ll have some probability. We’re going to bias it towards the higher probability of places to go and then we’ll expand those trees and then we will update the counts that we visited this and that will basically reduce the amount of probability that we’re going to select it again because this will reduce my exploration term. And if it’s highly valued, then we’re going to increase the Q on this because this is the expected value of going down this path.

**Ankit Gupta**

So the gist of it is fundamentally you want to take the optimal-ish path, but have enough exploration in this really expensive step you’re doing here so that you are making sure you’re getting a decent chunk of the other potential leaf nodes you could traverse to in these 30-step rollouts.

**Francois Chaubard**

And so I’m going to do this MCTS simulation 800 times here. And then for all 800, I have to go through this whole process and I have to invoke the model at least 30 times to get through all here. And so that’s 27,000-

**Ankit Gupta**

800 times 30 invocations.

**Francois Chaubard**

So 24,000 invocations of the model to develop this tree. And then once I have it-

**Ankit Gupta**

That’s per step.

**Francois Chaubard**

Per step. Just do one action into the game. A lot of people don’t understand that this is like you don’t store this MCTS tree, you throw it away after you make the move. But it’s very expensive to develop this MCTS tree. And once you have it, the probabilities of traversal are actually extremely useful for training. And then you end up biasing it and you train it with the MCTS tree, which is a little bit seems like circular motion or something like that, but you end up treating that as the pie that you’ll train in your loss function. So we have the R of did we win or lose? We have the pi of what was the end result of this whole expensive process. And then at test time we are going to do these 24,000 steps every single move to pick the ARG max that satisfies both exploration and exploitation.

**Ankit Gupta**

In this case, this still feels somewhat tractable though because the action space is small enough where this kind of works.

**Francois Chaubard**

Exactly.

**Ankit Gupta**

But now let’s say hypothetically, maybe we can draw an imaginary game of go where it’s like... Let’s say this game of go was like a thousand by a thousand. And so now you have A equals more or less a million. And now this tree we’re drawing here that has to take here, this has cardinal or width, I guess, one million and there’s S0 through S one million. And the number of steps you would have to take here presumably would have to be way more than 800 in order to get any reasonable kind of sampling of this. And so you’re probably multiplying the test time cost of doing a rollout or of doing a next step prediction astronomically if the game was even let’s say this is only a 100X bigger than the current game or not even 50X bigger than the current game.

#### 34:00 — Self-Driving: state space is infinite

**Francois Chaubard**

Everyone was very excited about AlphaGo and at the time, and what was this, 2017, 2016, everyone’s very excited about this. And the important thing to pick up is that we did 800 MCTS simulations to cover 361 possible actions on average. So that gives us about two samples roughly on an expectation for every single action.

**Ankit Gupta**

So here you need two million of them for a similar depth.

**Francois Chaubard**

Two million for a similar depth. And then that’s still to do a depth of 30, I would still have to do this times 30. This had be 60 million invocations of the model. So that better be a small model, right? That’s a lot. So yeah.

**Ankit Gupta**

That’s to do a single action to be clear.

**Francois Chaubard**

Yeah, so exactly to do one action. So just imagine, so why AlphaGo doesn’t scale? To me there’s one, the cardinality of the action space must be extremely small. If it’s big, sad. Two, I need a perfect deterministic environment, right? This doesn’t change. The rules of this game don’t change, but the rules of the stock market change all the time. The rules to venture change all the time. The real world changes quite often. So homo skedastic and real time. If you saw the movie, the documentary was such an amazing documentary. I’d highly recommend it to anyone to watch it.

**Ankit Gupta**

It’s really good.

**Francois Chaubard**

The guy’s sitting there for 60 seconds, maybe five minutes waiting for the computer to decide. And it’s kind of like imagine that we were driving a car and you took 60 seconds to turn the steering wheel. Everyone’s dead. The whole car is dead. And so now let’s talk about robotics and self-driving car and why that approach can’t scale.

**Ankit Gupta**

Yeah, I think it’s a really good contrast here because intuitively, I think in thinking through this exact star layout, it actually really changed how I think about the problem space of both of these two. So let’s take self-driving car as an example. This is one many people have started to experience for the first time because we have some self-driving cars that actually work. You have Waymo and Tesla FSD and whatnot. They seem like they kind of work. So let’s maybe apply your same star framing here. I would contend that the state space of self-driving car is enormous and it’s actually not intuitive to me whether it’s more or less large than this one. I mean, in a sense, the chess and AlphaGo state space is already more than the number of atoms in the universe or something to that effect. But just to emphasize that here, you are considering surroundings, vehicle state, camera details and so \[inaudible 00:37:25\].

**Francois Chaubard**

Weather.

**Ankit Gupta**

Weather. I guess the point is-

**Francois Chaubard**

Road conditions.

**Ankit Gupta**

It’s massive. This is massive.

**Francois Chaubard**

For all intents and purpose, it’s infinite.

**Ankit Gupta**

Yeah. For all intents and purpose, it is infinite. Correct. Yeah.

**Francois Chaubard**

And so is the space of pixels. What can I put in an image? I can take an image of anything.

**Ankit Gupta**

Yes, true. True.

**Francois Chaubard**

And so we’re able to handle it. And same thing here where we compress from the board state. We don’t represent the board state. We compress it with a comnet. And so they have some deep comnet that actually takes this state and converts it into a latent. And that latent compression is sufficient to do pattern matching, do some type of symmetric equivariance kind of things. And same thing with this. And even better with JEPA, which we can talk about at the end there, which is basically taking some type of state space and doing all of our optimization in the latent space, which Stable Diffusion did, that worked extremely well, which reduces our state space dramatically because I’m in some latent high-dimensional space.

**Ankit Gupta**

So the key thing there is that despite this state space being effectively infinite, we’ve actually gotten really good at compressing this. And we’ll talk more about some of the tricks for how we actually do this in practice here, but the TLDR is where there’s 10 years of deep learning work that basically makes us extremely good at compressing that very fast.

**Francois Chaubard**

Exactly right. Exactly.

**Ankit Gupta**

T seems to have a similar problem as before. In fact, maybe even more extreme. There’s infinity other variables around you of things going on.

**Francois Chaubard**

Right. In some ways you’d think that... This is physics. Newton’s laws of motion should apply. If I turn the steering wheel like this or I hit the gas, I should be able to really easily model this. But what is non-differentiable is that if I’m going into a circle, the biggest issue that we faced when I was doing self-driving car is you are imposing your will onto maybe driving in India, I think is one of the \[inaudible 00:39:22\].

**Ankit Gupta**

Yeah. Exactly, yeah.

**Francois Chaubard**

You’re imposing your will onto the environment and people just kind of adapt naturally. If you were doing Newton’s motion, you were going to collide. And so that the optimal policy, if you were being strict Newtonians here would be like, don’t move because anything you do, you’re going to crash. But it’s not true. Then we wouldn’t function. Cars wouldn’t go down the road. And so you have to include other people in the environment and understand the embodiment of how your action will change other people’s actions.

**Speaker 3**

YC’s next batch is now taking applications. Got a startup in you? Apply at ycombinator.com/apply. It’s never too early and filling out the app will level up your idea. Okay, back to the video.

**Ankit Gupta**

Now let’s talk about the action space. One way to look at the action space is that it seems relatively small. It seems like, well, you turn the steering wheel left to right, you hit the brake, you hit the gas. It doesn’t seem that big, but how big is it actually? How do we actually represent these action spaces when it comes to a realistic self-driving car scenario?

**Francois Chaubard**

Yeah, I don’t know how they do this nowadays. They’re doing a whole bunch of bird’s eye view, different things like that.

#### 40:30 — Model-Free vs. Model-Based RL

**Ankit Gupta**

Yeah. Let’s consider even just a very simplified case.

**Francois Chaubard**

But what do you have? You have a steering wheel that you can turn left, right. You have a brake pad and you have the gas. And so-

**Ankit Gupta**

This thing is 365 degrees. So it’s like a one to 365, let’s say, or zero to 365.

**Francois Chaubard**

Yep., And let’s just say you break this up into 10 different severities.

**Ankit Gupta**

Even with just this oversimplified model, your action space cardinality is 365,000. So that’s 100X bigger than AlphaGo. In fact, it’s about the size of the example.

**Francois Chaubard**

Yeah, right.

**Ankit Gupta**

In fact, a decent amount smaller than the size we said, which is brake and CPS.

**Francois Chaubard**

Exactly, yeah. And so yeah. So 36,000 action space is very large. And then even worse, unless you’re Tesla, we have a bunch of video of people driving cars. We don’t have video of dash cams like that. You actually don’t have, again, only Tesla has this, of the action as well. And so the things that you have access to, your trajectories are just like ST, ST plus one, ST plus two.

**Ankit Gupta**

So you’re saying there’s a decent number of these that’s from dash cam footage on YouTube or something, but not really that many either relative to complexity.

**Francois Chaubard**

And so if you wanted to do a self-driving car and you didn’t want to go spend a million dollars, trillion dollars on going collecting all this data, then you want to leverage this data somehow. And this is going to be really applicable for robotics because we have a lot of videos of people doing things, especially with egocentric. We have those videos, but what we don’t have is-

**Ankit Gupta**

The actions they take.

**Francois Chaubard**

Yeah.

**Ankit Gupta**

So this is a sequence of what you’re showing here.

**Francois Chaubard**

Unless you’re Tesla.

**Ankit Gupta**

Unless you’re Tesla.

**Francois Chaubard**

And Tesla has this. So this is a huge competitive moat of what do people do in that state? And then so you can behavior clone to go from here to here, from here to here, go here to here, et cetera. But even then, it’s still very, very difficult. It’s not sufficient. People think that, okay, I have this. We have a self-driving car, right? I mean, the amount of work that they’re doing at FSD is incredible and it’s not generally available. It’s not Waymo level yet.

**Ankit Gupta**

Would this be a good moment to briefly talk about model-free versus model-based RL?

**Francois Chaubard**

Yeah.

**Ankit Gupta**

I think that’s an important distinction that’s going to be relevant when you talk about more world models.

**Francois Chaubard**

Yeah, so this is a perfect point. So model-free just means that my policy pi of AT given ST, I have no world model involved. It’s literally doing what I said. I grab a bunch of these and I go from S to A, S to A, S to A.

**Ankit Gupta**

Yeah. Just predict the next day.

**Francois Chaubard**

That’s it. And this is logical VLA. This is giving us pretty good results. It’s behavior cloning. It’s all the stuff that it’s not getting us to Rosey the Robot just yet but-

**Ankit Gupta**

In many ways, it’s the closest thing that just looks like the next token prediction from LLMs that seems to scale pretty well with natural language.

**Francois Chaubard**

Exactly.

**Ankit Gupta**

I mean, it’s not exactly the same thing because there’s no action exactly, but picking a token is not exactly the same thing, but it’s very analogous to that basic thing \[inaudible 00:43:33\].

**Francois Chaubard**

Yeah. I basically take away the tokenizer head and I give it an action space and I collect a bunch of tele-ops data like this as the self-driving car does in Tesla. And I just take in the state, which is some image or maybe sequence of images and then I’ll output some action and that’s it. And this is, let’s say, model-free because I don’t have a model for the environment. And then now if I do model-based RL, I have not just some pi, but I have also SI as well here. And so by including this, I can have a much stronger policy, but it would take a lot more time to perform inference because I have to do this full test time planning.

#### 44:00 — Why robotics is the hardest case

**Ankit Gupta**

Just to remind us, that SI is referring to this specific transition function.

**Francois Chaubard**

Exactly.

**Ankit Gupta**

It’s referring to this. You’re saying this is specifically referring to a function of ST plus one given ST and action T.

**Francois Chaubard**

Yes, exactly right.

**Ankit Gupta**

So it’s like your ability to predict the next state you’ll be in is the crux of it. As opposed to just directly predicting the actions.

**Francois Chaubard**

Yeah. And the main thing that I believe is that this is required for AGI. This is what the human brain has been doing.

**Ankit Gupta**

At least in the way the human brain does it.

**Francois Chaubard**

Yeah. And let me go further in saying that if you look at the billions of years of evolution, basically there’s this thing called 10 million years ago called the great cortical expansion, which you see the size of a brain just explode, get bigger, bigger, bigger exponentially up until us and it basically stops. And if the entire point of the neocortex is world modeling, what happened is we started from VLAs. This would be like ants-

**Ankit Gupta**

And fish or whatever. Yeah.

**Francois Chaubard**

And fish. Yeah, right. Just very lizard brain, whatever you want to call it. And then we develop this neocortex to go from our motor cortex to actually simulate what’s going to happen. And that makes us just so much smarter. And then once we get those samples, we can compress it when we sleep or otherwise with this hippocampal, short wave ripple, whatever you want to call it. And then that helps us develop a better policy. And that marriage between the two not only helps us train on hallucinated examples, but it also allows us to test time plan.

**Ankit Gupta**

I guess the extreme case then of self-driving car is general robotics.

**Francois Chaubard**

Yes.

**Ankit Gupta**

Right. So if you’re a humanoid company like figure or pi or whatever, again, same STAR setup. I guess the gist of it is that A is now even bigger. I guess a very simple robot would be, how would you parameterize the action space? Let’s take a very basic one.

**Francois Chaubard**

If I take my six-axis arm as your standard here that we’re actually working on right now in Stanford Robotic Center, you have two degrees of freedom, two degrees of freedom, two degrees of freedom. And then you have another two for the end effector. And so the end effector-

**Ankit Gupta**

That’s a simple end effector, not even like a fancy one.

**Francois Chaubard**

Yeah. It’s literally a one-axis. You can rotate, but you have the one-axis Yumi style thing. So this is eight. So you have 16 degrees of freedom. And let’s just say that you do the 365 divided 10 or whatever kind of thing. I mean-

**Ankit Gupta**

It’s like 10 to the 16.

**Francois Chaubard**

It’s insane.

**Ankit Gupta**

It’s something like that.

**Francois Chaubard**

It’s an insane number. And so much bigger than self-driving car. And even worse, getting tele-ops data is extremely painful and expensive. It’s not just like, “Oh, we’ll just get some people in the Philippines, we’ll give them some things or whatever.” It totally, totally doesn’t work.

**Ankit Gupta**

And nor is there yet something like Tesla’s fleet where there are cars deployed that people are just using and they’re not even necessarily realizing that every time they turn the steering wheel, they’re providing this dataset for Tesla to train on.

**Francois Chaubard**

And then even worse, you have this what’s called cross embodiment gap. And so if I were to train this policy on Tesla Model X and I were to put it on a Tesla Model 3, it wouldn’t work. It totally wouldn’t work. So much of this, the way that if I were to brake on a Model 3 versus a Model X, the Model X, it weighs more. It has different dynamics, aerodynamics and things like that. And so what’s actually going to happen is very different. The degradation you have across embodiments is very, very, very strong.

**Ankit Gupta**

And clearly Tesla’s figured various ways to get around that. I mean, they have these that roll out, but actually even with Tesla as a new FSD today, they don’t roll out in all the cars at the same time probably for more or less that reason. And in this case, it’s even harder now. I mean, you have bigger differences between embodiments than a Model 3 versus Y, and you have way bigger action spaces you have to sell a model.

#### 48:20 — World models that actually work

**Francois Chaubard**

Yeah. Lane McIntosh, I played hockey with at Stanford who now runs Tesla FSD. I can ask him, but I would bet money that they shard the data per model per car type.

**Ankit Gupta**

Yeah, wouldn’t be surprised.

**Francois Chaubard**

Because that’s what I would do. There’s no way that I would trust data that was collected on a Model X on a Model 3. No way I would trust it.

**Ankit Gupta**

Okay. So now that we understand the basic setup here and why the action space problem is so big, why don’t we talk a little bit about how world models actually fit into this? Maybe first, I guess what didn’t work about the naive world models and how do we fix those? And then let’s talk about some of the newest world modeling techniques.

**Francois Chaubard**

Cool. So in robotics in particular, it’s very hard to get this kind of trajectories that you want, that you need to train for your VLAs. And people spend up with a whole bunch of tele-ops data. It’s very expensive, very expensive. Ideally, what we would do is take data like this from someone who just puts a camera on them and just making sushi. I want to make a sushi robot. How do I do it? Give it to all the sushi chefs, don’t put anything in their hands and just have them start cutting up sushi and making sushi.

**Ankit Gupta**

And ideally, we would train it in that way you were describing of somehow we would train a model just on these two and then later add this.

**Francois Chaubard**

Yes.

**Ankit Gupta**

Afterwards.

**Francois Chaubard**

And so the first real person that went after this was Jürgen Schmidhuber. So he doesn’t yell at us, we have to make sure we cite him. But he has this really cool paper called World Models, very aptly named. And it’s basically he took these OpenAI gym classic games, car racing and I think Doom as well. And then just trained a model at that time was an RNN. He had some funky zero order stuff in there or whatever. But basically the key premise was I can take an environment, I can extract a whole bunch of this type of data off of it. I think he actually does actually this data, but we’ll get into Dreamer where he does it in this way. And then trains a policy on only the synthetic data, the imaginated rollouts. And it actually performs well in the environment. This is the first time in my understanding that that actually happened and it actually works really well. And then-

**Ankit Gupta**

So the key thing there is you can basically use this if you have some predictive model of this in that case and eventually of this, you can use that as basically a synthetic training set to train your policy model and then basically fine-tune it on real data later.

**Francois Chaubard**

Exactly. And which is just a really powerful idea, especially since in robotics, the limiting step is access to large amounts of state action data. And so now the Dreamer series, so basically this publishes in May of 2018. Danijar Hafner publishes Dreamer 1 I think in November of 2018. And then now he’s been on this rampage for the last seven years publishing these papers. And Dreamer V4 I think is the capstone of it where he basically does the same thing and he focuses on Minecraft and he trains a world model on this type of data and then injects action conditioning on a very small amount of data to get to this type of world model that has the action conditioning as well. And then samples a lot from it and then trains a policy on those synthetic imaginated rollouts. And the policy is so good that it’s the first paper to mine diamonds in Minecraft. I’m not a big Minecraft player, but apparently that’s extremely difficult. That’s next level difficulty and it did it all on synthetic data, which is kind of crazy.

**Ankit Gupta**

And the key unlock there, yeah, you use synthetic data specifically on a model trained on just this sort of state transition type of thing.

**Francois Chaubard**

Yes.

**Ankit Gupta**

And this ends up being very convenient because it turns out we as a society have a lot of this.

**Francois Chaubard**

Exactly. Yeah, all of YouTube, right? He does do a very small amount of data to enable the action conditioning and that allows you to do this full simulated rollout. But yeah, it’s true. So we have YouTube, we have Flickr, we have all these datasets online of people doing things. We’d like to use it and no one has really gotten that to work. And then now that with these video generation models, we can take that data, create a world model out of it, add action conditioning, post-train it with action conditioning for some new task that we want it to do, chopping down wood or making sushi or folding my bed or whatever it is, only a few amount of examples. And then we can train a policy in this neural simulation.

**Ankit Gupta**

And we put out a video about diffusion models very recently and flow matching. I imagine that now ties very closely to this. Ultimately, the current state-of-the-art best way to do this on basically infinity data that we have available and can keep generating is using state-of-the-art video dfusion/flow matching models.

**Francois Chaubard**

Exactly. Yeah. So if you have your CDANCE or your SORA or-

**Ankit Gupta**

ONE.

**Francois Chaubard**

Exactly. All those models, basically the idea is now we have them and they’re already trained and they’re great. Let’s do a small amount of action conditioning on them to get to this world model and then we can sample from it a bunch and then train. And this is exactly what Wayve did with GAIA. And GAIA, I think they’ve raised $1.5 billion to basically run with this idea for self-driving car. I think a bunch of companies, Nvidia, this paper here is basically talking about doing exactly the same, this Dream 0 for robotics.

#### 54:10 — JEPA & latent space tricks

**Ankit Gupta**

What I thought was really cool about this paper is that they do exactly this process where they have this joint model of state transitions and actions. They train it by first instantiating it with the open source one video diffusion model. And then it only takes them about 500 hours of tele-op data, which is basically exactly this, to get it to be pretty good. And they have a lot of clever tricks that allowed it to be cross-embodiment and working on scene tasks with relatively small amounts of data. And it really is taking basically the exact concept, I believe, from the Dreamer paper and applying it specifically to these robot embodiments.

**Francois Chaubard**

Exactly.

**Ankit Gupta**

And it turns out it actually works actually better than I would’ve anticipated it working.

**Francois Chaubard**

Right. So yeah. So I think that this is basically the path, it was the path I believe is the path to get humans to be as good as we are genetically over the last 10, 20 million years of evolution. A bigger world model helps for training and for test time planning. And I think it’ll be the same thing as true for robotics.

**Ankit Gupta**

What’s also cool is there’s a bunch of applications of this to things outside of robotics too. I mean, there was a weather planning paper, for example. We were reading this Gencast paper, which I think applies a relatively similar concept in terms of how they model literally the world’s weather with something like this.

**Francois Chaubard**

Yeah, we have to talk about the world model for the world. Yeah. So basically they do this exact same thing where the key unlocks for this whole thing was getting diffusion to work in very high-dimensional state spaces like we talked about in the last lecture and then learning to use that to action condition in the way that he’s done. But they did this for the entire world with this exact same diffusion steps, which go from some... And they go back to two time steps, lag of order two, AR2 for the statisticians there. And then basically predict the next state of the world based on those things with this lingo and diffusion rollouts. My big assertion is that it was necessary for the human brain to develop world modeling. I actually just saw this paper that I wanted to make sure to call out because I though it was so great out of University of Washington where they say explicitly in the abstract, each cortical area estimates both latent sensory states and actions and the cortex as a whole predicts the consequences of those actions. That sounds like a world model to me.

**Ankit Gupta**

Yeah.

**Francois Chaubard**

Right?

**Ankit Gupta**

Yeah.

**Francois Chaubard**

And so-

**Ankit Gupta**

It’s actually describing exactly these two equations here.

**Francois Chaubard**

Right. Exactly, right.

**Ankit Gupta**

Where we’re estimating both the sensory latent states and actions. I mean, I guess it’s really the joint model that we showed earlier is what he’s describing here. It’s exactly this equation we’re showing now.

**Francois Chaubard**

Yeah. Exactly right. And so if it works in us, it should work in robotics. And I think that that takes us the rest of the distance.

**Ankit Gupta**

Why don’t we talk briefly about latent world models, especially the JEPA concept, because I think there’s been a number of papers that use JEPA as an element of their, I guess, architecture. Why don’t we just briefly introduce JEPA and how it fits into the current landscape of world modeling?

**Francois Chaubard**

Yeah. In classic RL, if you study Q learning, for example, you basically keep this matrix called the Q matrix and it’s going to be S by A. And so I have this S by-

**Ankit Gupta**

It’s states and actions.

**Francois Chaubard**

States and actions. And each one I need some amount of counts of being in this state action. And I take the average value of taking that action in this state and that’s my Q value there. And it’s a little bit more complicated in that. There’s Bellman equation, all this backup, all this stuff like that. So this scales horribly because as the cardinality of my state space gets bigger and my cardinal action space gets bigger, stuff, I don’t have enough, I become less and less sample efficient, right?

**Ankit Gupta**

In the case of robots or whatever, state is like, yeah, it’s this whole thing we described earlier. It’s absolutely massive because it has all of these elements in it. You couldn’t really enumerate a huge grid.

**Francois Chaubard**

And so the classic trick, I mean, since I took 229 with Androung in 2012 is you do this.

**Ankit Gupta**

Stick a neurolab, work on it.

**Francois Chaubard**

Exactly. And you basically are just going to compress that state into some lower dimensional state space. This actually predates deep learning. We were doing stuff like this. I think my first paper was basically doing something like this, basically turning a grid into a bunch of pyramids and the state was how much I’m in pyramid one or pyramid two or whatever. But anyway, the neural networking can just do this. And so basically the key idea in JEPA, if I have an image one and I have image two and I have image three, I can do my world modeling of ST plus one given ST and AT in pixel space and have, this is let’s say at time T, T plus one, T plus two, et cetera, et cetera. And I have to actually predict now the full image that’s extremely expensive from a computation standpoint and also from a sample efficiency standpoint. What I can do instead is put this through some comnet.

#### 59:00 — Open problems remaining

**Ankit Gupta**

Some encoder.

**Francois Chaubard**

Some encoder. And then I’ll get a latent for T and I’ll have a latent for T plus one and I’ll have a latent for ZT plus two. And then I’ll have from this, from ZT, I want to predict ZT plus one hat. And my goal is to make this and this and my loss function will be something very simple like I want to minimize this.

**Ankit Gupta**

Minimize that, yeah.

**Francois Chaubard**

That’s it. Now this doesn’t work. This collapse is hard. And so what happens is basically if you just predict zero, done.

**Ankit Gupta**

Yeah. It works. Yeah.

**Francois Chaubard**

Just output zero, which the model will learn to do. And I’m actually incorporating this into my current research right now. And so what you need to do is something called SIG Reg or this is one technique, VIC Reg is another. Where basically I add this another term that basically says over a large enough batch size, I want the distribution of ZT plus one to follow a Gaussian-

**Ankit Gupta**

It’s kind of like a normalized, like a batch norm type of trick. I mean not in the same case, yeah.

**Francois Chaubard**

And if it’s zero, it can’t be this because then this is non-zero. And so maybe I think that there’s probably this or something like that. But basically this prevents it from model collapse and it makes it do something good. And this is the most recent paper for the audience is LEWM, LE World Model, which is super, super great. However, to be completely frank, this is self-supervised learning, super great. It doesn’t work that well. If you were to not do these techniques and there’s a bunch of other techniques that you can do, it will actually outperform much better that are, let’s say for example, if I’m going to do an LLM. And you have Francois likes sushi, which is definitely true. And I tokenize this into a bunch of different tokens here and this is token ID 6, 19, 28, whatever, and I look up the encoding into this and that’s going to be E1, E2, E3, et cetera. What you can actually do is have the LLM output. The LLM will take in these things and will output the next token. And so it’d be like, let’s call it H. This would be the low jits coming out of it, two plus one. And what you can do is actually have this be close to ET plus one. And a lot of people are playing with this idea and getting rid of the cross-entropy loss entirely. And so if you were to do this, it actually is a proxy for the cross-entropy loss and there is no cross-entropy loss. And the cross-entropy head is actually very expensive. And so this is very cheap and this is literally just grabbing it. So people are playing around with this idea and basically as a cheaper proxy for the cross-entropy loss. So there’s lots of different ideas on basically taking this JEPA idea to not just pixels, but to LMs as well.

**Ankit Gupta**

Yeah, interesting. Yeah.

**Francois Chaubard**

So just to define what JEPA is, it’s joint embedding predictive architecture.

**Ankit Gupta**

I think one of the things I find cool about this JEPA idea is it feels like an idea we see over and over in deep learning. There’s a version of this idea that’s basically the staple diffusion idea. There’s a version of this idea that in my company training graph convolutional neural networks to design drugs we use to do latent variable generation, for example. And it’s an idea that comes back over and over and then has this various tricks that it actually takes to get it to work in practice.

**Francois Chaubard**

Yeah, yeah, yeah.

**Ankit Gupta**

Okay. Now we have a pretty good sense for how world models work. We have a pretty good sense for what the state of the art looks like. If we trust this paper, and it seems like these kind of work on robots too. I mean this paper’s only from the end of last year into this year, and it seems like they have various methods that allow you to train on relatively small amounts of data that’s tractable and pre-train on diffusion models. So are we good?

**Francois Chaubard**

We’re done.

**Ankit Gupta**

Does it all work?

**Francois Chaubard**

Yeah. 2026 will be the year of the robot. We’re going to have Rosey the Robot in your house. Yeah, no, I don’t think so.

**Ankit Gupta**

What are one or two, because there’s lots of open problems remaining, what are a few open problems maybe we can emphasize here that the community can go emphasize working on?

#### 01:04:30 — Does this pass the squint test?

**Francois Chaubard**

Yeah. So I think the first one is that PINNs doesn’t really work. What is PINNs? Physics-informed neural networks. So PINNs doesn’t really work. There’s physics-informed neural networks. And so basically if almost all of the self-driving car data looks like this, the car is driving down the road. And let’s just say, for example, I have a house here and I want to train the model on you not driving into the house. And so let’s say I put it into a state right here to drive into the house. What’s going to happen is because almost all the data looks like this driving down the road, this will just turn magically into a highway. And they’re just like, “Boo, just don’t worry. You crash it all.”

**Ankit Gupta**

Basically it needs a ton of data not to do that either from simulation for that to not happen.

**Francois Chaubard**

Yeah. In fact, I actually don’t even know if because of the data distribution, there’s no data here. There’s almost all the data here. And when you’re training a neural network, it has a tendency to collapse if you don’t keep the mini batch composition very even over the class space or whatever you want to call it. But you have to be very careful about your data mixing to make sure you get this right to solve this problem that no one really has. But even then, if you take just a simple thing like this, this is the kind of example, and I have some sine wave and I have these as my X. And I have these as my Y. So this is complete interpolation. I may mess this up, but Y, like this. We can’t get to machine precision. What is it? Minus 16 or whatever it is. The SGD will not get to effectively zero. So we’ll always have some residual. And for us to be a really good world model, to simulate body interactions, to simulate this, what’s going to happen when I do this? And let’s say that I’m trying to be LeBron James. I saw this one video of Steph Curry dribbling a basketball on a court and he just felt that there was a dead spot in the court because he’s so good and he knows exactly the physics of what’s going to happen. If I hit the ball with this force, the ball’s going to come back exactly this spot and it just didn’t. And he knew it wasn’t him, it was the court and he found a dead spot in the court. That’s how good the human brain is at world modeling. In my opinion, I think it’s an SGD issue. I think it’s probably an architecture issue. I think Sam Altman just came and just said that he thinks that there’s definitely an architecture that’s going to be more performant than the transformer. I think he’s right. I think the transformer doesn’t do compression in the time domain at all. It just keeps around everything. So anyway, so I think that getting higher fidelity in the world model is extremely important, one. I think two-

**Ankit Gupta**

Seems like test time probably is going to be a thing, like adaptation.

**Francois Chaubard**

Exactly. Test time planning, how quickly the human brain can... In sports and things like that, when you’re playing tennis, when you’re a tennis player, how quickly we can adapt to what a player is doing and things like that. We’re not going to sleep and retraining. We’re very quick to adapt to a new environment.

**Ankit Gupta**

It’s like the out of distribution prediction.

**Francois Chaubard**

Exactly.

**Ankit Gupta**

It’s really challenging.

**Francois Chaubard**

And one little data point we can quickly adapt to that new thing and change. I think there’s been a lot of papers on basically estimating the friction coefficients. And so those can change over time if you go to a human environment or not, for example, this friction might change and that’s important in control. And so you need to estimate that very quickly and adapt. And these models just don’t have a mechanism to do it.

#### 01:08:00 — Outro

**Ankit Gupta**

And then I guess there’s the practical speed elements of these. A lot of these are doing some sort of expensive planning step and we’re doing some sort of... We’re hacking around it with this pre-training process and synthetic data. But even so, to really get maximum performance right now, you’d want to do something that’s closer to the AlphaGo style rollout and that’s extremely slow.

**Francois Chaubard**

Right. The MCTS process can’t happen. The other thing that is pretty crazy about the way that the brain works is that everything is kind of running autonomously. And so you might be in the middle of saying sentence one and then be like, “Oh, actually no, something else.” And so what does happen there? It’s like type one and type two thinking are happening at the same time in some way. And so there’s definitely some really cool mix of these heterogeneous models and some are overriding others and taking control of the motor cortex and commanding the body to do a thing.

**Ankit Gupta**

Okay. But on the flip side now, we talked in the past video about the squint test and how we felt that auto-aggressive LLMs maybe don’t pass the squint test. Why don’t we reintroduce what the squint test was for a second? And then maybe let’s think about whether this passes the squint test despite all those limitations.

**Francois Chaubard**

Yeah. And the squint test for me I think is like, this comes from the Yann LeCun. We didn’t need flapping wings to achieve flight. And to that I say, “Well, we did need two wings.” And if I squint and I look at a bird and I squint and I look at a plane, I’m like, “Yeah.”

**Ankit Gupta**

It’s kind of similar.

**Francois Chaubard**

It looks right. Similarly, if I squint and I look at the human brain and I squint and I look at all these world models, we have this VLA, this action policy, and that they’re doing test time planning together and things like that. It’s getting really close. It’s much, much closer.

**Ankit Gupta**

It seems closer than an auto-aggressive LLM.

**Francois Chaubard**

100%.

**Ankit Gupta**

And this concept of a world model of implicitly predicting future states and actions feels intuitively like what our brain’s doing. And it seems like there’s some neuroscience evidence to support that.

**Francois Chaubard**

Yeah. I mean, I’m getting to the conclusion that I think that the brain is the optimizer, not the model and that the brain emits, has models that it invokes, but the brain is somehow also the optimizer itself. And so in that way it doesn’t pass the squint because something magical is happening when you’re sleeping. There’s no intelligent species that we’re aware of that have any amount of intelligence that don’t sleep. And so octopuses, dolphins, all those, elephants, they all sleep. There’s some reason for that. And that seems like a really thing about the evolutionary recourse of sleeping, you get eaten when you sleep. So for the benefit of sleeping should be so much better to outperform that. So I think we don’t have this idea of awake sleep in our current architecture, but I can imagine I’m simulating compress from the hippocampus some experience in the day. I’m training on more of those examples. Right?

**Ankit Gupta**

You’re collecting a whole bunch of these experienced rollouts and then you’re updating your policy function overnight or something like that. Yeah.

**Francois Chaubard**

There’s got to be something. There’s this thing called shortwave ripple where the hippocampus when you’re sleeping emits these spike trains that are actually reversed from when they actually happen back in through both the hemispheres and for seven times and then it stops.

**Ankit Gupta**

Interesting.

**Francois Chaubard**

So there’s something happening there that’s very training something. And if you don’t sleep, then you don’t have long-term memory.

**Ankit Gupta**

Right.

**Francois Chaubard**

Right? And so there’s definitely a reason why we’re training things that happened into our brain.

**Ankit Gupta**

So where does that put us now? We have all this work happening with world models. How should we think about what’s coming ahead in these next few years in the research community?

**Francois Chaubard**

Yeah, I think that we’re going to see a lot more of these world models in robotic policies. I think that’s going to unlock probably full self-driving would be one of those examples that they can get the real timeness of it.

**Ankit Gupta**

It seems like that’s coming.

**Francois Chaubard**

They could probably solve it with more compute to have parallel things and you probably don’t need it for most standard things. Maybe getting out of weird parking jams and things like that would take us some time similar to the Rosey the Robot, which we’ve always wanted to have a Rosey the Robot to clean up my room for me. I think that this feels like we’re getting to good enough that we can pay up for data in compute to get to Rosey the Robot. It does feel like that. It’ll be expensive to collect the data and do the Dreamer sequence of going from state to state and then getting the action conditioning to work. But I feel like it should work.

**Ankit Gupta**

Yeah. I mean, what’s pretty cool is we see a lot of companies at YC working at every step of this from the collecting egocentric data, collecting the tele-op data, training their own world models and action models, building new embodiments and then making ways of adapting those embodiments. And it feels like this is the first year where you see demos where you’re like, okay, this actually kind of is starting to look like it’s going somewhere. And it seems like a very exciting year ahead.

**Francois Chaubard**

Yeah. So anyway, I think that there are real AI problems to solve still. We talked about PINNs, we talked about the real time issues. And then on the robotics side, there’s real issues. It’s amazing how effective our epidermis is in terms of we can detect tactile.

**Ankit Gupta**

Oh, epidermis.

**Francois Chaubard**

Yeah, epidermis. Our tactile, we can detect sheer force, we can detect temperature, and it’s everywhere. And so versus we get one little sensor that only does tactile. We don’t have the friction component. We don’t have temperature. We don’t have all the feeling. We can’t estimate coefficient of friction very quickly. I can touch something and say, oh, this is smooth, this is rough. We don’t have any of that. And if I numb your hands, I actually had this experience just recently, if I numb your hands, you actually can’t tie your shoes.

**Ankit Gupta**

Yeah, interesting.

**Francois Chaubard**

So you can’t perform control. And so yeah, if you train on enough human data tying your laces, do I think you can do it with no feedback? Maybe. Maybe. But how much would you need if you did actually have the human touch? I think it’d be so much easier.

**Ankit Gupta**

Yeah. Well, there’s a lot of more research to do then.

**Francois Chaubard**

Yeah, yeah.

**Ankit Gupta**

Francois, thanks so much for joining us. Thanks so much for watching everyone. We’ll be back for the next episode of Decoded.
