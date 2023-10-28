# UNIT's Algorithm

[_The UNIT_ paper](https://github.com/toknowwhy/the-unit-paper/blob/main/the\_unit\_paper.pdf) describes the basis of UNIT's algorithm. We display two charts of the value of 1 unit over time on our website: the Bitcoin one (denominated in SATS) and the Ethereum one (in Finney).

### How to Obtain UNIT's Value

The value of 1 UNIT comes from the total market capitalization of our index divided by human years.

### Calculating the Total Market Capitalization

The total market capitalization is calculated by choosing cryptocurrency $$1$$ with supply $$S_1$$ _and adding the available supplies of each cryptocurrency_ $$(S_c)$$_times the price of each cryptocurrency_ $$c$$ _in terms of cryptocurrency_ $$1$$ $$(P_{c,1})$$_._

$$
S_1+S_2 P_{2,1}+\cdots+ S_n\ P_{n,1} = \displaystyle\sum_{c=0}^{n} S_cP_{c,1}
$$

### Finally

We let $$N$$ be the current total number of humans and $$Y$$the average life expectancy at birth. And one unit of value is defined by:



$$
\frac{S_1+S_2 P_{2,1}+\cdots+ S_n\ P_{n,1}}{NY}.
$$

## UNIT's Selection Criteria

Let $$S$$ be the total current supply of the Rank 1 currency (currently Bitcoin), and let $$\phi$$ be the golden ratio $$\frac{1+\sqrt{5}}{2}$$. Then the coins creating UNIT must satisfy the following conditions.

1. Valuation: The 180D average daily market capitalization must be greater than $$\frac{S}{\phi^{12}}\approx\frac{S}{322}$$.
2. Volume of Trade: The currency trades widely with at least a year of public trading. If $$R$$ is the 180D average market capitalization to trading volume ratio\*. The 180D average daily volumes must be greater than $$\frac{S}{\phi^{12}R}$$.
3. Issuance: The consensus rules must define the currency supply.
4. Availability: As a weak rule, 50% of the supply must be available for trading.

\* For a calculation of $$R$$ see [average-market-cap-to-volume-ratio.md](average-market-cap-to-volume-ratio.md "mention").
