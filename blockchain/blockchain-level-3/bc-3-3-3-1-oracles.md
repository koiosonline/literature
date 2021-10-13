# BC-3.3.3.1 Oracles 


## About this chapter?
Blockchains are digital ledgers that communicate via smart contracts with the online realm as well as the offline meatworld. The old credo “garbage in = garbage out” is becoming even more important in an immutable ledger, so we need good check-points on these moments of input. These bridges between online/offline worlds with input and the blockchain itself, are called oracles, and the problem of untrustworthy input is known as the oracle problem. So let´s talk about Oracles, their role, their problem and possible solutions out there. 

## What will we discuss? 

BC-3.3.3.1 Oracles

BC-3.3.3.2 Oracle types

BC-3.3.3.3 Socially driven oracles

BC-3.3.3.4 Incentives for oracles

BC-3.3.3.5 Overview of different projects working on implementations


## After this class, I can:
* Explain what the role of an Oracle is (understand)

* Describe the different types of Oracles (understand)

* Describe what the Oracle problem is (understand)

* Evaluate the effectiveness and limitations of different solutions for the Oracle problem (evaluate)


## Next chapter
# Oracles
![source]( https://academy.horizen.io/assets/post_files/technology/advanced/1.3-smart-contracts/oracle_D.jpg)
[Role oracle, Source]( https://academy.horizen.io/technology/advanced/summary/)

*What is the problem with smart contracts accessing the data outside the blockchain? *

(Public) Blockchain systems need to reach the same agreement on every node, no matter the environment of the node, its operating system and programs running besides it. Since all nodes must at all times, under same inputs, come to the same agreement, the execution environment of smart contracts must be deterministic (deterministic ≡ gives the same output for the same set of inputs). For example querying the data providers that are outside of the network, like communicating with Bloomberg API-s, would not necessarily return the same results to all nodes (perhaps due to different access rights, issues with the availability of the service etc.), therefore their code execution would not be in sync and nodes would have conflicting states.
In private blockchain settings, validating nodes could agree to a less restricted execution of contracts (because nodes are known, dispute resolution would be easier), but the risks of possible loopholes are making it practically impossible at this moment.

Hence, the execution environments, such as the EVM in Ethereum, have strict limitations: they are completely isolated and sandboxed, they can't access node's hardware, file system, full array of network protocols etc.

>💡 This brings us to the simple fact: the only world a smart contract sees, are other contracts and the transactions coming towards it.

In other words, all the data a certain contract X needs, must come from the blockchain – from another contract. Let’s call this contract O. Therefore O serves as a data source and
„someone“ or „something“ must set its state to hold the required data. This is the task of oracles.
Whatever data a smart contract requires from the outside of its network, it asks an oracle to provide it.

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-3-3-1-oracles-image1.png)
[Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-3-3-1-oracles-image1.png)


In ancient Greek religions, oracles were considered to speak about predictions or precognitions of the future, so in that sense we might limit the definition of an oracle to prediction markets. But smart contracts can just as productively use more real-time data feeds (keep in mind that real-time is not instant, because contract‘s state only changes when transaction block gets mined/validated).
In computer science, however, an oracle machine is a Turing computer connected to a black box that makes single-step decisions about a particular problem (basically, gives a solution to a query).

With regard to smart contracts, the process works like this:

* A contract X, that needs some external data, sends a request (i.e. a transaction) to the contract O, which will expectedly come up with the desired data in due time.

* An off-chain external application (a black box to the contract) monitors transactions to O and when it detects a new one, it parses the request, calculates the answer and sends a response (i.e. makes a transaction) to the contract X‘s callback function.

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-3-3-1-oracles-image2.png)
[Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-3-3-1-oracles-image2.png)

 

