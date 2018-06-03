---
swagger: "2.0"
info:
  title: Sound Cloud
  description: Access, host, upload, and comment on audio.
  version: 1.0.0
host: api.soundcloud.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{group_id}/contributors.json:
    get:
      summary: Get Groups Contributors
      description: Returns a collection of contributors of the group with group id
      operationId: getGroupsGroupContributors.json
      parameters:
      - in: query
        name: consumer_key
      responses:
        200:
          description: OK
      tags:
      - groups
      - contributors
definitions: []
x-collection-name: SoundCloud
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