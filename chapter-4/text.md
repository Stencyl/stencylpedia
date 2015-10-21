## Contents

* Introduction
* Fonts
* Creating Fonts
* Drawing Text
* HUDs
* Example: Drawing the Score
* Dialog System
 

## Introduction

Text is an essential element of most games. Text conveys information to the player in real-time. This article will teach you how to draw text to the screen and how to style it.
 

## Fonts

Fonts are a term used to describe the styling of text. Stencyl uses bitmap fonts to display text. Bitmap fonts are a special kind of font in which the font is pre-rendered to pixels.

![](http://static.stencyl.com/pedia2/ch4/text/image03.jpg)

**Pros**
* They look **consistent** regardless of device or hardware.
* They draw quickly.
* Because they're pixel based, they can take on many more shapes and forms than traditional vector-based fonts.

**Cons**
* You can’t grow them at runtime without ruining quality. (You have to create a new font for them)
* They sometimes take up more disk space.
 

## Creating Fonts

To create a font, use our [Font Editor](http://www.stencyl.com/help/view/font-editor/). You can create a new font by heading to **File > Create New > Font**.

This will bring up the Font Editor. Our Font Editor lets you style fonts based on both TrueType (TTF) font faces as well as images / sprite sheets.

If you'd like to learn more about creating fonts, read our [Font Editor](http://www.stencyl.com/help/view/font-editor/) article.


## Drawing Text

Once your game has a font, the easiest way to draw text is to draw it directly via the “when drawing” event. All text drawing blocks are found under Drawing > Drawing and Drawing > Styles.

#### Step 1: Set a Font

Never attempt to draw text without first telling the engine what font to use. If you fail to do this, the game may crash.

#### Step 2: Draw the text

Now, draw the text. Pass in the text and the (x,y) coordinates where you want it to draw. 

![](http://static.stencyl.com/pedia2/ch4/text/image10.png)

#### Extra Blocks

If you need to position the text more precisely or make calculations based on the text's size, we provide a few blocks to help you out under Drawing > Styles.

![](http://static.stencyl.com/pedia2/ch4/text/text-size.png)

 
##HUDs (Heads Up Displays)

A HUD (heads up display) is a transparent, graphical dashboard that displays on top of everything else.

![](http://static.stencyl.com/pedia2/ch4/text/image05.png)

**HUDs usually display statistics**. Think of them as the dashboard on your car, the one that displays how fast your car is going, how much gas you have left, your engine's temperature, etc.

![](http://static.stencyl.com/pedia2/ch4/text/image09.png)

#### HUDs do not follow the camera

One aspect of HUDs that’s unique is that they **don’t follow the camera**. They always draw at the same place on screen, regardless of where you are. Think of them as being this piece of glass that's on top of the game but not part of the game itself.

#### How to make an Actor "disobey" the camera

Have you seen this block? (under Actor > Drawing)

![](http://static.stencyl.com/pedia2/ch4/text/image07.png)

The ability to anchor an actor to the screen was made specifically for creating HUDs. As the name suggests, anchoring an actor makes the actor ignore the camera, so it **always is drawn at the same place on screen**.

**HUDs aren’t a part of Stencyl or a specific feature**. They’re just a common aspect of most games that they deserved special mention and to establish how to make them using the anchor block.
 

## Example: Drawing a Timer

In this example, we’ll talk about how to do something common: drawing a timer.

<a href="http://static.stencyl.com/pedia2/ch4/text/Demo.swf">![](http://static.stencyl.com/pedia2/ch4/text/image11.png)</a>

> **Controls:** Left/Right to move, Up to jump

#### Objectives

We want to draw the Timer shown in the demo.

* The timer counts up once per second.
* No matter where you are in the level, the timer stays at the same spot on screen.

#### Walkthrough (Part 1) - Adding a Timer
 
1. Download [this project](http://static.stencyl.com/pedia2/ch4/text/Test Demo.stencyl). (Use File > Import... to import it)
 
2. Open the demo project. This project is mostly built up (run it!). All you need to do is create the Timer feature.

3. Open up the Timer actor and flip to its **Events** tab.

4. Add a Number attribute called **Time** - and make it hidden.

5. Add an **Every N Seconds** event. Make it increment the Time attribute by 1.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/text/image08.png)<br/>

6. Add a **When Drawing** event. Make it draw the time, like this.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/text/image02.png)<br/>

7. That’s it (or is it?). Run the game, and you should now notice it drawing the timer, just like in the demo above.

#### Walkthrough (Part 2) - Fix the Bug

Wait, something's wrong. If you walk to the right, as the screen scrolls, the timer gets left behind. That's not right. Given what you've learned about making a HUD (heads up display), what do you need to do?
 
**Fix up the actor's behavior**, so it "sticks" to the screen. 

Stuck? Here's a [hint](http://static.stencyl.com/pedia2/ch4/text/image07.png).


#### Mini-Challenges

1. Tweak the timer to increment twice a second.
2. Show the timer on the right side of the screen. Don't hardcode the value - use blocks to calculate this, so it works no matter what the screen size is.
3. Show the timer in the center. Properly account for cases where the text may be shorter or longer.
 

## Dialog System

One of Stencyl's developers has independently created a fully-fledged dialog system. While it's technically a separate effort, it's officially endorsed by us.

[Visit their site](http://dialogextension.com/) to learn more.

![](http://static.stencyl.com/pedia2/ch4/text/dialog.png)


## Summary

* Stencyl uses bitmap fonts to draw text to ensure good performance and consistent results.
* HUDs are graphical displays of information that display on top of everything else and do not obey the camera.


## Challenge: Dialog Box

While Stencyl is home to a [powerful dialog system](http://dialogextension.com/), for learning purposes, it's not a bad idea to implement one system on your own to check your mastery of text drawing.

![](http://static.stencyl.com/pedia2/ch4/text/dialog2.png)

Create a simple system for displaying dialog, in which you specify a List of text (1 sentence per entry) to display.

The dialog should display 1 sentence at a time, and the player has to hit a key to proceed.

> **Bonus:** Bonus points for auto-wrapping text and displaying a little blinking arrow to indicate to the player that the sentence is “finished” and the system is waiting for the player’s go to continue.
