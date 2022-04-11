Part of game development is creating logic that not only works, but is also optimized for fast, smooth gameplay that meets or exceeds the 60 frames per second mark. In Stencyl, there are many ways to improve your game's performance. Here are a few common suggestions.

 
## Contents

* Avoid Too Many Collisions
* Limit use of "Make [actor] Always Active"
* Limit number of on screen actors
* Avoid expensive per-step calculations
* Use Custom Drawing in moderation
* Avoid drawing over the same spot many times
 

## Avoid having too many collisions

Stencyl uses Box2D for its physics engine, and the more Stencyl makes use of Box2D, the more calculations it's performing in a given step. Since collisions means the physics engine is working, more collisions means potential slowdown.

![](https://static.stencyl.com/help/images/CollidingActorsPic.png)

To avoid this, make sure the actors that are capable of colliding have something to do with the gameplay you're going for.

For example, unless you want bullets in your game to act like actual bullets, you can safely change their physics settings so they don't make more than basic use of Box2D when they collide with actors.

You can change the physics settings on the **Physics > General** page for an Actor.

![](https://static.stencyl.com/help/images/PhysicsSettings.png)

 
## Limit the number of Actors that use Always Active / Simulate

Although it's often helpful for actors to function while off screen (which is what Always Active allows), consider when you really need to do this in your game and when you can avoid it. The more actors that are running all of their Behaviors off screen, the worse your game's performance will be.

 
## Limit the Number of Actors on Screen

This can be tough when you want a game with a lot going on, but if you do need a lot of actors on screen, consider using [Images](https://www.stencyl.com/help/view/image-api) instead for actors that are decorative or "effects-like" in nature. 

> [Images](https://www.stencyl.com/help/view/image-api) are a limited form of Actor that do not take part in the physics engine, so many more of them can exist on-screen.
 

## Avoid Expensive Calculations Every Step

In the **Always event** block, you need to be careful about the types of calculations you choose to run here. The Always event block executes logic every step, so running calculations that use a lot of processing power each step will slow down your game. 

Examples of calculations to avoid using in the Always event block include trigonometric calculations, random number generation, calculating the square root of a value, and those involving exponents. While you may not notice any slowdowns on faster systems, on mobile devices and weaker systems, these calculations can make a difference.

 
## Limit Use of Custom Drawing

The Drawing blocks under the Drawing category in Design Mode allow you to draw custom shapes on screen.

Using them takes up a lot of processing power, though, so take into consideration how many custom shapes you're drawing on screen at any given time. Consider pre-rendering your effects instead.


## Don't Draw Multiple Things in the Same Place

When you draw anything on screen, avoid drawing things on top of one another. Doing this wastes processing power since you're drawing over the same spot multiple times.

![](https://static.stencyl.com/help/images/CustomDrawing.png)
 

## Now it's your turn. Share your tips.

What have you found, in your experiences, boosts performance of your games when you're in a bind? Use the comments area below to share your stories.

