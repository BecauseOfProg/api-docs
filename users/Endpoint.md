# /api/users - Users

## Get all users

GET /api/users

Response :

- `users` : List, all users

## Create user

POST /api/users

Request body :

- `email` : String, email address (length : minimum 6)
- `username` : String, username, used in the URL (length : minimum 2, maximum 32)
- `password` : String, password

## Get user

GET /api/users/{username}

Response :

- `user` : Dictionnary, the requested user

## Modify user

PATCH /api/users/{username}

**Require auth.**

Request body :

- `email` : String, email address (length : minimum 6)
- `displayname` : String, name which is displayed on comments and profile (length : minimum 2, maximum 32)
- `description` : String, description with some infos
- `biography`: String, biography
- `location` : String, location
- `socials` : List of dicts, social networks of the user
