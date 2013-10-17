#### Version 1.5.17
<ul>
<li> Adding in new CompilationException and removing cache file if it is called. Also putting in new relative path fix for CSS stylesheets. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/b83c399176b0a9bcf88fb214338e63f9a896bcbf" target="_blank">b83c399</a></li>
</ul>

#### Version 1.5.16
<ul>
<li> Fixing an issue with relative paths not converting to absolute paths correctly.  This should fix issue #32.  I also implemented the feature requests in issue #24, issue #27, and issue #21. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/52c78f6ddfd816a449f78f821a3b33f582606859" target="_blank">52c78f6</a></li>
</ul>

#### Version 1.5.15
<ul>
<li> - Fixed "PHP Warning: Invalid argument supplied for foreach()" in Image::checkNumberOfAllowedFilters() when glob() returns false - Moved Image::checkNumberOfAllowedFilters() and Image::checkReferrer() calls into Image::setupFile() function - Removed duplicate code in Image::checkCache() &mdash; Alexander Wenzel &bull; <a href="http://github.com/meenie/munee/commit/7b6317b5848417aaf2cd93ddfa651f42b10f602d" target="_blank">7b6317b</a></li>
<li> Changing SASS to SCSS &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/226e03dcb5fcb8c3008ead5d44737779334d1da8" target="_blank">226e03d</a></li>
</ul>

#### Version 1.5.14

<ul>
<li> Putting in fix for directly requesting an unfiltered image triggering`checkReferrer()` when it shouldn't &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/0386f343434c694037560c2ebc98ae17f22fd5b3" target="_blank">0386f34</a></li>
<li> Cementing in the versions of each library dependency. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/90ff6690d5fe94e62ae22c6e00f60fd78e3aca99" target="_blank">90ff669</a></li>
<li> Adding in API link to README file. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/e5df8fadef6727366b5f4e693b55311e4318e614" target="_blank">e5df8fa</a></li>
<li> Fix documentation errors. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/4e8b850bd49aa042933b5dc8748eab93f1c3e295" target="_blank">4e8b850</a></li>
<li> Fixing PhpDoc errors. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/ac86f057974385aab16a788a5e8be7fadb90a384" target="_blank">ac86f05</a></li>
<li> Updating README to remove all extraneous content since it was moved to mun.ee &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/8b4d0874d5a0179619ffa51a668baf2ad1e0d141" target="_blank">8b4d087</a></li>
<li> Putting in Githalytics badge. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/d7091e4a38334a397710cf9187f07d1d4f7f91b7" target="_blank">d7091e4</a></li>
<li> Moved the Bitdeli Badge to the top &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/c140097ba637608b4548b8c29b9a18ff915db1c8" target="_blank">c140097</a></li>
<li> Add a Bitdeli badge to README &mdash; Bitdeli Chef &bull; <a href="http://github.com/meenie/munee/commit/472ebb9162451ecdaefbab1bb8cfdeb2d3cba74a" target="_blank">472ebb9</a></li>
</ul>

#### Version 1.5.13

<ul>
<li> Put in some comments for the new changes. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/c00907fd109a62634f1c55cfdeef6af8fdbb7192" target="_blank">c00907f</a></li>
<li> Don' use ob_gzhandler() if zlib.output_compression ini option is set. &mdash; Kobayakawa &bull; <a href="http://github.com/meenie/munee/commit/8e9563da0ca2c5ea6875bae0c506c2e2d8ea9b9a" target="_blank">8e9563d</a></li>
<li> Don't minify if filename have .min in it &mdash; Kobayakawa &bull; <a href="http://github.com/meenie/munee/commit/8c2b12a6e6c4ccec8895955ce1275024bbf6287d" target="_blank">8c2b12a</a></li>
<li> Don't minify if filename have .min in it &mdash; Kobayakawa &bull; <a href="http://github.com/meenie/munee/commit/4f2ed14b225e5c22173ef221114f72e610c4bbc2" target="_blank">4f2ed14</a></li>
<li> fixing typo &mdash; olliebrennan &bull; <a href="http://github.com/meenie/munee/commit/5fdb14f9a3fe0a60a60b5ea51adab9f8a392b263" target="_blank">5fdb14f</a></li>
<li> Updating composer.json description &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/91be8b3bd13804dbf474708eaf30054bc9713681" target="_blank">91be8b3</a></li>
<li> Updating README with a better description of Munee &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/039cdaed18ca124537fd6acb85ae1c808658920c" target="_blank">039cdae</a></li>
<li> Updating readme with new Known Issues section thanks to issue 15. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/baf3eeb5c8298b551f178f905034892dfb445e36" target="_blank">baf3eeb</a></li>
</ul>

#### Version 1.5.12

<ul>
<li> added NC in the RewriteRule example to make the match case-insensitive (it will match JPG for example) &mdash; Emi Polak &bull; <a href="http://github.com/meenie/munee/commit/8afe0453eba9dbc34fcc0fd9ad9f0db819cead8b" target="_blank">8afe045</a></li>
<li> allow for uppercased asset extensions (such as .JPG) &mdash; Emi Polak &bull; <a href="http://github.com/meenie/munee/commit/aee8019b02f0d67cb7f2751c8c179960197619c0" target="_blank">aee8019</a></li>
</ul>

#### Version 1.5.11

<ul>
<li> Removing extra line. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/eb43072e7a10c5ca458843e024865dbb05ade365" target="_blank">eb43072</a></li>
<li> Update Dispatcher.php &mdash; Alexander &bull; <a href="http://github.com/meenie/munee/commit/796b5cd38b0d77b8043d15336be17338da7f3aa7" target="_blank">796b5cd</a></li>
<li> Adding in better error handling for CSS files.  If they fail to compile, the cache file will now be deleted.  Also the exceptions should now be caught. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/3a4988cc7f7307894272259d8db1328c448b1b57" target="_blank">3a4988c</a></li>
</ul>

#### Version 1.5.9

<ul>
<li> Fixed another PHP5.3 issue. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/7f9680952da6468aaf5716af99f2a7d98a598388" target="_blank">7f96809</a></li>
<li> Fixed a PHP5.3 issue. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/57a83f2b0ad6a22ac9c8884605d4b6e0e0770879" target="_blank">57a83f2</a></li>
<li> Merging in pull request #8 and making some changes. Making the structure more PSR-2 compliant. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/fd16f78a91674051a2b91495f8122e911b498be5" target="_blank">fd16f78</a></li>
<li> Fixing quotes &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/c09866e8c2b9ec4fd73be829ebc921a6eb28c3bf" target="_blank">c09866e</a></li>
<li> Add imageProcessor in options, for optional switch from GD to ImageMagick or GMagick &mdash; Alexey Ch &bull; <a href="http://github.com/meenie/munee/commit/456ac4c34e19ba4d7dac418ce9a9028c1bc43d96" target="_blank">456ac4c</a></li>
<li> fix relative image path for list-style-image css property &mdash; Emi Polak &bull; <a href="http://github.com/meenie/munee/commit/41c2360c79bebcd504dc3a9daad919f87ee891fe" target="_blank">41c2360</a></li>
<li> - Made "WEBROOT" more flexible; it's now able to be set through a setDocroot method. - Removed $_GET dependency and unpredictable alteration of $_GET variables. - Added setFiles method to set file path(s) without needing $_GET['files']. - HTTP headers are no longer set directly through PHP's header() function, but instead go through a (configurable) HeaderSetter class or subclass. - Due to the addition of 'docroot', the CSS _fixRelativeImagePaths had to be changed to prevent bugs when LESS/other files were outside of the web root - though I don't see why this method is needed at all. - Updated unit tests as applicable to the above changes. &mdash; tcopestake &bull; <a href="http://github.com/meenie/munee/commit/2a8a67b2b6ee2df49cea0ff73a5736ca87c085fa" target="_blank">2a8a67b</a></li>
</ul>

#### Version 1.5.7

<ul>
<li> Made the javascript-packer it's own composer package and hosted it on github.  This should fix some issues with Munee not updating passed 1.5.3 &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/e6a2c5ffd9b6051f30e421269f4d864873cd631f" target="_blank">e6a2c5f</a></li>
<li> Added in Dean Edwards' JavaScript Packer &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/5a646e544191cb9a9347eb5b2b2ad716f9261c10" target="_blank">5a646e5</a></li>
<li> Removing some uneeded code &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/84cb192416e1b520063e2b8fb3f625e10eb8136a" target="_blank">84cb192</a></li>
<li> Adding new a couple new filters for images so some effects can applied to them. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/f59faa069c816880dbdaab3b1c3e68718669099f" target="_blank">f59faa0</a></li>
</ul>

#### Version 1.5.3

<ul>
<li> Remove CoffeeScript-PHP header &mdash; Jeremy P &bull; <a href="http://github.com/meenie/munee/commit/2a9bbb6f02c2415aa99a93774a9d470c35ec4124" target="_blank">2a9bbb6</a></li>
<li> Fixing a security issue, putting in fix for BOM issue, fixing bug with image resizing. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/879d09d74d987f8712b85ec2a9fb3e25a48d74e4" target="_blank">879d09d</a></li>
</ul>

#### Version 1.5.1

<ul>
<li> Fixing options keys. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/27af3baa0f690f5c2e67634f90218caa9b333ee6" target="_blank">27af3ba</a></li>
<li> Putting in Flattr button &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/a971de95a6124edb911cce8fc48b4b933a09926d" target="_blank">a971de9</a></li>
</ul>

#### Version 1.5.0

<ul>
<li> Updating the README with an important notice and slightly different installation instructions. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/0b4121c0a86ded3b5cc6b05434bec0157218fa9f" target="_blank">0b4121c</a></li>
<li> Updating Copyright date. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/658e429b965463465676846bb3972ca822c6ec71" target="_blank">658e429</a></li>
<li> Second step to rename directory &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/e0148d0e475d98d0678e5347c3778dd3e802df85" target="_blank">e0148d0</a></li>
<li> First step to rename directory &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/2c0829d37facc0dc69c1aad2c045628b79493169" target="_blank">2c0829d</a></li>
<li> Second step to renaming directories. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/a855981ad5227bba0483ae2828054a1dacf9295a" target="_blank">a855981</a></li>
<li> First step to renaming directories. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/1e133f8f31ee35f38126980ae3c7452e4c892c7d" target="_blank">1e133f8</a></li>
<li> Changing all the namespaces to uppercase. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/317925ae5bdf429abc3b8d25c65b5d1e75661512" target="_blank">317925a</a></li>
<li> Changing Vendor name to uppercase. &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/777b5f09ddc61c13196364685825eb4ef5fe0e14" target="_blank">777b5f0</a></li>
<li> Finish renaming vendor tests folder &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/b27a22d418f9cbd2c29c12a9c646e9d4d9557b99" target="_blank">b27a22d</a></li>
<li> Renaming test vendor folder, first step &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/7bca0725f44fefceb196bb82316cbf6c7c768c00" target="_blank">7bca072</a></li>
<li> Finishing the renaming of vendor folder &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/12fbcb1be267e9bce55af559691ad72cb0e81244" target="_blank">12fbcb1</a></li>
<li> Renaming vendor file to temp name &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/39a684b5147b265c069b74dfa865799672a765cd" target="_blank">39a684b</a></li>
<li> Updating README to fix a typo &mdash; Cody Lundquist &bull; <a href="http://github.com/meenie/munee/commit/f2dcad60f1686224faf2ac584ecbfa3ae865d664" target="_blank">f2dcad6</a></li>
</ul>
