# Attributes > Functions

***

## Operations

### <a name="tween-number"></a> Tween a Number Attribute

![change dropdown to number over number sec using dropdown](https://static.stencyl.com/pedia2/block-images/attributes/functions/tween-number.png)

Applies a [tween](https://www.stencyl.com/help/view/tweening/) to the given number attribute.

```
var attributeTween = attributeTweens.get("[ATTRIBUTE]");
if(attributeTween == null) {
  attributeTween = new TweenFloat();
  attributeTween.doOnUpdate(function() {[ATTRIBUTE] = attributeTween.value;});
  attributeTweens.set("[ATTRIBUTE]", attributeTween);
}
attributeTween.tween([ATTRIBUTE], [NUMBER], [EASING], Std.int([NUMBER]*1000));

//Or in one line (slower, uses dynamic typing)
tweenNumber([TEXT], [NUMBER], [NUMBER], [EASING]) //internal name, value, duration (seconds), easing
```

***

### <a name="cancel-tween-number"></a> Cancel Tween

![stop changing dropdown](https://static.stencyl.com/pedia2/block-images/attributes/functions/cancel-tween-number.png)

Stops an ongoing number tween.

```
abortTweenNumber("[ATTRIBUTE]");
```

***

### <a name="value"></a> Has Value?

![attribute has value](https://static.stencyl.com/pedia2/block-images/attributes/functions/value.png)

Returns `true` if the given attribute has a value (is not "null").

```
(hasValue([ATTRIBUTE]))
(!hasValue([ATTRIBUTE]))
```

***

### <a name="clear"></a> Clear Value of Attributes

![clear value of attribute](https://static.stencyl.com/pedia2/block-images/attributes/functions/clear.png)

Disassociates the given attribute from any value. (Sets its value to "null", does not have any effect on primitive types like numbers/booleans)

```
[ATTRIBUTE] = getDefaultValue([ATTRIBUTE]);
```

***
