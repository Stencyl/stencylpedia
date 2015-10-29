# Sound & Images > Show Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Display Images

### Create Instance of Image

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

Creates an Image Instance from the given image. Usually assigned to an attribute right away.

```
new BitmapWrapper(new Bitmap([IMAGE]))
```

***

### Attach Image Instance to Actor

![attach-actor-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-actor.png)

Attaches the image instance to the specified actor at the given position.

```
attachImageToActor([IMAGE INSTANCE], [ACTOR], [NUMBER], [NUMBER], 1); // front
attachImageToActor([IMAGE INSTANCE], [ACTOR], [NUMBER], [NUMBER], 2); // behind
```

***

### Attach Image Instance to Layer

![attach-layer-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-layer2.png)

Attaches the image instance to the specified layer (via ID or name) at the given position.

```
attachImageToLayer([IMAGE INSTANCE], 0, [LAYER], [NUMBER], [NUMBER], 1); //front
attachImageToLayer([IMAGE INSTANCE], 0, [LAYER], [NUMBER], [NUMBER], 2); //behind
```

***

### Attach Image Instance to Screen

![attach-screen-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-hud.png)

Attaches the image instance to the HUD layer at the given position. This will make it draw in front of everything and ignore the camera.

```
attachImageToHUD([IMAGE INSTANCE], [NUMBER], [NUMBER]);
```

***

### Remove Image Instance from Parent (the thing it is attached to)

![remove-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-remove.png)

Takes the image instance out of the game (by removing it from the object it is attached to).

```
removeImage([IMAGE INSTANCE]);
```

***

## Z-Order

### Set Z-Order for Image Instance

![set-z-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-z.png)

aaa

```
setOrderForImage([IMAGE INSTANCE], [NUMBER]);
```

***

### Send Image Instance to Different Layer

![switch-layer-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-z-friendly.png)

aaa

```
bringImageBack([IMAGE INSTANCE]);
bringImageBack(image inst);
bringImageBack(image inst);
bringImageBack(image inst);
```

***

### Z-Order for Image Instance

![get-z-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-get-z.png)

aaa

```
getOrderForImage([IMAGE INSTANCE])
```

***

## Properties

### Set Position for Image Instance

![position-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props0.png)

aaa

```
setXForImage([IMAGE INSTANCE], [NUMBER]);
setYForImage([IMAGE INSTANCE], [NUMBER]);
```

***

### Set Direction (Angle) for Image Instance

![direction-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props1.png)

aaa

```
[IMAGE INSTANCE].rotation = [NUMBER];
```

***

### Resize an Image Instance

![resize-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props2.png)

aaa

```
[IMAGE INSTANCE].scaleX = ([NUMBER]/100);
[IMAGE INSTANCE].scaleX = ([NUMBER]/100);
```

***

### Set Origin Point for Image Instance

![origin-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-origin.png)

aaa

```
setOriginForImage([IMAGE INSTANCE], [NUMBER], [NUMBER]);
```

***

### Get [Position/Direction/Scale/Opacity] for Image Instance

![props-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-get-props.png)

aaa

```
[IMAGE INSTANCE].x/Engine.SCALE
MANY MORE
```

***

## Tweening

### Slide an Image Instance

![slide-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-slide.png)

aaa

```
moveImageBy([IMAGE INSTANCE], [NUMBER], [NUMBER], [NUMBER], [EASING]);
```

***

### Spin an Image Instance

![spin-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-spin.png)

aaa

```
spinImageBy([IMAGE INSTANCE], [NUMBER], [NUMBER], [EASING]);
```

***

### Fade [In/Out] an Image Instance

![fade-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-fade.png)

aaa

```
fadeImageTo([IMAGE INSTANCE], [NUMBER] / 100, [NUMBER], [EASING]);
```

***

### [Grow/Shrink] an Image Instance

![grow-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-scale.png)

aaa

```
growImageTo([IMAGE INSTANCE], [NUMBER]/100, [NUMBER]/100, 0, [EASING]);
```

***

## Transforms

### Set Blend Mode for Image Instance

![blend-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-blend.png)

aaa

```
[IMAGE INSTANCE].blendMode = [BLEND MODE];
```

***

### Apply Effect to Image Instance

![effect-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-apply-filter.png)

aaa

```
setFilterForImage([IMAGE INSTANCE], [EFFECT]);
```

***

### Remove All Effects from Image Instance

![remove-effects-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-clear-filter.png)

aaa

```
clearFiltersForImage([IMAGE INSTANCE]);
```

***
