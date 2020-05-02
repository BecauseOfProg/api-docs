<div align="center">
  <img src="https://cdn.becauseofprog.fr/v2/sites/becauseofprog.fr/assets/logos/bop.min.svg" alt="Logo BecauseOfProg" width="150" />
  <h1>BecauseOfProg's API</h1>
  <h3>📚 Fetch all kind of information related to the BecauseOfProg</h3>
</div>

## Introduction

Welcome on the BecauseOfProg's API ! Here, you can fetch data available from our website, such as :

- Users registered on the website
- Posts and blog posts that we published

First of all, you need a URL in order to access it. The root URL for the API is `https://api.becauseofprog.fr`. This URL is followed by the version of this format : `v{number}`. You can find versions below :

| Version | Status    |
| ------- | --------- |
| 1       | Available |

Every response is in JSON format, and has in its body a `code` which is `1` or `0`, depending on the request's success or not, and all requested fields.

## Table of Contents

- [Change log](CHANGELOG.md)
- [License](LICENSE)
- **Topics**
  - [Authentication](topics/Authentication.md)
  - [Permissions](topics/Permissions.md)
- **Resources**
  - [Post](resources/Post.md)
  - [Blog post](resources/BlogPost.md)
  - [User](resources/User.md)
