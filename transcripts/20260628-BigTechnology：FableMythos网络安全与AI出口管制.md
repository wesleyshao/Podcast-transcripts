---
访谈时间: 2026-06-28
访谈时间说明: "无法从公开元数据确认独立录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Alex Stamos"
嘉宾公司名称: "Corridor"
播客名称: "Alex Kantrowitz / Big Technology Podcast"
播客url地址: "https://www.youtube.com/watch?v=rJ6YdXhvGpY"
transcript_source: "YouTube automatic captions, en-orig json3."
全文提及的关键名词:
  - Fable
  - Mythos
  - Anthropic
  - Amazon Bedrock
  - AWS Secret Cloud
  - Opus 4
  - GPT-5
  - Kimi
  - AI cybersecurity
  - bug finding
  - exploit creation
  - export controls
  - China
  - open letter
companies:
  - AMZN
  - Anthropic
  - OpenAI
  - 月之暗面
industries:
  - 网络安全
  - 云计算
technologies:
  - LLM
keywords:
  - 出口管制
tags:
  - AMZN
  - Anthropic
  - OpenAI
  - 月之暗面
  - 网络安全
  - 云计算
  - LLM
  - 出口管制
---

# AI’s True Cyber Risk: Fable, Mythos, China, and The Rest — With Alex Stamos

## Transcript

We're obviously at this moment where the government has pulled down or or basically forced Anthropic to pull down fable or mythos uh its frontier model,

>> right? Both of them. Yes.

>> What happened?

>> Right. So uh just for recap uh for everybody uh last Friday uh what happened was the White House became aware of research that Amazon had did. Um it is not unreasonable for Amazon to do this work, right? So uh Amazon hosts uh anthropics models in in what they call bedrock. Uh this includes in all of the classified spaces. So if the NSA is using anthropics models, it is running in AWS secret cloud or top secret cloud. Uh and so Amazon is doing security testing. I expect this was part of

getting ready to host Fable and Bedrock. and uh found some things that they wanted to complain about with Fable's protections that make Fable different than Mythos. I guess we can talk about the exact ones. Uh Amazon had sent over these results to Anthropic. There was some disagreement between Anthropic and Amazon during the week of how serious they were. Now, I don't have the exact details here, but somehow apparently Andy Jasse, the CEO of Amazon, mentions this to somebody at the White House, and the White House freaks out and uh according

to reporting uh calls Amazon or Anthropic uh and uh is not happy with how quickly they can get Anthropic on the phone. Anthropic is asking for more technical details. They're not able to get details from the White House of what the White House wants. So, the White House orders them to take Fable down. Uh, Enthropic says, "No, we can just fix these issues. Why don't we work it out together?" And as a result, instead of working out together on Friday afternoon, something around 5:00 p.m. Pacific time, the Commerce Department signs

an order saying that the models are designated export controlled and that no foreigner, including the foreign citizens who worked and actually built the models themselves, can can touch them. Uh whether or not the administration actually has that legal power is disputed, but Enthropic decides to actually follow through instead of immediately getting a temporary restraining order. And they because they have no ability to make sure that no uh foreign uh citizen is is seeing the models actually pulls them down. Uh both Mythos uh which was privately accessible as well as Fable

uh which was publicly available.

>> Now you've spent a career working in security.

>> Yes. Um Ron John and I for months now have had this debate about whether all of this talk of doom and super powerful models from anthropic like for instance mythos a model so powerful that you can't access it. Um whether that represented a real capability increase or whether that was

>> just marketing and it's a step change uh not not really a step change in capabilities. So I actually want to toss it to Rajan who is firmly on the marketing side of this thing just to make the argument of why you think this is marketing and Alex can address that. Yeah, I think trying to understand like what is that capabil new capability that is so dangerous? What is that step change? I think the reason I get so suspect on it is how perfectly coordinate coordinated a lot of the marketing

and communications are around how they roll these out. Like again, mythos is the most dangerous thing. There's someone eating a sandwich in a park that actually got like where the model broke out of containment was like a PR release. It was it was a very coordinated thing. So what is that danger that they're trying to kind of bring to the world? Like what is it really? What does it look like, feel like, or what is it actually going to be a problem?

>> Uh so how much money do you guys have writing on this? That's [laughter]

>> Well, how would we even play this? Like I don't even know.

>> Oh, like as a bet?

>> As a bet? Like is there a poly market? Uh yeah, I'm trying to see what my angle is here. Apparently I have. Yeah.

>> Well, well, no, you are the person that knows action. you know the answers here and we have just been kind of like debating

>> we just like to argue we just argue on

>> so okay so it's actually it's actually a little bit of a complicated answer so um mythos is almost it is the best bug finding model that we know about for sure it is most likely the best bugfinding model in the world and I say most likely because we do not know what the Chinese secretly have in their labs but for all the stuff for which we have open known security evaluations for it scores the best. Now, is it the avenging cyber god that anthropic makes it out to be? I

personally don't think so. Yes, it is.

>> You're not necessar you're not right yet,

>> but but it is it is really good. It is really good at finding bugs. But from my perspective, the like Opus 48, GPT 5.5, a bunch of other models are here in Mythosis here

>> at bug finding

>> at bugf finding and exploit development and it is not here, which is kind of where you would think from reading all this stuff. The other thing is that everybody pretends that mythos was the breakthrough, but that is not true. For people in the security world who've been paying attention, this Rubicon was crossed well last year, okay, with the Opus 4 series, with the GPD5 series, that is when the models became better or as good or or better than the best human bugfinders. And not just as good as the best

bug finders. And there's like 50 or 100 of these people and I know a couple dozen of them. The problem is those people are very expensive, right? And they don't scale. You can't just throw water on them and make them multiply like gremlins. That would be nice. I mean, certainly the NSA would love that, but models can you can just scale them as much as you want with money and power and and and GPUs. And so that last year was a huge deal because all of a sudden you saw these

amateur bugfinders. Imagine you went to a high school track meet and every single kid is posting Olympic World record times. You'd be like, "Man, they're juicing, right? That something had happened." That is what last year was like. like mid la mid to late last year in the vulnerability discovery world is the kids started juicing right and it's because the models hit this point where they could find everything and so yes mythos is really good at finding bugs it's really good at writing exploits fable is not and so that is that

is what the whole point of fable is it is the same model weights as mythos but anthropic put a protection in place to keep it from doing the really nasty stuff that mythos will do And anth uh Amazon has some complaints about that. But what happened is the complaints Amazon has uh a number of us have looked at them and then Enthropic has pushed back even with the jailbreaks that Amazon has. You cannot get Fable to do things that you can't do with the Opus series with GPT5 and even with

a bunch of Chinese models. So that is why the the actions by the Trump administration make absolutely no sense because those models will not refuse at all. You can just ask GPD5 to go find these bugs and it will go do it for you. Um, you can just ask Kimmy, which is an open source Chinese model. It will go write you these exploits. And so, yes, you can trick Fable into doing certain things, but you can't trick it into doing the really powerful Mythos stuff, which is like grind on the

Linux kernel for all day and find a bunch of bugs, which will cost you hundreds of thousands of dollars, it turns out, if you pay the full price. Um, and those have not been jailbroken. And so there's no real good reason for what happened. So yes, Mythos is really powerful. It has only been accessible to a very small number of companies. It is not magically powerful. The other thing you have to remember here is like bugs are cheap. Exploits are like we're now drowning in bugs because these models are so

good at finding and we have so much bad software. We've been writing bad software forever. And it turns out that like writing human beings writing code in C and C++ especially was a really bad idea that like we should not have been writing like building our entire lives like based upon memory unsafe languages and then in the presence of these superhuman bug finders not just mythos but all of them that was not a good idea. And so, uh, if you're a pedestrian and you get hit by a F-150 at 80

miles per hour or a McLaren at 200 miles per hour, you don't really care. You're dead, right? [laughter] And that's the difference here is like the Mythos is the F1, right? Mythos is the F1.

>> Yeah, exactly. And Kimmy or GLM52 is the F-150. And so you could take the the the McLaren off the market, but all you've done is actually hurt the defenders who want to have full coverage, right? Who want to be able to find all the bugs. An attacker only needs one or two bugs to string together to actually pull off the attack. And so that's why, you know, so about 150 of us wrote this open letter and signed it saying this is really stupid because all you're doing is hurting defenders

and you're also really hurting the US AI industry. Okay, I think Ron John wins the debate.

>> Well, no, it's not all marketing, but it's

>> it's not all marketing, but like I I just want to say like mythos is really powerful, but doesn't really matter because there's so many bugs out there that you can use any of these models to find them. I what I'd like to do is I'd like to shift the debate one away from finding bugs because the other problem here is like we cannot set the standard that US AI models can't find bugs. That is a terrible terrible terrible standard. If you have a p if you are writing software with

an LLM, it has to be able to understand what a bug looks like. So it does not write those bugs. It has to. And that is that's the trick actually Amazon used was they tricked it into basically finding bugs in individual lines of code because it has to be able to do that to write secure code. If if our if American LMS know nothing about security, they will create more security flaws. So we cannot create a standard where American LLMs are dumb about security. That would be a humongous own goal.

And that is one of the possible outcomes here of of this whole brewhaha. That would be really stupid. And so uh you know my I think yes I I don't think either one of you wins. I mean as the referee here I think Ron John has a little bit of a you have a point but mythos is really good. It just

>> it doesn't Anthropic has pleaded up too much. Um, OpenAI is rumored to be releasing something that's mythos quality really soon. Um, and I doubt that they're gonna like follow they'll just give it a number like uh I think they've learned from Enthropic you don't call your thing like the cyber gorgon. Um,

>> uh,

>> that actually would sell.

>> Yeah. Yeah. It sells a little too well, right? Um, right. Maybe as a Greek with the Odyssey coming out, I'm getting a little sensitive about the the marketing here, but like like you know, let's let's like back off on the naming scheme and move back to numbers. Uh uh but like I I think a a big part of this is we just have to like reset the standard of like not bug finding, but the actual creating creation of exploits and then other kinds of offensive operations of which there's a

bunch of other things you can do offensively with these models. Those are the things that we should call off limits, not bug finding because that is something that we have to do much more quickly than we're doing right now. C

>> can I I just want to try to articulate my point which is you know this is all right. So when we talk about is mythos material or is mythos marketing um my argument would be like wouldn't if something was material it would look a lot like what we're seeing today right like at a certain point these models are increasing in capabilities you're going to want to put some safeguards on them and so is what anthropic is doing that different from like where you'd want to be

>> if you actually had these concerns

>> I mean I think both anthropic and openai have a path in which they have like a KYC model now

>> know your customer

>> a know your customer. Yeah. So, Open AI actually has a couple levels. They have a public one where you can basically say, I want access to cyber capabilities and then they have a private one. I believe anthropic only has the private one, right, to get access to mythos. Uh but uh I I do think it's reasonable to have some level of gating, but in the case of Glass, I think it was honestly it I thought it was not widespread enough. I know of like critical infrastructure companies that don't have

access to mythos right now. Um

>> nobody does right now. Well, no, right now before last week, like people who should have had access did not have access. Now, seeing what happened here, you can see why they were so careful. Um, but from my perspective as defenders, we are in a race against time, right? We have all of these bugs that need to be fixed. And we also have this weird thing where we're like, this whole conversation is predicated on the idea that like the American labs are years ahead of our adversaries. And that is just

not true. Right? So while Fable was shut down on Tuesday of this week, GLM 5.2 was shipped right from Z.AI which is a Chinese lab. This is an openweight model. It is MIT licensed. So any of you can go not just download the weights from HuggingFace, but you can include it in your own product and you can retrain it. It is within percentage points of the top closed models from anthropic and open AI in a bunch of things. um a bunch of of evals. We don't know how good it is

at bug finding yet. So there hasn't been any good testing here. But in coding and a bunch of other intelligence tasks, it's almost as good as the best the United States has. And that's the best Chinese model we know about, right? Unlike American labs, the Chinese are not going to announce their mythos, right? And so the idea that we should be doing everything in the United States to just be playing defense is we're playing like a a defensive model here, that is stupid from my perspective. We need to be accelerating

our capability to do these things and not just playing defense.

>> Well, now I am sufficiently scared even though I've thought that the mythos was pure marketing. But but what do we do about it? Like how do we what is that like and I I think I share that glasswing again why it felt like marketing to me. It was this kind of exclusive club that people were invited to and I actually spoke with people who are using it and they spoke about it almost like it was a club like oh yeah we got access to mythos. We're spending a ton of

money. Like I think what should it look like this kind of roll out to actually

>> when us and glass I mean it they're fixing real bugs. They have found like 10,000 bugs. Now one of the problems with glasswing is they've found like 10,000 bugs but they've only fixed a thousand right? So like you do not want a 10 to1 ratio of the bugs you found to fixed. Um we just joined a thing called project Athena which chain guard is running which is all about fixing specifically open source bugs. Right. So Glasswing is a lot of that is closed source with inside commercial companies. We are

part of this coalition that is using uh Mythos to fix open source bugs which is a huge challenge because like just finding the people who have access to that that source code uh commit access is difficult. Uh so that's going to be like a huge push. So it it's not like just totally BS. Um, I do think that one of the things that's going on here is that if these companies ran any modern AI security tool against their codebase, they'd find 80% of those bugs. They don't have to use Mythos.

Right. Okay. So, um, it's just that they've never looked, right? It's they're like,

>> that's concerning.

>> Yeah. Right. And and so they've they're like, "Oh, yeah. I've got this old crappy code." And they look for the first time and they all of a sudden they find

>> and they could have done it a year ago or six months ago and found some number or some percentage. I had this conversation with a CEO this morning who's like, "How do I get into Mythos? Alex, who can call?" And I said, "Don't wait.

>> Here you go. Here's an API key for Opus right now. It works today because do not wait for the Trump administration to figure out what they're doing with Mythos. Use Opus 48 right now and I guarantee you'll get 70% of the bugs you care about."

>> Alex, you're you're a security researcher. One of the stipulations about getting Fable back. So, by the way, Anthropic has said they expect uh Fable to come back on soon. Um, but one of the stipulations that's been talked about to do that is that they have to prevent it from being able to be jailbroken. [laughter] Is that possible?

>> Yeah. I saw I saw you did jailbreak in air quotes.

>> Yeah. No.

>> So, we have we have two minutes left. So, talk a little bit about why that's not possible.

>> No. There's actually a paper from NIST. It's like a kind of a goal completeness theorem kind of uh paper that basically says it's impossible to make a model that is completely not jailbreakable. Like I said, Fable needs to be able to understand what security flaws are to be able to do its job. I think what what Enthropic might what what Enthropic might the game might they might be playing here is redefine what jailbreak is back to what their system card says. So their system card says we define different levels

of cyber capability and finding a couple of bugs and knowing what a bug is is okay but we won't let you like build exploit chains and and do lots of long-term stuff. And so if they can define back to their system card what a jailbreak is then they're fine, right? Um, what would be terrible for the entire American AI and cyber security industries is if the Trump administration defines a jailbreak as having any ability to find any vulnerability in code because then all of us have to go to Chinese models.

>> That's it. Yes. Like that would be a terrible terrible outcome. And that might happen because unfortunately one the news that broke just in the last couple hours is Politico is reporting that Anthropic and the Trump administration are negotiating what the AI safety standards should be. So like I don't know it's like Howard Lutnik writing an eval right now. Like I find that a little terrifying. So um I I am hoping that Enthropic obviously there's very smart people in working on this. I am hoping that they are able to come

up with something reasonable that moves stuff towards exploitation not bug finding. like we have to have the ability as as defenders to find and fix flaws. The other thing I just want because we don't have a lot of time. The other real own goal here was that this injected a type of political instability and political risk into the USI industry that did not exist. There are a bunch of companies that are now going to be have to use openweight models because at any time on a Friday afternoon, it's it's good

thing that Fable was only out for a week because people weren't didn't have time to work into their critical path. But if if if Fable had been out for a month and at 5 PM on a Friday all of a sudden it got yanked, then pagers across the country would have gone off because every every systems would have fallen over. And so now this week CIOS and CTO's are signing contracts to have openweight models on different hosts on US hosts. They're not using Chinese hosts, but they're using Chinese models on

as backups through LM routers because political risk is now a risk of using AI companies. That is a massive own goal. The United States of America does not need to do that. We should not do that again. That is incredibly stupid at a moment of maximum pressure from the People's Republic of China. Um, and so I can't stress enough like we we lost a war this weekend. Like, let's not lose another war by making it unreliable to utilize the United States for AI.

>> Alex, will you come on the show for a longer conversation?

>> Absolutely. I'd love to. Yeah.

>> Alex Stamos and Ron. Thank you.
