# Collisions > Basic

***

## Actor 1 vs. Actor 2

Each block in this section lets you choose between Actor 1 and Actor 2. Collision events involve 2 actors. When the event is reported, the first actor in the event's block corresponds to Actor 1 and the second actor in the block corresponds to Actor 2.

![explained](https://static.stencyl.com/pedia2/blocks/collision/basic/1st2nd.png)

You can refer to Actor 1 and Actor 2 directly using the blocks embedded in the event itself.

![explained-more](https://static.stencyl.com/pedia2/ch3/collisions/image16.png)

***

## Collision Side

### <a name="collision-top"></a> <a name="collision-left"></a> <a name="collision-bottom"></a> <a name="collision-right"></a> Top / Left / Bottom / Right Side was Hit

![the top of actor 1 was hit](https://static.stencyl.com/pedia2/block-images/collision/basic/collision-top.png)
![the left side of actor 1 was hit](https://static.stencyl.com/pedia2/block-images/collision/basic/collision-left.png)<br/>
![the bottom of actor 1 was hit](https://static.stencyl.com/pedia2/block-images/collision/basic/collision-bottom.png)
![the right side of actor 1 was hit](https://static.stencyl.com/pedia2/block-images/collision/basic/collision-right.png)

Returns `true` if the actor's [top/left/bottom/right] side was hit. If the collision shape is not a box, we still approximate the shape as a box to calculate this.

```
event.thisFromTop
event.thisFromLeft
event.thisFromBottom
event.thisFromRight

event.otherFromTop
event.otherFromLeft
event.otherFromBottom
event.otherFromRight
```

***

## Collision Details

### <a name="collision-shape-group2"></a> Group of Colliding Shape

![group for actor 1 colliding shape](https://static.stencyl.com/pedia2/block-images/collision/basic/collision-shape-group2.png)

Returns the group of the shape for the "other" (or "second") object in the collision. In most cases, the group of the shape is the same as that of the actor, but that [isn't always the case](https://www.stencyl.com/help/view/collisions-and-groups/).

```
internalGetGroup(event.thisActor, event.thisShape, event)
internalGetGroup(event.otherActor, event.otherShape, event)
```

***

### <a name="collision-type2"></a> Hit an Actor / Terrain / Tile / Sensor

![actor 1 hit an actor](https://static.stencyl.com/pedia2/block-images/collision/basic/collision-type2.png)

Returns `true` if the "other" (or "second") object in the collision was an [actor / terrain region / tile / sensor].

```
event.thisCollidedWithActor
event.thisCollidedWithTerrain
event.thisCollidedWithTile
event.thisCollidedWithSensor
```

***
