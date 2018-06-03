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
  /pages:
    get:
      summary: Get Pages
      description: List of all pages from this portal
      operationId: getPages
      responses:
        200:
          description: OK
      tags:
      - pages
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