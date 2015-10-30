# Scene > Game Flow

***

> Read our guide on [changing scenes](http://www.stencyl.com/help/view/changing-scenes/) and [pausing](http://www.stencyl.com/help/view/pausing/) for an explanation of these blocks.

***

## Transitions

### Switch Scene (Fade In/Out)

![scene-change-color](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-change-color.png)

Switches to a different scene using a fade in/out transition.

```
switchScene([SCENE].getID(), createFadeOut([NUMBER], [COLOR]), createFadeIn([NUMBER], [COLOR]));
```

***

### Switch Scene (Crossfade / Slide)

![scene-change-through](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-change-through.png)

Switches to a different scene using a crossfade or slide transition.

```
switchScene([SCENE].getID(), null, createCrossfadeTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideUpTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideDownTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideLeftTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideRightTransition([NUMBER]));
```

***

### Reload Current Scene (Fade In/Out)

![scene-reload-color](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-reload-color.png)

Reloads the current scene using a fade in/out transition.

```
reloadCurrentScene(createFadeOut([NUMBER], [COLOR]), createFadeIn([NUMBER], [COLOR]));
```

***

### Reload Current Scene (Crossfade / Slide)

![scene-reload-through](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scene-reload-through.png)

Reloads the current scene using a crossfade or slide transition.

```
reloadCurrentScene(null, createCrossfadeTransition([NUMBER]));
reloadCurrentScene(null, createSlideUpTransition([NUMBER]));
reloadCurrentScene(null, createSlideDownTransition([NUMBER]));
reloadCurrentScene(null, createSlideLeftTransition([NUMBER]));
reloadCurrentScene(null, createSlideRightTransition([NUMBER]));
```

***

### Get Scene (using name)

![scenebyname](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/scenebyname.png)

Returns a Scene by its name. Use inside a scene-switching block for an easy way to switch scenes by name or by text.

```
GameModel.get().scenes.get(getIDForScene([TEXT]))
```

***

### Scene is transitioning?

![is-transitioning](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/is-transitioning.png)

Returns `true` if the game is in the process of transitioning to another scene, transitiont from another scene or reloading.

```
isTransitioning()
```

***

## Post-Transition

### Create Actor in next scene

![create-actor3-next](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/create-actor3-next.png)

Notifies the game to creates an actor in the next scene (or the reload of the current one). This is useful for top-down games (like Zelda) where you'll exit the screen on one side and want to seamlessly reappear on the "correct" side.

```
createActorInNextScene([ACTOR TYPE], [NUMBER], [NUMBER], Script.FRONT);
createActorInNextScene([ACTOR TYPE], [NUMBER], [NUMBER], Script.MIDDLE);
createActorInNextScene([ACTOR TYPE], [NUMBER], [NUMBER], Script.BACK);
```

***

## Pausing

### [Pause / Unpause] Game

![pause-unpause](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/pause-unpause.png)

[Pauses](http://www.stencyl.com/help/view/pausing/) (or Unpauses) the game. You can selectively opt out actors on the Physics > Advanced page of their editor.

```
engine.pause();
engine.unpause();
```

***

### Game is Paused?

![is-paused](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/5%20-%20Game Flow/is-paused.png)

Return `true` if the game is paused.

```
engine.isPaused()
```

***

