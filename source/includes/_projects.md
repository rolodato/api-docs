# Projects

> An example `Project`:

```json
{
  "locator": "git+github.com/ilikebits/assert-http",
  "url": "https://github.com/ilikebits/assert-http",
  "title": "assert-http",
  "description": "Test helpers for testing a HTTP interface",
  "public": true,
  "setup": true,
  "authors": [
    "tom@example.org"
  ],
  "scm_url": null,
  "manual_scm_url": false,
  "issue_tracker_url": "github.com/ilikebits/assert-http",
  "issue_tracker_id": null,
  "issue_tracker_type": "github",
  "browsing_access_level": "common",
  "browsing_access_depth": 3,
  "unlicensed_access_level": "full",
  "unlicensed_newer_flag": true,
  "organizationId": 90,
  "policyId": 251,
  "unlicensed_access_depth": 3,
  "policies_access_level": "common",
  "policies_access_depth": 3,
  "policies_approve_multilicense": true,
  "attribution_access_level": "common",
  "attribution_issue_enabled": false,
  "attribution_access_depth": 3,
  "project_scopes": ["compile", "runtime"],
  "environment_variables": [],
  "maven_profiles": [],
  "gradle_build_file": null,
  "tracking_branches": ["master"],
  "default_branch": "master",
  "transitive_excludes": [],
  "bom_column_settings": [],
  "bom_public_id": null,
  "disable_large_badge": false,
  "require_mediated_dependencies": false,
  "scan_mediated_dependencies": true,
  "createdAt": "2017-11-29T04:38:20.478Z",
  "updatedAt": "2017-11-29T04:40:52.106Z",
  "references": [
    {
      "id": 569364,
      "type": "branch",
      "name": "master",
      "revision_id": "git+github.com/ilikebits/assert-http$4080d6d4749e7eba3a56e3eb35e0cea5d2c25d86",
      "project_id": "git+github.com/ilikebits/assert-http",
      "revision": {
        "loc": {
          "fetcher": "git",
          "package": "github.com/ilikebits/assert-http",
          "revision": "4080d6d4749e7eba3a56e3eb35e0cea5d2c25d86"
        },
        "licenses": [],
        "locator":
          "git+github.com/ilikebits/assert-http$4080d6d4749e7eba3a56e3eb35e0cea5d2c25d86",
        "url": null,
        "resolved": true,
        "projectId": "git+github.com/ilikebits/assert-http",
        "unsupported": false,
        "source_type": "CommonJSPackage",
        "error": null,
        "parent_locator": "git+github.com/ilikebits/assert-http$f23ba7e3380a2aa5c395e2759dbe70cb5ea5102d",
        "attribution_file": null,
        "transitive_excludes": [],
        "author": "ilikebits <leo@fossa.io>",
        "message": "1.1.5\n",
        "revision_timestamp": "2017-07-11 22:09:56.000 +00:00",
        "all_origin_paths": ["package.json"],
        "license_count": 11,
        "dependency_count": 138,
        "todo_count": 6,
        "unresolved_issue_count": 5,
        "dependency_cache_valid": "2017-11-29T04:40:53.448Z",
        "dependency_cache_updated": "2017-11-29T04:40:53.448Z",
        "package_cache_error": "Error: Refused to cache.",
        "createdAt": "2017-11-29T04:38:20.587Z",
        "updatedAt": "2017-11-29T04:40:53.868Z",
        "meta": [
          {
            "organizationId": 90,
            "revisionId": "git+github.com/ilikebits/assert-http$4080d6d4749e7eba3a56e3eb35e0cea5d2c25d86",
            "last_scan": "2017-11-29T04:40:52.076Z",
            "to_scan": null,
            "createdAt": "2017-11-29T04:39:24.032Z",
            "updatedAt": "2017-11-29T04:40:52.077Z"
          }
        ],
        "builds": [
          {
            "locator":
              "git+github.com/ilikebits/assert-http$4080d6d4749e7eba3a56e3eb35e0cea5d2c25d86",
            "error": null,
            "task": {
              "id": 334930,
              "status": "SUCCEEDED",
              "started": "2017-11-29T04:40:06.426Z"
            }
          },
          {
            "locator":
              "git+github.com/ilikebits/assert-http$4080d6d4749e7eba3a56e3eb35e0cea5d2c25d86",
            "error": null,
            "task": {
              "id": 334927,
              "status": "SUCCEEDED",
              "started": "2017-11-29T04:38:21.705Z"
            }
          }
        ]
      }
    }
  ]
}
```

A `Project` is a single module of code, generally a package, dependency, or
repository. `Project`s may have dependencies on other `Project`s.

When we refer to a `Project`, we often mean a "top-level" project i.e. one that
a user explicitly imported for analysis. When we talk about dependencies that
are brought in by top-level projects, we often use the term `Component`.

## List Projects

```bash
http 'http://api.fossa.io/api/projects' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Project 1 elided */
  },
  {
    /* Project 2 elided */
  },
  {
    /* Project 3 elided */
  }
  // ...
];
```

Lists all projects in your organization.

This endpoint supports the standard filtering, search, sorting, and pagination
operators.

### HTTP Request

`GET http://api.fossa.io/api/projects`

### Query parameters

| Parameter  | Type            | Required? | Description                                                                                                                                                                                |
| ---------- | --------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `${field}` | `keyof Project` | N         | Filter results to only include rows where `${field}` is set to the value passed as `${field}`. For example, to only include rows where `organizationId` is `42`, pass `organizationId=42`. |
| `q`        | `any`           | N         | Perform a substring search for the value across all fields.                                                                                                                                |
| `sort`     | `keyof Project` | N         | Sort by the specified field name. Prefix with `-` to sort by descending order. For example, to sort in descending order by `createdAt`, pass `sort=-createdAt`.                            |
| `count`    | `int`           | N         | Paginate response to include only `count` rows per response.                                                                                                                               |
| `page`     | `int`           | N         | Set the pagination page index.                                                                                                                                                             |
| `offset`   | `int`           | N         | Begin pagination at the specified row offset.                                                                                                                                              |

## Retrieve Project

```bash
http 'http://api.fossa.io/api/projects/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Project */
}
```

Retrieve a `Project` by ID.

### HTTP Request

`GET https://api.fossa.io/api/projects/:projectId`

### Path parameters

| Parameter    | Type     | Required? | Description                        |
| ------------ | -------- | --------- | ---------------------------------- |
| `:projectId` | `string` | Y         | The ID of the project to retrieve. |

## Get Project Badge

```bash
http 'http://api.fossa.io/api/projects/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway.svg' 'Authorization: token 123456789'
```

> Renders the project's license scan status badge in SVG format.

Renders a project's license scan status badge.

### HTTP Request

`GET https://api.fossa.io/api/projects/:projectId.svg`

### Query parameters

| Parameter | Type     | Required? | Description                                                                                      |
| --------- | -------- | --------- | ------------------------------------------------------------------------------------------------ |
| `type`    | `string` | N         | Selects the type of badge to render. Defaults to `shield`. Can be `shield`, `small`, or `large`. |

### Path parameters

| Parameter    | Type     | Required? | Description                                               |
| ------------ | -------- | --------- | --------------------------------------------------------- |
| `:projectId` | `string` | Y         | The ID of the project for which to render a status badge. |

## List Project Revisions

```bash
http 'http://api.fossa.io/api/projects/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway/revisions' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Revision 1 elided */
  },
  {
    /* Revision 2 elided */
  },
  {
    /* Revision 3 elided */
  }
  // ...
];
```

Lists all revisions for a project.

This endpoint supports the standard filtering, search, sorting, and pagination
operators.

### HTTP Request

`GET http://api.fossa.io/api/projects/:projectId/revisions`

### Query parameters

| Parameter  | Type             | Required? | Description                                                                                                                                                                                |
| ---------- | ---------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `${field}` | `keyof Revision` | N         | Filter results to only include rows where `${field}` is set to the value passed as `${field}`. For example, to only include rows where `organizationId` is `42`, pass `organizationId=42`. |
| `q`        | `any`            | N         | Perform a substring search for the value across all fields.                                                                                                                                |
| `sort`     | `keyof Revision` | N         | Sort by the specified field name. Prefix with `-` to sort by descending order. For example, to sort in descending order by `createdAt`, pass `sort=-createdAt`.                            |
| `count`    | `int`            | N         | Paginate response to include only `count` rows per response.                                                                                                                               |
| `page`     | `int`            | N         | Set the pagination page index.                                                                                                                                                             |
| `offset`   | `int`            | N         | Begin pagination at the specified row offset.                                                                                                                                              |

### Path parameters

| Parameter    | Type     | Required? | Description                                        |
| ------------ | -------- | --------- | -------------------------------------------------- |
| `:projectId` | `string` | Y         | The ID of the project for which to list revisions. |
