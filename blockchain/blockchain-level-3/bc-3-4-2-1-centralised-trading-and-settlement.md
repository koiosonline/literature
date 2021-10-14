# BC-3.4.2.1 Centralized trading and settlement 

What you can trade: 

* Tangible Assets: Real estate, commodities, intellectual property, plant/equipment, pollution credits, etc

* Financial Assets: Instruments that represent ownership of tangible assets and their associated cash flows. The three main classes of financial assets are:

* Equity: Common Stocks Preferred Stocks

* Other variations for convenience: American Depository Receipts, Exchange Traded Funds

* Debt

* Bonds (corporate)

* Treasury Bills/Notes/Bonds (sovereign) Mortgages, Car loans, etc.

* Derivatives (Instruments whose value is derived from another underlying instrument or entity):  Forwards/Futures Options, Swaps, Asset-Backed Securities.

## An analysis of the transfer, three parts
There is a split into three categories when you transfer the previous mentioned. **This divided into three functions is inevitable given the faster cycles required by trading (now down to the milliseconds) vs. settlement (still measured in multiple days). **

**1. Trading:** Matching bid/ask orders among traders


** 2. Clearing:** Everything that must be done between trade and settlement: order reconciliation, risk/credit management, handling failure states, etc.

The clearing is the process of confirming the trade, ensuring intra-day credit limits are not breached, netting out transactions, trade reporting (market price, trades), and generally managing all activities pre-settlement. It is usually handled by organizations that are separate from the brokers/dealers/traders/exchanges as they need to be a trusted, neutral third party. 

The clearing was a significantly more complicated process of pre-electronic trading when verbal trades had to be confirmed by both parties. Open-outcry systems, while shrinking, have persisted into the 21st century across various markets, and clearing systems have still needed to handle these trades. 

In electronic trading, as a general rule, trading and confirming the trade happen automatically as electronic systems have all information needed for the transaction ("straight-through processing"). Other activities such as monitoring credit limits and netting transactions remain essential roles for clearing systems. 

In derivatives markets, there is a large effort (pushed by regulators) in place to move to centralized counterparty clearing as opposed to a bilateral clearing. 

In a centralized clearing, a central counterparty is a counterparty to all trades (it is the counterparty to the buyer and the seller), so the buyer and seller are not exposed to individual counterparty risk. 

The members of the exchange support the counterparty, and any credit losses are distributed among all members

**3. Settlement**: Actual transfer of the securities, cash to execute the trading promise. 
Settlement is the process of changing the ownership of financial instruments (or, in rare cases, physical commodities)
On the whole, securities are held by third-party custodians, so they can easily be settled in the event of a trade
Custodians are also independent organizations whose job is to reduce counterparty and execution risk
Current settlement timeframes are T+3 for US equities (day of trade + 3 business days) and T+1 for US Treasury securities). EU recently (October 2014) is aiming for a T+2 settlement cycle. Other major markets in the Asia/Pacific region are already on T+2 or T+1. Singapore and Australia are also actively looking to reduce their settlement cycle from T+3
Longer settlement times mean (a) increased counterparty risk, (b) higher collateral costs and (c) more complex operations, (d) less trading flexibility (aka a proxy vote might occur during a day within the T+3 period).

## The participants

The instruments above and they're trading commonly need the following participants:

* Instrument issuers and underwriters

* Regulators overseeing the issuance of the instruments, the operation of exchanges, and clearing/settlement systems

* Exchanges (or alternative trading systems) where the instruments can be traded and a buy/ sell order ledger kept (order book)

* A clearing system that exchanges the traded instruments between old owners and new (a central counterparty)

* A custodial and settlement system that holds assets and settles beneficiaries based on the contractual obligations of the parties

Market Structure reflects the trading rules and trading systems used by a specific market. These choices include:

* Who trades

* Who trades directly vs. indirectly? How orders are matched

* What information is available to internal and external participants

* When trades can happen

* Different market structures exist in different markets, and that impacts:

* Trading strategies

* Liquidity provided Volatility

* Relationship with participants And so on

## Liquidity? 
We mentioned liquidity a few times already. In the previous sector, the transfer of payments meant: can you pay your bill? In the case of trading, you can dumb it down to: is somebody buying what you are selling/is somebody selling what you want to buy? 

A party that places a standing limit order (an order to buy or sell at a specific price) provides liquidity to a market. In other words, it allows someone to trade with them when they want/need to trade (in some markets, this party is called a "maker").

A party that fills transactions with that standing order is taking liquidity from a market (in some markets, this party is called a "taker"). Providing liquidity offers a type of uncompensated option to a potential counterparty (aka the ability to buy from or sell to you) which is why it has value to counterparties and, therefore, exchanges.

The main difference between a standing limit order and an option (an option premium would be paid) is how long it is valid. A compensated option is valid for longer periods (days/months/year) and cannot be withdrawn; a standing limit order can usually be withdrawn. As with options, standing limit orders are more valuable in volatile markets if near the strike price. Traders provide options for 'free' to achieve a better price than the market price.

**Standing Limit Orders Provide Liquidity Which Is Good For Markets**

## Trading forum types

Physically convened markets: all traders must trade-in a common trading floor ("posts" for equities, "pits" for futures). 

Distributed access markets: trading can occur anywhere using screens and phones. Gaining ground on physically convened markets. 

## Trade session types 

Call-based trading: all orders are submitted in advance, and all trades clear simultaneously at the market-clearing price (increase liquidity by consolidating orders). 

Continuous trading: trading can occur any time the market is open. Traders continually try to arrange mutually beneficial trades and trades occur when two parties match orders. Most major markets today are continuously traded. 

## Execution systems

Order-driven systems = All trades arranged directly from trader orders. 

Rules match buyers to sellers (order precedence) and determine the pricing of the trades (trade pricing)

Dealers can trade-in order-driven markets but just as a trader

More transparent, less liquid than quote-driven, all else being equal. Can be open outcry auctions or rules-based electronic matching.

Quote driven systems = Dealers arrange trades by serving as the intermediary between all traders
Dealers maintain inventory of securities and add to / subtract from it when buying from / selling to traders. Dealers quote bid/ask prices. Most bond and currency markets and some stock markets (NASDAQ) is quote-driven. More liquid, less transparent than order-driven, all else being equal.

Brokered trading systems = Used for illiquid or unique assets.  The most common brokered system we regularly encounter is real estate. Brokered systems, however, can also sometimes operate for illiquid financial instruments or large block trades. Brokers also serve as representatives/ credit guarantors of small retail customers in order/ quote-driven markets


Note: hybrid markets arise today. NYSE has its roots in order-driven systems and NASDAQ in quote-driven systems, but they are considered hybrid markets today.

![Source]( https://raw.githubusercontent.com/koiosonline/literature-images/main/blockchain-level3/bc-3-4-2-1-centralised-trading-and-settlement-image1.png)
[Source: Larry Harris, Trading and Exchanges: Market Microstructures For Practitioners.]( http://www-bcf.usc.edu/~lharris/Trading/Book/Book-extract.pdf)


## Conclusion Trading
While many major markets are hybridized, on the whole, trading market structure in equity markets is evolving toward:

* Order-driven systems

* Electronic order taking systems 

* Distributed access

* Competition, transparency, and interoperability between trading systems (forced by regulators)

On the whole, these are positive trends that have increased liquidity and volume while lowering spreads, though some concerns remain about:

* Price discovery / fragmentation

* Logistical integration of various market systems

* Possibility for electronic systems to enter unusual uncontrolled feedback loops

Possible ways to mitigate those concerns have included:

* Circuit breakers and other mechanisms to stop/reverse erroneous trades 

* Creating volume hurdles for integrated markets

Conclusions: Clearing and Settlement	

Clearing and settlement in most markets have lagged significantly behind the rate of change and technological development in trading. Depending on the market, settlement ranges from T+1 to T+3 and has only changed slowly.

Custodians and clearing organizations are typically independent of the exchanges. 

Changing the clearing and settlement process is a complex initiative. Requires significant investment in IT and process reengineering by every participant in the system in exchange for future cost savings that are harder to define and will pay off over time. This causes a collective action problem of sorts. There are limited individual benefits in making the necessary investments (unlike in trading) until most system participants also decide to make the investments and changes.

The greatest immediate improvements are likely in the EU as T2S replaces national systems with a cross-national settlement system. The DTCC in the United States is pushing for a move to T+2 (instead of T+3).

In markets like derivatives that were historically settled bilaterally, there has been progressing in moving to centralized clearing, but this is a long and ongoing process and is happening primarily at the behest of regulators.



