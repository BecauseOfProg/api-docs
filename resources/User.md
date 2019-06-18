# 👥 User resource

Users are the central part of the API. They interact with content and, in some cases, create it.

### User object

| Field            | Type            | Description                                                  | Can be null ?   |
| ---------------- | --------------- | ------------------------------------------------------------ | --------------- |
| username         | string          | username, will be taken in the profile URL (2-32 characters) |                 |
| displayname      | string          | "pretty" name to display (2-32 characters)                   |                 |
| timestamp        | integer         | unix timestamp, user creation                                |                 |
| picture          | string          | url of the user's profile picture                            |                 |
| description      | string          | user's description, markdown format                          | ✅              |
| biography        | string          | user's biography                                             | ✅              |
| location         | string          | user's location                                              | ✅              |
| socials          | list of objects | user's social networks                                       | ✅ (`[]`)       |
| is_email_public? | boolean         | wether the user's email is public or private                 |                 |
| email            | string          | user's email, if it's public                                 | ✅ (if private) |

## Get all users

`GET /users`

Get all the users. Returns a `data` object corresponding to a [user object](#user-object). Requires auth and `USER_WRITE` permission.

## Get user

`GET /users/{user.username}`

Get user's informations based on his username. Retuns a `data` object corresponding to a [user object](#user-object).

## Create user

`POST /users`

Create a new user.

### Request body

| Field    | Type   | Description                                                  |
| -------- | ------ | ------------------------------------------------------------ |
| email    | string | user's email adress (6 characters minimum)                   |
| username | string | username, will be taken in the profile URL (2-32 characters) |
| password | string | user's password (be careful to choose strong enough one)     |

## Edit user's profile

`PATCH /users/{user.username}`

Edit the user's profile informations. Requires auth, and user has to be itself.

**Editable fields :** `displayname`, `picture`, `description`, `biography`, `locations`, `socials`.

## Get user's permissions

`GET /users/{user.username}/permissions`

Get the permissions a user has. Returns a `data` list. Requires auth and `USER_WRITE` permission.

## Edit user's permissions

`PATCH /users/{user.username}/permissions`

Edit permissions a user has, to grant or limit access to resources. Requires auth and `USER_WRITE` permission.

### Request body

| Field       | Type | Description                    |
| ----------- | ---- | ------------------------------ |
| permissions | list | permissions the user will have |
