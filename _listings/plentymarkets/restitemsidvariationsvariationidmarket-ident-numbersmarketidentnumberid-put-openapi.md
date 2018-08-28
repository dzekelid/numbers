---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Updates a market ident number
  description: Updates a market ident number (ASIN/ePID) of a variation.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/orders/{orderId}/items/serialNumbers:
    get:
      summary: List serial numbers of an order
      description: Lists all serial numbers of an order. The ID of the order must
        be specified.
      operationId: getRestOrdersOrderItemsSerialnumbers
      x-api-path-slug: restordersorderiditemsserialnumbers-get
      parameters:
      - in: path
        name: orderId
      responses:
        200:
          description: OK
      tags:
      - List
      - Serial
      - Numbers
      - Of
      - Order
  /rest/orders/{orderId}/items/{orderItemId}/serialNumbers:
    get:
      summary: List serial numbers of an order item
      description: Lists all serial numbers of an order item. The ID of the order
        and the ID of the order item must be specified.
      operationId: getRestOrdersOrderItemsOrderitemSerialnumbers
      x-api-path-slug: restordersorderiditemsorderitemidserialnumbers-get
      parameters:
      - in: path
        name: orderId
      - in: path
        name: orderItemId
      responses:
        200:
          description: OK
      tags:
      - List
      - Serial
      - Numbers
      - Of
      - Order
      - Item
  /rest/orders/{orderId}/packagenumbers:
    get:
      summary: List package numbers of an order
      description: Lists the package numbers of an order. The ID of the order must
        be specified.
      operationId: getRestOrdersOrderPackagenumbers
      x-api-path-slug: restordersorderidpackagenumbers-get
      parameters:
      - in: path
        name: orderId
      responses:
        200:
          description: OK
      tags:
      - List
      - Package
      - Numbers
      - Of
      - Order
  /rest/items/{id}/variations/{variationId}/market_ident_numbers:
    get:
      summary: List ident number of a variation
      description: Lists the ident number (ASIN/ePID) of a variation. The ID of the
        item and the ID of the variation must be specified.
      operationId: getRestItemsVariationsVariationMarketEntNumbers
      x-api-path-slug: restitemsidvariationsvariationidmarket-ident-numbers-get
      parameters:
      - in: path
        name: id
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - List
      - Ident
      - Number
      - Of
      - Variation
    post:
      summary: Create a market ident number
      description: Creates a market ident number (ASIN/ePID) for a variation.
      operationId: postRestItemsVariationsVariationMarketEntNumbers
      x-api-path-slug: restitemsidvariationsvariationidmarket-ident-numbers-post
      parameters:
      - in: body
        name: /rest/items/{id}/variations/{variationId}/market_ident_numbers
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Market
      - Ident
      - Number
  /rest/items/{id}/variations/{variationId}/market_ident_numbers/{marketIdentNumberId}:
    delete:
      summary: Deletes a market ident number
      description: Deletes a market ident number (ASIN/ePID) of a variation.
      operationId: deleteRestItemsVariationsVariationMarketEntNumbersMarketentnumber
      x-api-path-slug: restitemsidvariationsvariationidmarket-ident-numbersmarketidentnumberid-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: marketIdentNumberId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - S
      - Market
      - Ident
      - Number
    get:
      summary: Get a market ident number
      description: Gets a market ident number (ASIN/ePID) of a variation.
      operationId: getRestItemsVariationsVariationMarketEntNumbersMarketentnumber
      x-api-path-slug: restitemsidvariationsvariationidmarket-ident-numbersmarketidentnumberid-get
      parameters:
      - in: path
        name: id
      - in: path
        name: marketIdentNumberId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - Market
      - Ident
      - Number
    put:
      summary: Updates a market ident number
      description: Updates a market ident number (ASIN/ePID) of a variation.
      operationId: putRestItemsVariationsVariationMarketEntNumbersMarketentnumber
      x-api-path-slug: restitemsidvariationsvariationidmarket-ident-numbersmarketidentnumberid-put
      parameters:
      - in: body
        name: /rest/items/{id}/variations/{variationId}/market_ident_numbers/{marketIdentNumberId}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: path
        name: marketIdentNumberId
      - in: path
        name: variationId
      responses:
        200:
          description: OK
      tags:
      - S
      - Market
      - Ident
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