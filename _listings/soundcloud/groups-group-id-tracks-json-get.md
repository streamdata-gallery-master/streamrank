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
  /groups/{group_id}/tracks.json:
    get:
      summary: Get Groups Tracks
      description: Returns a collection of tracks contributed to the group with group
        id
      operationId: getGroupsGroupTracks.json
      parameters:
      - in: query
        name: consumer_key
      responses:
        200:
          description: OK
      tags:
      - groups
      - tracks
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