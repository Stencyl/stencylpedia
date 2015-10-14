## Contents

* Introduction
* Accelerometer Values
* How to Use the Values
* Challenge: Low Pass Filter
 
 
## Introduction

Some developers use a device's accelerometer to create games a user can control by **tilting the device**. One famous example is a "labyrinth" game.

![Maze Game](http://static.stencyl.com/help/images/accel/image03.gif)


## Accelerometer Values

You can access accelerometer data through a trio of blocks under the **User Input > Mobile** category in the Design Mode Palette.

![Accel Blocks](http://static.stencyl.com/help/images/accel/image04.png)

> **Aside:** The "z" value is largely useless for 2D games. It would be triggered by laying the device flat and spinning it around.

#### Explanation

The values of each of these range **between -1.0 and 1.0 inclusive**. Those values represent how much the device is tilted in a given direction.

* An **x value of 1** would mean it's tilted **all the way to the right**. 
* An **x value of -1** would mean it’s tilted **all the way to the left**.

![Directions](http://static.stencyl.com/help/images/accel-1.png)

The values are **flipped for a landscape oriented game**. In other words, the values are always relative to portrait orientation and won't automatically adapt for a landscape game. See the example below for details.

#### Summary

<br/>

**Portrait Orientation**

Name | Description
--- | ---
X (Positive) | Right
X (Negative) | Left
Y (Positive) | Up
Y (Negative) | Down

**Landscape Orientation**

Name | Description
--- | ---
X (Positive) | Up
X (Negative) | Down
Y (Positive) | Left
Y (Negative) | Right

> **Warning:** Do not enable auto-rotation for a game that uses the accelerometer. This will cause the values to flip when the device's orientation changes and will create a confusing situation.


## How to Use the Values

To replicate a basic tilting motion for a landscape-oriented game, create a simple behavior as shown in the image below. You can adjust the value **-70** to another that suits your needs.

![example](http://static.stencyl.com/help/images/accel/image02.png)

#### Why are x and y flipped? Shouldn't it be the other way around?
As stated in the previous section, the x and y values are flipped for landscape-oriented games.

####Why is it -70 rather than 70?
If you input 70, the game will act the opposite of what you'd expect. 

> **Full Explanation:** As mentioned above, a positive y-accelerometer value indicates a left tilt. However, since this is opposite of how Stencyl works (right is positive, left is negative), that's why the negative sign has to be there.


## Challenge: Low Pass Filter

At times, you may find the accelerometer values to be overly **sensitive**, leading to **jerky** motion or motion where none is desired.

To combat this, add some logic to **throw out low, absolute values**, so that the device has to be tilted beyond some minimum theshold before responding.
