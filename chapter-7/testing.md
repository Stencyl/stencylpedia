## Contents

* Testing your Game
* Testing Standalone Games (Windows, Mac, Linux)
* Testing on Mobile Devices (iOS, Android)
* Printing to the Console
* Debug Draw
* FPS Monitor
* Compile Errors
* Runtime Errors
* Tips
 

## Testing your Game

Pick the Platform and press the Test Game button.

![Flash Player](https://static.stencyl.com/help/images/Flash-Player-Option.png) ![Option Button](https://static.stencyl.com/pedia2/ch6/testing/image00.png)

You can also do this from the **Run** menu.

![Run Menu](https://static.stencyl.com/help/images/Testing1.png)

> Prefer keyboard shortuts? Type Ctrl + Enter (or Command + Enter on Mac) to test your game.


## Testing Standalone Games (Windows, Mac, Linux)

[See this article](https://www.stencyl.com/help/view/publishing-standalone-game/) for the steps required to get standalone games running.


## Testing on Mobile Devices

[Setting up for iOS](https://www.stencyl.com/help/view/ios-getting-started)

[Setting up for Android](https://www.stencyl.com/help/view/setup-android)

 
## Print to the Console

It's often useful to record things that happen in a game during testing in a way that can be easily seen. For example...

* Telling whether a piece of logic "happened", especially if you suspect that that logic is not being reached
* Telling what the value of an attribute is. It may be different from what you think!

One quick and easy way to do this is to print these values to the console. Think of the console as a temporary text file that you can write out text to and view from Stencyl's Log Viewer.

> If you prefer to see the console inside the game (as was the case before Stencyl 3), [use this extension](https://community.stencyl.com/index.php/topic,35554.0.html).

#### How to Print to the Console

Use this block. (under Flow > Debug)

![Print Block](https://static.stencyl.com/pedia2/ch6/testing/image01.png)


## Debug Draw

Debug drawing is a special mode in which collision shapes are drawn as outlines. This can help you debug physics-related problems.

![Debug Draw](https://static.stencyl.com/pedia2/ch6/testing/image05.png)

Debug drawing is toggled from the **Run > Enable Debug Drawing** menu item.

 
## FPS Monitor

The FPS Monitor reports the framerate and memory usage for your game in the top-right corner. It can be toggled from the Run > Enable FPS Monitor menu item.

*It's normal for a game to see small but continual memory increases even if nothing is happening.* After a while (30 - 60 seconds), the memory usage will suddenly drop back to a baseline level. This is known as **garbage collection**, which refers to the act of ditching memory that an app no longer has use for.

> **Summary:** Don't obsess over this point. Memory usage isn't a problem unless it continually grows without ever dropping and is accompanied by a choppy framerate.
 

## Compiler Errors (can't run game)

Ever seen this window? This is a Compiler Error, which is an error that happens when we're unable to build your game into a Flash SWF for testing or exporting.

![Error](https://static.stencyl.com/pedia2/ch6/testing/image08.png)

In most cases, if you hit OK, we'll open the offending behavior and highlight the blocks that are at fault.

![Error Cause](https://static.stencyl.com/pedia2/ch6/testing/image09.png)

In this case, we've used the "actor inside region" block outside its context. It has to be used inside its wrapper (something that seems obvious but can easily happen if you're not careful).

![Solution](https://static.stencyl.com/pedia2/ch6/testing/image10.png)

(Correct usage)
 

#### What are the common causes of compiler errors?

* Using blocks outside their intended contexts, like what happened above.
* Something changed on our end, and it broke your game.


#### What can I do about them if I'm stuck?

* Drag out the offending blocks and see if the error goes away. Divide and conquer works well in isolating the issue.
* Once you've figured out WHERE the problem is, try to understand the problem. What is the error message trying to say?
* If you're stuck, ask for help on the [forums](https://community.stencyl.com/index.php/board,3.0.html). Describe your problem, take screenshots and attach your [logs](https://www.stencyl.com/help/view/generating-logs/).
 

## Runtime Errors (game crashes)

Runtime Errors are errors that happen while the game is running. They frequently lead to "freezing" or "crashing" of the game. If your game is freezing up, check what shows up in the Log Viewer (View > Log Viewer if it isn't open). You might see this kind of text.

![Flash Error](https://static.stencyl.com/pedia2/ch6/testing/image11.png)

> **Note:** Stencyl 3.0 and later, Flash itself will display a popup with an error of its own with similar information.

Fortunately for you, a runtime error usually tells you what's going on. The first line usually tells you where the error happened. You often see line numbers (line 57), which can point you roughly towards the offending line.

![Flash Error](https://static.stencyl.com/pedia2/ch6/testing/image12.png)

#### What causes runtime errors?

By far, the most common cause is **referring to an actor after it's been killed**.

> If you're stuck, ask for help on the [forums](https://community.stencyl.com/index.php/board,3.0.html). Describe your problem, take screenshots and attach your [logs](https://www.stencyl.com/help/view/generating-logs/).

 
## Tips

1. Come up with a testing workflow that you feel comfortable with. **Don't blindly guess what's wrong**. Stick to the facts and verify your assumptions by **printing to the console**.

2. **Is your game running slowly?** Read [this](https://www.stencyl.com/help/view/optimize-game-performance/) and [this](https://www.stencyl.com/help/view/optimize-actor-performance/) to diagnose the causes and come up with solutions.

3. **It can tempting to "reinstall" the software to fix problems**. In reality, this not only wastes time, but it can also **cause more problems** in the long run. Although there are circumstances where a reinstall is required, avoid the temptation and only switch to it as a last resort.

 
## Summary

* Use print blocks to print to the console.
* Use the FPS Monitor to measure memory usage.
* Debug drawing can be useful for debugging physics.
* Develop a testing workflow that works for you.
