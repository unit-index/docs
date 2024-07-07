# UNIT's Algorithm

[_The UNIT_ paper](https://github.com/toknowwhy/the-unit-paper/blob/main/the\_unit\_paper.pdf) describes the basis of the UNIT's algorithm. UNIT's algorithm aims to track what it would be to hold the top cryptocurrencies over the long haul.

### How to Obtain UNIT's Value

In short, the value of 1 UNIT comes from the relative price motions of the top cryptocurrencies. To follow the value of UNIT we display three charts of the value of 1 UNIT over time on our website: the [Bitcoin chart](https://app.unitindex.org/unit/btc) (denominated in SATS), the [Ethereum chart](https://app.unitindex.org/unit/ETH) (in Finney), and the [USD chart](https://app.unitindex.org/unit/USD).

### Calculating the Value of UNIT

First, we chose the first cryptocurrency ever created, Bitcoin, to price other coins in terms of that one.

We define the weight $$w_{C, m}$$ of a coin $$C$$ on a given month $$m$$ as the market cap of that coin at the beginning of the month over the total market cap of all coins in the UNIT at the given month.

$$
w_{C,m}= \frac{M_{C,m}}{\sum_cM_{c,m}}
$$

As usual, the total market capitalization is calculated by adding the circulating supplies $$S_c$$ times the price of each cryptocurrency in the UNIT,  $$P_{c}$$, in terms of the first cryptocurrency, Bitcoin.

$$
\displaystyle\sum_{c} S_cP_{c}
$$

Let the UNIT on month $$m$$, $$U_m$$, be defined by

$$
U_m = \left(\sum_{c}\frac{P_{c,m}}{P_{c,m-1}} w_{c,m-1}\right) U_{m-1}
$$

where $$P_{c,m}$$ is the price of a coin $$c$$ in the Unit at month $$m$$ and $$w_{c,m}$$ is the weight of a coin $$c$$ in the Unit at month $$m$$.

## UNIT's Selection Criteria

Let $$S_1$$ be the total current supply of the Rank 1 currency (currently Bitcoin), and let $$\phi$$ be the golden ratio $$\frac{1+\sqrt{5}}{2}$$. Then the coins creating UNIT must satisfy the following conditions.

1. Valuation: The 30D average daily market capitalization must be greater than $$\frac{S_1}{\phi^{12}}\approx\frac{S_1}{322}$$.
2. Fundamental Metrics: - Volume of Trade: The currency trades widely with at least a year of public trading. - Fees Accrued: The currency or underlying project brings profits to miners, validators, and other verifying participants.
3. Issuance: The consensus rules must define the currency supply.
4. Availability: As a weak rule, 50% of the supply must be available for trading.
