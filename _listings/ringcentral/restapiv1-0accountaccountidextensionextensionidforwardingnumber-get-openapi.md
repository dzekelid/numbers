---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 0
info:
  title: RingCentral Get Forwarding Numbers
  description: "Returns the list of extension phone numbers used for call forwarding
    and call flip. The returned list contains all the extension phone numbers used
    for call forwarding and call flip.\nApp Permission\nReadAccounts\nUser Permission\nReadUserForwardingFlipNumbers\nUsage
    Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
    Message\n   \n \n\n400\nCMN-101\nParameter [perPage] value is invalid\n\n\n401\nCMN-405\nLogin
    to extension required\n\n\n401\nOAU-151\nAuthorization method not supported\n\n\n403\nCMN-401\nIn
    order to call this API endpoint, application needs to have [ReadAccounts] permission\n\n\n403\nCMN-403\nThe
    feature is not available for this extension type\n\n\n403\nCMN-408\nIn order to
    call this API endpoint, user needs to have [ReadUserForwardingFlipNumbers] permission
    for requested resource.\n\n\n404\nCMN-102\nResource for parameter [accountId]
    is not found"
  version: 1.0.0
host: platform.ringcentral.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/blocked-number:
    get:
      summary: Get Blocked Numbers
      description: "Returns the list of phone numbers which are specified by the user
        to block inbound calls and SMS messages.\nApp Permission\nReadAccounts\nUser
        Permission\nReadBlockedNumbers\nUsage Plan Group\nLight\nError Codes\n\n \n
        \ \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [perPage] value is invalid\n\n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadAccounts] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [ReadBlockedNumbers] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: listBlockedNumbers
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidblockednumber-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Numbers
    post:
      summary: Add Blocked Numbers
      description: "Adds a new phone number to the blocked number list.\nApp Permission\nEditExtensions\nUser
        Permission\nEditBlockedNumbers\nUsage Plan Group\nMedium\nError Codes\n\n
        \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [phoneNumber] value is invalid\n\n\n403\nCMN-401\nIn order to call this API
        endpoint, application needs to have [EditExtensions] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [EditBlockedNumbers] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: blockNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidblockednumber-post
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Numbers
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/caller-blocking/phone-numbers:
    get:
      summary: Get Blocked Numbers
      description: "Returns the lists of blocked and allowed phone numbers.\nApp Permission\nReadAccounts\nUser
        Permission\nReadBlockedNumbers\nUsage Plan Group\nLight\nError Codes\n\n \n
        \ \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n404\nCMN-102\nResource
        for parameter [accountId] is not found"
      operationId: listBlockedAllowedPhoneNumberLists
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidcallerblockingphonenumbers-get
      parameters:
      - in: path
        name: accountId
      - in: path
        name: extensionId
      - in: query
        name: page
      - in: query
        name: perPage
      - in: query
        name: status
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Numbers
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/forwarding-number:
    get:
      summary: Get Forwarding Numbers
      description: "Returns the list of extension phone numbers used for call forwarding
        and call flip. The returned list contains all the extension phone numbers
        used for call forwarding and call flip.\nApp Permission\nReadAccounts\nUser
        Permission\nReadUserForwardingFlipNumbers\nUsage Plan Group\nLight\nError
        Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [perPage] value is invalid\n\n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadAccounts] permission\n\n\n403\nCMN-403\nThe
        feature is not available for this extension type\n\n\n403\nCMN-408\nIn order
        to call this API endpoint, user needs to have [ReadUserForwardingFlipNumbers]
        permission for requested resource.\n\n\n404\nCMN-102\nResource for parameter
        [accountId] is not found"
      operationId: listExtensionForwardingNumbers
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidforwardingnumber-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: query
        name: page
        description: Indicates the page number to retrieve
      - in: query
        name: perPage
        description: Indicates the page size (number of items)
      responses:
        200:
          description: OK
      tags:
      - Forwarding
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