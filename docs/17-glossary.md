# Glossary

Every term in one place, in alphabetical order.

| Term | Meaning |
| --- | --- |
| **Angle** | How much the channel leans (−2.4 … +2.4), the trend read. |
| **Balance** | What you hold in each currency; positions open from it and pay back into it. |
| **Bind** | The moment a signed price report sets your entry and locks your multiplier. Nobody chooses the entry price. |
| **Breach** | Backing a wall to break before the end; wins the moment a wall is touched. |
| **Ceiling** | The maximum multiplier, set per currency (25× for $OVER, 10× for $USDG), which keeps each vault solvent. |
| **Channel** | An angled band of two walls, drawn on the live price. It exists as an NFT; its creator earns a royalty when another player's position on it wins. |
| **Currency** | The money a position is opened in, $OVER or $USDG. Its deposit, fees and payout all stay in it. |
| **Currency filter** | A dashboard section's choice of how its money reads: USD, $OVER or $USDG ($OVER or $USDG on the Leaderboard). Each section remembers its own. |
| **Daily loss limit** | A share of each vault's capital (5% for $OVER, 50% for $USDG) that refills over a day and with every lost position. A win larger than what is left pauses trading for a review. It always shows in the vault's own currency, never in USD. |
| **Duration** | How long the position runs (15m … 24h). |
| **Entry permit** | A short-lived signature the operator gives wallets with at least 100,000 $OVER staked on mainnet, so they can open $USDG positions. A new stake gets one within about 5 minutes, and it renews automatically while the stake stays at 100,000 $OVER or more. Below that, it lapses within about 30 minutes: new $USDG positions stop, and open ones run to the end. |
| **Fee** | The vault's transparent, published margin: an open fee (the greater of 1% and a fixed minimum, 20 $OVER or 0.05 USDG) plus a 10% fee on the profit of a winning close. |
| **Genesis airdrop** | 1% of the $OVER supply for early stakers and testnet players. Points closed Oct 19, 12:00 UTC; allocations vest daily over 15 days, with 30 days to claim from the start of vesting. See [Genesis airdrop](https://docs.overcall.io/airdrop). |
| **In review** | A win held for a review, usually because trading is paused: your stake is paid at once, and the rest waits for the review's decision. |
| **Liquidation** | A wall touch ending the Survive side at 0; the same signed breach report pays the Breach side in full (during a review pause, its stake at once and the rest held for review). Proven onchain, never decided. |
| **Minimum multiplier** | The floor under M (1.01×); a side priced below it is cancelled, not offered. |
| **Multiplier (M)** | Your payout factor, final at bind: Survive M = (1 − δ) / P, Breach M = (1 − δ) / (1 − P), the honest inverse of your side's win probability, less the spread, capped by a ceiling. |
| **Operator** | The service that maintains the volatility estimate, posts signed quotes, binds entries to reports in batches, liquidates breaches, settles positions at the end, and signs the entry permits that let wallets with 100,000 $OVER or more staked open $USDG positions. It cannot pick an entry price or a winner, and everything it does is reproducible from signed inputs. |
| **$OVER** | Overcall's token, the asset every product is built around: take positions in it, stake it to earn a share of platform fees (and, from 100,000 $OVER, to unlock $USDG positions), and claim channel royalties in it. |
| **$OVER P&L** | The figure the $OVER board ranks by: your realized $OVER positions plus the royalty you claimed from $OVER predictions on your channels. |
| **Payout waiting** | An amount the vault keeps for you because the token refused the transfer to your address; you withdraw it from the dashboard. |
| **Position** | A stake on a channel, your own or someone else's, on a side: Survive (it holds) or Breach (a wall breaks), in one currency, $OVER or $USDG. Entered at the bound mark. |
| **Prediction** | Taking a side, Survive or Breach, on someone else's live channel, at odds from its survival probability. |
| **Range** | An asset's typical move (its volatility unit); sizes the channel at open, never decides the outcome. |
| **Rejected** | A held win the review did not approve: you keep the stake already paid. |
| **Robinhood Chain** | The network Overcall runs on: an Arbitrum-based L2, chain ID 4663 on mainnet. Gas is paid in ETH. |
| **Royalty** | The channel creator's cut of every winning prediction on their channel: 15% of its profit fee, in $OVER and $USDG. It accrues in the prediction's currency and is claimed with Claim all in User space; $USDG royalty is swapped into $OVER when you claim it. |
| **Spread (δ)** | The platform's transparent, published margin, the same for both sides. There is no hidden odds edge. |
| **Staking** | Putting $OVER in the staking contract on mainnet, non-custodial and with instant unstake: 25% of the profit fees from $OVER positions go to stakers, and 100,000 $OVER or more unlocks $USDG positions. |
| **Survival probability (P)** | The model's chance the channel survives to the end; prices both sides. |
| **Survive** | Backing a channel to hold every wall to the end; wins if no wall is touched. |
| **Testnet demo** | The free practice version of Overcall on Robinhood Chain's test network (chain ID 46630), with tOVER and tUSDG, test tokens that have no value. |
| **Trading paused** | The state after a daily loss limit is hit or trading is paused by hand: new positions wait, open positions keep running, and wins are held for review. See [When trading pauses](07-vault.md#when-trading-pauses). |
| **USD value** | How the dashboard shows money: USD first, with the token amount beside it. What you hold is valued at the current price, what already happened at the price when it settled; $OVER at its mainnet market price (tOVER too, on the testnet), $USDG at $1. |
| **$USDG** | Global Dollar, the second currency positions can open in, with its own vault; $USDG positions need 100,000 $OVER or more staked. |
| **Vault** | The neutral onchain counterparty (the Settlement Vault), one per currency, that pays every winning close in that currency. |
| **Watch link** | A public link that renders a live position on the real chart, no wallet needed; the prediction ticket sits beside it. |
| **Width** | Wall distance from the center (±2.5× … ±38× range, ±19× on VIRTUAL), the room to breathe. |

<sub>Source: [docs.overcall.io/glossary](https://docs.overcall.io/glossary)</sub>

---

[← FAQ](16-faq.md) · [Contents](../README.md#documentation)
