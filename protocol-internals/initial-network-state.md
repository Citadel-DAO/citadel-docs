# Initial Network State

## Alpha State

The initial network features a one-way treasury (money goes in, none comes out), the bonding contract (through which supply increases and profits are produced), and the staking contract (where profits are distributed).

The following are the initial policy states:

*   **BCV**

    [BCV](../references/glossary.md#bcv) varies based on bond types. It is tuned regularly by the Policy team to meet the protocol goals. For example, if the protocol wants to accumulate more liquidity into its treasury, it can lower the BCV for [liquidity bonds](../contracts/bonds.md#ctdl-dai-lp-bond) to increase their bond capacity. To view the BCV targets for different bond types, visit the [Citadel Policy Dune page](https://dune.xyz/shadow/Citadel-Policy).
*   **Bond vesting term**

    It is set to 33110 Ethereum blocks or approximately five days for all bond types.
*   **CTDL distribution**

    Every time someone purchases a bond, the proceed will go to the Citadel treasury. A corresponding amount of CTDL will be minted and distributed to three parties:

    *   Bonder

        The bond purchaser will receive the quoted amount of CTDL linearly over the vesting term.
    *   DAO

        The DAO receives the same amount of CTDL as the bonder. This represents the DAO profit.
    *   Stakers

        After accounting for the CTDL distributed to the bonder and the DAO, the rest will be distributed among all stakers in the protocol.
