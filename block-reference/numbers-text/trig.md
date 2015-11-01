# Numbers & Text > Trig / Exponents

***

## Conversion

### <a name="to-degreesradians"></a> Degrees <--> Radians

![degrees-block](http://static.stencyl.com/pedia2/blocks/numbers_text/trig/Conversions.png)

Converts the given number to degrees or radians.

```
Util.toDegrees([NUMBER])
Util.toRadians([NUMBER])
```

***

## Constants

### <a name="pi"></a> Pi

![pi-block](http://static.stencyl.com/pedia2/blocks/numbers_text/trig/Pi.png)

Returns the value of Pi (3.14159...).

```
Math.PI
```

***

### <a name="e"></a> e

![e-block](http://static.stencyl.com/pedia2/blocks/numbers_text/exponents/ConstantE.png)

Returns e, the base of natural logarithms. (2.718...)

```
2.71828
```

***

## Trig Functions

### <a name="trig-master"></a> Sin / Cos / Tan

![trig-block](http://static.stencyl.com/pedia2/blocks/numbers_text/trig/Trig.png)

Returns the result of applying a trigonometric function to the given number. Dropdown for degrees/radians specifies what format the **incoming** number is in. Supports sin/cos/tan/asin/acos/atan.

```
//Incoming number is Degrees
Math.sin([NUMBER] * Utils.RAD)

//Incoming number is Radians
Math.sin([NUMBER])

//Other operations
Math.cos([NUMBER])
Math.tan([NUMBER])
Math.asin([NUMBER])
Math.acos([NUMBER])
Math.atan([NUMBER])
```

***

### <a name="atan2"></a> Inverse Tangent

![inverse-tan-block](http://static.stencyl.com/pedia2/blocks/numbers_text/trig/Atan.png)

Converts from rectangular to polar coordinates.

```
Math.atan2([NUMBER],[NUMBER])
```

#### Example: Point Actor Towards Mouse

![atan-example](http://static.stencyl.com/pedia2/blocks/numbers_text/trig/TrigExample1Thumb.png)

Using inverse tangent, we can calculate the angle to rotate the actor to based on the mouse's position.

***

## Exponents

### <a name="sqrt"></a> Square Root

![sqrt-block](http://static.stencyl.com/pedia2/blocks/numbers_text/exponents/ExponentSqrt.png)

Returns the square root of the given number.

```
Math.sqrt[NUMBER]
```

***

### <a name="pow"></a> Power

![power-block](http://static.stencyl.com/pedia2/blocks/numbers_text/exponents/ExponentExponent.png)

Returns the given number to the specified power (e.g., x<sup>y</sup>).

```
Math.pow[NUMBER, NUMBER]
```

***

### <a name="lnexp"></a> Natural Logarithm / E Raised to a Power

![log-block](http://static.stencyl.com/pedia2/blocks/numbers_text/exponents/LogBlocks.png)

**ln** - Returns the natural log of the given number.<br/>
**e^** - Returns the number e to the given power.

```
Math.log[NUMBER]
Math.exp[NUMBER]
```

***
