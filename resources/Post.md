# 📰 Post resource

Posts are created by BOP members and inform about the news around the team, the projects or anything else.

### Post object

| Field     | Type                               | Description                     | Can be null ?                           |
| --------- | ---------------------------------- | ------------------------------- | --------------------------------------- |
| title     | string                             | post's title                    |                                         |
| url       | string                             | post's URL                      |                                         |
| category  | string                             | post's category                 |                                         |
| banner    | string                             | post's banner                   |                                         |
| author    | [user object](User.md#user-object) | post's author                   |                                         |
| timestamp | integer                            | unix timestamp, post creation   |                                         |
| content   | string                             | post's content, markdown format | ✅ (if inclued in a many-posts request) |

## Get all posts

`GET /posts`

Get all the posts. Returns a list of [post objects](#post-object) without the content.

## Get one post

`GET /posts/{post.url}`

Get one post by its URL. Returns a [post object](#post-object) with post's content.

## Create post

`POST /posts`

Write a new post and publish it. Requires auth and `POST_WRITE` permission.

### Request body

| Field    | Type   | Description                     |
| -------- | ------ | ------------------------------- |
| title    | string | post's title                    |
| banner   | string | post's banner                   |
| url      | string | post's URL                      |
| category | string | post's category                 |
| content  | string | post's content, markdown format |

## Edit post

`PATCH /posts/{post-url}`

Edit a post. Requires auth and `POST_WRITE` permission.

**Editable fields :** `title`, `category`, `banner`, `content`.

## Delete post

`DELETE /posts/{post-url}`

Delete a post. Requires auth and `POST_WRITE` permission.
