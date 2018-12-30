# Actors > Position

***

## Position

### <a name="get-xy"></a> Get Position

![x of actor](http://static.stencyl.com/pedia2/block-images/actor/position/get-xy.png)

Gets the current [X / Y] position of the actor.

```
[ACTOR].getX()
[ACTOR].getY()
[ACTOR].getXCenter()
[ACTOR].getYCenter()
[ACTOR].getScreenX()
[ACTOR].getScreenY()
```

***

### <a name="set-xy"></a> Set Position

![set x to number for actor](http://static.stencyl.com/pedia2/block-images/actor/position/set-xy.png)

Sets the [X, Y] position of the actor.

```
[ACTOR].setX([NUMBER]);
[ACTOR].setY([NUMBER]);
[ACTOR].setXCenter([NUMBER]);
[ACTOR].setYCenter([NUMBER]);
[ACTOR].setScreenX([NUMBER]);
[ACTOR].setScreenY([NUMBER]);
```

***

### <a name="isonscreen"></a> Actor is on screen?

![actor is on screen](http://static.stencyl.com/pedia2/block-images/actor/position/isonscreen.png)

Returns `true` if the specified actor is at least partially on screen.

```
[ACTOR].isOnScreen()
```

***

## Direction

### <a name="getdir"></a> Get Direction (Angle)

![direction of actor](http://static.stencyl.com/pedia2/block-images/actor/position/getdir.png)

Returns the actor's direction (angle), in degrees. 0 degrees -> facing right. 90 degrees -> facing down.

```
(Utils.DEG * [ACTOR].getAngle())
```

***

### <a name="setangle"></a> Set Direction (Angle)

![point actor towards number degrees](http://static.stencyl.com/pedia2/block-images/actor/position/setangle.png)

Sets the actor's direction (angle), in degrees. 0 degrees -> facing right. 90 degrees -> facing down.

```
[ACTOR].setAngle(Utils.RAD * [NUMBER]);
```

***

### <a name="rotate"></a> Turn Clockwise

![turn actor by number degrees](http://static.stencyl.com/pedia2/block-images/actor/position/rotate.png)

Instantly rotates the the actor clockwise by the given number of degrees.

```
[ACTOR].rotate(Utils.RAD * [NUMBER]);
```

***

### <a name="rotate2"></a> Turn Counter Clockwise

![turn actor by number degrees](http://static.stencyl.com/pedia2/block-images/actor/position/rotate2.png)

Instantly rotates the the actor counter-clockwise by the given number of degrees.

```
[ACTOR].rotate(-Utils.RAD * [NUMBER]);
```

***
