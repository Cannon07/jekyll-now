---
title: What Is Ethereum?
published: true
layout: post
---

In my last essay, I alluded to the potential of blockchain as a powerful enabler for drug discovery and biology in general.
I've been exploring this idea depth recently and as a result, have been too busy to write an in-depth essay introduction 
to the space. However, I have been exploring important blockchain concepts on Twitter via tweetstorm. The following
(lightly edited) tweetstorm explains the fundamentals of Ethereum, the most powerful (and arguably most popular) developer
platform for blockchain applications. I explain what Ethereum is, why it's exciting, and even touch on how I suspect the
first artificial general intelligences (AGIs) might emerge on systems like Ethereum.

1/ Despite all discussion of bitcoin valuations, most developer excitement in crypto is on Ethereum. But what is Ethereum?

2/ In the Ethereum foundation's words: "Ethereum intends to provide a blockchain with a built-in fully fledged Turing-complete programming language"

3/ Ethereum's whitepaper starts with a recap of Bitcoin. In this telling, bitcoin can be viewed as a "state transaction system"

4/ State is a listing of who owns which bitcoins. Transactions change ownership of bitcoin. Mining is a transaction, and so is fund transfer.

5/ Bitcoin is quite good at being a money store, but is not very extensible; even slight modifications require bootstrapping new chains.

6/ Imagine now that bitcoin could be "scripted." For example, maybe want "multisig" where if 2 of 3 owners authorize transaction, it works.

7/ Or fancifully, want transactions that only pass muster on a full moon (werewolf transactions...). Hard to make bitcoin do this.

8/ Ethereum attempts to improve on bitcoin by enabling arbitrary transactions. Does so with "Turing complete" scripting language.

9/ That is, the decision of whether to approve a transaction can be made by arbitrary programs. So multisig and "werewolf" are now easy!

10/ As with bitcoin, Ethereum is modeled as consisting of "states" and "state transactions. States are "accounts."

11/ Accounts have "ether" (analogous to bitcoin). Innovation is they can now have "contract code" as well.

12/ That is, accounts on Ethereum can be controlled by arbitrary programs ("contracts").

13/ Transactions transfer ether between accounts. Transactions also have "gas-limits" and "gasprice" which make large transactions expensive.

14/ This "gas" is necessary since transactions now execute arbitrary computer programs! (So we need to prevent infinite loops...).

15/ But where is this transaction executed? On a miner's computer! Miners are paid in ether for executing transaction desired. (Recall miners secure blockchain transactions for both Bitcoin/Ethereum).

16/ This code is written in Ethereum Virtual Machine code, a bytecode like java virtual machine bytecode or python bytecode.

17/ Programming in bytecode isn't easy, so people use higher level language that compiles to EVM code (like Java compiles to jvm bytecode)

18/ The most popular of these languages is called [solidity](https://github.com/ethereum/solidity).

19/ With this extra structure in place, mining ethereum, like mining bitcoin, is the act of clearing transactions.

20/ Underneath the hood, a little algorithmic trickiness needed. Juggling program state uses some exotic structures like "Patricia Trees."

21/ "Alt-currencies" are now simply contracts running on ethereum with different rules on how money can be transferred.

22/ From here, it's easy to get creative. The ethereum network is basically a giant computer, so can do many things.

23/ Can have "decentralized storage" where contract dictates rewards to those who can produce random data chunk on demand.

24/ Can have "decentralized cloud" where contract dictates rewards to those who can prove they did random parts of calculation right

25/ It's worth noting that development challenges here can be *formidable*. The ethereum world computer is pretty embryonic.

26/ And as any software developer knows, the devil is in the details. Beautiful ideas which don't actually run aren't much use.

27/ My two cents is that it will be years before Ethereum really matures into a stable platform for distributed applications ("dApps").

28/ I don't even want to imagine getting, say, a [DeepChem](https://deepchem.io) modeling running on Ethereum...

29/ But, I do suspect that it will be possible. Let's end with a few words on why this is exciting.

30/ Recall that accounts can be programs themselves. What if the accounts are themselves AI programs?

31/ Ethereum provides a world for AI to "live", with ether as "money" which can be earned and spent.

32/ Perhaps like free-roaming bacteria, AI will reinforcement learn to earn more ether trawling the network.

33/ Evolutionary processes could kill inefficient AI, with only fittest surviving. Ether trades for "real" money so this isn't a game world.

34/ A rich AI on the network could learn to influence world events to maximize its fitness function.

35/ And it isn't entirely inconceivable that an artificial general intelligence (AGI) could be born on Ethereum one day.

36/ Readily armed with the power to influence world events and shift capital....

37/ On that note, I hope you'll agree that it's worth paying attention to Ethereum!

38/ Practically speaking, as a developer, it's actually pretty painful to develop on Ethereum. Not easy to execute/debug solidity locally.

39/ I like Python, so I've been making good use of [Populus](https://github.com/pipermerriam/populus), a tool to deploy/manage contracts.

40/ Start developing on test networks. Can run a "mini" ethereum instance locally on a single machine!

41/ Scale outwards to test networks like "ropsten". Finally move up to the full ethereum network.

42/ Note that you'll need to spend "real" money to do anything on full network. Probably easiest to buy ether via [coinbase](https://www.coinbase.com/).

43/ You can get "address" of this money and use it as reserves to fuel your programs.

44/ Have fun because development is a bit of a ride!

45/ Fin
