---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 0
info:
  title: RingCentral Update Blocked Number
  description: "Updates blocked number(s) by their ID(s). Currently only the name
    can be updated. Batch request is supported.\nApp Permission\nEditExtensions\nUser
    Permission\nEditBlockedNumbers\nUsage Plan Group\nMedium\nError Codes\n\n \n  \n
    \  HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
    [] value is invalid\n\n\n403\nCMN-401\nIn order to call this API endpoint, application
    needs to have [EditExtensions] permission\n\n\n403\nCMN-408\nIn order to call
    this API endpoint, user needs to have [EditBlockedNumbers] permission for requested
    resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId] is not found"
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
    post:
      summary: Add Blocked Number
      description: |-
        Updates either blocked or allowed phone number list with a new phone number.
        App Permission
        EditExtensions
        User Permission
        EditBlockedNumbers
        Usage Plan Group
        Medium
      operationId: createBlockedAllowedPhoneNumberLists
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidcallerblockingphonenumbers-post
      parameters:
      - in: path
        name: accountId
      - in: path
        name: extensionId
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Number
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
    post:
      summary: Create Forwarding Numbers
      description: "Adds a new forwarding number to the forwarding number list.\nApp
        Permission\nEditExtensions\nUser Permission\nEditUserForwardingFlipNumbers\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nAWR-180\nCall handling settings not available for
        Fax tiers\n\n\n400\nCMN-101\nParameter [phoneNumber] value is invalid\n\n\n400\nFPN-102\nLabel
        of number Work duplicates with existing forwarding number label\n\n\n400\nFPN-103\nLimit
        of available forwarding numbers (10) exceeded\n\n\n400\nFPN-104\nLimit of
        available custom labeled forwarding numbers (7) exceeded\n\n\n400\nFPN-105\nNumber
        +18442015485 duplicates with company/extension direct number\n\n\n400\nFPN-108\nInternational
        calling is currently disabled\n\n\n403\nCMN-401\nIn order to call this API
        endpoint, application needs to have [EditExtensions] permission\n\n\n403\nCMN-403\nThe
        feature is not available for this extension type\n\n\n404\nCMN-102\nResource
        for parameter [extensionId] is not found"
      operationId: createExtensionForwardingNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidforwardingnumber-post
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: body
        name: body
        description: JSON body
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
      - Forwarding
      - Numbers
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/forwarding-number/{forwardingNumberId}:
    put:
      summary: Update Forwarding Numbers
      description: "Updates the existing forwarding number from the forwarding number
        list.\nApp Permission\nEditExtensions\nUser Permission\nEditUserForwardingFlipNumbers\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [flipNumber] value is invalid\n\n\n400\nFPN-102\nLabel
        of number Home duplicates with existing forwarding number label\n\n\n400\nFPN-105\nNumber
        +18552050457 duplicates with company/extension direct number\n\n\n400\nFPN-106\nFlip
        number 2 is already in use\n\n\n400\nFPN-108\nInternational calling is currently
        disabled\n\n\n403\nCMN-401\nIn order to call this API endpoint, application
        needs to have [EditExtensions] permission\n\n\n403\nCMN-408\nIn order to call
        this API endpoint, user needs to have [EditUserForwardingFlipNumbers] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [forwardingNumberId]
        is not found"
      operationId: updateExtensionForwardingNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidforwardingnumberforwardingnumberid-put
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: body
        name: body
        description: JSON body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: path
        name: forwardingNumberId
        description: Internal identifier of a forwarding number; returned in response
          in the id field
      responses:
        200:
          description: OK
      tags:
      - Forwarding
      - Numbers
    get:
      summary: Get Forwarding Number
      description: "Returns a specific forwarding number.\nApp Permission\nReadAccounts\nUser
        Permission\nReadUserForwardingFlipNumbers\nUsage Plan Group\nLight\nError
        Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n403\nCMN-401\nIn
        order to call this API endpoint, application needs to have [ReadAccounts]
        permission\n\n\n403\nCMN-403\nThe feature is not available for this extension
        type\n\n\n403\nCMN-408\nIn order to call this API endpoint, user needs to
        have [ReadUserForwardingFlipNumbers] permission for requested resource.\n\n\n404\nCMN-102\nResource
        for parameter [accountId] is not found"
      operationId: getForwardingNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidforwardingnumberforwardingnumberid-get
      parameters:
      - in: path
        name: accountId
      - in: path
        name: extensionId
      - in: path
        name: forwardingNumberId
      responses:
        200:
          description: OK
      tags:
      - Forwarding
      - Number
    delete:
      summary: Delete Forwarding Number
      description: "Deletes a forwarding number from the forwarding number list by
        its ID.\nApp Permission\nEditExtensions\nUser Permission\nEditUserForwardingFlipNumbers\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n403\nCMN-408\nIn order to call this API endpoint, user
        needs to have [EditUserForwardingFlipNumbers] permission for requested resource.\n\n\n403\nFPN-107\nDevice
        number cannot be deleted from the forwarding number list\n\n\n404\nCMN-102\nResource
        for parameter [forwardingNumberId] is not found"
      operationId: deleteExtensionForwardingNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidforwardingnumberforwardingnumberid-delete
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: path
        name: forwardingNumberId
        description: Internal identifier of a forwarding number
      responses:
        200:
          description: OK
      tags:
      - Forwarding
      - Number
  /restapi/v1.0/account/{accountId}/phone-number:
    get:
      summary: Get All Company Phone Numbers
      description: "Returns the list of phone numbers assigned to RingCentral customer
        account. Both company-level and extension-level numbers are returned.\nApp
        Permission\nReadAccounts\nUser Permission\nReadCompanyPhoneNumbers\nUsage
        Plan Group\nHeavy\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [perPage] value is invalid\n\n\n401\nCMN-405\nLogin
        to extension required\n\n\n401\nOAU-151\nAuthorization method not supported\n\n\n403\nCMN-401\nIn
        order to call this API endpoint, application needs to have [ReadAccounts]
        permission\n\n\n404\nCMN-102\nResource for parameter [accountId] is not found"
      operationId: listAccountPhoneNumbers
      x-api-path-slug: restapiv1-0accountaccountidphonenumber-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: query
        name: page
        description: Indicates the page number to retrieve
      - in: query
        name: perPage
        description: Indicates the page size (number of items)
      - in: query
        name: usageType
        description: Usage type of a phone number
      responses:
        200:
          description: OK
      tags:
      - Company
      - Phone
      - Numbers
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/blocked-number/{blockedNumberId}:
    get:
      summary: Get Blocked Number
      description: "Returns specific information on blocked phone number(s) by their
        ID(s). Batch request is supported.\nApp Permission\nReadAccounts\nUser Permission\nReadBlockedNumbers\nUsage
        Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n403\nCMN-401\nIn order to call this API endpoint, application
        needs to have [ReadAccounts] permission\n\n\n403\nCMN-408\nIn order to call
        this API endpoint, user needs to have [ReadBlockedNumbers] permission for
        requested resource.\n\n\n404\nCMN-102\nResource for parameter [accountId]
        is not found"
      operationId: loadBlockedNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidblockednumberblockednumberid-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: blockedNumberId
        description: Internal identifiers of a blocked number list entry
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Number
    put:
      summary: Update Blocked Number
      description: "Updates blocked number(s) by their ID(s). Currently only the name
        can be updated. Batch request is supported.\nApp Permission\nEditExtensions\nUser
        Permission\nEditBlockedNumbers\nUsage Plan Group\nMedium\nError Codes\n\n
        \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [] value is invalid\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [EditExtensions] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [EditBlockedNumbers] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: updateBlockedNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidblockednumberblockednumberid-put
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: blockedNumberId
        description: Internal identifier of a blocked number list entry
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
      - Number
    delete:
      summary: Delete Blocked Number
      description: "Deletes a phone number from the blocked number list. Batch request
        is supported.\nApp Permission\nEditExtensions\nUser Permission\nEditBlockedNumbers\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n403\nCMN-401\nIn order to call this API endpoint, application
        needs to have [EditExtensions] permission\n\n\n403\nCMN-408\nIn order to call
        this API endpoint, user needs to have [EditBlockedNumbers] permission for
        requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: unblockNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidblockednumberblockednumberid-delete
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: blockedNumberId
        description: Internal identifiers of a blocked number list entry
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Number
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/caller-blocking/phone-numbers/{blockedNumberId}:
    get:
      summary: Get Blocked Number
      description: "Returns blocked or allowed phone number(s) by their ID(s). Batch
        request is supported.\nApp Permission\nReadAccounts\nUser Permission\nReadBlockedNumbers\nUsage
        Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n404\nCMN-102\nResource for parameter [accountId] is not
        found"
      operationId: listBlockedAllowedPhoneNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidcallerblockingphonenumbersblockednumberid-get
      parameters:
      - in: path
        name: accountId
      - in: path
        name: blockedNumberId
      - in: path
        name: extensionId
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Number
    delete:
      summary: Delete Blocked Number
      description: |-
        Deletes blocked or allowed phone number(s) by their ID(s). Batch request is supported.
        App Permission
        EditExtensions
        User Permission
        EditBlockedNumbers
        Usage Plan Group
        Medium
      operationId: deleteBlockedAllowedPhoneNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidcallerblockingphonenumbersblockednumberid-delete
      parameters:
      - in: path
        name: accountId
      - in: path
        name: blockedNumberId
      - in: path
        name: extensionId
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Number
    put:
      summary: Update Blocked Number
      description: |-
        Updates blocked or allowed phone number(s) by their ID(s). Batch request is supported.
        App Permission
        EditExtensions
        User Permission
        EditBlockedNumbers
        Usage Plan Group
        Medium
      operationId: updateBlockedAllowedPhoneNumber
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidcallerblockingphonenumbersblockednumberid-put
      parameters:
      - in: path
        name: accountId
      - in: path
        name: blockedNumberId
      - in: path
        name: extensionId
      responses:
        200:
          description: OK
      tags:
      - Blocked
      - Number
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/phone-number:
    get:
      summary: Get Extension Phone Number List
      description: "Returns the list of phone numbers that are used by a particular
        extension, and can be filtered by the phone number type. The returned list
        contains all numbers which are directly mapped to a given extension plus the
        features and also company-level numbers which may be used when performing
        different operations on behalf of this extension.\nApp Permission\nReadAccounts\nUser
        Permission\nReadUserPhoneNumbers\nUsage Plan Group\nLight\nError Codes\n\n
        \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [usageType] value is invalid\n\n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadAccounts] permission\n\n\n404\nCMN-102\nResource
        for parameter [extensionId] is not found"
      operationId: listExtensionPhoneNumbers
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidphonenumber-get
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
      - in: query
        name: usageType
        description: Usage type of a phone number
      responses:
        200:
          description: OK
      tags:
      - Extension
      - Phone
      - Number
      - List
  /restapi/v1.0/account/{accountId}/phone-number/{phoneNumberId}:
    get:
      summary: Get Phone Number
      description: "Returns the phone number(s) belonging to a certain account or
        extension by phoneNumberId(s). Batch request is supported.\nApp Permission\nReadAccounts\nUser
        Permission\nReadCompanyPhoneNumbers\nUsage Plan Group\nLight\nError Codes\n\n
        \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n403\nCMN-401\nIn
        order to call this API endpoint, application needs to have [ReadAccounts]
        permission\n\n\n404\nCMN-102\nResource for parameter [accountId] is not found"
      operationId: loadAccountPhoneNumber
      x-api-path-slug: restapiv1-0accountaccountidphonenumberphonenumberid-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: phoneNumberId
        description: Internal identifier of a phone number
      responses:
        200:
          description: OK
      tags:
      - Phone
      - Number
  /restapi/v1.0/number-parser/parse:
    post:
      summary: Parse Phone Number [Beta]
      description: "Returns one or more parsed and/or formatted phone numbers that
        are passed as a string.\nUsage Plan Group\nLight\nError Codes\n\n \n  \n   HTTP
        Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter [nationalAsPriority]
        value is invalid"
      operationId: parsePhoneNumber
      x-api-path-slug: restapiv1-0numberparserparse-post
      parameters:
      - in: body
        name: body
        description: JSON body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: homeCountry
        description: Internal identifier of a home country
      - in: query
        name: nationalAsPriority
        description: The default value is False
      responses:
        200:
          description: OK
      tags:
      - Parse
      - Phone
      - Number
      - '[Beta]'
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