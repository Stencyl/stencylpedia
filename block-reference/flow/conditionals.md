# Flow > Conditions

***

## Conditionals

### <a name="if"></a> If

![if boolean](https://static.stencyl.com/pedia2/block-images/flow/conditionals/if.png)

Checks whether the condition is `true` or `false`. If the condition is `true`, the blocks wrapped inside will execute.

```
if([BOOLEAN]) {
  [ACTIONS]
}
```

***

### <a name="else"></a> Otherwise

![otherwise](https://static.stencyl.com/pedia2/block-images/flow/conditionals/else.png)

Use directly below an "If" block. If the condition in the preceding "If" block is `false`, the blocks wrapped inside the "Otherwise" block will execute.

```
else {
  [ACTIONS]
}
```

***

### <a name="else-if"></a> Otherwise If

![otherwise if boolean](https://static.stencyl.com/pedia2/block-images/flow/conditionals/else-if.png)

Use directly below an "If" block. If the condition in the preceding "If" block is `false`, and the condition of this wrapper is `true`, the blocks wrapped inside the "Otherwise If" block will execute. Equivalent to doing the following:

![equivalent-to-otherwise-if-block](https://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/OtherwiseIf2.png)

```
else if([BOOLEAN]) {
  [ACTIONS]
}
```

***

## Booleans

Booleans (denoted by a hexagon shape) are conditions that resolve to `true` or `false`.

### <a name="and"></a> And

![boolean and boolean](https://static.stencyl.com/pedia2/block-images/flow/conditionals/and.png)

Returns `true` if both of the provided conditions are `true`. If the first condition is `false`, the second condition will not be evaluated.

```
[BOOLEAN] && [BOOLEAN]
```

***

### <a name="or"></a> Or

![boolean or boolean](https://static.stencyl.com/pedia2/block-images/flow/conditionals/or.png)

Returns `true` if at least one of the provided conditions is `true`. If the first condition is `true`, the second condition will not be evaluated.

```
[BOOLEAN] || [BOOLEAN]
```

***

### <a name="not"></a> Not

![not boolean](https://static.stencyl.com/pedia2/block-images/flow/conditionals/not.png)

Returns `true` if the condition resolves to `false`. Testing `if not [CONDITION]` is equivalent to `if [CONDITION] = false`.

```
![BOOLEAN]
```

***

### <a name="true"></a> <a name="false"></a> True / False

![true](https://static.stencyl.com/pedia2/block-images/flow/conditionals/true.png)
![false](https://static.stencyl.com/pedia2/block-images/flow/conditionals/false.png)

Literal values of `true` and `false`.

```
true
false
```

***

## Equality

### <a name="eq"></a> Equals

![object = object](https://static.stencyl.com/pedia2/block-images/flow/conditionals/eq.png)

Returns `true` if both values are equal.

```
[VALUE] == [VALUE]
```

***

### <a name="noteq"></a> Not Equal

![object not = object](https://static.stencyl.com/pedia2/block-images/flow/conditionals/noteq.png)

Returns `true` if the values are not equal.

```
[VALUE] != [VALUE]
```

***

### <a name="less"></a> <a name="lesseq"></a> <a name="more"></a> <a name="moreeq"></a> Comparators

Returns `true` if...

Operator | Description
--- | ---
![number < number](https://static.stencyl.com/pedia2/block-images/flow/conditionals/less.png)|First number is smaller than second number.
![number <= number](https://static.stencyl.com/pedia2/block-images/flow/conditionals/lesseq.png)|First number is smaller than or equal to than second number.
![number > number](https://static.stencyl.com/pedia2/block-images/flow/conditionals/more.png)|First number is larger than second number.
![number >= number](https://static.stencyl.com/pedia2/block-images/flow/conditionals/moreeq.png)|First number is larger than or equal to second number.

```
[NUMBER] < [NUMBER]
[NUMBER] <= [NUMBER]
[NUMBER] > [NUMBER]
[NUMBER] >= [NUMBER]
```

***

## Conversion

### <a name="as-boolean"></a> Boolean Conversion

![object as boolean](https://static.stencyl.com/pedia2/block-images/flow/conditionals/as-boolean.png)

Converts the given value (typically text) into a Boolean. May throw a compile-time or runtime error if conversion is not possible.

```
asBoolean([VALUE])
```

***

## Stop

### <a name="stop"></a> Stop

![stop](https://static.stencyl.com/pedia2/block-images/flow/conditionals/stop.png)

Skips the rest of the code in this event for the current step/frame.

```
return;
```

***
