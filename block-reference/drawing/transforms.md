# Drawing > Transforms

***

## Transforms

### <a name="draw-transtoby"></a> Move Pen (Drawing Origin)

![move pen by x number y number](https://static.stencyl.com/pedia2/block-images/drawing/transforms/draw-transtoby.png)

Moves the origin point of drawing to or by the specified amount.

**To** = Sets to the specified amount.<br/>
**By** = Adds the specified amount to the existing amount.

```
g.translate([NUMBER], [NUMBER]);
g.moveTo([NUMBER], [NUMBER]);
```

***

## Space Conversion

### <a name="to-screen-space"></a> Switch to Screen Space

![switch to screen space](https://static.stencyl.com/pedia2/block-images/drawing/transforms/to-screen-space.png)

By default, when drawing on actors, the coordinates are relative to the actor. This blocks switches the origin point of drawing to screen coordinates. This allows you to draw HUD's and other graphics that are anchored to the screen (and are unaffected by the camera).

```
g.translateToScreen();
```

***

### <a name="to-local-space"></a> Switch to Actor Space

![switch to actor space for actor](https://static.stencyl.com/pedia2/block-images/drawing/transforms/to-local-space.png)

Moves the origin point of the drawing to match the position of the specified actor.

```
g.translateToActor([ACTOR]);
```

***

## Drawing Layer

### <a name="set-drawing-layer"></a> Set Drawing Layer

![set drawing to layer id object](https://static.stencyl.com/pedia2/block-images/drawing/transforms/set-drawing-layer.png)

Set the layer for drawing.

```
Script.setDrawingLayer(engine.getLayerById([INT]));
Script.setDrawingLayer(engine.getLayerByName([TEXT]));
```

***

### <a name="set-drawing-layer-scene"></a> Draw on Scene

![set drawing to scene layer](https://static.stencyl.com/pedia2/block-images/drawing/transforms/set-drawing-layer-scene.png)

Set the layer for drawing to the HUD layer, above all other layers.

```
Script.setDrawingLayerToSceneLayer();
```

***

### <a name="set-drawing-layer-actor"></a> Draw on Layer with Actor

![set drawing to layer of actor](https://static.stencyl.com/pedia2/block-images/drawing/transforms/set-drawing-layer-actor.png)

Set the layer for drawing to the layer with the specified actor.

```
Script.setDrawingLayerToActorLayer([ACTOR]);
```

***
