---
swagger: "2.0"
info:
  title: News API
  description: Get breaking news headlines, and search for articles from over 5,000
    news sources and blogs with our news API.
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
  sources/:
    get:
      summary: Sources
      description: This endpoint returns the subset of news publishers that top headlines
        (/v2/top-headlines) are available from
      operationId: getsources
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
        name: country
        description: Find sources that display news in a specific country
        type: string
        format: string
      - in: query
        name: language
        description: Find sources that display news in a specific language
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - news
definitions: []
x-collection-name: News API
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