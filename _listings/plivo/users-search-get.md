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
  /users/search:
    get:
      summary: Get Users Search
      description: Return listing of ten (up to one hundred) users from search results
        for a specified search term
      operationId: return-listing-of-ten-up-to-one-hundred-users-from-search-results-for-a-specified-search-term
      parameters:
      - in: query
        name: term (required)
        description: A keyword to search for
      responses:
        200:
          description: OK
      tags:
      - users
      - search
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