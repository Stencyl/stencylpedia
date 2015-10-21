## Contents

* What are Backgrounds?
* How do Backgrounds scroll? (Parallax Scrolling)
* How To: Importing Backgrounds
* Animated Backgrounds
* Auto-Scrolling
* Repeating Backgrounds
* Backgrounds in the Scene Designer
 

## What are Backgrounds?

Backgrounds are **large images** that scroll alongside a scene, usually behind or in front of a scene.

Backgrounds can visually enhance a game and provide the illusion of depth. Some games even draw backgrounds in front of a screen for visual flair (like in the video above) or to obscure part of the screen.

<object height="315" width="420"><param name="movie" value="http://www.youtube.com/v/c7hrV_WUmj4?version=3&amp;hl=en_US"><param name="allowFullScreen" value="true"><param name="allowscriptaccess" value="always"><embed allowfullscreen="true" allowscriptaccess="always" height="315" src="http://www.youtube.com/v/c7hrV_WUmj4?version=3&amp;hl=en_US" type="application/x-shockwave-flash" width="420"></object>


## How do Backgrounds scroll? (Parallax Scrolling)

Put simply, backgrounds scroll at the same pace that you progress overall inside a scene, where "progress" is defined by the location of the Camera. This is commonly known as **Parallax Scrolling**.

If you’re halfway through a scene, the background will be scrolled halfway through.

![background-scrolling-example](http://static.stencyl.com/pedia2/ch4/backgrounds/image05.png)

Likewise, if you're at the end of the scene, the background will be scrolled through to the end.

![background-scrolling-scene-example](http://static.stencyl.com/pedia2/ch4/backgrounds/image06.png)

To think about this another way, since backgrounds are almost always larger than the screen size, they’ll **scroll at a slower-pace than the main layers**, making them feel like they’re **in the distance**.

In this video, notice how things in the "foreground" scroll by quickly while things in the "background" (hills)  scroll by slowly.

<object height="315" width="560"><param name="movie" value="http://www.youtube.com/v/kGndaktrLcw?version=3&amp;hl=en_US"><param name="allowFullScreen" value="true"><param name="allowscriptaccess" value="always"><embed allowfullscreen="true" allowscriptaccess="always" height="315" src="http://www.youtube.com/v/kGndaktrLcw?version=3&amp;hl=en_US" type="application/x-shockwave-flash" width="560"></object>

Intuitively, this makes sense. If you look outside your car's window, the **close-by buildings you drive by will fly by quickly**. But the mountains in the distance **will move relatively slowly** because they are far away.

> **Bottom Line:** You don't need to do anything special to make Parallax Scrolling work in Stencyl, but it helps to understand how this kind of scrolling works.
 

## How To: Importing Backgrounds

Importing backgrounds works much like importing any other kind of graphic into Stencyl.

1. Create a new Background (under File > Create New > Background). Give it a name.<br/><br/>![stencyl-create-background](http://static.stencyl.com/pedia2/ch4/backgrounds/image04.png)<br/>

2. Inside the Background Editor, click the dotted box to choose an image or drag and drop the image in.<br/><br/>![stencyl-create-background-frame](http://static.stencyl.com/pedia2/ch4/backgrounds/image02.png)<br/>

3. Once you've done that, click the Attach to Scene button at top-right corner to attach this background to a Scene.<br/><br/>![stencyl-add-background-to-scene](http://static.stencyl.com/pedia2/ch4/backgrounds/attach-scene.png)<br/>
 
#### Gotcha: Avoid making a background that’s smaller than the screen size

This will lead to unfilled space at the lower-right hand corner of the screen. The one exception is if you’re creating a repeating background, in which case, the image will tile-itself until it fills out the screen.


## Animated Backgrounds

You may notice that you can **import multiple frames** into a background and edit each frame's individual duration, much like [animations](http://www.stencyl.com/help/view/animations/) for an actor. Doing this will cause the background to animate.

> **Tip:** Avoid creating animated backgrounds for mobile games, as it can quickly exhaust the limited atlas space you already have.
 

## Auto-Scrolling

Some games call for a background that automatically scrolls, regardless of the player’s progression through a scene. Auto-scrolling can impart the sense of **constant motion**.

This Stencyl game [demonstrates](http://www.stencyl.com/game/play/2014) auto-scrolling at its best.

> **Note:** Don’t confuse auto-scrolling backgrounds with the notion of an auto-scrolling level in Super Mario Bros, the kind where you’re forced to stay on screen and complete the level at the set pace. We cover this topic inside our [Camera](http://www.stencyl.com/help/viewArticle/114/) article.


#### How To: Enable Auto-Scrolling

Setting a background to auto-scroll is simple. Just edit the Horizontal / Vertical Scroll Speed values at the top-right corner of the editor.

![stencyl-background-scroll-speed](http://static.stencyl.com/pedia2/ch4/backgrounds/image01.png)

The values don’t hold much meaning in themselves (pixels per sub-frame). **Just experiment until you get a value that works for your game**.


## Repeating Backgrounds

What if your background is meant to be a repeating pattern like the following?

![stencyl-repeating-background](http://static.stencyl.com/pedia2/ch4/backgrounds/image09.png)

Mark the Repeat Background checkbox if this is the case. (it's at the top-right corner)

![stencyl-repeat-background-checkbox](http://static.stencyl.com/pedia2/ch4/backgrounds/image07.png)

Repeating Backgrounds can auto-scroll, but they **do not parallax scroll**. In other words, they scroll directly alongside the main layers.

 
## Backgrounds and the Scene Designer

Backgrounds are considered by Stencyl to be layers, to they are managed through a Scene's Layers pane. This contrasts with our prior approach, which managed backgrounds separately and only allowed them to exist above or below regular layers.

#### Adding a Background

To add a background, click on the + icon at the bottom of the Layers Pane and pick New Background Layer.

![](http://static.stencyl.com/pedia2/ch4/backgrounds/layers-pane.png)

#### Adding a "Foreground"

Place a "foreground" by placing a Background layer above every other layer. Note that the HUD (Heads Up Display) layer which was described in our [Text Drawing article](http://www.stencyl.com/help/view/drawing-text-and-huds/) still exists above the highest layer.

#### Customizing Properties

After adding a background, you can customize a few properties by clicking the cog icon at the right of each entry in the Layers Pane. These properties include:

* Name
* Opacity
* Blend Mode
* Parallax Scroll Factors (described below)

![background-customization](http://static.stencyl.com/pedia2/ch4/backgrounds/background-props.png)

#### Scroll Factors (for Backgrounds and Layers)

As described earlier, backgrounds scroll in parallax. This means that they scroll at the same pace that you progress overall inside a scene. For example, if you’re halfway through a scene, the background will be scrolled halfway through.

![halfway-through](http://static.stencyl.com/pedia2/ch4/backgrounds/image05.png)

For some games, this standard behavior isn't ideal. For enhanced visual effect, some developers want the scrolling to happen faster or slower than normal, or in some cases, for the layer not to scroll at all.

To do this, you must customize the Scroll Factor for a layer.

![customizing-scroll-factor](http://static.stencyl.com/pedia2/ch4/backgrounds/background-props.png)

By default the Scroll Factor is 1. 

* Switching it to 2 will double the amount of scroll that is done.
* Switching it to 0.5 will halve it. 
* Switching it to 0 will stop scrolling entirely for that layer.

**Tip:** Not only can you apply a custom Scroll Factor to backgrounds, but you can also **apply a custom Scroll Factor to regular layers**!


## Summary

* Backgrounds are large images that scroll behind or in front of the screen.
* Backgrounds are like mountains in real life - they scroll by slower than what’s happening right in front of you.
* Use auto-scrolling to make a game feel like it’s in constant motion.
 

## Challenge: Endless Game

Endless games such as Canabalt and Jetpack Joyride are popular examples of this genre. Even Stencyl has its own variation on this theme in the form of Super Belly Boarder, a winter-themed take on an endless game.

![stencyl-background-challenge-game-pic](http://static.stencyl.com/pedia2/ch4/backgrounds/image00.jpg)

Create a simple endless game of your own, using an auto-scrolling background to impart the illusion of constant motion.

Think carefully about how you’d make the game truly endless and random in nature. In other words, **don’t make an enormous level**. That’s the wrong way to do it.
