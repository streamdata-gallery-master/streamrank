---
swagger: "2.0"
x-collection-name: News API
x-complete: 0
info:
  title: News API Top Headlines
  description: This endpoint provides live top and breaking headlines for a country,
    specific category in a country, single source, or multiple sources. You can also
    search with keywords. Articles are sorted by the earliest date published first.
  termsOfService: https://newsapi.org/terms
  version: 1.0.0
host: newsapi.org
basePath: v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  top-headlines/:
    get:
      summary: Top Headlines
      description: This endpoint provides live top and breaking headlines for a country,
        specific category in a country, single source, or multiple sources. You can
        also search with keywords. Articles are sorted by the earliest date published
        first.
      operationId: getTopHeadlines
      x-api-path-slug: topheadlines-get
      parameters:
      - in: header
        name: apiKey
        description: Your API key
        type: string
        format: string
      - in: query
        name: category
        description: Find sources that display news of this category
        type: string
        format: string
      - in: query
        name: page
        description: Use this to page through the results
        type: string
        format: string
      - in: query
        name: pageSize
        description: The number of results to return per page
        type: string
        format: string
      - in: query
        name: q
        description: Keywords or phrases to search for
        type: string
        format: string
      - in: query
        name: sources
        description: A comma-seperated string of identifiers (maximum 20) for the
          news sources or blogs you want headlines from
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - News
x-streamrank:
  polling_total_time_average: "0.21"
  polling_size_download_average: "12418.37"
  streaming_total_time_average: "0.12"
  streaming_size_download_average: "6222.76"
  change_yes: "1830"
  change_no: "7430"
  time_percentage: "42"
  size_percentage: "50"
  change_percentage: "20"
  last_run: "2018-05-12"
  days_run: "26"
  minute_run: "0"
---