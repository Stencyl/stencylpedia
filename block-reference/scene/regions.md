# Scene > Regions

***


> Read our guide on [regions](http://www.stencyl.com/help/view/regions/) for an explanation of these blocks.

***

## Get Region

### Choose Region

![region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/region.png)

Returns a Region of choice (whether an instance of one, an attribute or other form).

```
[REGION]
```

***

### Actor is Inside Region?

![is-in-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/is-in-region.png)

Returns `true` if the actor is inside the specified region.

```
isInRegion([ACTOR], [REGION])
```

***

## Create

### Create Box Region

![create-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/create-region.png)

Creates a rectangular region with the given location and size. Assign to a Region attribute to refer to it in the future.

```
createBoxRegion([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### Create Circle Region

![create-circular-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/create-circular-region.png)

Creates a circular region with the given location and size. Assign to a Region attribute to refer to it in the future.

```
createCircularRegion([NUMBER], [NUMBER], [NUMBER]);
```

***

## Delete

### Delete Region

![delete-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/delete-region.png)

Deletes a region from the current scene. (It will return if you leave the scene and come back.)

```
removeRegion([REGION].getID());
```

***

## Move

### Move Region

![move-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/move-region.png)

Moves the region to the given point.

```
[REGION].setLocation([NUMBER], [NUMBER]);
```

***

### Move Region to Actor

![follow-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/follow-region.png)

Moves the region to the given actor's location using its origin point.

```
[REGION].follow([ACTOR]);
```

***

## Resize

### reset size of %0

![reset-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/reset-region.png)

Resets the region to its original size.

```
[REGION].resetSize();
```

***

### Resize Circle Region

![resize-region1](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/resize-region1.png)

Sets the size of a circular region to the given diameter.

```
[REGION].setRegionDiameter([NUMBER]);
```

***

### Resize Box Region

![resize-region2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/resize-region2.png)

Sets the size of a box region to the given width and height.

```
[REGION].setRegionSize([NUMBER], [NUMBER]);
```

***

## Properties

### Position of Region

![get-region-pos](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/get-region-pos.png)

Gets the [X/Y] location of the region.

```
[REGION].getX()
[REGION].getY()
```

***

### [Width/Height] of Region

![get-region-size](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/get-region-size.png)

Gets the [Width/Height] of the region.

```
[REGION].getWidth()
[REGION].getHeight()
```

***

