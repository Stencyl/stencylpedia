## Introduction

One of the most important ways to ensure fast, smooth game performance is by making sure you're using actors in your game efficiently. The following tips can help you do this.


## Don't create too many actors. Use Images instead.

Stencyl is based on Box2D, an industry standard physics engine that provides convincing collision detection out of the box. The numerous calculations required to run it can be taxing, so it's best to use fewer actors rather than more. There's no hard number which is "bad" since this can vary widely depending on the device and the game.

If you must have many objects on-screen, consider using [Images](https://www.stencyl.com/help/view/image-api) in place of full actors. 

Images are quasi-actors that do not make use of the physics engine - this improves performance if you don't need them to register collisions. Examples of such actors include decorations and special effects.


## Remove Actors when they're no longer needed

There are many times when you should remove an actor from your game because they are temporary in nature. Examples include bullets, temporary power ups, certain enemies, and more.

Generally speaking, if an actor is only encountered once by the player, it should be removed as soon as possible. The conditions for removal will differ from game to game. 

The following examples demonstrate a few common scenarios and pitfalls to watch out for.


#### Actor collides with another actor

<br/>

![Remove an actor](https://static.stencyl.com/help/images/KillOnCollision.png)

> **Warning:** If actor A collides with actor B, there are no guarantees about which collision event runs first (since two will be dispatched - one for actor A and one for actor B). Do not make assumptions about which one will run first.


#### Actor leaves the screen

<br/>

![Leaving Screen](https://static.stencyl.com/help/images/RemoveAfterLeavingScreen.png)

> **Explanation:** In this case, the boolean attribute called **Actor On Screen?** ensures that the actor isn't removed before it has a chance to appear on screen. You'd set **Actor On Screen?** to true once that actor appears on screen. Then, when the actor leaves the screen again, it will be killed.
 

## Now it's your turn. Share your tips.

What have you found, in your experiences, boosts performance of your games when you're in a bind? Use the comments area below to share your stories.
