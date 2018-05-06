---
swagger: "2.0"
info:
  title: Disqus
  description: Welcome to the Disqus Web API. The API enables developers to communicate
    with Disqus data from within their own applications.
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /forums/interestingForums.json:
    get:
      summary: Forums InterestingForums
      description: "\n     Forums InterestingForums "
      operationId: forums-interestingforums
      parameters:
      - in: query
        name: limit
        description: Defaults to 5                         Maximum value of 100
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - forums
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.17"
  polling_size_download_average: "10724.69"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "5392.64"
  change_yes: "346"
  change_no: "52"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "87"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---