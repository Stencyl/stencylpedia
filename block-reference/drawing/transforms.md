# Drawing > Transforms

***

## Transforms

### <a name="draw-transtoby"></a> Move Pen (Drawing Origin)

![move-pen-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/2%20-%20Transforms/draw-transtoby.png)

Moves the origin point of drawing [to / by] the specified amount.

**To** = Sets to the specified amount.<br/>
**By** = Adds the specified amount to the existing amount.

```
g.translate([NUMBER], [NUMBER]);
g.moveTo([NUMBER], [NUMBER]);
```

***

## Space Conversion

### <a name="to-screen-space"></a> Switch to Screen Space

![screen-space-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/2%20-%20Transforms/to-screen-space.png)

By default, when drawing on actors, the coordinates are relative to the actor. This blocks switches the origin point of drawing to screen coordinates. This allows you to draw HUD's and other graphics that are anchored to the screen (and are unaffected by the camera).

```
g.translateToScreen();
```

***

### <a name="to-local-space"></a> Switch to Actor Space (for Specific Actor)

![actor-space-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/2%20-%20Transforms/to-local-space.png)

Moves the origin point of the drawing to match the position of the specified actor.

```
g.translateToActor([ACTOR]);
```

***
