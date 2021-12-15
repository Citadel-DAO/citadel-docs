# Bonds

## DAI Bond

All bond contracts are more or less the same, with the one exception of the assets or LP tokens they manage. The bond contracts handle all deposits and redemptions. Here parameters for monetary policy are configured. Such parameters are for instance the [BCV](../references/glossary.md#bcv) and the max individual payout. Below are listed DAI bond contracts by version, where the latest version represents the currently active contract.

* V1&#x20;

## ETH Bond

Since ETH is not an ERC-20 token itself, our ETH bonds utilize [wETH](https://weth.io). All things being equal to our other bond types, the only exception for ETH bonds is that we do not mint CTDL against wETH taken in to begin with. Below are listed ETH bond contracts by version, where the latest version represents the currently active contract.

* V1

## CTDL / DAI LP Bond

* V1&#x20;

## Redeem Helper

The redeem helper contract is configured with all active bond contract addresses. When calling `redeemAll` all claimable bond rewards are redeemed for the given recipient. Below are listed redeem helper contracts by version, where the latest version represents the currently active contract.

* V1
