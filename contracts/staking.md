# Staking

## Distributor

The distributor contract receives minted CTDL from the treasury in order to drip-feed rewards to stakers. The reward rate target as of time of writing is set to 3500, which translates to 0.35% of total supply, since the reward rate is defined in tens of thousands. Note that the reward rate determines the rebase rate and that the rebase rate determines the APY. Below are listed distributor contracts by version, where the latest version represents the currently active contract.

* V1&#x20;
* V2&#x20;
* V3
* V4&#x20;

## LP Staking

LP staking is deprecated. You can unstake your LP via Etherscan still.

* V1&#x20;

## Staking

The staking contract for CTDL works with a staking helper contract (). The staking helper contract calls "stake" and then "claim" of the staking contract. When the "stake" function is called, sCTDL is put into a warmup phase and all the information about how much sCTDL a user has staked is stored in the new staking contract. When the "claim" function is called, sCTDL is retrieved from the warmup and then sent to the user's wallet.
