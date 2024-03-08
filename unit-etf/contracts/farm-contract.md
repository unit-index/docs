---
description: Farm Contract Detailed Documentation
---

# Farm Contract

### Overview

The `Farm` contract allows users to stake their LP tokens and earn rewards over time.&#x20;

The main features of the contract are:

* Ability to stake LP tokens and lock them for a specified period.
* Ability to withdraw staked tokens after the lock period has expired.
* Ability to claim earned rewards.
* Ability to transfer ownership of locked tokens.
* Allocation of rewards based on the amount of tokens staked and the time they are staked for.

### Contract Details

#### Structs

* `UserInfo`: Stores information about a user's staking activity, including the amount staked and the user's accumulated reward debt.
* `PoolInfo`: Stores information about a pool, including the LP token, allocation points, the last block when rewards were distributed, and the accumulated rewards per share.
* `UserLockInfo`: Stores information about a user's locked tokens, including the amount, unlock time, multiplier, reward debt, and the pool ID.

#### Variables

* `accCakePerShareArchive`: An array storing the accumulated rewards per share at the end of each period.
* `totalAllocPoint`: The total allocation points of all pools.
* `startBlock`: The block number when the contract started.
* `cakePerBlock`: The amount of rewards distributed per block.
* `periodAmount`: An array storing the amount of rewards for each period.
* `periodBlock`: The number of blocks in a period.
* `periodIndex`: The current period index.
* `lastPeriodStartBlock`: The block number when the last period started.
* `tokenFactory`: The address of the token factory contract.
* `userLock`: A mapping of each user's address to their locked tokens.
* `userUnlockIndexs`: A mapping of each user's address to their unlock index.
* `poolInfo`: An array storing the information of all pools.
* `multiplier1, multiplier2, multiplier3, multiplier4`: The multipliers for different lock periods.
* `un`: The address of the UN token contract.
* `lockTime`: An array storing the lock times.
* `multipliers`: An array storing the multipliers.
* `unPerBlockList`: An array storing the amount of UN tokens distributed per block.
* `totalWeights`: The total weights representing the sum of all multipliers.
* `userInfo`: A mapping of each pool ID to a mapping of each user's address to their user information.

#### Functions

* `constructor`: Initializes the contract with the owner's address, period block, UN per block list, start block, and UN token address.
* `setMultiplier`: Sets the multipliers for different lock periods.
* `add`: Adds a new pool.
* `depositAndLock`: Allows a user to deposit and lock their LP tokens.
* `withdraw`: Allows a user to withdraw their locked tokens after the lock period has expired.
* `claim`: Allows a user to claim their earned rewards.
* `claimAll`: Allows a user to claim all their earned rewards.
* `pendingRewards`: Returns the pending rewards of a user.
* `updateStakingPool`: Updates the staking pool.
* `massUpdatePools`: Updates all pools.
* `updatePool`: Updates a specific pool.
* `updatePeriod`: Updates the period.
* `transfer`: Transfers LP tokens to a specified address.
* `getTime`: Returns the time difference between two block numbers.
* `transferLockOwner`: Transfers the ownership of locked tokens to a new owner.

#### Events

* `Deposit`: Emitted when a user deposits and locks their tokens.
* `Withdraw`: Emitted when a user withdraws their tokens.
* `Claim`: Emitted when a user claims their rewards.
* `TransferLockOwner`: Emitted when the ownership of locked tokens is transferred.
