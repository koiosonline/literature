# BC-3.1.7.3 The benefits and downsides of blockchain forking 

**Benefits and downsides of forking: it can improve software (updates) or slow down software (split resources)**

When a soft fork is supported by only a minority of the nodes in the network, it could become the shortest chain and consequently become orphaned by the network. In the case of a hard fork, the chain can be split off and create two separate chains. This may be acceptable for cryptocurrencies, but this may have become unwanted in business processes as it may cause fragmentation or loss of control. Or imagine if you have your house recorded on one blockchain, and it forks ten times. 

Hard forks are also susceptible to political impasses, caused when a portion of the community decides not to abide by new rules and keeps implementing older consensus rules. When forks are unmanaged, the risk of attacks could involve inconsistency of data stored in the ledger. All significant issues with forks occur mainly in public blockchains. For this reason, it is important to consider this when considering a public or private type of blockchain. They do recover fundamental errors, an example of such an improvement: [the value overflow incident]( https://en.bitcoin.it/wiki/Value_overflow_incident)

However, it is still valuable to avoid hard forks when possible. A [hard fork]( https://bitcoin.stackexchange.com/questions/9173/what-is-a-hard-fork) is a non-backward compatible change. Downsides of hard forks include:
•	It reduces network effects. Not everyone is speaking the same language anymore.
•	It creates work. Anyone using the forked protocol probably had their code broken in a world that is increasingly interconnected through transparent and trustless code execution, these effects compound.
•	It reduces trust. Now that we’ve had a breaking change, those previously referencing the protocol must now go outside the blockchain and somehow figure out what the “right” new version is to use.

>💡 Sometimes a fork is compared with a military coop (bloody) 

Blockchains have network effects, and blockchain communities generally would prefer to stay together than to fork apart. However, because blockchains are software running on the internet, a portion of the community that questions the legitimacy of a governance decision can make a copy of the blockchain network (and corresponding software repositories) and maintain a “fork” of the blockchain outside of the governance of the original chain. See Bitcoin Cash and Ethereum Classic for case studies of blockchain forks.
Forking a blockchain is a coordination problem because participants might have peers who are signaling their intent to adopt different sides of the fork, possibly because of contention about which post-fork community gets to use the pre-fork trademark.
As a general rule, I recommend that the reader imagine that forking a blockchain is much easier than forking a nation-state but much harder than forking Linux³. As another general rule, there is naturally a “power law” distribution, where most blockchains have relatively small communities relative to a small number of blockchains with relatively large communities. [source]( https://blog.goodaudience.com/blockchain-governance-101-eea5201d7992)

One of the risks after a fork is a so-called replay attack. A replay attack (also known as playback attack) is a network attack in which valid data transmission is maliciously or fraudulently repeated or delayed. This is carried out either by the originator or by an adversary who intercepts the data and re-transmits it. For example: if I see your transaction on blockchain A and copy that in blockchain B as well, I receive funds twice via blockchain A and blockchain B but only give you the goods once. 
Solutions: wait till all the dust is settled with your transaction (time differs per blockchain). In the case of the BTC-BCH fork, two weeks was suggested if you wanted to be sure. 
More explanation is needed regarding replay attacks? Watch [this clip]( https://www.youtube.com/watch?v=XBk8hBJ1xVo&feature=emb_logo)

## Further Thinking
Sometimes things [tend to get heated]( https://www.youtube.com/watch?v=oCOjCEth6xI) in hard forks & different visions for the protocol. So what do you think about this ‘Forkmania’: what are your opinions, should we, for example, all unite under one flag, do you believe forks something beautiful will walk out of this [zoo of forks]( https://en.wikipedia.org/wiki/List_of_Bitcoin_forks ) (let the strong survive), etc.? 

