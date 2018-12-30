# Scenes > Game Flow

***

> Read our guide on [Changing Scenes](http://www.stencyl.com/help/view/changing-scenes/) and [Pausing](http://www.stencyl.com/help/view/pausing/) for an explanation of these blocks.

***

## Transitions

### <a name="scene-change-color"></a> Switch Scene (Fade In/Out)

![switch to scene and fade out for number secs using color and fade in for number secs using color](http://static.stencyl.com/pedia2/block-images/scene/flow/scene-change-color.png)

Switches to a different scene using a fade in/out transition.

```
//Using fade in and out
switchScene([SCENE].getID(), createFadeOut([NUMBER], [COLOR]), createFadeIn([NUMBER], [COLOR]));

//Other Transition types
createBlindsOut([NUMBER], [COLOR]), createBlindsIn([NUMBER], [COLOR]),
createBubblesOut([NUMBER], [COLOR]), createBubblesIn([NUMBER], [COLOR]),
createCircleOut([NUMBER], [COLOR]), createCircleIn([NUMBER], [COLOR]),
createPixelizeOut([NUMBER], [COLOR]), createPixelizeIn([NUMBER], [COLOR]),
createRectangleOut([NUMBER], [COLOR]), createRectangleIn([NUMBER], [COLOR])
```

***

### <a name="scene-change-through"></a> Switch Scene (Crossfade / Slide)

![switch to scene and crossfade for number secs](http://static.stencyl.com/pedia2/block-images/scene/flow/scene-change-through.png)

Switches to a different scene using a crossfade or slide transition.

```
switchScene([SCENE].getID(), null, createCrossfadeTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideUpTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideDownTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideLeftTransition([NUMBER]));
switchScene([SCENE].getID(), null, createSlideRightTransition([NUMBER]));
```

***

### <a name="scene-reload-color"></a> Reload Current Scene (Fade In/Out)

![reload and fade out for number secs using color and fade in for number secs using color](http://static.stencyl.com/pedia2/block-images/scene/flow/scene-reload-color.png)

Reloads the current scene using a fade in/out transition.

```
//Using fade in and out
reloadCurrentScene(createFadeOut([NUMBER], [COLOR]), createFadeIn([NUMBER], [COLOR]));

//Other Transition types
createBlindsOut([NUMBER], [COLOR]), createBlindsIn([NUMBER], [COLOR]),
createBubblesOut([NUMBER], [COLOR]), createBubblesIn([NUMBER], [COLOR]),
createCircleOut([NUMBER], [COLOR]), createCircleIn([NUMBER], [COLOR]),
createPixelizeOut([NUMBER], [COLOR]), createPixelizeIn([NUMBER], [COLOR]),
createRectangleOut([NUMBER], [COLOR]), createRectangleIn([NUMBER], [COLOR])
```

***

### <a name="scene-reload-through"></a> Reload Current Scene (Crossfade / Slide)

![reload and crossfade for number secs](http://static.stencyl.com/pedia2/block-images/scene/flow/scene-reload-through.png)

Reloads the current scene using a crossfade or slide transition.

```
reloadCurrentScene(null, createCrossfadeTransition([NUMBER]));
reloadCurrentScene(null, createSlideUpTransition([NUMBER]));
reloadCurrentScene(null, createSlideDownTransition([NUMBER]));
reloadCurrentScene(null, createSlideLeftTransition([NUMBER]));
reloadCurrentScene(null, createSlideRightTransition([NUMBER]));
```

***

### <a name="scenebyname"></a> Get Scene (using name)

![scene with name text](http://static.stencyl.com/pedia2/block-images/scene/flow/scenebyname.png)

Returns a Scene by its name. Use inside a scene-switching block for an easy way to switch scenes by name.

```
GameModel.get().scenes.get(getIDForScene([TEXT]))
```

***

### <a name="is-transitioning"></a> Scene is transitioning?

![scene is transitioning](http://static.stencyl.com/pedia2/block-images/scene/flow/is-transitioning.png)

Returns `true` if the game is in the process of transitioning to another scene, transitioning from another scene, or reloading.

```
isTransitioning()
```

***

## Post-Transition

### <a name="create-actor3-next"></a> Create Actor in next scene

![create actortype at x number y number at front in next scene](http://static.stencyl.com/pedia2/block-images/scene/flow/create-actor3-next.png)

Notifies the game to creates an actor in the next scene (or the reload of the current one). This is useful, for example, for top-down games (like Zelda) where you'll exit the screen on one side and want to seamlessly reappear on the "correct" side.

```
createActorInNextScene([ACTOR TYPE], [NUMBER], [NUMBER], Script.FRONT);
createActorInNextScene([ACTOR TYPE], [NUMBER], [NUMBER], Script.MIDDLE);
createActorInNextScene([ACTOR TYPE], [NUMBER], [NUMBER], Script.BACK);
```

***

## Pausing

### <a name="pause-unpause"></a> Pause / Unpause Game

![pause game](http://static.stencyl.com/pedia2/block-images/scene/flow/pause-unpause.png)

[Pauses](http://www.stencyl.com/help/view/pausing/) (or unpauses) the game. You can selectively opt out actors on the Physics > Advanced page of their editor.

```
engine.pause();
engine.unpause();
```

***

### <a name="is-paused"></a> Game is Paused?

![game is paused](http://static.stencyl.com/pedia2/block-images/scene/flow/is-paused.png)

Returns `true` if the game is paused.

```
engine.isPaused()
```

***
