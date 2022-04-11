# Drawing > Styles

***

## Color and Font

### <a name="rgb-to-color"></a> Create Color (from RGB)

![red green blue as color](https://static.stencyl.com/pedia2/block-images/drawing/styles/rgb-to-color.png)

Creates a **Color** value from red, green, blue channels. Numbers must be between [0-255] inclusive.

```
Utils.getColorRGB([INT], [INT], [INT])
```

***

### <a name="set-color"></a> Set Color

![set fill color to color](https://static.stencyl.com/pedia2/block-images/drawing/styles/set-color.png)

Sets the color used for filling shapes (does not apply to fonts). You can select the color using the color picker, drag in a color attribute or drag in any block that returns a color.

```
g.fillColor = Utils.convertColor([COLOR]);
```

***

### <a name="set-font-new"></a> Set Font

![set current font to font](https://static.stencyl.com/pedia2/block-images/drawing/styles/set-font-new.png)

Sets the font used in drawing text. You can pick the font directly or drag in a font attribute block.

```
g.setFont([FONT]);
```

***

### <a name="letter-spacing"></a> Set Spacing

![set spacing to number for font](https://static.stencyl.com/pedia2/block-images/drawing/styles/letter-spacing.png)

Sets the spacing between characters of the font.

```
[FONT].setLetterSpacing([NUMBER]);
```

***

## Opacity

### <a name="set-alpha"></a> Set Opacity

![set opacity to number %](https://static.stencyl.com/pedia2/block-images/drawing/styles/set-alpha.png)

Sets the opacity (alpha) used in drawing to the specified percentage. Number must be between [0-100] inclusive.

```
g.alpha = ([NUMBER]/100);
```

***

## Stroke

### <a name="set-stroke-color"></a> Set Stroke Color

![set stroke color to color](https://static.stencyl.com/pedia2/block-images/drawing/styles/set-stroke-color.png)

Sets the stroke color used when drawing shapes (does not apply to fonts). You can select the color using the color picker, drag in a color attribute or drag in any block that returns a color.

```
g.strokeColor = [COLOR];
```

***

### <a name="set-thickness"></a> Set Stroke Thickness

![set stroke thickness to int](https://static.stencyl.com/pedia2/block-images/drawing/styles/set-thickness.png)

Sets the stroke thickness (width) used when drawing shapes. Set to 0 to disable.

```
g.strokeSize = [INT];
```

***

## Font Width

### <a name="get-font-width"></a> Get Width of Text for Current Font

![get width for text using current font](https://static.stencyl.com/pedia2/block-images/drawing/styles/get-font-width.png)

Returns the width of the specified text using the current font. Useful for calculating text drawing positions. May only be used in a `when drawing` event.

```
g.font.font.getTextWidth([TEXT], g.font.letterSpacing)/Engine.SCALE
```

***

### <a name="get-font-width2-new"></a> Get Width of Text for Specific Font

![get width for text using font](https://static.stencyl.com/pedia2/block-images/drawing/styles/get-font-width2-new.png)

Returns the width of the specified text using the given font. Useful for calculating text drawing positions.

```
[FONT].font.getTextWidth([TEXT], [FONT].letterSpacing)/Engine.SCALE
```

***

## Font Height

### <a name="get-font-height"></a> Get Height for Current Font

![get height using current font](https://static.stencyl.com/pedia2/block-images/drawing/styles/get-font-height.png)

Returns the height of text using the current font. Useful for calculating text drawing positions. May only be used in a `when drawing` event.

```
g.font.getHeight()/Engine.SCALE
```

***

### <a name="get-font-height2-new"></a> Get Height for Specific Font

![get height using font](https://static.stencyl.com/pedia2/block-images/drawing/styles/get-font-height2-new.png)

Returns the height of text using the given font. Useful for calculating text drawing positions.

```
[FONT].getHeight()/Engine.SCALE
```

***
