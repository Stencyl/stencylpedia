# Sound & Images > Show Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Display Images

### Create Instance of Image

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
new BitmapWrapper(new Bitmap(image))
```

***

### Attach Image Instance to Actor

![attach-actor-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-actor.png)

aaa

```
attachImageToActor(image inst, __, Std.int(0), Std.int(0), 1);
```

***

### Attach Image Instance to Layer

![attach-layer-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-layer2.png)

aaa

```
attachImageToLayer(image inst, 0, "" + "text", Std.int(0), Std.int(0), 1);
```

***

### Attach Image Instance to Screen

![attach-screen-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-hud.png)

aaa

```
attachImageToHUD(image inst, Std.int(0), Std.int(0));
```

***

### Remove Image Instance from Parent (the thing it is attached to)

![remove-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-remove.png)

aaa

```
removeImage(image inst);
```

***

## Z-Order

### Set Z-Order for Image Instance

![set-z-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-z.png)

aaa

```
setOrderForImage(image inst, Std.int(0));
```

***

### Send Image Instance to Different Layer

![switch-layer-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-z-friendly.png)

aaa

```
bringImageBack(image inst);
bringImageBack(image inst);
bringImageBack(image inst);
bringImageBack(image inst);
```

***

### Z-Order for Image Instance

![get-z-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-get-z.png)

aaa

```
getOrderForImage(image inst)
```

***

## Properties

### Set Position for Image Instance

![position-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props0.png)

aaa

```
setXForImage(image inst, 0);
setXForImage(image inst, 0);
```

***

### Set Direction (Angle) for Image Instance

![direction-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props1.png)

aaa

```
image inst.rotation = 0;
```

***

### Resize an Image Instance

![resize-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-set-props2.png)

aaa

```
image inst.scaleX = (0/100);
image inst.scaleX = (0/100);
```

***

### Set Origin Point for Image Instance

![origin-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-origin.png)

aaa

```
setOriginForImage(image inst, 0, 0);
```

***

### Get [Position/Direction/Scale/Opacity] for Image Instance

![props-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-get-props.png)

aaa

```
image inst.x/Engine.SCALE
MANY MORE
```

***

## Tweening

### Slide an Image Instance

![slide-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-slide.png)

aaa

```
moveImageBy(image inst, 0, 0, 0, Linear.easeNone);
```

***

### Spin an Image Instance

![spin-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-spin.png)

aaa

```
spinImageBy(image inst, 0, 0, Linear.easeNone);
```

***

### Fade [In/Out] an Image Instance

![fade-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-fade.png)

aaa

```
fadeImageTo(image inst, 0 / 100, 0, Linear.easeNone);
```

***

### [Grow/Shrink] an Image Instance

![grow-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-tween-scale.png)

aaa

```
growImageTo(image inst, 0/100, 0/100, 0, Linear.easeNone);
```

***

## Transforms

### Set Blend Mode for Image Instance

![blend-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-blend.png)

aaa

```
image inst.blendMode = BlendMode.ADD;
```

***

### Apply Effect to Image Instance

![effect-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-apply-filter.png)

aaa

```
setFilterForImage(image inst, effect);
```

***

### Remove All Effects from Image Instance

![remove-effects-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-clear-filter.png)

aaa

```
clearFiltersForImage(image inst);
```

***
