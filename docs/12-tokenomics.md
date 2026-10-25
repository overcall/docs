# Tokenomics

$OVER is the central economic engine of the whole Overcall suite, not a standalone token. $OVER positions settle in it, staking it earns a share of platform fees and unlocks $USDG positions from 100,000 $OVER, and channel royalties are claimed in it, so as the platform scales, utility and value accrue straight back into the token.

## Supply and allocation

The design prioritizes sustained long-term utility over short-term speculation. $OVER has a fixed total supply of 1,000,000,000 $OVER (1B). The full breakdown, with every amount, share and unlock term, is below and laid out over time in the [unlock schedule](#unlock-schedule).

| Allocation | Amount | Share | Unlock |
| --- | --- | --- | --- |
| **Automated Capital Formation**<br>Core protocol liquidity, formed via the Limit Order Program. | 250M | 25.00% | $2M → $160M FDV |
| **Team**<br>Core team allocation. Nothing releases at launch. | 250M | 25.00% | 12-month cliff, then 6 monthly tranches · 16 Sep 27 → 13 Feb 28 |
| **Platform vault liquidity**<br>Backs $OVER payouts: 50M in the onchain $OVER vault, the counterparty to every $OVER position, and 100M in the $OVER reserve. | 150M | 15.00% | 1-month cliff · Unlocks 17 Oct 26 |
| **Liquidity Pool**<br>Floating market liquidity. | 124.1M | 12.41% | Fixed supply, liquid at launch |
| **Sniper Tax Buyback for Team**<br>Sniper-tax revenue bought back for the team. | 75.9M | 7.59% | 3-month cliff, then 9 monthly tranches · 18 Dec 26 → 15 Aug 27 |
| **Trading & MM liquidity**<br>Market-making liquidity for $OVER across venues. | 47.5M | 4.75% | 20% after a 3-month cliff, then 80% over 760 days · Unlocks 17 Dec 26 |
| **Product & development**<br>Funds engineering, infrastructure, and new products. | 32.5M | 3.25% | 1-month cliff, then 720-day vesting · Unlocks 17 Oct 26 |
| **Security & audits**<br>Contract audits, bug bounties, and ongoing security work. | 25M | 2.50% | 20% after a 3-month cliff, then 80% over 760 days · Unlocks 17 Dec 26 |
| **Marketing & growth**<br>User acquisition, campaigns, and growth programs. | 22.5M | 2.25% | 1-month cliff, then 720-day vesting · Unlocks 17 Oct 26 |
| **Partnerships & grants**<br>Ecosystem integrations and grants for teams building with Overcall. | 12.5M | 1.25% | 20% after a 3-month cliff, then 80% over 760 days · Unlocks 17 Dec 26 |
| **Airdrop**<br>The Genesis airdrop for early testnet players and $OVER stakers. See [Genesis airdrop](https://docs.overcall.io/airdrop). | 10M | 1.00% | 1-month cliff · Unlocks 17 Oct 26 |

> [!IMPORTANT]
> **No day-one sell pressure, no emissions.** No team tokens release at launch, held behind a strict 12-month cliff, and the pre-buy buckets begin unlocking no earlier than one month post-TGE. The loop is funded by a transparent, published fee, never inflationary emissions. See [the flywheel](11-over-token.md#the-flywheel).

## Pre-buy allocation

To fund protocol security, expansion, and mainnet execution, 30% of supply was acquired via the bonding curve into strategic protocol buckets, keeping the platform self-sufficient and operational: Platform vault liquidity, Trading & MM liquidity, Product & development, Security & audits, Marketing & growth, Partnerships & grants, and the Airdrop. Each unlocks on its own schedule as listed above, the earliest no sooner than one month after the TGE.

## Unlock schedule

The same cliffs and vesting, in time order: from the TGE on 17 Sep 2026 to the end of the longest vesting track, across the full supply of 1,000,000,000 $OVER. The live docs draw this as a chart of cumulative supply unlocked per allocation.

| When | Allocation | Share | Unlock term |
| --- | --- | --- | --- |
| TGE, 17 Sep 2026 | Liquidity Pool | 12.41% | Fixed supply, liquid at launch |
| $2M → $160M FDV | Automated Capital Formation | 25.00% | Formed via the Limit Order Program |
| 17 Oct 26 | Platform vault liquidity | 15.00% | 1-month cliff |
| 17 Oct 26 | Airdrop | 1.00% | 1-month cliff |
| 17 Oct 26 | Product & development | 3.25% | 1-month cliff, then 720-day vesting |
| 17 Oct 26 | Marketing & growth | 2.25% | 1-month cliff, then 720-day vesting |
| 17 Dec 26 | Trading & MM liquidity | 4.75% | 20% after a 3-month cliff, then 80% over 760 days |
| 17 Dec 26 | Security & audits | 2.50% | 20% after a 3-month cliff, then 80% over 760 days |
| 17 Dec 26 | Partnerships & grants | 1.25% | 20% after a 3-month cliff, then 80% over 760 days |
| 18 Dec 26 → 15 Aug 27 | Sniper Tax Buyback for Team | 7.59% | 3-month cliff, then 9 monthly tranches |
| 16 Sep 27 → 13 Feb 28 | Team | 25.00% | 12-month cliff, then 6 monthly tranches |

## The 15% vault unlock, in the open

The Platform vault liquidity, 15% of supply or 150M $OVER, unlocked about one month after the TGE, timed with the mainnet transition by design. It is not market float or team sell pressure: **all of it is set aside to back $OVER payouts**. 50M $OVER is in the $OVER vault, the counterparty to every $OVER position, and 100M $OVER is in the $OVER reserve, [0x437b…5065](https://robin.etherscan.io/address/0x437bCF676D11FFE5542BfAa842b560e431285065), kept apart for security and for expanding to other chains. The dashboard's Vault + reserve figure counts both. $USDG positions are backed by a separate $USDG vault with its own capital. See [Vault architecture](07-vault.md#vault-architecture) for how the counterparty is sized.

## Staking and the airdrop

Staking went live at the TGE and powered the Genesis airdrop: 1% of supply in three pools.

| Pool | Share of the airdrop |
| --- | --- |
| Stakers | 50% |
| Testnet activity | 25% |
| Channel royalties | 25% |

Points closed on Oct 19, 12:00 UTC; allocations vest daily over 15 days, with 30 days to claim from the start of vesting (see [Genesis airdrop](https://docs.overcall.io/airdrop)). On mainnet, staking earns a share of real protocol revenue: 25% of the profit fees from $OVER positions go to stakers, and a stake of 100,000 $OVER or more also unlocks $USDG positions. Full detail is on [Staking](13-staking.md).

<sub>Source: [docs.overcall.io/tokenomics](https://docs.overcall.io/tokenomics)</sub>

---

[← The $OVER token](11-over-token.md) · [Contents](../README.md#documentation) · [Staking →](13-staking.md)
