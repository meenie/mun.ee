There are some constants that can be overridden in your dispatcher file before *Munee* has been included in the file.  They provide a bit of customisation if needed.  *Munee* is designed to work right out of the box, so most of the time these settings are not needed.

#### Setting Webroot
*Munee* does a pretty good job guessing what the webroot of your application is but for some reason or another it might not get it right.

```php
define('WEBROOT', '/full/path/to/webroot');
```

#### Setting Cache Directory
By default, *Munee* stores the cache of each asset within it's own directory structure.  If for some reason you want to store it somewhere else, then use this bit of code.

```php
define('MUNEE_CACHE', '/full/path/to/alternate/cache');
```

#### Setting the Character Encoding
The default setting at the moment is UTF-8, but you may change this to whatever you want.

```php
define('MUNEE_CHARACTER_ENCODING', 'iso-8859-1');
```