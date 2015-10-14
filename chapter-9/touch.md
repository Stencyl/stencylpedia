# Contents

* Introduction
* Single Touch
* Multi-Touch
* Example: Multi-Touch
* Swiping
* Example: Swiping
 

## Introduction

Mobile apps are driven by touching, tapping and other gestures. Stencyl exposes all of these features through a combination of events and blocks.

 
## Single Touch

#### Using Blocks

Single-touch is handled **using the mouse blocks**. In other words, treat touch just like using the mouse.

![mouse-blocks](http://static.stencyl.com/help/images/mobile-input-1.png)

Mouse Action | Touch Action
--- | ---
Mouse is Down | Touching Screen
Mouse is Down on Actor | Touching Actor
X of Mouse | X of Touch
Y of Mouse | Y of Touch

#### Using Events

If you prefer to use Events, the analogous Mouse Events do the same thing.

![mouse-events](http://static.stencyl.com/help/images/mobile-input-2.png)


## Multi-Touch

For many games, single-touch is sufficient, but for some games, it’s necessary to support multi-touch. Such games require **tracking several fingers on screen moving independently**. One very common example of this use case is a game that displays multiple on-screen buttons, such as a platformer.

Stencyl supports multi-touch exclusively through an event.

![multitouch-event](http://static.stencyl.com/help/images/mobile-input-3.png)

This event is triggered **any time a touch begins, is dragged around or ends**. Using the **ID of touch block**, which maintains the same value throughout the lifecycle of a touch, you can refer to that touch and act accordingly. 

Additionally, you'll find that the ID of touch block also lets you get the X/Y positions of that particular touch by selecting those options from its dropdown.

![position-of-touch]()

 
#### Warning: Do Not Mix Single and Multi-Touch
You must enable multi-touch in **Settings > Mobile > User Input** to receive multi-touch events. Moreover, when multi-touch is enabled, avoid using single-touch input blocks, for they will act in unexpected ways.

In other words, when multi-touch is enabled, count on using multi-touch blocks all the way through.
 

## Example: Multi-Touch

In this example, the player can move some objects independently of each other using multi-touch.

* [Download the Demo](http://community.stencyl.com/index.php?action=dlattach;topic=16105.0;attach=14613) 
* [Discuss the Demo](http://community.stencyl.com/index.php/topic,16105.0.html)

> **Tip:** Are you just looking to implement virtual, on-screen buttons? Grab the On Screen Button behavior from StencylForge, which uses multi-touch in its implementation.


## Swiping

Swiping is a gesture in which the player presses a finger on screen and drags it in one direction. It is commonly used to scroll through menus or trigger certain actions.

![swipe](http://static.stencyl.com/help/images/mobile-input-4.png)

#### Swipe Event
In Stencyl, the preferred way to detect a swipe is through a Swipe event, accessed via **Add Event > Input > Swipe**.

![swipe-event](http://static.stencyl.com/help/images/mobile-input-5.png)
![swipe-event](http://static.stencyl.com/help/images/mobile-input-6.png)

#### Swipe Block
If you prefer to use a block to check for this instead, you can find one under User Input > Mobile-Only.

![swipe-block](http://static.stencyl.com/help/images/mobile-input-7.png)

