# 📰 Blog post resource

These posts are created by BOP members in the blog. They can be articles, tutorials and tips on various subjects such as informatic, development, etc...

### Blog post object

| Field            | Type                   | Description                      | Can be null ?                           |
| ---------------- | ---------------------- | -------------------------------- | --------------------------------------- |
| url              | string                 | post's URL                       |                                         |
| title            | string                 | post's title                     |                                         |
| timestamp        | integer                | unix timestamp, post creation    |                                         |
| author           | [user object](User.md) | informations about post's author |                                         |
| type             | string                 | post's category                  |                                         |
| category         | string                 | post's category                  |                                         |
| description      | string                 | a summary of post's content      |                                         |
| labels           | list of strings        | labels for SEO                   |                                         |
| banner           | string                 | post's banner                    |                                         |
| article_language | string                 | `html` or `md`                   |                                         |
| content          | string                 | post's content, markdown format  | ✅ (if inclued in a many-posts request) |

For the moment, a post can be in HTML or Markdown. This is precised in the `article_language` field.

## Get all posts

`GET /blog-posts`

Get all the posts. Returns a `data` list with [post objects](#blog-post-object) inside.

## Get last post

`GET /blog-posts/last`

Get the last published post. Returns a `data` object corresponsing to a [post object](#blog-post-object).

## Create post

`POST /blog-posts`

Write a new post and publish it. Requires auth and `BLOG_WRITE` permission.

### Required data body

| Field       | Type            | Description                     |
| ----------- | --------------- | ------------------------------- |
| url         | string          | post's URL                      |
| title       | string          | post's title                    |
| type        | string          | post's category                 |
| category    | string          | post's category                 |
| description | string          | a summary of post's content     |
| labels      | list of strings | labels for SEO                  |
| banner      | string          | post's banner                   |
| content     | string          | post's content, markdown format |

## Get one post

`GET /blog-posts/{post.url}`

Get one post by its URL. Returns a `data` object corresponding to a [post object](#blog-post-object) with post's content.

## Edit post

`PATCH /blog-posts/{post-url}`

Edit a post. Requires auth and `BLOG_WRITE` permission.

**Editable fields :** `title`, `type`, `category`, `description`, `labels`, `banner`, `content`.

## Delete post

`DELETE /blog-posts/{post-url}`

Delete a post. Requires auth and `BLOW_WRITE` permission.