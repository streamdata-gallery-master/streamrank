---
swagger: "2.0"
info:
  title: CoinMarketCap Professional API Documentation
  description: "# IntroductionThe CoinMarketCap Professional API is a suite of high-performance
    RESTful JSON endpoints that are specifically designed to meet the mission-critical
    demands of application developers, data scientists, and enterprise business platforms.This
    API reference includes all technical documentation developers need to integrate
    third-party applications and platforms. Additional answers to common questions
    can be found in the [CoinMarketCap Professional API FAQ](https://pro.coinmarketcap.com/faq).***Note:**
    If you&rsquo;re using the CoinMarketCap Public API, you'll want to access the
    [Public API Documentation](https://coinmarketcap.com/api/); the Professional API
    is an entirely separate API product. If you're uncertain of which you need for
    your needs, check the [feature comparison matrix](https://pro.coinmarketcap.com/faq).*#
    Quick Start GuideFor developers eager to hit the ground running with the Professional
    API here are 3 quick steps to make your first call with the Professional API.1.
    **Sign up.** Sign up for an API Key in one of our two Professional API environments:-
    [sandbox.coinmarketcap.com](https://sandbox.coinmarketcap.com) - This testing
    sandbox has free access to all endpoints and all subscription plans to test with
    a snapshot of our market data.  - [pro.coinmarketcap.com](https://pro.coinmarketcap.com)
    - This is our live production environment with the latest market data. Select
    the free `Starter` plan if it meets your needs or upgrade to a paid tier.    2.
    **Get your API Key.** Once you sign up you'll land on your Developer Portal account
    dashboard. Copy your API from the `API Key` box in the top left panel.3. **Make
    a test call using your key.** Here is an example, [fetch all active cryptocurrencies
    by market cap and return market values in USD and Euros](https://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/latest?start=0&amp;limit=5000&amp;convert=USD,EUR)
    *[replace API Key in querystring with your own]*.```//this basic example is in
    Node.js ES5var xhr = new XMLHttpRequest();xhr.setRequestHeader('X-CMC_PRO_API_KEY',
    'b54bcf4d-1bca-4e8e-9a24-22ff2c3d462c');xhr.responseType = 'json';xhr.setRequestHeader('Accept',
    'application/json');xhr.open('GET', 'https://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/latest?start=0&amp;limit=5000&amp;convert=USD,EUR');xhr.onreadystatechange
    = function handler() {  if (xhr.readyState === 4 &amp;&amp; xhr.status === 200)
    {    console.log(xhr.response);  }};xhr.send();```4. **Implement your application.**
    Now that you've confirmed your API Key is working, get familiar with the API by
    reading the rest of this API Reference and commence building your application!***Note:**
    Making HTTP requests on the client side with Javascript is currently prohibited
    through CORS configuration. This is to protect your API Key which should not be
    visible to users of your application so your API Key is not stolen. Secure your
    API Key by routing calls through your own backend service.*# Authentication###
    Acquiring an API KeyAll HTTP requests made against the Professional API must be
    validated with an API Key. If you don't have an API Key yet visit the [Professional
    API Developer Portal](https://pro.coinmarketcap.com/) to register for one.###
    Using Your API KeyYou may use any *server side* programming language that can
    make HTTP requests to target the Professional API. All requests should target
    domain `https://pro-api.coinmarketcap.com`.You can supply your API Key in REST
    API calls in one of two ways:1. Preferred method: Via a custom header named `X-CMC_PRO_API_KEY`2.
    Convenience method: Via a query string parameter named `CMC_PRO_API_KEY`***Security
    Warning:** It's important to secure your API Key against public access. The custom
    header option is strongly recommended over the querystring option for passing
    your API Key in a production environment.*### API Key Usage CreditsMost plans
    include a monthly limit or &quot;hard cap&quot; to the number of data calls that
    can be made. This limit is tied to your API Key's [usage tier](https://pro.coinmarketcap.com/pricing)
    and resets at midnight UTC at the beginning of each calendar month.An API Key's
    monthly usage limit is tracked as API &quot;call credits&quot; which are incremented
    1:1 against successful (HTTP Status 200) data calls made with your key with these
    exceptions:- Account management endpoints, usage stats endpoints, and error responses
    are not included in this monthly limit.- **Paginated endpoints:** List-based endpoints
    track an additional call credit for every 100 data points returned (rounded up)
    beyond our 100 data point defaults. Our lightweight `/map` endpoints are not included
    in this limit and always count as 1 credit.- **Bundled API calls:** Many endpoints
    support [resource and currency conversion bundling](#section/Standards-and-Conventions).
    Bundled resources are also tracked as 1 call credit for every 100 resources returned
    (rounded up). Optional currency conversion bundling using the `convert` parameter
    also increment an additional API call credit for every conversion requested beyond
    the first.You can log in to the [Developer Portal](https://pro.coinmarketcap.com/)
    to view live stats on your API Key usage and limits including the number of credits
    used for each call. You can also find call credit usage in the JSON response for
    each API call. See the [`status` object](#section/Standards-and-Conventions) for
    details.# Endpoint Overview### The Professional API is divided into 4 top-level
    categoriesEndpoint Category  | Description-------------------|---------------[/cryptocurrency/*](#tag/cryptocurrency)
    | Endpoints that return data around cryptocurrencies such as ordered cryptocurrency
    lists or price and volume data.[/exchange/*](#tag/exchange) | Endpoints that return
    data around cryptocurrency exchanges such as ordered exchange lists and market
    pair data.[/global-metrics/*](#tag/global-metrics) | Endpoints that return aggregate
    market data such as global market cap and BTC dominance.[/tools/*](#tag/tools)
    \ | Useful utilities such as cryptocurrency-to-fiat price conversions.### Endpoint
    paths follow a pattern matching the type of data providedEndpoint Path  | Endpoint
    Type | Description----------------------|-------------|---------*/latest | Latest
    Market Data | Latest market ticker quotes and averages for cryptocurrencies and
    exchanges.*/historical | Historical Market Data | Intervals of historic market
    data like OHLCV data or data for use in charting libraries.*/info | Metadata |
    Cryptocurrency and exchange metadata like block explorer URLs and logos.*/map
    | ID Maps | Utility endpoints to get a map of resources to CoinMarketCap IDs.###
    \ Cryptocurrency and exchange endpoints provide 2 different ways of accessing
    data depending on purpose- **Listing endpoints:** Flexible paginated `*/listings/*`
    endpoints allow you to sort and filter lists of data like cryptocurrencies by
    market cap or exchanges by volume.- **Item endpoints:** Convenient ID-based resource
    endpoints like `*/quotes/*` and `*/market-pairs/*` allow you to bundle several
    IDs; for example, this allows you to get latest market quotes for a specific set
    of cryptocurrencies in one call.### Full Endpoint ListClick on the endpoint for
    detailed documentation about each endpoint.Type | Endpoint  | Description | Example
    Call-----|--------------|-------------|--------------Cryptocurrency | [/v1/cryptocurrency/info](#operation/getV1CryptocurrencyInfo)
    | Get cryptocurrency metadata | https://pro-api.coinmarketcap.com/v1/cryptocurrency/info?id=1,2,10Cryptocurrency
    | [/v1/cryptocurrency/map](#operation/getV1CryptocurrencyMap) | Get cryptocurrency
    CoinMarketCap ID map | https://pro-api.coinmarketcap.com/v1/cryptocurrency/map?listing_status=active&amp;start=0&amp;limit=100Cryptocurrency
    | [/v1/cryptocurrency/listings/latest](#operation/getV1CryptocurrencyListingsLatest)
    | List all cryptocurrencies (latest)| https://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/latest?sort=market_cap&amp;start=0&amp;limit=10&amp;cryptocurrency_type=tokens&amp;convert=USD,BTCCryptocurrency
    | [/v1/cryptocurrency/market-pairs/latest](#operation/getV1CryptocurrencyMarketpairsLatest)
    | Get cryptocurrency market pairs (latest) | https://pro-api.coinmarketcap.com/v1/cryptocurrency/market-pairs/latest?id=1&amp;convert=LTC,ETHCryptocurrency
    | [/v1/cryptocurrency/ohlcv/historical](#operation/getV1CryptocurrencyOhlcvHistorical)
    | Get cryptocurrency OHLCV values (historical) | https://pro-api.coinmarketcap.com/v1/cryptocurrency/ohlcv/historical?time_start=2017-01-01&amp;id=1&amp;time_start=2017-01-01&amp;time_end=2018-01-01&amp;interval=7d&amp;count=12&amp;convert=CADCryptocurrency
    | [/v1/cryptocurrency/quotes/latest](#operation/getV1CryptocurrencyQuotesLatest)
    | Get cryptocurrency market quotes (latest) | https://pro-api.coinmarketcap.com/v1/cryptocurrency/quotes/latest?symbol=BTC,ETH,XRP,BCH,EOS,LTC,XLM&amp;convert=BTC,ETH,EURCryptocurrency
    | [/v1/cryptocurrency/quotes/historical](#operation/getV1CryptocurrencyQuotesHistorical)
    | Get cryptocurrency market quotes (historical) | https://pro-api.coinmarketcap.com/v1/cryptocurrency/quotes/historical?id=1&amp;time_start=2017&amp;time_end=2018&amp;interval=30d&amp;count=12Exchange
    | [/v1/exchange/info](#operation/getV1ExchangeInfo) | Get exchange metadata |
    https://pro-api.coinmarketcap.com/v1/exchange/info?id=1,2,10Exchange | [/v1/exchange/map](#operation/getV1ExchangeMap)
    | Get exchange to CoinMarketCap ID map | https://pro-api.coinmarketcap.com/v1/exchange/map?listing_status=active&amp;start=0&amp;limit=100Exchange
    | [/v1/exchange/listings/latest](#operation/getV1ExchangeListingsLatest) | List
    all exchanges (latest) | https://pro-api.coinmarketcap.com/v1/exchange/listings/latest?limit=10&amp;market_type=no_fees&amp;convert=USDExchange
    | [/v1/exchange/market-pairs/latest](#operation/getV1ExchangeMarketpairsLatest)
    | Get exchange market pairs (latest) | https://pro-api.coinmarketcap.com/v1/exchange/market-pairs/latest?slug=gdax&amp;convert=LTC,XRP,EURExchange
    | [/v1/exchange/quotes/latest](#operation/getV1ExchangeQuotesLatest) | Get exchange
    market quotes (latest) | https://pro-api.coinmarketcap.com/v1/exchange/quotes/latest?id=2,16&amp;convert=USD,BTC,LTC,EURExchange
    | [/v1/exchange/quotes/historical](#operation/getV1ExchangeQuotesHistorical) |
    Get exchange market quotes (historical) | https://pro-api.coinmarketcap.com/v1/exchange/quotes/historical?id=270&amp;time_start=2018-01-01&amp;time_end=2018-05-01&amp;interval=30d&amp;count=12Global
    Metrics | [/v1/global-metrics/quotes/latest](#operation/getV1GlobalmetricsQuotesLatest)
    | Get aggregate market metrics (latest) | https://pro-api.coinmarketcap.com/v1/global-metrics/quotes/latest?convert=BTC,ETH,LTC,EURGlobal
    Metrics | [/v1/global-metrics/quotes/historical](#operation/getV1GlobalmetricsQuotesHistorical)
    | Get aggregate market metrics (historical) | https://pro-api.coinmarketcap.com/v1/global-metrics/quotes/historical?interval=monthly&amp;count=100Tools
    | [/v1/tools/price-conversion](#operation/getV1ToolsPriceconversion) | Price conversion
    tool | https://pro-api.coinmarketcap.com/v1/tools/price-conversion?symbol=BTC&amp;amount=50&amp;convert=USD,GBP,LTC#
    Standards and ConventionsEach HTTP request must contain the header `Accept: application/json`.
    You should also send an `Accept-Encoding: deflate, gzip` header to receive data
    fast and efficiently.### Endpoint Response Payload FormatAll endpoints return
    data in JSON format with the results of your query under `data` if the call is
    successful.A `Status` object is always included for both successful calls and
    failures when possible. The `Status` object always includes the current time on
    the server when the call was executed as `timestamp`, the number of API call credits
    this call utilized as `credit_count`, and the number of milliseconds it took to
    process the request as `elapsed`. Any details about errors encountered can be
    found under the `error_code` and `error_message`. See [Errors and Rate Limits](#section/Errors-and-Rate-Limits)
    for details on errors.```{  &quot;data&quot; : {    ...  },  &quot;status&quot;:
    {    &quot;timestamp&quot;: &quot;2018-06-06T07:52:27.273Z&quot;,    &quot;error_code&quot;:
    400,    &quot;error_message&quot;: &quot;Invalid value for \\&quot;id\\&quot;&quot;,
    \   &quot;elapsed&quot;: 0,    &quot;credit_count&quot;: 0  }}```### Cryptocurrency,
    Exchange, and Fiat currency identifiers- Cryptocurrencies may be identified in
    endpoints using either the cryptocurrency's unique CoinMarketCap ID as `id` (eg.
    `id=1` for Bitcoin) or the cryptocurrency's symbol (eg. `symbol=BTC` for Bitcoin).
    For a current list of supported cryptocurrencies use our [`/cryptocurrency/map`
    call](#operation/getV1CryptocurrencyMap).- Exchanges may be identified in endpoints
    using either the exchange's unique CoinMarketCap ID as `id` (eg. `id=270` for
    Binance) or the exchange's web slug (eg. `slug=binance` for Binance). For a current
    list of supported exchanges use our [`/exchange/map` call](#operation/getV1ExchangeMap).-
    All fiat currency options use the standard [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)
    currency code (eg. `USD` for the US Dollar). Unless otherwise stated, endpoints
    with fiat currency options support these 32 major currency codes:Currency | Currency
    Code---------|-------------United States dollar ($) | USDAustralian dollar ($)
    | AUDBrazilian real (R$) | BRLCanadian dollar ($) | CADSwiss franc (Fr) | CHFChilean
    peso ($) | CLPChinese yuan (&yen;) | CNYCzech koruna (K\u010D) | CZKDanish krone
    (kr) | DKKEuro (&euro;) | EURBritish pound (&pound;) | GBPHong Kong dollar ($)
    | HKDHungarian forint (Ft) | HUFIndonesian rupiah (  Rp) | IDRIsraeli new shekel
    (\u20AA) | ILSIndian rupee (\u20B9) | INRJapanese yen (&yen;) | JPYSouth Korean
    won (\u20A9) | KRWMexican peso ($) | MXNMalaysian ringgit (RM) | MYRNorwegian
    krone (kr) | NOKNew Zealand dollar ($) | NZDPhilippine piso (\u20B1) | PHPPakistani
    rupee (\u20A8) | PKRPolish z\u0142oty (z\u0142) | PLNRussian ruble (\u20BD) |
    RUBSwedish krona (kr) | SEKSingapore dollar ($) | SGDThai baht (\u0E3F) | THBTurkish
    lira (\u20BA) | TRYNew Taiwan dollar ($) | TWDSouth African rand (R) | ZAR***Note:**
    Using CoinMarketCap IDs is always recommended as cryptocurrency symbols are not
    always unique and can change with a cryptocurrency rebrand. If a symbol is used
    the API will always default to the cryptocurrency with the highest market cap.
    You may use the convenient `/map` endpoints to quickly find the corresponding
    CoinMarketCap ID for a cryptocurrency or exchange.*### Bundling API Calls- Many
    endpoints support ID and crypto/fiat currency conversion bundling. This means
    you can pass multiple comma-separated values to an endpoint to query or convert
    several items at once. Check the `id`, `symbol`, `slug`, and `convert` query parameter
    descriptions in the endpoint documentation to see if this is supported for an
    endpoint.- Endpoints that support bundling return data as an object map instead
    of an array. Each key-value pair will use the identifier you passed in as the
    key.For example, if you passed `symbol=BTC,ETH` to `/v1/cryptocurrency/quotes/latest`
    you would receive:```&quot;data&quot; : {    &quot;BTC&quot; : {      ...    },
    \   &quot;ETH&quot; : {      ...    }}```Or if you passed `id=1,1027` you would
    receive:```&quot;data&quot; : {    &quot;1&quot; : {      ...    },    &quot;1027&quot;
    : {      ...    }}```Price conversions that are returned inside endpoint responses
    behave in the same fashion. These are enclosed in a `quote` object.### Date and
    Time Formats- All endpoints that require date/time parameters allow timestamps
    to be passed in either [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)
    format (eg. `2018-06-06T01:46:40Z`) or in Unix time (eg. `1528249600`). Timestamps
    that are passed in ISO 8601 format support basic and extended notations; if a
    timezone is not included, UTC will be the default.- All timestamps returned in
    JSON payloads are returned in UTC time using human-readable ISO 8601 format which
    follows this pattern: `yyyy-mm-ddThh:mm:ss.mmmZ`. The final `.mmm` designates
    milliseconds. Per the ISO 8601 spec the final `Z` is a constant that represents
    UTC time.- Data is collected, recorded, and reported in UTC time unless otherwise
    specified.### VersioningThe Professional API is versioned to guarantee new features
    and updates are non-breaking. The latest version of this API is `/v1/`.# Errors
    and Rate Limits### API Request ThrottlingUse of the Professional API is subject
    to API call rate limiting or &quot;request throttling&quot; that scales with the
    [usage tier](https://pro.coinmarketcap.com/pricing) tied to your API Key. Free
    / Trial plans are limited to 10 calls a minute. Paid subscription tiers are limited
    to 60 calls a minute. Custom enterprise subscription tiers may have a higher limit.###
    HTTP Status CodesThe API uses standard HTTP status codes to indicate the success
    or failure of an API call.- `400 (Bad Request)` The server could not process the
    request, likely due to an invalid argument.- `401 (Unauthorized)` The request
    lacks valid authentication credentials, likely an issue with your API Key.- `403
    (Forbidden)` The request was rejected due to a permission issue, likely a restriction
    on the API Key's associated service plan.- `429 (Too Many Requests)` The API Key's
    rate limit was exceeded; consider slowing down your API Request frequency if this
    is a request throttling error. Consider upgrading your service plan if you have
    reached your monthly api credit limit.- `500 (Internal Server Error)` An unexpected
    server issue was encountered.### Error Response CodesA `Status` object is always
    included in the JSON response payload for both successful calls and failures when
    possible. You may check this object for additional details about any errors encountered
    under the `error_code` and `error_message` properties.# Best PracticesThis section
    contains a few recommendations on how to efficiently utilize the Professional
    API for your enterprise application, especially if you already have a large base
    of users for your application.### Creating a Robust API IntegrationWhenever implementing
    any 3rd party API service it's highly recommended to implement a &quot;Retry with
    exponential backoff&quot; coding pattern for your REST API call logic. This means
    if your API call happens to get rate limited (HTTP 429) or encounters an unexpected
    server side condition (HTTP 5xx), your code would automatically recover and try
    again using an intelligent recovery scheme. You may use one of the many libraries
    available, for example &lt;a target=&quot;_blank&quot; href=&quot;https://github.com/litl/backoff&quot;&gt;this
    one&lt;/a&gt; for Python.### Implement a Caching StrategyThere are standard legal
    data safeguards built into the &lt;a href=&quot;https://pro.coinmarketcap.com/user-agreement-commercial&quot;
    target=&quot;_blank&quot;&gt;Commercial User Terms&lt;/a&gt; that application
    developers should keep in mind. These Terms help prevent unauthorized scraping
    and redistributing of CMC data but are intentionally worded to allow legitimate
    local caching of market data to support the operation of your application. If
    your application has a significant user base and you are concerned with staying
    within the call credit and API throttling limits of your subscription plan consider
    implementing a data caching strategy.  For example instead of making a /cryptocurrency/quotes/latest
    call every time one of your application's users needs to fetch market rates for
    specific cryptocurrencies, you could pre-fetch and cache the latest market data
    for every cryptocurrency in your application's local database every 60 seconds.
    This would only require 1 API call, /cryptocurrency/listings/latest?limit=5000,
    every 60 seconds. Then, anytime one of your application's users need to load a
    custom list of cryptocurrencies you could simply pull this latest market data
    from your local cache without the overhead of additional calls. This kind of optimization
    is practical for customers with large, demanding user bases.### Reach Out and
    Upgrade Your PlanIf you're uncertain how to best implement the Professional API
    in your application you can reach out to api@coinmarketcap.com. If your current
    or future needs outgrow our current self-serve subscription tiers please contact
    us. We'll review your needs and budget and may be able to tailor a custom enterprise
    plan that is right for you."
  termsOfService: https://coinmarketcap.com/terms/
  version: 1.0.0
host: pro-api.coinmarketcap.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/cryptocurrency/info:
    get:
      summary: Get metadata
      description: Returns all static metadata for one or more cryptocurrencies including
        name, symbol, logo, and its various registered URLs
      operationId: getV1CryptocurrencyInfo
      parameters:
      - in: query
        name: id
        description: One or more comma-separated CoinMarketCap cryptocurrency IDs
      - in: query
        name: symbol
        description: Alternatively pass one or more comma-separated cryptocurrency
          symbols
      responses:
        200:
          description: OK
      tags:
      - blockchain
      - metadata
definitions:
  Cryptocurrencies Info - URLs object:
    properties:
      website:
        description: This is a default description.
        type: get
      explorer:
        description: This is a default description.
        type: get
      source_code:
        description: This is a default description.
        type: get
      message_board:
        description: This is a default description.
        type: get
      chat:
        description: This is a default description.
        type: get
      announcement:
        description: This is a default description.
        type: get
      reddit:
        description: This is a default description.
        type: get
      twitter:
        description: This is a default description.
        type: get
  Cryptocurrencies Info - Cryptocurrency object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      category:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      logo:
        description: This is a default description.
        type: get
      tags:
        description: This is a default description.
        type: get
  Cryptocurrency Info - Results map:
    properties: []
  API Status Object:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      error_code:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      credit_count:
        description: This is a default description.
        type: get
  Cryptocurrencies Info - Response Model:
    properties: []
  status:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      error_code:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      credit_count:
        description: This is a default description.
        type: get
  HTTP Status 400 Error Object:
    properties: []
  status 1:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      error_code:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      credit_count:
        description: This is a default description.
        type: get
  HTTP Status 401 Error Object:
    properties: []
  status 2:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      error_code:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      credit_count:
        description: This is a default description.
        type: get
  HTTP Status 403 Error Object:
    properties: []
  status 3:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      error_code:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      credit_count:
        description: This is a default description.
        type: get
  HTTP Status 429 Error Object:
    properties: []
  status 4:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      error_code:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      credit_count:
        description: This is a default description.
        type: get
  HTTP Status 500 Error Object:
    properties: []
  Cryptocurrency Map - Cryotocurrency Object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      is_active:
        description: This is a default description.
        type: get
      first_historical_data:
        description: This is a default description.
        type: get
      last_historical_data:
        description: This is a default description.
        type: get
  Cryptocurrency Map - Response Model:
    properties:
      data:
        description: This is a default description.
        type: get
  Exchanges Info - URLs object:
    properties:
      website:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      chat:
        description: This is a default description.
        type: get
      fee:
        description: This is a default description.
        type: get
      twitter:
        description: This is a default description.
        type: get
  Exchanges Info - Exchange Info object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      logo:
        description: This is a default description.
        type: get
  Exchanges Info - Results map:
    properties: []
  Exchanges Info - Response Model:
    properties: []
  Exchange Map - Exchange Object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      is_active:
        description: This is a default description.
        type: get
      first_historical_data:
        description: This is a default description.
        type: get
      last_historical_data:
        description: This is a default description.
        type: get
  Exchange Map - Response Model:
    properties:
      data:
        description: This is a default description.
        type: get
  Tools Price Conversion - Quote object:
    properties:
      price:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Tools Price Conversion - Quotes map:
    properties: []
  Tools Price Conversion - Results Object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      amount:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Tools Price Conversion - Response Model:
    properties: []
  Cryptocurrency Listings Historical - Quote object:
    properties:
      price:
        description: This is a default description.
        type: get
      volume_24h:
        description: This is a default description.
        type: get
      market_cap:
        description: This is a default description.
        type: get
      percent_change_1h:
        description: This is a default description.
        type: get
      percent_change_24h:
        description: This is a default description.
        type: get
      percent_change_7d:
        description: This is a default description.
        type: get
  Cryptocurrency Listings Historical - Quote map:
    properties: []
  Cryptocurrency Listings Historical - Cryptocurrency object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      cmc_rank:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      circulating_supply:
        description: This is a default description.
        type: get
      total_supply:
        description: This is a default description.
        type: get
      max_supply:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Cryptocurrency Listings Historical - Response Model:
    properties:
      data:
        description: This is a default description.
        type: get
  Cryptocurrency Listings Latest - Quote object:
    properties:
      price:
        description: This is a default description.
        type: get
      volume_24h:
        description: This is a default description.
        type: get
      market_cap:
        description: This is a default description.
        type: get
      percent_change_1h:
        description: This is a default description.
        type: get
      percent_change_24h:
        description: This is a default description.
        type: get
      percent_change_7d:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Cryptocurrency Listings Latest - Quote map:
    properties: []
  Cryptocurrency Listings Latest - Cryptocurrency object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      cmc_rank:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      circulating_supply:
        description: This is a default description.
        type: get
      total_supply:
        description: This is a default description.
        type: get
      max_supply:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Cryptocurrency Listings Latest - Response Model:
    properties:
      data:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Exchange Info object:
    properties:
      exchange_id:
        description: This is a default description.
        type: get
      exchange_slug:
        description: This is a default description.
        type: get
      exchange_name:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Pair Base Currency Info object:
    properties:
      currency_id:
        description: This is a default description.
        type: get
      currency_symbol:
        description: This is a default description.
        type: get
      currency_type:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Pair Base Currency Info object 1:
    properties:
      currency_id:
        description: This is a default description.
        type: get
      currency_symbol:
        description: This is a default description.
        type: get
      currency_type:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Market Pair Quote:
    properties:
      price:
        description: This is a default description.
        type: get
      volume_24h_base:
        description: This is a default description.
        type: get
      volume_24h_quote:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Market Pair Quote object:
    properties: []
  Cryptocurrency Market Pairs Latest - Market Pair Info object:
    properties:
      market_pair:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Results object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      market_pairs:
        description: This is a default description.
        type: get
  Cryptocurrency Market Pairs Latest - Response Model:
    properties: []
  Cryptocurrency OHLCV Historical - Quote object:
    properties:
      open:
        description: This is a default description.
        type: get
      high:
        description: This is a default description.
        type: get
      low:
        description: This is a default description.
        type: get
      close:
        description: This is a default description.
        type: get
      volume:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  Cryptocurrency OHLCV Historical - Quote map:
    properties: []
  Cryptocurrency OHLCV Historical - Interval Quote object:
    properties:
      time_open:
        description: This is a default description.
        type: get
      time_close:
        description: This is a default description.
        type: get
  Cryptocurrency OHLCV Historical - Results object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      quotes:
        description: This is a default description.
        type: get
  Cryptocurrency OHLCV Historical - Response Model:
    properties: []
  Cryptocurrency Quotes Historical - Currency Quote object:
    properties:
      price:
        description: This is a default description.
        type: get
      volume_24hr:
        description: This is a default description.
        type: get
      market_cap:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Cryptocurrency Quotes Historical - Quote currency map:
    properties: []
  Cryptocurrency Quotes Historical - Interval Quote object:
    properties:
      timestamp:
        description: This is a default description.
        type: get
  Cryptocurrency Quotes Historical - Result object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      quotes:
        description: This is a default description.
        type: get
  Cryptocurrency Quotes Historical - Results map:
    properties: []
  Cryptocurrency Quotes Historical - Response Model:
    properties: []
  Cryptocurrency Quotes Latest - Quote map:
    properties: []
  Cryptocurrency Quotes Latest - Cryptocurrency object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      symbol:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      cmc_rank:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      circulating_supply:
        description: This is a default description.
        type: get
      total_supply:
        description: This is a default description.
        type: get
      max_supply:
        description: This is a default description.
        type: get
      date_added:
        description: This is a default description.
        type: get
  Cryptocurrency Quotes Latest - Cryptocurrency Results map:
    properties: []
  Cryptocurrency Quotes Latest - Response Model:
    properties: []
  Exchange Listings Historical - Quote object:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      volume_24h:
        description: This is a default description.
        type: get
      volume_7d:
        description: This is a default description.
        type: get
      volume_30d:
        description: This is a default description.
        type: get
      percent_change_volume_24h:
        description: This is a default description.
        type: get
      percent_change_volume_7d:
        description: This is a default description.
        type: get
      percent_change_volume_30d:
        description: This is a default description.
        type: get
  Exchange Listings Historical - Quote map:
    properties: []
  Exchange Listings Historical - Exchange object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      cmc_rank:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  Exchange Listings Historical - Response Model:
    properties:
      data:
        description: This is a default description.
        type: get
  Exchange Listings Latest - Quote object:
    properties:
      volume_24h:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Exchange Listings Latest - Quote map:
    properties: []
  Exchange Listings Latest - Exchange object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      cmc_rank:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Exchange Listings Latest - Response Model:
    properties:
      data:
        description: This is a default description.
        type: get
  Exchange Market Pairs Latest - Pair Base Currency Info object:
    properties:
      currency_id:
        description: This is a default description.
        type: get
      currency_symbol:
        description: This is a default description.
        type: get
      currency_type:
        description: This is a default description.
        type: get
  Exchange Market Pairs Latest - Market Pair Info object:
    properties:
      market_pair:
        description: This is a default description.
        type: get
  Exchange Market Pairs Latest - Results object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      market_pairs:
        description: This is a default description.
        type: get
  Exchange Market Pairs Latest - Response Model:
    properties: []
  Exchange Historical Quotes - Currency Quote object:
    properties:
      volume_24hr:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  Exchange Historical Quotes - Quote currency map:
    properties: []
  Exchange Historical Quotes - nterval Quote object:
    properties:
      timestamp:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
  Exchange Historical Quotes - exchange object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      quotes:
        description: This is a default description.
        type: get
  Exchange Historical Quotes - Results map:
    properties: []
  Exchange Historical Quotes - Response Model:
    properties: []
  Exchange Quotes Latest - Quote object:
    properties:
      volume_24h:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Exchange Quotes Latest - Quote map:
    properties: []
  Exchange Quotes Latest - Exchange object:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      num_market_pairs:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Exchange Quotes Latest - Exchange Results map:
    properties: []
  Exchange Quotes Latest - Response Model:
    properties: []
  Global Metrics Quotes Historic - Currency Quote object:
    properties:
      total_market_cap:
        description: This is a default description.
        type: get
      total_volume_24h:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  Global Metrics Quotes Historic - Quote currency map:
    properties: []
  Global Metrics Quotes Historic - Interval Quote object:
    properties:
      btc_dominance:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  Global Metrics Quotes Historic - Results object:
    properties:
      quotes:
        description: This is a default description.
        type: get
  Global Metrics Quotes Historic - Response Model:
    properties: []
  Global Metrics Quotes Latest - Quote object:
    properties:
      total_market_cap:
        description: This is a default description.
        type: get
      total_volume_24h:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Global Metrics Quotes Latest - Quote map:
    properties: []
  Global Metrics Quotes Latest - Results Object:
    properties:
      btc_dominance:
        description: This is a default description.
        type: get
      eth_dominance:
        description: This is a default description.
        type: get
      active_cryptocurrencies:
        description: This is a default description.
        type: get
      active_market_pairs:
        description: This is a default description.
        type: get
      active_exchanges:
        description: This is a default description.
        type: get
      last_updated:
        description: This is a default description.
        type: get
  Global Metrics Quotes Latest - Response Model:
    properties: []
x-collection-name: CoinMarketCap
x-streamrank:
  polling_total_time_average: "0.3"
  polling_size_download_average: "1676.7"
  streaming_total_time_average: "0.25"
  streaming_size_download_average: "841.7"
  change_yes: "5"
  change_no: "5"
  time_percentage: "19"
  size_percentage: "50"
  change_percentage: "50"
  last_run: "2018-09-09"
  days_run: "0"
  minute_run: "0"
---