# BC-3.3.4 Reputation based systems

## About this chapter? 

One of the proposed solutions for the Oracle problem was creating a reputation based system. This system can however play multiple roles and is possibly important for future blockchain governance and regular governance alike! 

## What will we discuss? 

BC-3.3.4.1 Reputation based systems 
(note: also includes decentralized reputation & reputation tokens)

## After this class, I can:
* Explain the role reputation based systems play in blockchain ecosystems 

* Explain the role a blockchain can play in reputation based systems 

* Explain the role a cryptocurrency can play in reputation based systems 

* Evaluate whether a reputation based system or reputation token could play a role in my blockchain business case

* Evaluate how a reputation based system or reputation token could play a role in the ecosystem of KOIOS 


## Next chapter
 


# BC-3.3.4.1 Reputation based systems

When entities that are interacting are known, trust is established as soon as identities are recognized. In decentralized blockchain systems, trust can be reputation-based. In terms of game theory, reputation helps us make better interactions with other players, because it is tracking behavior in a repeated game (not just one-off, but the game of trust is played again and again; remember iterated Prisoners’ dilemma).

*Reputatio est vulgaris opinio ubi non est veritas.* Reputation is common opinion where there is no actual fact. - Bouvier, M. A Law Dictionary, 1856 

## Can blockchain bring facts, or at least mathematical proofs of their existence, to reputation?

Virtual life online relies heavily on reputation systems. E-commerce with a seemingly infinite number of online stores would be a nightmare, but tracking reviews of sellers and buyers while helpful, is but the tip of the iceberg. A vast portion of security mechanisms are dependent on reputation systems, like chain certificates that web browsers require to function or the web of trust (authentication of public keys in PGP) and so on.

Furthermore, in the future, when there will actually be more than a handful of oracles, trustworthiness of oracles will be critically important. When smart contracts will interact with the physical world more frequently, marketplaces for oracles will become an important part of the ecosystem. To some extent, government agencies might have a significant role here, at least with some services/data they offer already (e.g. a trustful source to questions like: is a particular day a holiday, is a certain person still alive, is a particular document valid...).

In practice, reputation capital has a strong influence on sales performance: seller reputation is strongly correlated to sales volumes and/or sales prices!1 Therefore it can be used as a resource in itself.

## Reputation systems consist of two major components:
1.	The trust model, which describes whether an agent is trustworthy
2.	The data management scheme for storing trust-related data (in decentralized systems this is at least safer than centralized databases used in common reputation systems)

Sources for trust model depend on particular use-case, in general the most relevant are:

* Direct experiences (based on actual interactions)

* Conceptual (cognitive, based on beliefs, or game-theoretical, based on utility functions of agents)

* Witness information (based on observing interactions of others‘, making it a bit more unreliable)

* Others

[Source 1](http://web.csulb.edu/journals/jecr/issues/20131/paper1.pdf)

[Source 2](http://procaccia.info/papers/trust.ijcai07.pdf)
 

## Decentralized reputation

Here, we are not talking only about decentralized storage of reputation data, but about a decentralized trust model where identities are unknown. 

Reputation is accumulated over time and is usually tightly coupled with an identity. In a digital world, a reliable reputation system is faced with many challenges, that are all too known to online stores:

* Altering reputation through fake accounts (Sybil attacks)

* Exit scams (lessened by multi-sig escrow, where moderators are encouraged for at least partial real- world identity disclosure)

* Preserving anonymity (too much ties with the real world – and the security of users is compromised, too loose – and reputation statistics are misleading)

One interesting live experiment of decentralized reputation system is OpenBazaar. Its reputation is based on ratings. Identities are pseudonymous, presented by GUID (a large number), although users can link this GUID to a friendlier handler (Onename Blockchain ID) and make browsing easier. While the identities of buyers are not disclosed publicly, the vendor does see buyers network data, but it is not stored in contracts. Only buyers‘ payment address (e.g. Bitcoin address) is known (that should be unique for each transaction).

Rating can be granular to the level of each particular transaction. It is in best interest of both buyers and vendors to rate the transaction as it is the source for nurturing their reputation and also for the item itself! Even moderators who handle disputes, could be under the pressure of ratings. Which might also be an issue: collusion between buyer/vendor with moderator. 

## Reputation tokens

However, reputation systems are not trivial to create. Some of the challenges to overcome are:
To what object is reputation linked? If it is simply an address, it can be problematic with regards to
managing its private key. If it is an identity object, how is that identity managed?
Who is rewarding the reputation? If it is a central entity, that could be problematic for the 3 types of risks that we mentioned at the beginning of the course. If it is an autonomous contract, how does it increase the reputation of an object – there needs to be some kind of a secure proof available that this action of rewarding reputation is safe.

Are reputation tokens tradeable? Can’t then a desired reputation score simply be bought?
How to reduce the reputation of an object? Burning the reputation tokens would finally bring the reputation score to 0, which is the same score that a new user would get anyhow, thus we are making it seem equal to be a “bad guy with zero score” with being a “new user in the system with default zero score”. Also, is negative reputation possible?


## Augur

An example of a Dapp is Augur (www.augur.net) - A decentralized prediction market which is built on the Ethereum blockchain. 

How it Works

* Users purchase and sell shares in the outcome of an event

* The current market price of a share is an estimate of the probability of an event occurring – this is a typical application of the wisdom of the crowd principle.

Augur aims to address traditional prediction market drawbacks by eliminating counterparty risks and allowing users to settle their bets in cryptocurrencies. Funds are stored in smart contracts.
Augur uses the crowd to report on market outcomes. Each reporter keeps a reputation balance (REP), based on the correct outcomes s/he has provided in the past.

Using Augur, users are able to create a prediction market on any subject and win trading fees (either as market makers or as good reporters).

* [Augur Source 1](https://tokeneconomy.co/the-three-powers-of-augur-7e5aa476d0c5)
* [Augur Source 2](https://tokeneconomy.co/19-augur-predictions-for-19-fc1c1e4d52ba)
* [Augur Source 3](https://www.pdotindex.com/#about)
 
