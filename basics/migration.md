# V2 Migration

## Why do I need to migrate?

V2 migration introduces new features such as on-chain governance and auto-staking
for bonds.

Transitioning from sCTDL V1 to gCTDL allows for multiple bonds to be taken at one
time, as opposed to one bond per vesting period as it was in v1.

Partial liquidity will remain for v1 CTDL while the migration is in progress. This
provides sufficient liquidity for borrowers to close or move their borrowing
position.

You can read more about this on the [Citadel Medium page](https://olympusdao.medium.com/introducing-olympus-v2-c4ade14e9fe).

{% hint style="info" %}
You have **two months to migrate after V2 launch.** If you don't, your sCTDL V1
balance will stop rebasing, but the difference will be honored when you migrate.
{% endhint %}

{% hint style="info" %}
For this article, we added V1 and V2 after each token name to help you differentiate
between the old and new tokens. Partner websites, price aggregators, or your wallet
will not display the version information.
{% endhint %}

## What is the TLDR?

- wsCTDL V1 (wrapped, staked CTDL) will be replaced by gCTDL (Governance CTDL). They
function exactly the same, but gCTDL is set up for on-chain governance.

- CTDL and sCTDL tokens will have their identical V2 counterparts. CTDL V1 becomes
CTDL V2, and sCTDL V1 becomes sCTDL V2.

- Token tickers will remain the same for V1 tokens. For example, after migration,
your wallet will show "CTDL" instead of "CTDL V1". Make sure to update the token
contract in your wallet with the [V2 addresses](../contracts/tokens.md) to show
your balances.

- When migrating CTDL V1 and/or sCTDL V1, you will get gCTDL in return. Although
the token balance will be different (gCTDL price is calculated differently, which
is based on the Current Index), the **dollar amount remains the same.**

- After the migration, CTDL V1 pools such as CTDL-DAI will utilize CTDL V2. This applies
to new bonds as well. Partners like Abracadabra will only accept new deposits in
gCTDL. So, you will need to migrate if you want to use these features. Otherwise,
you can sit tight and migrate only when you want to.

## What if I don't migrate?

You don't get to enjoy the new features introduced by V2. Some partners such as
Rari Capital will only accept V2 tokens once they are deployed, so you would
need to migrate if you want to spend more tokens (e.g. make new deposits) on these
platforms.

## Gas fees are high now, will I lose my rebase rewards if I delay the migration?

No, you can migrate at your leisure once it goes live. The smart contract will
keep track of your entitled rebase rewards so you wouldn't miss any of them.

## What is the migration process?

When the migration is live, the Citadel front-end will be updated to allow the
migration of all your V1 tokens (i.e. CTDL, sCTDL, and wsCTDL) to gCTDL.

The migration process requires two steps: one to approve the contract for each
of your V1 tokens, and another that actually migrates all your tokens to gCTDL.

{% hint style="info" %}
Each V1 token type requires its own approval step. For example, if you have CTDL
V1 and sCTDL V1 in your wallet, you need to perform two token approvals, but only
one migration operation (three transactions in total).
{% endhint %}

## Can I migrate a specific type of V1 token and leave out the others?

No. You can either migrate all your V1 tokens (i.e. CTDL, sCTDL, and wsCTDL) or none
at all.

## Can I switch back to V1 tokens after migrating them to gCTDL?

No, you can't switch back from gCTDL to V1 tokens through our migration tool.

## Can you walk me through an example of how much gCTDL I can expect from the migration?

Assuming you have 20 CTDL V1, 20 sCTDL V1, and 20 wsCTDL, and the [Current Index](https://docs.olympusdao.finance/main/basics/basics#how-do-i-track-my-rebase-rewards)
is 10.

- 20 CTDL V1 = 2 gCTDL. Take your 20 CTDL and divide it by the Current Index to get
your gCTDL.

- 20 sCTDL V1 = 2 gCTDL. Take your 20 sCTDL and divide it by the Current Index to
get your gCTDL.

- 20 wsCTDL = 20 gCTDL. 1 wsCTDL is equivalent to 1 gCTDL.

{% hint style="info" %}
As a reminder, if you're migrating from a non-index-based token (CTDL, sCTDL) to an
index-based token (gCTDL), you won't receive the same amount of tokens after the
migration, but they still worth the same in dollar term.
{% endhint %}

## Will my gCTDL still earn rebase rewards?

Yes. Although gCTDL does not change in quantity upon rebase like sCTDL does, it
still earns you rebase rewards. This is because the price of gCTDL is tied to the
Current Index:

$$
gCTDL_{price} = CTDL_{price} * CurrentIndex
$$

Every rebase event will cause the Current Index to go up, and your gCTDL is worth
more as a result (provided that CTDL's price stays constant).

## How are bonds affected after the migration?

In V2, you can purchase multiple bonds of the same type without resetting the
bond vesting period.

Also, there is no need to claim bond rewards and stake them manually, as this process
will be automated. The bonders will receive their entitled sCTDL at the end of the
vesting period.

Learn more about how bonds will behave in V2 from the [Citadel Medium page](https://olympusdao.medium.com/introducing-olympus-v2-c4ade14e9fe).

## Is Citadel V2 audited?

All V2-related contracts are live, and some of them are still under audit process.
We are working with Runtime Verification for the audit, and the results will be
published once they become available.
