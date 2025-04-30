# Silo Finance Mitigation Review
- Total Prize Pool: $8,000 in USDC
  - Warden awards: $6,800 in USDC
  - Judge awards: $950 in USDC
  - Scout awards: $250 in USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Starts May 01, 2025 20:00 UTC
- Ends May 05, 2025 20:00 UTC

## Important note 

Each warden must submit a mitigation review for *every* individual item listed in the `Scope` section below. **Incomplete or insufficient mitigation reviews will not be eligible for awards.**

## Scope

### Branch

https://github.com/silo-finance/silo-contracts-v2

### Mitigation of High & Medium Severity Issues

Mitigations of all High and Medium issues listed here will be considered in-scope:

| Fix | Mitigation of | Notes | 
| ----------- | ------------- | ----------- |
| [PR 1162](https://github.com/silo-finance/silo-contracts-v2/pull/1162) (solution) and [PR 1173](https://github.com/silo-finance/silo-contracts-v2/pull/1173) (optimization) | [F-11: Deflation attack](https://code4rena.com/audits/2025-03-silo-finance/submissions/F-11) | Ensure that deposit does not generate zero shares | 
| [PR 1166](https://github.com/silo-finance/silo-contracts-v2/pull/1166) | [F-17: Supply function doesn't account for market maxDeposit when providing assets to it](https://code4rena.com/audits/2025-03-silo-finance/submissions/F-17) | Account for `maxDeposit` when doing deposit | 
| [PR 1163](https://github.com/silo-finance/silo-contracts-v2/pull/1163) | [F-26: SiloVault will incorrectly accrue rewards during user transfer/transferFrom actions due to unsynced totalSupply()](https://code4rena.com/audits/2025-03-silo-finance/submissions/F-26) | Ensure we can deposit 100% of the CAP | 
| [PR 1165](https://github.com/silo-finance/silo-contracts-v2/pull/1165) | [F-57: SiloVault.sol :: Markets with assets that revert on zero approvals cannot be removed](https://code4rena.com/audits/2025-03-silo-finance/submissions/F-57) | Reset approval to 1 wei | 
 

## Out of Scope

- [F-195: Lack of slippage and deadline protection in deposit(), withdraw() and redeem()](https://code4rena.com/audits/2025-03-silo-finance/submissions/F-195)
- [F-207: Incorrect reward distribution due to feeShares minting order](https://code4rena.com/audits/2025-03-silo-finance/submissions/F-207)
