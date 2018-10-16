## Contents

* Introduction
* How To: Switch to Full Screen Mode
* How it Works
* What if I don't want to use the high-res graphics?
 

## Introduction

As the name implies, Full Screen Mode fills the entire screen (or most of it) with your app, providing a more immersive experience.

Stencyl supports full screen mode for Flash and Desktop (Windows, Mac, Linux) games. 

> **Note**: For mobile games, the Full Screen scaling mode is discussed in our [App Scaling article](http://www.stencyl.com/help/view/mobile-app-scaling/).

 
## How To: Switch to Full Screen Mode

Use the block under **Scene > View** to switch between windowed and full screen mode.

![Toggle full screen mode block](http://static.stencyl.com/help/images/full-screen-mode-1.png)

> **Note**: Alternatively, you can instruct a game to begin in full screen mode through **Settings > Web > Start in Full Screen?** and **Settings > Desktop > Start in Full Screen?** respectively.

 
## How it Works

By default, full screen mode will use the game's hi-res graphics to draw to the screen, up to a maximum of 4x. It will pick the closest match (rounded down) and letterbox the result, identical to the **No Scaling (Letterboxing)** mode for mobile apps.

**These are the same graphics used for the mobile variants of the game**, as described in our [App Scaling](http://www.stencyl.com/help/view/mobile-app-scaling/) article.

![high-res graphics](http://static.stencyl.com/help/images/full-screen-mode-2.png)

For example, if your game's base resolution is 480 x 320, and your screen's resolution is 1024 x 768, the game will scale to 2x (960 x 640).

 
## What if I don't want to use the high-res graphics?

If you are OK with scaling up your game directly from its 1x (standard resolution) graphics versus the hi-res graphics, configure the following settings under **Settings > Web** and/or **Settings > Desktop**.

Setting | Value
--- | ---
Scale | 1x
Scale Mode | Scale to Fit (Letterbox)
Scales | Only check off 1x
Start the game in full-screen | Yes

> Why would a game want this? This is particularly useful for retro-like games and has the main benefit of reducing the file/download size of the game.
