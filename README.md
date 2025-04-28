# Silo Finance Mitigation Review
- Total Prize Pool: $8,000 in USDC
  - Warden awards: $6,800 in USDC
  - Judge awards: $950 in USDC
  - Scout awards: $250 in USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Starts April 30, 2025 20:00 UTC
- Ends May 05, 2025 20:00 UTC

## Important note 

Each warden must submit a mitigation review for *every* individual item listed in the `Scope` section below. **Incomplete or insufficient mitigation reviews will not be eligible for awards.**

## Overview of changes [optional]

[ ⭐️ SPONSORS ADD INFO HERE ]
Please provide context about the mitigations that were applied if applicable and identify any areas of specific concern. 

## Scope

### Branch

https://github.com/silo-finance/silo-contracts-v2

### Mitigation of High & Medium Severity Issues

Mitigations of all High and Medium issues listed here will be considered in-scope:

| Fix | Mitigation of | Notes | 
| ----------- | ------------- | ----------- |
| [PR 1162](https://github.com/silo-finance/silo-contracts-v2/pull/1162) (solution) and [PR 1173](https://github.com/silo-finance/silo-contracts-v2/pull/1173) (optimization) | [F-11: Deflation attack](https://code4rena.com/audits/2025-03-silo-finance/submissions/S-454) | Ensure that deposit does not generate zero shares | 
| [PR 1166](https://github.com/silo-finance/silo-contracts-v2/pull/1166) | [F-17: Supply function doesn't account for market maxDeposit when providing assets to it](https://code4rena.com/audits/2025-03-silo-finance/submissions/S-312) | Account for `maxDeposit` when doing deposit | 
| [PR 1165](https://github.com/silo-finance/silo-contracts-v2/pull/1165) | [F-57: SiloVault.sol :: Markets with assets that revert on zero approvals cannot be removed](https://code4rena.com/audits/2025-03-silo-finance/submissions/S-107) | Reset approval to 1 wei | 

### Additional scope to be reviewed
[🔴 EM: Remove this section if the sponsor is only mitigating HMs. Add all relevant PRs/commits to the table below. This can include lows, QA reports, and fixes not included in the C4 audit.  If the finding does not have a finding (or submission) number from the C4 audit, please use the `ADD-01` as the naming convention.]

These are additional changes that will be in scope.

| Fix | Mitigation of | Notes | 
| ----------- | ------------- | ----------- |
| [Commit XXX](https://github.com/your-repo/sample-contracts/pull/XXX) | ADD-01 | This mitigation does XYZ | 

## Out of Scope

- [F-26: SiloVault will incorrectly accrue rewards during user `transfer`/`transferFrom` actions due to unsynced `totalSupply()`](https://code4rena.com/audits/2025-03-silo-finance/submissions/S-566)
