---
title: Why Blockchain Could (One Day) Topple Google
published: true
layout: post
---

Blockchain is the one computer science technology that big web companies like Google and Facebook are really behind the curve on. The classic business book The Innovator's Dilemma [1] explains that it's hard for a company to invest in a product that undermines its core business competencies. Blockchain, with its promise of decentralized data ownership, holds the potential to undermine Google’s core strategy of amassing mountains of user data to serve ads. If the same services can be offered via a blockchain backend why do users need a centralized repository like Google? For this reason, I suspect that blockchain is the one present computer science discipline with the potential to topple the Google empire itself.

To understand why, we need to dig a little deeper into blockchain. At its heart, a blockchain holds a simple distributed ledger. Think of it like a database spread across many users. It's a little silly to think a slower and buggier version of MySQL could topple the Google empire right? Wrong.

It’s more fruitful way to understand blockchain as an effective algorithm for multiple parties to agree on a set of shared facts in the presence of mutual distrust. In this scenario, each participant cannot trust that other participants will play by the rules. In fact, each participant is expect to maximize their personal interest over the shared good. In computer science, this is known as the Byzantine Generals Problem [2], where a group of generals want to coordinate an attack while minimizing casualties for their individual battalions. The danger in this scenario is that if not enough generals commit to an attack, there could be a rout for the unlucky attackers. The shared fact in this scenario is whether an attack is going to happen or not. 

The Bitcoin protocol [3] is a profound accomplishment in computer science because it provides essentially the first trustless solution to the Byzantine generals problem (that is, Bitcoin is Byzantine fault tolerant). For Bitcoin, the shared facts consist of the ledger which details who owns how many bitcoins and what transactions have been made upon them. The Bitcoin protocol has survived many practical upheavals and is perhaps the world’s largest Byzantine fault tolerant system. 

Despite its profound accomplishment, Bitcoin has limited scope. It’s an excellent cryptocurrency, but little else. Ethereum [4] generalizes Bitcoin’s notion of transaction to include execution of arbitrary smart contracts. In practice, this means that financial transactions can be programmatically controlled via smart contract languages such as solidity [5]. A number of interesting financial instruments such as initial coin offerings (ICOs), novel alternatives to traditional venture financing [6] have been constructed on the Ethereum platform, and it’s likely that a host of further financial innovations will follow.

However, it’s important to emphasize that Ethereum’s conceptual leap reaches far beyond financial novelty. The idea of blockchain as a tool for enabling mutually distrustful parties to execute arbitrary programs has profound implications. Let’s consider a small case study from the blockchain future: Merck, Pfizer, Aztra Zeneca, Glaxo Smith Kline, and Roche wish to coordinate the design of a new drug. Each firm has complementary strengths and pooling their respective talents could achieve a breakthrough molecular design while lowering risk. It’s possible to envision a trustless smart contract that coordinates this arrangement, with ownership in eventual molecules being fairly partitioned between the firms. The Byzantine fault tolerance of the network could enable robustness against corporate malfeasance if one of the firms attempts to cheat. In practice however, the Ethereum network is far from being able to implement contracts of this sophistication, but the potential is there.

You might now be convinced that there’s something to blockchain mania, but perhaps you’re not seeing why the technology is a threat to modern web titans like Google. In order to understand the full potential of blockchain, we need to add additional primitives. The first primitive to add is data storage. Let’s suppose we have a new blockchain, which is able to coordinate its mutually distrustful participants to agree about shared facts like “node X stores data blob Y,” where “node X” is some participant in the blockchain ecosystem and “blob Y” is an arbitrary (and potentially large) piece of data. A decentralized network with such guarantees could provide a service a lot like Dropbox or Amazon’s S3, enabling users to store data on the blockchain directly [7, 8].

The next additional primitive we need to add is heavy duty computing power. While Ethereum is capable of executing arbitrary smart contracts in theory, in practice this ability is currently heavily limited by the gas limit [9] which dictates that only short contracts can be executed successfully. A number of technical proposals are currently circulating [10, 11] which propose solutions to allow arbitrary computations to be executed on the blockchain [12]. Let’s suppose for a thought experiment that these issues have been resolved, and that our blockchain can coordinate its participants to agree on shared facts such as “node X executed program Z on blob Y”.  Here “program Z” could be an arbitrary computation such as the training of a deep learning system or a complex graph algorithm like Google’s PageRank. Things start to get interesting now. Our hypothetical blockchain has the ability to store data and run arbitrary computation. In fact, it’s starting to sound a lot like a modern cloud provider like Amazon Web Services (AWS).

This is interesting, but perhaps not revolutionary. It’s likely that a blockchain AWS will likely be a buggier version of plain AWS. Why bother? Well, let’s imagine that all of us are participants on this blockchain. That is, I’m paying to run “node X” and I’ve stored “blob Y” on the blockchain with my personal data. Let’s assume that “blob Y” is encrypted so that my personal information is safe out there on the blockchain. The exciting part is that there are a host of efforts underway to design “program Z”s which can compute with my encrypted data in a trustless Byzantine generals world! [13, 14]. Currently, we trust that Google or Facebook will act as responsible stewards of our personal information. To their credit, they have mostly stepped up to the challenge. But not perfectly by any means [15].

Imagine now that independent designers could design “program Z”s modularly without access to your personal data. Perhaps one such Z is a new privacy preserving version of Gmail. Perhaps another is a new privacy preserving version of Google Street View (which avoids embarrassing privacy failures [16]). In this version of the world, Google wouldn’t own your emails or the street view photos. Rather, individuals would, and their personal settings would control what information leaks out into the world. If our hypothetical blockchain reaches the scale of Google or Facebook with billions of participants, it could offer a full fledged, privacy preserving alternative to the modern Web economy. Such an entity could offer an existential threat to Google itself. Google’s business model revolves around access to our personal information. If we can get the same services without losing our privacy, why would we need Google?

It’s important to emphasize that I’m not arguing Google lacks the technical sophistication to execute a blockchain project. In fact, I wouldn’t be surprised if Google currently had an internal team working on some blockchain related code today. Google already has significant expertise in federated learning, which takes an important technical step towards distributed, private machine learning [17]. However, I do argue that Google lacks the business willpower to seize the transition that’s coming. A similar sequence of events unfolded within Google during the rise of cloud computing. Google’s Borg [18] was probably the world’s most powerful internal cloud system and served as the backend for Google’s many services. But Google couldn’t turn that into a working cloud product until well after Amazon had seized the lead with its AWS cloud offering. A public cloud would have weakened the profound advantage Google possessed with its private Borg cloud, so stakeholders within the company didn’t commit necessary resources to a cloud product. As a result, GCP (Google’s cloud) became a secondary player in the cloud ecosystem despite strenuous subsequent effort to catch up to frontrunner Amazon. I project that a similar situation will unroll with blockchain. We have not yet seen the first breakthrough blockchain application (barring Bitcoin’s bull run in 2017), but when we do, I think Google will enter the market as a follower.

This is why those of us working on blockchain are excited. It's a chance to overthrow incumbents, a transformation potentially as disruptive as the advent of the internet and mobile all rolled into one. In fact, I suspect many applications we can’t envision today will become feasible. When individuals can trust they control the usage of their private information, they might become more willing to gather their personal information for use in AI powered healthcare, drug discovery, entertainment or education. Consumers could then benefit from secure AI that can help them reach their full potential. This is a world in which a centralized corporation will no longer have the power to forecast our destinies and we seize back control of our futures.

Acknowledgments: Thanks to Aarthi Ramsundar for detailed editorial feedback.

[1] https://en.wikipedia.org/wiki/The_Innovator%27s_Dilemma 

[2] https://en.wikipedia.org/wiki/Byzantine_fault_tolerance#Byzantine_Generals'_Problem

[3] https://bitcoin.org/bitcoin.pdf 

[4] http://rbharath.github.io/what-is-ethereum/ 

[5] https://solidity.readthedocs.io/en/develop/ 

[6] https://www.investopedia.com/terms/i/initial-coin-offering-ico.asp 

[7] You might protest I’m fudging here. It’s very unlikely that the data would be stored “on-chain,” that is directly recorded on a distributed ledger. The entire bitcoin ledger is only a couple hundred gigabytes today for example. What’s more likely is that data will be stored “off-chain” by nodes on the network, but there will be “on-chain” mechanisms for verifying that these nodes are honest and that the stored data hasn’t been corrupted.

[8] https://filecoin.io/filecoin.pdf 

[9] https://bitcoin.stackexchange.com/questions/39132/what-is-gas-limit-in-ethereum 

[10] http://golemproject.net/doc/DraftGolemProjectWhitepaper.pdf 

[11] https://people.cs.uchicago.edu/~teutsch/papers/truebit.pdf 

[12] Again, I’m fudging vocabulary. It’s likely the actual compute will be performed “off-chain” but there will be “on-chain” methods for verifying the validity of the performed computation.

[13] https://openmined.org/ 

[14] https://www.henrycg.com/files/academic/papers/nsdi17prio.pdf 

[15] https://www.recode.net/2017/12/22/16811558/facebook-russia-trolls-how-to-find-propaganda-2016-election-trump-clinton 

[16] http://www.nytimes.com/2013/03/13/technology/google-pays-fine-over-street-view-privacy-breach.html?pagewanted=all 

[17] https://research.googleblog.com/2017/04/federated-learning-collaborative.html 

[18] https://research.google.com/pubs/pub43438.html 
