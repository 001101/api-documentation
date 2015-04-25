# GET category/get

    http://api.bidvoy.net/category/get/

## Description
Returns a category object specified by its unique id.

***

## Authentication
Authentication via api key is required for this call.

***

## Parameters
- **id** (required) — The id of the category you want to get. **Examples**: 1, 7, 206, 1304
- **language** (optional) — This identifier sets the language of the API output. **Examples**: us [default], uk, de, at
- **apikey** (required) — This is your api key. **Examples:** e1568c571e684e0fb1724da85d215dc0

## Example
**Request**

    GET category/get
    Parameters: id=9355&language=us&apikey=e1568c571e684e0fb1724da85d215dc0


**Return**

``` json
{
    "status": 200,
    "errorMessage": "",
    "data": {
        "id": "9355",
        "name": "Cell Phones &amp; Smartphones",
        "parentid": "15032"
    }
}
```