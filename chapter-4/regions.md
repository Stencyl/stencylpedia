## Contents

* What are Regions?
* Example: Entering a Door
* Creating Regions
* Detecting Entry/Exit
* Region Types
* Moving Regions
* Resizing Regions
 

## What are Regions?

Regions are invisible areas of a Scene that **detect the entry and exit** of Actors. In other words, we use regions when we want to know **when certain actors reach certain parts of a scene**.

![](http://static.stencyl.com/pedia2/ch4/regions/image09.png)

#### In what situations would regions be useful?

* Entering doors, pipes and other transportation devices
* Entering an area that continually heals the player (Healing Zone)
* Entering an area that continually harms the player (Lava Zone)
* Stepping on a switch


## Example: Entering a Door

Suppose that you are making an adventure game.

Your hero is walking outside, and he comes across a door to a house. You want to program your game so that when your hero **walks to the door**, he ends up **inside the house**.

![](http://static.stencyl.com/pedia2/ch4/regions/image12.png)
 
#### How would you do this?

We want the game to **detect** that the hero walked on top of the door. When this happens, we want to **transition to the house scene**.

Regions do exactly what we want. Here's how we'd do this (going with our example scenario).

1. Inside the **Scene Designer**, place a Region.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/regions/image06.png)<br/>

2. Flip to the scene's **Events** page. Add a **Specific Actor Enters Region** event.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/regions/image04.png)<br/>

3. **Fill out the event** with the desired values. In our case, we want to detect when our Hero enters the Door region.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/regions/image03.png)<br/>

4. Finally, we add in the **scene switch block** (under Scene > Game Flow) to change the scene.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/regions/image13.png)

That's it! Here's a [demo of the game in action](http://dl.dropbox.com/u/2769678/region-1.swf) [unavailable]. We've drawn the region for you, so you can see exactly where it is.


## Creating Regions

Regions can be created in one of two ways.

#### Method 1: Place Directly
You can place a Region directly into a Scene, as we did in the demo above.

![](http://static.stencyl.com/pedia2/ch4/regions/image06.png)

#### Method 2: Create on the fly
You can create a region on the fly from a Behavior or Event using a block. The block is under **Scene > Regions**.

![](http://static.stencyl.com/pedia2/ch4/regions/image14.png)

If you'd like to refer to this newly created region, use the Last Created Region entry anytime you're asked to Choose Region.

![](http://static.stencyl.com/pedia2/ch4/regions/image10.png)

 
## Detecting Actors entering, exiting or being inside Regions

Once you place a Region, you can detect when an Actor enters or exits the Region using an Event.

![](http://static.stencyl.com/pedia2/ch4/regions/image03.png)

Alternatively, you can **detect** if an actor is **currently** inside a given region.

![](http://static.stencyl.com/pedia2/ch4/regions/image07.png)

#### What's the difference?

* **Event** = I entered the house.
* **Is Inside** = Are you currently inside your house?

> **Troubleshooting Tip:** Be sure that collisions are enabled for the actor. Regions rely on the collision system to work.


## Region Types

Regions come in 3 flavors: Box, Circle and Polygon.

![](http://static.stencyl.com/pedia2/ch4/regions/image01.png)

Use the shape that best suits your game. For most games, box regions suffice.

> **Tip:** Hold down SHIFT while placing a box region to force it to become a square.


## Moving Regions

You can move regions around to a specific (x,y) coordinate or have a region "follow" an actor, which will reposition the region around the actor's center point.

In both cases, the operation happens instantly. If you wish to have a region continually follow an actor, you must continually move the region using either of these two blocks.

![](http://static.stencyl.com/pedia2/ch4/regions/image16.png)

The difference is that the "follow" block centers the region on the target Actor's center point.

 
## Example: Fiery Barrier

Suppose that in an adventure game, one of the hero's special moves is a fiery barrier in which all enemies approaching him within a 100 pixel radius automatically get killed.

([Play the Demo](http://dl.dropbox.com/u/2769678/RegionsDemo.swf)) [ no longer available ]

This could be implemented by creating a box region and having that region continually follow the Hero. When actors from the Enemy group enter this region, they get killed.

![](http://static.stencyl.com/pedia2/ch4/regions/image00.png)

 
## Resizing Regions

You can change the size of a Box or Circular region on the fly. **Resizing** uses the **top-left corner as the origin**.

![](http://static.stencyl.com/pedia2/ch4/regions/image05.png)

Because boxes and circles are defined differently, you have to use the corresponding block depending on what kind of region you're working with.

![](http://static.stencyl.com/pedia2/ch4/regions/image15.png)

If you need to reset a region's size back to its original, use the reset size of [ Region ] block. This block works on both box and circle regions.


## Summary

* Regions tell us when actors have reached certain parts of a scene.
* You can detect when an actor enters, exits or is currently inside a region.
* You can create regions either by placing them in the scene or creating them from a behavior.
* You can move and resize regions.
 

## Challenge: Pipes!

One of the signature moves in a Mario game is the ability to enter pipes. Implement this classic mechanic, using Regions.

<embed allowscriptaccess="never" height="315" loop="true" play="true" quality="high" src="http://www.youtube.com/v/ZX-mEw6YmDM?version=3&amp;hl=en_US" type="application/x-shockwave-flash" width="420">
