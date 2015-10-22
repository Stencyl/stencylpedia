## Contents

* Introduction
* Use the Full Screen
* How To: Specifying a Splash Screen
* How To: Adapting to Different Displays


## Introduction

In recent years, Apple has upgraded its phones with larger, widescreen displays, starting with the iPhone 5. Developers are expected to support these screen sizes in accordance with Apple's guidelines.

Before reading this article, read our [App Scaling](http://www.stencyl.com/help/view/mobile-app-scaling/) article. It covers most of the concepts we'll be talking about here.


## How to Use the Full Screen

Apple dictates that you **may not [letterbox](http://static.stencyl.com/v3/images/announcement/stf1.jpg)** your game. In other words, your game has to fill up the screen, one way or another.

Given this restriction, you have a few options for filling out the screen using our **Scale Modes**.

> **Reminder:** You can find the Scale Mode dropdown inside Settings > Mobile > General.<br/><br/>![](http://static.stencyl.com/help/images/iphone5-3.png)

#### Using Scale to Fit (Full Screen) - [Recommended]
This will fill out the game's screen, but more of the game will show than on standard aspect ratio (3:2) screens. You'll need to re-position your interface elements to adjust between different screen sizes.

#### Using Stretch to Fit
This will fill out the game's screen, but the game's image will be distorted on elongated screens.

#### Using Scale to Fit (Fill)
This will fill the game's screen but crop out the left/right edges (Landscape) or top/right edges (Portrait).


## How To: Specifying a Splash Screen

Apple requires separate splash screens for each size of device that they make. Your game will not publish unless all of these splash screens are provided.

You can specify the splash screen right on the same screen as the other splash screens. (under Settings > Mobile > Logos & Splash)

![](http://static.stencyl.com/help/images/iphone5-4.png)


## How To: Adapting to Different Displays

If you want your app to look great all displays, you’ll need to adapt your game to each screen's format, so that the game's interface elements appear in the same place regardless of what device you’re on.

We provide a block (under **Flow > Advanced**) to let you detect this, so you can do something different on these devices to use that extra space.

![](http://static.stencyl.com/help/images/iphone5-5.png)

For example, if you're using **Scale to Fit (Full Screen)** as we recommend above and you want your [HUD](http://www.stencyl.com/help/view/drawing-text-and-huds/) to fit each screen, you could position the HUD elements, so they always adapt to each screen's width.


## Additional Resources

Prefer a video? This [video series](http://www.youtube.com/watch?v=4I_HqB9-bis&list=PLkcZhcNsGmYq8xa9-4XP-gegXP6Om3Ilp) explains this concept really well.
