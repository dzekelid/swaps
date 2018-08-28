swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
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
  /api/2/version/{id}/mergeto/{moveIssuesTo}:
    put:
      summary: Merge versions
      description: Merges two project versions. The merge is completed by deleting
        the version specified in `id` and replacing any occurrences of its ID in `fixVersion`
        with the version ID specified in `moveIssuesTo`. Consider using [Delete and
        replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
        instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`,
        and custom fields. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.mergeVersions_put
      x-api-path-slug: api2versionidmergetomoveissuesto-put
      parameters:
      - in: path
        name: id
        description: The ID of the version to delete
      - in: path
        name: moveIssuesTo
        description: The ID of the version to merge into
      responses:
        200:
          description: OK
      tags:
      - Merge
      - Versions
  /api/2/version/{id}/removeAndSwap:
    post:
      summary: Delete and replace version
      description: Deletes a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
        Alternative versions can be provided to update issues that use the deleted
        version in `fixVersion`, `affectedVersion`, or any version picker custom fields.
        If alternatives are not provided, occurrences of `fixVersion`, `affectedVersion`,
        and any version picker custom field, that contain the deleted version, are
        cleared. Any replacement version must be in the same project as the version
        being deleted and cannot be the version being deleted.
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.deleteAndReplaceVersion_post
      x-api-path-slug: api2versionidremoveandswap-post
      parameters:
      - in: path
        name: id
        description: The ID of the version
      responses:
        200:
          description: OK
      tags:
      - Replace
      - Version