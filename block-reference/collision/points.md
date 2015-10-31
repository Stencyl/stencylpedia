# Collision > Collision Points

***

## Loop Over Each Point

### <a name="collision-foreach"></a> For each collision point

![foreachpoint-block](http://static.stencyl.com/pedia2/blocks/collision/collisionpoints/ForEachPoint.png)

Loops over each collision point in the current collision event.

```
for(point in event.points) {
  [ACTIONS]
}
```

***

### <a name="collision-xynxy"></a> Collision Point

![point-block](http://static.stencyl.com/pedia2/blocks/collision/collisionpoints/Point.png)

Returns the (x,y) position of the current collision point. Must be used within `for each collision point`.

```
Engine.toPixelUnits(point.x)
Engine.toPixelUnits(point.y)
```

***

### <a name="tile-data-for-collision"></a> Get Data for Collided Tile

![data-block](http://static.stencyl.com/pedia2/blocks/collision/collisionpoints/TileData.png)

Returns the text associated with the tile you collided with. Must be used within `for each collision point`.

> **What is this for?** You can [tag tiles](http://www.stencyl.com/help/view/tiles/) with textual data that can be accessed during game. For example, a lava tile could convey that it's deadly to the touch, or a healing tile in an RPG could heal the character passing over it. <br/> ![tile-editor](http://static.stencyl.com/pedia2/ch4/tiles/tile-metadata.png)

```
getTileDataForCollision(event, point)
```

***
