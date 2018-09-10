---
swagger: "2.0"
info:
  title: DuckDuckGo Instant Answer API
  description: 'Our Instant Answer API gives you free access to many of our instant
    answers like: topic summaries (API example), categories (API example), disambiguation
    (API example), and !bang redirects (API example). This API does not include all
    of our links, however. That is, it is not a full search results API or a way to
    get DuckDuckGo results into your applications beyond our instant answers. Because
    of the way we generate our search results, we unfortunately do not have the rights
    to fully syndicate our results, free or paid. For the same reason, we cannot allow
    framing our results without our branding. Please see our partnerships page for
    more info on guidelines and getting in touch with us.'
  version: 1.0.0
host: api.duckduckgo.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /:
    get:
      summary: Search
      description: Our Zero-click Info API gives you free access to much of our topic
        summaries, categories, disambiguation, !bang redirects, definitions and more
      operationId: zero-click-info
      parameters:
      - in: query
        name: callback
        description: Function to callback (for a JSONP formatted response)
      - in: query
        name: format
      - in: query
        name: no_html
        description: 1 to remove HTML from text, e
      - in: query
        name: no_redirect
        description: 1 to skip HTTP redirects (for !bang commands - see http://duckduckgo
      - in: query
        name: q
        description: Search terms
      - in: query
        name: skip_disambig
        description: 1 to skip disambiguation (D) Type
      responses:
        200:
          description: OK
      tags:
      - search
definitions:
  Resource:
    properties:
      Abstract:
        description: This is a default description.
        type: get
      AbstractSource:
        description: This is a default description.
        type: get
      AbstractText:
        description: This is a default description.
        type: get
      AbstractURL:
        description: This is a default description.
        type: get
      Answer:
        description: This is a default description.
        type: get
      AnswerType:
        description: This is a default description.
        type: get
      Definition:
        description: This is a default description.
        type: get
      DefinitionSource:
        description: This is a default description.
        type: get
      DefinitionURL:
        description: This is a default description.
        type: get
      Heading:
        description: This is a default description.
        type: get
  Result:
    properties:
      FirstURL:
        description: This is a default description.
        type: get
      Result:
        description: This is a default description.
        type: get
      Text:
        description: This is a default description.
        type: get
  RelatedTopic:
    properties:
      FirstURL:
        description: This is a default description.
        type: get
      Result:
        description: This is a default description.
        type: get
      Text:
        description: This is a default description.
        type: get
  Icon:
    properties:
      Height:
        description: This is a default description.
        type: get
      URL:
        description: This is a default description.
        type: get
      Width:
        description: This is a default description.
        type: get
x-collection-name: DuckDuckGo
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