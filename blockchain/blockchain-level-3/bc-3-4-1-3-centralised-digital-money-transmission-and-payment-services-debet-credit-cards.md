# BC-3.4.1.3 Centralised digital money transmission and payment services (debit & credit cards)

So what remains are the small micro-transactions we regularly do daily. These are generally done via debit- or credit cards. 

**Charge Card:** A card where the balance must be paid off by the end of the month. This card is equivalent to a very short-term line of credit (between 1-30 days).

**Credit Card:** A card where the customer is extended a revolving line of credit of some or all might be paid back at the end of the month: 
“Revolver”: A credit card customer who carries balances from month to month, paying them off over time and accruing interest charges
“Transactor”: A credit card customer who pays their balance monthly and does not accrue interest charges

**Debit Card:** A card that pays from the funds in a checking or savings account

** Prepaid cards:** Cards funded out of a pre-filled/pre-paid cash account (that does not have general checking account privileges)


>💡Realize that all cards are payment processing cards but only charge, and credit cards also offer lending options.

## Credit cards 
“Credit” cards emerged in the 19th and early 20th century in the United States on a merchant-specific basis. A customer would present an identifying paper to a clerk establishing him or herself as a creditworthy customer to whom the merchant would extend credit. Merchants felt this convenient form of payment would cement loyalty and increase sales.

>💡 Diner’s Club was the first general-purpose charge card founded in 1950 by Frank McNamara. It focused on high-end entertainment and travel. Their initial fees were 7% of each transaction charged to the merchant.
Four major credit card networks emerged after Diner’s Club. American Express launched a charge card business in 1957 (AmEx had an existing money order business). They did not launch their first credit card until 1987. Bank of America launched BankAmericard in 1958. In time, and after many iterations, BankAmericard eventually became the consortium now known as Visa. Wells Fargo and three other banks launched Master Charge / the Interbank card in 1966. In time, and after many iterations, Master Charge became the consortium now known as MasterCard. Sears launched Discover Card in 1985 (Sears owned the Dean Witter brokerage at the time). Other notable networks include JCB (Japan) and UnionPay (the domestic ‘switch’ monopoly in China).

 
 
>💡 It took credit cards multiple decades to get globally adopted. 
Visa/MasterCard neither lend nor acquire merchants directly: 

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-3-centralised-digital-money-transmission-and-payment-services-debet-credit-cards-image1.png)
[Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-3-centralised-digital-money-transmission-and-payment-services-debet-credit-cards-image1.png)

## But why such a complex 5-party+ system?	
The objective of this complex system is simple: achieving operational scale in three different dimensions

**1. Network Effects **

Operating as a network of banks (unified by a scheme) rather than each bank having its payment scheme makes the system more valuable for consumers and merchants and is a dominant strategy vs. single bank only payment systems.

* Consumers prefer cards with broad merchant acceptance
* Merchants prefer payment systems with broad consumer usage


**2. Operational Leverage**

Independently, separating the scheme from the card issuance (consumer acquiring) and merchant acquiring allows the schemes to leverage the brands, distribution, marketing, and geographic reach of tens of thousands of banks worldwide in end-customer acquisition (consumers, merchants)


**3. Credit Risk Management**

Both issuers and merchant acquirers (banks in both cases) are ultimately responsible for their customers (consumers/merchants). This allows the payment scheme only to manage the creditworthiness of a small set of regulated, general creditworthy institutions (banks) rather than hundreds of millions of individual consumers and businesses. 



## Authorization
This is what the consumer feels is the ‘payment’, but is just an initial authorization
A merchant submits transaction details to their merchant bank (who has likely outsourced the processing to a payment processor). The payment processor submits it to the switch operator (Visa/MasterCard/etc.), which then submits it to the issuing bank for approval
In most cases, this takes 5-15 seconds and happens approximately 182 billion times / year1 (nearly 6,000 times a second) (Source: Nilson Report, Chart of Month, 2015).

## Clearing
Once a day for most merchants, a batch of transactions is uploaded to the payment system operator and, after being processed, sent to the acquiring and issuing banks. This non-monetary exchange of data is used to verify transactions, update customer records, and so on


## Settlement
Within two days, net settlement amounts are calculated by the system operator for issuing and acquiring banks. Settlement usually occurs through FedWire but sometimes via ACH or wire transfers. 
Once the bank receives the payments, individual merchant/consumer accounts are credited/debited
Note that from the merchant’s perspective, even this settlement might not be final for weeks or months as consumers have the right to request a chargeback in limited circumstances. In those cases, the system operator adjudicates the dispute, and transactions may be reversed.

>💡 Though they vary greatly, total fees to merchants are in the 1.5-3% range. 

## The following parties levy fees as part of a credit card payment system


** Issuing Bank **
The interchange fee typically goes to the issuing bank. This fee ranges from 1.5% to 2.5%, plus a minimum value of $0.20 or $0.30 in the United States. In aggregate, it averages about 1.5%.
Note also that the issuing bank also generates profits from the lending component of the card
Profits from lending are Net Interest Margin (interest charges less Cost of capital), fewer defaults less servicing fees

By a wide margin, the most profitable customers for a credit card issuer are those who ‘revolve’ (keep a balance) but don’t default. ‘Transactors’ are only profitable if they are high volume spenders
Interchange fees are hugely complex. This is a representative example of the US Interchange fees for [VISA]( https://usa.visa.com/dam/VCOM/download/merchants/Visa-USA-Interchange-Reimbursement-Fees-2015-April-18.pdf)

**Acquiring Bank / Processor**
Fees for the acquiring bank are lower, on average, in the $0.20-$0.30 per transaction range
There are typically additional fees for payment gateways and other specialized processing

**Network Operator**
Visa/MasterCard charge low fees for themselves (~0.11%) but charge them on every transaction

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-3-centralised-digital-money-transmission-and-payment-services-debet-credit-cards-image2.png)
[Source: Goldman Sachs on Bitcoin.]( http://www.paymentlawadvisor.com/files/2014/01/GoldmanSachs-Bit-Coin.pdf)


**Merchants**

All these fees are paid, in aggregate, by the merchant through their “merchant discount rate,” or the difference between how much they billed the customer and how much they ultimately received once all the fees are paid.
Fees are higher for ‘card not present businesses on average (such as online businesses where the merchant does not physically see the card)

## Hidden costs 

Credit card companies have done an excellent job of ‘hiding’ their costs from consumers: 

* Receive ‘rewards’ like points, miles, or cashback

* Are largely or fully protected against fraud in most countries

* It makes cards appear like a cost-free choice – no risk plus extra benefits vs. using cash

This system works because the costs are embedded on the merchant site and socialized across all customers (regardless of payment type)

**Merchants are less better off, though:**

* Have to pay 1.5-3% per transaction

* 1.5% - 3% is a huge figure when looked at relative to profits instead of revenue.

* Healthy companies might achieve a 10% margin. Competitive industries might have 5% or lower.

>💡 In that light, 1.5-3% is 15-50% of a merchant’s net income which seems surprising for an electronic transaction (!!!)

>💡 These costs are ultimately embedded in product prices, so the consumer does ‘pay’ for them in the end
Until recently, merchants could not surcharge in the US for credit card usage, meaning there was no discount for using cash/checks/etc. In this model, cash purchasers effectively subsidized credit card purchasers. Even though surcharges are now legal, many merchants do not use them yet

## Visa/MasterCard have faced a practically non-stop set of antitrust lawsuits

* 1996: (United States): Visa/MasterCard lost a merchant class action suit re price-fixing. Settled for $3B

* 1998-2007 (United States): Visa/MasterCard lost case relating to the prohibition of its issuing banks from doing business with American Express and Discover; paid damages to American Express of $2.2B

* 2010 (EU): Reduction of debit card fees

* 2007-2014 (EU): Antitrust lawsuit against Visa/MasterCard, culminating in caps on interchange fees in EU (0.30% on credit cards, 0.20% or 7 cents (whichever is lower) on debit cards)

* 2010 (United States): Justice Department v. Visa/MasterCard. The ruling allows merchants to opt-out of certain cards and offers discounts for using cheaper cards

* 2011 (United States): Dodd-Frank Act limits debit card interchange revenue to $0.21. Retailers are still upset. “The first 20-odd cents of every transaction will go to the financial services industry, and that’s not such a problem if you’re selling computers or wide-screen TVs or digital cameras,” Lane said. “It’s a huge problem when you’re selling newspapers and coffee and donuts and candy bars.” – Spokesperson for Retail Industry Leaders Association


* 2012-present (United States): Class action lawsuit relating to price-fixing on the setting of interchange fees (and discouraging merchants from promoting other payment methods). A judge ordered a $7B settlement, but most large merchants have opted out of the settlement and are still pursuing this through private lawsuits

* And many other regulators or civil actions across multiple jurisdictions
Poor behavior by the networks/banks or inevitable outcome of a global oligopoly?


## And what about the debit cards? 

PIN-based Debit cards have their own set of EFT (electronic fund transfer networks) for PIN-based transactions at ATM networks and at point-of-sale terminals. These networks were initially developed for ATM withdrawals in the ‘70s and ‘80s. These networks are “single message”. A single message handles authorization, clearing, and settlement, and the user’s account is debited immediately. 

## Why do these networks settle instantly? 
Because they were designed for ATMs that release cash and cash is the original real-time gross settlement system. The consumer side is irrevocable (the consumer is holding the cash), so the transaction has to be debited on the bankside instantly. In the 1980s, supermarkets started including ATMs on-premises. They then started experimenting with accepting PIN debit at the point of sale. However, it took years for standards to be finalized and for regulatory clarity (at first, there were questions about whether an ATM was a ‘branch’ and therefore subject to bank regulation. Note that the current structure of the debit card industry is largely similar to the 5-party structure in cards with merchants, consumers, merchant acquirers, issuing banks, and network operators. It is interesting that EFT networks started with a completely different purpose/scope than credit card networks but, over decades, developed similar coverage and characteristics. 

The EFTs started as regional networks (Star, NYCE, etc.) as banks realized the benefits of having networks of ATMs available to their customers. Over time the EFT networks in the United States consolidated. There are 12 PIN networks, of which 5 have 90%+ aggregate market share. Each of Visa (Interlink), MasterCard (Maestro), and Discover also own one of the PIN networks. Visa, MasterCard, and Discover also provide ‘signature’ based debit over their credit card network that settles in 2-3 days like credit cards do. Before Dodd-Frank, they aimed to move consumers to the signature-based debit because they charged higher interchange fees. The Dodd-Frank Act brought significant changes to EFT networks:
Applied caps to PIN-based debit card interchange fees (except for small banks), capping charges at $0.21
Prevented network exclusivity arrangements (that tied signature networks to PIN networks)
Prohibited routing restrictions on merchants (on which network to choose)

## Impact debit vs. Credit Cards	

For merchants:

* Debit cards are significantly less expensive for merchants to process, and they also settle faster

* Merchants still feel that debit cards are too expensive for small transactions

* Merchants would prefer that consumers would use debit cards

* Overall, debit cards are less profitable for banks than credit cards

* Lower interchange fees for transactions

* No lending component

After Dodd-Frank reduced the fees in debit cards, banks:

* Cut back debit card reward programs

* Marketed debit cards less aggressively and are not pushing consumers to use them

* Have publicly floated the concept of charging consumers to use their debit cards

## Pull vs. Push Payments	

A credit card or bank transfer authorization is a “pull” authorization. The payor is giving the payee authority to pull payments from their cash or credit account without further authorization. This is true for both individual transactions and recurring transactions
While an accepted and normal part of everyday life, it is rather staggering if one thinks about it too carefully. A large array of parties may potentially have access to this information, including the merchant, the acquirer, the payment processor, the gateway, the network, and all of its employees, contractors, and vendors.
And, in practice, there have been many breaches at the merchant level. The Target data breach of 70M records was particularly notable: http://krebsonsecurity.com/2014/05/the-target-breach-by-the-numbers/ 

## Push transactions like cash, Bitcoin, m-Pesa, etc., work oppositely. 
The payer is ‘pushing’ a certain amount of money to the payee but not giving the payee open access to their account. This theoretically is a less risky model for both payers (limits exposure to the number of payments) and payees (money good settlement). 

## Credit card security 

The initial security architecture and outcome of BankAmericard was shambolic, made the consumer responsible for fraud, and almost ended the whole project. Over time, the credit card industry has developed a wide range of measures to improve security. Some of the more notable ones are: formation of PCI-SSC (Payments Card Industry Security Standards Council), a consortium of Visa, MasterCard, American Express, Discover, and JCB to develop a joint set of standards for data security
PCI developed the PCI-DSS (Data Security Standard), which is a set of network, encryption, and control measures to protect card-member data for all parties involved with stiff penalties for merchants and processors who fail to uphold them: 

* Common blacklists of suspicious merchants
* Neural networks and other software to flag questionable transactions
The fact that transactions are reversible, so merchants have no incentive to try to cheat the system

Upcoming technology improvements include:
* Chip and PIN (common in Europe, uncommon in the United States) as embodied in the EMV (Europay, MasterCard, Visa) global standard
* Tokenization (which is potentially more useful for securing online transactions than Chip and PIN)

Though the above is a patchwork system, the net effect is a relatively low fraud rate given a global ‘pull’ network. However, the greatest innovation has been repaying the consumer and absorbing the costs at the network/merchant level. This has provided a huge boost in adoption, particularly in the area of online where credit card usage was stalled for years due to fraud concerns


>💡 Push payments theoretically are more secure in that: only two parties have access to the payment information, the payment provider and the consumer device only the transaction at hand is at risk (not the whole account). 

While the above is true, push payments open up a new set of problems in that they make consumer end-points (browsers, phones, etc.) the most important point to protect. This presents complexity:
Consumers are not particularly capable of defending their machines against malware, errors, phishing, or man-in-the-middle attacks (where the consumer thinks they are paying the payer but are paying someone else)

Payment networks have less ability to manage, track, block centrally, and reverse transactions
Less clear who will take responsibility for fraud/errors since giving consumers full protection opens up the risk of consumer fraud

Richard Brown highlights some key issues regarding this topic [here]( http://gendal.me/2014/07/29/think-payment-cards-are-insecure-just-wait-until-push-payments-hit-primetime/ http://www.emc.com/collateral/white-papers/h13282-report-rsa-discovers-boleto-fraud-ring.pdf)

## Conclusions
Payment networks are at least one step, sometimes two steps, removed from the RTGS. The initially separate credit card and ATM payment networks have evolved to be close competitors. Credit card (and to a lesser degree, debit card) networks have a vast global network scale built up over decades and scalable structures to acquire customers (merchants, consumers). In addition, most of the processing, fraud, and profit-seeking costs of credit card networks are well- hidden from consumers who have a fairly straightforward payment experience.

>💡 The market structure of payment networks is an oligopoly, leading to frequent legal clashes with regulators and merchants. 
 
 
 


 

>💡 Cost of payments is a high cost of doing business for many retailers.

