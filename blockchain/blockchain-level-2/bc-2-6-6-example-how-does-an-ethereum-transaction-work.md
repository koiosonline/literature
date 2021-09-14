# BC-2.6.6 Example: how does an Ethereum transaction work

## The first world computer

Ethereum can be seen as "the first world computer". With every transaction, every input, the computer recalculates its new "World State". It is a representation of a single source of truth. It shows all the accounts and the state that they are in, just as in double-accounting.

>💡 Where bitcoin resembles more single-entry accounting, Ethereum resembles double-entry accounting. Instead of transactions being in the lead, in Ethereum, the accounts are leading.

 
 
>💡 Ethereum / The Ethereum virtual machine (EVM) / "The first world computer" = nothing more than an overview of accounts and their current state.

Just as a double-entry accounting financial ledger states the financial status per account in a total overview, the World state of Ethereum states the status per public key in a total overview. Ethereum doesn't follow the state of transactions (which UTXO is, whereas in Bitcoin). Still, it tracks the state of each public key (holding transactions). This slight nuance makes all the difference! Why? That we will explain in this session 😊

## Account-based system

The accounts-based system = administration per account number ("Account"). Examples are a bank account number or a general ledger account. In short: Ethereum is account-based accounting, where the miners track the accounts and keep up the state of the accounts.


>💡 This seemingly minor tweak in accounting, from transaction-based in Bitcoin to account-based in Ethereum, makes a huge difference! In Ethereum, we record **the state of accounts** (= how the data looks like per public key) instead of the state of transactions (= where the unspent transaction outputs).

 

>💡 This enables Ethereum Virtual Machine to calculate and compose transactions that change in state WITHIN the account, not only between accounts. So where Bitcoin miners record changes BETWEEN accounts, Ethereum record changes BETWEEN and WITHIN accounts.


 
 
>💡 Within accounts = the data (value) is changed in the account (public key) without transferring data (value) to another account (public key). So the data only transfers/changes within the public key, made possible by the code that lets the data run a specific course (sounds familiar?). So once again, the ledger's state changes while no data is exchanged between accounts but within accounts.

A simplified example would be:
Person A owns $10. Person B owns $10. In Bitcoin, you can only send the $'s between the persons. In Ethereum, you also have an automated code ("smart contract") in which you, as person A or person B, can give input to move the $10 from your left pocket to your right pocket. So person A still has $10, person B still has $10, but person A moved the 10$ from the left pocket to the right pocket. This might seem like a minor change in accounting. Still, it enables an entirely new world of automated smart contracts 😊!

A smart contract can change the state of a public key, for example, move data from spot 1 (left pocket) to spot 2 (right pocket). In Ethereum, huge private numbers become public keys, and a set of code / a written smart contract can be hashed into a public key on its own. This way, you can update the ledger's state when a smart contract runs but doesn't send value (= move money between pockets).

Slight nuance: Bitcoin can make smart contracts in a smaller fashion—more about this in later courses.

>💡 Ethereum uses account-based accounting and can therefore transact within accounts instead of only between accounts. This enables the smart contract to execute without sending value but still changing the ledger's state because the account changes.

## Ethereum gimmicks

If you would like to learn more about transactions on Ethereum, we highly recommend [reading this source](https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369). We copied a few of the highlights for you.

**Accounts**

There are two types of accounts (where bitcoin as only one type of account, namely externally owned accounts)

![Source]( https://miro.medium.com/max/512/1*HIpgnjvHE9Jpb58icF5MgQ.png)
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)

Externally owned accounts. Which is controlled by private keys and has no code associated with them.
Contract accounts, which are controlled by their contract code and have code associated with them.

It's essential to understand the fundamental difference between externally owned accounts and contract accounts. An externally owned account can send messages to other externally owned or other contract accounts by creating and signing a transaction using its private key. Thus, a message between two externally owned accounts is simply a value transfer. But a message from an externally owned account to a contract account activates the contract account's code, allowing it to perform various actions (e.g., transfer tokens, write to internal storage, mint new tokens, perform some calculation, create new contracts, etc.).

Unlike externally owned accounts, contract accounts can't initiate new transactions on their own. Instead, contract accounts can only fire transactions in response to other transactions they have received (from an externally owned account or another contract account). We'll learn more about contract-to-contract calls in the "Transactions and Messages" section.


![Source]( https://miro.medium.com/max/512/1*I635Y9btMh667inOhDBQ_g.png)
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)



The account state consists of four components, which are present regardless of the type of account:

Nonce: If the account is externally owned, this number represents the number of transactions sent from the account's address. If the account is a contract account, the nonce is the number of contracts created.
Balance: The number of Wei owned by this address. There are 1e+18 Wei per Ether.
StorageRoot: A hash of a Merkle Patricia tree (we'll explain Merkle trees later on). This tree encodes the hash of the storage contents of this account and is empty by default.
CodeHash: The hash of this account's EVM (Ethereum Virtual Machine — more on this later) code. For contract accounts, this is the code that gets hashed and stored as the code has. For externally owned accounts, the codeHash field is the hash of the empty string.

![Source]( https://miro.medium.com/max/512/1*fYY7nqa6NZkDS4WSkXmQoQ.png)
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)

**Gas and fees**

![Source]( https://miro.medium.com/max/512/1*xSotR_QvCSKCF5C3APmIpA.png)
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)

![Source]( https://miro.medium.com/max/512/1*UNCaS12SsPln7DEnRvcONQ.png )
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)


The mining Fee is paid in GAS. Gas is the unit used to measure the fees required for a particular computation. Gas price is the amount of Ether you are willing to spend on every unit of gas and is measured in "gwei." "Wei" is the smallest unit of Ether, where 1⁰¹⁸ Wei represents 1 Ether. One gwei is 1,000,000,000 Wei. With every transaction, a sender sets a gas limit and gas price. The gas price and gas limit product represent the maximum amount of Wei that the sender is willing to pay for executing a transaction. For example, the sender sets the gas limit to 50,000 and a gas price to 20 gwei. This implies that the sender is willing to spend at most 50,000 x 20 gwei = 1,000,000,000,000,000 Wei = 0.001 Ether to execute that transaction.


![Source]( https://miro.medium.com/max/1920/1*M_hHF3ML8gx46pIU3kJV6A.png)
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)

Suppose the sender does not provide the necessary gas to execute the transaction. In that case, the transaction runs "out of gas" and is considered invalid. In this case, the transaction processing aborts, and any state changes that occurred are reversed. Thus, we end up back at the state of Ethereum before the transaction. Additionally, a record of the failed transaction shows what was attempted and where it failed. And since the machine already expended effort to run the calculations before running out of gas,  none of the gas is refunded to the sender.


![Source]( https://miro.medium.com/max/1920/1*BGZrZkYyRmLfehz3-Djv6w.png
)
[Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)

All the money spent on gas by the sender is sent to the "beneficiary" address, which is typically the miner's address. Since miners are expending the effort to run computations and validate transactions, miners receive the gas fee as a reward. Typically, the higher the gas price the sender is willing to pay, the greater the value the miner derives from the transaction. Thus, the more likely miners will be to select it. In this way, miners are free to choose which transactions they want to validate or ignore. To guide senders on what gas price to set, miners have the option of advertising the minimum gas price for which they will execute transactions.


[More information about current gas and fee prices Ethereum](https://ethgasstation.info/)

>💡 Transactions per block are not determined based on MB as with BTC but based on the quantity of gas. (Max gas per block](https://ethstats.net/)

** Gas **

Gas is the engine oil to run the transactions/contracts. The standard transaction needs 21,000 gas to execute itself, smart contracts more. GWEI is the fairy prize for miners. The higher the Gwei, the higher the fairy prize

[Explanation 1](https://www.youtube.com/watch?time_continue=1&v=nHgGQVmcmYs)

[Explanation 2](https://www.youtube.com/watch?time_continue=3&v=yFb2nuUUDX0)


If you want to know the nitty-gritty, please continue with [the article]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)!

## Portfolio assignment 2.6.6 Example: how does an Ethereum transaction work

Summarise these two articles in your own words and describe what you have learned from it:
https://medium.com/@permabullnino/bitcoin-an-accounting-revolution-40efcb903d7b
https://www.preethikasireddy.com/post/how-does-ethereum-work-anyway

## Further reading

* [Source how does Ethereum work anyway]( https://medium.com/@preethikasireddy/how-does-ethereum-work-anyway-22d1df506369)

