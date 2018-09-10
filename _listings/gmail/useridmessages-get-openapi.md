---
swagger: "2.0"
info:
  title: Gmail
  description: Access Gmail mailboxes including sending user email.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /gmail/v1/users
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{userId}/messages:
    get:
      summary: Get Message
      description: Lists the messages in the user's mailbox
      operationId: gmail.users.messages.list
      x-api-path-slug: useridmessages-get
      parameters:
      - in: query
        name: includeSpamTrash
        description: Include messages from SPAM and TRASH in the results
      - in: query
        name: labelIds
        description: Only return messages with labels that match all of the specified
          label IDs
      - in: query
        name: maxResults
        description: Maximum number of messages to return
      - in: query
        name: pageToken
        description: Page token to retrieve a specific page of results in the list
      - in: query
        name: q
        description: Only return messages matching the specified query
      - in: path
        name: userId
        description: The user's email address
      responses:
        200:
          description: OK
      tags:
      - email
definitions:
  AutoForwarding:
    properties:
      disposition:
        description: This is a default description.
        type: post
      emailAddress:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
  BatchDeleteMessagesRequest:
    properties:
      ids:
        description: This is a default description.
        type: post
  BatchModifyMessagesRequest:
    properties:
      addLabelIds:
        description: This is a default description.
        type: post
      ids:
        description: This is a default description.
        type: post
      removeLabelIds:
        description: This is a default description.
        type: post
  Draft:
    properties:
      id:
        description: This is a default description.
        type: post
  Filter:
    properties:
      id:
        description: This is a default description.
        type: post
  FilterAction:
    properties:
      addLabelIds:
        description: This is a default description.
        type: post
      forward:
        description: This is a default description.
        type: post
      removeLabelIds:
        description: This is a default description.
        type: post
  FilterCriteria:
    properties:
      excludeChats:
        description: This is a default description.
        type: post
      from:
        description: This is a default description.
        type: post
      hasAttachment:
        description: This is a default description.
        type: post
      negatedQuery:
        description: This is a default description.
        type: post
      query:
        description: This is a default description.
        type: post
      size:
        description: This is a default description.
        type: post
      sizeComparison:
        description: This is a default description.
        type: post
      subject:
        description: This is a default description.
        type: post
      to:
        description: This is a default description.
        type: post
  ForwardingAddress:
    properties:
      forwardingEmail:
        description: This is a default description.
        type: post
      verificationStatus:
        description: This is a default description.
        type: post
  History:
    properties:
      id:
        description: This is a default description.
        type: post
      labelsAdded:
        description: This is a default description.
        type: post
      labelsRemoved:
        description: This is a default description.
        type: post
      messages:
        description: This is a default description.
        type: post
      messagesAdded:
        description: This is a default description.
        type: post
      messagesDeleted:
        description: This is a default description.
        type: post
  HistoryLabelAdded:
    properties:
      labelIds:
        description: This is a default description.
        type: post
  HistoryLabelRemoved:
    properties:
      labelIds:
        description: This is a default description.
        type: post
  HistoryMessageAdded:
    properties: []
  HistoryMessageDeleted:
    properties: []
  ImapSettings:
    properties:
      autoExpunge:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
      expungeBehavior:
        description: This is a default description.
        type: post
      maxFolderSize:
        description: This is a default description.
        type: post
  Label:
    properties:
      id:
        description: This is a default description.
        type: post
      labelListVisibility:
        description: This is a default description.
        type: post
      messageListVisibility:
        description: This is a default description.
        type: post
      messagesTotal:
        description: This is a default description.
        type: post
      messagesUnread:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      threadsTotal:
        description: This is a default description.
        type: post
      threadsUnread:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  ListDraftsResponse:
    properties:
      drafts:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      resultSizeEstimate:
        description: This is a default description.
        type: post
  ListFiltersResponse:
    properties:
      filter:
        description: This is a default description.
        type: post
  ListForwardingAddressesResponse:
    properties:
      forwardingAddresses:
        description: This is a default description.
        type: post
  ListHistoryResponse:
    properties:
      history:
        description: This is a default description.
        type: post
      historyId:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListLabelsResponse:
    properties:
      labels:
        description: This is a default description.
        type: post
  ListMessagesResponse:
    properties:
      messages:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      resultSizeEstimate:
        description: This is a default description.
        type: post
  ListSendAsResponse:
    properties:
      sendAs:
        description: This is a default description.
        type: post
  ListSmimeInfoResponse:
    properties:
      smimeInfo:
        description: This is a default description.
        type: post
  ListThreadsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      resultSizeEstimate:
        description: This is a default description.
        type: post
      threads:
        description: This is a default description.
        type: post
  Message:
    properties:
      historyId:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      internalDate:
        description: This is a default description.
        type: post
      labelIds:
        description: This is a default description.
        type: post
      raw:
        description: This is a default description.
        type: post
      sizeEstimate:
        description: This is a default description.
        type: post
      snippet:
        description: This is a default description.
        type: post
      threadId:
        description: This is a default description.
        type: post
  MessagePart:
    properties:
      filename:
        description: This is a default description.
        type: post
      headers:
        description: This is a default description.
        type: post
      mimeType:
        description: This is a default description.
        type: post
      partId:
        description: This is a default description.
        type: post
      parts:
        description: This is a default description.
        type: post
  MessagePartBody:
    properties:
      attachmentId:
        description: This is a default description.
        type: post
      data:
        description: This is a default description.
        type: post
      size:
        description: This is a default description.
        type: post
  MessagePartHeader:
    properties:
      name:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  ModifyMessageRequest:
    properties:
      addLabelIds:
        description: This is a default description.
        type: post
      removeLabelIds:
        description: This is a default description.
        type: post
  ModifyThreadRequest:
    properties:
      addLabelIds:
        description: This is a default description.
        type: post
      removeLabelIds:
        description: This is a default description.
        type: post
  PopSettings:
    properties:
      accessWindow:
        description: This is a default description.
        type: post
      disposition:
        description: This is a default description.
        type: post
  Profile:
    properties:
      emailAddress:
        description: This is a default description.
        type: post
      historyId:
        description: This is a default description.
        type: post
      messagesTotal:
        description: This is a default description.
        type: post
      threadsTotal:
        description: This is a default description.
        type: post
  SendAs:
    properties:
      displayName:
        description: This is a default description.
        type: post
      isDefault:
        description: This is a default description.
        type: post
      isPrimary:
        description: This is a default description.
        type: post
      replyToAddress:
        description: This is a default description.
        type: post
      sendAsEmail:
        description: This is a default description.
        type: post
      signature:
        description: This is a default description.
        type: post
      treatAsAlias:
        description: This is a default description.
        type: post
      verificationStatus:
        description: This is a default description.
        type: post
  SmimeInfo:
    properties:
      encryptedKeyPassword:
        description: This is a default description.
        type: post
      expiration:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      isDefault:
        description: This is a default description.
        type: post
      issuerCn:
        description: This is a default description.
        type: post
      pem:
        description: This is a default description.
        type: post
      pkcs12:
        description: This is a default description.
        type: post
  SmtpMsa:
    properties:
      host:
        description: This is a default description.
        type: post
      password:
        description: This is a default description.
        type: post
      port:
        description: This is a default description.
        type: post
      securityMode:
        description: This is a default description.
        type: post
      username:
        description: This is a default description.
        type: post
  Thread:
    properties:
      historyId:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      messages:
        description: This is a default description.
        type: post
      snippet:
        description: This is a default description.
        type: post
  VacationSettings:
    properties:
      enableAutoReply:
        description: This is a default description.
        type: post
      endTime:
        description: This is a default description.
        type: post
      responseBodyHtml:
        description: This is a default description.
        type: post
      responseBodyPlainText:
        description: This is a default description.
        type: post
      responseSubject:
        description: This is a default description.
        type: post
      restrictToContacts:
        description: This is a default description.
        type: post
      restrictToDomain:
        description: This is a default description.
        type: post
      startTime:
        description: This is a default description.
        type: post
  WatchRequest:
    properties:
      labelFilterAction:
        description: This is a default description.
        type: post
      labelIds:
        description: This is a default description.
        type: post
      topicName:
        description: This is a default description.
        type: post
  WatchResponse:
    properties:
      expiration:
        description: This is a default description.
        type: post
      historyId:
        description: This is a default description.
        type: post
x-collection-name: Gmail
x-streamrank:
  polling_total_time_average: "0.07"
  polling_size_download_average: "288.24"
  streaming_total_time_average: "0.04"
  streaming_size_download_average: "145.68"
  change_yes: "2"
  change_no: "2331"
  time_percentage: "43"
  size_percentage: "49"
  change_percentage: "0"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---