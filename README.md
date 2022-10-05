goodreads-api
=============

A quick PHP wrapper class for the GoodReads API.

**This repository is no longer maintained.** I stopped using GoodReads (moved to The StoryGraph), so I won't be updating this in future. **If you've created a newer/better PHP GoodReads API, let me know and I'll link it here.**

---

Disclaimer
----------
This is something I hacked together quickly, it isn't beautiful, and can only access a few API endpoints. However it's a good starting point, and from a cursory glance implementing other methods wouldn't be particularly tricky. Caching support is also baked in.

Please also bear in mind the GoodReads API itself isn't great (some methods for example only support XML!), you can read/comment on that in their forums.

Requirements
------------
* PHP 5.3.x or higher
* cURL
* GoodReads API key

Available methods
-----------------
* [author.show](https://www.goodreads.com/api#author.show)
* [author.books](https://www.goodreads.com/api#author.books)
* [book.show](https://www.goodreads.com/api#book.show)
* [book.show_by_isbn](https://www.goodreads.com/api#book.show_by_isbn)
* [book.title](https://www.goodreads.com/api#book.title)
* [reviews.list](https://www.goodreads.com/api#reviews.list)
* [review.show](https://www.goodreads.com/api#review.show)
* [user.show](https://www.goodreads.com/api#user.show)

Usage
-----
1. Include class
2. Initialise wrapper `$api = new GoodReads('PUT YOUR API KEY HERE', 'writable directory for caching');`
3. Call a method `$data = $api->getLatestReads(4148474);`

License
-------
Simplified BSD (included).

Changes
-------
2018-06-02 [Tyler Paulson](https://github.com/tyler-paulson)
* Added function to get a user by username rather than ID.

2018-03-04 [Tyler Paulson](https://github.com/tyler-paulson)
* Added function to get all of a user's books, read or otherwise.

2017-12-10 [Daniel G Wood](https://github.com/danielgwood)
* Added 5 endpoints: author.books, book.show, book.show_by_isbn, book.title and review.show
* Updated documentation.

2016-05-13 [Victor Davis](https://github.com/victordavis/goodreads-api)
* Added LIBXML_NOCDATA arg to simplexml_load_string to capture CDATA in returned XML
* Added 2 endpoints: author.show & user.show
