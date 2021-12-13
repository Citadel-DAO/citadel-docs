# Stake Your CTDL (3, 3)

Staking allows you to earn CTDL passively via auto-compounding. By staking your CTDL with CitadelDAO, you receive sCTDL (staked CTDL) in return at a 1:1 ratio. After that, your sCTDL balance will increase automatically on every epoch based on the current APY.

## How to Buy CTDL

{% hint style="warning" %}
There are several venues to purchase CTDL: [Sushiswap](https://app.sushi.com/swap), [Uniswap](https://app.uniswap.org/#/swap), or DEX aggregators such as [matcha](https://matcha.xyz). Make sure to **check the slippage first** before buying CTDL, as some venue offers worse rate than the others due to low liquidity.
{% endhint %}

1. Go to [this Sushiswap swap page](https://app.sushi.com/swap?outputCurrency=0x383518188c0c6d7730d91b2c03a03c837814a899). We use Sushiswap as an example here. It is recommended to compare the exchange rate across different DEXes to ensure you are getting the best price.
2. Make sure the output currency is CTDL. You can also copy and paste the CTDL contract address into the output currency field to ensure you are swapping for the right token.
3. You can select any input currency based on your available wallet balance. It is recommended to use DAI as the input currency to minimize the slippage.
4. Select the amount of CTDL you want to swap for. Then click "Approve" and sign the transaction.
5. After the "Approve" transaction has been processed successfully, click "Swap" and sign the transaction.
6. You should see CTDL in your wallet balance now after the swap transaction is successful. If you cannot find it in your wallet, add CTDL contract address to your wallet.

{% hint style="info" %}
The "Approve" transaction is only needed when you swap CTDL for the first time; subsequent swapping only requires you to perform the "Swap" transaction.
{% endhint %}

## How to Stake

1. Go to the Stake page of the CitadelDAO website. Select the "Stake" tab.
2. Enter the amount of CTDL that you would like to stake in the input field. If you would like to stake all your CTDL, press the "Max" button and the input field will be populated with all your available CTDL balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Stake" and sign the transaction. Voila, you have staked your CTDL!

## How to Unstake

1. Go to the Stake page of the CitadelDAO website. Select the "Unstake" tab.
2. Enter the amount of sCTDL that you would like to unstake in the input field. If you would like to unstake all your sCTDL, press the "Max" button and the input field will be populated with all your available sCTDL balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Unstake" and sign the transaction.

_Note: The "Approve" transaction is only needed when staking/unstaking for the first time; subsequent staking/unstaking only requires you to perform the "Stake" or "Unstake" transaction._

## Reading the Info

**APY** tells you the annualized rate of return based on the reward yield. It takes into account the effect of compounding since sCTDL rebases exponentially.

**TVL** measures the dollar amount of all the staked CTDL in Citadel.

**Current Index** allows you to track your gain from staking. The index started from 1 at epoch 0, and increases every epoch. If you staked at genesis (epoch 0) and never unstaked any CTDL, your balance today would be X times greater, where X is the current index. You can use the index to track your position by marking down the index number when you stake and unstake. You divide the index number when you unstake by the index number when you stake to get the ratio by which your sCTDL balance has increased.

**Your Balance** tells you how many unstaked CTDL are in your wallet. This is the maximum amount that you can stake.

**Your Staked Balance** tells you how many staked CTDL are in your wallet. This is the maximum amount that you can unstake.

**Next Rebase** tells you the remaining time until the next rebase.

**Reward Yield** tells you how much your sCTDL balance will increase when the next epoch begins. For example, if you stake 100 CTDL and the upcoming rebase is 0.5427%, your sCTDL balance would increase from 100 to 100.5427.

**ROI (5-Day Rate)** estimates how much your sCTDL balance will increase after 5 days, if the reward yield stays the same during this period. For example, if you stake 100 CTDL and the rate is 8.4577%, your sCTDL balance would increase from 100 to 108.4577 after 5 days.
