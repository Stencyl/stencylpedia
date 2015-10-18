## Contents

* What is Continuous Collision Detection (CCD)?
* How do you turn CCD on/off?
* When should I turn CCD on/off?
* How to turn CCD off globally
 

## What is Continuous Collision Detection?

The physics engine in Stencyl (Box2D) handles collisions between objects, which prevents your characters from walking through walls.

In some cases, however, **fast-moving actors, such as bullets or falling objects, can pass right through a wall or floor**. That's where CCD comes in.

In the physics engine, collisions are detected every step at the point where the object moves to. If the object moves into another object or a tile (as illustrated by the purple area in the image), then the physics engine pushes it back to where the collision happened initially.

![Successful-collision-detection](http://static.stencyl.com/help/images/ContCollisionDetect1.png)

You never actually see what happens in the middle image, but that is what is happening behind the scenes. On the other hand, if you have a ball that is moving really quickly towards a platform, then it's possible that the two objects never actually intersect and the engine doesn't detect the collision. When this happens, the ball will pass right through. This is called **tunnelling**.

![collision-detection-tunnelling-example](http://static.stencyl.com/help/images/ContCollisionDetect2.png)

The way physics engines generally solve this problem is to allow for what is called **Continuous Collision Detection (CCD)**.

What this means is that when an object moves during a step, it actually checks all the positions between where it started and where it ended up. If the engine detects any objects in this path, then the engine detects a collision. This is shown in the next image, where the purple area is the object's path.

![Continuous-collision-detection](http://static.stencyl.com/help/images/ContCollisionDetect3.png)

As you can imagine, checking that entire area is significantly more **processor intensive** than checking a single spot every step. Leaving it on if you really don't need it, especially with large numbers of objects, will slow your game down.


## Is CCD on by default in Stencyl?

As of Stencyl 3.3, CCD is **ON** by default. 
 

## How do I turn it off?

Two methods let you turn CCD on/off.

#### Method 1: Use the Actor Physics Setting

Located under the Physics > Advanced page for an Actor.

![stencyl-enable-continuous-collision-detection-button](http://static.stencyl.com/pedia2/ch5/ccd.png)

#### Method 2: Use the Block

The block's located under Actor > Properties > Misc.

![stencyl-design-mode-continous-collision-detection-block](http://static.stencyl.com/help/images/EnableCCD.png)


 
## When should I use it?

As mentioned above, enabling Continuous Collision Detection can strain a game's performance (particularly on mobile), so you should use it sparingly. **You should only enable it on fast-moving objects**, such as bullets or things that are falling.

If you see objects passing right through walls or floors, and you checked that their collision shapes are in order, then CCD is worth trying.

You can test whether enabling continuous collision detection is necessary by first slowing down your object and seeing whether it collides as you'd expect. **If it collides with walls when moving slowly, but not when moving quickly, then you need to enable it**.

 

## Is there a global flag for turning CCD off?

Add a code block with the code shown below to turn the entire system **OFF**. This can only be used to shut the entire CCD system off.

```
box2D.dynamics.B2World.m_continuousPhysics = false;
```


## Summary

* Continuous Collision Detection (CCD) prevents cases of small, fast-moving actors from traveling through thin walls.
* CCD impacts performance. Use only on the actors that need it.
 

## Challenge: Replicate the "tunneling" problem

Want to test your complete understanding of CCD?

**Create a game that replicates a scenario that requires CCD to solve**. Think about the conditions required for "tunneling" to happen.
