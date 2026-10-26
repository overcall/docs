# FAQ

The questions worth asking, answered straight.

## Trading

### What can I trade?

Crypto: BTC, ETH, BNB, SOL, HYPE and VIRTUAL today, with XRP and DOGE coming soon. Tokenized stocks (NVDA, AAPL, MSFT, GOOGL, AMZN, META, HOOD, TSLA) are coming soon too. Same rules and payout table across all of them. Positions are in $OVER, or in $USDG if you stake 100,000 $OVER or more. See [Markets](03-parameters-and-markets.md).

### Do I win only if the market goes up?

No. In Channels you pick a side, **Survive** (your channel holds every wall to the end, up or down) or **Breach** (a wall breaks first), and shape it with the tilt (angle), the room (width) and how long it runs (duration).

### Can I take a position on someone else's channel?

Yes. Every open channel is a two-sided market: back it to **Survive** (it holds to the end) or **Breach** (a wall breaks first), at odds from the channel's survival probability. That is Prediction; on your own channel you take a side exactly the same way. See [Prediction](04-prediction.md).

### How many positions can I hold?

As many as you like, there is no cap on concurrent open positions per wallet. Each one needs room in the vault of its currency, which reserves its maximum payout before the position opens. See [Parameters and limits](03-parameters-and-markets.md).

## Pricing, fees and payouts

### Is Overcall my counterparty?

You trade against a neutral onchain vault in your position's currency, like a perp DEX. Its only margin is a published fee, never a number hidden inside your odds. The market, priced by a decentralized feed, decides every outcome. See [Vault architecture](07-vault.md#vault-architecture).

### What are the fees?

Two, both published. The **open fee**, the greater of 1% of your deposit and a fixed minimum (20 $OVER, or 0.05 USDG on a $USDG position), is carved out of the deposit at open, win or lose. The **profit fee** is 10% of the profit on a winning close, and 15% of it goes to the channel's creator as a royalty when the winning position is someone else's. An early close also carries a 5% penalty on its mark-to-market value. 25% of the profit fees from $OVER positions go to $OVER stakers. There is no edge hidden in the multiplier. See [Parameters and limits](03-parameters-and-markets.md).

### How is my multiplier set?

One number, your channel's survival probability P, prices both sides: Survive pays M = (1 − δ) / P and Breach pays M = (1 − δ) / (1 − P), where δ is a published spread. Each is capped by a ceiling set per currency (25× for $OVER, 10× for $USDG) so each vault stays solvent, and final when your entry binds onchain; the ticket shows the capped multiplier. Anyone can recompute it from the signed inputs. See [Opening a position](02-channels.md).

### When do I get paid, and how much?

The instant it resolves, unless trading is paused for a review: then a win pays your stake at once and holds the rest for the review (see [When trading pauses](07-vault.md#when-trading-pauses)). Survive collects stake × M if the channel holds to the end, and 0 if a wall is touched; Breach collects stake × M the moment a wall breaks, and 0 if the channel holds. Either side can close early for a mark-to-market amount set by its current win probability, less a small penalty. See [Closing a position](02-channels.md).

### What happens if a wall is touched?

The channel resolves right there: the **Breach** side is paid in full, and the **Survive** side is liquidated (0), like a futures liquidation. One signed proof settles every position and prediction on the channel, whichever side each took, your own included. Everything you already collected from closed positions is safe.

## Getting started

### What chain is this, and how do I add it?

Robinhood Chain mainnet (chain ID 4663), an Arbitrum-based L2: a blockchain network built with Arbitrum technology. When you connect, the app asks your wallet to switch to it and adds it if needed; the details to add it by hand are on [Wallet and network](15-using-the-app.md#wallet-and-network). Gas is paid in ETH on Robinhood Chain.

### Where do I buy $OVER?

On Uniswap on Robinhood Chain, where you swap ETH for $OVER; the app's Buy $OVER link opens that swap. Check the token address first: $OVER is `0x6245Db7f52379bD9757c9DdcE6519768FfaB3a4F`. See [Wallet and network](15-using-the-app.md#wallet-and-network).

### Can I try it for free first?

Yes. The testnet demo runs the same app and rules with free test tokens (tOVER from the faucet) that have no value. See [Testnet demo](15-using-the-app.md#testnet-demo).

### Do I have to verify my identity?

No. $OVER positions need only a connected wallet; $USDG positions also need 100,000 $OVER or more staked from the same wallet. Connecting X is optional and sets how you appear (your handle and avatar on the leaderboard, feed and share cards). It never gates playing and is never custody of anything.

### Can AI agents trade? Is there an API?

Yes. Everything is a contract call plus a signed report and a public GraphQL API, so agents can trade and read without a proprietary API; a $USDG position also takes an entry permit from the same public API. Where to find the ABI and the API is on [Developers and agents](10-developers.md).

## $OVER, staking and the airdrop

### What is the token supply and tokenomics?

$OVER is the token every product is built around, and it launched on Virtuals. Fixed supply of 1B, with the full allocation, cliffs and vesting on the [Tokenomics](12-tokenomics.md) page. See [The $OVER token](11-over-token.md).

### What do stakers earn?

A share of real platform revenue: 25% of the profit fees from $OVER positions go to stakers. Claiming rewards is not live yet, and the projected APR shows on the Staking page once it can be worked out from live fees. Unstake any time, instantly. See [Staking](13-staking.md).

### When can I claim the Genesis airdrop?

Now: claiming is live on the Staking & Airdrop tab of the dashboard. Vesting started on Oct 20, 10:00 UTC, and a fifteenth of your allocation unlocks every 24 hours, from Oct 21 to Nov 4, 10:00 UTC. Claim by Nov 19, 10:00 UTC; anything left unclaimed then flows into the vault. See [Genesis airdrop](https://docs.overcall.io/airdrop).

### Did $USDG positions count for the airdrop?

No. Only $OVER positions of 1,000 or more counted toward the testnet activity and channel royalty pools. See [Genesis airdrop](https://docs.overcall.io/airdrop).

## $USDG positions

### What are $USDG positions?

Positions in $USDG, the second currency next to $OVER. A $USDG position takes its deposit, fees and payout in $USDG, against a separate $USDG vault, on the same channels and at the same fee percentages. They are open to wallets with 100,000 $OVER or more staked. See [Opening a position](02-channels.md).

### Who can open $USDG positions?

Wallets with at least 100,000 $OVER staked on Robinhood Chain mainnet, from the same address. A new stake is recognized within about 5 minutes. If your stake falls below 100,000 $OVER, for example after an unstake, new $USDG positions stop within about 30 minutes; positions already open run to the end. See [Staking](13-staking.md).

### How do I get tUSDG?

tUSDG is the testnet twin of $USDG, for the testnet demo. Stake 100,000 $OVER or more on Robinhood Chain mainnet, and once your stake is recognized (within about 5 minutes), claim it from the faucet in the Balance tab of the testnet app, next to tOVER. See [Testnet demo](15-using-the-app.md#testnet-demo).

### Can I predict in $USDG?

Yes. The currency belongs to your position, not the channel, so with 100,000 $OVER or more staked you can back any live channel in $OVER or $USDG, whichever currency its creator used. See [Prediction](04-prediction.md).

### Why does a $USDG position show a lower multiplier?

Each currency has its own multiplier cap: 10× for $USDG and 25× for $OVER. A side priced above the cap is offered at the cap, and the ticket shows the capped multiplier. See [Parameters and limits](03-parameters-and-markets.md).

## Royalties, reviews and payouts

### How is royalty from $USDG predictions paid?

Your royalty is 15% of the profit fee of every winning prediction on your channels, in $OVER and $USDG. The $USDG part is swapped into $OVER when you claim it, so its total is an estimate until then. **Claim all** in User space claims your $OVER royalty first, then the $USDG royalty swapped into $OVER, with two confirmations in your wallet. See [Dashboard and metrics](15-using-the-app.md#dashboard-and-metrics).

### Why can't I claim my royalty yet?

A channel's royalty unlocks once the channel has ended, every position on it, in either currency, has settled, and every win on it held for review is decided.

### What do "Trading paused" and "In review" mean?

Each vault has a daily loss limit. When a single win is larger than what is left of it, trading pauses for a review in both currencies: new positions wait, open positions keep running, and if you win, your stake is paid at once while the rest is held for the review (In review). Trading resumes once the review is done. See [When trading pauses](07-vault.md#when-trading-pauses).

### What is "Payout waiting"?

The token refused a transfer to your address, so the vault kept the amount for you. Withdraw it from your dashboard once your address can receive the token again.

## Dashboard and leaderboard

### Do $USDG positions count for the leaderboard?

Not on the $OVER board, the default one, which ranks $OVER positions. Where $USDG positions are offered, the currency filter on the Leaderboard picks a separate $USDG board, and the two are never added together. See [Dashboard and metrics](15-using-the-app.md#dashboard-and-metrics).

### Why does the dashboard show dollars?

So both currencies read on one scale. Every money figure shows USD first, with the token amount beside it: what you hold at the current price, what already happened at the price when it settled. $OVER is valued at its mainnet market price (tOVER too, on the testnet) and $USDG at $1. The loss limit always shows in each vault's own currency, and every position, payout and vault still runs in its own currency. Each section's currency filter switches to $OVER or $USDG. See [Dashboard and metrics](15-using-the-app.md#dashboard-and-metrics).

<sub>Source: [docs.overcall.io/faq](https://docs.overcall.io/faq)</sub>

---

[← Using the app](15-using-the-app.md) · [Contents](../README.md#documentation) · [Glossary →](17-glossary.md)
