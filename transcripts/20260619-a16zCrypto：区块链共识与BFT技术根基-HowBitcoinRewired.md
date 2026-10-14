---
访谈时间: 2026-06-19
访谈时间说明: "无法确认实际访谈时间，使用 YouTube 发布时间"
嘉宾名字: "Tim Roughgarden and Ittai Abraham"
嘉宾公司名称: "a16z crypto"
播客名称: "a16z crypto"
播客url地址: "https://www.youtube.com/watch?v=u2jTgXcGimU"
全文提及的关键名词:
  - "Tim Roughgarden and Ittai Abraham"
  - "a16z crypto"
  - "AI"
  - "Bitcoin"
  - "Ethereum"
  - "How Bitcoin Rewired"
  - "Classic Computer Science Problem"
  - "Tim Roughgarden"
  - "Ittai"
  - "What Bitcoin"
  - "Byzantine"
  - "Satoshi"
  - "First"
  - "Head"
  - "Research"
  - "Columbia"
  - "Ittai Abraham"
  - "Decentralized Thoughts"
---

# How Bitcoin Rewired a Classic Computer Science Problem (ft. Tim Roughgarden and Ittai Abraham)

## Transcript

So, this was in 2007. I was at a workshop, and the goal of the workshop is going to see whether Byzantine fault tolerance is practical or [music] not.

But, there was actually two big complaints. One is that maybe nobody needs it, and the other was that the performance was horrible.

>> So, the question wasn't whether consensus protocols are practical. The question was do you really need to be a robust [music] to potentially very unpredictable failures as opposed to just crashing?

>> Satoshi Nakamoto, he kind of realized that. He said the core technical aspect of Bitcoin is solving Byzantine [music] agreement. I would say de facto all the major chains that we know are running some version of Byzantine fault tolerance. [music] They are the proof-of-stake protocols.

>> They were not very efficient. They had blocks every 10 minutes, and so really if you're thinking about serving billions of people or systems that really manage large economies, you want to have kind of a wartime mode and a peacetime mode. So, in peacetime there's no failures. And the thing is that you do want to be able to switch to wartime.

[music] So, if you are under attack, then you do have a way to kind of overcome a massive attempt to corrupt your system.

>> Hi everyone. I'm Tim Roughgarden, head of research at a16z crypto and professor of computer science at Columbia University. And today, we're kicking off a new series called First Principles, the scientific roots of blockchain technology that explores one of the most exciting areas of research at the intersection of theory and practice today. Blockchains and where the ideas that make them possible come from.

At their core are decades of work across computer science, economics, and mathematics, ideas about how distributed systems reach agreement, how trust can emerge without central authority, and how computation can be verified across networks of strangers. So, we'll trace these ideas from their origins to the systems running in production today. And we'll talk with the scientists and the scholars whose breakthroughs made it all possible.

To start, we're going to focus on one of the deepest threads, which is distributed consensus. How many machines can agree on a shared state even in the presence of failures and adversarial behavior.

Concepts like Byzantine agreement and state machine replication, developed decades ago now, sits at the hearts of modern blockchain technology.

So, to begin, I'm joined by a16z crypto research partner, Ittai Abraham. Ittai is one of the world's leading researchers in Byzantine agreement and consensus protocols.

He's a founding member of VMware's blockchain project. He's also the founder of Decentralized Thoughts, one of the field's most respected and long-running technical blogs.

Together, we unpack the work of two pioneers, Barbara Liskov and Leslie Lamport, whom you'll hear directly from in the episodes ahead.

All right, so Ittai, very, very cool. We get to interview um both Leslie Lamport and Barbara Liskov. It's great honor, really, really cool we get to do this.

Um you know, maybe for the audience benefit, we should talk a little bit about how the pioneering work that they did connects to blockchain technology.

You know, so the first blockchain that came out, Bitcoin, 2008, 2009, you know, part of what it is is a consensus protocol.

And so, the question is like, what does that mean? A lot of the work that uh Lamport and Liskov both did, it's way before Bitcoin, right? It's from the '90s, from the '80s, even earlier.

What's the connection? Bitcoin's a consensus protocol, but there's also this classic work consensus protocols.

Was Bitcoin reinventing the wheel, or how should we think about that?

>> Bitcoin was not just a whole disruption in in distributed computing. It also has innovation in economics and cryptography. But here, we're going to focus on the distributed computing part.

It actually took quite a few years for people to realize that this is kind of solving a Byzantine agreement problem. So, Byzantine agreement problem is kind of this very core academic problem that has been studied for 40 years. And that sense, Bitcoin is kind of this huge revolution in the how to solve uh Byzantine agreement. In fact, if you look at early emails from Satoshi Nakamoto, he kind of realized that. So, he said, you know, the core technical aspect of Bitcoin is solving Byzantine agreement.

>> So, Nakamoto apparently knew that this was a well-known problem in distributed computing. So, what's the connection then between the Bitcoin protocol and, you know, the protocols we're going to hear about?

>> Yeah, so so in a sense both the protocols that we're going to hear about from Barbara Liskov and Leslie Lamport are Byzantine agreement protocols or agreement protocols in general. So, Bitcoin solves this in a much different setting, permissionless with a much smaller setup, much more kind of geared towards a cryptocurrency and crypto economics. But if you kind of think about this from the foundational perspective, they're both solving the same agreement problem. So, agreement is kind of this problem where you have multiple different parties and they might have different types of inputs and they need to reach agreement even though a fraction of the participants are are behaving maliciously or in a corrupt manner.

>> So, like in the Bitcoin protocol, who are the parties that have to agree and what is it that they're agreeing on?

>> Right, so you have a miners, right? And the miners are trying to kind of push the the protocol forward by generating new blocks by solving proof of work.

And it might be that not all the miners are trying to do the right thing. Some of them may try to subvert the protocol or they're behaving in a in a corrupt manner. Maybe they're trying to create some sort of double spend attack or some attack that will basically cause different people to see different views on the blockchain.

And what this protocol basically does, Nakamoto consensus it's called, right?

The consensus protocol of Bitcoin is kind of guarantee that even if a fraction of the miners are corrupt, this protocol still gives you a single consistent view of the of the ledger.

And in a sense, that's exactly the thing that has been studied 40 years ago, right? In state machine replication and Byzantine fault tolerance.

>> And so, state machine replication, so how does that compare to agreement?

>> So, in a sense, kind of the core problem is is just reaching an agreement on the content of the log. So, now you have kind of a log that has different commands on them.

>> So, a log would be an abstraction of a blockchain in this case.

>> Yeah, so you could think about every every block in your blockchain as just a set of commands. And then you have kind of a yeah, a chain of commands that would be kind of a log or a chain. It's kind of the same thing. But, really what you want to do is not just record things, but you want to try to see what is the outcome of executing them. So, this is where you have some sort of a smart contract language or or some scripting language like Bitcoin script.

And in this case, you know, maybe you're you want to verify some signatures or run some sort of a contract. So, this is the execution part of it.

And so, the very powerful abstraction, this is an abstraction that that we'll hear about from Leslie Lamport, is what's called the state machine replication. It's that clients are basically thinking as if they are interacting with a single state machine.

So, what is a state machine? It's simply a single system that that you can send it commands, and through that commands it updates its state from one state to the other to the next. And each time you kind of run a command, the state updates to a the next state of of the system.

>> And then I guess in a in a blockchain context, that state would include, for example, everybody's balances in a native cryptocurrency, plus I guess maybe like local storage in smart contracts. That would all be kind of part of this state, right?

>> Exactly. So, for example, in Bitcoin, maybe the state of the system is that I have a token. And maybe if I send a payment to you, then the way the the state would change is that now my token is erased, and there's a new token that forms that's under your public key.

Right? So, now you can use that token.

So, the state is kind of recording what are all the unspent tokens or transactions that are on the chain.

>> So, one thing that I think I find fascinating is, you know, you had for a while two parallel threads of research that at least it seems to me have converged to a large degree over the last 5 years. But, I'm curious about your thoughts.

But, you you have distributed computing uh dates back again at this point, you know, 45 years or more. And we'll hear from, you know, both Doctors Lamport and Liskov about that early work. And then separately, you know, Bitcoin launched kind of blockchain technology and sort of a research community around that thinking about how to build better better blockchain protocols.

And that was in 2009. So that was nearly about 30 years after some of the earliest, you know, pioneering work on the distributed computing side.

And so in addition to being 30 years later, I feel like it was kind of a parallel thread for a while there.

But now it seems to me that those two threads have been coming together over the past maybe five years or so. So I guess do do you sort of share that view?

And if so, like what do you think has been driving that sort of convergence recently?

>> Yeah, absolutely. First of all, I really think that, you know, Bitcoin is this kind of huge revolution. We're probably going to spend a lot of time talking about that.

But but in a way, when it happened, people didn't really understand what it's doing. It actually took quite a few years for the research community and for everybody to understand that this is solving kind of a a very hard academic problem.

Once it was clear that that is the problem that Bitcoin solves, there was this effort to try to connect that to this classical work.

You know, it took quite a few years.

Around 2017 or 16 was when this change. I think the first protocols were Tendermint as an example. These were the protocols that kind of were using the uh classical Byzantine fault tolerant protocols, but applying them on proof of stake. So really I think that this is this transition from proof of work based protocols to proof of stake ones. And the realization that you can kind of mimic the same effect that Bitcoin obtained in proof of work using proof of stake protocols. So I think that was kind of the the first wave of 2016-17.

Maybe the next one to mention is Casper.

This is the the Ethereum finality gadget. Appeared around 2017.

>> That's a great point. I mean, now even the theory is at the point where we understand there's a formal sense in which you kind of can't do the traditional consensus protocols in a proof of work context, And is an interesting interaction between kind of the type of civil resistance, right? So, if if you don't know who people are and you can't do one vote per person cuz you don't know who the people are, so you have to do one vote per some scarce resource. That's what I mean by civil resistance mechanism. And Bitcoin famously uses uses proof of work. In some sense, that's incompatible with the types of techniques that Doctors Lamport and Liskov will be talking about. Whereas, proof of stake civil resistance, well, there's a lot of other reasons you might want to use that as well, you know, maybe you're concerned about environmental reasons or, you know, scalability, what have you. It also actually unlocks those techniques that

Doctors Lamport and Liskov will will tell us about. So, that's a great point.

>> And it was not trivial at the time. So, I remember 2015, people were saying, "Oh, there's this idea of proof of stake, but how do we do it? It seems impossible." You know, there were a lot of people that said that, you know, there's no way to to kind of do to something similar. So, it was a non-trivial advance during those years.

>> Absolutely. So, for example, you know, Ethereum I know was already talking about proof of stake before they even launched their original mainnet in 2015, and then the actual transition to proof of stake wasn't until 2022, right? Seven seven eight years later. So, I agree, it seems like that turned out to be a much more difficult problem than, you know, just the initial idea.

So, you mentioned Tendermint, which may be familiar to listeners from the Cosmos ecosystem, among among other places. You mentioned Casper, which is used in today's Ethereum. So, today's Ethereum has sort of two layers. It has like a longest chain sort of lower layer, and then a finality gadget based on top Casper. And as you say, the techniques in Casper are going to be very related to the techniques that that our guests um tell us about today.

I actually, you know, on a personal note, I think I first um became aware of this interesting interplay. The idea that the Bitcoin protocol on the one hand was sort of solving a well-established academic problem, but then doing so in a way no one had ever thought about. It was See, a survey you wrote, I think, with Dahlia Malkhi that that sort of first pointed that out. So, that was maybe 2017 or something like that. That made a that made a big impression on me at the time.

>> Yeah, so it actually took, I think, quite a few years uh for this kind of prevailing I guess uh community understanding, right? That Byzantine fault tolerance is the core thing that that blockchains are doing.

But that actually wasn't obvious.

There were early protocols that kind of did things that were not consensus protocols or didn't solve Byzantine agreement.

And it took quite a while until kind of things settled I would say. And today or at least you know, even from 2017 to the 2020s, there was kind of an explosion of research in in Byzantine fault tolerance.

And and I would say de facto, all the major chains that we know are running some version of Byzantine fault tolerance.

>> One thing that's been wild I'd say about blockchain technology is it sort of breathed a lot of new life and also frankly a lot of new resources into a lot of areas of computer science that have been around for quite a while, right? So like another example would be say the development of SNARKs, which for many decades was viewed as a purely theoretical construct. It was kind of you know, something magical which you'd never hope to implement. And you know, now we're really seeing very concretely efficient SNARKs come into production.

And you know, while consensus protocols they were always sort of meant to be practical as as I think we'll hear about today, they've been supercharged as well by having, you know, blockchain technology as a sort of extremely high-value application of better consensus protocols.

>> Let me even tell you another story. So this was in 2007. So 2007 I was at a workshop and the goal of the workshop was to kind of see whether Byzantine fault tolerance is practical or not.

This was really a few years after Google and and Yahoo and Microsoft were using kind of the non-Byzantine version of of agreement, right? This is kind of Paxos-type protocols.

>> So the question wasn't whether consensus protocols were practical. The question was did you really need to be robust to potentially very adversarial or very unpredictable failures as opposed to uh just crashing?

Is that right?

>> Right, but there was actually two two big complaints. One is that maybe nobody needs it and the other was that the performance was horrible. So people kind of didn't believe that it's possible to do it any better, right? They they said, "Oh, this is going to be very slow. We now have these very efficient Paxos-like algorithms. Those are practical, right?

Those are used by a lot of these cloud service providers. But, yeah, Byzantine fault tolerance, oh, that's that's not practical. That that's too expensive." So, yeah, I think we're we've seen this arc of a a lot of work in the space kind of really exponentially improved.

>> So, like last 5 years, are there some sort of innovations in consensus but originating from the blockchain community that you have you find particularly notable?

>> So, we are seeing, you know, not just a lot of systems are using Byzantine fault tolerance, but we're also kind of seeing a lot of innovations in this space. A lot of it is focused on getting much higher throughput and much lower latency.

>> Yeah, and so I guess just to make that concrete, so from the user perspective, you want high throughput because you want there to be space for your transactions and even sort of you want it to be cheap to send your transactions. Low latency just means whatever you ask the blockchain to do, like do a transfer whatever, you want it to happen ideally close to instantaneously, right? That would be the latency, right?

>> Yeah, and and maybe, you know, we can go back to to Bitcoin 2009, right? Or even 2017, the early proof of stake protocols. They were not very efficient.

They had blocks every 10 minutes if it's Bitcoin or whatever, you kind of tens of seconds.

And the throughput was actually quite small. And so, really, if you're thinking about serving, you know, billions of people or or systems that really manage large economies, then that wouldn't be enough for some types of use cases. So, you want to have something that can serve many, many users. And not only that, they can give them a real-time experience. So, serving a lot of users, that's going to be, you know, high throughput. And giving people kind of real-time experience, that would be kind of low latency. One type of innovation is these DAG-based protocols. These are protocols that have a two different layers, and they really push the throughput of these systems quite a bit.

We've seen this, for example, in Sui and protocols like Mysten Labs. That's kind of one one family of major improvements.

And and the other one was a focus on trying to reduce latency.

Can you kind of reach Byzantine agreement with very, very few round trips? And you know, we've seen these new protocols that kind of have two different modes. So, a regular mode that maybe has three message delays and a fast path that has just two message delays. And this is the optimal thing that you could expect. Even in a non-Byzantine setting, right? You could just think about this. It's really just that server sends it to all replicas and gets response back and the transaction's committed. So, really you get the smallest latency that you could possibly imagine.

>> Yeah, and I think this is a very cool approach. This is basically just optimizing the common case, right? Which is just usually usually a good idea. And this itself has, you know, precursors in the academic literature that predate blockchain technology. You know, maybe most famously with, you know, Alpine Glow, which is the proposed new version of Solana's consensus protocol, which I think will be rolled out in 2026. That's really kind of a in-production implementation of this idea. Like maybe, you know, 90-some odd percent of the time you can be super fast while losing little if any in the remaining percent from what you what you had before.

>> Yeah, the the way I like to think about this is from a systems design perspective, right? Is that you want to have kind of a a wartime mode and a peacetime mode. So, in peacetime, there's no failures, everything's good, you want to be super fast and super efficient.

>> And that's going to be most of the time, right?

>> That's going to be 99% of the time where you can >> Yeah, and we now we now empirically can be just watching all these blockchains in production, empirically we know that's most of the time.

>> Exactly. I mean, there's kind of cryptoeconomic incentives, right? So, so once you make attacking it not efficient, then people will attack it less and so on. And the thing is that you do want to be able to switch to wartime, right? So, if you are under attack, then you do have a way to kind of overcome, again, a massive attempt to corrupt your system.

Um, so I think these kind of dual mode protocols are fascinating and and I think make a lot of sense in this world.

>> One final thought on the the influence, you know, of the academic literature on consensus protocols to modern blockchain protocols.

I would also say like even just the language people use to talk about blockchain protocols and the guarantees they have, I'd say is, you know, deeply, deeply informed by the foundations that were laid kind of on the on the research side, right? Like, even if it's just meant to be a purely practical blockchain protocol, still there's an expectation that you would have, for example, optimal fault tolerance in partial synchrony, which is a bunch of, you know, academic words. I mean, it all translates to precise mathematical statements, you know, about sort of a mathematical abstraction of the of the practical protocol. But yet, that has almost become sort of table stakes for new generations of blockchain protocols.

And so, to me, just just the whole way people think about what makes a protocol good or sort of state of the art, you know, that is I think very deeply shaped by the last, you know, now almost half century of work in this field.

>> Yeah, I mean, you know, for us this is extremely exciting because we come from kind of a theoretical computer science.

And here we have something that's extremely practical. As you said, the language and the way to think about these to reason about these protocols is actually using theory and mathematical abstraction. And this is a non-trivial idea, right? That you have a real-world system and you're actually using abstract mathematical thinking and, you know, you're using proofs and you're using that language in order to reason about your system. And what's to me even more exciting is that this is not a new idea. This is an idea that, as we're going to see, has been studied for 40 years in in distributed systems. So, there's kind of this very deep and successful connection between relatively theoretical notions and mathematical models and things that are just kind of in, I guess, in in theory and practical systems that are deployed in real world both in kind of, you know, clouds in the 2000s and today in in basically all blockchain protocols.

>> Yeah, right. The famous quote is that the gap between theory and practice is always smaller in theory than in practice. But I I will say I really feel like this gap has been getting narrower thanks to the efforts of sort of lots of smart people both on the research side and on the sort of engineering side. I mean, you know, it's not perfect convergence, but you know, like you say, I mean, really the The being developed right now really is intended to usefully inform the next generation of of in-production blockchain protocols. Which is very exciting to sort of, you know, see that see that synergy between them.

>> Very much. And and for me I think it's because it's a two-way street, right? So it's not that oh, there's somebody sitting in every tower and kind of, you know, writing theorems. It's actually you see what what's happening in practice and you analyze that and then you realize oh, you can So so this two-way connection is extremely important and and was very fruitful. I think for both both sides.

>> And I you know, I I would guess for both, you know, Leslie Lamport and Marly Liszkowski, right? I mean there's you know, anyone can see there's a really major loop between kind of the theoretical innovations and sort of the practical the practical solutions. So I'm sure we'll hear more about that from them as well.
