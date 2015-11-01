# Numbers & Text > Math

***

## Arithmetic

### <a name="plus"></a> <a name="minus"></a> <a name="times"></a> <a name="divide"></a>  Add / Subtract / Multiply / Divide

![arithmetic-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/arithmetic.png)

Adds/Subtracts/Multiplies/Divides the two provided numbers.

```
([NUMBER] + [NUMBER])
([NUMBER] - [NUMBER])
([NUMBER] * [NUMBER])
([NUMBER] / [NUMBER])
```

***

### <a name="neg"></a> Negate

![negate-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Negate.png)

Flips the sign of the given number.

```
-([NUMBER])
```

***

### <a name="mod"></a> Remainder (Modulo)

![remainder-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Remainder.png)

Returns the integer remainder after dividing the first number by the second.

```
([NUMBER] % [NUMBER])
```

***

## Random Numbers

### <a name="randint"></a> Random Integer

![random-int-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/RandomInt.png)

Returns a random integer between the first and second numbers, inclusive. Provide integers for both numbers.

```
randomInt(Math.floor(Number), Math.floor(Number))
```

***

### <a name="random"></a> Random Floating Point Number

![random-float-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/RandomFloat.png)

Returns a random floating point number between 0 and 1, inclusive.

```
randomFloat()
```

***

## Increment / Decrement

### <a name="incdec"></a> Increment / Decrement Number

![increment-decrement-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Increment.png)

Adds (or subtracts) the given number to/from a **number attribute**.

```
[ATTRIBUTE] += [NUMBER];
[ATTRIBUTE] -= [NUMBER];
```

***

## Operations

### <a name="abs"></a> Absolute Value

![abs-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/AbsoluteValue.png)

Returns the absolute value of the given number. (Makes it positive)

```
Math.abs([NUMBER])
```

***

### <a name="minmax"></a> Smaller / Larger of Two Numbers

![smaller-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Smaller.png)
![larger-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Larger.png)

Returns the smaller (or larger) of the two numbers.

```
Math.min([NUMBER], [NUMBER])
Math.max([NUMBER], [NUMBER])
```

***

### <a name="roundnew"></a> Round / Floor / Ceiling

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

### <a name="as-number"></a> Number Conversion

![number-convert-block](http://static.stencyl.com/pedia2/blocks/numbers_text/math/Conversion.png)

Converts the given value (can be any type) to a number. In practice, this is mainly useful for text and booleans (where true = 1, false = 0).

```
asNumber([VALUE])
```

***
