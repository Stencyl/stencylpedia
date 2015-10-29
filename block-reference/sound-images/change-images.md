# Sound & Images > Change Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Draw on Image

### Draw Image onto Image

![draw-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-draw.png)

Draws the first image on top of the second image at the specified location.

```
drawImageOnImage([IMAGE], [IMAGE], [NUMBER], [NUMBER], [BLEND MODE]);
```

***

### Draw Text onto Image

![draw-text-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-draw-text.png)

Draws the given text (using a font) on top of the image at the specified location.

```
drawTextOnImage([IMAGE], [TEXT], [NUMBER], [NUMBER], [FONT]);
```

***

### Fill Image with Color

![fill-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-fill.png)

Replaces all pixels in the image with the given color.

```
fillImage([IMAGE], [COLOR]);
```

***

### Make Color (from RGB)

![rgb-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/rgb-to-color.png)

Creates a color from red, green, blue channels. Numbers must be between [0-255] inclusive.

```
Utils.getColorRGB([NUMBER], [NUMBER], [NUMBER])
```

***

## Clear Image

### Clear Part of Image

![clear-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-clear.png)

Clears out the specified part of the image by making those pixels transparent.

```
clearImagePartially([IMAGE], [NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### Clear Whole Image

![clear-full-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-clear-all.png)

Clears out the entire image by making its pixels transparent.

```
clearImage([IMAGE]);
```

***

### [Clear/Retain] Image using Mask

![mask-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-mask.png)

Clears out the image using the second image as a mask. The second image will "cut out" pixels from the first. If using "retain", will do the opposite -- it will clear out all pixels except for those that are in the mask.

```
clearImageUsingMask([IMAGE], [IMAGE], [NUMBER], [NUMBER]);
retainImageUsingMask([IMAGE], [IMAGE], [NUMBER], [NUMBER]);
```

***

## Transform Image

### Apply Effect to Image

![effect-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-filter.png)

Applies the given [effect](http://www.stencyl.com/help/view/effects/) to the image.

```
filterImage([IMAGE], [EFFECT]);
```

***

### Flip Image

![flip-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-flip.png)

Flips the image horizontally or vertically.

```
flipImageHorizontal([IMAGE]);
flipImageVertical([IMAGE]);
```

***

### Swap Colors in Image

![swap-color-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-swap.png)

Replaces all pixels of the first color with the second color in the image.

```
imageSwapColor([IMAGE], [COLOR], [COLOR]);
```

***

## Pixel Operations

### Batch Draw

![batch-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-wrapper.png)

When setting many pixels at a time, this tells the system not to push an image update until you have finished your work. A must-use for performance reasons.

```
[IMAGE].lock();
[ACTIONS]
[IMAGE].unlock();
```

***

### Set Pixel

![set-pixel-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-set-px.png)

Sets a pixel in the image to the specified color.

```
imageSetPixel([IMAGE], [NUMBER], [NUMBER], [COLOR]);
```

***

### Draw Image onto Image

![get-pixel-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/2%20-%20Change%20Images/image-get-px.png)

Returns the color for the specified pixel in the image.

```
imageGetPixel([IMAGE], [NUMBER], [NUMBER])
```

***
