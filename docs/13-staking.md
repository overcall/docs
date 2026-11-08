# Staking

Stake $OVER on Robinhood Chain mainnet to earn a share of real platform revenue: 25% of the fees from $OVER positions go to stakers, paid in $OVER. A stake of 100,000 $OVER or more also unlocks $USDG positions.

| | In short | Detail |
| --- | --- | --- |
| **Rewards** | From real fees | 25% of the fees from $OVER positions, the open fee and the profit fee net of the creator royalty, go to stakers, so rewards follow live platform volume, not token emissions. |
| **Payout** | $OVER, streamed over 24 hours | Each fee is paid out over the next 24 hours to whoever is staked meanwhile, pro rata to stake and time. Claim any time, or add your rewards to your stake. |
| **Access** | $USDG at 100,000 $OVER | Stake 100,000 $OVER or more, and the same wallet can open positions in $USDG as well as $OVER. |
| **Exit** | Unstake any time | Instantly, in one transaction, with no lock: your $OVER goes straight back to your wallet. |

## How staking works

Stake from the [**Staking & Airdrop**](https://app.overcall.io/dashboard/staking) tab of the dashboard, with $OVER in your wallet on Robinhood Chain mainnet. Staking is non-custodial and onchain: you hold the keys, every stake settles onchain, and your principal is never at risk, because staked $OVER stays yours. Unstake any time, instantly, and your $OVER goes straight back to the same wallet. While it is staked, your $OVER is out of circulation, a supply sink.

## Rewards from real fees

Staking rewards come from platform revenue, not from new tokens: 25% of the fees from $OVER positions go to stakers: the open fee and the profit fee, net of the channel creator's royalty. The early-close penalty and lost stakes go to the vault's capital and are not shared. The busier the platform, the more there is to share.

| | How it works |
| --- | --- |
| **Paid in** | $OVER, from the $OVER vault. |
| **Stream** | Each fee is paid out evenly over the next 24 hours to whoever is staked meanwhile, pro rata to stake and time. A stake added just before a large fee and removed right after earns only for the time it was staked. |
| **Claim** | Any time: your earned $OVER goes to your wallet. |
| **Compound** | Add your earned $OVER to your stake instead of claiming it. |
| **$USDG positions** | 25% of the fees from $USDG positions is swapped into $OVER (buybacks); it is not paid to stakers. |
| **Earlier fees** | Fees booked before the new staking contract went live stay protocol revenue. |

The Staking page shows your rewards in its **Claim rewards** tab, next to Stake and Unstake: what you can claim now and what you have earned all-time.

## Moving from the old staking contract

Rewards are paid by a new staking contract; its mainnet address will be published on [Contracts and addresses](09-contracts.md#addresses) at launch. The first staking contract, [0x2165…b306](https://robin.etherscan.io/address/0x2165E659406F6B4F122F10A540B634252249b306), has no reward logic and cannot be upgraded, so it stays for withdrawals only: you can still unstake from it at any time, but not stake into it. To earn rewards, move your stake: unstake from the old contract and stake the same $OVER into the new one, two transactions.

## Staking 100,000 $OVER unlocks $USDG positions

Stake **100,000 $OVER or more** on Robinhood Chain mainnet, and the same wallet can open positions in $USDG as well as $OVER, both when you draw a channel and when you predict, and claim tUSDG on the [testnet demo](15-using-the-app.md#testnet-demo).

| When | What happens |
| --- | --- |
| A new stake is made | It is recognized within about 5 minutes. |
| Your stake falls below 100,000 $OVER, for example after an unstake | New $USDG positions stop within about 30 minutes; positions already open run to the end. |

## The Genesis airdrop

Staking also powered the **Genesis airdrop**, 1% of the $OVER supply shared among stakers and testnet players. Points closed on Oct 19, 12:00 UTC. Your allocation, its daily vesting and the Claim button live on the same Staking & Airdrop tab. See [Genesis airdrop](https://docs.overcall.io/airdrop).

<sub>Source: [docs.overcall.io/staking](https://docs.overcall.io/staking)</sub>

---

[← Tokenomics](12-tokenomics.md) · [Contents](../README.md#documentation) · [Roadmap →](14-roadmap.md)
