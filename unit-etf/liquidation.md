# Liquidation

## Why liquidate？

When the value of the collateral within a Vault is insufficient to support the debt, the system needs to take over the collateral and debt and auction it off to achieve a situation where the system's assets exceed its liabilities.

{% hint style="info" %}
The most important principle of the system is that **at any moment, the value of assets cannot be less than the value of liabilities.** To achieve this purpose, we need a liquidation system and an auction system.
{% endhint %}

Liquidation In the Ethereum network, a block is typically around 10 seconds, and during network congestion, the confirmation time for a transaction might be longer, making liquidation not very real-time. However, in the Arbitrum network, a transaction can be confirmed within a second, allowing for rapid price feeding. And the gas cost is much lower than on the Ethereum mainnet.



\
