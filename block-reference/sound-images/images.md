# Sound & Images > Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Create Images

### Create Blank Image

![blank-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-create.png)

Create a blank image of the specified width and height. Usually assigned to an Image attribute right away.

```
new BitmapData([NUMBER] * Engine.SCALE, [NUMBER] * Engine.SCALE, true, 0)
```

***

### Copy of Image

![copy-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-copy.png)

Returns a copy of the specified image. This is a true copy, so altering the copy will not affect the original.

```
[IMAGE].clone()
```

***

### Part of Image

![part-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-subimage.png)

Returns the specified part of the image as a new image.

```
getSubImage([IMAGE], [NUMBER], [NUMBER], [NUMBER], [NUMBER])
```

***

### Resized Copy of Image

![resize-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-resize.png)

Returns a larger (or smaller) copy of the image. Width and Height are given as percentages - 100% means keep it the same. 200% means double. 50% means half.

```
//Smoothing
resizeImage([IMAGE], ([NUMBER]/100), ([NUMBER]/100), true)

//No Smoothing
resizeImage([IMAGE], ([NUMBER]/100), ([NUMBER]/100), false)
```

***

## From the Game

### Current Screen as Image

![screen-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-screen.png)

Captures the current screen as an image and returns that. This takes time (it may pause the game for a a tenth of a second), so use it sparingly.

```
captureScreenshot()
```

***

### Image from Actor

![actor-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-actor.png)

Returns the current image for the specified actor. (In other words, the exact visual state of the actor at the time that you use this.)

```
getImageForActor([ACTOR])
```

***

## From External Sources

### Image from File

![file-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-file.png)

Returns an image that is loaded from a file. Images must be placed into the **extras** subfolder of your game.

```
getExternalImage([TEXT])
```

***

### Load Image from URL

![url-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-url.png)

Returns an image that is loaded from a URL. When the image successfully loads, the enclosed blocks will run. Use the embedded `the image` block to refer to the loaded image. If the image does not load, the enclosed blocks will not run.

```
loadImageFromURL([TEXT], function(img:BitmapData):Void {
  [ACTIONS]
});
```

***

## Convert Image to/from Text

### Image to Text

![to-text-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-to-text.png)

Converts an image into text form and returns that. Useful for storing image data on servers (via an HTTP request). This takes time to run (a split second or longer).

```
imageToText([IMAGE])
```

***

### Text to Image

![from-text-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-from-text.png)

Returns an image that was converted to text using the prior block. This takes time to run (a split second or longer).

```
imageFromText([TEXT])
```

***
