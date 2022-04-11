# Actors > Properties

***

## Alive / Dead

### <a name="die"></a> Kill Actor

![kill actor](https://static.stencyl.com/pedia2/block-images/actor/properties/die.png)

Immediately kills the specified actor.

If killing the current actor from its own actor behavior, the remaining logic will continue to run. We recommending using the stop block to prevent errors from happening in this case.

```
recycleActor([ACTOR]);
```

***

### <a name="kill-leave-screen"></a> Kill Actor (after leaving screen)

![kill actor after leaving screen](https://static.stencyl.com/pedia2/block-images/actor/properties/kill-leave-screen.png)

Instructs the game to kill the actor if it exits the screen. This is useful for "bullets" and other temporary actors that aren't of much use to hold around once they're off the screen.

```
[ACTOR].killSelfAfterLeavingScreen();
```

***

### <a name="isalive"></a> Is Actor alive?

![actor is alive](https://static.stencyl.com/pedia2/block-images/actor/properties/isalive.png)

Returns `true` if the specified actor is alive. Useful for checking prior to performing operations with that actor -- working with a dead actor may cause the game to crash.

```
[ACTOR].isAlive()
```

***

## Size

### <a name="get-wh"></a> Get Width / Height

![width of actor](https://static.stencyl.com/pedia2/block-images/actor/properties/get-wh.png)

Returns the width or height of the actor.

```
([ACTOR].getWidth())
([ACTOR].getHeight())
([ACTOR].getWidth()/2)
([ACTOR].getHeight()/2)
```

***

## Groups / Types

### <a name="getatype"></a> Get Actor Type

![type of actor](https://static.stencyl.com/pedia2/block-images/actor/properties/getatype.png)

Returns the actor's Actor Type.

```
[ACTOR].getType()
```

***

### <a name="getgroup"></a> Get Group

![group of actor](https://static.stencyl.com/pedia2/block-images/actor/properties/getgroup.png)

Returns the actor's (Collision) Group.

```
[ACTOR].getGroup()
```

***

### <a name="pick-type"></a> Choose Actor Type

![actor type](https://static.stencyl.com/pedia2/block-images/actor/properties/pick-type.png)

Returns the chosen Actor Type.

```
[ACTOR TYPE]
```

***

### <a name="pick-group"></a> Choose Actor Group

![actor group](https://static.stencyl.com/pedia2/block-images/actor/properties/pick-group.png)

Returns the chosen Actor Group. Useful for making comparisons in collision events.

```
getActorGroup([INT])
```

***

### <a name="pick-type-by-name"></a> Get Actor Type (from name)

![actor type with name text](https://static.stencyl.com/pedia2/block-images/actor/properties/pick-type-by-name.png)

Retrieves an Actor Type by name and returns it if it exists.

```
getActorTypeByName([TEXT])
```

***

### <a name="group-setresponse"></a> Set Collision Response

![set collision response of actorgroup and actorgroup to a sensor](https://static.stencyl.com/pedia2/block-images/actor/properties/group-setresponse.png)

Override the default collision response between two groups.

```
Collision.addResponse([ACTORGROUP], [ACTORGROUP], "sensor");
Collision.addResponse([ACTORGROUP], [ACTORGROUP], "solid");
```

***

## Performance

### <a name="ignore-screen-tolerance2"></a> Make Actor Always / Sometimes Active

![make actor active always](https://static.stencyl.com/pedia2/block-images/actor/properties/ignore-screen-tolerance2.png)

Normally, actors stop updating after they're off-screen. This block can turn that option off and makes them always active no matter where they are. Choosing "sometimes" sets the actor to the default behavior.

```
[ACTOR].makeAlwaysSimulate();
[ACTOR].makeSometimesSimulate();
```

***

### <a name="bullet-mode2"></a> Toggle Continuous Collision Detection

![enable continuous collision detection for actor](https://static.stencyl.com/pedia2/block-images/actor/properties/bullet-mode2.png)

Toggles whether an actor travels through terrain at high speeds.

```
makeActorNotPassThroughTerrain([ACTOR]);
makeActorPassThroughTerrain([ACTOR]);
```

***

## Collision Shapes

### <a name="addshape-rectangle"></a> Add Rectangle Collision Shape

![add rectangular collision shape x number y number w number h number to actor](https://static.stencyl.com/pedia2/block-images/actor/properties/addshape-rectangle.png)

Adds a new box collision shape to the actor's current animation.

```
[ACTOR].addRectangularShape([NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="addshape-circle"></a> Add Circle Collision Shape

![add circular collision shape x number y number r number to actor](https://static.stencyl.com/pedia2/block-images/actor/properties/addshape-circle.png)

Adds a new circle collision shape to the actor's current animation.

```
[ACTOR].addCircularShape([NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="addshape-polygon"></a> Add Polygon Collision Shape

![add polygonal collision shape to actor with vertices...](https://static.stencyl.com/pedia2/block-images/actor/properties/addshape-polygon.png)

Adds a new polygon collision shape to the actor's current animation. Specify the points using the next ``vertex`` block right below.

```
var polygonActor:Actor = [ACTOR];
var vertices:Array<B2Vec2> = new Array<B2Vec2>();
[ACTIONS]
polygonActor.addPolygonalShape(vertices);
```

***

### <a name="addshape-vertex"></a> Add Point to Polygon Shape

![vertex x number y number](https://static.stencyl.com/pedia2/block-images/actor/properties/addshape-vertex.png)

Adds a point to the newly created polygon collision shape. Must be used in the `add polygonal collision shape` block above.

```
polygonActor.addVertex(vertices, [NUMBER], [NUMBER]);
```

***

### <a name="foreach-shape"></a> For Each Collision Shape...

![for each of actor](https://static.stencyl.com/pedia2/block-images/actor/properties/foreach-shape.png)

Lets you perform certain actions on each collision shape for the actor. Use the `make the shape solid / a sensor`, `remove the shape` and `scale the shape` blocks below.

```
var shapeActor:Actor = [ACTOR];
if (shapeActor.physicsMode == 0) {
  var fixture:B2Fixture = shapeActor.getBody().getFixtureList();
  while (fixture != null) {
    [ACTIONS]
    fixture = fixture.getNext();
  }
}
```

***

### <a name="shape-sensorsolid2"></a> Make Collision Shape Solid / Sensor

![make collision shape a sensor](https://static.stencyl.com/pedia2/block-images/actor/properties/shape-sensorsolid2.png)

Sets the collision shape to be solid or a sensor (not solid but still can detect collisions).

```
[COLLISION SHAPE].setSensor(true); //Make it a sensor
[COLLISION SHAPE].setSensor(false); //Make it solid
```

***

### <a name="shape-destroy2"></a> Remove Collision Shape

![remove collision shape](https://static.stencyl.com/pedia2/block-images/actor/properties/shape-destroy2.png)

Removes the collision shape from the actor.

```
[COLLISION SHAPE].getBody().DestroyFixture([COLLISION SHAPE]);
```

***

### <a name="shape-scale2"></a> Resize Collision Shape

![scale collision shape by number %](https://static.stencyl.com/pedia2/block-images/actor/properties/shape-scale2.png)

Resizes the collision shape in percentage terms, relative to the original size (100%).

```
Actor.scaleShape([COLLISION SHAPE].getShape(), [COLLISION SHAPE].getBody().getLocalCenter(), [NUMBER] / 100);
```

***

### <a name="shape-group"></a> Get Collision Group for Shape

![collision group of collision shape](https://static.stencyl.com/pedia2/block-images/actor/properties/shape-group.png)

Returns the collision group assigned to a shape. Normally the group of the actor type the shape is attached to.

```
engine.getGroup([COLLISION SHAPE].groupID, [COLLISION SHAPE].getUserData())
```

***

### <a name="shape-setgroup"></a> Set Collision Group for Shape

![set collision group to actorgroup for collision shape](https://static.stencyl.com/pedia2/block-images/actor/properties/shape-setgroup.png)

Sets the collision group for this shape.

```
[COLLISION SHAPE].groupID = [ACTORGROUP].ID;
```

***

### <a name="shape-last-added"></a> Last Added Shape

![last added shape](https://static.stencyl.com/pedia2/block-images/actor/properties/shape-last-added.png)

Returns the last collision shape added to the actor.

```
[ACTOR].getLastCreatedFixture()
```

***

## Properties

### <a name="actor-set-prop"></a> Set Actor Value

![set actor value text for actor to object](https://static.stencyl.com/pedia2/block-images/actor/properties/actor-set-prop.png)

Associates a value with the given text key. Useful for storing (and later retrieving) arbitrary data in an actor without having to do this through other means in the toolset.

```
[ACTOR].setActorValue([TEXT], [VALUE]);
```

***

### <a name="actor-get-prop"></a> Get Actor Value

![get actor value text for actor](https://static.stencyl.com/pedia2/block-images/actor/properties/actor-get-prop.png)

Returns the value that is associated with the given text key, if available. Returns `null` if it doesn't exist.

```
[ACTOR].getActorValue([TEXT])
```

***
