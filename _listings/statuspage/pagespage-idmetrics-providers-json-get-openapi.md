---
swagger: "2.0"
info:
  title: StatusPage.io
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /pages/[page_id]/metrics_providers.json:
    get:
      summary: Get a list of metric providers linked to your page
      description: Get a list of metric providers linked to your page
      operationId: get-a-list-of-metric-providers-linked-to-your-page
      x-api-path-slug: pagespage-idmetrics-providers-json-get
      responses:
        200:
          description: OK
      tags:
      - metric providers
definitions: []
x-collection-name: StatusPage
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---