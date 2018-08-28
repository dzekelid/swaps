---
swagger: "2.0"
x-collection-name: AWS Elastic Beanstalk
x-complete: 0
info:
  title: AWS Elastic Beanstalk API Swap Environment C N A M Es
  version: 1.0.0
  description: Swaps the CNAMEs of two environments.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=SwapEnvironmentCNAMEs:
    get:
      summary: Swap Environment C N A M Es
      description: Swaps the CNAMEs of two environments.
      operationId: swapEnvironmentCNAMEs
      x-api-path-slug: actionswapenvironmentcnames-get
      parameters:
      - in: query
        name: DestinationEnvironmentId
        description: The ID of the destination environment
        type: string
      - in: query
        name: DestinationEnvironmentName
        description: The name of the destination environment
        type: string
      - in: query
        name: SourceEnvironmentId
        description: The ID of the source environment
        type: string
      - in: query
        name: SourceEnvironmentName
        description: The name of the source environment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
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