# GET analysis/statistics

    http://api.bidvoy.net/analysis/statistics/

## Description
The actual search routine. Provides you with statistical data based on your given product and category. Hint: You need a keyword and its category to call this method. If you don't know the categoryid, use the category endpoint previously to get it.

***

## Authentication
Authentication via api key is required for this call.

***

## Parameters
- **keyword** (required) — This is the name of your product/article. **Examples:** iPhone 4 16gb black, ray ban 3364
- **category** (required) — This is the category of your requested product that gets evaluated. **Examples:** 1, 7, 206, 1304
- **state** (optional) — The state attribute determines whether the calculation should be done with used or new products. **Examples:** used [default], new
- **listing** (optional) — Determines whether the calculation should be done with auction or buyitnow products. **Examples:** auction [default], buyitnow
- **startdate** (optional) — Sets the start date of the analysis period. Please note that you can only go 183 days back in time. Format: mm/dd/yyyy **Examples:** 10/08/2013
- **enddate** (optional) — Sets the end date of the analysis period. Format: mm/dd/yyyy **Examples:** 10/11/2013
- **quickdate** (optional) - Instead of startdate and enddate parameter you can use quickdate to evaluate predefined intervals (weeks or months). **Examples:** 1w, 2w, 3w, 1m, 2m, 3m, 4m, 5m, 6m
- **language** (optional) — This identifier sets the language of the API output.
**Examples:** us [default], uk, de, at
- **apikey** (required) — This is your api key. **Examples:** e1568c571e684e0fb1724da85d215dc0

## Example
**Request**

    GET analysis/statistics
    Parameters: keyword=Galaxy%20Nexus%20i9250&category=9355&language=us&apikey=e1568c571e684e0fb1724...


**Return**

``` json
{
    "status": 200,
    "errorMessage": "",
    "data": {
        "keyword": "Galaxy Nexus i9250",
        "currency": "USD",
        "averagePrice": "224.06",
        "analyzedQuantity": "128",
        "weeklyTrend": "-1.23",
        "priceMargin": "139.95",
        "ebaySellingFee": "20.16",
        "link": "http://us.bidvoy.net/Galaxy_Nexus_i9250/9355"
    }
}
```