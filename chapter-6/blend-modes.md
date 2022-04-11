## Contents

* What are Blending Modes?
* How to Set the Blending Mode
* Limitations
 

## What are Blending Modes?

When semi-transparent images are drawn (particularly when two or more overlap), the graphics engine has to know how to draw the overlapping area. This is known as blending.

Blending Modes are the equations used to determine how to draw these semi-transparent images. There's no better way to show this than through a live demo.

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0" data="https://static.stencyl.com/pedia2/ch6/blending/ImageBlending.swf" height="384" width="640"><param name="quality" value="high" /><param name="movie" value="https://static.stencyl.com/pedia2/ch6/blending/ImageBlending.swf" /><embed height="384" pluginspage="http://www.macromedia.com/go/getflashplayer" quality="high" src="https://static.stencyl.com/pedia2/ch6/blending/ImageBlending.swf" type="application/x-shockwave-flash" width="640"></embed></object>

Isn't that neat? You may wonder **which blend modes are commonly used**. In reality, the majority of games get by with "**Normal**" (the default), "**Add**" and "**Multiply**."
 

## How to Set the Blending Mode

Blending Modes can be set directly on an actor or an entire layer.

#### Set an Actor's Blending Mode
Use the "set blend mode for Actor" block (Actor > Effects) to change the actor's blend mode.

![stencyl-design-mode-set-blend-mode-block](https://static.stencyl.com/pedia2/ch6/blending/image11.png)

#### Set a Layer's Blending Mode

1. Click on the cog icon for a Layer. <br/> ![stencyl-blend-mode-set-for-layer](https://static.stencyl.com/pedia2/ch6/blending/image10-2.png)

2. Set the Blend Mode in the popup. <br/> ![stencyl-blend-mode-layers-pane](https://static.stencyl.com/pedia2/ch6/blending/image10-3.png)


## Limitations

Blending modes only fully work for Flash games due to limitations with the underlying technology (OpenFL/Lime).

*Some* Blending Modes work on Desktop and Mobile targets but only **Add, Multiply and Screen**. We hope that in the future, OpenFL will support all blending modes on these targets.


## Summary

* Blending Modes determine how semi-transparent images are drawn, particularly when multiple ones overlap.
* View our demo to determine which ones fit your needs. The vast majority of cases just need Normal, Add and Multiply.
* You can apply a blending more to an actor or an entire layer.
