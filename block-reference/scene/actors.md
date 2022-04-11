# Scenes > Actors

***

## Create Actor

### <a name="create-actor3"></a> Create Actor

![create actortype at x number y number at front](https://static.stencyl.com/pedia2/block-images/scene/actors/create-actor3.png)

Creates an actor at the specified position.

```
createRecycledActor([ACTOR TYPE], [NUMBER], [NUMBER], Script.FRONT);
createRecycledActor([ACTOR TYPE], [NUMBER], [NUMBER], Script.MIDDLE);
createRecycledActor([ACTOR TYPE], [NUMBER], [NUMBER], Script.BACK);
```

***

### <a name="create-actor-on-layer"></a> Create Actor on Layer

![create actortype at x number y number on layer with id object](https://static.stencyl.com/pedia2/block-images/scene/actors/create-actor-on-layer.png)

Creates an actor at the specified position and layer (given a Layer ID or Name).

```
createRecycledActorOnLayer([ACTOR TYPE], [NUMBER], [NUMBER], engine.getLayerById([INT]));
createRecycledActorOnLayer([ACTOR TYPE], [NUMBER], [NUMBER], engine.getLayerByName([TEXT]));
```

***

## Get Actor

### <a name="actor"></a> Get Actor Instance

![actor](https://static.stencyl.com/pedia2/block-images/scene/actors/actor.png)

Let you choose a specific actor instance to return.

```
[ACTOR]
```

***

### <a name="actors-on-screen"></a> For Each Actor On Screen ...

![for each](https://static.stencyl.com/pedia2/block-images/scene/actors/actors-on-screen.png)

Loops over all actors on the screen. Use the embedded `actor on screen` block to refer to each actor.

```
engine.allActors.reuseIterator = false;
for(actorOnScreen in engine.allActors) {
  if(actorOnScreen != null && !actorOnScreen.dead && !actorOnScreen.recycled && actorOnScreen.isOnScreenCache) {
    [ACTIONS]
  }
}
engine.allActors.reuseIterator = true;
```

***

### <a name="actors-in-region"></a> For Each Actor in Region ...

![for each region](https://static.stencyl.com/pedia2/block-images/scene/actors/actors-in-region.png)

Loops over all actors inside the specified region. Use the embedded `actor within region` block to refer to each actor.

```
for(actorInRegion in getActorsInRegion([REGION])) {
  if(actorInRegion != null && !actorInRegion.dead) {
    [ACTIONS]
  }
}
```

***

### <a name="actors-of-type3"></a> For Each Actor of Type ...

![for each actortype](https://static.stencyl.com/pedia2/block-images/scene/actors/actors-of-type3.png)

Loops over all actors of a given Actor Type (whether on or off screen). Use the embedded `actor of type` block to refer to each actor.

```
for(actorOfType in getActorsOfType([ACTOR TYPE])) {
  if(actorOfType != null && !actorOfType.dead && !actorOfType.recycled) {
    [ACTIONS]
  }
}
```

***

### <a name="actors-in-group"></a> For Each Actor of Actor Group ...

![for each actorgroup](https://static.stencyl.com/pedia2/block-images/scene/actors/actors-in-group.png)

Loops over all actors inside the specified Actor Group (whether on or off screen). Use the embedded `actor of group` block to refer to each actor.

```
for(actorInGroup in [ACTOR GROUP].list) {
  if(actorInGroup != null && !actorInGroup.dead && !actorInGroup.recycled) {
    [ACTIONS]
  }
}
```

***
