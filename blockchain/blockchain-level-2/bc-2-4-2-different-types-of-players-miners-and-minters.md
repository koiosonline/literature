# BC-2.4.2 The different types of players: miners and minters

This chapter discusses miners and minters but also discusses the mining process and the energy debate. It eventually became a mining and minting special.

## The core job of mining and minting
Miners = proof of work, and Minters = proof of stake. What do they do? They both collect and record valid transactions. First, they check the digital signature, ownership, double-spending, etc. If all transactions are correct, they gather them and organize them in a block. Next, they hash the block either by solving a puzzle or providing a stake, eventually presenting the blocks to other miners and nodes. Finally, the other nodes check their work.

>💡 In short: miners and minters record and validate transactions and offer the ledger security. They replace the role of the TTP.     


## Mining services
A mining service is often nothing more than an intermediate party that enables/simplifies participating in mining. Please don't get it confused with the mining pools, where you often need to set up and enroll yourself (unless you do it via a mining service, who does it for you). A [mining pool]( https://en.wikipedia.org/wiki/Mining_pool) is not to be confused with the mempool. A mempool is where the transactions between users are stored before miners in a block gather them. A mining pool is nothing more than individual miners teaming up to increase their chance of hash power and increase the likelihood of receiving bitcoin.

Why would you team up like that?

Imagine if you wanted to mine but don't want to invest in computational power. It is not a fair contest against the ASIC mining farms from big corporations located in volcanoes. If you manage to solve a block, you will earn 12,5BTC + fee. Still, unfortunately, the chances of getting lucky and mining an entire block are very slim, and you would be wasting your energy. But suppose you collect the mining power of multiple people. In that case, you could hash together and get luckier with your joined mining power.

You will have to distribute the funds somehow. How this distribution of mined bitcoins is done between its contributing members depends on the mining pool. So this time, your mining power is not wasted as you'll receive a portion of the mining rewards (for example, 0,01 BTC instead of 6,25 BTC). A short introduction of mining [here]( https://www.youtube.com/watch?v=GmOzih6I1zs) includes this mining pool concept.

## ASIC mining in PoW
You can imagine that these mining pools got quite popular over a while. Big mining pools often mine the power of the masses and blocks. Once, one mining pool managed to get up to nearly 51% of the network and decided to cut loose some of its members because of the damage this could do to the network's image. However, the fact remains that bitcoin mining is not 100% decentralized. Perfection doesn't exist. At least, not yet 😊

The centralization is mainly caused by ASIC mining, which allows you to buy computing power, securing the network with your staked money in hardware. Sounds familiar / see the resemblance with PoS where minters risk the digital public key instead of physical hardware?

Check this [video]( https://www.youtube.com/watch?v=-z4qbkQ3cK8)  or [this comparison]( https://www.bitcoinmining.com/bitcoin-mining-hardware/) to see how ASICS looks like. An ASIC is nothing more than a video card (often used in gaming). It is finetuned for one thing only: calculating as many hashes per second as possible. So it is a specialized graphic card that looks a bit like a mini-computer. The hardware we show you in the video is a node, a tiny computer (Raspberry Pi). It does not compute as fast as an ASIC card. So the better the mining gear, the more hashes it can compute, and of course, the bigger the chances are that you find your random number, which will lead to the block solution.

## Who are the miners?


[In case of Bitcoin](https://bitnodes.earn.com/)
[In case of Ethereum](https://www.etherchain.org/charts/miner )


Bitcoin has relatively centralized mining powerhouses. There are multiple big mining companies and pools. Most of them were Chinese in the past, but we have seen some changes in the last two years. There is a famous picture of four or five persons sitting on stage. All of them together were approximately 70 to 80% of bitcoins mining power. In Ethereum, you've got a bit more miners and very concentrated mining pools. But Ethereum is moving towards PoS as we speak. Less centralized than in Bitcoin (SHA-256 is very well suited for Asic Mining, where the KECCAK hash from Ethereum is less so). So, therefore, most of the ASIC -mining power concentrates on Bitcoin and not Ethereum, which you can also see in the hash rate of both networks. Therefore, attacking a block is more complex and expensive in Bitcoin than in Ethereum. Ethereum also produces blocks +/- 15 seconds instead of every 10 minutes.

## The energy debate

Do realize that this concentration of mining power in one current region is merely a current situation. This can change as miners tend to relocate to find the cheapest energy (often in oversupply, as shown below). They use these market inefficiencies caused by overproduction or legislation. In some regions of the world, you can use cheaper dirtier types of energy. You can imagine a mining farm uses a tremendous amount of energy. Besides, the noise (as you people wearing headphones in this 360 videos [short clip]( https://www.youtube.com/watch?v=73fqVCH5F4U&feature=emb_logo) also needs a lot of cooling, which also costs energy. Sometimes they are, therefore, also located in colder regions. As a big mining company, you need to find your trade-off between costs of energy, good natural resources, good legislation, and many more choices. A change in one of these variables might lead to a shift in strategy and location. [The cost of mining]( https://www.youtube.com/watch?time_continue=126&v=E4c6GrI4qVs&feature=emb_logo) is an essential factor, of course.

That's also where currently, a lot of the friction lies with Bitcoin. The [Bitcoin energy]( https://cbeci.org/methodology/) increases every year. As our field partner Martijn Bolt beautifully [puts it]( http://www.martijnbolt.com/top-7-persistent-myths-about-bitcoin-refuted/): Bitcoin's network validation by miners runs for over [74% on renewables]( https://coinsharesgroup.com/research/bitcoin-mining-network-june-2019) and naturally supports innovation in green energy production.

If you want to tackle the "[energy problem]( https://medium.com/@dergigi/bitcoins-energy-consumption-6dd7d7a2e463)" (not a problem, but design choice creating energy money): why is that dirty energy still available and allowed to be used in regions of the world. These companies aren't bound to one area (they fill the market opportunities created by different legislators, etc.). So some suggest that if you want to tackle the real problem, attack the source of the problem. In this case, try to (dis)incentives miners by, for example, increasing the tax rate on dirty energies. So if you raise the dirty energy tax rate, miners can/must relocate to cheaper forms of energy (because of the zero-sum, where one miner wins, another loses). Eventually, perhaps even renewable energy. I will upload a [video]( https://www.youtube.com/watch?time_continue=2&v=2T0OUIW89II&feature=emb_logo) of Antonopoulos, who explains this well (minute 39:00 - 42:00). 
This article also reflects on this video:

![Source Antonopoulos]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-4-2-different-types-of-players-miners-and-minters-image1.JPG)
 

A final side note is that the dependency of bitcoin mining on one supplier (ASIC) is not a very healthy decentralized utopia. There are many more centralized spots. But we will show later in the Bitcoin/Blockchain Bootstrap that doesn't necessarily mean we have a problem (not optimal, though). Just remember that there is always room for improvement, so let's get to work 😉!

## Game theory & mining cycles

Let's talk about game theory, economics, and the importance of blockchains when related to mining.

>💡 PoW mining is a zero-sum game (where one wins, another loses). You can both still make a profit in $ when the price of the cryptocurrency rises. Besides being zero-sum, mining is a cycle:

![Mining cycle]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-4-2-different-types-of-players-miners-and-minters-image2.png)
(Based on source Bitcoin wiki]( https://en.bitcoin.it/wiki/Difficulty)


1. Let's start with the mining "race". As you now know, the race is nothing more than adding random numbers (nonce) to solve the puzzle (reach outcome < hash target).

2. The more random numbers you can generate (computing hash power) / the faster hashes per second = the faster you solve puzzles than your competition.

3. So, if you buy faster rates per second, the total hash increases. If the hash rate increases, the difficulty will increase by setting a lower target. The block becomes more secured because more computing power is needed to solve the puzzle.

4. This means that it will take that person less time to solve the block puzzle. Because increased hash rate means there's more power in the block, which means the block is more secure because it's more expensive to alter the past. It becomes more immutable, as we say.

5. Finally, if it takes less time to mine the block, the protocol checks every 2016 block (in the case of Bitcoin). It will validate: is the approximate solving time past 2016 blocks 10 minutes? If it's 10 minutes, the difficulty won't change if the average time would be five minutes, the difficulty doubles. For example, the target number drops from <100 to below 50 (as with Limbo dancing, the lower, the more difficult). So the increase in difficulty will lead to a more demanding race to build a block, which brings us back to 1. A more challenging race needs faster hashes per hour, which increases the hash rate / more security. More security will lead to more hash rate, which will lead to a shorter solving time, where the protocol checks every 2016 block "is the average time still 10 minutes?" If yes, we can continue (it won't increase nor decrease). If not, it will become more complex.

Note: if it takes 20 minutes on average, the [target]( https://en.bitcoin.it/wiki/Target) will be made less complicated. It can only gain or drop 2x every time in [difficulty]( https://en.bitcoin.it/wiki/Difficulty#What_is_the_maximum_difficulty.3F). It is a protection mechanism to protect from somebody taking over the network and leave the others behind. So if you have a supercomputer, you still won't leave all the other mining networks behind. The beauty, of course: if you do have all of a sudden an "alien or secret NSA supercomputer" that gives you an advantage over all the competitors, everybody will see this. They will see that the mining is compromised but still spend valuable resources (energy, supercomputer). However, your reward is still in the local digital currencies. For example, let's say Ether: Ether's price will fall in this case (of using a supercomputer) because everybody sees that the mining is (extremely) centralized to one entity. Therefore the network is compromised / less valuable (it loses trust, rewards will drop).

An exciting story as follow up, love this story: once three Russian researchers connected the nuclear computer power to mine bitcoins. Because of the open character of the network, this was instantly visible, and people led it back to this nuclear power plant. I don't know if they got fired or if this story is even true. Still: strange developments are instantly visible because of the open character of the protocol.


## Energy money
Interestingly, we now enabled energy backing currencies, "energy money", which is also digital and well-equipped for the future. As Mark Twain once beautifully put it: ``To make a man/woman covet a thing, it is only necessary to make the thing difficult to attain." When Satoshi designed PoW, he fundamentally changed how consensus between humans is formed from political votes to apolitical votes (hashes) via energy conversion. PoW is proof of burn, or the validation that energy was burnt. Why is that important? It's the most simplistic and fairway for the physical world to validate something in the digital world. PoW is about physics, not code. Bitcoin is a super commodity, minted from energy, the universe’s fundamental [commodity]( https://mitpress.mit.edu/books/energy-and-civilization). PoW transmutes electricity into digital gold. [Source: POW is efficient]( https://medium.com/@danhedl/pow-is-efficient-aa3d442754d3).

We talked way too long about miners already, so let's make the next session much shorter 😊!

## Further readings

* [Short overview mining](https://www.electriccapital.com/electric-research)
* [What is a mining pool](https://en.wikipedia.org/wiki/Mining_pool)
* [How the blockchain is changing money and business | Don Tapscott](https://www.youtube.com/watch?v=Pl8OlkkwRpc)
* [Mining farm 1](https://www.youtube.com/watch?v=-z4qbkQ3cK8)
* [Comparison bitcoin mining hardware](https://www.bitcoinmining.com/bitcoin-mining-hardware/)
* [Overview bit nodes Bitcoin](https://bitnodes.earn.com/)
* [Overview miners Ethereum](https://etherchain.org/charts/miner)
* [Mining farm 2](https://www.youtube.com/watch?v=73fqVCH5F4U&feature=emb_logo)
* [Cost of mining](https://www.youtube.com/watch?v=73fqVCH5F4U&feature=emb_logo )
* [Energy research](https://cbeci.org/methodology/)
* [Bitcoins energy consumption](https://medium.com/@dergigi/bitcoins-energy-consumption-6dd7d7a2e463 )
* [Antonopoulos on energy consumption](https://www.youtube.com/watch?time_continue=2&v=2T0OUIW89II&feature=emb_logo)
* [Inside a secret Chinese mining farm](https://www.youtube.com/watch?time_continue=1&v=K8kua5B5K3I&feature=emb_logo)
* [Energy and civilization](https://mitpress.mit.edu/books/energy-and-civilization )
* [PoW is efficient](https://medium.com/@danhedl/pow-is-efficient-aa3d442754d3)
* [Mining software](https://99bitcoins.com/bitcoin-mining/software/ )
* [Energie report Bitcoin](https://coinsharesgroup.com/research/bitcoin-mining-network-june-2019 )
* [Blog Martijn Bolt](http://www.martijnbolt.com/top-7-persistent-myths-about-bitcoin-refuted/ )
* [Target](https://en.bitcoin.it/wiki/Target )
* [Difficulty](https://en.bitcoin.it/wiki/Difficulty#What_is_the_maximum_difficulty.3F )




