# Actor > Properties

***

## Alive / Dead

### <a name="die"></a> Kill Actor

![kill-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/die.png)

Immediately kills the specified actor. 

If killing the current actor from its own actor behavior, the remaining logic will continue to run. We recommending using the stop block to prevent errors from happening in this case.

```
recycleActor([ACTOR]);
```

***

### <a name="kill-leave-screen"></a> Kill Actor (after leaving screen)

![kill-actor-later-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/kill-leave-screen.png)

Instructs the game to kill the actor if it exits the screen. This is useful for "bullets" and other temporary actors that aren't of much use to hold around once they're off the screen.

```
[ACTOR].killSelfAfterLeavingScreen();
```

***

### <a name="isalive"></a> Is Actor alive?

![exists-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/isalive.png)

Returns `true` if the specified actor is alive. Useful for checking prior to performing operations with that actor -- working with a dead actor may cause the game to crash.

```
[ACTOR].isAlive()
```

***

## Size

### <a name="get-wh"></a> Get Width / Height

![size-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/get-wh.png)

Returns the width or height of the actor.

```
([ACTOR].getWidth())
([ACTOR].getHeight())
```

***

## Groups / Types

### <a name="getatype"></a> Get Actor Type

![gettype-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/getatype.png)

Returns the actor's Actor Type.

```
[ACTOR].getType()
```

***

### <a name="getgroup"></a> Get Group

![group-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/getgroup.png)

Returns the actor's (Collision) Group.

```
[ACTOR].getGroup()
```

***

### <a name="pick-type"></a> Choose Actor Type

![choose-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/pick-type.png)

Returns the chosen Actor Type.

```
[ACTOR TYPE]
```

***

### <a name="pick-group"></a> Choose Actor Group

![choose-group-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/pick-group.png)

Returns the chosen Actor Group. Useful for making comparisons in collision events.

```
[ACTOR GROUP]
```

***

### <a name="pick-type-by-name"></a> Get Actor Type (from name)

![pick-type-name-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/pick-type-by-name.png)

Retrieves an Actor Type by name and returns it if it exists.

```
getActorTypeByName([TEXT])
```

***

## Misc

### <a name="ignore-screen-tolerance"></a> Make Actor Always Active

![always-simulate-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/ignore-screen-tolerance.png)

Normally, actors stop updating after they're off-screen. This block turns that option off and makes them always active no matter where they are.

```
[ACTOR].makeAlwaysSimulate();
```

***

### <a name="bullet-mode"></a> Enable Continuous Collision Detection

![ccd-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/bullet-mode.png)

Enables continuous collision detection for the specified actor.

```
makeActorNotPassThroughTerrain([ACTOR]);
```

***

## Collision Shapes

### <a name="addshape-rectangle"></a> Add Rectangle Collision Shape

![rect-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-rectangle.png)

Adds a new box collision shape to the actor's current animation.

```
[ACTOR].addRectangularShape([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="addshape-circle"></a> Add Circle Collision Shape

![circle-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-circle.png)

Adds a new circle collision shape to the actor's current animation.

```
[ACTOR].addCircularShape([NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="addshape-polygon"></a> Add Polygon Collision Shape

![poly-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-polygon.png)

Adds a new polygon collision shape to the actor's current animation. Specify the points using the next ``vertex`` block right below.

```
var polygonActor:Actor = [ACTOR];
var vertices:Array<B2Vec2> = new Array<B2Vec2>();
[ACTIONS]
polygonActor.addPolygonalShape(vertices);
```

### <a name="addshape-vertex"></a> Add Point to Polygon Shape

![point-add-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/addshape-vertex.png)

Adds a point to the newly created polygon collision shape. Must be used in the `add polygonal collision shape` block above.

```
polygonActor.addVertex(vertices, [NUMBER], [NUMBER]);
```

***

### <a name="foreach-shape"></a> For Each Collision Shape...

![foreach-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/foreach-shape.png)

Lets you perform certain actions on each collision shape for the actor. Use the `make the shape solid / a sensor`, `remove the shape` and `scale the shape` blocks below.

```
var shapeActor:Actor = [ACTOR];
if (shapeActor.physicsMode == 0) {
	var body:B2Body = shapeActor.getBody();
	var fixture:B2Fixture = body.getFixtureList();
	while (fixture != null){
		[ACTIONS]
		fixture = fixture.getNext();
	}
}
```

### <a name="shape-sensorsolid"></a> Make Collision Shape Solid / Sensor

![solid-sensor-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/shape-sensorsolid.png)

Sets the collision shape to be solid or a sensor (not solid but still can detect collisions). Must be used within the `for each collision shape` block above.

```
fixture.setSensor(true); //Make it a sensor
fixture.setSensor(false); //Make it solid
```

### <a name="shape-destroy"></a> Remove Collision Shape

![remove-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/shape-destroy.png)

Removes the collision shape from the actor. Must be used within the `for each collision shape` block above.

```
body.DestroyFixture(fixture);
```

### <a name="shape-scale"></a> Resize Collision Shape

![resize-shape-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/shape-scale.png)

Resizes the collision shape in percentage terms, relative to the original size (100%). Must be used within the `for each collision shape` block above.

```
Actor.scaleShape(fixture.getShape(), body.getLocalCenter(), [NUMBER] / 100);
```

***

## Properties

### <a name="actor-set-prop"></a> Set Actor Value

![set-val-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/actor-set-prop.png)

Associates a value with the given text key. Useful for storing (and later retrieving) arbitrary data in an actor without having to do this through other means in the toolset.

```
[ACTOR].setActorValue([TEXT], [VALUE]);
```

***

### <a name="actor-get-prop"></a> Get Actor Value

![get-val-actor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/actor-get-prop.png)

Returns the value that is associated with the given text key, if available. Returns `null` if it doesn't exist.

```
[ACTOR].getActorValue([TEXT])
```

***

### <a name="as-boolean"></a> Convert to Boolean

![cast-bool-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/as-boolean.png)

Converts the value to a Boolean. Meant to be used in conjunction with the `get-actor-value` block.

```
asBoolean([VALUE])
```

***

### <a name="as-number"></a> Convert to Number

![cast-number-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/as-number.png)

Converts the value to a Number. Meant to be used in conjunction with the `get-actor-value` block.

```
asNumber([VALUE])
```

***

### <a name="as-text"></a> Convert to Text

![cast-text-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/2%20-%20Properties/tostring.png)

Converts the value to a Text value. Meant to be used in conjunction with the `get-actor-value` block.

```
("" + [VALUE])
```

***
