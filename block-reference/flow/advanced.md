# Flow > Advanced

***

## Code

### Code Block (Single Line, Multi Line)

![code-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/CodeThumb.png)

Lets you embed code into your Behavior. Can be used in many ways. Particularly useful for calling functions that Stencyl or Haxe provide but don't exist in block form.

### Code Block (Inline)

![code-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/CodeInline.png)

Lets you embed a fragment of code into a block field.

***

## Constants

### Current Scale

![scale-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/CurrentScale.png)

Returns the current [scale](http://www.stencyl.com/help/view/mobile-app-scaling/) of the game. Either 1, 1.5, 2, 3 or 4.

```
Engine.SCALE
```

### Game URL

![game-url-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/GameURL.png)

Returns the URL of the website where this game is running (on Flash, HTML5). Returns an empty text on other platforms.

```
gameURL()
```

### Step Size

![step-size-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/StepSize.png)

Returns the number of milliseconds in each "frame" of the game. This corresponds to the time elapsed between updates to **when updating** events.

```
getStepSize()
```

***

## Platforms

***

## Memory Management

These blocks are deprecated. We now recommend handling [atlases](http://www.stencyl.com/help/view/mobile-atlases/) entirely using the Atlas page.

### Load/Unload Atlas

![atlas-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/Atlas.png)

Tells the game to load (or unload) an atlas in the **next** scene. Specify the **Atlas ID**.

```
loadAtlas([NUMBER]);
unloadAtlas([NUMBER]);
```

### Is Atlas Loaded?

![atlas-check-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/AtlasLoaded.png)

Returns `true` if the specified atlas (using Atlas ID) is currently loaded.

```
atlasIsLoaded([NUMBER])
```

***
