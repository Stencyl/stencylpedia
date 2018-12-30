## Contents

* What is Tweening?
* Easing
* Uses for Tweening
* Gotchas


## What is Tweening?

Tweens. We're not talking about pre-teens.

Instead, we're talking about a powerful ability to bring **numerical properties** of actors to a **destination value** over time.

![Tween Example](http://static.stencyl.com/pedia2/ch3/tweening/image02.png)

Tweens apply to the following properties.

* X Position
* Y Position
* Angle
* Scale (Size)
* Opacity (Fading)


## How To Tween

All Tweens are initiated using blocks under the **Actors > Tweening** category.

![](http://static.stencyl.com/pedia2/ch3/tweening/image05.png)

The parameters for each block differ a little, but each tween block requires these 3 bits of info:

* The **actor** the tween will apply to.
* **How long** (in seconds) the tween will last.
* What **easing** function is used. We describe this next.
 

## Easing

You may wonder what the final dropdown in each tweening block is all about. We call this the Easing Function, or Easing for short.

![Easing](http://static.stencyl.com/pedia2/ch3/tweening/image03.png)

Suppose that we want to slide an actor from point A to point B. Without easing, the actor would move directly from A to B at a constant speed. In many cases, this would look flat and boring.

Easing changes this by varying the rate at which that change happens in accordance with some mathematical functions. It's best to try this out for yourself and see what works best for your game.


## Uses for Tweening

Use tweens to add **visual flair and polish** to your game. How so?

* **Slide** buttons off the screen when exiting a menu.
* **Grow** a button when your mouse rolls over it.
* **Rotate** an object to provide visual affordance or flair.
* **Fade** out elements that are inactive or not meant to be touched.

Tweens can make all the difference between a game that feels polished and one that is functional but feels raw.

Next time you play a game, **observe where tweens are used**. You'll be surprised to see how pervasive they are!


## Gotchas

#### Scaling sometimes doesn't scale up the collision bounds.

If you specify an Actor to not auto-scale its collision bounds, you may observe that scaling an Actor up or down will not change its collision bounds accordingly.

![Auto Scale](http://static.stencyl.com/pedia2/ch3/tweening/image01.png)

#### Tweening and Physics

When sliding, rotating or scaling actors, do not expect the physics to act reliably during this time.

For example, if you are sliding an actor to the right, and it slams into a box, it may sail past the box instead. Why? Because tweening is directly setting the position (or rotation) of the actor continually. It's difficult for the physics engine to work properly since you are effectively "teleporting" the actor around.

If accurate physics are desired, **avoid using tweens** and **use conventional methods** instead.

* Set the actor's velocity or angular velocity.
* Use forces to push the actor or twist it.
 

## Summary

* Tweens let you apply gradual changes to an Actor's property over time.
* Physics becomes inaccurate (it works, but is like directly setting position) when using tweening to move an Actor. Use forces or velocity setting instead.
