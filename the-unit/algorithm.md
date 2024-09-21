---
description: The core of UNIT
---

# UNIT's Algorithm

[_The UNIT_ paper](https://github.com/toknowwhy/the-unit-paper/blob/main/the\_unit\_paper.pdf) describes the basis of the UNIT's algorithm. UNIT's algorithm aims to track what it would be to hold the top cryptocurrencies over the long haul.

## How to Obtain UNIT's Value

In short, the value of 1 UNIT comes from the relative price motions of the top cryptocurrencies. To follow the value of UNIT we display three charts of the value of 1 UNIT over time on our website: the [Bitcoin chart](https://app.unitindex.org/unit/btc) (denominated in SATS), the [Ethereum chart](https://app.unitindex.org/unit/ETH) (in Finney), and the [USD chart](https://app.unitindex.org/unit/USD).

## Calculating the Value of UNIT

First, we chose the first cryptocurrency ever created, Bitcoin, to price other coins in terms of that one.

We define the weight $$w_{C, m}$$ of a coin $$C$$ on a given month $$m$$ as the market cap of that coin at the beginning of the month over the total market cap of all coins in the UNIT at the given month.

$$
w_{C,m}= \frac{M_{C,m}}{\sum_iM_{i,m}}
$$

As usual, the total market capitalization is calculated by adding the circulating supplies $$S_i$$ times the price of each cryptocurrency in the UNIT, $$P_{i}$$, in terms of the first cryptocurrency, Bitcoin.

$$
\displaystyle\sum_{i} S_iP_{i}
$$

Let the UNIT on month $$m$$, $$Ø_m$$, be defined by

$$
Ø_m = \left(\sum_{i}\frac{P_{i,m}}{P_{i,m-1}} w_{i,m-1}\right) U_{m-1}
$$

where $$P_{i,m}$$ is the price of a coin $$i$$ in the Unit at month $$m$$ and $$w_{i,m}$$ is the weight of a coin $$i$$ in the Unit at month $$m$$.
