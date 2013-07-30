All LESS & SCSS (SASS is not supported!) files are automatically compiled into CSS and cached, there is nothing extra that you need to do.  Any changes you make to your CSS, even LESS/SCSS files you have `@import`ed will automatically recreate the cache, invalidate the client side cache, and force the browser to download the newest version.
________

## Dispatcher Options

These options can be set in the first parameter of the `Request` class in the dispatcher file. For example:

```php
echo \Munee\Dispatcher::run(new \Munee\Request(array('css' => array('lessifyAllCss' => true))));
```

<table>
  <tr>
    <th>Name</th><th>Type</th><th>Default</th><th>Description</th>
  </tr>
  <tr id="lessify-all-css">
    <td><code>lessifyAllCss</code></td>
    <td>Boolean</td>
    <td><code>false</code></td>
    <td>Run **all css** through the <code>LESS</code> compiler (regardless of if it's extension is <code>.css</code>)</td>
  </tr>
  <tr>
    <td><code>scssifyAllCss</code></td>
    <td>Boolean</td>
    <td><code>false</code></td>
    <td>Run **all css** through the <code>SCSS</code> compiler (regardless of if it's extension is <code>.css</code>)</code></td>
  </tr>
</table>
______

## CSS Filters
[Read here about Asset Filters](/Introducing_Munee#using-asset-filters)

### Minify Filter
<table>
  <tr>
    <th>Name</th><th>Value</th><th>Description</th>
  </tr>
  <tr>
    <td><code>minify</code></td>
    <td><code>true</code></td>
    <td>Strip all non-essential whitespace.</td>
  </tr>
</table>

### Minify Example

This would minify the css (Strip all non-essential whitespace).
```html
<link rel="stylesheet" href="/css/site.css?minify=true">
```
