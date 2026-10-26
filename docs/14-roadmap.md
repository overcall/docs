# Roadmap

Where the platform is and where it is going. Everything already shipped is checked, work in progress is marked as such, and everything ahead is planned.

> [!NOTE]
> Timeframes are directional, not commitments, and the plan evolves with the platform.

## Pre-TGE

Shipped and proven on the testnet before the TGE: the full engine, the terminal, both products, the dashboard, accounts and content, and the public opening.

### Engine (rails)

- [x] **Full smart-contract stack**: separate contracts for the game logic, value custody, asset and model configuration, roles and timelocked upgrades, so every rule of the game is enforced onchain, not by us
- [x] **Full-reserve vault**: a full-reserve vault per currency custodies every deposit, settlement payout, creator royalty and protocol fee in that currency, and reserves each payout up front, so the platform can always pay what it owes
- [x] **Onchain model registry**: the pricing model is published and pinned onchain, so anyone can recompute their multiplier
- [x] **Oracle-anchored entries**: entries bind to signed Chainlink Data Streams reports, so no party picks your entry price
- [x] **Autonomous operator**: quoting, binding, liquidations and settlement run unattended around the clock
- [x] **Live data pipeline**: the price engine and indexer keep every client on one live feed and continuously verify the offchain view against the chain
- [x] **GraphQL API**: public reads and live subscriptions for the app and anyone building on it
- [x] **AWS infrastructure**: production co-located with the oracle origin, deployed as code on every merge
- [x] **Testnet faucet**: free tOVER, the testnet twin of $OVER, so anyone can trade the full system end to end, and tUSDG, the testnet twin of $USDG, for wallets with 100,000 $OVER or more staked

### Terminal

- [x] **View modes**: Focus auto-frames the action, Manual gives full navigation and drawing tools
- [x] **Chart navigation**: interval selector and zoom tools
- [x] **Chart styles**: line and candles
- [x] **Positions panel**: Channels and Prediction taxonomy with product filters
- [x] **Asset selector**: crypto and tokenized stocks, with filters
- [x] **Watch**: spectate any position live via shareable public /position and /prediction links
- [x] **Themes**: dark and light
- [x] **Platform navigation**: one-click dashboard access from anywhere in the app
- [x] **Guided tour**: interactive walkthrough of the whole interface
- [x] **Wallet connect**: injected wallet support

### Products

- [x] **Channels**: draw your own channel on a live chart and back it to Survive or Breach; both sides priced from its survival probability
- [x] **Channels Prediction**: open a position on someone else's live channel, Survive or Breach, at the same probability-honest odds

### Dashboard

- [x] **Overview home**: account and platform at a glance
- [x] **Platform metrics**: live platform stats, vault performance and the activity feed
- [x] **User space**: balances, open positions, history and activity
- [x] **Leaderboard**: skill ranking by realized P&L
- [x] **Settings**: identity and preferences

### Accounts & social

- [x] **X connectivity**: link an X profile and appear by handle across the platform
- [x] **Wallet profiles**: a shareable public profile for every wallet, with profile share cards
- [x] **Share on X**: position and prediction result cards rendered from real position geometry
- [x] **Creator royalties**: a channel earns its creator royalties from predictions taken on it
- [x] **Access system**: invite-code gate for the private testnet

### Brand & content

- [x] **Landing page**: the platform story at overcall.io
- [x] **Documentation**: full product documentation, from quick start to contracts

### Milestone

- [x] **Public testnet opening**: the invite gate lifts and anyone can trade

## TGE ↔ Mainnet

- [x] **$OVER TGE**: token generation event on Virtuals; $OVER is live on Robinhood Chain mainnet at [0x6245…3a4F](https://robin.etherscan.io/address/0x6245Db7f52379bD9757c9DdcE6519768FfaB3a4F)
- [x] **Airdrop campaign**: launched together with the TGE; points closed Oct 19, 12:00 UTC (see [Genesis airdrop](https://docs.overcall.io/airdrop))
- [x] **Staking on mainnet**: stake $OVER for the airdrop, and 100,000 $OVER or more to unlock $USDG positions
- [x] **$USDG positions**: positions in $USDG alongside $OVER, for wallets with 100,000 $OVER or more staked
- [x] **Data Streams on mainnet**: Chainlink Data Streams integration for Robinhood mainnet
- [x] **Partnerships**: first ecosystem partnerships and joint campaigns
- [x] **Architecture iteration**: continuous refinement from feedback and testing

## Mainnet day

- [x] **Mainnet open to everyone**: any wallet trades at [app.overcall.io](https://app.overcall.io) in $OVER, and in $USDG with a stake of 100,000 $OVER or more
- [x] **Crypto asset class live**: six crypto markets live on mainnet: BTC, ETH, BNB, SOL, HYPE and VIRTUAL
- [x] **Vault seeding**: of the 150M $OVER Platform vault liquidity, 50M is in the $OVER vault and 100M in the $OVER reserve; the $USDG vault has its own capital
- [x] **Full stack on mainnet**: both products and the data pipelines live
- [x] **Two environments**: mainnet and the testnet run side by side, and the testnet becomes a free demo (see [Testnet demo](15-using-the-app.md#testnet-demo))

## Post-mainnet (3-month horizon)

- [ ] **Airdrop distribution**: final allocations published, claiming live with daily vesting over 15 days, until Nov 19 `In progress`
- [ ] **Staking rewards transformation**: staking earns a share of platform fees: 25% of the profit fees from $OVER positions go to stakers `In progress`
- [ ] **New platform product**: built on the same rails
- [ ] **Stock asset class**: the tokenized stock class launches on mainnet
- [ ] **Crypto expansion**: the crypto class expands with more assets, starting with CASHCAT, added Oct 25 `In progress`
- [ ] **Multichain**: platform and token expand to a second blockchain
- [ ] **Agent playbook**: developer reference, API surface and quickstarts for AI agents
- [ ] **Agent integrations**: first ecosystem agents trading on the platform
- [ ] **Community features**: new features shipped on community demand
- [ ] **Longer durations**: extended position duration bounds
- [ ] **$OVER perps**: a new market and a hedge for the price risk of open $OVER positions

## Post-mainnet (6-month horizon)

- [ ] **Asset expansion**: 25+ crypto and stock assets in total
- [ ] **CEX listing**: 1+ centralized exchange listing for $OVER
- [ ] **Fiat on-ramp**: direct fiat funding integration
- [ ] **Next products**: further platform products on the same engine

## Post-mainnet (moving forward)

- [ ] **Community demand**: further products and features as the platform grows

<sub>Source: [docs.overcall.io/roadmap](https://docs.overcall.io/roadmap)</sub>

---

[← Staking](13-staking.md) · [Contents](../README.md#documentation) · [Using the app →](15-using-the-app.md)
