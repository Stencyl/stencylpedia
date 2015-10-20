## Contents

* Introduction
* Scrolling
* Example: Making the Camera Follow the Player
* Moving the Camera
* Off Screen Actors Become Inactive


## Introduction

In this article, we introduce the concept of the camera and describe how you can make games scroll using the camera.


## Scrolling

Although some games exist entirely on a single screen, many extend beyond that. For example, think about a game similar to Super Mario Bros. Levels **extend beyond a single screen**.

![](http://static.stencyl.com/pedia2/ch4/camera/image07.png)

In games like these, when the player walks to the right, the game “scrolls” to the right.

![](http://static.stencyl.com/pedia2/ch4/camera/image00.png)

How does this “scrolling” work? In simple terms, scrolling is the act of **changing** what part of the scene is **visible**.

![](http://static.stencyl.com/pedia2/ch4/camera/image04.png)

One can draw a connection to something we’re familiar with - peering through the viewfinder (or screen) of a camera to compose a photograph.

The “camera” in our engine is the exact same concept - it’s the “thing” that controls what part of the scene is visible.

> **Note:** In fact, the “camera” is an actor! It’s an invisible, non-physical actor, but like any kind of actor, it has a position and it can be moved around.
 

## Example: Making the Camera Follow the Player

In many games, the camera follows the player, so that the player is always on screen.

<embed allowscriptaccess="never" height="315" loop="true" play="true" quality="high" src="http://www.youtube.com/v/ZX-mEw6YmDM?version=3&amp;hl=en_US" type="application/x-shockwave-flash" width="420">

This turns out to be trivial to accomplish since we have a “camera follow player” block as well as a pre-defined Behavior that you can attach to any scene that does the same thing.

![](http://static.stencyl.com/pedia2/ch4/camera/image05.png)


## Moving the Camera

The camera can be moved in 2 different ways, both which involve these blocks (under Scene > View > Camera).

![Camera Blocks](http://static.stencyl.com/pedia2/ch4/camera/image02.png)

#### Method 1: Set the Position

Move the camera to a specific (x,y) position inside the scene.

#### Method 2: Move to Actor

This will set the camera’s position to the center point of the Actor.


> **Note:** One question you may have is: what if I make the camera go outside the scene’s boundaries? It turns out that the camera is locked to those boundaries and won’t head beyond them.

 
## Off Screen Actors Become Inactive

Something you may notice is that actors that are off screen **stop working**, as if they **froze** in time. We do this to preserve performance.

Nevertheless, there are cases where you want an actor to be active regardless of whether it’s on or off screen.

To make an actor always active, use the following block (under Actor > Properties > Misc).

![](http://static.stencyl.com/pedia2/ch4/camera/image01.png)


## Summary

* Scrolling is controlled by the camera.
* The camera is a special kind of actor. It has a position and can be moved around.
* Off screen actors become inactive. Use the “always simulate” block to override this.


## Challenge 1: Auto-Scrolling

In some platformers, levels can auto-scroll. The player has no control over the camera.

<object height="315" width="420"><param name="movie" value="http://www.youtube.com/v/UQIq6DkEK7E?version=3&amp;hl=en_US"><param name="allowFullScreen" value="true"><param name="allowscriptaccess" value="always"><embed allowfullscreen="true" allowscriptaccess="always" height="315" src="http://www.youtube.com/v/UQIq6DkEK7E?version=3&amp;hl=en_US" type="application/x-shockwave-flash" width="420"></object>

How do we accomplish this effect given that you only have control over setting the camera’s position?

One approach is to make a **dummy actor** that controls the camera (by having the camera continually follow this actor).

![](http://static.stencyl.com/pedia2/ch4/camera/image03.png)

By controlling this dummy actor, you gain complete control over the camera and can do more with it, such as **panning** it towards a destination over a time period.

![](http://static.stencyl.com/pedia2/ch4/camera/image06.png)

Your challenge is this: **Create a game that implements auto-scrolling**.

Once you’ve got a simple auto-scrolling behavior completed, extend it so that once it reaches its first destination, begin auto-scrolling to the next one. Generalize this to work with an arbitrary number of destination points.

After that, **figure out a way to prevent the player from exiting from the left/right sides of the screen**. If you play any Mario game, you’ll notice that there’s an invisible **wall** that pushes you along should you try to exit the sides of the screen.


## Challenge 2: Grid-Based Camera

Retro games have seen a resurgence in the past few years. To complete the retro feel of these games, some developers go to great lengths to preserve the precise, “8-bit” feel of these games.

Your task is this: create a retro-feeling camera that locks to the scene’s grid.

Instead of smooth, continuous motion, the **camera only assumes positions that are multiples of the tile size**. Create a game with this kind of camera motion.
