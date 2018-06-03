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
  /projects/{PROJECT_ID}/stories/{STORY_ID}/tasks:
    get:
      summary: Get Projects Project Stories Story Tasks
      description: Get projects project stories story tasks
      operationId: getProjectsProjectStoriesStoryTasks
      parameters:
      - in: path
        name: PROJECT_ID
        description: The ID of the project
      - in: path
        name: STORY_ID
        description: The ID of the story
      responses:
        200:
          description: OK
      tags:
      - projects
      - project
      - id
      - stories
      - story
      - id
      - tasks
definitions: []
x-collection-name: Pivotal Tracker
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