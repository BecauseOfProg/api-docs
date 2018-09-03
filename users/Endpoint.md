# /api/users - Users

## Get all users

GET /api/users

Response :

- `users` : List, all users

## Create an user

POST /api/users

Request body :

- `email` : String, email adress
- `username` : String, username, used in the URL (length : minimum 2, maximum 32)
- `password` : String, password
