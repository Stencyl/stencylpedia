# Scenes > Regions

***

> Read our guide on [Regions](https://www.stencyl.com/help/view/regions/) for an explanation of these blocks.

***

## Get Region

### <a name="region"></a> Choose Region

![region](https://static.stencyl.com/pedia2/block-images/scene/regions/region.png)

Returns a Region of choice (whether an instance of one, an attribute or other form).

```
[REGION]
```

***

### <a name="is-in-region"></a> Actor is Inside Region?

![actor is inside region](https://static.stencyl.com/pedia2/block-images/scene/regions/is-in-region.png)

Returns `true` if the actor is inside the specified region.

```
isInRegion([ACTOR], [REGION])
```

***

## Create

### <a name="create-region"></a> Create Box Region

![create region at x number y number with w number h number](https://static.stencyl.com/pedia2/block-images/scene/regions/create-region.png)

Creates a rectangular region with the given location and size. Assign to a Region attribute (using the "Last Created Region" selection) to refer to it in the future.

```
createBoxRegion([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="create-circular-region"></a> Create Circle Region

![create circular region at x number y number with radius number](https://static.stencyl.com/pedia2/block-images/scene/regions/create-circular-region.png)

Creates a circular region with the given location and size. Assign to a Region attribute (using the "Last Created Region" selection) to refer to it in the future.

```
createCircularRegion([NUMBER], [NUMBER], [NUMBER]);
```

***

## Delete

### <a name="delete-region"></a> Delete Region

![delete region](https://static.stencyl.com/pedia2/block-images/scene/regions/delete-region.png)

Deletes a region from the current scene. (It will return if you leave the scene and come back.)

```
removeRegion([REGION].getID());
```

***

## Move

### <a name="move-region"></a> Move Region

![move region to x number y number](https://static.stencyl.com/pedia2/block-images/scene/regions/move-region.png)

Moves the region to the given point.

```
[REGION].setLocation([NUMBER], [NUMBER]);
```

***

### <a name="follow-region"></a> Move Region to Actor

![make region follow actor](https://static.stencyl.com/pedia2/block-images/scene/regions/follow-region.png)

Moves the region to the given actor's location using its origin point.

```
[REGION].follow([ACTOR]);
```

***

## Resize

### <a name="reset-region"></a> Reset Region Size

![reset size of region](https://static.stencyl.com/pedia2/block-images/scene/regions/reset-region.png)

Resets the region to its original size.

```
[REGION].resetSize();
```

***

### <a name="resize-region1"></a> Resize Circle Region

![set diameter of region to number px](https://static.stencyl.com/pedia2/block-images/scene/regions/resize-region1.png)

Sets the size of a circular region to the given diameter.

```
[REGION].setRegionDiameter([NUMBER]);
```

***

### <a name="resize-region2"></a> Resize Box Region

![set size of region to w number h number](https://static.stencyl.com/pedia2/block-images/scene/regions/resize-region2.png)

Sets the size of a box region to the given width and height.

```
[REGION].setRegionSize([NUMBER], [NUMBER]);
```

***

## Properties

### <a name="get-region-pos"></a> Position of Region

![x of region](https://static.stencyl.com/pedia2/block-images/scene/regions/get-region-pos.png)

Gets the [X/Y] location of the region.

```
[REGION].getX()
[REGION].getY()
[REGION].getXCenter()
[REGION].getYCenter()
```

***

### <a name="get-region-size"></a> Width / Height of Region

![width of region](https://static.stencyl.com/pedia2/block-images/scene/regions/get-region-size.png)

Gets the [Width/Height] of the region.

```
[REGION].getWidth()
[REGION].getHeight()
```

***
