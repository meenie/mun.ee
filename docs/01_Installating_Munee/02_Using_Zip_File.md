You can download a zip file that contains *Munee* as well as it's library dependencies. This means there is no need to use Composer.

## Step 1: Download Munee.zip File

Download the zip and extract it in your application; preferrably outside of webroot: <a href="/download.php?filename=munee.zip" id="zipDownload" class="btn btn-success">Download Munee.zip</a>

## Step 2: Use Munee in your library</h2>

Create a file called `munee.php` that is web accessible and paste in the following

```php
<?php
// Define webroot
define('WEBROOT', __DIR__);
// Include Munee's autoload.php file
require '../munee/autoload.php';
// Echo out the response
echo \Munee\Dispatcher::run(new \Munee\Request());
```

**Important**: Make sure the `cache` folder inside `munee/meenie/Munee` is writable by the server.
**Note:** Update the correct path to the `autoload.php` file.
______

## Step 3: Create A RewriteRule rule - [Optional](/Tips_&_Tricks#no-htaccess)

Open the `.htaccess` file in your webroot and paste in the following:

```bash
#### Munee .htaccess Code Start ####
RewriteRule ^(.*\.(?:css|less|scss|js|coffee|jpg|png|gif|jpeg))$ munee.php?files=/$1 [L,QSA,NC]
#### Munee .htaccess Code End ####
```