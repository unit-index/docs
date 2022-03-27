# Average Market Cap to Volume Ratio

Label the coins in The Unit $$1,\ldots,n$$. For each coin $$c$$ in $$\{1,\ldots,n\}$$ and each day $$d$$ of the last 180 days,

$$
R_{c,180}=\frac{\displaystyle\sum_{d=1}^{180} S_{c,d}P_{c,d}}{\displaystyle\sum_{d=1}^{180}V_{c,d}},
$$

where $$S_{c,d}$$ is the supply of coin $$c$$ on day $$d$$, $$P_{c,d}$$ is the price in UNIT of coin $$c$$ on day $$d$$, and $$V_{c,d}$$ is the trading volume in UNIT of coin $$c$$ on day $$d$$.

Then,

$$
R=\frac{\displaystyle\sum_{c=1}^{n} R_{c,180}}{n}.
$$
