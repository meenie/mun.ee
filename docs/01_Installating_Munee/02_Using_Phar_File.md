*Munee* can be used by just including a [Phar](http://php.net/manual/en/book.phar.php) file when creating your dispatcher file.  There is no need to use Composer as *Munee* and all of it's library dependencies are packaged into the phar file.
______

## Step 1: Download Munee.phar File

Download the phar and place it in your application; preferrably outside of webroot: <a href="/download.php?filename=munee.phar" id="pharDownload" class="btn btn-success">Download Munee.phar</a>
______

## Step 2: Use Munee in your library</h2>

Create a file called `munee.php` that is web accessible and paste in the following

```php
<?php
// Define webroot
define('WEBROOT', __DIR__);
// Define cache folder
define('MUNEE_CACHE', __DIR__ . '/cache');
// Include munee.phar
require '../path/to/munee.phar';
// Echo out the response
echo \Munee\Dispatcher::run(new \Munee\Request());
```

**Important:** You must define a cache folder when using the Phar file since PHP has issues with creating files within Phar files. Make sure the directory you define is writable by the server.
**Note:** Update the correct path to the `munee.phar` file.
______

## Step 3: Create A RewriteRule rule - [Optional](/Tips_&_Tricks#no-htaccess)

Open the `.htaccess` file in your webroot and paste in the following:

```bash
#### Munee .htaccess Code Start ####
RewriteRule ^(.*\.(?:css|less|scss|js|coffee|jpg|png|gif|jpeg))$ munee.php?files=/$1 [L,QSA,NC]
#### Munee .htaccess Code End ####
```