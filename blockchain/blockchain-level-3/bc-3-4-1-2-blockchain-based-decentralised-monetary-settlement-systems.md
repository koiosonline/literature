# BC-3.4.1.2 Settlement in digital currencies - Bitcoin as an RTGS?

## Real-Time
Bitcoin transactions are verified for validity and propagate through the network’s nodes globally in roughly 2 seconds. They are not immediately irreversible, however. As they appear in more and more blocks (approximately ten minutes), they become more irreversible. They are considered ‘confirmed’ for most high value uses within an hour

## Gross
Transactions are **not netted (!)** with others, but they are settled on an individual basis when transacting within the protocol. Not only that, but the inputs of a transaction must be the outputs of a previous transaction, meaning that no netting ever takes place, and full clients verify each transaction back to the Genesis block. It is, as you have learned in level 1, not “debt-based” money. 

## Settlement
Settlement on the blockchain is final and increasingly irrevocable the more blocks are added on the blockchain. Thus, funds are immediately available after the transaction is confirmed (in some cases, even before). An exception is newly mined coins which must “mature” for 100 blocks.

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-2-blockchain-based-decentralised-monetary-settlement-systems-image1.png)
[Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-2-blockchain-based-decentralised-monetary-settlement-systems-image1.png)


Most organizations are not good at developing new products (or services or ventures). So, if we assume Bitcoin is an RTGS, what are the significant advantages/disadvantages relative to traditional RTGS?

**Advantages**

* Globally accessible. Without authorization, any person on the planet can access this RTGS vs. the vetted financial institutions (usually national) that are allowed to participate in an RTGS. This would seem to eliminate the need for correspondent relationships to access and RTGS
* Operates on a 24/7/365
* Programmable for more complex cases than simple settlement

**Disadvantages**

* Somewhat slower settlement times
* Native currency unit not in widespread real economy use so far

## Settlement in digital currencies – Bitcoin and Net Settlement Systems	
Net settlement systems exist in a world of gross settlement systems primarily for cost/ efficiency savings for lower priority payments:
* Lower liquidity needs (over a day) 
* Fewer transactions (and therefore transaction fees)

It seems conceivable that the exact needs would emerge in a Bitcoin-centric economy. E.g., two firms that trade with each other daily may not want to tie up BTC for hour-long intervals for each transaction but instead aggregate at the end of the day. 

<blockquote style="border-color: #ff0bac">❓ Is there a net settlement system in the Bitcoin ecosystem? If not, what would a future system of this type look like?</blockquote>


When two customers share the same financial institution, settlements are typically done on an internal basis. E.g., when Bob at XYZ transfers money to Alice at XYZ Advantages of this model are faster transaction times and no fees. This seems to have a direct parallel in the extensive online hosted wallet companies. E.g., When you transfer a Bitcoin balance from one Binance (or CoinBase) account to another, there is no Blockchain transaction occurring. It is only a simultaneous entry on the firm’s internal ledger (“off-chain”). 

<blockquote style="border-color: #ff0bac">❓ Are there other areas where internal settlement systems will emerge? Where do so-called 2nd layer networks (like the Lightning Network) fall in this regard, and are they more of a clearing than a settlement network? (more on the Lightning Network and Atomic Swaps later)
</blockquote>

## Settlement in digital currencies – Bitcoin and settlement for Other Settlement Systems	
Existing RTGS often serve as the ultimate settlement mechanism for other settlement systems
For example, let’s say we are operating a securities settlement system. Firm A had a net balance with Firm B. They could settle via their Fedwire. This seems like an area with tremendous possibilities for Bitcoin. It could provide ultimate global settlement for settlement systems of any kind worldwide.

<blockquote style="border-color: #ff0bac">❓ What types of systems could settle on Bitcoin? Be creative and expansive. </blockquote>

