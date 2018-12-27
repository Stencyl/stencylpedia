# Flow > Conditions

***

## Conditionals

### <a name="if"></a> If

![if-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/if.png)

Checks whether the condition is `true` or `false`. If the condition is `true`, the blocks wrapped inside will execute.

```
if([BOOLEAN]) {
  [ACTIONS]
}
```

***

### <a name="else"></a> Otherwise

![otherwise-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/else.png)

Use directly below an "If" block. If the condition in the preceding "If" block is `false`, the blocks wrapped inside the "Otherwise" block will execute.

```
else {
  [ACTIONS]
}
```

***

### <a name="else-if"></a> Otherwise If

![otherwise-if-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/else-if.png)

Use directly below an "If" block. If the condition in the preceding "If" block is `false`, and the condition of this wrapper is `true`, the blocks wrapped inside the "Otherwise If" block will execute. Equivalent to doing the following:

![equivalent-to-otherwise-if-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/OtherwiseIf2.png)

```
else if([BOOLEAN]) {
  [ACTIONS]
}
```

***

## Booleans

Booleans (denoted by a hexagon shape) are conditions that resolve to `true` or `false`.

### <a name="and"></a> And

![and-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/and.png)

Returns `true` if both of the provided conditions are `true`. If the first condition is `false`, the second condition will not be evaluated.

```
[BOOLEAN] && [BOOLEAN]
```

***

### <a name="or"></a> Or

![or-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/or.png)

Returns `true` if at least one of the provided conditions is `true`. If the first condition is `true`, the second condition will not be evaluated.

```
[BOOLEAN] || [BOOLEAN]
```

***

### <a name="not"></a> Not

![not-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/not.png)

Returns `true` if the condition resolves to `false`. Testing `if not [CONDITION]` is equivalent to `if [CONDITION] = false`.

```
![BOOLEAN]
```

***

### <a name="true"></a> <a name="false"></a> True / False

![true-false-blocks](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/true.png) ![true-false-blocks](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/false.png)

Literal values of `true` and `false`.

***

### <a name="as-boolean"></a> Boolean Conversion

![boolean-convert-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/as-boolean.png)

Converts the given value (typically text) into a Boolean. May throw a compile-time or runtime error if conversion is not possible.

```
asBoolean([VALUE])
```

***

## Equality

### <a name="eq"></a> Equals

![equals-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/eq.png)

Returns `true` if both values are equal.

```
[VALUE] == [VALUE]
```

***

### <a name="noteq"></a> Not Equal

![not-equals-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/0%20-%20Conditions/noteq.png)

Returns `true` if the values are not equal.

```
[VALUE] != [VALUE]
```

***

### <a name="less"></a> <a name="lesseq"></a> <a name="more"></a> <a name="moreeq"></a> Comparators

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

***
