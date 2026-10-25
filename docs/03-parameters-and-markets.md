# Parameters and markets

Every knob and every limit in one place, plain meaning first, with the exact values set in the contracts and enforced by the chain, followed by the markets they apply to.

## Parameters and limits

| Knob / limit | Range | What it means |
| --- | --- | --- |
| Angle | −2.4 … +2.4 | trend lean (the channel's slope); steeper drifts faster toward a wall |
| Width | ±2.5× … ±38× range (±19× on VIRTUAL) | wall distance (the channel's height), in range; tighter is harder to survive |
| Duration | 15m … 24h | position length in the app's ticket (the contract accepts from 2m); longer gives the price more time to reach a wall |
| Currency | $OVER or $USDG | the currency of the deposit, the fees and the payout; $USDG positions need a stake of 100,000 $OVER or more |
| Position size | per currency | the minimum and maximum deposit (see [Terms per currency](#terms-per-currency) below) |
| Survival probability P | 0 … 1 | the model's chance the channel survives to the end; prices both sides |
| Spread δ | published | the platform's transparent margin, the same number for both sides (there is no hidden edge) |
| Ceiling | per currency | the maximum multiplier (25× for $OVER, 10× for $USDG), which keeps each vault solvent; a side priced higher is offered at the cap, and the ticket shows it |
| Minimum multiplier | 1.01× | the floor on M; a side priced below it is cancelled, not offered |
| Open positions | unlimited | no cap on concurrent live positions per wallet; each one needs room in its currency's vault, which reserves its maximum payout up front |
| Exposure cap | per currency | full reserving: each currency's vault reserves every position's maximum payout from its own capital; a request it cannot cover is refused |
| Daily loss limit | per currency | a share of each vault's capital (5% for $OVER, 50% for $USDG) that refills over a day; a win larger than what is left pauses trading for a review (see [When trading pauses](07-vault.md#when-trading-pauses)) |
| Open fee | max(1%, fixed minimum) | the fixed minimum is 20 $OVER or 0.05 USDG; carved out of the deposit at open, win or lose; the payout multiplies the rest |
| Profit fee | 10% of profit | charged on any payout above the stake, published beside the odds |
| Creator royalty | 15% of the profit fee | paid to the channel's creator on every winning position others take on their channel, in that position's currency ($OVER or $USDG); $USDG royalty is swapped into $OVER when the creator claims it |
| Stakers' share | 25% of $OVER profit fees | 25% of the profit fees from $OVER positions go to $OVER stakers (see [Staking](13-staking.md)) |
| Early-close penalty | 5% | the discount on an early close's mark-to-market value |

### Terms per currency

A position opens in $OVER or $USDG, and a few terms are set per currency. The fee percentages, the royalty share, the early-close penalty and the minimum multiplier (1.01×) are the same in both. These are the mainnet values, set in the contracts on Robinhood Chain. The [testnet demo](15-using-the-app.md#testnet-demo) runs the same terms, except a 50× cap on tOVER positions.

| Term | $OVER | $USDG |
| --- | --- | --- |
| Who can open | everyone | wallets with 100,000 $OVER or more staked (see [Staking](13-staking.md)) |
| Position size | 500 … 200,000 $OVER | 0.50 … 50.00 USDG |
| Open fee | max(1%, 20 $OVER) | max(1%, 0.05 USDG) |
| Multiplier cap | 25× | 10× |
| Daily loss limit | 5% of the vault's capital | 50% of the vault's capital |

> [!NOTE]
> $USDG positions need 100,000 $OVER or more staked on Robinhood Chain mainnet, from the same wallet. A new stake is recognized within about 5 minutes. If the stake falls below 100,000 $OVER, new $USDG positions stop within about 30 minutes, and positions already open run to the end.

### Range: the volatility unit

Width and angle are measured in **range**, the typical size of a move for *that* asset, right now. It is what makes "±10× range wide" the same difficulty on BTC as on TSLA. The operator maintains range as a smoothed estimate that reacts to the current regime without jumping on a single spiky minute.

Range only **sizes** your channel at open, and is frozen into your walls from there. It never decides who wins: the price against your walls does. It is the one bounded input the platform maintains, and it can only scale a channel, never move a wall after open.

## Markets

Crypto and tokenized stocks, all on the same rails and the same payout table. Because everything is measured in [range](#range-the-volatility-unit), one channel is the same difficulty on BTC as on TSLA.

| Group | Markets | Hours | Status |
| --- | --- | --- | --- |
| Crypto | BTC · ETH · BNB · SOL · HYPE · VIRTUAL | 24/7 | open on mainnet, $OVER and $USDG positions |
| Crypto | XRP · DOGE | 24/7 | soon |
| Tokenized stocks | NVDA · AAPL · MSFT · GOOGL · AMZN · META · HOOD · TSLA | market hours | soon |

BTC, ETH, BNB, SOL, HYPE and VIRTUAL are open on mainnet, each taking $OVER and $USDG positions; XRP, DOGE and the tokenized stocks are coming soon. Crypto markets are open around the clock. Tokenized stocks follow their regular trading session; outside market hours a stock market pauses.

Every market is priced by the same decentralized feed and settles under the same contract, so nothing about the rules changes when you switch assets, only the volatility unit (range) does. New markets can be added without new rules, because any market the oracle can price, the vault can take.

<sub>Source: [docs.overcall.io/params](https://docs.overcall.io/params), [docs.overcall.io/markets](https://docs.overcall.io/markets)</sub>

---

[← Channels](02-channels.md) · [Contents](../README.md#documentation) · [Prediction →](04-prediction.md)
