# Actor > Tweening

***

> Read our article on [Tweening](http://www.stencyl.com/help/view/tweening/) for an explanation of these blocks.

***

## Slide

### Slide

![slide-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/4%20-%20Tweening/moveToBy.png)

Slides (moves) the actor by the given distance (or to the given location) over the specified time.

```
[ACTOR].moveBy([NUMBER], [NUMBER], [NUMBER], [EASING]);
[ACTOR].moveTo([NUMBER], [NUMBER], [NUMBER], [EASING]);
```

***

## Spin

### Spin

![spin-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/4%20-%20Tweening/spinToBy.png)

Spins (rotates) the actor [by / to] the given amount in degrees over the specified time. For the "to" case, it will always spin clockwise.

```
[ACTOR].spinBy([NUMBER], [NUMBER], [EASING]);
[ACTOR].spinTo([NUMBER], [NUMBER], [EASING]);
```

***

## Fade

### Fade [In/Out]

![fade-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/4%20-%20Tweening/fadeInOut.png)

Fades the actor [in / out] over the specified time. This means that its opacity will either go to 100% (fade in) or 0% (fade out).

```
[ACTOR].fadeTo(1, [NUMBER], [EASING]); //fade in
[ACTOR].fadeTo(0, [NUMBER], [EASING]); //fade out
```

***

### Fade To

![fadeto-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/4%20-%20Tweening/fadeTo.png)

Sets the actor's opacity to the given amount (in percent) over the specified time. Amount must be between [0 - 100] inclusive.

```
[ACTOR].fadeTo([NUMBER] / 100, [NUMBER], [EASING]);
```

***

## Scale

### Grow / Shrink

![scale-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/4%20-%20Tweening/scaleTo.png)

Resizes the actor's width and height (in percentage terms) over the specified time. Amounts are relative to the actor's original size -- 100% means original size, 200% means twice the size, 50% means half the size.

```
[ACTOR].growTo([NUMBER]/100, [NUMBER]/100, [NUMBER], [EASING]);
```

***
