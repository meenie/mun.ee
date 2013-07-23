### Resizing Images In Emails

If you want to resize images through *Munee* in your emails, you will need to turn off one of the security features in *Munee*.  This is the Referrer check.  To get it working, you can pass in the following option when you instantiate *Munee*:

```php
echo \Munee\Dispatcher::run(new \Munee\Request(array(
    'image' => array(
        'checkReferrer' => false
    )
)));
```
______

### Minimising JavaScript Errors When Minified

Make sure and use curly brackets for block statements (`if`, `while`, `switch`, etc) and terminate lines with a semicolon.  When the JavaScript is minified, it will put all of your code on one line.  If you have left out some brackets for an `if` statement, it will include the rest of your code inside that `if` statement and cause a lot of problems.  As long as you follow decent coding standards, you will not have a problem.
______

<h3 id="no-htaccess">Using Munee without the .htaccess file</h3>

If you would like to use *Munee* without having to use a `.htaccess` you will need to change how your assets are added in your template.  So instead of doing this:

```html
<link rel="stylesheet" href="/css/libs/bootstrap.min.css,/css/site.css?minify=true">
```

You will need to do this:

```html
<link rel="stylesheet" href="/path/to/munee.php?files=/css/libs/bootstrap.min.css,/css/site.css&minify=true">
```
______

### Preventing Munee From Setting Headers

If for some reason you would like to prevent *Munee* from setting any headers, you can pass a second argument in the Dispatcher::run() function with `array('setHeaders' => false)`.

```php
$content = \Munee\Dispatcher::run(new \Munee\Request(array('files' => '/css/site.css')), array('setHeaders' => false));
```