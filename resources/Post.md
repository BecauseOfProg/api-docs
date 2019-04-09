# 📰 Post resource

Posts are created by BOP members and inform about the news around the team, the projects or anything else.

### Post object

| Field     | Type    | Description                     | Can be null ?                           |
| --------- | ------- | ------------------------------- | --------------------------------------- |
| title     | string  | post's title                    |                                         |
| url       | string  | post's URL                      |                                         |
| category  | string  | post's category                 |                                         |
| banner    | string  | post's banner                   |                                         |
| author    | object  | [user object](User.md)          |                                         |
| timestamp | integer | unix timestamp, post creation   |                                         |
| content   | string  | post's content, markdown format | ✅ (if inclued in a many-posts request) |

## Get all posts

`GET /posts`

Get all the posts. Returns a `posts` list with [post objects](#post-object) inside.

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

## Get post

`GET /posts/{post.url}`

Get one post by its URL. Returns a [post object](#post-object).

## Edit post

`PATCH /posts/{post-url}`

Edit a post. Requires auth and `POST_WRITE` permission.

### Request body

| Field    | Type   | Description                     |
| -------- | ------ | ------------------------------- |
| title    | string | post's title                    |
| banner   | string | post's banner                   |
| category | string | post's category                 |
| content  | string | post's content, markdown format |

## Delete post

`DELETE /posts/{post-url}`

Delete a post. Requires auth and `POST_WRITE` permission.
