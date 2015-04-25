# Bidvoy API

## Welcome great developer!

On the following pages you can find documentation and resources of the bidvoy API. Every application out there helps us to make bidvoy more awesome. So, if you are programming based on our RESTful API feel free to contact us anytime. We are really looking forward to your feedback in order to extend the API here and make it better. We really love to here from your project!

## Get started

The first step is always the hardest.. but not here. We designed our API in a way that it is easy to understand and simply to handle. No one wants to read pages of text before getting started. That's why we present you a short overview of our endpoints together with a sample call for each method to make it more concrete.

#### API token

Right now our API is kind of a beta version. That means that you need a token to authorize your application and are allowed to make calls. How do you get such a key? Easy as pie. Just drop us a line ([info@bidvoy.net](mailto:info@bidvoy.net)) containing the following information:

- Where do you want to use it? (domain)
- What do you want to do? (a short description is fine)

After we have approved your request, you get your personal API token and you can start immediately. Again the whole procedure is because of the beta state of our API. We promise that everything gets easier later.

#### Github

All of your API related feedback, suggestions or bug reports can and should be filed in this github repository as an issue.

## Endpoints

#### Account

- **[<code>GET</code> account/usage](https://github.com/bidvoy/api-documentation/blob/master/endpoints/account/GET_usage.md)**

#### Category

- **[<code>GET</code> category/get](https://github.com/bidvoy/api-documentation/blob/master/endpoints/category/GET_get.md)**
- **[<code>GET</code> category/searchbykeyword](https://github.com/bidvoy/api-documentation/blob/master/endpoints/category/GET_searchbykeyword.md)**

#### Analysis

- **[<code>GET</code> analysis/statistics](https://github.com/bidvoy/api-documentation/blob/master/endpoints/analysis/GET_statistics.md)**

#### Article (Deprecated in favor of Analysis endpoint)

- **[<code>GET</code> article/analyse](https://github.com/bidvoy/api-documentation/blob/master/endpoints/article/GET_analyse.md)**

## Changes

**2015/04/26**

- All endpoints support the country Austria now
- category/searchbyname enpoint was removed
- category/searchbykeyword Response field "parent" renamed to "parentid"
- article/analyse endpoint was renamed to analysis/statistics; article/analyse stays functional for a while, however we strongly suggest to update
- analysis/statistics Request parameter "quickdate" added 
- analysis/statistics Response field "currency" contains now ISO 4217 code instead of currency symbol 
- all endpoints: Response field "dataCount" removed
- all endpoints: Response field "status" contains now HTTP status codes instead of "OK/FAIL"

**2013/10/11**

- article/analyse Request parameter "startdate" and "enddate" added

**2013/06/29**

- account/usage Response field "dailyLimit" removed, "monthlyLimit" added

**2013/06/17:**

- Initial release