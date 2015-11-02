# Flow > Advanced

***

## Code

### <a name="code-long"></a> Code Block (Single Line, Multi Line)

![code-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/custom-code.png)<br/>
![code-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/code-long.png)

Lets you embed code into your Behavior. Can be used in many ways. Particularly useful for calling functions that Stencyl or Haxe provide but don't exist in block form. Take a look at our [API](http://static.stencyl.com/api/33/) to see what's available.

***

### <a name="custom-code"></a> Code Block (Inline)

![code-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/code-short.png)

Lets you embed a fragment of code into a block field.

***

## Constants

### <a name="engine-scale"></a> Current Scale

![scale-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/engine-scale.png)

Returns the current [scale](http://www.stencyl.com/help/view/mobile-app-scaling/) of the game. Either 1, 1.5, 2, 3 or 4.

```
Engine.SCALE
```

***

### <a name="game-url"></a> Game URL

![game-url-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/game-url.png)

Returns the URL of the website where this game is running (on Flash, HTML5). Returns an empty text on other platforms.

```
gameURL()
```

***

### <a name="stepsize"></a> Step Size

![step-size-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/stepsize.png)

Returns the number of milliseconds in each "step" of the game. This corresponds to the time elapsed between updates to **when updating** events. The default step size is 10 milliseconds.

```
getStepSize()
```

***

## Platforms

### <a name="is-platform"></a> Running on Platform

![do-platform-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/is-platform.png)

Returns `true` if the game is running on the selected platform.

**Choices:**
* Flash
* HTML5
* Desktop
* iOS
* Android
* Web
* Mobile
* Windows
* Mac
* Linux

```
#if(PLATFORM) true #else false #end
```

### <a name="is-device2"></a> Running on Specific iOS Device

![do-platform-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/is-device2.png)

Returns `true` if the game is running on the selected kind of iOS device. Useful if you want to fine-tune a game's display or behavior on specific devices.

**Choices:**
* 3.5" iPhone
* 4.0" iPhone
* 4.7" iPhone
* 5.5" iPhone
* iPad

```
#if(mobile && !android) Engine.isStandardiOS #else false #end
#if(mobile && !android) Engine.isExtendedIOS #else false #end
#if(mobile && !android) Engine.isIPhone6 #else false #end
#if(mobile && !android) Engine.isIPhone6Plus #else false #end
#if(mobile && !android) Engine.isTabletIOS #else false #end
```

***

### <a name="do-on-platform"></a> Do only on Platform

![do-platform-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/do-on-platform.png)

Include the wrapped blocks only on the specified platform. On other platforms, the wrapped blocks will not exist at all.

**Choices:**
* Flash
* HTML5
* Desktop
* iOS
* Android
* Web
* Mobile
* Windows
* Mac
* Linux

```
#if(PLATFORM)
[ACTIONS]
#end
```

***

### <a name="exit-game"></a> Exit Game

![exit-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/exit-game.png)

Quits out of a Desktop game or standalone Flash game. Does nothing on Flash/HTML5 running in a browser. On iOS/Android, it may send the app to the background (and goes against platform guidelines).

```
exitGame();
```

***

## Memory Management

These blocks are deprecated. We now recommend handling [atlases](http://www.stencyl.com/help/view/mobile-atlases/) entirely using the Atlas page.

### <a name="load-unload-atlas"></a> Load / Unload Atlas

![atlas-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/load-unload-atlas.png)

Tells the game to load (or unload) an atlas in the **next** scene. Specify the **Atlas ID**.

```
loadAtlas([NUMBER]);
unloadAtlas([NUMBER]);
```

***

### <a name="atlas-loaded"></a> Is Atlas Loaded?

![atlas-check-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/4%20-%20Advanced/atlas-loaded.png)

Returns `true` if the specified atlas (using Atlas ID) is currently loaded.

```
atlasIsLoaded([NUMBER])
```

***
