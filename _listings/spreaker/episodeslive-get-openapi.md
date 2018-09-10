---
swagger: "2.0"
info:
  title: Spreaker API
  version: v1
host: api.spreaker.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /episodes/live:
    get:
      summary: Get Live Episodes
      description: Retrieves all live episodes at the moment of the request
      operationId: getEpisodesLive
      x-api-path-slug: episodeslive-get
      parameters:
      - in: query
        name: show_id
        description: An list of show_id applied as a filter
      responses:
        200:
          description: OK
      tags:
      - podcasts
      - live
      - episodes
definitions: []
x-collection-name: Spreaker
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