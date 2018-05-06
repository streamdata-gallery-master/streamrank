---
swagger: "2.0"
info:
  title: Eventbrite
  description: The Eventbrite API is the best way to integrate and extend Eventbrite
    for your event or organising needs. Version 3 of the API brings you faster responses,
    consistent data types, more endpoints, and easier debugging and testing.
  version: 1.0.0
host: www.eventbriteapi.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /categories/:
    get:
      summary: Get Categories
      description: |-
        Returns a list of category as categories, including
        subcategories nested
      operationId: getCategories
      responses:
        200:
          description: OK
      tags:
      - categories
definitions: []
x-collection-name: Eventbrite
x-streamrank:
  polling_total_time_average: "0.21"
  polling_size_download_average: "4760.28"
  streaming_total_time_average: "0.11"
  streaming_size_download_average: "2380.14"
  change_yes: "3"
  change_no: "497"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---