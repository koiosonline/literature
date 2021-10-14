# BC-3.4.1 (de)centralised monetary systems 


## About this chapter?
This paragraph is split into two main components. The first component concerns the settlement of "money" between parties: I owe you X, and you owe me Y, so settle. The second component involves the digital transfer of money between parties: debit and credit cards & cryptocurrencies. Both parts first describe the current centralized systems and, secondly, discuss their upcoming decentralized counterparts. 

## What will we discuss? 

BC-3.4.1.1	Centralised monetary settlement systems

BC-3.4.1.2	Blockchain-based decentralized monetary systems

BC-3.4.1.3	Centralised digital money transmission and payment services (Debit & credit cards)

BC-3.4.1.4	Cryptocurrencies as methods of payment and processing


## After this class, I can:

1.	Explain the difference between the centralized and decentralized monetary system 

## NEXT CHAPTER

# BC-3.4.1.1 Centralised Settlement Systems – simplified scenario's

*Scenario 1: Two Accounts In The Same Bank.* 

This is the most simple scenario. Bob wants to send $50 to Lucy, and they are both customers of XYZ Bank. XYZ will debit Bob's account $50 and credit Alice her account with $50. The journal remains in balance (double-entry accounting system), and they will digitally enter this mutation. In other words: XYZ won't move physical cash from the safe of Bob to the safety of Alice (as you already learned, there is no cash because of the fractional reserve system). They will say that they owe Bob $ 50 less and will owe Lucy $50 more. This whole transaction is done internally, so entirely within the internal systems of XYZ (their own ledger/accounting book). There is no external entity involved, so there is no counterparty risk for XYZ. It doesn't impact the bank's liquidity in any way (they don't need to pay anybody from outside their ledger). In other words, in this scenario, bank XYZ is in control of the settlement. 

*Scenario 2: Corresponding Banks.*  But what happens if Alice and Bob both have a different bank? 

Bob (at bank XYZ) wants to send $50 to Alice (at bank ABC). Bank XYZ and ABC have multiple customers doing business with each other. Therefore a correspondent relationship / they maintain accounts with each other. In this case, there isn't just one ledger that needs to be updated, as in scenario 1. In this scenario, two ledgers need to be updated: XYZ debits Bob's account $50, which means they owe Bob $50 less. To equal the double entry, XYZ also credits ABC's account $50 (instead of Alice's internal account in scenario 1, XYZ now credits ABC's external account). The ABC bank does the opposite: they will credit Alice her account with $50 (because they will owe Lucy $50 more, a credit/debt for the bank). This nets out against the $50 credit they received from XYZ, so Citibank nets out. Again, all are equal in both ledgers (still no physical cash moving, every happens in digital ledgers!). This is an effective system but has some weaknesses: 
(1) It is not at all practical for every bank to have a correspondent relationship with every other bank
(2) The banks are exposed to credit risk/counterparty risk with each other. 

*Scenario 3: Settlement Systems.* This is the most generic system. Bob (at XYZ) wants to send $50 to Lucy (at ABC). Here comes the trick: instead of XYZ and ABC having accounts at each other, they both have an account at the "settlement system" (as well as many other banks at the same time!). So what happens: 

XYZ can debit Bob's account $50 (aka, they will owe Bob $50 less)

The settlement system debits XYZ's settlement system account $50 & credits ABC's settlement system account $50

ABC credits Alice her account with $50

The settlement system can be a private company or, in the case of the ultimate settlement systems, the Central Bank of the country

But why do this? Like a bank, do you still need to settle with an external entity? Settling with Central Bank money has significant advantages to system users:

* No counterparty/credit risk
* (Usually) provision of credit/overdraft as needed
* (Usually) low costs

>💡 In this process, we have two parts of the transaction, "clearing" & "settlement". **Clearing**: The activities associated with transferring information relating to payment and related activities (confirmation, error resolution, etc.). **Settlement**: The actual transfer of funds. 'Final Settlement' is irrevocable.

<blockquote style="border-color: #ff0bac">❓ Does this described settlement system have “final settlement”? </blockquote>

## Three Types of Settlement Systems	
There are three different types of settlement systems: 

Gross settlement systems: each transaction is processed as it happens. The transactions aren't bundled or batched with others. Benefit: reduces intra-day credit risk (smaller amounts and live settlement). Downside: increases liquidity needs (you need to fund each transaction at a time) and, subsequently, cost of liquidity (more reserves or interest charges). 
Net settlement systems: transactions are netted out at the end of the day. Benefit: Reduces liquidity needs as only the net amount has to be available from a liquidity perspective. As you might have guessed, the downside: increases the credit risk (larger amounts and less frequent settlement) 
Hybrid settlement systems are nearly real-time but look for betting opportunities (liquidity benefits). Methods to do this: Netting of queued orders, Prioritization of orders, Delaying orders above certain liquidity limits

Most developed economies now have Real-Time Gross Settlement systems (RTGS) backed by their Central Bank. Net settlement approaches are more popular for other systems but have largely migrated to hybrid models.

## Euro settlement system - Target2

![source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-1-centralised-monetary-settlement-systems-image1.png)
[source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-1-centralised-monetary-settlement-systems-image1.png)


So a quick recap of these settlement systems tells you that consumers don't have a peer-to-peer transaction. Still, the transaction settlement moves via their bank, towards the settlement system, back to the bank of the other peer to the peer. In the EU, this settlement system is called Target2. Target2 operates like the Federal Reserve, where accounts are credited and debited at the national level (with national Central Banks), and national Central Banks hold credit/debit balances with each other. 

![source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-1-centralised-monetary-settlement-systems-image2.png)
[source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-1-1-centralised-monetary-settlement-systems-image2.png)


While this is unremarkable in other settlement systems, it has raised questions in Target2 about possible credit risk to national central banks in the event of, for example, a member state exiting the Euro or losing trust from other central banks. More detail on this issue [can be found here](http://www.bis.org/publ/work393.pdf). 

Fun fact: Target2 is often confused with the SWIFT messaging system. SWIFT, however, is nothing more than the communication system that communicates the transaction. The Society for Worldwide Interbank Financial Telecommunication (SWIFT) is a member-owned cooperative, operating with 10,793 financial institutions in 215 countries. SWIFT is a perpetual point of confusion for people from outside the industry. It is NOT a payment or settlement system. It is simply a messaging system used by other payment or settlement systems (funds settlement, securities settlement, etc.) to pass along the relevant information related to a transaction. SWIFT exchanges about 28M messages per day on average, of which 48.6% funds. Source 

## A recap
It is important to note that the previously described doesn't mean that all your small transactions move via the settlement system of your country's central bank. That would be too costly. Hence the transactions that settle via Target2 or FedWire are limited: +/- 400,000 (Target2) and 600,000 (FedWire). All major currency zones have a Central Bank-backed RTGS. This serves as the backbone of the payment system, both directly and indirectly:

 

* Directly: For high value, time-critical transactions
* Indirectly: As an ultimate settling system for other payment systems
In all cases with no counterparty risk for the users of the system
Despite the existence of RTGS, there is a variety of (a) economic, (b) liquidity, (c) historical, or (d) specialization reasons that other net settlement payment systems exist, creating heterogeneous payments and settlement environment.

Additional specialized systems exist for retail payments, securities, other assets, and so on. But before we dive into those, let's take a closer look at Bitcoin and the idea of Bitcoin as an RTGS (Real Time Gross Settlement System). 

