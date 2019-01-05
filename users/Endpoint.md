# 👥 /users - Users

Users are the central part of the API. They interact with content and, in some cases, create it.

## Create user

POST /users

Request body :

- `email` : String, email address (length : minimum 6)
- `username` : String, username, used in the URL (length : minimum 2, maximum 32)
- `password` : String, password

## Get user

GET /users/{username}

Response :

- `user` : Dictionnary, the requested user

## Edit user's profile

PATCH /users/{username}

**Requires auth.**

Request body :

- `displayname` : String, name which is displayed on comments and profile (length : minimum 2, maximum 32)
- `picture` : String, profile picture
- `description` : String, description with some infos
- `biography`: String, biography
- `location` : String, location
- `socials` : List of dicts, social networks of the user

## Get user's permissions

GET /users/{username}/permissions

**Requires auth and `USER_WRITE` permission.**

Response :

- `permissions` : List, all the permissions that user has

## Edit user's permissions

PATCH /users/{username}/permissions

**Requires auth and `USER_WRITE` permission.**

Request body :

- `permissions` : List, all the permissiosn granted to the user
