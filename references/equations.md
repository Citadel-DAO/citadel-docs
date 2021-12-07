# Equations

## Staking

$$
deposit = withdrawal
$$

Swaps between CTDL and sCTDL during staking and unstaking are always honored 1:1. The amount of CTDL deposited into the staking contract will always result in the same amount of sCTDL. And the amount of sCTDL withdrawn from the staking contract will always result in the same amount of CTDL.

$$
rebase = 1 - ( ohmDeposits / sCTDLOutstanding )
$$

The treasury deposits CTDL into the distributor. The distributor then deposits CTDL into the staking contract, creating an imbalance between CTDL and sCTDL. sCTDL is rebased to correct this imbalance between CTDL deposited and sCTDL outstanding. The rebase brings sCTDL outstanding back up to parity so that 1 sCTDL equals 1 staked CTDL.

## Bonding

$$
bond Price = 1 + Premium
$$

CTDL has an intrinsic value of 1 DAI, which is roughly equivalent to $1. In order to make a profit from bonding, Citadel charges a premium for each bond.

$$
Premium = debt Ratio * BCV
$$

The premium is derived from the debt ratio of the system and a scaling variable called [BCV](https://docs.olympusdao.finance/references/glossary#bcv). BCV allows us to control the rate at which bond prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new CTDL is minted from the profit and subsequently distributed among all stakers.

$$
debt Ratio = bondsOutstanding/ohmSupply
$$

The debt ratio is the total of all CTDL promised to bonders divided by the total supply of CTDL. This allows us to measure the debt of the system.

$$
bondPayout_{reserveBond} = marketValue_{asset}\ /\ bondPrice
$$

Bond payout determines the number of CTDL sold to a bonder. For [reserve bonds](https://docs.olympusdao.finance/references/glossary#reserve-bonds), the market value of the assets supplied by the bonder is used to determine the bond payout. For example, if a user supplies 1000 DAI and the bond price is 250 DAI, the user will be entitled 4 CTDL.

$$
bondPayout_{lpBond} = marketValue_{lpToken}\ /\ bondPrice
$$

For [liquidity bonds](https://docs.olympusdao.finance/references/glossary#liquidity-bonds), the market value of the LP tokens supplied by the bonder is used to determine the bond payout. For example, if a user supplies 0.001 CTDL-DAI LP token which is valued at 1000 DAI at the time of bonding, and the bond price is 250 DAI, the user will be entitled 4 CTDL.

## CTDL Supply

$$
CTDL_{supplyGrowth} = CTDL_{stakers} + CTDL_{bonders} + CTDL_{DAO} + CTDL_{pohmExercise}
$$

CTDL supply does not have a hard cap. Its supply increases when:

* CTDL is minted and distributed to the stakers.
* CTDL is minted for the bonder. This happens whenever someone purchases a bond.
* CTDL is minted for the DAO. This happens whenever someone purchases a bond. The DAO gets the same number of CTDL as the bonder.
* CTDL is minted for the team, investors, advisors, or the DAO. This happens whenever

  the aforementioned party exercises their pCTDL.

$$
CTDL_{stakers} = CTDL_{totalSupply} * rewardRate
$$

At the end of each epoch, the treasury mints CTDL at a set [reward rate](https://docs.olympusdao.finance/references/glossary#reward-rate). These CTDL will be distributed to all the stakers in the protocol. You can track the latest reward rate on the [Citadel Policy dashboard](https://dune.xyz/shadow/Citadel-Policy).

$$
CTDL_{bonders} = bondPayout
$$

Whenever someone purchases a bond, a set number of CTDL is minted. These CTDL will not be released to the bonder all at once - they are vested to the bonder linearly over time. The bond payout uses a different formula for different types of bonds. Check the [bonding section above](equations.md#bonding) to see how it is calculated.

$$
CTDL_{DAO} = CTDL_{bonders}
$$

The DAO receives the same amount of CTDL as the bonder. This represents the DAO profit.

$$
CTDL_{pohmExercise} = pCTDL + DAI
$$

The individual would supply 1 pCTDL along with 1 DAI to mint 1 CTDL. The pCTDL is subsequently burned. Read [this Medium article](https://olympusdao.medium.com/what-is-poh-16b2c38a6cd6) for more information on pCTDL.

## Backing per CTDL

$$
CTDL_{backing} = treasuryBalance_{stablecoin} + treasuryBalance_{otherAssets}
$$

Every CTDL in circulation is backed by the Citadel treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

$$
treasuryBalance_{stablecoin} = RFV_{reserveBond} + RFV_{lpBond}
$$

The stablecoin balance in the treasury grows when bonds are sold. [RFV](https://docs.olympusdao.finance/references/glossary#rfv) is calculated differently for different bond types.

$$
RFV_{reserveBond} = assetSupplied
$$

For reserve bonds such as DAI bond and FRAX bond, the RFV simply equals to the amount of the underlying asset supplied by the bonder.

$$
RFV_{lpBond} = 2sqrt(constantProduct) * (\%\ ownership\ of\ the\ pool)
$$

For LP bonds such as CTDL-DAI bond and CTDL-FRAX bond, the RFV is calculated differently because the protocol needs to mark down its value. Why? The LP token pair consists of CTDL, and each CTDL in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating CTDL are backed, the protocol marks down the value of these LP tokens, hence the name _risk-free_ value \(RFV\).

