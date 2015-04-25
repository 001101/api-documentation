# GET category/searchbykeyword

    http://api.bidvoy.net/category/searchbykeyword/

## Description
Returns a list of categories in which your product occures at least once. This method is helpful if you have a specific product and want to get the right categoryid in order to call for example the article endpoint.

***

## Authentication
Authentication via api key is required for this call.

***

## Parameters
- **keyword** (required) — This is the name of your product/article. **Examples:** iPhone 4 16gb black, ray ban 3364
- **language** (optional) — This identifier sets the language of the API output.
**Examples:** us [default], uk, de, at
- **pagesize** (optional) — Determines the quantity of returned entities. Could be used for a pagination together with pageid. Maximum is 100. **Examples:** 3, 10 [default], 20
- **pageid** (optional) — This is the id of the page returned (zero based). Could be used for a pagination together with pagesize. **Examples:** 0 [default], 1, 2
- **apikey** (required) — This is your api key. **Examples:** e1568c571e684e0fb1724da85d215dc0

## Example
**Request**

    GET category/searchbykeyword
    Parameters: keyword=iPhone%204s%2016GB%20black&apikey=e1568c571e684...


**Return**

``` json
{
    "status": 200,
    "errorMessage": "",
    "data": [
        {
            "id": 9355,
            "name": "Cell Phones & Smartphones",
            "parentid": 15032,
            "quantity": 25997
        },
        {
            "id": 20349,
            "name": "Cases, Covers & Skins",
            "parentid": 9394,
            "quantity": 117
        },
        {
            "id": 42428,
            "name": "Other",
            "parentid": 15032,
            "quantity": 88
        },
        {
            "id": 42425,
            "name": "Other",
            "parentid": 9394,
            "quantity": 47
        },
        {
            "id": 43304,
            "name": "Replacement Parts & Tools",
            "parentid": 15032,
            "quantity": 29
        },
        {
            "id": 58543,
            "name": "Accessory Bundles",
            "parentid": 9394,
            "quantity": 28
        },
        {
            "id": 122962,
            "name": "Straps & Charms",
            "parentid": 9394,
            "quantity": 21
        },
        {
            "id": 45070,
            "name": "Cell Phones",
            "parentid": 45065,
            "quantity": 17
        },
        {
            "id": 166030,
            "name": "Armbands",
            "parentid": 9394,
            "quantity": 16
        },
        {
            "id": 43307,
            "name": "Manuals & Guides",
            "parentid": 9394,
            "quantity": 7
        }
    ]
}
```