# Scene > Actors

***

## Create Actor

### create %0 at ( x: %1 y: %2 ) at %3

![create-actor3](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/create-actor3.png)

Creates an actor.

```
createRecycledActor(!ERROR!, 0, 0, Script.FRONT);
```

***

### create %0 at ( x: %1 y: %2 ) on layer with %3 : %4

![create-actor-on-layer](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/create-actor-on-layer.png)

Creates an actor on a specific layer.

```
createRecycledActorOnLayer(!ERROR!, 0, 0, 0, "" + "text");
```

***

## Get Actor

### [sp] %0 [sp]

![actor](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actor.png)

Choose an actor.

```
__
```

***

### for each %1

![actors-on-screen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-on-screen.png)

Loops over all actors on the screen.

```
engine.allActors.reuseIterator = false;
for(actorOnScreen in engine.allActors)
{
	if(actorOnScreen != null && !actorOnScreen.dead && !actorOnScreen.recycled && actorOnScreen.isOnScreenCache)
	{
		
	}
}
engine.allActors.reuseIterator = true;
```

***

### for each %2 %0 

![actors-in-region](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-in-region.png)

Fetches all actors inside the region.

```
for(actorInRegion in getActorsInRegion(__))
{
	if(actorInRegion != null && !actorInRegion.dead){
		
	}
}
```

***

### for each  %2 %0

![actors-of-type3](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-of-type3.png)

Fetches all actors of the given type.

```
for(actorOfType in getActorsOfType(!ERROR!))
{
	if(actorOfType != null && !actorOfType.dead && !actorOfType.recycled){
		
	}
}
```

***

### for each %2 %0 

![actors-in-group](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/0%20-%20Actors/actors-in-group.png)

Fetches all actors that are members of the group.

```
for(actorInGroup in cast(!ERROR!, Group).list)
{
	if(actorInGroup != null && !actorInGroup.dead && !actorInGroup.recycled){
		
	}
}
```

***

