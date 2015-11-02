# Drawing > Styles

***

## Color and Font

### <a name="rgb-to-color"></a> Create Color (from RGB)

![rgb-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/rgb-to-color.png)

Creates a **Color** value from red, green, blue channels. Numbers must be between [0-255] inclusive.

```
Utils.getColorRGB([NUMBER], [NUMBER], [NUMBER])
```

***

### <a name="set-color"></a> Set Color

![set-color-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-color.png)

Sets the color used for filling shapes (does not apply to fonts). You can select the color using the color picker, drag in a color attribute or drag in any block that returns a color.

```
g.fillColor = [COLOR];
```

***

### <a name="set-font-new"></a> Set Font

![set-font-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-font-new.png)

Sets the font used in drawing text. You can pick the font directly or drag in a font attribute block.

```
g.setFont([FONT]);
```

***

## Opacity

### <a name="set-alpha"></a> Set Opacity

![set-opacity-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-alpha.png)

Sets the opacity (alpha) used in drawing to the specified percentage. Number must be between [0-100] inclusive.

```
g.alpha = ([NUMBER]/100);
```

***

## Stroke

### <a name="set-stroke-color"></a> Set Stroke Color

![set-stroke-color-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-stroke-color.png)

Sets the stroke color used when drawing shapes (does not apply to fonts). You can select the color using the color picker, drag in a color attribute or drag in any block that returns a color.

```
g.strokeColor = [COLOR];
```

***

### <a name="set-thickness"></a> Set Stroke Thickness

![set-stroke-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-thickness.png)

Sets the stroke thickness (width) used when drawing shapes. Set to 0 to disable.

```
g.strokeSize = [NUMBER];
```

***

## Font Width

### <a name="get-font-width"></a> Get Width of Text for Current Font

![get-font-width-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-width.png)

Returns the width of the specified text using the current font. Useful for calculating text drawing positions. May only be used in a `when drawing` event.

```
g.font.font.getTextWidth([TEXT])
```

***

### <a name="get-font-width2-new"></a> Get Width of Text for Specific Font

![get-font-width-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-width2-new.png)

Returns the width of the specified text using the given font. Useful for calculating text drawing positions.

```
[FONT].font.getTextWidth([TEXT])
```

***

## Font Height

### <a name="get-font-height"></a> Get Height for Current Font

![get-font-height-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-height.png)

Returns the height of text using the current font. Useful for calculating text drawing positions. May only be used in a `when drawing` event.

```
g.font.getHeight()
```

***

### <a name="get-font-height2-new"></a> Get Height for Specific Font

![get-font-height-block](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-height2-new.png)

Returns the height of text using the given font. Useful for calculating text drawing positions.

```
[FONT].getHeight()
```

***
