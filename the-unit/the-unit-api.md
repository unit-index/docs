---
description: UNIT's API uses GraphQL
---

# UNIT's API

Playground Url: https://graph.unitindex.org

## Schemas

#### UnitData

| Field       | Type   | Description                                                  |
| ----------- | ------ | ------------------------------------------------------------ |
| time        | String | The timestamp when UNIT's value got recorded                 |
| value       | Float  | The value of UNIT                                            |
| market\_cap | Float  | Daily/hourly total market cap of all the coins creating UNIT |
| volume      | Float  | Daily/hourly total volume of all the coins creating UNIT     |

#### CoinUnitData

| Field                          | Type   | Description                                              |
| ------------------------------ | ------ | -------------------------------------------------------- |
| time                           | String | The timestamp when the coin's price in UNIT got recorded |
| price                          | Float  | UNIT's price of the coin                                 |
| market\_cap                    | Float  | Daily/hourly total market cap of the coin                |
| volume                         | Float  | Daily/hourly total volume of the coin                    |
| coin\_id                       | String | the coin id                                              |
| price\_change\_24h             | Float  | 24h change of the coin's price in UNIT                   |
| price\_change\_percentage\_24h | Float  | 24h change in percentage of the coin's price in UNIT     |

## Queries

**coinUnitPrice: String**

_Get the price of a coin in UNIT_

* (Required Param) coin\_id: String - the id of the coin
* (Return value) if the coin passed as param is in our supported list, this query will return the corresponding price in UNIT; if not in the list, it will return error message.

\*\*supportedCoinList: \[String] \*\*

_Get the list of coins supported to get the price in UNIT_

* (Return Value) List of coin ids supported in coinUnitPrice query

\*\*coinUnitPriceWithCurrency: Float \*\*

_If the coin is not in supported list, get the unit price with a stable-coin currency and amount_

* (Required Param) currency: String - The currency to be converted into the unit price. Currently four currencies are supported: "usdt", "usdc", "dai", "busd".
* (Required Param) amount: Float - The amount of currencies that needs to be converted.

#### unitDailyData: \[UnitData]

_Get the daily data of UNIT_

* (Optional Param) limit: Int - How many records will be returned in the response

#### coinUnitDailyData: \[CoinUnitData]

_Get the daily data of a specific coin in UNIT_

* (Required Param) coin\_id: String - the id of the coin to be queried
* (Optional Param) limit: Int - How many records will be returned in the response

#### unitHourlyData: \[UnitData]

_Get the hourly data of UNIT_

* (Optional Param) limit: Int - How many records will be returned in the response

#### coinUnitHourlyData: \[CoinUnitData]

_Get the hourly data of a specific coin in UNIT_

* (Required Param) coin\_id: String - the id of the coin to be queried
* (Optional Param) limit: Int - How many records will be returned in the response

More queries coming soon
