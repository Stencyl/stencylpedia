# Sound & Images > Change Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Draw on Image

### Draw Image onto Image

![draw-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-draw.png)

Draws an image

```
drawImageOnImage([IMAGE], [IMAGE], [NUMBER], [NUMBER], [BLEND MODE]);
```

***

### Draw Text onto Image

![draw-text-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-draw-text.png)

aaa

```
drawTextOnImage([IMAGE], [TEXT], [NUMBER], [NUMBER], [FONT]);
```

***

### Fill Image with Color

![fill-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-fill.png)

aaa

```
fillImage([IMAGE], [COLOR]);
```

***

### Make Color (from RGB)

![rgb-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/rgb-to-color.png)

aaa

```
Utils.getColorRGB([NUMBER], [NUMBER], [NUMBER])
```

***

## Clear Image

### Clear Part of Image

![clear-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-clear.png)

aaa

```
clearImagePartially([IMAGE], [NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### Clear Whole Image

![clear-full-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-clear-all.png)

aaa

```
clearImage([IMAGE]);
```

***

### Clear Image using Mask

![mask-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-mask.png)

aaa

```
clearImageUsingMask([IMAGE], [IMAGE], [NUMBER], [NUMBER]);
```

***

## Transform Image

### Apply Effect to Image

![effect-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-filter.png)

aaa

```
filterImage([IMAGE], [EFFECT]);
```

***

### Flip Image

![flip-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-flip.png)

aaa

```
flipImageHorizontal([IMAGE]);
```

***

### Swap Colors in Image

![swap-color-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-swap.png)

aaa

```
imageSwapColor([IMAGE], [COLOR], [COLOR]);
```

***

## Pixel Operations

### Batch Draw (Pixels)

![batch-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-wrapper.png)

aaa

```
[IMAGE].lock();
[ACTIONS]
[IMAGE].unlock();
```

***

### Set Pixel

![set-pixel-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-set-px.png)

aaa

```
imageSetPixel([IMAGE], [NUMBER], [NUMBER], [COLOR]);
```

***

### Draw Image onto Image

![get-pixel-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-get-px.png)

aaa

```
imageGetPixel([IMAGE], [NUMBER], [NUMBER])
```

***
