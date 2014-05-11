#CSSslidy

An auto-generated, responsive CSS image slider

### Use:
* Ensure that all the images you wish to use are exactly the same size.
* Create an element with an `id` of `slidy-container` and an element with an `id` of `slidy` containing your images. Optionally, include caption information.
```html
<div id="slidy-container">
  <figure id="slidy">
    <img src="antelope-canyon.jpg" alt data-caption="Antelope Canyon, Arizona">
     <img src="canyonlands.jpg" alt data-caption="Canyonlands Vista, Arizona" >
     <img src="mesa-arch.jpg" alt data-caption="Mesa Arch sunrise, Moab, Utah">
     <img src="wave-canyon.jpg" alt data-caption="Canyonlands, Arizona">
  </figure>
</div>

```
(The `id` values may be changed and customised in the script)
* Add `cssslidy.js` to the bottom of the page.
* Call `cssSlidy()`:
```html
<script> cssSlidy(); </script>
```

### Customize:
To customize your slidy, pass an options object to the `cssSlidy()` call:
```html
<script>
  cssSlidy({
  	timeOnSlide: 5,
  	timeBetweenSlides: .5,
  	slidyContainerSelector: 'custom-container',
  	slidySelector: 'custom-slidy',
  	captionSource: 'data-caption',
  	captionBackground: 'rgba(0,0,0,0.9)',
  	captionColor: '#ff0',
  	captionFont: 'Brittanic Bold, Hevetica, sans-serif',
  	captionPosition: 'top',
  	captionAppear: 'perm',
  	captionSize: '16px',
  	captionPadding: '1em',
  	fallbackFunction: function(){ alert("Oh noes! You can't animate!"); },
  	cssAnimationName: 'custom-animation'
  });
</script>
```


#### Available options:

Option | Type | Default Value | Description
---|---|---|---
`timeOnSlide` | number | `3` | Amount of time (in seconds) per slide
`timeBetweenSlides` | number | `1` | Amount of time (in seconds) per transition
`slidyContainerSelector` | string | `'#slidy-container'` | Define the *ID* used for the slidy container element
`slidySelector` | string | `'#slidy'` | Define the *ID* used for the slidy element
`slidyDirection` | string | `'left'` | Define the slider direction of travel
`captionSource` | string | `'data-caption'` | Attribute value to use for caption text for the image. Can also be set to `'alt'` or `'none'`
`captionBackground` | string | `'rgba(0,0,0,0.3)'` | Background color for the caption. Takes any valid CSS color value
`captionFont` | string | `'Avenir, Avenir Next, Droid Sans, DroidSansRegular, Corbel, Tahoma, Geneva, sans-serif'` | Font-stack for the caption
`captionColor` | string | `'#fff'` | Caption color: any valid CSS color value
`captionPosition` | string | `'bottom'` | Location of the image caption. Can also be set to `'top'`
`captionAppear` | string | `'slide'` | How the caption appears on mouseover. Can also be set to `'perm'` (permanent) or  `'fade'`
`captionSize` | string | `'1.6rem'` | Font-size of the caption, in any valid CSS length unit
`captionPadding` | string | `'.6rem'` |  Padding within the caption. Takes any valid CSS length value
`fallbackFunction` | function | `function(){}` | Function called if CSS Animation is not supported
`cssAnimationName` | string | `'slidy'` | Name of CSS animation

### Note:

Any added manipulation of the caption `font-size` – such as inside `@media` breakpoints added inside your CSS – will require `important` to overwrite the appearence rules generated by the script. For example:

`@media screen and (max-width: 600px) { #slidy-container figcaption { font-size: 1rem !important; } }`
=======
An auto-generated, responsive CSS image slider
>>>>>>> 277c1e37e2029d75a514354b11e67bbc2f60ad1c
