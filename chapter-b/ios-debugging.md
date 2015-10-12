> **Call for Help:** This article is incomplete. Want to help us improve it? [Propose edits](https://www.github.com/Stencyl/stencylpedia/edit/master/chapter-b/ios-debugging.md) to this article.

## Contents

* Introduction
* Logs
* Game Won't Start
* Viewing Device Logs
* Understanding Crashes
* Debugging Tips
 

## Introduction

At some point during testing, your game may quit unexpectedly to the home screen, spew errors in the log or act in an unexpected way. It's rare for a game to run perfectly the first time you make it. Bugs and crashes are an inevitable part of the game development lifecycle. This guide exposes you to the various tools avilable for debugging your games.


## Logs

Your game's logs record much of what goes on while your game is running as well as any additional information you decide to add in.

Logs come in two forms - the ones that Stencyl / Haxe emits and the ones that the iOS device emits. In most cases, even in the event of a crash, the Stencyl / Haxe ones provide all the info you need.


#### Viewing the Logs
Turn on the Log Viewer by selecting **View > Log Viewer** from the main menu.

#### Adding Info to the Logs
To add information to the logs, use the **print block**, located under **Flow > Debug** in the palette.

![Print Block](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/Print.png)

This can be particularly useful when something goes wrong and you want to know the value of an attribute, for example.

 

## Game Won't Start

Before your game runs, it has to compile. Compiling means translating all the blocks and code for your game into a form that the computer or device understands.

Errors in your behaviors are generally caught by Stencyl, with the offending behaviors automatically opened up. Most of the time, you're able to figure out what's wrong. That's not what we're focusing on here.

#### Why it happens

What we're focusing on are the cases where your game gets stuck in the "Compiling..." state or abruptly tells you that the game could not be built. The first thing to realize is that your game isn't stuck. It hit an error that we couldn't detect for reasons like these.

* Errors with iOS certificates.
* Errors with signing an app.
* Haxe errors.
* Couldn't establish connection with device.

#### Best Practices

Although we try to scan and identify common errors, some inevitably slip through the cracks. Here's what you can do to stay informed during the process, so you aren't left waiting forever.

1. **Turn on the Log Viewer** before you run a game. (View > Log Viewer)

2. Run your game.

3. The Log Viewer **should continually spew out new lines**. It may slow down at times, but progress should be steady.

4. If it stops, scan the last page or so worth of lines for errors. 

5. If you locate an error, try to **understand what it means** and search on Google. This is most useful for iOS certificate errors where the solutions to such issues are well documented on Q&A sites such as StackOverflow. 

6. If you can't figure out what's going on, [export your logs](http://www.stencyl.com/help/view/generating-logs/) and ask a question on the forums.


## Viewing Device Logs

If you're testing your game on your iOS device, viewing the console logs for your device when it's running your app is useful to know. There are various ways to do this.

#### Method 1: Xcode

Xcode's Organizer (Window > Organizer) lets you browse your device's past logs.

**Pros:** Quick access<br />
**Cons:** Device must be connected to your computer.


#### Method 2: Use the Console App

This app displays your device's console logs. Useful if your game crashes, and you don't know why.

[Get the Console App](http://itunes.apple.com/us/app/console/id317676250?mt=8)

**Pros:** For quick checking while device is untethered (such as a friend's device)<br />
**Cons:** Hard to get the info off the device. E-mailing it to yourself is your best bet.


#### Method 3: Use iTunes

[Instructions](http://aplus.rs/apple/how-to-find-crash-logs-for-iphone-applications-on-mac-vista-and-xp/)

**Pros:** Better for generating bug reports or a more detailed look<br />
**Cons:** Device must be connected to your computer.


## Understanding Crashes

Crashes are errors in your game’s logic or the Stencyl engine that cause the game to suddenly quit. Many types of errors can cause crashes. The most common ones include the following:

* Referring to something that no longer exists, such as a dead actor.
* Doing something illegal, such as dividing by 0 or attempting to grab an element from a list that does not exist.
* Performing an operation on something that doesn’t support that operation.

Sometimes crashes are due to reasons beyond your control (and ours), but if you find that you made an edit and the game crashes, try to recall what you did, undo that change and see if the game runs.

> **Tip:** If you believe you are the cause of the crash (vs. a bug in the engine), run the game in Flash and see if you can get it to error out there. This is easier for you to debug because Flash crash logs are significantly easier to understand.

 
## Debugging Tips

Putting the elements discussed previously together, you can now debug your game when it crashes. Here’s a summary of what to do:

#### Step 1: Make the crash happen again (“repro,” short for “reproduce,” the problem)
This will cue you in on what actually caused the problem.

#### Step 2: Examine the game logs and stack trace in the Stencyl's Log Viewer (or Mac's Console)
See if you can recognize your behaviors. Is it something you can trace back to your game and fix?

#### Step 3: Tinker with your game to isolate the issue
If you can’t recognize the faulty behavior, disable suspicious behaviors, based on what you know causes the crash, until the game no longer crashes.

Once you’ve figure out the offending behavior(s), try to narrow it down to particular blocks, if possible. If you are unable to fix the issue, or if you think it’s a problem on our end, report it on the forums and include the following info.

1. Your logs
2. Exact steps taken to make your game produce the crash. If the crash happens randomly, let us know.
3. Generate a simple 1-scene test game that demonstrates the issue. This forces you to understand the issue, making a resolution a lot quicker and easier for everyone.
