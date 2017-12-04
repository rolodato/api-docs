# Rules

> An example Rule:

```json
{
  "action": "FLAG",
  "createdAt": "2016-01-08T01:14:52.166Z",
  "depthCondition": null,
  "id": 108,
  "license": {
    "id": "52c86a2d9f62d5643500007f",
    "shorthand": "cddl",
    "title": "Common Development and Distribution License (CDDL-1.0)"
  },
  "linkingCondition": null,
  "nameCondition": null,
  "notes":
    "Safe if code isn’t modified and notice requirements are followed. Otherwise, you must state and disclose the source code of modifications/derivative works.",
  "policyId": 4,
  "project": null,
  "target": "license",
  "targetId": "52c86a2d9f62d5643500007f",
  "updatedAt": "2016-01-08T01:14:52.166Z"
}
```

A rule describes the actions that FOSSA takes to handle a particular component
when certain conditions are met. Many rules make up a Policy, and each project
and organization may have its own Policy to configure how FOSSA handles
different components.

## Create Rule

## List Rules

```bash
http 'http://api.fossa.io/api/rules' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Rule 1 elided */
  },
  {
    /* Rule 2 elided */
  },
  {
    /* Rule 3 elided */
  }
  // ...
];
```

Lists all rules.

This endpoint supports the standard filtering, search, sorting, and pagination
operators.

### HTTP Request

`GET http://api.fossa.io/api/rules`

### Query parameters

| Parameter  | Type         | Required? | Description                                                                                                                                                                    |
| ---------- | ------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `${field}` | `keyof Rule` | N         | Filter results to only include rows where `${field}` is set to the value passed as `${field}`. For example, to only include rows where `action` is `FLAG`, pass `action=FLAG`. |
| `q`        | `any`        | N         | Perform a substring search for the value across all fields.                                                                                                                    |
| `sort`     | `keyof Rule` | N         | Sort by the specified field name. Prefix with `-` to sort by descending order. For example, to sort in descending order by `createdAt`, pass `sort=-createdAt`.                |
| `count`    | `int`        | N         | Paginate response to include only `count` rows per response.                                                                                                                   |
| `page`     | `int`        | N         | Set the pagination page index.                                                                                                                                                 |
| `offset`   | `int`        | N         | Begin pagination at the specified row offset.                                                                                                                                  |

## Retrieve Rule

## Update Rule

## Delete Rule
