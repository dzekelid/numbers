---
swagger: "2.0"
x-collection-name: ARIN
x-complete: 0
info:
  title: Autonomous System Numbers (ASNs) API Autonomous System Number(s)
  description: ""
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /asn:
    get:
      summary: Autonomous System Number(s)
      description: ""
      operationId: asn
      x-api-path-slug: asn-get
      parameters:
      - in: query
        name: handle
        description: the handle of the ASN
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Autonomous Systen Numbers
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---