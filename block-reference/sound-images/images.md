# Sound & Images > Images

***

> Read our [Image API](http://www.stencyl.com/help/view/image-api) guide for an explanation of these blocks.

***

## Create Images

### Create Blank Image

![blank-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-create.png)

aaa

```
new BitmapData([NUMBER] * Engine.SCALE, [NUMBER] * Engine.SCALE, true, 0)
```

***

### Copy of Image

![copy-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-copy.png)

aaa

```
[IMAGE].clone()
```

***

### Part of Image

![part-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-subimage.png)

aaa

```
getSubImage([IMAGE], [NUMBER], [NUMBER], [NUMBER], [NUMBER])
```

***

### Resized Copy of Image

![resize-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-resize.png)

aaa

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

aaa

```
captureScreenshot()
```

***

### Image from Actor

![actor-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-actor.png)

aaa

```
getImageForActor([ACTOR])
```

***

## From External Sources

### Image from File

![file-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-file.png)

aaa

```
getExternalImage([TEXT])
```

***

### Load Image from URL

![url-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-url.png)

aaa

```
loadImageFromURL([TEXT], function(img:BitmapData):Void {
  [ACTIONS]
});
```

***

## Convert Image to/from Text

### Image to Text

![to-text-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-to-text.png)

aaa

```
imageToText([IMAGE])
```

***

### Text to Image

![from-text-image-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/1%20-%20Images/image-from-text.png)

aaa

```
imageFromText([TEXT])
```

***
