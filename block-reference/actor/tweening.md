# Actors > Tweening

***

> Read our article on [Tweening](https://www.stencyl.com/help/view/tweening/) for an explanation of these blocks.

***

## Slide

### <a name="moveToBy"></a> Slide

![slide actor by x number y number over number sec using dropdown](https://static.stencyl.com/pedia2/block-images/actor/tweening/moveToBy.png)

Slides (moves) the actor by the given distance (or to the given location) over the specified time.

```
[ACTOR].moveBy([NUMBER], [NUMBER], [NUMBER], [EASING]);
[ACTOR].moveTo([NUMBER], [NUMBER], [NUMBER], [EASING]);
```

***

## Spin

### <a name="spinToBy"></a> Spin

![spin actor by number degrees over number sec using dropdown](https://static.stencyl.com/pedia2/block-images/actor/tweening/spinToBy.png)

Spins (rotates) the actor [by / to] the given amount in degrees over the specified time. For the "to" case, it will always spin clockwise.

```
[ACTOR].spinBy([NUMBER], [NUMBER], [EASING]);
[ACTOR].spinTo([NUMBER], [NUMBER], [EASING]);
```

***

## Fade

### <a name="fadeInOut"></a> Fade In / Out

![fade in actor over number sec using dropdown](https://static.stencyl.com/pedia2/block-images/actor/tweening/fadeInOut.png)

Fades the actor [in / out] over the specified time. This means that its opacity will either go to 100% (fade in) or 0% (fade out).

```
[ACTOR].fadeTo(1, [NUMBER], [EASING]); //fade in
[ACTOR].fadeTo(0, [NUMBER], [EASING]); //fade out
```

***

### <a name="fadeTo"></a> Fade To

![fade actor to number % over number sec using dropdown](https://static.stencyl.com/pedia2/block-images/actor/tweening/fadeTo.png)

Sets the actor's opacity to the given amount (in percent) over the specified time. Amount must be between [0 - 100] inclusive.

```
[ACTOR].fadeTo([NUMBER] / 100, [NUMBER], [EASING]);
```

***

## Scale

### <a name="scaleTo"></a> Grow / Shrink

![grow actor to w number % h number % over number sec using dropdown](https://static.stencyl.com/pedia2/block-images/actor/tweening/scaleTo.png)

Resizes the actor's width and height (in percentage terms) over the specified time. Amounts are relative to the actor's original size -- 100% means original size, 200% means twice the size, 50% means half the size.

```
[ACTOR].growTo([NUMBER]/100, [NUMBER]/100, [NUMBER], [EASING]);
```

***
