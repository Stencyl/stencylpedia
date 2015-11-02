# Scene > Shaders

***

> Read our guide on [Shaders](http://www.stencyl.com/help/view/shaders/) for an explanation of these blocks.

***

## Shaders

### <a name="shader-apply"></a> Apply Shader

![shader-apply](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-apply.png)

Applies the specified shader to the game. This replaces the existing shader. To use multiple shaders at a time, use the combine shader blocks below.

```
[SHADER].enable();
```

***

### <a name="shader-clear"></a> Clear Shaders

![shader-clear](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-clear.png)

Removes the existing shader from the game.

```
engine.clearShaders();
```

***

### <a name="shader-hud"></a> Toggle shaders for HUD layer

![shader-hud](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-hud.png)

Enables/disables shaders for the HUD (top, non-scrolling) layer.

```
engine.toggleShadersForHUD();
```

***

### <a name="shader-combine"></a> Combine 2 Shaders

![shader-combine](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-combine.png)

Combines 2 shaders together. If combining more than 2, stick further combines in the second slot.

```
[SHADER].combine([SHADER])
```

***

### <a name="shader-combine3"></a> Combine 3 Shaders

![shader-combine3](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-combine3.png)

Combines 3 shaders together.

```
[SHADER].combine([SHADER]).combine([SHADER])
```

***

### <a name="shader-combine4"></a> Combine 4 Shaders

![shader-combine4](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-combine4.png)

Combines 4 shaders together.

```
[SHADER].combine([SHADER]).combine([SHADER]).combine([SHADER])
```

***

### <a name="shader-file"></a> Load Shader from File

![shader-file](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-file.png)

Loads a shader placed into a game's **extras** directory.

```
new ExternalShader([TEXT])
```

***

### <a name="shader-text"></a> Load Shader from Text

![shader-text](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-text.png)

Define a shader inline using [GLSL](https://en.wikipedia.org/wiki/OpenGL_Shading_Language).

```
new InlineShader([TEXT])
```

***

## Properties

### <a name="shader-set"></a> Set Shader Property

![shader-set](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-set.png)

Instantly set a shader's properties. This lets you tweak a shader (in ways that the blocks don't allow) and alter its appearance after creation.

Consult our [Shaders article](http://www.stencyl.com/help/view/shaders/) for property names.

```
[SHADER].setProperty([TEXT], [VALUE]);
```

***

### <a name="shader-tween"></a> Tween a Shader Property

![shader-tween](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-tween.png)

Change a shader's properties over time. Consult our [Shaders article](http://www.stencyl.com/help/view/shaders/) for property names.

```
[SHADER].tweenProperty([TEXT], [NUMBER], [NUMBER], [EASING]);
```

***

### <a name="shader-time"></a> Set Time Scale for Shader

![shader-time](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-time.png)

Makes animated shaders run faster/slower. Useful for porting shaders written for other environments. 1.0 is normal time. 2.0 is twice as fast.

```
[SHADER].setTimeScale([NUMBER]);
```

***

## Color Shaders

### <a name="shader-hue"></a> Hue

![shader-hue](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-hue.png)

Adjusts the screen's hue in degrees.

```
new HueShader(0)
```

***

### <a name="shader-csb"></a> Contrast / Saturation / Brightness

![shader-csb](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-csb.png)

Adjust the screen's contrast, saturation or brightness, in percentages. 100% means original value, 200% means twice as much, 50% means half as much.

```
CSBShader.create("contrast", [NUMBER]/100)
CSBShader.create("saturation", [NUMBER]/100)
CSBShader.create("brightness", [NUMBER]/100)
```

***

### <a name="shader-tint"></a> Tint

![shader-tint](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-tint.png)

Apply a color-based tint to the screen using the specified opacity in pecentage between 0% (no tint), 100% (full tint).

```
new TintShader([COLOR], [NUMBER]/100)
```

***

## Filter Shaders

### <a name="shader-filters"></a> Filters (Grayscale / Inverse / Sepia)

![shader-filters](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-filters.png)

Apply simple filters (grayscale, inverse, sepia) to the screen.

```
new GrayscaleShader()
new InverseShader()
new SepiaShader()
```

***

### <a name="shader-blur"></a> Blur

![shader-blur](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-blur.png)

Applies a directional blur to the screen. x/y collectively define a 'slope' for the direction, so -1,-1 is a diagonal blur.

```
new BlurShader([NUMBER], [NUMBER], [NUMBER])
```

***

### <a name="shader-sharpen"></a> Sharpen

![shader-sharpen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-sharpen.png)

Sharpen with the given intensity.

```
new SharpenShader([NUMBER])
```

***

### <a name="shader-bloom"></a> Bloom

![shader-bloom](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-bloom.png)

Causes highlights (bright areas) to bleed and glow.

```
new BloomShader()
```

***

## Effect Shaders

### <a name="shader-grain"></a> Grain

![shader-grain](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-grain.png)

Apply a dynamic, film grain effect to the screen.

```
new GrainShader()
```

***

### <a name="shader-scanline"></a> Scanlines

![shader-scanline](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-scanline.png)

Apply TV-like scanlines to the screen.

```
new ScanlineShader(0)
```

***

