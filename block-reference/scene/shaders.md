# Scenes > Shaders

***

> Read our guide on [Shaders](http://www.stencyl.com/help/view/shaders/) for an explanation of these blocks.

***

## Shaders

### <a name="shader-apply"></a> Apply Shader

![apply shader to game](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-apply.png)

Applies the specified shader to the game. This replaces the existing shader. To use multiple shaders at a time, use the combine shader blocks below.

```
[SHADER].enable();
```

***

### <a name="shader-clear"></a> Clear Shaders

![clear shaders from game](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-clear.png)

Removes the existing shader from the game.

```
engine.clearShaders();
```

***

### <a name="shader-hud"></a> Toggle shaders for HUD layer

![toggle shaders for hud layer](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-hud.png)

Enables/disables shaders for the HUD (top, non-scrolling) layer.

```
engine.toggleShadersForHUD();
```

***

### <a name="shader-combine"></a> Combine 2 Shaders

![shader + shader](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-combine.png)

Combines 2 shaders together. If combining more than 2, stick further combines in the second slot.

```
[SHADER].combine([SHADER])
```

***

### <a name="shader-combine3"></a> Combine 3 Shaders

![shader + shader + shader](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-combine3.png)

Combines 3 shaders together.

```
[SHADER].combine([SHADER]).combine([SHADER])
```

***

### <a name="shader-combine4"></a> Combine 4 Shaders

![shader + shader + shader + shader](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-combine4.png)

Combines 4 shaders together.

```
[SHADER].combine([SHADER]).combine([SHADER]).combine([SHADER])
```

***

### <a name="shader-file"></a> Load Shader from File

![shader from file text](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-file.png)

Loads a shader placed into a game's **extras** directory.

```
new ExternalShader([TEXT])
```

***

### <a name="shader-text"></a> Load Shader from Text

![shader from code text](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-text.png)

Define a shader inline using [GLSL](https://en.wikipedia.org/wiki/OpenGL_Shading_Language).

```
new InlineShader([TEXT])
```

***

## Properties

### <a name="shader-set"></a> Set Shader Property

![set text for shader to object](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-set.png)

Instantly set a shader's properties. This lets you tweak a shader (in ways that the blocks don't allow) and alter its appearance after creation.

Consult our [Shaders article](http://www.stencyl.com/help/view/shaders/) for property names.

```
[SHADER].setProperty([TEXT], [VALUE]);
```

***

### <a name="shader-tween"></a> Tween a Shader Property

![change text for shader to number over number sec using dropdown](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-tween.png)

Change a shader's properties over time. Consult our [Shaders article](http://www.stencyl.com/help/view/shaders/) for property names.

```
[SHADER].tweenProperty([TEXT], [NUMBER], [NUMBER], [EASING]);
```

***

### <a name="shader-time"></a> Set Time Scale for Shader

![set time scale to number for shader](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-time.png)

Makes animated shaders run faster/slower. Useful for porting shaders written for other environments. 1.0 is normal time. 2.0 is twice as fast.

```
[SHADER].setTimeScale([NUMBER]);
```

***

## Color Shaders

### <a name="shader-hue"></a> Hue

![adjust hue by number degrees](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-hue.png)

Adjusts the screen's hue in degrees.

```
new HueShader([NUMBER])
```

***

### <a name="shader-csb"></a> Contrast / Saturation / Brightness

![set contrast to number %](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-csb.png)

Adjust the screen's contrast, saturation or brightness, in percentages. 100% means original value, 200% means twice as much, 50% means half as much.

```
CSBShader.create("contrast", [NUMBER]/100)
CSBShader.create("saturation", [NUMBER]/100)
CSBShader.create("brightness", [NUMBER]/100)
```

***

### <a name="shader-tint"></a> Tint

![tint using color at number %](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-tint.png)

Apply a color-based tint to the screen using the specified opacity in pecentage between 0% (no tint), 100% (full tint).

```
new TintShader([COLOR], [NUMBER]/100)
```

***

## Filter Shaders

### <a name="shader-filters"></a> Filters (Grayscale / Inverse / Sepia)

![grayscale filter](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-filters.png)

Apply simple filters (grayscale, inverse, sepia) to the screen.

```
new GrayscaleShader()
new InvertShader()
new SepiaShader()
```

***

### <a name="shader-blur"></a> Blur

![blur by x number y number , number pixels](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-blur.png)

Applies a directional blur to the screen. x/y collectively define a 'slope' for the direction, so -1,-1 is a diagonal blur.

```
new BlurShader([NUMBER], [NUMBER], [NUMBER])
```

***

### <a name="shader-sharpen"></a> Sharpen

![sharpen by number](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-sharpen.png)

Sharpen with the given intensity.

```
new SharpenShader([NUMBER])
```

***

### <a name="shader-bloom"></a> Bloom

![bloom filter](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-bloom.png)

Causes highlights (bright areas) to bleed and glow.

```
new BloomShader()
```

***

## Effect Shaders

### <a name="shader-grain"></a> Grain

![add grain](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-grain.png)

Apply a dynamic, film grain effect to the screen.

```
new GrainShader()
```

***

### <a name="shader-scanline"></a> Scanlines

![add scanlines with width number px](http://static.stencyl.com/pedia2/block-images/scene/shaders/shader-scanline.png)

Apply TV-like scanlines to the screen.

```
new ScanlineShader([NUMBER])
```

***
