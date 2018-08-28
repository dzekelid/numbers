swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite VWAP
  description: provides-delayed-and-historical-volumeweightedaverage-price-vwap-information-
  version: 1.0.0
host: www.xignite.com
basePath: xVWAP.json/XigniteVWAP
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetEventsForNextNumberOfDays:
    get:
      summary: Get Events For Next Number Of Days
      description: Get events for the next number of days into the future.
      operationId: postGeteventsfornextnumberofdays
      x-api-path-slug: geteventsfornextnumberofdays-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Events
      - Next
      - Number
      - Days