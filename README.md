Animated_GIF
============

#### Javascript library for creating animated GIFs ####

### How to use it? ###

```javascript
var imgs = document.querySelectorAll('img');
var ag = new Animated_GIF();
ag.setSize(320, 240);

for(var i = 0; i < imgs.length; i++) {
    ag.addFrame(imgs[i]);
}

var animatedImage = document.createElement('img');

animatedImage.href = ag.getB64GIF();

document.body.appendChild(animatedImage);

```

### Credits ###

* Anthony Dekker's [NeuQuant](http://members.ozemail.com.au/~dekker/NEUQUANT.HTML) image quantization algorithm which was ported from C into Java by Kevin Weiner and then to [ActionScript 3](http://www.bytearray.org/?p=93) by Thibault Imbert, and to [JavaScript](http://antimatter15.com/wp/2010/07/javascript-to-animated-gif/) by antimatter15, and fixed, patched and revised by [sole](http://soledadpenades.com).
* Dean McNamee's [omggif](https://github.com/deanm/omggif) library - for actually encoding into GIF89
