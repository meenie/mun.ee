### Update 1.5.0 Important Note

I have changed the vendor to be uppercase so you will need to update how you instantiate the *Munee* library.  Please follow [step 2 of the installion instructions](/Installation_Instructions#step-2).

### Update 1.3.0 Important Note

In this and future versions of *Munee*, the way CSS is run through the LESS compiler has changed.  By default, only `.less` files will be compiled and you will have to set a special parameter to have all CSS (`.css`) files run through the compiler as well. [See here](/Usage_Instructions/CSS#lessify-all-css) for more instructions. The reason behind this change is technically `.less` files should have only valid LESS in them and `.css` should only have valid CSS in them.