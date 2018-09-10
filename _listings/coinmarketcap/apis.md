---
name: CoinMarketCap
x-slug: coinmarketcap
description: Cryptocurrency market cap rankings, charts, and more
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
x-kinRank: "7"
x-alexaRank: "276"
tags: StreamRank
created: "2018-09-10"
modified: "2018-09-10"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/apis.md
specificationVersion: "0.14"
apis:
- name: CoinMarketCap Professional API Documentation - Get metadata
  x-api-slug: v1cryptocurrencyinfo-get
  description: |-
    Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.

    **This endpoint is available on the following API plans:**
    - Starter
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/v1cryptocurrencyinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/v1cryptocurrencyinfo-get-openapi.md
- name: CoinMarketCap Professional API Documentation - List all cryptocurrencies (latest)
  x-api-slug: v1cryptocurrencylistingslatest-get
  description: "Get a paginated list of all cryptocurrencies with latest market data.
    You can configure this call to sort by market cap or another market ranking field.
    Use the \"convert\" option to return market values in multiple fiat and cryptocurrency
    conversions in the same call.   \n\n\nCryptocurrencies are listed by CoinMarketCap
    Rank by default. You may optionally sort against any of the following:\n**name**:
    The cryptocurrency name.\n**symbol**: The cryptocurrency symbol.\n**date_added**:
    Date cryptocurrency was added to the system.\n**market_cap**: market cap (latest
    trade price x circulating supply).\n**price**: latest average trade price across
    markets.\n**circulating_supply**: approximate number of coins currently in circulation.\n**total_supply**:
    approximate total amount of coins in existence right now (minus any coins that
    have been verifiably burned).\n**max_supply**: our best approximation of the maximum
    amount of coins that will ever exist in the lifetime of the currency.\n**num_market_pairs**:
    number of market pairs across all exchanges trading each currency.\n**volume_24h**:
    24 hour trading volume for each currency.\n**percent_change_1h**: 1 hour trading
    price percentage change for each currency.\n**percent_change_24h**: 24 hour trading
    price percentage change for each currency.\n**percent_change_7d**: 7 day trading
    price percentage change for each currency.\n\n  **This endpoint is available on
    the following API plans:**\n  - Starter\n  - Hobbyist\n  - Standard\n  - Professional\n
    \ - Enterprise\n\n**Cache / Update frequency:** Every ~1 minute. \n  \n*NOTE:
    Use this endpoint if you need a sorted and paginated list of cryptocurrencies.
    If you want to query for market data on a few specific cryptocurrencies use /v1/cryptocurrency/quotes/latest
    which is optimized for that purpose. The response data between these endpoints
    is otherwise the same.*"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/v1cryptocurrencylistingslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/v1cryptocurrencylistingslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get market quotes (latest)
  x-api-slug: v1cryptocurrencyquoteslatest-get
  description: |-
    Get the latest market quote for 1 or more cryptocurrencies. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.

    **This endpoint is available on the following API plans:**
    - Starter
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Every ~1 minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/v1cryptocurrencyquoteslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/coinmarketcap/v1cryptocurrencyquoteslatest-get-openapi.md
x-common:
- type: x-github
  url: https://github.com/coinmarketcap
- type: x-openapi
  url: https://pro-api.coinmarketcap.com/swagger.json
- type: x-api-gallery
  url: http://coinfabrik.api.gallery.streamdata.io
- type: x-email
  url: legal@coinmarketcap.com
- type: x-twitter
  url: https://twitter.com/CoinMarketCap
- type: x-website
  url: https://pro.coinmarketcap.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---