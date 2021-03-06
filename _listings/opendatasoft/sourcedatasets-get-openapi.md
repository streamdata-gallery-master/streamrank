---
swagger: "2.0"
info:
  title: OpenDataSoft
  description: OpenDataSoft is a cloud-based turnkey platform for data publishing
    and API management. Its interface is intuitively designed to empower anyone, regardless
    of technical skills, to upload easy-to-understand Open Data, or to even share
    data within an admi...
  version: 2.1.0
host: public.opendatasoft.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{source}/datasets:
    get:
      summary: Get Source Datasets
      description: List of available datasets, each with their endpoints, paginated
      operationId: getDatasets
      x-api-path-slug: sourcedatasets-get
      responses:
        200:
          description: OK
      tags:
      - source
      - datasets
definitions:
  attachment:
    properties:
      href:
        description: This is a default description.
        type: get
      metas:
        description: This is a default description.
        type: get
  dataset:
    properties:
      attachments:
        description: This is a default description.
        type: get
      data_visible:
        description: This is a default description.
        type: get
      dataset_id:
        description: This is a default description.
        type: get
      features:
        description: This is a default description.
        type: get
      fields:
        description: This is a default description.
        type: get
      has_records:
        description: This is a default description.
        type: get
      metas:
        description: This is a default description.
        type: get
  link:
    properties:
      href:
        description: This is a default description.
        type: get
      rel:
        description: This is a default description.
        type: get
  metadata_template:
    properties:
      name:
        description: This is a default description.
        type: get
      schema:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  page:
    properties:
      description:
        description: This is a default description.
        type: get
      slug:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  record:
    properties:
      fields:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  reuse:
    properties:
      created_at:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      thumbnail:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      user:
        description: This is a default description.
        type: get
  snapshot:
    properties:
      created_at:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      href:
        description: This is a default description.
        type: get
      snapshot_id:
        description: This is a default description.
        type: get
x-collection-name: OpenDataSoft
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