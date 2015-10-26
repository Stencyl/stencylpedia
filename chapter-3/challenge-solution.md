This is the solution to the Chapter 3 Challenge. We'll walk you through each step.

[Return to the Chapter 3 Challenge](http://www.stencyl.com/help/view/chapter-3-challenge/)
 

## Download the Solution

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://static.stencyl.com/pedia2/ch3/Chapter3Solution.stencyl">Download</a>

To install the project, either drag the file into the Stencyl window from the Welcome Center or import it from the File menu (File > Import Game…). Requires Stencyl 3.4.0 or later.

![breakout-screenshot](http://static.stencyl.com/pedia2/ch3/challenge/image02.png)


## Contents

* Part 1: Setting Collision Groups
* Part 2: Making the Two Way Movement Behavior
* Part 3: Keeping the Paddle On Screen
* Part 4: Creating the Destroy Block Behavior
* Part 5: Making the Launch Ball Behavior
* Part 6: Recycling the Ball Actors
* Part 7: Putting it All Together
 

## Part 1: Setting Collision Groups

1) To start, we need one new Collision Group, one for the Ball.

![](http://static.stencyl.com/pedia2/ch3/challenge/image08.png)

2) Next, we need to set our paddle Actor to the correct group. Which do you think it should belong to?

3) The group our Ball Actor belongs to should be easy to set.

4) Lastly, we want to ensure that our Ball Actor can collide with our paddle Actor when we set the Collision Groups for each of them.


## Part 2: Making the Two Way Movement Behavior

Let’s start with the Behavior used to control the paddle.

1) We want it to allow the player to move the paddle right or left at a set speed. We also want it to stop moving when the player isn’t pressing any keys. You’ll need to use blocks that control the Actor’s horizontal speed and ones to check which keys are pressed.

Here’s a snapshot of the solution.

![stencyl-design-mode-two-way-movement-behavior-example](http://static.stencyl.com/pedia2/ch3/challenge/image06.png)

> **Note:** We use **otherwise if** instead of a series of **if** blocks because doing so improves performance. When the game sees **otherwise if**, it only evaluates the boolean (the true/false condition) rather than the complete chunk of code, thereby reducing how much it has to process.

2) One thing to remember is that when the player is pressing the key to move the paddle left, its x-speed is set to the negative of the **Top Speed** value.

![2d-game-coordinates](http://static.stencyl.com/pedia2/ch3/challenge/image01.png)

Remember, as you move down the screen, the Y value gets larger, and as you move up, it gets smaller. As you move to the right, the X value gets larger, and as you move left, it gets smaller.

3) Next, the last part of the Behavior tells the game exactly what to do when the player isn’t pressing any keys.

4) The Attributes in the Behavior to make it easy to configure. Some obvious choices are **Top Speed** (of the ball), **Right Control**, and **Left Control**. Based on what they do, you should be able to figure out their types.


## Part 3: Keeping the Paddle On Screen

Normally, when two Actors collide, they push each other in opposite directions. In our game, though, the paddle shouldn’t move when the ball collides with it. We need to do two things. First, we need to change how our paddle Actor responds when it collides with other Actors.

1) Open up the paddle Actor, click the Physics tab, then under the **General** tab, set the **What Kind of Actor Type?** option to **Cannot be pushed**. Now the Actor won’t move when the ball hits it.

![stencyl-actor-physics-cannot-be-pushed](http://static.stencyl.com/pedia2/ch3/challenge/image05.png)

2) Although this setting keeps the ball from knocking the paddle off screen, our paddle Actor will now go right through tiles. We need a Behavior to fix this. The Behavior should check the position of the paddle Actor, and if it moves beyond certain boundaries, move it back into the correct bounds.

Here’s a screenshot one one that will do just that.

![stencyl-design-mode-restrict-movement-example](http://static.stencyl.com/pedia2/ch3/challenge/image03.png)

> **Note:** This Behavior “always” checks the position of the paddle relative to the walls of the Scene (the screen size is the same as the Scene size in our game). If we try to move the paddle Actor past those bounds, the Behavior adjusts the Actor’s position.

The screenshots below show how we figured out the boundary coordinates.

![restrict-movement-behavior-tile-coordinates-explanation](http://static.stencyl.com/pedia2/ch3/challenge/image10.png)

The coordinate above is as far left as we want our paddle Actor to move.

![stencyl-restrict-movement-tile-coordinates-example-right](http://static.stencyl.com/pedia2/ch3/challenge/image09.png)

The coordinate above is as far right as we want the paddle to move.


## Part 4: Creating the Destroy Block Behavior

Now that we’ve got the Paddle’s movement under control, we need to tell our game what happens to a block when a ball collides with it.

1) Let’s go over what we originally planned: When the ball hits the block, the block should flash, make a sound, and then vanish.

2) You also want to ensure this only happens when the ball collides with the paddle.

Here’s the Behavior that makes this happen.

![stencyl-design-mode-destroy-block-example](http://static.stencyl.com/pedia2/ch3/challenge/image00.png)

> **Note:** The only thing you might not expect is the do after block that delays the sound effect and the block’s destruction. We need that delay so the player can see the color change effect in action.


## Part 5: Making the Launch Ball Behavior

We have a paddle the player can move and blocks that break, but we need a Behavior to launch the ball from the paddle. Although we could make a Behavior that lets the player launch new balls as quickly as he or she can press a key, adding a short delay keeps the player from spamming the controls.

1) To start, you’ll need blocks that create our Ball Actor and one that sets it in motion.

Here’s a screenshot of the Behavior that does this.

![stencyl-design-mode-launch-ball-behavior-example](http://static.stencyl.com/pedia2/ch3/challenge/image04.png)

> **Note:** To be clear, although the **when created** block is shown in the image above, it’s actually in a separate Event in the Behavior.

2) The Behavior only allows the player to launch a new ball once per second. Notice the **Wait?** boolean the Behavior checks? The Launch Ball key only launches a new ball when **Wait?** is set to **false**.

3) In addition, to improve the game’s performance, we use **Recycled Actors**. Also, when creating our Recycled Actor, it’s important to create it at coordinates offset from the paddle Actor’s current position.


## Part 6: Recycling Our Ball Actors

Because we’re creating Recycled Actors, we need to use another Behavior called Recycle Self to recycle our Ball Actor.

1) This Behavior only involves two blocks. What condition should apply when the ball needs to be recycled? That should give you a hint as to which Event to use.

Here is a screenshot of the solution.

![stencyl-design-mode-recycle-actor-example](http://static.stencyl.com/pedia2/ch3/challenge/image07.png)

> **Note:** We want to recycle the ball when it’s off-screen, so we use an Actors Event that checks when our Ball Actor leaves the screen.


## Part 7: Putting it All Together

Now we’ve got all our the game assets we need, let’s put everything together.

1) Our paddle Actor Type needs 3 Behaviors. Out of the 3 we made, which are they?

2) Our Ball Actor Type only needs one Behavior. Same goes for our Brick.

3) Test our game!

![stencyl-breakout-screenshot-final](http://static.stencyl.com/pedia2/ch3/challenge/image11.png)

> **Note:** If something doesn’t work right, start with the Collision Groups. Make sure each Actor Type belong to the correct Group. From there, look over the Behaviors and compare the ones you made to those in the screenshots. Lastly, make sure each Actor Type has the correct Behavior(s).
 

## On to Chapter 4

Now that you’ve learned more about Actors and how they can use Behaviors, let’s move on to Chapter 4 and talk about Scenes.

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/view/scene-basics/">Continue to Chapter 4</a>
