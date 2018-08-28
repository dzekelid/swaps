swagger: "2.0"
x-collection-name: AWS Elastic Beanstalk
x-complete: 1
info:
  title: AWS Elastic Beanstalk API
  version: 1.0.0
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