# Actor > Draw

***

## Animation

### Current Animation

![get-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/getanim.png)

aaa

```
aaa
```

***

### Switch Animation

![switch-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setanim.png)

aaa

```
aaa
```

***

### Get Animation (from text)

![get-text-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/string-to-anim.png)

aaa

```
aaa
```

***

### Is an Animation playing?

![is-playing-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/is-anim.png)

aaa

```
aaa
```

***

### Set Frame # for Animation

![set-frame-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/set-frame.png)

aaa

```
aaa
```

***

### Get Current Frame #

![get-frame-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-frame.png)

aaa

```
aaa
```

***

### Get Number of Frames in Current Animation

![get-num-frames-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-num-frames.png)

aaa

```
aaa
```

***

### Get Duration of Current Frame

![get-frame-duration-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/get-frame-duration.png)

aaa

```
aaa
```

***

### Set Duration of Current Frame

![set-frame-duration-anim-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/set-frame-duration.png)

aaa

```
aaa
```

***

## Layer (Z-Order)

### Get Layer ID

![get-layerid-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/getlayer.png)

aaa

```
aaa
```

***

### Switch Layer by ID

![switch-layer-id-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setzindex.png)

aaa

```
aaa
```

***

### Switch Layer

![switch-layer-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setlayer2.png)

aaa

```
aaa
```

***

### Switch Order (within layer)

![switch-order-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/movewithinlayer.png)

aaa

```
aaa
```

***

### Get Z-Order (within layer)

![get-order-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/zindex.png)

aaa

```
aaa
```

***

### Set Z-Order (within layer)

![set-order-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/setzindex.png)

aaa

```
aaa
```

***

### Number of Actors within Layer

![num-actors-layer-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/actorswithinlayer2.png)

aaa

```
aaa
```

***

## Drawing

### [Show/Hide] Sprite

![show-sprite-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/3%20-%20Draw/toggle-image.png)

Makes the actor invisible or visible. Everything else about the actor still works, and the `[actor] is on screen?` block will still return `true`.

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
