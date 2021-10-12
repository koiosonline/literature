# BC 3.1.9.1 Lightning Network

The idea is that not all transactions need to be recorded on the blockchain. 
- If two people make multiple transactions between them, there is no need to record all the transactions on the blockchain, which ultimately makes the network “heavier”. 
- a payment channel (SPV) between these people can be created. The opening of this channel is recorded on the blockchain (two-way pegging). Participants will then transact through the payment channel (off-chain – no blockchain transactions at this point) as much as they wish. 
- When participants decide to close the channel, only the final balance of the transactions will be recorded on the blockchain. 
Another hypothetical scenario: person A, person B, person C. 2 payment channels exist: the channel between A-B & channel between B-C. If A wants to send one bitcoin to C; 
- B will send one bitcoin to C, 
- A will send one bitcoin to B for reimbursement. 

●	An original white paper by Poon and Dryja (2016). “The future of Bitcoin”

●	An open-source payment protocol that sits on top of blockchains (for example, the Bitcoin network) to allow for anonymously routed payment channels that have the capacity of millions of transactions per second.

●	A decentralized network that uses the smart contract functionality in the blockchain to facilitate instant payments across a network of participants.

●	It comes as an answer to the “Bitcoin Scalability Problem”.

●	The Problem: The Bitcoin network's capacity to process transactions (i.e., the amount of transactions that the Bitcoin network can process) is limited due to the size and frequency of blocks.

●	If the Lightning Network works as intended, the Bitcoin can theoretically scale to infinity (Quittem, 2018b).
●	A possible solution to the “Bitcoin Scalability Problem” is highly debated –rather an “ideological battle”, not just a technical debate.


## Lightning Network - payment channel

•	Funds are locked in a payment channel (think of them as a safety box). These funds are used for

•	transactions between the 2 participants

•	Participants open up a channel by committing a certain amount of Bitcoins.

•	A “promise of ownership” for a certain amount of bitcoins is transferred between the two participants in the channel when they want to transact. This can happen multiple times

•	Any one of the two participants may decide to close the channel at any given time

•	Closing a channel would mean that a transaction concerning the final balance of the participants will be recorded on the Blockchain, i.e., each participant’s share of the “safety box” is recorded on the blockchain forever

![Source]( https://pbs.twimg.com/media/DvL8ZxZV4AEZ7XG?format=jpg&name=medium)
[Source]( https://twitter.com/lopp/status/1077200836072296449)

## Lightning Network – commonly heard disadvantages
Of course, as you now understand, scaling has downsides as well. The most commonly hear disadvantages are: 
•	1. Set up and close the payment channel. Unfortunately, setting up and closing a payment channel are still expensive transactions on the blockchain.
•	2. Centralization. There is a risk that the network will centralize around a few large hubs. These are central points that have set up large networks of payment channels. Most payments will therefore go through these hubs, which can ensure that there are still parties that can exercise a lot of power. Moreover, this ensures that Bitcoin is more sensitive to outside attacks.
•	3. Bitcoins are locked up. The Bitcoins that you use for your payment channel can only be used for this. If you need it for other payments, you must first close the payment channel to free your Bitcoins.
•	4. Liquidation. There must always be enough Bitcoins on a payment channel to use it. One big issue and the payment channel is empty.
•	5. Always online. You must always be online to receive a payment on the Lightning Network. A transaction can only be done with the approval of both parties.

## Lightning Network – Scenario analysis & conclusion
[Please read this source]( https://blog.bitmex.com/the-lightning-network/) 

## Conclusion
The Lightning Network does appear to offer significant and transformational improvements for scalability potentially. As a result, transaction speeds and fee rates should dramatically improve without impacting the underlying security of the core protocol. Crucially, however, the inferior security properties of Lightning payments may make the Lightning Network unsuitable for larger payments (or, at least, it may be irresponsible to use it for larger payments). Speculation and investment flows, which require these larger payments, are currently the major driving force in the cryptocurrency space. The volume of retail payments is relatively small in comparison. Because of that, Lightning may not be as big a game-changer as some imagine, at least in the medium term. While enthusiasts appear likely to adopt this technology quickly, widespread adoption may take considerable time.

•	Andreas Antonopoulos himself has a distinction to make (and much more to say) in his very interesting video [“Bitcoin Q&A: Misconceptions about Lightning Network.”]( https://www.youtube.com/watch?v=c4TjfaLgzj4)

•	Antonopoulos’ video is a critique of a popular video titled: [“How The Banks Bought Bitcoin | Lightning Network”](https://www.youtube.com/watch?v=UYHFrf5ci_g ) that you might want to watch before Antonopoulos’ video.



## Extra optional sources

•	Explained: https://www.youtube.com/watch?time_continue=11&v=rrr_zPmEiME 

•	LN explained: https://www.youtube.com/watch?time_continue=2&v=MpfvhiqFw7A

•	Playlist / good collection of 35 video’s about Lightning Network: https://www.youtube.com/watch?v=julWo8IJX_8&list=PLPQwGV1aLnTurL4wU_y3jOhBi9rrpsYyi 

•	Good article from Bitmex (trading platform): https://blog.bitmex.com/the-lightning-network/
•	[Source](https://www.linkedin.com/posts/pkravchenko_lightning-network-architecture-ugcPost-6605164245468409856-WAW_/ )
•	[Source](https://www.coindesk.com/researchers-uncover-bitcoin-attack-that-could-slow-or-stop-lightning-payments)
•	[Source](https://medium.com/@jonaldfyookball/mathematical-proof-that-the-lightning-network-cannot-be-a-decentralized-bitcoin-scaling-solution-1b8147650800)
•	[Source](https://medium.com/@timevalueofbtc/the-bitcoin-second-layer-d503949d0a06)
•	[Source](https://medium.com/@timevalueofbtc/the-time-value-of-bitcoin-3807b91f02d2)
•	[Source](https://medium.com/@timevalueofbtc/the-bitcoin-risk-spectrum-949f6abec290)
•	[Source](https://twitter.com/lopp/status/1077200836072296449)

