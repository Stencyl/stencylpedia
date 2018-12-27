# Sound & Images > Show Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Display Images

### <a name="image-inst-create"></a> Create Instance of Image

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

Creates an Image Instance from the given image. Usually assigned to an attribute right away.

```
new BitmapWrapper(new Bitmap([IMAGE]))
```

***

### <a name="image-inst-actor"></a> Attach Image Instance to Actor

![attach-actor-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-actor.png)

Attaches the image instance to the specified actor at the given position.

```
attachImageToActor([IMAGE INSTANCE], [ACTOR], [NUMBER], [NUMBER], 1); // front
attachImageToActor([IMAGE INSTANCE], [ACTOR], [NUMBER], [NUMBER], 2); // behind
```

***

### <a name="image-inst-layer2"></a> Attach Image Instance to Layer

![attach-layer-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-layer2.png)

Attaches the image instance to the specified layer (via ID or name) at the given position.

```
attachImageToLayer([IMAGE INSTANCE], 0, [LAYER], [NUMBER], [NUMBER], 1); //front
attachImageToLayer([IMAGE INSTANCE], 0, [LAYER], [NUMBER], [NUMBER], 2); //behind
```

***

### <a name="image-inst-hud"></a> Attach Image Instance to Screen

![attach-screen-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-hud.png)

Attaches the image instance to the HUD layer at the given position. This will make it draw in front of everything and ignore the camera.

```
attachImageToHUD([IMAGE INSTANCE], [NUMBER], [NUMBER]);
```

***

### <a name="image-inst-remove"></a> Remove Image Instance from Parent (the thing it is attached to)

![remove-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-remove.png)

Takes the image instance out of the game (by removing it from the object it is attached to).

```
removeImage([IMAGE INSTANCE]);
```

***

## Z-Order

### <a name="image-set-z"></a> Set Z-Order for Image Instance

![set-z-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-z.png)

Sets the drawing order (within the layer/actor) for the image instance.

```
setOrderForImage([IMAGE INSTANCE], [NUMBER]);
```

***

### <a name="image-set-z-friendly"></a> Send Image Instance to Different Layer

![switch-layer-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-z-friendly.png)

Sets the drawing order (within the layer/actor) for the image instance in a user-friendly way.

```
bringImageBack([IMAGE INSTANCE]);
bringImageForward([IMAGE INSTANCE]);
bringImageToFront([IMAGE INSTANCE]);
bringImageToBack([IMAGE INSTANCE]);
```

***

### <a name="image-get-z"></a> Z-Order for Image Instance

![get-z-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-get-z.png)

Returns the drawing order (within the layer/actor) for the image instance.

```
getOrderForImage([IMAGE INSTANCE])
```

***

## Properties

### <a name="image-set-props0"></a> Set Position for Image Instance

![position-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props0.png)

Sets the position of the image instance (relative to the actor/layer it is attached to).

```
setXForImage([IMAGE INSTANCE], [NUMBER]);
setYForImage([IMAGE INSTANCE], [NUMBER]);
```

***

### <a name="image-set-props1"></a> Set Direction (Angle) for Image Instance

![direction-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props1.png)

Sets the direction (angle, in degrees) of the image instance (relative to the actor/layer it is attached to).

```
[IMAGE INSTANCE].rotation = [NUMBER];
```

***

### <a name="image-set-props2"></a> Resize an Image Instance

![resize-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props2.png)

Sets the width and height (in percentage) of the image instance. 100% keeps that dimension the same. 200% will double it. 50% will halve it.

```
[IMAGE INSTANCE].scaleX = ([NUMBER]/100);
[IMAGE INSTANCE].scaleY = ([NUMBER]/100);
```

***

### <a name="image-origin"></a> Set Origin Point for Image Instance

![origin-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-origin.png)

Sets the origin (pivot) point for the image instance. This affects how it's scaled and rotated.

```
setOriginForImage([IMAGE INSTANCE], [NUMBER], [NUMBER]);
```

***

### <a name="image-get-props"></a> Get Position / Direction / Scale / Opacity for Image Instance

![props-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-get-props.png)

Returns various properties for the image instance.

```
[IMAGE INSTANCE].x
[IMAGE INSTANCE].y
[IMAGE INSTANCE].rotation
[IMAGE INSTANCE].width
[IMAGE INSTANCE].height
[IMAGE INSTANCE].width/100
[IMAGE INSTANCE].height/100
[IMAGE INSTANCE].alpha
```

***

## Tweening

### <a name="image-tween-slide"></a> Slide an Image Instance

![slide-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-slide.png)

Slides (moves) the image instance over the specified time.

```
moveImageBy([IMAGE INSTANCE], [NUMBER], [NUMBER], [NUMBER], [EASING]);
```

***

### <a name="image-tween-spin"></a> Spin an Image Instance

![spin-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-spin.png)

Spins (rotates) the image instance over the specified time.

```
spinImageBy([IMAGE INSTANCE], [NUMBER], [NUMBER], [EASING]);
```

***

### <a name="image-tween-fade"></a> Fade In / Out an Image Instance

![fade-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-fade.png)

[Fades In / Fades Out] the image instance over the specified time.

```
fadeImageTo([IMAGE INSTANCE], [NUMBER] / 100, [NUMBER], [EASING]);
```

***

### <a name="image-tween-scale"></a> Grow / Shrink an Image Instance

![grow-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-scale.png)

Resizes the image instance in percentage terms over the specified time. 100% keeps that dimension the same. 200% will double it. 50% will halve it.

```
growImageTo([IMAGE INSTANCE], [NUMBER]/100, [NUMBER]/100, [NUMBER], [EASING]);
```

***

## Transforms

### <a name="image-blend"></a> Set Blend Mode for Image Instance

![blend-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-blend.png)

Changes the blending mode for the image instance.

```
[IMAGE INSTANCE].blendMode = [BLEND MODE];
```

***

### <a name="image-apply-filter"></a> Apply Effect to Image Instance

![effect-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-apply-filter.png)

Applies the specified effect to the image instance. The effect persists until removed, so you do not need to call this each frame.

```
setFilterForImage([IMAGE INSTANCE], [EFFECT]);
```

***

### <a name="image-clear-filter"></a> Remove All Effects from Image Instance

![remove-effects-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-clear-filter.png)

Removes all effects from the image instance.

```
clearFiltersForImage([IMAGE INSTANCE]);
```

***
