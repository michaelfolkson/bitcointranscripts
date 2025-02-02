---
title: Day 2 Group Summaries
TranscriptBy: Bryan Bishop
---

Day 2 group summaries

<https://twitter.com/kanzure/status/785151245883412480>

Our epic journey in Milan is coming to an end. Let's get seated. Each group is going to have a maximum of 3 minutes to report back. First let's have collaboration between bitcoin community and academia.

# Collaboration between bitcoin community and academia

In the first half the workshop, 6 universities gave introductions of their activities and relationship to engineering and companies. We share the fact that most universities have joint research work with companies. Then we recognize the pitfall, that is, business side usually focus on short-term problems, but academia tends to think about big picture.  Then some examples of collaborations were introduced. Some private companies sponsor academic conference and some university researchers provides information of security valuation. We also recognized that it is fundamental issue to give good incentive to academic researchers.

One good idea was proposed to enhance the communication. Bitcoin developer members make BIR: Bitcoin Improvement Request and BRR: Bitcoin Research Request. It is helpful to define research topic in academia side. We also discussed about communication channels additional to current mailing list and annual Scaling Bitcoin workshop. It is proposed to make new open chat channel, and Github to enhance communication between two communities. This idea was supported by both academic researchers and developers.


# Wallet implementation discussion

One of the implementation issues is that we had a lot of topics like key management, hardware wallet implementation, common protocol standards ,definition of a singing protocol. We spoke about SPV, validation, we spoke about high-level libraries in addition to wallets but also joinmarket, tumblebit, multisig support. We discussed coin selection in terms of privacy and efficiency and different strategies like expiration. We also discussed fee estimation and fee handling. Problems with "SPV" wallets needing access to the mempool. Incentives to lie about fees if we decide to use fee information into a coinbase as a soft-fork. We discussed making things more visible to users in the UI, like Uber's surge pricing. And using multiple providers as a solution to "SPV" wallets, similar to having multiple exchange prices. Replace-by-fee. Open-source software in terms of wallets. In terms of key management we discussed a lot of how to solve that, in terms of verification and reminders to users to backup their seed and wallets and so on. And maybe using external key recovery services with multisig. Tattoos. Private messaging stuff. We discussed accessibility... I don't think any wallet provides accessibility to blind people, I think. We discussed scripting support, lightning support, interoperability across wallets so that you can reuse your seed across wallet. Sweeping support. BIP70 and payment protocol extensions for either shopping purposes or other purposes. And also UI for wallets.

# Breaking the chain

<http://diyhpl.us/wiki/transcripts/scalingbitcoin/milan/breaking-the-chain/>

Our section was sybil attacked-- there were two distinct topics under this heading. On the topic of directed cyclic graphs, DV talked about jute for ordering blocks in a cohort. I think we all agree that in order to solve the 51% selfish mining problem we need inclusive policies, to include all blocks in order to solve selfish mining. One point of contention is how to allocate transaction fees. In jute, they advocate for using a deep mempool which solves problems like fee sniping and taking over a large transaction fee and grinding in a low-subsidy environment. Lastly, one point of future work that we have to deal with is that-- in jute, it revolves around all blocks having the same difficulty. We still have to deal with the problem of merging two users with different histories. You need to figure out merge rules.

The other thing we talked about was essentially going a further into my talk about how to implement this, with treechains too, it's basically linking tree chains and linking them together. It's not breaking the chain, it's combining them. What would mining look like there? How would you pay transaction fees when not everyone has the same data? What strategy would you use to reduce fees on a p2p network? What if we don't want to give miners 5 gigs of transaction history to a miner? How would transactions be structured, like a transaction validated in part rather than in whole, in particular with splitting transaction inputs and outputs where inputs would commit to merkle sum trees to things to add to inputs, like one input actually sending funds to an output that isn't yet complete without other inputs. And finally we touched a little bit about just kind of implementation issues, what it would take to make this real. Thank you.

# Block propagation

I think we forgot to allocate someone to take notes. We spent a bunch of time comparing xthin and compact blocks. There's similarities between the two. We spent some time talking about mempool sync and how to make these protocols more efficient because they all require mempool syncing between nodes to reduce bandwidth and hoping latency. We talked about firewalls and how the internet is a terrible link. We talked a bit about fibre and ways to work around that problem.

# Getting into bitcoin protocol development

We had a great discussion. There's a very wide diversity of different experiences. We had people brand new and people who have been contributing to Core for many years and people who had implemented alternative implementations. We had application developers and also an ethereum developer. Bitcoin development is hard to get into. There's a high barrier to entry. You seem to have to know lots. So how can we lower that barrier and get people to contribute in some way? Things we came up... it's difficult to know what the process is for finding information. There's IRC. Stackexchange. Mailing lists. It would be helpful if there was a pointer for new people to know where to look. It would be great if more experienced developers would-- if there was a place for new developers to join and ask questions to more experienced people. I did a hacker residency last month. MIT is starting a bootcamp at some point. We talked about mentors. It's great to know someone who is a Bitcoin Core developer who can ask questions. We talked about how it would be great if there was a developer advocate or technical writer funded in the community somehow. There's documentation out there, but it's in lots of different places. It would be good if there was someone looking at that. There's a lot of low hanging fruit. It's not impossible to get into bitcoin development. It's something that many people can do. People who are new to bitcoin don't necessarily know this. So there should be some way to advertise this and an easy way to get into bitcoin development. And finally someone said, it was good that there is multiple implementations because not everyone knows C++, so it's great that there's bitcoinj and btcd because some people prefer a higher-level programming language. It could be good to have a tract for people who want to mentor others and new comers that want to start with lowhanging fruit.
