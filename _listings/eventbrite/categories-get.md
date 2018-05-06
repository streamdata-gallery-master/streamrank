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
  polling_total_time_average: ~
  polling_size_download_average: ~
  streaming_total_time_average: ~
  streaming_size_download_average: ~
  change_yes: ~
  change_no: ~
  time_percentage: ~
  size_percentage: ~
  change_percentage: ~
  last_run: ~
  days_run: ~
  minute_run: ~
---