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
      x-api-path-slug: listingstrending-get
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
  polling_total_time_average: "0.53"
  polling_size_download_average: "26707"
  streaming_total_time_average: "0.28"
  streaming_size_download_average: "13353.5"
  change_yes: "2"
  change_no: "130"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "2"
  last_run: "2018-09-10"
  days_run: "1"
  minute_run: "0"
---