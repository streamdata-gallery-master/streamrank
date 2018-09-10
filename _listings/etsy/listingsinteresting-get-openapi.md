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
      - products
      - commerce
definitions: []
x-collection-name: Etsy
x-streamrank:
  polling_total_time_average: "0.52"
  polling_size_download_average: "25028.62"
  streaming_total_time_average: "0.27"
  streaming_size_download_average: "12700.77"
  change_yes: "2"
  change_no: "131"
  time_percentage: "48"
  size_percentage: "49"
  change_percentage: "2"
  last_run: "2018-09-10"
  days_run: "1"
  minute_run: "0"
---