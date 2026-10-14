---
访谈时间: 2026-07-04
访谈时间说明: "无法确认实际访谈时间，使用 YouTube 发布时间。"
嘉宾名字: "Clay Bavor"
嘉宾公司名称: "Sierra"
播客名称: "20VC"
播客url地址: "https://www.youtube.com/watch?v=YWg_YCQEZhI"
全文提及的关键名词:
  - "Clay Bavor"
  - "Sierra"
  - "Bret Taylor"
  - "enterprise AI"
  - "token budget"
  - "frontier intelligence"
  - "Pinecone"
  - "AI agents"
  - "customer support"
  - "Fortune 50"
  - "forward deployed teams"
  - "Sequoia"
  - "Benchmark"
  - "Greenoaks"
  - "GV"
  - "Tiger Global"
---

# The 100000 Token Budget Every Engineer Will Need Sierra Co-Founder

## Transcript

We have not yet appreciated the unbounded demand for call it frontier levels of intelligence. Part of the driver of the difference is probably the willingness of Chinese companies to do scaled distillation of the frontier models. Clay Pavore joining me in the hot seat, co-founder of Sierra, one of the fastest growing AI companies in the world. Sierra has raised more than one a half billion. They work with some of the biggest companies in the world and they're valued at almost $16 billion and they work with 40% of the Fortune50. If you can't build Frontier models yourself, okay, maybe the next best approach is to distill them and offer them up. Every one of our rounds, we actually guided to and took a lower price than we could have. Some of our most effective employees at the entire

company are 22 or 23 years old and have been completely AIP. We completely changed our engineering interview process. So it now looks much more like ready to go.

Clay, I am so excited for this dude. I I said to you downstairs, we do a lot of shows and I often speak to people before a show and when I speak to Neil Mater, Ravi Gupta, Zangin at GV and I hear what I hear, honestly, they were some of the most astounding references I've had. So, thank you for joining me.

>> Oh, it's nice to hear. No, pleasure to be here. Thanks for having me.

>> No, I mean, listen, they paid a lot to be featured. So, you know, you got to drop the sponsor.

>> They are great. So grateful to be working with each one of those guys. It only cost 500 million bucks. Um, so I want to start with I heard that Brett tried to hire you or start a company with you several times before Sierra.

>> Yeah.

>> Why third time lucky? Why after 18 years?

>> Third time's a charm.

>> Yeah. Why after 18 years at Google? We like, now.

>> Yeah. So Brett and I met 20 years ago.

We both started our careers in the associate product management program at Google. He was class one. I was class three. and we met in the context of some kind of shared project that we were assigned to and kind of hit it off and ended up staying in touch socially uh through mostly a monthly poker group that you in a good year might play two or three times so not not quite monthly and uh had always wanted to work together and almost did a couple times I think when Brett left I can't remember if it was for friend feed or quip tried to get me to join that and the short answer is twofold one I just loved my time at Google. Culturally, it was me. I learned more than I can ever imagine having learned in in those years. And uh the people were so extraordinary to work with. And um I had a series of managers

and leaders I got to work with who took bets on me, gave me on paper at least more responsibility than I deserved and got to work on just truly fascinating things. And so I was just incredibly happy and engaged and growing as a person and professional. And then in late 22 kind of the planets aligned in a way that I didn't think that they would probably align again. I'd always wanted to start a company. I started a very modest company when I was 13 years old and always thought I would start another. And if you're going to start a company with someone, you want to make sure that they're excellent in competence and in character and and then that the timing is right. And we could see that language models were going to be a thing. And uh if ever, you know, there's a time when the proverbial deck

of cards are shuffled in the favor of kind of smaller companies, it's when you're at the advent of the new technology. So uh happy at Google, planets finally aligned and took the leap and we're I don't know three years in change in now.

>> 18 years at Google is one hell of a stint.

>> Yeah. I >> I started counting in colleges. Gosh, I've been there one college, two colleges, three colleges, four colleges.

Yeah. It's a it's a long run. It's even more terrifying. It's a long run. Um, my question to you on the back of that is, and it's a terrible question, you can chastise me for it. What are your single biggest takeaways from that experience that you took with you to Sierra? And what did you leave behind?

>> It's such an interesting question. Of course, the the scale of a, you know, two and then 10 and then 100 person enterprise software company is very different from I think when I left Google, it was roughly 150,000 people.

things that I've definitely brought with me. Uh number one is a willingness to invest as far down the technology stack as you need in order to build the service and product that you want.

Google I think from the early days famously you built its own if not data centers cluster architectures and they were the first really to use commodity hardware that required building novel distributed systems for uh serving and data storage and and so on and so we could see that language models and uh you know as early as you know April of 23 when we started the company that agents were going to be a thing this was before All anyone wanted to talk about was agents. And we realized, okay, this should be possible. It's not yet possible, but we're going to have to invent frameworks for building these things, our own architectures really from scratch. So, actually, our our first uh founding head of research was the Princeton professor who literally wrote the paper on language model based

agents, the React paper. And so we invented, we invented and uh went, you know, further down the stack than I think some companies at that point would have been willing to. And we're not, you know, we're not doing our own pre-training. Uh we'll leave the capital expense there to, you know, the labs and uh the larger companies.

>> Before we moved to two, can I ask did you consider that because I completely understand the desire to own as much as possible.

>> Yeah.

>> Did you consider training own models and what was the thought process around not?

>> That's a great question. we did briefly and discarded it. Uh if you recall at the time, so late 22, early 23 as a startup in AI, you were kind of nobody if you weren't doing your own pre-training and building your own foundation models, character, inflection, adapt, great people at these companies, but the capital expense uh the ongoing capital expense to create what is effectively a highly perishable bag of floatingoint numbers just doesn't work. just doesn't work for any but a small number of companies. And so our calculus was for areas that are deeply capital intensive, how do we slipstream behind the investments that the labs that uh the hyperscalers are making and take as much as we can off the shelf while still being willing to uh engineer more deeply. So today we have a set of

our own proprietary fine-tune models, but these are fine-tunes on top of open weights models. So we're not going, you know, all the way down to the uh, you know, mega cluster training runs. Um, and I I think it's important that you are in control of your own destiny enough and that you don't tell yourself a story that you need to go further than you actually need to do. Is the future open models fine-tuned to specific company needs? And if that is the future with the realization that frontier models are too expensive, is that a bare case for frontier models? I think it's a lot more complicated than that. I think uh if you asked any software company, would you like to upgrade your staff level software engineers to principal or distinguished level software engineers? Yes or no? A

hundred out of a hundred would say, "Yeah, that sounds pretty great." So I I think we have not yet appreciated the unbounded demand for call it frontier levels of intelligence. And now you don't need that in every domain, right?

So for for instance, in our own right, we build AIs for companies to interact with their customers. You don't need mythos to return a pair of shoes, right?

Like you're good, right? It's like uh you want to do that well but you know we we've got some capability overhang so to speak for doing something like that. uh but in in a range of domains uh coding certainly uh science material science um uh uh legal right where the stakes are very high there's a high degree of complexity I I think we're going to see effectively unbounded demand for greater levels of intelligence and therefore the frontier models that said there will be an assembly line of cool uh GPT4 which in you know March April May of 2023 three was good enough to do some set of things is now 1/300th the the cost for an intelligence equivalent token. And so you'll have some assembly line of taking models uh that were once at the frontier to perform certain workloads and then

build open weights fine-tune models uh for those and I think you'll end up with companies using uh uh uh both mixing and matching them depending on the task at hand.

>> As we see open become more and more advanced.

Does that not mean the problem set for frontier models becomes more and more challenging? As you said, we've seen the progression of open so much that actually they can do the majority where it's like I get it for like solving climate change, cancer treatments and material, but actually like for the majority like what percent of enterprise tasks can be done with open today?

>> Well, I think if you look at what percent of enterprise tasks are completely automated today, it's a rounding error, right? It's very low.

So, is that is that a model gap? Is that a diffusing the technology into the company? Is that an application layer gap? I think it's probably all of these uh some combination of them. You're obviously correct that as the open weights models become more capable, the set of things they can do grows larger.

The set of things where all else being equal, if they are much less expensive, that you would want to point a frontier model uh becomes smaller. But again, I think we're not imagining just how high the ceiling is uh in terms of demand for frontier intelligence, invention, discovery, building new products, building new services. I I think it's hard to get your mind around when you have intelligence that can work around the clock and uh to invent to build to discover how you would use that and how much of you how much of it you could use. Can you help me understand when when we look at token economics, we thought with chat like tokens over time would go down in cost and with the movement from pure chat to chat and agents and agent economy based, we're seeing token costs increase, not

decrease. How do we see the evolution of token costs with the evolving formats, do you think?

>> Yeah, you missed one thing in there, which is a large amount of token use is driven by reasoning models now, right?

thinking out loud to themselves. And I I think actually one of the most underrated developments of the past few years was the 01 model from OpenAI in late 2024 where uh if you recall there was a chart that showed okay test time compute or in amount of inference done amount of thinking out loud and performance and it just keeps going up and to the right. It it it's logarithmic so it it starts to level out but what it effectively demonstrated is if you have enough time in compute the model will be that much smarter. So as for what happens with uh token economics, I I think there are many drivers uh underneath it. One is you're going to end up with uh hardware that is uh able to produce more tokens of at equivalent cost and so kind of the cost of the inputs so to speak will will go down. We

talked about I think you'll have this migration of certain workloads to uh open weights models. I think one of the drivers that's hard to predict how it will play out across both the open weights models and the frontier models is just the availability of compute and you know it's classic economics it's you know microeconomics 101 supply demand if you have unbounded demand for frontier level intelligence or GPUs to run open weights models and the rate limiter is the you know number of black wells and H100s you have you end up with kind of a floor on the the cost of tokens because you've got to pay for the energy, you've got to pay for the comput.

>> We had the founder of Nebius on the show the other day and he said that if they 10x supply, they could still sell out in a day.

>> I believe that. I believe that and I think that that makes the point which is I think um okay, open weights models will be cheaper because you're kind of avoiding some of the margin stack in uh the you know the hosted frontier models.

Okay, but what is the fundamental input?

its GPU capacity, its power, that's still constrained.

>> One thing that could slightly alleviate that is actually running models locally.

People say that it could be the future >> on your cluster of Mac minis or whatever.

>> Yeah. Or on even on device on phones. I I don't quite understand that when we think about always on AI 24 hours a day.

That's an awful lot to run locally. Is it a pipe dream or do we think that's actually a reality that would alleviate the server side challenge? Oh, it certainly wouldn't alleviate it. I think it will make some consumer applications much better, but I mean the reality is you need, you know, pedlops, exoflops of compute, certainly for training, and you want a whole bunch of compute quickly at inference time. And you just run into thermal limits on on your phone. I I do think it is shocking that we're all carrying around in our pockets, you know, hypercomputers these days. And will they get better? Yes. Will you have uh language model optimized hardware rolling out in in our phones in our computers? Yes, I can see a sort of uh home appliance which is you know you plug into the mains and you get you know

ondemand access to a whole bunch of compute for things in your home and maybe that helps alleviate some of it.

Certainly for uh frontier workloads though it's like there's one place you can go to for that and you know it is a giant rack of TPUs or GPUs in a data center somewhere. We spoke about kind of frontier versus open frontier obviously you have open AI and anthropic in the US who are the dominant leaders everyone knows >> and and my alma matter and Google >> and Google of course we had Damis on the show incredible incredible I love Damis >> I love Damis too >> my god he's also one of the most humble leaders I've ever met um so absolute agree there um open in the US has lagged behind we see Chinese models being unbelievably advanced and impressive do you agree that we have a challenging open ecosystem in the US and does that worry you?

>> Part of the driver of the difference is probably the willingness of Chinese companies to do scaled distillation of the frontier models uh from from the labs. My impression is many of the models uh the open weights models coming from China are derived from training runs uh done in the US. I think if you have the US-based uh labs and hyperscalers developing the frontier models, there's an obvious you like are they going to compete with themselves and drive, you know, price pressure on the frontier models by, you know, developing and releasing models, open weights models that are of similar capability. You know, if I was running that business, that's not something I would do. So, I think that's if if you can't build frontier models yourself.

Okay, maybe the next best approach is to distill them and offer them up. I think that's probably the main driver of the difference.

>> I have to ask, you mentioned earlier enterprise being a team sport. I love that. Um, and you mentioned earlier about kind of who wouldn't want you more advanced software engineers internally.

You had Lovable announced yesterday hitting I think 500 millionaire with 149 people. And in a show that comes out tomorrow, uh, Rory, who's one of my co-hosts on this kind of weekly show that we do, um, says, "Well, if you're Sierra, you can't do that." I mean as you mentioned Sierra it's a enterprise business and you have to have a different structure of the team.

When you look at the future of teams are we seeing a world of dramatically leaner fewer people in teams or actually is it still very much dependent on customers and we will still have very large teams for companies like Sierra with enterprise.

>> I think the general the general direction of travel clearly is towards smaller higher leverage teams. We have software engineers who are uh completely AI pill and using claude codeex our own internal agent we call pine cone that we used to run much of the company on and they estimate they are between three and 20 times more productive in terms of feature shipped. Now the the productivity gains certainly in software engineering and uh data science, data analysis and other area we're seeing it in in spades but I think in time it will touch all parts of uh really every company. So that's the general trend. I I think within a company like Sierra where we serve in particular the large enterprise we work with 40% of the Fortune 50. We have 50% of our customers doing over a billion in revenue. We have

30% doing over 10 billion in revenue.

These are some of the most complex and in cases regulated organizations in the world. And to be able to sell and implement our product and solutions successfully for organizations which are snowflakes. The process of selling and more importantly successfully implementing and deploying a solution like ours into the large enterprise is still a lot about deeply understanding our customers business outcomes and objectives about understanding their technology stack, integrating with it successfully, building relationships, uh earning trust to show up not just as a vendor that throws some software over the wall, but as a true partner in diffusing this technology into in our case, all of the front office, sales, support, marketing, and and so on. That's how I think about it. I mean, there's so many things for

me to unpack there. I was scribbling furiously. I I have to ask, you mentioned the internal agent pine cone.

>> Can you talk to me about what that is, how it was built, what it does. I'm just intrigued to see how companies change in how they operate.

>> Yeah, >> it's one of the more significant developments in how we run the company of the last six or nine months. And we we began by building what we call our MCP gateway. This is a single MCP server that aggregates all of the main systems and services that we use to run the company. And so you can add this single gateway to your cloud instance to your codeex instance uh and uh indeed to to pine cone and basically via any one of those agents have full access with the permissions of course that you as as an individual at the company. You can't read someone else's documents, but you can read your own. You can read your own Slack messages. And it's kind of like having superpowers, right? You can you can interrogate in essence the entirety of the company, all information that is

published, whether it's um Slack messages or presentations or operating reviews uh and and so on, and use access to all of that information to better reason, make decisions, get things done.

Pine Cone of course incorporates that MCP gateway but then is a purpose-built harness for all of Sierra. So Pine Cone knows how to build Pine Cone. So it it there's a whole harness around the engineering of Pine Cone and our engineers there are phenomenally productive. We have a whole harness around the core of our platform, our agent architecture, agent studio where uh you build and and deploy agents uh speeding up software development there.

And then we have a uh shared library of skills that anyone at the company can build. You can build one that's private to you. I have a whole bunch of skills including one that is basically the uh clay scanner of interview packets. So I to date review and approve every single hire we make and I get some help from Pine Cone and I've basically taught it what are the things that I look for what do I scan for flag these if there are any instances of them and it's kind of a shortcut to a faster deeper read of of every packet. So, uh, Pine Cone has just become this this approaching indispensable. I think we're not quite there yet, but approaching indispensable tool for running the company. And, um, I could go on on some of the other interesting things we built. Uh, I been working on what I call Sierra Brain and

um, some other things in the >> What's Sierra Brain? Sierra Brain is it starts with a 20 or 30 page document that grounds any agent in what we are as a company, what we do, how we're organized, our team structure, the competitive landscape, our strengths and weaknesses, all of these things. And uh then uh on top of that I've given it access to uh every one of our recent board letters uh every one of our recent operating reviews uh other insights and observations we have about like what we believe to be true about the world and I can then use it to reason about what we should be doing as a as a company. And so it's uh a bit like a strategy thought partner um if you will that knows the company, you know, if not inside and out very deeply.

>> We're going to get to your board letters cuz I heard about these and how you have boards every six weeks, not every quarter because the world moves too fast apparently. Uh oh, trust me, I stalk the [ __ ] out of you. Um, but I I I just want to kind of stay on like internal builds cuz you mentioned there, you know, Bney, the internal agent that you have, we we're having a lot of CEOs who I speak to who like, I got no idea. Do I just let my devs teams run wild on token spend? Do I give them some form of budget?

>> Token maxing.

>> Yeah. What what's your personal take and what do you and Brad sit around the fire and say, should we put a cap on this? Do we just encourage them to go wild? How do you approach it?

>> Yeah. So I think over the past six months using a bunch of tokens was a proxy for you're using AI, you're you're leaning into it, you're trying to be more productive with it. So I think it's generally been a positive signal. I have heard and I have observed that top engineers who are really leaning in to cla codeex and so on are spending more than $100,000 on a run rate basis on tokens per year. That's a meaningful fraction right of of an engineering salary. So I think the direction that we're headed is some amount of token budgeting on a per employee basis. I think for CFOs in the future like capital allocation will look more like how do we allocate opex and not just opex and then headcount and headcount will be both headcount for salaries and SBC and also tokens associated with uh

with headcount and so here's your salary here's your token budget have at it we are not yet at that point our our usage compared to some of those larger numbers is modest And I think the benefit of learning at the fastest rate possible uh outweighs kind of the you know capital uh capital discipline at this point. We prefer to learn quickly see what works.

It'll be interesting to see how the rate limiter in software development moves around. How the you know Andy Grove breakfast factory you know what is the what is the constraining factor? It used to be writing code. Now it's probably reviewing code. pretty soon we'll be deciding what is worth building and kind of editing kind of what could exist to what should exist. So the dynamics there will be interesting.

>> I think the core question for us to understand if if everything is slightly overhyped is what percent of developer salary will be spent on tokens in the future. Mark Beni off you said larger companies said that he spends 300 million a year on anthropic for his dev teams. That works out to about 3.8% of developer salaries.

Not actually as much as the headline 300 million makes you feel. If it stays at 3.8%.

A lot of the companies that we're investing in and see around us are actually grossly overvalued.

If it goes to 20%, they're undervalued.

And I had Brandon at Mccor on the show who says he spends more on tokens than he does headcount.

>> Yeah, >> I think 3.8% is wildly off from where the steady state will converge. Where do you think it I'm not going to hold you to it in five years time, but do you see it being at 20%.

>> Oh, I do. I do.

>> So, the 100 grand a year actually will be normalized because you think about a great dev in the valley. I presume 500k is kind of where they're at for a great dev.

>> Uh, sure. That would be the upper end.

Yeah. Yeah. In salary.

>> So, it feels kind of normal.

>> Yeah. I would not bet on 3.8%. I would bet on much closer to 20%. In software engineering, the gains to me seem unequivocally there. You can debate is it 2x, 10x, 20x, even if it's 2x, okay, you've just effectively doubled the size of your engineering team. That's remarkable. You mentioned the 40 of the Fortune50 being customers and I you use that quite a lot in a lot of your marketing materials >> and it strikes me as like a very enterprise company. Candidly, is it difficult or how do you retain a real product focus, a real closeness to customers when you're so enterprise? Is that difficult?

>> I think it's a little bit of a false choice you're implying there. I I think being being large enterprise doesn't necessarily mean you need to be distant from your customers and in our case, our customers customers. So, uh, Brett and I are constantly building agents ourselves. Uh, one of the more interesting things of the last six months, we released Ghostriter. This is an agent for building agents. It's kind of agents all the way down. It's pretty cool. But we are constantly in the products ourselves. And, uh, Brett is actually still an extraordinarily capable software engineer. It's remarkable. So, you know, some of the code that is in production, right, he he has written um I've I've probably got a couple lines here or there, but you know, pales in comparison. And and so,

of course, we can't on our own simulate the complex multi-system environments that characterize many of our largest enterprise customers. So, that, you know, we have to kind of simulate in our heads, but we're in the product. And then one of the one of the things I think a lot about is we will in short order be in a way one of the larger B2C companies. We're doing that via our customers but you know we'll we'll we're serving hundreds of millions of interactions right soon billions of interactions and uh so staying close to the end experience there as well. voice fluency, latency, the quality of the experience, all of that stuff is very energizing in things that we're close to. So yeah, I I don't feel I don't feel distant from from the product either from our customers perspective or from

their customers perspective. I always looked at the space itself and I was like amazing space, what a huge town, what a problem and AI perfectly suited for it. And then I kind of peek under the covers and I'm like, "Oh my god, like 15 companies funded with 100 million bucks. Salesforce, Atlassian, Zenesk, all the other incumbents. Oh my god. What is the like market maturation of this space? Help me understand how this evolves in like a 5 to 10 year period." >> Yeah. Yeah. I think first of all to state the obvious, the the great thing about being in a giant market is it's a giant market. The challenging thing about being in a giant market is it's a giant market and other folks know it too and it's it's startups, it's um long-standing companies. Uh it's the incumbents and uh so your point on it

being competitive is is certainly right.

Uh five or 10 years especially, you know, in the the age that we're in is is a long time. I think what I would point to is amongst the startups, customers are voting with their feet. So we are at multiple larger uh multiple larger size than kind of our next nearest similar vintage startup competitors growing faster and as I said are working with many of the great companies in the world and um and so I >> you think it's like an Uber lift market or do you think it's an AWS Google Cloud Azure market?

>> It's it's hard to know. I I think I think because the economies of scale in terms of depth and breadth of platform, experience in specific industry verticals and so on really compounds. My hunch is it will be more like an Uber lift market. Um and we obviously think we're in the pole position uh to be the bigger of those two and um that's how I think about it.

>> You sell again we sell to some of the biggest enterprises in the world. Um, I had a guest on the show the other day say you can't sell to enterprise without an FTE motion.

>> Would you agree with that knowing all that you know now selling to 40 of the 50? I would like to think at least in the AI space I would say rediscovered and borrowed this model from Palunteer and we came to it almost accidentally. So we started the company and the first thing we did was reach out to people we trusted to understand what are the biggest unsolved problems that you were looking at and saw oh interesting service and support as a foothold into something much broader helping support customers across the entire life cycle. We then enlisted uh half a dozen design partners that we built the first version of our product and platform with and for and these are in the history of the company legendary legendary companies. Olai great flip-flops you should buy them. Uh

Sirius XM uh Sonos uh Weight Watchers and we built the first version of our uh platform with our engineers deeply embedded inside those companies. So much so that uh our founding engineer uh Mihi uh was actually an employee of Weight Watchers including getting like its performance review time emails and and so on. And what we realized in that was no one has ever deployed an AI agent. No one has ever put AI in this way in front of their customers. And in order for us to build the best thing as quickly as we and our customers would like being so close to the business, the mechanics of it, the people, their business model that we understand it, I won't say as well as our customers, but uh approaching that we we saw so much power in that. And so starting in early 2024, we really

started building out this forward deployed team and uh customers use it in in widely ranging ways. Our platform is highly extensible and very transparent.

You can see exactly how an agent is built. Uh you can export agent definitions and completely build your own. So no need for for deployed if if you don't want it. What we generally find though is in getting started having Sierra and help from our teams kind of drive while our customer is in the passenger seat but navigating for the first version. It's what has enabled us to take companies like Next live in six weeks from kickoff to live uh behind their phone number and chat in six weeks or Sigma right one of the largest healthcare companies in the world live in I think it was 58 days and so time to market uh time to impact time to value and then the quality of the result um we think it makes a big difference I wouldn't say it's binary though as you you framed it I I do think you can sell

without a forward deployed team Um uh but I think for getting to the impact of this technology as quickly as possible and at the magnitude that we know is possible. Boy is it an important catalyst.

>> Are we at a unique time in history where for this specific moment in time every buyer is in the market for the product normally not everyone is in the market for a product at the same time.

Every CEO is being told by their board, how are we using AI?

>> Yeah.

>> Is it a unique time because there is buyer pull like never before for this specific moment?

>> There is effectively unbounded demand I I I think in in two areas. One, we've talked about coding agents. The other is the space where we're the category leader. And so one of the reasons we've grown as quickly as we have is to meet that moment and meet that demand. We um we're now 100 people here in Europe. We recently acquired a company in Japan, Opera Technologies. You and I were talking about this to hit the ground running there and to have a team that can be attuned to the cultural nuances of of Japan and um you know the concept of omotanashi which is like extreme hospitality like that is what is expected in Japanese service and that's what we intend to build there. Can I ask you you obviously starting with the kind of beach head in customer support and customer service to scale into the

company you want to be you you have to move out of customer support into complete life cycle management I guess.

Is Sierra a sales platform in the future? Is it a conversion platform? Is it a marketing platform?

What is it?

I think rocket is actually a pretty good indicator of the direction that we're headed. And so you think about the uh life of a rocket customer. It begins with search and discovery of a home they might want to buy. We worked with Redfin to rethink their search experience. Uh we help Rocket reach out to folks who've expressed interest in a refinance and make contact that way. uh we worked with them to build rocket assist to help bring people in and uh help them shape and size their loan, gather all the information needed and so on. None of that is service and support, right? We do do that, right? Loan servicing and and so on. So, I think that's a a good example of of where things are headed.

>> That's an inbound sales machine.

>> Inbound, outbound and outbound.

>> Inbound, inbound and outbound. You're right. And uh it's not just Rocket alone. Uh, next we worked with them on personalized product recommendations.

How do you help someone build an outfit uh a bigger basket of things they will love? And again, that's that's much more sales than uh support. So, >> this sounds and feels more like kind of a uh Fortune50, Fortune 500 Palunteer, but more con consumerized where you're building these kind of amazing solutions for these products to fit their needs.

Is that unfair of me?

>> Um, first of all, Palanteer is an amazing company and and we have we have taken a lot of inspiration slash you know copied from them elements of our for deployed approach. Um, my understanding is you know Palunteer has kind of low hundreds of customers. we we we are and intend to be at a lot larger scale than that and I think where that will come from in particular is building real domain expertise and specific industry verticals and uh you know of course our our first second and third customer deployments were by definition unique one of a kind I think we've learned some things about how to help build a basket in the retail setting uh and in some of these other industries how best to handle a question about uh the status of a health care claim, healthcare insurance claim,

or um questions about a fee around a checking account. And so I I think we're going to have these deeper and deeper lessons in specific industries and be able to apply those in a in a much more scaled way. Will you build products that aren't uniformly applicable across customer bases? So if one customer needs specific cart abandonment product features, is that something we build or is it no that's not applicable to the platform?

>> One of our approaches in building the company and this kind of goes back to where we started.

You can build a platform and hope that people come right the applications get developed on it or you can build applications to inform a platform that makes building the third, fourth and fifth that much easier. And so wherever we can, we're scanning for opportunities to strengthen our platform. So commonality is much better than something that is truly a one-off. That said, if we're working with a Fortune50 or Fortune 20 or Fortune 10 or Fortune 5 uh company and there is some element of that company that is literally unique, of course, we'll build that. Of course, we'll build that. And one of the neat things is it's actually become feasible to build that because of coding agents, because of the pace at which you can move. There's a real unlock there in being able to build uh a solution on an

already deep platform, but extend it in in ways that uh may apply, you know, to a to a single customer. My hunch though is that if you build it for one, right, it someone else is going to have that same problem, right? And so it's it's less common than you would think. True.

everyone at once. I >> I totally agree with you and get that. I I do want to go to the way that you run the company. It was so important in so many of my conversations before this. If we start with like the board meetings, I I spoke to as I said many of the investors every six weeks, not every quarter, can you talk to me about your biggest lessons on how to really get the most out of your board and run the best board meetings?

>> We do a couple things. You mentioned the uh six week cadence. We have kind of a tick- tock, a three-hour meeting and a one and a one one and a half hour meeting. We've done this since the beginning of the company because we could just see if you're on the AI time clock, it moves a lot faster. Things are changing and you most recently we came back from winter break and suddenly coding coding agents were amazing. You had right claude 45 codeex 52. There was a fundamental step change in the capabilities of these models. It changed our approach to software development. it changed our approach to the core product. And so having a cadence where you can take in information even from the last six weeks, kind of update your priors and then change course I think is quite important. As for running the the

board meetings themselves, we don't have board decks, we have board memos. So Brett and I write a usually six to 10 page memo.

There's a a saying, writing is just thinking on paper. And I I think it's very hard to hide from writing. And so getting our thoughts clearly out onto paper, sending that in advance, giving each of our board members some kind of soak time to to think through the issues and come prepared rather than be like presented to and managed I think is a big part of it. And then the contents of the board letters themselves I think is notable. you we've done quite well in our you know first eight quarters in in market and generally the the format of a of a board letter is like we exceeded forecast by a wide margin yet again things are going well we landed these these customers and here are the seven things we think we could be doing better where where we're unhapp we could be going faster

here need to hire in this area and and so on the board meetings kind of take form on their own based on that you get the scaffolding right you get the people right. You get kind of setting the table of the big questions we're asking and and then genuinely genuinely inviting our board members in to challenge us and improve and sharpen our thinking. Those are some of the ingredients.

>> I heard that you write also about everything that you suck at.

>> Yeah.

>> What was one of the most memorable writings on what you suck at? one early on was we had such good indicators of the demand we were going to see and we just didn't hire fast enough to meet that demand. Right? So it was it it was like h like we we we could have taken on this additional set of customers and we had the data in front of us like we could see it and we didn't act decisively enough to build out a recruiting team right like scale faster. This this was early 2024 so early days in the company you know we've since corrected but that was one that stands out.

>> We are going to go to hiring. You mentioned some of the people around the table. You know, often people say this, but you really can. You and Brett, I mean, like, it's the dream team, the best of the best operators. You can choose any investors at almost any price, which is kind of hard. How do you and Brett sit down and discuss price on a new round because investors will pay anything to get in?

>> You want it to be like high obviously, >> but also not too high. How do you actually think about that? Is it like okay three years on next year's target?

What does it look like?

>> Um it it's generally been inbound is the answer. We think about it um honestly not in terms of valuation. We think what is the amount of capital that we need to raise to get to the next unequivocally higher watermark in terms of revenue, company scale and so on. So we think of it as like milestone to milestone funding. Um and then uh we're sensitive but not maximally so to dilution. And so right how do you how do you balance those things? And I think in every one of our rounds um we actually uh guided to and took a lower price than than we could have >> again spoke to them. They said about the values within the company craftsmanship, intensity and family, >> trust and customer obsession as well.

Craftsmanship, intensity, and family are three that I I wouldn't normally see.

>> Can you talk to me a little bit about why those are so important?

>> I'll start with craftsmanship. Both Brett and I, just because of the way we are, we care about doing things well. If you're going to do something, do it with excellence. And I think there's two ways in which doing things with excellence mean much more than just kind of sweating the details.

One is what is a great company? A great company is an aggregation of thousands and thousands of things that are themselves great. It's great people.

It's processes that are welldesigned.

It's a great product.

It's a great culture. And and so how do you build an excellent company? Well, you build everything with excellence.

And and so I think holding ourselves to the standard like if it is worth doing it is worth doing well is is one part of that because that adds up to to a great company. How else do you get there? The other is you think about what our customers are trusting us with. Back to the trust value but I'll I'll make the connection with craftsmanship. It is with their most precious asset. It is their customers.

How will a company know? How will a set of people who are considering working with us know how we will show up with their customers? A lot of it is how we show up with them. And so sweating the details in how we show up and interact with our customers. The level of professionalism, care, dropping everything when something matters. I give you an example there.

when we in our first Black Friday Cyber Monday with a set of retailers, one of uh one of our lead engineers, our head of operations, me or Brett was in real time personally reading every single conversation that our agents were having because we we wanted to make sure we were doing right by our customers. So that's craftsmanship and again adds up to a great company and it's I think very meaningful in helping our customers understand the care we will have for their customers.

>> Intensity and family.

>> Yeah.

>> Can you expand on those again two that I don't often get?

>> Intensity. So I think it's it's back to this great thing about giant market.

Giant market hard thing about giant market. Giant market and others are in it too. I think there is an inevitability to companies interacting with their customers via really sophisticated agents that capture all that they know and all they can do on behalf of their customers and get the job done on their behalf that handle the complexity as opposed to pointing you to websites and and so where the the conversation is the interface, right? I I think there's an inevitability to that and uh and therefore in order to win in order to build the best company in the space it is about pace it is about winning it is about uh building the best product it is about uh being competitive and being intense about it and uh knowing that you know we don't have the the luxury of patience there's no nothing written in the wind

right that that any particular company will be the showing up in our fifth engagement uh and 500th engagement, you know, as intensely as we did our first like you have to do that. And so I think there's also I talk about the ven diagram of who we hire for. Smart, nice, and tense. And it it's hard actually to get all of those three in a single person. When you when you do, it's fantastic. And you can feel it in the office. And another way of translating intensity is doing things with excellence. Doing things with pace relates to craftsmanship as well. Is there anything that you can do or add to an organization to increase or to maintain intensity? Be it timelines, be it rewards, incentives. How do you keep intensity with scale?

>> I think it starts with the founders.

like Brett and I are quite intense and and so I think we we have to be the pace setters, right? We have to be the examples of intensity and and so it it shows up in how we manage the company. He and I aren't deep in details and are constantly is this good enough? How could this be better? How could we go faster on this? Why can't it happen tomorrow instead of next week? So I think it has to start with with the founders as as one. How do you determine what you should be in versus what you shouldn't? We've seen the resurgence of like founder mode of founders being in the weeds.

>> Yeah, >> it's also not possible in everything and it's not right in everything. How do you determine that?

>> You have to edit it. You have to have judgment for it. And I I think you have to look at what is the thing that is not going to happen or won't happen as quickly without direct applied force from one of us. uh or both of us and and so you know it's pointless to be in quote founder mode you know 17 layers in the details and something that doesn't matter. It matters a lot if it's our next generation agent architecture and there's something that we can add.

Uh and so we try to be selective about where we engage at at that level but um it's anything but kind of hands-off uh hands-off management. So I think it starts with the founders. Um I think uh ambitious goals have a way of becoming self-fulfilling.

You set out a goal whether it's the quality of a product or a revenue number. It's like well what would have to be true in order to get there? Like let's suspend disbelief and just imagine like what would have to be true to cover this much ground this quickly? Why can't we do that? Why?

Okay. Why shouldn't we? Japan is an interesting example of that. Like why why can't we have a giant business in Japan this year and not next year? What would have to be true? Oh, we'd have to have like 10 people on the ground. I was like, why don't we buy a company there?

So, you see how this stuff hangs together. So, ambitious goals can take the form of of a date. Sure. You know, dateriven development can sometimes work. I think also work is like a gas and tends to expand to fill all available space that you give it. And so there's a danger in setting dates as well where it's like well we've got this long uh it may not need to take that long. So >> it ties to the third one which is like work expands to the room that you give it. Yeah. I give everything to my work and I love that.

>> Third family >> as a as a value.

>> Yeah.

>> I'm just interested by that one.

>> Each of our values comes directly from Brett and me. And actually one of the best decisions we made was I think it was the time we were five or six employees. We spent half a day. Brett and I have a technique we call think apart think together where we'll initialize on a prompt. And the idea is not to group think one another. So we want to get kind of the best of our independent thinking. And so we we did a think apart think together on on values.

Went off and spent an hour kind of writing up what what our view was. Came back and compared notes. There was first of all a shocking amount of overlap which I guess shouldn't have in retrospect been surprising. It was like we had wanted to work together. We've been friends. I think we deeply similar in in many of our values. Really all of our core values I would say. Um family uh comes from I've got four young kids, Brett's got three kids. And um I you know I married my high school sweetheart. Uh, and I think for both of us, the only thing that's more important than Sierra is our families. And our belief is that you can be part of something that is growing fast. You can be intense about your work. You can turn on the afterburners when when you need.

And yet, and it doesn't just mean kids, it's picking up your parents at the airport when they get in from out of town. It's uh going to the friends, you know, extended birthday weekend. It's being Yes. at the parent teacher conference or whatever it is. And I think there's too often uh an image of kind of a sometimes performative grind uh in uh certainly Silicon Valley startups. And it's not that we don't believe in hard work like boy do we like again intensity. Um but it's in in working smart and finding some balance um that gives you uh space for again translate family to things that matter to you in the sense of your your whole being beyond just work. Are you literally able to work as hard though when you have a family and you have four I mean Clay amaz four four kids it's it's a lot of kids

>> I find uh I I work a lot um you know of course if you just magically handed me you know 15 hours in in a week that I you know wasn't wasn't with kids probably do something with those I find I am intensely focused and efficient and so like boy do I get a lot out of uh every hour I have uh one of the things uh I've done I spend a lot of time on 101 um uh going to and from the office we were all about in person and coming out of the pandemic it was something of you know a novelty being opinionated uh about being in person so I spent like an hour and a half um sometimes two on the road every day I now have a very complex networking setup that combines two cellular networks and a Starlink uh mini so that I uninterrupted beautiful connectivity to and from the city every day. You're efficient. You get

everything that you can out of every hour.

>> Why are you so opinionated about in person?

>> In particular for a young company, I think it is, I won't say impossible, but very challenging to build a culture, a set of shared norms, camaraderie. I think so many of the things we talked about enterprise software as a team sport. It feels great to be part of an amazing team and it's different when your connection to that amazing team is via a Brady bunch of Zoom squares.

And so we have rituals that we've developed that we only would have developed if we were all working in person.

There's I think for younger employees apprenticeship and mentorship that happens. So much of what I learned and I think the initial conditions of of my career were from experienced people taking me under their wing or letting me in cases literally look over their shoulder at how they were doing something. Uh I think there's um an element of paying it forward that's that's important. Uh and and in person has a role to play in that as well.

There's a talk that I love by the renowned computer scientist Richard Hamming. you and your research and it's for any new graduate probably the single best thing uh on a per word basis I think you can read and there's several interesting points in it but one of the central thesis is find great people work with them and learn from them and I I mean it it it sounds obvious but there's something deeply correct like how do we learn as human beings we observe someone doing something and we effectively copy So find great people and copy them.

That's how you accumulate skills and capabilities. And one of the other points Hamming makes in this talk is knowledge and hard work are like compound interest. And we all know the earlier you start saving because of the miracle of compounding interest, right?

It it can massively change the trajectory of your life. And so I I think any young person should be intensely focused on learning as much as they can as early as they can locking in those kind of lessons and and capabilities uh if you will because it is literally trajectory changing.

>> Do you want to hear two funny things?

One, we used to do five shows a week. Um I just worked harder than anyone else when I was starting out.

>> That's a lot of shows, Harry.

>> Yeah. Yeah. It was 11 years ago, but it was five shows a week. Um, and then two, I didn't have a thousand listeners per show for three years, and I never made a dollar on the show for three years. It was never about money or recognition. I only cared actually about using this as a method to learn from you. And probably when, especially when I was 18, it was harder to meet amazing people. And so I completely agree with those two. There are a lot of young people today you have kids can picture them leaving university who are uncertain about where the world is what to do. What would you advise Sam knowing all that you know?

>> The obvious kind of tsunami coming is AI and okay what are the implications on jobs for that? I think there's been a lot of concern understandably about okay what what happens to entry level jobs how do you apprentice and so on. I think the unfair advantage that young people have coming out of university is you've just had four years to spend effectively unlimited time. You got to go to class and, you know, pass some exams and stuff, but you have huge control over your time and disposable hours.

Coming out of university as a master of these AI tools, boy, I let me point you to a thousand companies that would love to have you infuse what you know into how they're doing things. And I I I can't remember a time when a young person with no work experience, but with the right mindset and experience using some of these tools, has ever been so valued. Some of our most effective employees at the entire company are 22 or 23 years old and have been completely AIL and have a comfort and facility with these tools uh that many of our more experienced folks don't.

>> Has the way that you hire changed for the profile that wins in this AI pill world?

>> Yes, we completely changed our engineering interview process. So, it now looks much more like here's a very um here's a a kind of prompt.

Think through an application you would like to build. Cool. Okay. Here's $150 to spend on choose your coding agent.

You can use whatever setup you want. Use whatever tools you want completely.

Bring your own laptop. Bring your own tools. We're going to pay for your tokens and then build it. Tell us how you went through building it and so on.

So at least in engineering it is an AI native interview and of course we we test for architecture, systems design, uh product thinking, uh culture, smart, nice, intense, uh the extent to which we think people manifest our values. Uh but that's changed very significantly and I will be disappointed if in the next no more than two months not every one of our interviews has some strong AI native component to it. Do you think you mentioned architecture there? Do you think we are entering a golden age for cyber and for cyber security given the proliferation of code generated by AI that may not be as secure as it needs to be >> in terms of importance?

It is it is obvious to me that it has never been more important given that the kind of offensive capabilities just ratcheted up five notches. So um I think cyber security seems like a pretty good bet to me. The question is whether the offensive tools turn to be defensive tools, right? If actually Mythos and Codeex 55 cyber, if they themselves are the solution, not kind of a uh more narrowly focused um cyber security product. Not an area of expertise for me.

>> What was the most recent disagreement you and Brett had? Couple weeks ago, uh we were trying to figure out how to get something to move much faster in one space and uh it's interesting. We we basically always converge. It's like we we're highly truth seeeking. It's like what is we have a funny expression like this is correct. Okay. What what does that mean from from some objective truth seeeking perspective like this is the right way to do it. So we we try to get to okay what is the correct solution.

I was on one side was like I I think we need better kind of process and structure around this thing. Brett was on the side of people and maybe we need different leadersh.

Um the answer as with most things like turned out to be some of both right turned out to be some of both. But um I think um we we started from uh no it can't just be solved with it's like no it's not just people and you know we pull on those threads and this wasn't think apart think together so much as just kind of interrogating each other again with the goal of just getting to the right and best approach to something. What when Brett says something are you like, "Yep, I'm sure he's a G at that." And what when you say something, is Brett like, "Yep, Clay's Clay's the expert." >> We think about rather than dividing up the company, we think about majors and minors for every part of the company.

So, uh, Brett's majors are definitely sales and then engineering. He is really good at selling software. He is really good as a software engineer still. We both spend a lot of time on product and I I major in what I've like the running of the company. So operations, finance, legal and and so on. But um I do a lot of first calls like he understands our most important contracts. Uh you know for things that are highly consequential on how we run the the company, you know, we have kind of two nuclear keys that that we turn on those.

Brett uh having spent time at at Salesforce really learned from the best.

Like Mark is extraordinary and so he's the best seller I've ever met.

>> Unbelievable. The goat. The goat.

Unbelievable.

>> How's the weather, Mark? Have I told you about agent force?

>> The just but but honest honest respect.

Uh and and so when it comes to instincts on how to sell, you was like, "Yep, okay, makes sense." Um Brett's instinct on system design and architecture are second to none. And so I trust his judgment more than I I trust my own. Um on on people stuff, on kind of the building and running of the company, I it was like whatever Clay says, I would go with that. So that's probably the the rough uh yin-yang uh major minor split.

>> Dude, I would love to do a quick fire around if it's okay.

>> Yeah, let's do it.

>> Okay. What was your biggest lesson from working with Sundar? Cinder has a remarkable ability to look at a problem from wildly different zoom levels. His dynamic range and thinking is second to none zoomed all the way out. Highest level strategy. How is this going to unfold over the next five years all the way into the the details, the pixels, right? the drop shadows, the sound, the texture of something. And I I have tried to emulate that. Talk about surrounding yourself by great people or having the privilege of working for someone. I observed a leader who is extraordinarily focused on the product, the work, building something great and also is just a wonderful human being and deeply focused on the humanity and folks around him.

>> What does no one know about Google that you think everyone should know? What people underestimate about Google is when you have the alignment of an ambitious, enduring mission, incredibly smart people and a culture that values truth and building in service of that mission. That company can kind of solve anything. People sometimes criticize Google for a thousand flowers bloom. If you have smart, well-meaning people caring for every one of those flower beds and they're they're directed in the right way, it is quite a force for invention and discovery and building new things.

>> I got asked to ask you about your book list.

>> I hear you read a lot.

>> That's a [ __ ] question. Forgive me for it. What's the must readad for me leaving this conversation?

>> Oh, give me one. David McCulla, the Wright brothers. It's so good. It's so good. It's a tight history of obviously the invention of the first uh heavier than air aircraft. And to me, it is as accurate a portrait of entrepreneurship and invention as has been written anywhere. The aircraft could not have existed without this kind of network of pre-existing inventions. Most importantly, a lightweight internal combustion engine.

And then it was try, it didn't work.

Try, it didn't work. There's scenes of them stuck out in North Carolina being eaten alive by mosquitoes. It's the hardship uh and then the triumph of, you know, having built something that flies. Uh, I've never said this before in a show, but have you seen a wonderful film called uh Those Magnificent Men in Their Flying Machines?

>> No.

>> I'm gonna I'm gonna send this to you.

>> Oh, I look Okay, sounds good.

>> It is about the kind of pursuit to fly from mankind.

>> Oh, fantastic.

>> It's amazing. 1940s50s.

>> That's great. I'm looking forward to that one.

>> Um, okay. Parenting four kids and an unbelievable operation and founder.

>> What's your biggest advice? First of all, uh having kids is the greatest gift. It is such a privilege and I a few things I I would say. First of all, you feel that way. Um you will be a changed and different person, you know, on the other side of holding your son or daughter. It's just it is the in my opinion single uh fastest rate of change single biggest change that anyone experiences in their life after they themselves are being born right welcoming your your first child carve out time family dinner uh we have uh many mornings on Sundays maker mornings with two of my sons where we block out an hour or two and we build something at home and so rituals and discipline around making time and space it I think anything important in life my view is a product of clear goals and

good habits and so I think if you have a clear goal around how you want to be as a parent and then habits that help you build towards that I think that's a very important ingredient and then the other is making kids interests your own and so I'm terrible at basketball my eldest son is an incredible basketball player. I am so proud of him. I go and watch him play and say he does things like I could never do that. Not only can't I do that, I could never do that. And and so I I follow the playoffs. I've I've learned about the sport. I've learned about the the best players. I've learned about coaching so that I can try to uh enjoy and support him in this interest uh more fully than I otherwise would be. And so I think for for each of our four, it's it's being aware of what gets the

synapses going for them, what they light up about, and then making that interest my own.

>> Would you say that's the same for your partner? Like, do you need to have aligned interests in a partnership in a marriage, or is it good to have different ones?

>> I mentioned married to my high school sweetheart. Uh we we will have been together for almost 30 years. Um and I yeah you I'm not that old. Um I think a great mar a great marriage is a partnership. It is and a and a partnership means you are working in pursuit of in service of some shared set of goals and and so you asked about interest. I think having shared interest in what you are pursuing as a partnership is deeply important. happy kids who grow into uh uh adults who can enjoy their lives and contribute meaningfully to those uh around them. um building a set of values in one's family that are aligned with with your own and then and then I think ensuring as part of that partnership that the other member in it themselves themsself thrives and fully realizes themsself and and there those interests

may be different but there can be a shared interest in enabling each other to become the best that you're able to become.

>> Final one for you, but I I do like it.

What's the kindest thing that anyone's ever done for you?

>> I feel such gratitude to my parents. And I'm sorry if it's a straight down the fairway answer. Uh my father was a career cardiologist. My mom is a very quilt talented quilt maker. And neither of them were in engineering or technology.

And they saw that when I got a hold of my first computer, I just lit up. And not really understanding what computers were about. My mom was uh good with them in in the 80s, but um it was not at all clear where they would go, but they could see that I was obsessed with them.

And they supported that interest to, you know, to to the hilt. My I remember going with my father and my mom and dad uh to buy an early Power Mac and you know my dad was pushing like would you be able to do more if we had more memory in it? I I think I would be like well we should get more and I was like is this real life you know? Um my mom would take me out of school one day a year and we would go to Ken's House of Pancakes, get breakfast.

she would make up a doctor's appointment or something for me and then we'd go to Macworld and I would get to spend the day at Macworld which for me was like Nirvana and so uh I feel such gratitude to them and seeing in me that interest and how I lit up about this thing that was unfamiliar to them but that they then pushed and and enabled and of course it was a direct line from that to uh wonderful 18 years at Google starting Sierra and today.

>> They must be very proud of you.

>> I think they are. I I think they are. Um I know that they are.

>> The thing that strikes me from the show is I don't mean to say copantic, is just like what a what a good person you are.

>> Oh, >> do you know I know I I interview a lot of people and they're brilliant and they're intellectually brilliant. You obviously are that like what a a genuinely good person you are, which is really um it's very tangible. So like I really can't thank you enough for doing this and you've been an incredible guest.

>> Thank you so much, Harry. I really appreciate it.
