<div align="center">
  <img src="https://cdn.becauseofprog.fr/v2/sites/becauseofprog.fr/assets/logos/bop.min.svg" alt="Logo BecauseOfProg" width="150" />
  <h1>BecauseOfProg's API</h1>
  <h3>📚 Fetch all kind of information related to the BecauseOfProg</h3>
</div>

- [Change log](CHANGELOG.md)
- [License](LICENSE)
- **Topics**
  - [Authentication](topics/Authentication.md)
  - [Pagination](topics/Pagination.md)
  - [Permissions](topics/Permissions.md)
- **Resources**
  - [Post](resources/Post.md)
  - [Blog post](resources/BlogPost.md)
  - [User](resources/User.md)

## Introduction

Welcome on the BecauseOfProg's API ! From there, you can fetch data available on our website :

- Users registered on the website
- Posts and blog posts that we published

First of all, you need a URL in order to access it. The root URL for the API is `https://api.becauseofprog.fr`. This URL is followed by the version of this format : `v{number}`. You can find versions below :

| Version | Status    |
| ------- | --------- |
| 1       | Available |

### Requests

Some requests need user to be authenticated : learn mode on the [Authentication topic](topics/Authentication.md).

Every request to the API that require a body must be JSON-formatted, with an object as a container.

### Responses

Every response is in JSON format, and has in its body a `code` which is `1` or `0`, depending on the request's success or not, and a `data` variable containing the requested data.
