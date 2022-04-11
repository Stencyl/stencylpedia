# Numbers & Text > Math

***

## Arithmetic

### <a name="plus"></a> <a name="minus"></a> <a name="times"></a> <a name="div"></a> Add / Subtract / Multiply / Divide

![arithmetic-block](https://static.stencyl.com/pedia2/blocks/numbers_text/math/arithmetic.png)

Adds/Subtracts/Multiplies/Divides the two provided numbers. Note that only Chuck Norris can divide by 0.

```
([NUMBER] + [NUMBER])
([NUMBER] - [NUMBER])
([NUMBER] * [NUMBER])
([NUMBER] / [NUMBER])
```

***

### <a name="neg"></a> Negate

![negate number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/neg.png)

Flips the sign of the given number.

```
-([NUMBER])
```

***

### <a name="mod"></a> Remainder (Modulo)

![remainder of number / number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/mod.png)

Returns the integer remainder after dividing the first number by the second.

```
([NUMBER] % [NUMBER])
```

***

## Random Numbers

### <a name="randint"></a> Random Integer

![random integer between int and int](https://static.stencyl.com/pedia2/block-images/numbers-text/math/randint.png)

Returns a random integer between the first and second numbers, inclusive. Provide integers for both numbers.

```
randomInt([INT], [INT])
```

***

### <a name="randomfloat"></a> Random Float Between Numbers

![random float between number and number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/randomfloat.png)

Returns random floating point number between the first number (inclusive) and the second number (exclusive).

```
randomFloatBetween([NUMBER], [NUMBER])
```

***

### <a name="random"></a> Random Float Between Zero and One

![random float between 0.0 and 1.0](https://static.stencyl.com/pedia2/block-images/numbers-text/math/random.png)

Returns a random floating point number between 0 and 1, inclusive.

```
randomFloat()
```

***

## Increment / Decrement

### <a name="incdec"></a> Increment / Decrement Number

![increment dropdown by number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/incdec.png)

Adds (or subtracts) the given number to/from a **number attribute**.

```
[ATTRIBUTE] += [NUMBER];
[ATTRIBUTE] -= [NUMBER];
```

***

## Operations

### <a name="abs"></a> Absolute Value

![absolute value of number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/abs.png)

Returns the absolute value of the given number. (If it is negative, makes it positive.)

```
Math.abs([NUMBER])
```

***

### <a name="minmax"></a> Smaller / Larger of Two Numbers

![smaller-block](https://static.stencyl.com/pedia2/blocks/numbers_text/math/Smaller.png)
![larger-block](https://static.stencyl.com/pedia2/blocks/numbers_text/math/Larger.png)

Returns the smaller (or larger) of the two numbers.

```
Math.min([NUMBER], [NUMBER])
Math.max([NUMBER], [NUMBER])
```

***

### <a name="roundnew"></a> Round / Floor / Ceiling

![round number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/roundnew.png)

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

![object as number](https://static.stencyl.com/pedia2/block-images/numbers-text/math/as-number.png)

Converts the given value (can be any type) to a number. In practice, this is mainly useful for text and booleans (where true = 1, false = 0).

```
asNumber([VALUE])
```

***
