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

Teams of users are grouped together in Organizations. Users can only belong to
one organization at a time.

## Retrieve Organization

```bash
http 'http://api.fossa.io/api/organization/90' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Organization */
}
```

Retrieve an Organization by ID.

### HTTP Request

`GET https://api.fossa.io/api/organization/:organizationId`

### Path Parameters

| Parameter         | Type     | Required? | Description                             |
| ----------------- | -------- | --------- | --------------------------------------- |
| `:organizationId` | `string` | Y         | The ID of the organization to retrieve. |

<aside class="notice">
You can retrieve the ID of your organization by examining your <code>User</code> model. See <a href="#list-users">List Users</a> for more details.
</aside>

## Invite User

## List Invoices

## Get Organization Report

## Scan Projects

## Send Badge PRs to Projects

## List Issues

## Search Components
