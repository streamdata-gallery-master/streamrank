---
swagger: "2.0"
info:
  title: New York Times
  description: You already know that NYTimes.com is an unparalleled source of news
    and information. But now it's a premier source of data, too &mdash; why just read
    the news when you can hack it?
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
        Times articles from Sept
      operationId: article-search-requests-use-the-following-uri-structure
      parameters:
      - in: query
        name: api-key
        description: The API key
        type: string
        format: string
      - in: query
        name: begin_date
        description: "\"Format: YYYYMMDD \n\nRestricts responses to results with publication
          dates of the date specified or later"
      - in: query
        name: end_date
        description: "\"Format: YYYYMMDD \n\nRestricts responses to results with publication
          dates of the date specified or earlier"
      - in: query
        name: facet_field
        description: |-
          Comma-delimited list of facets

          Specifies the sets of facet values to include in the facets array at the end of response, which collects the facet values from all the search results
      - in: query
        name: facet_filter
        description: When set to true, facet counts will respect any applied filters
          (fq, date range, etc
      - in: query
        name: fl
        description: |-
          "Comma-delimited list of fields (no limit)

            Limits the fields returned in your search results
      - in: query
        name: fq
        description: '"Filtered search query using standard Lucene syntax'
      - in: query
        name: hl
        description: Enables highlighting in search results
      - in: query
        name: page
        description: '"The value of page corresponds to a set of 10 results (it does
          not indicate the starting number of the result set)'
      - in: query
        name: q
        description: Search query term
      - in: query
        name: sort
        description: '"By default, search results are sorted by their relevance to
          the query term (q)'
      responses:
        200:
          description: OK
      tags:
      - news
definitions:
  Article:
    properties:
      section:
        description: This is a default description.
        type: get
      subsection:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      abstract:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      thumbnail_standard:
        description: This is a default description.
        type: get
      short_url:
        description: This is a default description.
        type: get
      byline:
        description: This is a default description.
        type: get
      item_type:
        description: This is a default description.
        type: get
      updated_date:
        description: This is a default description.
        type: get
  Doc:
    properties:
      web_url:
        description: This is a default description.
        type: get
      snippet:
        description: This is a default description.
        type: get
      lead_paragraph:
        description: This is a default description.
        type: get
      abstract:
        description: This is a default description.
        type: get
      print_page:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      source:
        description: This is a default description.
        type: get
      headline:
        description: This is a default description.
        type: get
      keywords:
        description: This is a default description.
        type: get
      pub_date:
        description: This is a default description.
        type: get
  Event:
    properties:
      event_id:
        description: This is a default description.
        type: get
      event_schedule_id:
        description: This is a default description.
        type: get
      last_modified:
        description: This is a default description.
        type: get
      event_name:
        description: This is a default description.
        type: get
      event_detail_url:
        description: This is a default description.
        type: get
      web_description:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      film_rating:
        description: This is a default description.
        type: get
      critic_name:
        description: This is a default description.
        type: get
  ArticleWithCountType:
    properties:
      url:
        description: This is a default description.
        type: get
      count_type:
        description: This is a default description.
        type: get
      column:
        description: This is a default description.
        type: get
      section:
        description: This is a default description.
        type: get
      byline:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      abstract:
        description: This is a default description.
        type: get
      published_date:
        description: This is a default description.
        type: get
      source:
        description: This is a default description.
        type: get
      media:
        description: This is a default description.
        type: get
  Movie:
    properties:
      display_title:
        description: This is a default description.
        type: get
      mpaa_rating:
        description: This is a default description.
        type: get
      critics_pick:
        description: This is a default description.
        type: get
      byline:
        description: This is a default description.
        type: get
      headline:
        description: This is a default description.
        type: get
      summary_short:
        description: This is a default description.
        type: get
      publication_date:
        description: This is a default description.
        type: get
      opening_date:
        description: This is a default description.
        type: get
      date_updated:
        description: This is a default description.
        type: get
      link:
        description: This is a default description.
        type: get
  Critic:
    properties:
      display_name:
        description: This is a default description.
        type: get
      sort_name:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      bio:
        description: This is a default description.
        type: get
      seo_name:
        description: This is a default description.
        type: get
      multimedia:
        description: This is a default description.
        type: get
  Concept:
    properties:
      concept_id:
        description: This is a default description.
        type: get
      concept_name:
        description: This is a default description.
        type: get
      is_times_tag:
        description: This is a default description.
        type: get
      concept_status:
        description: This is a default description.
        type: get
      vernacular:
        description: This is a default description.
        type: get
      concept_type:
        description: This is a default description.
        type: get
      concept_created:
        description: This is a default description.
        type: get
      concept_updated:
        description: This is a default description.
        type: get
      taxonomy:
        description: This is a default description.
        type: get
      links:
        description: This is a default description.
        type: get
  ConceptRelation:
    properties:
      concept_id:
        description: This is a default description.
        type: get
      concept_name:
        description: This is a default description.
        type: get
      is_times_tag:
        description: This is a default description.
        type: get
      concept_status:
        description: This is a default description.
        type: get
      vernacular:
        description: This is a default description.
        type: get
      concept_type:
        description: This is a default description.
        type: get
      concept_created:
        description: This is a default description.
        type: get
      concept_updated:
        description: This is a default description.
        type: get
x-collection-name: New York Times
x-streamrank:
  polling_total_time_average: "0.19"
  polling_size_download_average: "3306.75"
  streaming_total_time_average: "0.12"
  streaming_size_download_average: "1772.55"
  change_yes: "200"
  change_no: "3243"
  time_percentage: "39"
  size_percentage: "46"
  change_percentage: "6"
  last_run: "2018-02-19"
  days_run: "3"
  minute_run: "0"
---