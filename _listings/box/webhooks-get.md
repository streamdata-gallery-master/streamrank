---
swagger: "2.0"
info:
  title: Box
  description: The Box Content API gives you access to secure content management and
    content experience features for use in your own app. It strives to be RESTful
    and is organized around the main resources you&rsquo;re familiar with from the
    Box web interface.
  version: 1.0.0
host: api.box.com
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /webhooks:
    get:
      summary: Get Webhooks
      description: Returns all defined webhooks for the requesting application and
        user, up to the limit
      operationId: getWebhooks
      parameters:
      - in: query
        name: limit
        description: The maximum number of webhooks to return per page
      - in: query
        name: marker
        description: A marker string returned by Box if the result contains less than
          the full number of webhooks that are defined
      responses:
        200:
          description: OK
      tags:
      - documents
      - webhooks
definitions:
  Error:
    properties:
      type:
        description: This is a default description.
        type: delete
      status:
        description: This is a default description.
        type: delete
      context_info:
        description: This is a default description.
        type: delete
      code:
        description: This is a default description.
        type: delete
      help-url:
        description: This is a default description.
        type: delete
      message:
        description: This is a default description.
        type: delete
      request_id:
        description: This is a default description.
        type: delete
  Reference:
    properties:
      id:
        description: This is a default description.
        type: delete
      type:
        description: This is a default description.
        type: delete
  Pagination:
    properties:
      total_count:
        description: This is a default description.
        type: delete
      limit:
        description: This is a default description.
        type: delete
      offset:
        description: This is a default description.
        type: delete
      order:
        description: This is a default description.
        type: delete
  MarkerPagination:
    properties:
      limit:
        description: This is a default description.
        type: delete
      next_marker:
        description: This is a default description.
        type: delete
      prev_marker:
        description: This is a default description.
        type: delete
  ChunkPagination:
    properties:
      chunk_size:
        description: This is a default description.
        type: delete
      next_stream_position:
        description: This is a default description.
        type: delete
  UserReference:
    properties:
      type:
        description: This is a default description.
        type: delete
      id:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
      login:
        description: This is a default description.
        type: delete
  FolderUploadEmail:
    properties:
      access:
        description: This is a default description.
        type: delete
      email:
        description: This is a default description.
        type: delete
  FolderPermissions:
    properties:
      can_download:
        description: This is a default description.
        type: delete
      can_upload:
        description: This is a default description.
        type: delete
      can_rename:
        description: This is a default description.
        type: delete
      cand_delete:
        description: This is a default description.
        type: delete
      can_share:
        description: This is a default description.
        type: delete
      can_invite_collaborator:
        description: This is a default description.
        type: delete
      can_set_share_access:
        description: This is a default description.
        type: delete
  FilePermissions:
    properties:
      can_download:
        description: This is a default description.
        type: delete
      can_preview:
        description: This is a default description.
        type: delete
      can_upload:
        description: This is a default description.
        type: delete
      can_rename:
        description: This is a default description.
        type: delete
      cand_delete:
        description: This is a default description.
        type: delete
      can_share:
        description: This is a default description.
        type: delete
      can_invite_collaborator:
        description: This is a default description.
        type: delete
      can_set_share_access:
        description: This is a default description.
        type: delete
  CopyFile:
    properties:
      parent:
        description: This is a default description.
        type: delete
      version:
        description: This is a default description.
        type: delete
      name:
        description: This is a default description.
        type: delete
  SharedLinkPermissions:
    properties:
      can_download:
        description: This is a default description.
        type: delete
      can_preview:
        description: This is a default description.
        type: delete
  SharedLink:
    properties:
      url:
        description: This is a default description.
        type: delete
      download_url:
        description: This is a default description.
        type: delete
      password:
        description: This is a default description.
        type: delete
      vanity_url:
        description: This is a default description.
        type: delete
      is_password_enabled:
        description: This is a default description.
        type: delete
      unshared_at:
        description: This is a default description.
        type: delete
      download_count:
        description: This is a default description.
        type: delete
      preview_count:
        description: This is a default description.
        type: delete
      access:
        description: This is a default description.
        type: delete
      effective_access:
        description: This is a default description.
        type: delete
  TemplateFields:
    properties:
      type:
        description: This is a default description.
        type: delete
      key:
        description: This is a default description.
        type: delete
      displayName:
        description: This is a default description.
        type: delete
      description:
        description: This is a default description.
        type: delete
      hidden:
        description: This is a default description.
        type: delete
      options:
        description: This is a default description.
        type: delete
  MetadataTemplate:
    properties:
      templateKey:
        description: This is a default description.
        type: delete
      scope:
        description: This is a default description.
        type: delete
      displayName:
        description: This is a default description.
        type: delete
      hidden:
        description: This is a default description.
        type: delete
      fields:
        description: This is a default description.
        type: delete
  WatermarkReference:
    properties:
      created_at:
        description: This is a default description.
        type: delete
      modified_at:
        description: This is a default description.
        type: delete
      imprint:
        description: This is a default description.
        type: delete
  Watermark:
    properties: []
  Event:
    properties:
      type:
        description: This is a default description.
        type: delete
      event_id:
        description: This is a default description.
        type: delete
      event_type:
        description: This is a default description.
        type: delete
      session_id:
        description: This is a default description.
        type: delete
      source:
        description: This is a default description.
        type: delete
      additional_details:
        description: This is a default description.
        type: delete
  RealtimeServer:
    properties:
      type:
        description: This is a default description.
        type: delete
      url:
        description: This is a default description.
        type: delete
      ttl:
        description: This is a default description.
        type: delete
      max_retries:
        description: This is a default description.
        type: delete
      retry_timeout:
        description: This is a default description.
        type: delete
  RetentionPolicyList:
    properties:
      entries:
        description: This is a default description.
        type: delete
  RetentionPolicyAssignmentList:
    properties:
      entries:
        description: This is a default description.
        type: delete
  AssignmentCounts:
    properties:
      user:
        description: This is a default description.
        type: delete
      folder:
        description: This is a default description.
        type: delete
      file:
        description: This is a default description.
        type: delete
      file_version:
        description: This is a default description.
        type: delete
  CreateTaskAssignment:
    properties: []
  InviteUser:
    properties: []
  CreateLegalHoldPolicyAssignment:
    properties:
      policy_id:
        description: This is a default description.
        type: delete
  CreateRetentionPolicyAssignment:
    properties:
      policy_id:
        description: This is a default description.
        type: delete
x-collection-name: Box
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---