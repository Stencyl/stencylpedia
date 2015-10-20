## Contents

* What are Animations?
* How To: Importing Animations
* Frames
* Collision Data
* Switching Animations
* Controlling Playback
* Design Problem - More Animations vs. More Actor Types
* Gotchas
 

## What are Animations?

Animations bring actors to life. They represent the visuals of an actor, its collision bounds and the notion of being in a certain "state" - such as running, walking and jumping.

#### What are examples of animation states?

* A platformer hero's states (Stand, Walk, Run, Jump)
* Destructible Objects that "break" when hit by something else (Broken, Not Broken)
treasure-chest-animation
* Treaure Chest (Opened, Not Opened)<br/><br/>![](http://static.stencyl.com/pedia2/ch3/animation/image18.png)

#### What does an Animation Consist of?

Each Animation state consists of 2 separate parts:

* Frames (how it **looks**)
* Collision Bounds (its collision **shape**)

**Frames** are like pages in a flipbook. Each frame represents a a different image or "page" in the book. When these images change quickly over a period of time, the result is an animation.

![stencyl-animation-frames](http://static.stencyl.com/pedia2/ch3/animation/image21.png)

**Collision Bounds** determine the physical shape(s) that an an actor assumes in a particular Animation state.

![](http://static.stencyl.com/pedia2/ch3/animation/image06.png)
 

## How To: Importing Animations

Now that you understand what animations are, let's go over the import process. You can import animations in one of several ways.

* Pick an image.
* Drag and Drop.
 

#### Method 1: Pick an Image

> *In this instance, we're assuming you've already got an Actor open in the Actor Editor.*

1. Click on **Click here to add frame** under the Frames pane. <br/><br/>![stencyl-choose-image](http://static.stencyl.com/pedia2/ch3/animation/image08.png)<br/>

2. You'll now see this dialog. Click the **Choose an Image...** button and pick out the desired image. Want to follow this exact example? Use this [image](http://static.stencyl.com/pedia2/ch3/animation/sample.png).<br/><br/>![stencyl-import-images](http://static.stencyl.com/pedia2/ch3/animation/image09.png)<br/>

3. Now, configure **columns and rows** to break up the image, as appropriate depending on how many cells it has in those directions.<br/><br/>![stencyl-import-frames](http://static.stencyl.com/pedia2/ch3/animation/image10.png)<br/>

4. If applicable, enter in values for the border and spacing fields. The majority of images do not need to worry about these fields.

5. Click Add to complete the process. That's it.

After importing frames, you can give the Animation a name, alter frame durations and other properties we described above.

> Note: Mobile games have to import images at quadruple their size in order to accomodate larger resolution displays. Read our [Scaling](http://www.stencyl.com/help/view/mobile-app-scaling/) article for details.
 

#### Method 2: Drag and Drop

You can drag and drop an image into Stencyl while the Actor Editor is open. Doing this will bring up the dialog you see in Step (2) of the standard method.

> **Notes**
* Dragging in an animated GIF will bypass the dialog and immediately import the frames.
* Dragging in an image to the Dashboard or an editor that is not the Actor Editor will have varying effects, none which will import a new animation for the current Actor.


## Working with Animations

Now that you've imported an image, you'll see its details, We'll step through what each part means.

![stencyl-animation-frames](http://static.stencyl.com/pedia2/ch3/animation/anim-page.png)

#### Name
Each animation state is given a name, which you use when you want to switch animations.

#### Looping?
Frames can be set to loop or play through just once.

#### Synchronized?
Synchronized animations will animate in at the same time as each other. To put this more concretely, think about the coins in a Mario game. Have you noticed that their animations always look the same no matter what? If this weren't the case, it would look disconcerting.

#### Origin Point
An Animation can also have a designated origin point. The origin point is used to determine the point by which an actor **rotates or scales**. **By default, this is set to the center point**.

![image-origin-point](http://static.stencyl.com/pedia2/ch3/animation/image07.png)

#### Frame Duration
Every frame can be given a different duration (in milliseconds). Double-click each frame's box to edit the duration.

![stencyl-frame-duration](http://static.stencyl.com/pedia2/ch3/animation/anim-duration.png)

> **Notes:** The minimum duration is 10ms. To edit multiple frame durations at a time, select multiple frames (using SHIFT or CTRL/Command) and click Edit Frame in the bar below.

#### Editing in an External Editor

Individual animation frames can be edited in an external editor. This is useful for making small tweaks to the graphics, without having to re-import the whole animation.

Double-click a frame's box to bring up its edit dialog. Then, click the **Edit Image** button to open it up an external editor.

![](http://static.stencyl.com/pedia2/ch3/animation/edit-frame.png)

> **Note:** You set the External Editor from Stencyl's Preferences dialog. By default, we use an image editor that we [bundle](http://www.stencyl.com/help/view/pencyl-image-editor/) in, but you can set it to any app you like, such as Photoshop, GIMP or Paint.NET.


## Collision Bounds

Collision Bounds determine the physical shape(s) that an an actor assumes in a particular Animation state.

To define Collision Bounds, flip to the "Collisions" page of the Actor Editor. There, you will be able to edit your Animation's Collision Bounds on a per-animation basis.

![collision-bounds](http://static.stencyl.com/pedia2/ch3/animation/image06.png)

#### Collision Shapes

Stencyl supports 3 kinds of collision shapes: Boxes, Circles and Polygons. (For Polygons, only convex shapes are allowed!)

![stencyl-collision-shapes-buttons](http://static.stencyl.com/pedia2/ch3/collisions/image01.png)

You can place an arbitrary number of these shapes, in order to form more complex ones.

![stencyl-place-collision-bounds](http://static.stencyl.com/pedia2/ch3/collisions/image04.png)

#### How To: Adding Collision Shapes

To place a collision shape, click the Add Box / Add Circle / Add Polygon button. A dialog will pop up asking you for the shape's dimensions and position. 

IMG

After confirming that, the shape will be added to the canvas.

IMG

> **Tip:** You cannot set collision bounds per-frame, yet. This can be worked around by defining a new animation per-frame and switching animations.
 


 

## Switching Animations

All of these blocks are found under **Actor > Drawing**.

#### Switch Animation
This block switches the actor's animation to the one you specify.

![stencyl-design-mode-switch-animation-block](http://static.stencyl.com/pedia2/ch3/animation/image13.png)

> **Note:** Do not type in the animation name directly. Instead, use the "as animation" block and type the name into that.

![stencyl-switch-animation-block](http://static.stencyl.com/pedia2/ch3/animation/image11.png)
 
#### What's the current Animation?
This block returns the animation that is currently playing. Note that this returns the animation, not the textual name of the animation.

![stencyl-design-mode-get-current-animation-block](http://static.stencyl.com/pedia2/ch3/animation/image14.png)

#### Is the current Animation still playing?
Returns ```true``` if the current animation is still playing, otherwise it returns ```false```. This is only useful for animations that aren't set to loop.

![stencyl-design-mode-animation-playing-block](http://static.stencyl.com/pedia2/ch3/animation/image12.png)


## Controlling Playback

#### Switch to Frame
This block lets you skip around an animation or reset an animation to its starting frame. Specify the frame index you wish to jump to.

![stencyl-design-mode-switch-frame-block](http://static.stencyl.com/pedia2/ch3/animation/image15.png)

> **Note:** Frame indices are displayed in the gray boxes and start from 0. Switching to an invalid frame leads to nothing happening.
 
#### Current Frame Index
This block reports the index that the animation is currently playing. 

![stencyl-design-mode-get-current-frame-block](http://static.stencyl.com/pedia2/ch3/animation/image16.png)

> **Tip:** This is useful when you want to tie some logic that's triggered when a certain index is reached. In animation terms, this is called a keyframe.

#### Total Frame Count
This block reports the total number of frames in the current animation.

![stencyl-design-mode-get-frame-count-block](http://static.stencyl.com/pedia2/ch3/animation/image17.png)
 

## Design Problem: More Animations or More Actors?

There is no limit to the number of animations an actor may have. However, it's best to consider when it's appropriate to go with more animations or whether it's better to create a brand new actor.

#### The "Zelda" Dilemma

The "Zelda" Dilemma is a classic game design problem you run into when making an Adventure game and decide how you want to create your Hero character.

So suppose that we start with just the basic animations.

* Walk
  * Left
  * Right
  * Up
  * Down

Not to bad so far. But Link holds a sword! So we have to add 2 more sets of animations, one for holding the sword and one for slashing it.

* Walk
  * Left
 * Right
 * Up
 * Down
* Walk + Sword
 * Left
 * Right
 * Up
 * Down
* Walk + Slashing Sword
 * Left
 * Right
 * Up
 * Down

But wait, there's more! Link changes swords throughought the game. He can hold the plain sword, the Master Sword and the Golden Sword, and they all look different! That would triple the animation count.

![zelda-link-animation](http://static.stencyl.com/pedia2/ch3/animation/image00.png)

And what about the Bow and Arrow, holding a shield and... you get the picture.

#### The Bottom Line
In cases like these, **it's better to create a new actor rather than add more animations**. This is particularly applicable when an actor equips items that don't alter his animation and could be convincingly drawn separately.

![zelda-link-sword-animation](http://static.stencyl.com/pedia2/ch3/animation/image01.png)

There are other benefits to having "attachments" as different actors.

* Easier to define collision bounds, particularly for weapons.
* Confines extra behaviors to the separate actor, rather than creating 1 monolithic actor with everything.

 
## Gotchas

#### It's best if all animations are the same size.
It's often necesary to ensure that all animations of an actor are equal in size. Making animations different sizes, for the same actor, could have a negative impact, especially if the origin point is different in each animation.

Two common scenarios are:

* The actor magically jumps to a slightly off-center location when you switch animations.
* The actor's collisions mess up because the new animation has the collision bounds located in a different part of the animation.

#### Animations, Blocks & Attributes
Note that when using the "switch animation" block, you cannot type text directly into the blank. Instead, you have to wrap that text inside an "as animation" block like the following.

![stencyl-design-mode-as-animation-casting-block](http://static.stencyl.com/pedia2/ch3/animation/image11.png)

> **Reminder:** All animation-related blocks are located under Actor > Draw.
 

#### Actors with No Animations
Actors with no animations at all may crash the game. We'll address this in a future version of Stencyl. Note that this is different from an Actor with a single blank (0 frame) animation, which will work just fine.


 

## Summary

* Animations are states, such as standing, walking and running.
* Animations consist of frames (how it looks) and collision bounds.
* Exercise good judgement in deciding whether to go with an actor with many animations versus several actors with fewer animations.
 

## Challenge: Equipment for an Adventure Game

We talked about the "Zelda Dilemma" above. Now's your chance to see this for yourself and do things the right way.

Create a simple walkaround demo in which the character can equip different items that show up in that character. Do this the right way, by making those items each their own actors.

![zelda-link-animation-frames](http://static.stencyl.com/pedia2/ch3/animation/image00.png)
