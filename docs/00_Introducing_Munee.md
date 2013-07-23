*Munee* is a PHP5.3 library to easily on-the-fly compile LESS, SCSS (SASS is not supported!), or CoffeeScript, resize/manipulate images on-the-fly, minify CSS and JS, and cache assets locally and remotely for lightening fast requests. No need to change how you include your assets in your templates. Just follow the couple of installation instructions below and you are ready to go!
______

## Features

* On-the-fly LESS, SCSS, CoffeeScript Compiling
* On-the-fly Image Resizing/Manipulation
* Smart Asset Caching - Client Side & Server Side
* Combine CSS or JS into one request
* Minifying and Gzip Server Response
______

## Why the name *Munee*?

The reason I chose the name *Munee* is because it sounds like 'Money' which is another word for 'Assets' and what this library optimises. Also, I needed a top level uniquely named Namespace for the library.
______

## Requirements

+ PHP5.3+
+ `RewriteEngine` turned on inside a `.htaccess` file (Or in the Apache Config file) **Optional**
______

<h2 id="using-asset-filters">Using Asset Filters</h2>

*Munee* uses the concept of Filters leveraging Query Strings to manipulate an asset before it has been cached.  An asset can have multiple Filters applied to it at once.  They are used for simple tasks such as minifying CSS or complex tasks like resizing an image.  The filter value can either be a simple string or multiple arguments. Arguments can either be in long form or use their shortened form (which will be notated in each usage section).  The value for an argument must be wrapped in square brackets `[]`. There is no need to put any characters between each parameter, although you can if you want.

Example of a simple filter to minify some CSS:
```html
<link rel="stylesheet" href="/css/site.scss?minify=true">
```

Example of a complex filter to resize/crop an image and then turn it grayscale:
```html
<img src="/path/to/image.jpg?resize=width[100]height[100]exact[true]&grayscale=true">
```
______

<h2 id="concatenating-text-assets">Concatenating Text Assets</h2>

One of the best features of *Munee* is the ability to concatenate multiple CSS or JS files into one request. This can be achieved by creating a comma (,) delimited list of all similar assets in your `link` or `script` tags.

Example for CSS files
```html
<link rel="stylesheet" href="/css/libs/bootstrap.min.css,/css/site.less">
```

Example for JS files
```html
<script src="/js/libs/jquery-1.8.1.min.js,/js/libs/bootstrap.min.js,/js/site.js"></script>
```

**Note:** Munee will prefix each asset with a forward slash (/) if one doesn't exist. This will make the URL of each asset absolute.
______

## Note On Caching

*Munee* caches asset requests server side and returns a `304 Not Modified` on subsequent requests if the asset hasn't been modified. If the asset has been modified, it will overwrite that cache and tell the browser they must revalidate it's cache so the new file can be shown. To accomplish this without the browser's caching engine trying to be smart, Munee sets the `Cache-Control` header to `must-revalidate`.  If you run into any problems, please [submit an issue](https://github.com/meenie/munee/issues).