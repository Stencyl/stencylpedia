# Images > Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Image API settings

### <a name="image-autoscale"></a> Toggle Image API Auto-scaling

![enable image api auto scaling](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-autoscale.png)

Set whether Image API output is scaled automatically. This is set to `true` by default. This setting affects how all the blocks below work.

When this is enabled, the coordinates and dimensions passed to all Image API blocks will be scaled by `Engine.SCALE`. By settings this to false, you can use the Image API blocks to manipulate images on a per-pixel basis, no matter how your game is upscaled.

```
imageApiAutoscale = true;
imageApiAutoscale = false;
```

***

## Create Images

### <a name="image-create"></a> Create Blank Image

![blank image with w int h int](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-create.png)

Create a blank image of the specified width and height. Usually assigned to an Image attribute right away.

```
newImage([INT], [INT])
```

***

### <a name="image-copy"></a> Copy of Image

![copy of image](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-copy.png)

Returns a copy of the specified image. This is a true copy, so altering the copy will not affect the original.

```
[IMAGE].clone()
```

***

### <a name="image-subimage"></a> Part of Image

![part of image x int y int w int h int](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-subimage.png)

Returns the specified part of the image as a new image.

```
getSubImage([IMAGE], [INT], [INT], [INT], [INT])
```

***

### <a name="image-resize"></a> Resized Copy of Image

![copy of image at w number % h number % using smoothing](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-resize.png)

Returns a larger (or smaller) copy of the image. Width and height are given as percentages - 100% means keep it the same, 200% means double, 50% means half.

```
//Smoothing
resizeImage([IMAGE], ([NUMBER]/100), ([NUMBER]/100), true)

//No Smoothing
resizeImage([IMAGE], ([NUMBER]/100), ([NUMBER]/100), false)
```

***

## From the Game

### <a name="image-screen"></a> Current Screen as Image

![current screen as image](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-screen.png)

Captures the current screen as an image and returns that. This takes time (it may pause the game for a a tenth of a second), so use it sparingly.

```
captureScreenshot()
```

***

### <a name="image-actor"></a> Image from Actor

![image from actor](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-actor.png)

Returns the current image for the specified actor. (In other words, the exact visual state of the actor at the time that you use this.)

```
getImageForActor([ACTOR])
```

***

## From External Sources

### <a name="image-file"></a> Image from File

![image from file text](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-file.png)

Returns an image that is loaded from a file. Images must be placed into the **extras** subfolder of your game.
Some blocks require the images to be saved with transparency enabled to work properly.

```
getExternalImage([TEXT])
```

***

### <a name="image-url"></a> Load Image from URL

![load image from url text and then do...](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-url.png)

Returns an image that is loaded from a URL. When the image successfully loads, the enclosed blocks will run. Use the embedded `the image` block to refer to the loaded image. If the image does not load, the enclosed blocks will not run.

> For a Flash game you may need to give [permissions](http://www.stencyl.com/help/view/web-flash-security/) to access the web. 

```
loadImageFromURL([TEXT], function(img:BitmapData):Void {
  [ACTIONS]
});
```

***

## Convert Image to/from Text

### <a name="image-to-text"></a> Image to Text

![image as text](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-to-text.png)

Converts an image into text form and returns that. Useful for storing image data on servers (via an HTTP request). This takes time to run (a split second or longer).

```
imageToText([IMAGE])
```

***

### <a name="image-from-text"></a> Text to Image

![text as image](http://static.stencyl.com/pedia2/block-images/sound-images/images/image-from-text.png)

Returns an image that was converted to text using the prior block. This takes time to run (a split second or longer).

```
imageFromText([TEXT])
```

***
