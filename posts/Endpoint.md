# /posts - Posts

Posts are created by BOP's members and inform about the news around the team, the projects or anything else.

## Get all posts

GET /posts

Response :

- `posts` : List, the posts

## Create post

POST /posts

**Requires auth and `POST_WRITE` permission**

Request body :

- `title` : String, title
- `url` : String, URL to the post
  **Must be unique**
- `category` : String, category
- `content` : String, content using Markdown

## Get post

GET /posts/{post-url}

Response :

- `post` : Dictionnary, the requested post

## Edit post

PATCH /posts/{post-url}

**Requires auth and `POST_WRITE` permission**

Request body :

- `title` : String, title
- `banner` : String, banner to decorate the post
- `category` : String, category
- `content` : String, content using Markdown

## Delete post

DELETE /posts/{post-url}

**Requires auth and `POST_WRITE` permission**
