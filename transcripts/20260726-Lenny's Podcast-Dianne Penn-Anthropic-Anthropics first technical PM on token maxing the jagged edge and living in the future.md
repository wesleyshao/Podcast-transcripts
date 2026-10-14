---
访谈时间: "2026-07-26"
访谈时间说明: "未在公开视频元数据中确认单独录制日期，使用 YouTube 发布时间 2026-07-26。"
嘉宾名字: "Dianne Penn"
嘉宾公司名称: "Anthropic"
播客名称: "Lenny's Podcast"
播客url地址: "https://www.youtube.com/watch?v=tivaWTTVRhY"
全文提及的关键名词:
  - "Dianne Penn"
  - "Anthropic"
  - "Claude"
  - "Claude Code"
  - "MCP"
  - "Skills"
  - "computer use"
  - "tool use"
  - "reasoning"
  - "Fable"
  - "Claude 2"
  - "Opus"
  - "token maxing"
  - "evals"
  - "PRDs"
  - "frontier model safeguards"
  - "Anthropic Labs"
  - "AI research"
  - "product management"
  - "Amazon Alexa"
  - "JP Morgan"
  - "OpenAI"
youtube_video_id: "tivaWTTVRhY"
YouTube发布时间: "2026-07-26"
播客标题: "Anthropic's first technical PM on token maxing, the jagged edge, and living in the future"
字幕来源: "YouTube public subtitles: en-orig json3"
---

# Anthropic's first technical PM on token maxing, the jagged edge, and living in the future

## Transcript

[00:00] In 2023 when I started, nobody said
[00:03] anthropic and claude and coding in the
[00:05] same sentence.
[00:06] >> I want to go back to the beginning of
[00:09] anthropic. I remember dealing, man,
[00:11] these guys have no chance. OpenAI is so
[00:13] far ahead.
[00:14] >> At the time, I saw people were starting
[00:16] to use these models not just for code
[00:18] autocomplete, but actually writing long
[00:20] form code and [music] sat an opportunity
[00:22] for us to train Opus 3 to be better at.
[00:25] That was the inflection. [music] I
[00:26] always think about Opus 45 a year later
[00:28] during winter break when everyone was
[00:30] home able to code.
[00:31] >> What was magical about Opus 45 is we
[00:34] also now not just had a model but a
[00:37] vehicle a great product experience like
[00:39] cloud code. Opus 45 wouldn't have had
[00:42] that moment without a product like cloud
[00:44] code and cloud code wouldn't have had
[00:46] that type of adoption accelerated
[00:48] without opus 45.
[00:50] >> I want to talk about how the product
[00:52] role is changing
[00:53] >> for my team. The way to drive user value
[00:56] is to figure out the right user
[00:57] feedback. The evals, we actually have a
[01:00] saying on the team of evals are the new
[01:01] PRDs.
[01:02] >> Something Gary Tan's been talking about.
[01:04] If you are willing to spend $100,000 a
[01:06] year right now in tokens, you are living
[01:08] the way somebody in 2028 is going to
[01:10] live.
[01:10] >> You have to sweat the tokens as much as
[01:12] you sweat the pixels. You have to be
[01:14] using the models to come up with good
[01:17] and great and better ideas. And there's
[01:19] no substitute for that. People need to
[01:21] be more ambitious with AI tools these
[01:23] days because they're just capable of so
[01:25] much.
[01:25] >> One thing I ask the team is let's say
[01:28] Claude 8 comes around. What changes in
[01:30] what users do? What does that mean for
[01:32] how you're building today?
[01:36] >> Today my guest is Diane Penn, head of
[01:38] product for the AI research and labs
[01:40] teams at Anthropic. She joined Anthropic
[01:42] as the first technical product manager
[01:44] over three years ago, which is a
[01:46] lifetime [music] in AI time when the
[01:48] product team was just five engineers.
[01:50] She's helped ship every model adropic
[01:52] from claw 2 through fable. She's also
[01:55] helped incubate and launch claw code,
[01:57] MCP, skills, claw design, and also core
[02:00] capabilities like computer [music] use,
[02:02] tool use, and reasoning. It is always
[02:04] such a treat and so mind expanding to
[02:07] get to talk to someone who's at the very
[02:08] center of AI and product management.
[02:11] It's hard to imagine someone who has
[02:12] seen more of where things are going than
[02:15] the head of product for anthropics
[02:16] [music]
[02:16] research and labs teams. Before we get
[02:18] into it, don't forget to check out
[02:20] lenniesproass.com
[02:22] for a year free of the hottest and most
[02:25] beautifully crafted AI products in the
[02:27] world available exclusively to Lenny's
[02:29] newsletter subscribers. With that, I
[02:31] bring you Diane Penn.
[02:36] Diane, thank you so much for being here
[02:38] and welcome to the podcast.
[02:40] >> Thank you, Lenny. It's so nice to see
[02:42] you again.
[02:43] >> I want to go back to the beginning of
[02:47] Anthropic, uh, the early days. I
[02:50] remember when Anthropic first launched,
[02:51] this was, I don't know, years, the first
[02:52] model when it launched years ago, three
[02:54] years ago, something like that.
[02:55] >> It was
[02:56] >> three years. I remember just like
[02:58] feeling that man these guys have no
[03:01] chance. Open AAI is so far ahead every
[03:04] like how what are they thinking? How is
[03:05] this possible? Open AI has won. It's too
[03:08] late. Uh things are very different now.
[03:11] The latest number I saw was Anthropic
[03:13] was making like I don't know $50 billion
[03:15] in ARR. That's like what companies used
[03:17] to go public at like very successful
[03:20] companies went public at 50 billion in
[03:22] valuation. Anthropic reportedly is
[03:24] making that every single year. You
[03:27] joined as one of the earliest PMs. There
[03:30] were something like five engineers when
[03:32] you joined. The model hasn't hadn't even
[03:34] [clears throat] launched when you
[03:35] joined. What was it like in those early
[03:38] days of Anthropic? What's something that
[03:41] might surprise people about what it was
[03:43] like at the beginning?
[03:44] >> I think a big part of what's made
[03:47] anthropic today actually has been very
[03:50] much the core of even the early days. So
[03:53] I joined in 2023 like you said we had
[03:57] five product engineers. There was one
[03:59] engineer for the entirety of our API
[04:01] business if you if you believe. Um and I
[04:05] think a big portion of it was the
[04:07] culture was really strong and I think
[04:10] this is something I emphasize for folks
[04:12] who are interested in the company. Um
[04:14] really do walk the walk of um the
[04:17] mission and the culture and the values.
[04:19] Um, and the energy was very much like a
[04:22] startup. And I think you're right. We
[04:24] were very much trying to find our
[04:27] identity in the early years. Like I
[04:30] think there's one piece around the
[04:32] technology, but how does that technology
[04:34] bring value to users, bring value to
[04:37] society, and what could it possibly be?
[04:40] And I think the early years were us
[04:42] exploring that in different ways. Like
[04:44] we did start with like cloud.ai I like
[04:46] another chat chat assistant and evolving
[04:50] into things like tool use. Um I think
[04:53] one of the moments where really we
[04:56] started to get into our groove was
[04:58] shipping things like Golden Gate Claude.
[05:00] I don't know if you like remember that.
[05:02] No.
[05:02] >> Um so this this was actually up for
[05:05] about 24 hours or so. Uh we had just
[05:08] published one of our um early
[05:10] interpretability research in early 2024.
[05:14] And one of the examples was essentially
[05:17] you could have what's called like
[05:19] features of the model within the layers
[05:22] which uh express certain types of uh
[05:25] thematics. So one of the one of the
[05:27] themes that the researchers was able to
[05:30] identify was uh let's say bullet point
[05:33] writing. Another one was people and
[05:35] places. And one that really came up
[05:38] frequently that uh resonated was the
[05:40] Golden Gate Bridge. And so when you
[05:42] actually uh essentially dialed up that
[05:45] feature, Claude would obsess about the
[05:48] Golden Gate Bridge. So meaning in every
[05:50] one of its responses, it would come back
[05:52] and talk about the Golden Gate Bridge.
[05:54] So if you said like, "Give me a recipe
[05:56] for making spaghetti." Uh it would say,
[06:00] "Here is a recipe, and the orange color
[06:03] is just like international red that the
[06:06] Golden Bridge, Golden Gate Bridge looked
[06:08] like." Um, and so it was like really
[06:10] quirky and we we we very much wanted to
[06:14] in that situation just bring that user
[06:16] bring bring it to the masses and bring
[06:18] it to people who are starting to use
[06:20] claude and uh so the entire uh
[06:23] experience actually we spun up on our
[06:25] cloud.ai I website within 24 hours and
[06:29] that took like engineering, product,
[06:32] design, uh our like research teams all
[06:35] working together and we were really
[06:38] really proud of it. I think it maybe
[06:39] reach only 2,000 people to [laughter] be
[06:41] honest. Uh but it it made us feel like
[06:44] oh we can actually bring new user
[06:46] experiences, showcase our research in a
[06:49] way that's different and authentic to us
[06:52] and in a very startupy like pace. That
[06:56] to me was like one of those like maybe
[06:58] hidden inflection points of we were
[07:00] starting to find our identity that we
[07:02] could build products, build experiences
[07:04] that were different for what our
[07:06] competitors had seen, what was already
[07:09] out there. And I think that obviously
[07:12] labs, clog code, etc. Like we then
[07:15] started to identify ourselves as what we
[07:18] actually think the world uh how to think
[07:21] about AI, how to bring that closer to
[07:23] the public. Um but it was a very bottoms
[07:25] up culture. And so that entire
[07:27] experience was very bottoms up. I see
[07:30] engineers, I see uh designers donating
[07:33] time to work on. Um, and so I I like to
[07:36] always use that as example of like what
[07:38] the day early days were like, but the
[07:40] culture and and and the values have very
[07:42] much I think stayed the same since those
[07:45] early days.
[07:46] >> This episode is brought to you by our
[07:48] season's presenting sponsor work OS.
[07:51] What do OpenAI, Anthropic, Cursor,
[07:53] Versell, Replet, Sierra, Clay, and
[07:56] hundreds of other winning companies all
[07:58] have in common? They are all powered by
[08:00] work OS. If you're building a product
[08:02] for the enterprise, you've felt the pain
[08:04] of integrating single signon, skim,
[08:06] arback, audit, logs, and other [music]
[08:08] features required by large companies.
[08:10] Work OS turns those deal blockers into
[08:13] drop-in APIs with a modern developer
[08:15] platform built specifically for B2B SAS.
[08:18] Literally, every startup that I'm an
[08:20] investor in that starts to expand
[08:22] upmarket ends up working with work OS.
[08:24] And that's because they are the best.
[08:26] Whether you are a seedstage startup
[08:28] trying to land your first enterprise
[08:29] customer or a unicorn expanding
[08:31] globally, work OS is the fastest path to
[08:33] becoming enterprise ready and unblocking
[08:35] [music] growth. It's essentially Stripe
[08:37] for enterprise features. Visit
[08:39] workos.com to get started or just hit up
[08:42] their Slack where they have actual
[08:43] engineers waiting to answer your
[08:45] questions. Workos allows you to build
[08:47] faster with delightful APIs,
[08:49] comprehensive docs, and a smooth
[08:51] developer experience. Go to works.com to
[08:54] make your app enterprise ready today.
[08:56] What are some of the other um big
[08:58] inflection moments as you think about
[09:00] just Anthropic going from just this like
[09:02] lab that's trying to compete with this
[09:04] juggernaut of OpenAI at that point to
[09:06] what it is today? What are some moments
[09:08] that stick out of like wow that really
[09:09] changed things? Definitely when we were
[09:12] training and uh testing uh Opus 3, I
[09:17] think that was the moment when the
[09:19] company I think we were less than 200
[09:21] people still at that point and it was
[09:25] very clear that we needed and wanted to
[09:27] create a frontier model and a uh that
[09:32] was very important in terms of like our
[09:34] ability to reach like users, consumers
[09:37] and uh to showcase our research.
[09:40] And we were looking for ways for also
[09:44] why should somebody choose Claude? And
[09:48] that was like a core question and that
[09:49] was a core question we were getting
[09:51] asked in the early days. And I think
[09:53] with Opus 3, you know, it launched I
[09:56] think early March 2024. But there was
[09:59] many many months of various teams across
[10:02] inference across research fine-tuning
[10:05] pre-training that rallied at different
[10:07] points and towards a common goal and uh
[10:12] I think everybody that was involved was
[10:14] like really proud. I remember uh being
[10:17] the PM, us uh the research leagues,
[10:20] myself, we were all in our um this was
[10:22] around December, so we were all at home
[10:25] in our various uh um parents' homes and
[10:28] seeing everybody's background of like
[10:30] their childhood room and everybody was
[10:32] working really hard uh to figure out
[10:35] that like what are we training the model
[10:36] for? Is it showing up the right way? So
[10:39] I think that was really powerful in
[10:41] terms of just building a lot of trust
[10:44] and a lot of our research leads have
[10:46] actually uh from that time are now like
[10:49] leading reinforcement learning leading
[10:52] our character work alignment work. So
[10:54] that that foundational trust I think
[10:56] also helped us work well now with any of
[11:00] our production models across product and
[11:02] research because we were working just so
[11:04] much in the trenches together in the
[11:06] early days. And then I think there were
[11:09] things like identifying that coding was
[11:11] important. Right? In 2023 when I started
[11:15] um nobody said anthropic and claude and
[11:19] coding in the same sentence. I think
[11:21] competitor models like GPT4 at the time
[11:24] was used a bit for coding but it was one
[11:27] of many use cases. And one thing that
[11:30] for example I saw was
[11:33] people are starting to use code uh these
[11:35] models not just for code not just like
[11:38] code autocomplete but actually writing
[11:41] long form code and is that an
[11:43] opportunity for us to train you know
[11:45] opus 3 to be better at and it ended up
[11:48] being a relatively smaller change from a
[11:52] training perspective but it ended up
[11:54] helping us differentiate in the early
[11:56] days uh competitively for users. and
[11:59] actually bring a lot of the very early
[12:02] cla enthusiasts and developers because
[12:05] we were uh providing a value that they
[12:07] didn't really think was possible at the
[12:09] time.
[12:10] >> It's so interesting you talk about Opus
[12:11] 3 like that's so long ago and just like
[12:13] it's hard to think that was a big
[12:15] inflection and so this is really
[12:16] interesting to hear that that was
[12:18] internally a big milestone. It almost
[12:20] feels like this confidence you all built
[12:22] that wow we could really ship a frontier
[12:24] model which is now today so not great if
[12:27] you compare it to what we've got today.
[12:28] What I always think about is Opus 45
[12:30] which was and interestingly like a year
[12:32] later also during winter break when
[12:34] everyone was home able to code. Uh was
[12:37] that another big milestone?
[12:38] >> Yeah. Um Opus 45 was definitely another
[12:42] large moment. I think what was magic
[12:45] about magical about Opus 45 is we also
[12:49] now not just had a model but a vehicle
[12:53] which is like a great product experience
[12:55] like cloud code. Um one thing we say a
[12:58] lot on the team is you need frontier
[13:00] products in order to have frontier
[13:03] models and for people to feel the magic
[13:06] of frontier models. And I think you know
[13:09] we felt the magic of cloud code for very
[13:12] for for uh for many months before that.
[13:15] Uh but the fact that the model
[13:18] essentially got to a level of
[13:20] intelligence where at a very broad level
[13:24] users can experience
[13:27] both frontier intelligence in new use
[13:29] cases allow it to run things end to end
[13:32] in an agent manner. I think that was the
[13:35] inflection. It was actually both. I I
[13:38] think Opus 45 wouldn't have had that
[13:40] moment without a product like Cloud Code
[13:43] and Cloud Code I think wouldn't have had
[13:46] that type of adoption accelerated
[13:48] without Opus45.
[13:50] >> So kind of speaking on on this on this
[13:53] thread uh Daario interestingly if you
[13:55] look back at all his predictions he's
[13:57] just like okay coding is going to be
[13:59] solved it 100% in like a year something
[14:01] like that. He kept talking about how
[14:03] we're going to do code like AI is going
[14:04] to do all our code. And I remember
[14:05] everyone uh being like, "There's no way.
[14:08] This is way too complicated. How is how
[14:09] is AI ever going to get really good at
[14:11] this very complex thing that humans do?
[14:13] No, this is going to be humans for a
[14:14] long time." He was completely right.
[14:17] Something else that he talks a lot about
[14:18] is this exponential that we're now that
[14:21] we're on. That's the way he describes it
[14:22] now. We're like, we're on the
[14:23] exponential curve. I remember not long
[14:26] ago we were new models were being
[14:27] released and everybody was like, "Okay,
[14:29] we're done. There's no more upside. It's
[14:31] plateauing. It's over. There's no more
[14:32] room to grow." Uh, and now it's like the
[14:35] opposite. Now we're inside, like if you
[14:37] think about the curve of the
[14:37] exponential. We're like inside of the
[14:39] exponential now, which by definition
[14:42] means every improvement is a massive
[14:44] jump because we're like on that hockey
[14:46] stick part. What's it like just being on
[14:48] the inside of this crazy historic moment
[14:52] when AI is improving so fast, so much is
[14:56] being unlocked? uh what is it like and
[14:59] how should people prepare for the coming
[15:02] acceleration of more and more
[15:04] improvement from AI? One thing I like to
[15:06] say on the team is most of us weren't
[15:09] like actively working yet when the
[15:11] internet transitioned from this novelty
[15:14] to something that everyone can use and
[15:18] it feels like that's just taking humans
[15:21] uh I think analogies are helpful and so
[15:23] like the analogy of that is I think a
[15:27] couple of things um number one is
[15:30] adaptability
[15:32] becomes very important um I Think we
[15:37] we have evals. We have you know on the
[15:40] safety side safety testing red teaming
[15:43] on the capabilities and product side new
[15:45] prototypes
[15:47] products like cloud code tag and others
[15:50] but it's very hard to predict the exact
[15:52] moment or the exact model and so the
[15:55] adaptability of when you're faced with
[15:57] new information how do you then make
[15:59] better decisions versus keeping the same
[16:02] plan. And so like that agility is really
[16:05] important. I think another piece is with
[16:08] that how do you actually be thinking
[16:11] very first principles and reason through
[16:14] what's next? What's the so what? How do
[16:17] we invest in new products? How do we
[16:19] invest in explaining the differences to
[16:22] users? So a lot of the a lot of the
[16:25] experiences I think of being in that
[16:28] exponential is that pace understanding
[16:31] how you operate and make better
[16:33] decisions and then applying that first
[16:35] principles thinking to then do something
[16:39] that maybe we pull up a plan that uh we
[16:43] would were expecting a few months from
[16:46] now but now the model can actually do uh
[16:48] and work on and actually bring that to
[16:51] user. So this is things like co-work
[16:54] skills tag, you know, as the it's a very
[16:58] positive self-reinforcing loop. And I I
[17:01] I think a big part of it also is just
[17:03] having the like trust in each other like
[17:06] making sure we have like we're we're
[17:08] thinking through the right decision
[17:09] making. We're bringing folks along. Some
[17:12] teams might see the exponential feel it
[17:15] faster than others. So how do we kind of
[17:17] have the grace to bring the
[17:19] organization, the growing organization
[17:20] and company along on that?
[17:22] >> So what I'm hearing here is you almost
[17:24] don't know what will be possible with
[17:26] every model release. And so the
[17:29] important things to focus on is being
[17:31] adaptable as things emerge. Uh to your
[17:34] point, the product itself has to stay up
[17:37] to has to catch up to what is possible.
[17:40] To your point again, just like it can do
[17:42] so much, but people may not understand
[17:44] how to do it and may not be able to do
[17:45] it. So the product making it easy and
[17:47] even just like telling you here's
[17:48] something you could do feels like an
[17:49] important part. Is that roughly what
[17:50] you're describing?
[17:52] >> I I think so. I think um there's some
[17:54] really interesting graphs in the
[17:56] original scaling law papers and I think
[17:59] folks are very familiar with the scaling
[18:02] loss in in the lens of um as you add in
[18:05] more compute and data what's called loss
[18:08] aka the loss from next token prediction
[18:11] uh goes down. And so it's a very smooth
[18:13] linear curve of like the models get more
[18:15] intelligent as you scale them up. What's
[18:17] actually also interesting uh in that
[18:20] paper is there are these like very uh
[18:23] different emerging capability graphs.
[18:26] And so for example uh as you add in more
[18:29] data and you train the models with more
[18:32] compute you essentially see these
[18:34] actually discontinuous emerging
[18:36] capabilities jump. So the models go from
[18:40] 1 + one being a thing that it can't
[18:42] calculate to a thing that it can
[18:44] reliably calculate. And so these
[18:46] emerging capabilities, this like some
[18:49] nature of like predictability is is is
[18:53] not necessarily everyone knows the exact
[18:55] moment like you need the ebells to be
[18:57] able to assess that has actually always
[19:00] been a part of uh how this technology
[19:03] works and also what makes like things
[19:05] like safety harder because unless you
[19:07] have the eval unless you have the
[19:09] systems to test um these jumps might
[19:13] actually happen and you don't know M
[19:16] that's so interesting that you may have
[19:18] developed this like AI brain that uh can
[19:20] do something you're not even aware of
[19:22] and so part of the job is just
[19:24] uncovering wow we just got really good
[19:25] at this thing what can we do with that
[19:27] >> I think there's like product overhang
[19:29] and user overhang like to to maybe put
[19:32] it in our um PM language even on today's
[19:35] models and I think there's like a lot
[19:38] that uh we could be exploring on like
[19:41] our current opuses and definitely with
[19:43] like Fable for example temple and that
[19:47] that discovery is actually another part
[19:50] of what's been in the early days of
[19:52] anthropics DNA
[19:54] and I think is also continuing to be a
[19:57] big part of how we operate in product in
[20:00] labs and and across research. This makes
[20:03] me think about something Gary Tan's been
[20:05] talking about uh president of YC. I
[20:07] don't know what his title is. uh he's he
[20:09] had this interesting point that if
[20:11] you're willing to spend $100,000 a year
[20:13] right now in tokens, you are living the
[20:16] way somebody in 2028 is going to live
[20:19] because by then it'll be really cheap.
[20:20] Everyone can work this way. But if you
[20:22] there's this alpha opportunity right now
[20:23] to just live in the future, go crazy on
[20:26] token spend. Uh and so there's a big
[20:28] opportunity for people to learn what the
[20:30] future's like and also just build much
[20:32] faster. Thoughts on this idea of and the
[20:35] value of token maxing, let's call it.
[20:37] Yeah, I think I I take more of like a
[20:40] almost product lens. It's almost like
[20:42] token spin is more the input and really
[20:44] the output is what you described of
[20:46] experimentation
[20:48] and I think if we were orienting like
[20:51] goals around experimentation. I feel
[20:53] like that that might be the better
[20:55] framing of the outcomes and therefore
[20:57] there might be different ways of
[20:58] achieving that outcome. I will say
[21:01] internally some of the most creative
[21:04] thinkers, the best like prototypers do
[21:07] spend a lot of time with Claude with
[21:09] every new version of a research model
[21:12] that we have. And so there is something
[21:15] around you have to be like using the
[21:18] models to then come up with good then
[21:22] great than better ideas and there's no
[21:25] substitute for that. um it's very hard
[21:28] to come up with a perfect strategy
[21:31] without touching the technology when
[21:33] it's moving this quickly.
[21:35] At the same time, I think there's other
[21:37] things that we could be doing like so
[21:39] one thing that we um do a lot is
[21:43] actually working in public at internally
[21:45] within anthropic. And so in the early
[21:48] days when we had less product surfaces,
[21:51] there was a slack channel where everyone
[21:54] almost the entire company was testing
[21:57] early versions of Claude and trying
[21:59] different use cases. Like people were
[22:01] not calling them use cases, but you
[22:02] might be asking it to edit an essay or
[22:06] uh to come up with the right way to send
[22:09] this email. Like they were all different
[22:10] use cases, but we all worked in public.
[22:14] And then what you would see magically is
[22:18] different users or different different
[22:20] folks on the team coming up with an idea
[22:23] and then other people trying different
[22:24] variations of that idea and then within
[22:27] maybe
[22:29] 10 or so requests there was something
[22:32] magical or potentially a new use case
[22:34] that emerges. And I think there's a lot
[22:38] in not just individuals figuring out by
[22:41] themselves how to use this technology. I
[22:43] think we could be doing more to actually
[22:45] bring like that communal discovery when
[22:48] we do experimentation. Like
[22:50] experimentation is not always
[22:52] necessarily a individual sport.
[22:55] >> It's so interesting. Yeah. This idea
[22:56] that we're just we're not sure what this
[22:58] is capable of or what we could do with
[23:00] it and it takes all this poking around
[23:02] and people trying things, hearing what
[23:04] other people are trying to figure out
[23:06] what's possible. such an interesting I
[23:08] don't know technology or just like okay
[23:10] here's what oh I figured out it could do
[23:12] this thing what are you gonna do with
[23:13] that
[23:13] >> I think at a broad theme we know right
[23:15] we know that the models to write great
[23:17] essays or you can write long form
[23:18] writing but individual pain points of
[23:21] what can you actually solve with that
[23:24] and bring it to like a user level that
[23:26] people can use um I think is something
[23:28] that is more exploration or
[23:30] experimentation
[23:32] uh based
[23:33] >> following this thread you uh you oversee
[23:36] product for the labs team which uh is
[23:39] extremely cool. We've had Ben man on the
[23:40] podcast, Mike Griger who whom both work
[23:42] on labs now talk about labs. What is
[23:45] labs? What's come out of labs? Many
[23:49] people have heard of these things and
[23:51] how do they work that enables them to
[23:53] create such innovative ideas outside of
[23:56] even the core anthropic product team.
[23:57] The thesis of labs in many ways is
[24:01] identifying and pulling the thread on
[24:03] the thread of discontinuous large bets
[24:07] that might not be in the core road map
[24:11] and figuring out is there a there there
[24:13] and also what is the 10x 100x a
[24:17] thousandx of the there there
[24:21] and so for example uh things like cloud
[24:24] code um I think
[24:26] >> I've heard of
[24:27] [laughter]
[24:28] uh things like cloud code uh things like
[24:32] uh skills and most recently cloud design
[24:36] MCP the thing that we really try to
[24:39] emphasize within the teams is especially
[24:42] right now there are so many things that
[24:44] could be built what does it mean then to
[24:46] have a discontinuous bet and I think one
[24:51] approach that we're taking this year is
[24:53] you can be very strongly held opinion
[24:56] about the theme or the area and then
[24:59] more weekly held about the exact
[25:01] prototype. And so like there is a
[25:04] culture of experimentation.
[25:06] Um there's a lot of the bottoms up like
[25:09] engineers on the team are very selfable
[25:13] um self-driven to test out different
[25:14] ideas and sometimes uh we have a thesis
[25:18] and it might not work yet and so we then
[25:21] might revisit it in one to two model
[25:23] generations. And so this idea of like
[25:26] these prototypes that actually end up
[25:29] just helping us learn like that's also
[25:31] valuable even if it doesn't lead to
[25:33] something immediately shipping. And so I
[25:36] think that allows the incubation and
[25:38] like the charter of labs to really
[25:40] accelerate and see around corners more
[25:42] broadly for anthropic. It's so funny to
[25:45] think about a labs within an anthropic
[25:47] which is already so innovative and and
[25:49] creative and just you know shipping like
[25:51] crazy that there's value to still
[25:53] creating a labs team within anthropic.
[25:56] What enables labs to work as well as it
[25:58] has because you listed all these
[26:00] products and it's let's like what else
[26:02] has anthropic shipped it like feels like
[26:04] all the biggest wins almost. I'm sure
[26:05] there are many that I'm not thinking
[26:06] about right now. What's what's kind of
[26:08] core to creating a successful labs or
[26:10] within within a larger company? I think
[26:13] that team culture like similar to
[26:16] broadly at anthropic I think that team
[26:18] culture is very valuable. I think Ben
[26:22] sets an uh incredible vision and pushes
[26:26] people to think about the 10x 100x of
[26:29] the idea and you know our the teams the
[26:34] pods within labs is small. Sometimes
[26:36] these ideas start with one engineer,
[26:39] right? And I think uh sometimes when
[26:43] there's almost really large teams
[26:46] pursuing very ambiguous large ideas, you
[26:49] end up actually being slowed down
[26:52] because of that. Um so I think it's
[26:55] culture. I think you know we actually
[26:58] also select for
[27:01] folks who actually want to do that zero
[27:04] to one experimentation and it's not
[27:06] easy. There's a lot of bets that we end
[27:08] up turning down or turning off. Um and
[27:12] maybe you know we revisit them in the
[27:14] future. Uh but that's hard. That's hard
[27:17] when you pour your heart and soul.
[27:18] You're acting as a founder for a bet and
[27:20] it's not working yet. Um so I think it's
[27:23] like that type selecting for that type
[27:25] of personality folks who are really
[27:28] passionate and deep about the zero to
[27:29] one.
[27:30] >> So you lead product for the research
[27:31] team. You work with the researchers at
[27:33] anthropic. A lot of people kind of get
[27:35] an sense of what is research what are
[27:36] research what researchers do. I think a
[27:38] lot of people don't totally understand
[27:39] these very valuable people uh at all the
[27:42] AI labs. Uh the way I think about it and
[27:44] I want to help people understand help me
[27:47] understand just what are researchers
[27:48] doing all day. What I imagine is they
[27:50] have a hypothesis for how to improve the
[27:51] model. They find data, they tweak some
[27:55] algorithms, they check adjust how it's
[27:57] trained, and they test it, see how it
[28:00] did, keep iterating, and keep trying to
[28:01] find ways to improve the model. Is that
[28:03] roughly right slash help us understand
[28:06] what researchers are doing all day?
[28:08] >> That's really I I think that's a lot of
[28:12] uh maybe the the like the more
[28:13] day-to-day. I think one piece around uh
[28:17] researchers and like research
[28:20] organizations like at anthropic is
[28:23] there's also a vision of the future like
[28:26] more broadly. So for example things like
[28:29] uh I think even at the founding of the
[28:32] company researchers were talking about
[28:34] how do we get cla to you use a computer
[28:37] how do we get AI to like navigate a
[28:39] screen right so there's a lot of
[28:41] actually very founderlike energy is how
[28:44] I describe it within researchers or
[28:46] really bold and ambitious researchers
[28:49] um and we have a ton of those at at
[28:51] anthropic so there's one layer of
[28:55] vision of what this technology can go
[28:58] and then I think on this other side of
[29:00] the loop there's also now that this
[29:02] technology or cloud is in people's hands
[29:05] how do we make it better today so it's a
[29:07] medium and long term and a lot of energy
[29:10] thinking about that lens of the future
[29:13] and also in the immediate and short term
[29:15] what are the improvement areas we can
[29:17] make and so like I think you're
[29:19] describing a really good sense of how do
[29:22] we make iterative improvements on
[29:24] different versions of claude
[29:26] the way that like my team works with
[29:29] researchers is kind of being very
[29:31] integrated and embedded in in those
[29:33] loops particularly areas where there's a
[29:36] lot of impact on users. So this is
[29:39] things like vision, computer use,
[29:43] coding, agent coding, tool use, test
[29:46] time, compute, things where there's a
[29:48] direct user impact and then figuring out
[29:52] what are the ways to
[29:55] uh bring the user feedback and ground it
[29:59] in a level that is understandable for
[30:02] user uh for researchers and also
[30:05] actionable for researchers. And I think
[30:08] that's the second piece is actually a
[30:11] big part of the job and sometimes a hard
[30:13] part of the job. So for example, we
[30:16] might get feedback on cla.ai. Claude
[30:19] hallucinated.
[30:21] It's very vague. If you bring that to a
[30:23] researcher and you say, "Please fix
[30:26] Claude from being hallucinated." It's
[30:28] not very actionable. And so part of the
[30:31] time of the team is understanding, okay,
[30:33] what's the trajectory of why that user
[30:36] gave that feedback? And it's like
[30:37] consented. And so we we we look at okay
[30:41] what should Claude have called tools in
[30:44] that moment or from its current
[30:46] knowledge or it called the right it
[30:48] looked at the right document but it
[30:50] looked at the wrong facts. In the first
[30:53] case that would have been a failure on
[30:55] tool use. On the second case it would
[30:58] have been a failure on let's say search
[31:00] or knowledge and search and search
[31:02] synthesis or it could be something
[31:05] around alignment. And so bring that
[31:07] level of detail to researchers
[31:11] coming up with like is this a big enough
[31:13] problem figure out things like evals to
[31:16] then describe how we've improved it like
[31:19] those are the levels of actionability
[31:21] and it's the day-to-day language of the
[31:24] researchers. And so we try to stay very
[31:26] close to how to bring that in an
[31:29] actionable manner uh between users to to
[31:32] the core model training and the research
[31:34] development loop.
[31:36] >> I was talking to someone the other day
[31:37] about how feels like research AI
[31:40] research is uh the place to be now if
[31:43] you want to be very successful in life.
[31:46] What does it take to become a really
[31:47] successful researcher from what you can
[31:49] tell uh you know not everyone can get in
[31:51] not everyone's brain is going to work
[31:52] this way but just say people are like
[31:53] hey I want to explore this career path
[31:55] from what you've seen what does it take
[31:57] to to make it there
[31:59] >> researchers generally are research and
[32:01] product managers working with research
[32:02] or both
[32:03] >> let's do both but uh the researchers
[32:06] like you know PM's working researchers
[32:07] also going to be very successful but it
[32:09] feels like everyone's trying to you know
[32:11] poach all the top researchers across
[32:13] every company so just I I know you're
[32:15] not an AI researcher, but just from what
[32:17] you've seen, just like what does it take
[32:18] to make it in that in that career path?
[32:21] >> Yeah, I think a lot of the most
[32:24] successful researchers and research
[32:26] leadership at Anthropic are folks who
[32:29] are really strong first principles
[32:31] thinkers about problems. Like they
[32:33] reason through problems really well. um
[32:37] who are just passionate about their
[32:39] research area and have a bold
[32:43] description of what that could look like
[32:46] and then who are actually close to the
[32:48] details and so uh you know our like
[32:53] leadership our chief scientists our
[32:56] heads of like fine-tuning and like RL
[32:58] folks are actually really close to the
[33:00] training runs and actually look at
[33:03] things like how the training run is
[33:06] eval looking at the underlying data. So
[33:09] like actually staying really close and
[33:11] be excited to be in the details I think
[33:14] have been like a sign of like really
[33:16] strong researchers and developing taste.
[33:19] And
[33:20] I think like another piece is just like
[33:23] their ability to think big over time and
[33:26] be like very ambitious, right? like the
[33:28] Dario like we can transform software
[33:31] engineering and and and the and I think
[33:34] uh going in that direction you learn so
[33:37] much you get you had to shoot for the
[33:40] stars in in in many ways across u your
[33:44] ideas I think in order to be a a
[33:47] successful researcher
[33:48] >> I I love just this meme of just be more
[33:50] ambitious comes up so often now which is
[33:53] so hard like it's it's easy to say that
[33:55] it's hard to actually just like how big
[33:56] can you
[33:58] and how that's so much of what AI now
[33:59] unlocks. Just be more ambitious.
[34:01] >> Yeah.
[34:02] >> Yeah.
[34:03] >> I think it's
[34:05] thinking through it once or twice and to
[34:07] end and then being I think stubborn
[34:12] about the uh area and maybe more uh
[34:17] loose around the exact like approach. Um
[34:23] it it is a question we challenge
[34:24] ourselves with. uh but the technology is
[34:28] moving so quickly and so how do you make
[34:30] sure what you're building is actually uh
[34:34] forward compatible
[34:37] and so it's also actually part of like I
[34:39] think the core product development loop
[34:40] to think bigger right uh one thing I ask
[34:44] the team frequently or how I think about
[34:47] when we're building a product is let's
[34:50] say claude 8 comes around what do what
[34:53] changes in what users do and then what
[34:57] should what does that mean for how
[34:58] you're building today? Is it going to be
[35:00] forward compatible to that experience,
[35:02] right? So like just grounding it's I
[35:04] think um being ambitious is very broad
[35:08] and so trying to like ground it in in
[35:10] some ways of describing describing that
[35:12] >> and also yeah everything heading in a
[35:14] direction that all is cohesive and makes
[35:16] sense versus just ambitious in a
[35:18] completely different direction. Speaking
[35:19] of ambition and cloud8, uh, Fable Mythos
[35:23] recently feels like hit this very new
[35:26] kind of tipping point with models where
[35:29] it used to be you have an awesome model,
[35:32] release it. Hey everyone, welcome.
[35:33] Opus45 is out, everyone can use it.
[35:36] Mythos went in a very different
[35:37] direction. It got blocked. There was a
[35:39] lot of scrutiny, a lot of concern about
[35:41] what it was capable of. Uh, all the
[35:44] companies had to go make sure it wasn't
[35:45] going to hack into all their systems.
[35:47] And it feels like now every model
[35:50] because they continue to get better will
[35:52] now have a lot more scrutiny and there
[35:54] will be more restrictions on who can use
[35:56] them which feels like a big deal. How do
[35:59] you think about that? How does that
[36:00] change the way you operate?
[36:02] >> I'm going to maybe leave the policy and
[36:04] the export control side to to folks that
[36:08] um own that and work on that. Um I think
[36:10] the product question and how we interact
[36:13] with these internally is I think as you
[36:16] mentioned as frontier models become more
[36:19] capable the safeguards and the ways of
[36:22] red teaming and testing and the
[36:25] pre-release process uh also needs to
[36:28] evolve and adapt quickly to to address
[36:30] that. And so one example is you know
[36:35] before fable models we didn't have as
[36:38] strong of let's say fallback UX's and
[36:41] systems because our our our goal was to
[36:44] make sure that like there is
[36:46] asymmetrical benefit for this technology
[36:49] and to minimize like the downside or
[36:52] like a severe risk of of it. And so we
[36:56] ended up building like fallback systems
[36:58] so that users will still get a great
[37:01] response from Opus 4.
[37:04] And so I think there's a piece around uh
[37:08] as we evolve and like improve safety
[37:10] systems. How do we continue to develop
[37:12] and deliver great user experiences?
[37:15] I think there's more that we can do on
[37:18] both sides. And so you'll see us
[37:20] innovating, improving on what we call
[37:23] now the model safeguards package uh more
[37:26] and more in the coming coming weeks and
[37:28] months.
[37:29] >> What's really interesting and just like
[37:30] unexpected here is creates this really
[37:32] interesting advantage for anthropic
[37:34] where you have access to the latest
[37:35] stuff and this is going to happen at
[37:37] every lab. Everyone's going to keep
[37:39] improving and it's it creates this
[37:40] unfair advantage within the labs to have
[37:42] access to the best stuff that other
[37:43] people can't yet outside of your
[37:45] control. You'd prefer everyone use it.
[37:47] So it's a really interesting this new
[37:48] feedback loop that's going to start
[37:50] where models that are so advanced are
[37:52] only accessible to certain companies and
[37:54] that's going to be a whole new unexpect
[37:56] it's like a second order effect of of
[37:57] all these restrictions. Our goal is to
[37:59] be uh to develop these systems and the
[38:01] models to be as inclusive as possible.
[38:04] Um I think our goal is to not have that
[38:08] happen uh for the general purpose
[38:10] general use like technologies and to
[38:13] make it more accessible. I think, you
[38:15] know, it this is like one of our top
[38:17] priorities right now to kind of reduce
[38:19] what we're seeing there.
[38:20] >> Yeah, that makes sense. I would imagine
[38:22] you'd want as many customers if people
[38:24] using this thing as possible. This
[38:26] episode is brought to you by Mercury,
[38:28] radically different banking, loved by
[38:30] over 300,000 entrepreneurs and now with
[38:33] command. I've been a customer of
[38:35] Mercury's for over 6 years. I have never
[38:37] once thought about leaving. Mercury is
[38:39] basically what happens when banking is
[38:41] built by product people, not by bankers.
[38:44] They make it so easy, dare I say fun, to
[38:47] send invoices, move money [music]
[38:49] around, set up virtual cards for folks
[38:51] on my team. Does your bank have an API,
[38:54] a terminal native CLI or an AI ready MCP
[38:57] server? I don't [music] think so. And
[38:59] just recently, they launched Command, a
[39:02] conversational interface built directly
[39:04] into Mercury, which acts as your
[39:06] financial operator. I've been using
[39:07] command to transfer money around to
[39:09] figure out what categories I've been
[39:11] spending the most money in, analyze my
[39:13] cash flows, and just today I used it to
[39:15] find out how much I've made from a
[39:17] specific sponsor over the past year. I
[39:19] just ask, [music] "How much have I made
[39:21] from X over the past year?" 10 seconds
[39:23] later, I have an answer. It is so
[39:25] freaking cool. Visit mercury.com to
[39:28] learn more and apply online in minutes.
[39:30] Mercury is a fintech company, not an
[39:31] FDIC insured bank. banking services
[39:34] provided through choice financial group
[39:35] and column NA members FDIC. I want to
[39:38] talk a little bit about how the product
[39:41] role is changing and who who is doing
[39:43] well in this new world uh now that AI is
[39:46] such a core part of uh of our life. When
[39:50] you're hiring PMs, product people, when
[39:53] you're looking at people that do well in
[39:55] today's world, what are some things that
[39:57] you notice? What are you looking for
[39:58] more most? What are you looking for
[40:00] more? What's kind like trending up in
[40:01] what you find is important and what's
[40:03] kind of trending down? We actually on my
[40:05] team have not changed our hiring loop uh
[40:09] for three years now. Um
[40:13] so what we actually look for and the
[40:16] traits and how we evaluate uh
[40:19] generalists like PM's generalist like
[40:21] research product managers have actually
[40:23] been the same. Um so I think some of
[40:27] those traits number one is first
[40:30] principles thinking
[40:32] and this is really uh rather than
[40:35] pattern matching what you used to do in
[40:38] let's say consumer product or B2B SAS
[40:43] um but actually figuring out in this
[40:45] moment for this user group with this
[40:47] technology what what is the user value
[40:50] >> is there an example that a lot of people
[40:52] hear first principles thinking they're
[40:53] like yes I about it. I'm good at this.
[40:55] What is what's an example of someone
[40:56] having really demonstrated really good
[40:58] first principles thinking?
[40:59] >> I think one example is I think you think
[41:02] of a product manager as I own product
[41:05] strategy and delivering user value as
[41:09] but I demonstrate day-to-day by writing
[41:12] a PRD or writing a product vision doc.
[41:16] And for for my team as like research
[41:20] product managers, the way to drive user
[41:22] value is to figure out the right user
[41:25] feedback, the evals,
[41:29] right? That then can be a
[41:31] personification of that user need. So
[41:36] like we do write some product documents
[41:40] and PRDs, but we actually have a saying
[41:42] on the team of evals are the new PRDs,
[41:45] right? because in order to deliver that
[41:47] user value uh it's not that exact
[41:49] artifact that people used to write in
[41:51] the last like one to two decades it's a
[41:54] new way of working and so the first
[41:57] think principal thinking would be let me
[41:59] figure out what is the thing I should do
[42:02] to achieve my goals rather than here is
[42:05] a set of activities that I've done and
[42:08] therefore I will continue to do
[42:10] >> so the idea here is used to be have kind
[42:12] of an idea create a PRD talk to people
[42:15] about it. Align on the plan, design it,
[42:17] build it, ship it, see how it goes,
[42:19] iterate. What I'm hearing here is it's
[42:21] like, okay, here's some feedback about
[42:23] something that's wrong or an
[42:24] opportunity. Step one is the eval is now
[42:27] how you define what the work is versus a
[42:31] PRD.
[42:32] >> Maybe maybe step one would be uh
[42:35] understanding the user painoint. And so
[42:39] the way to even access that user
[42:40] painpoint is different, right? In the
[42:42] past, we might do a user interview and I
[42:45] think if you go like deep enough, you
[42:47] you might have the user walk you through
[42:49] their user flow, the pixels. Here, you
[42:52] have to sweat the tokens as much as you
[42:55] sweat the pixels. And so, one activity
[42:58] we have on the team is reading the
[43:00] transcripts and understanding
[43:04] uh what was the trajectories that failed
[43:07] very deeply to then say was this like a
[43:10] hallucination? was this claw being
[43:13] overconfident. So like the theme of the
[43:15] failure actually has a lot of nuance
[43:18] and then that allows you to build a
[43:21] description
[43:23] a like sustained description of that
[43:26] painoint.
[43:27] Uh so that could be essentially in a new
[43:30] eval and is the eval on distribution
[43:34] right is it capturing both the positive
[43:37] situations where this is failing and
[43:39] also areas when it should actually not
[43:42] fail and then bring that back to let's
[43:45] say research so then we can make the
[43:47] improvements and actually measure the
[43:49] quality of okay when we have opus 5.5 is
[43:54] this area improving or not is claude now
[43:56] able to uh identify the right places in
[44:00] the document uh and pull the right
[44:03] synthesis out. So it's just the
[44:05] actionability like and and shortening
[44:08] the distance to actionability
[44:10] um for for our stakeholders and partner
[44:13] teams like researchers um to take action
[44:16] on.
[44:16] >> Is there an example of something like
[44:18] this where you found an issue or
[44:20] opportunity and then wrote the eval? And
[44:22] what is what is the eval looking like in
[44:24] in most cases? uh what when people want
[44:26] to picture an eval what is that what is
[44:28] what do they picture?
[44:29] >> We actually uh pioneered this concept
[44:31] within anthropic. So uh one of the early
[44:34] examples is the early cloud models were
[44:38] not very good at following specific
[44:41] schemas. So like things like outputs and
[44:43] JSON and uh now that is fundamental to
[44:48] claude being able to be a good agent.
[44:51] Right? if you can't output a certain
[44:53] format, you don't know how to like
[44:54] access APIs, you can't call tools, etc.
[44:58] And so the initial uh end to end was I
[45:03] was hearing feedback around you know
[45:05] claude 2 days claude was not very good
[45:08] at following instructions. So then
[45:10] digging in with users, what do you mean
[45:13] by claude is not good at following
[45:14] instructions? Give me what situations
[45:17] this was happening like what's the exact
[45:19] like paragraph? what did you ask? What
[45:21] was Claude's response? Going to like
[45:23] that level of detail. And what I saw was
[45:27] something like 80% of what people meant
[45:29] in the early days for this failure was
[45:32] Claude would not write the right JSON.
[45:35] And so then, okay, let's generate maybe
[45:38] to start just 30 to 40 examples
[45:42] of when Claude was not doing this thing
[45:44] correctly. And then that actually is
[45:47] your eval set. And you could have
[45:49] essentially uh a prompt and a response.
[45:54] And if that is not working uh in the
[45:58] right golden answer that you might have,
[45:59] then that means that the the eval
[46:01] essentially uh is beneficial because
[46:04] it's identifying a painoint
[46:06] consistently. And so then we added that
[46:08] to our um repositories for evals. And
[46:13] when we have uh versions of claude, we
[46:17] actually run that eval and just check. I
[46:19] think at this point it's always 100% or
[46:22] like 99.9. And so it's no longer a pain
[46:25] point. Uh but in the early days was
[46:27] taking the user feedback, figuring out
[46:29] actually what they mean, can we
[46:31] reproduce it, is it consistent, is it a
[46:33] big issue, and then figuring out how to
[46:37] uh standardize it in a way that can be
[46:39] consumable for researchers. It's
[46:42] basically test-driven development for
[46:44] PMs is is the world we're living now. Uh
[46:46] where you write the test first. So is
[46:48] this just a core part of the product
[46:50] management job now at Enthropic writing
[46:52] bells?
[46:52] >> I think so. I I also think it's um
[46:56] something I've talked to other Piana
[46:59] other companies about and I think it's
[47:01] also more and more of the skill set more
[47:03] broadly because a lot of the products
[47:06] that we're building is at the
[47:07] intersection of models with harnesses
[47:12] with a set of contexts for a set of
[47:14] users. And so having things like eval
[47:18] isn't is a way not just for uh folks
[47:22] working on models but generally within
[47:24] product uh to to get to better user
[47:27] experiences because you can't improve
[47:29] what you can't measure and a lot of this
[47:31] is very still tactile based. It's still
[47:34] very judgment based and so you have to
[47:36] stay close to the details
[47:38] >> and also very non-deterministic which is
[47:40] a big part of this just like it's not
[47:42] going to give you the same answer every
[47:43] time. So you got to describe it kind of
[47:45] more broadly. It's not going to be yeah
[47:47] an exact match. So this is a really
[47:49] interesting change in the way product
[47:50] happens and will happen is eval
[47:55] is is a big part of this. Do you guys
[47:56] still do PRDS? Is there still like a one
[47:58] pager describing a problem or is it
[48:00] play? Okay, now you're shaking your
[48:01] head. Yes,
[48:02] >> we we we are we do I think um when
[48:05] there's a very defined problem I think
[48:07] things like eval might be almost a
[48:08] shorthand. I think there's other cases
[48:11] where PRDs are really valuable. Um, PRDS
[48:15] are great vehicles for getting a very
[48:18] large group of people aligned on a set
[48:21] of sources of truth about experience and
[48:24] setup goals. So when we do have a model,
[48:27] we actually for every model we do have a
[48:29] PRD less necessarily for our researchers
[48:32] but more for our growing product
[48:36] surfaces, for our engineering teams, for
[48:40] our um stakeholders like uh legal and
[48:45] safety and others as just a source of
[48:47] truth of putting together what we're
[48:49] aiming to achieve so that a big group of
[48:51] people can row in the same direction.
[48:54] The other place where I do think PRDS
[48:57] are valuable are on the more ambiguous
[48:59] problems and opportunities right so we
[49:02] if we haven't shipped a thing like
[49:04] computer use we don't necessarily have a
[49:06] set of like user specific pain points
[49:09] always and I think there's value in the
[49:11] product vision portions of a PRD to
[49:14] explore
[49:16] what could even if a technology is not
[49:19] yet ready to work for everyone how do
[49:23] you get it to work well for some group.
[49:25] So you can explore the value, you can
[49:29] actually bring something that is uh
[49:32] coherent to a user group. So we do have
[49:35] PRDS. Um I think the application is a
[49:38] little different now.
[49:39] >> Okay, this is great. There's I just had
[49:41] a uh Andrew for he's the head of the
[49:43] codeex app at OpenAI and he's you guys
[49:45] are aligned. Uh PD is not dead. Still
[49:47] very useful for specific projects and
[49:50] ideas. Uh great. Okay, we've closed
[49:52] closed the book on purity is still
[49:54] kicking. Okay, so we've been talking a
[49:57] bit about just what kind of skills are
[49:58] kind of emerging for product people. Um,
[50:01] is there anything else that you find is
[50:04] shifted in what patterns
[50:07] uh are common across people that are
[50:09] doing well in this new AI world in terms
[50:11] of product managers and folks on the
[50:13] product teams? Is there anything else
[50:14] that you're like, okay, does something
[50:15] you got to shift or something you look
[50:17] for more people? I think maybe
[50:19] specifically
[50:21] uh for
[50:24] folks who might be midc career or folks
[50:27] who have been more in a managerial like
[50:29] product like leadership seat. Um, one
[50:32] thing that I think I feel pretty
[50:35] strongly about is in order to be good
[50:38] managers of teams
[50:40] and PMs working with this technology,
[50:43] you have to be really hands-on
[50:45] yourself and have spent not just time
[50:49] tinkering but actually shipping with
[50:51] this technology and and and again being
[50:54] in the details and sweating the tokens
[50:59] along with your PMS and your engineer.
[51:02] and your teams. And so
[51:06] even for folks that I hire who have more
[51:08] tenure PM experience, the onboarding
[51:11] plans are exactly the same as somebody
[51:14] who is like more uh early career and
[51:17] it's around understanding users, reading
[51:21] like consented user feedback, talking to
[51:24] customers. I think there's something
[51:26] around
[51:28] uh being able to like understand what to
[51:31] do with this, what what good looks like
[51:34] and having developed that in a very
[51:36] hands-on manner. That's important. Um
[51:39] it's not necessarily easy for someone to
[51:44] uh
[51:46] agree or be able to see what a what a
[51:48] good or great AI product or AI feature
[51:51] could look like if they haven't kind of
[51:53] experienced building
[51:56] themselves. Um, so I think I think there
[51:59] is a I I I do feel pretty strongly that
[52:02] like, you know, if you're a manager, you
[52:05] have to be hands-on. You have to spend a
[52:06] portion of your time actually shipping.
[52:09] You you have to kind of walk in the
[52:10] shoes of your teams. uh and and that's I
[52:14] I always try to carve out a portion of
[52:16] time uh to to actually like own one to
[52:19] two work streams when we have models in
[52:22] order to keep like keep my theory of
[52:24] mind, keep my sense of how the models
[52:27] are moving, how quickly it's improving
[52:30] uh uh so I can help the team make make
[52:33] decisions and and make better decisions.
[52:35] So, what I'm hearing here is if you're
[52:36] not, no matter where you are in the
[52:38] ladder of hierarchy at a company, if
[52:40] you're not building yourself, if you're
[52:42] not actually talking to Claude, talking
[52:43] to Codex, building stuff, you're not
[52:45] going to make it.
[52:46] >> And you should have fun working with his
[52:48] technology. I think that's the other
[52:49] piece. I think the folks that would be
[52:51] most successful regardless of their
[52:53] level are people who love working with
[52:56] AI and and are exploring and
[53:00] experimenting and carving out the time
[53:03] not just for the experimentation but
[53:05] actually hands-on shipping end to end
[53:08] getting the user feedback I think has to
[53:10] be fundamental for everyone.
[53:12] >> I 100% know what you mean there. Just
[53:14] like me sitting on my newsletter and
[53:16] this podcast just talking about stuff
[53:17] and like yeah that sounds great. Like
[53:19] every time I actually build something
[53:21] and I tinker with all kinds of little
[53:22] projects, you're just like, "Okay, I see
[53:24] what's happening here." And you just get
[53:25] so much more, it's like hard to exactly
[53:27] describe what you're what you what you
[53:29] experience actually working with the
[53:31] models and building stuff, but it's like
[53:32] a whole different world of like, "Okay,
[53:33] I see. Here's where the here's what
[53:34] they're talking about computer use.
[53:36] Here's what they're talking about with
[53:37] this limitation, this UX situation."
[53:39] >> Yeah.
[53:39] >> So, yeah. So, it's just like, and you
[53:42] made this really interesting point that
[53:43] you have to have fun with it, which is
[53:46] not easy for a lot of people because
[53:48] they're pushed to use AI or they just
[53:50] don't know exactly what to do with it.
[53:52] For people that are just like, I don't
[53:53] know, it's just so annoying. I just have
[53:55] to do this. I don't know what's so like,
[53:57] I hate this freaking thing. Why do I
[53:59] have to work with this? Things are
[54:00] changing so much. I'm tired. Uh, advice
[54:02] for helping people find that find that
[54:04] joy in this work. I think maybe I'll
[54:07] reemphasize something I said earlier
[54:09] around just that experimentation is not
[54:12] an individual sport. Like some of the
[54:14] moments where I think I've touched
[54:17] practically every version of research
[54:19] models across
[54:21] 20 versions of production clause at this
[54:24] point and
[54:26] I think part of the joy comes from
[54:28] seeing other people discover use cases
[54:30] too. And so maybe one idea here would be
[54:35] pairing with somebody who is excited
[54:38] and seeing what
[54:41] on a use case that you care about and
[54:42] and working together versus um uh
[54:47] identifying or trying to figure out the
[54:49] perfect use case yourself because that
[54:51] might feel like work. Working with
[54:53] others feels like joy a lot of the time.
[54:56] And is there more that we could do to
[54:57] bring that bring other people along?
[55:00] That's something like a lot of times
[55:02] internally we have somebody who is like
[55:04] very curious and them sharing an idea of
[55:07] a new prototype actually brings a ton
[55:09] more people who are like oh I didn't
[55:11] know this could work now with claude and
[55:14] so there's just some virtuous cycles
[55:15] here um and and ways of yeah bring
[55:20] continue to have joy with with this
[55:21] technology.
[55:22] >> That's such a good point. I think that's
[55:24] also why Twitter's so useful for a lot
[55:26] of this is you see other people sharing
[55:28] what they've done
[55:30] >> and it inspires you to come up with your
[55:32] own little ideas and also it's just like
[55:33] fun to share your own thing that you've
[55:35] done.
[55:36] >> So that's a really good point just like
[55:37] find other people to kind of play around
[55:38] with and look for use cases. The thing
[55:41] I've also heard a lot is just find like
[55:42] a problem you want to solve in your life
[55:44] or work and just open up cloud cloud
[55:46] code tell it here's what I want to do
[55:48] and it's incredible how far you can get
[55:50] just with like a vague idea of a problem
[55:52] you want to solve. Yeah. I think it gets
[55:54] hard in that there's so many different
[55:55] things that you could try.
[55:57] >> Yeah.
[55:57] >> And so you just like narrowing in on
[56:00] either pairing with someone, working
[56:02] with somebody who who is who have a lot
[56:04] of joy about this technology or figuring
[56:07] out something that you could immediately
[56:09] find value. Like either of them those
[56:12] things allow you to go deeper rather
[56:14] than like more high level about too many
[56:17] things. Um I I find it hard to keep pace
[56:21] with the number of prototypes or
[56:23] products that are out there and so my
[56:26] lens has been how do I go deep in one to
[56:28] two of them
[56:30] >> myself. That's uh that's so interesting
[56:32] you say that because that's exactly it.
[56:33] We just had this survey uh that I I ran
[56:36] with uh my colleague Noam uh asking my
[56:39] readers just how they're feeling about
[56:41] all the things going on in the tech
[56:42] right now and AI and uh one of the most
[56:45] interesting takeaways we had was uh to
[56:47] find that happiness is exactly what you
[56:49] said is go deep in a couple things
[56:52] versus trying to just ton of little
[56:53] things. find a couple things to really
[56:56] solve well and then go deep and that is
[56:58] a source because a lot of the happiness
[57:00] people feel is when they finally
[57:01] unlocked a way for AI to actually make
[57:03] their lives better versus just like a
[57:05] couple messed up broken half working
[57:07] things.
[57:08] >> Yeah, it's it's um how do you go from
[57:10] this being a check the box, right? And
[57:14] so like us as product people, it's then
[57:17] a exercise of product prioritization of
[57:20] your time and your energy. And and if
[57:22] the goal is to experiment with joy, then
[57:25] how do you what are the inputs that you
[57:27] need for that? Um, but yeah, I I I think
[57:32] a lot of the um I think the secret sauce
[57:36] of anthropic is the culture and the
[57:38] bottoms of nature of how people work and
[57:41] this like experimenting in public.
[57:44] Um, and by doing that, it's very much
[57:48] about how to bring other people along.
[57:52] Um, that ends up being, I think, really
[57:54] valuable. Yeah, I've heard this so many
[57:56] times from all the labs just like no no
[57:59] no one's exactly sure how some of this
[58:01] is going to be used and a lot of it is
[58:03] just putting stuff out early, seeing how
[58:04] people use it, seeing what it's what's
[58:06] possible and then using that information
[58:08] to build the actual product to lead in.
[58:10] >> Yeah. Yeah.
[58:11] >> I'm curious how kind of on this thread
[58:13] of finding ways AI for AI to help you in
[58:15] your work in life. Are there any
[58:17] interesting ways you've been using
[58:19] Claude lately in your work as a as a PM?
[58:21] I think there's a lot of things with um
[58:25] you know fable and things like tag. So
[58:29] there there I think tag is um in in the
[58:32] very like early days I think there's
[58:34] something around how you work in a
[58:36] different paradigm of allowing this an
[58:38] agent to go off and work and then bring
[58:40] back uh product and experiences to you.
[58:44] I think one area that it's not very
[58:46] recent, but one that um I bring up a lot
[58:50] with the team and I think we could do
[58:53] more on using AI is just like how to use
[58:57] it to also be more uh
[59:01] to have better conversations with each
[59:03] other to be better managers.
[59:05] I don't think it's necessarily
[59:08] uh just about raising the IQ of like
[59:11] experiences we build, but also I used it
[59:14] a lot and actually like prepping for how
[59:17] to have better conversations
[59:19] um in the moment during like crucial
[59:21] conversations. So, I love that book and
[59:23] so I actually have a skill that helps me
[59:25] figure out am I having am I going in the
[59:28] right level of detail given the the
[59:31] situation at hand and actually helping
[59:33] me be a better manager and better
[59:34] supporter for the team. Um, so for for
[59:38] like managers on the team, that's
[59:40] actually a thing that I've been sharing
[59:42] more with with a uh with our managers of
[59:45] okay, how how do you actually use use
[59:47] claude to to to make you a better coach
[59:50] >> because it's hard sometimes to find the
[59:52] right perfect words and the models have
[59:54] a lot of perfect and right words and
[59:57] >> uh I think there is something about how
[59:59] how it can actually augment us from like
[01:00:01] an ET perspective in addition to you. Oh
[01:00:04] man, there's so much interesting stuff
[01:00:06] there. So just to understand what you're
[01:00:07] doing there. So you built a skill.
[01:00:09] You're just like Claude build a skill
[01:00:11] pulling in lessons from Crucial
[01:00:13] Conversations the book which it knows
[01:00:15] enough about. You don't have to even
[01:00:16] give it the content. And then you use
[01:00:18] that skill to talk to Claude. Hey, I
[01:00:20] have this very difficult conversation
[01:00:21] coming up with a colleague.
[01:00:23] >> Give me some tips on how to approach it.
[01:00:25] >> Yeah. And it's it's a great uh it's
[01:00:29] almost like uh coaching like
[01:00:33] individualized personalized coaching of
[01:00:35] just how to make you and and there's so
[01:00:37] much context switching that we do all
[01:00:38] day and having like Claude help me pair
[01:00:42] and help me and maybe there are times
[01:00:45] where I end up not using suggestions
[01:00:47] from Claude. Uh but it actually is uh
[01:00:50] ends up being very helpful for for just
[01:00:53] coming up and brainstorming. Am I
[01:00:55] thinking about reactions in the right
[01:00:58] way? How do I actually uh go a bit
[01:01:01] deeper faster? Build trust faster, uh be
[01:01:04] more direct.
[01:01:05] >> Yeah, man. I have so many questions
[01:01:06] here. This so interesting. Uh one is
[01:01:09] just like there's concern people are
[01:01:10] going to start talking the way AI writes
[01:01:13] because they're talking AI so much and
[01:01:14] it's going to be like Diane, it's not
[01:01:16] this, but it's that. Uh I know that
[01:01:18] you're not doing that, but that's a you
[01:01:19] know, a concern people have. Let me just
[01:01:22] ask about that, I guess. Do you fear
[01:01:23] this? There's this, you know, brain rot
[01:01:25] atrophy stuff people talk about it.
[01:01:27] We're just so reliant on AI now and we
[01:01:29] stop learning and thinking and, you
[01:01:32] know, overly AI thoughts on that being
[01:01:34] so close to it and being so integrated
[01:01:36] with with AI constantly.
[01:01:38] >> A lot of actually thinking process and
[01:01:40] writing process are tied together for me
[01:01:42] personally. And so I think
[01:01:46] there are ways where I use claw to
[01:01:48] augment my thinking. But what I want to
[01:01:51] make sure and maybe this is what you're
[01:01:52] describing is Claude doesn't take over
[01:01:54] all of my thinking for me. And so I
[01:01:58] think depending on the situation,
[01:01:59] depending on how much more personal
[01:02:01] judgment I want to have in a situation,
[01:02:04] I might uh um come up with my own POV
[01:02:09] first and then work with Claude through
[01:02:11] that. Um and making sure that like I
[01:02:15] maintain my sense and tone throughout. I
[01:02:19] think there are then other things like
[01:02:21] updates right we have like monthly
[01:02:23] business reviews and then in those cases
[01:02:26] it's much more I want actually want it
[01:02:28] to be standard and I want it to be much
[01:02:31] more like it gets a cris crystallized
[01:02:33] information in the right way and maybe
[01:02:35] and I have a skill and like we're
[01:02:36] augmenting and improving our skill for
[01:02:38] that but I want to get a to a place
[01:02:40] where like the monthly business review
[01:02:42] the writing of that is potentially
[01:02:47] asymmetrically less
[01:02:49] valuable than the thinking and so how do
[01:02:51] I get that piece delegated to claude
[01:02:54] fully and I'm more of a reviewer and a
[01:02:57] verifier of that information. So I think
[01:02:58] it depends on like what you're using
[01:03:01] Claude for and what you're trying to
[01:03:02] convey and like is there is there
[01:03:06] asymmetrical value in in delegating more
[01:03:10] to Claude.
[01:03:11] >> What I'm also hearing the first tip is
[01:03:12] really great which was think first have
[01:03:15] a point of view and then kind of use
[01:03:17] Claude as a sparring partner almost to
[01:03:19] evolve the idea push back on the idea.
[01:03:22] >> Yeah. Yeah. And I think this is where
[01:03:24] things like actually our alignment
[01:03:26] research and safety research is helpful
[01:03:28] because it what you don't want is like a
[01:03:32] AI that just agrees with you, right?
[01:03:34] What you want is this technology to
[01:03:36] actually augment and grow and like get
[01:03:38] to a better outcome. And so sometimes
[01:03:41] it's
[01:03:42] having Claude push back makes me better.
[01:03:45] And so that's great. like a co-orker, I
[01:03:49] want somebody to push back when my ideas
[01:03:51] are not fully formed.
[01:03:53] >> I want to hear more about that. But I've
[01:03:54] heard that when Ben man was on the
[01:03:55] podcast, he talked about the
[01:03:57] constitution that is built into Claude
[01:03:59] and how unintuitively the work and the
[01:04:03] focus on safety and alignment as you
[01:04:05] said and this constitution that
[01:04:07] describes how Claude should think and
[01:04:10] operate that actually you would think
[01:04:12] that would limit the abilities of Claude
[01:04:15] and make it less fun and interesting.
[01:04:17] It's exactly the opposite. Claude is the
[01:04:20] most interesting personality. I hear
[01:04:21] that constantly. It's just like I much
[01:04:23] prefer talking to a like open claw
[01:04:25] famously was built on claude and then
[01:04:28] people were forced to we won't get into
[01:04:30] it were forced to switch to and
[01:04:32] they're like this is so bad this is not
[01:04:34] who I'm used to talking to. Uh so that
[01:04:36] is I think a really interesting point I
[01:04:38] just want to make sure we spend a little
[01:04:39] time on. Why is it why is that the case
[01:04:41] just this focus on alignment safety
[01:04:43] having this clear constitution? Why does
[01:04:45] that make Claude better and and more
[01:04:47] interesting to talk to? Also,
[01:04:49] >> in order to make Claude as like
[01:04:51] intelligent and as capable as possible,
[01:04:54] being able to have Claude actually push
[01:04:57] back in the right points and then add
[01:05:01] it's like a yes or no and actually helps
[01:05:05] you come to a better conclusion. So,
[01:05:09] I've used Claude to help with things
[01:05:10] like, are we making the right pricing
[01:05:12] decision on the next version of Claude?
[01:05:15] It's a little bit meta, but using a
[01:05:17] research version of Opus, asking it to
[01:05:20] figure out how it should price and being
[01:05:22] able to come out with better outcomes is
[01:05:25] a goal at the end of the day. And so
[01:05:28] having AI not just be an assistant, not
[01:05:31] just be a doer, not and being delegated
[01:05:36] task, but figuring out is it doing the
[01:05:38] right thing. That's actually very
[01:05:40] integrated with knowing when to push
[01:05:42] back,
[01:05:43] >> right? That's part of knowing when you
[01:05:45] should be proactive. Proactivity is not
[01:05:48] a necessarily always doing a thing that
[01:05:51] you are scheduled to do. It is knowing
[01:05:53] when to come up with a new idea. And so
[01:05:55] in order for Claw to be more useful, the
[01:05:59] general approach has to be that it knows
[01:06:02] when to push back. It's a core part of
[01:06:05] the characteristics together uh of the
[01:06:08] models.
[01:06:09] >> That is so interesting. It's so
[01:06:11] interesting that that is what a big part
[01:06:12] of like it be it being less compliant is
[01:06:15] almost what makes it better and more
[01:06:16] useful because we need that. Like I've
[01:06:19] had so many people where they're like,
[01:06:20] "Hey, like AI told me I was right." and
[01:06:22] like no I wish I wish to other people.
[01:06:26] >> Yeah. And it comes back to our earlier
[01:06:28] point around thinking, right? How do you
[01:06:30] protect your thinking?
[01:06:31] >> Um if you have a AI that can be a
[01:06:34] thinking partner, a thinking partner
[01:06:37] doesn't just agree with you. It should
[01:06:39] add to you and you should come away at
[01:06:42] the end of the day having better ideas
[01:06:45] because you worked with Claude. That
[01:06:47] should be the hero goal, not just making
[01:06:49] your ideas 10% better. Yeah, I love this
[01:06:52] since like it used to be think 10x. I
[01:06:54] used to be the the way you know founders
[01:06:57] push people like what if we 10x this and
[01:06:59] I love what I keep hearing is like it's
[01:07:00] like how do we go thousandx from this
[01:07:02] idea? What is the most ambitious version
[01:07:04] of this? I want to come back to
[01:07:06] something that I I was thinking about as
[01:07:07] we were talking about uh talking to
[01:07:09] Claude constantly. Um it's very clear
[01:07:12] when AI has written something still.
[01:07:14] It's funny that it's a large language
[01:07:16] model. you would think of all things it
[01:07:18] would be very good at writing and
[01:07:19] interestingly just no AI is very good at
[01:07:22] writing it's always very clear this was
[01:07:24] AI written
[01:07:26] do you think we'll get to a place where
[01:07:29] we will not know this was AI
[01:07:32] >> I think it depends on what's the
[01:07:35] uh goal that you're looking to achieve
[01:07:38] by knowing yeah uh what's the eval um I
[01:07:42] actually do think there's more that we
[01:07:45] could be doing on making Claude write
[01:07:46] better. There's actually very active
[01:07:49] efforts um on on my team and on the
[01:07:52] research side about making Claude write
[01:07:54] better. Just generally I think it should
[01:07:57] be clear where an idea is ident is being
[01:08:02] led by you or by you Lenny or me Diane.
[01:08:06] I think it really depends on uh what's
[01:08:10] the goal of that writing. like for
[01:08:12] something like a monthly business
[01:08:14] review, I would actually love to have
[01:08:17] that end to end be written by Claude.
[01:08:21] Uh,
[01:08:21] >> and obviously and not make it feel like
[01:08:23] it was written by a human. It's such an
[01:08:24] interesting point you're making like is
[01:08:26] it actually better for us to know that
[01:08:28] it's AI versus not.
[01:08:29] >> Yeah. But but it's it's um but it's also
[01:08:34] for maybe the lens is more around like
[01:08:36] verifiability or who's verifying
[01:08:40] >> the output. Right. Right. like who's
[01:08:42] signing off. Uh maybe less around who's
[01:08:44] writing, but who's verifying who's
[01:08:46] signing off. That becomes like more what
[01:08:48] matters than who's writing it.
[01:08:52] >> Why Why do you think AI is not great at
[01:08:55] writing? Like my guess is it has studied
[01:08:58] all of the best writing in all of
[01:09:00] humanity. It's figured out here's the
[01:09:03] best way to write. And now that we and
[01:09:05] it's just there's only so many ways to
[01:09:07] to write. And so we've just recognized,
[01:09:09] okay, this is what AI does. It has these
[01:09:12] tropes. Is that the core of it? Is there
[01:09:14] something else that's keeping it from
[01:09:15] being a great writer? Ironically, being
[01:09:17] a large language model of all things,
[01:09:19] you think it'd be really great at
[01:09:20] language.
[01:09:21] >> I think part of it is also uh we need to
[01:09:25] invest more in training improvements to
[01:09:28] make AI continuously strong on areas
[01:09:31] like writing. Um I think it's also
[01:09:35] like the technology is jagged edged like
[01:09:37] like we mentioned. So sometimes when the
[01:09:40] models were good at writing but not
[01:09:41] agentic our our thesis is how do we make
[01:09:45] the models more agentic or call the
[01:09:46] right tools. Now that that's improved a
[01:09:48] bit then it's well now these other areas
[01:09:51] actually become more of the rough edges.
[01:09:54] And so I think we're in one of those
[01:09:55] moments with writing where uh we need to
[01:09:59] actually just focus and prioritize on
[01:10:02] training the models to be like great at
[01:10:04] this area and like that is an active a
[01:10:07] very active area for us that you
[01:10:10] mentioned.
[01:10:11] >> Okay. I'm glad I'm glad. And also uh
[01:10:14] it's going to be interesting once AI is
[01:10:15] so good we're like I don't know who
[01:10:16] wrote that but um to your point
[01:10:18] sometimes we actually want to know that
[01:10:19] it's AI. That's really interesting. I
[01:10:20] never thought of it that way. The other
[01:10:22] interesting part of this is that there's
[01:10:24] that comedian who was joking that we're
[01:10:25] like on a plane and the Wi-Fi is down
[01:10:27] and we're just like, "What the hell? The
[01:10:29] Wi-Fi is not working on this plane. The
[01:10:31] sucks. How dare you?" When you're like
[01:10:33] in a in a tube in the sky flying like a
[01:10:35] bird and uh how dare you complain that
[01:10:38] the Wi-Fi doesn't work. Like your point
[01:10:39] is there's so much advancement and so
[01:10:42] much power. Uh we can't fix it all. We
[01:10:44] can't make it all work the best
[01:10:47] possible. And so uh basically AI writing
[01:10:49] has been not the priority and it feels
[01:10:51] like there's more investment happening
[01:10:52] there.
[01:10:53] >> Yeah, I think like tone and character is
[01:10:55] a priority. I think it's this
[01:10:57] advancement of the technology is a work
[01:11:00] in progress and so we made we we see a
[01:11:04] leap or emergence of like a jump in
[01:11:08] agentic behaviors and so that is a new
[01:11:11] normal and then these other capabilities
[01:11:14] needs to continue like improving
[01:11:16] >> and I think once we improve let's say
[01:11:19] writing and like tone and character uh
[01:11:22] we probably will say like
[01:11:24] >> how do we have Claude be even more
[01:11:25] proactive like productivity is an
[01:11:28] opportunity and that's human nature like
[01:11:30] we want to make ourselves better. We
[01:11:32] want to make this technology better. Um
[01:11:35] so yeah I I think we're applying it to
[01:11:37] to AI which is the right thing. We
[01:11:39] should be making it better.
[01:11:41] >> I want to ask you a couple questions I'd
[01:11:42] like to ask folks working at the very
[01:11:44] center of the future of that is coming.
[01:11:47] Um one is where do you think human
[01:11:50] brains will continue to be most valuable
[01:11:53] over the years? I know anthropic's
[01:11:55] mission and and vision is we'll reach a
[01:11:58] GI a super intelligence. So in the
[01:12:01] future maybe nowhere but before we get
[01:12:03] there where do you think human brains
[01:12:05] will continue to be most valuable as
[01:12:07] we've approached that that timeline?
[01:12:09] >> We started to talk about making claude
[01:12:12] and models better at judgment um
[01:12:16] especially in the last um year or so. I
[01:12:20] think judgment is one and is an area
[01:12:22] where it's an accumulation of so much
[01:12:25] nuance and so much experience and these
[01:12:29] systems haven't experienced as much as
[01:12:31] humans have and so I think that
[01:12:34] hard-earned
[01:12:35] like judgment is a a a area for for
[01:12:40] product leaders and just generally um
[01:12:43] will continue to be really critical.
[01:12:45] There are so many things AIs can build.
[01:12:48] which one are the things that you know
[01:12:51] an or like lab should build right a lot
[01:12:53] of that requires like human judgment
[01:12:55] persistence so proactivity these are all
[01:12:59] traits that are beyond just general
[01:13:00] capabilities but just behaviors and
[01:13:02] characteristics of like people at that
[01:13:06] level of like how do you get to the best
[01:13:08] solutions how do you create the the best
[01:13:11] experiences so I think those types of
[01:13:13] traits are actually the tactile uh
[01:13:16] traits that I think will
[01:13:18] uh continue to be important. Um
[01:13:22] I think there is also
[01:13:24] uh still a lot of like capabilities and
[01:13:27] subject matter expertise as well. I
[01:13:30] think you know software engineering has
[01:13:33] been really transformed by AI. I think
[01:13:35] there's areas like uh biology, life
[01:13:39] sciences. These are all things that um
[01:13:42] we're just kind of at like the foot of
[01:13:44] the exponential on like maybe software
[01:13:47] engineering. We're on the exponential on
[01:13:49] some of these area other areas. We're
[01:13:51] not quite there yet. And so um I think
[01:13:53] you're seeing us ship things like cloud
[01:13:56] science investing in these areas because
[01:13:59] those are areas that um I think is just
[01:14:03] bring the this technology to society and
[01:14:06] having a positive benefit for society.
[01:14:09] So I think there's a lot more to go
[01:14:10] there.
[01:14:11] >> Another question I want to ask is um as
[01:14:13] someone with kids, how do you think
[01:14:15] about what you are encouraging them to
[01:14:20] learn? or do you think you're gonna
[01:14:22] nudge them to be successful in this wild
[01:14:26] new world that we're entering?
[01:14:27] >> I actually think it's a lot of the same
[01:14:28] traits like you and I probably grew up
[01:14:31] with, which is
[01:14:33] >> curiosity for learning, persistence,
[01:14:37] believing in your own inner voice,
[01:14:39] developing, and then believing in your
[01:14:41] own inner voice. Like I have a
[01:14:44] four-year-old, I have a 8-year-old. It's
[01:14:46] on us to help uh it's on me to help them
[01:14:49] develop their indoor voice and whether
[01:14:52] that's being opinionated and taking a
[01:14:56] stance to me right and developing that
[01:14:59] encouraging that uh I think that those
[01:15:01] types of skill sets are things that um
[01:15:04] is important in the future and like
[01:15:08] having their own individual voice.
[01:15:10] >> That is so interesting. It's so related
[01:15:12] to the answer you had when I asked about
[01:15:14] how to avoid a brain rot essentially and
[01:15:16] overrelying on AI which is just keep
[01:15:20] focused on your own point of view and
[01:15:21] your own perspective before you overly
[01:15:23] AI and just this idea you're describing
[01:15:25] of building that in kids is is really
[01:15:27] important. Uh that is so interesting and
[01:15:29] I love how this all this kind of
[01:15:30] connects judgment persistence in a point
[01:15:33] of view of your own.
[01:15:34] >> Yeah.
[01:15:35] >> Both for kids and also adults.
[01:15:36] >> Yeah. Anything we think about um for
[01:15:38] your
[01:15:39] >> Oh man. Well, like the question I'm
[01:15:40] thinking about is just when to get them
[01:15:42] on like some AI thing, you know, when I
[01:15:44] have a three-year-old, so it's pretty
[01:15:46] early for that, but you know, how do you
[01:15:48] get how do you onboard them to this
[01:15:50] crazy thing? I had I was at an event
[01:15:51] recently and bunch of parents were
[01:15:53] talking about how they think about AI in
[01:15:54] their kids and one person had a really
[01:15:56] interesting approach which is uh keep
[01:15:59] them on the very early models so that
[01:16:01] they still have to struggle a bit and
[01:16:03] not get all the answers immediately.
[01:16:06] thought that was interesting. Like an
[01:16:07] open source local model,
[01:16:08] >> not stable.
[01:16:10] >> Yeah.
[01:16:10] >> Yeah.
[01:16:11] >> Yeah. And curiosity is something uh I I
[01:16:14] keep mentioning Ben man, but his answer
[01:16:16] actually to this question has always
[01:16:17] stuck with me, which is um curiosity and
[01:16:20] also just like he's a big fan of
[01:16:21] Monosuri, which is what I'm we're
[01:16:23] encouraging for our kids. So, there's
[01:16:25] something there. Maybe a last question
[01:16:28] just along kind of along these lines,
[01:16:30] something Fiona Fun actually suggested
[01:16:31] to ask you uh who's recently on the
[01:16:34] podcast. How do you stay just recharged
[01:16:36] and not burn out being in the center of
[01:16:37] this crazy storm of AI as a mom uh
[01:16:41] working in, you know, we're seeing the
[01:16:44] research work at Enthropic. Uh I just
[01:16:47] like we're living through the most
[01:16:48] unprecedented time working at just like
[01:16:51] being, you know, being on the outside of
[01:16:52] Anthropic. It's crazy. I don't even know
[01:16:54] what it's like to be on the inside. Um
[01:16:55] what have you learned about avoiding
[01:16:57] burnout, staying recharged, staying sane
[01:16:59] during the middle of all this? In 2024,
[01:17:02] we shipped four models for the in the
[01:17:05] whole year or four series of models and
[01:17:08] I think we did more than that volume in
[01:17:10] just Q2 of this year.
[01:17:13] [laughter]
[01:17:14] I think I've been really lucky with uh
[01:17:18] the team that we grown and built both
[01:17:20] the stakeholders on the research side
[01:17:22] and within our research product
[01:17:25] management team. Um I think that one of
[01:17:28] the magical parts about approaching all
[01:17:32] of this is that it's not an individual
[01:17:34] sport. Um there's like a sense of
[01:17:37] radical ownership and team collaboration
[01:17:43] that I think
[01:17:46] sometimes it does feel like a high
[01:17:47] performance sport because you're in very
[01:17:50] critical decisions. there's new
[01:17:52] information about users about training
[01:17:55] and you have to make recommendations and
[01:17:57] judgments and decisions very quickly and
[01:18:00] nobody can do that sustainably by
[01:18:02] themselves. Um, and so I think what's
[01:18:06] really helped is having a team that is
[01:18:10] incredible, who looks out for each
[01:18:13] other, who, you know, night before a
[01:18:15] launch, even if they're not the core
[01:18:17] DRRi on that model, will stay up and
[01:18:20] help the DRRi, who uh to review the blog
[01:18:23] post and make edits and come up with
[01:18:25] better demos and knowing to be each
[01:18:28] other's sort of extra hand. I think it's
[01:18:31] very easy if you take all of this change
[01:18:33] on your own shoulders to feel like
[01:18:36] you're alone and to feel like you have
[01:18:38] to do everything. Uh but I think one of
[01:18:41] the like magical parts of anthropic is
[01:18:43] this ability for us to
[01:18:47] uh figure out what are those
[01:18:49] opportunities to help each other and
[01:18:51] actually then taking the next mile of
[01:18:52] like mindmelding. We called it like
[01:18:55] entering the hive mind. There was an
[01:18:56] article about this and I think like part
[01:18:59] of that is just that allows like the
[01:19:01] team to replenish. It's not that you I I
[01:19:04] was just on PTO in June. It's not just
[01:19:06] that you can take PTO and you come back
[01:19:08] to like 3x the amount of things to do.
[01:19:11] It's actually that you can take PTO and
[01:19:13] know the team can figure out the right
[01:19:16] things to do and that we individually
[01:19:19] can like watch out for each other. Um so
[01:19:22] I think that's a big part. I'm really
[01:19:24] lucky just personally um also my partner
[01:19:27] is really supportive um this is year six
[01:19:30] of me working in AI so Amazon and then
[01:19:33] anthropic and so he sees how much I just
[01:19:35] love the technology and what this can do
[01:19:38] and that really helps I think also um
[01:19:41] from like a personal perspective as
[01:19:43] well.
[01:19:44] >> I love I love how many of these answers
[01:19:46] connect. So what I'm hearing here is
[01:19:48] just the having other people, working
[01:19:50] with other people, relying on other
[01:19:52] people, helping each other out when
[01:19:54] things get crazy. Uh which is a similar
[01:19:57] answer you had for just how to how to
[01:19:59] find the joy and and and fun in this
[01:20:01] work. Just get be inspired by other
[01:20:03] people, see what they're doing,
[01:20:05] >> work together.
[01:20:06] >> Yeah. And it's interesting when Fiona
[01:20:08] was on the podcast recently, she I was
[01:20:10] asking her just like what's changed in
[01:20:11] the world of software engineering and
[01:20:12] she pointed out it's a lot lonier now
[01:20:15] because now we're working with agents
[01:20:16] instead of other humans. Teams are
[01:20:18] smaller, people are have all these
[01:20:20] fleets they're talking to constantly.
[01:20:22] And so this is just a reminder of just
[01:20:23] the power of just actual other humans
[01:20:25] around you.
[01:20:26] >> We're we're asked to work and make
[01:20:28] decisions on really big things because
[01:20:31] you have more scale from the technology,
[01:20:33] right? And I think
[01:20:37] having individuals, having other folks
[01:20:40] more who can have some level of like
[01:20:43] mind meld with what you work on, how you
[01:20:45] approach maybe not exactly every detail,
[01:20:47] but what are the first principles? What
[01:20:49] are the assumptions you make then helps
[01:20:52] them uh you know back up for you or uh
[01:20:56] push your decision and sharpen your
[01:20:58] thinking. Um, so I think you know we
[01:21:01] really try to like I really try to look
[01:21:03] for that when like building the team,
[01:21:05] growing the team, hiring like is this
[01:21:07] person going to care about their own ego
[01:21:09] and building out a big org or are they
[01:21:12] going to care about contributing to
[01:21:13] anthropic and contributing to the like
[01:21:16] impact of the team and orienting towards
[01:21:19] folks who are like low ego team
[01:21:22] oriented. Um, I think that's,
[01:21:26] yeah, it it's a big part of I think the
[01:21:29] sustainability.
[01:21:30] >> Yeah, just always a lot of it always
[01:21:32] just comes down back to culture and
[01:21:34] hiring and and I know I've heard a lot
[01:21:36] just the reason Anthropic is able to
[01:21:38] move so fast. I remember that moment
[01:21:39] when like something shipped every day of
[01:21:41] the month. There's like a calendar of
[01:21:43] launches and people were talking about
[01:21:44] how is this possible and what I heard a
[01:21:46] lot is just because everyone is so
[01:21:48] aligned around the mission and the
[01:21:50] values it allows people to make
[01:21:52] decisions really quickly before we get
[01:21:54] to our very exciting lightning round. Is
[01:21:56] there anything else Dan that you wanted
[01:21:58] to share? Anything else you wanted to
[01:22:00] touch on? Anything you want to maybe
[01:22:01] double down on of things we've talked
[01:22:03] about?
[01:22:04] >> This was actually really fun because I
[01:22:05] feel like your questions actually
[01:22:06] sharpen some of my thinking around how
[01:22:08] the dots kind of connect. I'm I'm your
[01:22:10] real human claude over here.
[01:22:13] One thing that I really uh want to like
[01:22:17] convey or um have people take away is I
[01:22:21] think one in the ways of working, but
[01:22:23] also just two that like this is a
[01:22:29] this is a lot of like growth and change
[01:22:31] and having the joy in using this
[01:22:34] technology and like if you're feeling
[01:22:36] like in this moment you don't have as
[01:22:39] much of that feeling of initial joy, how
[01:22:41] do you find people who do
[01:22:44] uh if this is an area that that you're
[01:22:46] excited and like want to work on and I
[01:22:49] think developing skill sets replenishing
[01:22:52] skill sets in many ways of things like
[01:22:55] thinking from a first principles manner
[01:22:57] about what you solve I think
[01:22:59] fundamentally you didn't ask me this but
[01:23:01] there is this question in the community
[01:23:03] of do we still need PMS when the models
[01:23:06] are so capable when engineers are
[01:23:07] leaning in um I think the role of people
[01:23:13] who are user centric who go into the
[01:23:16] details of understanding what users are
[01:23:19] trying to accomplish bubbling that up in
[01:23:22] an actionable manner and doing the
[01:23:25] relentless work to do that like that to
[01:23:28] me is a core of a product person and I
[01:23:31] actually think we need more of that.
[01:23:33] I think we are becoming very technology
[01:23:38] layered driven and actually to make that
[01:23:41] impactful it's you have to go deep you
[01:23:43] have to be curious you have to be super
[01:23:45] hands-on and those are things that I
[01:23:47] think are also traits that have I think
[01:23:49] helped anthropic from a product
[01:23:51] development and model development
[01:23:53] perspective and as part of the culture
[01:23:55] and hopefully that's valuable for others
[01:23:57] as well.
[01:23:59] >> Amazing. What an inspiring way to end
[01:24:01] it. Oh man. Yeah. And this is I've been
[01:24:04] saying this too for a long time just now
[01:24:05] that building is easy
[01:24:08] the hard part part becomes as you said
[01:24:10] what should we build and is the thing we
[01:24:11] have built correct and good and worth
[01:24:13] leaning into and to me that's what PMs
[01:24:16] do and what PMs are good at.
[01:24:17] >> Yeah. Yeah. Yeah. And it's getting into
[01:24:20] the details of the user.
[01:24:22] >> Yeah. Empathy. Okay. Great. PMs are
[01:24:25] going to make it. Okay. PRD is not dead.
[01:24:28] [laughter] All kinds of all kinds of uh
[01:24:30] important lessons here. Uh Dan, with
[01:24:32] that we've reached our very exciting
[01:24:34] lightning round. I've got five questions
[01:24:35] for you. Are you ready?
[01:24:36] >> Yep.
[01:24:37] >> First question. What are two or three
[01:24:39] books that you find yourself
[01:24:41] recommending most to other people?
[01:24:43] >> One personal one I really like how to
[01:24:47] raise an adult.
[01:24:49] So uh
[01:24:52] I'm a mom. I think a lot about what is
[01:24:56] the things that I want to instill in in
[01:24:58] in my kids. in that book is really
[01:25:01] helpful for describing we're not trying
[01:25:02] to raise children, we're trying to raise
[01:25:04] adults. So just the framing of what does
[01:25:06] that mean and what does it mean? What
[01:25:08] are the characteristics that we want to
[01:25:10] hone and like harness and foster in our
[01:25:12] kids? Um the other book that I uh was
[01:25:16] listening to on Audible recently is
[01:25:18] Incorable by Eric Reese. So the
[01:25:22] >> Incorruptible Incorruptible Yes. Yes.
[01:25:24] >> Yeah. His recent podcast guest.
[01:25:26] >> Um Yeah. And I I I just I think the
[01:25:30] question of how to build great companies
[01:25:32] is important. I personally just been
[01:25:35] most fascinated with how to keep great
[01:25:37] teams and great companies going further.
[01:25:41] And it was very interesting to just kind
[01:25:43] of see his framing and reframing of the
[01:25:45] question. Um I loved some of the
[01:25:48] examples around having metrics around
[01:25:50] culture. you if you can't if you only
[01:25:53] measure revenue and then that's kind of
[01:25:56] how you're going against but if you have
[01:25:58] other better metrics that's actually the
[01:26:00] way uh to to to sustain the the values
[01:26:03] you care about. I've been kind of trying
[01:26:05] to think about how to actually bring
[01:26:06] that to the team level of like how do we
[01:26:08] better articulate right our norms a lot
[01:26:11] of the things we talked about on the
[01:26:12] team. So I think [snorts] that's also a
[01:26:14] really good read.
[01:26:15] >> There you go. Uh that'll be your next
[01:26:17] watch everyone as you're listening to
[01:26:18] this the Eric Greece episode. Yeah.
[01:26:20] >> Such a good episode. Yeah.
[01:26:22] >> And his book just came out.
[01:26:23] Incorruptible.
[01:26:24] >> Yes.
[01:26:25] >> And I think it was like a New York Times
[01:26:26] bestseller. Like it's actually doing
[01:26:28] incredibly well, which I was really
[01:26:30] happy to see.
[01:26:31] >> Yeah, exactly.
[01:26:32] >> Next question. Favorite recent movie or
[01:26:34] TV show you really enjoyed. Most people
[01:26:36] at Antropic don't have time to do what
[01:26:38] to watch things, but I'm curious if you
[01:26:39] have an answer. I would say um during uh
[01:26:43] some time off last month, I did get to
[01:26:46] like binge watch Fallout on Amazon
[01:26:48] Prime. So that was actually I kind of
[01:26:52] like um it's kind of uh Have you heard
[01:26:55] of it?
[01:26:56] >> Yeah. Yeah, it's based on the video
[01:26:57] game.
[01:26:58] >> Yes, it's based on the video game. Uh I
[01:27:00] think it's a it was really um it's
[01:27:03] witty, it's humorous, it's also like
[01:27:05] super actionoriented. So highly
[01:27:07] recommend.
[01:27:08] >> Okay, next question. Do you have a
[01:27:09] favorite product you recently discovered
[01:27:11] that you really love?
[01:27:12] >> I really do think like claw tag is very
[01:27:16] interesting in terms of a product
[01:27:17] experience. Um, we actually have like
[01:27:19] different versions of this uh within
[01:27:22] Anthropic and I I I think it's actually
[01:27:25] been really uh really really uh powerful
[01:27:28] tool.
[01:27:28] >> Yeah, it feels like I think some people
[01:27:30] are like what's the big deal? The fact
[01:27:32] that everyone at Anthropic is like
[01:27:34] raving about it tells me something
[01:27:35] important is going on here. And I'm
[01:27:37] trying to actually get it working within
[01:27:39] my Slack community that I have for paid
[01:27:41] newsletter subscribers. How cool would
[01:27:42] that be?
[01:27:43] >> Yeah.
[01:27:43] >> Yeah. I'm trying to figure out how it
[01:27:44] works when it's not a company when it's
[01:27:46] just a bunch of people that don't know
[01:27:48] each other and how that might work. But
[01:27:50] we're trying it out. Okay. Uh two more
[01:27:52] questions. Your favorite life motto that
[01:27:53] you find yourself often coming back to
[01:27:55] in work or in life. So I was actually
[01:27:57] raised by my grandparents uh for the
[01:28:00] first 10 10 years of my life and my
[01:28:03] parents were immigrant uh college and
[01:28:06] master students in the US.
[01:28:08] >> Oh wow. And um my grandfather always
[01:28:11] says, "No matter how far you go, there's
[01:28:14] always another level,
[01:28:18] [laughter]
[01:28:18] which uh um is I think um a really good
[01:28:24] way though, like a pretty uh intense way
[01:28:26] of describing uh his his life
[01:28:29] philosophy. But I go back to that
[01:28:31] whenever there's something new or
[01:28:32] unprecedented that we experience. And I
[01:28:35] think you know first half of this year
[01:28:37] there was definitely a lot of that like
[01:28:39] there was a lot of new things that we
[01:28:40] were learning. I was learning um so just
[01:28:44] feeling like there's always like another
[01:28:47] mountain another uh opportunity to
[01:28:50] >> not good enough Dan we need to go better
[01:28:53] >> we need to go bigger. Uh makes me think
[01:28:55] about actually another Ben man line from
[01:28:57] his podcast episode that this is the
[01:28:59] most normal it's ever going to be. It's
[01:29:01] only going to get weirder and crazier.
[01:29:03] >> Yeah. Yeah. No, we're good.
[01:29:06] Okay, final question. Uh, I was poking
[01:29:08] around at your LinkedIn. You were a high
[01:29:10] yield bond trader, JP Morgan Chase early
[01:29:13] in your career. Uh, you had like uh you
[01:29:16] have this like redacted uh hundred
[01:29:20] million dollar trading portfolio of some
[01:29:22] kind. Uh what did you learn from that
[01:29:25] time in your life that has stuck with
[01:29:27] you and or is there a crazy story from
[01:29:29] that period? It was four years of your
[01:29:30] life. I think I learned actually a lot
[01:29:33] that I uh apply here uh at at Anthropic
[01:29:37] and other uh jobs thereafter. Um so when
[01:29:40] I was at JP Morgan um the trading floor
[01:29:45] you could kind of envision like sort of
[01:29:47] Waffle Wall Street that's very
[01:29:48] different. Uh most traders I think are
[01:29:51] in front of a terminal. They're much
[01:29:53] more doing analyses uh on their
[01:29:55] computers. Um, but it's still very, I
[01:29:58] would say, like male-dominated.
[01:30:00] And so, uh, I was the only woman. I was
[01:30:04] the only, uh, um, person with like my
[01:30:08] background, uh, on the trading desk. And
[01:30:11] I learned that
[01:30:14] the it was a very good environment to
[01:30:17] kind of building one my sense of
[01:30:19] authentic self
[01:30:21] and two uh that even if I was the most
[01:30:25] junior person, even if I may look
[01:30:29] different, uh that the best ideas
[01:30:35] and having conviction in the best ideas
[01:30:38] uh irregardless of all of those other
[01:30:41] factors like is the most important
[01:30:42] thing. And so I think just bringing that
[01:30:45] sense of um how I show up more at work.
[01:30:50] Um I'm pretty vulnerable and authentic
[01:30:52] with my team. Uh I try to really make
[01:30:55] sure that regardless of people's levels
[01:30:57] or tenures, if they have a great idea,
[01:30:59] how to help them pursue that and to do
[01:31:02] also the same. Um so to like put the
[01:31:05] idea out there to actually um have
[01:31:08] conviction in it to do the follow
[01:31:10] through to do the like nitty-gritty work
[01:31:12] to make it happen. Um so those were all
[01:31:14] things that I learned from trading. Um
[01:31:17] and yeah I think applies to any any job
[01:31:19] in many ways.
[01:31:20] >> That is beautiful. Where can people find
[01:31:23] you online if they want to follow you
[01:31:26] and how can listeners be useful to you?
[01:31:28] >> I don't have a large presence on like uh
[01:31:32] social. Uh I think the best way to uh
[01:31:36] find my work uh my team's work is really
[01:31:40] uh the anthropic blog and when we're
[01:31:42] publishing new models, new product
[01:31:44] experiences I think in terms of uh
[01:31:49] useful uh for me I think the best thing
[01:31:52] number one is your feedback like we
[01:31:55] actually if if you thumbs up or thumbs
[01:31:58] down on any of our product surfaces if
[01:32:00] you contact your salesperson with
[01:32:02] feedback back about the model, it will
[01:32:04] make its way to me. Uh we actually with
[01:32:07] every like research model, I actually
[01:32:09] get pretty close into understanding
[01:32:11] favorability and feedback. Um so giving
[01:32:14] us that feedback, pushing Claude,
[01:32:16] telling us where it's falling down, um
[01:32:18] those help us make Claude better. Uh the
[01:32:21] other the other thing is like if you
[01:32:23] have folks in your network who seem like
[01:32:25] this type of profile of person that I
[01:32:27] just talked about I'm hiring the team is
[01:32:31] growing.
[01:32:32] We really will love just people who love
[01:32:35] this technology who are deeply curious
[01:32:37] first principles thinkers who are
[01:32:40] fearless in questioning assumptions um
[01:32:43] and who have like a tinkering hackery
[01:32:45] spirit.
[01:32:46] >> Wow dream job. So basically open open PM
[01:32:49] roles add anthropic on the research
[01:32:51] team.
[01:32:52] >> Yes.
[01:32:52] >> And they apply I assume on the website
[01:32:54] the careers page.
[01:32:55] >> Yes.
[01:32:56] >> Holy moly. All right. Here we go. Enjoy
[01:32:58] the flood of resumes you're about to
[01:33:00] receive.
[01:33:01] >> Thank you. [laughter]
[01:33:03] >> Uh Dan, thank you so much for being
[01:33:05] here.
[01:33:06] >> Thank you so much for having me. Thank
[01:33:07] you for um really helpful,
[01:33:10] thoughtprovoking questions um helping me
[01:33:14] even connect the dots on how how we
[01:33:16] work, how how this whole technology is
[01:33:18] coming together and being product people
[01:33:20] in it.
[01:33:21] >> I really appreciate that. But thank you
[01:33:23] Dan for real. Okay. Well, bye everyone.
[01:33:27] Thank you so much for listening. If you
[01:33:29] found this valuable, you can subscribe
[01:33:30] to the show on Apple Podcast, Spotify,
[01:33:33] or your favorite podcast app. Also,
[01:33:36] please consider giving us a rating or
[01:33:37] leaving a review as that really helps
[01:33:39] other listeners find the podcast. You
[01:33:41] can find all past episodes or learn more
[01:33:44] about the show at lennispodcast.com.
[01:33:47] See you in the next episode.
