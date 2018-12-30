# Actors > Motion

***

## Speed

### <a name="get-dxy"></a> Get Speed

![x speed of actor](http://static.stencyl.com/pedia2/block-images/actor/motion/get-dxy.png)

Returns the current [X / Y] speed for the actor.

```
[ACTOR].getXVelocity()
[ACTOR].getYVelocity()
```

***

### <a name="set-dxy"></a> Set Speed

![set x speed to number for actor](http://static.stencyl.com/pedia2/block-images/actor/motion/set-dxy.png)

Sets the [X / Y] speed for the actor.

```
[ACTOR].setXVelocity([NUMBER]);
[ACTOR].setYVelocity([NUMBER]);
```

***

### <a name="setvel"></a> Set Velocity (given Direction and Speed)

![set velocity to dir number degrees , speed number for actor](http://static.stencyl.com/pedia2/block-images/actor/motion/setvel.png)

Sets the actor's velocity, given a direction and a magnitude (speed) rather than X/Y components like above.

```
[ACTOR].setVelocity([NUMBER], [NUMBER]);
```

***

## Force

### <a name="push-shove"></a> Push (given X/Y)

![push actor gently towards x dir number y dir number at number force](http://static.stencyl.com/pedia2/block-images/actor/motion/push-shove.png)

Pushes (or shoves) an actor, given an X/Y direction and force. Shoving is more "forceful" than pushing - experiment and see which works better for you.

```
[ACTOR].push([NUMBER], [NUMBER], [NUMBER]);
[ACTOR].applyImpulse([NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="push-shove2"></a> Push (given Angle)

![push actor gently towards number degrees at number force](http://static.stencyl.com/pedia2/block-images/actor/motion/push-shove2.png)

Pushes (or shoves) an actor, given an angle and force. Shoving is more "forceful" than pushing - experiment and see which works better for you.

```
[ACTOR].pushInDirection([NUMBER], [NUMBER]);
[ACTOR].applyImpulseInDirection([NUMBER], [NUMBER]);
```

***

### <a name="twist"></a> Twist (rotate using force)

![twist actor with number force](http://static.stencyl.com/pedia2/block-images/actor/motion/twist.png)

Twists (applies torque) to an actor, given a force.

```
[ACTOR].applyTorque(Utils.RAD * [NUMBER]);
```

***

## Turning Speed

### <a name="getangvel"></a> Get Turning Speed

![turning speed of actor](http://static.stencyl.com/pedia2/block-images/actor/motion/getangvel.png)

Returns the turning speed (angular velocity) of the actor (in degrees).

```
Utils.DEG * ([ACTOR].getAngularVelocity())
```

***

### <a name="setav"></a> Set Turning Speed

![set turning speed to number for actor](http://static.stencyl.com/pedia2/block-images/actor/motion/setav.png)

Sets the turning speed (angular velocity) of the actor (in degrees). Positive turns clockwise. Negative turns counter-clockwise.

```
[ACTOR].setAngularVelocity(Utils.RAD * [NUMBER]);
```

***

## Physics

### <a name="toggle-grav"></a> Toggle Gravity

![enable gravity for actor](http://static.stencyl.com/pedia2/block-images/actor/motion/toggle-grav.png)

Enables or disables gravity for this actor.

```
[ACTOR].setIgnoreGravity(false); //enable gravity
[ACTOR].setIgnoreGravity(true); //disable gravity
```

***

### <a name="toggle-rot"></a> Toggle Rotation

![enable rotation for actor](http://static.stencyl.com/pedia2/block-images/actor/motion/toggle-rot.png)

Enables or disableds rotation for this actor. 

```
[ACTOR].enableRotation();
[ACTOR].disableRotation();
```

***

### <a name="set-fric-bounce"></a> Set Friction / Bounciness

![set friction to number for actor](http://static.stencyl.com/pedia2/block-images/actor/motion/set-fric-bounce.png)

Sets the actor's friction and bounciness settings. Provide a value between [0.0 - 1.0] inclusive.

Read our [Physics guide](http://www.stencyl.com/help/view/working-with-physics/) for an explanation of what these fields mean.

```
[ACTOR].setFriction([NUMBER]);
[ACTOR].setBounciness([NUMBER]);
[ACTOR].setMass([NUMBER]);
[ACTOR].setAngularMass([NUMBER]);
[ACTOR].setLinearDamping([NUMBER]);
[ACTOR].setAngularDamping([NUMBER]);
```

***

### <a name="get-fric-bounce"></a> Get Friction / Bounciness

![friction of actor](http://static.stencyl.com/pedia2/block-images/actor/motion/get-fric-bounce.png)

Gets the actor's friction and bounciness settings. Read our [Physics guide](http://www.stencyl.com/help/view/working-with-physics/) for an explanation of what these fields mean.

```
[ACTOR].getFriction()
[ACTOR].getBounciness()
[ACTOR].getMass()
[ACTOR].getAngularMass()
[ACTOR].getLinearDamping()
[ACTOR].getAngularDamping()
```

***
