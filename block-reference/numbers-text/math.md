# Numbers & Text > Math

***

## Arithmetic

### Add / Subtract / Multiply / Divide

![arithmetic-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/arithmetic.png)

Adds/Subtracts/Multiplies/Divides the two provided numbers.

```
([NUMBER] + [NUMBER])
([NUMBER] - [NUMBER])
([NUMBER] * [NUMBER])
([NUMBER] / [NUMBER])
```

***

### Negate

![negate-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Negate.png)

Flips the sign of the given number.

```
-([NUMBER])
```

***

### Remainder (Modulo)

![remainder-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Remainder.png)

Returns the integer remainder after dividing the first number by the second.

```
([NUMBER] % [NUMBER])
```

***

## Random Numbers

### Random Integer

![random-int-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/RandomInt.png)

Returns a random integer between the first and second numbers, inclusive. Provide integers for both numbers.

```
randomInt(Math.floor(Number), Math.floor(Number))
```

***

### Random Floating Point Number

![random-float-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/RandomFloat.png)

Returns a random floating point number between 0 and 1, inclusive.

```
randomFloat()
```

***

## Increment / Decrement

***

### Increment / Decrement Number

![increment-decrement-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Increment.png)

Adds (or subtracts) the given number to/from a **number attribute**.

```
[ATTRIBUTE] += [NUMBER];
[ATTRIBUTE] -= [NUMBER];
```

***

## Operations

### Absolute Value

![abs-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/AbsoluteValue.png)

Returns the absolute value of the given number. (Makes it positive)

```
Math.abs([NUMBER])
```

***

### Smaller / Larger of Two Numbers

![smaller-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Smaller.png)
![larger-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Larger.png)

Returns the smaller (or larger) of the two numbers.

```
Math.min([NUMBER], [NUMBER])
Math.max([NUMBER], [NUMBER])
```

***

### Round / Floor / Ceiling

![round-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Round.png)

Returns the nunber as an integer, with rounding applied as follows:

**Round** - Rounds up if the fractional part is 0.5 or more. Otherwise, rounds down.

**Floor** - Always rounds down.

**Ceiling** - Always rounds up.

```
Math.round([NUMBER])
Math.floor([NUMBER])
Math.ceil([NUMBER])
```

***

## Conversion

***

### Number Conversion

![number-convert-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Conversion.png)

Converts the given object to a number. In practice, this is mainly useful for text and booleans (where true = 1, false = 0).

```
asNumber([ANYTHING])
```

***
