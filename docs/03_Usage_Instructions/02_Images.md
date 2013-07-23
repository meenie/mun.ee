Using *Munee*, you can resize/crop/stretch/fill images on-the-fly using a set of arguments.  The resulting image will be cached and served up on subsequent requests.  If the source image is modified, it will recreate the cache and invalidate the client side cache and force the browser to download the newest version.
_______

## Security

When using an on-the-fly image resizing tool like this, there is an inherent risk that someone will try and exploit it to try and resize a photo a thousand different ways to take down your server.
*Munee* has a couple of ways to minimise this risk a great deal.  One is it checks that the referer is set and is coming from the same domain that the image is located on.  Another is it only allows 3 resizes of an image within a 5 minute time span. Both of these features can be either turned off or changed within the dispatcher settings.
_______

## Dispatcher Options

These options can be set in the first parameter of the `Request` class in the dispatcher file. For example:

```php
echo \Munee\Dispatcher::run(new \Munee\Request(array('image' => array('checkReferrer' => false))));
```

<table>
  <tr>
    <th>Name</th><th>Type</th><th>Default</th><th>Description</th>
  </tr>
  <tr>
    <td><code>checkReferrer</code></td>
    <td>Boolean</td>
    <td><code>true</code></td>
    <td>Check to make sure the referer matches the same domain where the image is hosted</td>
  </tr>
  <tr>
    <td><code>numberOfAllowedFilters</code></td>
    <td>Integer</td>
    <td><code>3</code></td>
    <td>How many filters can be done within the <code>allowedFiltersTimeLimit</code></td>
  </tr>
  <tr>
    <td><code>allowedFiltersTimeLimit</code></td>
    <td>Integer</td>
    <td><code>300</code></td>
    <td>Number of seconds before another resize can happen after the <code>numberOfAllowedFilters</code> has been reached</td>
  </tr>
  <tr>
    <td><code>imageProcessor</code></td>
    <td>String</td>
    <td><code>GD</code></td>
    <td>Which image processor to use. Values can be: <code>GD</code>, <code>Imagick</code>, <code>Gmagick</code></td>
  </tr>
  <tr>
    <td><code>placeholders</code></td>
    <td>Boolean|Array</td>
    <td><code>false</code></td>
    <td>Setup placeholders to be used for any images are missing. Placeholder services like http://placedog.com can be used as well. <a href="#placeholders">Examples can be found below</a>.</td>
  </tr>
</table>
______

## Image Filters
[Read here about Asset Filters](/Introducing_Munee#using-asset-filters)

### Resize Filter
<table>
  <tr>
    <th>Name</th><th>Value</th><th>Description</th>
  </tr>
  <tr>
    <td><code>resize</code></td>
    <td>Arguments</td>
    <td>The resize filter can resize/crop/fill images.</td>
  </tr>
</table>

### Resize Arguments
<table>
  <tr>
    <th>Name</th><th>Type</th><th>Default</th><th>Description</th>
  </tr>
  <tr>
    <td><code>height</code> (or <code>h</code>)</td>
    <td>Integer</td>
    <td>N/A</td>
    <td>The max height you want the image.</td>
  </tr>
  <tr>
    <td><code>width</code> (or <code>w</code>)</td>
    <td>Integer</td>
    <td>N/A</td>
    <td>The max width you want the image.</td>
  </tr>
  <tr>
    <td><code>exact</code> (or <code>e</code>)</td>
    <td>Boolean</td>
    <td><code>false</code></td>
    <td>Crop the image to the exact <code>height</code> and <code>width</code>.</td>
  </tr>
  <tr>
    <td><code>stretch</code> (or <code>s</code>)</td>
    <td>Boolean</td>
    <td><code>false</code></td>
    <td>Stretch the image to match the exact <code>height</code> and <code>width</code>.</td>
  </tr>
  <tr>
    <td><code>fill</code> (or <code>f</code>)</td>
    <td>Boolean</td>
    <td><code>false</code></td>
    <td>Draw a background the exact size of the <code>height</code> and <code>width</code> and centre the image in the middle. (If you do not want the image to be stretched, then do not use the <code>stretch</code> argument along with <code>fill</code>).</td>
  </tr>
  <tr>
    <td><code>fillColour</code> (or <code>fc</code>)</td>
    <td>HEX Colour (without #)</td>
    <td><code>FFFFFF</code></td>
    <td>This works in conjunction with <code>fill</code>. The colour of the filled in background.</td>
  </tr>
  <tr>
    <td><code>quality</code> (or <code>q</code>)</td>
    <td>Integer</td>
    <td><code>75</code></td>
    <td>JPEG compression value.</td>
  </tr>
</table>

**Note:** Boolean arguments can use `true`, `t`, `yes`, `y` for `truthy` values and `false`, `f`, `no`, `n` for `falsey` values.


### Resize Examples

Resize an image to a specific width and keep it's correct aspect ratio. **Note:** This is using the long form of the arguments.

```html
<img src="/img/my-image.jpg?resize=width[250]">
```

Resize an image and keep it's correct aspect ratio but neither width or height can be bigger than specified.

```html
<img src="/img/my-image.jpg?resize=width[100]-height[50]">
```

Crop an image to an exact size.  If the image is smaller than the provided dimensions, it will not stretch or fill the image out to match the height and width. **Note:** This is using the shortened form of the arguments.

```html
<img src="/img/my-image.jpg?resize=w[100]h[85]e[true]">
```

Crop an image and stretch it to an exact size.

```html
<img src="/img/my-image.jpg?resize=w[200]h[300]e[true]s[true]">
```

Resize an image and put it on dark grey background the exact size of the dimensions.

```html
<img src="/img/my-image.jpg?resize=w[500]h[500]f[true]fc[444444]">
```
______

### Colorize Filter
<table>
  <tr>
    <th>Name</th><th>Value</th><th>Description</th>
  </tr>
  <tr>
    <td><code>colorize</code></td>
    <td>HEX Color (without #)</td>
    <td>Applies the <a href="http://imagine.readthedocs.org/en/latest/usage/effects.html#colorize" target="_blank">Imagine Colorize Effect</a>.</td>
  </tr>
</table>

### Colorize Example

This would put a red overlay on the image.
```html
<img src="/img/my-image.jpg?colorize=FF0000">
```
______

### Grayscale Filter
<table>
  <tr>
    <th>Name</th><th>Value</th><th>Description</th>
  </tr>
  <tr>
    <td><code>grayscale</code></td>
    <td><code>true</code></td>
    <td>Applies the <a href="http://imagine.readthedocs.org/en/latest/usage/effects.html#grayscale" target="_blank">Imagine Grayscale Effect</a>.</td>
  </tr>
</table>

### Grayscale Example

This would convert the image to grayscale.
```html
<img src="/img/my-image.jpg?grayscale=true">
```
______

### Negative Filter
<table>
  <tr>
    <th>Name</th><th>Value</th><th>Description</th>
  </tr>
  <tr>
    <td><code>negative</code></td>
    <td><code>true</code></td>
    <td>Applies the <a href="http://imagine.readthedocs.org/en/latest/usage/effects.html#negative" target="_blank">Imagine Negative Effect</a>.</td>
  </tr>
</table>

### Negative Example

This would covert the image to it's negative form.
```html
<img src="/img/my-image.jpg?negative=true">
```
________

<h2 id="placeholders">Placeholders</h2>

A new feature in *Munee* is being able to use image placeholders for missing images. This is a great feature to have if you are designer just starting a new site and don't necessarily have all of your images available.  You can specify a specific image or use one of the numerous image placeholder websites out there like http://placedog.com.

You can also specify different image paths for different placeholder images as well. So if you want a different image for all of your /img/category/* images and another for all of your /img/product/* images, it's very easy to do.

**Note:** When specifying which images on your site you want to use placeholders for, you can use a wildcard (*) reference.

```php
// Use a specific image for all missing images.
echo \Munee\Dispatcher::run(
    new \Munee\Request(array(
        'image' => array(
            'placeholders' => array(
                '*' => WEBROOT . DS . 'img' . DS . 'placeholder-image.jpg'
            )
        )
    ))
);
```

```php
/**
 * Use a placeholder for all generic images, a specific placeholder for product images,
 * and a placeholder service for category images.
 * /img/category/missing-image.jpg --> Pulls in a random puppy image
 * /img/product/missing-image.jpg --> Uses /img/missing-product.image.jpg
 * /img/wherever-else/missing-image.jpg --> Uses /img/placeholder-image.jpg
 */
echo \Munee\Dispatcher::run(
    new \Munee\Request(array(
        'image' => array(
            'placeholders' => array(
                '/category/*' => 'http://placedog.com/1024/768',
                '/product/*' => WEBROOT . DS . 'img' . DS . 'missing-product-image.jpg',
                '*' => WEBROOT . DS . 'img' . DS . 'placeholder-image.jpg'
            )
        )
    ))
);
```