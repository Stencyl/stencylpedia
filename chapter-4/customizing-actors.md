## Contents

* Introduction
* What is Actor Customization?
* You can refer to specific Actors/Regions inside a Scene
* Example: Pressing Switches


## Introduction

Sometimes, you want an actor to **act a little bit differently** from the norm. Suppose that we've created a basic enemy for a Mario-like game, like a Goomba.

Now, we want to make a Hopping Goomba - one that jumps.

You could do this by creating a brand new Actor Type, copying everything about the regular Goomba, and adding a Jump behavior. But a few too many times and you end up with this...

![](http://static.stencyl.com/pedia2/ch4/customize/image00.png)

Is there a better way to go about this? There is. It's called **Actor Customization**.


## What is Actor Customization?

Actor Customization is a feature that lets you tweak a specific instance of an Actor to behave differently.

#### How To: Customize an Actor

1. To customize an Actor, left-click on the actor. Then click the Inspector Pane tab on the right hand side of the screen.<br/><br/>![Inspector Tab](http://static.stencyl.com/help/images/Inspector-Tab-Pic.png)<br/>

2. From there, check "Customize" box.<br/><br/>![Customize Check Box](http://static.stencyl.com/help/images/Inspector-Customize-CheckBox.png)

From this point, you can start customizing the actor in a few ways.

* You can add Behaviors.
* You can remove Behaviors.
* You can customize the values of the behaviors it has.

#### How To: Add Behaviors
Click the + button in the Inspector to add a Behavior.

![Add Behavior Button](http://static.stencyl.com/help/images/Inspector-Add-Behavior-Button.png)

Doing so will bring up a dialog that lets you choose a Behavior to add, for example one that lets our Actor jump and run.

![Add Jump and Run Behavior](http://static.stencyl.com/help/images/Inspector-Add-Behavior.png)

#### How To: Remove Behaviors
You can also remove a Behavior (for this Actor instance) from the Inspector by clicking the X button.

![Delete Behavior](http://static.stencyl.com/help/images/Inspector-Delete-Behavior-Button.png)

#### How To: Customize Behaviors
Suppose that we want a particular Actor to walk really quickly. We could increase the "Minimum Speed" field for the "Wander" Behavior that's already attached to this actor.

![Walking Speed](http://static.stencyl.com/help/images/Inspector-Walking-Speed.png)

 
## You can refer to specific Actors and Regions within a scene.

Recall that an Actor's behaviors can't directly refer to specific objects within a scene. This is why, when you attach a Behavior to an Actor, and that behavior has an **Actor attribute**, you see this.

![](http://static.stencyl.com/pedia2/ch4/customize/image05.png)

Because an Actor's behaviors are generic, they have no connections to specific scenes. In other words, **there's no context for referring to things in specific scenes**.

Is there a way to enter values into these fields for Actors? There is! Once you customize an actor, those Actor attribute fields can now let you pick out specific Actors and Regions within a scene.

![](http://static.stencyl.com/pedia2/ch4/customize/image02.png)

I'll explain how to do this through a common example: pressing switches.

 

## Example: Pressing Switches

Suppose that you're playing an adventure game like Zelda. You're inside a dungeon, and you come across a room with several switches. Stepping on a switch causes a particular door to open.

[![](http://static.stencyl.com/pedia2/ch4/customize/image13.png)](http://static.stencyl.com/pedia2/ch4/customize/Switches.swf)
 
#### How can we use Actor Customization to make this work?

In short, we'll create a "Switch" behavior that, given a "Door" actor, will tell that Door actor to open up when our Hero steps on (collides with) the switch. (The switch should also visually change to a pressed-down state.)

![](http://static.stencyl.com/pedia2/ch4/customize/image07.png)

Through Actor Customization, we can customize **each instance of a switch**, so each one will **open up a particular door** when pressed.

#### Walkthrough

> **Note:** As always, these explanations are for learning purposes. You'll need to tweak the approach to fit your game's needs.

1. Download the [Customizing Actors](http://static.stencyl.com/pedia2/ch4/customize/Switches.stencyl) project. Import it using **File > Import Game...** and open it up.

2. Open the main scene.

3. Left-click the left switch (there are two switches total). Then, click the Inspector tab on the right. Click the **Customize** check box in the Inspector.

4. Notice that you now have full control over what behaviors are attached to this particular switch.<br/><br/>![Inspector Switch Behavior](http://static.stencyl.com/help/images/Inspector-Switch-Behavior.png)<br/>

5. Click on **Door Actor...** in the Inspector - this will prompt you to choose the actor that this switch is connected to. Choose the left door.<br/><br/>![Choose Door](http://static.stencyl.com/help/images/Inspector-Choose-Door-Pic.png)<br/>

6. Test the game. Step on the left switch. The left door will open.

7. Finally, configure the right switch to open the right door. Test again.

That's it!

#### Recap

You've customized the switches so that when the left/right switch is pressed, the left/right door opens.

How does this work? Let's take a peek into the "guts" of this sytem. Open up the **Switch Behavior** behavior.

![](http://static.stencyl.com/pedia2/ch4/customize/image11.png)

The key piece is the Actor attribute called **Door Actor**. When you customized the Switch actor (via the Inspector pane), the "Door Actor" attribute lets you pick a **SPECIFIC** door within the scene.

![](http://static.stencyl.com/pedia2/ch4/customize/image12.png)

If you understand that connection, you now fully understand how Actor Customization works.


## Summary

* Use Actor Customization to tweak the behavior of actors rather than creating brand new ones.
* Actor Customization lets you modify the attached set of behaviors and modify each behavior's values, for a particular instance of an Actor within a scene.
* You can refer to specific Actors and Regions within a scene through Actor Customization.
