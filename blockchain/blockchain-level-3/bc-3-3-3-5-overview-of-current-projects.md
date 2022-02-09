# BC-3.3.3.5	Overview of current projects (optional!)

## Reality Keys
[Reality Keys]( https://www.realitykeys.com/) is a service that provides yes/no answers to a supported set of queries. It has been operating since January 2014 and is one of the first, if not the first, such service.

It supports queries about exchange rates (from Coindesk, Poloniex, and the European Central Bank), basic information about the blockchain state of few protocols (Bitcoin, Litecoin, Peercoin), and even supports queries against WikiData (a large, public, document-oriented database suitable for automated queries).

The service is free. Only the dispute resolution, which is done manually, needs to be paid about $10.

It works like this (either manually through their website or through an API):
1.	user submits a query, and the time of resolution
2.	Reality Keys prepares two key pairs: one pair for a YES answer and one for a NO answer. Both public keys are published.
3.	Reality Keys executes the query at the requested time, and only the private key to the corresponding answer is published.

Think of it as a part of a multi-sig transaction that releases the funds based on the query results.

## Realit.io
[Realit.io]( https://realit.io/) is a crowdsourced oracle for the Ethereum platform from the same creator as Reality Keys.

The process is simple yet powerful: you post a question, set the end date, send the reward funds and choose the arbitrator to solve potential disputes. Arbitration can be done in several ways, one of which is using human intervention.

It also features protection from front-running by using pre-commit schemes. The answers are submitted in a hashed form and only revealed later.

## Oraclize.it
„[Oraclize](HTTPS:www.oraclize.it) is a provably-honest oracle service“, running since November 2015. Their services are somewhat broader than that of Reality Keys. Still, Oraclize works quite differently: for example, integrated as an Ethereum contract. You need to call and provide a callback function where the results will be sent.

The current list of data sources contains a set of generics:
•	generic URL queries
•	WolframAlpha queries
•	various blockchain queries, like current block height, hash rate, balance
•	contents of files on IPFS
•	also containerized applications and scripts.

The service is not free (it is accessible on the testnet), so besides providing enough gas for transactions in both ways, you have to add a small call fee for the Oraclize service.

## Chainlink
SmartContract.com is a service of Secure Asset Exchange, Inc. that uses ChainLink middleware for providing oracle services. Its whitepaper was published in September 2017.
ChainLink aims to use many of the concepts we have discussed so far to create a decentralized oracle network. ChainLink has an interface for creating pre-defined/custom requests and can provide data from various sources to the Bitcoin and Ethereum blockchain.
It aggregates data from multiple oracle nodes and multiple data sources, and the client (user) can specify the details in a service level agreement (SLA) with the oracle provider, such as:
Specific query parameters
The number of oracles required to satisfy the security assumptions The reputation of the oracle nodes desired
Which aggregating contracts will be used
You can find the whitepaper at: https://link.smartcontract.com/whitepaper  

## A recipe for your oracle
If you are interested in creating your oracle, an excellent place to start is to study a nice little project on Ethereum called TinyOracle, made by Alex Beregszaszi in 2015.
Axis is a very active contributor to the Ethereum platform, from Solidity to eWASM, teeth, etc.
You will feel how requests to an oracle are handled by the code behind and then how the results of a query are transmitted back to the caller.
You can find it on GitHub: https://github.com/axic/tinyoracle

## Conclusions

•	We have come to understand one of the more exciting and fundamental issues with smart contracts, how their isolation makes them secure but cut off from other networks and the physical world. Oracles are serving as a bridge between smart contracts and data outside their network.

•	There are few oracle services running today, some more are planned for the near future, but their time has not come yet. However, once blockchain technology becomes widely accepted, oracles will be an integral and critical part of many use-cases.

•	The reputation of oracles will play a significant role, as they will compete in the market, and the premiums they will be able to extract will depend on their reputation score. With that, there is another issue of determining a trust model in a decentralized world with anonymous peers.
