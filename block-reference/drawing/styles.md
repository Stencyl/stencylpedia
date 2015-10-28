# Drawing > Styles

***

## Color and Font

### Create Color (from RGB)

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/rgb-to-color.png)

aaa

```
Utils.getColorRGB(Std.int(0), Std.int(0), Std.int(0))
```

***

### Set Color

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-color.png)

aaa

```
g.fillColor = Utils.getColorRGB(255,200,0);
```

***

### Set Font

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-font-new.png)

aaa

```
g.setFont(!ERROR!);
```

***

## Opacity

### Set Opacity

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-alpha.png)

aaa

```
g.alpha = (0/100);
```

***

## Stroke

### Set Stroke Color

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-stroke-color.png)

aaa

```
g.strokeColor = Utils.getColorRGB(255,200,0);
```

***

### Set Stroke Thickness

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/set-thickness.png)

aaa

```
g.strokeSize = Std.int(0);
```

***

## Font Width

### Get Width of Text for Current Font

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-width.png)

aaa

```
g.font.font.getTextWidth("text")/Engine.SCALE
```

***

### Get Width of Text for Specific Font

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-width2-new.png)

aaa

```
!ERROR!.font.getTextWidth("text")/Engine.SCALE
```

***

## Font Height

### Get Height for Current Font

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-height.png)

aaa

```
g.font.getHeight()/Engine.SCALE
```

***

### Get Height for Specific Font

![](http://static.stencyl.com/pedia2/block-images/9%20-%20Drawing/1%20-%20Styles/get-font-height2-new.png)

aaa

```
!ERROR!.getHeight()/Engine.SCALE
```

***
