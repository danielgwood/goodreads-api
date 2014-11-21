goodreads-api
=============

A quick PHP wrapper class for the GoodReads API.

Disclaimer
----------
This is something I hacked together quickly, it isn't beautiful, and as you'll see I only implemented one API endpoint (the only one I needed). However it's a good starting point, and from a cursory glance implementing other methods wouldn't be particularly tricky. Caching support is also baked in.

Please also bear in mind the GoodReads API itself isn't great (some methods for example only support XML!), you can read/comment on that in their forums.

Requirements
------------
* PHP 5.3.x or higher
* cURL
* GoodReads API key

Available methods
-----------------
* [reviews.list](https://www.goodreads.com/api#reviews.list)

Usage
-----
# Include class
# Initialise wrapper
    $api = new GoodReads('PUT YOUR API KEY HERE', 'writable directory for caching');
# Call a method
    $data = $api->getLatestReads(4148474);
