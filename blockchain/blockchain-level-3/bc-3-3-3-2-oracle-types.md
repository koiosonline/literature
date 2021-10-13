# BC-3.3.3.2 Smart contracts & external data: oracle types

A bit simplified, we can view oracles as programmable agents with three possibilities of where the data comes from (of course they all use some kind of software at a certain point, here let’s focus on the very source of the data feed):
software oracles (application data feeds)
hardware oracles (data from physical devices, for example from the Internet-of-Things network)
human oracles (prediction markets)
The data that an oracle can provide is limited only by the capabilities of a particular black box, and can be anything from the data in another blockchain, stock market prices or sport results, to GPS coordinates of a device, or sensor data in an autonomous vehicle. It can be said that the really exciting things with smart contracts are those that are linked to the real life and for that we need „good“ oracles!

## Identity?
With smart contracts unable to fetch the outside data for themselves, data providers are required and they need to earn and preserve the trust users have in them. They can do so in various ways:
by proving their integrity – which could be done by attaching some kind of proof, that the data-feed is genuine and not tampered with; this is a little less difficult with software oracles (because of the existing methods to check the integrity of code and digitally signing the data), harder with hardware oracles (still, there are so called „trusted environments“ that can be used), but almost impossible with human oracles („wetware“)
participating in a pool of oracles – where a majority of oracles needs to agree on the result set and bad providers are voted off or possibly punished in another way, like not getting paid or losing their security deposits. With multiple oracles, the request cost rises also.
by having an already well-established reputation in the real world – can be disputed ex post, for instance, suppose that Bloomberg and Reuters will someday act as an oracle to Ethereum smart contracts. In some cases, they will probably be trusted a priori, with probable cross-checks to be sure.

## Automated oracles
Since smart contracts are limited to the blockchain they are running on, anything beyond that must be processed off-chain. Delegating this load can be done in various ways: you can run such a service right beside your blockchain node and somehow reacting to on-chain events, or you can „outsource“ this task either to an app-hosting provider, to a pool of oracles, or send it for processing „in the cloud“ with tighter coupling to the blockchain.
Let‘s describe these options through some of currently known proposals.

**Oracle** – a contract that is trusted to provide data in a reliable and honest manner. You send a query to it and trust it that it will respond in the expected timeframe with correct data (you trust that the oracle will execute the query honestly, without altering the data). Such an oracle could also be your own traditional non-blockchain application, but then it wouldn‘t be a dApp J. There are some interesting ways that third-party oracle providers can prove their honesty, which we will examine a bit later.

** “Smart Oracle” (contract host) **– a contract that includes the code for off-chain execution, which the contract owner/author/developer and end-user all agree upon, and is executed at a service-hosting provider. Basically, you package your arbitrarily complex, untrusted code to be executed at any third- party provider (decentralization could be preserved by the formation of a market of providers). It must be executed by the smart oracle in an isolated environment as it may be malicious even to the provider.


** “Introspection Oracle” (I/Oracle) ** – a pair of contracts where the first contract accepts generalized requests, which are then executed inside an isolated and specialized machine (unikernel), and the second contract to store the result of execution. The idea behind advanced I/Oracles is to make the untrusted code be run with bare minimum (unikernels don‘t even need an operating system underneath, they are not virtual, but are self-contained), and at the same time be „close“ to the blockchain, see the chart here from Loyyal. *Loyyal is no longer exploring the idea, but the original author Shannon Code is still working in this direction.

** Non-social oracles (software/hardware oracles) ** are thus solving the constraints of smart contracts by providing them with data they need via black-box execution of some code.Requirements of such black boxes:verifiable code (openly available for participants to inspect, it is signed so can’t be altered) secure execution of this code reliable hosting. 

By considering all that, we can now better understand the capabilities that oracle services companies are offering or will offer in the future. For instance, Microsoft Cryptlets (a.k.a. “enterprise smart contracts”) have a whole protocol just for the registration of oracles, with verification of trusted signatures, discovery mechanisms and code execution in secure enclaves of Intel SGX chips available through the use of their Azure cloud etc.

[An example of automated oracle coffee measuring machine](https://www.youtube.com/watch?v=Z4SwLD4frlo)

