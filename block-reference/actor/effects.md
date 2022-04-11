# Actors > Effects

***

> Read our article on [Effects](https://www.stencyl.com/help/view/effects/) and [Blend Modes](https://www.stencyl.com/help/view/blending-modes/) for an explanation of these blocks.

***

## Blend Modes

### <a name="set-blend-actor"></a> Set Blend Mode

![set blend mode for actor to dropdown](https://static.stencyl.com/pedia2/block-images/actor/effects/set-blend-actor.png)

This block sets an actor's blend mode. [Blend Modes](https://www.stencyl.com/help/view/blending-modes/) control how a game draws semi-transparent graphics.

```
[ACTOR].setBlendMode([BLEND MODE]);
```

***

## Add / Remove

### <a name="apply-filter"></a> Apply Effect

![apply effect filter to actor](https://static.stencyl.com/pedia2/block-images/actor/effects/apply-filter.png)

Applies the specified effect to the actor. Effects stack on each other in the order they were added.

```
[ACTOR].setFilter([[EFFECT]]);
```

***

### <a name="clear-filter"></a> Remove all Effects

![remove all effects from actor](https://static.stencyl.com/pedia2/block-images/actor/effects/clear-filter.png)

Removes all effects from the actor.

```
[ACTOR].clearFilters();
```

***

## Effects

### <a name="filter-tint"></a> Tint using Color

![tint using color at number %](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-tint.png)

Applies a "tinting" effect to an actor given a color and a percentage amount (where 0 means no tint and 100 means that the actor is completely colored).

```
createTintFilter([COLOR], [NUMBER]/100)
```

***

### <a name="filter-hsb"></a> Hue

![adjust hue by number degrees](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-hsb.png)

Shifts the hue of the actor, given an amount in degrees. The full spectrum spans 0 - 360 degrees inclusive and wraps around if you exceed that in either direction.

```
createHueFilter([NUMBER])
```

***

### <a name="filter-sat"></a> Saturation

![set saturation to number %](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-sat.png)

Adjust how "vivid" the actor's colors are in relative percentage amounts. 0% would make an actor grayscale. 100% would restore the default saturation. 200% would make it look very vivid.

```
createSaturationFilter([NUMBER])
```

***

### <a name="filter-bright"></a> Brightness

![adjust brightness by number %](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-bright.png)

Adjust how bright (or dark) the actor is in relative percentage amounts. 0% means total darkness. 100% is the default. 200% would make it brighter than usual.

```
createBrightnessFilter([NUMBER])
```

***

### <a name="filter-grayscale"></a> Grayscale

![make grayscale](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-grayscale.png)

Makes the actor draw in grayscale.

```
createGrayscaleFilter()
```

***

### <a name="filter-negative"></a> Negative

![make negative](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-negative.png)

Inverts the actor's colors.

```
createNegativeFilter()
```

***

### <a name="filter-sepia"></a> Sepia

![make sepia](https://static.stencyl.com/pedia2/block-images/actor/effects/filter-sepia.png)

Applies an "old photograph" look to the actor. Sort of like grayscale but with a tinge of brown.

```
createSepiaFilter()
```

***
