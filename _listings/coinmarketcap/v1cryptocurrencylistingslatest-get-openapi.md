---
swagger: "2.0"
x-collection-name: CoinMarketCap
x-complete: 0
info:
  title: CoinMarketCap List all cryptocurrencies (latest)
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
      description: |-
        Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.

        **This endpoint is available on the following API plans:**
        - Starter
        - Hobbyist
        - Standard
        - Professional
        - Enterprise

        **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
      operationId: getV1CryptocurrencyInfo
      x-api-path-slug: v1cryptocurrencyinfo-get
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
      - Blockchain
      - Metadata
  /v1/cryptocurrency/listings/latest:
    get:
      summary: List all cryptocurrencies (latest)
      description: "Get a paginated list of all cryptocurrencies with latest market
        data. You can configure this call to sort by market cap or another market
        ranking field. Use the \"convert\" option to return market values in multiple
        fiat and cryptocurrency conversions in the same call.   \n\n\nCryptocurrencies
        are listed by CoinMarketCap Rank by default. You may optionally sort against
        any of the following:\n**name**: The cryptocurrency name.\n**symbol**: The
        cryptocurrency symbol.\n**date_added**: Date cryptocurrency was added to the
        system.\n**market_cap**: market cap (latest trade price x circulating supply).\n**price**:
        latest average trade price across markets.\n**circulating_supply**: approximate
        number of coins currently in circulation.\n**total_supply**: approximate total
        amount of coins in existence right now (minus any coins that have been verifiably
        burned).\n**max_supply**: our best approximation of the maximum amount of
        coins that will ever exist in the lifetime of the currency.\n**num_market_pairs**:
        number of market pairs across all exchanges trading each currency.\n**volume_24h**:
        24 hour trading volume for each currency.\n**percent_change_1h**: 1 hour trading
        price percentage change for each currency.\n**percent_change_24h**: 24 hour
        trading price percentage change for each currency.\n**percent_change_7d**:
        7 day trading price percentage change for each currency.\n\n  **This endpoint
        is available on the following API plans:**\n  - Starter\n  - Hobbyist\n  -
        Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:**
        Every ~1 minute. \n  \n*NOTE: Use this endpoint if you need a sorted and paginated
        list of cryptocurrencies. If you want to query for market data on a few specific
        cryptocurrencies use /v1/cryptocurrency/quotes/latest which is optimized for
        that purpose. The response data between these endpoints is otherwise the same.*"
      operationId: getV1CryptocurrencyListingsLatest
      x-api-path-slug: v1cryptocurrencylistingslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: cryptocurrency_type
        description: The type of cryptocurrency to include
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: sort
        description: What field to sort the list of cryptocurrencies by
      - in: query
        name: sort_dir
        description: The direction in which to order cryptocurrencies against the
          specified sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Cryptocurrencies
      - (latest)
x-streamrank:
  polling_total_time_average: "0.15"
  polling_size_download_average: "88194"
  streaming_total_time_average: "0.15"
  streaming_size_download_average: "88194"
  change_yes: "1"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "100"
  last_run: "2018-09-09"
  days_run: "0"
  minute_run: "0"
---