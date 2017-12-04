# Revisions

> An example Revision:

```json
{
  "loc": {
    "fetcher": "git",
    "package": "github.com/ilikebits/datasets-api-gateway",
    "revision": "61a994bba02325694e93ad697419e0acab5eed78"
  },
  "licenses": [
    {
      "id": "52e58b3e81519e003b00009f",
      "title": " ISC License",
      "shorthand": "isc",
      "spdx_id": "ISC",
      "permissiveness_score": 50,
      "RevisionLicense": {
        "id": 829259,
        "licenseId": "52e58b3e81519e003b00009f",
        "revisionId":
          "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
        "licenseGroupId": 163087,
        "ignored": false,
        "title": "ISC",
        "url": null,
        "text": null,
        "match": "ISC",
        "file_count": 1,
        "manual": false,
        "createdAt": "2017-11-29T03:51:34.603Z",
        "updatedAt": "2017-11-29T03:51:34.603Z"
      }
    },
    {
      "id": "52c85ec302e7ac6f34000008",
      "title": "MIT License (Expat)",
      "shorthand": "mit",
      "spdx_id": "MIT",
      "permissiveness_score": 62,
      "RevisionLicense": {
        "id": 829258,
        "licenseId": "52c85ec302e7ac6f34000008",
        "revisionId":
          "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
        "licenseGroupId": 163086,
        "ignored": false,
        "title": "MIT",
        "url": null,
        "text": null,
        "match": "MIT",
        "file_count": 1,
        "manual": false,
        "createdAt": "2017-11-29T03:51:34.558Z",
        "updatedAt": "2017-11-29T03:51:34.558Z"
      }
    }
  ],
  "locator":
    "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
  "url": null,
  "resolved": true,
  "projectId": "git+github.com/ilikebits/datasets-api-gateway",
  "unsupported": false,
  "source_type": "CommonJSPackage",
  "error": null,
  "parent_locator":
    "git+github.com/ilikebits/datasets-api-gateway$2247565519e719d5ac4fd493f6a2bc962bf8c889",
  "attribution_file": null,
  "transitive_excludes": [],
  "author": "Tom MacWright <tmcw@users.noreply.github.com>",
  "message": "Adding isc license, as intended by package.json",
  "revision_timestamp": "2017-01-26 15:48:32.000 +00:00",
  "all_origin_paths": ["package.json"],
  "license_count": 4,
  "dependency_count": 60,
  "todo_count": 4,
  "unresolved_issue_count": 0,
  "dependency_cache_valid": "2017-11-29T04:15:10.442Z",
  "dependency_cache_updated": "2017-11-29T04:15:10.442Z",
  "package_cache_error": "Error: Refused to cache.",
  "createdAt": "2017-11-29T01:41:05.389Z",
  "updatedAt": "2017-12-01T23:42:12.121Z",
  "builds": [
    {
      "error": null,
      "id": 326988,
      "task": {
        "started": null,
        "finished": null,
        "status": "CREATED",
        "id": 334944
      }
    },
    {
      "error": null,
      "id": 326983,
      "task": {
        "started": "2017-11-29T03:51:20.031Z",
        "finished": "2017-11-29T03:51:35.189Z",
        "status": "SUCCEEDED",
        "id": 334924
      }
    },
    {
      "error": null,
      "id": 326982,
      "task": {
        "started": "2017-11-29T01:41:06.918Z",
        "finished": "2017-11-29T01:41:13.668Z",
        "status": "SUCCEEDED",
        "id": 334918
      }
    }
  ],
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
  },
  "isSteady": true,
  "dependencies": [
    {
      "loc": {
        "fetcher": "npm",
        "package": "body-parser",
        "revision": "1.18.2"
      },
      "licenses": [
        {
          "id": "52c85ec302e7ac6f34000008",
          "title": "MIT License (Expat)",
          "permissiveness_score": 62,
          "tags": ["Open Source", "OSI-Approved", "Permissive"],
          "shorthand": "mit",
          "RevisionLicense": {
            "id": 672040,
            "licenseId": "52c85ec302e7ac6f34000008",
            "revisionId": "npm+body-parser$1.18.2",
            "licenseGroupId": 56449,
            "ignored": false,
            "title": "MIT",
            "url": null,
            "text": null,
            "match": "MIT",
            "file_count": 8,
            "manual": false,
            "createdAt": "2017-09-22T18:53:01.912Z",
            "updatedAt": "2017-09-22T18:53:01.912Z",
            "matches": [{ "path": "README.md" }, { "path": "DECLARED_LICENSE" }]
          }
        }
      ],
      "locator": "npm+body-parser$1.18.2",
      "resolved": true,
      "parent_locator": "npm+body-parser$1.18.1",
      "builds": [
        {
          "error": null,
          "id": 285056,
          "task": {
            "started": "2017-09-22T18:52:47.318Z",
            "finished": "2017-09-22T18:53:03.628Z",
            "status": "SUCCEEDED",
            "id": 268614
          }
        }
      ],
      "project": {
        "locator": "npm+body-parser",
        "title": "body-parser",
        "organizationId": null,
        "browsing_access_level": "common",
        "project_scopes": [],
        "url": "https://github.com/expressjs/body-parser"
      },
      "revisionLicenses": [
        {
          "id": 672040,
          "licenseId": "52c85ec302e7ac6f34000008",
          "revisionId": "npm+body-parser$1.18.2",
          "licenseGroupId": 56449,
          "ignored": false,
          "title": "MIT",
          "url": null,
          "text": null,
          "match": "MIT",
          "file_count": 8,
          "manual": false,
          "createdAt": "2017-09-22T18:53:01.912Z",
          "updatedAt": "2017-09-22T18:53:01.912Z",
          "license": {
            "id": "52c85ec302e7ac6f34000008",
            "title": "MIT License (Expat)",
            "permissiveness_score": 62,
            "tags": ["Open Source", "OSI-Approved", "Permissive"],
            "shorthand": "mit",
            "RevisionLicense": {
              "id": 672040,
              "licenseId": "52c85ec302e7ac6f34000008",
              "revisionId": "npm+body-parser$1.18.2",
              "licenseGroupId": 56449,
              "ignored": false,
              "title": "MIT",
              "url": null,
              "text": null,
              "match": "MIT",
              "file_count": 8,
              "manual": false,
              "createdAt": "2017-09-22T18:53:01.912Z",
              "updatedAt": "2017-09-22T18:53:01.912Z",
              "matches": [
                { "path": "README.md" },
                { "path": "DECLARED_LICENSE" }
              ]
            }
          },
          "matches": [{ "path": "README.md" }, { "path": "DECLARED_LICENSE" }]
        }
      ],
      "DependencyLock": {
        "organizationId": 90,
        "type": "DETERMINED",
        "root":
          "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
        "locator": "npm+body-parser$1.18.2",
        "unresolved_locators": [
          "npm+body-parser$^1.15.2",
          "npm+body-parser$1.18.2"
        ],
        "origin_paths": ["package.json"],
        "depth": 1,
        "manual": false,
        "optional": false,
        "tags": ["dependencies"],
        "is_submodule": false,
        "createdAt": "2017-11-29T04:15:10.332Z",
        "updatedAt": "2017-11-29T04:15:10.332Z"
      },
      "origin_paths": ["package.json"],
      "manual": false,
      "unresolved_locators": [
        "npm+body-parser$^1.15.2",
        "npm+body-parser$1.18.2"
      ],
      "is_submodule": false,
      "type": "DETERMINED",
      "depth": 1
    },
    {
      "loc": { "fetcher": "npm", "package": "express", "revision": "4.16.2" },
      "licenses": [
        {
          "id": "52c85ec302e7ac6f34000008",
          "title": "MIT License (Expat)",
          "permissiveness_score": 62,
          "tags": ["Open Source", "OSI-Approved", "Permissive"],
          "shorthand": "mit",
          "RevisionLicense": {
            "id": 702668,
            "licenseId": "52c85ec302e7ac6f34000008",
            "revisionId": "npm+express$4.16.2",
            "licenseGroupId": 78600,
            "ignored": false,
            "title": "MIT",
            "url": null,
            "text": null,
            "match": "MIT",
            "file_count": 14,
            "manual": false,
            "createdAt": "2017-10-10T03:33:09.557Z",
            "updatedAt": "2017-10-10T03:33:09.557Z",
            "matches": [{ "path": "Readme.md" }, { "path": "DECLARED_LICENSE" }]
          }
        }
      ],
      "locator": "npm+express$4.16.2",
      "resolved": true,
      "parent_locator": "npm+express$4.16.1",
      "builds": [
        {
          "error": null,
          "id": 295197,
          "task": {
            "started": "2017-10-10T03:32:48.546Z",
            "finished": "2017-10-10T03:33:13.577Z",
            "status": "SUCCEEDED",
            "id": 282120
          }
        }
      ],
      "project": {
        "locator": "npm+express",
        "title": "express",
        "organizationId": null,
        "browsing_access_level": "common",
        "project_scopes": [],
        "url": "https://github.com/expressjs/express"
      },
      "revisionLicenses": [
        {
          "id": 702668,
          "licenseId": "52c85ec302e7ac6f34000008",
          "revisionId": "npm+express$4.16.2",
          "licenseGroupId": 78600,
          "ignored": false,
          "title": "MIT",
          "url": null,
          "text": null,
          "match": "MIT",
          "file_count": 14,
          "manual": false,
          "createdAt": "2017-10-10T03:33:09.557Z",
          "updatedAt": "2017-10-10T03:33:09.557Z",
          "license": {
            "id": "52c85ec302e7ac6f34000008",
            "title": "MIT License (Expat)",
            "permissiveness_score": 62,
            "tags": ["Open Source", "OSI-Approved", "Permissive"],
            "shorthand": "mit",
            "RevisionLicense": {
              "id": 702668,
              "licenseId": "52c85ec302e7ac6f34000008",
              "revisionId": "npm+express$4.16.2",
              "licenseGroupId": 78600,
              "ignored": false,
              "title": "MIT",
              "url": null,
              "text": null,
              "match": "MIT",
              "file_count": 14,
              "manual": false,
              "createdAt": "2017-10-10T03:33:09.557Z",
              "updatedAt": "2017-10-10T03:33:09.557Z",
              "matches": [
                { "path": "Readme.md" },
                { "path": "DECLARED_LICENSE" }
              ]
            }
          },
          "matches": [{ "path": "Readme.md" }, { "path": "DECLARED_LICENSE" }]
        }
      ],
      "DependencyLock": {
        "organizationId": 90,
        "type": "DETERMINED",
        "root":
          "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
        "locator": "npm+express$4.16.2",
        "unresolved_locators": ["npm+express$^4.14.0"],
        "origin_paths": ["package.json"],
        "depth": 1,
        "manual": false,
        "optional": false,
        "tags": ["dependencies"],
        "is_submodule": false,
        "createdAt": "2017-11-29T04:15:10.332Z",
        "updatedAt": "2017-11-29T04:15:10.332Z"
      },
      "origin_paths": ["package.json"],
      "manual": false,
      "unresolved_locators": ["npm+express$^4.14.0"],
      "is_submodule": false,
      "type": "DETERMINED",
      "depth": 1
    },
    {
      "loc": {
        "fetcher": "npm",
        "package": "express-jwt",
        "revision": "3.4.0"
      },
      "licenses": [
        {
          "id": "52c85ec302e7ac6f34000008",
          "title": "MIT License (Expat)",
          "permissiveness_score": 62,
          "tags": ["Open Source", "OSI-Approved", "Permissive"],
          "shorthand": "mit",
          "RevisionLicense": {
            "id": 654833,
            "licenseId": "52c85ec302e7ac6f34000008",
            "revisionId": "npm+express-jwt$3.4.0",
            "licenseGroupId": 42604,
            "ignored": false,
            "title": "MIT",
            "url": null,
            "text": null,
            "match": "MIT",
            "file_count": 2,
            "manual": false,
            "createdAt": "2017-09-13T05:47:13.909Z",
            "updatedAt": "2017-09-13T05:47:13.909Z",
            "matches": [{ "path": "README.md" }, { "path": "DECLARED_LICENSE" }]
          }
        }
      ],
      "locator": "npm+express-jwt$3.4.0",
      "resolved": true,
      "parent_locator": "npm+express-jwt$3.3.0",
      "builds": [
        {
          "error": null,
          "id": 275803,
          "task": {
            "started": "2017-09-13T05:46:49.574Z",
            "finished": "2017-09-13T05:47:14.123Z",
            "status": "SUCCEEDED",
            "id": 256384
          }
        },
        {
          "error": null,
          "id": 91431,
          "task": {
            "started": "2017-03-09T13:23:57.309Z",
            "finished": "2017-03-09T13:24:07.785Z",
            "status": "SUCCEEDED",
            "id": 75462
          }
        }
      ],
      "project": {
        "locator": "npm+express-jwt",
        "title": "express-jwt",
        "organizationId": null,
        "browsing_access_level": "common",
        "project_scopes": ["compile", "runtime"],
        "url": "https://www.npmjs.com/package/express-jwt"
      },
      "revisionLicenses": [
        {
          "id": 654833,
          "licenseId": "52c85ec302e7ac6f34000008",
          "revisionId": "npm+express-jwt$3.4.0",
          "licenseGroupId": 42604,
          "ignored": false,
          "title": "MIT",
          "url": null,
          "text": null,
          "match": "MIT",
          "file_count": 2,
          "manual": false,
          "createdAt": "2017-09-13T05:47:13.909Z",
          "updatedAt": "2017-09-13T05:47:13.909Z",
          "license": {
            "id": "52c85ec302e7ac6f34000008",
            "title": "MIT License (Expat)",
            "permissiveness_score": 62,
            "tags": ["Open Source", "OSI-Approved", "Permissive"],
            "shorthand": "mit",
            "RevisionLicense": {
              "id": 654833,
              "licenseId": "52c85ec302e7ac6f34000008",
              "revisionId": "npm+express-jwt$3.4.0",
              "licenseGroupId": 42604,
              "ignored": false,
              "title": "MIT",
              "url": null,
              "text": null,
              "match": "MIT",
              "file_count": 2,
              "manual": false,
              "createdAt": "2017-09-13T05:47:13.909Z",
              "updatedAt": "2017-09-13T05:47:13.909Z",
              "matches": [
                { "path": "README.md" },
                { "path": "DECLARED_LICENSE" }
              ]
            }
          },
          "matches": [{ "path": "README.md" }, { "path": "DECLARED_LICENSE" }]
        }
      ],
      "DependencyLock": {
        "organizationId": 90,
        "type": "DETERMINED",
        "root":
          "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78",
        "locator": "npm+express-jwt$3.4.0",
        "unresolved_locators": ["npm+express-jwt$3.4.0"],
        "origin_paths": ["package.json"],
        "depth": 1,
        "manual": false,
        "optional": false,
        "tags": ["dependencies"],
        "is_submodule": false,
        "createdAt": "2017-11-29T04:15:10.332Z",
        "updatedAt": "2017-11-29T04:15:10.332Z"
      },
      "origin_paths": ["package.json"],
      "manual": false,
      "unresolved_locators": ["npm+express-jwt$3.4.0"],
      "is_submodule": false,
      "type": "DETERMINED",
      "depth": 1
    }
  ],
  "issues": []
}
```

A `Revision` represents a `Project` at a specific point in time. This is
specified in a source-dependent way, such as git commit hashes, NPM package
versions, etc.

## Retrieve Revision

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Revision */
}
```

Retrieve a Revision by ID.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId`

### Path parameters

| Parameter     | Type     | Required? | Description                         |
| ------------- | -------- | --------- | ----------------------------------- |
| `:revisionId` | `string` | Y         | The ID of the revision to retrieve. |

## Rebuild Revision

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/rebuild' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Revision */
  }
];
```

Queues another round of dynamic analysis for a revision. This is useful for
resolving problems when builds or analysis rounds are flakey or misconfigured.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/rebuild`

### Path parameters

| Parameter     | Type     | Required? | Description                        |
| ------------- | -------- | --------- | ---------------------------------- |
| `:revisionId` | `string` | Y         | The ID of the revision to rebuild. |

## List Revision Dependencies

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/dependencies' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Revision */
  }
];
```

Loads the dependencies of a `Revision`.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/dependencies`

### Query parameters

| Parameter         | Type      | Required? | Description                                                                                                                                          |
| ----------------- | --------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `include_ignored` | `boolean` | N         | If `true`, includes dependencies with ignored issues.                                                                                                |
| `mediate`         | `boolean` | N         | If `true`, prefers mediated dependencies where possible. Mediated dependencies are those discovered through dynamic (as opposed to static) analysis. |

### Path parameters

| Parameter     | Type     | Required? | Description                                            |
| ------------- | -------- | --------- | ------------------------------------------------------ |
| `:revisionId` | `string` | Y         | The ID of the revision for which to load dependencies. |

## List Revision Dependency Graph Edges

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/edges' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
{
  "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78": [
    "npm+express-jwt$3.4.0",
    "npm+body-parser$1.18.2",
    "npm+mapbox$1.0.0-beta9",
    "npm+express$4.16.2"
  ],
  "npm+jwa$1.1.5": [
    "npm+buffer-equal-constant-time$1.0.1",
    "npm+base64url$2.0.0",
    "npm+safe-buffer$5.0.1",
    "npm+ecdsa-sig-formatter$1.0.9"
  ],
  "npm+finalhandler$1.1.0": [
    "npm+unpipe$1.0.0",
    "npm+statuses$1.3.1",
    "npm+parseurl$1.3.2",
    "npm+on-finished$2.3.0",
    "npm+debug$2.6.9",
    "npm+encodeurl$1.0.1",
    "npm+escape-html$1.0.3"
  ],
  "npm+jws$3.1.4": [
    "npm+jwa$1.1.5",
    "npm+base64url$2.0.0",
    "npm+safe-buffer$5.0.1"
  ],
  "npm+serve-static$1.13.1": [
    "npm+send$0.16.1",
    "npm+encodeurl$1.0.1",
    "npm+parseurl$1.3.2",
    "npm+escape-html$1.0.3"
  ],
  "npm+express$4.16.2": [
    "npm+etag$1.8.1",
    "npm+merge-descriptors$1.0.1",
    "npm+safe-buffer$5.1.1",
    "npm+path-to-regexp$0.1.7",
    "npm+array-flatten$1.1.1",
    "npm+fresh$0.5.2",
    "npm+depd$1.1.1",
    "npm+range-parser$1.2.0",
    "npm+content-disposition$0.5.2",
    "npm+content-type$1.0.4",
    "npm+methods$1.1.2",
    "npm+utils-merge$1.0.1",
    "npm+cookie$0.3.1",
    "npm+escape-html$1.0.3",
    "npm+body-parser$1.18.2",
    "npm+accepts$1.3.4",
    "npm+encodeurl$1.0.1",
    "npm+qs$6.5.1",
    "npm+debug$2.6.9",
    "npm+send$0.16.1",
    "npm+statuses$1.3.1",
    "npm+setprototypeof$1.1.0",
    "npm+parseurl$1.3.2",
    "npm+on-finished$2.3.0",
    "npm+type-is$1.6.15",
    "npm+finalhandler$1.1.0",
    "npm+proxy-addr$2.0.2",
    "npm+cookie-signature$1.0.6",
    "npm+vary$1.1.2",
    "npm+serve-static$1.13.1"
  ],
  "npm+accepts$1.3.4": ["npm+mime-types$2.1.17", "npm+negotiator$0.6.1"],
  "npm+body-parser$1.18.2": [
    "npm+debug$2.6.9",
    "npm+qs$6.5.1",
    "npm+type-is$1.6.15",
    "npm+on-finished$2.3.0",
    "npm+depd$1.1.1",
    "npm+http-errors$1.6.2",
    "npm+iconv-lite$0.4.19",
    "npm+content-type$1.0.4",
    "npm+bytes$3.0.0",
    "npm+raw-body$2.3.2"
  ],
  "npm+raw-body$2.3.2": [
    "npm+unpipe$1.0.0",
    "npm+iconv-lite$0.4.19",
    "npm+http-errors$1.6.2",
    "npm+bytes$3.0.0"
  ],
  "npm+express-jwt$3.4.0": [
    "npm+lodash.set$4.3.2",
    "npm+jsonwebtoken$5.7.0",
    "npm+express-unless$0.3.1",
    "npm+async$1.5.2"
  ],
  "npm+on-finished$2.3.0": ["npm+ee-first$1.1.1"],
  "npm+http-errors$1.6.2": [
    "npm+setprototypeof$1.0.3",
    "npm+statuses$1.3.1",
    "npm+inherits$2.0.3",
    "npm+depd$1.1.1"
  ],
  "npm+send$0.16.1": [
    "npm+etag$1.8.1",
    "npm+escape-html$1.0.3",
    "npm+fresh$0.5.2",
    "npm+http-errors$1.6.2",
    "npm+depd$1.1.1",
    "npm+range-parser$1.2.0",
    "npm+mime$1.4.1",
    "npm+debug$2.6.9",
    "npm+destroy$1.0.4",
    "npm+encodeurl$1.0.1",
    "npm+ms$2.0.0",
    "npm+on-finished$2.3.0",
    "npm+statuses$1.3.1"
  ],
  "npm+jsonwebtoken$5.7.0": [
    "npm+xtend$4.0.1",
    "npm+jws$3.1.4",
    "npm+ms$0.7.2"
  ],
  "npm+type-is$1.6.15": ["npm+media-typer$0.3.0", "npm+mime-types$2.1.15"],
  "npm+proxy-addr$2.0.2": ["npm+ipaddr.js$1.5.2", "npm+forwarded$0.1.2"],
  "npm+mapbox$1.0.0-beta9": ["npm+rest$2.0.0", "npm+es6-promise$4.1.1"],
  "npm+ecdsa-sig-formatter$1.0.9": [
    "npm+safe-buffer$5.1.1",
    "npm+base64url$2.0.0"
  ],
  "npm+mime-types$2.1.15": ["npm+mime-db$1.27.0"],
  "npm+debug$2.6.9": ["npm+ms$2.0.0"],
  "npm+mime-types$2.1.17": ["npm+mime-db$1.30.0"]
}
```

Loads the dependency graph a `Revision` as a directed adjacency list.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/edges`

### Path parameters

| Parameter     | Type     | Required? | Description                                                    |
| ------------- | -------- | --------- | -------------------------------------------------------------- |
| `:revisionId` | `string` | Y         | The ID of the revision for which to load the dependency graph. |

## List Revision Dependency Paths

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/paths?locator=npm%2Bbody-parser%241.18.2' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
[[["npm+body-parser$1.18.2"], ["npm+express$4.16.2", "npm+body-parser$1.18.2"]]]
```

Loads the paths from a project to a specified target dependency.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/paths`

### Query parameters

| Parameter | Type     | Required? | Description                                  |
| --------- | -------- | --------- | -------------------------------------------- |
| `locator` | `string` | Y         | The ID of the path's destination dependency. |

### Path parameters

| Parameter     | Type     | Required? | Description                                                       |
| ------------- | -------- | --------- | ----------------------------------------------------------------- |
| `:revisionId` | `string` | Y         | The ID of the source revision for which to load dependency paths. |

## List Revision Licenses

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/licenses' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
[
  {
    "id": "52c85ec302e7ac6f34000008",
    "title": "MIT License (Expat)",
    "shorthand": "mit",
    "permissiveness_score": 62,
    "depths": [
      2,
      2,
      2,
      1,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      3,
      3,
      2,
      2,
      2,
      2,
      1,
      1,
      2,
      2,
      3,
      2,
      2,
      2,
      3,
      3,
      2,
      3,
      2,
      3,
      2,
      2,
      3,
      3,
      3,
      3,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      2,
      3,
      2,
      2,
      3,
      0
    ],
    "matches": [
      "npm+accepts$1.3.4",
      "npm+array-flatten$1.1.1",
      "npm+async$1.5.2",
      "npm+body-parser$1.18.2",
      "npm+bytes$3.0.0",
      "npm+content-disposition$0.5.2",
      "npm+content-type$1.0.4",
      "npm+cookie$0.3.1",
      "npm+cookie-signature$1.0.6",
      "npm+debug$2.6.9",
      "npm+depd$1.1.1",
      "npm+destroy$1.0.4",
      "npm+ee-first$1.1.1",
      "npm+encodeurl$1.0.1",
      "npm+es6-promise$4.1.1",
      "npm+escape-html$1.0.3",
      "npm+etag$1.8.1",
      "npm+express$4.16.2",
      "npm+express-jwt$3.4.0",
      "npm+express-unless$0.3.1",
      "npm+finalhandler$1.1.0",
      "npm+forwarded$0.1.2",
      "npm+fresh$0.5.2",
      "npm+http-errors$1.6.2",
      "npm+iconv-lite$0.4.19",
      "npm+inherits$2.0.3",
      "npm+ipaddr.js$1.5.2",
      "npm+jsonwebtoken$5.7.0",
      "npm+jws$3.1.4",
      "npm+lodash.set$4.3.2",
      "npm+media-typer$0.3.0",
      "npm+merge-descriptors$1.0.1",
      "npm+methods$1.1.2",
      "npm+mime$1.4.1",
      "npm+mime-types$2.1.17",
      "npm+ms$2.0.0",
      "npm+negotiator$0.6.1",
      "npm+on-finished$2.3.0",
      "npm+parseurl$1.3.2",
      "npm+path-to-regexp$0.1.7",
      "npm+proxy-addr$2.0.2",
      "npm+range-parser$1.2.0",
      "npm+raw-body$2.3.2",
      "npm+rest$2.0.0",
      "npm+safe-buffer$5.1.1",
      "npm+send$0.16.1",
      "npm+serve-static$1.13.1",
      "npm+setprototypeof$1.1.0",
      "npm+statuses$1.3.1",
      "npm+type-is$1.6.15",
      "npm+unpipe$1.0.0",
      "npm+utils-merge$1.0.1",
      "npm+vary$1.1.2",
      "npm+xtend$4.0.1",
      "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78"
    ]
  },
  {
    "id": "52e58b3e81519e003b00009f",
    "title": " ISC License",
    "shorthand": "isc",
    "permissiveness_score": 50,
    "depths": [3, 2, 0],
    "matches": [
      "npm+inherits$2.0.3",
      "npm+setprototypeof$1.1.0",
      "git+github.com/ilikebits/datasets-api-gateway$61a994bba02325694e93ad697419e0acab5eed78"
    ]
  },
  {
    "id": "52c869359f62d56435000055",
    "title": "BSD 3-Clause License (Revised)",
    "shorthand": "bsd3",
    "permissiveness_score": 50,
    "depths": [2],
    "matches": ["npm+qs$6.5.1"]
  }
]
```

Loads the licenses of a project and the dependencies from which those licenses
are brought in.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/licenses`

### Path parameters

| Parameter     | Type     | Required? | Description                                        |
| ------------- | -------- | --------- | -------------------------------------------------- |
| `:revisionId` | `string` | Y         | The ID of the revision for which to load licenses. |

## List Revision Obligations

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/todos' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
{
  "CANNOT": {},
  "MUST": {
    "Include Copyright": { "count": 56 },
    "Include License": { "count": 56 }
  }
}
```

Loads the obligations of a project from the licenses applied to it.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/todos`

### Query parameters

| Parameter | Type       | Required? | Description                                                                |
| --------- | ---------- | --------- | -------------------------------------------------------------------------- |
| `role`    | `string`   | N         | If `CANNOT`, `CAN`, or `MUST`, filters obligations by type.                |
| `counts`  | `booleans` | N         | If `true`, includes counts for how many times an obligation is brought in. |

### Path parameters

| Parameter     | Type     | Required? | Description                                                  |
| ------------- | -------- | --------- | ------------------------------------------------------------ |
| `:revisionId` | `string` | Y         | The ID of the source revision for which to load obligations. |

## Get Revision Attribution Report

```bash
http 'http://api.fossa.io/api/revisions/git%2Bgithub.com%2Filikebits%2Fdatasets-api-gateway%2461a994bba02325694e93ad697419e0acab5eed78/attribution' 'Authorization: token 123456789'
```

> This endpoint returns an HTML report.

Generates an HTML report for this project, listing its deep dependencies,
licenses, obligations, etc.

### HTTP Request

`GET https://api.fossa.io/api/revisions/:revisionId/attribution`

### Query parameters

| Parameter                   | Type      | Required? | Description                                                                            |
| --------------------------- | --------- | --------- | -------------------------------------------------------------------------------------- |
| `format`                    | `string`  | N         | One of `HTML`, `PDF`, or `MD`. Selects the report output file format.                  |
| `includeLicenseScan`        | `boolean` | N         | If `true`, includes license scan section.                                              |
| `includeLicenseList`        | `boolean` | N         | If `true`, includes license list section.                                              |
| `includeDirectDependencies` | `boolean` | N         | If `true`, includes direct dependencies section.                                       |
| `includeDeepDependencies`   | `boolean` | N         | If `true`, includes deep dependencies section.                                         |
| `diff`                      | `boolean` | N         | If `true`, computes attribution diff between two different revisions for this project. |
| `src`                       | `string`  | N         | The `revisionId` of the source revision for attribution diffing.                       |
| `dest`                      | `string`  | N         | The `revisionId` of the target revision for attribution diffing.                       |

### Path parameters

| Parameter     | Type     | Required? | Description                                                     |
| ------------- | -------- | --------- | --------------------------------------------------------------- |
| `:revisionId` | `string` | Y         | The ID of the source revision for which to generate the report. |
