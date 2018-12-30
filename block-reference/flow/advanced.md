# Flow > Advanced

***

## Code

### <a name="custom-code"></a> <a name="code-long"></a> Code Block (Single Line, Multi Line)

![code text](http://static.stencyl.com/pedia2/block-images/flow/advanced/custom-code.png)<br/>
![code text](http://static.stencyl.com/pedia2/block-images/flow/advanced/code-long.png)

Lets you embed code into your Behavior. Can be used in many ways. Particularly useful for calling functions that Stencyl or Haxe provide but don't exist in block form. Take a look at our [API](http://static.stencyl.com/api/33/) to see what's available.

***

### <a name="code-short"></a> Code Block (Inline)

![code text](http://static.stencyl.com/pedia2/block-images/flow/advanced/code-short.png)

Lets you embed a fragment of code into a block field.

***

## Constants

### <a name="game-url"></a> Game URL

![game url](http://static.stencyl.com/pedia2/block-images/flow/advanced/game-url.png)

Returns the URL of the website where this game is running (on Flash, HTML5). Returns an empty text on other platforms.

```
gameURL()
```

***

### <a name="language"></a> language

![language](http://static.stencyl.com/pedia2/block-images/flow/advanced/language.png)

The language code of the system (device) on which the game is running.

```
openfl.system.Capabilities.language
```

***

### <a name="stepsize"></a> Step Size

![step size](http://static.stencyl.com/pedia2/block-images/flow/advanced/stepsize.png)

Returns the number of milliseconds in each "step" of the game. This corresponds to the time elapsed between updates to `when updating` events. The default step size is 10 milliseconds.

```
getStepSize()
```

***

### <a name="null"></a> null

![null](http://static.stencyl.com/pedia2/block-images/flow/advanced/null.png)

Returns "null", which stands for the absence of a value.

```
null
```

***

## Platforms

### <a name="is-platform"></a> Running on Platform

![running on platform](http://static.stencyl.com/pedia2/block-images/flow/advanced/is-platform.png)

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

***

### <a name="is-device2"></a> Running on Specific iOS Device

![running on device](http://static.stencyl.com/pedia2/block-images/flow/advanced/is-device2.png)

Returns `true` if the game is running on the selected kind of iOS device. Useful if you want to fine-tune a game's display or behavior on specific devices.

**Choices:**
* 3.5" iPhone
* 4.0" iPhone
* 4.7" iPhone
* 5.5" iPhone
* iPad

```
#if(ios) Engine.isStandardIOS #else false #end
#if(ios) Engine.isExtendedIOS #else false #end
#if(ios) Engine.isIPhone6 #else false #end
#if(ios) Engine.isIPhone6Plus #else false #end
#if(ios) Engine.isTabletIOS #else false #end
#if(ios) Engine.isIPhoneX #else false #end
#if(ios) Engine.isIPhoneXMax #else false #end
#if(ios) Engine.isIPhoneXR #else false #end
```

***

### <a name="do-on-platform"></a> Do only on Platform

![do only on platform](http://static.stencyl.com/pedia2/block-images/flow/advanced/do-on-platform.png)

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

![exit game](http://static.stencyl.com/pedia2/block-images/flow/advanced/exit-game.png)

Quits out of a Desktop game or standalone Flash game. Does nothing on Flash/HTML5 running in a browser. On iOS/Android, it may send the app to the background (and goes against platform guidelines).

```
exitGame();
```

***

## Memory Management

These blocks are deprecated. We now recommend handling [atlases](http://www.stencyl.com/help/view/mobile-atlases/) entirely using the Atlas page.

### <a name="load-unload-atlas"></a> Load / Unload Atlas

![load atlas with id int](http://static.stencyl.com/pedia2/block-images/flow/advanced/load-unload-atlas.png)

Tells the game to load (or unload) an atlas in the **next** scene. Specify the **Atlas ID**.

```
loadAtlas([INT]);
unloadAtlas([INT]);
```

***

### <a name="atlas-loaded"></a> Is Atlas Loaded?

![atlas with id int is loaded](http://static.stencyl.com/pedia2/block-images/flow/advanced/atlas-loaded.png)

Returns `true` if the specified atlas (using Atlas ID) is currently loaded.

```
atlasIsLoaded([INT])
```

***
