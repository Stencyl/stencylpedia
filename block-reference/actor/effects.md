# Actor > Effects

***

> Read our article on [Effects](http://www.stencyl.com/help/view/effects/) and [Blend Modes](http://www.stencyl.com/help/view/blending-modes/) for an explanation of these blocks.

***

## Blend Modes

### Set Blend Mode

![blend-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/set-blend-actor.png)

This block sets an actor's blend mode. [Blend Modes](http://www.stencyl.com/help/view/blending-modes/) control how a game draws semi-transparent graphics.

```
[ACTOR].setBlendMode([BLEND MODE]);
```

***

## Add / Remove

### Apply Effect

![apply-fx-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/apply-filter.png)

Applies the specified effect to the actor. Effects stack on each other in the order they were added.

```
[ACTOR].setFilter([[EFFECT]]);
```

***

### Remove all Effects

![remove-fx-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/clear-filter.png)

Removes all effects from the actor.

```
[ACTOR].clearFilters();
```

***

## Tint

### Tint using Color

![tint-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-tint.png)

Applies a "tinting" effect to an actor given a color and a percentage amount (where 0 means no tint and 100 means that the actor is completely colored).

```
createTintFilter([COLOR], [NUMBER]/100)
```

***

### Hue

![hue-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-hsb.png)

Shifts the hue of the actor, given an amount in degrees. The full spectrum spans 0 - 360 degrees inclusive and wraps around if you exceed that in either direction.

```
createHueFilter([NUMBER])
```

***

### Saturation

![saturation-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-sat.png)

Adjust how "vivid" the actor's colors are in percentage amount. 0% would make an actor grayscale. 100% would restore the default saturation. 200% would make it look very vivid.

```
createSaturationFilter([NUMBER])
```

***

### Brightness

![brightness-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-bright.png)

Adjust how bright (or dark) the actor is in percentage amount (0 - 100 inclusive). 0 means total darkness. 100 is the default.

```
createBrightnessFilter([NUMBER])
```

***

## Other

### Grayscale

![grayscale-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-grayscale.png)

Makes the actor draw in grayscale.

```
createGrayscaleFilter()
```

***

### Negative

![negative-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-negative.png)

Inverts the actor's colors.

```
createNegativeFilter()
```

***

### Sepia

![sepia-block](http://static.stencyl.com/pedia2/block-images/0%20-%20Actor/5%20-%20Effects/filter-sepia.png)

Applies an "old photograph" look to the actor. Sort of like grayscale but with a tinge of brown.

```
createSepiaFilter()
```

***
