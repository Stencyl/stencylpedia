## Contents

* Introduction
* The Approach
* Two Key Principles
* Scale Modes
* Scaling on iOS
* Scaling on Android
* FAQ
 

## Introduction

Every year, many new mobile devices get introduced with flagship devices from Apple, Google and Samsung getting refreshed annually. With each new generation comes different screen sizes to support. How do you make your app look good on each device in a consistent and satisfactory way?


## The Approach

To make a game fit each device's screen, we need to do two things:

1. **Resize the game** to fill/fit each device's screen. This is what our **Scale Modes** do.

2. **Use higher resolution graphics on higher resolution screens**. The original iPhone sported a 480 x 320 resolution. Today's flagships are up to 1920 x 1080 or even higher. Higher-resolution graphics are necessary to keep a game looking crisp.

 
## Two Key Principles

#### Design the game at 1x (Standard) resolution.
Regardless of what the game is targeted towards, you'll be designing your game at a standard (1x) resolution. **This means that, if your game was designed to be a 480 x 320 game (to fit the original iPhone), the game size is 480 x 320.** The scaling happens automatically at runtime depending on the device used to play the game, so for example, it would run at 1x scale on the original iPhone, at 2x scale on an iPhone 4 and at 4x scale on an iPad Air.

![](https://static.stencyl.com/help/images/app-scaling-2.png)

#### Draw and import your graphics at 4x resolution.
In contrast, you'll want to draw your graphics as large as you can. If your base resolution is 480 x 320, then quadruple that is 1920 x 1280, which will accomodate recent iPads and Android flagships.

> **Note**: When you import your graphics (at 4x - the default), Stencyl will automatically generate a set of 1x, 1.5, 2x, 3x graphics to use on lower-resolution devices.

 

## Scale Modes - What to do with the extra space?

In a perfect world, every device would be an exact multiple of the base resolution (480 x 320). Unfortunately, this isn't the case because each device's aspect ratio is different. This means that after using high-res graphics to scale a game up to 2x or 4x, some extra space can remain.

Under Settings > Mobile > Display is a **Scale Mode dropdown** for both iOS and Android. This dropdown controls how the extra space is handled.

#### Demo
<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0" data="https://static.stencyl.com/pedia2/ch9/scaling-modes.swf" height="320" width="640"><param name="quality" value="high"><param name="movie" value="https://static.stencyl.com/pedia2/ch9/scaling-modes.swf"><embed height="320" pluginspage="http://www.macromedia.com/go/getflashplayer" quality="high" src="https://static.stencyl.com/pedia2/ch9/scaling-modes.swf" type="application/x-shockwave-flash" width="640"></object>

#### No Scaling (Letterboxing)
After selecting the multiple to draw at, this mode will not perform any resizing. The unused space is left blank.

#### Full Screen
After selecting the multiple to draw at, this mode will display the game "as is" without any further scaling. Anchors to the top-left. This will cause **more of the game to be shown on certain device and less on others**.

#### Stretch to Fit
Stretches the game to fill the entire screen. If the aspect ratio of the screen and game differ, this will slightly distort the image.

#### Scale to Fit (Letterbox)
Stretches the game until the larger game dimension fits the screen, while preserving the game's aspect ratio. Because of this, a **small portion of the screen will remain blank**.

#### Scale to Fit (Fill)
Stretches the game until the smaller game dimension fits the screen, while preserving the game's aspect ratio. Because of this, a **small portion of the game will be chopped off**.

#### Scale to Fit (Full Screen) <-- RECOMMENDED FOR MOST GAMES
Acts just like Letterbox, except that the extra portions of the screen are displayed. This will cause more of the game to be shown on certain device and less on others. **(Added in Stencyl 3.1. Isn't part of the demo above.)**

![](https://static.stencyl.com/v3/images/announcement/stf1.jpg) ![](https://static.stencyl.com/v3/images/announcement/stf2.jpg)

 
## Scaling on iOS

The following table lists what scales each iOS device will run at.

#### iPhone
Device | Screen Resolution | Scale
--- | --- | ---
iPhone Original/3G/3GS | 480 x 320 | 1x
iPhone 4/4S | 960 x 640 | 2x
iPhone 5/5S/5C/SE | 1136 x 640 | 2x
iPhone 6/6S/7/8 | 1334 x 750 | 2x
iPhone 6+/6S+/7+/8+ | 2208 x 1242 | 3x
iPhone X/Xs | 2436 x 1125 | 3x
iPhone XR | 1792 x 828 | 2x
iPhone Xs Max | 2688 x 1242 | 3x

#### iPod 
Device | Screen Resolution | Scale
--- | --- | ---
iPod Touch 2/3 | 480 x 320 | 1x
iPod Touch 4 | 960 x 640 | 2x
iPod Touch 5/6 | 1136 x 640 | 2x

#### iPad
Device | Screen Resolution | Scale
--- | --- | ---
iPad 1/2/Mini | 1024 x 768 | 2x
iPad Pro 10.5" | 2224 x 1668 | 4x
iPad Pro 12.9" | 2732 x 2048 | 4x
Other iPads | 2048 x 1536 | 4x
 

## Scaling on Android

The following table lists what scales common Android devices will run at. Instead of covering everything, we've picked out devices that are representative of that class and tried to hit all the major screen resolutions.

Device | Screen Resolution | Scale
--- | --- | ---
First-Gen Devices | 480 x 320 | 1x
Nexus S | 800 x 480 | 1.5x
Moto E | 960 x 540 | 1.5x
Nexus 7 (2012) | 1280 x 800 | 2x
Moto G | 1280 x 720 | 2x
Moto X (2014) | 1920 x 1080 | 3x
Nexus 6 | 2560 x 1440 | 4x


## FAQ

#### Do I absolutely have to design my graphics at 4x?
You can import at a lower scale such as 1x or 2x (you can tell Stencyl what scale you are importing at, at the time that you import), and Stencyl will generate the hi-res variants. This is useful for retro games.

#### What does the Phone-Only mode do?
It forces the game to max out at 2x resolution, even on tablets and smartphones where a higher resolution could be used. With most device resolutions trending well past the 2x point now, we think this isn't all that useful and may remove it in the future.

#### What does Tablet-Only mode do?
Tablet-only mode is useful for tablet-only games. You still must import your graphics at 4x, but we'll omit the inapplicable (1x) sets from the app at publication time to save you a little bit of space.
