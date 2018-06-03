---
swagger: "2.0"
info:
  title: Swagger Hub Registry
  description: The registry API for SwaggerHub
  contact:
    name: SwaggerHub
    url: http://swaggerhub.com
    email: info@swaggerhub.com
  version: 1.0.45
host: api.swaggerhub.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apis/{owner}/{api}/{version}/.comment:
    get:
      summary: Returns the list of comments for the specified API
      description: Returns the list of comments for the specified api
      operationId: getApiComments
      parameters:
      - in: path
        name: api
        description: API identifier
      - in: path
        name: owner
        description: API owner identifier
      - in: path
        name: version
        description: version identifier
      responses:
        200:
          description: OK
      tags:
      - apis
      - owner
      - version
      - ""
      - comment
definitions:
  AccessToken:
    properties:
      token:
        description: This is a default description.
        type: get
  ApiMetadata:
    properties:
      categories:
        description: This is a default description.
        type: get
      defaultVersion:
        description: This is a default description.
        type: get
      links:
        description: This is a default description.
        type: get
      tags:
        description: This is a default description.
        type: get
  ApiMetadataLink:
    properties:
      type:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  ApisJson:
    properties:
      apis:
        description: This is a default description.
        type: get
      created:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      modified:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      offset:
        description: This is a default description.
        type: get
      specificationVersion:
        description: This is a default description.
        type: get
      totalCount:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  ApisJsonApi:
    properties:
      description:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      properties:
        description: This is a default description.
        type: get
      tags:
        description: This is a default description.
        type: get
  ApisJsonProperty:
    properties:
      type:
        description: This is a default description.
        type: get
  CodegenLanguage:
    properties:
      customValues:
        description: This is a default description.
        type: get
      visible:
        description: This is a default description.
        type: get
  CodegenSettings:
    properties:
      client:
        description: This is a default description.
        type: get
      server:
        description: This is a default description.
        type: get
  Collaboration:
    properties:
      members:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
      owners:
        description: This is a default description.
        type: get
      pendingMembers:
        description: This is a default description.
        type: get
      teams:
        description: This is a default description.
        type: get
  CollaborationHint:
    properties:
      type:
        description: This is a default description.
        type: get
  CollaborationMember:
    properties:
      name:
        description: This is a default description.
        type: get
      startTime:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      uuid:
        description: This is a default description.
        type: get
  CollaborationMembershipList:
    properties:
      items:
        description: This is a default description.
        type: get
  CollaborationRoles:
    properties:
      api:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
      roles:
        description: This is a default description.
        type: get
  Comment:
    properties:
      body:
        description: This is a default description.
        type: get
      created:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      modified:
        description: This is a default description.
        type: get
  CommentPatch:
    properties:
      body:
        description: This is a default description.
        type: get
  CommentsBatch:
    properties:
      addComment:
        description: This is a default description.
        type: get
      addReply:
        description: This is a default description.
        type: get
      deleteComment:
        description: This is a default description.
        type: get
      deleteReply:
        description: This is a default description.
        type: get
      updateComment:
        description: This is a default description.
        type: get
      updateReply:
        description: This is a default description.
        type: get
      updateStatus:
        description: This is a default description.
        type: get
  Comparison:
    properties: []
  ComparisonDetail:
    properties:
      content:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
  ComparisonPart:
    properties:
      type:
        description: This is a default description.
        type: get
  EntryId:
    properties:
      name:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
      version:
        description: This is a default description.
        type: get
  GitHubExportSettings:
    properties:
      branch:
        description: This is a default description.
        type: get
      notificationEmail:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      repository:
        description: This is a default description.
        type: get
      token:
        description: This is a default description.
        type: get
      yamlPath:
        description: This is a default description.
        type: get
  LifecycleSettings:
    properties:
      published:
        description: This is a default description.
        type: get
  MissingSpecMembers:
    properties:
      names:
        description: This is a default description.
        type: get
  NewComment:
    properties:
      body:
        description: This is a default description.
        type: get
      position:
        description: This is a default description.
        type: get
      replies:
        description: This is a default description.
        type: get
  NewReply:
    properties:
      body:
        description: This is a default description.
        type: get
  NotCollaboratorProjectMembers:
    properties:
      missingApisMembers:
        description: This is a default description.
        type: get
      missingApisTeams:
        description: This is a default description.
        type: get
      missingDomainsMembers:
        description: This is a default description.
        type: get
      missingDomainsTeams:
        description: This is a default description.
        type: get
  Page:
    properties:
      items:
        description: This is a default description.
        type: get
      offset:
        description: This is a default description.
        type: get
      total:
        description: This is a default description.
        type: get
  PluginConfiguration:
    properties:
      configuration:
        description: This is a default description.
        type: get
      definitionId:
        description: This is a default description.
        type: get
      draft:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      lifecycles:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      objectId:
        description: This is a default description.
        type: get
      ownerName:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
  PluginDefinition:
    properties:
      configurationSchema:
        description: This is a default description.
        type: get
      createdBy:
        description: This is a default description.
        type: get
      createdOn:
        description: This is a default description.
        type: get
      enabled:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      implementingClass:
        description: This is a default description.
        type: get
      limit:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      version:
        description: This is a default description.
        type: get
  Position:
    properties:
      column:
        description: This is a default description.
        type: get
      line:
        description: This is a default description.
        type: get
  Private:
    properties:
      private:
        description: This is a default description.
        type: get
  ProjectEntry:
    properties:
      apis:
        description: This is a default description.
        type: get
      domains:
        description: This is a default description.
        type: get
      groupId:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      projectId:
        description: This is a default description.
        type: get
  ProjectMember:
    properties:
      name:
        description: This is a default description.
        type: get
      roles:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  ProjectMemberList:
    properties:
      members:
        description: This is a default description.
        type: get
  ProjectsJson:
    properties:
      offset:
        description: This is a default description.
        type: get
      projects:
        description: This is a default description.
        type: get
      totalCount:
        description: This is a default description.
        type: get
  SimpleSpec:
    properties:
      name:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
  SpecId:
    properties:
      name:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
      version:
        description: This is a default description.
        type: get
  SystemPluginConfiguration:
    properties:
      configuration:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      implementingClass:
        description: This is a default description.
        type: get
      lifecycles:
        description: This is a default description.
        type: get
      version:
        description: This is a default description.
        type: get
  Template:
    properties:
      id:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  TemplateCatalog:
    properties:
      templates:
        description: This is a default description.
        type: get
  User:
    properties:
      active:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
  UserCredentials:
    properties:
      password:
        description: This is a default description.
        type: get
      username:
        description: This is a default description.
        type: get
  VersionMetadata:
    properties: []
x-collection-name: SwaggerHub
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