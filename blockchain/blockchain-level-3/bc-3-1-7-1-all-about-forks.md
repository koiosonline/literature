# BC-3.1.7.1 All about forks!

>💡 A fork is a method to upgrade the network. The goal of forking is to upgrade the software protocol. 

## Reasons for the occurrence of a blockchain fork 

1. **Add new functionality** 

The Blockchain code is upgraded regularly. Since most public blockchains are open source, it is developed by people from around the world. The improvements, issues are created, resolved and new versions are released when the time is suitable.

2. **Fix security issues**

Blockchain (and cryptocurrency on top of it) is a relatively new technology compared to the traditional currency (notes, coins, cheque). Research is still underway to understand it fully. So, versions are bumped, and updates are released to fix the security issues that arise in the way.

3.**Reverse transactions** 

The community can void all the transactions of a specific period if they are breached and malicious.

We've seen many examples of forking so far, and this is great! In physical nations, forking is nearly impossible. This was also the case in software until blockchains emerged. They make it easy to take all the code and state of a system and try a new path. In the Web 2.0 world, **forking is the equivalent of Facebook allowing any competitor to take their entire database and codebase to a competitor.** Don't like how Facebook is operating its newsfeed? Create a fork with all the same code, social connections, and photos.

>💡 The ability to fork significantly reduces lock-in and increases diversity, allowing many more paths to be tried than we would ever see in modern governments, central banks, or Web 2.0 companies.
 

>💡 As in corporate spinoffs, forking is also beneficial when two niche chains can more effectively serve distinct needs than one chain ineffectively doing both sets of needs.

## So why should you improve blockchains?

A quick overview of the (many!) multi-disciplinary challenges ahead: 

* The blockchain scaling debate (many "on chain" and "off chain" solutions, each with its trade-offs. This chapter will discuss what these types of solutions are, and we will give you some examples. 

* Challenges regarding anonymity and how we can protect the privacy of individuals. 

* Governance Dilemma's and how to structure your "decentralized" ecosystem

* Lack of builders and knowledge base. We just started this era, and already we shape (and luckily sometimes reshape) the fundamentals on which we build next generations

* Tribalism – "mine blockchain is better than yours". Luckily we see some outstanding interoperability initiatives connecting the tribes that operate in open environments. 

* Scams & Hacks. Just remember the ICO-booms and Ponzi schemes. The rise of STO's & DAICO's to reduce the scam rate need to be tested on the masses, but the masses burnt their fingers, so they need some time to adjust. 

* Legal Framework – after years, there is still a lot of uncertainty in the air. 

* Other topics: energy consumption & consensus experiments, ownership keys & user-friendliness and educating users, Oracle problems with input uncertainty, and other limitations regarding smart contracts (more about this later on ☺!) 

Looking at the challenges above and being discouraged is like writing off the Internet in 1990 and saying, "this won't work." 

## Anti-fragile 

>💡 Blockchains (like all distributed systems) are not so much resistant to bad actors as they are 'antifragile' – that is, they respond to attacks and grow stronger. But how? 

It can either be done by: 

* Upgrading the ledger (blockchain) and protocol (called "on chain" solutions and is done by "forking") 

* Building techniques that are outside the protocol & blockchain but heavily interact with both of them (called "off chain solutions" and is done by building new techniques that are interoperable with the blockchain & protocol). 

Let's dive into the first one: forking!

## Hard fork 

>💡 A hard fork is often a softening(!) of consensus rules. 



![Source soft fork investopedia](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-1-7-1-all-about-forks-image1.JPG)

[Source soft fork investopedia](https://www.investopedia.com/terms/h/hard-fork.asp) 

**Hard Forks: A hard fork is a permanent divergence** from the previous version of a blockchain. A new set of consensus rules is introduced into the network that is incompatible with the older network. In other words, a hard fork can be thought of as a **software upgrade that is not compatible with previous versions of the software**. All network participants must upgrade to the latest version of the software to continue verifying and validating new blocks of transactions. Under a hard fork, blocks confirmed by nodes that are not yet upgraded to the latest version of the protocol software will be invalid. Nodes running the previous software version will have to follow the new set of consensus rules for their blocks to be valid on the forked network. **In the event of a hard fork, if there is still mining support for the minority chain, two blockchains can continue to exist simultaneously.** As has happened with Ethereum and Ethereum Classic, for example.

## Soft fork

>💡 A soft fork is often a tightening(!) of consensus rules. 

![Source soft fork investopedia](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-1-7-1-all-about-forks-image2.JPG)

[Source soft fork investopedia](https://www.investopedia.com/terms/s/soft-fork.asp) 

**A soft fork is a backward compatible method of upgrading a blockchain**. In other words, a soft fork is a software upgrade that is backward compatible with previous versions of the software. **Soft forks do not require nodes on the network to upgrade to maintain consensus because all blocks on the soft-forked blockchain follow the old set of consensus rules as well as the new ones.** Blocks produced by nodes conforming to the old consensus rules may violate the new set of consensus rules. As a result, it will likely be made stale by the upgrading mining majority. **For a soft fork to work, a majority of miners need to recognize and enforce the new set of consensus rules**. If this majority is reached, the older network will fall into disuse, with the more recent blockchain gaining recognition as the 'true' blockchain. 

An example of a soft fork would be implementing a new consensus rule changing the network block size from 1MB to 500KB. Nodes that have not been upgraded will continue to see incoming transactions as valid. These nodes follow the old consensus rules and the new (500KB is less than 1MB). Mining nodes that have not upgraded to the new consensus rule and attempt to mine new blocks will have them rejected, as they do not conform to the new set of consensus rules (block sizes of 500KB). Thus, the blockchain with 1MB sized blocks is likely to fall into disuse as miners enforce the new consensus rule of 500KB

Another example of a temporary soft fork is when two or more miners find blocks simultaneously. As a result, the blockchain temporarily diverges into two chains, also seen as a soft fork. This ambiguity is resolved when subsequent blocks are added to one, making it the longest chain. In contrast, the other block gets "orphaned" or abandoned by the network. 

If you would like to have a visualization of the different forks and how they work, we recommend watching these two short clips: 
1.	[What is a Bitcoin hard fork]( https://www.youtube.com/watch?v=XCo6yyutYAM)
2.	[Hard and soft forking]( https://www.youtube.com/watch?v=pdaXY1OOiWQ)

 

Or read [this article](https://masterthecrypto.com/guide-to-forks-hard-fork-soft-fork/) explaining it in laymen's terms. A more technical explanation can be found [here](https://bitcoin.org/en/blockchain-guide#consensus-rule-changes)


>💡 A must-see regarding forkology is [Forkology, a study of forks for newbies]( https://www.youtube.com/watch?v=rpeceXY1QBM) from Andreas Antonopoulos. 

 

