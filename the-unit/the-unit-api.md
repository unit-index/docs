---
description: The Unit API uses GraphQL
---

# The Unit API

Playground Url: https://graph.20y.org

## Schemas

#### UnitData

| Field       | Type   | Description                                                     |
| ----------- | ------ | --------------------------------------------------------------- |
| time        | String | The timestamp when the unit value got recorded                  |
| value       | Float  | The value of The Unit                                           |
| market\_cap | Float  | Daily/hourly total market cap of all the coins that in The Unit |
| volume      | Float  | Daily/hourly total volume of all the coins that in The Unit     |

#### CoinUnitData

| Field                          | Type   | Description                                         |
| ------------------------------ | ------ | --------------------------------------------------- |
| time                           | String | The timestamp when the coin unit price got recorded |
| price                          | Float  | The unit price of the coin                          |
| market\_cap                    | Float  | Daily/hourly total market cap of the coin           |
| volume                         | Float  | Daily/hourly total volume of the coin               |
| coin\_id                       | String | the coin id                                         |
| price\_change\_24h             | Float  | 24h change of the coin's unit price                 |
| price\_change\_percentage\_24h | Float  | 24h change in percentage of the coin's unit price   |

## Queries

**coinUnitPrice: String**

_Get the unit price of a coin_

* (Required Param) coin\_id: String - the id of the coin
* (Return value) if the coin passed as param is in our supported list, this query will return the corresponding unit price; if not in the list, it will return error message.&#x20;

**supportedCoinList: \[String] **

_Get the list of coins supported to get the unit price_

* (Return Value) List of coin ids supported in coinUnitPrice query

**coinUnitPriceWithCurrency: Float **

_If the coin is not in supported list, get the unit price with a stable-coin currency and amount_

* (Required Param) currency: String - The currency to be converted into the unit price. Currently four currencies are supported: "usdt", "usdc", "dai", "busd".
* (Required Param) amount: Float - The amount of currencies that needs to be converted.

#### unitDailyData: \[UnitData]

_Get the daily data of The Unit_

* (Optional Param) limit: Int - How many records will be returned in the response

#### coinUnitDailyData: \[CoinUnitData]

_Get the daily unit data of a specific coin_

* (Required Param) coin\_id: String - the id of the coin to be queried
* (Optional Param) limit: Int - How many records will be returned in the response

#### unitHourlyData: \[UnitData]

_Get the hourly data of The Unit_

* (Optional Param) limit: Int - How many records will be returned in the response

#### coinUnitHourlyData: \[CoinUnitData]

_Get the hourly unit data of a specific coin_

* (Required Param) coin\_id: String - the id of the coin to be queried
* (Optional Param) limit: Int - How many records will be returned in the response



More queries coming soon
