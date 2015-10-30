# Scene > Regions

***

## Get Region

### [sp] %0 [sp]

![region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/region.png)

Choose a region.

```
__
```

***

### %0 is inside %1

![is-in-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/is-in-region.png)

Returns true if the given actor is inside the given region.

```
isInRegion(__, __)
```

***

## Create

### create region at ( x: %0 y: %1 ) with ( w: %2 h: %3 )

![create-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/create-region.png)

Creates a region.

```
createBoxRegion(0, 0, 0, 0);
```

***

### create circular region at ( x: %0 y: %1 ) with radius: %2

![create-circular-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/create-circular-region.png)

Creates a circular region.

```
createCircularRegion(0, 0, 0);
```

***

## Delete

### delete %0

![delete-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/delete-region.png)

Deletes a region.

```
removeRegion(__.getID());
```

***

## Move

### move %0 to ( x: %1 y: %2 )

![move-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/move-region.png)

Moves the region to the given point.

```
__.setLocation(0, 0);
```

***

### make %0 follow %1

![follow-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/follow-region.png)

Forces the region to follow the given actor using its anchor point.

```
__.follow(__);
```

***

## Resize

### reset size of %0

![reset-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/reset-region.png)

Resets region to original size.

```
__.resetSize();
```

***

### set diameter of %0 to %1 px

![resize-region1](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/resize-region1.png)

Sets size of circular region to given diameter.

```
__.setRegionDiameter(0);
```

***

### set size of %0 to ( w: %1 h: %2 )

![resize-region2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/resize-region2.png)

Sets size of box region to given width and height.

```
__.setRegionSize(0, 0);
```

***

## Properties

### %1 of %0

![get-region-pos](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/get-region-pos.png)

Gets position of region.

```
__.getX()
```

***

### %1 of %0

![get-region-size](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/1%20-%20Regions/get-region-size.png)

Gets size of region.

```
__.getWidth()
```

***

