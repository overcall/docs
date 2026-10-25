# Security

The whole pitch is that you do not have to trust us. Here is what backs that up, and where the real risks are, named outright.

## Never stuck: funds cannot be trapped

A channel that reaches its end settles with no oracle report, so an outage cannot freeze your position. Liquidations are prompt: the operator publishes breach proof in its next batch, so the vault is never left holding a losing position. Two payouts can wait: the rest of a win while trading is paused for a review (your stake is paid at once), and a payout your address cannot receive, which the vault keeps for you to withdraw.

## No custody: only your position is at stake

Only the position you open is ever at risk. The rest of your balance, in either currency, stays yours, and no operator can seize it or your winnings. It is all onchain.

## Roles disclosed: what admin can and cannot do

| Admin can | Admin cannot |
| --- | --- |
| Change the terms for new positions (fees, caps, curves; a position's terms are fixed when it opens) | Touch the price |
| Rotate the operator and the guardian (the role that can pause trading) | Seize your balance |
| Approve or reject a win held for review during a pause (see [When trading pauses](07-vault.md#when-trading-pauses)) | |

## Public math: recompute every result

The payout math, the caps and the settlement rules are in a contract anyone can read, and every result is an onchain event you can recompute from public data.

## Residual risks, stated plainly

- Prompt liquidation depends on the operator publishing breach proof in its next batch; if the operator goes dark, your fallback is reclaiming your deposit after the 7-day settlement window.
- The vault is a loss-bearing counterparty, sized by caps so no single win can sink it, but it can draw down.
- Range is an operator-maintained input, bounded and sizing-only, but it is the one input the platform maintains.
- One pause covers both currencies (see [When trading pauses](07-vault.md#when-trading-pauses)), so a run of wins against the $USDG vault can pause $OVER positions too, and a $USDG request is refused when that vault's free capital cannot reserve its maximum payout.

<sub>Source: [docs.overcall.io/security](https://docs.overcall.io/security)</sub>

---

[← Vault](07-vault.md) · [Contents](../README.md#documentation) · [Contracts and addresses →](09-contracts.md)
