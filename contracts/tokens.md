# Tokens

## gCTDL

gCTDL stands for Governance CTDL. It supersedes [wsCTDL](#wsohm) as part of the [v2
migration](../basics/migration.md). gCTDL is wrapped sCTDL V2, which allows you to
use sCTDL V2 on different blockchains. It is priced exactly the same as wsCTDL:

$$
gCTDL_{price} = CTDL_{price} * CurrentIndex
$$

You still collect rebase rewards just as if you had sCTDL, but you won't see your
token balance increase because the increase in value is based on the Current Index
at the time of purchase and sale. [See this FAQ](../basics/basics.md#how-do-i-track-my-rebase-rewards)
for more details.

Below are listed gCTDL contracts by version, where the latest version represents
the currently active contract.

Ethereum:

* V1 [0x0ab8...a52f](https://etherscan.io/address/0x0ab87046fBb341D058F17CBC4c1133F25a20a52f)

Arbitrum One:

* V1 [0x8D9b...5FB1](https://arbiscan.io/token/0x8D9bA570D6cb60C7e3e0F31343Efe75AB8E65FB1)

Avalanche:

* V1 [0x321e...4251](https://snowtrace.io/token/0x321e7092a180bb43555132ec53aaa65a5bf84251)

Fantom:

* V1 [0x91fa...3FDc](https://ftmscan.com/token/0x91fa20244Fb509e8289CA630E5db3E9166233FDc)

Polygon:

* V1 [0xd8cA...5195](https://polygonscan.com/token/0xd8cA34fd379d9ca3C6Ee3b3905678320F5b45195)

{% hint style="info" %}
**Current Index explanation / Why does it show less CTDL for me during migration?**

The Current Index is how many CTDL one would have if they staked 1 CTDL since the
protocol inception. Check out the [Citadel dashboard](https://app.olympusdao.finance/#/dashboard)
for the Current Index value.

Unsure about the gCTDL balance you get after the V2 migration? [Read the FAQ](../basics/migration.md#can-you-walk-me-through-an-example-of-how-much-gohm-i-can-expect-from-the-migration)
for more details about the calculation.
{% endhint %}

## CTDL

If you want to buy CTDL on Sushiswap or any other DEX please make sure the token address of the token you purchase matches the one shown above. Never buy any CTDL token which address you cannot verify yourself. Further, knowing the CTDL token address you can see the list of holders and available exchanges providing liquidity for CTDL on Etherscan. Below are listed CTDL contracts by version, where the latest version represents the currently active contract.

* V1 [0x3835...a899](https://etherscan.io/address/0x383518188c0c6d7730d91b2c03a03c837814a899)

## sCTDL

You receive sCTDL when you stake CTDL at a 1:1 ratio. Adding this address to your wallet allows you to track your sCTDL balance which increases with every rebase. Below are listed sCTDL contracts by version, where the latest version represents the currently active contract.

* DEPRECATED: V1 [0x3193...Fbbe](https://etherscan.io/address/0x31932E6e45012476ba3A3A4953cbA62AeE77Fbbe)
* Current: V2 [0x04f2...111f](https://etherscan.io/address/0x04f2694c8fcee23e8fd0dfea1d4f5bb8c352111f)

## wsCTDL

wsOhm is wrapped staked CTDL.  The non-rebasing wrapper is used to package up staked
CTDL in a non-rebasing container that can be transferred between chains.  Currently,
this token is supported on Ethereum, Arbitrum, and Avalanche (AVAX) networks.
Below are listed wsCTDL contracts by version and network, where the latest version
represents the currently active contract. **Please double check the network** for
the address you are adding.

ETH Mainnet:

* V1 [0xca76...3e65](https://etherscan.io/address/0xca76543cf381ebbb277be79574059e32108e3e65)

Arbitrum L2:

* V1 [0x739c...BC4B](https://arbiscan.io/token/0x739ca6d71365a08f584c8fc4e1029045fa8abc4b)

AVAX Chain:

* V1 [0x8CD3...2073](https://cchain.explorer.avax.network/token/0x8CD309e14575203535EF120b5b0Ab4DDeD0C2073)

# Historical Tokens

The tokens below are only relevant if you've had CTDL from the genesis block.  They're still of interest to everyone.

## aCTDL

When CitadelDAO first launched, alphaCTDL \(aCTDL\) was used as a pre-allocation token which allowed the early participants to lay claim to CTDL. Moving forward aCTDL will serve as the in-game currency of [Alpha Omega](https://medium.com/@alpha_omega/alpha-omega-a-tale-of-two-cities-80a94966376b), a community-led social game that runs on the blockchain. Other than that aCTDL is not relevant to CTDL or the operation of CitadelDAO. Below are listed aCTDL contracts by version, where the latest version represents the currently active contract.

* V1 [0x24ec...792e](https://etherscan.io/address/0x24ecfd535675f36ba1ab9c5d39b50dc097b0792e)

## pCTDL

pCTDL, previously known as pOLY, is the presale token of Citadel. It was used to raise funds from private investors to bootstrap Citadel. You can read more about pCTDL in this [Medium article](https://olympusdao.medium.com/what-is-poh-16b2c38a6cd6). Below are listed pCTDL contracts by version, where the latest version represents the currently active contract.

* V1 [0x3699...c800](https://etherscan.io/token/0x36994486c6e97c170065899d8659a28d7371c800)
