## Contents

* What is Box2D?
* The Physics Page
* General Tab
* Heaviness Tab
* Material Tab
* Damping Tab
* Advanced Tab
* Lightweight Actors
* Gotchas
 

## What is Box2D?

Stencyl uses an industry-standard physics engine (**Box2D**) in all its games. What's the benefit? You get realistic and accurate collisions for free, and Actors generally **behave like real-world objects**.

How realistic? Try out the following demo.

<a href="https://www.stencyl.com/game/play/10715">![Ragdoll Demo](https://static.stencyl.com/pedia2/ch3/ragdoll.png)</a>

 
> **Note:** The rest of this article is a reference guide for an actor's Physics page. If you're skimming or are a first timer, read through these sections and skip the others for now. They are the most important! 
* General Tab
* Lightweight Actors
* Gotchas
 

## General Tab

#### What kind of Actor Type?
Determines whether the Actor can move or not.

* **Cannot Move**: The actor cannot move or be moved, thus, becoming stationary.
* **Cannot Be Pushed:** The actor can move but cannot be moved by another actor.
* **Normal:** The Actor can move on its own and be moved by other Actors.

> **Gotcha:** A "Cannot Be Pushed" actor will not collide with tiles. In Box2D speak, it's known as a Kinematic body. A clever way to simulate "Cannot Be Pushed" without its sideeffects is to assign a very high mass to an Actor.

#### Can Rotate?
Determines whether or not your actor can rotate. Rotation happens either naturally through physics, setting the turning speed or twisting it with some force.

> **Note:** Setting the direction (angle) of an actor can still be done, regardless of this setting. Tweening also ignores this setting.

#### Affected by Gravity?
Gravity is a constant force that affects all bodies within a scene. Gravity can be set to *any* direction and magnitude (strength) via the Physics page of a Scene. **Gravity does not necessarily have to point downwards**.

You can set an Actor to obey or ignore gravity.

> **Note:** The apparent "strength" of gravity is affected by an Actor's mass. The higher the Actor's mass, the slower it will fall. This is **not** how gravity works in real life but is a simple approximation by Box2D to simulate it.


## Heaviness Tab

#### Mass
How much your actor "weighs." The "heavier" you make an actor, the harder it will be for other objects to move it.

> **Tip:** Setting a very high mass can roughly simulate infinite mass / cannot be pushed, without the side-effects of that mode.

#### Angular Mass
Angular mass determines an actor's resistance to rotational forces. As such, the higher the number, the slower an actor will rotate when subjected to rotational forces (twisting).

> **Note:** Angular mass is only relevant if the Actor is set to "Can Rotate"


## Material Tab

#### Preset Materials
Materials are preset values that use different combinations of Friction and Bounciness to simulate the material listed.

Material | Friction | Bounciness
--- | --- | ---
Wood | 0.5 | 0.17
Metal | 0.13 | 0.17
Stone | 0.75 | 0.05
Plastic | 0.38 | 0.09
Rubber | 0.75 | 0.95
Dead Weight | 1 | 0
Super Ball | 1 | 0.95

#### Friction
Friction determines the "roughness" of the Actor's surface. A high friction will cause an Actor to slow down quicker when sliding. A low, or zero, friction will cause the Actor to glide far or never slow down at all.

In real-life high friction surfaces would include dirt and sandpaper. Low-friction surfaces could include ice and glass.

<a href="https://static.stencyl.com/pedia2/ch3/physics/Friction.swf">![Friction Demo](https://static.stencyl.com/pedia2/ch3/physics/demo3.png)</a>

> **Demo Note:** In this demo, press left/right and lift your key off. Observe that one actor stops moving quickly (high friction) and the other keeps moving, as if he were on ice.
 
#### Bounciness
Setting bounciness to a value of 1.0 means an actor will bounce back to the same height it fell from, whereas a value of 0.0 means it won't bounce at all.

<a href="https://static.stencyl.com/pedia2/ch3/physics/Bounciness.swf">![Bounce Demo](https://static.stencyl.com/pedia2/ch3/physics/demo2.png)</a>

> **Demo Note:** Demo Note: In this demo, the balls bounce differently depending on their bounciness. The one with bounciness = 1 bounces back to the same height.
 
#### How Friction / Bounciness Work  
Friction and Bounciness **multiply** the values of the two colliding Actors to come up with the effective Friction or Bounciness. For example, if two actors have a friction of 0.5, their effective friction becomes 0.25.

This works out well for actors that have a friction or bounciness of 0 - as you'd expect, that negates everything and causes an effective friction/bounciness value of 0, too.

Terrain/Tiles have friction and bounciness values of 1, so they have no net effect whichever way.


## Damping Tab

Damping is a difficult topic to visualize. It's a form of resistance against motion or rotation that varies depending on how quickly the Actor is moving or rotating.

#### Linear Damping
Linear Damping is like wind or **air resistance**. It grows stronger as your Actor moves more quickly to the point where the Damping is so strong that the Actor is unable to move any faster. This is known as Terminal Velocity.

<a href="https://static.stencyl.com/pedia2/ch3/physics/Damping.swf">![Damping Demo](https://static.stencyl.com/pedia2/ch3/physics/demo4.png)</a>

#### Angular Damping
**Angular Damping is the same idea, except applied to rotation**. It puts an effective cap on how fast an Actor can rotate and smooths out things if you find your Actor to rotate too quickly when subjected to twisting (angular forces).


## Advanced Tab

#### Disable Physics
Let you opt this Actor out of physics. We talk about this further in the [next section](https://www.stencyl.com/help/view/working-with-physics/#lightweight).

> **Note:** Collisions for this Actor will also cease to function when you do this.
 
#### Auto-Scale Collision Bounds
Choosing "Yes" for this option will automatically re-size your Actor's collision bounds when you resize the Actor using the "scale to" Tweening block. Choosing "No" means the collision bounds will stay the same regardless of what happens to the Actor.

![](https://static.stencyl.com/pedia2/ch3/physics/image00.png)

<a href="https://static.stencyl.com/pedia2/ch3/physics/Auto-Scale%20Collision%20Bounds.swf">![Scale Bounds Demo](https://static.stencyl.com/pedia2/ch3/physics/demo1.png)</a>

> **Demo Note:** Notice that the actor on the right remains at the same collision size.
 
#### Enable Continuous Collisions
Enable this setting to prevent this Actor, if it moves quickly enough, from penetrating through thin surfaces, like shown below. This setting is useful for small and quick actors, such as bullets, arrows and other weapons. 

![CCD](https://static.stencyl.com/help/images/ContCollisionDetect3.png)

[Learn more](https://www.stencyl.com/help/view/continuous-collision-detection/) about Continuous Collisions.


#### Can be paused?
Opts an Actor in/out of the [Pausing](https://www.stencyl.com/help/view/pausing/) system.

 
## Lightweight Actors

**Lightweight Actors are actors that opt out of the physics system.**

The Lightweight Actors feature works well for games that **involve many actors** or require more precise motion and collision detection than Box2D allows. For example...

* Shoot 'Em ups
* Puzzle Games
* Pixel Perfect Platformers (like N)
* Point and Click Adventures

The Lightweight physics feature lets you **selectively opt an actor out of physics**. Even in regular games, this can prove to be useful for...

* User Interface Elements
* Particles
* HUDs

Bear in mind that when you turn off physics, the actor **no longer collides with anything**, can no longer be pushed and is generally barred from any physics-related features. Setting position and velocity will still work.

Going with lightweight actors can be a game-saving choice if done right, but you need to understand its limitations.

> **Note:** [Images](https://www.stencyl.com/help/view/image-api) are arguably a more powerful form of lightweight actor. They are more difficult to setup and have a different set of limitations, but they work particularly well for creating special effects and eye-candy.

 
## Gotchas

#### Snagging
Sometimes, an actor will get caught in the corner of a box and be unable to move further. In a similar scenario, a jumping actor who jumps right next to a wall versus a little bit off the wall will find his jump to be shorter.

![Snagging](https://static.stencyl.com/pedia2/ch3/physics/image02.png)

The reasons behind this are quite technical, but the workarounds are less so. The easiest workaround is to redo the actor's collision shape as...

* A circle.
* A box with its corners chopped off slightly or some other means to avoid the sharp 90 degree corners. We did this for a Mario-like platformer and made an **octagon**.<br/><br/>![](https://static.stencyl.com/pedia2/ch3/physics/image01.png)

#### My actors don't collide!
Several legitimate reasons for this.

* The two actors are set to "Cannot Move", "Cannot Be Pushed" or a combination of the two. This is just the way Box2D works and can catch you off guard.
 
* Did you make sure the actors aren't set as [Sensors](https://www.stencyl.com/help/view/collisions-and-groups/#sensors)?<br/><br/>![Sensors](https://static.stencyl.com/pedia2/ch3/collisions/image13.png)<br/>

* Did you make sure that the actors are from a pair of [Groups](https://www.stencyl.com/help/view/collisions-and-groups/#groups) that are to collide with each other?<br/><br/>![Groups](https://static.stencyl.com/pedia2/ch3/collisions/image14.png)


## Summary

* Through Box2D, Stencyl brings realistic physics to all games.
* Opt an Actor out of physics to improve performance for games with many actors or no need for physics.
* Box2D is powerful, but it can sometimes present challenges when you want your game to not operate like the real world.
 

## Challenge: Platforms!

**Create a simple game with moving platforms** inside of it, like you would find in any Mario game. It's trickier than it sounds at first!

What are some of the considerations?

* How do you prevent the platform from shifting when something steps on it?
* How will the character stay on the platform after stepping on it?
* If the platform is moving up and down, what happens if it moves too quickly downwards?
* How will you move the platforms? Setting position? Velocities? Forces?
* How do you ensure that the platform starts and ends at the same positions?

Start with a platform that moves up and down. Then, try one that moves left and right.
