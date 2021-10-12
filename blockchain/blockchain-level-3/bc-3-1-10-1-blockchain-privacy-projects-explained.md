# BC-3.1.10.1 Introduction of blockchain privacy projects

We shouldn't be making the mistake of saying that we don't need increased privacy because we have nothing to hide. This is a slippery slope to saying we don't need free speech because we may have nothing to say or the equivalent of permanently removing the shutters/blinds from our house. Fungibility and privacy are important enough topics for the cryptocurrency community. However, it's a tricky problem involving complicated cryptographic schemes that are understood by few (so far) and are not very accessible to the average user without a practical way to hide the complexity.

•	[Privacy on the blockchain](https://hackernoon.com/privacy-on-the-blockchain-7549b50160ec)

•	[Snowden: Privacy and Bitcoin, at Bitcoin 2019 Conference](https://masterthecrypto.com/privacy-coins-anonymous-cryptocurrencies/)

## Monero

Monero was launched in April 2014 as a fork of Bytecoin. Bytecoin was an obscure cryptocurrency that, while having pioneered a novel way to achieve privacy, was plagued with a shady history and an unfair launch. As a result, the community forked the code of Bytecoin. It began a long, multi-year project of cleaning it up, documenting it, and getting the fundamental aspects right. As a result, Monero provides strong privacy by default while offering optional transparency, allowing its users to disclose their transactional history to selected parties selectively. Privacy is inherent to the protocol and requires no additional steps (interactivity) from the user. As a result, fungibility is greatly improved as well.
Monero's architecture provides a clear separation of the node functionality and the wallet. Originally having just a command-line wallet, which was deemed too difficult for non-technical users to use. 

In Bitcoin, transactions are traceable as the transaction graph is visible in the blockchain; sender and recipient addresses and transaction amounts are visible. Unfortunately, this makes Bitcoin vulnerable to coin tainting and susceptible to blockchain analysis, thus potentially significantly reducing its fungibility and usefulness as digital cash (which should be indiscernible from any other coin). Various techniques have been proposed and utilized to improve Bitcoin's privacy. However, they either suffer from trusting centralized services (coin mixers) of dubious quality and legal status or from requiring manual user intervention and coordination (such as CoinJoin).
Providing privacy and fungibility by default is considered a core principle of the Monero project. Therefore, Monero obscures the transaction graph and hides transaction amounts by a combination of Ring Signatures and Confidential Transactions, and hides user addresses via the use of Stealth Addresses.

Mobile & Light Wallets proposed by members of the community: 

[My Monero](https://mymonero.com/#/)

[Monerujo](https://monerujo.io/)

## Ring signatures and stealth addresses	
Monero originally used two techniques to make blockchain analysis difficult: Ring signatures and Stealth Addresses.
"A ring signature is a type of group signature that makes use of your [](https://getmonero.org/resources/moneropedia/account.html) keys, and several public keys (also known as outputs) pulled from the [](https://getmonero.org/resources/moneropedia/blockchain.html) using a triangular distribution method…In a "ring" of possible signers, all ring members are equal and valid. Thus, there is no way an outside observer can tell which of the possible signers in a signature group belongs to your account similar in function to a bank account, contains all of your sent and received transactions."
[Source:](https://getmonero.org/resources/moneropedia/ringsignatures.html)
Ring Signatures obfuscate the transaction graph by associating each transaction input to not just one but many possible and equiprobable outputs. This number of possible outputs is called the [](https://getmonero.org/resources/moneropedia/ring-size.html) of the transaction. This process is constant, and no manual user intervention is needed.
Monero also hides recipient addresses by using [Stealth Addresses]( https://getmonero.org/resources/moneropedia/stealthaddress.html). While the recipient can always give the same address to every sender, this address is used to generate a different, one-time address to use each time a transaction is made. Thus, the recipient's address never appears on the blockchain, and transactions are unlinkable, as nobody can prove that two transactions have the same recipient.
Originally, transaction amounts were visible in Monero's blockchain. However, in January 2017, a hard fork was performed that upgraded the Monero protocol to utilize a new scheme, [Ring Confidential Transactions]( https://lab.getmonero.org/pubs/MRL-0005.pdf), that combines Ring Signatures with Gregory Maxwell's "Confidential Transactions" scheme. Unfortunately, this evolution allowed the obfuscation of the transaction amounts, which means that Monero's blockchain is opaque.

## Monero & Satoshi
Here's an interesting [early discussion]( https://bitcointalk.org/index.php?topic=770.msg9074#msg9074 
) on the topic with Satoshi Nakamoto discussing the potential of Ring Signatures 
You can read more about it, and its features in more detail [here](https://getmonero.org/home)

## Z-Cash (zerocash) & ZK-snarks

Due to the limitations of Zerocoin, its original authors created an improved implementation called "Zerocash" (an Alt-coin). Zerocash addresses Zerocoin's performance and bloat issues and provides further functionality, such as Obfuscating payment history (e.g., payment destinations, amounts). 
 Zerocoin hides a payment's origin but not its destination or amount/ While some users may currently work around some of Bitcoin's privacy issues by employing multiple addresses for separate payments, transaction graph analyses are still possible.

The authors of Zerocash point out that Bitcoin currently exhibits the following privacy concerns: 

1.	It is less private than a traditional bank account (due to its public ledger)

2.	It makes your transaction history public for anyone to see (i.e., user identity can be deduced) 

3.	It introduces privacy-intrusion concerns (e.g., data mining by third parties, etc.)

[Understanding zero-knowledge blockchains](http://www.multichain.com/blog/2016/11/understanding-zero-knowledge-blockchains/)

## Z-Cash (zero cash) in detail
According to its protocol specification, Zerocash:
Creates an anonymous cryptocurrency called "zerocoins", whereby non-anonymous bitcoins
(referred to as "basecoins") are the base currency.
Dictates a different method of Bitcoin payment transaction assembly and verification. Extends Bitcoin with two new types of transactions:
Mint transactions – used to convert non-anonymous existing bitcoins from a bitcoin address to
the equivalent zero coins which will belong to a specified Zerocash address.
Pour transactions enable anonymous/private payments by consuming existing user coins to produce new coins, using [zero-knowledge proofs]( https://en.wikipedia.org/wiki/Zero-knowledge_proof)
The basis of Mint transactions is a "[cryptographic commitment]( https://en.wikipedia.org/wiki/Commitment_scheme)" (see next slide) to a new coin, which is itself generated using the SHA-256 hash function. This commitment is based on the coin's value, a unique serial number, and the owner's address. While value and address remain hidden by the commitment, any user can later demonstrate ownership through its de-committed values.

## Z-Cash (zero cash) in detail
A "cryptographic commitment" is a binding scheme enabling one party to commit to a value or statement while keeping it a secret from any other parties. The original party can reveal (or de-commit from) the committed value, which another party can verify. Thus, a commitment scheme consists of two phases: 
Commit phase – whereby a party commits to a value that is unknown to any other parties
Reveal phase – whereby the value is revealed and verified
An example of such a commitment would be:
Alice claims to Bob that she can predict next week's winning lottery numbers.
Alice commits by writing the winning numbers on a piece of paper, locking the paper in a safety box, and giving the box to Bob for safekeeping (Commit phase).
Finally, next week, Alice gives Bob the key to the safety box so that Bob can verify that Alice's prediction was indeed correct (Reveal phase).
Zerocoin and Zerocash apply these principles in Mint transactions

## "Zero-knowledge proofs." 
"Zero-knowledge proofs" allow one party (e.g., the sender) to prove to another (e.g., the receiver) that a given statement is true while not providing any further information beyond the fact that the statement is true. For performance reasons, Zerocash uses so-called "zero-knowledge Succinct Non-interactive Arguments of Knowledge" (or zk-SNARK), which are mathematical proofs that are short and easy to verify (it only takes milliseconds). 
Zerocoin and Zerocash apply these principles in Pour transactions. In addition, zerocoin developer team and [](https://eprint.iacr.org/2013/879.pdf) have moved to work on a cryptocurrency named Zcash, aiming to solve fungibility issues in cryptocurrencies.

**A pour transaction allows:**
●	A user to show ownership of input coins
●	These input coins appear in previous mint transactions or as output coins of some previous pour transaction Indication that the input coins' total value equals the output coins' total value.
The pour transaction reveals the serial numbers of input coins. Still, it hides the values of the input/output coins and the addresses of their owners. It can optionally be used to convert zerocoins back into non-anonymous bitcoins (basecoins) or to pay transaction fees.

●	[Extra source demonstrate how zero-knowledge proof works](https://www.linkedin.com/pulse/demonstrate-how-zero-knowledge-proofs-work-without-using-chalkias/)

●	[Vitalik Buterin, ZK-snarks under the hood](https://medium.com/@VitalikButerin/zk-snarks-under-the-hood-b33151a013f6)

●	[How Ethereum can scale with Snarks](https://tokeneconomy.co/how-ethereum-can-scale-with-snarks-101-5b06ff048bb7)


