# /auth - Authentication

## Get user token

POST /users

Request body :

- `username` : String, username, _not displayname!_ (length : minimum 2, maximum 32)
- `password` : String, password

Response :

- `token` : String, token of the user.

**To use the token in requests that require auth, add `?token={token}` at the end of the URL.**
