---
swagger: "2.0"
info:
  title: Building Block API
  description: When I started API Evangelist, I began tracking on the elements that
    other leading API providers use to operate their API programs, and eventually
    I started calling these building blocks. I keep a running list of building blocks,
    broken down into groups. I think use these to keep track of which building blocks
    companies are using. This is the API I use to manage these elements of everyday
    API operation.
  contact:
    name: Kin Lane
    url: http://kinlane.com
    email: info@kinlane.com
  version: v1
host: buildingblock.api.kinlane.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /buildingblocks/{building_block_id}/logs/:
    get:
      summary: Get Logs for Building Block
      description: get building block logs
      operationId: getBuildingBlockLogs
      parameters:
      - in: query
        name: appid
        description: your appid for accessing the building block
      - in: query
        name: appkey
        description: your appkey for accessing the building block
      - in: path
        name: building_block_id
        description: id for building block
      responses:
        200:
          description: OK
      tags:
      - logsbuilding
      - block
definitions:
  buildingblock:
    properties:
      building_block_id:
        description: This is a default description.
        type: delete
      building_block_category_id:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
      about:
        description: This is a default description.
        type: delete
      sort_order:
        description: This is a default description.
        type: delete
  log:
    properties:
      api_id:
        description: This is a default description.
        type: delete
      type:
        description: This is a default description.
        type: delete
      note:
        description: This is a default description.
        type: delete
      details:
        description: This is a default description.
        type: delete
      log_date:
        description: This is a default description.
        type: delete
  tool:
    properties:
      tool_id:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
      details:
        description: This is a default description.
        type: delete
      post_date:
        description: This is a default description.
        type: delete
      url:
        description: This is a default description.
        type: delete
  url:
    properties:
      note_id:
        description: This is a default description.
        type: delete
      type:
        description: This is a default description.
        type: delete
      url:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
  image:
    properties:
      api_id:
        description: This is a default description.
        type: delete
      image_id:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
      path:
        description: This is a default description.
        type: delete
      type:
        description: This is a default description.
        type: delete
  organization:
    properties:
      organization_id:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
      details:
        description: This is a default description.
        type: delete
      summary:
        description: This is a default description.
        type: delete
      post_date:
        description: This is a default description.
        type: delete
      url:
        description: This is a default description.
        type: delete
      phone:
        description: This is a default description.
        type: delete
      email:
        description: This is a default description.
        type: delete
      address:
        description: This is a default description.
        type: delete
      city:
        description: This is a default description.
        type: delete
  tag:
    properties:
      tag_id:
        description: This is a default description.
        type: delete
      tag:
        description: This is a default description.
        type: delete
      api_count:
        description: This is a default description.
        type: delete
  category:
    properties:
      category_id:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
      sort_order:
        description: This is a default description.
        type: delete
      type:
        description: This is a default description.
        type: delete
x-collection-name: TidyHQ
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