# Scene > View

***

## Screen Bounds

### %0 of camera [i:camera]

![screen-xy](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/screen-xy.png)

The camera's horizontal (X) or vertical (Y) position.

```
getScreenX()
```

***

### screen %0

![screen-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/screen-wh.png)

The game's screen width/height.

```
getScreenWidth()
```

***

## Camera

### move [i:camera] camera center to ( x: %0 y: %1 )

![camera-move](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/camera-move.png)

Moves the camera center to the given point.

```
engine.moveCamera(0, 0);
```

***

### move [i:camera] camera center to %0

![camera-follow](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/camera-follow.png)

Forces the camera center to follow the given actor using its anchor point.

```
engine.cameraFollow(__);
```

***

## Effects

### shake screen for %1 sec with intensity %0 [pct]

![shake-start](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/shake-start.png)

Shake the screen. Good for conveying explosions or earthquakes. 1 is a good intensity.

```
startShakingScreen(0 / 100, 0);
```

***

### stop shaking screen

![shake-stop](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/shake-stop.png)

Immediately stop shaking the screen

```
stopShakingScreen();
```

***

### toggle full-screen mode [i:desktop]

![toggle-fullscreen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/toggle-fullscreen.png)

Enables/Disables full-screen. Works for Flash & Desktop targets.

```
toggleFullScreen();
```

***

## Color Background

### set color background to solid color %0

![set-color-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-color-bg.png)

Changes the background color to a solid color.

```
setColorBackground(Utils.getColorRGB(255,200,0));
```

***

### set color background to vertical gradient with %0 and %1

![set-grad-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-grad-bg.png)

Changes the background color to a vertical gradient.

```
setColorBackground(Utils.getColorRGB(255,200,0), Utils.getColorRGB(255,200,0));
```

***

## Layer Properties

### set autoscroll speed for background with %0 : %1 to ( x: %2 , y: %3 )

![set-bg-speed](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-bg-speed.png)

Changes the speed that the specified background layer scrolls at (must have already been a scrolling background).

```
setScrollSpeedForBackground(0, "" + "text", 0, 0);
```

***

### set scroll factor for layer with %0 : %1 to ( x: %2 [pct] , y: %3 [pct] )

![set-layer-scrollfactor](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-layer-scrollfactor.png)

Change the speed at which a layer scrolls, as a percentage of the baseline.

```
setScrollFactorForLayer(0, "" + "text", 0, 0);
```

***

### %0 layer with %1 : %2

![showhide-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/showhide-layer2.png)

Shows/Hides the given layer.

```
hideTileLayer(0, "" + "text");
```

***

### fade layer with %0 : %1 to %2 [pct] over %3 secs

![fadeTo-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/fadeTo-layer2.png)

Fades the given layer to the specified alpha (0 - 100%) over time.

```
fadeTileLayerTo(0, "" + "text", 0/100, 0);
```

***

### set blend mode for layer with %0 : %1 to %2 [i:flash]

![set-blend-layer2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-blend-layer2.png)

Set Blend Mode for Layer (by ID or name)

```
setBlendModeForLayer(0,"" + "text",BlendMode.ADD);
```

***

### change image for background layer with %0 : %1 to %2

![set-bg-image](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-bg-image.png)

Change the image displayed in the specified background layer.

```
changeBackgroundImage(0, "" + "text", image);
```

***

## Add/Remove Layers

### create background layer with name %1 using background %0 at z-index %2

![create-bglayer-from-bg](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/create-bglayer-from-bg.png)

Add a new background layer.

```
addBackground("text", "text", 0);
```

***

### create %1 background layer with name %2 using %0 at z-index %3

![create-bglayer-from-image](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/create-bglayer-from-image.png)

Add a new background layer using an image.

```
addBackgroundFromImage(image, true, "text", 0);
```

***

### remove background layer with %0 : %1

![remove-bglayer](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/remove-bglayer.png)

Remove a background layer.

```
removeBackground(0, "text");
```

***

## Layer Order

### set z-index of layer with %0 : %1 to %2

![set-layer-order](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/set-layer-order.png)

Set the display order of the specified layer. 0 is the back, higher numbers are closer.

```
engine.moveLayerToOrder(0, "text", 0);
```

***

### z-index of layer with %0 : %1

![get-layer-order](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/get-layer-order.png)

Get the display order of the specified layer. 0 is the back, higher numbers are closer.

```
engine.getOrderOfLayer(0, "text")
```

***

### number of layers

![numlayers](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/numlayers.png)

The number of layers.

```
engine.getNumberOfLayers()
```

***

## Offscreen Bounds

### set offscreen bounds to ( top: %0 left: %1 bot: %2 right: %3 )

![offscreen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/3%20-%20View/offscreen.png)

Used in determining when actors are off-screen relative to the screen.

```
setOffscreenTolerance(0, 0, 0, 0);
```

***

