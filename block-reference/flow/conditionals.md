# Flow > Conditions

***

## Conditionals

### If

![if-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/if.png)

Checks whether the condition is `true` or `false`. If the condition is `true`, the blocks wrapped inside will execute.

```
if([BOOLEAN]) {
  [ACTIONS]
}
```

***

### Otherwise

![otherwise-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/else.png)

Used directly below an "If" block. If the condition in the preceding "If" block is `false`, the blocks wrapped inside the "Otherwise" block will execute.

```
else {
  [ACTIONS]
}
```

***

### Otherwise If

![otherwise-if-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/else-if.png)

Equivalent to doing the following.

![equivalent-to-otherwise-if-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/OtherwiseIf2.png)

```
else if([BOOLEAN]) {
  [ACTIONS]
}
```

***

## Booleans

Booleans (denoted by a hexagon shape) are conditions that resolve to `true` or `false`.

### And

![and-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/and.png)

Returns `true` if both of the provided conditions are `true`.

```
[BOOLEAN] && [BOOLEAN]
```

***

### Or

![or-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/or.png)

Returns `true` if at least one of the provided conditions is `true`. If the first condition is `true`, the second condition will not be evaluated.

```
[BOOLEAN] || [BOOLEAN]
```

***

### Not

![not-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/not.png)

Returns `true` if the condition resolves to `false`.

```
![BOOLEAN]
```

***

### True / False

![true-false-blocks](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/true.png) ![true-false-blocks](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/false.png)

Literal values of `true` and `false`.

***

### Boolean Conversion

![boolean-convert-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/as-boolean.png)

Converts the given value (typically text) into a Boolean. May throw a compile-time or runtime error if conversion is not possible.

```
asBoolean([VALUE])
```

***

## Equality

### Equals

![equals-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/eq.png)

Returns `true` if both values are equal.

```
[VALUE] == [VALUE]
```

***

### Not Equal

![not-equals-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/noteq.png)

Returns `true` if the values are not equal.

```
[VALUE] != [VALUE]
```

***

### Comparators

Returns `true` if...

Operator | Description
--- | ---
![less-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/less.png)|First number is smaller than second number.
![lte-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/lesseq.png)|First number is smaller than or equal to than second number.
![greater-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/more.png)|First number is larger than second number.
![gte-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/moreeq.png)|First number is larger than or equal to second number.

```
([NUMBER] < [NUMBER])
([NUMBER] <= [NUMBER])
([NUMBER] > [NUMBER])
([NUMBER] >= [NUMBER])
```

