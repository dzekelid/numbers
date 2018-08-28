swagger: "2.0"
x-collection-name: Clover
x-complete: 1
info:
  title: ""
  version: 1.0.0
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/customers/{customerId}/phone_numbers:
    post:
      summary: Create a phone number for a customer
      description: Creates a phone number associated to a merchant's customer.
      operationId: DelegatedCreateCustomerPhoneNumber
      x-api-path-slug: v3merchantsmidcustomerscustomeridphone-numbers-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: customerId
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Customers
      - CustomerId
      - Phone
      - Numbers
  /v3/merchants/{mId}/customers/{customerId}/phone_numbers/{phoneId}:
    post:
      summary: Update a phone number for a customer
      description: Updates a merchant's customer's phone number.
      operationId: DelegatedUpdateCustomerPhoneNumber
      x-api-path-slug: v3merchantsmidcustomerscustomeridphone-numbersphoneid-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: customerId
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: phoneId
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Customers
      - CustomerId
      - Phone
      - Numbers
      - PhoneId
    delete:
      summary: Delete a customer phone number
      description: Deletes a merchant's customer's phone number.
      operationId: DelegatedDeleteCustomerPhoneNumber
      x-api-path-slug: v3merchantsmidcustomerscustomeridphone-numbersphoneid-delete
      parameters:
      - in: path
        name: customerId
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: phoneId
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Customers
      - CustomerId
      - Phone
      - Numbers
      - PhoneId