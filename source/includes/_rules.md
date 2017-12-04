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
when certain conditions are met. Many rules make up a `Policy`, and each `Project`
and `Organization` may have its own `Policy` to configure how FOSSA handles
different components.

## Create Rule

```bash
http --form POST 'http://api.fossa.io/api/rules' action=FLAG target=license policyId=252 targetId=532b52275d0187c662000038 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// The newly created Rule.
{
  "id": 157406,
  "action": "FLAG",
  "target": "license",
  "targetId": "532b52275d0187c662000038",
  "policyId": 252,
  "notes": "",
  "updatedAt": "2017-12-04T09: 22: 27.660Z",
  "createdAt": "2017-12-04T09: 22: 27.660Z",
  "linkingCondition": null,
  "nameCondition": null,
  "depthCondition": null,
  "license": {
    "id": "532b52275d0187c662000038",
    "title": "Aladdin Free Public License",
    "shorthand": "aladdin"
  },
  "project": null
}
```

Creates new Rules.

### HTTP Request

`POST http://api.fossa.io/api/rules`

### Query parameters

| Parameter  | Type         | Required? | Description                                                                        |
| ---------- | ------------ | --------- | ---------------------------------------------------------------------------------- |
| `${field}` | `keyof Rule` | N         | Sets the field's value. If not specified, fields will default to their zero value. |

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

```bash
http 'http://api.fossa.io/api/rules/157406' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{
  /* Rule */
}
```

Retrieve a Rule by ID.

### HTTP Request

`GET https://api.fossa.io/api/rules/:ruleId`

### Path parameters

| Parameter | Type     | Required? | Description                     |
| --------- | -------- | --------- | ------------------------------- |
| `:ruleId` | `number` | Y         | The ID of the rule to retrieve. |

## Update Rule

```bash
http --form PUT 'http://api.fossa.io/api/rules/157406' action=APPROVE 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// The updated Rule.
{
  "id": 157406,
  "action": "APPROVE",
  "target": "license",
  "targetId": "532b52275d0187c662000038",
  "policyId": 252,
  "notes": "",
  "updatedAt": "2017-12-04T09: 22: 27.660Z",
  "createdAt": "2017-12-04T09: 22: 27.660Z",
  "linkingCondition": null,
  "nameCondition": null,
  "depthCondition": null,
  "license": {
    "id": "532b52275d0187c662000038",
    "title": "Aladdin Free Public License",
    "shorthand": "aladdin"
  },
  "project": null
}
```

Updates Rules.

### HTTP Request

`PUT http://api.fossa.io/api/rules/:ruleId`

### Path parameters

| Parameter | Type     | Required? | Description                   |
| --------- | -------- | --------- | ----------------------------- |
| `:ruleId` | `number` | Y         | The ID of the rule to update. |

### Query parameters

| Parameter  | Type         | Required? | Description                                                             |
| ---------- | ------------ | --------- | ----------------------------------------------------------------------- |
| `${field}` | `keyof Rule` | N         | Sets the field's value. If not specified, fields will remain unchanged. |

## Delete Rule

```bash
http DELETE 'http://api.fossa.io/api/rules/157406' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
{}
```

Delete a Rule by ID.

### HTTP Request

`DELETE https://api.fossa.io/api/rules/:ruleId`

### Path parameters

| Parameter | Type     | Required? | Description                   |
| --------- | -------- | --------- | ----------------------------- |
| `:ruleId` | `number` | Y         | The ID of the rule to delete. |
