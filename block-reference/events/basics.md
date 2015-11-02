# Events > Basics

***

### <a name="when-creating-event"></a> When Creating

![when-creating-event](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/0%20-%20Basics/init.png)

Happens just once -- when this behavior is first initialized. For an actor, this happens when the actor is created. For a scene, this happens when you enter the scene. 

> **Tip:** If some logic needs to run at the "beginning" of a scene but *after* the scene's actors and behaviors finishe initializing, use a `do after 0.01 seconds` block to accomplish this.

***

### <a name="when-drawing-event"></a> When Drawing

![when-drawing-event](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/0%20-%20Basics/draw.png)

All drawing code goes here. Happens once every frame. The number of frames per second (FPS) is variable, capped at 60 frames per second. 

***

### <a name="when-updatingevent"></a> When Updating

![when-updatingevent](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/0%20-%20Basics/step.png)

The "meat" of a behavior's logic goes here. Happens for every step of the game. A step takes 10 milliseconds, therefore there are 100 steps per second.

***

