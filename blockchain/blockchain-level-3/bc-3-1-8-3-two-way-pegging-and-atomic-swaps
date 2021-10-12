# BC-3.1.8.3 Two-way pegging & atomic swaps

Instead of destroying assets and creating new assets every time you want to transfer them from one blockchain to another, like in the case of the one-way peg, we transfer existing assets from the parent chain, i.e., we create a transaction on the first blockchain by locking the assets on the first blockchain. Then we create a transaction on the second blockchain and provide cryptographic proofs to the transaction on the second blockchain that the assets were locked correctly on the first blockchain. So sidechains cannot cause unauthorized creation of coins. 

![source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-1-8-3-two-way-pegging-and-atomic-swaps-image1.png)
[Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-1-8-3-two-way-pegging-and-atomic-swaps-image1.png)


## Symmetric two-way peg

Suppose we want to transfer assets from the parent chain to a sidechain. In that case, we send those assets from the parent chain to a special output located on the parent chain itself and lock it there. Then, we can redeem these coins in the sidechain from the special output located on the sidechain by providing SPV proofs to the sidechain that the assets were locked correctly on the parent chain.

So what are SPV(Simplified payment verification) proofs?
It is used to verify if a transaction has occurred or not. It has a list of block headers demonstrating proof-of-work and cryptographic proof that output was created in one of the blocks in the list. Thus, anyone in possession of an SPV proof can determine the chain's state without needing to replay every block.

![Source]( https://miro.medium.com/max/276/1*kKv59wZBnxFt9F731OEB4Q.png)
[Source & reading]( https://medium.com/blockchain-musings/pegged-sidechains-cafe1d8c7023)

We can synchronize this process by having two waiting periods:
•	1. Confirmation Period: The duration of time for which the coins are locked on the parent chain before they can be transferred to the sidechain. After locking the coins in the special output of the parent chain, the user has to wait until the confirmation period is over. After the confirmation period, the user can create a transaction on the sidechain by providing SPV proof that the coins were locked correctly on the parent chain.

•	2. Contest period: The main purpose of having the contest period is to prevent double-spending. The user has to wait for this duration of time before spending the newly transferred coin. Suppose a reorganization proof is provided during this delay which doesn't include the block in which the lock output was created. In that case, the previous proof is invalidated.


•	Both confirmation and contest periods would be on the order of a day or a two. We can use atomic swaps to avoid this delay. Atomic Swaps, or atomic cross-chain trading, is the exchange of one cryptocurrency for another cryptocurrency without the need to trust a third-party

•	The Lightning Network enables "Off-Chain, Cross-Chain Atomic Swaps."

•	Atomic swaps facilitate exchanging different cryptocurrencies or tokens for one another in a decentralized, fee-less, trustless way, and instantly, and safely, without the need for a third party.


•	According to Andreas Antonopoulos, Atomic Swaps can couple two blockchains together so the blockchains can exchange value.

•	Background-The Problem to be solved: Cryptocurrency exchange transactions typically take place on exchanges, which, as you already know, are centralized. Thus, they are risky as they can be hacked (remember Mt. Gox). They also take fees. In addition, they can crash during high market activity.


•	Atomic swaps, this "revolutionary development" - considered to be the future of crypto trading - is here to "take the promise of decentralization to a whole different level." (Peaster, 2018)


•	By allowing peer-to-peer (P2P) trades in a completely trustless way, with no need for any kind of third- party, or centralized infrastructure.

•	More specifically, let's suppose that two people, Alice and Bob, wish to trade some Vertcoin for Bitcoin (the example is from Matthew Hrones, 2017).

•	The two parties agree upon the exchange rate. Therefore, no third party is required.

•	What happens next?


## How they work
Alice is the initiator in this scenario, and she creates something like a "lockbox" (known as a "contract address ") that holds funds during the swap. To open the "lockbox" and access the funds, two things are required:
1. Bob's signature, and
2. A secret number that Alice generates herself.
•	Alice mustn't share the number with Bob, as he could open the box and take the coins before the swap.
•	Alice takes the secret number and creates a hash (acts as the "lock") of the number (the "key" of the lock, as you can get the hash from the number but not vice versa).
•	But even if Alice has both the lock and key, she can still not open the box and get her funds back because, as you recall, the "lockbox" still needs Bob's signature.
•	Bob will then inspect Alice's contract address ("lockbox") and make sure everything is in order before he creates his own "lockbox".
•	Alice will send Bob the hash of her box so that Bob can make a similar box with the same key, but in his case, he needs Alice's signature to open it.
•	From this point, Alice has both the key and the ability to sign for Bob's box and can redeem the funds tied to the address. When this is done, the secret number that Bob needs but does not know is broadcasted for all to see.
•	Bob can then take the secret number, open Alice's box, and redeem the funds.
•	The exchange has taken place!
•	What would happen if either Alice or Bob backs out halfway through the swap?

## Recommended reading:
•	Atomic Swaps explained in the video: [here]( https://www.youtube.com/watch?v=fh-i8lVhN9o)
•	Atomic Swaps explained in the article: [here]( https://coincentral.com/what-are-atomic-swaps-a-beginners-guide/) or [here]( https://www.cryptocompare.com/coins/guides/what-are-atomic-swaps/)

## Atomic Swaps – Advantages and Applications	

•	Both lockboxes are made in a way that provides that if the swap does not take place, all funds are returned to their owners depending on a specific period set by each party.
•	"Off-chain," i.e., Atomic Swaps can complete a transaction without registering it on the blockchain (no fee);
•	"Cross-chain," i.e., the transaction is between two different chains (e.g., swap BTC for LTC);
•	"Atomic," i.e., two outcomes are possible: either the two parties successfully exchange assets, or nothing happens (Quittem, 2018).
•	Since it will be easier to exchange cryptocurrencies, the adoption of cryptocurrencies is going to increase. "Switching costs" between cryptocurrencies will reduce dramatically (or get eliminated) and additional security - as you don't keep your private key on an exchange. 

 

