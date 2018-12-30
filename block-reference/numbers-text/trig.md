# Numbers & Text > Trig / Exponents

***

## Conversion

### <a name="to-degreesradians"></a> Degrees <--> Radians

![number as degrees](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/to-degreesradians.png)

Converts the given number to degrees or radians.

```
Utils.DEG * [NUMBER]
Utils.RAD * [NUMBER]
```

***

## Constants

### <a name="pi"></a> Pi

![pi](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/pi.png)

Returns the value of Pi (3.14159...).

```
Math.PI
```

***

### <a name="e"></a> e

![e](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/e.png)

Returns e, the base of natural logarithms. (2.718...)

```
2.71828
```

***

## Trig Functions

### <a name="trig-master"></a> Sin / Cos / Tan

![sin number degrees](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/trig-master.png)

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

![atan2 y number x number](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/atan2.png)

Converts from rectangular to polar coordinates. The return value is in radians.

```
Math.atan2([NUMBER], [NUMBER])
```

#### Example: Point Actor Towards Mouse

![atan-example](http://static.stencyl.com/pedia2/blocks/numbers_text/trig/TrigExample1Thumb.png)

Using inverse tangent, we can calculate the angle to rotate the actor to based on the mouse's position.

***

## Exponents

### <a name="sqrt"></a> Square Root

![sqrt number](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/sqrt.png)

Returns the square root of the given number.

```
Math.sqrt([NUMBER])
```

***

### <a name="pow"></a> Power

![number ^ number](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/pow.png)

Returns the given number to the specified power (e.g., x<sup>y</sup>).

```
Math.pow([NUMBER], [NUMBER])
```

***

### <a name="lnexp"></a> Natural Logarithm / e Raised to a Power

![ln number](http://static.stencyl.com/pedia2/block-images/numbers-text/trig/lnexp.png)

**ln** - Returns the natural logarithm of the given number.<br/>
**e^** - Returns the number e to the given power.

```
Math.log([NUMBER])
Math.exp([NUMBER])
```

***
