---
swagger: "2.0"
info:
  title: PagerDuty
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /notifications:
    get:
      summary: List notifications
      description: List notifications for a given time range, optionally filtered
        by type (sms_notification, email_notification, phone_notification, or push_notification)
      operationId: list-notifications-for-a-given-time-range-optionally-filtered-by-type-sms-notification-email-notific
      parameters:
      - in: query
        name: filter
        description: Return notification of this type only
      - in: query
        name: include[]
        description: Array of additional details to include
      - in: query
        name: No Name
      - in: query
        name: since
        description: The start of the date range over which you want to search
      - in: query
        name: until
        description: The end of the date range over which you want to search
      responses:
        200:
          description: OK
      tags:
      - notifications
definitions: []
x-collection-name: PagerDuty
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