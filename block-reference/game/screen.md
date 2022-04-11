# Game > Screen

***

## Screen Size

### <a name="set-screen-wh"></a> Set Screen Size

![set screen size to w int h int](https://static.stencyl.com/pedia2/block-images/game/screen/set-screen-wh.png)

Change the width / height of the game screen. On Desktop, this will change the size of the window.

```
Config.stageWidth = [INT];
Config.stageHeight = [INT];
engine.reloadScreen();
```

***

### <a name="screen-wh"></a> Screen Size

![screen width](https://static.stencyl.com/pedia2/block-images/game/screen/screen-wh.png)

Returns the game's screen width/height.

```
getScreenWidth()
getScreenHeight()
```

***

## Window Size

### <a name="set-fullscreen"></a> Set Fullscreen State

![set full screen enabled boolean](https://static.stencyl.com/pedia2/block-images/game/screen/set-fullscreen.png)

Enter or exit fullscreen. On some platforms, enter fullscreen must be in response to user input.

```
engine.setFullScreen([BOOLEAN]);
```

***

### <a name="is-fullscreen"></a> Is Game Fullscreen?

![full screen enabled](https://static.stencyl.com/pedia2/block-images/game/screen/is-fullscreen.png)

Returns true if the game is currently in fullscreen mode.

```
engine.isInFullScreen()
```

***

### <a name="set-windowscale"></a> Set Game Scale

![set game scale to number](https://static.stencyl.com/pedia2/block-images/game/screen/set-windowscale.png)

Set the window scale if playing in windowed mode.

```
Config.gameScale = [NUMBER];
engine.reloadScreen();
```

***

### <a name="get-windowscale"></a> Game Scale

![game scale](https://static.stencyl.com/pedia2/block-images/game/screen/get-windowscale.png)

Returns the game scale which applies if playing in windowed mode.

```
Config.gameScale
```

***

## Scale Mode

### <a name="set-scalemode"></a> Set Scale Mode

![set scale mode to int](https://static.stencyl.com/pedia2/block-images/game/screen/set-scalemode.png)

Set the scaling mode used by the game in fullscreen mode.

```
Config.scaleMode = [INT];
```

***

### <a name="get-scalemode"></a> Get Scale Mode

![scale mode](https://static.stencyl.com/pedia2/block-images/game/screen/get-scalemode.png)

Returns the scaling mode used by the game in fullscreen mode.

```
Config.scaleMode
```

***

### <a name="scalemode"></a> Scale Mode Values

![no scaling](https://static.stencyl.com/pedia2/block-images/game/screen/scalemode.png)

Use this block with the set / get scale mode blocks.

```
ScaleMode.NO_SCALING
ScaleMode.FULLSCREEN
ScaleMode.STRETCH_TO_FIT
ScaleMode.SCALE_TO_FIT_LETTERBOX
ScaleMode.SCALE_TO_FIT_FILL
ScaleMode.SCALE_TO_FIT_FULLSCREEN
```

***

### <a name="engine-scale"></a> Current Scale

![current scale](https://static.stencyl.com/pedia2/block-images/game/screen/engine-scale.png)

Returns the current [scale](https://www.stencyl.com/help/view/mobile-app-scaling/) of the game. Either 1, 1.5, 2, 3 or 4.

```
Engine.SCALE
```

***
