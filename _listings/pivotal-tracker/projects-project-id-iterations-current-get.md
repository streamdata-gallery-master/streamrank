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
  /projects/{PROJECT_ID}/iterations/current:
    get:
      summary: Get Projects Project Iterations Current
      description: Retrieves iterations from the "current" group, with stories
      operationId: getProjectsProjectIterationsCurrent
      parameters:
      - in: path
        name: PROJECT_ID
        description: The ID of the project
      responses:
        200:
          description: OK
      tags:
      - projects
      - project
      - id
      - iterations
      - current
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