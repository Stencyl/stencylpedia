# Collision > Basic

***

## Actor 1 vs. Actor 2

Each block in this section lets you choose between Actor 1 and Actor 2. Collision events involve 2 actors. When the event is reported, the first actor in the event's block corresponds to Actor 1 and the second actor in the block corresponds to Actor 2.

![explained](http://static.stencyl.com/pedia2/blocks/collision/basic/1st2nd.png)

You can refer to Actor 1 and Actor 2 directly using the blocks embedded in the event itself.

![explained-more](http://static.stencyl.com/pedia2/ch3/collisions/image16.png)

***

## Collision Side

### <a name="collision-top"></a> Top / Left / Bottom / Right Side was Hit

![collision-side-block](http://static.stencyl.com/pedia2/blocks/collision/basic/Side.png)

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

![group-block](http://static.stencyl.com/pedia2/blocks/collision/basic/Group.png)

Returns the group of the shape for the "other" (or "second") object in the collision. In most cases, the group of the shape is the same as that of the actor, but that [isn't always the case](http://www.stencyl.com/help/view/collisions-and-groups/).

```
internalGetGroup(event.thisActor, event.thisShape, event);
internalGetGroup(event.thisActor, event.otherShape, event);
```

***

### <a name="collision-type2"></a> Hit an Actor / Terrain / Tile / Sensor

![hittype-block](http://static.stencyl.com/pedia2/blocks/collision/basic/HitType.png)

Returns `true` if the "other" (or "second") object in the collision was an [actor / terrain region / tile / sensor].

```
event.thisCollidedWithActor
event.thisCollidedWithTerrain
event.thisCollidedWithTile
event.thisCollidedWithSensor
```

***
