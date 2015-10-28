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

### Running on [PLATFORM]

![do-platform-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/RunningPlatform.png)

Returns `true` if the game is running on the selected platform.<br/>
Choices: [Flash, HTML5, Desktop, iOS, Android, Web, Mobile, Windows, Mac, Linux]

```
#if(PLATFORM) true #else false #end
```

### Running on [SPECIFIC IOS DEVICE]

![do-platform-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/RunningDevice.png)

Returns `true` if the game is running on the selected kind of iOS device. Useful if you want to fine-tune a game's display or behavior on specific devices.<br/>
Choices: [3.5" iPhone, 4.0" iPhone, 4.7" iPhone, 5.5" iPhone, iPad]

```
#if(mobile && !android) Engine.isStandardiOS #else false #end
#if(mobile && !android) Engine.isExtendedIOS #else false #end
#if(mobile && !android) Engine.isIPhone6 #else false #end
#if(mobile && !android) Engine.isIPhone6Plus #else false #end
#if(mobile && !android) Engine.isTabletIOS #else false #end
```

### Do only on [PLATFORM]

![do-platform-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/DoPlatform.png)

Include the wrapped blocks only on the specified platform. On other platforms, the wrapped blocks will not exist at all.<br/>
Choices: [Flash, HTML5, Desktop, iOS, Android, Web, Mobile, Windows, Mac, Linux]

```
#if(PLATFORM)
[ACTIONS]
#end
```

### Exit Game

![exit-block](http://static.stencyl.com/pedia2/blocks/flow/flow_advanced/Exit.png)

Quits out of a Desktop game. Does nothing on Flash/HTML5. On iOS/Android, it may send the app to the background (and goes against platform guidelines).

```
exitGame();
```

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
