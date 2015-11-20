## Contents

* Overview
* Opting Out (Staying Active)
* Example: Simple Pause/Unpause


## Overview

Pausing is such a common feature that we decided to include it in the Stencyl engine itself.

We opted for a simple approach to pausing: 

* Pause everything by default.
* You tell us what should remain active.

This approach gives you full control, and at the same time, it minimizes the amount of work on your part.


#### How To: Pause

To pause and unpause the game, use these blocks under **Scene > Game Flow**.

![Pause Blocks](http://static.stencyl.com/pedia2/ch5/pausing/image00.png)

#### Details

What exactly is paused and what remains unpaused?

* All **When Updating** events for Actors will stop happening (unless opted out)
* All **Do Every** and **Do After** events for Actors events will stop happening
* All physics for Actors will be paused (unless opted out)
* All **When Updating** events for Scenes will continue to happen
* All **Drawing** events still happen (but paused actors will not animate)

#### Gotcha: Pause Buttons

When pausing using a pause button actor, do not forget to opt the pause button out of pausing. Otherwise, the button itself will be frozen and unable to receive click events.


## Opting Out an Actor (Staying Active)

Actors that opt out of pausing will remain active while the game is paused. To opt an Actor out, flip to its Physics > Advanced page. Select “No” for the **Can be Paused?** option.

![Physics Page](http://static.stencyl.com/pedia2/ch5/pausing/image01.png)


## Example: Simple Pause/Unpause

#### Event 1: Toggling the Pause State
This part toggles between paused and unpaused when you press the spacebar.

![Event 1](http://static.stencyl.com/pedia2/ch5/pausing/image02.png)

> Put this inside a scene behavior, or else it will stop working once the game is paused, leaving you stuck in the paused state.


#### Event 2: Tinting the Screen when Paused
This part darkens the screen a little when while the game’s paused by drawing a semi-transparent black rectangle on top of everything.

![Event 2](http://static.stencyl.com/pedia2/ch5/pausing/image03.png)

> As mentioned above, drawing events happen regardless of paused state.


## Summary

* Pausing affects all actors by default.
* Pausing stops updates to actors but does not affect scene behaviors/events.
* Opt actors out to keep them active.
 

## Challenge: Pause “Spell”

Who said that pausing had to be used just to pause the game? Let’s use pausing to create a Pause “Spell”, one that **causes all enemies in a scene to freeze temporarily**.

Create a game in which picking up a “timer” item will, for 30 seconds, cause all enemies to freeze up. Everything else will operate normally, including the player.
