---
swagger: "2.0"
info:
  title: Etsy
  description: Bring Etsy's handmade marketplace and community into your apps.
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
  /listings/trending:
    get:
      summary: Get Trending Listings
      description: Collects the list of listings used to generate the trending listing
        page
      operationId: getTrendingListings
      responses:
        200:
          description: OK
      tags:
      - products
      - commerce
      - trending
definitions: []
x-collection-name: Etsy
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