# Actor > Draw

***

## Animation

### Current Animation

![get-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/getanim.png)

Returns the current animation for the actor.

```
[ACTOR].getAnimation()
```

***

### Switch Animation

![switch-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setanim.png)

Changes the animation for the actor to the specified one.

```
[ACTOR].setAnimation([ANIMATION]);
```

***

### Get Animation (from text)

![get-text-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/string-to-anim.png)

Returns the Animation (within the actor) whose name matches the specified text.

```
([TEXT])
```

***

### Is an Animation playing?

![is-playing-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/is-anim.png)

Returns `true` if the actor's current animation is still playing. This is only relevant for non-looping animations since looping ones will always return `true`.

```
[ACTOR].isAnimationPlaying()
```

***

### Set Frame # for Animation

![set-frame-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/set-frame.png)

Sets the frame (by index) for the actor's current animation.

```
[ACTOR].setCurrentFrame([NUMBER]);
```

***

### Get Current Frame #

![get-frame-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-frame.png)

Returns the index of the current frame in the actor's current animation.

```
[ACTOR].getCurrentFrame()
```

***

### Get Number of Frames in Current Animation

![get-num-frames-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-num-frames.png)

Returns the number of frames in the actor's current animation.

```
[ACTOR].getNumFrames()
```

***

### Get Duration of Current Frame

![get-frame-duration-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-frame-duration.png)

Returns the duration (in seconds) of the current frame in the actor's current animation.

```
[ACTOR].currAnimation.getFrameDurations()[[NUMBER]]
```

***

### Set Duration of Current Frame

![set-frame-duration-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/set-frame-duration.png)

Sets the duration (in seconds) of the current frame in the actor's current animation.

```
[ACTOR].currAnimation.setFrameDuration([NUMBER], [NUMBER]);
```

***

## Layer (Z-Order)

### Get Layer ID

![get-layerid-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/getlayer.png)

Returns the ID of the layer that this actor is part of.

```
[ACTOR].getLayerID()
```

***

### Switch Layer by ID

![switch-layer-id-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setlayer2.png)

Changes an actor's layer by either specifying the Layer ID or Layer Name. You can find both pieces of info in the Scene Designer's Layers Pane.

```
[ACTOR].moveToLayer(0, [TEXT]); //By Layer ID
[ACTOR].moveToLayer(1, [TEXT]); //By Layer Name
```

***

### Switch Layer

![switch-layer-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/backforward.png)

A user-friendly way of making adjustments to an actor's layer. Can move to front/back/forward 1 layer/back 1 layer.

```
[ACTOR].sendBackward();
[ACTOR].bringForward();
[ACTOR].sendToBack();
[ACTOR].bringToFront();
```

***

### Switch Drawing Order (within layer)

![switch-order-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/movewithinlayer.png)

A user-friendly way of making adjustments to an actor's **drawing order** (z-order) within a layer. Can move to front/back/forward 1 layer/back 1 layer.

```
[ACTOR].moveDown();
[ACTOR].moveUp();
[ACTOR].moveToBottom();
[ACTOR].moveToTop();
```

***

### Get Drawing Order (within layer)

![get-order-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/zindex.png)

Returns an actor's **drawing order** (z-order) within its layer.

```
[ACTOR].getZIndex()
```

***

### Set Drawing Order (within layer)

![set-order-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setzindex.png)

Sets an actor's **drawing order** (z-order) within its layer. This lets you make fine-tuned adjustments to layering without introducing a more layers to the game.

```
[ACTOR].setZIndex([NUMBER]);
```

***

### Number of Actors within Layer

![num-actors-layer-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/actorswithinlayer2.png)

Returns the number of actors in the specified actor's layer. Can specify by Layer ID or Layer Name. You can find both pieces of info in the Scene Designer's Layers Pane.

```
engine.getNumberOfActorsWithinLayer(0, [TEXT]) //by Layer ID
engine.getNumberOfActorsWithinLayer(1, [TEXT]) //by Layer Name
```

***

## Drawing

### [Show/Hide] Sprite

![show-sprite-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/toggle-image.png)

Makes the actor invisible or visible. Everything else about the actor still works, and the `[actor] is on screen?` block will still return `true`.

```
[ACTOR].enableActorDrawing();
[ACTOR].disableActorDrawing();
```

***

### Set Opacity

![set-opacity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/set-opacity.png)

Sets the actor's opacity (alpha) value, which controls how "transparent" the actor is. Value must be between [0 - 100] inclusive. 0 means fully transparent. 100 is the default.

```
[ACTOR].alpha = [NUMBER] / 100;
```

***

### Get Opacity

![get-opacity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-opacity.png)

Returns the actor's opacity (alpha) value as a value between [0 - 100] inclusive.

```
([ACTOR].alpha * 100)
```

***

## Anchoring

### Anchor Actor to Screen

![anchor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/anchor-screen.png)

Moves the actor to the HUD layer, which is on top of all regular layers. The actor will ignore the camera, so when the screen scrolls, the actor will still remain in the same place.

```
[ACTOR].anchorToScreen();
```

***

### Unanchor Actor from Screen

![unanchor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/unanchor-screen.png)

Moves the actor back from the HUD layer.

```
[ACTOR].unanchorFromScreen();
```

***
