# Developers and agents

Overcall is built for humans and AI agents alike: everything a wallet can do, a program can do, because the rules are a contract and the data is onchain events and signed reports. There is no proprietary API between you and the chain; the one exception is the entry permit a $USDG position needs, which you fetch from the public API.

## Trade: straight to the contract

Open and close positions by calling the engine directly from your wallet, after approving the vault of the position's currency; the operator brings the signed price report that binds your entry. The ABI is all you need, plus an entry permit from the public API for a $USDG position, which it issues to wallets with 100,000 $OVER or more staked.

## Read: live GraphQL, no key

Prices, the activity feed, positions with their currency, each currency's terms and the $OVER vault's stats are served by a public GraphQL API, queries and live subscriptions, no key. Every vault's own state is onchain. Query the API, or read the events directly from the chain and recompute anything yourself.

## Reproduce: recompute any result

Download the model file pinned by its onchain hash and recompute any multiplier from the signed quote, report and shape. Every result is verifiable, not trusted.

Because the odds, a position's terms and the payout math are all onchain and deterministic, an agent can price a position, decide, and settle without trusting any intermediary. The model parameters are pinned by a hash onchain, so an agent can recompute any multiplier from the signed quote and report and check it against the contract.

## Settlement identity

```text
depositIn + fromCapital = toPlayer + toRevenue + toRoyalty + toCapital
```

Holds on every settlement, in each currency's vault, to the smallest unit.

## Where to start

The ABI of every contract is on its verified explorer page: open any address on [Contracts and addresses](09-contracts.md#addresses) and read its Contract tab. The public GraphQL API answers at these endpoints, with no key:

| Network | GraphQL endpoint |
| --- | --- |
| Mainnet | https://api.overcall.io/graphql |
| Testnet demo | https://api.overcall.dev/graphql |

<sub>Source: [docs.overcall.io/developers](https://docs.overcall.io/developers)</sub>

---

[← Contracts and addresses](09-contracts.md) · [Contents](../README.md#documentation) · [The $OVER token →](11-over-token.md)
