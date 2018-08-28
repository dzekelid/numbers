---
swagger: "2.0"
x-collection-name: Shopify
x-complete: 0
info:
  title: Shopify Count all the total number of fulfillments for an order.
  description: Count all the total number of fulfillments for an order..
  version: 1.0.0
host: DefaultParameterValue:DefaultParameterValue@DefaultParameterValue.myshopify.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/orders/4528049998/fulfillments/count.json:
    get:
      summary: Count all the total number of fulfillments for an order.
      description: Count all the total number of fulfillments for an order..
      operationId: getAdminOrders4528049998FulfillmentsCount.json
      x-api-path-slug: adminorders4528049998fulfillmentscount-json-get
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Count
      - Total
      - Number
      - Fulfillmentsan
      - Order
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