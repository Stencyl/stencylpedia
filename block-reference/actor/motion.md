# Actor > Motion

***

## Speed

### <a name="get-dxy"></a> Get Speed

![get-speed-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/get-dxy.png)

Returns the current [X / Y] speed for the actor.

```
[ACTOR].getXVelocity()
[ACTOR].getYVelocity()
```

***

### <a name="set-dxy"></a> Set Speed

![set-speed-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/set-dxy.png)

Sets the [X / Y] speed for the actor.

```
[ACTOR].setXVelocity([NUMBER]);
[ACTOR].setYVelocity([NUMBER]);
```

***

### <a name="setvel"></a> Set Velocity (given direction, speed)

![set-velocity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/setvel.png)

Sets the actor's velocity, given a direction and a magnitude (speed) rather than X/Y components like above.

```
[ACTOR].setVelocity([NUMBER], [NUMBER]);
```

***

## Force

### <a name="push-shove"></a> Push (given X/Y)

![push-xy-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/push-shove.png)

Pushes (or shoves) an actor, given an X/Y direction and force. Shoving is more "forceful" than pushing - experiment and see which works better for you.

```
[ACTOR].push([NUMBER], [NUMBER], [NUMBER]);
[ACTOR].shove([NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="push-shove2"></a> Push (given Angle)

![push-angle-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/push-shove2.png)

Pushes (or shoves) an actor, given an angle and force. Shoving is more "forceful" than pushing - experiment and see which works better for you.

```
[ACTOR].pushInDirection([NUMBER], [NUMBER]);
[ACTOR].shoveInDirection([NUMBER], [NUMBER]);
```

***

### <a name="twist"></a> Twist (rotate using force)

![twist-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/twist.png)

Twists (applies torque) to an actor, given a force.

```
[ACTOR].applyTorque(Utils.RAD * [NUMBER]);
```

***

## <a name="getangvel"></a> Turning Speed

### Get Turning Speed

![get-avelocity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/getangvel.png)

Returns the turning speed (angular velocity) of the actor (in degrees).

```
Utils.DEG * ([ACTOR].getAngularVelocity())
```

***

### <a name="setav"></a> Set Turning Speed

![set-avelocity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/setav.png)

Sets the turning speed (angular velocity) of the actor (in degrees). Positive turns clockwise. Negative turns counter-clockwise.

```
[ACTOR].setAngularVelocity(Utils.RAD * [NUMBER]);
```

***

## Physics

### <a name="toggle-grav"></a> Toggle Gravity

![gravity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/toggle-grav.png)

Enables or disables gravity for this actor.

```
[ACTOR].setIgnoreGravity(false); //enable gravity
[ACTOR].setIgnoreGravity(true); //disable gravity
```

***

### <a name="toggle-rot"></a> Toggle Rotation

![toggle-rotation-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/toggle-rot.png)

Enables or disableds rotation for this actor. 

```
[ACTOR].enableRotation();
[ACTOR].disableRotation();
```

***

### <a name="set-fric-bounce"></a> Set Friction / Bounciness

![set-friction-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/set-fric-bounce.png)

Sets the actor's friction and bounciness settings. Provide a value between [0.0 - 1.0] inclusive.

Read our [Physics guide](http://www.stencyl.com/help/view/working-with-physics/) for an explanation of what these fields mean.

```
[ACTOR].setFriction([NUMBER]);
[ACTOR].setBounciness([NUMBER]);
```

***

### <a name="get-fric-bounce"></a> Get Friction / Bounciness

![get-friction-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/get-fric-bounce.png)

Gets the actor's friction and bounciness settings. Read our [Physics guide](http://www.stencyl.com/help/view/working-with-physics/) for an explanation of what these fields mean.

```
[ACTOR].getFriction()
[ACTOR].getBounciness()
```

***
