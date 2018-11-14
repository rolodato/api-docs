# Builds

> An example Build:

```json
{
  "id": 326982,
  "locator":
    "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
  "ownerId": null,
  "error": null,
  "warnings": null,
  "post_mediate": false,
  "taskId": 334918,
  "createdAt": "2017-11-29T01:41:05.651Z",
  "updatedAt": "2017-11-29T01:41:11.289Z",
  "task": {
    "createdAt": "2017-11-29T01:41:05.779Z",
    "started": "2017-11-29T01:41:06.918Z",
    "finished": "2017-11-29T01:41:13.668Z",
    "id": 334918,
    "status": "SUCCEEDED"
  },
  "revision": {
    "loc": {
      "fetcher": "git",
      "package": "github.com/ilikebits/datasets-api-gateway",
      "revision": "61a994bba02325694e93ad697419e0acab5eed78"
    },
    "licenses": [],
    "locator":
      "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
    "projectId": "git+github.com/ilikebits/datasets-api-gateway",
    "message": "Adding isc license, as intended by package.json",
    "meta": [
      {
        "organizationId": 90,
        "revisionId":
          "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
        "last_scan": "2017-12-01T23:42:11.938Z",
        "to_scan": null,
        "createdAt": "2017-11-29T01:41:25.486Z",
        "updatedAt": "2017-12-01T23:42:11.939Z"
      }
    ],
    "project": {
      "title": "datasets-api-gateway",
      "description":
        "An example server application for handling requests to the Datasets API",
      "authors": [
        "tmcw@users.noreply.github.com",
        "tom@macwright.org",
        "rafa@mapbox.com",
        "geografa@users.noreply.github.com",
        "admin+snyk-bot@snyk.io"
      ],
      "locator": "git+github.com/ilikebits/datasets-api-gateway",
      "url": "https://github.com/ilikebits/datasets-api-gateway",
      "public": true,
      "browsing_access_level": "common",
      "browsing_access_depth": 3,
      "transitive_excludes": [],
      "project_scopes": ["compile", "runtime"],
      "organizationId": 90,
      "bom_column_settings": [],
      "default_branch": "master",
      "scan_mediated_dependencies": true
    }
  }
}
```

A `Build` of a `Revision` represents the task and result of performing dynamic
analysis on a particular `Revision`.

## List Builds

```bash
http 'https://app.fossa.io/api/builds' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Build 1 elided */
  },
  {
    /* Build 2 elided */
  },
  {
    /* Build 3 elided */
  }
  // ...
];
```

Lists all builds.

This endpoint supports the standard filtering, search, sorting, and pagination
operators.

### HTTP Request

`GET https://app.fossa.io/api/builds`

### Query parameters

| Parameter  | Type          | Required? | Description                                                                                                                                                                      |
| ---------- | ------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `${field}` | `keyof Build` | N         | Filter results to only include rows where `${field}` is set to the value passed as `${field}`. For example, to only include rows where `ownerId` is `null`, pass `ownerId=null`. |
| `q`        | `any`         | N         | Perform a substring search for the value across all fields.                                                                                                                      |
| `sort`     | `keyof Build` | N         | Sort by the specified field name. Prefix with `-` to sort by descending order. For example, to sort in descending order by `createdAt`, pass `sort=-createdAt`.                  |
| `count`    | `int`         | N         | Paginate response to include only `count` rows per response.                                                                                                                     |
| `page`     | `int`         | N         | Set the pagination page index.                                                                                                                                                   |
| `offset`   | `int`         | N         | Begin pagination at the specified row offset.                                                                                                                                    |

## Retrieve Build

```bash
http 'https://app.fossa.io/api/builds/326982' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Build */
}
```

Retrieve a Build by ID.

### HTTP Request

`GET https://app.fossa.io/api/builds/:buildId`

### Path parameters

| Parameter  | Type     | Required? | Description                      |
| ---------- | -------- | --------- | -------------------------------- |
| `:buildId` | `number` | Y         | The ID of the build to retrieve. |
