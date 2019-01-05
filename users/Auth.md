# 🔐 /auth - Authentication

In order to do some actions, a guest must be authenticated as a user.

## Get user token

POST /users

Request body :

- `username` : String, username, _not displayname!_ (length : minimum 2, maximum 32)
- `password` : String, password

Response :

- `token` : String, token of the user.

**To use authentication in requests that require it, add the `Authorization` header with your token inside.**
