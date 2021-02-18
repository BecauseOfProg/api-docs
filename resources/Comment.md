# 💬 Comment resource

Comments are made by readers on specific blog posts to give their opinion, suggest changes, give sources, interact with authors...

### Comment object

| Field            | Type                      | Description                                           | Can be null ?                           |
| ---------------- | ------------------------- | ----------------------------------------------------- | --------------------------------------- |
| slug             | string                    | unique identifier of the comment                      |                                         |
| username         | string                    | username of the comment's author (2-64 characters)    |                                         |
| email            | string                    | their email                                           | ✅ (without `USER_WRITE` permission)    |
| encoded_email    | string                    | encoded hash of their email for Gravatar              |                                         |
| ip               | string                    | IP from where the comment was published               | ✅ (without `USER_WRITE` permission)    |
| post             | string                    | identifier of the [blog post](./BlogPost.md)          |                                         |
| content          | string                    | comment's content (5-500 characters)                  |                                         |
| is_validated     | boolean                   | if it's validated by a moderator (publicly available) | ✅ (without `USER_WRITE` permission)    |
| pinned           | boolean                   | if it's pinned (at the top)                           |                                         |
| timestamp        | integer                   | unix timestamp, comment creation                      |                                         |

## Get all comments

`GET /comments`

Get the comments on all articles. Returns an array of [comment objects](#comment-object). Requires auth and `USER_WRITE` permission.

## Get comments on an article

`GET /comments/{post.url}`

Get comments published on a specific article. Returns an array of [comment objects](#comment-object)

## Submit a comment

`POST /comments/{post.url}`

Submit, as a user, a comment on an article. Note that a moderator will have to [validate the comment](#validate-a-comment) in order for it to be published.

### Required data

| Field       | Type            | Description                      |
| ----------- | --------------- | -------------------------------- |
| username    | string          | username of the comment's author |
| email       | string          | their email                      |
| content     | string          | comment's content                | 

## Validate a comment

`PUT /comments/{post.url}/{comment.url}`

Validate a comment to publish it. Requires auth and `USER_WRITE` permission.

## Delete a comment

`DELETE /comments/{post.url}/{comment.url}`

Delete a comment, published or not. Requires auth and `USER_WRITE` permission
