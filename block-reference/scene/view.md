# Scene > View

***

> Read our article on [Backgrounds](http://www.stencyl.com/help/view/backgrounds-and-foregrounds/) and [Camera](http://www.stencyl.com/help/view/the-camera/) for an explanation of some of these blocks.

***

## Screen Bounds

### <a name="screen-xy"></a> Camera Position

![screen-xy](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/screen-xy.png)

Returns the camera's horizontal (X) or vertical (Y) position.

```
getScreenX()
getScreenY()
```

***

### <a name="screen-wh"></a> Screen Size

![screen-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/screen-wh.png)

Returns the game's screen width/height.

```
getScreenWidth()
getScreenHeight()
```

***

## Camera

### <a name="camera-move"></a> Move Camera

![camera-move](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/camera-move.png)

Moves the camera to the given point.

```
engine.moveCamera([NUMBER], [NUMBER]);
```

***

### <a name="camera-follow"></a> Move Camera to Actor

![camera-follow](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/camera-follow.png)

Moves the camera to the given actor's location.

```
engine.cameraFollow([ACTOR]);
```

***

## Effects

### <a name="shake-start"></a> Shake Screen

![shake-start](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/shake-start.png)

Shakes the screen for the specified time. Good for conveying explosions or earthquakes. Intensity specifies how "violent" the shaking is.

```
startShakingScreen([NUMBER] / 100, [NUMBER]);
```

***

### <a name="shake-stop"></a> Stop Shaking Screen

![shake-stop](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/shake-stop.png)

Immediately stop shaking the screen.

```
stopShakingScreen();
```

***

### <a name="toggle-fullscreen"></a> Toggle Full-Screen Mode

![toggle-fullscreen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/toggle-fullscreen.png)

Enables/Disables full-screen mode for Flash & Desktop targets.

```
toggleFullScreen();
```

***

## Color Background

### <a name="set-color-bg"></a> Set Background to Color

![set-color-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-color-bg.png)

Changes the background color to a solid color (if you don't have an image background covering it up).

```
setColorBackground([COLOR]);
```

***

### <a name="set-grad-bg"></a> Set Background to Gradient

![set-grad-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-grad-bg.png)

Changes the background color to a vertical gradient (if you don't have an image background covering it up).

```
setColorBackground([COLOR], [COLOR]);
```

***

## Layer Properties

### <a name="set-bg-speed"></a> Set Autoscroll Speed (for layer)

![set-bg-speed](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-bg-speed.png)

Changes the speed that the specified background layer (automatically) scrolls at. The layer must be designated as scrolling to begin with for this to work.

```
setScrollSpeedForBackground(0, [TEXT], [NUMBER], [NUMBER]); //specify a layer ID
setScrollSpeedForBackground(1, [TEXT], [NUMBER], [NUMBER]); //specify a layer name
```

***

### <a name="set-layer-scrollfactor"></a> Set Scroll Factor for (for layer)

![set-layer-scrollfactor](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-layer-scrollfactor.png)

Change the speed at which any layer scrolls, as a percentage of the baseline. In other words, 100% is the original value, 200% is twice as much and 50% is half as much.

```
setScrollFactorForLayer(0, [TEXT], [NUMBER], [NUMBER]); //specify a layer ID
setScrollFactorForLayer(1, [TEXT], [NUMBER], [NUMBER]); //specify a layer name
```

***

### <a name="showhide-layer2"></a> Show / Hide Layer

![showhide-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/showhide-layer2.png)

Shows/Hides the given layer.

```
showTileLayer(0, [TEXT]); //specify a layer ID
showTileLayer(1, [TEXT]); //specify a layer name

hideTileLayer(0, [TEXT]); //specify a layer ID
hideTileLayer(1, [TEXT]); //specify a layer name
```

***

### <a name="fadeTo-layer2"></a> Fade Layer

![fadeTo-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/fadeTo-layer2.png)

Fades the given layer to the specified opacity value (0 - 100%) over time.

```
fadeTileLayerTo(0, [TEXT], [NUMBER]/100, [NUMBER]); //specify a layer ID
fadeTileLayerTo(1, [TEXT], [NUMBER]/100, [NUMBER]); //specify a layer name
```

***

### <a name="set-blend-layer2"></a> Set Blend Mode (for layer)

![set-blend-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-blend-layer2.png)

Set the [Blend Mode](http://www.stencyl.com/help/view/blending-modes/) for the specified layer.

```
setBlendModeForLayer(0, [TEXT], [BLEND MODE]); //specify a layer ID
setBlendModeForLayer(1, [TEXT], [BLEND MODE]); //specify a layer name
```

***

### <a name="set-bg-image"></a> Change Background Image (for layer)

![set-bg-image](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-bg-image.png)

Change the image displayed in the specified background layer.

```
changeBackgroundImage(0, [TEXT], [IMAGE]); //specify a layer ID
changeBackgroundImage(1, [TEXT], [IMAGE]); //specify a layer name
```

***

## Add/Remove Layers

### <a name="create-bglayer-from-bg"></a> Create a Background Layer

![create-bglayer-from-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/create-bglayer-from-bg.png)

Add a new background layer. Provide the name, the name of the Background resource and the drawing order (z-order). 0 is the back, higher numbers display on top.

```
addBackground([TEXT], [TEXT], [NUMBER]);
```

***

### <a name="create-bglayer-from-image"></a> Create a Background Layer (from image)

![create-bglayer-from-image](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/create-bglayer-from-image.png)

Add a new background layer using an image. Provide the image, name and drawing order (z-order). 0 is the back, higher numbers display on top.

```
addBackgroundFromImage([IMAGE], true, [TEXT], [NUMBER]); //tiled background
addBackgroundFromImage([IMAGE], false, [TEXT], [NUMBER]); //regular background
```

***

### <a name="remove-bglayer"></a> Remove Background Layer

![remove-bglayer](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/remove-bglayer.png)

Remove the specified background layer.

```
removeBackground(0, [TEXT]); //specify a layer ID
removeBackground(1, [TEXT]); //specify a layer name
```

***

## Layer Order

### <a name="set-layer-order"></a> Set Drawing Order for Layer

![set-layer-order](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-layer-order.png)

Set the drawing order of the specified layer. 0 is the back, higher numbers display on top.

```
engine.moveLayerToOrder(0, [TEXT], [NUMBER]); //specify a layer ID
engine.moveLayerToOrder(1, [TEXT], [NUMBER]); //specify a layer name
```

***

### <a name="get-layer-order"></a> Get Drawing Order for Layer

![get-layer-order](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/get-layer-order.png)

Get the drawing order of the specified layer. 0 is the back, higher numbers display on top.

```
engine.getOrderOfLayer(0, [TEXT]) //specify a layer ID
engine.getOrderOfLayer(1, [TEXT]) //specify a layer name
```

***

### <a name="numlayers"></a> Number of Layers

![numlayers](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/numlayers.png)

Returns the number of layers in the current scene.

```
engine.getNumberOfLayers()
```

***

## Offscreen Bounds

### <a name="offscreen"></a> Set Offscreen Bounds

![offscreen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/offscreen.png)

Used to set how far actors have to be off-screen to be considered off screen.

```
setOffscreenTolerance([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***
