---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 0
info:
  title: Callfire Update a lease config
  description: Updates a phone number lease configuration. Use this API endpoint to
    add an Inbound IVR or Call Tracking feature to a CallFire phone number. Call tracking
    configuration allows you to track the incoming calls, to analyze and to respond
    customers using sms or voice replies. For more information see [call tracking
    page](https://www.callfire.com/products/call-tracking)
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /numbers/leases:
    get:
      summary: Find leases
      description: Searches for all numbers leased by account user. This API is useful
        for finding all numbers currently owned by the user. Returns a paged list
        of number leases.
      operationId: findNumberLeases
      x-api-path-slug: numbersleases-get
      parameters:
      - in: query
        name: city
        description: A city name
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: labelName
        description: A label name
      - in: query
        name: lata
        description: A local access and transport area (LATA)
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: prefix
        description: A 4-7 digit prefix
      - in: query
        name: rateCenter
        description: A rate center
      - in: query
        name: state
        description: A two-letter state code
      - in: query
        name: zipcode
        description: A five-digit Zipcode
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Leases
  /numbers/leases/configs:
    get:
      summary: Find lease configs
      description: Searches for all number lease configs for the user. Returns a paged
        list of NumberConfig
      operationId: findNumberLeaseConfigs
      x-api-path-slug: numbersleasesconfigs-get
      parameters:
      - in: query
        name: city
        description: A city name
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: labelName
        description: A label name
      - in: query
        name: lata
        description: A local access and transport area (LATA)
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: prefix
        description: A 4-7 digit prefix
      - in: query
        name: rateCenter
        description: A rate center
      - in: query
        name: state
        description: A two-letter state code
      - in: query
        name: zipcode
        description: A five-digit Zipcode
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Leases
      - Configs
  /numbers/leases/configs/{number}:
    get:
      summary: Find a specific lease config
      description: Returns a single NumberConfig instance for a given number lease
      operationId: getNumberLeaseConfig
      x-api-path-slug: numbersleasesconfigsnumber-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: number
        description: A phone number in E
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Leases
      - Configs
      - Number
    put:
      summary: Update a lease config
      description: Updates a phone number lease configuration. Use this API endpoint
        to add an Inbound IVR or Call Tracking feature to a CallFire phone number.
        Call tracking configuration allows you to track the incoming calls, to analyze
        and to respond customers using sms or voice replies. For more information
        see [call tracking page](https://www.callfire.com/products/call-tracking)
      operationId: updateNumberLeaseConfig
      x-api-path-slug: numbersleasesconfigsnumber-put
      parameters:
      - in: body
        name: body
        description: The configuration of a number lease object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: A phone number in E
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Leases
      - Configs
      - Number
  /numbers/leases/{number}:
    get:
      summary: Find a specific lease
      description: Returns a single NumberLease instance for a given number
      operationId: getNumberLease
      x-api-path-slug: numbersleasesnumber-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: number
        description: A phone number in E
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Leases
      - Number
    put:
      summary: Update a lease
      description: Updates a number lease instance. Ability to turn on/off autoRenew
        and toggle call/text features for a particular number
      operationId: updateNumberLease
      x-api-path-slug: numbersleasesnumber-put
      parameters:
      - in: body
        name: body
        description: A NumberLease object to update
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: A phone number in E
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Leases
      - Number
  /numbers/local:
    get:
      summary: Find local numbers
      description: Searches for numbers available for purchase in CallFire local numbers
        catalog . At least one additional parameter is required. User may filter local
        numbers by their region information.
      operationId: findNumbersLocal
      x-api-path-slug: numberslocal-get
      parameters:
      - in: query
        name: city
        description: A city name
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: lata
        description: A local access and transport area (LATA)
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: prefix
        description: A 4-7 digit prefix
      - in: query
        name: rateCenter
        description: A rate center
      - in: query
        name: state
        description: A two-letter state code
      - in: query
        name: zipcode
        description: A five-digit Zipcode
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Local
  /numbers/regions:
    get:
      summary: Find number regions
      description: Searches for region information. Use this API to obtain detailed
        region information that can be used to query for more specific phone numbers
        than a general query.
      operationId: findNumberRegions
      x-api-path-slug: numbersregions-get
      parameters:
      - in: query
        name: city
        description: A city name
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: lata
        description: A local access and transport area (LATA)
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: offset
        description: Offset to the start of a given page
      - in: query
        name: prefix
        description: A 4-7 digit prefix
      - in: query
        name: rateCenter
        description: A rate center
      - in: query
        name: state
        description: A two-letter state code
      - in: query
        name: zipcode
        description: A five-digit Zipcode
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Regions
  /numbers/tollfree:
    get:
      summary: Find tollfree numbers
      description: Searches for the toll free numbers which are available for purchase
        in the CallFire catalog
      operationId: findNumbersTollfree
      x-api-path-slug: numberstollfree-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: pattern
        description: Filter toll free numbers by prefix, pattern must be 3 char long
          and should end with *
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Tollfree
  /orders/numbers:
    post:
      summary: Purchase numbers
      description: Purchase numbers. There are many ways to purchase a number. Set
        either 'tollFreeCount' or 'localCount' along with some querying fields to
        purchase numbers by bulk query. Set the list of numbers to purchase by list.
        Available numbers will be purchased using CallFire credits owned by the user.
        Make sure the account has enough credits before trying to purchase
      operationId: orderNumbers
      x-api-path-slug: ordersnumbers-post
      parameters:
      - in: body
        name: body
        description: 'Request object contains a list of numbers to buy, you can filter
          the numbers by their region information: city, state, zipcode, LATA, etc'
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Orders
      - Numbers
  /contacts/dncs/{number}:
    delete:
      summary: Delete do not contact (dnc) number. If number contains commas treat
        as list of numbers
      description: Delete a Do Not Contact (DNC) contact entry.
      operationId: deleteDoNotContact
      x-api-path-slug: contactsdncsnumber-delete
      parameters:
      - in: path
        name: number
        description: Number associated with Do Not Contact (DNC) entry
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
      - Number
    get:
      summary: Get do not contact (dnc)
      description: Get Do Not Contact (DNC) object create by user. This DoNotContact
        entry only affects calls/texts/campaigns on this account.
      operationId: getDoNotContact
      x-api-path-slug: contactsdncsnumber-get
      parameters:
      - in: path
        name: number
        description: Number associated with Do Not Contact (DNC) entry
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
      - Number
    put:
      summary: Update an individual do not contact (dnc) number
      description: Update a Do Not Contact (DNC) contact entry. Can toggle whether
        the DNC is enabled for calls/texts.
      operationId: updateDoNotContact
      x-api-path-slug: contactsdncsnumber-put
      parameters:
      - in: body
        name: body
        description: DoNotContact object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: "~"
      responses:
        200:
          description: OK
      tags:
      - Contacts
      - Dncs
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