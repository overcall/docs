# Prediction

Every open channel is a two-sided market. Take a view on someone else's call: back it to **Survive**, or back a wall to **Breach**.

## Predict on any live channel

Both sides are priced in the open from the channel's own survival probability. Take it in $OVER or, if you stake 100,000 $OVER or more, in $USDG: the currency belongs to your prediction, not to the channel.

| Side | You back | What it means |
| --- | --- | --- |
| **Survive** | the channel to hold | Survive pays if the channel keeps every wall to the very end. You are backing the caller's read. |
| **Breach** | a wall to break | Breach pays if a wall gets hit before the end. One channel, two sides, priced in the open. |

One survival probability prices both sides. When the price drifts toward a wall, P falls, so Survive pays more and Breach pays less, live.

**That is the whole idea.** For the odds, see [Prediction odds](#prediction-odds); for how a prediction resolves and closes, see [Settling and closing](#settling-and-closing). To find channels to back, see [Watch and spectate](15-using-the-app.md#watch-and-spectate).

## Prediction odds

Both sides of a live channel are priced from one number, so they can never drift apart or be arbitraged against each other.

### One probability, both sides

A live channel already has a survival probability **P**, the same number that [priced the position on it](02-channels.md#your-multiplier-the-honest-inverse-of-your-side). Prediction turns that into a two-sided market, each side the honest inverse of its own outcome, less the published spread:

**Prediction odds**

```text
Survive = (1 − δ) / P
Breach  = (1 − δ) / (1 − P)
```

δ is the published spread. Both sides are capped by a ceiling set per currency, and a side priced below the minimum is not offered (see [Parameters and limits](03-parameters-and-markets.md#parameters-and-limits)).

### The odds move as it plays

Entry odds on a running channel price the **time it has already survived** and steepen with the **distance to the nearest wall**: a nearly-finished call pays the Survive side less, and a channel drifting toward a wall pays the Survive side more. Whatever you take is final when your entry binds onchain, and recomputable by anyone from the signed inputs (see [Platform engine](05-engine.md)).

## Settling and closing

A prediction resolves with the channel it backs, and you can leave early for a known amount, just like a [position](02-channels.md#closing-a-position).

| Exit | You collect | When |
| --- | --- | --- |
| Your side wins | stake × odds | Survive: every wall holds to the end<br>Breach: a wall breaks first |
| Close early | mark-to-market × (1 − penalty) | you cash out before it resolves, for a known amount |
| Your side loses | 0 | the channel resolves the other way |

If trading is paused for a review when your side wins, you get your stake at once and the rest is held for the review (see [When trading pauses](07-vault.md#when-trading-pauses)).

### How it settles

If the price touches a wall before the end, **Breach** wins and **Survive** is out, from the same signed proof that liquidates the channel. If it holds to the end, Survive wins.

The channel's creator earns a **royalty** on every winning prediction inside it: 15% of the prediction's profit fee, in the prediction's currency, $OVER or $USDG. It is claimed from the dashboard, and $USDG royalty is swapped into $OVER when you claim it. Draw a channel others want to trade, and it pays you beyond your own ride.

### Close early

You do not have to wait for the end. Close a prediction any time for a mark-to-market amount set by its current win probability, less the early-close penalty, the same way a [position closes](02-channels.md#close-early-mark-to-market).

> [!TIP]
> **Watch, then predict.** Any position has a public watch link that renders the live channel on the real chart, no wallet needed, and the prediction ticket sits right there. See [Watch and spectate](15-using-the-app.md#watch-and-spectate).

<sub>Source: [docs.overcall.io/predict](https://docs.overcall.io/predict), [docs.overcall.io/predict-odds](https://docs.overcall.io/predict-odds), [docs.overcall.io/predict-settle](https://docs.overcall.io/predict-settle)</sub>

---

[← Parameters and markets](03-parameters-and-markets.md) · [Contents](../README.md#documentation) · [Platform engine →](05-engine.md)
