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

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
attachImageToActor(image inst, __, Std.int(0), Std.int(0), 1);
```

***

### Attach Image Instance to Layer

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
attachImageToLayer(image inst, 0, "" + "text", Std.int(0), Std.int(0), 1);
```

***

### Attach Image Instance to Screen

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
attachImageToHUD(image inst, Std.int(0), Std.int(0));
```

***

### Remove Image Instance from Parent (the thing it is attached to)

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
removeImage(image inst);
```

***

## Z-Order

### Set Z-Order for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
setOrderForImage(image inst, Std.int(0));
```

***

### Send Image Instance to Different Layer

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
bringImageBack(image inst);
bringImageBack(image inst);
bringImageBack(image inst);
bringImageBack(image inst);
```

***

### Z-Order for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
getOrderForImage(image inst)
```

***

## Properties

### Set Position for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
setXForImage(image inst, 0);
setXForImage(image inst, 0);
```

***

### Set Direction (Angle) for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
image inst.rotation = 0;
```

***

### Resize an Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
image inst.scaleX = (0/100);
image inst.scaleX = (0/100);
```

***

### Set Origin Point for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
setOriginForImage(image inst, 0, 0);
```

***

### Get [Position/Direction/Scale/Opacity] for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
image inst.x/Engine.SCALE
MANY MORE
```

***

## Tweening

### Slide an Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
moveImageBy(image inst, 0, 0, 0, Linear.easeNone);
```

***

### Spin an Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
spinImageBy(image inst, 0, 0, Linear.easeNone);
```

***

### Fade [In/Out] an Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
fadeImageTo(image inst, 0 / 100, 0, Linear.easeNone);
```

***

### [Grow/Shrink] an Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
growImageTo(image inst, 0/100, 0/100, 0, Linear.easeNone);
```

***

## Transforms

### Set Blend Mode for Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
image inst.blendMode = BlendMode.ADD;
```

***

### Apply Effect to Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
setFilterForImage(image inst, effect);
```

***

### Remove All Effects from Image Instance

![create-image-instance-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/3%20-%20Show%20Images/image-inst-create.png)

aaa

```
clearFiltersForImage(image inst);
```

***
