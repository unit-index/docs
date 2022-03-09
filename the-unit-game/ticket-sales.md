# Ticket Sales

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

## Example of Ticket Sale Calculation

Question: Will coin A enter The UNIT this round?

Calculate the probability $$p$$ that coin A will enter The UNIT in this round given equal $$0.5$$ probability that it will satisfy the requirements in any given day.

$$
p = \frac{1}{2^{13}}\biggl[\binom{13}{8}+\binom{13}{9}+\binom{13}{10}+\binom{13}{11}+\binom{13}{12}+\binom{13}{13}\biggr]
$$

$$
p \approx 0.29052734375
$$

Then, if 1 ETH is currently worth 1000 UNIT, then

$$
1 \;\textrm{ETH}= 1000*  0.70947265625\;\textrm{yUNIT}=709.47265625\;\textrm{yUNIT},
$$

$$
1 \;\textrm{ETH}= 1000 * 0.29052734375 \;\textrm{nUNIT} = 290.52734375\;\textrm{nUNIT}.
$$
