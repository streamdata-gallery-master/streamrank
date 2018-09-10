---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 0
info:
  title: Etsy Get Trending Listings
  description: Collects the list of listings used to generate the trending listing
    page.
  version: 1.0.0
host: openapi.etsy.com
basePath: /v2/private/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /listings/active:
    get:
      summary: Get Listings Active
      description: Finds all active Listing
      operationId: getListingsActive
      x-api-path-slug: listingsactive-get
      parameters:
      - in: query
        name: category
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: color
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: color_accuracy
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: keywords
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: materials
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: max_price
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: min_price
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: sort_on
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: sort_order
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: tags
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Listings
      - Active
  /listings/interesting:
    get:
      summary: Get Interesting Listings
      description: Collects the list of interesting listings
      operationId: getInterestingListings
      x-api-path-slug: listingsinteresting-get
      responses:
        200:
          description: OK
      tags:
      - Products
      - Commerce
  /listings/trending:
    get:
      summary: Get Trending Listings
      description: Collects the list of listings used to generate the trending listing
        page.
      operationId: getTrendingListings
      x-api-path-slug: listingstrending-get
      responses:
        200:
          description: OK
      tags:
      - Products
      - Commerce
      - Trending
x-streamrank:
  polling_total_time_average: "0.92"
  polling_size_download_average: "53326"
  streaming_total_time_average: "0.5"
  streaming_size_download_average: "26663"
  change_yes: "1"
  change_no: "1"
  time_percentage: "46"
  size_percentage: "50"
  change_percentage: "50"
  last_run: "2018-09-09"
  days_run: "0"
  minute_run: "0"
---