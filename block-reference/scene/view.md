# Scene > View

***

## Screen Bounds

### Camera Position

![screen-xy](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/screen-xy.png)

Returns the camera's horizontal (X) or vertical (Y) position.

```
getScreenX()
getScreenY()
```

***

### Screen Size

![screen-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/screen-wh.png)

Returns the game's screen width/height.

```
getScreenWidth()
getScreenHeight()
```

***

## Camera

### Move Camera

![camera-move](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/camera-move.png)

Moves the camera to the given point.

```
engine.moveCamera([NUMBER], [NUMBER]);
```

***

### Move Camera to Actor

![camera-follow](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/camera-follow.png)

Moves the camera to the given actor's location.

```
engine.cameraFollow([ACTOR]);
```

***

## Effects

### Shake Screen

![shake-start](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/shake-start.png)

Shakes the screen for the specified time. Good for conveying explosions or earthquakes. Intensity specifies how "violent" the shaking is.

```
startShakingScreen([NUMBER] / 100, [NUMBER]);
```

***

### Stop Shaking Screen

![shake-stop](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/shake-stop.png)

Immediately stop shaking the screen.

```
stopShakingScreen();
```

***

### Toggle Full-Screen Mode

![toggle-fullscreen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/toggle-fullscreen.png)

Enables/Disables full-screen mode for Flash & Desktop targets.

```
toggleFullScreen();
```

***

## Color Background

### Set Background to Color

![set-color-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-color-bg.png)

Changes the background color to a solid color. (if you don't have an image background covering it up)

```
setColorBackground([COLOR]);
```

***

### Set Background to Gradient

![set-grad-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-grad-bg.png)

Changes the background color to a vertical gradient. (if you don't have an image background covering it up)

```
setColorBackground([COLOR], [COLOR]);
```

***

## Layer Properties

### Set Autoscroll Speed (for layer)

![set-bg-speed](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-bg-speed.png)

Changes the speed that the specified background layer scrolls at (must have already been a scrolling background).

```
setScrollSpeedForBackground(0, [TEXT], [NUMBER], [NUMBER]); //specify a layer ID
setScrollSpeedForBackground(1, [TEXT], [NUMBER], [NUMBER]); //specify a layer name
```

***

### Set Scroll Factor for (for layer)

![set-layer-scrollfactor](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-layer-scrollfactor.png)

Change the speed at which a layer scrolls, as a percentage of the baseline.

```
setScrollFactorForLayer(0, "" + "text", 0, 0); //specify a layer ID
```

***

### [Show/Hide] Layer

![showhide-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/showhide-layer2.png)

Shows/Hides the given layer.

```
hideTileLayer(0, "" + "text"); //specify a layer ID
```

***

### Fade Layer

![fadeTo-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/fadeTo-layer2.png)

Fades the given layer to the specified alpha (0 - 100%) over time.

```
fadeTileLayerTo(0, "" + "text", 0/100, 0); //specify a layer ID
```

*** Set Blend Mode (for layer)

### set blend mode for layer with %0 : %1 to %2 [i:flash]

![set-blend-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-blend-layer2.png)

Set Blend Mode for Layer (by ID or name)

```
setBlendModeForLayer(0,"" + "text",BlendMode.ADD); //specify a layer ID
```

***

### Change Background Image (for layer)

![set-bg-image](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-bg-image.png)

Change the image displayed in the specified background layer.

```
changeBackgroundImage(0, "" + "text", image); //specify a layer ID
```

***

## Add/Remove Layers

### Create a Background Layer

![create-bglayer-from-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/create-bglayer-from-bg.png)

Add a new background layer.

```
addBackground("text", "text", 0); //specify a layer ID
```

***

### Create a Background Layer (from image)

![create-bglayer-from-image](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/create-bglayer-from-image.png)

Add a new background layer using an image.

```
addBackgroundFromImage(image, true, "text", 0); //specify a layer ID
```

***

### Remove Background Layer

![remove-bglayer](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/remove-bglayer.png)

Remove a background layer.

```
removeBackground(0, "text"); //specify a layer ID
```

***

## Layer Order

### Set Drawing Order for Layer

![set-layer-order](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-layer-order.png)

Set the display order of the specified layer. 0 is the back, higher numbers are closer.

```
engine.moveLayerToOrder(0, "text", 0); //specify a layer ID
```

***

### Get Drawing Order for Layer

![get-layer-order](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/get-layer-order.png)

Get the display order of the specified layer. 0 is the back, higher numbers are closer.

```
engine.getOrderOfLayer(0, "text") //specify a layer ID
```

***

### Number of Layers

![numlayers](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/numlayers.png)

Returns the number of layers in the current scene.

```
engine.getNumberOfLayers()
```

***

## Offscreen Bounds

### Set Offscreen Bounds

![offscreen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/offscreen.png)

Used to set how far actors have to be off-screen to be considered off screen.

```
setOffscreenTolerance([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

