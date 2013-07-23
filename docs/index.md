<p class="lead">
    <strong>Munee</strong> is a PHP5.3 library to easily on-the-fly compile LESS, SCSS, or CoffeeScript,
    resize/manipulate images on-the-fly, minify CSS and JS, and cache assets locally and remotely for lightening fast
    requests. No need to change how you include your assets in your templates.
    <br><br>Just follow the couple of <a href="/Installation_Instructions">installation instructions here</a> and you are ready to go!
</p>

<hr/>
<h3>Features</h3>
<hr/>
<div class="row features">
    <div class="span5"><i class="feature-icon icon-flag"></i>

        <h4>Easy To Install &amp; Use</h4>

        <p>
            Using <a href="http://getcomposer.org" target="_blank">Composer</a>, <em><strong>Munee</strong></em> can be
            installed in 3 easy steps.
            You will not have to change how you include your assets, everything just works!
        </p>
    </div>
    <div class="span5"><i class="feature-icon icon-magic"></i>

        <h4>Smart Caching</h4>

        <p>
            Assets are cached server-side and client-side. On every request, each asset is checked if a newer version
            is available. If so, <em><strong>Munee</strong></em> will bust the cache and force the browser to download
            the latest version.
        </p>
    </div>
</div>
<div class="row features">
    <div class="span5"><i class="feature-icon icon-resize-full"></i>

        <h4>On-The-Fly Image Resizing</h4>

        <p>
            Quickly resize/crop/fill images on the fly utilising <a target="_blank" href="http://imagine.readthedocs.org/en/latest/">Imagine</a>
            and an easy to use parameter syntax. Once the image has
            been manipulated, the cached version will be served on the next request. Security measures are put in place
            to stop malicious users in their tracks.
        </p>
    </div>
    <div class="span5"><i class="feature-icon icon-cogs"></i>

        <h4>LESS/SCSS/CoffeeScript Compiling</h4>

        <p>
            Just include these assets (<code>.less, .scss, .coffee</code>) to your HTML and
            <em><strong>Munee</strong></em>
            will automatically compile and cache them for future requests.
        </p>
    </div>
</div>
<div class="row features">
    <div class="span5"><i class="feature-icon icon-signin"></i>

        <h4>Combine CSS/JS Into One Request</h4>

        <p>
            When creating your <code>&lt;link&gt;</code> and <code>&lt;style&gt;</code> tags, you can comma delimit
            each file into one request. <em><strong>Munee</strong></em> will cache each file individually and combine
            each files content.
        </p>
    </div>
    <div class="span5"><i class="feature-icon icon-resize-small"></i>

        <h4>Minification &amp; Gzip Compression</h4>

        <p>
            The CSS &amp; JavaScript can optionally be minified to save on bandwidth. <em><strong>Munee</strong></em>
            will also use
            <code>ob_gzhandler()</code> to Gzip the response to save even more bandwidth.
        </p>
    </div>
</div>

<div class="clear"></div>
<hr/>