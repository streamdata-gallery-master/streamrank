swagger: "2.0"
x-collection-name: Pinboard
x-complete: 1
info:
  title: Pinboard
  description: store-manage-and-share-bookmarks-on-pinboard
  version: 1.0.0
host: api.pinboard.in
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /posts/suggest:
    get:
      summary: Get Popular Tags
      description: Returns a list of popular tags and recommended tags for a given
        URL. Popular tags are tags used site-wide for the url; recommended tags are
        drawn from the user's own tags.
      operationId: posts.suggest.get
      x-api-path-slug: postssuggest-get
      parameters:
      - in: query
        name: format
        description: the format to return
        type: string
        format: string
      - in: query
        name: url
        description: url to suggest from
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Posts
      - Suggest