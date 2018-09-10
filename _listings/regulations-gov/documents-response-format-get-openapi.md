---
swagger: "2.0"
info:
  title: Regulations.gov
  description: Provides public users access to federal regulatory content.
  version: 1.0.0
host: api.data.gov
basePath: /regulations/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /documents.{response_format}:
    get:
      summary: Search for Documents
      description: This API allows users to build a query based on any of the parameters
        below
      operationId: getDocuments.ResponseFormat
      x-api-path-slug: documents-response-format-get
      parameters:
      - in: query
        name: a
        description: 'Federal Agency: List of accepted Federal Agency values'
      - in: query
        name: cat
        description: 'Document Category: <ul><li>AD (Aerospace and Transportation)</li>
          <li>AEP (Agriculture, Environment, and Public Lands)</li> <li>BFS (Banking
          and Financial)</li> <li>CT (Commerce and International)</li> <li>LES (Defense,
          Law Enforcement, and Security)</li> <li>EELS (Education, Labor, Presidential,
          and Government Services)</li> <li>EUMM (Energy, Natural Resources, and Utilities)</li>
          <li>HCFP (Food Safety, Health, and Pharmaceutical)</li> <li>PRE (Housing,
          Development, and Real Estate)</li> <li>ITT (Technology and Telecommunications)</li></ul>'
      - in: query
        name: cmd
        description: 'Comment Period End Date: Enter a date in the form of MM/DD/YY'
      - in: query
        name: cmsd
        description: 'Comment Period Start Date: Enter a date in the form of MM/DD/YY'
      - in: query
        name: countsOnly
        description: 'Counts Only: <ul><li>1 (will return only the document count
          for a search query)</li><li>0 (will return documents as well)</li></ul>'
      - in: query
        name: cp
        description: 'Comment Period: <ul><li>O: Open</li><li>C: Closed</li></ul>'
      - in: query
        name: crd
        description: 'Creation Date: Enter a date in the form of MM/DD/YY'
      - in: query
        name: cs
        description: 'Comment Period Closing Soon: <ul><li>0 (closing today)</li><li>3
          (closing within 3 days)</li><li>15 (closing within 15 days)</li><li>30 (closing
          within 30 days)</li><li>90 (closing within 90 days)</li></ul>'
      - in: query
        name: dct
        description: 'Document Type: <ul><li>N: Notice</li><li>PR: Proposed Rule</li><li>FR:
          Rule</li><li>O: Other</li><li>SR: Supporting & Related Material</li><li>PS:
          Public Submission</li></ul>'
      - in: query
        name: dkt
        description: 'Docket Type: <ul><li>R: Rulemaking</li><li>N: Nonrulemaking</li></ul><p>A
          Docket Type is either Rulemaking or Nonrulemaking'
      - in: query
        name: dktid
        description: Valid Docket ID (ex
      - in: query
        name: dktst
        description: 'Docket Subtype: Only one docket subtype at a time may be selected'
      - in: query
        name: dktst2
        description: 'Docket Sub-subtype: Only one docket sub-subtype at a time may
          be selected'
      - in: query
        name: docst
        description: 'Document Subtype: Single or multiple document subtypes may be
          included'
      - in: query
        name: encoded
        description: 'Encoded: <ul><li>1 (will accept Regulations'
      - in: query
        name: np
        description: 'Newly Posted: <ul><li>0 (posted today)</li><li>3 (posted within
          last 3 days)</li><li>15 (posted within last 15 days)</li><li>30 (posted
          within last 30 days)</li><li>90 (posted within last 90 days)</li></ul>  For
          periods of time beyond 90-days, please use a date range with the Posted
          Date parameter'
      - in: query
        name: pd
        description: 'Posted Date: Enter a date in the form of MM/DD/YY'
      - in: query
        name: po
        description: Enter the page offset (always starts with 0)
      - in: query
        name: rd
        description: 'Received Date: Enter a date in the form of MM/DD/YY'
      - in: path
        name: response_format
        description: Format
      - in: query
        name: rpp
        description: Results Per Page 10, 25, 100, 500, 1,000
      - in: query
        name: s
        description: Keyword(s)
      - in: query
        name: sb
        description: 'Sort By: <ul><li>docketId (Docket ID)</li><li>docId (Document
          ID)</li><li>title (Title)</li><li>postedDate (Posted Date)</li><li>agency
          (Agency)</li><li>documentType (Document Type)</li><li>submitterName (Submitter
          Name)</li><li>organization (Organization)</li></ul> Sort Order is REQUIRED
          if this parameter is included'
      - in: query
        name: so
        description: 'Sort Order: <ul><li>ASC: Ascending</li><li>DESC: Descending</li></ul>'
      responses:
        200:
          description: OK
      tags:
      - regulations
      - documents
definitions: []
x-collection-name: Regulations.gov
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