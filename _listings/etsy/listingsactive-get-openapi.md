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
  /listings/active:
    get:
      summary: Get Listings Active
      description: Finds all active Listing
      operationId: getListingsActive
      x-api-path-slug: listingsactive-get
      parameters:
      - in: query
        name: category
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: color
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: color_accuracy
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: keywords
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: limit
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: materials
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: max_price
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: min_price
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: sort_on
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: sort_order
        description: Bring Etsy's handmade marketplace and community into your apps
      - in: query
        name: tags
        description: Bring Etsy's handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - listings
      - active
definitions: []
x-collection-name: Etsy
x-streamrank:
  polling_total_time_average: "0.68"
  polling_size_download_average: "30847.64"
  streaming_total_time_average: "0.35"
  streaming_size_download_average: "15661.32"
  change_yes: "37"
  change_no: "96"
  time_percentage: "48"
  size_percentage: "49"
  change_percentage: "28"
  last_run: "2018-09-10"
  days_run: "1"
  minute_run: "0"
---