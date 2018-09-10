---
swagger: "2.0"
info:
  title: The Guardian
  description: The Guardian Content API is a public service for accessing all the
    content the Guardian creates and the collections we have of that content (tags
    and sections). There are over one and a half million items available published
    as far back as 1999. This overview will give you some idea of what data is available,
    how to find what you need, and what you will see when you make a request to us.
  version: v1
host: content.guardianapis.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search:
    get:
      summary: Search
      description: Searches news content across the Guardian news platform
      operationId: search
      x-api-path-slug: search-get
      responses:
        200:
          description: OK
      tags:
      - news
definitions: []
x-collection-name: The Guardian
x-streamrank:
  polling_total_time_average: "0.56"
  polling_size_download_average: "2071.42"
  streaming_total_time_average: "0.31"
  streaming_size_download_average: "1036.81"
  change_yes: "218"
  change_no: "3225"
  time_percentage: "44"
  size_percentage: "50"
  change_percentage: "6"
  last_run: "2018-05-06"
  days_run: "20"
  minute_run: "0"
---