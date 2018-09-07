# /api/posts - Posts

## Get all posts

GET /api/posts

Response :

- `posts` : List, the posts

## Create post

POST /api/posts

**Require auth. Needed permissions : `POST_WRITE`**

Request body :

- `title` : String, title
- `url` : String, URL to the post
- `category` : String, category
- `content` : String, content using Markdown

## Get post

GET /api/posts/{post-url}

Response :

- `post` : Dictionnary, the requested post

## Modify post

PATCH /api/posts/{post-url}

**Require auth. Needed permissions : `POST_WRITE`**

Request body :

- `title` : String, title
- `banner` : String, banner to decorate the post
- `category` : String, category
- `content` : String, content using Markdown

## Delete post

DELETE /api/posts/{post-url}

**Require auth. Needed permissions : `POST_WRITE`**
