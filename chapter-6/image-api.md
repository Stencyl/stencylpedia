## Contents

* Overview
* Concepts: Images vs. Image Instances
* Creating Images
* Drawing on Images
* Creating Image Instances
* Tweening, Effects and More
* Challenges
 

## Overview

Up until this point, Stencyl has been based around Actors. If you want to accomplish something, you create an Actor. 

The problem with this approach is that Actors do a lot of things, and this limits how many Actors can be on screen at one time. When people push the limits of what Stencyl can do, they often create tons of actors, dragging the game's performance down, leading to misguided perceptions that the Stencyl engine is "slow." In reality, what's missing are better ways to accomplish visual eye candy without actors.

The Image API lets you do this, by **letting you create, modify and manipulate plain images in your game**. This sounds abstract, and rather than going handwavy about it, see the following demos to get a taste of what can be accomplished.

#### Demos

* [Tanks](https://static.stencyl.com/pedia2/ch6/image/tank.gif)
* [Swirl](https://static.stencyl.com/pedia2/ch6/image/swirl.gif)
* [Full Screen Effects](https://static.stencyl.com/pedia2/ch6/image/fs.gif)

 

## Concepts - Images vs. Image Instances

In order to use the Image API, you need to understand two things - **Images** and **Image Instances**.

**Images** are literally, the images themselves. In ActionScript, they are equivalent to BitmapData.

Images in themselves aren't displayed in game. In order to do that, you have to create an **instance** of an image, conveniently called an Image Instance. In ActionScript, they are equivalent to Bitmaps.

This distinction isn't all that different from the contrast between an Actor Type and an Actor (Instance). One is a template, and the other's the actual instance of the thing.

 

## Creating Images

Images can be pulled from many sources.

* Create a blank image with Width/Height.
* Create a copy of an existing image.
* Create an image from part of an existing image.
* Capture a screenshot of the game's current view and use that as an image.
* Use an Actor's current drawing as an image.
* Load an image from a file.
* Load an image from the web. (Images > Images > From External Sources > load image from URL: [ text ] and then do...)
 

#### Always Do This: Create Attributes for Images
When creating images, you almost always want to create an Image attribute, so that you can refer to the image in the future.

#### Loading Image from a File
You can load an image from a bundled file by following these steps.

> **Tip:** Use the menu item: **Debug > View > View Folder for this Game** to reveal your game's folder.

* Create an **extras** folder under your game's folder.
* Place your images under this folder.
* Use the **image from file** block to load them into images.

#### Gotchas
Do not abuse the capture screenshot feature. It takes time and is meant to be used sparingly, not every frame!


## Drawing on Images

Once you've created an image, you can perform drawing operations on that image. Note that if you create instances of the same image, modifying the original image will modify what each of those instances is displaying.

* Draw an image onto another image.
* Draw text on an image.
* Fill an image with a color.
* Clear a part of an image (or the whole image).
* Apply a mask to an image.
* Apply an effect (the same ones used for actors) to an image.
* Flip an image.
* Pixel swap an image.

> **Note:** All of these operations are permanent, so there is no way to undo them.
 

#### Applying Masks

The **clear/retain image using image** block is a powerful way to apply masks to an image. You can use this block to cut out shapes from an image, perfect for lighting effects.

When using **clear**, anything black in an image will be cleared out, while anything transparent will be retained. Values in between the two extremes are fine and will be treated as expected.

<img alt="Source" src="https://static.stencyl.com/pedia2/ch6/image/mask2.png" />&nbsp;+&nbsp;<img alt="Mask" src="https://static.stencyl.com/pedia2/ch6/image/mask1.png" />&nbsp;=&nbsp;<img alt="Result" src="https://static.stencyl.com/pedia2/ch6/image/mask3.png" />

Conversely, when using **retain**, anything black in an image will be kept, while anything transparent will be cleared out.

![Retain](https://static.stencyl.com/pedia2/ch6/image/mask4.png)

> **Note:** When using files from the **extras** folder, make sure the images were saved with transparency enabled.

#### Setting Pixels
When setting many pixels at a time, use the batch draw block (placed right above the set pixel block). This informs the system not to push an image's updates to all its instances until you've finished your work.

![Setting Pixels](https://static.stencyl.com/pedia2/ch6/image/batch.png)

#### Gotchas
Many of these operations, particularly pixel swap, effects and masks perform these operations in software, so they are not meant to be used in real-time but rather, applied sparingly.

 

## Creating Image Instances

In order to display an image on your game, you must **create an image instance** and then **attach** that image instance to the scene.

You can attach in one of three ways.

1. Attach it to an actor.
2. Attach it to a specific layer in the scene.
3. Attach it to the very front. This will disregard the camera.
 
#### A Common Mistake
New users often make a common mistake when creating instances. They find themselves doing the following and wondering why their image instance is doing nothing. Can you spot what's wrong?

![common-mistake-1](https://static.stencyl.com/pedia2/ch6/image/mistake.png)

The problem is that they are **creating a brand new instance for each subsequent operation**. What they really meant to do was save that instance to an attribute for future reference.

![common-mistake-2](https://static.stencyl.com/pedia2/ch6/image/mistake-fixed.png)

 
## Tweening, Effects and More

Once you've created an image instance, you can manipulate its properties much like a regular actor.

* Set z-order (layer)
* Set position, angle, size, opacity
* Tween it.
* Apply a blend mode to it.
* Apply an effect to it.
* Set its origin point.
 
#### Z-Order
Altering the z-order for an image instance will do so within the confines of what it's attached to. It does not switch the layer it's attached to or anything like that. It's strictly to control ordering of elements within what it's attached to.

> **Note:** Setting the z-order as a number can be finnicky if you provide too high a value. Consider using the relative layering features instead (move back/forward a layer, to front/back).
 

#### Setting the Size
Setting the width/height of an image instance is done in relative (percentage) format, so 200% will double its size in that dimension while 50% will halve it.

> **Note:** Getting an image's width/height (in %) returns the value in relative format where 1.0 means 100%, 0.5 means 50% and 2.0 means 200%.
 

#### Setting the Origin Point
By default, scaling and rotations on an image instance are relative to the top left point. To change this, set the origin point.

![setting-origin-point](https://static.stencyl.com/pedia2/ch6/image/origin.png)
 

## Challenges

The Image API is undoubtedly a powerful tool that opens up new possibilities for Stencyl. We've just scratched the surface and put these challenges out as exercises for you to work through.

#### Challenge 1 - Destructible Terrain
Create a Tank Wars kind of game where shooting the terrain will destroy it by exploding holes into it. Want a hint? You'll need to implement some form of collision detection using the **get pixel** block.

![Tanks](https://static.stencyl.com/pedia2/ch6/image/tank.gif)

#### Challenge 2 - Lighting Effects
Using the mask feature, create a game in which both the hero and enemies hold lanterns that project light in front of them.
