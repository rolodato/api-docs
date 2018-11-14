# Teams

> An example Team:

```json
{
    "id": 1,
    "organizationId": 1,
    "name": "Awesome Team That's Really Long",
    "autoAddUsers": false,
    "autoAddProjects": false,
    "createdAt": "2018-09-25T18:04:15.000Z",
    "updatedAt": "2018-10-09T19:18:44.000Z",
    "teamUsers": [
        {
            "userId": 2
        }
    ],
    "teamProjects": [
        {
            "projectId": "git+github.com/lackstein/cryptopals"
        }
    ]
}
```

Teams are a way of organizing projects and giving users access to a group of projects.

## Create Team

```bash
http --form POST 'https://app.fossa.io/api/teams' name='new team' autoAddUsers='true' autoAddProjects='false' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// The newly created Team.
{
    "createdAt": "2018-10-11T20:52:12.000Z",
    "updatedAt": "2018-10-11T20:52:12.000Z",
    "id": 5,
    "name": "new team",
    "autoAddUsers": true,
    "autoAddProjects": false,
    "organizationId": 1
}
```

Creates a new team.

### HTTP Request

`POST https://app.fossa.io/api/teams`

### Body parameters

| Parameter  | Type           | Required? | Description                                                                        |
| ---------- | -------------- | --------- | ---------------------------------------------------------------------------------- |
| `name` | `string`   | Y         | The name of the team |
| `autoAddUsers` | `boolean` | N | Whether new users added to your FOSSA organization should automatically be added to this team (default false) |
| `autoAddProjects` | `boolean` | N | Whether newly imported projects should be automatically added to this team (default false) |

## List Teams

```bash
http 'https://app.fossa.io/api/teams' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* Team 1 elided */
  },
  {
    /* Team 2 elided */
  },
  {
    /* Team 3 elided */
  }
  // ...
];
```

Lists all teams, the IDs of the users that have access to each team, and the locators of the projects in each team.

### HTTP Request

`GET https://app.fossa.io/api/teams`

## Update Team

```bash
http --form PUT 'https://app.fossa.io/api/teams/1' name='changed team' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// The updated Team.
{
    "id": 1,
    "organizationId": 1,
    "name": "changed team",
    "autoAddUsers": false,
    "autoAddProjects": false,
    "createdAt": "2018-09-25T18:04:15.000Z",
    "updatedAt": "2018-10-11T21:02:19.000Z",
    "teamUsers": [
        {
            "userId": 2
        }
    ],
    "teamProjects": [
        {
            "projectId": "git+github.com/lackstein/cryptopals"
        }
    ]
}
```

Updates Teams.

### HTTP Request

`PUT https://app.fossa.io/api/teams/:teamId`

### Path parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `:teamId`   | `number` | Y         | The ID of the team to update.   |

### Body parameters

| Parameter  | Type           | Required? | Description                                                             |
| ---------- | -------------- | --------- | ----------------------------------------------------------------------- |
| `${field}` | `keyof Team`   | N         | Sets the field's value. If not specified, fields will remain unchanged. |

## Delete Team

```bash
http DELETE 'https://app.fossa.io/api/teams/5' 'Authorization: token 123456789'
```

> Returns an HTTP status of 200

Delete a Team by ID.

### HTTP Request

`DELETE https://app.fossa.io/api/teams/:teamId`

### Path parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `:teamId`   | `number` | Y         | The ID of the team to delete.   |

## Manage Users

```bash
http --form PUT 'https://app.fossa.io/api/teams/1/users' action='replace' users=1 users=2 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// All users that belong to the team.
{
    "id": 1,
    "users": [
        1,
        2
    ]
}
```

Add or remove users from a team.

### HTTP Request

`PUT https://app.fossa.io/api/teams/:teamId/users`

### Path parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `:teamId`   | `number` | Y         | The ID of the team to delete.   |

### Body parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `action`    | `add`, `remove`, or `replace` | N | Whether to add or remove the specified user ids from the team. `replace` will replace the current list of team users with the provided user ids. (default replace) |

## Manage Projects

```bash
http --form PUT 'https://app.fossa.io/api/teams/1/projects' action='replace' projects='git+github.com/lackstein/cryptopals' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
// All users that belong to the team.
{
    "id" 1,
    "projects": [
        "git+github.com/lackstein/cryptopals"
    ]
}
```

Add or remove projects from a Team.

### HTTP Request

`PUT https://app.fossa.io/api/teams/:teamId/projects`

### Path parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `:teamId`   | `number` | Y         | The ID of the team to delete. |

### Body parameters

| Parameter   | Type     | Required? | Description                     |
| ----------- | -------- | --------- | ------------------------------- |
| `action`    | `add`, `remove`, or `replace` | N | Whether to add or remove the specified project locators from the team. `replace` will replace the current list of team projects with the provided project locators. (default replace) |
