---
swagger: "2.0"
x-collection-name: Flowroute
x-complete: 0
info:
  title: FlowRoute API Search for Purchasable Phone Numbers
  description: This endpoint lets you search for phone numbers by state or rate center,
    or by your specified search value.
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/numbers/available:
    get:
      summary: Search for Purchasable Phone Numbers
      description: This endpoint lets you search for phone numbers by state or rate
        center, or by your specified search value.
      operationId: this-endpoint-lets-you-search-for-phone-numbers-by-state-or-rate-center-or-by-your-specified-search-
      x-api-path-slug: v2numbersavailable-get
      parameters:
      - in: query
        name: contains
        description: Retrieve phone numbers containing the specified value
      - in: query
        name: ends_with
        description: Retrieve phone numbers that end with the specified value
      - in: query
        name: limit
        description: Limits the number of items to retrieve
      - in: query
        name: offset
        description: Offsets the list of phone numbers by your specified value
      - in: query
        name: rate_center
        description: Filters by and displays phone numbers in the specified case-insensitive
          abbreviated rat    e center, not the full name as differentiated in the
          NPA Rate Center Reports
      - in: query
        name: starts_with
        description: Retrieve phone numbers that start with the specified value
      - in: query
        name: state
        description: Filters by and displays phone numbers in the specified case-insensitive
          abbreviated rat    e center, not the full name as differentiated in the
          NPA Rate Center Reports
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - SearchPurchasable
      - Phone
      - Numbers
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