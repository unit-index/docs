# UNIT's Algorithm

[_The UNIT_ paper](https://github.com/toknowwhy/the-unit-paper/blob/main/the\_unit\_paper.pdf) describes the basis of the UNIT's algorithm.

### How to Obtain UNIT's Value

In short, the value of 1 UNIT comes from the total market capitalization of our index divided by human years. To follow the value of UNIT we display three charts of the value of 1 UNIT over time on our website: the [Bitcoin chart](https://app.unitindex.org/unit/btc) (denominated in SATS), the [Ethereum chart](https://app.unitindex.org/unit/ETH) (in Finney), and the [USD chart](https://app.unitindex.org/unit/USD).

### Calculating the Total Market Capitalization

The total market capitalization is calculated by choosing cryptocurrency $$1$$ with supply $$S_1$$ _and adding the available supplies of each cryptocurrency_ $$(S_c)$$_times the price of each cryptocurrency_ $$c$$ _in terms of cryptocurrency_ $$1$$ $$(P_{c,1})$$_._

$$
S_1+S_2 P_{2,1}+\cdots+ S_n\ P_{n,1} = \displaystyle\sum_{c=0}^{n} S_cP_{c,1}
$$

### Finally

To normalize and anchor our unit to humanity, we let $$N$$ be the current total number of humans and $$Y$$the average life expectancy at birth. And one unit of value (1 UNIT)  is defined by:



$$
\frac{S_1+S_2 P_{2,1}+\cdots+ S_n\ P_{n,1}}{NY}.
$$

## UNIT's Selection Criteria

Let $$S_1$$ be the total current supply of the Rank 1 currency (currently Bitcoin), and let $$\phi$$ be the golden ratio $$\frac{1+\sqrt{5}}{2}$$. Then the coins creating UNIT must satisfy the following conditions.

1. Valuation: The 180D average daily market capitalization must be greater than $$\frac{S_1}{\phi^{12}}\approx\frac{S_1}{322}$$.
2. Volume of Trade: The currency trades widely with at least a year of public trading. If $$R$$ is the 180D average market capitalization to trading volume ratio\*. The 180D average daily volumes must be greater than $$\frac{S_1}{\phi^{12}R}$$.
3. Issuance: The consensus rules must define the currency supply.
4. Availability: As a weak rule, 50% of the supply must be available for trading.

\* The next section is the calculation of $$R$$.

## Average Market Cap to Volume Ratio

Label the coins creating UNIT $$1,\ldots,n$$. For each coin $$c$$ in $$\{1,\ldots,n\}$$ and each day $$d$$ of the last 180 days,

$$
R_{c,180}=\frac{\displaystyle\sum_{d=1}^{180} S_{c,d}P_{c,d}}{\displaystyle\sum_{d=1}^{180}V_{c,d}},
$$

where $$S_{c,d}$$ is the supply of coin $$c$$ on day $$d$$, $$P_{c,d}$$ is the price in UNIT of coin $$c$$ on day $$d$$, and $$V_{c,d}$$ is the trading volume in UNIT of coin $$c$$ on day $$d$$.

Then,

$$
R=\frac{\displaystyle\sum_{c=1}^{n} R_{c,180}}{n}.
$$

## Population Data

Currently, we use the population data estimated by the United Nations Department of Economic and Social Affairs [Population Division](https://population.un.org/). We found this to be the most accurate.

In the future, we would like to collaborate with several population oracles to update this data more often and increase its accuracy.

We use these data because this way UNIT accounts for both live human experience and potential in human years. An increase in human years would indicate a potential increase in the economy and would also create an increase in the total number of units. This makes UNIT extra stable as a financial benchmark for the global economy.

The slow update of this data is acceptable for the correct functioning of UNIT since population and life expectancy at birth data change slowly from year to year.
