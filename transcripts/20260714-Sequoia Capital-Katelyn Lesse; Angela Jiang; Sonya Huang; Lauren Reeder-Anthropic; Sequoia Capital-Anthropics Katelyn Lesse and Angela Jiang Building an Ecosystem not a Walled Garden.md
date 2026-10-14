---
访谈时间: "2026-07-14"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Katelyn Lesse; Angela Jiang; Sonya Huang; Lauren Reeder"
嘉宾公司名称: "Anthropic; Sequoia Capital"
播客名称: "Sequoia Capital"
播客url地址: "https://www.youtube.com/watch?v=vPnVTHYplrQ"
全文提及的关键名词: 
  - "Anthropic"
  - "Claude"
  - "developer platform"
  - "MCP"
  - "skills"
  - "agents"
  - "sandboxes"
  - "Modal"
  - "Vercel"
  - "Cloudflare"
  - "ecosystem standards"
字幕来源: "automatic_captions:en-orig:English (Original)"
YouTube视频标题: "Anthropic's Katelyn Lesse & Angela Jiang: Building an Ecosystem, not a Walled Garden"
---

## Transcript

[00:00:00] The last layer of abstraction on top of
[00:00:01] this is probably the coordination layer.
[00:00:03] So you have knowledge and you have
[00:00:04] execution, you have coordination. And at
[00:00:06] the coordination layer, we're beginning
[00:00:07] to think of these things called like
[00:00:08] strategies where basically it's almost
[00:00:10] like a meta harness. The true low-level
[00:00:13] harness is designed for execution. But
[00:00:14] the next one is about okay if tokens
[00:00:16] aren't really fungeible and you need to
[00:00:18] give them different jobs like maybe some
[00:00:19] this token is advising versus this token
[00:00:21] is executing you want to start composing
[00:00:23] these like these kind of orchestrated
[00:00:25] strategies that go together and they
[00:00:26] should sit on top of all these things
[00:00:28] because at the end of the day you still
[00:00:29] need to execute and the execution still
[00:00:30] needs to know what to do. So everything
[00:00:32] in theory should kind of like ladder
[00:00:33] together. And so I think you know if you
[00:00:35] were to look at our road map and the
[00:00:36] maybe kind of project forward a little
[00:00:37] bit where you kind of expect us to go.
[00:00:39] We'll move more and more from the
[00:00:41] knowledge layer to the execution layer
[00:00:42] and from the execution layer to the kind
[00:00:44] of coordination layer in terms of the
[00:00:45] abstractions that you can see us put
[00:00:47] out.
[00:01:04] Caitlyn and Angela, thank you so much
[00:01:06] for joining us today. Lauren and I are
[00:01:07] thrilled to have you here. You are
[00:01:09] responsible for building Anthropics
[00:01:10] platform and so you are responsible for
[00:01:13] building what I think is one of the most
[00:01:15] important if not the most important
[00:01:16] developer platform in the world and we
[00:01:18] are really excited to interview you
[00:01:20] today to understand more about what's
[00:01:21] ahead and so maybe just to get started
[00:01:23] can you give us the context of you know
[00:01:25] what is anthropic platform and where do
[00:01:27] you sit within anthropic? Yeah. So
[00:01:29] platform is both our externally facing
[00:01:31] APIs, our developer platform that people
[00:01:33] build on top of when they want to build
[00:01:35] applications and system that systems
[00:01:37] that access cloud's intelligence as well
[00:01:39] as internally um we run our product
[00:01:42] infrastructure and basically we're the
[00:01:44] layer that our apps build on top of uh
[00:01:47] internally as well.
[00:01:49] >> Awesome. What's your northstar as a
[00:01:50] team?
[00:01:51] >> It's a great question. We actually
[00:01:52] because we have both internal and
[00:01:54] external. We actually kind of have like
[00:01:55] two north stars which is probably like
[00:01:57] you know you' be like why there should
[00:01:58] only be one north star but um no we
[00:02:00] >> different planetary system.
[00:02:02] >> Yes exactly they're separate solar
[00:02:03] system so it's fine. Um but uh on the
[00:02:06] internal side like we really want to
[00:02:07] provide is like literally as much
[00:02:08] leverage as possible for our internal
[00:02:10] teams to be able to ship like AGI pill
[00:02:14] products. Um and we want them to be able
[00:02:16] to move fast, be able to have reliable
[00:02:18] like great like uh platform uh to be
[00:02:20] able to build on top of. But I think
[00:02:22] that key bit about speed is like really
[00:02:24] intentional for us and we really really
[00:02:26] care about that internally. Externally
[00:02:28] um we actually have a lot more like
[00:02:29] complicated set of things. Um but one of
[00:02:31] the true norths that we have there is to
[00:02:33] be able to basically give any builder
[00:02:35] the tools to be able to work with claude
[00:02:37] to build whatever they want to build.
[00:02:39] And so it's a bit of a broad statement
[00:02:41] but as a result that uh boils it itself
[00:02:44] down into you know being wherever that
[00:02:46] business is. Like we really care about
[00:02:47] like bringing our platform really really
[00:02:49] close to that business. This is why we
[00:02:51] spend a lot of time with the
[00:02:51] hyperscalers integrating really closely
[00:02:54] uh directly with them like AWS, Google,
[00:02:55] so on and so forth. Um and it is a lot
[00:02:58] of like primitives that we end up
[00:03:00] creating. We want people to be able to
[00:03:02] express what they think their product
[00:03:04] should be. We want them to be able to
[00:03:05] almost do like custom software in their
[00:03:07] own way. You know, like in this new
[00:03:09] world with AI, uh what used to be
[00:03:11] probably economically impossible was
[00:03:13] that last mile of of custom software now
[00:03:16] in theory should be like very very
[00:03:18] achievable. Um, and we want to give them
[00:03:20] all the tools and all the capabilities
[00:03:21] to go and do that. And so sometimes that
[00:03:22] comes in the form of primitives and APIs
[00:03:25] and higher order abstractions. And
[00:03:26] sometimes that comes in the form of just
[00:03:28] like standards. Uh, so for example like
[00:03:30] skills and MCP. Um, those are things
[00:03:33] just like cloud needs them to be useful
[00:03:34] and we can just give them out to the
[00:03:36] rest of the ecosystem, work with
[00:03:37] everyone to help you create those things
[00:03:39] and get the best out of cloud. So um I
[00:03:42] would say externally you know we really
[00:03:43] are oriented around just helping you
[00:03:45] just be able to build but internally
[00:03:47] that orientation while still existing is
[00:03:49] probably more you know specified towards
[00:03:52] speed and being able to move really
[00:03:54] quickly.
[00:03:54] >> How do you decide what goes into the
[00:03:56] platform what gets externalized and what
[00:03:58] doesn't to decide what products should
[00:04:00] be available?
[00:04:01] >> Yeah I mean we generally try to have a
[00:04:03] philosophy that we try to be consistent
[00:04:05] across the board. It's actually one of
[00:04:06] the reasons uh why we do internal and
[00:04:09] external. Um there's plenty of other you
[00:04:11] know platform businesses and constructs
[00:04:13] where you actually like bifrocate these
[00:04:14] two things. Um for us we kind of try to
[00:04:16] intentionally keep it equal and then as
[00:04:18] a result we try to hold this philosophy
[00:04:20] as much as we can around like you know
[00:04:21] for any builder internal or external
[00:04:23] even though if our internal builders
[00:04:25] might have some slightly different
[00:04:26] requirements in the same way any user
[00:04:27] would have slightly different
[00:04:28] requirements. Uh we want to have the
[00:04:29] same primitives that are available to
[00:04:31] everyone. And one of the maybe the
[00:04:33] overarching thesis for that is that
[00:04:34] we've just seen like the capabilities of
[00:04:36] these models just grow and such just
[00:04:38] exponential and it's really hard to
[00:04:40] figure out like a longlasting form
[00:04:41] factor. I think two years ago we were
[00:04:43] all like everything's chat and now
[00:04:44] everyone's like forget chat and just
[00:04:45] like agents and like there's going to be
[00:04:47] another form factor, another form
[00:04:48] factor. Um and we kind of imagine that
[00:04:51] like constantly evolving. And so the
[00:04:53] best way for us to kind of enable that
[00:04:55] for everyone and also ourselves is to
[00:04:57] actually build a really robust platform
[00:04:58] that gives people those kinds of like
[00:05:00] tools to figure out what those form
[00:05:01] factors are. And I don't think we by any
[00:05:03] means feel like we're the only ones
[00:05:04] capable of figuring out that form factor
[00:05:06] like not at all. In fact, the more
[00:05:07] democratization we can do on that and
[00:05:09] help people and allow people to
[00:05:10] experiment, I think the the more those
[00:05:12] form factors will actually kind of
[00:05:13] naturally come out of the market.
[00:05:15] >> Yeah. Yeah. And I think within our team,
[00:05:16] we've we've had moments where we're
[00:05:19] experimenting even with just like a
[00:05:20] packaging up of our primitives in a
[00:05:22] different sort of higher order way. And
[00:05:24] we've thought about, okay, cool. We've
[00:05:26] solved this exact type of problem with
[00:05:28] this product that we've built into the
[00:05:30] world. And so we can go and dog food it
[00:05:32] for ourselves, but we'd never want to
[00:05:33] fall into this trap of like we're
[00:05:35] overindexed on the problem as it needs
[00:05:37] to be solved for an internal user. Like
[00:05:40] because exactly what Angela said,
[00:05:41] internal users have very specific
[00:05:43] requirements. External users have very
[00:05:45] specific requirements and so if you
[00:05:46] overindex on one or the other, you fall
[00:05:48] into a trap. So a lot of the time what
[00:05:50] we'll do is dog food something
[00:05:51] internally at the same time that we open
[00:05:53] up early access of some sort with
[00:05:55] external customers so that we can kind
[00:05:57] of get a range of feedback and bring
[00:05:58] those things back into the platform.
[00:06:00] >> I'd love to talk about the higher levels
[00:06:02] of abstraction that you discussed. So I
[00:06:04] guess at the base level this is just you
[00:06:06] know raw access to CLA opus or whatever
[00:06:09] tokens. How do you think about the I
[00:06:11] guess the layer cake of abstractions
[00:06:13] above that?
[00:06:14] >> Yeah, if you look back um so when I
[00:06:17] joined Anthropic around a year ago um
[00:06:19] the platform was basically just the
[00:06:21] messages API. It was a messages API. Um
[00:06:24] you know we had come out with standards
[00:06:26] like MCP. We obviously have developer
[00:06:28] tooling around our SDKs and our docs and
[00:06:30] our console and things like this. But
[00:06:31] for the most part it was a stateless
[00:06:32] API. Um, and what's interesting to
[00:06:36] Angela's point on form factors evolving
[00:06:38] over time is we found a lot of our
[00:06:40] customers solving the same problems over
[00:06:42] and over again that we also were solving
[00:06:44] over and over again around as the models
[00:06:46] got better at running for longer and
[00:06:48] working with more contexts at a given
[00:06:50] time. You want to build agents that can
[00:06:53] succeed in a kind of longunning context
[00:06:55] and even a remote context that doesn't
[00:06:57] necessarily have a human in the loop.
[00:06:59] And so we found that we could piece
[00:07:02] together our primitives and stand up all
[00:07:04] the same infrastructure that we're
[00:07:05] finding ourselves standing up internally
[00:07:07] to power our own products and arrive at
[00:07:09] some higher order abstractions that let
[00:07:11] you do more agentic work out of the box.
[00:07:14] And the problems that we're solving for
[00:07:15] you are, you know, infrastructure being
[00:07:17] kind of a hard thing to deal with. like
[00:07:19] how do you figure out spawning sandboxes
[00:07:22] that are going to have the right
[00:07:23] governance and security and like you
[00:07:25] know spin them up and spin them down
[00:07:26] when you need to or the storage around
[00:07:29] transcript sessions so that you can
[00:07:31] resume a session if you stop it and pick
[00:07:33] it back up later. Um so that
[00:07:34] infrastructure is a big thing that we
[00:07:36] wanted to be able to provide more of out
[00:07:37] of the box and we do more of that today.
[00:07:39] Um, and then the second thing just being
[00:07:42] harnesses and harness engineering.
[00:07:44] There's a lot of thought and energy
[00:07:45] going into how do I do my prompt caching
[00:07:47] and how do I manage my context window as
[00:07:50] well as how do I actually just get more
[00:07:51] intelligence out of the model um, and
[00:07:54] how do I manage my costs and things like
[00:07:55] that. So we've kind of packaged up our
[00:07:58] primitives a bit more in tune with the
[00:08:01] problems that we found ourselves solving
[00:08:02] to provide more of these things out of
[00:08:04] the box for people so that they can if
[00:08:07] they're building systems for themselves
[00:08:08] internally, if they're building
[00:08:10] products, they can just be more focused
[00:08:11] on the problems that they want to be
[00:08:13] solving and if they want to offload some
[00:08:15] aspects of those problems to us, they
[00:08:17] can. Um, and that's kind of the ethos.
[00:08:19] And are your customers generally
[00:08:20] choosing to opt from the grab bag of
[00:08:22] stuff that you offer or are they like
[00:08:24] how how often are they opting into the
[00:08:26] just the the managed agents offering? I
[00:08:27] guess just take care of it all for me.
[00:08:29] >> Um it varies by like the the user group.
[00:08:32] So like for I would say you know like
[00:08:34] really AI native startups like the ones
[00:08:36] who are like tinkering and like
[00:08:38] experimenting at a really low layer
[00:08:40] they're just going to go for the
[00:08:40] primitives. Um and then for everyone
[00:08:43] else and these are kind of classic like
[00:08:44] more like enterprises or areas where
[00:08:46] it's like the purpose of the startup or
[00:08:48] the philosophy behind the startup isn't
[00:08:49] necessarily to optimize on um some kind
[00:08:51] of hill climbing piece. It's more like
[00:08:53] stringing together a bunch of workflows
[00:08:54] and you know providing unique user value
[00:08:56] at uh to that user. For those people um
[00:08:59] you know it's just kind of not their
[00:09:00] core competency. It's not where they
[00:09:01] want to focus their time and resources
[00:09:03] and they reach much more for these kind
[00:09:04] of like higher order like package
[00:09:06] offerings.
[00:09:07] >> What are some examples of the primitives
[00:09:08] you've released at different layers in
[00:09:10] the last few months? We've seen a few of
[00:09:12] them. Would love to hear.
[00:09:13] >> Yeah. I think maybe one framing I would
[00:09:15] give um for some of the constructs that
[00:09:17] Caitlin was talking about is like and
[00:09:18] this is a bit of an oversimplification,
[00:09:20] but effectively there's approximately
[00:09:22] like three like layers of this cake. At
[00:09:24] the very bottom is just kind of like
[00:09:26] like knowledge. And so at this layer
[00:09:29] like in many ways it's it's knowledge
[00:09:30] about the model. It's knowledge about
[00:09:31] the things that the model needs. And
[00:09:33] it's just like the ability to know how
[00:09:34] to actually do something with claude is
[00:09:36] maybe the way I'd phrase that. And so
[00:09:37] there the primitives that we have spent
[00:09:40] more and more time on uh have been
[00:09:41] actually things of the past because like
[00:09:43] we still evolve them but they tend to be
[00:09:45] a little bit more baked. Like for
[00:09:46] example there's very specific shapes and
[00:09:48] parameters we put on the messages API
[00:09:50] and it's more like trying to expressly
[00:09:53] like uh showcase Claude's like design
[00:09:57] like Claude the model's uh actual design
[00:09:59] the way it thinks the way it respects
[00:10:00] certain parameters the way it kind of
[00:10:02] like um will do tool calls like all of
[00:10:05] those different pieces. And then we
[00:10:06] started standardizing like tools. And
[00:10:08] then we started standardizing bits and
[00:10:09] pieces of like context that you could
[00:10:11] put in at different moments in time
[00:10:12] which is concretely like skills and like
[00:10:14] memory. And so those are like the kind
[00:10:16] of like knowledge layer type of
[00:10:17] abstractions that we've put out over the
[00:10:19] past um I guess like year plus plus a
[00:10:21] bit. Um the next layer of abstraction
[00:10:24] that we've actually started to spend
[00:10:25] more and more of our time on is like
[00:10:27] once you kind of know stuff you then
[00:10:29] need to like execute. And so at the
[00:10:31] execution layer, that level of
[00:10:32] abstraction is the part that Caitlin was
[00:10:34] talking about around like we're doing
[00:10:35] these like higher order pieces, but like
[00:10:36] what are we putting higher order there?
[00:10:38] It really is because you're now getting
[00:10:40] Claude to execute work. It's not just to
[00:10:42] know something, right? I can give it a
[00:10:44] question and give me an answer. You can
[00:10:45] put string a lot of that stuff together.
[00:10:47] Uh but now if you need to execute like
[00:10:49] do work, give me the output, edit files
[00:10:51] in a bunch of different systems, that
[00:10:53] becomes a lot more complicated and
[00:10:54] requires infrastructure to handle. And
[00:10:56] so that layer is basically I would say a
[00:10:58] low-level harness plus manage
[00:11:00] infrastructure as like the set of
[00:11:01] abstractions. Today we just like our
[00:11:03] highle product for that is called cloud
[00:11:05] manage agents. Um and so that's like a
[00:11:06] piece but we started to wrap more and
[00:11:08] more pieces in that. Um I think there's
[00:11:10] going to be a layer like on top of that
[00:11:11] we have like some inklings of it we
[00:11:13] started to build towards but the last
[00:11:15] layer of abstraction on top of this is
[00:11:16] probably the coordination layer. So you
[00:11:18] have knowledge and you have execution
[00:11:19] you have coordination. And at the
[00:11:20] coordination layer, um, we've started to
[00:11:23] expose some of these in ways that like
[00:11:24] aren't very obvious, but we're beginning
[00:11:26] to think of these things called like
[00:11:27] strategies where basically it's almost
[00:11:29] like a meta harness, right? The harness,
[00:11:31] the true low-level harness is designed
[00:11:33] for execution. But the next one is about
[00:11:35] okay if tokens aren't really funible and
[00:11:38] you need to give them different jobs
[00:11:39] like maybe some this token is advising
[00:11:41] versus this token is executing this
[00:11:42] token is dreaming versus this token's
[00:11:44] executing so on and so forth you want to
[00:11:46] start composing these like these kind of
[00:11:48] orchestrated strategies that go together
[00:11:49] and they should sit on top of all these
[00:11:51] things because at the end of the day you
[00:11:52] still need to execute and the execution
[00:11:54] still needs to know what to do so
[00:11:55] everything in theory should kind of like
[00:11:56] ladder together and so I think you know
[00:11:58] if you were to look at our road map and
[00:12:00] the maybe kind of project forward a
[00:12:01] little bit where you kind of expect us
[00:12:02] to go we'll move more and more from the
[00:12:05] knowledge layer to the execution layer
[00:12:06] and from the execution layer to the kind
[00:12:08] of coordination layer in terms of the
[00:12:10] abstractions that you can see us put
[00:12:11] out.
[00:12:12] >> That's a really cool.
[00:12:13] >> How do you think this all comes together
[00:12:15] into a broader ecosystem beyond just the
[00:12:17] things that you guys are building? How
[00:12:19] do you help support people building
[00:12:21] products on top of it and how do you
[00:12:22] help them get the most out of all these
[00:12:24] pieces?
[00:12:25] >> Yeah, I think this is like super top of
[00:12:27] mind for us. like we really want to find
[00:12:28] a way to be to support as many people in
[00:12:32] doing this as we can. I think we're
[00:12:34] still like learning like a lot of the
[00:12:35] industry like has evolved. We've seen,
[00:12:37] you know, a lot of different pieces um
[00:12:40] get spun up and spun down. And I think
[00:12:42] the the operative part for for Caitlyn
[00:12:44] and I has been in the category of like
[00:12:47] making sure at least at the base layer
[00:12:49] that we provide as many primitives
[00:12:51] across the board as possible. So you
[00:12:53] know this kind of like yeah like
[00:12:54] knowledge execution coordination layer
[00:12:56] we want to give all of that out to
[00:12:57] everyone so that people can start to
[00:12:59] compose and create on top of that. Um
[00:13:01] and that's just from like I think pure
[00:13:03] builder kind of point of view. Then
[00:13:04] there's a point of view around like how
[00:13:06] do you kind of like plug in with us
[00:13:07] right like we're also building
[00:13:09] firstparty products of our own. We've
[00:13:11] also created some ways to embed natively
[00:13:13] with us like for example connectors
[00:13:15] which are built on top of the MCP spec.
[00:13:17] Um, and we try to be more open about
[00:13:19] those types of things. And we're
[00:13:20] starting to figure out like what are the
[00:13:21] right bits and pieces, but what we're
[00:13:23] really trying to do is get to a place
[00:13:24] where, you know, in a company is able to
[00:13:27] get created and built on uh they can
[00:13:29] build whatever products that they want.
[00:13:31] They can build agents if they need to.
[00:13:32] And then those agents and those products
[00:13:34] could be things that could plug into
[00:13:36] other agents. Some of those agents could
[00:13:37] be cloud agents, some of those agents
[00:13:38] could be other people's agents. Um, but
[00:13:41] we want to be able to enable that kind
[00:13:42] of like transactability across the
[00:13:44] board. And then I think in order for all
[00:13:45] of that to kind of ultimately be true,
[00:13:48] there is a bit around like standard
[00:13:50] setting and I think there's the
[00:13:51] traditional standard setting which is
[00:13:52] around you know how do systems
[00:13:54] interoperate um and that's uh you know
[00:13:56] things that you've kind of seen us do
[00:13:57] with like skills and MCP but they're at
[00:13:59] again like the builder layer. I think at
[00:14:01] a higher order layer there's also a bit
[00:14:02] around interoperability and standard
[00:14:04] setting around how do we all kind of
[00:14:06] like treat safety together and you know
[00:14:08] we've talked to a lot of these companies
[00:14:09] and this is less from you know
[00:14:11] philosophies aside just more like no one
[00:14:13] really wants to have technology that's
[00:14:16] like for example like doing negative
[00:14:18] things on um on their service right so
[00:14:21] cyber I think is a great example of this
[00:14:22] uh you want to protect your own systems
[00:14:24] from like negative actors or or bad
[00:14:27] actors and so like these kinds of like
[00:14:29] standard settings of like how we find
[00:14:31] ways to partner with more and more
[00:14:32] people to be like, yeah, we all kind of
[00:14:35] want to make sure our critical
[00:14:36] infrastructure is good. We all want to
[00:14:38] prevent like fraud or any of those
[00:14:40] things from happening and how can we
[00:14:42] work better with each of these members.
[00:14:43] I think on the last layer, we're still
[00:14:45] kind of like we're still evolving and I
[00:14:47] think we're still very much like trying
[00:14:48] to find ways that we can be better and
[00:14:50] work with the rest of the industry to
[00:14:52] bring people along and and work with
[00:14:53] them. Um but those are kind of like you
[00:14:55] know the higher order primitives or
[00:14:57] pieces that we wish to kind of like be
[00:14:59] in place. Um so they can work with folks
[00:15:01] to to ultimately solve this. I think if
[00:15:03] I were to like take a step back at the
[00:15:04] end of the day on on all of these things
[00:15:06] um you know like this technology is so
[00:15:08] transformative. Uh and if it's a little
[00:15:11] bit like electricity in the sense like
[00:15:13] before electricity there was just like
[00:15:14] you know you had to like have a candle
[00:15:16] and it was like you can only do so many
[00:15:17] things. Um, but with electricity, the
[00:15:21] reason why it's such a transforming
[00:15:22] technology for all of us and so greatly
[00:15:24] of a utility is because you can actually
[00:15:26] like wire it into everything. Everyone
[00:15:28] is able to actually access it. We also
[00:15:29] have like standards and ways to plug in
[00:15:31] and do all the pieces that we need. And
[00:15:33] that's not something that anybody can do
[00:15:34] by themselves. They always have to work
[00:15:36] with the ecosystem and work with
[00:15:37] partners um to figure out a path
[00:15:38] forward.
[00:15:39] >> How do you think about the philosophy of
[00:15:41] building an open ecosystem
[00:15:43] uh versus a walled garden? And you know,
[00:15:46] how do you think about what products are
[00:15:48] really important for you to own first
[00:15:49] party versus where you're perfectly
[00:15:51] happy to plug into other components of
[00:15:53] the ecosystem?
[00:15:54] >> Yeah, there's so maybe in using Angela's
[00:15:58] kind of layered cake that we talked
[00:15:59] about a little bit earlier, you'll see
[00:16:01] that on some pieces of this like
[00:16:02] execution for example, um what we've
[00:16:05] done within something like cloud managed
[00:16:07] agents and I think over time you'll see
[00:16:09] us try to make this a little bit more
[00:16:10] modular. We actually aren't precious
[00:16:12] about you should run these things on our
[00:16:14] infrastructure like it should be
[00:16:15] sandboxes that we control or it should
[00:16:17] be a storage layer that we control. Um
[00:16:20] well we actually like for example we
[00:16:22] launched self-hosted sandboxes and we
[00:16:24] partnered with modal and versel and
[00:16:26] cloudflare and a bunch of other folks um
[00:16:28] even like Amazon's new microVMs
[00:16:32] um to have a first class offering where
[00:16:34] you can go plug any of those things in.
[00:16:36] Um, we launched MCP tunnels so that you
[00:16:38] can call out to your MCP servers that
[00:16:40] are behind your firewall, right? And um,
[00:16:43] be able to punch through there. And so
[00:16:45] for some of these things, we, you know,
[00:16:47] the weather, whether it runs on our
[00:16:48] infrastructure versus somebody else's
[00:16:50] infrastructure is actually not important
[00:16:52] to us because the thing that's important
[00:16:53] to us is more that the architecture of
[00:16:55] how you put together these agents in a
[00:16:57] way that will be powerful, in a way that
[00:16:59] will be reliable and scalable. um we
[00:17:02] have strong opinions on that and you can
[00:17:04] kind of just conform to the interfaces
[00:17:06] that we put out there and plug those
[00:17:08] things in. Um and we think that that
[00:17:10] generally is a thing that works really
[00:17:12] well. Yeah, I think on the the kind of
[00:17:14] like verticals where we might build
[00:17:15] products um you know I think we we kind
[00:17:18] of have like two frames here. The first
[00:17:20] one is we are always trying to figure
[00:17:22] out a form factor like an evolving form
[00:17:25] factor. We by the way don't think form
[00:17:26] factors are like static. It's like a
[00:17:27] dynamic thing. So what might be awesome
[00:17:29] for one year's worth of AI development
[00:17:31] will probably not be awesome for the
[00:17:33] next year's worth. And we just kind of
[00:17:34] try to have that mentality. We tell the
[00:17:36] team uh just overall like around
[00:17:38] anthropic. Everyone's always trying to
[00:17:39] be like is this agi pill enough? Um and
[00:17:41] then we always have this mentality of
[00:17:43] like you know we built something it
[00:17:44] works it was cool for a year and maybe
[00:17:47] it's not the right next thing and so
[00:17:49] throw it away try again. Um and we we
[00:17:51] tell like platform users the same thing.
[00:17:52] um I just think that's probably just
[00:17:54] like you know attached to the technology
[00:17:56] but so yeah one one principle is like
[00:17:57] trying to always constantly find this
[00:17:58] new form factor. So sometimes we'll like
[00:18:00] launch products in certain areas to try
[00:18:02] to showcase a new type of form factor.
[00:18:04] Um, it's not necessarily because we
[00:18:05] think it's like the biggest ham or the
[00:18:08] most important thing to go after, but
[00:18:09] sometimes you're like, okay, this is
[00:18:10] like always been a really difficult
[00:18:11] thing and people have always
[00:18:12] communicated this way or tried some
[00:18:13] things this way and can we show that
[00:18:16] maybe there's a slightly different way.
[00:18:18] Um, and because the model capabilities
[00:18:19] are are so advanced now, can we try to
[00:18:21] express it a bit differently? Um,
[00:18:24] >> what's an example of that?
[00:18:25] >> Yeah, you know, like uh cloud design is
[00:18:28] a little bit of of that way. I think
[00:18:30] depending on how you squint, you might
[00:18:31] see it as like a way that we kind of
[00:18:32] going into design as as like you know
[00:18:35] one of the verticals. But more often
[00:18:37] than not, it's like if you take a look
[00:18:38] at what we're trying to do with that
[00:18:40] product, there's a couple of like
[00:18:41] decisions that were made in there. The
[00:18:43] first one is that like you can actually
[00:18:45] try to offload more and more and more to
[00:18:46] Claude. Um, and so it tries to be kind
[00:18:49] of opinionated on like, you know, just
[00:18:50] just like talk to it and like let it
[00:18:52] really try to figure out. And yes, you
[00:18:53] can still edit it and then do these
[00:18:55] kinds of things, but kind of like
[00:18:56] discourage a little of that and more
[00:18:57] just like let just talk to Claude to go
[00:18:59] figure it out. Um, the second thing was
[00:19:01] it was really trying to express that
[00:19:03] actually like code is a is a a way to
[00:19:06] solve for things that you wouldn't
[00:19:07] normally think would be the way. So a
[00:19:09] lot of people who have built kind of
[00:19:10] generative um you know like slide decks
[00:19:13] or designs or whatever um will pick uh
[00:19:15] the way of like they have like some kind
[00:19:17] of design system you integrate against
[00:19:19] design system. It's almost the
[00:19:20] traditional like classic wissywig style
[00:19:22] of designing something. And with like
[00:19:25] quad design, it was like okay, can we
[00:19:26] try to just like use code purely have
[00:19:30] Claude generate that code and would it
[00:19:32] like do a good job? And we found through
[00:19:34] some experiments early on. It's like
[00:19:35] actually it looks like it can kind of do
[00:19:37] that and how can we kind of showcase
[00:19:39] that uh to the world. So that's like an
[00:19:41] example. We have a lot of other internal
[00:19:43] projects and this kind of falls in the
[00:19:44] category of like expressing form factor.
[00:19:46] We'll all try it out internally. it'll
[00:19:48] be super cool for like two weeks and
[00:19:49] then we move on to the next thing. We
[00:19:50] never even ship the thing frankly. But
[00:19:52] yeah, we actually do a lot of product
[00:19:53] experimentation in that area and that's
[00:19:55] like our labs team. And then there's
[00:19:56] like the second category which is that
[00:19:58] we actually do look at TAM like we're a
[00:20:00] business. We do look at TAM. We do look
[00:20:01] at areas that we think uh you know
[00:20:03] there' be reasonable agentic like
[00:20:05] operations that would happen in those
[00:20:07] areas. Uh we do tend to have an
[00:20:10] orientation towards things that are more
[00:20:11] tokenheavy. And by token heavy or token
[00:20:13] hungry maybe is the way I would say that
[00:20:15] is like what we mean is like you know
[00:20:17] you for spending once you spend a like
[00:20:19] call it like one turn you look at the
[00:20:22] end of that turn and you say like am I
[00:20:23] done or am I actually so glad that I did
[00:20:25] that thing I want to do more of that
[00:20:27] thing we like industries where it's like
[00:20:29] the answer to that question you say I
[00:20:30] want to do more of that thing so coding
[00:20:31] is obviously the one that we all know
[00:20:33] and the great thing about coding is that
[00:20:35] what it's actually doing is that like
[00:20:37] once you finished a turn you look at
[00:20:38] that and you're like that was incredible
[00:20:40] I'm like unlocked I'm going to do like
[00:20:42] more. I'm going to build more. I can do
[00:20:43] more. And there's other services where
[00:20:45] it's like actually when you finish that
[00:20:46] turn, you completed the job and you just
[00:20:48] move on. You know what I mean? Um, and
[00:20:50] so we tend to like go into the ones that
[00:20:51] are a bit more like there's this kind of
[00:20:53] like iterative flow. You're going to
[00:20:54] build more, generate more together. Um,
[00:20:57] and then the last angle that we kind of
[00:20:58] take a look at is just sort of like, you
[00:21:00] know, there's going to be certain
[00:21:01] business functions that we're like, they
[00:21:03] are the buyer that we like to go to. We
[00:21:04] want to help them optimize their
[00:21:06] workflows, help them create better
[00:21:07] products there. And I think we've been
[00:21:09] pretty transparent with some of the
[00:21:10] verticalization. Like we've done like
[00:21:11] finance, we've done like legal um and
[00:21:14] we've tried to kind of like narrow on
[00:21:16] into specific areas where we feel like
[00:21:18] by having the right context and the
[00:21:19] right tools and putting it together in a
[00:21:20] good form factor is probably useful um
[00:21:23] for us to to be able to do.
[00:21:25] >> And in each of those areas, we do we're
[00:21:28] trying to do a bit of like showing the
[00:21:29] art of the possible across all the
[00:21:31] different ways that you would accomplish
[00:21:33] those outcomes. And so for you know like
[00:21:35] finance for example is a good one. Um,
[00:21:38] you know, we you could be a company that
[00:21:41] solves problems in finance and you could
[00:21:43] build directly on the messages API and
[00:21:45] you can just get some tokens and you can
[00:21:47] build everything else on top or you
[00:21:49] could be someone who builds on cloud
[00:21:51] managed agents. You can get a lot more
[00:21:52] out of the box or you could say I'm
[00:21:54] going to build a plug-in that or like a
[00:21:56] connector right that's going to sit
[00:21:58] within one of our products and within
[00:22:00] those form factors. When we did
[00:22:02] recently, we launched like claude for
[00:22:03] financial services is like, "Okay, cool.
[00:22:06] We've got packages of skills and things
[00:22:08] like this that you could choose to use
[00:22:09] within our product, within other
[00:22:11] people's products. We even launch like
[00:22:12] cookbooks on here's how you would use
[00:22:14] cloud managed agents to go and do these
[00:22:16] things." And so, I think for us, it's
[00:22:19] all kind of an experimentation around
[00:22:21] like, you know, we provide people all
[00:22:23] these different pieces and see kind of
[00:22:24] where they run with it. And then
[00:22:26] sometimes we put together products that
[00:22:28] are just packaging of all of these
[00:22:30] things like claw tag I think is a really
[00:22:32] good example like we had been seeing
[00:22:34] people in the industry go and say like
[00:22:36] Shopify did this with River um Square
[00:22:39] Block recently did this with Builderbot.
[00:22:41] Um, there's like a few of these examples
[00:22:43] where people said, "I'm going to pro I'm
[00:22:44] going to build like an agentic platform
[00:22:47] internal to my company and I'm going to
[00:22:48] try to give it all the right context and
[00:22:50] I'm going to make it accessible from
[00:22:51] Slack or from various other um, you
[00:22:54] know, platforms that you'd want it to be
[00:22:56] accessible at." And I think Claude tag
[00:22:58] was very much a packaging of all those
[00:23:00] same things that anybody could choose to
[00:23:03] build something similar but this is how
[00:23:05] we're kind of like well this is how
[00:23:06] we're doing it internally and if you
[00:23:08] would like to just kind of plug in and
[00:23:10] go here's what that looks like.
[00:23:11] >> What do you think people misunderstood
[00:23:13] about cloud tag? Because there was all
[00:23:14] this like ruckus about oh my gosh it's
[00:23:16] just a slackbot like tell tell us what
[00:23:18] the magic of tag is.
[00:23:19] >> No I think it's a great question. Um and
[00:23:21] I I do think it actually showcases a
[00:23:22] little bit of where maybe the future
[00:23:24] could be going. Um, yeah. I think like
[00:23:26] the I think if you look at products in
[00:23:28] the past, people are like, "Oh, you
[00:23:29] really attach to like the form or the
[00:23:31] the UI almost, right? Like it looks like
[00:23:33] this." So, it's like super cool. Um, and
[00:23:35] I think when you look at like tag, uh,
[00:23:37] it like yeah, like the way you interact
[00:23:39] with it is that you like literally tag
[00:23:41] it in Slack. Uh, and so yeah, that is
[00:23:43] like the interface, but that's not
[00:23:45] really the important part. The important
[00:23:47] part, um, is all the kind of like
[00:23:50] context engineering and like
[00:23:52] architecture that we put underneath the
[00:23:54] hood. So that tag just works. It really
[00:23:57] should just like just feel like a
[00:23:59] co-orker like a co, you know, if you go
[00:24:01] to a company and you onboard and a
[00:24:02] co-orker comes into your channel and
[00:24:04] then you can chat with it. It's
[00:24:05] proactive. It figured out like what's
[00:24:07] like useful you and um it just gets
[00:24:10] stuff like done for you. And so if you
[00:24:12] think about, you know, especially like
[00:24:13] nontechnical audiences, this is like
[00:24:15] it's a huge unlock. you just you
[00:24:17] literally create a channel and then you
[00:24:18] atclude or sometimes you don't even
[00:24:19] atclude and you're like hey I want to be
[00:24:21] able to do this and do that and I can't
[00:24:23] figure out this and how do I actually
[00:24:24] like submit an expense report again and
[00:24:26] traditionally you think about how to
[00:24:27] solve that workflow you are going all
[00:24:29] over the place and you're talking to
[00:24:30] your manager you're talking to your spin
[00:24:31] buddy and it's really really complicated
[00:24:34] and uh today now you just like go talk
[00:24:36] to cla tag and we do a lot of the hard
[00:24:39] work on doing the context engineering
[00:24:41] the proactivity a lot of the harness
[00:24:43] pieces I think Andre Kaparthi said it
[00:24:44] really well it's like it's like an org
[00:24:46] level harness There's a lot of like
[00:24:47] complexity baked into that like Kayla
[00:24:49] mentioned like you can use our APIs to
[00:24:50] go and construct that. You have to do a
[00:24:52] lot of the experimentation yourself
[00:24:53] obviously but this is like an
[00:24:54] opinionated take from anthropic on like
[00:24:56] how you can have this really awesome
[00:24:58] always on uh kind of agent for your
[00:25:01] entire entire company. And the bit
[00:25:03] that's like futuristic I guess is like a
[00:25:07] lot of that complexity is actually like
[00:25:09] it's like an iceberg. is like all the
[00:25:11] stuff underneath it that's actually
[00:25:12] becoming the harder and harder and like
[00:25:14] useful part that we're trying to like
[00:25:16] push through. And I think we'll see more
[00:25:18] and more like that kind of like tip bit
[00:25:20] that's like outside in the water. It's
[00:25:22] just like the interface can actually
[00:25:24] constantly swap like today, right? Like
[00:25:26] Slack is a place where a lot of people
[00:25:28] collaborate, a lot of business
[00:25:29] collaborate, but also a lot of people
[00:25:30] collaborate in teams and some people
[00:25:32] collaborate by a WhatsApp group um or
[00:25:34] they text each other or they may some
[00:25:36] people still email each other and like
[00:25:37] those could be the form factors that
[00:25:39] actually completely you can imagine
[00:25:41] agents just going there and being and
[00:25:42] they're almost taking up the same form
[00:25:44] factors as humans have taken up. It was
[00:25:46] almost like a very almost like boring
[00:25:48] take, but it's actually like I feel like
[00:25:50] the most like forward one because you
[00:25:51] want the agent and you want AI to
[00:25:53] basically be like another person and
[00:25:56] it's helping you, but it's like you know
[00:25:58] very intelligent can figure out all the
[00:26:00] context and you can always have it to be
[00:26:02] a really helpful assistant.
[00:26:03] >> Totally. You talked about context and
[00:26:05] then harnesses quite a bit and so your
[00:26:08] team is just, you know, has such an
[00:26:09] opinionated point of view on like what
[00:26:11] it takes to build an exceptional agent.
[00:26:12] I imagine a lot of that comes down to
[00:26:14] the context engineering and the
[00:26:15] harnesses.
[00:26:16] >> Totally.
[00:26:16] >> Maybe like what best practices or advice
[00:26:19] would you would you share with people
[00:26:20] about what you need to get right on the
[00:26:22] harness and what you need to get right
[00:26:23] on the context.
[00:26:24] >> Yeah, I think so. It's interesting
[00:26:26] because we've kind of talked about, you
[00:26:28] know, we launched cloud manage agents as
[00:26:30] this like very generic but high
[00:26:33] performing harness because we've done
[00:26:36] all the nitty-gritty work that's
[00:26:37] actually like really boring and not
[00:26:39] super interesting around how do you deal
[00:26:41] with prom caching? How do you deal with
[00:26:43] context management? You like clear old
[00:26:45] stuff out of the window. Sometimes you
[00:26:46] like call tools programmatically so you
[00:26:48] don't pull everything into the context
[00:26:50] window and you can keep it clean.
[00:26:51] There's a lot of those sort of details
[00:26:53] on the lower level harness layer. Um and
[00:26:56] I think honestly like best practices are
[00:26:58] just stuff like prom caching. Do it.
[00:27:01] You're going to save a lot of money and
[00:27:03] and token costs. Um, obviously like try
[00:27:05] to keep your context window clear and
[00:27:07] then putting those things together in uh
[00:27:10] a harness that will be performant is is
[00:27:13] you know sometimes specific to the task
[00:27:16] that you're trying to accomplish, right?
[00:27:18] And then of course evals. Um I'm
[00:27:20] surprised we got this far into this
[00:27:22] thing before one of us said the word
[00:27:23] evals, but like you need evals um to
[00:27:25] make sure that what you're trying to
[00:27:26] accomplish is performance. Um, but I
[00:27:29] think where we're starting to go, and
[00:27:31] Angela mentioned this a little bit
[00:27:32] earlier, is more of a concept of
[00:27:34] strategies or metah harnesses because I
[00:27:37] do think that yes, you can again make
[00:27:40] this lower level harness is going to be
[00:27:41] performant and maybe that's interesting
[00:27:42] for you to do yourself or maybe not and
[00:27:44] you offload it to us. But this concept
[00:27:47] that you can take any given token and
[00:27:49] spend that token on just executing or
[00:27:52] you could take that same token and
[00:27:54] choose to actually reflect on your past
[00:27:56] agentic sessions and write learnings to
[00:27:58] memory so that the next agent does a
[00:28:00] good job or you could take that token
[00:28:02] and advise with a bigger model so that a
[00:28:04] smaller model can execute and do a
[00:28:06] better job. Um or you can say execute
[00:28:09] execute and then like a greater comes in
[00:28:11] is like did you do a good job? No, you
[00:28:12] didn't try again. Right? And so I think
[00:28:15] the the like interesting innovation is
[00:28:18] going to come more at that higher level
[00:28:20] on like the meta level, right? And I
[00:28:22] think optimizing within those strategies
[00:28:25] is something that our team is really
[00:28:26] excited about and we're starting to do a
[00:28:28] lot of work there. Um, and I think a lot
[00:28:30] of other people are starting to feel
[00:28:31] really excited about this concept of
[00:28:33] strategies and like the jobs you give to
[00:28:34] tokens because again like yes, there's
[00:28:37] best practices on stuff like your prom
[00:28:39] caching and exactly how you clear stuff
[00:28:41] out of your context window and how you
[00:28:42] write your evals and like a lot of
[00:28:44] things like this, but I I don't know
[00:28:46] that there's necessarily so much juice
[00:28:47] to squeeze in a lot of cases out of that
[00:28:50] layer as compared to a layer higher than
[00:28:52] that.
[00:28:53] >> Yeah. And one of the reasons for that I
[00:28:54] think is it has to do with the
[00:28:55] generations of the the models. I if you
[00:28:57] look like two years ago, a lot of the
[00:28:59] harness was like a scaffold to kind of
[00:29:01] like tell the model to go from point A
[00:29:03] to point B. And you had to like you
[00:29:05] really had to like build in a lot. You
[00:29:07] practically build one wall here and one
[00:29:08] wall here. So like the thing would go in
[00:29:10] a straight line. And now the models are
[00:29:12] actually very very steerable. Um and so
[00:29:15] a lot of that steering you could just
[00:29:16] put in the prompt, right? Like go do go
[00:29:19] from point A to point B and the model
[00:29:20] like will go from point A to point B.
[00:29:23] So, a lot of if you have harnesses um
[00:29:25] that are like designed to kind of do
[00:29:28] that kind of like steering, you can
[00:29:30] delete that part. Like that part we
[00:29:31] actually frequently encourage like you
[00:29:32] can delete part of those harnesses. I
[00:29:33] think various people have said things
[00:29:34] along those lines. And that's I think
[00:29:36] what people often times mean when
[00:29:38] they're like the model will kind of
[00:29:39] consume some of the scaffolding and like
[00:29:41] in that sense like for sure if your
[00:29:42] scaffolding is telling it to go in
[00:29:43] direction um that it can just
[00:29:45] intelligently figure out like that I
[00:29:47] think will increasingly continue to to
[00:29:48] be so. But as a result of of this, what
[00:29:51] the harness needs to start doing is more
[00:29:53] allow it to run longer. And so that's
[00:29:56] where like that execution bit tends to
[00:29:57] be. I think like it sounds like a maybe
[00:29:59] somewhat silly point, but I do think it
[00:30:00] results in a lot of differences because
[00:30:02] because you can go in the direction that
[00:30:04] you tell it to go. You obviously don't
[00:30:05] want it to stop at B. You're going to be
[00:30:06] like, "Okay, now go from B to C and then
[00:30:08] go to F and then go to Z and then come
[00:30:10] back to me on A." You know, something
[00:30:12] funky like that. In order to be able to
[00:30:14] do a lot of those things, the kinds of
[00:30:16] harnesses that you do are less the
[00:30:18] steering harness and it's more like
[00:30:19] these kind of strategy harnesses that
[00:30:20] Caitlyn's mentioning, which allows you
[00:30:22] to operate at a slightly higher level of
[00:30:24] thinking which matches I think a lot of
[00:30:26] the intelligence gains that we're trying
[00:30:27] to see with the model.
[00:30:28] >> Do you think task specific harnesses
[00:30:30] make sense or a vertical specific or
[00:30:32] task specific harnesses?
[00:30:33] >> I think people have different opinions
[00:30:34] on this. Like our opinion is yes. I
[00:30:36] don't think there's like a general
[00:30:37] harness. I think there are some
[00:30:39] capabilities that are obviously very
[00:30:41] general and they tend to like be very
[00:30:43] useful. Uh like coding is a capability
[00:30:45] that like is very useful because you can
[00:30:47] use it across so many things and
[00:30:48] software as uh you know just like eaten
[00:30:51] so much of of what is capable. So our
[00:30:53] ability to like write software is
[00:30:54] therefore useful. I think when you think
[00:30:56] about like very very specific types of
[00:30:58] domains they're going to require like a
[00:31:00] couple of pieces of the harness to be
[00:31:03] sort of like customized. One of that uh
[00:31:05] I do think is how you choose to kind of
[00:31:07] like handle sort of like errors uh
[00:31:10] between when you do something and you
[00:31:11] hand something off to the model. Um, so
[00:31:13] in like domains where you require like
[00:31:15] an extreme level of verification, that
[00:31:17] logic of how you handle that ver like it
[00:31:19] again, I think it sounds small, but like
[00:31:21] I totally understand why some people
[00:31:23] feel like they really want to own the
[00:31:24] harness because tweaking that last bit
[00:31:26] will give you a ton of juice and
[00:31:27] especially domains like like legal and
[00:31:29] finance where there's a lot of
[00:31:30] consequences um to you not getting it
[00:31:33] perfectly correct like is really going
[00:31:34] to matter and that's going to be the
[00:31:36] difference between your product and
[00:31:37] someone else's product being the thing
[00:31:38] that the user ultimately uses. Um and
[00:31:41] then there are other domains for which
[00:31:42] like I would say uh it's not going to
[00:31:45] matter as much because you're able to
[00:31:46] compress it into like a general model
[00:31:48] capability. So the tweaks that I guess
[00:31:51] like you know where we feel like the
[00:31:52] domain specificity is really going to
[00:31:54] matter is the specific like verification
[00:31:56] logic between the model and your
[00:31:58] execution. And then um I think it's
[00:32:01] going to be about like some of these
[00:32:03] kind of like higher order strategies on
[00:32:05] how well um you're able to actually like
[00:32:07] allocate your token budget. Um, I think
[00:32:10] the context bit is actually a little
[00:32:12] like overdone. Like yes, you're going to
[00:32:14] like throw in context and like that's uh
[00:32:16] but any harness can actually handle a
[00:32:18] lot of context and so that's just more
[00:32:19] like you have the data and if you have
[00:32:20] the data then obviously you're you're
[00:32:22] uniquely qualified to do something
[00:32:23] useful.
[00:32:24] >> Yeah. And I think when people say
[00:32:25] harnesses they often mean a lot of
[00:32:27] different things and I think this is why
[00:32:29] in part there's so many different
[00:32:31] opinions on this. Like you can think of
[00:32:32] a harness as literally just like a loop
[00:32:35] um that's like okay cool like user model
[00:32:38] user model tool you know like that sort
[00:32:40] of thing. Um then you could think of the
[00:32:42] harness as also all of the tools that
[00:32:45] are packaged up with the harness right
[00:32:47] and and there's just like a lot of
[00:32:48] different definitions of these things.
[00:32:50] And I think the stuff that can be pretty
[00:32:52] generic and like less interesting to own
[00:32:55] and and deal with is what I was kind of
[00:32:56] saying earlier is like getting your
[00:32:58] prompt caching right right like maybe
[00:33:00] that is not the world's most interesting
[00:33:02] thing. Choosing to clear out old tool
[00:33:05] calls from the context window and and
[00:33:07] things like that right are like maybe a
[00:33:08] little bit less interesting and you like
[00:33:10] go a layer higher into some of the stuff
[00:33:12] Angela's talking about and then you get
[00:33:14] into like okay yeah these are things
[00:33:15] that I might want to own and control.
[00:33:18] And so it's interesting with cloud
[00:33:19] manage agents like the thing that we
[00:33:21] built today, we call it higher order,
[00:33:23] but it's not really like that high order
[00:33:26] in the sense that you can choose to
[00:33:28] define all of the tools that you want to
[00:33:30] bring in as custom tools with the
[00:33:32] harness, right? And like we give you a
[00:33:34] lot of knobs to control, you can define
[00:33:36] skills, you can do your system prompts,
[00:33:37] you can do a whole bunch of different
[00:33:38] things, MCP servers and things like
[00:33:40] this. And I think where you know we want
[00:33:42] to get to is a point where you can
[00:33:44] literally just tell an agent here's the
[00:33:46] outcome I want and here's the budget
[00:33:47] that I want to spend like ready set go
[00:33:49] and you may be like don't think about
[00:33:51] any of those things underneath. And so I
[00:33:53] think there's just a few different
[00:33:54] layers of this right that for certain
[00:33:56] things like you might want to sit at a
[00:33:58] different layer of what you actually go
[00:34:00] and control. Um and you can probably get
[00:34:02] better outcomes within some of those
[00:34:04] layers by doing a little bit more
[00:34:06] optimization work.
[00:34:07] >> Very cool. One of the things I'm curious
[00:34:09] about and one that I love about
[00:34:11] infrastructure and platform teams is
[00:34:12] that you get to see what the most
[00:34:13] advanced users in the world are using
[00:34:15] and learn from them. I'm curious what
[00:34:17] are some things that you're seeing and
[00:34:18] learning from from the people building
[00:34:20] on your platform.
[00:34:21] >> There's some people that have been doing
[00:34:22] some really funky ways of like handling
[00:34:25] context. Um we ourselves explore this a
[00:34:28] lot. That's actually like one of the
[00:34:29] reasons why TAG is like uh such a great
[00:34:31] product is like there's a lot of really
[00:34:33] awesome like context kind of engineering
[00:34:34] that that's happening. Um, we've seen
[00:34:36] some teams be really clever about like
[00:34:39] how they do that and they are able to
[00:34:41] kind of think through like, okay, if I
[00:34:42] have all these contacts in a bunch of
[00:34:44] different places, how can I proactively
[00:34:45] go reach out to them? How can I try to
[00:34:47] generate enough like um permissions
[00:34:50] across each of them? So, and then feed
[00:34:52] that all into like an agent. And it's
[00:34:54] interesting that like um I guess like
[00:34:56] this is kind of the level of innovation
[00:34:57] that like we're actually like very
[00:34:58] excited by. It doesn't express itself as
[00:35:00] like a completely different product form
[00:35:02] factor. Um, but what it actually does
[00:35:04] express itself as is like maximally
[00:35:05] useful to users and we've been seeing
[00:35:07] this more and more with like inter
[00:35:09] actually like internal use cases instead
[00:35:11] of like external ones. So like companies
[00:35:13] who are becoming more AI native
[00:35:14] basically they're the ones we're seeing
[00:35:16] increasingly more and more innovation
[00:35:17] out of and so you know we've had like
[00:35:19] customers try to do this for their like
[00:35:22] they've built their own like custom SDLC
[00:35:24] kind of setup in very very innovative
[00:35:25] ways. We've had uh ones who do that for
[00:35:28] like their entire back office and just
[00:35:30] like the kind of nuances of how they
[00:35:32] like stream in context I think has been
[00:35:33] like actually really interesting in
[00:35:35] terms of like how they've been putting
[00:35:36] together the pieces. So that's been like
[00:35:38] one category that's been like really
[00:35:39] really like fascinating. Uh another
[00:35:41] category that's been like really
[00:35:43] interesting has actually been with
[00:35:45] companies that are dealing with like
[00:35:46] really old school software. And so
[00:35:48] there's a lot of like healthcare
[00:35:48] companies um that we kind of engage with
[00:35:50] and you know like they're like the the
[00:35:52] systems I'm working with they don't even
[00:35:54] have APIs. like that's that's a a dream.
[00:35:57] Um and so you know how can they use
[00:36:00] computer use uh and things like this to
[00:36:02] be able to start to kind of automate and
[00:36:04] create more connectivity with our
[00:36:06] systems. Um and that area of innovation
[00:36:08] I think has been really exciting. It's
[00:36:09] been really interesting to see people
[00:36:10] try all sorts of crazy stuff from like
[00:36:12] taking a laptop and trying to like run a
[00:36:13] bunch of things on it to autogenerate a
[00:36:14] bunch of things that then their agents
[00:36:16] can go and use. Um, and this has
[00:36:18] actually been probably like an area of
[00:36:19] um, I think a lot of innovation coming
[00:36:21] from a lot of our customers that we want
[00:36:23] to find ways to like support better and
[00:36:25] see like okay maybe there are like how
[00:36:26] can we make this easier for you? How can
[00:36:28] we help you with some standardization?
[00:36:31] How can we get it so that you know like
[00:36:32] you can just have a spec and then claude
[00:36:34] can then respect it and so it's much
[00:36:36] easier for you to organically connect a
[00:36:38] lot of these things. But yeah, maybe the
[00:36:39] the general theme I would just give you
[00:36:40] is like interestingly a lot of the
[00:36:42] innovation that's most exciting out
[00:36:44] there right now has been uh this kind of
[00:36:46] like context and connectivity layer
[00:36:48] which has been really fascinating.
[00:36:49] >> Yeah. Like a good one in that um we were
[00:36:52] working with a customer who they've
[00:36:54] built some agents on cloud manage
[00:36:56] agents. They also have some agents they
[00:36:57] built on other models and other
[00:36:59] platforms and they've kind of optimized
[00:37:01] each of these agents to be good at the
[00:37:03] things that they want. They want these
[00:37:05] agents to all be able to work well
[00:37:06] together. Um, and they kind of were
[00:37:08] like, "Wow, Galaxy brain. Like, what if
[00:37:10] I expose an MCP server on top of this
[00:37:12] agent so that it can then go and like
[00:37:14] have this other agent call a tool on
[00:37:16] that agent, right? And and have these
[00:37:18] things just be more modular and be able
[00:37:19] to work together." And we were like,
[00:37:21] "Yeah, totally." And we sat down with
[00:37:22] them and worked through it and and it
[00:37:24] worked perfectly and it was pretty cool.
[00:37:25] And so, we're seeing a lot of again that
[00:37:27] connectivity layer that I think is one
[00:37:29] of the cooler areas where people are
[00:37:31] innovating. But outside of that, one
[00:37:34] thing that has been cool is just seeing
[00:37:35] the shift in I guess like industry
[00:37:38] trends of where we're seeing a lot of
[00:37:39] our usage come from like talked a lot
[00:37:42] about coding like coding as a category
[00:37:43] like of course absolutely explode in.
[00:37:45] There's so much going on there and we're
[00:37:47] starting to see some of these emerging
[00:37:48] trends like more recently. Um, we're
[00:37:50] starting to see manufacturing really
[00:37:52] pick up as just a category where people
[00:37:55] are building with AI and like one of our
[00:37:57] PMs like getting on a flight to Detroit
[00:37:59] to go like figure out what these
[00:38:01] customers like what they need and what's
[00:38:03] going on. And so I think we're going to
[00:38:05] start to see a lot more just kind of
[00:38:07] like outside of the box of what people
[00:38:09] think about today sort of use cases
[00:38:11] which we're really excited about. H
[00:38:13] >> it seems like there's now there's a we
[00:38:15] went through a token maxing moment of
[00:38:16] history and now there's like the token
[00:38:19] rationalization moments of history. What
[00:38:21] are your thoughts on that and like what
[00:38:23] what should companies be doing and then
[00:38:25] how how does the platform team think
[00:38:26] about uh enabling that?
[00:38:28] >> Yeah, I mean it it makes sense. Uh it it
[00:38:31] makes sense from the high you start to
[00:38:33] rationalize. I I really like that
[00:38:34] framing and I think there's like a
[00:38:36] couple things that that are like top of
[00:38:37] mind for us on this front. I think like
[00:38:39] again it makes sense and as these models
[00:38:40] get more and more capable you're going
[00:38:41] to hit like levels of intelligence max
[00:38:43] maxing that are like there that then you
[00:38:45] want to do the next kind of dimension
[00:38:47] and the next dimension after
[00:38:48] intelligence will either be cost or it
[00:38:50] will be speed. Um and you just kind of
[00:38:53] you know go through that across all
[00:38:54] possible tax complexities in the
[00:38:55] distribution. Um, and as we kind of see
[00:38:58] that like happen, you know, something
[00:38:59] that's like really top of mind for us
[00:39:00] that we kind of try to spend some time
[00:39:02] with users on is like what you don't
[00:39:04] want to do is like stop AI usage, right?
[00:39:06] Like that's kind of the wrong move. And
[00:39:07] we do actually see some of our our
[00:39:09] customers do that. So oftent times the
[00:39:11] way that AI spend has erupted inside
[00:39:13] their company has been through some kind
[00:39:14] of like uh shadow IT, you know, like
[00:39:16] their employees just like want to use
[00:39:18] it, they find a way, they end up
[00:39:19] procuring it themselves, and before you
[00:39:20] know it, like half your or has like
[00:39:22] found some way to have installed cloud
[00:39:24] code. And in that world it is kind of
[00:39:25] hard to to manage because these things
[00:39:27] are again like they're very token hungry
[00:39:28] ultimately. And so what we try to kind
[00:39:30] of encourage our customers is like okay
[00:39:31] you don't want to like stop the
[00:39:32] innovation like if you are getting
[00:39:34] returns on top of this you are shipping
[00:39:35] faster than ever before you can like run
[00:39:37] more operationally like uh efficient
[00:39:40] then those are gains. And so the area
[00:39:42] that we actually try to encourage people
[00:39:44] is like if there is a way for you to
[00:39:46] kind of construct again like a strategy
[00:39:48] that allows you to design an
[00:39:49] architecture that says like given a task
[00:39:51] assesses level of complexity. I mean I'm
[00:39:53] effectively describing a router but like
[00:39:56] there are ways to do this that are like
[00:39:57] I think a bit better now and so like
[00:39:58] this task comes in has a certain level
[00:40:00] of complexity for that level of
[00:40:01] complexity like you can define some
[00:40:03] rules but for the most part right if
[00:40:04] it's like a hard task you should
[00:40:06] probably route that to like a big super
[00:40:08] smart model and if it's not a hard task
[00:40:09] you can route that to like cheaper
[00:40:11] models um designing that I think has a
[00:40:13] little bit of like there's a lot of
[00:40:14] technical complexity in that but it's
[00:40:15] like very very doable and we actually
[00:40:17] like encourage people to try those kinds
[00:40:19] of things I think ultimately
[00:40:20] >> offer rather
[00:40:21] >> I I think within the clawed space it
[00:40:24] will like make sense. It's actually one
[00:40:25] of the strategies we imagine like
[00:40:26] designing because the way that we kind
[00:40:28] of thinking a lot of these things is
[00:40:29] like it almost feels like every month
[00:40:31] there was a new era of something. Um and
[00:40:33] if we take a step back like okay and
[00:40:35] this seems to be like really fast and so
[00:40:37] what are the different ways that are
[00:40:38] recomposable so we can redesign very
[00:40:40] quickly for any new whatever the cool
[00:40:43] thing is that month kind of like bit. Um
[00:40:45] and so this is like in that category of
[00:40:47] things where we feel like we can
[00:40:48] actually just like recompose a lot of
[00:40:49] our primitives and then design it. I
[00:40:52] think the bit that we do feel really
[00:40:53] strongly about on the model routing
[00:40:55] front is like we are designing our
[00:40:58] platform for Claude and we want to make
[00:40:59] sure that Claude is great at like
[00:41:01] solving all these things. So we'll like
[00:41:03] restrict to that space um rather than
[00:41:06] you know I don't think we're that
[00:41:07] interested in saying like okay and then
[00:41:08] you know you should route to a different
[00:41:09] model or whatever.
[00:41:11] >> Makes sense.
[00:41:11] >> Yeah. and and well some of that too is
[00:41:13] just like I think we have a strong
[00:41:14] belief that harnesses and and just like
[00:41:17] the agentic layer should be tuned to the
[00:41:19] model family that you use it with. And
[00:41:21] so I think there was a period where
[00:41:23] people were kind of like yeah cool I can
[00:41:24] like build a harness and build an agent
[00:41:26] and then just like plug in a different
[00:41:28] model underneath and they were excited
[00:41:29] about routers from that perspective. And
[00:41:32] I think we started to see um like
[00:41:34] Verscell just did this with harness
[00:41:35] agent for example like some of these
[00:41:37] players in the space like come up a
[00:41:40] layer of abstraction and say actually
[00:41:41] like plug in the whole harness and the
[00:41:43] whole agent that's tied to a model
[00:41:44] family which makes a lot of sense and so
[00:41:46] what we could provide is a little bit
[00:41:47] better smarter like how do you mix and
[00:41:49] match the right models within the model
[00:41:51] family underneath that thing if that
[00:41:53] makes sense. But yeah, on the general
[00:41:55] question of token maxing costs and these
[00:41:57] sorts of things, I think we're just kind
[00:41:59] of going through what feels like a
[00:42:01] normal natural cycle for companies and
[00:42:03] figuring out how to make the best use of
[00:42:05] this technology and run their businesses
[00:42:08] really well and really effectively. And
[00:42:10] um it's interesting like before working
[00:42:12] at Anthropic I was at Stripe and we were
[00:42:14] kind of in the very reasonable era of
[00:42:16] like we paid a lot of attention to our
[00:42:18] AWS bill and so you know if someone were
[00:42:21] to have built some background job and
[00:42:23] they like didn't quite configure it
[00:42:25] correctly and this thing's like burning
[00:42:27] through like CPU or whatever it is right
[00:42:30] like at any given moment and causing you
[00:42:33] know big increase in spend that's not
[00:42:34] actually worth it right like we have put
[00:42:37] in place the guardrails to find that and
[00:42:39] then go ask that engineer very nicely to
[00:42:41] please turn off their background job
[00:42:42] that's not like within the bounds of of
[00:42:45] what they should be spending for the
[00:42:46] thing they're trying to accomplish. I
[00:42:48] think those are the things with AI that
[00:42:50] people are going to start to go and
[00:42:52] figure out. And I think to Angela's
[00:42:53] point, a thing that gets dangerous is
[00:42:55] when you're kind of just like here's a
[00:42:57] cap and you're stuck within your cap
[00:42:59] like ready, set go. But I do think that
[00:43:02] encouraging innovation, encouraging
[00:43:04] people to, you know, create really
[00:43:06] excellent outcomes with this stuff and
[00:43:08] then coming in from the side and looking
[00:43:09] and saying like, okay, well, there are
[00:43:12] few different ways that we probably
[00:43:13] could have accomplished that outcome,
[00:43:15] right? And one is like you take Opus and
[00:43:18] you run it all night and you do
[00:43:20] something crazy. And another is maybe to
[00:43:21] get a little bit smarter with the
[00:43:23] strategies that you put together in
[00:43:24] order to create that same outcome within
[00:43:26] a lower cost. And I think that's the
[00:43:28] like next layer of thinking that
[00:43:30] everyone's going to start to do.
[00:43:31] >> Very cool. Is there anything that you
[00:43:33] guys are excited about building over the
[00:43:34] next few months that you can share a
[00:43:35] hint at what might come next?
[00:43:37] >> Uh yeah. I mean I know we said this word
[00:43:39] like 20 million times. I apologize but
[00:43:40] like we really are trying to build ways
[00:43:42] for you to compose strategies. Um and so
[00:43:45] uh that is an area that that we're like
[00:43:48] trying to move into that kind of like
[00:43:49] yeah uh coordination layer of the
[00:43:51] abstraction. Um, and we want to start at
[00:43:53] this front because the types of problems
[00:43:54] that we see people building, they are at
[00:43:57] a layer where it's like in order to get
[00:43:59] the most return on this, you have to be
[00:44:01] a little clever about like what is the
[00:44:03] nature of the problem that you're
[00:44:04] solving. So to give you something like
[00:44:06] concrete like when you try to solve for
[00:44:08] like let's say you want to build an
[00:44:09] agent that's like trying to um do bug
[00:44:12] hunting and you could just send one off
[00:44:15] to go and do that and it's going to give
[00:44:16] you a certain type of return a level of
[00:44:18] return of possibility um and then people
[00:44:20] kind of get stuck at that and they're
[00:44:22] like okay my next options are I can like
[00:44:24] make a bigger I can just like swap the
[00:44:26] model for a different I probably bigger
[00:44:28] model um or I could like let it run like
[00:44:31] longer and that's pretty much like the
[00:44:32] only two like levers that you have to
[00:44:34] like try to make this like bug hunting
[00:44:35] agent. From a lot of experimentation,
[00:44:37] when we do these kinds of things,
[00:44:38] there's like actually the thing like
[00:44:40] those two those two things are still
[00:44:42] true, but you actually have like a third
[00:44:43] lever and tends to actually do a lot
[00:44:45] more than you think it does, which is
[00:44:46] that actually if you were to like best
[00:44:48] of end the thing, it would like give you
[00:44:50] a lot more returns. But like just to be
[00:44:51] just saying those words are fine and
[00:44:53] there's plenty of papers and people have
[00:44:54] published it to actually build that
[00:44:56] thing and put it into production so you
[00:44:57] can actually test it on users uh and see
[00:44:59] the results for yourself, that's like
[00:45:01] really really freaking hard. and you end
[00:45:02] up building all these like custom
[00:45:03] harnesses so on so forth like you know
[00:45:05] all that stuff. Um but we're seeing like
[00:45:07] this is where the alpha is and it's hard
[00:45:09] and so like in the same very simple
[00:45:11] philosophy that we talked about at the
[00:45:12] beginning like if it's like gives you
[00:45:14] the return that you want and it's hard
[00:45:15] we're going to try to make it easy for
[00:45:17] you so then you can use it to then run
[00:45:19] the experiments you actually need to
[00:45:20] run.
[00:45:20] >> Reminds me of when people are talking
[00:45:22] about agent swarms a year ago. It's some
[00:45:24] version of that.
[00:45:25] >> Has it been a whole year?
[00:45:26] >> Yeah. Oh my god,
[00:45:27] >> I know. We're finally there.
[00:45:28] >> Yes. Um yeah. No, I think that that's
[00:45:31] like that's a type of strategy. Exactly.
[00:45:33] In the same way that you have like, you
[00:45:34] know, one big one that separates a bunch
[00:45:35] as another type of strategy. And I think
[00:45:37] people have thought about this maybe the
[00:45:38] in the way of like human organization.
[00:45:41] >> I guess it could be similar, but if you
[00:45:42] take it to kind of its ends, it's
[00:45:43] actually more just like the token has a
[00:45:45] job. And I think it's this job piece
[00:45:47] that we're we're really indexed on and
[00:45:49] um we see a lot of returns too and
[00:45:52] that's the thing that we want to spend
[00:45:53] time with users and the rest of the
[00:45:55] ecosystem on on like how can we just
[00:45:56] make that easier for folks to then
[00:45:58] experiment like we can give you like
[00:46:00] five jobs off the top of our head and
[00:46:01] we'll probably like that's what we have
[00:46:02] internally. Um and if we give this out
[00:46:04] to the rest of the ecosystem there's
[00:46:06] probably going to be like 100,000
[00:46:07] 200,000 who knows what other
[00:46:08] combinations that people could put
[00:46:09] together. Yeah, we want to be able to
[00:46:11] keep doing this hill climbing on like
[00:46:13] how do you get the most value, the most
[00:46:15] intelligence per dollar and just put
[00:46:17] that power in people's hands, but around
[00:46:19] the edges of that, we have these
[00:46:21] personas that have kind of just like
[00:46:23] things they have to work through in
[00:46:24] order to be able to like really deploy
[00:46:26] AI either within their companies or
[00:46:29] within their products. And um that's
[00:46:32] like the sort of enterprise ready
[00:46:34] security and compliance controls and
[00:46:36] things like this. But really even just
[00:46:38] like making the platform more modular in
[00:46:41] the right ways like being able to plug
[00:46:42] in different pieces of the solutions
[00:46:44] that we're building like I want to use
[00:46:45] memory for this thing over here, right?
[00:46:47] or whatever else it is and having a
[00:46:50] truly excellent developer experience
[00:46:52] around that because we spent a lot of
[00:46:53] time with enterprises who are like okay
[00:46:56] I have this like walled garden and I
[00:46:58] need to figure out exactly how I can
[00:47:00] plug these solutions in and so we're
[00:47:02] we've got a part of our team that's
[00:47:03] innovating on things like strategies and
[00:47:05] jobs and trying to help you maximize
[00:47:06] intelligence and they're like that's
[00:47:08] really cool but I can't actually use any
[00:47:09] of that for XYZ reasons. So I think
[00:47:11] solving those problems is really really
[00:47:13] important to us. But then the other
[00:47:14] persona is you know the like weekend
[00:47:16] developer who's like I want to go and
[00:47:19] build something useful for myself right
[00:47:21] and they're often doing that on top of
[00:47:23] our platform and on top of many other
[00:47:25] just pieces of developer platforms in
[00:47:26] the community. And I think for some of
[00:47:28] those folks, there's more that we can do
[00:47:31] to be provide solutions that are maybe
[00:47:33] more open or more hackable or whatever
[00:47:34] it might be for those folks to kind of
[00:47:37] just like go wild with what we can offer
[00:47:39] them and have this really excellent
[00:47:41] developer experience. And so I think
[00:47:43] there's a lot of stuff that maybe I
[00:47:44] would put in the category of table
[00:47:46] stakes that I'm really excited about
[00:47:48] because I think those are the things
[00:47:49] that then unlock getting people to say,
[00:47:52] "Okay, yes, this thing works for me and
[00:47:54] now I can plug in on some of the stuff
[00:47:55] that you guys are doing." that's really
[00:47:57] innovative and hill climby to get more
[00:47:59] intelligence and save costs and things
[00:48:00] like that.
[00:48:01] >> Wonderful. Caitlyn, Angela, I feel I
[00:48:04] mean you are building one of the most
[00:48:06] important developer platforms in the
[00:48:07] world and talking to the two of you over
[00:48:09] time. I just feel really optimistic that
[00:48:11] that platform is in very thoughtful uh
[00:48:15] hands that that care about the
[00:48:16] ecosystem. So, thank you for taking the
[00:48:18] time today to share what you're up to
[00:48:19] and um we look forward to what's ahead.
[00:48:21] >> Thanks for having us.
[00:48:22] >> Thank you guys.
