# 🔐 Authentication

In order to do some actions, a guest must be authenticated as a user.

## Get user token

`POST /auth`

Get the token of a user, to authenticate it. Returns a `token` string and a `user` field corresponding to a [user object](../resources/User.md#user-object) including permissions.

### Request body

| Field    | Type   | Description     |
| -------- | ------ | --------------- |
| email    | string | user's email    |
| password | string | user's password |

**To use authentication in requests that require it, add the `Authorization` header with your token inside.**

## Get user data by token

`GET /auth/data`

Get the data of a user based on his token, to re-authenticate him. Retuns a [user object](../resources/User.md#user-object) including permissions and corresponding to the token inside the `Authorization` header.
