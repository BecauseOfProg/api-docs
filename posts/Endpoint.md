# /api/posts - News

## Get news

GET /api/posts

Response :

- `posts` : List, the news

## Create a post

POST /api/posts

**Require auth. Needed permissions : `POST_WRITE`**

Request body :

- `title` : String, title
- `url` : String, URL to the post
- `category` : String, category
- `content` : String, content using Markdown

## Get one post

GET /api/posts/{post-url}

Response :

- `post` : Dictionnary, the requested post
