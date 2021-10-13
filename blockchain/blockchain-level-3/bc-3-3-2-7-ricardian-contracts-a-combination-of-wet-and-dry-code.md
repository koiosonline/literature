# BC-3.3.2.7 Ricardian Contracts: a combination of wet & dry code


“Smart contracts have been dubbed the killer application of blockchain technology. They may seem revolutionary, but smart contracts are nothing new and have been around for a long time. For example, smart contracts are already in place in most modern office buildings. For example, access cards that determine whether you are allowed entry to a certain area are pre-defined by a piece of code and linked to a database.
However, there is one problem with existing smart contracts, which is that they are not legally binding. As a result, in 2018, there has been a renewed interest in Ricardian Contracts. These types of contracts differ from smart contracts that they are legally binding, and it records the agreement between multiple parties in a human-readable and machine-readable text (contrary to smart contracts, which only executes what is defined in an agreement). This means that it is a legal contract that is easy to read and understand by everyone, so not only your lawyer. 
Ricardian contracts use cryptographic signatures for legal agreements. If there is a dispute among parties involved, the case can be decided in court, which is not the case with smart contracts. Once a human-readable agreement is turned into a machine-readable agreement, it can be hashed. The hash is then stored on a blockchain. As a result, each part of the document can be uniquely identified by its hash and it becomes impossible to change the original agreement without the other parties knowing. Ricardian contracts are, therefore, extremely secure. We can expect to see a lot more applications benefitting from Ricardian contracts. [Source]( https://vanrijmenam.nl/five-blockchain-trends-consider-this-year/)


![Source]( https://i0.wp.com/vanrijmenam.nl/wp-content/uploads/Ricardian-contracts-web.png?w=903&ssl=1)
[Source]( https://vanrijmenam.nl/five-blockchain-trends-consider-this-year/)



>💡 "A Ricardian contract places the defining elements of a legal agreement in a format that can be expressed and executed in software. The key is to make the format both machine readable such that they can easily be extracted for computational purposes, and readable as an ordinary prose document such that lawyers and contracting parties may read the essentials of the contract without undue inconvenience." – Ian Grigg

## Use cases 

Ricardian contracts are implemented in a number of systems, some of them are:

* Designed in the 1990s by Ian Grigg from company Systemics.
* Used in Open Transactions contracts, built by Chris Odom, since 2010
* Used in Open Bazaar for forming trades of bids and offers, since 2014
* And finally, in 2016, announced to be used in Corda as a legitimizing lever to smart contracts

## Technical definition 

>💡 With respect to smart contracts, **Ricardian triple** is defined as: **{ Prose, Parameters, Code }**

Parameters: instantiate a particular case of a smart contract template, with the help of hashed code and legal prose (authentication) and digital signatures (proof of agreement).
Code: expressed in plain text (source code), not compiled, so is independent of actual deployment 
Prose: expressed as human-readable, structured legal text
Code and prose are to be semantically equivalent. The former is used for automated execution of smart contracts, while the latter serves as legitimizing the agreement. 
Note: Ricardian contract is a good fit for triple entry accounting (credits + debits + cryptographic proofs (receipts) that these transactions occurred).

Keeping Ricardian contracts in mind (code + prose + parameters), we can define smart (legal) contract as automatically executable contract code, which has capabilities of being legally enforced. Compared to Ethereum, Ricardian triple gives users priority over programs: „smart code“ is not „smart contract“ by itself – smart contract must be human-readable and must live as much in a real human world as it lives in a digital one.

When thinking about contracts, we must take into account law & regulatory compliance and the whole lifecycle of a contract, including amendments and testing them in court. These are predispositions of what the firm R3 is building with Corda. Corda is patent-pending distributed ledger technological fabric, a part of a wider R3‘s vision named Concord (from Latin concordia, which means agreement), though at least as of 2018, R3 is solely focused on Corda.



## Further readings: 

* [Code is law / code is not law]( https://medium.com/cryptolawreview/cryptolaw-9410cf7a8fd4 ) 

* 
[Against smart contracts]( https://medium.com/cryptolawreview/against-smart-contracts-4a1f43133215)

