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
      x-api-path-slug: usersinterestingusersjson-get
      responses:
        200:
          description: OK
      tags:
      - users
      - interesting
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.22"
  polling_size_download_average: "5741.75"
  streaming_total_time_average: "0.12"
  streaming_size_download_average: "2875.24"
  change_yes: "11679"
  change_no: "215"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "98"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---