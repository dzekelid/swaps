---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Delete version
  description: Deletes a project version. Deprecated, use [Delete and replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    that supports swapping version values in custom fields, in addition to the swapping
    for `fixVersion` and `affectedVersion` provided in this resource. Alternative
    versions can be provided to update issues that use the deleted version in `fixVersion`
    or `affectedVersion`. If alternatives are not provided, occurrences of `fixVersion`
    and `affectedVersion` that contain the deleted version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/version/{id}:
    delete:
      summary: Delete version
      description: Deletes a project version. Deprecated, use [Delete and replace
        version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
        that supports swapping version values in custom fields, in addition to the
        swapping for `fixVersion` and `affectedVersion` provided in this resource.
        Alternative versions can be provided to update issues that use the deleted
        version in `fixVersion` or `affectedVersion`. If alternatives are not provided,
        occurrences of `fixVersion` and `affectedVersion` that contain the deleted
        version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.deleteVersion_delete
      x-api-path-slug: api2versionid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the version
      - in: query
        name: moveAffectedIssuesTo
        description: The ID of the version to update `affectedVersion` to when the
          field contains the deleted version
      - in: query
        name: moveFixIssuesTo
        description: The ID of the version to update `fixVersion` to when the field
          contains the deleted version
      responses:
        200:
          description: OK
      tags:
      - Version
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