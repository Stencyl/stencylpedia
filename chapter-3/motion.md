## Contents

* How Actors Move and Rotate
* Position
* Velocity (Speed)
* Forces (Pushing)
* Velocity vs. Forces
* Direction
* Turning Speed
* Twisting
 

##How Actors Move and Rotate

What good is a physics game if you can’t make things move?

In Stencyl, you can **move** an Actor in one of three ways:

* Setting the Actor’s **position**
* Setting the Actor’s **velocity**
* **Pushing** the Actor in the direction you’d like it to move

On top of this, you can **rotate** an Actor in a similar set of ways:

* Setting the Actor's **angle**
* Setting the Actor's **turning speed**
* **Twisting** the Actor in the direction you'd like it to rotate


## Position

The position of an Actor is its location within a scene, measured in X (horizontal) and Y (vertical) coordinates. (0,0) corresponds to the top left corner of the scene.

![position](http://static.stencyl.com/pedia2/ch4/basics/image12.png)

#### How To: Setting an Actor's Position
You can set an Actor’s position using the “Set X/Y to” block under **Actor > Position**.

![set actor position](http://static.stencyl.com/pedia2/ch3/motion/image00.png)

#### How To: Getting an Actor's Position
You can get the Actor's position using the "Get X/Y" block under **Actor > Position**.

![get actor position](http://static.stencyl.com/pedia2/ch3/motion/image01.png)

> **Note:** The dropdown has variants for grabbing the "center" x and y positions too.
 
#### Gotcha: Setting Position = Teleporting
You'll find that while setting an Actor's position is a simple and easy way of moving an Actor, it comes with **drawbacks** depending on the game you're making.

Problems come about if you're making a game that leans on physics. Let's take a simple example.

Imagine that you've got an Actor that moves across a floor towards a wall.

![](http://static.stencyl.com/pedia2/ch3/motion/image18.png)

To move the Actor, you are incrementing its position like this. (In short, x = x + 10)

![](http://static.stencyl.com/pedia2/ch3/motion/image17.png)

You now test the game and notice that the ball sails right past the wall as if it weren't there. What happened?

Because setting positions is like teleporting. The actor isn't smoothly moving towards the right. He's teleporting to the right in steps, big enough steps that he skips the wall entirely, and no collisions are recorded.

![](http://static.stencyl.com/pedia2/ch3/motion/image16.png)

So what's the bottom line? The bottom line is to **avoid setting an Actor's position when you're trying to achieve constant motion**.

If you're trying to teleport an actor, or if the game isn't quite so physical in nature (an RPG), then setting an actor's position is appropriate.

 

## Velocity (Speed)

Velocity is the speed of an object in a given direction.

 

#### How To: Setting an Actor's Velocity
Set an Actor’s X/Y speed using the “Set X/Y speed to” block under **Actor > Motion**.

![](http://static.stencyl.com/pedia2/ch3/motion/image02.png)

**Reminder about Directions**

Value | Direction
--- | ---
Positive X | Right
Negative X | Left
Positive Y | Down
Negative Y | Up

> **Note:** The unit of speed in Stencyl is 10 pixels per second.
 

#### How To: Setting an Actor's Velocity using Direction + Speed
If you prefer setting the Velocity in terms of a direction and speed, we have a block for that too under **Actor > Motion**.

![](http://static.stencyl.com/pedia2/ch3/motion/image03.png)

> **Note:** Direction is in degrees (0 - 360). 0 degrees is right. Angle sweeps clockwise, so 90 degrees would be down.
 
#### How To: Getting an Actor's Velocity
In some cases we may also want to find out how fast an Actor is traveling in a given direction. We can do this by using the “X/Y speed of” block under **Actor > Motion**.

![](http://static.stencyl.com/pedia2/ch3/motion/image05.png)

 
## Forces (Pushing)

What is a force? In Stencyl terms, a force is something that **pushes an object in a given direction** with a certain magnitude (the strength/power).

![](http://static.stencyl.com/pedia2/ch3/motion/image14.png)

> **Note:** Forces are always applied relative to the Center of Mass.
 

#### How To: Pushing
You can push an object towards a given point using the “Push toward [X, Y]” block. (Actor > Motion)

![](http://static.stencyl.com/pedia2/ch3/motion/image06.png)

The "strength" of the force is something you'll have to experiment with to pin down a good value. Bear in mind that like real forces, the mass of the target Actor will determine just how effective your push is. We'll talk about setting the Actor's mass in the [Physics lesson](http://www.stencyl.com/help/view/working-with-physics/).

**Reminder about Directions**

Value | Direction
--- | ---
Positive X | Right
Negative X | Left
Positive Y | Down
Negative Y | Up
 

#### How To: Pushing towards Angle
You can push an object in a given direction using the “Push toward [angle]” block. (Actor > Motion)

![](http://static.stencyl.com/pedia2/ch3/motion/image07.png)

> **Note:** Angle is in degrees (0 - 360). 0 degrees is right and sweeps clockwise. What would 90 degrees be?

 

#### Gently vs. Sharply
When using any force block, you are given the option to push an object either gently or sharply.

![](http://static.stencyl.com/pedia2/ch3/motion/image15.png)

Gently is basically like having a bumper - it applies the force over a longer time, while sharply applies it all at once, like a head-on crash!

The bottom line is that the two methods differ a lot, and **you should experiment and see what works for your game**. There's no correct answer.

> **Explained:** The difference goes into elementary physics. Recall the concept of an "impulse" and that may conjure up fond memories of crashing cars and bumpers. You learned that the "severity" of a collision depended on how "long" the collision took. This is why cars have bumpers, to lengthen the collision by spreading out the force's application over longer time.
 

## Velocity vs. Forces

#### Forces

Generally speaking, forces are the most natural way of moving objects. Everything "just works" like it does in real life. You don't need to be explicit about everything.

Examples: Wind, conveyor belts, platforms.

#### Velocity

Velocity is good if you need to maintain a certain speed or require more control over an object's motion.

Example: 4 way motion in an RPG

To sum it up, it's a tradeoff between having more control (and responsibilities) or less. There's no right answer. Just experiment and **see what works best for your game**.

 
## Direction (Angle)

The direction of an Actor is the angle it's facing. By default, actors have a direction of 0 degrees (facing right).

![](http://static.stencyl.com/pedia2/ch3/motion/image13.png)

> **Note:** Clockwise is positive. Counter-clockwise is negative.
 

#### How To: Setting the Direction
This block instantly sets the Actor's direction to the given amount in degrees. (under **Actor > Position**)

![](http://static.stencyl.com/pedia2/ch3/motion/image08.png)

The following 2 blocks instantly rotate the Actor clockwise and counter-clockwise respectively. (under **Actor > Position**)

![](http://static.stencyl.com/pedia2/ch3/motion/image09.png)


#### How To: Getting the Direction
Returns the direction, in degrees. (under **Actor > Position**)

![](http://static.stencyl.com/pedia2/ch3/motion/image10.png)


## Turning Speed (Angular Velocity)

Turning speed dictates how quickly an actor rotates.

The following 2 blocks (under **Actor > Motion**) set the turning speed and get it, respectively.

![](http://static.stencyl.com/pedia2/ch3/motion/image11.png)

> **Note:** Clockwise is positive. Counter-clockwise is negative.
 

## Twisting (Angular Force)

You can also rotate, or twist, an object with a given force using the “twist” block. This is **like twisting the cap off a jar**.

Much like the distinction between Velocity and Forces, the same kinds of differences between Turning Speed and Twisting apply here.

The following block twists an actor (under **Actor > Motion**). There's, curiously, no notion of gently/sharply here since Box2D does not provide it.

![](http://static.stencyl.com/pedia2/ch3/motion/image12.png)


## Summary

* An Actor can move in three ways: Set its position, Set its Velocity, Apply a Force to it.
* Setting an Actor’s position is like teleporting.
* Setting the velocity of an actor makes it move at a constant speed in a given direction.
* Forces push actors around. They're the most natural but the most difficult to get a constant/fixed result from.
* Direction, Turning Speed and Twisting are the angular equivalents to Position, Velocity and Force.
