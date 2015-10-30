# Scene > Actors

***

## Create Actor

### Create Actor

![create-actor3](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/create-actor3.png)

Creates an actor at the specified position.

```
createRecycledActor([ACTOR TYPE], [NUMBER], [NUMBER], Script.FRONT);
createRecycledActor([ACTOR TYPE], [NUMBER], [NUMBER], Script.MIDDLE);
createRecycledActor([ACTOR TYPE], [NUMBER], [NUMBER], Script.BACK);
```

***

### Create Actor on Layer

![create-actor-on-layer](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/create-actor-on-layer.png)

Creates an actor at the specified position and layer (given a Layer ID or Name).

```
createRecycledActorOnLayer([ACTOR TYPE], [NUMBER], [NUMBER], 0, [TEXT]); //By Layer ID
createRecycledActorOnLayer([ACTOR TYPE], [NUMBER], [NUMBER], 1, [TEXT]); //By Layer Name
```

***

## Get Actor

### Get Actor Instance

![actor](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actor.png)

Let you choose a specific actor instance to return.

```
[ACTOR]
```

***

### For Each Actor On Screen...

![actors-on-screen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-on-screen.png)

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

### For Each Actor in Region...

![actors-in-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-in-region.png)

Loops over all actors inside the specified region. Use the embedded `actor within region` block to refer to each actor.

```
for(actorInRegion in getActorsInRegion([REGION])) {
  if(actorInRegion != null && !actorInRegion.dead) {
    [ACTIONS]
  }
}
```

***

### For Each Actor of Type...

![actors-of-type3](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-of-type3.png)

Loops over all actors of a given Actor Type (whether on or off screen). Use the embedded `actor of type` block to refer to each actor.

```
for(actorOfType in getActorsOfType([ACTOR TYPE])) {
  if(actorOfType != null && !actorOfType.dead && !actorOfType.recycled) {
    [ACTIONS]		
  }
}
```

***

### For Each Actor of Actor Group...

![actors-in-group](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-in-group.png)

Loops over all actors inside the specified Actor Group (whether on or off screen). Use the embedded `member of group` block to refer to each actor.

```
for(actorInGroup in [ACTOR GROUP].list) {
  if(actorInGroup != null && !actorInGroup.dead && !actorInGroup.recycled) {
    [ACTIONS]
  }
}
```

***

