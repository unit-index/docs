# The Unit Algorithm

__[_The Unit_ paper](https://github.com/toknowwhy/the-unit-paper/blob/main/the\_unit\_paper.pdf) describes the basis of The Unit algorithm. We display two charts of the value of 1 unit over time on our website: the Bitcoin one (denominated in SATS) and the Ethereum one (in Finney).

## How to Obtain The Unit value

The value of 1 unit comes from the total market capitalization of our index devided by human years.

## Calculating the Total Market Capitalization

The total market capitalization is calculated by choosing cryptocurrency $$0$$ with supply $$S_0$$_ and adding the available supplies of each cryptocurrency _$$(S_i)$$_times the price of each cryptocurrency _$$i$$_ in terms of cryptocurrency _$$0$$_ _$$(P_{i,0})$$_._

$$
S_0+S_1 P_{1,0}+ S_2\ P_{2,0}+\cdots+ S_n\ P_{n,0} = \displaystyle\sum_{i=0}^{n} S_iP_{i,0}
$$

## Finally

We let $$N$$ be the current total number of humans and $$Y$$the average life expectancy. And one unit of value is defined by:



$$
\frac{S_0+S_1 P_{1,0}+ S_2\ P_{2,0}+\cdots+ S_n\ P_{n,0}}{NY}
$$
