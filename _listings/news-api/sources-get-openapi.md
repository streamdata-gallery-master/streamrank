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
      x-api-path-slug: sources-get
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
  polling_total_time_average: "0.19"
  polling_size_download_average: "39818.02"
  streaming_total_time_average: "0.11"
  streaming_size_download_average: "19982.96"
  change_yes: "21"
  change_no: "2143"
  time_percentage: "42"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "7"
  minute_run: "0"
---