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
  /GetDelayedSwap:
    get:
      summary: Get Delayed Swap
      description: Returns a delayed quote for a NYMEX swap contract.
      operationId: postGetdelayedswap
      x-api-path-slug: getdelayedswap-get
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
      - Swap
  /GetHistoricalSwapStrip:
    get:
      summary: Get Historical Swap Strip
      description: Returns a future strip for a commodity.
      operationId: postGethistoricalswapstrip
      x-api-path-slug: gethistoricalswapstrip-get
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
      - Swap
      - Strip
  /GetHistoricalSwap:
    get:
      summary: Get Historical Swap
      description: Returns a historical quote for a future swap.
      operationId: postGethistoricalswap
      x-api-path-slug: gethistoricalswap-get
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
      - Swap
  /GetHistoricalSwapRange:
    get:
      summary: Get Historical Swap Range
      description: Returns a range of historical quotes for a future swap.
      operationId: postGethistoricalswaprange
      x-api-path-slug: gethistoricalswaprange-get
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
      - Swap
      - Range
  /GetSwapQuote:
    get:
      summary: Get Swap Quote
      description: Returns realtime quote for a swap
      operationId: GetSwapQuote
      x-api-path-slug: getswapquote-get
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
      - Swap
      - Quote
  /GetHistoricalSwapQuotes:
    get:
      summary: Get Historical Swap Quotes
      description: Returns historical swap quotes within a date range
      operationId: GetHistoricalSwapQuotes
      x-api-path-slug: gethistoricalswapquotes-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Swap
      - Quotes
  /GetSwapRate:
    get:
      summary: Get Swap Rate
      description: Returns a Swap rate
      operationId: postGetswaprate
      x-api-path-slug: getswaprate-get
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
      - Swap
      - Rate
  /GetSwapRateFamily:
    get:
      summary: Get Swap Rate Family
      description: Returns a Swap rate Family
      operationId: postGetswapratefamily
      x-api-path-slug: getswapratefamily-get
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
      - Swap
      - Rate
      - Family
  /GetHistoricalSwapRate:
    get:
      summary: Get Historical Swap Rate
      description: Returns a Swap rate as of a historical date
      operationId: postGethistoricalswaprate
      x-api-path-slug: gethistoricalswaprate-get
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
      - Swap
      - Rate
  /GetHistoricalSwapRateRange:
    get:
      summary: Get Historical Swap Rate Range
      description: Returns a Swap rate as of a historical date
      operationId: postGethistoricalswapraterange
      x-api-path-slug: gethistoricalswapraterange-get
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
      - Swap
      - Rate
      - Range
  /GetSwapRateExtended:
    get:
      summary: Get Swap Rate Extended
      description: Returns latest Swap rate
      operationId: postGetswaprateextended
      x-api-path-slug: getswaprateextended-get
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
      - Swap
      - Rate
      - Extended
  /GetSwapRateFamilyExtended:
    get:
      summary: Get Swap Rate Family Extended
      description: Returns latest Swap rate family
      operationId: postGetswapratefamilyextended
      x-api-path-slug: getswapratefamilyextended-get
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
      - Swap
      - Rate
      - Family
      - Extended
  /GetHistoricalSwapRateExtended:
    get:
      summary: Get Historical Swap Rate Extended
      description: Returns historical swap rate
      operationId: postGethistoricalswaprateextended
      x-api-path-slug: gethistoricalswaprateextended-get
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
      - Swap
      - Rate
      - Extended
  /GetHistoricalSwapRateExtendedRange:
    get:
      summary: Get Historical Swap Rate Extended Range
      description: Returns historical Swap rate range
      operationId: postGethistoricalswaprateextendedrange
      x-api-path-slug: gethistoricalswaprateextendedrange-get
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
      - Swap
      - Rate
      - Extended
      - Range
  /ListSwapRates:
    get:
      summary: List Swap Rates
      description: Returns swap rate currencies and tenors
      operationId: postListswaprates
      x-api-path-slug: listswaprates-get
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
      - Swap
      - Rates