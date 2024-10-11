# UNIT's Oracle

The UNIT Oracle is designed to gather token price and market cap data from various decentralized institutions, calculate the price of UNIT, and broadcast this information to the Ethereum blockchain. The Oracle ensures that the pricing data used to compute the UNIT index is both accurate and fair, utilizing a robust two-step median calculation process to enhance reliability and resistance to manipulation.

<figure><img src="../.gitbook/assets/oracle nodes network transparent (2).png" alt=""><figcaption><p>UNIT Oracle Overview</p></figcaption></figure>

## **Network Composition**

The UNIT Oracle network consists of multiple decentralized nodes, each responsible for retrieving token prices and market cap data from trusted data aggregators or exchanges. These nodes work together to ensure data accuracy, security, and the final computation of the UNIT price.

**Key Components:**

* **Oracle Nodes:** Distributed nodes in the network responsible for collecting token price and market cap data from external sources and calculating an initial median price.&#x20;
* **Data Sources:** Trusted platforms (e.g., CoinGecko) or exchanges, from which Oracle nodes retrieve token prices and market cap data.&#x20;
* **Median Calculation Engine:** The Oracle employs a two-step median calculation process, filtering out outliers or manipulated data twice to ensure accuracy.&#x20;
* **Blockchain Broadcast:** Once the UNIT price is finalized and signed, it is broadcasted to the Ethereum blockchain for use in smart contracts.

## Price Aggregation and Two-Step Median Calculation

To ensure accuracy and reduce the risk of manipulation, the UNIT Oracle uses a two-step median calculation process. This process helps filter extreme values at both the data source and network levels.

### **Step 1: Node-Level Median Calculation**

Each Oracle node independently retrieves token price and market cap data from its chosen sources (data aggregators or exchanges). The node calculates the first median from these sources. The node operator has flexibility in choosing which data sources to use, but the final median calculated at this stage ensures outliers are removed at the node level.

If the number of data sources is even, the system will randomly select one of the two middle values as the median. For instance, if a node retrieves four prices, it will randomly select either the second or third price as the median.

### **Step 2: Network-Level Median Calculation**

Once each node calculates its own median, it signs the result using its private key and shares it with other nodes via a P2P network. The P2P network allows anyone to collect these signed prices.

In the next stage, any user can submit at least five signed prices to the Ethereum smart contract. The smart contract will verify the signatures to ensure that they are from authorized Oracle nodes and then compute the second median from these five or more values. This second median represents the final price, which is then published on-chain.

**Example —** If five nodes calculate the following median prices for **LINK**:

* Ø29,000
* Ø28,900
* Ø29,500
* Ø30,000
* Ø29,200

The smart contract would compute the final median price as Ø29,200, representing the most reliable estimate from the available data.

### How Prices and Market Caps Are Collected

UNIT Oracle retrieves token price and market cap data from multiple trusted sources, such as CoinGecko or other exchanges. To mitigate the risk of manipulated or erroneous data, the system calculates the median from these sources at each Oracle node, ensuring that extreme values (outliers) do not disproportionately affect the final price.

### Why Median Calculation?

The median calculation is critical because it helps to filter out extreme prices or erroneous data points. By using the median instead of the average, the system ensures that the most representative price and market cap values are used to compute the UNIT index. This approach protects against anomalies or any malicious attempts to manipulate the price by isolating outliers.

### Minimum Data Sources Requirement

Each Oracle node must collect price and market cap data from a minimum number of sources to calculate an accurate median. The system requires at least a certain number of sources (e.g., Bar()), and if this threshold is not met, the price update will be rejected. This ensures that data fed into the system is well-rounded and less susceptible to manipulation.

## Data Integrity and Security Mechanisms

UNIT Oracle employs several mechanisms to ensure the reliability and security of its data to prevent manipulation:

* **Cryptographic Signatures**: Every price update is signed using Ethereum's V, R, S signature scheme, verifying that it comes from an authorized Oracle node.
* **Source Reputation**: The Oracle system tracks the reliability of each data source. Persistently unreliable or manipulated sources are flagged and removed from the active pool of sources.
* **Multiple Sources**: Using multiple independent sources significantly reduces the risk of price manipulation by any single malicious actor.

## Public Price Submission to the Blockchain

One unique feature of the UNIT Oracle system is that anyone can submit signed price data to the Ethereum blockchain. This "anyone" could be any user or third-party application willing to pay the associated gas fees. The process works as follows:

* A user collects at least five signed prices from the P2P network, ensuring the signatures are from authorized Oracle nodes.
* The user submits these prices to the smart contract, which verifies the signatures and calculates the final median price from the submitted values.
* The contract requires at least five valid signatures for the price to be considered.

This open submission process ensures that the Oracle is decentralized and accessible, allowing external participants to contribute to the process by submitting price updates. However, Oracle node operators are not required to submit prices themselves—they can choose to only sign and broadcast their prices, leaving it to others to handle the on-chain submission.

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
