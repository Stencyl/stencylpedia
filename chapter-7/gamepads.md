## Contents

* Introduction
* Basic Usage
* User-Provided Controls
* Analog Controls
 

## Introduction

Stencyl supports external controllers (such as gamepads) for Windows, Mac and Linux games. Standard controllers are supported, including popular models such as the Xbox and Playstation controllers. 

> **Note:** Controllers are not yet supported on Flash, HTML5, iOS and Android.

 
## Basic Usage

#### Overview

* Use the "enable gamepad" block before doing anything.
* Discover the gamepad button names using a [gamepad event](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-event.png).
* Map buttons on your gamepad to Controls using the [map button block](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-mapping.png).
* If you want to support any kind of controller (not just presets), you'll need to let the user manually configure their controller. Skip down to the User Provided Controls section for a sample game.
 
#### How it Works
As you may recall from the [Controls](http://www.stencyl.com/help/view/controls/) article, Stencyl doesn't encourage you to work directly with input devices. 

In order to establish "controls" for a game, you set up Controls in the Game Settings editor and assign specific keys (such as up/down/left/right/Z/X) to those controls. That way, if you decide to change a control's key in the future, you only have to change that in one place, versus many.

<img alt="" src="http://static.stencyl.com/pedia2/ch3/controls/image05.png" style="width: 240px; height: 240px;">

It turns out that this setup makes gamepad support easier for you too. To support gamepads, you do the same thing - **bind a key on your controller to a control**.

![bind control block](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-map.png)

Sounds simple enough, but to do this, you need to know what the **names** of the buttons are. They differ from device to device.

#### How to Discover Button Names
If you would like to build a controller mapping, you'll first need to figure out what the **button ID's** are for the controls for your game.

To do this, use the **Gamepad event, located at Add Event > Input > Desktop-Only > Any Button**. Then, print out the input like so.

![](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-event.png)

Run a game with this behavior and take down the ID's (by pressing the button on your controller and observing the output in the Log Viewer).

For example, these are **some** of the IDs for an Xbox 360 controller. (We've added the names for your reference.)

Name | Button ID
--- | ---
X | 0,2
A | 0,0
B | 0,1
Y | 0,3
Left | 0,left hat
Right | 0,right hat
Up | 0,up dat
Down | 0,down hat

> **Aside:** The 0 that precedes each button ID corresponds to "controller 0" -- meaning that if multiple controllers are hooked up, this part can change depending on what's plugged in.


#### Build a Controller Map

To build a mapping, use the **map button** block to establish that. (All Gamepad blocks are located under **User Input > Gamepad**)

![](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-mapping.png)


#### Frequently Asked Questions

**What if a player wants to custom configure their controller?**<br/>
See the next section.

**Does Stencyl provide out-of-the-box support for common controllers like the XBox and PlayStation controllers?**<br/>
Not at this time. If you've come up with some, upload them and share a link. We'll include them in future updates to this article.

**What should I watch out for?**<br/>
* Unplugging and replugging a controller may generate unpredictable results. 
* Plugging in multiple controllers may generate unpredictable button names.
* It isn't easily possible to auto-detect a controller type because we can't get a controller's model name.
OpenFL is working on all of these issues, but the fixes are not available at the time of this writing. 


## User-Provided Controls

Players using a less common controller will need to manually configure their controller during the game. This typically involves running through each game control one by one, prompting them for a button press and then saving that out to a file.

We provide two blocks to assist with the saving/loading of configurations...

![](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-saveload.png)

*(Much like our save/load blocks, provide a filename in the lone blank. It doesn't really matter what you put in.)*

#### Sample Game
This sample project demonstrates how accomplish what we described above -- namely, getting the user configure each game's control by pressing a button on their controller. We leave it to you to customize the look to fit your game's needs.

[Download Project](https://github.com/Stencyl/stencylpedia/blob/master/chapter-7/Sample%20Game%20for%20Gamepad%20Configuration.stencyl?raw=true)

 
## Analog Controls

Analog Controls correspond to buttons on a controller that detect not just whether they are pressed down, but **how much they are pressed down**. This contrasts with Digital Controls, which can only detect whether they are down or not.

On most modern controllers, two kinds of buttons fall into this category.

* Control Sticks
* Shoulder (Trigger) Buttons

<img alt="" src="http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-analog.png" style="width: 250px; height: 298px;">

In the case of a control stick, the stick detects how far it's tilted, so that a character walks quicker when it's tilted fully, versus halfway. As for the shoulder button, pressing the button down harder will be registered differently from pressing it down softer.

Stencyl provides two blocks for working with analog controls.

#### Getting the Pressure (amount of tilt/press)
This block gets you the pressure (amount of tilt/press) for a given control as a value between 0 and 1, inclusive, where 0 means no tilt/press and 1 means full tilt/press.

![](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-pressure.png)

#### Setting the Sensitivity ("dead zone")
Have you ever played a game and found the character walking by himself despite you not touching the controller?

This setting lets you set the sensitivity ("dead zone") for an analog control, so that lesser amounts of pressing/tilting don't get interpreted as actions. The default value is 0.

Provide a value between 0-100, inclusive, where 0 means that any amount of tilt/press will be detected and 100 effectively disables the button. We advise setting it between 10-25 and for games where this is critical, allowing the user to configure it to their liking.

![](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-sensitivity.png)




 
