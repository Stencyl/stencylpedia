> **Call for Help:** This article is incomplete. Want to help us improve it? [Propose edits](https://www.github.com/Stencyl/stencylpedia/edit/master/chapter-b/android-debugging.md) to this article.

## Contents

* Introduction
* Logs
* Game Won't Start
* Understanding Crashes
* Debugging Tips
 

## Introduction

It's rare for a game to run perfectly the first time you make it. Bugs and crashes are an inevitable part of the game development lifecycle. This guide exposes you to the various tools avilable for debugging your games.

## Logs

Your game's logs record much of what goes on while your game is running as well as any additional information you decide to add in. 

### Viewing the Logs
Turn on the Log Viewer by selecting **View > Log Viewer** from the main menu.

### Adding Info to the Logs
To add information to the logs, use the **print block**, located under **Flow > Debug** in the palette.

![Print Block](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/Print.png)

This can be particularly useful when something goes wrong and you want to know the value of an attribute, for example.

 

## Game Won't Start

Before your game runs, it has to compile. Compiling means translating all the blocks and code for your game into a form that the computer or device understands.

Errors in your behaviors are generally caught by Stencyl, with the offending behaviors automatically opened up. Most of the time, you're able to figure out what's wrong. That's not what we're focusing on here.

#### Why it happens

What we're focusing on are the cases where your game gets stuck in the "Compiling..." state seemingly forever. The first thing to realize is that your game isn't stuck. It hit an error that we couldn't detect for reasons like these.

* Errors with certificates.
* Errors with signing an app.
* Internal Haxe errors.
* Couldn't establish connection with device.

#### Best Practices

Although we try to scan and identify common errors, some inevitably slip through the cracks. Here's what you can do to stay informed during the process, so you aren't left waiting forever.

1. **Turn on the Log Viewer** before you run a game. (View > Log Viewer)

2. Run your game.

3. The Log Viewer **should continually spew out new lines**. It may slow down at times, but progress should be steady.

4. If it stops, scan the last page or so worth of lines for errors. 

5. If you locate an error, try to **understand what it means** and search on Google. This is most useful for certificate errors where the solutions to such issues are well documented on Q&A sites such as StackOverflow. 

6. If you can't figure out what's going on, export your logs and ask a question on the forums.

 

## Understanding Crashes

Crashes are errors in your game’s logic or the Stencyl engine that cause the game to suddenly quit. Many types of errors can cause crashes. The most common ones include the following:

* Referring to something that no longer exists, such as a dead actor.
* Doing something illegal, such as dividing by 0 or attempting to grab an element from a list that does not exist.
* Performing an operation on something that doesn’t support that operation.

The **Android Device Monitor** gives you visibility into the raw Android system logs. They can be daunting for an average user to go through, which is why they're filtered out by default. However, when your game crashes, they can be your main source of information.

> **Note:** This section tells you how to use the Android Device Monitor. The Debugging Tips section helps you reach the root cause of the crash.
 
#### How to Launch the Android Device Monitor
Select **Debug > Android > Launch Device Monitor** from the main menu.

#### How to Use It
The Android Device Monitor consists of 3 sections. The left section lets you pick what device to inspect. The center section provide advanced information geared towards programmers. The bottom section provides the raw logs. We'll mostly focus on the bottom section.

Android logs can appear complex and overwhelming at first. Here are a couple things to look out for.

* Anything starting with **I/trace** is a Stencyl-related log.
* Look out for any lines mentioning your **App ID** (the thing that usually looks like com.yoursite.gamename). These are relevant to your game.
* Crashes usually show up towards the end and are accompanied by the term **tombstone**, which refers a process that unexpectedly quit (crashed, ran out of memory, etc.).
 

## Debugging Tips

Putting the elements discussed previously together, here's what you can do debug your game when it crashes.

####Step 1: Make the crash happen again (“repro,” short for “reproduce,” the problem)
This will cue you in on what actually caused the problem.

####Step 2: Examine the game logs and Android Monitor logs for cues.
See if you can recognize your behavior names, which can sometimes be printed out in a stack trace (a "blame" list that traces all the steps leading to an error. Is it something you can trace back to your game and fix?

####Step 3: Tinker with your game to isolate the issue
If you can’t recognize the faulty behavior, disable suspicious behaviors, based on what you know causes the crash, until the game no longer crashes.

Once you’ve figure out the offending behavior(s), try to narrow it down to particular blocks, if possible. If you are unable to fix the issue, or if you think it’s a problem on our end, report it on the forums and include the following info.

1. Android Monitor logs.
2. Stencyl logs.
3. Exact steps taken to make your game produce the crash. If the crash happens randomly, let us know.
4. If possible, generate a simple 1-scene test game that demonstrates the issue. This forces you to understand the issue, making a resolution a lot quicker and easier for everyone.
