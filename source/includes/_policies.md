# Policies

> An example Policy:

```json
{
  "createdAt": "2017-02-23T02:04:11.651Z",
  "default_action": null,
  "description":
    "Policy template for when all code and resources are linked & bundled into a single binary distribution (i.e. most mobile apps, embedded systems, or compiled binary releases).",
  "id": 253,
  "organizationId": 90,
  "rules": [
    {
      "action": "FLAG",
      "createdAt": "2017-02-23T02:04:11.932Z",
      "depthCondition": null,
      "id": 7998,
      "license": {
        "id": "53a218ac763c784c60000037",
        "title": "Mozilla Public License 1.1 (MPL-1.1)"
      },
      "linkingCondition": null,
      "nameCondition": null,
      "notes":
        "Safe if code isn’t modified and notice requirements are followed. Otherwise, you must state and disclose the source code of modifications/derivative works.",
      "policyId": 253,
      "project": null,
      "target": "license",
      "targetId": "53a218ac763c784c60000037",
      "updatedAt": "2017-02-23T02:04:11.932Z"
    },
    {
      "action": "APPROVE",
      "createdAt": "2017-02-23T02:04:11.933Z",
      "depthCondition": null,
      "id": 8001,
      "license": {
        "id": "559ec2ca47cdaa075e000230",
        "title": "Apache License 1.1 (Apache-1.1)"
      },
      "linkingCondition": null,
      "nameCondition": null,
      "notes":
        "Permissive license which is perfectly safe to use provided proper attribution is given and retained.",
      "policyId": 253,
      "project": null,
      "target": "license",
      "targetId": "559ec2ca47cdaa075e000230",
      "updatedAt": "2017-02-23T02:04:11.933Z"
    }
  ],
  "title": "Single-Binary Distribution",
  "updatedAt": "2017-02-23T02:04:11.651Z"
}
```

Policies are sets of `Rule`s that can be attached to an `Organization` or `Project`
to configure how FOSSA handles the components of projects.

To modify the rules in a policy, use the [`Rule`](#rules) operations.

## Create Policy

```bash
http --form POST 'http://api.fossa.io/api/policies' title='test policy' description='test description' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// The newly created Policy.
{
  "id": 4679,
  "title": "test policy",
  "description": "test description",
  "organizationId": 90,
  "updatedAt": "2017-12-04T09:45:20.232Z",
  "createdAt": "2017-12-04T09:45:20.232Z",
  "default_action": null
}
```

Creates new Policies.

<aside class="notice">
To create Policies from templates, use the special <code>template</code> key. Valid values include <code>single_binary</code>, <code>hosted_service</code>, and <code>standard_bundle</code>.
</aside>

### HTTP Request

`POST http://api.fossa.io/api/policies`

### Query parameters

| Parameter  | Type           | Required? | Description                                                                        |
| ---------- | -------------- | --------- | ---------------------------------------------------------------------------------- |
| `${field}` | `keyof Policy` | N         | Sets the field's value. If not specified, fields will default to their zero value. |

## List Policies

```bash
http 'http://api.fossa.io/api/policies' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Policy 1 elided */
  },
  {
    /* Policy 2 elided */
  },
  {
    /* Policy 3 elided */
  }
  // ...
];
```

Lists all policies.

This endpoint supports the standard filtering, search, sorting, and pagination
operators.

### HTTP Request

`GET http://api.fossa.io/api/policies`

### Query parameters

| Parameter  | Type           | Required? | Description                                                                                                                                                                                          |
| ---------- | -------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `${field}` | `keyof Policy` | N         | Filter results to only include rows where `${field}` is set to the value passed as `${field}`. For example, to only include rows where `default_action` is `APPROVE`, pass `default_action=APPROVE`. |
| `q`        | `any`          | N         | Perform a substring search for the value across all fields.                                                                                                                                          |
| `sort`     | `keyof Policy` | N         | Sort by the specified field name. Prefix with `-` to sort by descending order. For example, to sort in descending order by `createdAt`, pass `sort=-createdAt`.                                      |
| `count`    | `int`          | N         | Paginate response to include only `count` rows per response.                                                                                                                                         |
| `page`     | `int`          | N         | Set the pagination page index.                                                                                                                                                                       |
| `offset`   | `int`          | N         | Begin pagination at the specified row offset.                                                                                                                                                        |

## Retrieve Policy

```bash
http 'http://api.fossa.io/api/policies/4679' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Policy */
}
```

Retrieve a Policy by ID.

### HTTP Request

`GET https://api.fossa.io/api/policies/:policyId`

### Path parameters

| Parameter   | Type     | Required? | Description                       |
| ----------- | -------- | --------- | --------------------------------- |
| `:policyId` | `number` | Y         | The ID of the policy to retrieve. |

## Update Policy

```bash
http --form PUT 'http://api.fossa.io/api/policies/4679' default_action=APPROVE 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// The updated Policy.
{
  "id": 4679,
  "title": "test policy",
  "description": "test description",
  "organizationId": 90,
  "updatedAt": "2017-12-04T09:45:20.232Z",
  "createdAt": "2017-12-04T09:45:20.232Z",
  "default_action": "APPROVE"
}
```

Updates Policies.

### HTTP Request

`PUT http://api.fossa.io/api/policies/:policyId`

### Path parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `:policyId` | `number` | Y         | The ID of the policy to update. |

### Query parameters

| Parameter  | Type           | Required? | Description                                                             |
| ---------- | -------------- | --------- | ----------------------------------------------------------------------- |
| `${field}` | `keyof Policy` | N         | Sets the field's value. If not specified, fields will remain unchanged. |

## Delete Policy

```bash
http DELETE 'http://api.fossa.io/api/policies/4679' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```json
{}
```

Delete a Policy by ID.

### HTTP Request

`DELETE https://api.fossa.io/api/policies/:policyId`

### Path parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `:policyId` | `number` | Y         | The ID of the policy to delete. |
