# BC-2.2.3 The crypto flower leaf 2: Distributed Systems & Consensus

As you know, we are currently still describing the playing field by using the crypto flower. As you probably noticed, the leaves intersect with each other. Proof of Work uses cryptography, but it is also used to buy time for the nodes to reach consensus. So the first leaf was about cryptography. Now we will discuss the second specialized area of blockchains: reaching a consensus within distributed systems. 

## Many different consensus algorithms 
Satoshi kicked off the decentralized consensus party in 2008 with the whitepaper and in 2009 with the launch of the Bitcoin protocol. Since then, many other ecosystems and individuals are experimenting with new forms. Some are taking serious forms and are valued by the [billions]( https://www.coingecko.com/en). 

Other than the division of public, private and hybrid, you have a distinction within those classes as well. So, there are many different algorithms within each realm. The most interesting realm, we think, is the public one. There are the most flavors, and due to the open accessibility, communities instantly learn from each other. Errors can be prevented by learning from others' mistakes. But you can also instantly try out a genius solution you witnessed working in another protocol. 


>💡 The power of open-source is that you can build on the shoulders of giants. The world inspires you, and you allow the world to be inspired by you. It attracts great minds and talent and is a fast-growing approach to build software. 

>💡 Thanks to the value-sharing mechanisms of blockchain technology, a new internet is coming (web3). This enables communities to pay developers to create open-source software (this used to be a huge problem!). A good example of this is the booming website of [Gitcoin]( https://gitcoin.co/). 

We talked about the Satoshi consensus, proof-of-work combined with the longest chain principle, limited blocksize, and alternatives (larger blocks, heaviest chain). But there is an entirely different category, one without the use of energy and calculating hashes. It uses stake instead of energy and is called proof of stake. 


>💡 Proof of stake opens up an entirely new scale of reaching consensus. A stake can take many forms but is often represented by the monetary value in tokens. But stake could also be a reputation, proof of contribution, etc. 


>💡 Each form of consensus has benefits and downsides. Many are tested and used to solve different use cases. Time will teach us which consensus algorithm is suited best for which use case. 


>💡 You will find many proponents or opponents for a consensus algorithm or a combination of a consensus algorithm for a particular use case. We recommend approaching this area and many other areas in life by using the complementary approach. Try to refrain from tribalism, "mine is better than yours, I'm right, and you are wrong". Listen and learn. Rise from the parroting, think, and discuss with respect. There is a chance you might be wrong yourself. Learn from the world. 
## Two sides of a coin

A downside could also be a strength. One of the downsides of proof-of-work is that it is deliberately slow. But that is a necessary cost to create a secure conservative blockchain. But it doesn't offer much flexibility or speed on the protocol layer. This is done to buy time for nodes to reach a consensus, prevent many orphan blocks, and secure the network by gathering a lot of hash power per block. It is, as you now understand, a trade-off between properties in the scaling dilemma. This means that sending bitcoins on the core layer (the blockchain itself) will most likely never be free because you need to pay miners the transaction fee for security. If it's very cheap, then the security might be cheap as well. Block rewards will disappear, and what remains are fees for the miners to validate transactions. So to scale bitcoin, combinations with other layers will probably be made in time. More about this later from Andreas Antonopoulos. 

But what if you need micro-transactions to happen in an instant? You could work on layer two or create a new consensus algorithm. Or both. Here we arrive once again at the doctrine: different use-case, different blockchain. We are perfectly fine with less security because the value of transactions is lower (for example machine – machine [IOT](https://en.wikipedia.org/wiki/Internet_of_things) transactions). There is no need to burn a lot of energy for security. So, let's switch to another common consensus type that offers more scaling solutions: proof-of-stake. The goal remains the same: reaching a consensus about the SSOT. But the goal and methods might differ (a different ball game). 

** Do remember**: the core concepts are often the same, so we still use public-private key encryption and hashes. We still use governance and game theory concepts. We still operate in an open environment, so we still have distribution problems (what were they again……😉?). The difference is the way we reach agreement all together. We still have a distributed ledger that needs to reach a consensus. 

## Proof of Stake (PoS)
But this time, we are not using random numbers and a lot of energy. This time we're doing it differently. Let's say we have ten miners. Sorry, not miners! When we're talking about proof of stake, we talk about minters. We mint coins. We don't mine coins, but we mint coins with PoS. So proof of work is mining, proof of stake is minting. The essence of proof of STAKE is that you put STAKE (skin/value) in the consensus game. As a silly reminder: call it proof of skin, as in you have to get skin in the game if you want to reap the rewards. 


 >💡 Some say that proof of work is also a form of proof of stake. The miners pay money for hardware and energy and are putting their skin in the game. 


So let's say we have some minters who want to reach a consensus. Each of them puts in 100 of their tokens. This means they store 100 tokens on their public key and signal that they are willing to play ball to the network. This means: they would like to determine the next block for the rewards (+ will have to verify the chain and keep it up to date). You can do this all techie via your hardware, but nowadays, your wallet can do this for you as well. Remember that there are many different variants of staking. More about this later. 

Let's go back to the example where we have minters staking 100 tokens in their wallets. If they cheat, their tokens get marked by the community and won't be accepted anymore. Or the reputation of the minter goes to waste. Suppose you act according to the protocol, or the wallet service does this for you (which you need to trust!). In that case, you will receive staking rewards when you help validate the network. It all differs per the consensus method. But how does this consensus process go? 

As a minter, I collect the transactions and hash them into a block. Just as with PoW, but only this time can I ignore the nonces and puzzle of 18 zeroes. That's easy and saves a lot of energy. It is, therefore, faster and less energy-consuming. I hash the block, and the first time is the right time (there is no difficulty in play here!). 

Easy as that, right? Well, not entirely: if it were that easy, everybody would do it, and we would soon have many different forms of truths and no consensus. So we need to establish a certain sequence and randomness that selects the next page. We could determine this in multiple ways, randomly appoint a public key that signaled as a volunteer, or pre-determine a sequence or even appoint a delegated group of minters (delegated Byzantine Fault tolerance, see further up ahead). Or we could upvote certain minters based on their reputations (you have only shown honest behavior, you can keep on minting as long as you don't cheat). 

There are many ways you can determine the sequence. Currently, the most common is that you stake a fixed amount in the protocol. Let's say in our example 100 tokens. Every wallet that has staked 100 tokens and signals for minting ("stake their tokens") can be randomly selected. Like a lottery. Or by voting. Or by some other mechanism. So if ten minters are signaling, each with one public key, your chances of minting the next block are 1/10. If you mint correctly, according to the protocol rules, you receive the newly minted tokens. Correctly = according to the protocol = only record valid transactions and propose only valid blocks = where valid is determined by the rules ("what is valid and what is not"). 

Let's say the reward is one token for each minter block. You will then have 101 tokens in your account. If you present an invalid block, your 100 tokens get marked. This is called **burning tokens**. You can't spend them anymore. Any other minter accepting your marked tokens as valid transactions doesn't act according to the protocol and gets burned as well. So everybody is very alert on what tokens are invalid. 


>💡 Minting tokens and receiving rewards is like owning a transparent glass toll house. You receive a small fee for every transaction, but if you misbehave, the entire group comes by and burns your toll house. How is that for an incentive 😉 


![Toll house image]( https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2F2.wlimg.com%2Fproduct_images%2Fbc-full%2F2019%2F10%2F32662%2Ftoll-barrier-1571739756-5126158.jpeg&f=1&nofb=1) 
[Source Toll House]( https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2F2.wlimg.com%2Fproduct_images%2Fbc-full%2F2019%2F10%2F32662%2Ftoll-barrier-1571739756-5126158.jpeg&f=1&nofb=1) 

This offers more speed and less wasted energy resources. But there are two sides to a coin. One of the problems is that if I'm well-financed, I can increase my stake and increase my chances of winning the lottery for the next block, which increases my amount of tokens and stake. So I'll keep getting richer and richer. For example, if I buy four other accounts, I will own 50% of the minted tokens (my own 100 tokens + 400 that I bought out of the 1000 minted tokens). If I stake and win the next random selection, I'll have 501/1001, which is more than 500/1000. Since my chances are statistically the biggest of everyone, I'll keep receiving more and more tokens, increasing my chances, which will lead to more tokens. Thus, a continuous cycle of the rich getting richer and the poor not getting in anymore. This is more nuanced because buying many stakes will cost you dearly in a full-grown ecosystem (prices will rise). However, buying tokens and acquiring a large stake isn't all that expensive at the start of a blockchain. 

## So, once more, the PoS process
But back to the example: the protocol algorithm randomly selects the minter based on the signal and stake tokens (or some other selection method). The minter collects the transactions and creates the block, including the coinbase with their staking public key, hashes the total including previous hash, etc. Just like with PoW, only this time without the trial and errors of a nonce. Suppose they act according to protocol, and it was indeed their turn to mint. In that case, their presented block gets accepted by the nodes. The minter receives the block reward and possibly the transaction fees. From there, we start all over again. Suppose the minter presents an invalid block or invalid transaction within that block (also resulting in an invalid block). In that case, the staked tokens on the public key get "burned" (marked as unacceptable tokens). The minter can still access the wallet and tokens (via the private key, which is only accessible for the minter him-/herself). Still, as soon as the minter sends the transaction to the network, the others won't risk losing their stake because they include a transaction that wasn't allowed according to the shared rules/protocol. 

>💡 PoS holds a certain risk of big stakes that might lead to bigger stakes = centralizing the governance of a blockchain. Solutions for these challenges are being tested (2021). 


>💡 Rules of consensus: by making behaviour predictable by promoting good behaviour with rewards and make cheating expensive (**[the handicap principle](https://en.wikipedia.org/wiki/Handicap_principle)**).


## Byzantine Fault Tolerance (BFT) systems 

During your consensus quest, you might encounter the term "Byzantine Fault Tolerance systems". BFT systems are just systems that are secure for the byzantine general problem. So problems caused by the BGP, distribution problems as described before. If you're Byzantine fault-tolerant, if you have a good Byzantine fault-tolerant grade, you are very secure regarding these kinds of distribution problems. In this regard, we have, for example, the related "Delegated Byzantine fault tolerance" consensus algorithm. This is a hybrid variant, where trusted authorities are selected and validate and record our transactions. Creating speed, but opening up to the three risks main categories once more. Making it less decentralized, but this time with more transparency for the community because all their behavior is visible and accountable! We can see and act if they misbehave. 

As mentioned, there are many ways to select validators and many different forms of consensus. Most commonly, experiments are run on reputation online (past behavior of validator & stake) or offline (big companies like in Hashgraph or co-founders, etc.). Although these other blockchains are less decentralized (which is up for debate!), they record transactions way faster. Because for example, with NEO, they only have to reach a consensus between 7 known nodes instead of 12,000 unknown nodes. In short: just another shift in the trilemma triangle 😊 

On a side note: we are currently only talking about blockchains. As you might remember from the first class, there are more distributed types of ledgers. They are outside of this scope for now. Still, we will encounter them later because they are very interesting and offer many new insights (like, for example, the DAG/Tangle from IOTA). 

## The consensus jungle 
Other consensus rules arose with different selection mechanisms. Each consensus algorithm has its trade-offs, making it suitable for some other use-case. Or none because they failed. Whether one super consensus will cover all the use-cases or whether these protocols will connect and form one massive network of protocols is unknown. 

>💡 One protocol to rule them all? Or interoperability between protocols? Time will tell. 


<blockquote style="border-color: #ff0bac">❓ What do you think will be the outcome? And what do you hope for? Why?  </blockquote>


Often all using the same basic principles, for example, rewarding honest behavior in paying in the native token of the network and punishing misbehavior by burning the tokens. Don't get lost in comparing and battling between consensus methods. Like mentioned soooooooo many times before: it is unrealistic to compare because the trade-offs are different, making it suited for an entirely different use-case. PoW is slow but seems to be more secure. PoS is faster but seems to bears more risks. Many other forms with benefits and downsides exist, but more about that in later deep dives in level 3. 


![Different types of consensus algorithms](https://findcrypto.net/wp-content/uploads/2018/08/CryptoCurrency-Different-types-of-Consensus-Algorithms.-Great-overview-by-Aviv-Lichtigstein.jpg) 
[Source Different types of consensus algorithms]( https://findcrypto.net/cryptocurrencies/crypto-news/cryptocurrency-different-types-of-consensus-algorithms-great-overview-by-aviv-lichtigstein/)

We finish with an overview of different groups of consensus out there or check out this image. Keep in mind when reading and listening: DYOR. We are all in the experimental phase. All of them need to be battle-tested over time! 


## A comparison between PoW and PoS
You can find a [short clip]( https://www.youtube.com/watch?v=M3EFi_POhps) about the two to get a gist of the discussion PoS versus PoW. Keep in mind: the opinion of the creator might be incorporated, so always think and DYOR. Ignorance is a choice 😉

We also like [this session](https://www.youtube.com/watch?v=3W_3AQrQEOM) from Andreas. Just remember, we are all experimenting, and different blockchains = different use-cases. Listen and learn from each other, be nice 😊 

## Portfolio assignments 2.2.3 The crypto flower leaf 2: Distributed Systems & Consensus


We explained the consensus algorithms PoW, PoS, BFT and dBFT. Which one of these consensus algorithms do you prefer and why?


Prove that you master the learning goals of this chapter:

categorize and break down the different set of properties of distributed ledgers (analyse)

evaluate which properties settings in a blockchain can lead to which properties of the network and therefore which possible use cases are suited (evaluate)

analyse a random blockchain of your liking and based on the collected information evaluate whether the blockchain is well-suited for their described main goal (analyse)

name the strengths and weaknesses of a blockchain or other form of distributed ledger based on the core properties (evaluate)

analyse the impact of a change in properties of the network and their impact on the goal of that network


## Further readings
* [Overview consensus shortly explained](https://hackernoon.com/a-hitchhikers-guide-to-consensus-algorithms-d81aae3eb0e3)
* [Overview from 101 blockchains (enterprise blockchains)](https://101blockchains.com/consensus-algorithms-blockchain/#prettyPhoto/0/ )
* [PoW versus PoS](https://www.youtube.com/watch?v=M3EFi_POhps )
* [Proof-of-Work (PoW), Proof-of-Stake (PoS), Delegated Proof-of-Stake (DPoS)](https://www.youtube.com/watch?v=3W_3AQrQEOM)
* [A hitchhiker’s guide to consensus alghoritms](https://hackernoon.com/a-hitchhikers-guide-to-consensus-algorithms-d81aae3eb0e3)
