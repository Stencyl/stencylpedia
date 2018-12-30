# Images > Show Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Display Images

### <a name="image-inst-create"></a> Create Instance of Image

![instance of image](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-inst-create.png)

Creates an Image Instance from the given image. Usually assigned to an attribute right away.

```
new BitmapWrapper(new Bitmap([IMAGE]))
```

***

### <a name="image-inst-actor"></a> Attach Image Instance to Actor

![attach image instance to actor at x int y int at front](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-inst-actor.png)

Attaches the image instance to the specified actor at the given position.

```
attachImageToActor([IMAGE INSTANCE], [ACTOR], [INT], [INT], 1); // front
attachImageToActor([IMAGE INSTANCE], [ACTOR], [INT], [INT], 2); // behind
```

***

### <a name="image-inst-layer2"></a> Attach Image Instance to Layer

![attach image instance to layer id object at x int y int at front](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-inst-layer2.png)

Attaches the image instance to the specified layer (via ID or name) at the given position.

```
attachImageToLayer([IMAGE INSTANCE], cast engine.getLayerById([INT]), [INT], [INT], 1); //front
attachImageToLayer([IMAGE INSTANCE], cast engine.getLayerById([INT]), [INT], [INT], 2); //behind
```

***

### <a name="image-inst-hud"></a> Attach Image Instance to Screen

![attach image instance to screen at x int y int](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-inst-hud.png)

Attaches the image instance to the HUD layer at the given position. This will make it draw in front of everything and ignore the camera.

```
attachImageToHUD([IMAGE INSTANCE], [INT], [INT]);
```

***

### <a name="image-inst-remove"></a> Remove Image Instance from Parent (the thing it is attached to)

![remove image instance from parent](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-inst-remove.png)

Takes the image instance out of the game (by removing it from the object it is attached to).

```
removeImage([IMAGE INSTANCE]);
```

***

## Z-Order

### <a name="image-set-z"></a> Set Z-Order for Image Instance

![set z order for image instance to int](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-set-z.png)

Sets the drawing order (within the layer/actor) for the image instance.

```
setOrderForImage([IMAGE INSTANCE], [INT]);
```

***

### <a name="image-set-z-friendly"></a> Send Image Instance to Different Layer

![send image instance back a layer](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-set-z-friendly.png)

Sets the drawing order (within the layer/actor) for the image instance in a user-friendly way.

```
bringImageBack([IMAGE INSTANCE]);
bringImageForward([IMAGE INSTANCE]);
bringImageToBack([IMAGE INSTANCE]);
bringImagetoFront([IMAGE INSTANCE]);
```

***

### <a name="image-get-z"></a> Z-Order for Image Instance

![z order for image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-get-z.png)

Returns the drawing order (within the layer/actor) for the image instance.

```
getOrderForImage([IMAGE INSTANCE])
```

***

## Properties

### <a name="image-set-props0"></a> Set Position for Image Instance

![set x to number for image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-set-props0.png)

Sets the position of the image instance (relative to the actor/layer it is attached to).

```
setXForImage([IMAGE INSTANCE], [NUMBER]);
setYForImage([IMAGE INSTANCE], [NUMBER]);
```

***

### <a name="image-set-props1"></a> Set Direction (Angle) for Image Instance

![set direction to number degrees for image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-set-props1.png)

Sets the direction (angle, in degrees) of the image instance (relative to the actor/layer it is attached to).

```
[IMAGE INSTANCE].rotation = [NUMBER];
```

***

### <a name="image-set-props2"></a> Resize an Image Instance

![set width to number % for image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-set-props2.png)

Sets the width and height (in percentage) of the image instance. 100% keeps that dimension the same. 200% will double it. 50% will halve it.

```
[IMAGE INSTANCE].scaleX = ([NUMBER]/100);
[IMAGE INSTANCE].scaleY = ([NUMBER]/100);
[IMAGE INSTANCE].alpha = ([NUMBER]/100);
```

***

### <a name="image-origin"></a> Set Origin Point for Image Instance

![set origin to x number y number for image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-origin.png)

Sets the origin (pivot) point for the image instance. This affects how it's scaled and rotated.

```
setOriginForImage([IMAGE INSTANCE], [NUMBER], [NUMBER]);
```

***

### <a name="image-get-props"></a> Get Position / Direction / Scale / Opacity for Image Instance

![get x for image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-get-props.png)

Returns various properties for the image instance.

```
[IMAGE INSTANCE].x/Engine.SCALE
[IMAGE INSTANCE].y/Engine.SCALE
[IMAGE INSTANCE].rotation
[IMAGE INSTANCE].width/Engine.SCALE
[IMAGE INSTANCE].height/Engine.SCALE
[IMAGE INSTANCE].scaleX*100
[IMAGE INSTANCE].scaleY*100
[IMAGE INSTANCE].alpha
```

***

## Tweening

### <a name="image-tween-slide"></a> Slide an Image Instance

![slide image instance by x number y number over number sec using dropdown](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-tween-slide.png)

Slides (moves) the image instance over the specified time.

```
moveImageBy([IMAGE INSTANCE], [NUMBER], [NUMBER], [NUMBER], [EASING]);
moveImageTo([IMAGE INSTANCE], [NUMBER], [NUMBER], [NUMBER], [EASING]);
```

***

### <a name="image-tween-spin"></a> Spin an Image Instance

![spin image instance by number degrees over number sec using dropdown](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-tween-spin.png)

Spins (rotates) the image instance over the specified time.

```
spinImageBy([IMAGE INSTANCE], [NUMBER], [NUMBER], [EASING]);
spinImageTo([IMAGE INSTANCE], [NUMBER], [NUMBER], [EASING]);
```

***

### <a name="image-tween-fade"></a> Fade In / Out an Image Instance

![fade image instance to number % over number sec using dropdown](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-tween-fade.png)

[Fades In / Fades Out] the image instance over the specified time.

```
fadeImageTo([IMAGE INSTANCE], [NUMBER] / 100, [NUMBER], [EASING]);
```

***

### <a name="image-tween-scale"></a> Grow / Shrink an Image Instance

![grow image instance to w number % h number % over number sec using dropdown](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-tween-scale.png)

Resizes the image instance in percentage terms over the specified time. 100% keeps that dimension the same. 200% will double it. 50% will halve it.

```
growImageTo([IMAGE INSTANCE], [NUMBER]/100, [NUMBER]/100, [NUMBER], [EASING]);
```

***

## Transforms

### <a name="image-blend"></a> Set Blend Mode for Image Instance

![set blend mode for image instance to dropdown](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-blend.png)

Changes the blending mode for the image instance.

```
[IMAGE INSTANCE].blendMode = [BLEND MODE];
```

***

### <a name="image-apply-filter"></a> Apply Effect to Image Instance

![apply effect filter to image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-apply-filter.png)

Applies the specified effect to the image instance. The effect persists until removed, so you do not need to call this each frame.

```
setFilterForImage([IMAGE INSTANCE], [EFFECT]);
```

***

### <a name="image-clear-filter"></a> Remove All Effects from Image Instance

![remove all effects from image instance](http://static.stencyl.com/pedia2/block-images/sound-images/show-images/image-clear-filter.png)

Removes all effects from the image instance.

```
clearFiltersForImage([IMAGE INSTANCE]);
```

***
