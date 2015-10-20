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

![](http://static.stencyl.com/pedia2/ch4/text/test-size.png)

 
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


(Controls: Left/Right/Up to jump)
 

Download the Project

- Unzip and stick the project into your Games directory as "Text Demo"

- Don't know where your Games directory is? Click the "View Games Directory" button at the bottom of the Welcome Center (the first screen you see after opening Stencyl)


 

Goal: We want to draw the Timer shown in the demo.

- The timer counts up once per second.
- As you walk towards the right, the timer stays at the same spot on screen.

Walkthrough - Adding a Timer
 
1) Open the demo project. This project is mostly built up (run it!). All you need to do is create the Timer feature.

2) Open up the (only) Scene and flip to the Events tab.

3) Add a Number attribute called “Time” - and make it hidden.



4) Add a “Every N Seconds” event. Make it do the following.



What does this do? This increments the timer once per second. It also anchors the actor to the screen, as explained in the previous section.
5) Add a “When Drawing” event. Make it do the following.



What does this do? This draws the current time, based on the “time” attribute we created earlier.
6) That’s it! Run the game, and you should now notice it drawing the timer, just like in the demo above.

 

Mini-Challenges

1) Tweak the timer to increment twice a second.
2) Show the timer on the right side of the screen.
3) Show the timer in the center. Properly account for cases where the text may be shorter or longer.
 

## Dialog System

A much-requested ability to implement a full-fledged dialog system is currently being handled one of the key developers of Stencyl. While it's technically a separate effort, it's officially endorsed by us.

[Visit their site](http://dialogextension.com/) to learn more.

![](http://static.stencyl.com/pedia2/ch4/text/dialog.png)


## Summary

* Stencyl uses bitmap fonts to draw text to ensure good performance and consistent results.
* HUDs are graphical displays of information that display on top of everything else and do not obey the camera.


## Challenge: Dialog Box

While Stencyl is home to a powerful dialog system, for learning purposes, it's not a bad idea to implement one system on your own to check your mastery of text drawing.

![](http://static.stencyl.com/pedia2/ch4/text/dialog2.png)

Create a simple system for displaying dialog, in which you specify a List of text (1 sentence per entry) to display.

The dialog should display 1 sentence at a time, and the player has to hit a key to proceed.

> **Bonus:** Bonus points for auto-wrapping text and displaying a little blinking arrow to indicate to the player that the sentence is “finished” and the system is waiting for the player’s go to continue.
