---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Forums ListThreads
  description: Forums ListThreads
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
  /forums/listFollowers.json:
    get:
      summary: Forums ListFollowers
      description: Forums ListFollowers
      operationId: forums-listfollowers
      x-api-path-slug: forumslistfollowers-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Lists
  /forums/listThreads.json:
    get:
      summary: Forums ListThreads
      description: Forums ListThreads
      operationId: forums-listthreads
      x-api-path-slug: forumslistthreads-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: include
        description: 'Defaults to [  open,  closed]                         Choices:
          open, closed, killed'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID You may pass us the &#39;ident&#39; query type instead of an ID by including
          &#39;forum&#39;
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
      - Lists
x-streamrank:
  polling_total_time_average: "0.32"
  polling_size_download_average: "24075.83"
  streaming_total_time_average: "0.17"
  streaming_size_download_average: "12039.41"
  change_yes: "381"
  change_no: "830"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "31"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---