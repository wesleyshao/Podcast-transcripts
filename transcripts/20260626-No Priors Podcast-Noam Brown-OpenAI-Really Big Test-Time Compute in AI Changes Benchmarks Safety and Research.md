---
访谈时间: "2026-06-26"
访谈时间说明: "未在公开视频元数据中确认单独录制日期，使用 YouTube 发布时间 2026-06-26。"
嘉宾名字: "Noam Brown"
嘉宾公司名称: "OpenAI"
播客名称: "No Priors Podcast"
播客url地址: "https://www.youtube.com/watch?v=AZrU6y3pUcU"
全文提及的关键名词:
  - "Noam Brown"
  - "OpenAI"
  - "test-time compute"
  - "benchmarks"
  - "safety evals"
  - "AI research"
  - "poker bots"
  - "latent capability"
  - "agent runtime"
  - "multi-agent coordination"
  - "model capability"
  - "cost-based evaluation"
youtube_video_id: "AZrU6y3pUcU"
YouTube发布时间: "2026-06-26"
播客标题: "Really Big Test-Time Compute in AI Changes Benchmarks, Safety and Research with OpenAI's Noam Brown"
字幕来源: "YouTube public subtitles: en-orig json3"
companies:
  - OpenAI
industries: []
technologies:
  - LLM
keywords: []
tags:
  - OpenAI
  - LLM
---

# Really Big Test-Time Compute in AI Changes Benchmarks, Safety and Research with OpenAI's Noam Brown

## Transcript

[00:00] With GBT3, you couldn't scale test time
[00:02] compute. Like if you gave it a budget of
[00:04] $10 million and said, "Okay, well, let's
[00:05] see what GB3 can do." It really can't do
[00:07] that much. The precurren frameworks and
[00:09] responsible scaling policies, they don't
[00:11] really account for the amount of testime
[00:12] compute. They just say, "Okay, well,
[00:13] what's the capability of the model?" The
[00:15] problem is we're in a world now where
[00:17] the capability of the model is a
[00:19] function of how much money you put into
[00:21] it. Basically, if you give it a budget
[00:23] of $10,000, it can do a lot more than
[00:26] what it can do with a budget of $10.
[00:27] Give it a budget of $10 million, you can
[00:29] do even more. At what budget should you
[00:31] evaluate these models? The policies that
[00:33] exist today don't really address that
[00:35] question.
[00:43] Hi listeners, I'm Sarah Goa and welcome
[00:45] back to No Priors. Today I'm here with
[00:47] Nome Brown, one of our godfathers of AI
[00:50] reasoning. We talk about the broken
[00:52] state of evaluations, very large-scale
[00:54] test time compute, how he thinks about
[00:57] recursive self-improvement, and what's
[00:59] next on the horizon for competition at
[01:01] the frontier. Welcome, Gnome. I'm so
[01:04] excited to have you back.
[01:05] >> That's great to be back. Yeah,
[01:06] >> you are our first guest. I'm very proud
[01:08] of my taste in friends and researchers
[01:11] for uh for the pod. um given you know
[01:14] how important uh you know inference time
[01:17] scaling has become to the industry you
[01:19] should be proud too having actually
[01:20] pioneered it
[01:21] >> played a part yeah among among many
[01:23] others
[01:24] >> you just wrote this essay that really
[01:27] resonated about large scale test time
[01:28] compute and why uh the industry is not
[01:32] evaluating these models as robustly as
[01:35] it should be what was the motivation for
[01:36] it
[01:37] >> yeah the motivation was we released 5.5
[01:40] and the initial reaction ction was kind
[01:44] of skepticism that it was a
[01:46] substantially better model. To be fair,
[01:47] that only lasted for a few hours before
[01:49] people had some time to play around with
[01:50] it and and try it out themselves and
[01:51] they saw that it was actually
[01:52] substantially better. Um, but I think a
[01:54] lot of the skepticism came from the
[01:57] benchmark grid that was published.
[01:58] Basically, whenever a new model is
[01:59] released, there's this benchmark grid
[02:01] where they show all these different
[02:02] benchmarks on on the x-axxis and then
[02:04] the performance of different models on
[02:05] the y- axis and you can just like
[02:07] compare different models. It's like a
[02:08] single number for a model on a single
[02:11] benchmark. And if you look on paper at
[02:13] the difference between like 5.5 and 5.4
[02:15] or or other models, it wasn't it was an
[02:18] improvement, but it wasn't a huge
[02:19] improvement. It was only a few
[02:21] percentage points in some benchmarks.
[02:23] So, people looked at that and they were
[02:24] skeptical that it was actually a better
[02:25] model. Um, once they played around with
[02:27] it, the story changed. I think the
[02:29] reason why it doesn't show up as so much
[02:32] better on the benchmarks is because the
[02:33] benchmarks are being presented, the
[02:35] benchmark results are being presented in
[02:37] the wrong way. They're not controlling
[02:39] for the amount of test time compute that
[02:41] is being used on that benchmark
[02:42] question. It turned out that 5.5 is just
[02:45] much more efficient with its thinking.
[02:46] If you run it at max settings, 5.4 is
[02:50] thinking for a lot longer. It takes
[02:51] longer to get back a response than 5.5.
[02:54] And once you control for the amount of
[02:55] thinking time, actually you can see that
[02:57] 5.5 is a substantial jump over 5.4. That
[03:00] is, I think, people's day-to-day
[03:01] experience with it. And then when I
[03:03] mention this to people the reaction, the
[03:05] typical question I get is like okay well
[03:06] why not just have 5.5 think for as long
[03:08] as 5.4 and the question is like well how
[03:11] long should they think for? Typically
[03:12] the response I get is well until the
[03:14] performance plateaus right there's at
[03:16] some point where the performance on the
[03:17] benchmark is going to plateau and you
[03:18] evaluate to that point. The thing is the
[03:20] point at which it plateaus is actually
[03:22] really far out these days. I mean, it
[03:24] was true in GBD3 land back in 2022, the
[03:27] models couldn't really think
[03:28] productively for that long. And so, you
[03:29] could just run them until they plateau.
[03:31] It's not that far away. But what we're
[03:34] seeing today with the modern models is
[03:35] that 5.5 and other models can think for
[03:39] if you scaffold them reasonably well,
[03:41] can think for weeks even um before
[03:45] having performance plateau on some of
[03:46] these benchmarks. And so, the point at
[03:48] which they plateau is simply too far out
[03:51] to reasonably test. we all need to
[03:53] actually reinforce um either like a
[03:55] patience limit or a budget limit from a
[03:58] token perspective now and that wasn't
[03:59] true a few years ago.
[04:00] >> Exactly. And so I think the proper way
[04:02] to and so my claim is the proper way to
[04:03] evaluate the models now is you either
[04:06] have some kind of budget for the
[04:08] benchmark whether it's tokens or cost or
[04:10] time or whatever or you plot the
[04:12] performance as a function of the amount
[04:13] of test time compute that's going into
[04:15] the model and then it becomes much more
[04:17] clear um how to compare the performance
[04:18] between these different models.
[04:20] >> Given the model evaluation cycle and the
[04:23] fact that performance does not asmtote
[04:26] for many tasks over um quite a long
[04:29] period of time. What do you do about
[04:31] that issue? The fact that some of the
[04:33] evals that you would want to run are
[04:36] both beyond the scope of budget or time
[04:38] that's reasonable given the current
[04:39] model release cycle.
[04:40] >> I mean, I think for things like cyber,
[04:42] we've seen and actually the AIS um in
[04:45] their evaluations has shown that the
[04:48] models continue to improve um at 100
[04:51] million tokens. You know, if you run
[04:53] them for 100 million tokens, they're
[04:54] still improving at beyond that point.
[04:55] >> And that can take a very long time to
[04:57] run. But you also do see that like the
[05:00] performance is is it's not just like a
[05:03] discontinuous jump. It's actually like
[05:05] you can see the slope of improvement
[05:06] over those 100 million tokens. And so
[05:08] you could you could probably do some
[05:11] kind of uh evaluation up to a certain
[05:13] budget and then just say okay well this
[05:15] is what we project the performance to
[05:17] look like. And I think this this there
[05:19] hasn't been a lot of research on this
[05:20] yet. I actually think this would be a
[05:21] great paper to publish if there's any
[05:23] academics out there looking for
[05:24] something to research. Can you predict
[05:26] what the performance looks like at an
[05:28] inference budget of let's say $10,000
[05:30] only using inference budgets up to 10 or
[05:33] 10 or $100?
[05:34] >> So maybe an orthogonal question for you.
[05:37] Uh do you think users are systematically
[05:39] like not thinking long enough with their
[05:41] models about problems?
[05:42] >> What do you mean by not thinking long
[05:44] enough? um if the if you can
[05:47] build an agent or control the amount of
[05:51] um test time compute being used like
[05:52] there's there's what is done by the
[05:54] model itself and there's what the user
[05:56] can do. Um do you think that like you
[05:59] know the industry is using test time
[06:01] compute an optimal amount uh way
[06:03] undershooting it or it's you know it's a
[06:04] problem in the models where they just
[06:06] need to be able to do that thinking
[06:07] faster.
[06:08] >> I I think it depends on the problem. Uh
[06:11] I think this idea that the models you
[06:14] just let them think for a week or
[06:15] whatever and then they respond. It's it
[06:17] sounds nice and yes the benchmarks look
[06:19] great but it's not very practical when
[06:21] working u because like okay you ask the
[06:23] model a question and then you sit there
[06:24] for a week waiting for it to come back
[06:25] to you.
[06:26] >> I think what people have have found most
[06:29] effective is to kind of like iterate
[06:31] quickly with the models and so the
[06:32] thinking time I think needs to be
[06:35] flexible. when it makes sense to respond
[06:37] quickly to the user, it should respond
[06:38] quickly. And then when it makes sense to
[06:39] think for a long time and the user wants
[06:41] it to think for a long time, then it
[06:42] makes sense to think for a long time. I
[06:43] think people have been striking the
[06:44] right balance given what they have to
[06:46] deal with right now.
[06:47] >> How would you characterize, you know,
[06:49] there's a lot of talk about benchmark
[06:51] maxing and the ability to game different
[06:53] benchmarks? What would you characterize
[06:55] the like landscape of benchmarks as
[06:57] today? And then do you have like
[06:59] favorites that you think are more
[07:00] indicative of capability than others? So
[07:03] the benchmark maxing thing is also
[07:05] motivation for for writing the essay
[07:06] that I think it's really easy to show
[07:10] you can do much better than previous
[07:12] benchmarks or or previous previous
[07:14] models on benchmarks by just for example
[07:17] scaffolding a bunch of models together.
[07:18] Um so if you say okay well we're going
[07:20] to instead of just running this model
[07:22] once we're going to run it five times
[07:23] and take the best of the five responses
[07:25] or like ask a judge which one it thinks
[07:27] is best then you can get much higher
[07:29] scores than that model. And so it's
[07:32] really easy to make something that looks
[07:35] a lot better on paper but is actually
[07:37] not better once you control for the
[07:38] amount of test time compute. That is one
[07:39] thing that I'm worried about when it
[07:40] comes to benchmark maxing. I mean it
[07:41] like it's it's a little misleading is
[07:43] the only concern that I have. And then
[07:45] as far as like the benchmarks
[07:46] themselves, I think there is always a
[07:48] risk of like just optimizing for the
[07:50] benchmark. And I've I've certainly
[07:53] encouraged my team and I think at OpenAI
[07:55] we're pretty good about not trying to
[07:56] optimize for for specific benchmarks.
[07:58] But once you put out a benchmark, it's
[08:00] there's it's always at risk of just
[08:02] being optimized for. And I think one way
[08:04] to one way to address that is to keep a
[08:06] held out private set um that isn't uh
[08:09] publicly available.
[08:10] >> The most popular fallback advice for you
[08:14] know figure out if a model is
[08:16] significantly better or not is to just
[08:18] play with it for a while. Do you have
[08:20] anything more sophisticated than that
[08:21] that you suggest people do? like do you
[08:24] create your own set of new evaluations
[08:27] each time besides private holdback at
[08:29] OpenAI?
[08:30] >> I think everybody has their own set of
[08:32] questions that they like to ask the
[08:32] model whenever it comes out.
[08:34] >> Um for me lately it's been I I use them
[08:37] to make poker bots and see how good they
[08:40] can make a poker bot. I think it's a
[08:41] nice eval because there is very little
[08:43] um open source code for making poker
[08:46] bots and there's a lot of published
[08:48] essay there's a lot of published papers
[08:49] on it but you really have to reason
[08:51] through everything and it's like
[08:52] requires a lot of just reasoning and
[08:56] iteration and like a lot of small
[08:57] gotchas
[08:58] >> that I can kind of I've already worked
[09:00] through myself so I can see where the
[09:01] models fail along the way. They've
[09:02] gotten really good at it now. Can you
[09:04] describe perhaps like with your poker
[09:07] bot creation like how reasoning might
[09:09] have progressed in model releases for
[09:12] you guys over a few uh releases?
[09:15] >> Yeah, when the early models were really
[09:18] bad at it, like they could not basically
[09:19] do anything. And then 5.2
[09:23] I was able to work with it to make a
[09:27] river solver.
[09:28] >> So that's like the final stage of poker.
[09:30] And um that itself was I thought really
[09:33] impressive. I mean I had to work with it
[09:34] a little bit, but I was actually really
[09:36] impressed cuz I was able to make the
[09:39] river solver probably about five times
[09:40] faster than I would have alone. There
[09:43] were a couple things that I got um
[09:44] tripped up on. Uh blockers was always a
[09:47] big big issue. But overall, like, you
[09:50] know, with a with a bit of gentle
[09:51] steering, it just kind of like it kind
[09:53] of felt like a grad student where, okay,
[09:55] they would run into issues, but at least
[09:56] like I would um know what those issues
[09:59] were and know how to fix it, and I could
[10:00] just make suggestions and it would go
[10:01] off and then do it and then pretty
[10:03] quickly it would actually come back with
[10:04] something really good.
[10:05] >> Mhm.
[10:05] >> And then especially the optimization I
[10:07] thought was very impressive. It was able
[10:09] to make it like 10 times faster than
[10:12] what I was able to do because it was
[10:14] just able to optimize um the code so
[10:16] well. The downsides with 5.2 is I felt
[10:18] like it was gaslighting me a lot and I
[10:21] always had to be very careful checking
[10:23] it and making sure like, okay, is it
[10:24] actually doing what it said it did? Um,
[10:26] are there any things that are like
[10:28] glaring issues that it's not recognizing
[10:29] or it's just pretending aren't issues?
[10:31] Um, I remember there was like one point
[10:34] uh where for one of the models I was
[10:35] playing around with it, not 5.2,
[10:37] I kind of like as a as a unit test, I
[10:39] told it, okay, well, let's say um I have
[10:43] $100 in the pot and I fold. How much am
[10:46] I losing? And the model said $92. And I
[10:48] was like, that's crazy. I have $100 in
[10:50] the pot and I just fold it. How do I not
[10:51] lose $100? And it said, oh, you know,
[10:53] it's 92. It's close to 100. It's fine.
[10:55] It's no big deal. And I was like,
[10:56] clearly this is a problem, right? So the
[10:59] models did have this problem where they
[11:00] would gaslight you a lot. But once we
[11:02] got to 5.5, I actually thought um it was
[11:06] way better. It was able to basically do
[11:07] it zero shot. And in fact, I've been
[11:09] working on just doing a full scale poker
[11:12] solver. Um and it it's basically able to
[11:14] do the whole thing uh with some gentle
[11:16] steering from me. And I wouldn't be
[11:18] surprised if you know 6 months or a year
[11:20] from now, the model is able to do zero
[11:21] shot an entire poker solver, basically
[11:23] my entire PhD thesis in one go. Let's
[11:26] talk about the larger implications of
[11:29] you know needing to evaluate these
[11:31] models relative to um let's say like
[11:34] speed of their reasoning or efficiency
[11:37] versus you know token volume right um or
[11:40] dollar budget or whatever whatever your
[11:42] scalar is. Can you describe some of the
[11:44] larger implications in your essay
[11:46] including around um like safety
[11:48] evaluations? Yeah, the safety
[11:50] evaluations thing. Um, it's it's a bit
[11:53] of an inconvenient truth thing where
[11:55] okay, so I guess for background, a lot
[11:57] of the all of the labs have these things
[11:59] called either responsible scaling
[12:00] policies, preparedness frameworks. They
[12:02] go by various names, but the idea is
[12:04] that whenever a model is released, they
[12:05] go through a series of evaluations to
[12:06] measure are there dangerous
[12:08] capabilities? Um, could these models do
[12:10] things that we're we we wouldn't want um
[12:13] a bad actor to do. And if the model
[12:16] isn't very capable, then it's no big
[12:17] deal. But if it is very capable, if it
[12:19] could be used for example to make
[12:20] bioweapons, then you want to put in
[12:22] mitigations against that.
[12:24] >> But the question is okay, well, how do
[12:25] you evaluate whether the model is
[12:27] capable of that? And they have like
[12:29] various protocols about like how they do
[12:30] these valuations. But a lot of these
[12:33] frameworks were developed around the era
[12:35] of chatgpt before after when test time
[12:38] comput scaling was not really uh as much
[12:41] of a thing and it made sense like with
[12:42] GPT3 you couldn't scale test time
[12:45] compute like if you gave it a budget of
[12:47] $10 million and said okay well let's see
[12:48] what GP3 can do it really can't do that
[12:50] much more than what you could do with
[12:52] like $10 or $1. the preparedness
[12:55] frameworks and responsible scaling
[12:56] policies, they don't really account for
[12:58] the amount of test time compute. They
[12:59] just say, "Okay, well, what's the
[13:00] capability of the model? The problem is
[13:02] we're in a world now where the
[13:03] capability of the model is a function of
[13:06] how much money you put into it.
[13:08] Basically, if you give it a budget of
[13:10] $10,000, it can do a lot more than what
[13:12] it can do with a budget of $10. If you
[13:14] give it a budget of $10 million, it can
[13:15] do even more." And so, at what budget
[13:19] should you evaluate these models? the
[13:22] policies that exist today don't really
[13:24] address that question.
[13:25] >> Mhm.
[13:25] >> Uh some do some do better than others,
[13:27] but um for the most part, this is not
[13:29] really a factor that's being heavily
[13:31] considered. Now, whether it should be
[13:33] released anyway, I don't I don't want to
[13:34] wait into this question. I think
[13:36] there's, you know, there's arguments on
[13:37] both sides, but I think the important
[13:38] thing to recognize is that this is a
[13:40] question that is not being we're just
[13:42] kind of like, you know, pretending that
[13:45] this issue doesn't exist. And I think
[13:47] it's important to just, you know, one
[13:48] way or the other um account for it.
[13:50] Yeah, it's the mirror image of the
[13:52] capability question of if the models can
[13:55] uh continue to do more and more without
[13:58] asmmptoing on some tasks at very large
[14:02] budgets um then they should also be able
[14:04] to do so for uh tasks we don't want them
[14:06] to do as a society, right? And so
[14:09] testing for that um and what budget is
[14:11] allocated. It also seems out of sync
[14:13] from the model release cycle itself,
[14:15] right? there's been this acceleration
[14:17] of, you know, you get a new model every
[14:21] sometimes few days and weeks at this
[14:23] point versus 6 months. And you have a
[14:26] line in the essay where you say like the
[14:28] the only way to truly evaluate an agent
[14:32] on some very longunning task might be to
[14:35] run it for a year. And that's going to
[14:36] be true of both like useful and uh
[14:39] negative tasks, right? And so how do you
[14:42] think about that versus the model
[14:43] release cycle? Yeah, this this is also
[14:45] an interesting dynamic where basically
[14:48] as the models have become stronger,
[14:49] they've they're more they're better able
[14:52] to operate over longer horizons.
[14:54] >> So again, with GPD3, if you wanted to
[14:56] run it for, you know, a week, there's
[14:59] really not much you could do to scaffold
[15:00] it into something useful that could
[15:02] actually run for a week. But we're
[15:03] seeing now with the most recent models
[15:05] that you can actually scaffold, for
[15:06] example, 5.5 into doing a series of
[15:09] experiments that can run for weeks, for
[15:12] months. Have you given your poker solver
[15:16] task like infinite budget yet?
[15:19] >> I haven't really scaffolded something
[15:20] together where I just tell it like,
[15:22] "Okay, just run this for um for weeks."
[15:25] I think I could give it I I could ask I
[15:28] could probably give it / goal and just
[15:29] like yeah, tell it to go nuts.
[15:31] >> But um I I think at this point it could
[15:34] 100% do the river solver. Um, if I just
[15:36] give it slash goal, I don't think it's
[15:38] at the level yet where it could do like
[15:39] the full poker solver if I gave it just
[15:40] slash goal and told it, yeah, go go run
[15:43] for a month. But we're going to pretty
[15:46] soon be at that point where I probably
[15:47] could just tell it like, yeah, go work
[15:48] on this for a month and then come back
[15:49] to me with a a full complete poker
[15:52] solver that's state-of-the-art.
[15:54] And the problem is if you want to
[15:57] evaluate the capabilities of a model,
[15:58] what it can do after running for a
[16:00] month, the only way to be fully sure is
[16:03] to actually run it for a month. And if
[16:05] you want to know after 6 months, the
[16:06] only way to know fully is to run it for
[16:08] six months. Now there I I'll get to like
[16:10] things we could do to address that a
[16:11] little bit later. But like it's
[16:13] important to recognize the model release
[16:14] cycle is look, we're releasing new
[16:17] models like every two or three months at
[16:19] this point. And so a model comes out, it
[16:22] takes two or 3 months to push it to its
[16:24] limits and then you have another model
[16:26] come out. And so nobody actually knows
[16:28] what the ceiling of capabilities are for
[16:30] these models because nobody's actually
[16:31] run them for long enough to really tell.
[16:33] When slash goal came out, for example, I
[16:36] mean, people started running things that
[16:39] it took over a week for it to finish.
[16:41] And so, people actually didn't realize
[16:42] that this was a big deal until after a
[16:43] week uh until a week after it was
[16:45] released.
[16:45] >> Mhm.
[16:46] >> I think that's going to be more and more
[16:48] true. You know, the implications of that
[16:49] are, I think, pretty interesting because
[16:52] what do the labs do to like fully
[16:53] evaluate their models before they're
[16:54] released? It's actually very difficult
[16:56] because, yeah, you would have to the
[16:59] only way to to really do the evaluations
[17:00] is then delay the model release cycle.
[17:03] Um and you know there's a lot of
[17:04] competitive pressure right now to not do
[17:06] that.
[17:06] >> Do you think there's um like exciting
[17:08] latent capability in the models that are
[17:10] already released that people have not
[17:13] fully explored given timeline?
[17:14] >> I think absolutely. I think actually a
[17:16] really great example is the erdo unit
[17:18] distance problem. So for the viewers
[17:21] that don't know like we used an internal
[17:23] model at OpenAI a few weeks ago to uh
[17:25] disprove the unit erdos unit distance
[17:27] conjecture. Now, I'm not a
[17:29] mathematician, but this seems like it
[17:30] was a pretty big deal in the in the math
[17:32] community. It was like the first uh
[17:34] first problem that a lot of
[17:35] mathematicians had really spent a lot of
[17:37] time on, and the model was able to do
[17:39] something that they weren't able to do
[17:40] and do it in a way that was actually
[17:42] interesting and useful for
[17:43] mathematicians. Honestly, it did it at a
[17:45] budget that was dirt cheap. I mean, we
[17:47] didn't put a lot of effort into this. We
[17:48] just we trained a new model and we were
[17:50] just curious what it could do. And we
[17:51] ran it through some problems. And this
[17:53] one at a pretty low budget, it was like,
[17:55] "Oh, yeah. I think I have a disproof."
[17:56] And then we were able to verify that
[17:58] yeah that this proof is correct after we
[18:01] announced the results a bunch of people
[18:04] found that you could get the answer out
[18:06] of 5.5 as well if now it's not as simple
[18:10] as just asking 5.5 hey here's the unit
[18:12] distance conjecture what's the disproof
[18:14] you had to scaffold it a bit you had to
[18:16] like steer it a bit and so somebody
[18:19] found okay you ask 5.5 list a bunch of
[18:22] ways that you could tackle this problem
[18:24] and then for it it lists one of the
[18:26] paths that are actually promising to get
[18:28] to the disproof and then you tell it
[18:30] like okay explore this some more and
[18:32] then if you do this enough times it
[18:33] actually ends up arriving at the
[18:35] disproof. Now what this means is you
[18:38] could in principle ask 5.5 to you know
[18:41] as as a general purpose scaffold list a
[18:44] bunch of different strategies and then
[18:45] for each strategy tell it to investigate
[18:47] that strategy and then it would probably
[18:50] be able to arrive at the disproof with a
[18:53] general purpose scaffold. Now that
[18:54] scaffold would be very expensive. I mean
[18:56] it would probably cost I I just ballpark
[18:58] like thousand to 10 to $100,000. Um but
[19:02] it would be possible and it would have
[19:03] been possible for somebody to disprove
[19:05] the erdos unit distance conjecture
[19:08] before we did using a general purpose
[19:10] model. And nobody had explored
[19:13] sufficiently what happens if I put
[19:15] $100,000 worth of compute into 5.5 what
[19:17] could it do? Um and the answer is like
[19:19] yeah you probably could get stuff like
[19:20] that out of it. So people should be
[19:22] experimenting more with the current
[19:23] generation in terms of
[19:24] >> well this is I think is an interesting
[19:25] question of is it worth it to experiment
[19:27] with because again the model release
[19:29] cycle is every every couple months we
[19:31] put out a new model that's even more
[19:32] powerful and so the cost of disproving
[19:36] the erdosha distance gesture drops by
[19:38] like 10 or 100x with every model release
[19:40] cycle probably in some cases more so
[19:43] >> you've seen the meme that's like oh I
[19:45] like why why bother doing any
[19:46] engineering work when I should just wait
[19:48] for the next
[19:48] >> model go on vacation come back two
[19:50] months later and and it's, you know, a
[19:51] thousand times cheaper. So,
[19:53] >> do you agree with that?
[19:54] >> I
[19:55] >> Is that what you're doing right now at
[19:56] OpenAI, just waiting for the next model
[19:57] release?
[19:58] >> I think I I mean, I will say we're we're
[20:00] in a period where progress is very fast
[20:02] and like yeah, the models are becoming
[20:03] more capable. I I can say like at OpenAI
[20:05] one of the things that we're we're
[20:06] actively not doing and look we have a
[20:08] lot of mathematicians we have a lot of
[20:09] physicists people are very excited about
[20:10] what these models can do right now
[20:12] especially you know the internal models
[20:14] we are trying to encourage people to not
[20:16] spend all their time just like going
[20:19] through all the mathematical open
[20:20] problems physics problems and um just
[20:23] seeing pushing the models to their
[20:24] limits to see what they can prove or
[20:26] disprove. Um because we really think the
[20:28] focus should be on how do we make even
[20:30] more capable models? how can we get them
[20:32] get them out safely to the world as
[20:33] quickly as possible so that all the
[20:34] scientists in the world can use these
[20:36] models to solve the problems themselves.
[20:38] Uh so yeah in some sense we are thinking
[20:41] about this that yes it's really tempting
[20:43] to um just put all of our efforts into
[20:45] scaling up these models and see what
[20:46] they can do at their limits right now
[20:48] but really the focus should be on how do
[20:50] we use these models to make even more
[20:53] powerful models even more capable models
[20:55] that can do everything much more
[20:57] cost-ffectively.
[20:59] What is changing about the uh direction
[21:03] or allocation of resources for research
[21:06] in your mind given your beliefs about
[21:08] this very large scale the impact of very
[21:10] large scale test time compute? How does
[21:12] this interact with the um idea of
[21:15] recursive self-improvement for example
[21:17] where you know it's a dominant idea for
[21:19] how you know any lab gets to the best
[21:22] capability model. So, one thing I should
[21:24] clarify, I don't think we're at the
[21:25] point where, okay, you just give it an
[21:27] arbitrary extremely high inference
[21:29] budget and it's just it's just super
[21:31] intelligent across the board.
[21:32] >> SL goal,
[21:33] >> yeah,
[21:34] >> make GPD 7 or whatever and yeah, just go
[21:37] nuts.
[21:37] >> What's between us and there then?
[21:39] >> I think having played around with the
[21:41] model uh so okay, so first of all, there
[21:43] are some benchmarks where the models
[21:45] will just not improve if they have more
[21:46] inference budget. So, I think a lot of
[21:48] factual ret uh factual um retrieval kind
[21:52] of questions fall into this category of
[21:54] if you ask a person when was Abraham
[21:56] Lincoln born and they don't know the
[21:58] date. They could sit there, they could
[21:59] think about it for a week, if they if
[22:02] they don't have access to Wikipedia or
[22:03] something, they're not going to be able
[22:03] to do better answering that question if
[22:05] they thought about it for a week
[22:06] compared to 5 seconds. Same with the
[22:10] model. If you actually, interestingly
[22:12] enough, if you give the model these
[22:13] kinds of like factual retrieval
[22:14] questions and you give them a little bit
[22:15] of time to think, they do actually do
[22:16] better. um but if you give them a week
[22:18] they're not suddenly going to do better
[22:20] at remembering dates. There are so
[22:22] there's some benchmarks where they
[22:24] clearly improve with more test time
[22:25] compute and there's some where they
[22:26] don't. I think on the other extreme
[22:28] there are um benchmarks where they kind
[22:32] of obviously will keep improving limit
[22:34] uh without limit with more test time
[22:36] compute. So the example I like to point
[22:37] to is sudoku. If you uh it's there's a
[22:41] really simple strategy to solving Sudoku
[22:43] which is just try a bunch of different
[22:44] random numbers and then see if it fits
[22:46] the criteria. If it if it matches all
[22:48] the constraints and if it doesn't just
[22:50] try a different random combination of
[22:52] numbers and clearly with enough time you
[22:55] will be able to solve any puzzle with
[22:57] this strategy. You can kind of trivally
[22:59] see like okay any model could keep doing
[23:00] better and better um if it was just
[23:02] given more test time compute. So you
[23:04] have and and all the benchmarks kind of
[23:05] exist somewhere between these two
[23:06] extremes. the models are not at the
[23:08] level where if you just give them enough
[23:10] test time on compute they will be able
[23:12] to do um all of our jobs just because
[23:15] yeah there's some benchmarks where they
[23:17] will not improve there are some things
[23:18] where they they will not improve one
[23:20] thing I see for research in particular
[23:21] is they don't have very good research
[23:22] taste right now and so I think they're
[23:24] actually a very good complement to
[23:26] researchers especially um you know I've
[23:29] found like I've found I'm much more
[23:31] effective by using these models but
[23:33] they're not able to fully replace the
[23:35] whole research cycle
[23:37] Now, does that change with time?
[23:39] Probably. I mean, I think the models are
[23:41] getting better across the board. Some
[23:43] some things are getting better the
[23:44] faster than others. Um, but they're not
[23:47] at the point where they're fully
[23:49] replacing uh researchers with just
[23:50] enough test time compute.
[23:52] >> Can you give um an example or two of
[23:54] like asking the model to do a research
[23:57] test for just like this is this is a
[23:58] terrible idea? I mean I I think going
[24:00] back to my poker solver example, I was
[24:05] really impressed with the model's
[24:07] ability to optimize the algorithms that
[24:09] I had developed in my in my PhD. It was
[24:12] honestly it it was it was shocking to
[24:14] see how inefficient I was um in
[24:17] retrospect and they were able to make it
[24:18] like you know 10 100x faster. And then I
[24:21] was like, okay, can you come up with an
[24:23] algorithm that is better than the
[24:26] algorithms that I came up with or that
[24:27] anybody else came up with and go ahead
[24:30] and like look at all the published work
[24:31] and synthesize that and then try to come
[24:33] up with something novel and it it's not
[24:35] able to do it. And I can give it a lot
[24:37] of time and it's it's still not able to
[24:39] do it. Now, it's possible that if I
[24:41] scaffolded something and like kind of
[24:43] constrained it a bit more that maybe it
[24:45] could eventually come up with something
[24:46] better. Um, but it would take a lot of
[24:48] it's not just as simple as saying,
[24:50] "Okay, please come up with a better
[24:51] algorithm."
[24:52] >> And how do you think that that gets
[24:54] improved?
[24:55] >> What I've seen is with every model
[24:56] release cycle, um, it does get better at
[24:59] this sort of thing. It's still it's
[25:00] still bad in my opinion, but it it's not
[25:03] as bad as it used to be. And I wouldn't
[25:05] be surprised if at some point, same
[25:07] thing with coding, same thing with math,
[25:08] where there's just like this inflection
[25:10] point where suddenly it's actually good
[25:13] enough to be useful. Um I wouldn't be
[25:15] surprised if we encounter that point for
[25:16] research taste as well.
[25:18] >> Given that what do you like what is your
[25:20] framing of RSI today? Like how should we
[25:22] think about it?
[25:24] >> The models are definitely accelerating
[25:26] what researchers can do inside the labs.
[25:28] But I think they are accelerating some
[25:29] things and not other things. And
[25:31] currently we're at the point where okay
[25:33] if something goes 100x faster you get
[25:36] bottlenecked by the things that don't go
[25:37] 100x faster. over time the things that
[25:39] we're getting bottlenecked on are going
[25:41] to shrink and and there will be I think
[25:43] um a kind of a gradual takeoff in that
[25:45] respect but it's more about transforming
[25:47] right now it's more about transforming
[25:48] what researchers do rather than fully
[25:50] replacing the researchers
[25:52] >> so that actually implies that you don't
[25:55] think we're close to a very fast takeoff
[25:57] right now
[25:58] >> I think fast takeoff is relative things
[25:59] are moving very fast but I think there
[26:01] is this hypothesis that you could have
[26:03] basically an overnight intelligence
[26:04] explosion where the models discover some
[26:07] kind of breakthrough through to make
[26:08] themselves smarter and then that leads
[26:10] to more breakthroughs that make
[26:11] themselves even smarter immediately and
[26:12] you have basically in an instance the
[26:16] models just you know becoming very
[26:18] superhuman across the board uh in in
[26:20] moments and I don't think we're headed
[26:22] to that world largely because of the
[26:25] fact that the models rely so much on
[26:27] large scale test time compute in order
[26:28] to achieve um their greatest
[26:30] intelligence. If you if it requires so
[26:32] much test time on compute to unlock the
[26:34] full capabilities of the model, then
[26:36] that means you're bottlenecked by time
[26:40] um things can only go so fast because
[26:42] the models need to run for long enough
[26:44] to um to actually do something really
[26:46] really powerful. Time itself becomes a
[26:48] bottleneck to what we can do and I I
[26:51] think that is the case right now for a
[26:53] lot of the labs that ultimately I think
[26:54] the biggest bottleneck for all of us is
[26:56] time and that's why all the researchers
[26:58] are working so intensely right now. It's
[27:00] it's just so many um so many hours per
[27:03] week are being put into this because we
[27:04] all see what the overhang is. We see
[27:06] what the capabilities are and we're just
[27:07] bottlenecked by how quickly can we do
[27:09] things.
[27:10] >> What do you think is on the frontier um
[27:12] that is less explored now? Like we've
[27:15] talked about multi-agent before.
[27:17] >> I think multi-agent is quite explored.
[27:20] Um I think
[27:22] >> at sufficient scale,
[27:24] >> I think there's a lot more that could be
[27:25] done. Um, but it's also one of the
[27:27] things that's that's hard to do at a lot
[27:29] of research is hard to do at small skin.
[27:31] I think multi- agent in particular, it
[27:33] really requires in order to fully unlock
[27:35] the cubilities. I think requires like
[27:36] frontier models. I think we've seen some
[27:39] pretty interesting multi- aent
[27:40] scaffolds. I think um they're able to do
[27:42] a lot, but I think it's really just
[27:44] scratching the surface of what it will
[27:45] be able to do. I mean, one way that I
[27:47] think about it is if if you look at
[27:50] human civilization, it's not that humans
[27:52] have become smarter over it's not that
[27:55] they evolved to become smarter over, you
[27:57] know, the past 50,000 years. It's that
[28:00] humans are able to do a lot more today
[28:02] than they were back in caveman times
[28:04] because there have been billions of
[28:06] humans thinking for a long time and
[28:09] building off of each other's accumulated
[28:11] knowledge.
[28:11] >> We have like very good retrieval and
[28:13] scaffolding versus 50,000 years ago. Uh
[28:16] it's not even I wouldn't even call it a
[28:17] scaffold. It's just like this is a very
[28:19] like organic emerging property of just
[28:20] like humans being able to accumulate
[28:22] knowledge, share it, um and build off of
[28:25] it. We're not seeing that with AI models
[28:28] today. They kind of they're they're born
[28:30] into a world for and they exist for a
[28:33] very short context window and then they
[28:34] just like disappear.
[28:36] >> And yeah, there are things that you can
[28:37] kind of do to like continue them, but
[28:39] it's very limited. I do think eventually
[28:41] we will and we're starting to see like
[28:43] signs that we're entering a world where
[28:45] they can coordinate on a large scale. I
[28:48] think multbook and open claw when they
[28:50] first came out I think it was obviously
[28:52] a bit overhyped but they were um
[28:56] an indication of where things could go
[28:57] in the future and I do think that
[28:59] eventually we get to that kind of world
[29:01] >> of some sort of coordinated compounding
[29:03] state.
[29:04] >> Yeah. uh the ability of the models to to
[29:06] share knowledge um on a more global
[29:09] level and be able to build on that
[29:10] knowledge productively.
[29:12] >> Given this set of beliefs and your work
[29:15] like uh how would you characterize just
[29:18] competition at the frontier between the
[29:21] between the three kingdoms if there is
[29:23] no overnight takeoff? It's just
[29:25] researchers grinding away trying to make
[29:28] good high taste algorithmic and
[29:30] investment decisions about where to go
[29:32] and then compute allocation and then
[29:35] policy decisions and eval decisions.
[29:39] >> Um
[29:39] >> that feels like slightly more grounded
[29:40] than um uh I support I suppose like
[29:44] racing towards some immediate hard
[29:46] takeoff that nobody can catch you on.
[29:48] >> I think the competition is very intense
[29:50] right now. I do think the models that
[29:53] exist today um are accelerating what
[29:56] researchers at the Frontier Labs can do.
[29:58] Um there's obviously like I said limits
[30:00] to that right now, but it the ability to
[30:03] use the models to improve the model
[30:06] research is a real thing and it's um it
[30:08] it is like an amplifying force. I think
[30:11] that will continue to be true. I think
[30:12] they'll become more true over time. One
[30:14] thing that I am comforted by is I think
[30:16] all the researchers at the frontier labs
[30:18] like all the frontier labs I think
[30:19] recognize what is at stake and what
[30:22] these models like what what the uh what
[30:24] the risks are and that's something that
[30:27] I I find comforting that I think
[30:28] everybody really understands like okay
[30:30] this is a pretty serious thing and it
[30:31] can lead to really great things or it
[30:33] can lead to really bad things and yes
[30:35] there's a competitive dynamic between
[30:36] the labs but like we can also try to
[30:39] figure out how we all get to the
[30:40] positive outcomes rather than the very
[30:42] negative outcomes. I I think you know
[30:44] I'd be remiss to ask just because you
[30:46] have been right very early for a long
[30:49] time um on the importance of test time
[30:52] compute and reasoning as a framework
[30:54] like are there ways in which you use the
[30:57] models that you should you would
[30:59] encourage others to right is it just
[31:01] goal everything
[31:03] >> I think for a lot of people
[31:05] they worked I mean this is probably not
[31:08] even true for your audience necessarily
[31:09] but there's a lot of people that
[31:11] experimented with AI back in like 2012
[31:12] 23 and felt like they couldn't trust the
[31:14] outputs and then don't use it for really
[31:16] high stakes decisions. And actually, I
[31:18] think the models have progressed to a
[31:19] point where they are very good for these
[31:22] kinds of things. I mean, I asked them
[31:24] tax advice or I bought a condo recently
[31:27] and I was asking it for advice on like,
[31:28] okay, well, what's all the paperwork
[31:29] that I have to fill out and like how to
[31:31] how do I what does it all mean? It's
[31:33] actually really good for these kinds of
[31:35] questions. Mhm.
[31:36] >> So, I use it dayto-day for for a lot of
[31:38] this kind of stuff. And I think they're
[31:41] at a point now where they've actually
[31:43] been at a point for a while now where I
[31:45] feel like I can just trust the outputs
[31:46] arguably more than I could trust the
[31:48] output from from a human,
[31:50] >> an expert human. Yeah.
[31:51] >> Okay. I have two two final questions for
[31:53] you. Um, one is uh is there something
[31:58] you think that the rest of the research
[31:59] community doesn't agree with you on or
[32:02] doesn't understand the importance of
[32:04] quite yet? Oh, these are such good
[32:06] questions. I wish I had time to think
[32:07] about this ahead of time.
[32:07] >> You can you can just hang out with me
[32:08] and think about it. Yeah.
[32:10] >> Is it weird to be like consensus now?
[32:12] You're a bit salty three years ago when
[32:13] you're like, why don't people understand
[32:14] how important this is?
[32:16] >> I still I still feel like it's not
[32:17] consensus though because like you know
[32:19] people still don't publish the
[32:20] benchmarks this way.
[32:21] >> Oh, that's true. Yeah.
[32:23] >> Like that's actually why
[32:24] >> I think that's like inertia.
[32:25] >> That's kind of Yeah, but that's kind of
[32:26] why I wrote the essay. I was just like
[32:27] look I mean we can talk about this but
[32:28] like yeah the part of the motivation is
[32:30] like I would talk to researchers about
[32:32] um we it makes sense to show the
[32:35] benchmarks with an x-axis whether it's
[32:37] tokens or cost or time there should be
[32:39] an x-axis and everybody would say like
[32:41] yeah that makes sense we should do that
[32:42] but everybody
[32:43] >> they're not acting with the importance
[32:44] of like good heart like this is we have
[32:46] to measure the correct thing
[32:47] >> well really their response is people
[32:50] expect us to to publish the grid
[32:53] >> and then okay why do people expect the
[32:55] grid to be published because everybody
[32:57] publishes the grid. And so you kind of
[32:59] end up in this this bad equilibrium
[33:00] where everybody kind of knows that it's
[33:02] a bad equilibrium, but like nobody wants
[33:03] to break out. And I I felt like, okay,
[33:05] well, if I just hopefully come out and
[33:07] say like, look guys, let's all recognize
[33:09] that we're in a bad equilibrium and
[33:10] let's move to this different equilibrium
[33:11] where we're we're plotting things with
[33:13] an X-axis that hopefully that can, you
[33:16] know, next time there's a model release,
[33:18] a company can feel comfortable not
[33:20] publishing the grid, at least not at the
[33:22] very front uh the top line. and um we
[33:26] can have a more productive evaluation of
[33:28] these models.
[33:29] >> Then a last question for you. How do you
[33:31] think about companies across all of
[33:34] these specialized domains who feel the
[33:38] value that they have is essentially like
[33:42] the routing layer, the choice layer of
[33:46] you know my goal is composed of a bunch
[33:51] of discrete tasks. Some require more
[33:53] intelligence and less and within my my
[33:56] job as a vendor is to um solve that
[33:59] problem or achieve the optimal outcome
[34:02] with uh taking into account the budget
[34:05] constraints. And so I will manage like
[34:08] the parallelization and how how much
[34:11] inference do you spend on it from what
[34:13] model because I I think the the frontier
[34:16] lab point of view is that that routing
[34:17] happens both within the you know behind
[34:21] the API behind the application and then
[34:23] some of it in the model itself. Um and
[34:26] that's pieces of that are clearly being
[34:28] externalized in all these applications.
[34:30] >> Yeah, I do I do think this is related to
[34:31] the fact that like benchmarks should be
[34:33] evaluated with an x-axis of tokens or
[34:35] cost. Um I I have seen some evals
[34:37] recently that show like okay well with
[34:39] with a routing layer you can achieve
[34:40] much better performance um by basically
[34:44] doing consensus among the models.
[34:46] >> Yeah.
[34:46] >> And like I definitely believe that if
[34:48] you do consensus among the models that
[34:49] you're going to achieve better
[34:50] performance than any individual model
[34:52] but
[34:53] >> it's important to ask like are you going
[34:54] to do better than having that model
[34:56] basically think for longer. Um like once
[34:58] you control for the amount of test time
[34:59] compute is it is it actually still doing
[35:01] better? That's that's the question that
[35:03] you want to figure out. Okay, that's
[35:04] very principle of view which is like yes
[35:06] routing is fine but it's all subject to
[35:08] the same budget question. Yeah,
[35:10] >> right. Um if you put it on the same
[35:12] scaler then you can make an optimal
[35:13] decision and I think maybe I win.
[35:15] >> Mhm. I I I don't even know necessarily
[35:17] that I I would believe that the routing
[35:19] does better but then there's still a
[35:21] question of um is it going to do
[35:22] significantly better? Is it very
[35:24] fragile? Is it um reflective of real
[35:26] world use cases compared to benchmarks?
[35:28] because like one issue you could run
[35:29] into is that you could optimize for
[35:31] certain benchmarks with the routing and
[35:32] then show like oh yeah we see this big
[35:34] improvement on these benchmarks. Um but
[35:35] in real world use cases it actually ends
[35:37] up not being a significant improvement.
[35:39] So I I would say at the very least like
[35:42] I would say you want to control for
[35:43] testime compute and then you also want
[35:45] to have all the same um skepticism about
[35:48] benchmarks that you would normally have.
[35:50] >> Awesome. N thanks so much and and for
[35:52] being on the mission for uh breaking us
[35:55] out of this false equilibrium. Yeah,
[35:57] it's great to be back.
[36:00] >> Find us on Twitter at no prior pod.
[36:03] Subscribe to our YouTube channel if you
[36:05] want to see our faces. Follow the show
[36:07] on Apple Podcasts, Spotify, or wherever
[36:09] you listen. That way, you get a new
[36:10] episode every week. And sign up for
[36:12] emails or find transcripts for every
[36:14] episode at no-briers.com.
