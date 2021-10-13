# BC-3.3.2.9 Bleeding edge technology


At this time, when smart contracts are still a bleeding-edge novelty, there are some profound and some pesky limitations to working with them. But, knowing where we are now, we can expect things to smooth in due time, hopefully in the next couple of years. 

## Technology life cycle 
Bleeding edge technology is but a first phase of the technology life-cycle:
* Research & Development phase (a.k.a. bleeding edge) – mainly here
* Ascent phase – the strongest phase, where competition is weak and premiums high – some areas here
* Maturity phase – high and stable gains from a mature technology –not here! 
* Decline phase – the utility of the technology fades away and earnings decline – will eventually end up here

## Risky phase 
It is important to know about bleeding edge because it is very risky (problem of not delivering) and is short-term expensive (problem of funding). In addition, there are no best practices established, both users and developers are unfamiliar with the product, lack of testing is very obvious, and the existing, broader ecosystem is a priori resistant to accept changes.


## The "benefits" of smart contracts & trust on the blockchain

•	Self-enforcing contracts" enabling "upfront compliance
•	Immediate clearing and settlement (t = 0). Software that simulates contract logic with guaranteed execution, enforcement, and payment
•	Secure and interruption-free / unstoppable – on the blockchain - with business logic insured by cryptography, with the ability to perform actions based on events
•	The ability to automate terms and conditions of agreements
•	Contracts are possible in both the long and very short term
•	Traceability & Transparency in transacting data 
•	Increasing cost efficiency (money & time) 
•	Accuracy - Smart contracts are executed by machines. (almost) no burden of human error.
•	Autonomy - The agreement is truly entered into by yourself.
•	Availability 
•	Backup - Because everyone has a copy of the blockchain, the contract cannot possibly be lost.

![Source](https://blockgeeks.com/wp-content/uploads/2016/10/Smart-Contracts-are-Awesome-1.png)

[Image from source Blockgeeks and good recap]( https://blockgeeks.com/guides/smart-contracts/)


## Challenges

![Source]( https://blog.pwc.lu/wp-content/uploads/2018/06/Smart-contracts_Infographic_10-Challenges-768x1253.png)
[Source]( https://blog.pwc.lu/smart-contracts-adoption-challenges/)

The nature of smart contracts makes their implementation a challenge in many ways. On one side, we have smart contracts on permissioned blockchains, which can be executed "fast "(consensus optimized for high transaction throughput) and "cheap "(no need to pay gas for execution, because spam is not an issue, but could otherwise still serve as a halting mechanism) – their larger problem is more political: adoption, standardization, liability, etc.

On the other hand, smart contracts on public blockchains have many technological challenges, some quite fundamental. Some of the most persistent are:

*Immutability*– we have talked about its benefits. Still, it is a delicate thing: whenever smart contracts interact with humans, mistakes happen, and they should have a recourse, which is difficult in an immutable context. 


*Security *– writing smart contracts is supposed to be easy, as is making transactions, but that is a two-edged sword: one mistake and money is irrevocably gone. Unfortunately, users are not always careful, and attackers have to scan the blockchain to find vulnerable contracts. That, joined with the immutable nature, can mean that we have more limited ways of fixing security holes.


*Confidentiality *– smart contracts on public blockchains can "show too much ". Of course, everything is transparent (both data and business logic), but they would be safer to use if they allow for some privacy. We can expect this to be researched and implemented somewhere shortly with the help of cryptography and secure hardware modules.


*Quality data feeds* – as we have seen in the previous session, the self-contained network where smart contracts live needs a secure bridge to the external world. So again, honest oracle services, or a reliable consensus from a group of syndicated oracles, is crucial.

## Development limitations
Programming in such a rapidly evolving and uncharted environment is quite an experience. Things are slippery and often change: not just the programming tools but also the underlying programming language and execution environment. "Often "means substantially more than in the classic application development world.
The situation is different on public blockchains than on private ones, but let's not consider private ones here as they can operate under any conditions suitable for them, can adjust easier, and are contained. In contrast, public ones are more general and operate in a hostile environment.
Best practices are only recently being formed, smart contracts fall way behind in testing, and vulnerabilities are everywhere to be found. Of course, this is just as expected since we said we're still in the bleeding edge phase, so there is nothing wrong with it – as long as real people don't unknowingly lose real money, of course.

## Languages 
What programming language can be used for smart contracts, which one is the best right now and which one will be maintained for the duration of your application (case in point with Ethereum: Serpent language is stalled, but some prominent projects, like Augur, depended on it and were forced to migrate from it in a short period). Sometimes a brand new programming language is made, for various reasons, to be used in smart contracts (like Solidity, or now Vyper, in Ethereum), meaning developers must learn it from scratch and have a very limited knowledge base to rely on.

## Clients 
choosing the right client to connect to the network might not be a problem with Bitcoin and private blockchains, as they currently often rely only on one client. Still, again with Ethereum, the geth client was the preferred one, but that changed drastically in 2017 when under heavy attacks, the Parity-Ethereum client proved itself to be more secure. In 2018, two new clients were emerging: Harmony and Trinity. In the end, it might be best to build an application that is indifferent to the client chosen.

## Frameworks 

A great boost to development are frameworks that speed up mundane tasks such as packaging, deploying, testing, etc. A smart contract can fit very well with existing frameworks, like Maven or Meteor, but some specialized ones are also. Ethereum has some very useful frameworks already (Truffle, Embark, Zeppelin), but stay calm when your project breaks during the upgrade of your client and the framework use old and incompatible libraries (or vice versa).

## Storage 
Storing data on the blockchain is expensive (remember that it is stored on every node), so there is a whole new concept of storage with smart contracts. Usually, it is done by storing only a hash of data on the blockchain. At the same time, the data itself is offloaded somewhere. In the case of Ethereum, the Swarm protocol will be used as an incentivized decentralized file storage, tightly linked to Ethereum. Still, in general, it seems that IPFS (a peer-to-peer file system) is gaining in popularity. With that, new kinds of issues arise: if the storage is decentralized – is it safe, will it always be accessible, how can you remove it, how to update it. Unfortunately, there are no easy answers.

## Speed (latency) 
In the world of instant messaging, instant payments, and instant coffee, waiting 10 minutes for an update in Bitcoin application or even 13 seconds in Ethereum is quite a paradigm shift. However, end-users are usually not willing to wait so much. That is why developers must design their applications with even more complexity to provide a smooth user experience.


## Scaling 
All nodes run the same code on existing blockchains. 

>💡 This means that the computing power of the entire network cannot be greater than a single computer or cluster of computers. This is because all nodes must have the same code as part of the process to perform the blockchain/transactions to verify. 

Challenge: Computers on the network cannot be clustered endlessly without their centralization. Therefore, unreliability arises (hence the scaling trilemma & different offered solutions). 
Interesting read: [Barclays Investment Bank describes technology challenges for smart contracts developers](https://uk.news.yahoo.com/barclays-investment-bank-describes-technology-205010242.html), (A sanity-checking article from the Ethereum DevCon1 conference in 2015, where an experienced banker asked provocative but well-intentioned questions about how can blockchain systems compete in scalability with highly specialized software currently used in financial institutions.)

## Costs
application deployment and updating data are not free on public blockchains because transactions and storage require paying fees.
Don't forget to account for fees when planning your Dapp 😊 
## Examples of security failures and mitigations	

This list extracts some of the most common security failures from Let's talk about Security on Ethereum [C. Brown, 2017]:
Phishing scams – people are often lured to malicious websites. Still, they have a similar address and design as the real website → if you are gathering funds or offering a dApp yourself, take great care to secure the inflow of users. Expect impersonators at all steps of your process.
Sending money to the wrong address – sending cryptocurrency or any tokens is difficult for users as the addresses are just a bunch of "random" characters, typing mistakes happen. Still, also, users do not know whether the address is real or fake → consider using ENS on Ethereum or similar services for user-friendly naming conventions; check user's comments for a particular address online [(like so)]( http://i.imgur.com/i99arJz.jpg).

Bugs in the code – there will be bugs with every software. Consider the whole security stack, from computer hardware to the wireless internet connection, to unknown services running in the operating system to good development practices, following security recommendations, etc.
Or just poorly written code that ultimately causes people's money to be stolen → considers audits of the source code. There are several companies already serving this niche. For example, one security company reports that [32% of all smart contracts they've audited contained critical vulnerabilities]( https://medium.com/%40hosho/auditing-the-unchained-capital-smart-contract-ac2d7ecea373)! Unfortunately, smart contracts are not easy to patch once deployed.

## The halting problem
A programming language that Turing is complete can theoretically perform all tasks that computers can accomplish. Almost all programming languages are Turing complete (ignoring limitations of finite memory). Moreover, Turing's complete languages offer extensive expressiveness. 
The Halting problem – Given a program/algorithm will ever halt or not? [Explained here ]( https://www.youtube.com/watch?v=wGLQiHXHWNk). In short: Turing completeness is inherently insecure because mathematically always there an infinite number of statements will not be can be proven or invalidated. Things can be done simultaneously, mathematically proven, right and wrong (0 and 1). An example: 
A teacher and student agree on the following:

• The law student pays 50% of the tuition fees in advance

• The second 50% will be paid by the student when they win the very first lawsuit

After graduation, the lecturer sues the student for the second half to pay (= first lawsuit student)

• If the student loses the lawsuit, they no longer need the teacher to pay, by the agreement

• If the student wins the lawsuit, they do not have to be the teacher pay according to the lawsuit

A solution to the halting problem: choosing consistency and decidability (instead of expressiveness). So use logic that is consistent and decidable (deterministic logic instead of non-deterministic
logic). Enabling that statements about code can be proved mathematically (bug-free code) and evidence can be trusted

## Further Thinking
<blockquote style="border-color: #ff0bac">❓ How can you gamble via the blockchain if every node runs the code with a random factor? Wouldn't every node reach a different random output and, therefore, different outcome & result?</blockquote>

[Further reading and example]( https://blockgeeks.com/how-smart-contracts-can-revolutionize-gambling-markets/)


