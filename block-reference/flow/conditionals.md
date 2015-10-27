# Flow > Conditions

***

## Conditionals

### If

![if-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/If.png)

Checks whether the condition is `true` or `false`. If the condition is `true`, the blocks wrapped inside will execute.

```
if([BOOLEAN]) {
  [ACTIONS]
}
```

***

### Otherwise

![otherwise-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/Otherwise.png)

Used directly below an "If" block. If the condition in the preceding "If" block is `false`, the blocks wrapped inside the "Otherwise" block will execute.

```
else {
  [ACTIONS]
}
```

***

### Otherwise If

![otherwise-if-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/OtherwiseIf.png)

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

![and-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/And.png)

Returns `true` if both of the provided conditions are `true`.

```
[BOOLEAN] && [BOOLEAN]
```

***

### Or

![or-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/Or.png)

Returns `true` if at least one of the provided conditions is `true`. If the first condition is `true`, the second condition will not be evaluated.

```
[BOOLEAN] || [BOOLEAN]
```

***

### Not

![not-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/Not.png)

Returns `true` if the condition resolves to `false`.

```
![BOOLEAN]
```

***

### True / False

![true-false-blocks](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/TrueFalse.png)

Literal values of `true` and `false`.

***

### Boolean Conversion

![boolean-convert-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/BooConvert.png)

Converts the given value (typically text) into a Boolean. May throw a compile-time or runtime error if conversion is not possible.

```
asBoolean([VALUE])
```

***

## Equality

### Equals

![equals-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/Equals.png)

Returns `true` if both values are equal.

```
[VALUE] == [VALUE]
```

***

### Not Equal

![not-equals-block](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/EqualsNot.png)

Returns `true` if the values are not equal.

```
[VALUE] != [VALUE]
```
