# Using the app

The Overcall app is at [https://app.overcall.io](https://app.overcall.io). This page is a condensed tour of what it does and why it matters; the full step-by-step guides are on [docs.overcall.io](https://docs.overcall.io).

## Quick start

From a connected wallet to your first payout:

1. **Connect a wallet.** Overcall is open to everyone, with no account and no invite code. The app asks your wallet to switch to **Robinhood Chain** mainnet (chain ID 4663) and to add the network if it is not there yet. Keep a little ETH on Robinhood Chain for gas (see [Wallet and network](#wallet-and-network)).
2. **Get $OVER.** You take positions with the **$OVER** in your wallet. Buy it on Uniswap on Robinhood Chain, where you swap ETH for $OVER. If you stake 100,000 $OVER or more, you can also open positions in $USDG (see [Staking](13-staking.md)).
3. **Pick a market and draw.** Choose an open market, then drag on the chart to set your angle, width and duration. The ticket prices both sides of your channel before you commit (see [The terminal](#the-terminal)).
4. **Take a side, open.** Back your channel to **Survive** (it holds every wall to the end) or **Breach** (a wall breaks first). Your entry is bound to a signed price report, so nobody picks your entry price; your multiplier is final when it binds.
5. **Close, get paid.** Survive collects the full multiplier if the channel holds to the end, and is liquidated at 0 if a wall is touched; that same touch pays Breach in full. Either side can close early for a known amount, and the vault pays you the instant it resolves, unless trading is paused for a review: then a win pays your stake at once and holds the rest for the review.

There is no account and no custody: every position and payout is an onchain event under your address.

Full guide: [docs.overcall.io/play](https://docs.overcall.io/play)

## The terminal

Where you draw and trade: a live price chart, the channel you shape on it, and a ticket that prices your position before you commit.

- **The chart.** Japanese candles by default, or a line. You draw your channel directly on it, dragging the tilt grip to set the **angle**, the wall grips to set the **width**, and the end grip to set the **duration**.
- **Focus and Manual.** **Focus** auto-frames and tracks your channel so the drawn shape always stays in view (the default on mobile). **Manual** hands you the wheel: free pan, zoom, scrollback, a price-axis drag (the default on desktop) and a full drawing toolkit, whose drawings save per market and sync to your wallet.
- **Market rail.** Every market runs down the left, grouped into crypto and tokenized stocks, each with a live price, 24h change and a sparkline (see [Markets](03-parameters-and-markets.md)).
- **The ticket.** The three sliders (angle, width, duration), the side you take (**Survive** or **Breach**, each with its own live multiplier), your position size, and a payout card that shows the estimated **multiplier**, the **full payout** and the **fees** before you open. Click the unit next to the position size to switch between $OVER and $USDG; $USDG needs a stake of 100,000 $OVER or more.

Full guide: [docs.overcall.io/terminal](https://docs.overcall.io/terminal)

## Watch and spectate

Every position is watchable, live, by anyone, no wallet needed. Open the **Predict** tab of the ticket to browse the most popular and the newest live channels, or search a position by ID or a whole wallet by its address; picking one renders that live channel on the real chart with its stats. From any watched channel you can open a prediction right there, backing it to Survive or Breach (see [Prediction](04-prediction.md)). Every position has a public **watch link** (for example `/channels/prediction/<id>`) that renders the live channel with no wallet, and unfurls a branded card when shared on X, Telegram or Discord. Add `?embed=1` for a chrome-less version to embed anywhere.

Full guide: [docs.overcall.io/watch](https://docs.overcall.io/watch)

## Dashboard and metrics

Everything about your account and the platform in one place, opened from the grid button in the top bar.

- **Money in USD.** Every money figure reads in **USD first**, with the token amount beside or under it: what you hold now is valued at the current price, what already happened at the price when it settled. $OVER is valued at its mainnet market price and $USDG at $1. The **loss limit** always shows in each vault's own currency, never in USD, and each section has its own currency filter.
- **Your account.** The **Overview** shows your balance, one row per currency, your identity and quick actions. **User space** is your full profile: your account, your standing on the leaderboard, your active and past positions, a performance equity curve, your activity and your royalties.
- **Royalties.** Your royalty is **15% of the profit fee of every winning prediction on your channels**, in $OVER and $USDG. It becomes claimable once the channel has ended, every position on it, in either currency, has settled, and every win on it held for review is decided. **Claim all** claims it in one go; royalty from $USDG predictions is swapped into $OVER when you claim it.
- **Platform metrics.** The whole venue at a glance: KPIs with sparklines (players, positions, average multiplier, most-popular market), the **vault** section (balance, capital, free capital, the loss limit left, vault revenue, volume, open exposure, positions settled), the biggest **top wins**, the **top players**, and a live **feed**.
- **Leaderboard.** Ranks players on the **$OVER board** by **$OVER P&L**: your realized $OVER positions plus the royalty you claimed from $OVER predictions on your channels. Where $USDG positions are offered, its currency filter picks a separate **$USDG board**, and the two are never added together.
- **Staking & Airdrop.** Stake $OVER there to earn a share of platform fees, and 100,000 $OVER or more to unlock $USDG positions (see [Staking](13-staking.md)). Your Genesis airdrop allocation, its vesting and the Claim button live on the same tab (see [Genesis airdrop](https://docs.overcall.io/airdrop)).

Full guide: [docs.overcall.io/dashboard](https://docs.overcall.io/dashboard)

## Profile and identity

Connecting an identity is optional and only changes how you appear, never your ability to play. Link your X account to set your **handle** and **avatar** everywhere they appear: the leaderboard, the activity feed, watch views and your share cards. It is a read-only connection for display, and you can disconnect any time. In Settings you choose how you are shown (your wallet, your X name, or your X handle), with a fallback to a short wallet address if you have not connected X. Every wallet is a public profile at `/dashboard/user-space/<address>`, with its standing and rank on the $OVER board, positions and history, and a performance curve, every figure backed by an onchain event.

Full guide: [docs.overcall.io/identity](https://docs.overcall.io/identity)

## Sharing and referrals

Every result and every profile is shareable, and the links carry your identity and bring people in. Any position becomes a branded **result card** that draws your real channel and its outcome (a win, an early close, or a loss, for whichever side you took), and your profile has its own **profile card** (rank and realized P&L on the $OVER board, top assets). Both unfurl automatically when the link is posted on X, Telegram or Discord, and each shared position is a live [watch link](#watch-and-spectate). Your invite link carries a referral tag: when someone connects through it they are attributed to you, and your invite count shows in the dashboard.

Full guide: [docs.overcall.io/share](https://docs.overcall.io/share)

## Wallet and network

Overcall runs on **Robinhood Chain** mainnet and is open to everyone: no account, no sign-up, no invite code. You need three things: a wallet, a little ETH for gas, and $OVER. Connect a browser wallet (on a phone, open the app in your wallet's built-in browser); the app asks your wallet to switch to Robinhood Chain, and to add the network first if your wallet does not know it yet. Robinhood Chain is an Arbitrum-based L2, a blockchain network built with Arbitrum technology. If your wallet does not add it for you, enter these details by hand:

| Setting | Robinhood Chain mainnet |
| --- | --- |
| Network name | Robinhood Chain |
| Chain ID | 4663 |
| RPC URL | `https://rpc.mainnet.chain.robinhood.com/rpc` |
| Currency symbol | ETH |
| Block explorer | <https://robin.etherscan.io> |
| App | <https://app.overcall.io> |

| What you need | How to get it |
| --- | --- |
| Gas | Every transaction, from opening a position to staking or claiming, costs a small amount of **ETH on Robinhood Chain**, the network's gas. Keep a little ETH in the same wallet as your $OVER; the app tells you when it runs low. |
| $OVER | Token address `0x6245Db7f52379bD9757c9DdcE6519768FfaB3a4F`. $OVER trades on **Uniswap on Robinhood Chain**, you swap ETH for $OVER ([open the swap on Uniswap](https://app.uniswap.org/swap?chain=robinhood&inputCurrency=NATIVE&outputCurrency=0x6245Db7f52379bD9757c9DdcE6519768FfaB3a4F)). The app's **Buy $OVER** link opens that swap in a new tab. |
| $USDG | Global Dollar on Robinhood Chain, at `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168`. |
| $USDG access | $OVER positions are open to everyone. Positions in $USDG need **a stake of at least 100,000 $OVER** on Robinhood Chain mainnet, from the same wallet: stake in the Staking & Airdrop tab of the dashboard, and your stake is recognized within about 5 minutes. If it falls below 100,000 $OVER, for example after an unstake, new $USDG positions stop within about 30 minutes, and positions already open run to the end (see [Staking](13-staking.md)). |

> [!WARNING]
> Always check the token address before you swap. A look-alike token shares the start and the end of the $USDG address, so always check the whole address.

A short **How to play** explainer opens on your first visit, and a **guided tour** walks the terminal step by step; replay either from Settings any time.

Full guide: [docs.overcall.io/access](https://docs.overcall.io/access)

## Testnet demo

The testnet is Overcall's free demo: the same app, products and rules on Robinhood Chain's test network, played with test tokens that have no value. Use it to learn the terminal and practice your reads before you trade on mainnet. Everything you do on mainnet works on the testnet too (drawing channels, predictions, early closes, the dashboard, sharing and watch links), prices come from the same kind of decentralized oracle reports, and every position settles onchain, on the test network.

To start, open the testnet app and connect a wallet: it asks your wallet to switch to Robinhood Chain Testnet, and to add it first if needed. Get free test ETH for gas, then claim tOVER in the Balance tab and draw your first channel.

| Setting | Robinhood Chain Testnet |
| --- | --- |
| Network name | Robinhood Chain Testnet |
| Chain ID | 46630 |
| RPC URL | `https://rpc.testnet.chain.robinhood.com/rpc` |
| Currency symbol | ETH (test ETH) |
| Block explorer | <https://explorer.testnet.chain.robinhood.com> |
| App | <https://testnet.overcall.io> |

| Item | Testnet details |
| --- | --- |
| Gas | Test ETH, free from the [Robinhood Chain testnet faucet](https://faucet.testnet.chain.robinhood.com/). |
| tOVER | The testnet twin of $OVER. Claim it from the faucet in the Balance tab of the app, and top up when it refills. |
| tUSDG | The testnet twin of $USDG. It comes from the same faucet for wallets with 100,000 $OVER or more staked on mainnet. |
| Multiplier cap | tOVER positions are capped at 50× instead of the 25× mainnet cap; every other term matches mainnet (see [Parameters and limits](03-parameters-and-markets.md)). |
| Records | Testnet positions, channels and leaderboards are separate from mainnet. |
| Contract addresses | Listed beside the mainnet ones on [Contracts and addresses](09-contracts.md). |

> [!NOTE]
> tOVER and tUSDG exist only on the testnet and have no value.

Full guide: [docs.overcall.io/testnet](https://docs.overcall.io/testnet)

<sub>Source: [docs.overcall.io/play](https://docs.overcall.io/play), [docs.overcall.io/terminal](https://docs.overcall.io/terminal), [docs.overcall.io/watch](https://docs.overcall.io/watch), [docs.overcall.io/dashboard](https://docs.overcall.io/dashboard), [docs.overcall.io/identity](https://docs.overcall.io/identity), [docs.overcall.io/share](https://docs.overcall.io/share), [docs.overcall.io/access](https://docs.overcall.io/access), [docs.overcall.io/testnet](https://docs.overcall.io/testnet)</sub>

---

[← Roadmap](14-roadmap.md) · [Contents](../README.md#documentation) · [FAQ →](16-faq.md)
