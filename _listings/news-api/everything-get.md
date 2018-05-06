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
  everything/:
    get:
      summary: Everything
      description: Search through millions of articles from over 5,000 large and small
        news sources and blogs
      operationId: getEverything
      parameters:
      - in: header
        name: apiKey
        description: Your API key
        type: string
        format: string
      - in: query
        name: domains
        description: A comma-seperated string of domains (eg bbc
        type: string
        format: string
      - in: query
        name: page
        description: Use this to page through the results
        type: integer
        format: string
      - in: query
        name: pageSize
        description: The number of results to return per page
        type: integer
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