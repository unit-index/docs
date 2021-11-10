# The Unit Algorithm

__[_The Unit_ paper](https://github.com/toknowwhy/the-unit-paper/blob/main/the\_unit\_paper.pdf) describes the basis of The Unit algorithm. We display two charts of the value of 1 unit over time on our website: the Bitcoin one (denominated in SATS) and the Ethereum one (in Finney).

## How to Obtain The Unit value

The value of 1 unit comes from the total market capitalization of our index.

## Calculating the Total Market Capitalization

$$
S_0+S_1 P_{1,0}+ S_2\ P_{2,0}+\cdots+ S_n\ P_{n,0} = \displaystyle\sum_{i=0}^{n} S_iP_{i,0}
$$
