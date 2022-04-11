Sound is a fundamental aspect of almost any game. This section covers the basics of importing music, playing it back and some interesting tidbits that may not be obvious.


## Contents

* Importing Sounds
* Example: Background Music
* Accepted Formats
* Music vs. Sound Effects
* Playing Sounds and Music
* Channels
* Known Issues
* Challenge: Zelda-Style Battle Music
* Challenge: Smooth Looping
 

## How to: Importing Sounds & Music

1. Import the clip into the Sound Editor by going to **File > Create New > Sound**.

2. Give it a name.

3. Click the following box to pick and import.

![Import Sound](https://static.stencyl.com/pedia2/ch4/sounds/image03.png)

> **Tip:** Alternatively, you can just drag and drop the sound in.


## Example: Looping Background Music

Looping "background" music takes just 1 block to do.

Make a Scene Behavior out of this, or stick this directly into the "Events" for a scene.

![Loop Music](https://static.stencyl.com/help/images/loopsound.png)

> **Exercise:** There's a flaw in this approach. Think about what happens when you re-enter this scene... That isn't desirable, is it?

Later in this article, we'll cover all the playback blocks available to you.


## Accepted Formats

Stencyl accepts MP3s and OGGs as follows. 

Platform | Accepted Format
--- | ---
Flash | MP3
HTML5 | MP3/OGG
Windows | OGG
Mac | OGG
Linux | OGG
iOS | OGG
Android | OGG

In short, we use OGG for every platform except for Flash, and HTML5 uses both sound types. If you're publishing your game to Flash and any of the other platforms, you'll need to import the sound in both formats. *(We recommend Audacity for exporting music. It's free.)*

#### MP3 Troubleshooting

If your game unexpectedly does not export your game to Flash, it's likely that sounds are the culprit. Ensure that your MP3s meet the following specifications.

* 44.1 KHz (versus 22 or 11)
* 16-bit
* Constant bitrate (versus VBR)
* No metadata

If you continue to experience issues with MP3s, post your issue to the [forums](https://community.stencyl.com/index.php/board,3.0.html) and generate [logs](https://www.stencyl.com/help/view/generating-logs/).

#### MP3s and Licensing

For Flash games, licensing is handled by Adobe (the creator of Flash), and as a game developer, you do not have to worry about licensing for your Flash game, even if it makes money.

For desktop and mobile games, we only work with OGG sounds, so the use of MP3s is irrelevant.


## Music vs. Sound Effects

![](https://static.stencyl.com/pedia2/ch4/sounds/image01.png)

Stencyl supports two kinds of sounds: **music** and **sound effects**.

**Music** is streamed (like viewing a YouTube video) since it's too large to fit into memory. This is best for background music. This incurs a small performance penalty on mobile devices.

**Sound Effects** are loaded into memory to reduce latency in playback. This is better for short clips that need to be played immediately but consumes memory, particularly on mobile devices.


## How to Play Sounds & Music

All sound-related blocks are conveniently located under the Sound category.

![](https://static.stencyl.com/pedia2/ch4/sounds/image00.png)

**Play** = Plays to the end once, then stops<br/>
**Loop** = Plays to the end and then repeats

Volume ranges between 0% and 100%, inclusive.<br/>
Panning ranges between -100% (left) and 100% (right), inclusive.

> **Note:** If you'd like to pause and resume a sound, skip down to the **Channels** section.

#### A Common Mistake: Looping Music

Looping music does not stop upon switching scenes. A common mistake, however, is to attach a "Background Music" behavior to every scene, causing the music to restart each time you enter a new "room" or "stack up."

How would you solve this? One approach is to create a blank scene prior to the first level which loops the music. Since this scene is not encountered again, the loop behavior runs just once.
 

## Channels

Suppose that you're playing Zelda. The regular tune plays, but then you approach an enemy, and the music switches over to the battle music. Once you defeat the enemy, the regular tune picks up where it left off.

**Channels** are a simple way to **refer back to a playback instance of sounds**, so that you can **control their volume and pause/resume them in the future**.

![Channels](https://static.stencyl.com/pedia2/ch4/sounds/image02.png)

Channels are **referred to by number**, starting at index 0, ending at index 31.

32 channels are available in total.

> **Note:** When you play a sound/music without specifying a channel, Stencyl picks the next available channel starting from 0. If none are available, nothing happens.


## Known Issues

On the Android target, playing sounds may be delayed by a quarter to half second on some devices. This is due to a bug in Android's sound APIs. As of late 2015, this bug still exists and affects all products that use this API.


## Summary

* Music = Streamed, Sound Effects = Loaded into Memory
* Channels let you control playback. They have little to do with the regular meaning of sound channels.
* Don't worry about MP3s - Adobe has you covered. On other platforms, we now use OGGs.
 

## Challenge: Zelda-style Battle Music

> Suppose that you're playing Zelda. The regular tune plays, but then you approach an enemy, and the music switches over to the battle music. Once you defeat the enemy, the regular tune picks up where it left off.

How would you build this sound system?

