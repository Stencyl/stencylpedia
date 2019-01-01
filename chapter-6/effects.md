## Contents

* What are Effects?
* Demo
* Effects & Performance
* Gotchas


## What are Effects?

Effects let you add visual flair to actors (and [images](http://www.stencyl.com/help/view/image-api)), without having to add new animations or additional code to the game. All effect-related blocks are located under **Actor > Effects**.

![Effect Blocks in Palette](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/effects-1.png)


## Demo

The following demo demonstrates all of the available effects in Stencyl.

<embed allowscriptaccess="never" height="640" quality="high" src="http://static.stencyl.com/pedia2/ch6/effects/EffectsSandbox.swf" type="application/x-shockwave-flash" width="640"></embed>


## Effects and Performance

**Don't continually re-apply effects every frame of the game.**

This will drain performance because the underlying images for the Actor's animation will continually be re-generated per-frame.

Effects in themselves are not performance impacting. It's the application of effects that takes relatively long.

 
## Gotchas

* Effects persist, even when an Actor's animation changes.
* Only 1 effect may be applied at a time to a particular actor or image. To apply several, use the apply block multiple times.
 

## Summary

* Use effects to add visual flair without importing new animations.
* Use effects responsibly to maintain good performance.
