# Scene > Game Flow

***

## Transitions

### switch to %0 and %1 for %2 secs using %3 and %4 for %5 secs using %6

![scene-change-color](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-change-color.png)

Switches to a different scene using a visual transition.

```
switchScene(!ERROR!.getID(), createFadeOut(0, Utils.getColorRGB(0,0,0)), createFadeIn(0, Utils.getColorRGB(0,0,0)));
```

***

### switch to %0 and %1 for %2 secs

![scene-change-through](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-change-through.png)

Switches to a different scene using a visual transition.

```
switchScene(!ERROR!.getID(), null, createCrossfadeTransition(0));
```

***

### reload and %0 for %1 secs using %2 and %3 for %4 secs using %5

![scene-reload-color](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-reload-color.png)

Reloads the current scene using a visual transition.

```
reloadCurrentScene(createFadeOut(0, Utils.getColorRGB(0,0,0)), createFadeIn(0, Utils.getColorRGB(0,0,0)));
```

***

### reload and %0 for %1 secs

![scene-reload-through](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-reload-through.png)

Reloads the current scene using a visual transition.

```
reloadCurrentScene(null, createCrossfadeTransition(0));
```

***

### scene with name: %0

![scenebyname](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scenebyname.png)

Get a Scene by its name. Use inside a switch to scene block.

```
GameModel.get().scenes.get(getIDForScene("text"))
```

***

### scene is transitioning

![is-transitioning](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/is-transitioning.png)

Returns true if scene is in transition mode.

```
isTransitioning()
```

***

## Post-Transition

### create %0 at ( x: %1 y: %2 ) at %3 in next scene

![create-actor3-next](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/create-actor3-next.png)

Creates an actor in the next scene.

```
createActorInNextScene(!ERROR!, 0, 0, Script.FRONT);
```

***

## Pausing

### %0 game

![pause-unpause](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/pause-unpause.png)

Pause/Unpause the game. Opt out actors in the Physics > Advanced page.

```
engine.pause();
```

***

### game is paused

![is-paused](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/is-paused.png)

Return true if the game is paused.

```
engine.isPaused()
```

***

