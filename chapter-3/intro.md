This article introduces you to the key concepts behind actors. Because Actor concepts are intertwined, it's useful to get a little exposure to each before delving into full detail.

## Contents

* What are Actors?
* Appearance
* Behaviors
* Collisions (Physics)
* Actor Types vs. Actor Instances


## What are Actors?

Actors are the living, interactive parts of a game. Actors are the players, enemies, projectiles, vehicles, inteface elements and anything in a game that "lives."

Every actor can be broken up into a few common elements.

* **Appearance** - How the actor **looks** or appears in-game.
* **Behavior** - How the actor **behaves** or acts.
* **Physics** - How the actor **interacts** with the world when it collides with it. This also determines what shape(s) the actor takes on, whether it's a box, a circle or something else.
 

## Appearance

Appearance dictates how an Actor looks. In the 2D games we build, we call these **animations**.

![Animations](https://static.stencyl.com/pedia2/ch3/animation/image21.png)

[Animations](https://www.stencyl.com/help/view/animations/) are a collection of frames that are played out in sequence and usually loop, to form a fluid, living visual representation of the actor.

Actors need not be bound to a single animation. They can switch between different states, each of which is associated with its own Animation and collision bounds.

Consider the hero or "player" character in a platformer such as Mario. This character will have states for standing, walking, running and jumping.

> **Coming from Scratch?** Animation States are equivalent to **costumes**.


## Behaviors

Behaviors tell an actor what to do and how to react. They provide specific logic which allows the actor to perform unique tasks like run, jump, walk, fire weapon and more.

![Behaviors](https://static.stencyl.com/pedia2/ch3/intro/image01.png)

Behaviors are unique in that they are **reusable** and **configurable**.

#### Reusable
They can be attached to other actors, thereby letting you reuse the same behavior for multiple actors. Reuse is good because it saves you effort and prevents bugs stemming from duplicate code (that you are likely to edit in the future).

![Reusable](https://static.stencyl.com/pedia2/ch3/intro/image00.png)

#### Configurable
You can configure their Attributes (properties). For example, if you attached a Walking behavior to an actor, you could customize its walking speed.

![Configurable](https://static.stencyl.com/pedia2/ch3/intro/image02.png)

#### Events Page
You may notice an "Events" page when opening up the Actor Editor. This page lets you attach Events directly to an actor, without requiring a full behavior.

This is useful for adding logic that's specific to the actor and is also great for rapidly prototyping ideas.

> **Further Reading:** We don't cover the Behaviors or Events pages in Chapter 3, since you got exposed to plenty of that already in Chapter 2. For a refresher, read [Chapter 2's introduction](https://www.stencyl.com/help/view/introduction-to-behaviors/).

 
#### Collisions (Physics)

In many games, Actors collide with other Actors. In our engine, our Actors **obey the laws of physics and act much like real-world objects**.

In order to make this all happen, the Actors need to assume a physical form, whether it's a box, a circle, a polygon or some combination of those.

![Add Collision Shape](https://static.stencyl.com/pedia2/ch3/collisions/image01.png)

These physical forms are known as **Collision Bounds**, and they are tied directly to **Animation States**. Intuitively, this makes sense. If your character stands, he takes on one shape. If he's "ducking" on the ground, his shape will be shorter.

![](https://static.stencyl.com/pedia2/ch3/intro/image03.png)

#### Sensors
Sensors allow collisions to occur without generating a physical reaction. This is useful when you don't want a certain Actor to "push" other actors away but do want that collision to happen.

For example, slashing a sword or being hit by a fireball shouldn't necessarily knock you back, but it should definitely hurt.

#### (Collision) Groups
[Groups](https://www.stencyl.com/help/view/collisions-and-groups/) let you filter collisions, so that only certain classes of Actors collide with each other.

![Collision Groups](https://static.stencyl.com/help/images/CollisionGroupsIllustration2.png)

To take a real-life example, consider the concept of "friendly fire" - sometimes, you don't want your enemy's bullets to kill other enemies. Groups let you prevent this from happening.

#### Physical Properties
As mentioned earlier, Actors obey the laws of physics. The Physics page lets you tweak an actor's [physical attributes](https://www.stencyl.com/help/view/working-with-physics/) that don't pertain to its collision bounds.

Here are just some of the properties you can tweak.

* Whether an actor moves, rotates or obeys gravity.
* Mass
* Friction
* Bounciness
* Damping

 
## Actor Types vs. Actor Instances

Two terms you may see thrown around are Actor Types and Actor Instances. More confusingly, we may abbreviate both to simply "Actor", with no indication, outside of context, which of the two we're talking about.

The difference is this...

* **Actor Types** are like **templates**
* **Actor Instances** are the actual "Actors" that **exist** inside a scene

 
#### Example: A Common Enemy
Consider a game like Super Mario Bros. Consider this familiar enemy, which you may recognize...

![Enemy](https://static.stencyl.com/pedia2/ch3/intro/image04.png)

We expect this enemy to act in the same way, namely to walk in one direction until it hits a wall, then to reverse direction. If we hit this enemy, we get hurt.

![Enemy](https://static.stencyl.com/pedia2/ch3/intro/image06.png)

But every instance of this enemy exists at a different location on the scene. When you step on one, it dies. These are each separate instances of Goomba.

![](https://static.stencyl.com/pedia2/ch3/intro/image05.png)

This, in essence, is the distinction between an Actor Type and Actor Instance.

> **Programmers' Note:** Types are akin to Classes, while Instances are akin to Objects.
 

## Summary

* Actors are the things that make a game come to life. In simple terms, they are the "objects" or "props".
* Actors can take on different Animation States, each with its own Animation and Collision Bounds.
* You can control how an Actor acts by attaching Behaviors or Events.
* Actors obey the laws of physics. You can tweak an Actor's physical properties, such as whether it can move, its mass and friction.
