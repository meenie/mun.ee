## Step 1: Download/Install Munee using composer

Add `meenie/Munee` to your `composer.json` file:

```js
{
    "require": {
        "meenie/Munee": "*"
    }
}
```

If you haven't already, download Composer

```bash
$ curl -s http://getcomposer.org/installer | php
```

Now install Munee

```bash
$ php composer.phar install
```

**Important:** Make sure the `cache` folder inside `vendor/meenie/Munee` is writable by the server.
______

<h2 id="step-2">Step 2: Use Munee in your library</h2>

Create a file called `munee.php` that is web accessible and paste in the following

```php
<?php
// Include the composer autoload file
require 'vendor/autoload.php';
// Echo out the response
echo \Munee\Dispatcher::run(new \Munee\Request());
```

**Note:** Update the correct path to the `autoload.php` file.
______

## Step 3: Create A RewriteRule rule - [Optional](/Tips_&_Tricks#no-htaccess)

Open the `.htaccess` file in your webroot and paste in the following:

```bash
#### Munee .htaccess Code Start ####
RewriteRule ^(.*\.(?:css|less|scss|js|coffee|jpg|png|gif|jpeg))$ munee.php?files=/$1 [L,QSA,NC]
#### Munee .htaccess Code End ####
```