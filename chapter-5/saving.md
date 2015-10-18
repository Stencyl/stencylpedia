## Contents

* Overview
* How To: Saving and Loading
* Detecting Failure
* Where is Data Saved?
* Challenge: Checkpoints


## Overview - Saving uses Game Attributes

Saving progress is a fundamental part of most games. Our saving system uses a game’s [Game Attributes](http://www.stencyl.com/help/viewArticle/158/) to save data. All you have to do is structure your game such that **anything you want to save is stored in Game Attributes**.

![Saving](http://static.stencyl.com/pedia2/ch5/saving/image01.png)

Similarly, **loading** a save file will completely **overwrite the game's current Game Attributes** and replace them with the values of those in the save file.


## How To: Saving and Loading

#### Usage
Saving and Loading involve just use these two blocks. (found under **Game > Saving**)

![Saving Blocks](http://static.stencyl.com/pedia2/ch5/saving/image00.png)

#### What happens when the save/load block is used?

1. The game attempts to save / load. This is quick (nearly instant), but the game will not progress until the save / load operation is complete or has failed.

2. When the save is complete (or has failed), the body (inside) of the block will run.

3. save succeeded / load succeeded will be true if saving/loading succeeded. Otherwise it will be false.

We talk more about how to handle failure below.

#### When should loading happen?

It's up to you, but most like to do it in the game's first scene. Remember again that loading will overwrite the game's game attributes.

#### Common Question: Playing for the first time.

Suppose the player is playing your game for the first time. How do you know this? You could create a game attribute called "first time" that is initially set to true. When you save the game, it's always set to false.


## Detecting Failure

Occasionally, a player will be unable to save, usually due to [restrictive security settings](http://www.stencyl.com/help/viewArticle/48/).

If saving/loading fails, you can detect this and use the “save succeeded” and “load succeeded” blocks react appropriately, such as showing an error message.

![Failure](http://static.stencyl.com/pedia2/ch5/saving/image02.png)

To use them, just drag them out as pictured and use them within an if-block.

> **Warning:** Don't use the save/load succeeded blocks outside the scope of the save/load wrapper, or you'll run into a compile-time error.
 

## Where is Data Saved?

Flash games use [Local Shared Objects](http://en.wikipedia.org/wiki/Local_shared_object). That is to say, it's stored by the browser indefinitely until cleared out.

Mobile games store save data directly on the file system but within the confines of the app's sandbox. This data is not deleted until the game itself is deleted (and settings/data are explicitly told to be removed). At this time, it isn't possible to specify custom save locations or write out arbitrary data at runtime.

 

## Summary

* Saving is based on Game Attributes.
* Loading will overwrite all Game Attribtues.
* Saving/Loading is an instant operation.


## Challenge: Checkpoints

Many games use a checkpoint system, a system in which reaching a certain part of the level will guarantee that, if a player dies, the player can continue from that checkpoint, rather than starting from the beginning.

Create a simple checkpoint system for your game, such that even if the player exits out of the game, he’ll begin from the last checkpoint he reached.
