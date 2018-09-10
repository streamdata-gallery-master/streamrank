swagger: "2.0"
x-collection-name: The New York Times
x-complete: 1
info:
  title: New York Times
  description: you-already-know-that-nytimes-com-is-an-unparalleled-source-of-news-and-information--but-now-its-a-premier-source-of-data-too--why-just-read-the-news-when-you-can-hack-it
  termsOfService: https://developer.nytimes.com/tou
  version: 2.0.0
host: api.nytimes.com
basePath: /svc
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/v2/articlesearch.json:
    get:
      summary: Article Search
      description: Article SearchWith the Article Search API, you can search New York
        Times articles from Sept. 18, 1851 to today, retrieving headlines, abstracts,
        lead paragraphs, links to associated multimedia and other article.
      operationId: article-search-requests-use-the-following-uri-structure
      x-api-path-slug: searchv2articlesearch-json-get
      parameters:
      - in: query
        name: api-key
        description: The API key
        type: string
        format: string
      - in: query
        name: begin_date
        description: 'Format: YYYYMMDD Restricts responses to results with publication
          dates of the date specified or later'
      - in: query
        name: end_date
        description: 'Format: YYYYMMDD Restricts responses to results with publication
          dates of the date specified or earlier'
      - in: query
        name: facet_field
        description: Comma-delimited list of facetsSpecifies the sets of facet values
          to include in the facets array at the end of response, which collects the
          facet values from all the search results
      - in: query
        name: facet_filter
        description: When set to true, facet counts will respect any applied filters
          (fq, date range, etc
      - in: query
        name: fl
        description: Comma-delimited list of fields (no limit)  Limits the fields
          returned in your search results
      - in: query
        name: fq
        description: Filtered search query using standard Lucene syntax
      - in: query
        name: hl
        description: Enables highlighting in search results
      - in: query
        name: page
        description: The value of page corresponds to a set of 10 results (it does
          not indicate the starting number of the result set)
      - in: query
        name: q
        description: Search query term
      - in: query
        name: sort
        description: By default, search results are sorted by their relevance to the
          query term (q)
      responses:
        200:
          description: OK
      tags:
      - News