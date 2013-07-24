*Munee* can be used to minify JavaScript as well as compile CoffeeScript into JavaScript on-the-fly. The only thing you need to do for the CoffeeScript to be comiled is set the extension of your file to `.coffee` and link it to your document.
________

<h2 id="dispatcher-options">Dispatcher Options</h2>

These options can be set in the first parameter of the `Request` class in the dispatcher file. For example:

```php
echo \Munee\Dispatcher::run(new \Munee\Request(array('javascript' => array('packer' => array('fastDecode' => false))));
```

<table>
  <tr>
    <th>Name</th><th>Type</th><th>Default</th><th>Description</th>
  </tr>
  <tr>
    <td><code>packer</code></td>
    <td>Array</td>
    <td>N/A</td>
    <td>
        Set options for the <a href="http://joliclic.free.fr/php/javascript-packer/en/" target="_blank">Packer Library</a><br>
        The parameters are:
        <ul>
            <li><code>encoding</code> (Default: 62) -  level of encoding, int or string : 0,10,62,95 or 'None', 'Numeric', 'Normal', 'High ASCII'</li>
            <li><code>fastDecode</code> (Default: true) - include the fast decoder in the packed result</li>
            <li><code>specialChars</code> (Default: false) - if you flagged your private and local variables in the script</li>
        </ul>
    </td>
  </tr>
</table>
_________

## JavaScript Filters
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

This would convert the image to grayscale.
```html
<script src="/js/libs/jquery-1.8.1.min.js,/js/libs/bootstrap.min.js,/js/site.js?minify=true"></script>
```
_______

### Packer Filter
<table>
  <tr>
    <th>Name</th><th>Value</th><th>Description</th>
  </tr>
  <tr>
    <td><code>packer</code></td>
    <td><code>true</code></td>
    <td>Run the javascript through the <a href="http://joliclic.free.fr/php/javascript-packer/en/" target="_blank">Packer Library</a>.</td>
  </tr>
</table>

**Note:** You can set a couple of different options for Packer above in the [Dispatcher Options](#dispatcher-options).

### Packer Example

This would convert the image to grayscale.
```html
<script src="/js/site.js?packer=true"></script>
```

**Note:** It would probably not be wise to run the javascript through the `minify` and `packer` filters at the same time :).