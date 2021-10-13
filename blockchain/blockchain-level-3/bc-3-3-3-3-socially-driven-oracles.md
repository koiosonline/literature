# BC-3.3.3.3 Socially driven oracles

Human oracles might be considered the most straightforward kind of oracle. Like a notary, they sign the fact as it happens in the real world and project it on-chain, while at the same time not being able to touch the funds of the contract. But, of course, in that case, we put our trust in this particular oracle. Now, for complex and unique events from a well-known person, this might even be justifiable, but not so much for relying on one person to provide simplistic data like price feeds.

Besides trusting one human oracle, there is another option – prediction markets – that can be used in cases such as:

* trusting one person is not acceptable
* the wisdom of crowds is required
* predicting future events, etc.

On prediction markets, participants indicate their predictions by betting on the outcome. It is (somewhat controversially) accepted that such aggregation of collective intelligence is entirely accurate“.

>💡 Decentralized prediction markets (like Augur, Gnosis, Bitcoin Hivemind, Open Bazaar) could make such endeavors safer and cheaper due to automated smart contracts. They can be used as a market for oracles.

## Syndicated oracles

We have mentioned a market for oracles in prediction markets, with [](21%20Inc.%20data%20marketplace%5d(%20https:/21.co/mkt/) ) [being one of them.
Gnosis has an idea of an Ultimate Oracle, which would be people that challenge the actual outcome of an oracle: „For further security, a combination of oracles can be chosen for event resolution. For example, a market creator may select five oracles for resolution and require a 3 out of 5 majorities for event decision. By requiring oracles to submit security deposits, this scenario creates a risk of loss for oracles who lie about event resolution or attempt to conspire to do so. In the extreme scenario, market participants can challenge a resolution, pushing it to a second step, calling the Ultimate Oracle. “


One of the first attempts of overcoming the limitations of relying on a single oracle was made in 2014 with the project Orisi, which proposed using a pool of oracles, that would reach a consensus by signing on a multi-sig address, but with the limitation that one signature must come from the user requesting their service. Unfortunately, the project is not maintained for a long time now, a clear sign of how some ideas are ahead of time.

[21 Inc. data marketplace]( https://21.co/mkt/)  was an example of choosing any number of hardware oracles providing sensor data. Such markets can act as a kind of syndication since competition among providers filters out bad ones. (Note that 21 Inc., at the time one of the largest VC-funded blockchain companies, has pivoted to a very different business in 2017 and was acquired by Coinbase in 2018.)
 


