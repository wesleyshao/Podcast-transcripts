---
访谈时间: "2026-05-13"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Eddy Lazzarin; Matt Gleason; Robert Hackett"
嘉宾公司名称: "a16z crypto"
播客名称: "a16z crypto"
播客url地址: "https://www.youtube.com/watch?v=e0o-hRCti7M"
全文提及的关键名词: 
  - "AI cybersecurity"
  - "DeFi exploits"
  - "crypto hacks"
  - "social engineering"
  - "defenders"
  - "attackers"
  - "geopolitical cyber activity"
  - "stress testing"
  - "onchain transparency"
  - "security engineering"
字幕来源: "automatic_captions:en-orig:English (Original)"
YouTube视频标题: "AI And The Future Of Cybersecurity"
---

# AI And The Future Of Cybersecurity

## Transcript

[00:00:00] Anthropic has been out there talking
[00:00:01] about the devastation to be wrought by
[00:00:04] its product mythos.
[00:00:05] >> The fact that people are so afraid of AI
[00:00:08] is completely backwards. I have great
[00:00:10] respect for Anthropic, but I do think
[00:00:12] that there is a degree of doomsday
[00:00:14] marketing here. The classes of harms
[00:00:17] that they think would be happening
[00:00:18] aren't happening.
[00:00:19] >> It isn't that we were secure and now
[00:00:21] we're not. It's we were never secure, we
[00:00:23] just didn't know it yet.
[00:00:24] >> If I had a thing and I heard it got
[00:00:26] hacked, the first thing I think is,
[00:00:27] "Man, I wish I used more AI to find the
[00:00:30] problems." If there was no AI and they
[00:00:32] had a super genius hiding in a mountain
[00:00:34] in North Korea and he had 300 IQ and
[00:00:36] he's breaking everything with his
[00:00:38] gigabrain power, that would be
[00:00:39] terrifying.
[00:00:40] >> DeFi hacks has been running rampant
[00:00:43] throughout the industry over the past
[00:00:44] month. What can people do to secure
[00:00:47] themselves?
[00:00:47] >> Well,
[00:00:49] I think
[00:00:56] >> All right. Hey and welcome everybody.
[00:00:58] We're here with Eddy Lazarin, general
[00:01:00] partner at a16z crypto, and Matt
[00:01:02] Gleason, senior security engineer, also
[00:01:04] here at a16z crypto. And today we're
[00:01:06] talking about the spate of DeFi hacks
[00:01:10] that has been running rampant throughout
[00:01:12] the industry over the past month. Um
[00:01:15] there have been almost as many hacks as
[00:01:18] there are days in April in April.
[00:01:22] About $635 million lost in total.
[00:01:26] What's going on? This is a huge uptick
[00:01:29] in security incidents, in hackings, in
[00:01:32] money lost.
[00:01:34] Why is this happening right now?
[00:01:37] >> So in general, we've seen an uptick in
[00:01:39] general cyber activity um throughout the
[00:01:42] beginning of this year. So the impetus
[00:01:44] there being
[00:01:45] kind of more capabilities, also some
[00:01:48] geopolitical tension stuff. And then
[00:01:50] we've seen market upticks after the US
[00:01:53] invasion in Iran. Um specifically at
[00:01:55] critical infrastructure and some
[00:01:57] financially motivated attacks.
[00:02:00] And so this may just be kind of a
[00:02:02] fruition of
[00:02:04] kind of two lines of thinking, which is
[00:02:07] attackers have increased their own
[00:02:08] capability with some of the AI models,
[00:02:12] specifically probably honestly
[00:02:14] the AI models hosted in China or hosted
[00:02:16] locally that are being released by China
[00:02:18] as well as just geopolitical tensions
[00:02:22] being at such a fever pitch that more of
[00:02:25] our adversaries are more willing to be
[00:02:27] more brazen to kind of
[00:02:29] fight back, right? It's a retaliatory
[00:02:32] effort.
[00:02:33] >> It's very hard to say and that's because
[00:02:35] often the post-mortem analysis of these
[00:02:38] hacks lack specific clues about the
[00:02:42] exact nature of the attackers. It takes
[00:02:44] a lot longer than, you know, than the
[00:02:46] month that we've had to get to the
[00:02:47] bottom of that. And in some of the most
[00:02:49] sophisticated cases, they actually can
[00:02:51] clean up their tracks. They can clean up
[00:02:53] behind them and make it even harder to
[00:02:54] figure out what's going on. From what I
[00:02:56] understand in my network, the belief is
[00:02:58] that this relates to an intensification
[00:03:01] of activity related to the North
[00:03:03] Koreans.
[00:03:04] Now that I doubt that that's all of
[00:03:05] these attacks.
[00:03:07] Uh but I think the most important part
[00:03:09] of what you're asking, Robert, the
[00:03:10] implication is has something changed in
[00:03:13] technology? Is something changed broadly
[00:03:16] that explains this as part of the result
[00:03:18] of a change as opposed to just like
[00:03:20] coincidentally hot month?
[00:03:23] And that theme is that people are
[00:03:24] wondering whether attackers use of AI
[00:03:27] has supported these attacks. Now even
[00:03:29] then, it's hard to say
[00:03:32] because an AI attack looks like a human
[00:03:34] attack, right? It's not like they knock
[00:03:36] down the door and you see them on the
[00:03:38] security camera, right? What happens is
[00:03:41] you see some access logs and you see
[00:03:43] some
[00:03:45] code run and you see some files appear
[00:03:47] and some files disappear, right? That's
[00:03:49] what these attacks actually look like
[00:03:51] and uh no significant difference really
[00:03:54] between a human being doing it or AI I'm
[00:03:56] doing it. But the worry is always that
[00:03:58] the increased sophistication of AI
[00:04:00] models means that it's easier for
[00:04:02] attackers to find and exploit
[00:04:04] vulnerabilities.
[00:04:06] Yeah, truth be told, I'm tripping over
[00:04:08] myself cuz what I'm really trying to say
[00:04:10] is that it doesn't matter.
[00:04:11] That it's AI or not.
[00:04:13] Okay, it doesn't matter. The bug was
[00:04:15] there before the AI found it. Do you see
[00:04:17] what I'm saying? Like like Mark tweeted
[00:04:18] that. Mark's right. Okay, that's the
[00:04:20] truth. Is that if there is an issue,
[00:04:23] the issue is that attackers
[00:04:26] maybe have adopted AI faster than
[00:04:29] defenders.
[00:04:30] And so if I had to summarize in one
[00:04:32] sentence my recommendation to defenders,
[00:04:35] it would be massively increase your use
[00:04:38] of AI to red team yourself and find the
[00:04:41] bugs.
[00:04:42] Start attacking yourself full speed.
[00:04:45] Like deploy every tool you can
[00:04:48] and get every security expert you can,
[00:04:50] get access to the latest, most
[00:04:52] sophisticated models
[00:04:54] to brutalize your company from every
[00:04:56] angle.
[00:04:58] Because that's the only way to feel
[00:04:59] safer. That's the only way to know. Is
[00:05:00] to remove the bug.
[00:05:02] >> Okay, so there's there's a hypothesis
[00:05:03] out here that maybe AI has gotten good
[00:05:07] enough to make this extremely easy for
[00:05:09] people to find and poke holes in
[00:05:12] existing protocols and tech stacks.
[00:05:16] And that defenders are not making the
[00:05:18] same use of that technology at this
[00:05:20] moment. At least there's been some
[00:05:22] window where attackers have had the
[00:05:24] upper hand.
[00:05:25] >> Yeah, potentially. That's incredibly
[00:05:27] hard to substantiate, honestly. That's
[00:05:29] at least what the zeitgeist seems to be
[00:05:31] conveying.
[00:05:32] But in any case, it's kind of
[00:05:34] irrelevant. Whether that's true or not,
[00:05:35] there is only one solution and it is to
[00:05:38] radically increase the use of the latest
[00:05:41] tools to basically rethink security from
[00:05:44] first principles.
[00:05:45] Because we can have it tested constantly
[00:05:48] in a more sophisticated way at all
[00:05:49] times. It's interesting. It's like a new
[00:05:50] type of thing.
[00:05:52] And to harden harden your security
[00:05:54] posture in all the conventional ways.
[00:05:56] And for crypto specific people,
[00:05:58] as far as I can tell, the vast majority
[00:06:00] of the issues have been, you know,
[00:06:01] conventional security issues as in keys
[00:06:04] getting stolen, machines getting
[00:06:06] accessed when they shouldn't have been
[00:06:07] accessed, code being run in places it
[00:06:09] shouldn't have been run.
[00:06:11] >> So, there are sort of two points you're
[00:06:12] making. One is given that we live in
[00:06:15] this world, in this environment where
[00:06:16] the tools exist, they're out there, they
[00:06:18] cannot be taken away, what do you do
[00:06:20] about it? And the answer is you meet the
[00:06:23] threat with a defensive posture and
[00:06:26] strategy that is commensurate with the
[00:06:28] risks that are now out there. And the
[00:06:31] other is the bugs were in there to begin
[00:06:33] with, and this would have happened, it's
[00:06:35] just a matter of time. And so, maybe if
[00:06:39] all of this is just happening at once
[00:06:41] right now, it might look bad, it might
[00:06:43] look scary, but it's just condensing
[00:06:47] kind of what might have happened anyway.
[00:06:49] The vulnerabilities were there.
[00:06:51] >> I can just reiterate that like someone's
[00:06:52] going to find the bug. Who do you want
[00:06:54] it to be?
[00:06:55] Better to be you than somebody else. The
[00:06:57] fact that people are so afraid of AI is
[00:07:00] like completely backwards.
[00:07:03] It's literally completely backwards.
[00:07:06] Because if I had a thing and I heard it
[00:07:08] got hacked,
[00:07:09] the first thing I think is
[00:07:12] man, I wish I used more AI to find the
[00:07:14] problems.
[00:07:15] Man, I wish I tried to hack myself with
[00:07:17] the AI.
[00:07:18] Like it moves the domain of control into
[00:07:20] yourself
[00:07:21] because you have access to those tools.
[00:07:24] You know what would be really scary? If
[00:07:26] there was no AI and they had a super
[00:07:28] genius hiding in a mountain in North
[00:07:30] Korea
[00:07:31] and he had 300 IQ and had like a
[00:07:34] 2-ft wide cranium and like no one could
[00:07:37] use the guy and he's breaking everything
[00:07:38] with his giga brain power.
[00:07:40] Do you see what I'm saying? That would
[00:07:41] be terrifying. How do you cuz how do you
[00:07:43] defend against that? Right? But it's
[00:07:45] actually the opposite. The tool that
[00:07:48] Open AI is rolling out, like the cyber
[00:07:50] fine tune,
[00:07:51] the special 5.5 cyber,
[00:07:54] they're going to let everybody use that
[00:07:55] eventually. Like basically everybody who
[00:07:57] has even like a you know, a defensible
[00:07:59] reason to use it. And it's not going to
[00:08:01] cost you 5 million a year. It's going to
[00:08:03] just cost you a normal
[00:08:05] like anything else. Like I think I have
[00:08:07] access to it and I'm paying like the 200
[00:08:09] bucks a month.
[00:08:10] That's the opposite of the
[00:08:12] giant guy in the cave. That's like
[00:08:15] incredible.
[00:08:16] Do you see what I'm saying? You have no
[00:08:17] excuse. You have the tool. So,
[00:08:19] uh you should be very encouraged. And
[00:08:22] maybe there's another thing that's
[00:08:23] that's left unsaid is like
[00:08:25] you know, people say there's always bugs
[00:08:27] and there's always exploits. And that's
[00:08:28] true. That's because it's nearly
[00:08:30] impossible to make software that is
[00:08:31] perfect.
[00:08:33] But there is a distinction, even if it's
[00:08:35] hard to quantify, between software that
[00:08:37] has been heavily scrutinized and
[00:08:40] software that has not been.
[00:08:42] That's what it means when there's like a
[00:08:43] heavily audited software or like things
[00:08:45] like this. There's degrees of
[00:08:46] verification. There's degrees of
[00:08:47] confidence we can have.
[00:08:49] The more AI there is and the better it
[00:08:51] is and the more powerful it is and the
[00:08:52] better it is specifically at hacking,
[00:08:55] the more confident and better you should
[00:08:57] feel about the software because you
[00:08:58] really can decrease the number of bugs
[00:09:01] in it for sure.
[00:09:03] You can actually like materially do that
[00:09:05] and develop conviction that it has few
[00:09:08] bugs if enough effort is spent by enough
[00:09:11] experts and enough resources.
[00:09:15] That's just a fact. The discouraging
[00:09:16] thing, if any,
[00:09:18] is that the attackers are just more AI
[00:09:22] built
[00:09:23] than the defenders.
[00:09:25] That that would that's scary.
[00:09:26] >> And that's certainly an argument that
[00:09:28] some people, including AI companies
[00:09:30] themselves, have been making. You know,
[00:09:32] Anthropic has been out there talking
[00:09:33] about the devastation to be wrought by
[00:09:36] its product mythos, you know, should it
[00:09:39] get into people's hands.
[00:09:41] >> And look, I have great respect for
[00:09:43] Anthropic, okay? I'm not going to
[00:09:44] disparage Anthropic, but I do think that
[00:09:46] there is a degree of doomsday marketing
[00:09:49] here. The classes of harms that they
[00:09:51] think would be happening aren't
[00:09:53] happening.
[00:09:54] And then the harms that could be
[00:09:56] happening maybe are happening, like the
[00:09:58] cyber stuff.
[00:09:59] There's only one treatment and it is to
[00:10:02] arm the defenders, in my view. You might
[00:10:04] say, "Oh, you don't you want to
[00:10:06] have the bad guys get their hands on
[00:10:07] it?" The bad guys are going to get their
[00:10:08] hands on it eventually. They're going to
[00:10:10] spend the money. They're going to make
[00:10:11] one. It's going to happen. No one's
[00:10:13] going to stop it ever.
[00:10:14] The only thing you can do is have it now
[00:10:17] and secure it now. Because we can,
[00:10:19] thanks to the way cryptography works and
[00:10:22] thanks to the way cybersecurity works,
[00:10:24] we can design systems that are easier to
[00:10:26] defend than to attack. Thankfully,
[00:10:28] nature allows us this luxury. So, let's
[00:10:31] lean into that.
[00:10:32] >> That is a wake-up call if I've ever
[00:10:34] heard one. Matt, what can people do
[00:10:37] given this state of affairs to secure
[00:10:39] themselves? From a user perspective,
[00:10:41] sure, and also from the protocol
[00:10:43] perspective, from a builder perspective,
[00:10:45] the people who are putting this
[00:10:46] technology out there.
[00:10:48] >> So, there's a few different points here
[00:10:50] I think that are worth stating.
[00:10:52] Um one is, of course, that
[00:10:55] we're kind of in for a painful
[00:10:57] transitionary period and that we're in a
[00:10:59] place where we need to be kind of
[00:11:02] creating more securable environments. Um
[00:11:04] so, this is
[00:11:06] basically implementing patterns or
[00:11:08] implementing access restrictions that
[00:11:10] allow us to kind of more reasonably
[00:11:13] guard what we want to keep safe. So,
[00:11:16] typically for a company, this would be
[00:11:17] your production environment. I think the
[00:11:19] first thing that's worth saying is like
[00:11:21] there will be pain, but it will be pain
[00:11:23] before kind of
[00:11:25] a place where we are more secure than we
[00:11:27] have ever been. Because
[00:11:29] the fact of the matter is these
[00:11:30] vulnerabilities, again, just to
[00:11:32] reiterate, have always existed. They
[00:11:34] were always there. You just needed a
[00:11:36] determined attacker who was informed
[00:11:37] enough to choose to exploit them.
[00:11:40] We happen to have people with motive who
[00:11:43] are determined, and people who have
[00:11:45] capabilities, um both AI-enabled as well
[00:11:48] as just their own,
[00:11:50] who have decided to kind of take it upon
[00:11:51] themselves to do harm.
[00:11:54] As the defenders catch up, we're going
[00:11:57] to see environments that are going to
[00:11:59] look like the most well-hardened
[00:12:01] environments, and they're going to be
[00:12:02] essentially everyone.
[00:12:04] Um because things are getting cheaper to
[00:12:05] build, things are getting cheaper to
[00:12:06] implement. The way we sift through ideas
[00:12:09] is a lot faster and cheaper. Like, we
[00:12:12] have ways of navigating through this,
[00:12:14] but we're all just going to kind of need
[00:12:15] to learn
[00:12:16] how to do it. There is some change that
[00:12:19] needs to be made for everyone. One is,
[00:12:21] of course, use the AIs to find your
[00:12:23] problems, right? If the attackers are
[00:12:25] using it to find your problems, the
[00:12:27] defenders can use it to find their
[00:12:28] problems. We're using the same AIs. You
[00:12:30] actually have an advantage as a defender
[00:12:31] cuz you know more about your
[00:12:32] environment. You have more visibility,
[00:12:34] and if you get caught, it isn't a big
[00:12:36] deal. You just go, "Okay, cool. I'll
[00:12:38] we'll just keep going."
[00:12:39] So, like, what what do people do now?
[00:12:41] You basically embrace the fact that
[00:12:44] we're transitioning how we approach
[00:12:46] problems. We're transitioning the amount
[00:12:49] of security you need to have in your
[00:12:51] organization. And we're transitioning
[00:12:53] the expectations you need to have with
[00:12:55] your own security teams or your
[00:12:56] development teams or your IT teams, the
[00:12:58] people who are performing the security
[00:13:00] stuff.
[00:13:01] They don't have an excuse for not
[00:13:02] knowing certain aspects of security cuz
[00:13:05] they can just go ask the omniscient AI
[00:13:08] and get the answer for themselves,
[00:13:10] right? They can kind of have
[00:13:11] conversations with it. They can they can
[00:13:13] use it to enable themselves to be
[00:13:14] better.
[00:13:15] And so, like, everyone needs to be
[00:13:18] better.
[00:13:19] And through being better, I think we're
[00:13:21] going to deploy much better
[00:13:22] environments. It's just how long that
[00:13:24] takes is the question.
[00:13:26] >> What is the scale this transition? I
[00:13:28] mean, the history of technology and
[00:13:30] warfare, there have been innovations
[00:13:32] that have caused really wide-sweeping
[00:13:35] societal changes. You know, you had the
[00:13:37] invention of the stirrup, and then all
[00:13:39] of a sudden people had to batten down
[00:13:42] and create castle fortifications. The
[00:13:45] nature of warfare, of attack and
[00:13:46] defense, changed. And then you got the
[00:13:49] invention of gunpowder and cannons, and
[00:13:51] all of a sudden fortifications and walls
[00:13:54] were not quite as useful as they had
[00:13:56] once been. Where are we at with this
[00:13:59] transition that we're undergoing right
[00:14:01] now, where we have these tools that
[00:14:03] allow you to have such scale and speed
[00:14:06] matched up against the way our systems
[00:14:09] work as is today?
[00:14:10] >> This is a great example of of of
[00:14:11] something where quantity has its own
[00:14:14] quality. There has always been large
[00:14:16] groups of gigabrains thinking about
[00:14:19] breaking systems and defending them.
[00:14:22] I mean, in the history of the internet,
[00:14:23] particularly the last 30 years of the
[00:14:26] internet. I think the difference is just
[00:14:28] the intensification,
[00:14:30] but not the intensification of the
[00:14:32] breaking energy. That is what we're kind
[00:14:34] of talking about with AIs, like the
[00:14:36] ability to figure out where the problems
[00:14:37] are quickly and act on exploiting them
[00:14:40] and so on. But the most important factor
[00:14:43] to me is actually the intensity of how
[00:14:46] everything else is wired into the
[00:14:48] internet and wired into devices.
[00:14:51] As more and more important things become
[00:14:53] connected to the internet, then the
[00:14:55] consequences, and therefore benefits,
[00:14:57] and therefore stakes of compromising
[00:15:00] them, escalates,
[00:15:01] which means proportionately more
[00:15:03] resources need to be expended on
[00:15:05] defending them, and are also expended by
[00:15:07] the attackers in trying to exploit them.
[00:15:10] Right? So, it's an intensification.
[00:15:13] Bringing AI into the story is just
[00:15:15] further intensification of the defense
[00:15:18] and of the offense.
[00:15:20] So, I don't see it as like a categorical
[00:15:22] change. That's why a lot of the actual
[00:15:26] recommendations, you know, we're not
[00:15:27] really getting super technical on this
[00:15:29] podcast, but if you go into the
[00:15:30] recommendations that technical experts
[00:15:31] make, they're not
[00:15:34] profoundly different in any way. It's
[00:15:36] the same stuff. It's like
[00:15:37] the different passwords, make sure
[00:15:39] permissioning in your organization is
[00:15:41] very fine-grained, and no one has
[00:15:44] unilateral access to key systems, try
[00:15:46] the latest tools on mitigating supply
[00:15:48] chain attacks. Like, these are all
[00:15:50] things that are all just parts of the
[00:15:52] same intensification. So, I don't see a
[00:15:54] huge structural change happening right
[00:15:57] now, except I see a rapid deployment of
[00:16:01] the new tools by the attackers and by
[00:16:04] the defenders.
[00:16:05] >> Yeah, I I I think comparing it to
[00:16:07] weapons or armaments is a little weird,
[00:16:11] um cuz I I I don't think this is itself
[00:16:14] a thing that
[00:16:16] does the attacking, right? Like, we're
[00:16:17] doing the attacking the same way we used
[00:16:19] to. We're doing the things the same way
[00:16:20] we used to. It'd be more synonymous with
[00:16:22] like going from like a torch, right?
[00:16:24] Something that's lit with fire and has
[00:16:26] limited visibility, to going to a
[00:16:28] flashlight or spotlight, where like, "Oh
[00:16:31] man, I just like turn that thing on and
[00:16:33] I can see everything in front of me."
[00:16:35] Right? It's granting superior visibility
[00:16:38] to people to be able to see what is. Cuz
[00:16:42] again,
[00:16:43] it isn't that we were secure and now
[00:16:45] we're not. It's we were never secure, we
[00:16:47] just didn't know it yet.
[00:16:50] And so, we just went from
[00:16:52] going around in the forest with a torch
[00:16:55] to someone just rolled up and shot a
[00:16:58] spotlight in front of us, and now we can
[00:17:00] see where all the bugs are.
[00:17:02] It's just more of a visibility
[00:17:05] amplifier. It's the the thing that gives
[00:17:07] you more context of what is going on, it
[00:17:10] allows you to process more information
[00:17:12] faster. It just allows you to look at
[00:17:14] more things than you used to be able to
[00:17:16] before.
[00:17:17] >> We've spent a good deal of time talking
[00:17:19] about the nature of AI, but what does
[00:17:21] this all mean for DeFi, for on-chain
[00:17:24] finance, and for the future of crypto?
[00:17:27] >> It's funny. I think crypto has such a
[00:17:28] headwind narratively here.
[00:17:31] And it's because I know a lot of
[00:17:33] traditional organizations that are
[00:17:35] worried about hacks and worried about
[00:17:37] all this like it's hard to quantify the
[00:17:40] damage. Right? You just hear like
[00:17:42] information leaked.
[00:17:44] Okay, how bad is that really? But the
[00:17:46] grand scope of the damage is hard to
[00:17:48] say, and it's still really bad, but it's
[00:17:50] mushier.
[00:17:51] But stealing like hundreds of of
[00:17:54] millions of dollars or 50 million or
[00:17:56] even just a million is so salient and so
[00:17:59] specific, and crypto is so public and so
[00:18:02] transparent that crypto's transparency
[00:18:06] makes it more evident
[00:18:08] when things have gone wrong.
[00:18:10] And a lot of the damage in conventional
[00:18:13] hacks is is hidden in the fact
[00:18:15] corporations have a very strong interest
[00:18:18] in avoiding people seeing it to avoid
[00:18:20] backlash and scandal.
[00:18:23] Right? And so, crypto has a unique
[00:18:26] disadvantage narratively when it comes
[00:18:28] to security issues.
[00:18:30] And that's unfortunate, but I think that
[00:18:32] I I actually don't think of this as a
[00:18:33] crypto-specific issue. I think it's
[00:18:35] exacerbated as a result of crypto's
[00:18:37] visibility.
[00:18:39] >> Yeah, I think that's an incredible
[00:18:40] point. I mean, if you combine it, Matt,
[00:18:42] with your point about how AI is more
[00:18:44] like a flash light or a spotlight, um
[00:18:47] it's just that the environment that you
[00:18:49] are shining light on happens to amplify
[00:18:52] that light many, many times over when
[00:18:54] we're talking about something as public
[00:18:56] and transparent as crypto
[00:18:58] versus something a little bit more
[00:19:00] shadowy and in the dark like the
[00:19:02] corporate world.
[00:19:03] >> I don't want to sound conspiratorial,
[00:19:04] but I think
[00:19:05] >> is very conspiratorial.
[00:19:06] >> Shadowy is dark.
[00:19:07] >> Yeah, but shadowy I don't know why, but
[00:19:10] >> you're right. I mean, yeah.
[00:19:11] >> Sort of is, yeah.
[00:19:13] So, I mean, you you said what are the
[00:19:14] consequences for DeFi? Well,
[00:19:17] I think DeFi has always had a lot of
[00:19:19] pressure on it to be secure. That has
[00:19:21] been true from the very, very, very
[00:19:23] beginning. That remains the case. And it
[00:19:25] should increase and it ought to
[00:19:26] increase. I think DeFi protocols need to
[00:19:29] be
[00:19:30] unbelievably paranoid, among the most
[00:19:32] paranoid on Earth, because they're
[00:19:34] they're offering people something very
[00:19:36] powerful, right? This self-custody.
[00:19:38] And if if you're giving people this
[00:19:39] incredible power to control it yourself,
[00:19:41] to you know, to be your own bank, to
[00:19:43] hold your own money,
[00:19:45] well, you can't get messed up. Your
[00:19:47] users can't There's 100 things to worry
[00:19:50] about there. With great power comes
[00:19:52] great responsibility, blah blah blah,
[00:19:53] you know. I think DeFi will adapt. I
[00:19:55] think the tools are getting better to be
[00:19:57] more secure, like we've been saying, not
[00:19:58] worse. And I think in its ideal form,
[00:20:01] DeFi is still more secure. A really
[00:20:03] important idea to get out is that
[00:20:06] of the hacks that I looked most closely
[00:20:08] at over the last 30 days, many of them
[00:20:11] would have been mitigated by more
[00:20:13] decentralization, not less.
[00:20:17] More decentralization, not less. In
[00:20:18] other words, the decentralization part
[00:20:20] wasn't the bug.
[00:20:21] The bug was that they were unexpectedly
[00:20:23] more centralized than many people
[00:20:26] believed.
[00:20:27] And the proof is in the response.
[00:20:30] Like with almost every crypto-adjacent
[00:20:33] hack I've seen, the response has
[00:20:35] something to do with, well, let's get
[00:20:37] more parties involved and decentralize
[00:20:39] and remove single points of failure.
[00:20:41] I'm saying like different designs
[00:20:43] require different tradeoffs.
[00:20:45] We have not learned that
[00:20:46] decentralization is bad. What we've
[00:20:48] learned is that
[00:20:49] inadvertent single points of failure is
[00:20:50] bad, which is a thing that we've always
[00:20:52] known.
[00:20:52] >> And so, the point you're underscoring,
[00:20:53] yeah, is that decentralization can
[00:20:55] actually enhance your defensive posture.
[00:20:59] >> Absolutely.
[00:21:00] >> Maybe maybe you two could help me get a
[00:21:01] sense for how much of this is social
[00:21:04] engineering versus chaining together
[00:21:08] technical software exploits.
[00:21:11] >> Those things usually go hand in hand.
[00:21:13] So, we don't have the full postmortem
[00:21:14] for a lot of these.
[00:21:16] My impression is
[00:21:18] there has been a substantial amount of
[00:21:20] social engineering for most of these. If
[00:21:23] I had to sketch the shape, I almost want
[00:21:25] to like draw on the whiteboard here,
[00:21:26] like the shape of a of a hack based on
[00:21:28] my experience.
[00:21:30] It is a series of little problems
[00:21:34] that are woven together
[00:21:36] in such a way that like 10 of them
[00:21:39] together, whatever, you know, four of
[00:21:40] them, 23 of them in sequence,
[00:21:44] all adds up to a huge problem.
[00:21:47] Like right? Like that that's how they
[00:21:49] add up. It's like it's tiny little
[00:21:51] cracks that all come together and then
[00:21:52] before you know it the whole thing
[00:21:53] explodes because just they found a way
[00:21:55] in. They found a way in with all this
[00:21:57] little weaving thing. Weaving through a
[00:21:58] bunch of small issues. In other words,
[00:22:01] you are trying to gradually open and
[00:22:04] expose your ability to exploit a company
[00:22:08] or exploit a project or exploit a user.
[00:22:11] And social engineering is a great tool
[00:22:13] to get a little edge in one dimension.
[00:22:16] It's like
[00:22:17] if only I was on this user's laptop,
[00:22:19] then I could blah blah blah. And then
[00:22:21] once I'm there, then I could do blah
[00:22:22] blah blah. And then I could convince
[00:22:23] another user to do blah blah blah. You
[00:22:25] can see how it might be click one little
[00:22:27] email, then get on a device, and then
[00:22:29] rely on a weak thing, and then this
[00:22:30] email thing, and then blah blah blah.
[00:22:32] You weave them all together as a huge
[00:22:33] problem. So, in almost every attack I
[00:22:35] have seen social engineering be a
[00:22:37] component and potentially a
[00:22:39] counterfactually necessary component. As
[00:22:42] in, if there was no social engineering,
[00:22:43] that attack couldn't have been possible.
[00:22:45] But then again, because of this large
[00:22:48] chain nature,
[00:22:50] you can design a system so that social
[00:22:52] engineering makes it harder to pull off
[00:22:53] an exploit. Right? It's much harder to
[00:22:55] socially engineer two people than it is
[00:22:57] one.
[00:22:58] Social engineering four people and then
[00:23:00] breaking a system that requires multiple
[00:23:02] signatures and then requires a time
[00:23:04] delay and then requires a blah blah blah
[00:23:06] is even harder.
[00:23:07] So, to answer your question, it is
[00:23:10] almost always a part of the mix.
[00:23:12] >> I see what you're getting at. It's sort
[00:23:13] of like the more you decentralize
[00:23:16] control and these access points,
[00:23:20] maybe the safer you are. Now, I'm sure
[00:23:22] there are
[00:23:24] caveats to that, but the point stands
[00:23:26] that
[00:23:27] if there are many walls in between you
[00:23:30] and the exploit, the more walls there
[00:23:33] are, the better you're off.
[00:23:35] >> There's been a meme in security for I
[00:23:38] think it's like 20-some years now. It
[00:23:40] goes like this:
[00:23:41] Social engineering {colon} because
[00:23:44] there's no patch for human stupidity.
[00:23:46] Um it is a bit crass, but like it is it
[00:23:49] is kind of the truth. It is hard to
[00:23:51] formulate technical controls around
[00:23:53] individuals within a company. It is and
[00:23:56] will continue to be the main way people
[00:23:58] get into things. By the numbers in terms
[00:24:01] of impact for the DeFi hacks, it's
[00:24:02] almost certainly
[00:24:04] almost all of it sources social
[00:24:06] engineering somewhere in the attack
[00:24:08] flow, right? Probably the way they got
[00:24:10] access.
[00:24:11] Um in some cases,
[00:24:13] the way they got everything. Like the
[00:24:15] entire thing is social engineering.
[00:24:17] We see other activity as well.
[00:24:19] So, there are hacks that aren't related
[00:24:22] to social engineering, but they're
[00:24:23] typically very small and not super
[00:24:27] impactful. But any of the heavy hitters
[00:24:30] you've heard about were typically like a
[00:24:32] key was compromised or a set of keys was
[00:24:34] compromised using social engineering as
[00:24:37] kind of the main first step.
[00:24:40] And so, social engineering continues to
[00:24:41] be the strongest thing that people use
[00:24:44] and it will continue to be there until
[00:24:46] of course we figure out how to have the
[00:24:48] AIs guard people.
[00:24:50] Um because guess what? That is the
[00:24:51] patch.
[00:24:52] >> Yeah, I was going to I was going to say
[00:24:54] kind of a
[00:24:55] if you'll let me say kind of a sci-fi
[00:24:57] idea Robert is like
[00:24:59] human beings have been prompt injectable
[00:25:01] since their original development.
[00:25:04] And it's unlikely we're going to be able
[00:25:07] to improve that. We use all types of
[00:25:08] trainings.
[00:25:10] We use all types of human feedback
[00:25:12] mechanisms to refine the humans and to
[00:25:15] make them less vulnerable to obvious
[00:25:17] types of social engineering attacks.
[00:25:20] But it's hard to do because human beings
[00:25:23] are so non-deterministic and so
[00:25:25] unpredictable
[00:25:27] and hard to measure and hard to
[00:25:28] instrument. So they are very challenging
[00:25:31] to put in the core loop of a system,
[00:25:34] which is why you have to put multiple of
[00:25:35] them because it turns out we've
[00:25:37] discovered that uh adding multiple
[00:25:39] humans into a cybernetic process
[00:25:43] and requiring consensus among those
[00:25:45] human beings in a sort of an ensemble
[00:25:48] setup is less prone to catastrophic
[00:25:50] error. That's like a way to put it,
[00:25:53] right?
[00:25:53] AIs, although they are goofy now and are
[00:25:56] prompt injectable and are flawed,
[00:25:59] are way better
[00:26:00] at design because first of all, it's
[00:26:02] gotten a lot harder to prompt inject an
[00:26:04] AI. Like it's possible still for sure,
[00:26:07] but it requires some clever new
[00:26:09] techniques that are developing, right?
[00:26:12] Uh but an AI can still be instrumented
[00:26:15] very heavily and it can be guarded very
[00:26:17] very very heavily and it can be measured
[00:26:19] very very carefully and you can push it
[00:26:22] through the same attack scenario
[00:26:25] billions of times
[00:26:28] and see exactly how it responds to
[00:26:30] hundreds of thousands if not millions of
[00:26:33] styles of attack. That's the thing that
[00:26:35] is happening now. We are learning to do
[00:26:36] that now. And so you'll be able to get
[00:26:38] your conviction around an AI's
[00:26:41] likelihood of being socially engineered,
[00:26:44] prompt injected, uh much sooner than you
[00:26:47] will for a human being.
[00:26:48] So in the end, probably not that long
[00:26:50] from now,
[00:26:52] it's going to be better to combine AI
[00:26:54] models and cryptography and other
[00:26:57] designs than to rely even on a person.
[00:27:00] To keep a system secure.
[00:27:02] I think that that's a real possibility.
[00:27:04] Not for all systems, but for some
[00:27:05] things. Who knows? I'm just kind of
[00:27:06] gesturing at something that's a little
[00:27:07] fuzzy to me, but it's at the it's on the
[00:27:09] horizon regarding social engineering.
[00:27:11] >> I like your framing of people as being
[00:27:13] prompt injectable and
[00:27:16] I think we should turn our attention to
[00:27:18] injecting some defensive prompts into
[00:27:20] the people who are listening to this and
[00:27:24] give them some
[00:27:26] idea about what they should do to combat
[00:27:29] it. What can or should they do to stay
[00:27:31] safe?
[00:27:33] >> I mean just for just for users I'll say
[00:27:35] improving the quality of your cognitive
[00:27:37] security should be a top priority today.
[00:27:40] I mean I'm not trying to make people
[00:27:42] stressed out, but you should basically
[00:27:44] assume that you should assume that
[00:27:46] you're under attack at all times really
[00:27:48] really right?
[00:27:49] >> Just be paranoid.
[00:27:50] >> Wait, I don't know what I'm saying.
[00:27:51] >> Don't go outside.
[00:27:52] >> you know, spam calls, spam messages,
[00:27:55] like you know those people are trying to
[00:27:57] take your money and they're trying to
[00:27:58] harm you. So
[00:28:00] just applying the same thing to
[00:28:02] everything, you know, someone sends you
[00:28:03] an email, someone sends you a link,
[00:28:05] someone's asking you to send some money,
[00:28:07] whatever, someone's trying to get some
[00:28:08] information from you, just assume that
[00:28:11] just because of how deeply
[00:28:12] interconnected we all are across the
[00:28:14] whole world, anyone can reach anyone at
[00:28:16] any time basically.
[00:28:18] You should just kind of assume that
[00:28:19] you're under attack.
[00:28:20] And therefore you should develop an
[00:28:22] intuition for what behaviors are
[00:28:24] dangerous and which ones are safe.
[00:28:25] Obviously giving people passwords,
[00:28:27] giving people keys, giving people
[00:28:29] logins, incredibly dangerous. That
[00:28:31] should be obvious that that's totally
[00:28:33] dangerous.
[00:28:34] Clicking on links, somewhat dangerous.
[00:28:36] Going to websites that someone texted
[00:28:39] you, some weird URL,
[00:28:41] pretty obviously dangerous. Installing
[00:28:44] software, especially last minute because
[00:28:46] the Zoom's not working and you really
[00:28:48] need to install it right now.
[00:28:49] >> As happened earlier as we were trying to
[00:28:51] get this going.
[00:28:52] >> Yeah. Should be scary, right? Installing
[00:28:55] software is scary, right? So, like I
[00:28:57] think like the youngest generations kind
[00:29:00] of learn this pretty quick and they
[00:29:01] learn not to trust the digital form of
[00:29:04] the proverbial man selling ice cream or
[00:29:07] handing out ice cream out of his truck
[00:29:08] or whatever. Like you just learn
[00:29:10] if someone texts you with a job
[00:29:12] opportunity,
[00:29:13] no, they do not have free ice cream for
[00:29:15] you. They are trying to hurt you. And
[00:29:17] the same goes for engineers at
[00:29:19] companies. They want to hurt you.
[00:29:21] >> Very appropriately for the timing of
[00:29:23] this conversation, I got logged out of
[00:29:24] all of my active sessions on X today for
[00:29:27] suspicious activity and behavior. So,
[00:29:30] uh yeah, I'm I'm feeling the heat over
[00:29:32] here as well.
[00:29:33] All right. Well, any final plea or
[00:29:36] advice for people to leave off with?
[00:29:40] >> Even if it's temporary,
[00:29:42] make an internal red team for a little
[00:29:44] while.
[00:29:44] And try to break your stuff. Like think
[00:29:46] about how your project is going to get
[00:29:49] wrecked. Think about how your company
[00:29:50] could get wrecked. Think about the
[00:29:51] scariest thing that could possibly
[00:29:52] happen.
[00:29:54] And then ask someone on your team to do
[00:29:56] it. Ask someone on your team to try to
[00:29:59] fish, try to take control of people's
[00:30:02] devices, try to trick people into
[00:30:04] installing things, try to, you know,
[00:30:07] escalate permissions without other
[00:30:10] people's sign-off. You know, run through
[00:30:12] the scenarios.
[00:30:13] Well, what if people take over our
[00:30:14] website? What if we get a email from a
[00:30:17] trusted vendor and the vendor was
[00:30:19] compromised and they emailed us a trick
[00:30:23] and a well-meaning person inside of our
[00:30:25] company clicked it.
[00:30:27] What would happen, right? Run through
[00:30:28] those exercises. And then even better,
[00:30:31] ask an AI to do it, too. Ask an AI how
[00:30:33] to be more thorough. There're going to
[00:30:35] be some really great products, I'm sure,
[00:30:36] this year
[00:30:38] that do exactly this. Like you ask them
[00:30:40] attack the hell out of every employee in
[00:30:41] my company and figure out how to break
[00:30:43] it, right?
[00:30:44] But, you know, until those products
[00:30:46] become available, try to do it yourself.
[00:30:48] You're going to learn a lot. That would
[00:30:49] be my plea.
[00:30:51] >> Matt, how about you?
[00:30:52] I mean, have the people who have access
[00:30:55] to the most sensitive stuff you own
[00:30:59] go through and like examine how from
[00:31:03] their position they would be able to
[00:31:06] like
[00:31:07] attack the company. Red team, but just
[00:31:09] have everyone do it.
[00:31:11] Um and then if they're like curious on
[00:31:14] like, "Oh, could you do this thing?" Ask
[00:31:16] the AI. "Hey AI, like would this be
[00:31:19] feasible?" Like you don't have to do the
[00:31:20] exploit, but you can get pretty good
[00:31:22] answers on like feasibility of certain
[00:31:25] types of attacks, feasibility of certain
[00:31:27] types of activities, and kind of what
[00:31:30] you would do. Because ultimately the way
[00:31:32] a hack's going to be performed is one of
[00:31:34] these people is going to accidentally
[00:31:36] get something on their computer, and
[00:31:38] then from there it's going to be
[00:31:40] perpetrated and go through their
[00:31:42] environment. And so like just take the
[00:31:44] people you're afraid of getting hacked
[00:31:46] and tell them
[00:31:48] "If you get hacked, what can you do to
[00:31:50] our environment? What's the worst things
[00:31:51] you could do?"
[00:31:52] And then try to figure out how to
[00:31:54] mitigate those things um through better
[00:31:56] controls, restrictions of access, dual
[00:31:59] authorization or multi-party
[00:32:00] authorization, just all sorts of
[00:32:02] techniques.
[00:32:03] But yeah, have have everyone take a role
[00:32:05] in this and figure out how to secure
[00:32:07] stuff.
[00:32:08] >> If I were to add something, I would
[00:32:10] really just say
[00:32:12] one, uh passkeys are great.
[00:32:14] If you can migrate to passkeys as the
[00:32:16] way you authenticate into things, it it
[00:32:18] just makes you a lot more robust to
[00:32:19] fishing patterns.
[00:32:21] Just by its design, it uses cryptography
[00:32:24] instead of you know, something you're
[00:32:26] just typing in words, right?
[00:32:28] It's way better. And then the second one
[00:32:30] is we actually have a really cool thing
[00:32:33] now. We have a very patient rubber ducky
[00:32:37] style thing that will talk back to you
[00:32:39] and kind of like not judge you for, you
[00:32:41] know, asking stupid questions.
[00:32:43] Um if you see something and you're like,
[00:32:45] man, I don't know if I should click
[00:32:47] this. You know, you can always ask the
[00:32:49] AI. It's not going to judge. It might
[00:32:53] give you the wrong advice sometimes, but
[00:32:55] at the very least you're taking some
[00:32:57] time to kind of
[00:32:59] step away from the problem to calm down
[00:33:02] because most fishing campaigns will rely
[00:33:04] on panic.
[00:33:05] >> I mean, it's such a good point, Matt.
[00:33:06] Like I actually reminded me of something
[00:33:07] I did this week. Like this is a real
[00:33:10] thing that happened to me. I needed to
[00:33:11] urgently validate that an email I
[00:33:14] received was actually sent to me by the
[00:33:18] sender, like the correct domain.
[00:33:20] And so I've validated DKIM signatures
[00:33:22] before and like check that email. I've
[00:33:24] done that, but like I kind of like
[00:33:25] forgot, whatever, you know, I'm in a
[00:33:27] rush.
[00:33:28] So I just took the whole body and I just
[00:33:30] pasted it into Codex and I just said
[00:33:33] like I'm scared this is a suspicious
[00:33:35] email. Validate the DKIM signature now.
[00:33:38] And not only did it do that with like
[00:33:40] real code, it actually wrote a little
[00:33:42] CLI program and did it like right there.
[00:33:44] But it also even looked up like how old
[00:33:46] the domain was. It's crazy. It did
[00:33:48] research on the sender.
[00:33:50] It found that that sender had recently
[00:33:53] changed domains and that there was
[00:33:54] actually a redirect on the old domain.
[00:33:56] It did like a whole investigation.
[00:33:59] And because I think it's unlikely that
[00:34:02] an attacker would have also compromised
[00:34:04] my Codex login. That is a possibility,
[00:34:06] right? But like I think that's unlikely.
[00:34:09] That made me feel really good and I
[00:34:10] trusted it.
[00:34:11] >> Yeah.
[00:34:12] >> It convinced me. You know what I'm
[00:34:13] saying? I was confident in that email.
[00:34:15] And of course everything ended up okay.
[00:34:16] But
[00:34:17] you see, you should use these tools at
[00:34:18] your disposal.
[00:34:19] Use the tool. Send the screenshot. Copy
[00:34:21] the thing. Send it. Explain what's going
[00:34:23] on and say, how could someone be
[00:34:25] attacking me like this? Am I getting
[00:34:27] screwed right now? What is happening
[00:34:29] right now, you know? And they'll
[00:34:31] actually give you a really good and like
[00:34:33] a super respectable answer
[00:34:35] and you don't have to be embarrassed and
[00:34:38] they work for you. It's pretty amazing.
[00:34:40] >> That's such a great example of turning
[00:34:41] the tables. So it's not just you know,
[00:34:45] you're under attack, but here's how you
[00:34:47] can use it for defense.
[00:34:48] All right. Well, you've heard it from
[00:34:50] our security gurus, Eddie and Matt.
[00:34:53] Thank you both so much for giving people
[00:34:56] some stuff to chew on. People, please
[00:34:58] take this seriously. Use the tools
[00:35:00] available to you and at your disposal to
[00:35:03] protect yourselves because
[00:35:05] the attackers are out there and they are
[00:35:07] coming. Thank you both for your time.
[00:35:10] >> Thank you.
