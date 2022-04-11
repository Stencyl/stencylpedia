# Actors > Draw

***

## Animation

### <a name="getanim"></a> Current Animation

![current animation for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/getanim.png)

Returns the current animation for the actor.

```
[ACTOR].getAnimation()
```

***

### <a name="setanim"></a> Switch Animation

![switch animation to animation for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/setanim.png)

Changes the animation for the actor to the specified one.

```
[ACTOR].setAnimation([ANIMATION]);
```

***

### <a name="is-anim"></a> Is an Animation playing?

![is animation playing for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/is-anim.png)

Returns `true` if the actor's current animation is still playing. This is only relevant for non-looping animations since looping ones will always return `true`.

```
[ACTOR].isAnimationPlaying()
```

***

### <a name="set-frame"></a> Set Frame # for Animation

![switch to frame int for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/set-frame.png)

Sets the frame (by index) for the actor's current animation.

```
[ACTOR].setCurrentFrame([INT]);
```

***

### <a name="get-frame"></a> Get Current Frame #

![get current frame for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/get-frame.png)

Returns the index of the current frame in the actor's current animation.

```
[ACTOR].getCurrentFrame()
```

***

### <a name="get-num-frames"></a> Get Number of Frames in Current Animation

![get frame count for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/get-num-frames.png)

Returns the number of frames in the actor's current animation.

```
[ACTOR].getNumFrames()
```

***

### <a name="get-frame-duration"></a> Get Duration of Current Frame

![duration of frame int for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/get-frame-duration.png)

Returns the duration (in milliseconds) of the current frame in the actor's current animation.

```
[ACTOR].currAnimation.getFrameDurations()[[INT]]
```

***

### <a name="set-frame-duration"></a> Set Duration of Current Frame

![set duration of frame int to int for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/set-frame-duration.png)

Sets the duration (in milliseconds) of the current frame in the actor's current animation.

```
[ACTOR].currAnimation.setFrameDuration([INT], [INT]);
```

***

## Layer (Z-Order)

### <a name="getlayer"></a> Get Layer ID

![layer id of actor](https://static.stencyl.com/pedia2/block-images/actor/draw/getlayer.png)

Returns the ID of the layer that this actor is part of.

```
[ACTOR].getLayerID()
```

***

### <a name="getlayername"></a> Get Layer Name

![layer name of actor](https://static.stencyl.com/pedia2/block-images/actor/draw/getlayername.png)

Returns the name of the layer that this actor is part of.

```
[ACTOR].getLayerName()
```

***

### <a name="setlayer2"></a> Switch Layer by ID / Name

![send actor to layer with id object](https://static.stencyl.com/pedia2/block-images/actor/draw/setlayer2.png)

Changes an actor's layer by either specifying the Layer ID or Layer Name. You can find both pieces of info in the Scene Designer's Layers Pane.

```
[ACTOR].moveToLayer(engine.getLayerById([INT]));
[ACTOR].moveToLayer(engine.getLayerByName([TEXT]));
```

***

### <a name="backforward"></a> Switch Layer

![send actor back a layer](https://static.stencyl.com/pedia2/block-images/actor/draw/backforward.png)

A user-friendly way of making adjustments to an actor's layer. Can move to front/back/forward 1 layer/back 1 layer.

```
[ACTOR].sendBackward();
[ACTOR].bringForward();
[ACTOR].sendToBack();
[ACTOR].bringToFront();
```

***

### <a name="movewithinlayer"></a> Switch Drawing Order (within layer)

![move actor down within the layer](https://static.stencyl.com/pedia2/block-images/actor/draw/movewithinlayer.png)

A user-friendly way of making adjustments to an actor's **drawing order** (z-order) within a layer. Can move to front/back/forward 1 layer/back 1 layer.

```
[ACTOR].moveDown();
[ACTOR].moveUp();
[ACTOR].moveToBottom();
[ACTOR].moveToTop();
```

***

### <a name="zindex"></a> Get Drawing Order (within layer)

![z index of actor within the layer](https://static.stencyl.com/pedia2/block-images/actor/draw/zindex.png)

Returns an actor's **drawing order** (z-order) within its layer.

```
[ACTOR].getZIndex()
```

***

### <a name="setzindex"></a> Set Drawing Order (within layer)

![set z index within the layer of actor to int](https://static.stencyl.com/pedia2/block-images/actor/draw/setzindex.png)

Sets an actor's **drawing order** (z-order) within its layer. This lets you make fine-tuned adjustments to layering without introducing a more layers to the game.

```
[ACTOR].setZIndex([INT]);
```

***

### <a name="actorswithinlayer2"></a> Number of Actors within Layer

![number of actors within the layer with id object](https://static.stencyl.com/pedia2/block-images/actor/draw/actorswithinlayer2.png)

Returns the number of actors in the specified actor's layer. Can specify by Layer ID or Layer Name. You can find both pieces of info in the Scene Designer's Layers Pane.

```
engine.getNumberOfActorsWithinLayer(engine.getLayerById([INT]))
engine.getNumberOfActorsWithinLayer(engine.getLayerByName([TEXT]))
```

***

## Drawing

### <a name="toggle-image"></a> Show / Hide Sprite

![show sprite for actor](https://static.stencyl.com/pedia2/block-images/actor/draw/toggle-image.png)

Makes the actor invisible or visible. Everything else about the actor still works, and the `[actor] is on screen` block will still return `true`.

```
[ACTOR].enableActorDrawing();
[ACTOR].disableActorDrawing();
```

***

### <a name="set-opacity"></a> Set Opacity

![set opacity of actor to number %](https://static.stencyl.com/pedia2/block-images/actor/draw/set-opacity.png)

Sets the actor's opacity (alpha) value, which controls how "transparent" the actor is. Value must be between [0 - 100] inclusive. 0 means fully transparent. 100 is the default.

```
[ACTOR].alpha = [NUMBER] / 100;
```

***

### <a name="get-opacity"></a> Get Opacity

![opacity of actor](https://static.stencyl.com/pedia2/block-images/actor/draw/get-opacity.png)

Returns the actor's opacity (alpha) value as a value between [0 - 100] inclusive.

```
([ACTOR].alpha * 100)
```

***

## Anchoring

### <a name="anchor-screen"></a> Anchor Actor to Screen

![anchor actor to screen](https://static.stencyl.com/pedia2/block-images/actor/draw/anchor-screen.png)

Moves the actor to the HUD layer, which is on top of all regular layers. The actor will ignore the camera, so when the screen scrolls, the actor will still remain in the same place.

```
[ACTOR].anchorToScreen();
```

***

### <a name="unanchor-screen"></a> Unanchor Actor from Screen

![unanchor actor from screen](https://static.stencyl.com/pedia2/block-images/actor/draw/unanchor-screen.png)

Moves the actor back from the HUD layer.

```
[ACTOR].unanchorFromScreen();
```

***
