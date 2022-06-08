## Contents

* Overview
* How To: Saving and Loading
* Where is Data Saved?
* Challenge: Checkpoints


## Overview - Saving uses Game Attributes

Saving progress is a fundamental part of most games. Our saving system uses a game's [Game Attributes](https://www.stencyl.com/help/viewArticle/158/) to save data. All you have to do is structure your game such that **anything you want to save is stored in Game Attributes**.

![Saving](https://static.stencyl.com/pedia2/ch5/saving/image01.png)

Similarly, **loading** a save file will **overwrite the running game's Game Attributes** and replace them with the values of those in the save file. For this reason, it's best to load a save file as early as possible.


## How To: Saving and Loading

#### Usage
Saving and Loading involve these two blocks. (found under **Game > Saving**)

![Saving Blocks](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-5/images/saving-1.png)

#### What happens when the save/load block is used?

1. The game attempts to save / load. This is quick (nearly instant), but the game will not progress until the save / load operation is complete or has failed.

2. When the save is complete (or has failed), the body (inside) of the block will run.

3. save succeeded / load succeeded will be true if saving/loading succeeded. Otherwise it will be false.

We talk more about how to handle failure next.

#### Handling Failures

Sometimes, a player will be unable to save due to [restrictive security settings](https://www.stencyl.com/help/viewArticle/48/) or other reasons.

If saving/loading fails, you can detect this and use the **save succeeded** and **load succeeded** blocks to react appropriately, such as showing an error message.

![Handling a failed save](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-5/images/saving-2.png)

To use them, just drag them out as pictured and use them as you see fit.

> **Warning:** Don't use the save/load succeeded blocks outside the scope of the save/load wrapper, or you'll run into a compile-time error.

#### When should loading happen?

There's no hard rule for this, but for most games, doing it early on in the game's first scene makes sense. Remember again that loading will overwrite the game's game attributes.

#### Common Question: Playing the game for the first time.

Suppose that the player is playing your game for the first time. How do you know this? You could create a game attribute called "first time" that is initially set to true. When you save the game, it's set to false, so that when the game is loaded up again, that flag will now always be false.


## Where is Save Data saved?

It depends on the platform.

#### Flash

Flash games use [Local Shared Objects](https://en.wikipedia.org/wiki/Local_shared_object). That is to say, it's stored by the browser indefinitely until cleared out.

#### iOS / Android / Desktop

Mobile games store save data directly on the device's file system but within the confines of the app's sandbox. This means that the data is "safe" and cannot be tampered with by any other apps.

This save data is not deleted until the game itself is deleted (and settings/data are explicitly told to be removed). 

> **Note:** At this time, it isn't possible to specify custom save locations or write out arbitrary data at runtime.


## Summary

* Saving is based on Game Attributes.
* Loading will overwrite all Game Attributes.
* Saving/Loading is an instant operation.


## Challenge: Checkpoints

Many games use a checkpoint system, a system in which reaching a certain part of the level will guarantee that, if a player dies, the player can continue from that checkpoint, rather than starting from the beginning.

Create a simple checkpoint system for your game, such that even if the player exits out of the game, (s)he'll automatically begin from the last checkpoint (s)he reached.
