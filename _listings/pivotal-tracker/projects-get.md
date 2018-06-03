---
swagger: "2.0"
info:
  title: Pivotal Tracker
  description: Access and manipulate agile project management data including projects,
    stories and tasks.
  version: 1.0.0
host: www.pivotaltracker.com
basePath: /services/v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /projects:
    get:
      summary: Get Projects
      description: Retrieves all of the user's projects
      operationId: getProjects
      responses:
        200:
          description: OK
      tags:
      - projects
definitions: []
x-collection-name: Pivotal Tracker
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