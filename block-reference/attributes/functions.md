# Attributes > Functions

***

## Operations

### Tween a Number Attribute

![tween-number-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/5%20-%20Functions/tween-number.png)

Applies a [tween](http://www.stencyl.com/help/view/tweening/) to the given number attribute (specified by internal name).

```
Actuate.tween(this, [NUMBER], {[TEXT]:[NUMBER]}).ease([EASING]);
```

***

### Has Value?

![value-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/5%20-%20Functions/value.png)

Returns `true` if the given attribute has a value (is not "null" or "empty").

```
(hasValue([ATTRIBUTE]))
```

***

### Clear Value of Attributes

![clear-block](http://static.stencyl.com/pedia2/block-images/5%20-%20Attributes/5%20-%20Functions/clear.png)

Disassociates the given attribute from any value. (Sets its value to "null", does not have any effect on primitive types like numbers/booleans)

```
if(!isPrimitive([ATTRIBUTE])) {
  [ATTRIBUTE] = getDefaultValue([ATTRIBUTE]);
}
```

***
