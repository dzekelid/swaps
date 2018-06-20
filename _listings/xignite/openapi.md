---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite Futures
  description: provide-delayed-and-historical-commodity-quote-information-from-supported-exchanges-nymex----
  version: 1.0.0
host: www.xignite.com
basePath: xFutures.json/XigniteFutures
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ListSwaps:
    get:
      summary: List Swaps
      description: List all commodity swaps and the exchange on which they are traded.
      operationId: postListswaps
      x-api-path-slug: listswaps-get
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
      - List
      - Swaps
  /ListSwapsByExchange:
    get:
      summary: List Swaps By Exchange
      description: List swaps information by exchange.
      operationId: postListswapsbyexchange
      x-api-path-slug: listswapsbyexchange-get
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
      - List
      - Swaps
      - By
      - Exchange
  /GetAllDelayedSwaps:
    get:
      summary: Get All Delayed Swaps
      description: Returns delayed quotes for all contracts for a commodity.
      operationId: postGetalldelayedswaps
      x-api-path-slug: getalldelayedswaps-get
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
      - Delayed
      - Swaps
  /GetHistoricalSwaps:
    get:
      summary: Get Historical Swaps
      description: Returns historical quotes for multiple future swaps.
      operationId: postGethistoricalswaps
      x-api-path-slug: gethistoricalswaps-get
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
      - Historical
      - Swaps
  /GetAllHistoricalSwaps:
    get:
      summary: Get All Historical Swaps
      description: Returns historical quotes for all contracts for a commodity swap
        as of a specific date.
      operationId: postGetallhistoricalswaps
      x-api-path-slug: getallhistoricalswaps-get
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
      - Historical
      - Swaps
---