---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Search Code
  description: Search code.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{username}/orgs:
    get:
      summary: Get Users Username Orgs
      description: List all public organizations for a user.
      operationId: list-all-public-organizations-for-a-user
      x-api-path-slug: usersusernameorgs-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: username
        description: Name of user
      responses:
        200:
          description: OK
      tags:
      - Users
      - Username
      - Orgs
  /user/orgs:
    get:
      summary: Get User Orgs
      description: List public and private organizations for the authenticated user.
      operationId: list-public-and-private-organizations-for-the-authenticated-user
      x-api-path-slug: userorgs-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      responses:
        200:
          description: OK
      tags:
      - User
      - Orgs
  /search/code:
    get:
      summary: Get Search Code
      description: Search code.
      operationId: search-code
      x-api-path-slug: searchcode-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: The search terms
      - in: query
        name: sort
        description: Can only be indexed, which indicates how recently a file has
          been indexedby the GitHub search infrastructure
      responses:
        200:
          description: OK
      tags:
      - Search
      - Code
x-streamrank:
  polling_total_time_average: "0.73"
  polling_size_download_average: "138484.75"
  streaming_total_time_average: "0.39"
  streaming_size_download_average: "69273.99"
  change_yes: "2167"
  change_no: "166"
  time_percentage: "46"
  size_percentage: "50"
  change_percentage: "93"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---