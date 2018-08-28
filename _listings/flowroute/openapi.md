swagger: "2.0"
x-collection-name: Flowroute
x-complete: 1
info:
  title: Flowroute APIs
  description: the-flowroute-apis-are-organized-around-rest--our-apis-have-resourceoriented-urls-support-http-verbs-and-respond-with-http-status-codes--all-api-requests-and-responses-including-errors-will-be-represented-as-json-objects--you-can-use-the-flowroute-apis-to-manage-your-flowroute-phone-numbers-including-setting-primary-and-failover-routes-for-inbound-calls-and-sending-text-messages-sms-and-mms-using-longcode-or-tollfree-numbers-in-your-account-
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
  /v2/numbers:
    get:
      summary: Account Phone Numbers
      description: Returns a list of all phone numbers currently on your Flowroute
        account. The response includes details such as the phone number's rate center,
        state, number type, and whether CNAM Lookup is enabled for that number.
      operationId: returns-a-list-of-all-phone-numbers-currently-on-your-flowroute-account-the-response-includes-detail
      x-api-path-slug: v2numbers-get
      parameters:
      - in: query
        name: contains
        description: Retrieves phone numbers containing the specified value
      - in: query
        name: ends_with
        description: Retrieves phone numbers that end with the specified value
      - in: query
        name: limit
        description: Limits the number of items to retrieve
      - in: query
        name: offset
        description: Offsets the list of phone numbers by your specified value
      - in: query
        name: starts_with
        description: Retrieves phone numbers that start with the specified value
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Account
      - Phone
      - Numbers
  /v2/numbers/{number_id}/relationships/failover_route:
    patch:
      summary: Update Failover Voice Route for a Phone Number
      description: Use this endpoint to update the failover voice route for a phone
        number. You must create the route first by following "Create an Inbound Route".
        You can then assign the created route by specifying its value in a PATCH request.
      operationId: use-this-endpoint-to-update-the-failover-voice-route-for-a-phone-number-you-must-create-the-route-fi
      x-api-path-slug: v2numbersnumber-idrelationshipsfailover-route-patch
      parameters:
      - in: path
        name: number_id
        description: The phone number in E
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Failover
      - Voice
      - Routea
      - Phone
      - Number
  /v2/numbers/{number_id}/relationships/primary_route:
    patch:
      summary: Update Primary Voice Route for a Phone Number
      description: Use this endpoint to update the primary voice route for a phone
        number. You must create the route first by following "Create an Inbound Route".
        You can then assign the created route by specifying its value in a PATCH request.
      operationId: use-this-endpoint-to-update-the-primary-voice-route-for-a-phone-number-you-must-create-the-route-fir
      x-api-path-slug: v2numbersnumber-idrelationshipsprimary-route-patch
      parameters:
      - in: path
        name: number_id
        description: The phone number in E
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Primary
      - Voice
      - Routea
      - Phone
      - Number
  /v2/numbers/{id}:
    post:
      summary: Purchase a Phone Number
      description: Lets you purchase a phone number from available Flowroute inventory.
      operationId: lets-you-purchase-a-phone-number-from-available-flowroute-inventory
      x-api-path-slug: v2numbersid-post
      parameters:
      - in: path
        name: id
        description: Phone number to purchase
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Purchase
      - Phone
      - Number
    get:
      summary: Phone Number Details
      description: Lists all of the information associated with any of the phone numbers
        in your account, including billing method, primary voice route, and failover
        voice route.
      operationId: lists-all-of-the-information-associated-with-any-of-the-phone-numbers-in-your-account-including-bill
      x-api-path-slug: v2numbersid-get
      parameters:
      - in: path
        name: id
        description: Phone number to search for which must be a number that you own
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Phone
      - Number
      - Details