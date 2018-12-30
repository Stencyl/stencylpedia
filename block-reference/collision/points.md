# Collisions > Collision Points

***

## Loop Over Each Point

### <a name="collision-foreach"></a> For each collision point ...

![for each collision point...](http://static.stencyl.com/pedia2/block-images/collision/points/collision-foreach.png)

Loops over each collision point in the current collision event.

```
for(point in event.points) {
  [ACTIONS]
}
```

***

### <a name="collision-xynxy"></a> Collision Point

![x of collision](http://static.stencyl.com/pedia2/block-images/collision/points/collision-xynxy.png)

Returns the (x,y) position of the current collision point. Must be used within the `for each collision point...` wrapper.

```
Math.round(Engine.toPixelUnits(point.x))
Math.round(Engine.toPixelUnits(point.y))
Math.round(Engine.toPixelUnits(point.normalX))
Math.round(Engine.toPixelUnits(point.normalY))
```

***

### <a name="tile-data-for-collision"></a> Get Data for Collided Tile

![data for collided tile](http://static.stencyl.com/pedia2/block-images/collision/points/tile-data-for-collision.png)

Returns the text associated with the tile you collided with. Must be used within the `for each collision point...` wrapper.

> **What is this for?** You can [tag tiles](http://www.stencyl.com/help/view/tiles/) with textual data that can be accessed during game. For example, a lava tile could convey that it's deadly to the touch, or a healing tile in an RPG could heal the character passing over it. <br/> ![tile-editor](http://static.stencyl.com/pedia2/ch4/tiles/tile-metadata.png)

```
getTileDataForCollision(event, point)
```

***
