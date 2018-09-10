swagger: "2.0"
x-collection-name: San Francisco California 311
x-complete: 1
info:
  title: San Francisco CA Open311 GeoReport API
  description: open311-allows-you-to-getpost-civic-information-of-cities-via-a-unified-interface--the-georeport-part-allows-you-to-submit-and-view-issues-at-the-public-local-space
  termsOfService: (depends on server instance for example NYC http://dev.cityofchicago.org/docs/api/tos)
  contact:
    name: Open311 community
    url: http://wiki.open311.org/GeoReport_v2/
    email: discuss@lists.open311.org
  version: 1.0.0
host: mobile311.sfgov.org
basePath: /open311/v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json