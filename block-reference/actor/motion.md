# Actor > Motion

***

## Speed

### Get Speed

![get-speed-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/get-dxy.png)

aaa

```
[ACTOR].getXVelocity()
[ACTOR].getYVelocity()
```

***

### Set Speed

![set-speed-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/set-dxy.png)

aaa

```
[ACTOR].setXVelocity([NUMBER]);
[ACTOR].setYVelocity([NUMBER]);
```

***

### Set Velocity (given direction, speed)

![set-velocity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/setvel.png)

aaa

```
[ACTOR].setVelocity([NUMBER], [NUMBER]);
```

***

## Force

### Push (given X/Y)

![push-xy-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/push-shove.png)

aaa

```
[ACTOR].push([NUMBER], [NUMBER], [NUMBER]);
[ACTOR].shove([NUMBER], [NUMBER], [NUMBER]);
```

***

### Push (given Angle)

![push-angle-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/push-shove2.png)

aaa

```
[ACTOR].pushInDirection([NUMBER], [NUMBER]);
[ACTOR].shoveInDirection([NUMBER], [NUMBER]);
```

***

### Twist (rotate using force)

![twist-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/twist.png)

aaa

```
[ACTOR].applyTorque(Utils.RAD * [NUMBER]);
```

***

## Turning Speed

### Get Turning Speed

![get-avelocity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/getangvel.png)

aaa

```
Utils.DEG * ([ACTOR].getAngularVelocity())
```

***

### Set Turning Speed

![set-avelocity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/setav.png)

aaa

```
[ACTOR].setAngularVelocity(Utils.RAD * [NUMBER]);
```

***

## Physics

### Toggle Gravity

![gravity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/toggle-grav.png)

aaa

```
[ACTOR].setIgnoreGravity(false); //enable gravity
[ACTOR].setIgnoreGravity(true); //disable gravity
```

***

### Toggle Rotation

![toggle-rotation-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/toggle-rot.png)

aaa

```
[ACTOR].enableRotation();
[ACTOR].disableRotation();
```

***

### Set Friction / Bounciness

![set-friction-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/set-fric-bounce.png)

aaa

```
[ACTOR].setFriction([NUMBER]);
[ACTOR].setBounciness([NUMBER]);
```

***

### Get Friction / Bounciness

![get-friction-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/1%20-%20Motion/get-fric-bounce.png)

aaa

```
[ACTOR].getFriction()
[ACTOR].getBounciness()
```

***
