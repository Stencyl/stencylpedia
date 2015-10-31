# Drawing > Drawing

***

## Basic

### <a name="draw-text"></a> Draw Text

![draw-text-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/draw-text.png)

Draws the specified text to the given location using the current font. Color and stroke settings do not apply to fonts.

```
g.drawString([TEXT], [NUMBER], [NUMBER]);
```

***

### <a name="draw-line"></a> Draw Line

![draw-line-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/draw-line.png)

Draws a line from the starting point to the ending point, using the current stroke color and thickness.

```
g.drawLine([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="draw-pixel"></a> Fill Pixel

![fill-pixel-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/draw-pixel.png)

Draws a single pixel to the given location, using the current color. We recommend using the [Image API](http://www.stencyl.com/help/view/image-api) if you intend to fill many pixels at a time.

```
g.fillPixel([NUMBER], [NUMBER]);
```

***

## Actor Drawing

### <a name="draw-image-actor"></a> Draw Image for Actor

![draw-actor-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/draw-image-actor.png)

Draws the specified actor's image to the current pen position. Will base this upon the actor's current animation (and current frame). Still works if the actor is hidden. Useful for drawing things behind an actor.

```
[ACTOR].drawImage(g);
```

#### Example

![example](http://static.stencyl.com/pedia2/blocks/drawing/drawing/actor_example.png)

Draws the following.

![example](http://static.stencyl.com/pedia2/blocks/drawing/drawing/actor_example2.png)

***

## Rectangles

### <a name="drawfill-rect"></a> Draw Rectangle

![draw-rect-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/drawfill-rect.png)

Draws an outline of (or fills) a rectangle at the specified position and size, using the current stroke color and thickness (and color for filling).

```
g.drawRect([NUMBER], [NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="drawfill-roundrect"></a> Draw Rounded Rectangle

![draw-round-rect-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/drawfill-roundrect.png)

Draws an outline of (or fills) a rounded rectangle at the specified position and size, using the current stroke color and thickness (and color for filling).

```
g.drawRoundRect([NUMBER], [NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

## Circles

### <a name="drawfill-circle"></a> Draw Circle

![draw-circle-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/drawfill-circle.png)

Draws an outline of (or fills) a circle at the specified position and size, using the current stroke color and thickness (and color for filling).

```
g.drawCircle([NUMBER], [NUMBER], [NUMBER]);
```

***

## Polygons

### <a name="drawfill-poly"></a> Draw Polygon

![draw-poly-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/drawfill-poly.png)

Draws an outline of (or fills) a polygon at the specified position, using the current stroke color and thickness (and color for filling). Use the `add point to polygon` block to add points to the polygon.

```
g.beginDrawPolygon();
[ACTIONS]
g.endDrawingPolygon();
```

***

### <a name="add-to-poly"></a> Add Point to Polygon

![add-poly-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/add-to-poly.png)

Adds the specified point to the polygon. At least 3 points must be specified. You do not have to "close" the polygon by repeating the starting point.

```
g.addPointToPolygon([NUMBER], [NUMBER]);
```

***
