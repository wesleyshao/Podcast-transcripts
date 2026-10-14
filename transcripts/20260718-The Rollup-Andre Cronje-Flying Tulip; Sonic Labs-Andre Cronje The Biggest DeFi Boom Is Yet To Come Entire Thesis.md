---
访谈时间: "2026-07-18"
访谈时间说明: "未能确认独立访谈录制日期，使用 YouTube 发布时间。"
嘉宾名字: "Andre Cronje"
嘉宾公司名称: "Flying Tulip; Sonic Labs; Yearn Finance"
播客名称: "The Rollup"
播客url地址: "https://www.youtube.com/watch?v=GXiXj6HYnfQ"
全文提及的关键名词:
  - "Andre Cronje"
  - "Flying Tulip"
  - "DeFi"
  - "Sonic"
  - "Yearn Finance"
  - "decentralization"
  - "circuit breakers"
  - "upgradable contracts"
  - "Flying Tulip USD"
  - "delta-neutral staking"
  - "RFQ liquidations"
  - "equity margin accounts"
  - "single asset pools"
  - "stablecoins"
  - "composability"
  - "curated vaults"
字幕来源: "automatic_captions:en-orig:English (Original)"
YouTube视频标题: "Andre Cronje: The Biggest DeFi Boom Is Yet To Come (Entire Thesis)"
---

# Andre Cronje: The Biggest DeFi Boom Is Yet To Come (Entire Thesis)

## Transcript

[00:00] We are live with Andre Cronier, uh, true
[00:02] DeFi OG in the building with us here
[00:05] today. It's not his first time. You guys
[00:07] know him well. I'm sure you guys have
[00:09] seen his, uh, products on chain before.
[00:11] Probably deposited into one if not a few
[00:14] of them.
[00:16] Sonic, list goes on. Today, we're going
[00:19] to be talking about Flying Tulip. Uh, as
[00:21] I mentioned earlier, you know, very
[00:22] unique launch strategy here. Uh, we, uh,
[00:26] fundraising strategy as well. So, we're
[00:27] going to get into some of that. This is
[00:29] our weekly stablecoin show powered by
[00:32] FRA and so FRA is doing great work.
[00:35] Genius compatible stablecoin open stable
[00:38] borderless. Uh Andre, man, it's a
[00:40] pleasure to welcome you back to the
[00:41] rollup.
[00:42] >> Likewise. Nice to be back.
[00:45] >> Absolutely.
[00:46] >> Don't think it that long ago I was on
[00:47] here or at least it doesn't feel that
[00:48] long ago.
[00:49] >> I think it was just a few months
[00:51] actually. What uh what have you been up
[00:52] to?
[00:53] um roll out mostly, you know, trying to
[00:56] get products online as
[01:00] as quickly as security allows
[01:05] and hopefully as fast as investors want,
[01:09] which is always a a interesting tug and
[01:12] pull game, I think. Um
[01:14] >> do you uh do you find yourself wanting
[01:18] to ship faster than investors want you
[01:21] to? No, no, no. I mean, investors always
[01:24] want everything live yesterday. Um,
[01:26] security is always the biggest
[01:28] constraint, you know, because it's
[01:32] audits is one thing. Um, I I think
[01:38] while audits are very important, they're
[01:40] a little bit overplayed in the space and
[01:42] not not overplayed. too much emphasis is
[01:46] put on only audits and then a lack of
[01:49] you know infra security, key security,
[01:53] um secondary order securities, things
[01:56] like circuit breakers or outflow
[01:57] monitoring.
[01:59] Um and those things take time you know
[02:01] like um capped launches, slow approaches
[02:05] and it it also creates user friction
[02:07] which in itself isn't nice
[02:10] >> because you end up limiting what your
[02:12] users can do at any given point in time
[02:14] and that also you know prevents scaling.
[02:16] >> Yeah. Yeah. I just saw there was a
[02:18] recent uh I think it was a vulnerability
[02:20] on OIUM the perex and $18 million left
[02:24] the protocol like that and people are
[02:25] calling Yeah. Yeah. That's why circuit
[02:27] breakers exist. they're a feature, not a
[02:29] bug. Um, and so, uh,
[02:33] >> so historically, circuit breakers didn't
[02:36] really make sense because
[02:39] there were only two interacting parties.
[02:41] It was the depositor and the smart
[02:43] contract. There there was nothing else.
[02:45] There was no multi-IG. There was no, you
[02:49] know, off-chain counterparty.
[02:52] Um,
[02:54] so old
[02:56] we we've inherited
[02:59] a lot of the design principles of old
[03:04] DeFi
[03:06] into this new category where we are now,
[03:08] which which is closer to onchain
[03:10] companies than it is decentralized
[03:13] finance. Um, so
[03:17] you know, back then if you had a smart
[03:19] contract and someone could not have
[03:22] instantaneous liquidity, you you'd be
[03:24] dead in the water right off the bat.
[03:27] >> Nowadays that you have, you know, a line
[03:30] of communication, a support channel,
[03:32] people you can reach out to. I I I think
[03:36] the assumptions are very different. And
[03:39] circuit breakers now make sense as well,
[03:41] right? Because circuit breakers are
[03:42] there
[03:44] And and our our system is also
[03:48] multiple layers of circuit breakers. And
[03:51] I've seen the friction it causes for
[03:52] users, you know, cuz a user might be
[03:54] used to or or or the fear it can cause,
[03:56] right? Cuz cuz using our circuit breaker
[03:58] as an example,
[04:00] we
[04:02] when you request the funds out, it goes
[04:04] into a queue and then you can claim it
[04:06] in 6 hours. But now myself sometimes
[04:09] while using the system I'll I'll claim
[04:10] it and I'll go check on epher scan and
[04:13] I'll see oh it didn't go to my wallet it
[04:15] went to zero xcb which is our server
[04:18] I've seen this
[04:19] >> but you know in my mind I'm like holy
[04:20] crap what went wrong meanwhile you know
[04:22] it's just sitting there waiting to be
[04:24] released so that I can claim it in a few
[04:25] hours but but something as simplistic as
[04:27] that you know causes fear and panic from
[04:29] a user's perspective.
[04:31] >> Yeah. Yeah. And hopefully we can solve
[04:32] some of that with UX developments,
[04:34] right? And a lot of this is you know
[04:36] going to be obfuscated underneath the
[04:37] hood. And you know the the I think a lot
[04:40] of one of the building principles that I
[04:42] I've heard from developers as of
[04:43] recently has been look we're building
[04:45] for the next cohort of users not
[04:48] necessarily the cryptonative ones that
[04:50] have been here and are the most
[04:51] sophisticated. you know, we're okay with
[04:53] sort of showing something on the UX
[04:55] side, right? And and on underneath,
[04:58] right? we know that, you know, it's in
[05:00] the circuit breaker. It's going to get
[05:01] claimed, but we're going to show the
[05:03] number as if it's, you know, still with
[05:06] the user because ultimately it will be
[05:08] and sort of
[05:10] >> maybe take some shortcuts that, you
[05:12] know, back in, you know, the the more
[05:14] the the DeFi purist days wouldn't
[05:17] wouldn't have really been uh wi within
[05:19] the realm of what people would have been
[05:21] accepting.
[05:23] >> Yeah. I mean, back then, you know, if
[05:25] again, if your counterparty is just a
[05:27] smart contract, I think it's not it's
[05:30] not too much for the user to expect that
[05:33] they have instant liquidity and instant
[05:35] access. Um, that's a fair ask if the
[05:40] only thing I can talk to is the smart
[05:42] contract, you know, cuz I can't cue a
[05:45] transaction in the smart contract and
[05:47] then ask someone to expedite the queue
[05:50] for me because in some cases, you do
[05:52] need to do that. So I look I I think
[05:57] the the old age fight between security
[06:01] and user experience is as old as time.
[06:03] You know I mean it comes down to you can
[06:06] have a password of one two three which
[06:09] from a user experience side is more
[06:12] convenient but much less secure. So what
[06:17] did they start doing? They started
[06:18] enforcing more and more complex
[06:21] passwords. Now you need at least eight
[06:24] characters and you know alpha numeric
[06:27] capitalization
[06:29] and some symbols. That's a lot harder to
[06:33] remember but it enhances the security.
[06:35] So so security and UX will always fight
[06:39] with each other.
[06:40] >> Yeah. I think this is just a part of the
[06:42] space maturing where we're starting to
[06:44] realize, look,
[06:46] we have to start including
[06:50] these small UX frustrations that
[06:54] ultimately provide a better order of
[06:57] magnitude in security.
[06:59] >> Mhm. Especially
[07:02] as
[07:04] and and and this is again a huge
[07:06] difference between you know sort of 2020
[07:08] 2021 or even earlier as early as 2018
[07:11] decentralized finance which was the goal
[07:14] was pure immutability and pure
[07:17] decentralization.
[07:18] >> Right nowadays
[07:21] I I'm I don't even preach that anymore.
[07:23] If if if if I work with a new team and
[07:26] they ask me if they should have their
[07:28] contracts upgradable or immutable, I
[07:30] always tell them upgradeable. I I think
[07:32] it's non-negotiable nowadays. You have
[07:34] to be able to upgrade your code. But
[07:38] that immediately means you have the
[07:40] biggest threat vector known to your
[07:42] entire protocol. Cuz if if if
[07:44] >> if if you have one developer key that's
[07:46] sitting on some guy's PC and he's able
[07:49] to unilaterally do a upgrade call on
[07:51] that contract, that can steal all of the
[07:53] money. So now you already have to make
[07:56] sure there are and and this is why I
[07:59] say, you know, smart contract audits
[08:00] aren't what they used to be. they're
[08:03] they're still majorly required but the
[08:06] best audits in the world won't capture
[08:08] that vector
[08:09] >> you know so you need
[08:12] >> traditional security in front now as
[08:14] well to make sure hey the the the key is
[08:17] properly offsite and you know probably
[08:19] some HSM signing or ideally the deployer
[08:22] key should be immediately handed over to
[08:25] you know a time lock and a multisc um
[08:28] but even therein is now again a
[08:31] different
[08:32] a different trade-off of consideration
[08:34] that you need to make because if if the
[08:35] contracts are fresh and you just
[08:37] upgraded it, you might you might not
[08:39] want the time lock because you might
[08:40] want you might need to be able to
[08:42] respond within a fairly short time
[08:44] window. Now, if something goes wrong,
[08:46] you can't wait 72 hours to do an upgrade
[08:49] or a freezer or something. So,
[08:51] >> so your your your contracts can't just
[08:54] be a single admin role and that admin is
[08:57] a time lock and that time lock is in a
[08:59] multisc. So using ours as an example,
[09:02] anything that moves money sits behind
[09:05] time lock and sits behind a multic.
[09:07] Anything that can that can momentarily
[09:11] pause or delay. So something that can
[09:13] either drag out the circuit breaker a
[09:15] little slower or pause funds outflow
[09:18] that can't sit behind the time lock. you
[09:20] know that we we we need to do in
[09:22] collaboration with and I mean there's
[09:24] some great teams out there that were
[09:25] also trying to still on board um
[09:27] Hypernative Seal 911 obviously um so you
[09:33] you know now all of a sudden from the
[09:36] base code level you need to start
[09:38] thinking about this role separation and
[09:40] how how these separate roles can sit in
[09:44] their separate areas.
[09:46] >> Yeah. Yeah. I I think you know this is
[09:48] one fantastic observation given that
[09:51] you've been you know in the space you've
[09:52] worked on multiple projects you've
[09:54] you've got the benefit of hindsight and
[09:57] uh and learning through the iterations
[09:59] of some of these things and you know
[10:01] there there's been several iterations
[10:03] that this space has gone through you
[10:05] know philosophically which calls for
[10:07] different design choices both on the on
[10:10] the security front as well as on the UX
[10:12] front and as you said these things are
[10:13] are constantly at odds with one another
[10:16] as we you We'll we'll get into Flying
[10:18] Tulip and and kind of the nuts and bolts
[10:20] there and and you know all all the
[10:22] updates, but I'm just curious before we
[10:23] dig in deeper. You know, some general
[10:26] observations that you've had. You
[10:27] mentioned auditability. You mentioned
[10:29] sort of this dichconomy, security, and
[10:31] UX. You know, some of some of your
[10:34] projects, you know, you you've you've
[10:35] worked on they're they're continuing to
[10:37] run. Um what have been the lessons like
[10:41] you know what are what are some of the
[10:42] the observations you know the general
[10:46] shifts and evolutions that the space has
[10:48] gone through that you're now putting
[10:50] into pro in in into practice with flying
[10:53] tulip you know in addition to
[10:55] auditability and security what else have
[10:58] you noticed about the space that's
[10:59] changed since you know the the the good
[11:03] good old days if you will
[11:05] >> um I I I think the most important Second
[11:07] one is decentralization is dead. Um
[11:11] we're no longer striving towards
[11:12] decentralization.
[11:14] If
[11:18] if if nowadays
[11:20] and and and and truth be told, I I I
[11:22] think this shift even started happening
[11:24] around
[11:26] probably towards the end of 2023, maybe
[11:30] even 2024 cuz I
[11:33] some
[11:36] year's
[11:37] fair launch
[11:39] which
[11:41] you know the the the so-called
[11:42] immaculate conception like like from the
[11:44] get-go I designed it as a mechanism of
[11:48] decentralization which is why you know I
[11:51] didn't have tokens everything was given
[11:52] away to the protocol users there was no
[11:55] team there was no foundation there was
[11:57] none of those allocations the goal there
[11:59] was decentralization right it's it's the
[12:03] it it it was trying to as closely
[12:08] copy
[12:10] the Bitcoin playbook where the original
[12:12] founder leaves and a community has to
[12:15] take it over. Um that today
[12:20] that today people are won't be
[12:22] interested in. People won't want that.
[12:24] They they need someone behind it that
[12:27] keeps driving value because the the
[12:31] tokens
[12:33] have become almost too valuable to the
[12:36] point where
[12:38] the the person holding the token. the
[12:40] and and this is also just an evolution
[12:42] of the of the user base interacting with
[12:47] blockchain and crypto as a whole cuz
[12:52] back then the majority of users were you
[12:54] know technocrats or at least technically
[12:57] educated people and they understood the
[13:00] token's value beyond
[13:03] it as an investment vehicle and I think
[13:05] nowadays everyone sees it first as the
[13:09] investment vehicle And second as a
[13:12] utility based something or anything like
[13:13] that. Um another example of immutability
[13:17] being dead you know is is something like
[13:21] um the decentralized
[13:24] um keeper network that we built
[13:26] originally for urine and [snorts] maker
[13:27] and a bunch of the stuff that was using
[13:29] it back then. that was again moving
[13:31] towards a decentralization and b
[13:35] immutability in that it was designed as
[13:38] a marketplace for unknown actors
[13:45] to be able to work jobs and provide
[13:48] facilities on chain. Uh again nowadays
[13:52] you know everyone just does their own
[13:53] infra offchain. They run their own they
[13:56] run their own bots their own keepers
[13:57] their own liquidation systems. It's it's
[13:59] not about trying to do it onchain
[14:01] anymore. Um it shifted more and more
[14:03] offchain.
[14:04] >> And then
[14:06] lastly, you know, immutability used to
[14:10] be a feature. Nowadays, I think it's a
[14:12] bug um in that it doesn't because cuz
[14:15] now if if you combine all of this, so
[14:17] you combine a new base that are looking
[14:18] at these things as an investment vehicle
[14:20] and no longer as a utility based thing.
[14:22] you are looking at teams that have to
[14:26] run more and more of their own infra
[14:28] offchain which means you know there's
[14:32] there's
[14:34] there's AWS or Google or Herzner or
[14:36] wherever you're hosting but but there's
[14:38] bills to pay right I mean apps again
[14:41] back in the original DeFi you know you'd
[14:44] throw up a UI on IPFS people would
[14:46] access it remotely you you wouldn't be
[14:49] hosting servers and infront stuff I mean
[14:51] the original year ran entirely on chain
[14:54] there. There was no off-chain server
[14:57] there. There was nothing. The only thing
[14:58] I paid for was the domain name. So
[15:03] that won't work nowadays because people
[15:05] need that extra usability. They need
[15:08] that access. They need that support
[15:09] channel. And and the second you need to
[15:11] provide all of these secondord functions
[15:13] that's not just smart contracts,
[15:16] you the the team needs to be
[15:19] appropriately incentivized. you know,
[15:20] you need to be able to pay salaries.
[15:22] People need to be able to stay on board,
[15:24] understand the vision, and want to see
[15:28] the vision beyond, you know, a two-year
[15:30] vesting term.
[15:32] >> Um, so I think it's drastically changed.
[15:34] I I I I don't think it's comparable at
[15:36] all. And that's why technically I'm
[15:39] actually a little bit against even still
[15:40] calling it DeFi because I don't think
[15:42] we're anywhere close to DeFi. I I
[15:45] generally when I talk to people I call
[15:46] it onchain finance if I do call it
[15:48] anything
[15:49] >> which is closer you know cuz because
[15:52] it's it's normal finance it's just we we
[15:54] we do things onchain that's the big
[15:57] difference.
[15:58] >> Yeah we call we call it neo finance
[16:01] which is effectively the same thing
[16:02] because it's not decentralized. You're
[16:04] absolutely right, but it takes there are
[16:06] certain functions that take place
[16:07] onchain and then there's a whole
[16:10] amalgamation of functions that take
[16:12] place offchain and users are just okay
[16:14] with it now because a of a combination
[16:17] of things. People have gotten burned,
[16:19] right, as a result of just code is law
[16:21] and not knowing any better. And also the
[16:24] cohort of people coming in, you know,
[16:26] they rely on some of the functionality
[16:28] that they've become accustomed to and
[16:30] the consumer behavior calls for, you
[16:32] know, customer support channels and
[16:34] forgot password buttons and and and
[16:36] these sorts of things. And so these are
[16:38] the design principles that they've come
[16:40] to expect. And I think you know maybe
[16:43] there has been this you know kind of
[16:46] this acceptance rather than you know
[16:49] trying to beat the drum and explain
[16:51] decentralization to people and expecting
[16:53] them to come to us and learn and adopt
[16:55] our our principles. We've decided no
[16:58] we're going to meet people where they
[17:00] are for the benefit of the adoption of
[17:02] this technology. We're going to build
[17:03] with their consumer behavior in mind and
[17:06] we're going to, you know, make the
[17:07] design choices that, you know, maybe
[17:09] sacrifice a little bit our on our own
[17:10] principles, but um, you know, as a
[17:13] whole, everyone is somewhat better off
[17:15] because something is better than
[17:17] nothing.
[17:20] >> In principle, agree. Yeah. I I I think
[17:23] the the gap comes in
[17:26] that we still have a lot of actors
[17:28] trying to sell
[17:31] >> it as if it's decentralized finance, you
[17:33] know, as if your counterparty risk is
[17:36] only
[17:38] the smart contract. And I think that
[17:41] disconnect is where the risk comes in.
[17:44] It's
[17:46] because
[17:48] I I I mean a perfect example is is is
[17:52] this new generation of curated vaults,
[17:55] right? Like like they would have you
[17:56] believe that the trust assumptions is
[17:58] the same as the old 2020 year vaults as
[18:00] an example
[18:02] >> where where there your counterparty was
[18:04] only the smart contract and the
[18:05] downstream you know whether it was a
[18:08] compound etc. Um,
[18:10] nowadays it's still happening onchain,
[18:14] but your counterparty is a curator. It's
[18:16] offchain. It's potentially a credit
[18:19] facility. It's potentially
[18:22] some non-liquidatable onchain RWA or
[18:27] some IOU. But
[18:30] if if you go and deposit in that vault,
[18:32] it's still kind of being presented as
[18:36] your counterpart is just a smart
[18:37] contract. Mhm.
[18:39] >> Um,
[18:39] >> yeah.
[18:40] >> So, and and and and the same is true for
[18:43] for tokens, right? So, I mean, if if you
[18:47] were to have a publicly listed token
[18:50] somewhere, there are very specific
[18:54] requirements in terms of disclosures,
[18:56] compliance,
[18:58] public audits, these kinds of things
[19:00] that are required. And we're trying to
[19:04] play in that space, but at the same
[19:06] time, we're still kind of avoiding
[19:10] that level of reporting and transparency
[19:13] etc. So now and and don't get me wrong I
[19:17] I don't think generally speaking it
[19:19] comes from a place of malice. I think
[19:21] it's a transitionary period that we're
[19:23] currently in where it is the old DeFi
[19:28] engineers that are now building
[19:30] fullyfledged businesses and it's just
[19:32] going to take time.
[19:33] >> Yeah. But I I do think there is a little
[19:35] bit of a disconnect in terms of what is
[19:37] being presented versus what it actually
[19:40] is.
[19:41] >> Yeah, I I I think that's right. And so I
[19:44] I mean you mentioned, you know, some of
[19:45] these curated vaults as an example, and
[19:48] you know, I'm sure we can dig into more
[19:49] of those, but I I'd love to dig into
[19:52] Flying Tulip as well. in terms of, you
[19:54] know, how you've been able to, you know,
[19:59] build Flying Tulip in such a way that
[20:01] you've attempted to, you know, make the
[20:03] most of these design choices because,
[20:05] you know, you're right, we're not in
[20:06] this DeFi purist, you know, uh, era
[20:09] anymore and we're also in this
[20:11] transitionary period where we don't have
[20:14] full, you know, clarity, you know,
[20:16] regulation in the US or just full market
[20:18] structure, regulatory clarity. And so
[20:21] there's sort of this transitionary phase
[20:23] and it's still trust me it's not it's
[20:25] not as bad as you know the Gary Gendler
[20:27] era in the US but you know we we've
[20:29] still got a long way to go as well. And
[20:31] so, you know, when it when it comes to
[20:33] some of these design choices, um, and
[20:36] let's, you know, just, uh, for the sake
[20:38] of honing in and and and, you know,
[20:40] understanding stick to the lending and
[20:42] the vault space, maybe you could just
[20:45] first give us a general understanding of
[20:47] Flying Tulip and then we'll get into the
[20:49] design choices that you've made and
[20:50] maybe how you see the the vault space
[20:52] and how you've been able to, you know,
[20:54] observe and implement some of these
[20:55] learnings in into the product.
[20:58] the the product itself,
[21:04] the the the suite of protocols that
[21:07] Flying Tulip really is
[21:10] is
[21:13] most simplistically it is the it's it's
[21:16] the composability of a lending market
[21:19] that can directly feed into an order
[21:22] book so that it offers you know trading
[21:24] and leverage
[21:26] that can directly feed into derivatives
[21:30] insurance.
[21:32] Um, and then we have our settlement
[21:34] layer, which is our native stable coin,
[21:36] the flying tulip USD. Um,
[21:41] it it it almost makes more sense why it
[21:44] exists and why it is the way it is. If
[21:46] you if you go back to again the premise
[21:51] of original DeFi, the original contracts
[21:55] one immutable
[21:57] two because there was no direct teams
[22:01] involved there weren't any fee
[22:02] extractions you know again using the
[22:05] original urine vaults it took zero fees
[22:08] so it's it was easy to build on those
[22:12] protocols because you knew the code was
[22:16] going to stay the way it was and you
[22:18] knew that there weren't fees. Nowadays,
[22:23] you know, you you've got unis swap v2,
[22:25] v3, v4, you've got a v3, v4. There's
[22:29] there's almost always
[22:32] and and they have to because, you know,
[22:34] they've become proper companies.
[22:37] So they need to a be able to
[22:40] continuously upgrade and deploy new
[22:41] systems and b be able to charge fees
[22:43] because they have to pay the people who
[22:45] are supporting these things. But that
[22:48] essentially killed composability cuz
[22:50] that meant cuz I could build a margin
[22:56] trading system on top of a cuz all
[23:00] you're actually doing is le let's say I
[23:03] want to I want to 10x leverage long BTC.
[23:08] What I'm what what what you would do is
[23:10] you would take a flash loan out of USDC.
[23:14] You would then on whatever trading venue
[23:17] you could, let's say unis swap, you
[23:20] would trade the USDC to wrapped BTC. I
[23:24] would deposit that wrapped BTC into a I
[23:29] would then borrow that amount of USDC
[23:33] and repay the flash loan. Now I have a
[23:36] 10x margin position in a but there's no
[23:40] incentive for anyone else to build that
[23:43] because the the fees are all going to a
[23:45] and if a then later on upgrades their
[23:47] system then same problem right I have to
[23:50] now redeploy and rebuild the whole
[23:52] system. So
[23:55] a lot of these features that we've
[23:58] combined in terms of composability is
[24:01] really just
[24:03] because the base layer which is in in
[24:07] the permission world the base layer is
[24:09] the is the lending market. In the in the
[24:12] in the non-permission world it's
[24:14] actually the AMM which is an interesting
[24:16] distinction. Um it needs to be aware of
[24:20] all of the things that's going to be
[24:21] built on top of it. not not necessarily
[24:23] in a it is already built methodology but
[24:26] at least in a terms of
[24:29] I am building in such a open way that
[24:32] these things could in future integrate
[24:34] into me um and and and that's that's
[24:37] also a design element that's
[24:41] you really don't see nowadays in onchain
[24:44] finance anymore because everyone is kind
[24:46] of building to protect their moat which
[24:48] also makes sense because it's businesses
[24:50] now right So you're not really building
[24:53] with other people are going to build on
[24:55] top of me in mind anymore. I I I think
[24:57] those those those days are largely done.
[25:01] >> But that left a massive gap, right? Cuz
[25:03] cuz one thing and and this is actually
[25:05] something I wrote about many many half a
[25:07] decade ago at this point which was back
[25:09] then called dairy swap, derivative swap.
[25:11] It was just one medium article and it
[25:13] was just a concept but then Gendler came
[25:15] in and kind [snorts] of ruined all
[25:17] chances of launching new stuff. So as
[25:19] you say the space is definitely better
[25:21] off. Um but the concept was simple. The
[25:24] concept was why can't idle liquidity
[25:28] sitting inside of a lending market at at
[25:31] the user's choice be deployed into a
[25:34] into a um single-sided liquidity
[25:37] position or if it is already in a AMM
[25:42] why can't the liquidity not being used
[25:44] in the AMM be deployed to a lending
[25:47] market you know and and we've sort of
[25:50] seen people try to do that right cuz
[25:52] you'll have Again using AVA and unis
[25:54] swap as the example nothing stops
[25:56] someone from going to unis swap and
[25:59] launching a a USDT a wtc which is ava
[26:04] USDT and ava wrapped bc pair and
[26:07] depositing that into the pool.
[26:09] The general problem there is that
[26:12] if I as a user rock land on unis swap's
[26:16] front end and I want to trade BTC to
[26:18] USDT,
[26:20] the engine doesn't know that a WB2C and
[26:25] a USDT actually represent the underlying
[26:27] assets because it only sees the
[26:29] tokenized version. Now aggregators have
[26:32] done a lot of work to be able to
[26:34] integrate those custom roots. But now
[26:37] I'm already talking about so many hops,
[26:38] right? like I first have to go to AA
[26:40] deposit stuff then to unis swap then get
[26:41] this stuff then an aggregator then set
[26:43] up this wrap and and it it if we were on
[26:47] that original sort of immutable and
[26:50] fearless and composable world you
[26:52] wouldn't need to do it that way right it
[26:54] it should be as easy as a tickbox that
[26:56] says yeah cool I want to opt in my
[26:58] liquidity for this and and that's the
[27:02] opportunity that's always existed that
[27:04] I've always been like
[27:06] yearning to exploit
[27:08] Um, and and that's where we're at now,
[27:10] right? Is is we've we've we've started
[27:14] with the margin accounts. That's that's
[27:17] and and now I'm probably getting a
[27:18] little bit too much into the weeds of
[27:20] the
[27:20] >> No, no, this is this is great. This is
[27:22] great.
[27:23] >> But but another thing, for example, is
[27:25] is LTV
[27:28] does its job well
[27:31] in old decentralized markets. So, our
[27:35] our lending market, and I'm even
[27:38] hesitant to call it a lending market. I
[27:39] I generally refer to it as margin
[27:41] accounts. Our margin accounts
[27:44] use an equitybased system similar to a
[27:48] margin account on an exchange would. So,
[27:52] so it compares the equity of your
[27:54] account. you know, that takes into
[27:55] account your P&L, that takes into
[27:57] account if you have netted assets like
[27:58] staked E versus E,
[28:00] >> um, staked Salana versus Salana, that
[28:03] that takes all of these extra things
[28:04] into account, which gives you a much
[28:06] more robust position than just
[28:10] LTV cuz just off of LTV
[28:14] and and and this originally actually
[28:15] started because USDE, Athena,
[28:19] um, which is the first time I even
[28:21] started discovering about, you know,
[28:22] Delta neutral
[28:24] yield farming essentially. But but I I
[28:28] was always frustrated that you can't do
[28:31] what Afina does offchain onchain.
[28:34] And the more I tried to kind of discover
[28:37] why, it's because you can't due to the
[28:39] nature of loan to value LTV, you can't
[28:44] hedge your delta away. Because if if my
[28:48] staked E is 90% LTV, there's always that
[28:51] 10% margin I can't get rid of. So it has
[28:54] to be 100 to 100. And you can't do that
[28:56] with LTV, but you can do that with
[28:57] equity based accounts. So you know,
[29:00] there's there are also a plethora of
[29:04] these
[29:06] more granular innovations that I think
[29:09] as a whole are also a step forward in
[29:11] the industry. Um, another small thing,
[29:15] you know, is when we do a trade on our
[29:18] own system,
[29:20] it doesn't just hit our order book. It
[29:22] automatically creates a RFQ order, and
[29:25] that RFQ order goes out and hunts the
[29:27] entire blockchain for liquidity. So, if
[29:29] it can give that user that wants to
[29:32] facilitate that trade a better quote
[29:35] somewhere else, we want to give them
[29:37] that quote.
[29:38] >> Mhm. because it's too often that you
[29:40] know if you go onto the specific
[29:43] AMM's website and you do a trade you're
[29:45] just going to be trading against their
[29:47] pools and and that that's that's not
[29:49] necessarily what the user wants. Now
[29:51] that does it gets fixed again because
[29:54] the responsibility is kind of shift onto
[29:56] the aggregator but but at the same time
[29:57] it shouldn't need to. Um there are lots
[30:01] of these little micro innovations we can
[30:02] go through. Another one I'm really proud
[30:04] of is actually that our liquidation
[30:06] system itself is RFQ based. So, it's not
[30:08] just, you know, you repay the debt, you
[30:10] get to get a chunk of the of the
[30:12] collateral. It's, hey, here's the
[30:15] collateral. You're an RFQ goes out. Give
[30:18] me a bid. And whatever the best bid is
[30:20] is what ends up getting sold. So, I
[30:22] mean, we've had it's unfortunately bad
[30:26] market. So there's been a lot of
[30:27] liquidations on the system and almost
[30:29] always our bad debt are well the
[30:32] liquidatable debt not bad debt the
[30:34] liquidatable debt is repaid dollar for
[30:37] dollar without a haircut to the user.
[30:39] You know it it's small but these little
[30:41] things add up. Mhm.
[30:42] >> Umh
[30:45] but look, all Flying Chulip mission
[30:48] statement really is is that there is no
[30:50] reason that every blockchain, whether
[30:52] it's a layer 1 or a layer 2, shouldn't
[30:55] be a fully featured centralized
[30:57] exchange. Right? If you go log into
[30:59] Binance, Coinbase, Kraken, whatever else
[31:01] right now, you can do lending, you can
[31:03] do yield vaults, you can do spot
[31:06] trading, you can do margin trading, you
[31:09] can do hedging. And and and that's the
[31:12] mission statement, right? It's having
[31:13] the central entry point where you can
[31:16] deposit funds and then offer you all of
[31:19] these features
[31:21] while giving you the best yield, capital
[31:25] efficiency, and composability. Because
[31:27] again, something simple, right? If you
[31:29] can place a limit order on our spot
[31:31] system, that limit order of yours is
[31:33] earning yield because it's in the margin
[31:35] account being lent out on the other
[31:37] side. So there there's never a point
[31:39] where your capital isn't put better to
[31:42] work. But anyway, I'm feeling a little
[31:44] bit too pitchy now and
[31:46] >> this was not the goal.
[31:48] >> I I understand. And I think well I think
[31:49] you're you're also talking about design
[31:51] choices in general that these chains are
[31:52] making and I think you know you've gone
[31:54] and decided and build in in this
[31:56] direction with Flying Tulip but you know
[31:59] the most the most recent example of this
[32:01] is Mega ETH right they they sunset their
[32:04] mega mafia cohort right of third party
[32:07] applications their incubator that they
[32:09] were doing and now you know they're
[32:10] they're going and building firstparty
[32:13] applications which is you know uh what
[32:15] what you say every chain is going to end
[32:17] up doing whether it's an L1 and L2 uh
[32:19] with some of these features in mind
[32:21] because ultimately we've learned you
[32:22] know through so many of these chains
[32:24] these are the primitives that people
[32:26] want and it just makes sense that we
[32:28] have a more composable world of each of
[32:31] these functions on each of these chains
[32:33] I and we uh you know I I want to get
[32:37] into the stable coin element of Flying
[32:39] Tulip. It's something that you didn't
[32:40] talk very much about but it's a core
[32:42] component and this is our stable coin
[32:44] segment on the show. So I want to talk
[32:46] about that. Uh be before we do I just
[32:48] want to close the loop on one thing that
[32:50] you mentioned earlier which was an
[32:51] interesting point. You mentioned how the
[32:53] core base of these composable systems in
[32:57] the traditional world was typically the
[32:58] lending market and I think that was
[33:00] mostly because of the margining profile
[33:02] and you were able to run and now you've
[33:04] actually implemented this equity margin
[33:06] like account on flying tulip. Um, and
[33:08] that's sort of, you know, the base
[33:09] account that gives way to most of these
[33:11] features. But on chain in the past, it
[33:15] had been these AMMs, right? And so I'm
[33:17] just curious about the distinction. Why
[33:19] was it the case that it was AMMs? And
[33:22] why did you choose to include this
[33:24] equity provisioning account on Flying
[33:26] Tulip more akin to the traditional world
[33:28] than the onchain native world?
[33:30] >> So well, the answer there is that it's
[33:33] still both. So, so
[33:37] within flying tulip itself, we have two
[33:39] distinct verticals. We have our
[33:41] permissioned set, which is the one we
[33:43] launched first because it's easier to
[33:45] control. So, the benefit of the
[33:49] permission set is that it's cross
[33:52] collateral. So, I can onboard BTC, E,
[33:56] USDC all in the same margin account. The
[34:00] problem with that is every time you add
[34:02] an asset,
[34:04] you are implicitly exposing the entire
[34:07] existing book to that same asset. Um,
[34:11] and that's true for, you know, any
[34:12] crossc collateral system. Every time a
[34:15] adds a new
[34:17] collateral asset, it's automatically
[34:20] exposed to the entire book. and and
[34:22] we've unfortunately seen the downsides
[34:24] of that um in the in the but but that
[34:28] means it can't work in the
[34:29] permissionless market, right? Cuz I want
[34:31] to
[34:32] >> sorry
[34:32] >> you're referencing like Kelp Dow and
[34:34] like how you know just the RS state ETH
[34:37] expose like potentially the entire ETH
[34:39] book on a and these sorts of things. Oh,
[34:43] unfortunately. Um,
[34:45] >> now now don't get me wrong, I I I don't
[34:48] think that was a a bad onboarding choice
[34:50] or curation choice or anything of that.
[34:52] I'm I'm just saying that the second you
[34:53] onboard these assets, you are implicitly
[34:55] exposing your entire credit facility to
[34:58] them and and that hurts your depositors.
[35:00] >> Yeah. Um but now let's say someone wants
[35:03] to you know come launch a new token and
[35:07] they of course can't automatically be
[35:09] part of that cross collateral margin. So
[35:13] our permission so so the permission set
[35:16] the first entry point is the lending
[35:17] market on the permissionless set the
[35:20] first entry point is actually still the
[35:22] AMM
[35:23] >> because
[35:24] >> Mhm.
[35:25] >> if it's a new token you have a few
[35:27] problems. Problem number one it doesn't
[35:28] have an oracle. So I can't just pull,
[35:31] you know, something from chain link or
[35:32] or redstone or or even just coin gecko,
[35:36] right? And sign it and post it on chain.
[35:38] So So I don't have that to work with.
[35:41] Thing number two is I don't know things
[35:45] like liquidatable depth or
[35:48] what kind of trade facility or I should
[35:51] offer or or how I should quote this
[35:53] asset even. Um so for all of the but you
[35:57] can solve each one of those pain points
[35:59] individually through the AMM itself.
[36:02] >> Yeah.
[36:03] >> So our our permissionless markets start
[36:05] with you launch your normal AMM which is
[36:08] two pairs right that's just your asset
[36:10] and ETH or your asset and USDC or your
[36:13] FSET and whatever else.
[36:17] this as that starts trading it starts
[36:21] building up your oracle data which is
[36:23] your TWWAP your time weighted average
[36:26] price
[36:27] >> and then it also starts building up
[36:29] something that I always found lacking in
[36:32] this space and it's something I actually
[36:33] included in the original um V33 designs
[36:38] all of those all of those V33 protocols
[36:41] actually all have this but I haven't
[36:43] seen any of them use them yet um and
[36:45] it's something I call Tiwir, which is
[36:47] time weighted average reserves. Because
[36:51] if if something is priced at $3,
[36:55] but I can only sell
[36:58] >> $1 of it because there's only that much
[37:01] liquidity, then its price being $3 isn't
[37:04] actually its price. Its actual price is
[37:06] how much can I sell this for.
[37:09] >> So more important to me in the DeFi
[37:12] space was time, weighted, average
[37:14] reserve. Now all AMMs have a have a A
[37:17] and a B reserve. So that's the number I
[37:19] actually want to want because that
[37:20] number means that at any snapshot in
[37:22] time I can ask the AMM, hey, how much
[37:26] can I liquidate this position for? Now
[37:28] normally you'd assume, hey, I can just,
[37:30] you know, ask it in real time. Why do I
[37:32] need to keep this historic metric? But
[37:34] that's unfortunately the world we live
[37:36] in with flash loans and LP manipulation
[37:38] means that you can never ask a question
[37:40] in real time. You always have to have
[37:42] historical snapshot of a question. And
[37:44] even if you do ask in real time, I need
[37:46] to be able to compare to some historical
[37:48] point that I can see is this a good
[37:51] reading, is this a bad reading, is
[37:53] someone manipulating. But the question
[37:56] you need to answer is how much can I
[37:58] sell? And the reason if you work back
[38:00] from that question,
[38:03] the the implicit question to that one is
[38:05] how much can I liquidate? So we actually
[38:07] end up using the the time weighted
[38:10] average reserve output to see what kind
[38:14] of LTV I can offer the user cuz now the
[38:18] same AMM pair let's say it's it's X and
[38:21] USDT.
[38:23] Now that same pair facilitates lending.
[38:25] So the user can provide their X as
[38:28] collateral and borrow their USDT and
[38:30] their LTV is based on their exposition
[38:32] relative to the pool. So it's not a
[38:34] fixed value. It's not you have a 50%.
[38:37] It's if you're if you're a very small
[38:39] bit of the pool, you get a very high LTV
[38:41] because your impact is [clears throat]
[38:42] low. If you're a big part, you get a low
[38:44] one. And inversely,
[38:46] >> um the next thing you need is interest
[38:48] rate models because you don't have that.
[38:50] So the other thing that these AM pools
[38:53] track is the the the moving averages and
[38:57] the volatility. Okay,
[38:58] >> the moving averages and the volatility
[39:01] also influence the the curve at which we
[39:04] quote the price. So assets that are are
[39:08] completely flat in terms of volatility
[39:11] are priced on the X3Y curve which means
[39:14] it's basically a stable coin.
[39:16] um the more higher that volatility is,
[39:18] the more it veers towards the
[39:20] traditional unis swap um XY and then
[39:23] anything in between it allows for and
[39:26] and this curve in itself I also need it
[39:28] because it facilitates forex trades
[39:30] because stable swaps or XY don't really
[39:33] work for forex trades because it's low
[39:36] volatility but it's not no volatility.
[39:38] So that also sits on this curve. So this
[39:40] curve the the pricing between the
[39:43] reserves is also influenced by the
[39:45] volatility and the moving average. The
[39:48] interest rate is also because in in the
[39:51] lending world you really have two
[39:52] interest rate models. You have volatile,
[39:55] you have three. You have volatile, you
[39:57] have major and then you have stable. Um
[40:01] and that's again answered by volatility
[40:03] and your moving day average. Um so now I
[40:06] can offer lending and I can already
[40:07] offer trading. I have all the data
[40:09] points I need to be able to set up these
[40:11] positions. And then the last thing you
[40:12] can do from that is you use the work
[40:15] from from GMX and their GLP to to allow
[40:19] that same LP to be the counterparty for
[40:21] derivatives as well. So that you can
[40:23] take a long or a short against that
[40:24] position. And because you already have
[40:26] the the lending market built in, now you
[40:28] can do leveraged positions as well. Um
[40:32] so so when when it comes to pure to pure
[40:37] >> permissionless
[40:38] >> single asset pair permissionless so
[40:40] anyone can launch this on their own you
[40:42] know they don't need to interact with us
[40:43] at any given point in time then your
[40:46] your starting base is still the AM and I
[40:48] don't think that's ever going to change
[40:49] because that's that's all of your data.
[40:51] Yeah, I mean this is fascinating stuff
[40:53] like h how you essentially you're given
[40:57] you know a single you know primitive and
[41:00] and you know single is maybe a little
[41:02] bit too too far you know you've got a
[41:04] couple of these different interest rate
[41:06] models you've got a couple of different
[41:08] AMM models right but from those base
[41:11] equations you're able to build this
[41:13] entire suite of functionality from the
[41:15] AMM you're able to build the lending
[41:17] market you're able to build the LP
[41:19] market and the per market all from this
[41:22] single AMM and you're able to do it in
[41:25] such a permissionless way.
[41:27] >> Only qualification I I'll make there,
[41:28] you know, is is it it's not a pure per.
[41:31] It's closer to a pre-market per cuz the
[41:33] pure per funding is obviously influenced
[41:36] between your external oracle price and
[41:38] your mark price. Here you don't have it.
[41:40] So your funding is actually closer to
[41:41] open interest. You know how much of how
[41:44] much are long versus short and then long
[41:45] space short. So it functions like these
[41:48] pre-market IPO per that's that's one
[41:50] small qualification I'll need to make
[41:52] but but other than that it it functions
[41:54] you know
[41:55] >> and I mean that's also been the
[41:57] benchmark for you know these low
[42:00] liquidity early stage perpetualist
[42:03] markets like that is the same way that
[42:05] all these other markets tend to work
[42:06] it's only just after you know they do go
[42:08] IPO they have some sort of liquid market
[42:11] price that's external to the to the book
[42:13] you know then you bring in that oracle
[42:15] price as a means of sort of smoothing
[42:17] out what would otherwise be a rather,
[42:20] you know, uh, uh, funky, you know,
[42:22] Oracle price because it's internal. Um,
[42:26] yeah, Andre, that I mean, that's
[42:27] fascinating stuff. I I I really enjoyed
[42:29] just kind of walking through these
[42:30] things, uh, with you and how you were
[42:32] able to illustrate the difference in
[42:34] building the per the their the
[42:36] permissioned stack versus the
[42:38] permissionless stack. So, makes a ton of
[42:40] sense. Um, I want to be conscious of
[42:42] your time, but I also want to get into
[42:43] the stable coin side of this. Um, you
[42:46] know, we talked a little bit around
[42:48] stable swaps and these sorts of things
[42:49] for low volatility pairs. Um, but maybe
[42:52] you could just talk about the flying
[42:54] tulip USD, you know, why it's such an
[42:56] important part of the overall system.
[42:59] Um, and and you know, generally, you
[43:01] know, how you foresee this growing as a
[43:04] core component to the book.
[43:07] Um I I I I
[43:10] think everyone will agree with the
[43:12] statement that we have seen stable coins
[43:14] are the primary settlement layer and
[43:17] liquidity of almost every single big
[43:19] system we have. Um
[43:22] the
[43:24] the original premise
[43:27] as I said came from Athenos USD. It was
[43:29] looking for a how can I
[43:32] >> do this leveraged delta neutral play
[43:35] onchain with LSTs because I also wanted
[43:38] to broaden it from just if you know I
[43:42] want to I I we obviously do SD E on
[43:45] Ethereum and SDSS on Sonic but I want to
[43:48] do Lista BNB BNB on BSC you know I want
[43:52] to do um Hydrax AX AX on Avalanche.
[43:57] Each one obviously has its own and and
[44:01] very often
[44:03] even even even if you do these things in
[44:05] a centralized fashion very often you
[44:07] can't because that staking asset doesn't
[44:09] really count as as collateral on most of
[44:12] these exchanges margin accounts. So
[44:16] there there isn't really a way to do
[44:19] that proper hedge. So that was from the
[44:22] outset kind of where we wanted to start
[44:24] with the stable coin is how can we do
[44:26] this leveraged deltaneutral
[44:30] tokenization of the staking yield. Um
[44:35] and and and we couldn't that's
[44:37] ultimately what it came down to
[44:40] we we needed something that you could
[44:42] properly hedge the position. So LTV was
[44:44] out right from the bat and that started
[44:46] influencing you know sort of we first
[44:49] looked at
[44:51] LTV but with standard netting so that
[44:55] within the config you could say this
[44:56] asset is netted against that asset. So
[44:58] if they are which which it kind of looks
[45:01] similar to to to aves emode um but
[45:04] you're still not going to hit 100%.
[45:06] You're going to hit 99 or something
[45:07] similar and you need to be able to hit
[45:08] 100% to properly hedge your position. Um
[45:11] so we built the equity market
[45:14] >> which is one of the reasons why we use
[45:15] the equity margin account. And so our
[45:17] margin accounts always allow that that
[45:20] play.
[45:21] >> Then the the other rationale of the
[45:24] stable coin was as a mechanism for
[45:26] scaling. So it's normally pretty easy to
[45:31] get any given blockchain's native asset
[45:33] in a large amount because there's a lot
[45:34] of liquidity for the native asset. So
[45:36] it's not hard to get a lot of people
[45:38] wanting to deposit because there's also
[45:40] not a lot of yield opportunities for
[45:41] native assets. So it's generally fairly
[45:45] easy to attract especially when you
[45:47] start talking to some of these digital
[45:48] asset treasuries and foundations and
[45:50] things. You know they have a lot to
[45:51] deploy.
[45:52] >> So we can get that easily enough. Now
[45:55] the other thing you need is in to your
[45:58] lending market is stable coin liquidity.
[46:01] >> Oh so maybe one thing one one this will
[46:04] make a lot more sense. I should have
[46:05] actually started with that. So with
[46:07] something like Athena's USDE, you know,
[46:10] they're they're what they are tokenizing
[46:13] is staked ETH as margin collateral and
[46:16] that's earning you 2.4%.
[46:18] >> And then they are taking out the the
[46:22] perpetual so the derivative short and
[46:25] then they collect that funding rate
[46:26] which is for argument sake four to 5%.
[46:28] It it's currently I don't think it's
[46:30] currently
[46:32] >> oh it is probably still positive. um and
[46:35] and then minus fees and settlement and
[46:37] all of those things. So you end up with
[46:38] a delta around like four to six%.
[46:41] >> Um our lending market is not a per
[46:44] market. It the pers are getting
[46:45] activated later on and then we will
[46:47] still do that standard trade but for now
[46:51] how we do it is we we use the USDC and
[46:54] the USDT that is deposited into flying
[46:57] tulip USD and that becomes collateral.
[46:59] So that becomes what we borrow the ETH
[47:02] against. And then we swap the ETH to
[47:05] staked ETH. And then the staked ETH
[47:07] becomes collateral as well. So the
[47:08] staked E and the E are still hedged, but
[47:10] it's grossly overcolateralized due to
[47:12] the USDT and the USDC. And that allows
[47:14] us to to leverage that loop as much as
[47:17] you know there is available deposits.
[47:20] But that means we're not we're earning
[47:21] the 2.4% 24% from the the the state E
[47:26] and that can safely be looped up to
[47:28] about eight times with this design. So
[47:31] we don't we're currently at about 1.5
[47:33] because we don't want to push the system
[47:35] too hard too quick and it also depends
[47:37] on available liquidity but you can um so
[47:40] that already will give you so 2.4 but
[47:44] you're still minus about 2.1ish for
[47:47] every E that you borrow. So you net
[47:50] about.3
[47:52] which that then at a eight times loop
[47:54] you know you end up it it's not 20 30%
[47:57] but it's still decent numbers and then
[48:00] you know the the 3.2 to 4% that you're
[48:02] earning on the stable coins and that
[48:04] gives you of your net of around like 11
[48:06] to 12%. Um so that's how that delta
[48:10] neutral loop looks and that's actually
[48:12] different than you know the standard
[48:14] derivativebased one. Um,
[48:18] so the the flying tulip USD is almost a
[48:21] little bit of a Trojan horse in terms of
[48:22] liquidity as well because people deposit
[48:25] because they want to get the yield. By
[48:27] depositing, they're offering more stable
[48:29] coin liquidity. Now, our margin account
[48:31] has the two most important things it
[48:32] needs. It has stable coin liquidity and
[48:34] it has the native asset. Almost all
[48:37] trades on any blockchain
[48:39] >> happen in either stablecoin or its
[48:41] native asset. So by having a lot of
[48:44] those two, we can start offering very
[48:46] competitive trade rates in the spot or
[48:48] the margin or the RFQ. Um so we start on
[48:52] boarding those assets. More people do
[48:54] the margin trades which means they
[48:55] borrow out more of the money. Interest
[48:57] rates go up that influences the interest
[48:59] rate on flying tulip USD. So its
[49:02] interest rate goes up. It attracts more
[49:03] deposits and then the kind of flywheel
[49:05] starts kicking in together with that. Um
[49:08] and that's even before PERS are
[49:10] activated. Once per are activated, then
[49:12] you know we'll do the standard carry as
[49:14] well as a secondary trade while it's
[49:16] positive.
[49:18] Um but further you know something like
[49:20] our total return swaps or any of our
[49:23] derivatives is also settled in flying
[49:25] tulip USD and that's because we can do
[49:29] instant settlement with it if we can
[49:30] mint and redeem at any given point to
[49:34] close the trade and then once the
[49:36] underlying is settled you know we can
[49:38] burn again or mint again depending on
[49:40] which way we have to go. So having that
[49:43] sort of mint and redeemability also
[49:45] gives that instantaneous settlement on
[49:47] the derivatives and things like the
[49:48] total return swaps which is important.
[49:51] But then generally speaking, you know,
[49:53] we also just want to offer the flying
[49:54] tulip USD as a as a ARB layer for once
[50:00] for once it is the base pair of more of
[50:04] our assets cuz if we can if we can
[50:08] increase supply or contract supply based
[50:09] on mint and burn at any given point in
[50:11] time, we can always take that ARB as
[50:12] well and provide that profit to the user
[50:14] since we won't have fees on it. And then
[50:17] lastly, your standard CDP model, you
[50:19] know, allowing people to mint against
[50:21] it. But that's just another
[50:23] interest rate source of people paying so
[50:26] that we can just diversify all of the
[50:28] yield opportunities on the flying jud.
[50:30] Um, but as you can see, you know, it's a
[50:32] touch point everywhere. It's it's a
[50:34] touch point for lending. It's a touch
[50:35] point for trading. It's a touch point
[50:36] for derivative. It's a touch point for
[50:38] all of your trade settlements. So
[50:41] building building that as an attractive
[50:44] offering is is your liquidity layer for
[50:49] your entire system, you know, and and
[50:50] and that's something that's something
[50:53] you see with with [snorts] um all all of
[50:56] these per markets, right? Like like they
[50:57] always have these big whether it's HLP
[50:59] or LLP or or or or any of these other
[51:02] derivatives. Um they always have this
[51:05] one big stable coin vault and
[51:07] >> you can do so much more with that. you
[51:09] know, there's so many more opportunities
[51:11] that you can place against that and that
[51:12] also hedges you against, you know,
[51:15] potentially when you've taken too many
[51:17] bad trades or there's a bad liquidation
[51:19] or a bad oracle feed or something like
[51:21] that.
[51:21] >> So, so
[51:24] it's it's
[51:26] I mean I'm I'm I'm hesitant to use
[51:28] statements like this, but you know, it
[51:29] ends up being sort of the lifeblood of
[51:31] the entire system because you need it
[51:33] running through all of these parts.
[51:35] >> Yeah. And it it's also the, you know,
[51:38] the jet fuel, the initial gasoline to
[51:40] get the thing off the ground initially
[51:43] because you walked through
[51:45] mathematically how it it is possible to
[51:48] develop these components and stack them
[51:51] again permission stack, permissionless
[51:54] stack. It is possible to create the the
[51:56] functionality from these core
[51:59] components. But of course, if there's no
[52:01] liquidity running through these systems,
[52:02] then what's the good of the system? And
[52:05] and so you walk through how important
[52:07] the liquidity in the system is to the
[52:09] system as a whole and how the stable
[52:11] coin helps to stimulate not only the
[52:13] initial liquidity but it helps to
[52:14] perpetuate the liquidity as well as the
[52:17] system continues to grow. So it it is
[52:20] you know obviously crucial to the system
[52:22] as a whole. Um and it's also I correct
[52:26] me if I'm wrong here but it also seems
[52:27] to be the the value acrruel the
[52:30] destination for a lot of the things a
[52:34] lot of the yield sources these things
[52:36] tend to go towards so because it's a
[52:38] touch point for all these things it also
[52:40] tends to be like sort of this rewards or
[52:43] yield accumulation layer where a lot of
[52:46] that value tends to occur
[52:48] >> 100%. I mean, if if there's if there's
[52:50] settlement fees in the derivatives, it
[52:52] goes there. If there's liquidation fees,
[52:54] it goes there. If there's trade fees, it
[52:56] goes there. If there's lending interest,
[52:58] it goes there. Um, so it and and again,
[53:04] it's kind of like I called it at the
[53:05] start, it's kind of the liquidity Trojan
[53:07] horse for the entire system because it
[53:08] ends up having all of these different
[53:10] touch points. Uh, and and I think we've
[53:12] seen that everywhere, right? like like
[53:15] the lending markets that survives are
[53:16] the ones that attract a lot of stable
[53:18] coin liquidity. The trade venues that
[53:20] survives are that have a healthy stable
[53:22] coin order book. The biggest derivative
[53:25] platforms have the biggest um stable
[53:28] coin LPS. So it's it's directly
[53:31] correlated to how much depth can I
[53:33] offer, how much volume can I offer, how
[53:35] much how many options can I offer to my
[53:38] user. Um, and at the same time, you
[53:41] know, I think also having it have all of
[53:44] these different touch point also
[53:46] massively diversifies its risk because
[53:48] now you don't just have the single, you
[53:50] know, my my only counterparty isn't just
[53:54] per trades, right? Because I know even
[53:57] if something goes wrong there, there
[53:58] there's a certain amount of just USDC
[54:00] USDT sitting in lending that's, you
[54:02] know, has a much safer risk profile. Um,
[54:08] stable coins are so important, man. I
[54:10] mean, I' I'd argue that's probably one
[54:11] of the best innovations of crypto as a
[54:14] whole.
[54:17] >> Yeah. Um, I mean, there's this is the
[54:20] last question I got for you and it's a
[54:21] wild card. The We've got the chat here
[54:23] because we are live and so people are
[54:25] they're they're loving your appearance
[54:26] and so we've got this this uh this
[54:28] question here in the chat that I'm going
[54:30] to ask you. Um, and you're right. I
[54:32] mean, stable coins are extremely
[54:33] important. We've seen that, you know, as
[54:35] a result of their growth uh now with,
[54:37] you know, Robin Hood chain and these
[54:38] sorts of things. People are saying, "Oh,
[54:40] you know what? Tkenized equities are an
[54:42] even bigger opportunity than stable
[54:44] coins." Um, so we'll, you know, we'll
[54:46] we'll see how that plays out. Similar
[54:48] question here. And I, this is a wild
[54:52] card question. I just I but I want to I
[54:53] want to, you know, give you a give you a
[54:55] chance to sort of address this. Travel
[54:57] Wings in the chat here says, "Will
[54:59] institution
[55:00] institutional capital institutions
[55:03] seriously look at flying tulip? I think
[55:05] retail is done with Andre." Look, I I
[55:09] just I want to give you a chance to just
[55:10] address, you know, the the perception
[55:13] that people may have of sort of like
[55:15] your journey because look, I understand
[55:18] the the depth and breadth that you've
[55:20] had in this space and and obviously, you
[55:23] know, this is an a feat of um incredible
[55:26] development work that you've done
[55:28] building this system and walking walking
[55:29] through it. I really really do
[55:30] appreciate you walking through it here
[55:32] today. And just to address you know the
[55:35] what some people might be thinking out
[55:37] there. So given this given this
[55:39] sentiment like what how how do you
[55:41] respond to you know this kind of this
[55:44] question right around retail sentiment
[55:47] and institutional sentiment when you
[55:50] know the they're looking at something
[55:52] like flying tulip.
[55:54] >> The only thing that matters is does it
[55:56] offer better riskadjusted yield? Does it
[55:59] offer more features than I get somewhere
[56:01] else or is it cheaper? Capital doesn't
[56:04] care.
[56:06] >> So, I don't think there's much to
[56:07] address there. I'd say the only thing I
[56:09] would address there is that the the the
[56:12] little circle jerk of CT narrative is
[56:14] very very different than what's actually
[56:16] happening out there in the real world.
[56:18] Um, interest is big. There's lots of
[56:20] conversations, but what it comes down to
[56:23] is is it cheaper? Is it safer? Does it
[56:27] reward better? And that's all that
[56:29] matters.
[56:31] >> Travel Wings, I hope you got the answer
[56:32] to your question there. Capital doesn't
[56:34] care. Uh Andre, man, really really
[56:36] appreciate you taking the time today. I
[56:38] know we went a little bit over time. I
[56:39] really do appreciate um you know, just
[56:41] kind of very methodically walking
[56:43] through some of the questions here and
[56:44] explaining the way that you've you've
[56:46] built this system, you know, the lessons
[56:48] that you've learned from previous
[56:49] projects and how you've implemented
[56:51] this. And uh very excited for the growth
[56:53] story of Flying Tulip um to see how this
[56:55] plays out over time. And uh man, I'd
[56:58] love to have you back on in a in a
[56:59] couple of months again and uh get a get
[57:01] another, you know, temperature check on
[57:03] how things are going.
[57:04] >> Yeah, always happy to and thanks for
[57:06] having me. Always like talking to me
[57:07] about this stuff.
[57:09] >> Absolutely. Appreciate learning about
[57:10] it. Uh we'll see you again soon. Thanks,
[57:13] Andre.
[57:13] >> Thanks, boss.
