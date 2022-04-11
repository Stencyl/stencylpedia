## Contents

* Introduction
* Tip #1 - Don't use too many layers.
* Tip #2 - Don't use too many actors.
* Tip #3 - Load in just the atlases you need.
* Tip #4 - Performance only matters on the actual device.
* Tip #5 - Watch your memory usage.
 

## Introduction

Performance is an important consideration for your game. Performance dictates how smoothly your game runs on an actual device. This directly affects a user's perception of your game.

You should always strive to hit 60 frames per second (FPS) with your game. A well-implemented game should hit 60 FPS on devices that are at least 2-3 years older than current flagships.

Although mobile devices are more powerful than in years past, they are still more sensitive to factors that affect performance than PCs are. For this reason, you need to monitor performance throughought your game's development, rather than just at the end.


## Tip #1 - Don't use too many layers.

Although mobile devices now have decent graphics chips, they can falter when drawing over the entire screen a few too many times.

To avoid this fate, **use fewer layers rather than more**. A good rule of thumb is to stick to **at most 5 layers** for your scenes. The fewer, the better.

Be mindful of the platform you're developing the game for and focus first and foremost on making the foundation of your game work (the "fun") before making it pretty. In the [words](https://lostgarden.home.blog/2007/10/15/lessons-about-failure/) of Shigeru Miyamoto, **find the fun**.

 

## Tip #2 -  Don't use too many actors. If you must have many objects, use [images]((https://www.stencyl.com/help/view/image-api)) instead.

Stencyl is based on Box2D, an industry standard physics engine, in order to provide easy, out-of-the-box collisions. The numerous calculations required to run it can be taxing, so it's best to use fewer actors rather than more. There's no hard number which is "bad" since this can vary widely depending on the device and the game.

If you must have many objects on-screen, consider using [Images](https://www.stencyl.com/help/view/image-api) in place of full actors. Images are quasi-actors that do not make use of the physics engine - this improves performance if you don't need them to register collisions.


## Tip #3 - Don't load in all atlases at once - use only what you need.

Stencyl stores its graphics inside **atlases**, which lets you control which graphics are loaded into memory.

**By default, Stencyl loads every atlas at the start of the game**. If you don't need all of those graphics right away, this can be wasteful since those graphics sit in memory, and high memory usage can degrade performance.

Instead, it's better to only load what you need. Read our [Atlases article](https://www.stencyl.com/help/view/mobile-atlases/) for more details.
 

## Tip #4 - Performance only matters on the actual device.

Although the iOS Simulator is an effective and efficient way to test your game, when testing for performance, **you should frequently test it on an actual device**.

Like its name suggests, the iOS Simulator is just a simulation of what happens in the game. Your computer is likely to provide significantly better performance than your device, so it will usually run the game faster than on the real thing.

The same principles apply to Android. You may own a flagship device, but you should test your games on older devices (that are least 2-3 years older) to ensure that they run smoothly.


## Tip #5 -  Watch your memory usage.

As described in our [Mobile Debugging article](https://www.stencyl.com/help/view/mobile-debugging-ios/), memory leaks can impact your game's performance over time. 

Although memory usage in itself does not affect performance, beyond a critical point, a device will see a huge dropoff in performance. This point can be reached if memory usage grows over time without dropping back down after switching scenes or removing actors.
