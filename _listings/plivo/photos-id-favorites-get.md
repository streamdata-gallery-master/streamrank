---
swagger: "2.0"
info:
  title: Codenvy Account API
  description: This is the API for managing Codenvy account.
  version: 1.0.0
host: /account
basePath: https://codenvy.com/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /photos/:id/favorites:
    get:
      summary: Get Photos Favorites
      description: Returns all users that had favorite that photo
      operationId: returns-all-users-that-had-favorite-that-photo
      parameters:
      - in: query
        name: page
        description: Return a specific page in the photo stream
      - in: query
        name: rpp
        description: The number of results to return
      responses:
        200:
          description: OK
      tags:
      - photos
      - :id
      - favorites
definitions:
  AccountUpdate:
    properties:
      name:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
  MemberDescriptor:
    properties:
      links:
        description: This is a default description.
        type: string
      userId:
        description: This is a default description.
        type: string
      accountReference:
        description: This is a default description.
        type: string
      roles:
        description: This is a default description.
        type: string
  RequestBodyDescriptor:
    properties:
      description:
        description: This is a default description.
        type: string
  UpdateResourcesDescriptor:
    properties:
      workspaceId:
        description: This is a default description.
        type: string
      runnerRam:
        description: This is a default description.
        type: string
      builderTimeout:
        description: This is a default description.
        type: string
      runnerTimeout:
        description: This is a default description.
        type: string
      resourcesUsageLimit:
        description: This is a default description.
        type: string
  NewMembership:
    properties:
      userId:
        description: This is a default description.
        type: string
      roles:
        description: This is a default description.
        type: string
  LinkParameter:
    properties:
      required:
        description: This is a default description.
        type: string
      valid:
        description: This is a default description.
        type: string
      description:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      type:
        description: This is a default description.
        type: string
      defaultValue:
        description: This is a default description.
        type: string
  SubscriptionDescriptor:
    properties:
      accountId:
        description: This is a default description.
        type: string
      startDate:
        description: This is a default description.
        type: string
      endDate:
        description: This is a default description.
        type: string
      links:
        description: This is a default description.
        type: string
      planId:
        description: This is a default description.
        type: string
      usePaymentSystem:
        description: This is a default description.
        type: string
      serviceId:
        description: This is a default description.
        type: string
      billingCycleType:
        description: This is a default description.
        type: string
      billingCycle:
        description: This is a default description.
        type: string
      billingContractTerm:
        description: This is a default description.
        type: string
  AccountDescriptor:
    properties:
      links:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
  AccountReference:
    properties:
      links:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
  NewSubscription:
    properties:
      accountId:
        description: This is a default description.
        type: string
      planId:
        description: This is a default description.
        type: string
      usePaymentSystem:
        description: This is a default description.
        type: string
      trialDuration:
        description: This is a default description.
        type: string
      properties:
        description: This is a default description.
        type: string
  NewAccount:
    properties:
      name:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
  Link:
    properties:
      rel:
        description: This is a default description.
        type: string
      href:
        description: This is a default description.
        type: string
      produces:
        description: This is a default description.
        type: string
      consumes:
        description: This is a default description.
        type: string
      requestBody:
        description: This is a default description.
        type: string
      method:
        description: This is a default description.
        type: string
      parameters:
        description: This is a default description.
        type: string
  Account:
    properties:
      id:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
x-collection-name: Plivo
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