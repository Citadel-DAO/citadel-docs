# Unstake sCTDL

Sometimes, the Citadel website might not be accessible due to hosting issues. Fear not, you can still interact with the Citadel contracts to perform certain actions such as unstaking. In this guide, we will show you how to unstake sCTDL tokens via [Etherscan](https://etherscan.io).

If you have never unstaked sCTDL before, there are two steps involved:

1. Approve the staking contract to spend your sCTDL tokens.
2. Unstake your sCTDL tokens.

If you have unstaked sCTDL before, there is only one step to perform: Unstake your sCTDL tokens.

## How to Approve sCTDL Spending via Etherscan

1. Go to the [Write Contract section of the sCTDL token contract](https://etherscan.io/address/#writeContract).
2. Check and ensure your selected network is "Ethereum Mainnet" in your wallet. Then press **Connect to Web3** to connect your wallet if you haven't done so.
3. Once it is connected, select the first option _approve_.
4. On the _spender (address)_ field, we would fill in the [staking contract address](../contracts/staking.md#staking). Enter this value: **XXXXX**
5. On the _amount (uint256)_ field, fill in the amount of sCTDL you would like the staking contract to spend on your behalf, and multiply it by 1e9. If you don't want to repeat this step whenever you want to unstake, you can choose a very large value. Let's say you want to allow the contract to spend up to 1e9 sCTDL on your behalf, you would enter: **1000000000000000000**
6. Click **Write**.
7. Sign the transaction on Metamask and wait for it to complete.

## How to Unstake sCTDL via Etherscan

1. Go to the [Write Contract section of the staking contract](https://etherscan.io/address/#writeContract).
2. Check and ensure your selected network is "Ethereum Mainnet" in your wallet. Then press **Connect to Web3** to connect your wallet if you haven't done so.
3. Once it is connected, select the last option _unstake_.
4. On the _\_amount (uint256)_ field, fill in the amount you wish to unstake, and multiply it by 1e9. For example, if you want to unstake 1 sCTDL, fill in the value: **1000000000**
5. On the _\_trigger (bool)_ field, fill in the value: **true**
6. Click **Write**.
7. Sign the transaction on Metamask and wait for it to complete.
