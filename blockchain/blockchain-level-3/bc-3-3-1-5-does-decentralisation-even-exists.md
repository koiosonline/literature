# BC-3.3.1.5 Does decentralization even exists?


## The meaning of decentralization
In case you need to refresh your memory about decentralized systems, read this article about ["the meaning of decentralization"]( https://medium.com/@VitalikButerin/the-meaning-of-decentralization-a0c92b76a274) 

## Three types of Decentralization
When people talk about software decentralization, they may be talking about three separate axes of centralization/decentralization. While in some cases it is difficult to see how you can have one without the other, in general, they are quite independent of each other. The axes are as follows:

**Architectural (de)centralization (the protocol)** — how many physical computers is a system made up of? How many of those computers can it tolerate breaking down at any single time?


** Political (de)centralization (the politics) ** — how many individuals or organizations ultimately control the computers that the system is made up of?


** Logical (de)centralization (the practical) **— does the interface and data structures that the system presents and look more like a single monolithic object or an amorphous swarm? One simple heuristic is: if you cut the system in half, including both providers and users, will both halves continue to operate as independent units fully?

![source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-3-1-5-does-decentralisation-even-exists-image1.png)


Blockchains are politically decentralized (no one controls them) and architecturally decentralized (no central infrastructural point of failure), but they are logically centralized (there is one commonly agreed state, and the system behaves like a single computer)

Do blockchains as they today manage to protect against common mode failure? Not necessarily. Consider the following scenarios:
•	All nodes in a blockchain run the same client software, which turns out to have a bug.
•	All nodes in a blockchain run the same client software, and the development team of this software turns out to be socially corrupted.
•	The research team that is proposing protocol upgrades turns out to be socially corrupted.
•	In a proof of work blockchain, 70% of miners are in the same country, and the government of this country decides to seize all mining farms for national security purposes.
•	The majority of mining hardware is built by the same company. Unfortunately, this company gets bribed or coerced into implementing a backdoor that allows this hardware to be shut down at will.
•	In a proof of stake blockchain, 70% of the coins at stake are held at one exchange.

Be careful: the internet was originally designed with autonomy in mind as well! Hardcoded defaults/trust anchors, centralized upgrade severs, user preference, proprietary features, spam, DDOS prevention...so many things can practically cause emergently centralized and given a handful of people uneven control over the whole system (and its future direction). Email is a perfect example of an ostensibly decentralized, distributed system that, in defending itself from abuse and spam, became a highly centralized system revolving around a few major oligarchical organizations. The majority of email sent to today is likely to find itself being processed by the servers of one of these organizations. [Source]( https://twitter.com/SarahJamieLewis/status/1029212002953060352)

In the blockchain, for example, Bitcoin: 
▪	Developers 
▪	Mining 
▪	Distribution of tokens
▪	Centralized organizations offering services (like fiat onramp CoinBase or trading platform Binance for example)

Conclusion: many experiments are being set up, new (and old!) forms of governance arise. 

## Decentralisation is a myth? Defensive decentralization

[See a great thread and multiple sources here](https://twitter.com/Melt_Dem/status/1031190564639830016)

The challenge is that natural systems inherently evolve towards hierarchies. We see this emergent property in cryptocurrencies and blockchain protocols as well. The result is: A well-constructed decentralized system will identify & attack emergent centralization (defensive decentralization). An interesting read is, for example: why flat organizations fail [(Source) ]( https://getlighthouse.com/blog/flat-organizational-structure-fails/).
"We need to move beyond naive conceptualizations of decentralization (like the % of nodes owned by an entity), and instead, holistically, understand how trust and power are given, distributed, and interact. Of course, sometimes trade-offs and concentration are desirable, but we should ensure those trade-offs don't have unintended consequences."
[Defensive Decentralization ]( https://fieldnotes.resistant.tech/defensive-decentralization/) 🡪 Conclusion: A chain is a strong as its weakest link…But also keep in mind…what is the end goal? Is it decentralization, or for example, censorship resistance? 
[Comprehensive list of resources for decentralized organizing](https://hackmd.io/@yHk1snI9T9SNpiFu2o17oA/Skh_dXNbE?type=view)

## Quantifying decentralization

If we could agree upon a quantitative measure, it would allow us to:
1.	Measure the extent of a given system's decentralization
2.	Determine how much a given system modification improves or reduces decentralization
3.	Design optimization algorithms and architectures to maximize decentralization

[So let's try to measure decentralization]( https://news.earn.com/quantifying-decentralization-e39db233c28e)
