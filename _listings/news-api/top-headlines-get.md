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
  top-headlines/:
    get:
      summary: Top Headlines
      description: This endpoint provides live top and breaking headlines for a country,
        specific category in a country, single source, or multiple sources
      operationId: getTopHeadlines
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
      - news
definitions: []
x-collection-name: News API
x-streamrank:
  polling_total_time_average: "0.2"
  polling_size_download_average: "12416.53"
  streaming_total_time_average: "0.12"
  streaming_size_download_average: "6221.95"
  change_yes: "800"
  change_no: "6298"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "11"
  last_run: "2018-02-21"
  days_run: "5"
  minute_run: "0"
---