---
swagger: "2.0"
info:
  title: Postmark Account-level
  description: Postmark makes sending and receiving email incredibly easy. The Account-level
    API allows users toconfigure all Servers, Domains, and Sender Signatures associated
    with an Account.
  version: 0.9.0
host: api.postmarkapp.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /servers:
    get:
      summary: List servers
      description: List servers
      operationId: listServers
      parameters:
      - in: query
        name: count
        description: Number of servers to return per request
      - in: query
        name: name
        description: Filter by a specific server name
      - in: query
        name: offset
        description: Number of servers to skip
      - in: header
        name: X-Postmark-Account-Token
        description: The token associated with the Account on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - servers
definitions:
  CreateServerPayload:
    properties:
      BounceHookUrl:
        description: This is a default description.
        type: put
      ClickHookUrl:
        description: This is a default description.
        type: put
      Color:
        description: This is a default description.
        type: put
      DeliveryHookUrl:
        description: This is a default description.
        type: put
      InboundDomain:
        description: This is a default description.
        type: put
      InboundHookUrl:
        description: This is a default description.
        type: put
      InboundSpamThreshold:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
      OpenHookUrl:
        description: This is a default description.
        type: put
      PostFirstOpenOnly:
        description: This is a default description.
        type: put
  DKIMRotationResponse:
    properties:
      DKIMHost:
        description: This is a default description.
        type: put
      DKIMPendingHost:
        description: This is a default description.
        type: put
      DKIMPendingTextValue:
        description: This is a default description.
        type: put
      DKIMRevokedHost:
        description: This is a default description.
        type: put
      DKIMRevokedTextValue:
        description: This is a default description.
        type: put
      DKIMTestValue:
        description: This is a default description.
        type: put
      DKIMUpdateStatus:
        description: This is a default description.
        type: put
      DKIMVerified:
        description: This is a default description.
        type: put
      ID:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
  DomainCreationModel:
    properties:
      Name:
        description: This is a default description.
        type: put
      ReturnPathDomain:
        description: This is a default description.
        type: put
  DomainEditingModel:
    properties:
      ReturnPathDomain:
        description: This is a default description.
        type: put
  DomainExtendedInformation:
    properties:
      DKIMHost:
        description: This is a default description.
        type: put
      DKIMPendingHost:
        description: This is a default description.
        type: put
      DKIMPendingTextValue:
        description: This is a default description.
        type: put
      DKIMRevokedHost:
        description: This is a default description.
        type: put
      DKIMRevokedTextValue:
        description: This is a default description.
        type: put
      DKIMTestValue:
        description: This is a default description.
        type: put
      DKIMUpdateStatus:
        description: This is a default description.
        type: put
      DKIMVerified:
        description: This is a default description.
        type: put
      ID:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
  DomainInformation:
    properties:
      DKIMVerified:
        description: This is a default description.
        type: put
      ID:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
      ReturnPathDomainVerified:
        description: This is a default description.
        type: put
      SPFVerified:
        description: This is a default description.
        type: put
      WeakDKIM:
        description: This is a default description.
        type: put
  DomainListingResults:
    properties:
      Domains:
        description: This is a default description.
        type: put
      TotalCount:
        description: This is a default description.
        type: put
  DomainSPFResult:
    properties:
      SPFHost:
        description: This is a default description.
        type: put
      SPFTextValue:
        description: This is a default description.
        type: put
      SPFVerified:
        description: This is a default description.
        type: put
  EditServerPayload:
    properties:
      BounceHookUrl:
        description: This is a default description.
        type: put
      ClickHookUrl:
        description: This is a default description.
        type: put
      Color:
        description: This is a default description.
        type: put
      DeliveryHookUrl:
        description: This is a default description.
        type: put
      InboundDomain:
        description: This is a default description.
        type: put
      InboundHookUrl:
        description: This is a default description.
        type: put
      InboundSpamThreshold:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
      OpenHookUrl:
        description: This is a default description.
        type: put
      PostFirstOpenOnly:
        description: This is a default description.
        type: put
  ExtendedServerInfo:
    properties:
      ApiTokens:
        description: This is a default description.
        type: put
      BounceHookUrl:
        description: This is a default description.
        type: put
      ClickHookUrl:
        description: This is a default description.
        type: put
      Color:
        description: This is a default description.
        type: put
      DeliveryHookUrl:
        description: This is a default description.
        type: put
      ID:
        description: This is a default description.
        type: put
      InboundAddress:
        description: This is a default description.
        type: put
      InboundDomain:
        description: This is a default description.
        type: put
      InboundHash:
        description: This is a default description.
        type: put
      InboundHookUrl:
        description: This is a default description.
        type: put
  SenderListingResults:
    properties:
      SenderSignatures:
        description: This is a default description.
        type: put
      TotalCount:
        description: This is a default description.
        type: put
  SenderSignatureCreationModel:
    properties:
      FromEmail:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
      ReplyToEmail:
        description: This is a default description.
        type: put
      ReturnPathDomain:
        description: This is a default description.
        type: put
  SenderSignatureEditingModel:
    properties:
      Name:
        description: This is a default description.
        type: put
      ReplyToEmail:
        description: This is a default description.
        type: put
      ReturnPathDomain:
        description: This is a default description.
        type: put
  SenderSignatureExtendedInformation:
    properties:
      Confirmed:
        description: This is a default description.
        type: put
      DKIMHost:
        description: This is a default description.
        type: put
      DKIMPendingHost:
        description: This is a default description.
        type: put
      DKIMPendingTextValue:
        description: This is a default description.
        type: put
      DKIMRevokedHost:
        description: This is a default description.
        type: put
      DKIMRevokedTextValue:
        description: This is a default description.
        type: put
      DKIMTestValue:
        description: This is a default description.
        type: put
      DKIMUpdateStatus:
        description: This is a default description.
        type: put
      DKIMVerified:
        description: This is a default description.
        type: put
      Domain:
        description: This is a default description.
        type: put
  SenderSignatureInformation:
    properties:
      Confirmed:
        description: This is a default description.
        type: put
      Domain:
        description: This is a default description.
        type: put
      EmailAddress:
        description: This is a default description.
        type: put
      ID:
        description: This is a default description.
        type: put
      Name:
        description: This is a default description.
        type: put
      ReplyToEmailAddress:
        description: This is a default description.
        type: put
  ServerListingResponse:
    properties:
      Servers:
        description: This is a default description.
        type: put
      TotalCount:
        description: This is a default description.
        type: put
  StandardPostmarkResponse:
    properties:
      ErrorCode:
        description: This is a default description.
        type: put
      Message:
        description: This is a default description.
        type: put
x-collection-name: Postmark
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