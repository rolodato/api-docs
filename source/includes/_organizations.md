# Organizations

> An example Organization:

```json
{
  "accessRequests": [],
  "access_level": "premium",
  "contributor_count": 0,
  "contributors_updated": "2017-12-04T07:43:58.573Z",
  "created": "2017-02-23T02:04:11.000Z",
  "createdAt": "2017-02-23T02:04:11.628Z",
  "custom_billing": true,
  "custom_contributor_count": null,
  "data_update_interval": 14400000,
  "defaultPolicyId": 251,
  "demo": false,
  "dependency_signatures": null,
  "email": null,
  "fetcher_config": {
    "mvn": {
      "repositories": [
        {
          "id": "central",
          "url": "https://repo1.maven.org/maven2"
        },
        {
          "id": "twitter",
          "url": "http://maven.twttr.com/"
        },
        {
          "id": "redhat",
          "url": "https://maven.repository.redhat.com/ga/"
        },
        {
          "id": "spring",
          "url": "https://repo.springsource.org"
        }
      ]
    }
  },
  "id": 90,
  "image": null,
  "jira": {
    "base_url": null,
    "credentials": {},
    "enabled": false,
    "resolved_statuses": ["Done", "Resolved", "Closed"]
  },
  "notification_default_email_build_users": [],
  "notification_default_email_scan_users": [],
  "notification_default_enabled": false,
  "notification_default_slack_build": false,
  "notification_default_slack_scan": false,
  "podSources": [],
  "policies": [
    {
      "createdAt": "2017-02-23T02:04:11.644Z",
      "default_action": null,
      "description":
        "Starter policy template for most types of apps and software bundles.",
      "id": 251,
      "organizationId": 90,
      "title": "Standard Bundle Distribution",
      "updatedAt": "2017-02-23T02:04:11.644Z"
    },
    {
      "createdAt": "2017-02-23T02:04:11.656Z",
      "default_action": null,
      "description":
        "Policy template for when all application code & libraries stand behind a server (i.e. most SaaS, websites, API services).",
      "id": 252,
      "organizationId": 90,
      "title": "Website/Hosted Service",
      "updatedAt": "2017-02-23T02:04:11.656Z"
    },
    {
      "createdAt": "2017-02-23T02:04:11.651Z",
      "default_action": null,
      "description":
        "Policy template for when all code and resources are linked & bundled into a single binary distribution (i.e. most mobile apps, embedded systems, or compiled binary releases).",
      "id": 253,
      "organizationId": 90,
      "title": "Single-Binary Distribution",
      "updatedAt": "2017-02-23T02:04:11.651Z"
    }
  ],
  "project_default_attribution_access_depth": 3,
  "project_default_attribution_access_level": "common",
  "project_default_attribution_issue_enabled": false,
  "project_default_browsing_access_depth": 3,
  "project_default_browsing_access_level": "common",
  "project_default_issue_tracker_id": null,
  "project_default_issue_tracker_type": null,
  "project_default_issue_tracker_url": null,
  "project_default_policies_access_depth": 3,
  "project_default_policies_access_level": "common",
  "project_default_policies_approve_multilicense": true,
  "project_default_require_mediated_dependencies": false,
  "project_default_scan_mediated_dependencies": false,
  "project_default_settings_enabled": false,
  "project_default_unlicensed_access_depth": 3,
  "project_default_unlicensed_access_level": "full",
  "project_default_unlicensed_newer_flag": true,
  "repo_limit": null,
  "revisionsUpdatedAt": null,
  "size": null,
  "slack": [],
  "stripe_subscription": null,
  "super": true,
  "title": "test-abe",
  "updateHook_default_scheduled_enabled": false,
  "updateHook_default_scheduled_interval": null,
  "updateHook_default_scheduled_interval_length": null,
  "updateHook_default_scheduled_interval_time": null,
  "updatedAt": "2017-12-04T07:43:58.574Z",
  "users": [
    {
      "email": "test@fossa.io",
      "id": 1525,
      "username": "test-user"
    }
  ]
}
```

Teams of `User`s are grouped together in an `Organization`. A `User` can only
belong to one organization at a time.

## Retrieve Organization

```bash
http 'http://api.fossa.io/api/organizations/90' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Organization */
}
```

Retrieve an Organization by ID.

### HTTP Request

`GET https://api.fossa.io/api/organizations/:organizationId`

### Path parameters

| Parameter         | Type     | Required? | Description                             |
| ----------------- | -------- | --------- | --------------------------------------- |
| `:organizationId` | `number` | Y         | The ID of the organization to retrieve. |

<aside class="notice">
You can retrieve the ID of your organization by examining your <code>User</code> model. See <a href="#list-users">List Users</a> for more details.
</aside>

## Invite User

```bash
http --form POST 'http://api.fossa.io/api/organizations/90/invite' emails[]=email1@example.com emails[]=email2@example.com 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
null
```

Invite users to an organization by email.

### HTTP Request

`POST https://api.fossa.io/api/organizations/:organizationId/invite?emails[]=test@example.com`

### Path parameters

| Parameter         | Type     | Required? | Description                                    |
| ----------------- | -------- | --------- | ---------------------------------------------- |
| `:organizationId` | `number` | Y         | The ID of the organization to invite users to. |

### Query parameters

| Parameter | Type       | Required? | Description           |
| --------- | ---------- | --------- | --------------------- |
| `emails`  | `string[]` | Y         | The emails to invite. |

## List Invoices

```bash
http 'http://api.fossa.io/api/organization/invoices' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Stripe invoices */
  }
];
```

Lists your `Organization`'s invoices.

<aside class="notice">
If your organization uses a custom billing scheme, or you're using an on-premises installation, this API may return <code>"Billing is disabled for this account"</code> to you. This is a known limitation, and we're working on resolving it.
</aside>

### HTTP Request

`GET https://api.fossa.io/api/organization/invoices`

## List Issues

```bash
http 'http://api.fossa.io/api/organization/issues' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    id: 126203,
    type: "unlicensed_dependency",
    revisionId: "mvn+org.apache.lucene:lucene-core$4.6.1",
    projectId: null,
    organizationId: 90,
    ruleId: null,
    licenseId: null,
    resolved: false,
    resolvedAt: null,
    issue_tracker_id: null,
    issue_tracker_type: "jira",
    notes: null,
    createdAt: "2017-11-06T22:34:46.619Z",
    updatedAt: "2017-11-06T22:34:46.619Z",
    parents: [
      {
        title: "Demo-Project",
        description: "",
        locator: "git+github.com/fossas/Demo-Project",
        url: "https://github.com/fossas/Demo-Project",
        public: true,
        IssueProject: { resolved: false }
      }
    ],
    resolutions: [],
    revision: {
      loc: {
        fetcher: "mvn",
        package: "org.apache.lucene:lucene-core",
        revision: "4.6.1"
      },
      licenses: [],
      projectId: "mvn+org.apache.lucene:lucene-core",
      locator: "mvn+org.apache.lucene:lucene-core$4.6.1",
      resolved: true,
      url: null,
      project: {
        title: "Lucene Core",
        description: "Apache Lucene Java Core",
        locator: "mvn+org.apache.lucene:lucene-core",
        url: null,
        public: true
      }
    },
    revisions: [ ... ] /* Revision objects of where issues were found */
  },
  {
    /* More issues */
  }
];
```

Returns a list of all issues for all projects in the organization.

### Response Parameters

| Parameter  | Type            | Description                                                                                                                                                                      |
| ---------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` | `int` | Issue ID                                                                                                                      |
| `type` | `string` | Issue type, can be one of `unlicensed_dependency`, `policy_confict`, `policy_flag`, `missing_attribution` or `vulnerability` |
| `organizationId` | `int` | Organization this issue belongs to |
| `ruleId` | `int` | Target Policy rule this issue references, defined only if issue is of type `policy_conflict` or `policy_flag`  |
| `projectId` | `string` | Target Project this issue references, defined only if issue is of type `missing_attribution`  |
| `revision` | `Revision` | Target Revision this issue references |
| `licenseId` | `string` | License this issue references, defined only if issue is of type `policy_conflict` or `policy_flag`  |
| `resolved` | `boolean` | `true` if this issue has been previously resolved in the FOSSA UI or an issue tracker |
| `resolvedAt` | `Date` | Timestamp of when the issue was resolved |
| `issue_tracker_id` | `string` | External ID in an issue tracker of where this issue was exported to |
| `issue_tracker_type` | `string` | Can be one of `jira` or `github` |
| `notes` | `string` | Any notes attached to issue during resolution in UI or issue tracker |
| `createdAt` | `Date` | Timestamp of when issue was created |
| `updatedAt` | `Date` | Timestamp of when issue was last updated |
| `parents` | `Project[]` | A list of projects this issue was found in |
| `revisions` | `Revision[]` | A list of revisions this issue was found in |

### HTTP Request

`GET https://api.fossa.io/api/organization/issues`

## Get Summary

```bash
http 'http://api.fossa.io/api/organization/summary' 'Authorization: token 123456789'
```

> This endpoint returns an HTML report.

Retrieves your `Organization`'s summary report. This report is an HTML page
which can be loaded in an `<iframe>` for display.

### HTTP Request

`GET https://api.fossa.io/api/organization/summary`

## Get Statistics

```bash
http 'http://api.fossa.io/api/organization/stats' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
{
  "projects": 3,
  "unsetup_projects": 0,
  "contributors": 0,
  "total_components": 198,
  "flagged_components": null,
  "revision_cache_count": 3
}
```

Returns interesting summary statistics for the organization.

### HTTP Request

`GET https://api.fossa.io/api/organization/stats`

## Search Components

```bash
http 'http://api.fossa.io/api/organization/search' 'Authorization: token 123456789'
```

> Returns data in shape of:

```json
[
  {
    "loc": { "fetcher": "pip", "package": "Pillow", "revision": "1.7.8" },
    "licenses": [],
    "locator": "pip+Pillow$1.7.8",
    "dependencyRoots": [
      {
        "loc": {
          "fetcher": "git",
          "package": "github.com/dropbox/hackpad",
          "revision": "da0b3dbc3525cd3094c52975d11817ab30087ac9"
        },
        "licenses": [],
        "locator":
          "git+github.com/dropbox/hackpad$da0b3dbc3525cd3094c52975d11817ab30087ac9",
        "project": {
          "locator": "git+github.com/dropbox/hackpad",
          "organizationId": 25,
          "default_branch": "master",
          "title": "hackpad"
        },
        "DependencyLock": {
          "organizationId": 25,
          "type": "DETERMINED",
          "root":
            "git+github.com/dropbox/hackpad$da0b3dbc3525cd3094c52975d11817ab30087ac9",
          "locator": "pip+Pillow$1.7.8",
          "unresolved_locators": ["pip+pillow$==1.7.8"],
          "origin_paths": ["contrib/glue/setup.py"],
          "depth": 1,
          "manual": false,
          "optional": false,
          "tags": [null],
          "is_submodule": false,
          "createdAt": "2017-09-07T22:12:00.704Z",
          "updatedAt": "2017-09-07T22:12:00.704Z"
        }
      }
    ],
    "project": {
      "title": "Pillow",
      "description":
        "Pillow\n======\n\nPython Imaging Library (Fork)\n-----------------------------\n\nPillow is the friendly PIL fork by `Alex Clark and Contributors <https://github.com/python-pillow/Pillow/graphs/contributors>`_. PIL is the Python Imaging Library by Fredrik Lundh and Contributors.\n\n.. start-badges\n\n.. list-table::\n    :stub-columns: 1\n\n    * - docs\n      - |docs|\n    * - tests\n      - | |linux| |macos| |windows| |coverage| |health|\n    * - package\n      - |zenodo| |version| |downloads|\n\n.. |docs| image:: https://readthedocs.org/projects/pillow/badge/?version=latest\n   :target: https://pillow.readthedocs.io/?badge=latest\n   :alt: Documentation Status\n\n.. |linux| image:: https://img.shields.io/travis/python-pillow/Pillow/master.svg?label=Linux%20build\n   :target: https://travis-ci.org/python-pillow/Pillow\n   :alt: Travis CI build status (Linux)\n\n.. |macos| image:: https://img.shields.io/travis/python-pillow/pillow-wheels/latest.svg?label=macOS%20build\n   :target: https://travis-ci.org/python-pillow/pillow-wheels\n   :alt: Travis CI build status (macOS)\n\n.. |windows| image:: https://img.shields.io/appveyor/ci/python-pillow/Pillow/master.svg?label=Windows%20build\n   :target: https://ci.appveyor.com/project/python-pillow/Pillow\n   :alt: AppVeyor CI build status (Windows)\n\n.. |coverage| image:: https://coveralls.io/repos/python-pillow/Pillow/badge.svg?branch=master&service=github\n   :target: https://coveralls.io/github/python-pillow/Pillow?branch=master\n   :alt: Code coverage\n\n.. |health| image:: https://landscape.io/github/python-pillow/Pillow/master/landscape.svg\n   :target: https://landscape.io/github/python-pillow/Pillow/master\n   :alt: Code health\n\n.. |zenodo| image:: https://zenodo.org/badge/17549/python-pillow/Pillow.svg\n   :target: https://zenodo.org/badge/latestdoi/17549/python-pillow/Pillow\n\n.. |version| image:: https://img.shields.io/pypi/v/pillow.svg\n   :target: https://pypi.python.org/pypi/Pillow/\n   :alt: Latest PyPI version\n\n.. |downloads| image:: https://img.shields.io/pypi/dm/pillow.svg\n   :target: https://pypi.python.org/pypi/Pillow/\n   :alt: Number of PyPI downloads\n\n.. end-badges\n\n\n\nMore Information\n----------------\n\n- `Documentation <https://pillow.readthedocs.io/>`_\n\n  - `Installation <https://pillow.readthedocs.io/en/latest/installation.html>`_\n  - `Handbook <https://pillow.readthedocs.io/en/latest/handbook/index.html>`_\n\n- `Contribute <https://github.com/python-pillow/Pillow/blob/master/.github/CONTRIBUTING.md>`_\n\n  - `Issues <https://github.com/python-pillow/Pillow/issues>`_\n  - `Pull requests <https://github.com/python-pillow/Pillow/pulls>`_\n\n- `Changelog <https://github.com/python-pillow/Pillow/blob/master/CHANGES.rst>`_\n\n  - `Pre-fork <https://github.com/python-pillow/Pillow/blob/master/CHANGES.rst#pre-fork>`_",
      "url": "http://python-pillow.org",
      "locator": "pip+Pillow"
    },
    "issueTargets": [
      {
        "id": 96004,
        "type": "unlicensed_dependency",
        "ruleId": null,
        "licenseId": null,
        "IssueRevisions": [
          {
            "issueId": 96004,
            "revisionId":
              "git+github.com/dropbox/hackpad$da0b3dbc3525cd3094c52975d11817ab30087ac9",
            "createdAt": "2017-07-21T08:16:28.938Z",
            "updatedAt": "2017-07-21T08:16:28.938Z"
          }
        ]
      }
    ]
  }
]
```

Searches through all issues in an organization. This endpoint can filter by the
whether an issue has been resolved.

### HTTP Request

`GET https://api.fossa.io/api/organization/search`

### Query parameters

| Parameter | Type     | Required? | Description                                                                         |
| --------- | -------- | --------- | ----------------------------------------------------------------------------------- |
| `q`       | `string` | N         | If set, searches only for issues on components whose names contain the query.       |
| `filter`  | `string` | N         | If set, filters the returned issues. Can be `resolvedIssues` or `unresolvedIssues`. |

## Scan Components

```bash
http 'http://api.fossa.io/api/organization/scan' 'Authorization: token 123456789'
```

> Returns the number of scanned projects.

```json
20
```

Queues all organization projects to be scanned for issues. This is useful if a
large number of projects have been updated recently, or if your organization has
adopted a new policy.

### HTTP Request

`GET https://api.fossa.io/api/organization/scan`
