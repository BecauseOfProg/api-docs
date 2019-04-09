# 🕓 Change log

## Added : User's informations with post

**April 9, 2019 :** when a post is returned, all the users informations are returned.

**Affecting :** [Post resource](resources/Post.md)

## Added : Get user's permissions

**January 5, 2018 :** getting user's permissions is now in `/users/{username/permissions` and requires `USER_WRITE` permission. [Details](users/Endpoint.md#get-users-permissions)

**Affecting :** [Get user](users/Endpoint.md#get-user)

## Changed : `avatar` is now `picture`

**January 5, 2018 :** user field `avatar` has been renamed into `picture`. [Details](users/Endpoint.md)

**Affecting :** [Get user](users/Endpoint.md#get-user), [Edit user's profile](users/Endpoint.md#edit-users-profile)

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
