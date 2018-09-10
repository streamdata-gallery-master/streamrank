---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Orgs Org Issues
  description: |-
    List issues.
    List all issues for a given organization for the authenticated user.
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
  /orgs/{org}/events:
    get:
      summary: Get Orgs Org Events
      description: List public events for an organization.
      operationId: list-public-events-for-an-organization
      x-api-path-slug: orgsorgevents-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Events
  /orgs/{org}/issues:
    get:
      summary: Get Orgs Org Issues
      description: |-
        List issues.
        List all issues for a given organization for the authenticated user.
      operationId: list-issueslist-all-issues-for-a-given-organization-for-the-authenticated-user
      x-api-path-slug: orgsorgissues-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
      - in: query
        name: filter
        description: Issues assigned to you / created by you / mentioning you / youresubscribed
          to updates for / All issues the authenticated user can see
      - in: query
        name: labels
        description: String list of comma separated Label names
      - in: path
        name: org
        description: Name of organisation
      - in: query
        name: since
        description: 'Optional string of a timestamp in ISO 8601 format: YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: sort
      - in: query
        name: state
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Issues
x-streamrank:
  polling_total_time_average: "0.09"
  polling_size_download_average: "65.33"
  streaming_total_time_average: "0.07"
  streaming_size_download_average: "64.67"
  change_yes: "3"
  change_no: "0"
  time_percentage: "30"
  size_percentage: "1"
  change_percentage: "100"
  last_run: "2018-05-04"
  days_run: "0"
  minute_run: "0"
---