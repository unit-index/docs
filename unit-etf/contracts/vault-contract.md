---
description: Vault Contract Detailed Documentation
---

# Vault Contract

### Overview

The `Vault` contract is a core component of the UNIT project. It is responsible for managing collateral and debt for users, as well as handling liquidation events. The contract also includes flash loan functionality.

### Key Features

1. **Collateral Management**: Users can increase or decrease their collateral using the functions `increaseCollateral` and `decreaseCollateral`.
2. **Debt Management**: Users can increase or decrease their debt using the functions `increaseDebt` and `decreaseDebt`.
3. **Flash Loans**: Flash loans can be taken out using the `flashLoan` function, which also increases the user's debt.
4. **Liquidation**: If a user's account is under-collateralized, it can be liquidated using the `liquidation` function.
5. **Governance**: The contract includes governance functionality, allowing the `gov` address to set various parameters such as the treasury address, liquidation ratio, minimum collateral, and more.

### Functions

#### Governance Functions

* `setGov`: Sets the governance address.
* `setPriceFeed`: Sets the address of the price feed contract.
* `setLiquidationRatio`: Sets the liquidation ratio for a given token.
* `setTreasury`: Sets the treasury address.
* `setMinimumCollateral`: Sets the minimum collateral amount.
* `setLiquidationTreasuryFee`: Sets the fee for liquidation.
* `setFreeFlashLoanWhitelist`: Sets the whitelist status for a given address for free flash loans.
* `upgradeVault`: Transfers tokens to a new vault contract.

#### Collateral and Debt Management Functions

* `increaseCollateral`: Increases the collateral for a given token for the sender's account.
* `decreaseCollateral`: Decreases the collateral for a given token from the sender's account.
* `increaseDebt`: Increases the debt for a given token for the sender's account.
* `decreaseDebt`: Decreases the debt for a given token for the sender's account.

#### Flash Loan Functions

* `flashLoan`: Allows the sender to borrow an amount of a given token and increases the sender's debt by the borrowed amount.
* `flashLoanFrom`: Similar to `flashLoan`, but allows an approved operator to initiate the flash loan on behalf of another account.
* `flashLoanAssets`: Allows the sender to borrow an amount of a given token without increasing the sender's debt.

#### Liquidation Functions

* `liquidation`: Liquidates an under-collateralized account, burning the debt and transferring the collateral to a specified address.

#### Utility Functions

* `tokenToTinu`: Converts a token amount to a TINU amount based on the current price.
* `getPrice`: Returns the current price of a given token.
* `transferVaultOwner`: Transfers ownership of an account's collateral and debt to a new account.

### Events

* `IncreaseCollateral`: Emitted when a user increases their collateral.
* `DecreaseCollateral`: Emitted when a user decreases their collateral.
* `CollateralOwnerTransfer`: Emitted when ownership of an account's collateral and debt is transferred to a new account.
* `IncreaseDebt`: Emitted when a user increases their debt.
* `DecreaseDebt`: Emitted when a user decreases their debt.
* `Approval`: Emitted when a user approves an operator to manage their account.
* `LiquidateCollateral`: Emitted when an account is liquidated.

### Modifiers

* `lock`: Ensures that certain functions cannot be re-entered while they are still executing.
* `onlyGov`: Ensures that only the governance address can call certain functions.

### Structs

* `Account`: Represents a user's account, including their total collateral (`tokenAssets`) and total debt (`tinuDebt`).

### Mappings

* `vaultOwnerAccount`: Maps each user's address and each token address to an `Account` struct.
* `vaultPoolAccount`: Maps each token address to an `Account` struct representing the total collateral and debt for that token.
* `allowances`: Maps each user's address and each operator's address to a boolean indicating whether the operator is allowed to manage the user's account.
* `liquidationRatio`: Maps each token address to its liquidation ratio.
* `freeFlashLoanWhitelist`: Maps each address to a boolean indicating whether it is whitelisted for free flash loans.
