This is the solution to Chapter 4’s Challenge, where we walk you through each step.

[Return to the Chapter 4 Challenge](http://www.stencyl.com/help/viewArticle/165/)
 

## Download the Solution

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://static.stencyl.com/pedia2/ch4/challenge/Chapter4Solution.stencyl">Download</a>

To install the project, import it from the File menu (File > Import Game…). Requires Stencyl 3.4.0 or later.
 
 
## Contents

* Part 1: Creating Your Scenes
* Part 2: Adding Background Music
* Part 3: Making the Switch Scene Behavior
* Part 4: Making the Enemies Destroyed Behavior
* Part 5: Making the Door Trigger Behavior
* Part 6: Making the Switch and Open Door Behaviors
* Part 7: Bringing it All Together


## Part 1: Creating Your Scenes

You’ll need at least 5 Scenes (though you can make more if you want).

Create each of your Scenes but leave space in each for a “door” Actor that the player’s Hero will have to open.

Add enemies to each Scene as you see fit.

![stencyl-dungeon-scene-pic](http://static.stencyl.com/pedia2/ch4/challenge/image03.png)


## Part 2: Adding Background Music

Just add this Behavior to the first Scene. **Music to Play** is an Sound attribute.

![stencyl-design-mode-loop-music-behavior](http://static.stencyl.com/pedia2/ch4/challenge/image11.png)


## Part 3: Making the Switch Scene Behavior

![stencyl-design-mode-switch-scene-example](http://static.stencyl.com/pedia2/ch4/challenge/image07.png)

1) A **Region** acts as the trigger for this Behavior in each Scene. Note this is a one-way Scene transition - the player can’t go back to a previous Scene.

![stencyl-scene-designer-region-example](http://static.stencyl.com/pedia2/ch4/challenge/image14.png)

2) In this case, our “door” Actor looks just like the walls, to make each one look like a “secret exit.” If you mouse over it, the Scene Designer will highlight it.

![stencyl-dungeon-secret-wall-pic](http://static.stencyl.com/pedia2/ch4/challenge/image13.png)

> **Tip:** To perfectly position an Actor so it aligns with the grid of tiles, **hold down the Shift key**.


## Part 4: Making the 'Enemies Destroyed' Behavior

Starting with this Behavior, each one from here on out will act as a different way for the player to progress from Scene to Scene.

![stencyl-dungeon-scene-with-enemies](http://static.stencyl.com/pedia2/ch4/challenge/image12.png)

1) This is a Scene Behavior. It uses a simple technique to find out how many enemies are in a Scene and then sets that value as the number of enemies the player’s Hero must destroy to progress.

![stencyl-design-mode-get-enemies-destroyed-behavior](http://static.stencyl.com/pedia2/ch4/challenge/image02.png)

2) This Behavior uses 3 types of Events, When Created, Actor Created/Dies, and Attribute.


## Part 5: Making the Door Trigger Behavior

![stencyl-design-mode-door-trigger-behavior-example](http://static.stencyl.com/pedia2/ch4/challenge/image05.png)

This is another simple Behavior. It’s attached to the Actor Type we’re using as a switch. The Hero only has to step on it to open the door.

![stencyl-dungeon-switch-example](http://static.stencyl.com/pedia2/ch4/challenge/image15.png)

 
## Part 6: Making the Switch and Open Door Behaviors

This Behavior is attached to two switch Actors. The player has to maneuver the Hero onto each switch and press a key

![stencyl-dungeon-switch-one-pic](http://static.stencyl.com/pedia2/ch4/challenge/image10.png) ![stencyl-dungeon-switch-two-pic](http://static.stencyl.com/pedia2/ch4/challenge/image00.png)

![stencyl-design-mode-activate-switch-on-key-press](http://static.stencyl.com/pedia2/ch4/challenge/image08.png)

1) This Behavior is attached to an Actor that’s a sensor, which allows our Hero to walk on it.

2)  It works with another Behavior called Open Door, shown below.

![stencyl-design-mode-active-switch-counter-behavior](http://static.stencyl.com/pedia2/ch4/challenge/image17.png)

3) We used a Game Attribute to keep track of the total number of switches the player’s Hero has activated. Don’t forget to set the value for Switch Counter to the actual number of switches in your Scene!

4) Open Door is attached to the door actor.


## Part 7: Bringing it All Together

![stencyl-scene-list-pic](http://static.stencyl.com/pedia2/ch4/challenge/image06.png)

1) Your final Scene needs a Behavior that draws text on screen. Make sure you can easily swap out the font.

2) Only place your Hero Actor in the first Scene.

If you want a little more of a challenge, add a title screen and after the player reaches the final room, switch back to the title screen.


## On to Chapter 5

Now that you’ve learned more about Scenes and how they work, let’s move on to Chapter 5 and delve deeper into the features you'll need to create a complete game.

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/view/playing-sounds-and-music/">Continue to Chapter 5</a>
