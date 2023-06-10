# Ticket Sales

The purchase value of tickets depends on the price in UNIT of the cryptocurrencies deposited and the probability of the outcome.

On day 1 of the round, tickets (yUNIT and nUNIT) are priced in UNIT at the rate of&#x20;

$$
1 \;\textrm{UNIT}= (1-p) \;\textrm{yUNIT},
$$

$$
1 \;\textrm{UNIT}= p\;\textrm{nUNIT},
$$

for $$p$$ being the probability of "yes".

On subsequent days, ticket prices depend on the updated probability of the outcome on each day.&#x20;

In the Ethereum network, for $$V$$ the price of 1 ETH in UNIT and $$p$$ the updated probability of "yes" we get that 1 ETH will yield the following amount of yUNIT and nUNIT tickets.

$$
1 \;\textrm{ETH}= V * (1-p) \;\textrm{yUNIT},
$$

$$
1 \;\textrm{ETH}= V * p \;\textrm{nUNIT}.
$$

## Example of Ticket Sale Calculation (Day 1)

Question: Will coin A enter The UNIT this round?

Calculate the probability $$p$$ that coin A will enter The UNIT in this round given equal $$0.5$$ probability that it will satisfy the requirements in any given day.

$$
p = \frac{1}{2^{13}}\biggl[\binom{13}{8}+\binom{13}{9}+\binom{13}{10}+\binom{13}{11}+\binom{13}{12}+\binom{13}{13}\biggr]
$$

$$
p =\frac{2380}{8192}= 0.29052734375.
$$

Then, if 1 ETH is currently worth 1000 UNIT, then

$$
1 \;\textrm{ETH}= 1000*  0.70947265625\;\textrm{yUNIT}=709.47265625\;\textrm{yUNIT},
$$

$$
1 \;\textrm{ETH}= 1000 * 0.29052734375 \;\textrm{nUNIT} = 290.52734375\;\textrm{nUNIT}.
$$

## Example of Ticket Sale Calculation (Day 2)

Same Question: Will coin A enter The UNIT this round?

Known Data: On Day 1, coin A met the requirements to enter The UNIT.

Again, calculate the probability $$p_1$$ that coin A will enter The UNIT in this round given equal $$0.5$$ probability that it will satisfy the requirements in any given day.

$$
p_1 = \frac{1}{2^{12}}\biggl[\binom{12}{7}+\binom{12}{8}+\binom{12}{9}+\binom{12}{10}+\binom{12}{11}+\binom{12}{12}\biggr]
$$

$$
p_1 = \frac{1586}{4096} =0.38720703125.
$$

Then, if 1 ETH is currently worth 1000 UNIT, then

$$
1 \;\textrm{ETH}= 1000*  0.61279296875\;\textrm{yUNIT}=612.79296875\;\textrm{yUNIT},
$$

$$
1 \;\textrm{ETH}= 1000 * 0.38720703125 \;\textrm{nUNIT} = 387.20703125\;\textrm{nUNIT}.
$$
