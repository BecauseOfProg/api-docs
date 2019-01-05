# ✅ Permissions list

Here is a list of all the permissions that users can have. They grant access to different parts of the API.

- Posts : `POST_WRITE`
  - Description : gives write access on posts to user. Then, can use `POST`, `PATCH` and `DELETE` HTTP methods on the `posts` endpoint.
  - Usage : `POST` on `/posts` and `PATCH`, `DELETE` on `/posts/{post-url}`
  - More informations : [Posts endpoint](../posts/Endpoint.md)
- Users : `USER_WRITE`
  - Description : gives write access on users.
  - Usage : `PATCH` on `/users/{username}`
  - More informations : [Users endpoint](../users/Endpoint.md)
- Blog : `BLOG_WRITE`
  - Description : gives write access on blog posts.
  - Usage : writing articles on the blog.
