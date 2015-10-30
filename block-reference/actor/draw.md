# Actor > Draw

***

## Animation

### Draw Text

![draw-text-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/0%20-%20Drawing/draw-text.png)

aaa

```
aaa
```

***

## Layer (Z-Order)

***

## Drawing

### Show Sprite

![show-sprite-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/toggle-image.png)

Enables (or disables) the graphics for this actor. In other words, makes the actor invisible or visible. Everything else about the actor still works, and the `[actor] is on screen?` block will still return `true`.

```
[ACTOR].enableActorDrawing();
[ACTOR].disableActorDrawing();
```

***

### Set Opacity

![set-opacity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/set-opacity.png)

Sets the actor's opacity (alpha) value, which controls how "transparent" the actor is. Value must be between [0 - 100] inclusive. 0 means fully transparent. 100 is the default.

```
[ACTOR].alpha = [NUMBER] / 100;
```

***

### Get Opacity

![get-opacity-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-opacity.png)

Returns the actor's opacity (alpha) value as a value between [0 - 100] inclusive.

```
([ACTOR].alpha * 100)
```

***

## Anchoring

### Anchor Actor to Screen

![anchor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/anchor-screen.png)

Moves the actor to the HUD layer, which is on top of all regular layers. The actor will ignore the camera, so when the screen scrolls, the actor will still remain in the same place.

```
[ACTOR].anchorToScreen();
```

***

### Unanchor Actor from Screen

![unanchor-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/unanchor-screen.png)

Moves the actor back from the HUD layer.

```
[ACTOR].unanchorFromScreen();
```

***
