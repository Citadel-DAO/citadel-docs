# Purchase A Bond (1, 1)

Bonds allow users to buy CTDL from the protocol at a discount by trading it with i) liquidity (LP tokens) or ii) other assets. The former is called [liquidity bonds](../../contracts/bonds.md#ctdl-dai-lp-bond) and the latter [reserve bonds](bond\_dai.md).

Bonds take roughly 15 epochs to vest, and CTDL tokens are vested linearly to the user over that period. Liquidity bonds help the protocol to accumulate and lock liquidity, while reserve bonds allow the protocol to grow its treasury, and thus its RFV faster.

Citadel offers five types of bonds on its website:

* [DAI bond](bond\_dai.md)
* [wETH bond](bond\_weth.md)
* [CTDL-DAI LP bond](ohm-dai-lp-bond.md)

## **How to Redeem**

Go to Bond page and select the bond type you have purchased. Select the "Redeem" tab. Then, click "Claim Rewards" to claim all of your available rewards.

## Reading the Info

**Balance** is your balance of SLP tokens. This is the asset used to create a bond.

**Bond Price** is the price of CTDL you get from bonding. You can calculate the bond price using the following formulae:

* SLP Bond: (Value of your SLP token / CTDL you'll get from bonding)
* DAI Bond: (Value of your DAI token / CTDL you'll get from bonding)

**Market Price** is the market price of CTDL.

**You Will Get** tells you how many CTDL you will get from bonding.

**Debt Ratio** measures the total amount of CTDL created from bonds that have yet to be paid out by the protocol. The debt ratio is calculated differently for SLP bond and DAI bond:

* SLP Bond: (CTDL created from unredeemed bonds / CTDL total supply)
* DAI Bond: (CTDL created from unredeemed bonds / CTDL circulating supply)

**Vesting Term** measures the period a bond takes to fully redeem. This number is in Ethereum blocks. 33110 blocks is approximately 5 days or 15 epochs.

**Discount** is the difference between the bond price and the market price. In the screenshot above, bonding would give you a 10.63% discount versus buying the same amount of CTDL from the market.

**Pending Rewards** is the amount of CTDL you are entitled to receive from bonding.

**Claimable Rewards** is the amount of CTDL that you can claim now. This amount keeps increasing as CTDL is vested to you over the bonding period.

**Full Bond Maturation** refers to the Ethereum block when the bond is fully redeemable.
