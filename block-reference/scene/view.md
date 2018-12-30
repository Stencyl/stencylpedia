# Scenes > View

***

> Read our article on [Backgrounds](http://www.stencyl.com/help/view/backgrounds-and-foregrounds/) and [Camera](http://www.stencyl.com/help/view/the-camera/) for an explanation of some of these blocks.

***

## Screen Bounds

### <a name="screen-xy"></a> Camera Position

![x of camera](http://static.stencyl.com/pedia2/block-images/scene/view/screen-xy.png)

Returns the camera's horizontal (X) or vertical (Y) position.

```
getScreenX()
getScreenY()
getScreenXCenter()
getScreenYCenter()
```

***

### <a name="screen-wh"></a> Screen Size

![screen width](http://static.stencyl.com/pedia2/block-images/scene/view/screen-wh.png)

Returns the game's screen width/height.

```
getScreenWidth()
getScreenHeight()
```

***

## Camera

### <a name="camera-move"></a> Move Camera

![move camera center to x number y number](http://static.stencyl.com/pedia2/block-images/scene/view/camera-move.png)

Moves the camera to the given point.

```
engine.moveCamera([NUMBER], [NUMBER]);
```

***

### <a name="camera-follow"></a> Move Camera to Actor

![move camera center to actor](http://static.stencyl.com/pedia2/block-images/scene/view/camera-follow.png)

Moves the camera to the given actor's location.

```
engine.cameraFollow([ACTOR]);
```

***

## Effects

### <a name="shake-start"></a> Shake Screen

![shake screen for number sec with intensity number %](http://static.stencyl.com/pedia2/block-images/scene/view/shake-start.png)

Shakes the screen for the specified time. Good for conveying explosions or earthquakes. Intensity specifies how "violent" the shaking is.

```
startShakingScreen([NUMBER] / 100, [NUMBER]);
```

***

### <a name="shake-stop"></a> Stop Shaking Screen

![stop shaking screen](http://static.stencyl.com/pedia2/block-images/scene/view/shake-stop.png)

Immediately stop shaking the screen.

```
stopShakingScreen();
```

***

## Color Background

### <a name="set-color-bg"></a> Set Background to Color

![set color background to solid color color](http://static.stencyl.com/pedia2/block-images/scene/view/set-color-bg.png)

Changes the background color to a solid color (if you don't have an image background covering it up).

```
setColorBackground([COLOR]);
```

***

### <a name="set-grad-bg"></a> Set Background to Gradient

![set color background to vertical gradient with color and color](http://static.stencyl.com/pedia2/block-images/scene/view/set-grad-bg.png)

Changes the background color to a vertical gradient (if you don't have an image background covering it up).

```
setColorBackground([COLOR], [COLOR]);
```

***

## Layer Properties

### <a name="layer-exists"></a> Layer Exists

![layer with id object exists](http://static.stencyl.com/pedia2/block-images/scene/view/layer-exists.png)

Returns true if a layer with the given name or ID exists.

```
(engine.getLayerById([INT], false) != null)
(engine.getLayerByName([TEXT], false) != null)
```

***

### <a name="set-bg-speed"></a> Set Autoscroll Speed (for layer)

![set autoscroll speed for background with id object to x number y number](http://static.stencyl.com/pedia2/block-images/scene/view/set-bg-speed.png)

Changes the speed that the specified background layer (automatically) scrolls at. The layer must be designated as scrolling to begin with for this to work.

```
setScrollSpeedForBackground(engine.getLayerById([INT]), [NUMBER], [NUMBER]);
setScrollSpeedForBackground(engine.getLayerByName([TEXT]), [NUMBER], [NUMBER]);
```

***

### <a name="set-layer-scrollfactor"></a> Set Scroll Factor for (for layer)

![set scroll factor for layer with id object to x number y number](http://static.stencyl.com/pedia2/block-images/scene/view/set-layer-scrollfactor.png)

Change the speed at which any layer scrolls, as a percentage of the baseline. In other words, 100% is the original value, 200% is twice as much and 50% is half as much.

```
setScrollFactorForLayer(engine.getLayerById([INT]), [NUMBER], [NUMBER]);
setScrollFactorForLayer(engine.getLayerByName([TEXT]), [NUMBER], [NUMBER]);
```

***

### <a name="showhide-layer2"></a> Show / Hide Layer

![hide layer with id object](http://static.stencyl.com/pedia2/block-images/scene/view/showhide-layer2.png)

Shows/Hides the given layer.

```
hideTileLayer(engine.getLayerById([INT]));
hideTileLayer(engine.getLayerByName([TEXT]));

showTileLayer(engine.getLayerById([INT]));
showTileLayer(engine.getLayerByName([TEXT]));
```

***

### <a name="fadeTo-layer2"></a> Fade Layer

![fade layer with id object to number % over number secs](http://static.stencyl.com/pedia2/block-images/scene/view/fadeTo-layer2.png)

Fades the given layer to the specified opacity value (0 - 100%) over time.

```
fadeTileLayerTo(engine.getLayerById([INT]), [NUMBER]/100, [NUMBER]);
fadeTileLayerTo(engine.getLayerByName([TEXT]), [NUMBER]/100, [NUMBER]);
```

***

### <a name="layer-alpha"></a> Opacity of Layer

![opacity of layer with id object](http://static.stencyl.com/pedia2/block-images/scene/view/layer-alpha.png)

Returns the opacity of layer (0% - 100%) with the given name or ID.

```
getTileLayerOpacity(engine.getLayerById([INT]))
getTileLayerOpacity(engine.getLayerByName([TEXT]))
```

***

### <a name="set-blend-layer2"></a> Set Blend Mode (for layer)

![set blend mode for layer with id object to dropdown](http://static.stencyl.com/pedia2/block-images/scene/view/set-blend-layer2.png)

Set the [Blend Mode](http://www.stencyl.com/help/view/blending-modes/) for the specified layer.

```
setBlendModeForLayer(engine.getLayerById([INT]),[BLEND MODE]);
setBlendModeForLayer(engine.getLayerByName([TEXT]),[BLEND MODE]);
```

***

### <a name="set-bg-image"></a> Change Background Image (for layer)

![change image for background layer with id object to image](http://static.stencyl.com/pedia2/block-images/scene/view/set-bg-image.png)

Change the image displayed in the specified background layer.

```
changeBackgroundImage(engine.getLayerById([INT]), [IMAGE]);
changeBackgroundImage(engine.getLayerByName([TEXT]), [IMAGE]);
```

***

## Add / Remove Layers

### <a name="create-tile-layer"></a> Create Tile Layer

![create tile layer with name text at z index int](http://static.stencyl.com/pedia2/block-images/scene/view/create-tile-layer.png)

Add a new layer for tiles and actors. Provide the name of the new layer and the drawing order (z-order). 0 is the back, higher numbers display on top.

```
addTileLayer([TEXT], [INT]);
```

***

### <a name="create-bglayer-from-bg"></a> Create a Background Layer

![create background layer with name text using background text at z index int](http://static.stencyl.com/pedia2/block-images/scene/view/create-bglayer-from-bg.png)

Add a new background layer. Provide the name, the name of the Background resource and the drawing order (z-order). 0 is the back, higher numbers display on top.

```
addBackground([TEXT], [TEXT], [INT]);
```

***

### <a name="create-bglayer-from-image"></a> Create a Background Layer (from image)

![create tiled background layer with name text using image at z index int](http://static.stencyl.com/pedia2/block-images/scene/view/create-bglayer-from-image.png)

Add a new background layer using an image. Provide the image, name and drawing order (z-order). 0 is the back, higher numbers display on top.

```
addBackgroundFromImage([IMAGE], true, [TEXT], [INT]); //tiled background
addBackgroundFromImage([IMAGE], false, [TEXT], [INT]); //regular background
```

***

### <a name="remove-layer"></a> Remove Layer

![remove layer with id object](http://static.stencyl.com/pedia2/block-images/scene/view/remove-layer.png)

Remove the specified layer. The behavior of objects that still exist on this layer when it is removed is unspecified.

```
engine.removeLayer(engine.getLayerById([INT]));
engine.removeLayer(engine.getLayerByName([TEXT]));
```

***

## Layer Order

### <a name="set-layer-order"></a> Set Drawing Order for Layer

![set z index of layer with id object to int](http://static.stencyl.com/pedia2/block-images/scene/view/set-layer-order.png)

Set the drawing order of the specified layer. 0 is the back, higher numbers display on top.

```
engine.moveLayerToOrder(engine.getLayerById([INT]), [INT]);
engine.moveLayerToOrder(engine.getLayerByName([TEXT]), [INT]);
```

***

### <a name="get-layer-order"></a> Get Drawing Order for Layer

![z index of layer with id object](http://static.stencyl.com/pedia2/block-images/scene/view/get-layer-order.png)

Get the drawing order of the specified layer. 0 is the back, higher numbers display on top.

```
engine.getOrderOfLayer(engine.getLayerById([INT]))
engine.getOrderOfLayer(engine.getLayerByName([TEXT]))
```

***

### <a name="numlayers"></a> Number of Layers

![number of layers](http://static.stencyl.com/pedia2/block-images/scene/view/numlayers.png)

Returns the number of layers in the current scene.

```
engine.getNumberOfLayers()
```

***

## Offscreen Bounds

### <a name="offscreen"></a> Set Offscreen Bounds

![set offscreen bounds to top number left number bot number right number](http://static.stencyl.com/pedia2/block-images/scene/view/offscreen.png)

Used to set how far actors have to be off-screen to be considered off screen.

```
setOffscreenTolerance([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***
