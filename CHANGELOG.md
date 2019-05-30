# 🕓 Change log

## Added : Blog posts endpoint

**May 30, 2019 :** You can now access to blog posts via a new endpoint. [Details](resources/BlogPost.md)

## Added : Arduino projects endpoint

**April 9, 2019 :** The API now includes the future Arduino projects hub. [Details](resources/Arduino.md)

## Changed : Optional fields

**April 9, 2019 :** All the fields in some PATCH requests are now optional, meaning that you can only include fields that you're going to edit.

**Affecting :** [Edit user's profile](resources/User.md#edit-users-profile), [Edit post](resources/Post.md#edit-post).

## Added : User's informations with post

**April 9, 2019 :** when a post is returned, all the users informations are returned.

**Affecting :** [Post resource](resources/Post.md)

## Added : Get user's permissions

**January 5, 2018 :** getting user's permissions is now in `/users/{username/permissions` and requires `USER_WRITE` permission. [Details](resources/User.md#get-users-permissions)

**Affecting :** [Get user](resources/User.md#get-user)

## Changed : `avatar` is now `picture`

**January 5, 2018 :** user field `avatar` has been renamed into `picture`. [Details](resources/User.md)

**Affecting :** [Get user](resources/User.md#get-user), [Edit user's profile](resources/User.md#edit-users-profile)

## Added : /users/{username}/permissions

**January 5, 2018 :** added the possibility to edit user's permissions. [Details](resources/User.md#edit-users-permissions)

## Added : `USER_WRITE` and `BLOG_WRITE` permissions

**January 5, 2018 :** updated permissions list to add these two permissions. [Details](topics/Permissions.md)

## Updated : Modify user request's parameters change

**January 5, 2018 :** `avatar` added and `email` removed.

## Breaking change : Auth now in a header

**September 24, 2018 :** The token should be passed in the `Authorization` header of the request.

## Removed : Access to all users

**September 8, 2018 :** The /users endpoint with GET method is no longer available.

## Breaking change : root is now /v1

**September 7, 2018 :** To have more clarity, the root URL is no longer /api, but /v1.
