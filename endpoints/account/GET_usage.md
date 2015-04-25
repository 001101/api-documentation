# GET account/usage

    http://api.bidvoy.net/account/usage/

## Description
Each api token has a limited number of calls for each month. This method shows you the limit of your key and provides you with the number of calls you have done. Please note that a call to this method gets not added to your amount of monthly calls.

***

## Authentication
Authentication via api key is required for this call.

***

## Parameters
- **apikey** (required) — Your api key for which you want to receive the usage statistics. **Examples:** e1568c571e684e0fb1724da85d215dc0

## Example
**Request**

    GET account/usage
    Parameters: apikey=e1568c571e684e0fb1724da85d215dc0


**Return**

``` json
{
    "status": 200,
    "errorMessage": "",
    "data": {
        "usageToday": 78,
        "usageMonth": 206,
        "monthlyLimit": 1337
    }
}
```