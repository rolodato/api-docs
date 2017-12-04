# Users

> An example User:

```json
{
  "bitbucketCloud": null,
  "createdAt": "2017-09-25T18:34:49.936Z",
  "demo": false,
  "email": "test@fossa.io",
  "email_verified": true,
  "full_name": "",
  "github": {
    "avatar_url": "https://avatars1.githubusercontent.com/u/2092654?v=4",
    "email": "test@fossa.io",
    "name": null
  },
  "id": 1525,
  "joined": "2017-09-25T18:34:49.000Z",
  "last_visit": "2017-09-25T18:34:49.000Z",
  "organization": {
    "access_level": "premium",
    "createdAt": "2017-02-23T02:04:11.628Z",
    "defaultPolicyId": 251,
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
    "jira": {
      "base_url": null,
      "credentials": {},
      "enabled": false
    },
    "podSources": [],
    "slack": [],
    "title": "test-abe",
    "updatedAt": "2017-12-04T07:43:58.574Z"
  },
  "organizationId": 90,
  "phone": "",
  "role": "",
  "super": false,
  "terms_agreed": "2017-11-15T20:53:49.887Z",
  "tokens": [
    {
      "callbackUrl": null,
      "createdAt": "2017-12-01T23:36:33.869Z",
      "email": null,
      "id": 351,
      "isDisabled": false,
      "organizationId": null,
      "token": "123456789",
      "type": "api",
      "updatedAt": "2017-12-01T23:36:33.869Z",
      "userId": 1525
    }
  ],
  "updatedAt": "2017-11-30T22:57:03.623Z",
  "username": "test-user"
}
```

`Organization`s contain many `User`s. Each `User` corresponds to an account
signed up with the current FOSSA instance.

## List Users

```bash
http 'http://api.fossa.io/api/users' 'Authorization: token 123456789'
```

> Returns data in the shape of:

```js
[
  {
    /* User 1 elided */
  },
  {
    /* User 2 elided */
  },
  {
    /* User 3 elided */
  }
  // ...
];
```

Lists all users in your organization. This includes yourself.

This endpoint supports the standard filtering, search, sorting, and pagination
operators.

### HTTP Request

`GET http://api.fossa.io/api/users`

### Query parameters

| Parameter  | Type         | Required? | Description                                                                                                                                                                                    |
| ---------- | ------------ | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `${field}` | `keyof User` | N         | Filter results to only include rows where `${field}` is set to the value passed as `${field}`. For example, to only include rows where `email_verified` is `true`, pass `email_verified=true`. |
| `q`        | `any`        | N         | Perform a substring search for the value across all fields.                                                                                                                                    |
| `sort`     | `keyof User` | N         | Sort by the specified field name. Prefix with `-` to sort by descending order. For example, to sort in descending by `username`, pass `sort=-username`.                                        |
| `count`    | `int`        | N         | Paginate response to include only `count` rows per response.                                                                                                                                   |
| `page`     | `int`        | N         | Set the pagination page index.                                                                                                                                                                 |
| `offset`   | `int`        | N         | Begin pagination at the specified row offset.                                                                                                                                                  |

## Retrieve User

## Update User

## Register New User

## Set Password

## Create API Token

## Revoke API Token
