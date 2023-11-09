# Collateralized Vaults

UNIT vaults are collateralized using assets admitted by The UNIT governance. Currently, **ETH** is the sole collateral source, but The UNIT governance will soon consider **other collateral sources**, such as the native tokens of **BSC, Polygon, Near,** and others**.** To mint TINU, participants must deposit ETH into UNIT vaults.&#x20;

<figure><img src="../.gitbook/assets/UNIT Vaults (1).png" alt=""><figcaption><p>A UNIT Vault</p></figcaption></figure>

Each vault only contains one particular asset and a set of **risk parameters** to ensure the stability of TINU:

* **Debt Ceiling**
* **Liquidation Ratio**
* **Liquidation Fee**

The minimum collateralization level to mint TINU depends on the **1-year price range in UNIT** of the asset used in the particular vault. This ensures that the vault will be protected **against high-volatility events**.

TINU is burned to retrieve the collateral in the vaults. Every time TINU is burned, a fee depending on the staking level will be charged and distributed to the remaining staking participants.

## Closing a Vault

Participants **control their vaults** as long as the collateral doesn’t fall below the **liquidation level**.&#x20;

To recover the collateral, vault owners must return all the **TINU** to the vault. As long as there is a TINU debt to the vault the collateral remaining must be greater than the **minimum deposit value** of **100 TINU**.

## Account Liquidations

Suppose an account's collateralization ratio falls below the **liquidation level**. In that case, the account owner will have **72 hours** to bring the vault back over the liquidation level by **adding more collateral or burning TINU**. However, after 72 hours, **anyone can claim** the collateral locked in the contract by burning the required amount of TINU set in the liquidation parameters.

The vault owner will pay a **liquidation fee** for the risk added to the system.

## Sepolia Testnet Contracts

We have deployed TINU vaults in the Sepolia Test Network. Here are the contract addresses as of 2023-06-26:

**TINU:** 0x510d78536accD71FC43a10DAB0183A12523E3851

**unitPriceFeed:** 0x4Bd57566cbe514df063BA4F9f99eb01b442FA58E

**vault:** 0x5FC50DBa21b2709c15289a57be762E9Ec166e273

**unitRouterV1:** 0x0aded79406574aAf1e85330a1f83c27e60f6D841
