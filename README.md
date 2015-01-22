jquery-splitFlap
================

jQuery module to transform a div text into splitflap display (airport-like).

[View the Demo &rarr;](http://htmlpreview.github.io/?https://github.com/zemax/jquery-splitFlap/blob/master/demo/index.html)

How to use
----------

``` html
<div class="my-splitflap">Hello World</div>
``` 

``` javascript
$('.my-spliflap').splitFlap();
```

Options
-------

You can pass options to the function

``` javascript
// Default :
$('.my-spliflap').splitFlap({
	image:          'images/chars.png',
	charsMap:       'ABCDEFGHIJKLMNOPQRSTUVWXYZ 0123456789.,!?#@()+-=',
	charWidth:      50,
	charHeight:     100,
	charSubstitute: ' ',
	speed:          3,
	speedVariation: 2,
	textInit:       '',
	autoplay:       true
});
```

### image
The path to the image used by the splitflap.

You will certainly need to change *charsMap*, *charWidth* and *charHeight* if you change this.

### charsMap
The string represented in the image.

### charWidth
The width of a character in the image, in pixels.

### charHeight
The height of a character in the image, in pixels.

### charSubstitute
The character used when the string contains a character not found in the charsMap.

### speed
The speed of the rotation, in letter by seconds.

### speedVariation
Random speed added to the fixed speed.

### textInit
The initial string the animation begin with.

### autoplay
If set to false, you'll need to start the animation manually (see below).

Special options
---------------

If the string 'splitflap' is passed as options on an already existing Splitflaped div, the internal SplitFlap object is returned.

With this object, you can start the animation manually by calling the animate() method.

``` javascript
// Get the animation object and start it manually
$('.my-spliflap').splitFlap('splitflap).animate();
```
