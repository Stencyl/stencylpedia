# Actor > Position

***

## Position

### Get Position

![position-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/get-xy.png)

Gets the current [X / Y] position of the actor.

```
[ACTOR].getX()
[ACTOR].getY()
```

***

### Set Position

![set-position-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/set-xy.png)

Sets the [X, Y] position of the actor.

```
[ACTOR].setX([NUMBER]);
[ACTOR].setY([NUMBER]);
```

***

### Actor is on screen?

![isonscreen-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/isonscreen.png)

Returns `true` if the specified actor is at least partially on screen.

```
[ACTOR].isOnScreen()
```

***

## Direction

### Get Direction (Angle)

![direction-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/getdir.png)

Returns the actor's direction (angle), in degrees. 0 degrees -> facing right. 90 degrees -> facing down.

```
Utils.DEG * ([ACTOR].getAngle())
```

***

### Set Direction (Angle)

![set-direction-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/setangle.png)

Sets the actor's direction (angle), in degrees. 0 degrees -> facing right. 90 degrees -> facing down.

```
[ACTOR].setAngle(Utils.RAD * [NUMBER]);
```

***

### Turn Clockwise

![turncw-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/rotate.png)

Instantly rotates the the actor clockwise by the given number of degrees.

```
[ACTOR].rotate(Utils.RAD * [NUMBER]);
```

***

### Turn Counter Clockwise

![turnccw-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/0%20-%20Position/rotate2.png)

Instantly rotates the the actor counter-clockwise by the given number of degrees.

```
[ACTOR].rotate(-Utils.RAD * [NUMBER]);
```

***
