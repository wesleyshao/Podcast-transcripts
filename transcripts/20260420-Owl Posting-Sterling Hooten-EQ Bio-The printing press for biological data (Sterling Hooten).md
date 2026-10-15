---
访谈时间: "2026-04-20"
访谈时间说明: "未确认单独录制日期。频道视频 RSS 的 YouTube 发布时间为 2026-04-20T14:59:26Z，文件名采用该日期。"
嘉宾名字: "Sterling Hooten"
嘉宾公司名称: "EQ Bio"
参与嘉宾:
  - 姓名: "Sterling Hooten"
    公司或机构: "EQ Bio"
    职务: "founder"
播客名称: "Owl Posting"
播客url地址: "https://www.youtube.com/watch?v=-rlJDGC2eC8"
全文提及的关键名词:
  - "Sterling Hooten"
  - "EQ Bio"
  - "Owl Posting"
  - "microfluidic bioreactor"
  - "biological data"
youtube_video_id: "-rlJDGC2eC8"
YouTube发布时间: "2026-04-20T14:59:26Z"
播客标题: "The printing press for biological data (Sterling Hooten)"
字幕来源: "YouTube 英文字幕原文，整理为段落，未翻译、未删减。"
companies: []
industries:
  - "生物技术"
  - "制药"
  - "制造业"
technologies:
  - "合成生物学"
keywords: []
tags:
  - "生物技术"
  - "制药"
  - "制造业"
  - "合成生物学"
---

# The printing press for biological data (Sterling Hooten)

## Transcript

What what we're building is Like in philosophy there's a difference between like changes in degree and changes in kind, right? So it's like, okay, you take a little step, you take a little step. And then you've got like, okay, when you 10x or you 100x something, right? It's like all of a sudden new things get get unlocked. Okay, those are like the axioms. It's like these are the things in you. And then I literally went through every manufacturing technique that I that I could find. I mean, it truly. Everything down to like, what are they doing with, you know, 3D printed glass, you know, at the moment? And and you can just kind of like knock these out for a variety of reasons. Our goal is to produce 99% of the world's dynamic biological data. And the reason that that's achievable is because we do not produce that much right now.

>> Today, my guest is Sterling Hooden. Sterling is the founder of EQ Bio, where he is building a microfluidic bioreactor built on a printed circuit board that cultures, senses, and streams biological data in real time, claiming 10,000x higher experimental throughput at 100x lower cost. It is one of the most niche areas of wet lab automation that I think I've ever discussed on this podcast, and I don't think I would have ever learned about it had not stumbled across Sterling at an event a few months back, where we had a conversation that was so fascinating that I immediately wished we had filmed it. Sterling, welcome to the podcast.

>> Thank you for having me. Very big fan. Really enjoy your articles.

>> Thank you. The So, I've given a brief introduction of what you're working on at Eku, but I'm sure I oversimplified some things. I'd like to hear your own pitch for what you're doing there, and why is it so valuable?

>> So, the like largest problems of the 21st century, things in medicine, for climate, for um material optimization, all of these are predicated on our ability to manipulate and control living matter. So, advancing our our understanding of biology is just so fundamental to these to these problems in the future. And yet, the tools that we use right now to interact with biology are primitive. Um they're primitive in an absolute sense, and they're primitive in a in a relative sense to to what we could be doing. Uh At its core, biology is, you know, time varying. It's um parallel, and it's sensitive. And yet, the tools that we use right now um that interface destroys at least one of those properties.

And in principle, uh advances in AI also would be an excellent, you know, connection with biology. But, that interface is fundamentally broken. So, like lab automation right now is stuck at the Petri dish and the microtiter plate level. Uh it's it's equivalent to the you know, like like handwriting manuscripts in the in the 15th century sometimes. And so, what we're building is the uh a printing press for biological data.

And the way that we're doing that is we're rethinking um that interface between uh compute and biology, and we're we're replacing uh traditional microfluidics with a printed circuit board that allows you to uh embed the fluidics, cells can live inside of it, and that allows you to communicate and control cells in a way that is um has not been possible before at at high throughput. And the like largest application that we see for is in biologics manufacturing. Um right now biologics, it's, you know, a half a trillion-dollar industry and it's supply limited. So, every year uh Samsung Biologics has to build a new $400 million facility. The reason they're doing that is because you you can only get so much out of out of a traditional a fab, basically a fab plant.

They're closer to to silicon fabs, actually. Um and the largest lever that they have is in yield. So, how much can you get out of these things are they producing and also like what are the costs? Core of that comes down to literally how many of these um dynamic cell culture experiments can you run? And that's a process called media optimization. Uh and it ends up that that is that core that one problem uh ends up being connected to this to this half a trillion-dollar industry.

>> It's like uh if I So, to to to paraphrase, if I wanted to increase biologics manufacturing by an order of magnitude, at least my capacity to produce like antibodies and the like, I the the lever that is most easily pushed on and most like has the likelihood to give you the most uh like bang for your buck is media optimization.

>> It it is the most bang for your buck. You are unlikely to get 10x on on on that. Uh the current what what you what you're looking at is how much can I produce per unit time and then how consistent is that. Um and those you you if you can produce more per unit time, you get higher throughput for the entire for the entire kind of facility and then uh if you have more stability in the product for for biologics and for things that go in our bodies, that's a it's a desirable outcome.

>> And so my my conception of these bioreactors that are producing antibodies is you have a bunch of like CHO cells maybe sitting in a very large tank. They're sitting in a fluid of media and they're constantly just excreting out these antibodies that are later then purified. Um Yuku comes in at the step of deciding what media to actually put into this tank. Is that fair to say?

>> Correct, yeah.

>> What is Well, like my I've never worked in the wet lab before. My conception of media is that it is sugar water that all cells are generally fine with drinking up. I've learned that this is incorrect and I'd like to hear your take for what actually is media.

>> I would say that that is a very limited view of what media is, not incorrect in that if we were talking about media for growing yeast, sugar in water is pretty close to pretty close to sufficient. Um but the more powerful way of thinking about media is that it is a very high-dimensional control surface for what you can get cells to do, right? Like cellular communication comes through things in the in the in the media, right? The media actually is the communication channel in a sense between cells. Um it's also what uh you know, carries nutrients into the cells. Uh in mammalian cell culture it's closer to um serum uh in blood. So, it has it has either, you know, many many different types of like proteins in it. Um it'll have different uh you know, metabolites. It'll have salts.

It'll have um, and in defined media, it'll have buffers to keep the pH It's going It basically has a lot of components that and and there are hundreds of them really, you know, down to down to um things like magnesium. And each of these are really communicating and interacting with the cells. And they also work across different time periods. So, you'll have growth media, which is when you're building up the cells, and then there's there's media when you really just want them producing these particular things. And right now, um, if you if you buy or produce media internally, it tends to be connected to a particular um clone or particular cell line.

And so, you will optimize a media for that particular cell line, or you'll optimize media for um, if you're doing, you know, if you're growing but neurons. Um, and so, every it's it's complicated enough and important enough to the results that you get exploring it is like very valuable. Like, I know that there are a few companies that have popped up like claiming to have like redesigned cell lines to make them better at biologics manufacturing. Does that also demand a change in media? It can demand it The The key thing is that the biologics that we are producing now are becoming more complicated and that is making media optimization more difficult. So, you do tend to pair the cell line with a media line. Both both for um, like repeatability and ease of use.

Uh also just for for commercial reasons. Like that's that's a that's a better business. Um but you can you can the what really happens is you tend to to take a standard growth media or something off the shelf and then you will kind of customize it for this particular thing that you're trying to that you're that you're trying to make because ultimately productivity is really the interaction of these of these three things or three or four things. It's the cell line. It's the uh it's the media. It's the like process conditions or the the tank that you put it in and then the actual compound of interest and things things that you're

>> You um you mentioned earlier about like um media is both a way like nutrients for the cell but is also the substrate upon which they actually communicate with each other. That second part was surprising to me. I did not naturally conceptualize like like cells in a tank actually talking to each other while they're like turning out antibodies. Where are they communicating exactly? Like what's the Does that Does that question make sense?

>> So I I I I think it's maybe easier to think about it in um you know, the the sense of our bodies, right? So you know cells will send out, you know, or communicate through through different hormones, right? Those will get released. Um you know, there are small signaling molecules that get that get kind of like broadcast. Those are carried through the media. Well, it it In the body we call it, you know, blood serum, right? These things. But in the sense it's it's media.

>> Like um you mentioned also uh you have different stages of media that you want to introduce to the cells depending on the cells' actual life cycle. Is that also true? Does that like Is that also true for serum in the human body? Does the body constantly adjust its own sera to whatever the cells need? Okay.

>> Yeah. Yeah. I mean um that that is the way that cells differentiate.

>> Does it?

>> Yeah. In a way, yeah. Like um you know, you've got some gradient that will that will that will happen. And then that that gradient that which, you know, that's basically saying you've got different media. And there's that that gradient kind of tell can tell cells how to orient or can tell cells how to develop. Um There and the you know from stem cells triggering when, you know, what they're going to end up being. That's that's also, you know, basically it becomes it becomes media as you add things into the cell environment there. So.

>> Why what's stopping me from just replicating human sera for my mammalian cells? Like is that not the best substrate to use?

>> Well, the first question is where are you going to get it?

>> Oh, yeah. Yeah. Well, like I imagine uh you you could Actually, I guess this is a more basic question. Do we understand human sera well enough to perfectly replicate it? Hm. I don't know. Um what I will say and that's gets closer to what you were talking originally is is that's what we've been doing historically, but instead of using humans, which not that very limited supply um or or limited willing supply uh we've been using um fetal bovine serum. So, from cows. There are problems with that. Uh it is it's highly variable. And for all of biologics manufacturing uh the goal is reduce variability. And if one of your largest inputs is is variable, that's that's that's a problem. Um it's also a challenge because things like like you can't sterilize it in the traditional way.

You can you can filter it. Um but you can't like heat it up without destroying and things like prions, which could be quite bad. Uh you you you would need to prevent those coming in. So there's the the industry has really moved much towards um formulated medias. So you're you're building it up from the constituent parts. And that's that that also allows you to be, you know, it reduces variation and gives you a lot more control then over how are you particularly tuning that media.

>> When you say like at like at some point fetal bovine serum was being used,

>> Still. It's it's it's still in use. It's it's mainly in use in um in research, I think. I I'm I'm maybe there are some biologics manufacturers who are using fetal bovine serum. I don't know. Um but I I I think the industry has pretty much moved to

>> At this point, like would you consider that the the like synthetic serums that are attempting to recapitulate the biochemical properties of fetal bovine serum, the synthetic stuff is better? Or is it just like it's easier to get, so you're okay with not perfectly capturing fetal bovine serum?

>> I think it's better.

>> Okay. Okay.

>> better. And I think it's better in that you again get to get to tune it.

>> Yeah.

>> You get to tune it.

>> Okay. And so attempting to be more concrete about it, what is what is a media optimization engineer exactly doing? Let's say I have um a plate of CHO cells. I want to produce Keytruda, so pembro. Um I I have a bunch of cells. I have like uh all of them are willing to produce the drug. They they've been genetically edited to to do that. What's the next step?

>> So, the process in general is guess and check. So, you will uh take a uh a cell line that you've that you know, edited or or produced for this. Um most most of the time it's just and then you'll take it out from the from the freezer. You're going to grow it up a little bit. And then you will you'll probably take four or five of those because you you don't kind of know yet, right? Like which particular strain will do will do best.

>> So, you're trying with multiple strains at the

>> to try with multiple strains. Um and and then you will run experiments that allow you to First, you're going to run it in microtiter plates normally, right? And you're going to just see kind of where are we um where does it look which which of these cell lines kind of seems like it fits best with with these. After you've after and after you've kind of you know, narrowed it down, you're going to move to something that has more control. And the reason that you're going to move to something that has more control is that what happens in a microtiter plate is is extremely disconnected from what happens in any kind of production environment. And the core reason for that has to do with flow.

So, in a in a microtiter plate um you you get a lot of a lot of uh sort of like capillary issues, right? It changes the the you've got the surface tension kind of comes up. That changes the the gas exchange rates. Uh you get evaporation, um you you and you don't get any of the uh the different kind of like gradients or different little bits of shear forces, all these things that actually affect how cells how cells grow and large reaction. So, what you do is you you put it into what's called um a a benchtop bioreactor. And so, this is, you know, a little bit bigger than than um than a Fiji bottle in terms of what it'll what it'll contain. And it's got an impeller in there and it'll spin it around.

So, now you're going to now you're going to to grow those cells in that media for 10 days or something, right? And during that time, you're going to also uh change the or or control the the pH level that's in there. You're going to control the temperature. You're going to um you know, you'll you'll you'll set different um you know, impeller rates, you know, kind of seeing seeing what's what's optimal. And you're you're going to run that for you one person can maybe run 12 of those experiments, 15 of those experiments is is pretty laborious right now to actually set those up. Um it's going to run and during that time you're going to pull off some samples. You'll take those to uh uh the the analytic section.

Depending on how booked up that is, that could be, you know, 3 days to to a week sometimes to to get all of your answers there. And then you and so, you'll do that

>> And so, what questions are you asking at that point? Like what is the sample meant to answer?

>> Right. So, ultimately, your your sample is meant to answer uh how much total biologic do we do we did we produce in here? Uh at what quality, right? And then and then you're the the The question there is like, you know, how overall like how consistent is it? Will it be? That that's actually a large sort of hidden cost is as I said like the best way to think about biologics manufacturing is to think about it as high precision manufacturing uh and closer to to to semiconductor manufacturing. That's really the reason why like Samsung Biologics is is in the position that they are is because they took what they learned in terms of process control and brought it over.

The reason that Fujifilm is a large manufacturer is because they took chemical process engineering and they they brought it over. These were not biological companies, right? They they are they are industrial manufacturing companies and when you when you think about reducing process variability one way of looking at that is is just you know, how how precise is the is the part that comes comes out kind of but then what makes makes up that right is like you know, basically how how much variation can we absorb without it affecting the end product? And so if you can come up with media and process conditions that are kind of more forgiving you're relaxing it a a bit, right?

It's like you can still end up with something that's very precise at the end but oh, we we didn't actually need as much we were kind of more forgiving over over here and that's that can be important because you know, if you lose a batch of biologics it's very expensive. And and that can't happen and it does happen and so the way the way to reduce that is through is is there's media optimization and so to finish to finish on this you you've run that set of experiments, you've got your readout there. Um and and you know, those readouts, although those are like the most important, you're you're also going to, um, you know, characterize kind of everything in there that you can because you want to see how those are affecting that that natural readout. Then you will repeat this.

And depending on how much time you have, um, maybe you will get three or or four kind of runs of that, and then that's it. Uh, and that that comes down for for biologics manufacturing to, you know, the the regulatory reasons.

>> How much of like, um, would you decide are like the optimal cell lines and the optimum optimal media? It's like there is like a threshold of quality you you want to meet and after that you're done versus you are trying to make this as like perfect as possible. Was it kind of dependent on what drug you were trying to produce?

>> I I think the goal is match what was in the phase three trials. So so uh, in the process of taking a drug to market, um, during your your your phase three trials, the batch that you produced there, that is what all of the all of the the FDA's kind of evaluation was based on. So they want to keep that as the same. So anything that deviates from that is undesirable.

>> Is this true even when the drug gets to the generics? Like it gets uh, like off balance and do the generic manufacturers, are they trying to make it even through they're trying to improve the process even more or even for them they're trying to replicate exactly what went on for the original or with the original company?

>> That's a great question. I should I should look into that because now truly because the I they do have to go through them so they have a couple options. The first thing is that they will basically just license the the cell and and the media from from the existing pharma company, right? Pay them for that. And then that that way the pharma company can still get some get some revenue from that. Uh the alternative is they need to come up with their own come up with their own cell and and do this. I I think the regulations are such that there's a way of I think it's like they can prove if you can prove that it's similar enough at all. Then it will it just counts as like a process change.

>> Mhm. The uh getting back to the question of actual media optimization like the the the media optimization person goes to the analytical chemist, the chemist tells you tells you like all you need to know about the samples that you've been given. You repeat this six to five times. What are all like the the levers of change that you have over the media?

>> So media is best thought of as this control surface for affecting what the cells are cells are doing. So what are the levers in there? Um you can you can change the components and then you can change concentration of those components and then you can change timing of those of those things. And if you start with, you know, 200 or more, let's start with 200 components that you can put in there. And then the different concentrations that they come in, and then the timing, that already is like a of quite a large space to explore. Then you have that interacting with the cell and the different cell lines. Larger space. And then with the with that um with that fixed compound that you're that you're looking for.

So, the you know, standard things that people are going to are going to change or tune in there, right, is uh when is a carbon source coming in, you know, and and when. Um what what's uh what as you start producing different proteins, the needs of the cell change. So, if you if you shift into a different mode for the cell, you can you can kind of signal it to shift into a different mode. Starts producing these other all of a sudden its needs change.

>> Mhm.

>> And being able to like anticipate, offer, and meet those meet those needs, that then has a lot to a lot to do with the the output.

>> How much of the uh how much of the optimization, like even the direction or specifics of the optimization, can be like theoretically known and applied versus just always empirically determined? I I guess like the more specific question I'm asking is like does a media engineer a media optimization engineer are they coming to every new problem almost like tabula rasa? They have like like whatever experience they had in the past does not apply to this new new cell line with this new drug. So, the the question of like how tractable is this of a of a problem and what's the current what's the current state of the art. Um the current state of the art is that you know, things best practices live in the in the mind of the practitioners.

And a lot of that comes down to, you know, familiarity with that with that cell line, familiarity with the media that you have, and most you know, manufacturers are working in a particular kind of domain or specialty, right? And so, as you're constraining that search space, it it does make it easier to to to operate in there. However, uh it is not the case that you will one shot it coming through. And then the second thing is it's it's actually uh reasonably easy to get caught in like a local local maxima. And if you don't if if if the cost of running those experiments or experiments themselves are sort of precious, um you're you're really not going to to to push very far out. The lever they currently use is mainly in strain engineering.

And so, they'll try to to to, you know, uh select strains that'll have the highest performance. Um but once once once those are are set or those those cells that you're that you're using right there, it it does all come down to the down to the media. For for optimization, um in a in a model sense, it it does seem that it's it's tractable. It does seem like there are that there's transfer learning. Um you know, how broad of that really comes down to what experiments have we been able to feed things so far under these models. And the And the answer is is not very many. Like Like the the largest the largest facility that I know of um, for running sort of like dynamic cell culture experiments. You know, they can run like 300 in parallel at any given time.

>> 300. And that's like that's the entire company is just doing that. So, that's like that's the state of the art or like that's that's kind of where it is. And a lot of that comes out back to the the fact that it's so manual.

>> Mhm. The The The The One last question I have before before we move on to how how Eku is fixing this is um I can understand being able to easily modify like concentration of the media. I understand being able to modify the timing of when which or when you're giving which media to the cell line. The the components the consis- considering components feels a lot more complicated cuz I that's like 200 components. How much of that is like in practice there's like 10 of them you modify at any given time and the other 190 are like pretty standard and all the cell lines will need this.

>> Yeah, so how how much is like what's what's what's the core? Is there some um Is there some dimensionality reduction?

>> Yeah, like is there an 80/20 thing going on? Oh, yeah.

>> Absolutely. Absolutely. Um, which which as I said like, you know, the the you glucose your your your sugar source or carbon source um energy uh the the the pH that you're running at um those those are Yeah, there's there's there there probably are 10 that are dominating it. But, that's why it's actually um that why it's so challenging is because there are 10 that are dominating. But, because the system that we're controlling is quite non-linear, uh it can amplify what are sometimes in certain conditions some some small change. And my my favorite example of this is that is that literally just like change it turned out it this was in um industrial manufacturing, but like changing the amount just changing the amount of magnesium at a particular point like doubled the output.

A- And it didn't necessarily need it there was no like a priori way of knowing like oh it would have been magnesium that like went in here. And you can say oh okay well sure like that's a lever and we should do that on each of these. But, the problem is that potential exists for all of those other 190 things or all those other things, right? So, it's like sure there are these core things that tend to like dominate like you know if

>> But, those 10 things could vary based on what the problem actually is.

>> Yeah. W- well well those those like the core things of like you do need to you know um you know the the salts that are in there, right? And the um and and what you know when when energy comes into the system those are definitely floor level you have to figure those out for it. Okay. But, then and and if you get those wrong basically like those are those are controlling kind of the um what where the where the floor is. So, if you get those if you get those wrong kind of doesn't matter what you do in these other areas. You're you're not going to you're not going to have high performance. But, just because you get those right doesn't mean that you have high performance at all. It's like they're they're just like those are table stakes. You need to you need to get those done.

>> That makes sense. Um and so like we we mentioned this engineer who's trying to produce Keytruda.

>> Sure.

>> Uh they're they're evidently building at like at the very beginning building in a Fiji-shaped

>> Yeah.

>> uh bioreactor

>> Yeah.

>> doing these rounds of iteration trying to get to something good. What is what is Eku's proposal for what's the better way to do it?

>> Our proposal is um to rethink what it is that you're trying to do when you run that experiment. So that Fiji bottle device gets used for two kind of purposes. One of which is like you you want to grow cells and you want to grow them uh to feed a seed train. So you're you're growing them in the Fiji. Or you you need like that quantity of those cells. That's one. And the second is that you need information and you need to be able to control the environment that the cells are in over time in order to get it. And so for this first this first set of things where you're trying to grow a lot of cells or grow them up, great. Perfect perfect use for it. If you're trying to extract the most amount of information and try to control the cells, it's a very limited way of doing it.

Um before you starting on on any of this, I I'd actually seen some of these benchtop reactors and and I asked them like if the thesis is that it gets better when you go smaller, why did you why did you stop at the at the Fiji bottle? And the answer was well, if we go any smaller, our sensors won't fit. And it's because they're they're using off-the-shelf sensors. And if you ever see a photo of these things, it's a hodgepodge of different things that have been kind of like crammed in there. And then there literally is like um they doing sensor design is its own it's its own field. And you need to design not just one type of sensor, you need to design many different types of sensors.

Uh and there's also not that much of a There's not that much of a benefit going from, you know, a Fiji bottle to half a Fiji bottle in size because of of the manual labor and all these things. So, our solution is to think about what's actually the best platform for building sensors. And then can you put cells inside of it? my my last company was a robotics company. Um we you know, any of the humanoids now that you that you see going on, um I'm highly skeptical of the economics of these things, but any of the humanoids that you that you are in the the core technology that enables them to like move, interact with the environment, those are what we built. And that is a sensor problem and it's a sensor in a high noise environment.

And that is abstractly quite close to what we're doing in in biology, right? Um the So, the the idea is if you have a good place for building and placing sensors of different types around, now you reduce the problem. And so, easy place to build sensors, now you just have to figure out how to put more cells inside of it and keep them keep them alive. And if you pick a uh a mass manufacturable technique for doing that, it also solves some of the scaling problems because the the challenge with controllable systems right now is that they still require they still literally require somebody to come over, unhook everything, you know, set it up. You you can use disposables to sort of take that down a bit.

But it it it also takes when you go larger, it takes more media, it takes it's more expensive to run it. Um it's less repeatable. Uh there like none of it makes sense except for it's a difficult engineering problem.

>> In in in like a practical sense, like I I can buy that I would like this this form factor was chosen purely because our sensors are not small enough to fit in something smaller. What is the form factor that you guys have?

>> So, the core differentiator is that we are reusing um printed circuit boards, which are ubiquitous. They are um in your phone, they're in your microwave. Um and we put microfluidic channels inside of them. And by doing that, it allows you to then have cells live live inside they can pass through, they can live inside there. Um and it turns out that making microfluidics previously that that integrate those types of sensors is extremely awkward. And so, you either don't do it or if you do do it, it's still hand-finished. And so, the big differentiator is we're everything comes straight from the fabricator ready to go. And this is this is a uh this is a like a a theme that has happened before.

So, in like silicon photonics, which is where you take existing silicon fabs, and you say, "Hey, can we use this in a in a new way?" And not to just do like integrated circuits, but can we um can we can we now do do things with light in it? Um or uh you know, the in your in your iPhone, the has like a lidar detector. That was like a new way of of using that. And the the core there is that um the the process that's used is called lithography, which is where um you'll you'll take a mask kind of like a snowflake, you project light down through that or something, and that cause certain things to react and certain things not. And lithography is a really powerful manufacturing technique because you get complexity for free.

What that means is normally, if you're doing like traditional subtractive manufacturing, you as your part gets like more complex, you've got more nooks and crannies in here, it takes more time to make it. Um or you've got more tool changes or all these things. But with lithography, you're you pay that cost once. You pay that cost when you when you make your snowflake. But it actually doesn't matter how complicated you make the snowflake for for it's down here. And so it pushes you to say like, what's the most complicated thing we can make here that has the most value because it literally costs the same. Doesn't matter if if it's one line through here or some complicated maze. So, that's what, you know, semiconductors are doing. Then they apply that to to to photonics, right? Lidar.

Printed circuit boards are made the same way. It's it's lithography. And if you can leverage that in more complicated ways, you you start both enabling capabilities that weren't possible before, and also uh are are riding like a cost curve that's really that's really beneficial. Um so, the the idea is like every time that we have found as a society a new use for lithography like large industries get built off of that.

>> And sorry, so where is the lithography component coming in when you talk about like building a new bioreactor?

>> So the way that we make our chips

>> Which you have

>> Right, yeah, yeah. That's let's let's Do we?

>> Oh man, they're They're They're They're comes out pretty small. Okay.

>> Yeah, look.

>> Yeah. Uh Okay, so I I am seeing that there yeah, there's a there's a bunch of uh like circuits um coming out from here. Where like like walk me through the anatomy of this device.

>> So So the first thing is that uh it it looks it looks kind of cohesive but it it's actually six layers. And each each layer either is carrying electrical signals or fluidics or you know, routing fluidics in there. And so for this for this particular chip uh it has a channel that's uh a a millimeter wide and a hundred about the size of a human hair um tall. And that's actually like a great size for cells. Uh and you can flow uh media with cells into it and then it has all of the components that uh sort of like a benchtop bioreactor or a more controllable system would have. And the way that you the way that you make these is through lithography.

So these lines and all of the features that are on here there's there's a snowflake kind of pattern that's made for that and then they will they will put what's called a resist and an etch on and so it will kind of keep those lines where you want them and etch away everything else and then you make the next layer And then you make the next layer. And then you And then you compress all of those together. And so, the the the way to think about it is it's like a 2.5D space. So, you've got two-dimensional plane, but you've got multiple two-dimensional planes. And so, uh topologically, that's going to allow you to uh like do things like take a spiral, and get to the middle, and you need to get out of it. And so, you can come up and out and in a way and round.

And it And it also allows you to um to put uh electrodes or different sensors in relation to the fluid, in relation to the cells, in different places. And that's kind of abstract, but but let me give you a very concrete example, which would be um if you want to have a readout of electrical signals of like heart cells, cardiomyocytes, uh you you want to read like across the cells. Well, you you need to be able to put uh you need to be able to put electrodes above and below them. Normally, right? Or you can put them side to side, right? If you're trying to trying to do these things. That's like a primitive. Like that is a really It sounds very simple. And yet, I will tell you that is with other techniques a difficult thing to do.

And so, by switching to this to this new substrate, um a a whole class of problems that are traditionally quite difficult become become substantially easier.

>> And sorry, I I don't have a great conception of like Where do the cells like like on on this on this like uh

>> Sure.

>> green thing? Like Are those like holes? Like where are you putting the

>> It is It is It is really It is You know, and actually, I have a drawing I should send you. You can put up a drawing. Because that that is that is also part of the problem is that from the outside, it literally looks the same as any printed circuit board. Second thing is in biotech, a printed circuit board looks like alien technology. Okay. Um but yeah, in it has actually small holes. There are there are ways of getting fluids into the into the actual device, and then you can you can run them past sensors, or you can you can run um it's it's often easier to run the the fluid past the cells, and then you're kind of reading things out on the out on the fluid.

>> And so there's not like a specific chamber here where the cells sit. They they they are literally like lined like in a line formation as you run fluids through them.

>> In this particular chip, um in this particular chip is like a year old. Uh you know, in in in newer designs, uh you you have more like a a chamber.

>> Okay.

>> And you're you're kind of seed that chamber, and then your cells are are growing over it. Um but the powerful thing about using this technique for for making microfluidics is that um you can make a large number of variations. And it's that's a difficult problem in traditional microfluidics because you would need to make new molds. And and a new mold is, you know, $25,000 or something, $40,000. You need to get uh a mold maker to come in and and machine it. Your economics on that mean that you need to make a lot of them. With printed circuit boards, it's it's easier to make variations to them, and then just just do that.

So we have we have kind of uh a core catalog that we're building of these are the the designs for particular applications, um but every new printing, it's relatively easy to to change it to whatever the condition is. Sorry, I Is it Is it fair to say that typically microfluidics are not built using lithography, but you are building them with with lithography? Microfluidics historically started with lithography. So, they started with lithography. Um they were built using similar techniques and they used for semiconductors and in in most research labs, when people build microfluidics, that's still the way it's done. Um what what you'll do is you will you will make a silicon uh mold and then you cast a polymer over it. This polymer is called PDMS.

And the desirable properties of it is that it's it's uh you you optically not transparent, but you can you can at least see into it. And it's gas permeable. And so, that allows you to uh have ex- exchange gases without um it's like you can put it in an incubator. You can use it there. Downside of that is you can also get evaporation. Um the the problems with with with that is you end up with a um a kind of a fragile output. And it's also fairly still fairly labor-intensive to to do it. The But, people like it because you can do it, you know, in your own in your own lab. The difference comes down to uh the use of lithography for sensors and fluidic channels together in this in this thing. And and critically for uh for silicon fabs, you need to be really careful about contaminants.

So, if you need, for example, like a gold plated electrode, you cannot do that in a silicon fab because you will contaminate the the fab. So, not allowed at all, very bad. Um So, with the printed circuit board as a as a medium, basically, you can integrate many more different types of sensor modalities than are sort of possible with with silicon. Uh and then and then the second thing is just on a um like the the reason to use silicon is because you want extremely fine features and detail. There there you once once you once you need something on the, you know, nanometer scale, it's kind of the only kind of the only option. Um but our thesis is that cells themselves are more on the on the, you know, five micron scale, which is few orders of magnitude difference.

>> Yeah.

>> And that's that's actually the the domain where printed circuit boards are a better place.

>> Is there like So, if historically people do use lithography for microfluidics, but they only use it for like the channels and not the actual electronics, what like where like what innovation allowed you to actually include electronics in the design of the microfluidic?

>> Yeah. So, let me let me state that um so, microfluidics is like a broad term. Uh for example, you know, DNA sequencing, you know, Illumina, right? Like, that's that's that's using silicon for um like for microfluidic system and doing and doing, you know, sensors. Um it's it's a really it's a really useful place for doing that, but it has limitations in terms of where where in space you can place things. Um Uh the example I gave earlier about trying to read across these cardiomyocytes, you can't do that with silicon. There's no there's no there's there's no kind of way to build a channel that size that you need for the cells to go through it, but it's buried and you have electrodes above and below it's just like it doesn't is you just can't make it that way.

So, the core the core innovation is is is first of all just conceptual conceptually thinking about printed circuit boards as a media for making as like a medium for making microfluidics.

>> Mhm.

>> Um I I been working with circuit boards for 10 years or something. Never occurred to me to put fluidics into them. Um been talking to people about this for 3 years. Never met anybody who was like, "Oh, yeah. Like, I've I've seen that before."

>> So, like as of today, there's no one combining circuit boards with microfluidics.

>> For if not for there there is for diagnostics.

>> Oh, okay.

>> Yeah. So, um the professor Despina Hashu at um the University of Bath, she's really like the pioneer of um of putting fluid of putting fluids into the reward from the fabricator. And the reason like that's so important that I keep coming back to it is uh you you can do a lot of things and academics are prone to this. You can do a lot of things by hand. That that does not scale if you need to make hundreds of thousands or a million of things, right? You If you're doing that, you need to pick something that is mass manufacturable. So in terms of, you know, cost and complexity you know, the the cheapest thing to to mass manufacture for for microfluidics a size like paper or um or or molded things when you build a lot of it.

Uh but if you So if you if you try to make microfluidics in a PCB in a lab, you know, you can do all kinds of of of weird things. Getting it to so that it's compatible with the standard fabrication process that's a different that's a different ask both because they're they're not they're not terribly keen on changing their processes for the most part. Um but then the second thing is that when you do it by hand you're introducing variability from the beginning. When you have it done in a fabricator, you're inheriting the like hundreds of billions of dollars that have been spent cumulatively on like printed circuit board development. Like it's been around for 60 years. Like entire industries are built upon it being already very good.

So let's just reuse that thing that's already quite good and low variability. Could you give me some intuition as to like how the device is actually put together? So, okay, like I my my misconception of lithography is like, yeah, you're you're you're able to create these like very fine channels in the silicon via like like shining light through a mask. Um what's the next step after that? Like maybe you do this on multiple layers. Um do you have like this multi-layered system of just like like channeled almost.

>> Yeah. So, for um traditional silicon fabrication, it really is like it's a mask and then you etch and then it's a mask and you etch and then it's a mask and you etch. Um with printed circuit boards, it's more like each each layer can be made out of different materials. So, this is where like there's an enormous amount of flexibility in terms of um it's like a it's like a it's a much richer palette to to start building out of. Uh so, the foundation is is what's called FR4, which is um a fiberglass structure. It's why they're normally green.

Uh it's this fiberglass structure and on top of it is it'll come coated in a in a layer of copper, layer of copper on the bottom, and that is the the simplest circuit board that you will that you will buy, the cheapest one, is is just that and it's just been etched. And then they will put down what's called um uh like basically protective layer on it. Um so, that's that you don't kind of just like scratch off the scratch off the copper. And then you'll silkscreen it, which is if you want to, you know, put labelings and and all these things. But that at its core, like that's that's what that's what the process is. When you add in microfluidics, you there are techniques for being able to make the fluidic channels on one layer.

As you need, you can just kind of like stack on another layer, and then that layer has fluid or in between them. Now, you can you can route like your your heaters, right? You know, you need to put your heaters there. Or um you know, if you if you want to put the um you know, electrodes or uh or um whatever your whatever your kind of like uh end sensor is, you can you'll pattern that on that layer, and then you sort of build it up. And then and then you kind of stack them together, you close it, and then

>> So, okay, so like like in in feature of this device, you have this chamber where the cells live.

>> Mhm.

>> Um you have microfluidics connecting this internal chamber, um maybe it's external, uh to like a bunch of pipes that like like feed in um like some some particular access of variation that you want to control during the media optimization process. And you also have like embedded or maybe external sensors that are connected to the circuit board to have some sort of readout of what's going on in this uh chamber where the cells live as the media is being applied, and like what's the output? Um what what do you actually What is the output of of the system? I like I imagine like one is maybe temperature, um maybe another is internal humidity. What what other axes are there that you can actually get straight off the sensor and straight off the device?

>> Um so, the the way to think about it is that if you're going to do any kind of cell culture, there are a set of table stakes that you that you sort of need to be able to to do in there. And those are those are temperature, pH, and dissolved oxygen. Um or or flow things through, so you need to be able to measure flow rate. Um and those those together, that's that's the that's the core set of things that were that our system is currently like reading from. The next layer are the like electrochemical sensors. So, um being able to read impedance is is actually very useful. Uh if you can read impedance for the media itself, you can you can detect some changes in in how the media is is adopting.

And if you place them in relation to the cells, you can also uh correlate cell growth with with this impedance, which is based on the um kind of like based on on how these charges sort of end up hitting against the cell walls at different at different frequencies. Uh so like that's a that's a that's like a core thing there. You can do conductivity through it, which is partially used for offsetting um where where the impedance reading is coming from because it can the impedance can sort of get um it can get interfered with in a lot of ways. And so you sort of like need a reference point in order to in order to do that. Um and then and then you can you can do other electrochemical techniques um like cyclic voltammetry.

Um but the the the the readouts right now are the impedance, the flow, dissolved oxygen, pH, and um and and temperature.

>> Theoretically, I imagine like all all of these sensors already had miniaturized versions of them available. Is that is that true not true?

>> Not the case. Uh it There are So nothing nothing that that that our system can do at the moment is anything that you couldn't have done by hand or with a very a very custom setup. The challenge is how do you do more than two of those three of those at at a time? How do you build them you know economically? Uh for for example like the the chip that I showed you it in any kind of reasonable quantities it's like $4 or something $3. And and and that's actually it's still

>> even you you can you can get it down to like less than less than a dollar on that. So if if you're buying sensors off the shelf that's not the economics are going to start killing you very quickly. And then the the second thing is it's it's a challenge to integrate those those things. So you know a big idea in in in robotics or or engineering any kind of real system is that interfaces and connectors are or what will kill you. Um they're very common points of failure. So the best solution is like no connectors. Uh when you build sensors all in the same platform you essentially get to do it with no connectors. Um So that's the like the the trade-off is hard more difficult engineering from the outset but lower lower variability and better economics at the the outset.

>> I imagine the like you get like dissolved oxygen pH and a few of these other parameters. I imagine like there's still there's still some you're missing in the sense of like uh like is the protein that I'm expecting to be produced is actually being produced? Uh uh So like it it sounds like you're you're cutting you're allowed to optimize to a threshold and then after that you need the analytical chemist to come back and and like do their thing. So our our our goal

>> is to make is to make the analytical chemist kind of a a confirmation rather than be limited by and the reason the reason comes down to um sort of lessons from control theory. So the first is that any any system that you're trying to control in this case cells if they if they move at a certain rate or certain speed and you want to be able to dampen that or amplify it, right? You need to be able to read it fast enough that you can come in and make an intervention. Anytime that you take a sample of something um and do an offline measurement that that that loop is normally too long, right? Sometimes sometimes that loop is you know five minutes or two minutes. Okay, maybe you can work with that. If you if you need to take something to your analytical chemist it's probably hours or days.

That that that information is not useful to you in the actual control of the culture, right? So what you want are real-time sensors. You want you want sensors that are truly like integrated into the thing. For these these the sensors that we're using now that that really is just the table stakes to enable us to start building in these other sensors. If if you don't have those core sensors, you can't even keep the cells alive. You can't like there's just no point. But things being able to have live readouts of um of like monoclonal antibodies, that is what we're building towards in the in the device. It's being able to have the optical sensors built in.

Um it's it's being able to leverage the uh sort of biological techniques or or or chemical biology techniques that we have right now for getting signals out of out of cells. All of those are like compatible with with our system. And that's what that's where I think like the real value starts starts becoming unlocked because there's there's a a large difference between like sort of philosophically between just reducing the cost of something versus what what questions become askable now. And the the questions that become askable and sort of like experiments that you could run. That's what I think is so powerful about about using this substrate as a as a technique is like okay you you make this core thing, can you grow cells like in high throughput in this dynamic way?

Okay, once you have that, every new sensor system you put in um gives you more lenses into it. And this comes back to why lithography is so powerful is that normally you have to make a trade-off. Right? Normally you're like uh every new every sensor I put in it costs me money. And so I'm only going to put in the sensors that I that I need here. But if it doesn't cost us any more or if it's basically trivial, then the idea is actually let's just instrument it. Let's just keep instrumenting it. And and and classically you'd say like, well, um I don't really care about those those features and those things those things don't matter. But what we're what we're moving towards is more of the of having fewer priors and having less human interpretation on the streams of data that are coming in.

And so for example, um you know, like the impedance sensing does not give you a simple number that comes out. Um it's a complex number that comes out. Okay, whatever you could you could still deal with that. But then there's a complex number across hundreds of frequencies. So you you're getting back this this this large data. All right. Um and then it's changing over time. So if you and I try to decode that, it it can it can be difficult, right? And we we can argue about this. But you know, machine learning is getting pretty good, arguably quite good at handling those types of things. And so the the way the way that I separate these two way we're separating these two is there are what are called narrow band sensors and then there are broad band sensors.

So a narrow band sensor is for example like read out on temperature. You you're going to resolve that to some either resistor variable or some, you know, temp or some, you know, um on some basis like like, you know, Celsius. And you want that to pretty much just just respond to temperature, not respond to anything else, okay, very easy thing to interpret. Um same way with uh your your lactate. That's that's that's in me. You want something that only responds to the lactate in the media, nothing coming out. These are narrow band sensors, they're meant to reject kind of everything else. And then there are there are what I'm going to call these wider band sensors, which is, you know, if you take a microscope and put it on something, it's a fairly wide band, right?

It's like it's a lot of stuff going going on in there. Um there's not kind of just like one answer about what's what's what's going on here. And you can sort of select like, oh, I think these things are more relevant to the questions I'm asking or not. And things like optical the impedance, um some of these other electrochemical techniques, um the the magnetic fields that are that are in there. Having when you have machine learning on the other end to interpret that, it would be it would be surprising to me that you would not that that's not useful.

>> This is maybe a naive question, but at the end of the day, all the all the signal you're able to extract from like this device is going to be some like electrical property of the of like the cell of like the tiny little bioreactor you have in there. Is that correct?

>> No, we're we're the the the the big picture is that we're integrating all of these different modalities. So, we're integrating the optical modality. We are, you know, my my my dream here is to get like Raman sensing into the into multiplexing Raman sensing across this, right? For having for having that method of of looking at it. Um it's it's having those with the the lactate and the glucose and the um you know, your your monoclonal antibody sort of like read out, right? Or what whatever those domains are. In in in an instrument sense, that's extremely that's extremely powerful. So, that's that's that's the goal.

>> Okay, interesting. The the um I imagine some of these some of these variables, like you mentioned, are like immediately interpretable. There's like a good value you should be reaching. Actually, like dissolved oxygen is one of those. Um for the more complicated ones where it's like you don't know whether this is a good value or bad value, like glucose or some other some other um uh mineral, where does like the ground truth come in? Is that where the analytical chemist comes in? Like they give one singular data points like what's good and then you the purpose of the system is like correlate everything that you put into the system and like all these output variables you got out to that ground truth or something else?

>> So, I I think a useful lens for this is um What's his name? Richard Hubbings? Uh is from book called How to Measure Anything. Highly recommend this book. Book changed my life. Uh and the idea is the expected value of perfect information. And it's that any reduction in in in uncertainty has some cost to it. And so, when we're when we're taking a measurement, there's an economic aspect to that. And therefore, a trade-off. So, uh you know, knowing the knowing the the temperature of this room there's not much value to us, right? Doesn't matter whether we're off 5°, you know, or 0.1°. Um for for uh semiconductor manufacturing, matters quite a lot, right? You need really really tight tight value there.

So, if you take that lens and you say certainly at the certainly like overall there's a need to there's a need to have precision on the readouts of like how much you know antibody do we get out of this and you know the the quality of that right? But earlier parts of the process like do you do you need that level of precision?

>> Well, I guess like at the end of the day I imagine like the whole purpose of the process is to get to anybody production. But I guess like or is like part of what you're saying that there earlier intermediate benchmarks you want to hit before you get to the antibody. Okay, okay.

>> What what what I'm what I'm saying is that um your ultimate your ultimate readout right is like yield tighter you know quality and and stability over these things. Those are the things you you care about and and pretty much in that in that order. Okay. Even on the even on the yield though you're still going to get there's still variation inherent in cells right? Every batch you run even though they're trying to reduce variability you're you're still going to get some you know variation in there. So if if if you take a sample and you learn to two decimal points you know the the the tighter that came out of that the yield that came out of that. Okay, great. But like your process variability is is you know like 1% anyway or something 2% anyway.

So knowing it to three decimal places doesn't really help you. And then the second part of it is like if you can cut down on the number of like if every measurement has a cost in in some sense can you change your measurement system such that you get the information that you need in a more economical way and part of the way of doing that is by loosening constraints when possible. So, ultimately, certainly, you still need like you you still are going to run um you're you're still going to run on your benchtop and your pilot things, and you are going to characterize it there, right? Because you do need like ground truth from those things. But, in terms of which is the right the right media or conditions to get to in there? Uh okay.

Do you do you do you do you do you need Do you need to decimal points of accuracy on that? Do you need all of those readouts to do it? Uh I No.

>> Is a good way of thinking about this is like you start with the EQ device at at the very beginning, and then once you're happy with what you see, then you move on to the benchtop device, get like allowing you to like narrow your search space down to like very small number of parameters.

>> Right. It would it would basically be like you're you're still going to you're still going to you're still going to end up The process looks pretty much the same. The difference is what is the the quality and speed that you came to that to that What What's the quality of the answer you came to? What's the speed that you came to it? And then And then the second part is how many of those um benchtop experiments did you did you need to run? Because there's a difference between running them in an exploratory sense versus running them in a validation sense, right? In a validation sense, you're just trying to make sure that things are like repeatable. So, you need to run, you know, let's let's say three to five, you know, copies of it or something.

Um but if you've if you've already if you're already quite confident that you're um that you're that you're at the optimal point, there's it's like doesn't make sense to do the experiment that sort of experimentation there anymore. Moving on to So like okay, you you've done the EQ optimization, and now it's time to like move on to the bigger things. How worried are you that like moving the cells to a physically larger space forces the media optimization to like move into completely different direction?

>> It's it's it's definitely possible and every uh every time that you change um physical you know, shape and and geometry, right? You you you do get some you do get some some variation there. The confidence comes from understanding that uh fir- first of all, empirically every microfluidic system that has flow integrated into it um ends up correlating quite well with the with larger system. The The reason that people have hesitation about it is because they think about microfluidics that doesn't have flow and the the recirculation effect. And that's actually the the key thing, right? It's a question of like, do you have flow in the thing or not? And how does that flow and those shear forces and the um the oxygen, you know, transfer rates and the the gradients that you create, right?

Like how are those representative at all what's going on here? So So that's that's one part of it. But let's say you don't buy any of that. The the the easier way is that it actually decomposes into two um two broad parts. There are uh parameters that change with scale. So these are things like your hydrostatic pressure definitely changes with with scale, right? You're not getting away from that. Um certain certain mixing times, you know, these change. Um you know, you can get pockets in in very large reactors, right? These these these change. But then there are a set of parameters that empirically don't seem to be scale invariant. And for the most part, media optimization seems to be scale invariant.

>> Do you imagine like in the ideal setting that this is a closed-loop system that just continuously tries different media optimization parameters, feeds it all into a model, and plans the next round of media optimization that that just goes in a loop.

>> Yeah. So, how does the um like aside from running the experiments, how do you actually interpret and decide what to what to So, clearly the entire you know, the zeitgeist right now is about replacing the control layer with with AI and and models. And whether you can do that on experimental design from reading a bunch of papers and then this is the the thing I'm going to build. I'm less convinced that that's necessarily the the best way, but for these for these types of experiments, certainly seems the way.

>> Uh

>> It's actually key for making the whole product because otherwise you're handed so much information back that the the problem then shifts to like processing it. So, one of the one of the lessons that I've that I've taken from talking to people who have tried um things in media optimization, tried doing cloud labs, or doing these things, is there's there's a lot of hesitation around um you know, sharing cell lines. Understandable. And it also comes down to information about what the um like what the result of those those cell lines are. So, like for for example, um like a company that was running experiments externally was not allowed to look at the at the results of some of these of these analysis. That was like in their contract that they're not allowed to actually look at the results.

Okay. So, it's really hard to improve or build your own model if you cannot look at the results. What what we're building is a federated model that allows the customers on-site to run the device. They can pull the model get a new experiment design that runs in there. And then the model weights are updated, right? This is the same way that the the the Tesla, you know, self-driving was was trained, right? Federated learning, you know, resolves that that IP sharing complaint uh or constraint. And the the reason that's so powerful is that now you have a model that is learning from diverse experiments across different cell lines um at different at different places, but still on the same hardware.

That's really key because otherwise there's too much experimental variability in the in the data you're getting back, and so you're you're not going to generalize well on that. Um and the the sort of hedged bet here is that if if if it's not tractable through machine learning and models. Um, we're still building the uh, high throughput, most economic way and fastest fastest way to get to that answer through still running experiments. And if it is tradable, we're going to have the best model for running those running those experiments. And I I think the answer is actually going to be a blend of a blend of both. I I do not believe that like experimentation is is going away. Um, but I do think that we will be able to get to much better much better answers much faster.

Because that's really the ideal, right? Like the the ideal is, um, you just you can then if you have if you once you have that model, now you can feed it in even earlier in the process, right? When you're doing your strain engineering. So, coupling those together becomes possible once you once you have once you have a model.

>> What parameters does a model actually intake and sort of like I imagine like it'll take in all the inputs you give into the system, all the outputs you get out of the system, and maybe what the system is actually meant to produce and the strain itself. Is that everything or is there are there others?

>> That's that's I think that's a complete Okay, I think that's a complete complete view.

>> If the if the belief is that like, "Oh, you'll probably still need human experimentation to help the system along and maybe the ML won't won't fix everything zero shot." Um, like can can I conceptualize this as like like like there are 10x media optimization engineers and they they will like they'll be able to iterate much faster on this model system as a result of that or do you imagine media like bioprocess engineering is a pretty standardized field where these are the first 10,000 things you try and maybe like in the old world you get to try like 5% of that and in the new world, you try those the 1,000 things, but ultimately the the it's the same set of parameters that you're tuning that the media optimization engineer is tuning.

>> Yeah. Uh so are are we tuning a different like a a larger set of things rather than the rather than just the the engineer?

>> Yeah. Yeah, like how like um I guess specifically like all the knobs that the engineer usually gets to tune, do they also get to tune in the system or is it a subset or maybe even larger?

>> It's it's a superset.

>> Superset. Okay. Okay.

>> You're you're getting to tune far far more. You're And And it's a superset in a few different sentences. Um the the first is that like just bringing the economics down, making it automatic allows you to to even if you had the capability previously to change a variable, you you you wouldn't be able to to kind of you wouldn't have essentially have the budget or the time budget or the or the the capital budget, right, to to actually exploit it. That's one sense. The second is that um it allows you to make finer interventions. Um you know, and with more with more feedback built in. So, the reason for having the the real-time sensors, why it's important, is like what what you actually want to do is be able to anticipate what the cell wants before it needs it.

Because there's always a delay between when something gets introduced into the environment to when it gets up to the cell, right? So, like ideally actually want to see that see those signals happening before they before the the cell needs it. Now, for in order to do that, you need real-time sensors that are that are kind of like picking up on that and starting starting to match that. So, that's so that's like that's a domain that's just like not kind of possible in in other systems.

>> The I'm curious about I assume there are microfluidic bioreactor systems that at least exist in the literature. How much how much improvement do people generally see by going for these systems versus like like the Fiji shaped benchtop

>> Right now, I would say close to zero. And the reason is the reason is economic. So, the the one metric or lens for looking at it is just what is the sort of cost all all in cost to getting that that dynamic cell culture data that that one experiment that data. And there's two components to that. The first is like what's your what's your capex, right? Like how much did it cost to actually get this device in here and use this thing? And what's like and and really this like capex per experimental lane. And then the second is what is the opex on that? Like every time that we that we run the experiment, how much how much does it cost?

And the So, to to give an example like a the benchtop reactors um depending on whether you're going with kind of the gold standard or some of the derivative ones now, um let's say the capex is between 5 to 15,000 dollars, 20,000 dollars for for each experimental lane. And then your opex is you know, all because you've got you've got not just the media. You need to also take the time to grow the cells up to be able to seed it. You've got the the human coming in and and running it. And then you've got the actual disposable or you've got cleaning the thing and sterilizing it. So, it ends up being around 1,500 or 2,000 dollars, right? Every experiment that you run. The closest like microfluidic system in capability it it's only four lanes. And it's $80,000.

And so that gives you a per lane cost of still $20,000. And then the disposable costs are are I think still around you know $500, $700 for each for each thing. So it's just like there's no there's no there's not much economic reason to it. The reason that that product is on the market is because it cuts down on on on media utilization. Um But like there But that's why I think it's not a very successful product. Um what what we're building is Like in philosophy there's a difference between like changes in degree and changes in kind, right? So it's like okay you take a little step, you take a little step and it's just like okay it's it's different but it's not like qualitatively that different. And then you've got like okay when you 10x or you 100x something, right?

It's like all of a sudden new things get get unlocked. And so we're looking at you know a cap ex of $8 a lane. And we're looking we're looking at at uh you know an op ex per experiment of like $20 or less, right? And so that just those two things together um really transform what is. And then if if as I said you can you start integrating more sensor systems into it, those those two parts are kind of fixed, right? The the cap ex and mostly op ex on that. But the amount of data and the amount of value that you can get out of it, that's where I think like there's much there's much higher much higher place to go.

>> Instinctively uh if if I understand correctly that both existing microfluidic systems and your have lithography as the like underlying manufacturing component. How come And like like yours like has like circuits integrated and that's how you can get like these sensors. But the underlying creation process is the same. Why is microfluidics so much more expensive than the EQ device?

>> So that that that device I was just rec- referencing is is not made with is not made with lithography. It's a it's a molded

>> Okay.

>> It's a molded device. But the key thing actually is that they don't have active There's a big divide in microfluidics between passive and active microfluidics. So passive is like um it like paper microfluidics or something, right? So your your pregnancy test is a paper microfluidics. Just kind of like does does one thing. Doesn't have feedback in it. Doesn't really have control and regulation. And then really separate is like, "Okay, can you can you come in here? Can you sense things and change things as they're as they're going on?" And most of the mhm most of the systems right now do not multiplex the control aspect across a large number of things.

And the sensing part of it and so the actuation part of it um if you if you have to if you use like molded plastic, there's kind of no way to to integrate sensors easily from molded plastic. Like it doesn't come out of the the factory with all of these things into it. You still have to go and like add all these things together. So then you're adding in labor costs there, right? And you're adding in all that. So even if the even if the even if kind of like the some of the end result is in certain capabilities similar the upstream manufacturing of it because you can't integrate everything together really constrains your your economics on it.

>> And so like even if the um lithography produced microfluidics devices potentially on the market that like that alone may cost something similar to the EQ device, but all the sensors that are added on increase the cost.

>> Right. Let me let me back up here and say that um lithography as a technique does have this property where it is the it is whatever the cost kind of like doesn't scale with how complicated you make it. Big difference is in silicon the base cost for making it is substantially higher than the base cost for making things in printed circuit boards. So in in general this is true of almost to my knowledge like all forms of manufacturing. Um as you increase, you know, precision requirements you increase cost. And um and it tends to scale like like logarithmically, logarithmically, right?

So uh if you if you make if you make a there there are two ways that you're kind of using um silicon and lithography, which is either you will um like I said make it as a as a mold that that you then so you're you're really just using the lithography as a mold. Uh and then you're kind of peel this casted thing off of it or people will actually use the silicon for and they make the fluidic channels in there. But the the problem with silicon is it's it's really expensive. Like you in general we do not make disposables out of things that are made in in in silicon lithography. Like it's because like to to make something to make something this size um probably $400 or something.

>> Why like it if it seems like the the the the big innovation here is combining lithography or like doing lithography on the circuit board as opposed to doing it either in silicon or like fire and mold both of which seem more expensive than the radio would. Was it simply a matter of like realizing that you could do this on circuit boards and dramatically reduce your cost? Like what Like why why did this not exist 10 years ago?

>> Right. So I I I think the the first is that you know, different worlds don't talk very much. And the in this case like the the tool builder world and the tool user world are very distinct. And the second is that um to to answer the question of how how did I come to it? I was uh uh I was in my apartment in São Paulo and uh and I'd been I'd I'd actually been really digging into um biofilms. And I was and I was like okay like, you know, just kind of like going deep on biofilms and what's what's going on here. I was like all right, so much of this is about like the concentration of of these things and like they're creating these little microenvironments and all of this.

And then I I was I was really at the time there was uh this concern about are we going to have enough um bio like capacity like capacity for for bioproduction. And what I'd seen work before is in traditional chemical synthesis uh they switched to continuous flow microreactors. So uh like Corning Glass that makes the makes the glass in your in your iPhone, they also make chemical reactors. And the the benefit of this is that you can flow things together. They react quite quickly. You can pull the heat off and things. It's really consistent. Um the reason you can't use that in biology at the moment is because in order to like traditional chemical synthesis, you really are pretty much you're just controlling flow rate and the reactions happen really fast normally, right?

You just mix them together and it's it's done. Um But in biology, right? Like you need sensors in order to see what's going on. The environment is really much more tightly controlled, right? There's more aspects to it. And um and cells cells themselves, right? Are are again like perturbing the the environment around them. So that was that was like the lens. I was looking at like how do you how do you make how do you bring this thing that clearly worked in in chemical engineering? How do you bring that to biology? And and then also thinking about like these biofilms. And uh so I I I studied mathematics. The I I literally wrote this down as a set of axioms. I was like, "What what do you need?" You need to be able to hold fluids apart. You need to be able to combine them together, right?

Um you need to uh integrate sensors of of different modalities so that you so that you can adapt it. Um it needs to be small both for mass transfer reasons because as you get as you get smaller, more there's more surface area around and the limitation for many reactions is literally just like how fast can you get um things from the from the gas phase into the liquid phase and that's purely a function of surface area. Even even actually in in large reactors when they're using bubbles, the bubbles are just creating surface area. Um and and it's and it's about diffusion across that. So if you go small, you get that.

You go small, you also get like laminar flow which is really really nice because uh it takes problems that are in a um that are like normally kind of chaotic and it linearizes them. So, there's a great experiment everybody should should should watch on on YouTube of you put a couple drops of dye into this kind of gel and the gel has a really high viscosity. And so and then they kind of like stir it up this way, right?

>> And they go backwards.

>> go backwards, right? And the idea is like, "Well, why can you do that?" You can you can do that because in a sense it's linear, right? Whereas in a in a chaotic system you'll you'll get to some point and now you can't tell which path you were at before, right? So, these are these are like things. And then you need to be able to run a lot of them both for in that in originally it was for throughput, but that that throughput idea also translates to to to to data parallelization. And then if you need a lot of them, you also need to be manufacturable, right? You need to be mass manufacturable and needs to come down. Okay, those are like the axioms. I was like, "These are the things you need." And then I literally went through every manufacturing technique that I that I could find.

I mean, it truly. Um everything down to like, "What are they doing with, you know, 3D printed glass, you know, at the moment?" And and you can just kind of like knock these out for a variety of reasons. The the molded polymers don't work because you can't um because you can't integrate the the sensors in them in them in them quickly. Um 3D printing doesn't work at all. Doesn't kind of matter what the modality is because it's the infrastructure isn't already there, right? So, it's like if you need to make a bunch of disposables, which great business. Um always make disposables. Um If you need to make a bunch of disposables, then you should you should pick something that that you don't need to have a lot of capital in order to scale it, right?

So, you need an existing manufacturing industry for it. And just all these came back. And then ultimately I was like, let me just reframe it. I was like, let's just like pick one of these and like optimize for that. I was like, how what's what's the best just best way to build sensors? I was like, well, I mean, like printed circuit boards are really good. And I was like, okay, can I then build the rest of this in here? Like, can I can I take like let me just common technique you're right. Like, can can I just select some subset of this of this problem, optimize for that, and then force the other ones to kind of like fit into it? And And I was like, yeah, okay, sensors are good there. It's good on manufacturing. Okay, here. And then and then and then after that, went to the literature.

I was like, okay, here's the the one person who's kind of who's kind of actually actually done this. Go fly to England, go work with her. And then the University of Bath. Bryson, yeah. Okay. Interesting. One person in the world has stumbled across this idea. Well, like well, I guess like surely if every if every technique seems to have like its mild drawbacks and there wasn't a single like optimal one that you stumbled across, what is the drawback of going for printed circuit board? Okay, well, I will tell you from a from a there is there's the problem that you might think and then there's a problem you'll discover. Um the problem you would you would think is that uh it's a kind of like a weird thing.

You have to get people to adapt to it or you know, also like you you do have to design each of those sensors. I mean, it's just just because you pick a good good good sort of palette to work with, you still have to like, you know, do a bunch of work, you know, do all this. That's those all end up actually being like not that big of a deal. The harder problem is this. Which is that nobody understands it.

>> That's true.

>> I really truly like nobody understands it.

>> I guess like who are you selling selling these to? Like I I can imagine one customer is like academic labs, maybe. Um how and I imagine the much bigger customer are people either preparing drugs for clinical trials or generics manufacturers. How one, how willing are they to buy this stuff? Um and two, is there like a customer base I'm missing?

>> Yeah, so I I'd say like our our first customer is actually the US Army.

>> Oh. Um and that's for that's for doing something quite different from media optimization, but still within the within the realm of you need to explore a larger space and current ways of doing that are like insufficient. Um the broader answer here of who who's the customer the customer who feels the most pain for this are the are the large CDMOs. This So um you know, I've spoken to people who have worked for those places. What is the thing that they talk about every year? It's the yield. That's like that's it. They they actually don't have We're talking about like degrees of freedom for them as a company. They don't have that many, right? They don't come up with their own products. Okay? They they aren't allowed to like they they aren't allowed to innovate on it once the process is set.

Um they have extraordinary downside risk if they make a mistake. Uh and they are they are in a competitive marketplace with you know, like the pharma companies are taking the bulk of the the pharma companies are getting the value capture, right? Like they they ultimately own distribution. Um and so they're they're winning there. So those features make them very desirable kind of buyers for it. But media optimization is if if you it both happens like within pharma companies for their for their for their sometimes pharma companies manufacture their own things, but also you just you like the process of running dynamic cell experiments like that dynamic cell culture like that is pervasive.

It That's that's that's where I think like the the largest opportunity really is you know, all of these problems um in biology m- many of them ultimately just reduce to how many dynamic cell culture experiments can you run. And so this is this is true for um uh this is true for like you know, new antibiotics discovery. Um it's true for doing things in like organ-on-a-chip. Um you know, it's it's true in cancer research. Like if you actually just take the lens of what are people trying to get out of this experiment? Well, they need to be able to come in, they need to be able to, you know, perturb things over time in this and they need to be able to read out during it. Okay. Maybe that's maybe that's too big of a lens, right?

Maybe there are there are particular areas like ah like our system is not going to going to go there. Okay, there are some edge cases where like it's it's not going to be compatible. But there's enough of a core there where and and you see the the justification for this empirically is that you you already see it. Like every time that benchtop every time that bioreactors have gotten smaller and more automated they diffuse more into the ecosystem. It gets adopted more and people continue to want more automation, more experiments, and and cheaper on it, so.

>> Is do you view Eku as like not just a media optimization company, the hope is that whatever the final device ends up looking like it's useful for almost any anything that's an in vitro system where you're trying to screen many things across it.

>> Yeah. My Our goal is to produce 99% of the world's dynamic biological data. And the reason that that's achievable is because we do not produce that much right now. And by by increasing the the throughput by increasing the the relevant modalities that we're putting in and those conditions. I think that that is a totally achievable achievable thing. That's where I started in the beginning talking about like this interface between computation and biology and there being that that mismatch. Like that interface, that layer, that's what we that's what we want to build and that's what we want to own.

>> I'm curious amongst the customers right now, like um maybe the department like uh like the military projects does its own direction for selling this to either like CDMOs, pharmas, generics manufacturers. My impression is that all of these groups like yeah, like you said, don't like variability. And so they're very hesitant to buy new technology that promises like uh like the the sky and the moon. Um what's the hardest part about selling to these people and how do you like reassure them that like things are going to be fine?

>> Uh I I certainly underestimated the importance of that of that aspect here. Um you know, I I've sold a lot of things in my life so far in very different domains. And I I will say that not only in biotech not only in pharma but for biopharma manufacturing the level of conservatism and and scrutiny is extraordinarily high. So, the the like wedge or way of getting into that into that distribution, um there are there are a few examples. Okay. The first one is the kind of traditional way, which would be who do the who do the CDMOs look towards? The CDMOs are not going to adopt it until they've seen a pharma company use it. Okay? Pharma companies are not going to talk to you until you have uh you know, a paper published from a from a probably premier lab of some sort, right?

The premier lab is is not going to touch anything until at least you have, you know, a white paper and and some, you know, connection, you know, in order to do this. And in order to do that, you need to kind of like build the the device. So, it's like, how do you resolve this problem of of getting getting to that getting to that getting to that end customer and doing it. Um the the first is that it's like there are ways of augmenting existing instruments. So, the advantage of it kind of being a stand-alone sensing system is that you can you can kind of come in as just an add-on to some some you're still going to have the same economics, but now we can offer you some more data out of that out of that same thing. And uh you can you can I that's like a lower threshold for them.

And it's not involved in the actual like they can just throw that part of the data away if they if they don't like it, right? If it's not useful. So, that that lowers some of it.

>> I guess it's like cheap enough such that it's not a major investment to try. Okay.

>> Right. Right. Um the the second is and and like I it's like a big I I was just rereading um Geoffrey Moore's uh crop crossing the the chasm, which Have you read this? Okay, highly recommend if It's been on my bookshelf for 8 years, 10 years. The other day I was just like I should reread this. I was like, "God." And the big idea is that, you know, for what counts as a market, like what counts as a market is is not only that people are sort of like buying something repeatedly, but critically that it's a group of people who talk to each other and and look at each other, right? And so you've got the you've got like the academic labs that sort of like look at each other and talk to each other.

And then, you know, the the pharma companies like look at each other and, you know, talk to each other. And then the CDMOs look at each other. But but the key thing is actually like the big CDMOs They they don't they don't they don't they don't talk that much. They don't associate that much with like the little the little CDMOs. But those are those are ones actually that we can that we can sell to and get some get some evidence coming in there. So there's there's building ancillary systems that can tack on to existing things for getting in there. And then and then there's the other way, which is just like be so good they can't ignore you in a sense.

>> I I was going to ask that. I imagine like the gold standard here is like you show one of these CDMOs like like here is the the the cost entire of expert produced media versus the cost entire of expert plus Iku media.

>> Well, actually the the gold standard is is not that not that we say it. The gold standard is that, you know, Eli Lilly says it, right? That's that because that's that's their customer. That And and those those pharma companies own those CDMOs.

>> Yeah. I I guess like has any pharma like done this and they have produced or like even you internally have have it like done this like side-by-side comparison and you have this very clean result to share to them or is it more like you're you're still in the phase of like you're seeing the magnitude of improvement the system gives.

>> I it's it's more like it will be extremely surprising if you do not get the first of all if if you don't get the the economics

>> Yeah.

>> and and and then also all evidence points to being able to run more and different experiments gets you to a better answer. So you can you can kind of work back from

>> Like if you follow the trend lines like it almost has like almost necessarily has to be the case that this is better than what's currently being used.

>> Yes.

>> Okay.

>> Yeah.

>> Is it um I'm curious uh has there been like any in the early initial deployments of this and like there will be like a white paper coming out in the next year of like here's what we found um by like using the ecosystem.

>> Sure. Um I I would say it will be much like necessarily more dull than that.

>> Okay. Okay.

>> So I I I would separate it actually between between two things. I would say there's like the the hype marketing stuff to do. And then there's the like what does a CSO actually look at, right? And from my interaction with with with scientists as a breed is first of all they are a breed. And and secondly that they are like allergic to any hype and any kind of and any kind of you know promotional stuff here. So what what they want to see and and I don't need to be creative here. Um what they need to see is your experiments run your device with some readout and then you take the gold standard and you replicate that and it needs to be you know at the same facility right needs to be that.

You need to show those two and uh basically the the the drawing the graph needs to be obvious enough that that is like okay I can see how these how these like correlate in the scale. They don't actually need to be perfect. That's none of none of them none of them are perfect. This is true um this is true for doing uh scale up from the bench top to the pilot and all these things, right? It's really just like a series of kind of like graphs like okay this thing maps onto this thing maps onto this thing. Um and then and then the the next step is actually you need um you need that replicated at another another facility. So like like for pharma to adopt something um it's not even just that like you need one lab.

You need it to be out of like three different labs who all who all who all get because like ultimately their thing is about is about repeatability.

>> Yeah, reducing variability. Okay, yeah. Um

>> Reducing variability but then also like re repeatability.

>> Hm.

>> Um yeah.

>> If uh if someone were to hand you um a hundred million dollars equity free to like push forward the mission of Eco as much as possible like one I'd be curious like where you would spend the money and two what are the actually I guess connected to the first question what are the axes of improvements that still like lie ahead of the future of the device?

>> Yeah. Uh I think first thing we would do is is really build this high throughput perfusion system. Um I would integrate Raman sensing and I think that that's like the uh I think that's like a killer app. I think I think if you do that it's just it unlocks so much. Um but also yeah if if you go back through the literature it people have been talking about the value and use of having a high throughput perfusion device for a quarter century. And that was before we had the the machine learning or AI to also like interpret that data. That was, you know, before the problems that we're encountering are also getting, you know, harder to to to manage. So, I think that's like that's that's very clearly there.

Along the way there, okay, you you build like organ on a organ on a chip high throughput. That's also like a constraint right now. It's um you know, when the larger manufacturers they're they're moving towards a little bit, but they still have some trade-offs as they as they as they as they try to move to it. Where I think is actually uh really interesting that I hadn't gone down until recently um is in is in droplet microfluidics. So, the idea of um So, what in some sense what we're doing with perfusion is like, okay, let's take you know, a benchtop bioreactor and all that control and let's shrink that down. The the droplet microfluidics is more like let's just take a test tube and shrink it really small, right?

And if you shrink That's where it's like 10x Genomics um that's a form of like droplet microfluidics. It tends to be more of an integration of of microfluidics with some some chemistry. Um you know, some some chemical technique to to kind of either help with signaling or um help with the the formations of particular types of of droplets that allow kind of um like memories that you can diffuse diffuse through in things. But I think what's what's really under explored are are two things from the customer side or from the data side it's higher resolution, more temporal data data sets from there, right? Like again, getting back to this idea that that cells are time varying and sensitive and you know and highly parallel. Um it in like a bunch of different different ways.

The ability to shrink it shrink that experimental system down that much explore the space but not lose the the temporal element the way that it is right now for the most part. I think that's like really really powerful. And I there are a couple there are a couple of techniques people have been trying to get down to they've there's there's a technique for like getting it down to like 7 minutes now. Um but but it's it's it it's still like there's still trade-offs. Like like when I look at it I'm like oh there's they still haven't resolved these trade-offs. So that's that's one aspect. I I think that could be enormously valuable.

Uh and then the the second thing is the droplet microfluidics right now don't like they're really focused on the formation of the droplets and these things kind of coming through. Um they are not as they're they're they're not really chaining things together. And in the literature there are all of these kind of um almost like transistor parts, right? Like little little parts that peop- people have built. And you can see like there's this dream of building like truly lab-on-a-chip, right? And the the problem is that right now as you try to build a lab on a a chip you try to do these things there just aren't enough of the the subsystems or steps that you can kind of like link together on there. So it's like you'll do a set of these then it's like okay, we got to come out of the chip, right?

And it's like then you kind of like lose all of it. And so I think it's really only in the past 5 years and then with with our technology for being able to to like actively manipulate things in there and and do the feedback.

>> I think like rather than conceiving of lab automation as automating manual tasks which has a hard upper bound on how much you know, efficiency and capability that you will get out of it. Like let's just start doing what we did in other industries which would be like, "No, no, no. Okay, we have to start over and we have to kind of like build some of these things in here." But we've already built a lot of them now. Why don't we actually start building those those that lab on a chip.

>> I I remember for my for my lab automation article one person remarked to me that it's a shame that liquid handlers have become so popular because like biology happens at much smaller scales than that. So like you're like you're making a system very large when it doesn't need to be that large.

>> It's it's it's Okay, like I don't know if you've I don't know if you've ever seen these um like robot arms that uh get like a cup of coffee and then like like you know, they've got them in like the San Francisco airport. Terrible idea. Um and it's like, "Okay, you go over and and it's like, okay, the machine, you know, picks up the cup and then puts it over here and does the grinder and like brings it to you." Okay, what that's doing is automating a manual task. It's taking the way that humans just have kind of done something and then been like, "I'm just going to throw an an arm or an anthropomorphic thing on top of it and then duplicate it." Okay, and the result of that is honestly not that great, right?

Like there's a reason that those things will continue to not take off in a any sense of a novelty other sense of a novelty. And compare that to your Nespresso which still has like an interface you still need to get your cup of but like far better, right? Like the Nespresso they're like, "Oh, actually, like, let's integrate like the the uh you know, the actual heater and the automatic dispenser and all of these things, right? And they made it much more compact. And this is Or, you know, like your your coffee vending machines also works this right? Neither one of those are trying to just take the human steps and then just be like literally wherever the human is, we'll just put this thing in here. And that's what I'm seeing happening right now in la- lab automation in general.

And um I don't just think it's like lazy. I do think it's lazy. I don't just think I think it's also um like close to philosophical like a crime. I think it's a crime. Because you think like they're

>> For automation to truly be useful, like, there needs to be a new way of interacting with the underlying systems.

>> Yeah, it's like it's like it's just they're not really thinking through the problem.

>> Well, I guess like one argument is that it's easier for these things to get adoption if you are allowing them to work in the exact same environment that humans are able to work in.

>> Yeah. And and I think I think that makes sense um for things like machine tenders for 3D print uh for um like CNC machines, right? But what's the difference? Well, the CNC part is you know, 100 mm. Right? Okay. So, it necessarily has to be closer to human to human scale. But look look at what's happened in um Like so, the the most kind of like useful places for robotics and and heuristic you can you can use is if it says robotics in it, it's not really that useful. Whereas if it if it says what it just does, then it's been a successful. So, a dishwasher is like a very useful robot, right? Self-driving car, very useful very useful robot. And in the uh industrial space, uh it's mainly around um like logistics and moving things, right?

So, the really successful ways of actually leveraging automation, first, they respect the the they they respect like what the real goal is, and they respect kind of like the limits of that um of the thing you're trying to manipulate. So, if the things you're trying to manipulate are, you know, like grocery grocery things, one way could be like, "Let's take a humanoid and it goes to the grocery store and it like picks up, you know, things off the shelf." That's what what people do, and that's what these humanoid companies want to do. And the alternative would be like, "Actually, if you look at the logistic companies that do the best of it, it looks nothing like that at all, right?" It's some like huge grid.

It has these things like running around like crazy, and all they're doing is like picking up these things and setting it down. And there's like there's no way that a humanoid system can compete with that, right? There's no way that this lazy and you can let the economics kind of like decide that over time. Um I Yeah, I I just this this idea that it's like actually pushing the lab the lab forward, I don't really buy. I just like I also also like I do not um see like Eli Lilly or Johnson & Johnson putting a robotic arm near their lab bench. I think what like what, you know, Ginkgo's doing with their um with their lab automation system, those carts around, yeah. Okay, right?

Like I I think that that's like at least sort of like a reasonable compromise in a sense, you know, we don't need to go and re-engineer each of these um each of these things that already already exist. If we if we can if we can literally just like make the interface of them easier. Okay. Um but then but then I think like the real the real goal should be like as much as possible. If the economics fit, just like think through the problem correctly. Just just just put put it on chip as much as as much as possible. So.

>> That makes sense. Um I think those were the last questions I had. Uh thank you so much for coming on.

>> Thank you for having me. Yeah.
