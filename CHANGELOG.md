# 🕓 Change log

## Added : /users/{username}/permissions

**January 5, 2018 :** added the possibility to edit user's permissions. [Details](users/Endpoint.md#edit-users-permissions)

## Added : `USER_WRITE` and `BLOG_WRITE` permissions

**January 5, 2018 :** updated permissions list to add these two permissions. [Details](users/Permissions.md)

## Updated : Modify user request's parameters change

**January 5, 2018 :** `avatar` added and `email` removed.

## Breaking change : Auth now in a header

**September 24, 2018 :** The token should be passed in the `Authorization` header of the request.

## Removed : Access to all users

**September 8, 2018 :** The /users endpoint with GET method is no longer available.

## Breaking change : root is now /v1

**September 7, 2018 :** To have more clarity, the root URL is no longer /api, but /v1.
