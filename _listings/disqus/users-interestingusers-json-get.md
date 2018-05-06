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
  /users/interestingUsers.json:
    get:
      summary: Interesting Users
      description: Interesting Users
      operationId: interestingUsers
      responses:
        200:
          description: OK
      tags:
      - users
      - interesting
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.2"
  polling_size_download_average: "5368.2"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "2689.4"
  change_yes: "2356"
  change_no: "201"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "92"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---