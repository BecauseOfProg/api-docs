# 🔐 Authentication

In order to do some actions, a guest must be authenticated as a user.

## Get user token

`POST /auth`

Get the token of a user, to authenticate it. Returns `token` string.

### Request body

| Field    | Type   | Description     |
| -------- | ------ | --------------- |
| email    | string | user's email    |
| password | string | user's password |

**To use authentication in requests that require it, add the `Authorization` header with your token inside.**
