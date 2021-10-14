# BC-3.3.7 Consensus


## About this chapter?

You can't do governance & blockchains without consensus between ecosystem members. This paragraph is a classic DYOR regarding the many experimental consensus variants out there. 

## What will we discuss? 


BC-3.3.7.1 Examples distribution problems & Different proposed solutions

## After this class, I can:

* Name three distribution problems and explain how they cause trouble for distributed systems (understand) 

* Evaluate for three decentralized consensus protocols whether they effectively solve your names distribution problems (evaluate)


## Next chapter 
# BC-3.3.7.1 sExamples distribution problems & Different proposed solutions


Hopefully, you can answer these questions well & square by now: 

* What are distributed systems? 

* What are centralized and decentralized systems? 

* How do we reach a consensus in each? 

* What is the Byzantine General Problem? 

* What is the role of a blockchain protocol? 

* [Further reading 1]( https://medium.com/scalar-capital/on-consensus-e47920cd8914) 

* [Further reading 2](https://medium.com/s/story/lets-take-a-crack-at-understanding-distributed-consensus-dad23d0dc95)


## Examples distribution problems

**Scaling** 

Scale (& speed) versus Privacy (& Security) versus Decentralisation

Scalability & speed – to support the growth of the network

Privacy & Security – to preserve open access and confidentiality
Decentralization – uniformity of the system without a coordinating entity
It is a game of trade-offs. For example, Bitcoin versus Bitcoin Cash. Things can get headed! 

Spread nodes – unfair distribution

![Source]( https://bitfalls.com/wp-content/uploads/2017/11/01-4.png) 
![Source]( https://bitfalls.com/wp-content/uploads/2017/11/02-2.png)

Source

** Limited knowledge & dependencies**

Examples of limitations when talking about blockchain distribution:

* Technical complexity: not a lot of people know how to run nodes. 

* Nodes are increasingly getting bigger

* Blockchains are increasingly getting more complicated (specials) 

* Not cheap to run a node (hardware & electricity) 

* Manufacturing dependencies like, for example, ASIC of Bitcoin Core dependencies 

Nowadays, the above is not debated as much as the different proposed scaling solutions. Several layer two solutions like Arbitrum and Optimism have successfully launched, and new blockchains with other properties increase the options. 


## The two desired properties of "correctness" - Liveness & Safety

Distributed systems - be they blockchains or otherwise - have a concept of correctness. Correctness can be broken down into two parts: safety and liveness.

>💡 Liveness (availability)	= it will keep on producing live (new) blocks


 
>💡 Safety (consistency) 	= the produced blocks are consistent (immutable / secure)

In very general terms, Liveness could be considered the guarantee that something good will happen, eventually. The "eventually" is crucial because it means there's no bound on the time it takes for the good thing to happen. Making things a little more specific, in a distributed system, an example of liveness is the guarantee that a distributed computation will terminate = all transactions of honest nodes will ultimately be slowed down more thank blocks deep in a fair chain, so that a Denial of Service (DoS) attack against live active fair nodes will never be successful. 
In a consensus mechanism, liveness guarantees that all processes/ validators/actors/ whatever eventually agree on a value. To complete the picture, safety guarantees that nothing wrong will ever happen in a given system. In terms of consensus, this would mean that no two processes/validators/actors/whatever ever decide on different values. When a transaction is more than xxx blocks deep in the blockchain data structure of a fair node, it is included in the chain of every fair node with an overwhelming probability. 

## Grinding
Grinding = trying to influence the selection process of the block-creating entities. A violation of the liveness principle 


Other consensus variants

Deep dive in different POS-forms (f. e. dPOS, Leased POS)
Hybrid POW-POS forms
Proof of Resources
Proof of Burn
Pre-mined
Merged Mining
EOS Ourobouros
Hashgraph
Ripple 
IOTA – Directed Acyclic Graph
Hybrid blockchains 
Private blockchains 
Consortia blockchains 
Create your blockchain

