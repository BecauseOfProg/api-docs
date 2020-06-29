# 📰 Pagination

Some requests can return a lot of database entries, that make the client request slower and the API overloaded. To overcome this problem, certain endpoints have a pagination, and the caller must compose with it.

**By default, the first ten entries are returned**. To get more, you must add the `page` parameter at the end of the URL, with the page number of your choice. The total amount of pages is available under the `pages` property, at the root of the JSON alongside `code` and `data`. If you go past this number, the data will be empty.
