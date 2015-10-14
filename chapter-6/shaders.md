## Contents

* Introduction
* Basic Usage
* Advanced: Custom Shaders
* Property Reference
* Advanced: Sample Shaders
* Advanced: How to Port Shaders
* Experimental: Shaders on Android
 

## Introduction

Shaders are filters that apply visual effects to the entire screen. They aren't all that different from the filters you apply to an photo in Instagram or Photoshop.

![Shader Demo](http://static.stencyl.com/v3/images/announcement/shader2.gif)


#### What can you do with shaders? 
You can...

* Turn shaders on and off at will.
* Alter a shader's properties at runtime.
* Combine as many shaders together as you want, within reason.
* All of this is hardware accelerated, so within reason, you can accomplish a lot.

#### Supported Platforms
Windows, Max and Linux. Shaders are not supported on Flash or iOS. They work to a limited extent on Android.

#### Tech Details
Shaders are written in GLSL, a programming language that your graphics card understands. Since our engine is based on OpenGL ES 2.0 (in order to support mobile targets), the syntax is more restricted than normal GLSL.
 

## Basic Usage

#### Creating a Shader
Shaders work much like effects. To apply a shader, use the following block and insert any shader into the lone field, like this:

![](http://static.stencyl.com/pedia2/ch6/shader/shader-basic-1.png)

All shader blocks can be found under **Scene > Shaders**.

> **Aside:** What does the toggle shaders for HUD layer block do? <br/><br/>![](http://static.stencyl.com/pedia2/ch6/shader/shader-hud.png)<br/><br/>Since shaders apply to the entire screen, this can sometimes be undesirable if those effects are also applied to a game's HUD (such as the health/score display). This block lets you opt the HUD layer out of shaders.
 
#### Multiple Shaders
By combining multiple shaders into a single, composite shader, you can apply all of these shaders at once. Use the **shader + shader** block to accomplish this.

![](http://static.stencyl.com/pedia2/ch6/shader/shader-basic-3.png)
 
#### Clearing Shaders
To turn off shaders, use the **clear shaders from game** block.

![](http://static.stencyl.com/pedia2/ch6/shader/shader-basic-2.png)

#### Shader Properties
Sometimes, you want to modify a shader's properties in real-time (or before application). For example, if you're using a Contrast shader, you'll want to change the contrast amount. Using our built-in blocks, you can instantly set properties and tween them (change them over time).

**How do you figure out the property names?** Refer to the **Property Reference** section later in this article.

#### Set Property
![](http://static.stencyl.com/pedia2/ch6/shader/shader-set.png)

#### Tween Property
![](http://static.stencyl.com/pedia2/ch6/shader/shader-tween.png)

> **Note:* All property names are case sensitive.
 

## Advanced: Custom Shaders

Stencyl comes with a sizable variety of shaders, but for the adventurous, we allow you to apply your own custom shaders. As mentioned earlier, shaders are written in GLSL and must comply with the OpenFL ES 2.0 standard.

#### Importing a Shader from a File
1. Create an **extras** folder inside your game's main folder. (Debug > View > View Folder for this Game)

2. Stick the shaders (file extension doesn't matter - we use .glsl in this example) under that extras folder.

3. Refer to your shaders using the **shader from file** block. For example, if your shader is called bloom.glsl, then you type bloom.glsl into the block. The engine automatically assumes that the shaders are under the extras folder, so need to mention that.<br/>![](http://static.stencyl.com/pedia2/ch6/shader/shader-file.png)

#### Specifying a Shader Inline (inside a Design Mode block)
Alternatively, for convenience, you can specify a shader's source directly within Design Mode using the shader from text block.

![](http://static.stencyl.com/pedia2/ch6/shader/shader-inline.png)


## Property Reference

Use the following properties to adjust a shader's behavior after creation by either setting the values directly or tweening them, as specified right above.

#### Hue / Saturation / Brightness / Contrast

Property Name | Accepted Values
--- | ---
hue | Between 0 - 360 degrees, inclusive.
saturation | 1.0 means regular saturation. 2.0 means double. 0.5 means half.
contrast | 1.0 means regular contrast. 2.0 means double. 0.5 means half.
brightness | 1.0 means regular brightness. 2.0 means double. 0.5 means half.


#### Tint

Property Name | Accepted Values
--- | ---
amount | 0 means no tint. 1.0 means full tinting.
red | Between 0 - 255, inclusive.
green | Between 0 - 255, inclusive.
blue | Between 0 - 255, inclusive.
 

#### Grayscale/Invert/Sepia

No properties.
 

#### Directional Blur

Property Name | Accepted Values
--- | ---
radius | How much to blur, in pixels. 0 turns off blurring.
dirx | What x-direction to blur in.
diry | What y-direction to blur in. 
 

#### Sharpen

Property Name | Accepted Values
--- | ---
amount | How much to sharpen, in pixels.
 

#### Bloom

Property Name | Accepted Values
--- | ---
currPixelWeight | How much you consider the current pixel when sampling. (Default = 0.25)
neighborPixelWeight | How much you consider neighboring pixels when sampling. (Default = 0.004)
sampleX | How many pixels left/right to sample next to the sample pixel. (Default = 4)
sampleY | How many pixels up/down to sample next to the sample pixel. (Default = 3)
lowThreshold | What brightness (between 0 - 1.0) to consider a pixel as low brightness. (Default = 0.4)
mediumThreshold | What brightness (between 0 - 1.0) to consider a pixel as medium brightness. (Default = 0.6)
lowMultiplier | How much brighter to make a low brightness pixel. (Default = 0.012)
mediumMultiplier | How much brighter to make a medium brightness pixel. (Default = 0.009)
highMultiplier | How much brighter to make a high brightness pixel. (Default = 0.0075)

Bloom is complicated. Here's roughly how it works.

1. First, the algorithm samples the current and neighboring pixels and sums them up into a single color, using the two pixel weight values to let you alter how much sway the current vs. neighboring pixels have. Increasing the sample sizes quickly exaggerates the effect, but it can look blotchy.

2. Based on how bright the original pixel is, the algorithm buckets it into 3 categories (low, medium, high) using the threshold values and lets you apply different multipliers to the final color's brightness to emphasize certain parts of the spectrum versus others.

**How does this work in practice?**

If you want to emphasize just the brighter colors, you'd move the low/medium threshold values higher (towards 1 to stop the effect from affecting darker areas), lower the low/medium multipliers to 0 (which would mean no changes to those pixels at all). That will reduce the effect to just the brights, then you'd alter the remaining values to your taste.

#### Grain

Property Name | Accepted Values
--- | ---
grainamount -| How dense the grain effect is. (Default = 0.05 (5%)).
colored | 1.0 = on, 1.0 = off
coloramount | Saturation of the colors.
grainsize | Size of the grain particles in pixels. Can be fractional.
lumamount | How bright the grain effect is.
 
#### Scanlines

Property Name | Accepted Values
--- | ---
scale | An integer specifying the width of the scanlines. 0 turns off the effect.
 

## Advanced: Sample Shaders

Treat these as working samples to base your own custom shaders off of. These are shaders that didn't make it into the built-in set but may be interesting.

#### Ripple

![](http://static.stencyl.com/v3/images/announcement/ripples.gif)

```
varying vec2 vTexCoord;
uniform sampler2D uImage0;
uniform float uTime;
void main()
{
    float amplitude = 0.03;
    float speed = 0.004;
    float twirliness = 12.0;

    vec2 tc = vTexCoord;
    vec2 p = -1.0 + 2.0 * tc;
    float len = length(p);
    vec2 uv = tc + (p / len) * cos(len * twirliness - uTime * speed) * amplitude;
    vec3 col = texture2D(uImage0, uv).xyz;
    gl_FragColor = vec4(col, 1.0);
}
```
 
#### Wave

![](http://static.stencyl.com/v3/images/announcement/waves.gif)

```
varying vec2 vTexCoord;
uniform sampler2D uImage0;
uniform float uTime;
void main()
{
    float amplitude = 0.02;
    float xTwirl = 5.0;
    float yTwirl = 10.0;
    float speed = 0.0025;

    vec2 texCoord = vTexCoord;
    texCoord.x = texCoord.x + cos(texCoord.y * yTwirl + uTime * speed) * amplitude;
    texCoord.y = texCoord.y + sin(texCoord.x * xTwirl + uTime * speed) * amplitude;
    gl_FragColor = texture2D(uImage0, texCoord);
}
```
 
#### Magnifying Glass

```
varying vec2 vTexCoord;
uniform vec2 uResolution;
uniform sampler2D uImage0;
float circleRadius = float(0.5);
float minZoom = 0.4;
float maxZoom = 0.6;

void main()
{
    vec2 resolution = uResolution;
    vec2 center = vec2(resolution.x / 2.0, resolution.y / 2.0);

   vec2 uv = vTexCoord; 
   uv.x *= (resolution.x / resolution.y);
 
   vec2 realCenter = vec2(0.0, 0.0);
   realCenter.x = (center.x / resolution.x) * (resolution.x / resolution.y);
   realCenter.y = center.y / resolution.y;
 
    float maxX = realCenter.x + circleRadius;
    float minX = realCenter.x - circleRadius;
    float maxY = realCenter.y + circleRadius;
    float minY = realCenter.y - circleRadius;
    if(uv.x > minX && uv.x < maxX && uv.y > minY && uv.y < maxY)
    {
        float relX = uv.x - realCenter.x;
        float relY = uv.y - realCenter.y;
        float ang =  atan(relY, relX);
        float dist = sqrt(relX * relX + relY * relY);
 
        if(dist <= circleRadius)
        {
            float newRad = dist * ((maxZoom * dist / circleRadius) + minZoom);
            float newX = realCenter.x + cos(ang) * newRad;
            newX *= (resolution.y / resolution.x);
            float newY = realCenter.y + sin(ang) * newRad;
            gl_FragColor = texture2D(uImage0, vec2(newX, newY));
        }
 
        else
        {
            gl_FragColor = texture2D(uImage0, vTexCoord);
        }
    }

    else
    {
        gl_FragColor = gl_FragColor = texture2D(uImage0, vTexCoord);
    } 
}
```


## Advanced: Porting Shaders

If you are porting shaders from another environment or from online examples, you may be interested in knowing what the main variables are (the texture, the current coordinate, the current time).

These 3 lines go at the top of every shader. Adjust the names you find accordingly to reference these.

```
varying vec2 vTexCoord;
uniform sampler2D uImage0;
uniform float uTime;
 ```


## Experimental: Shaders on iOS/Android

Shaders work on Android but are more restricted than their desktop counterparts. They do not work on iOS at this time.

#### What's different?

* Most shaders will heavily reduce a game's performance.
* While all built-in shaders work, some 3rd party shaders may require tweaks because mobiles support an even smaller set of instructions.
 
#### Recommended Shaders

* Grayscale, Invert, Sepia, Contrast, Saturation and Brightness incur no penalty (or a negligible one).
* Scanlines incur a small penalty.
* All other shaders incur a heavy penalty. We don't recommend using them inside a mobile game.
 
#### Best Practices

* Use shaders sparingly in mobile games.
* Provide a user option to turn off shaders, BEFORE they get used.
* Thoroughly test your game on devices of all kinds.
 

## Challenge

We'd love to see what you come up with! Build a shader on your own and share it on the forums or in the comments area.
