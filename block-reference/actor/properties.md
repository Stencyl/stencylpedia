# Actor > Properties

***

## Alive / Dead

### Kill Actor

![kill-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/die.png)

Immediately kills the specified actor. 

If killing the current actor from its own actor behavior, the remaining logic will continue to run. We recommending using the stop block to prevent errors from happening in this case.

```
recycleActor(__);
```

***

### Kill Actor (after leaving screen)

![kill-actor-later-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/kill-leave-screen.png)

Instructs the game to kill the actor if it exits the screen. This is useful for "bullets" and other temporary actors that aren't of much use to hold around once they're off the screen.

```
__.killSelfAfterLeavingScreen();
```

***

### Is Actor alive?

![exists-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/isalive.png)

aaa

```
__.isAlive()
```

***

## Size

### [Width / Height]

![size-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/get-wh.png)

aaa

```
(__.getWidth())
(__.getWidth())
```

***

## Groups / Type

### Get Actor Type

![gettype-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/getatype.png)

aaa

```
__.getType()
```

***

### Get Group

![group-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/getgroup.png)

aaa

```
__.getGroup()
```

***

### Choose Actor Type

![choose-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/pick-type.png)

aaa

```
[ACTOR TYPE]
```

***

### Choose Actor Group

![choose-group-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/pick-group.png)

aaa

```
[ACTOR GROUP]
```

***

### Get Actor Type (from name)

![pick-type-name-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/pick-type-by-name.png)

aaa

```
getActorTypeByName("text")
```

***

## Misc

### Make Actor Always Active

![always-simulate-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/ignore-screen-tolerance.png)

aaa

```
__.makeAlwaysSimulate();
```

***

### Enable Continuous Collision Detection

![ccd-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/bullet-mode.png)

aaa

```
makeActorNotPassThroughTerrain(__);
```

***

## Collision Shapes

### Add Rectangle Collision Shape

![rect-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-rectangle.png)

aaa

```
__.addRectangularShape(0, 0, 0, 0);
```

***

### Add Circle Collision Shape

![circle-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-circle.png)

aaa

```
__.addCircularShape(0, 0, 0);
```

***

### Add Polygon Collision Shape

![poly-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-polygon.png)

aaa

```
var polygonActor:Actor = __;
var vertices:Array<B2Vec2> = new Array<B2Vec2>();

polygonActor.addPolygonalShape(vertices);
```

***

### Add Point to Polygon Shape

![point-add-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-vertex.png)

aaa

```
polygonActor.addVertex(vertices, 0, 0);
```

***

### For Each Collision Shape...

![foreach-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/foreach-shape.png)

aaa

```
var shapeActor:Actor = __;
if (shapeActor.physicsMode == 0) {
	var body:B2Body = shapeActor.getBody();
	var fixture:B2Fixture = body.getFixtureList();
	while (fixture != null){
		
		fixture = fixture.getNext();
	}
}
```

***

### Make Collision Shape [Solid/Sensor]

![solid-sensor-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/shape-sensorsolid.png)

aaa

```
fixture.setSensor(true);
```

***

### Remove Collision Shape

![remove-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/shape-destroy.png)

aaa

```
body.DestroyFixture(fixture);
```

***

### Resize Collision Shape

![resize-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/shape-scale.png)

aaa

```
Actor.scaleShape(fixture.getShape(), body.getLocalCenter(), 0 / 100);
```

***

## Properties

### Set Actor Value

![set-val-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/actor-set-prop.png)

aaa

```
actor-set-prop
__.setActorValue("text", "anything");
```

***

### Get Actor Value

![get-val-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/actor-get-prop.png)

aaa

```
__.getActorValue("text")
```

***

### Convert to Boolean

![cast-bool-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/as-boolean.png)

aaa

```
asBoolean("anything")
```

***

### Convert to Number

![cast-number-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/as-number.png)

aaa

```
asNumber("anything")
```

***

### Convert to Text

![cast-text-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/tostring.png)

aaa

```
("" + "anything")
```

***
