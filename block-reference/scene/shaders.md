# Scene > Shaders

***

> Read our guide on [shaders](http://www.stencyl.com/help/view/shaders/) for an explanation of these blocks.

***

## Shaders

### Apply Shader

![shader-apply](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-apply.png)

Enables shader. Existing shaders will be disabled.

```
shader.enable();
```

***

### Clear Shaders

![shader-clear](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-clear.png)

Removes existing shaders from the game.

```
engine.clearShaders();
```

***

### Toggle shaders for HUD layer

![shader-hud](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-hud.png)

Enables/disables shaders for the HUD (top, non-scrolling) layer.

```
engine.toggleShadersForHUD();
```

***

### Combine 2 Shaders

![shader-combine](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-combine.png)

Combines 2 shaders together. If combining more than 2, stick further combines always in the second slot.

```
shader.combine(shader)
```

***

### Combine 3 Shaders

![shader-combine3](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-combine3.png)

Combines 3 shaders together.

```
shader.combine(shader).combine(shader)
```

***

### Combine 4 Shaders

![shader-combine4](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-combine4.png)

Combines 4 shaders together.

```
shader.combine(shader).combine(shader).combine(shader)
```

***

### Load Shader from File

![shader-file](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-file.png)

Load a shader placed into a game's 'extras' directory.

```
new ExternalShader("text")
```

***

### Load Shader from Text

![shader-text](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-text.png)

Define a shader inline using GLSL.

```
new InlineShader("")
```

***

## Properties

### Set Shader Property

![shader-set](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-set.png)

Instantly set a shader's properties. Consult Stencylpedia for property names.

```
shader.setProperty("text", 0);
```

***

### Tween a Shader Property

![shader-tween](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-tween.png)

Change a shader's properties over time. Consult Stencylpedia for property names.

```
shader.tweenProperty("text", 0, 0, Linear.easeNone);
```

***

### Set Time Scale for Shader

![shader-time](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-time.png)

Makes animated shaders run faster/slower. Useful for porting. 1.0 is normal time. 2.0 is twice as fast.

```
shader.setTimeScale(0);
```

***

## Color Shaders

### Hue

![shader-hue](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-hue.png)

Adjusts the screen's hue in degrees.

```
new HueShader(0)
```

***

### [Contrast / Saturation / Brightness]

![shader-csb](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-csb.png)

Adjust the screen's contrast, saturation and brightness, in percentages.

```
CSBShader.create("contrast", 0/100)
```

***

### Tint

![shader-tint](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-tint.png)

Apply a color to the screen.

```
new TintShader(Utils.getColorRGB(255,200,0), 0/100)
```

***

## Filter Shaders

### Filters (Grayscale / Inverse / Sepia)

![shader-filters](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-filters.png)

Apply simple filters (grayscale, inverse, sepia) to the screen.

```
new GrayscaleShader()
```

***

### Blur

![shader-blur](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-blur.png)

Directional blur. x/y define a 'slope', so -1,-1 is a diagonal blur.

```
new BlurShader(0, 0, 0)
```

***

### Sharpen

![shader-sharpen](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-sharpen.png)

Sharpen with the given intensity.

```
new SharpenShader(0)
```

***

### Bloom

![shader-bloom](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-bloom.png)

Causes highlights (bright areas) to bleed and blow.

```
new BloomShader()
```

***

## Effect Shaders

### Grain

![shader-grain](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-grain.png)

Apply a dynamic, film grain effect to the screen.

```
new GrainShader()
```

***

### Scanlines

![shader-scanline](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/4%20-%20Shaders/shader-scanline.png)

Apply TV-like scanlines to the screen.

```
new ScanlineShader(0)
```

***

