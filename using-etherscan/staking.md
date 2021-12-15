# Stake Your CTDL (3, 3)

Sometimes, the Citadel website might not be accessible due to hosting issues. Fear not, you can still interact with the Citadel contracts to perform certain actions such as staking. In this guide, we will show you how to stake CTDL tokens via [Etherscan](https://etherscan.io).

If you have never staked CTDL before, there are two steps involved:

1. Approve the staking contract to spend your CTDL tokens.
2. Stake your CTDL tokens.

If you have staked CTDL before, there is only one step to perform: Stake your CTDL tokens.

## How to Approve CTDL Spending via Etherscan

1. Go to the [Write Contract section of the CTDL token contract](https://etherscan.io/address/#writeContract).
2. Check and ensure your selected network is "Ethereum Mainnet" in your wallet. Then press **Connect to Web3** to connect your wallet if you haven't done so.
3. Once it is connected, select the third option _approve_.
4. On the _spender (address)_ field, we would fill in the [staking contract address](../contracts/staking.md#staking). Enter this value: XXXX
5. On the _amount (uint256)_ field, fill in the amount of CTDL you would like the staking contract to spend on your behalf, and multiply it by 1e9. If you don't want to repeat this step whenever you want to stake, you can choose a very large value. Let's say you want to allow the contract to spend up to 1e9 CTDL on your behalf, you would enter: **1000000000000000000**
6. Click **Write**.
7. Sign the transaction on Metamask and wait for it to complete.

## How to Stake CTDL via Etherscan

1. Go to the [Write Contract section of the staking contract](https://etherscan.io/address/#writeContract).
2. Check and ensure your selected network is "Ethereum Mainnet" in your wallet. Then press **Connect to Web3** to connect your wallet if you haven't done so.
3. Once it is connected, select the _stake_ option.
4. On the _\_amount (uint256)_ field, fill in the amount you wish to stake, and multiply it by 1e9. For example, if you want to stake 1 CTDL, fill in the value: **1000000000**
5. Click **Write**.
6. Sign the transaction on Metamask and wait for it to complete.
