vuze-client
===========

PHP library for control Vuze torrent-client.
Require installed XML over Http plugin for Vuze.

Library is based on a class of application <a href="http://strawp.net/azureus_php/">Azureus PHP Control Layer</a>.
The code has been rewritten, optimized and prepared for use in third-party projects.

Examples of use
===============

Get a list of all torrents:
```php
$client = new VuzeClient('127.0.0.1', 6884);
print_r($client->getDownloads());
```

Add torrent from data:
```php
$client = new VuzeClient('127.0.0.1', 6884);
$client->addTorrent(file_get_contents('/home/cosmologist/Downloads/some.torrent'));
```

Add torrent from url:
```php
$client = new VuzeClient('127.0.0.1', 6884);
$client->addTorrentUrl('http://localhost/some.torrent');
```
