---
swagger: "2.0"
x-collection-name: EU VAT API
x-complete: 0
info:
  title: EU VAT API Validate a VAT number
  description: Validate a vat number.
  version: "1"
host: vatapi.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /vat-number-check:
    get:
      summary: Validate a VAT number
      description: Validate a vat number.
      operationId: vat_number_validate
      x-api-path-slug: vatnumbercheck-get
      parameters:
      - in: header
        name: Response-Type
        description: The default response type is application/json if you would like
          to receive an XML response then set this to XML
      - in: query
        name: vatid
        description: The VAT number to validate
      responses:
        200:
          description: OK
      tags:
      - Validate
      - VAT
      - Number
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