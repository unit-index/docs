# UNIT's Oracle

The UNIT Oracle is designed to gather token price and market cap data from various centralized institutions, calculate the price of UNIT, and broadcast this information to the Ethereum blockchain. The Oracle ensures that the pricing data used to compute the UNIT index is both accurate and fair.

<figure><picture><source srcset="../.gitbook/assets/UNIT diagram dark mode.png" media="(prefers-color-scheme: dark)"><img src="../.gitbook/assets/UNIT diagram white mode.png" alt=""></picture><figcaption><p>UNIT Overview</p></figcaption></figure>

## **Network Composition**

The UNIT Oracle network consists of multiple decentralized nodes, each responsible for retrieving token prices and market cap data from trusted data aggregators like CoinGecko. These nodes work together to ensure data accuracy, security, and the final computation of the UNIT price.

**Key Components:**

* **Oracle Nodes**: These are distributed nodes in the network responsible for collecting token price and market cap data from external sources and calculating the UNIT price.
* **Data Sources**: Trusted platforms (e.g., CoinGecko) that provide token price and market cap information.
* **Median Calculation Engine**: After gathering data, Oracle calculates the median, filtering out outliers or manipulated data.
* **Blockchain Broadcast**: Once the UNIT price is finalized and signed, it is broadcasted to the Ethereum blockchain for use in smart contracts.

## Price Aggregation and Median Calculation

### **How Prices and Market Caps Are Collected**

UNIT Oracle retrieves token price and market cap data from multiple trusted sources like CoinGecko. To mitigate the risk of manipulated or erroneous data, the system calculates the median from multiple sources.

* **Why Median Calculation?**\
  Using the median ensures that extreme prices (outliers) from any single source do not disproportionately affect the final price. By collecting data from various sources and calculating the median rather than the average, the system protects against anomalies or malicious data, ensuring that the most representative token price and market cap are used to compute the UNIT index.
* **Minimum Data Sources Requirement**\
  The Oracle requires a minimum number of price sources (e.g., Bar()) to compute a median. If this threshold is not met, the system rejects the price update.

### **Example**

If five sources report the following Bitcoin prices: $29,000, $28,900, $29,500, $30,000, and $29,200, the median would be $29,200, representing the most reliable estimate from the available data.

## Data Integrity and Security Mechanisms

UNIT Oracle employs several mechanisms to ensure the reliability and security of its data to prevent manipulation:

* **Cryptographic Signatures**: Every price update is signed using Ethereum's V, R, S signature scheme, verifying that it comes from an authorized Oracle node.
* **Source Reputation**: The Oracle system tracks the reliability of each data source. Persistently unreliable or manipulated sources are flagged and removed from the active pool of sources.
* **Multiple Sources**: Using multiple independent sources significantly reduces the risk of price manipulation by any single malicious actor.

## Joining the Oracle Network

To become an Oracle node, participants must stake a specific number of tokens and apply to the community. The application is subject to a community vote, ensuring decentralization.

**Steps to Join:**

1. **Stake Tokens**: A certain number of tokens (TINU or UN) must be staked to participate.
2. **Apply for Node Status**: Submit an application through the governance portal.
3. **Community Vote**: The community votes to decide if the applicant can join the Oracle network.
4. **Set Up Node**: Once accepted, the operator must set up a server to run the Oracle node, which requires server management skills and uptime maintenance.

**Node Requirements:**

* **Hardware**: Detailed server requirements.
* **Network**: Reliable internet connectivity to ensure timely retrieval of price data and broadcasting updates.
* **Software**: Oracle node software (details on running the Oracle daemon).
