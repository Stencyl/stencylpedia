## Contents

* Introduction
* Use the Full Screen
* How To: Specifying a Splash Screen
* How To: Adapting to Different Displays


## Introduction

In recent years, Apple has upgraded its phones with larger, widescreen displays, starting with the iPhone 5. Developers are expected to support these screen sizes in accordance with Apple's guidelines.

Before reading this article, read our [App Scaling](http://www.stencyl.com/help/view/mobile-app-scaling/) article. It covers most of the concepts we'll be talking about here.


## How to Use the Full Screen

At the heart of the problem is this: Games are typically developed using a 3:2 aspect ratio such as 480 x 320 pixels. This matches the resolution of the original iPhone and earlier Android devices. When devices started getting larger screens, many moved over to widescreen displays with aspect ratios of 16:10 and 16:9.

The problem is this. Suppose that you developed a game at 480 x 320 (3:2). On the iPhone 5, your game would look like this because its screen is much wider than 3:2. Those extra pixels on the side would be unused. This effect is called **letterboxing**.

![](http://static.stencyl.com/pedia2/ch11/letterboxed.png)


#### You can't letterbox your game

Apple dictates that you **may not [letterbox](http://static.stencyl.com/v3/images/announcement/stf1.jpg)** your game. Given this restriction, you have a few options for filling out the screen using our [**Scale Modes**](http://www.stencyl.com/help/view/mobile-app-scaling/).

#### Using Scale to Fit (Full Screen) <-- [Recommended]
This will fill out the game's screen, but instead of chopping off the screen at the edges, more of the game will show instead. You'll need to re-position your interface elements to adjust between different screen sizes.

#### Using Stretch to Fit
This will fill out the game's screen, but the game's image will be distorted on elongated screens.

#### Using Scale to Fit (Fill)
This will fill the game's screen but crop out the left/right edges (Landscape) or top/right edges (Portrait). The wider the screen is, the more that will be cropped out.

> **Reminder:** You can find the Scale Mode dropdown inside Settings > Mobile > Display.<br/><br/>![](http://static.stencyl.com/help/images/iphone5-3.png)


## How To: Specifying a Splash Screen

Apple requires separate splash screens for each size of device that they make. Your game will not publish unless all of these splash screens are provided.

You can specify the splash screen right on the same screen as the other splash screens (under Settings > Mobile > Splash Screens).

![](http://static.stencyl.com/help/images/iphone5-4.png)


## How To: Adapting to Different Displays

If you want your app to look great on all displays, you'll need to adapt your game to each screen's format, so that the game's interface elements appear in the same place regardless of what device you're on.

You can tackle this problem in at least two ways.

#### Method 1: Use the Screen Width block

if you're using **Scale to Fit (Full Screen)** as we recommend above and you want your [HUD](http://www.stencyl.com/help/view/drawing-text-and-huds/) elements to fit each screen (Android, iPhone or otherwise), position the HUD elements to adapt to the screen's width.

![](http://static.stencyl.com/pedia2/ch11/adapt-example.png)

In this example, we're re-positioning this element to be 10 pixels from the screen's right edge.


#### Method 2: Handle iPhone 5/6/6+ (and beyond) as a special case

Using a special block (under **Flow > Advanced**), you can detect what model your game is running on, so you can do something different on these devices to use that extra space. This isn't as versatile as Method 1 but is useful if you want to tweak things specifically for these iPhone models.

![](http://static.stencyl.com/help/images/iphone5-5.png)


## Additional Resources

Prefer a video? This [video series](http://www.youtube.com/watch?v=4I_HqB9-bis&list=PLkcZhcNsGmYq8xa9-4XP-gegXP6Om3Ilp) was done for Stencyl 3.0, but it explains this concept really well.
