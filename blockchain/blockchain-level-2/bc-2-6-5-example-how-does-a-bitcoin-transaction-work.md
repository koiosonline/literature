# BC-2.6.5 Example: how does a Bitcoin transaction work

## The high-level examples
Let's start this session with two high-overview visualizations. Please go over them in your own pace.

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image1.png)
[Source How does a Bitcoin Transaction Work]( https://www.zerohedge.com/news/2013-05-12/visualizing-how-bitcoin-transaction-works)

![Source](https://www.weusecoins.com/images/bitcoin-transaction-life-cycle-high-resolution.png)
[Source Bitcoin transaction life cycle](https://www.weusecoins.com/images/bitcoin-transaction-life-cycle-high-resolution.png)

## Unspent transaction output (UTXO)

At "verifying," the miners check whether the send transaction ("tx") is valid. The tx is valid when (among other things):

The sender of the public key proves he/she/it owns the private key (remember private-public key pairs?)
History has shown that the public key actually (1) received the tx in the past and (2) hasn't spent it.
 
When you receive a transaction, you receive a so-called unspent (u) transaction (tx) output (o) = UTXO. It is unspent because you still haven't spent it. It will become a spent transaction for the previous owner. A UTXO is, therefore, the equivalent of (a part of) bitcoin. It merely states the amount of spendable bitcoin.

So every block, new bitcoins are created ("born"). In the coinbase, the miner can send bitcoins to their account. The protocol/rules also state that the miner must wait for 100 blocks before spending the bitcoins. The first block, the genesis block, has therefore created the very first bitcoins. A "fun" fact (and possible challenge for the Bitcoin ecosystem): approximately 1.000.000 bitcoins are mined in the first 20.000 blocks. They are probably owned by the entity Satoshi. What's interesting about these bitcoins is that they still haven't moved since the beginning. They are still recorded as unspent transactions (UTXO's a.k.a. bitcoins).

## The step-by-step approach of bitcoin transaction (simplified)

**Step 1 **

A single unit transaction of bitcoins is born in the Coinbase of a freshly new block (so not "6.25 units of 1" bitcoin, but "1 unit of 6.25 bitcoins". Because the miner can't spend this transaction for 100 blocks and therefore still hasn't spent it, the transaction is an unspent transaction output of 12.5 bitcoins.

>💡 Spending bitcoin: sending an unspent transaction output to another address. Making the unspent transaction spent in your public key and unspent in the receiving public key. In the bitcoin protocol, the miners follow these unspent transactions output and monitor which public keys own which utxo's (bitcoins).


**Step 2**

After 100 blocks, the miner can send the transactions to another public key = "spending" the bitcoins, for example, to the public key of the energy supplier to pay for used energy in the real world.


**Step 3** *Scenario 1*

The energy cost for mining happens to be the same amount as the block reward of 6.26 bitcoin. The wallet takes one single unit of 6.25 bitcoins and sends it to one address: 6.25 to the public key of the energy supplier. The UTXO is recorded as "spent" for the miner's public key and as "unspent" for the key of the energy supplier.

Note: we ignore the fee in this example. Check out the live fee [here](https://www.txstreet.com).




**Step 3** *Scenario 2*

The cost of energy is five bitcoins. Here comes the trick: The miner still sends the entire transaction of 6.25 BTC. Remember the single unit in the computing definition from the previous lecture: you send either the entirety or nothing at all. The wallet software uses two receiving addresses. This time a return address for the change is added!

Output (1) for 5 BTC to the PK of the supplier,
Output (2) 1.25 BTC back to (often a new) PK of the miner (= [change]( https://www.youtube.com/watch?time_continue=4&v=BuUPKC6rFlE&feature=emb_logo) goes back to the miner).

So now the miner has 6.25 spent, and a new unspent transaction of 1.25 is recorded at its public key. So the supplier now has a new unspent transactions unit of 10.


**Step 4 The energy supplier**

The energy supplier can spend the 5 UTXO. So let's say they spend 4 UTXO to pay the manager, the wallet sends 5 UTXO. 4 PK manager and 2 PK back to their own wallet. So what remains is a new UTXO of 2, waiting to be spent.


** Step 4 The miner **

The miner can spend the 1.25 UTXO, let's say 1 UTXO, to the PK of the grocery store. So the wallet sends 1.25 UTXO to 1 UTXO in the PK of the grocery store and 0.125 UTXO to a return address.

##A more detailed recap

This is all very well described and explained in [this course]( https://www.youtube.com/watch?v=t3hJsFpPmXs) from Princeton. We highly recommend watching the entire course, but we can imagine that you might be drowning in information already.

## Wait for change
Because you need to wait for your change, you can only send one transaction output per block. After the block, you receive your change back and can spend the difference.
Your wallet can also combine multiple unspent transactions into one new transaction, creating a new unspent transaction for the receiving party. So let's say the miner has paid the energy supplier 12 times and receives 1.25 UTXO units back each time. The wallet can combine the UTXO's and send them to one public key. If you need to pass somebody 5 BTC, the wallet would take 4 x 1.25 UTXO and send 4 unspent to one public key.

## Hash pointers
A miner checks the transaction history using "hash pointers" (each transaction points towards the previous transaction). Every block, the miners update the state of the ledger: which public keys hold which UTXO's. Thus, the ledger only records these transactions and their entire history. The miners, therefore, follow the transaction outputs and not the accounts (public keys)!! `


> 💡 Bitcoin is called a transaction-based ledger system. The transaction itself is leading, not the account sending or receiving them. `

 

>💡 In the next session, you will see that Ethereum flips this concept. They use an account-based system, where the accounts are leading and not the transaction.


Nodes keep track of the UTXO's - a reference to a transaction received and not yet sent forward yourself. In that case, you have a transaction that has not yet been spent, an unspent transaction. Everyone on the network agrees that you (your public key) have received the transaction and that you have not yet spent it, and they are all in agreement about that (the SSOT). As soon as you spend this, = send the UTXO = the single data unit to another public key. The transaction is recorded as 'spent' for your public key and "unspent" for the following public key.

So, after creating a bitcoin in a block, you get a whole series of referrals, a sort of decentralized consensus of different nodes that agree on the history of the current unspent transactions.
So the Bitcoin blockchain is currently nothing more than a decentralized distributed ledger with 10.000 nodes all in consensus on what public keys hold what unspent transactions outputs. "And that's all" ☺

>💡 To summarize previous parts: keeping the blockchain is mainly keeping track of transactions that have not yet been issued (unspent transaction outputs = UTXOs).

 
 
>💡 A Bitcoin is a reference to a transaction received. If you do not yet publish it yourself, in that case, you have a transaction that has not yet been issued = a bitcoin is nothing more than a reference to the past where you received a transaction input from somebody else! Everyone on the network agrees that you (your public key) have received the transaction and have not yet issued it.


## Detailed explanation 1

There is a small part in the Coursera video where [they talk about the mechanics](https://youtu.be/t3hJsFpPmXs?t=908). We tried to summarize it for you.

I, as a sender, stop $ 10 with a unique transaction ID 123456789 in your public safe / key. Before I check the deposit in your safe miners, the $ 10, I do not know your vault's private code/key, so once in your public vault, I will never be able to access the money without your code. Only you as owner/receiver knows the combination safe & code and therefore can also be the only one with the money and passing on / issuing.

99.9% of the transactions concern the above scenario and are followed 1-on-1 by script. Two people are also involved in the script. Part 1 is for the recipient:
1. Take your private key (code safe) = <sig>
2. and open your public address (open the safe) = <pubKey>

Part 2 of the script has been given by me as a sender (security conditions):
3. I uniquely send $ 10 ID123456789 to your secure public safe so that only you can get it = OP_DUP OP_HASH160 = <pub key hash>.
4. As soon as you claim the money, I check whether you are in front of the good vault = does the vault number you now represent (<pub key hash?>) Match the vault number where I put the money (OP_EQUALVERIFY)
5. Enter the correct code = OP_CHECKSIG

How does the script know if you have entered the correct code? Only with the private code can you transfer the $ 10 bill and send it (see step 3). To be able to forward these, you can only send $ 10 ID 123456789. In other words: to be sent through, the money must be removed from the vault (= be stripped of the old public key / safe / lock). You cannot leave the safe closed and with lock and all forward to the next person with the statement "there is $ 10 123456789 in" because that does not allow the miners.

## The Nicosia Explanation
Another explanation from the [Nicosia Introduction MOOC]( https://www.unic.ac.cy/blockchain/free-mooc/):

![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image2.png)


![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image3.png)

## Detailed explanation 2
The blockchain is a chain of registered transactions in various blocks (database), where both the individual transactions (Tx) and the block (block header) are linked to previous blocks with hash pointers. The owner of a token refers to previous blocks that refer to the output of the unspent transaction (UTXO) towards their public address. When they forward the transaction, they are "spent" for their public address and therefore unspent for the next public address. Decentralized miners provide consensus on the validity of these transactions, where the order is essential to prevent double-spending. Upon approval, they present the new block to all nodes in the world.

But what does the transaction chain (blockchain) look like?
The transaction: https://www.youtube.com/watch?v=sKnsDjtXPsU
The Blockchain: https://www.youtube.com/watch?v=FrfY6xj0GFg

Visualization:
![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image4.png)

Also interesting is Matt Thomas blockchain sessions on YouTube: https://www.youtube.com/channel/UCbXiy1W_1HSMawmBDfo_TOA

## Detailed explanation 3 - the real deal and meta-data

So far, still no zeroes and ones (bits), and we mainly saw a human-readable front in Matt Thomas' example. Between the Matrix-style bits & bytes and the human-readable user-friendly front end is another phase of visualizing transactions. Readable for the techies, but not for the "noobs". This phase contains the input and outputs (which we explained) and a sort of "household/clean-up" data called the meta-data. The software uses the meta-data to compose transactions and give some properties, like, for example, the lock time that states how many blocks we need to wait before we can spend the transaction. Take a quick peek at these slides from the Princeton MOOC (if you can't follow but want to, watch the Princeton MOOC!). It is outside the scope of the course, but see if you can follow a bit. If not but interested, join their MOOC.


![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image5.png)
![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image6.png)
![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image7.png)
![Source](https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level2/bc-2-6-5-example-how-does-a-bitcoin-transaction-work-image8.png)


## Portfolio assignment 2.6.5 Example: how does a Bitcoin transaction work

Look up your own transaction from lesson week 4 in the blockchain of Bitcoin and trace it back at least five steps (so write the five previous public keys / owners of your current UTXO.

Make yourself a YouTube video of up to 5-10 minutes in which you explain how hash pointers work in transactions. Want to go the extra mile? Include an explanation of the Merkle tree in your answer!

## Further reading


* [Source How does a Bitcoin Transaction Work](https://www.zerohedge.com/news/2013-05-12/visualizing-how-bitcoin-transaction-works)
* [Source Bitcoin transaction life cycle](https://www.weusecoins.com/images/bitcoin-transaction-life-cycle-high-resolution.png)
* [Transaction street](https://www.txstreet.com)
* [Explanation bitcoin change]( https://www.youtube.com/watch?time_continue=4&v=BuUPKC6rFlE&feature=emb_logo)
* [Princeton MOOC]( https://www.youtube.com/watch?v=t3hJsFpPmXs)
* [Nicosia Introduction MOOC](https://www.unic.ac.cy/blockchain/free-mooc/)
* [The transaction Matt Thomas](https://www.youtube.com/watch?v=sKnsDjtXPsU)
* [The Blockchain Matt Thomas](https://www.youtube.com/watch?v=FrfY6xj0GFg)
