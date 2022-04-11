## Contents

* Introduction
* Kongregate
* Newgrounds


## Introduction

Stencyl has partnered up with Kongregate and Newgrounds to bring you direct integration of each of these popular networks' APIs -- this brings **Ads, Leaderboards and Achievements** to your Flash games.

> **Note:** All of these blocks may be found under the Game > Flash section of the Palette.


## Kongregate

Kongregate is a popular gamer-oriented Flash portal. It's developer friendly and directed towards a more sophisticated hardcore audience than typical Flash portals.
 
#### Before you Start
The bulk of our support involves sending scores over to Kongregate's servers. To do this, you first need to set up high scores on Kongregate's end. [This page](http://developers.kongregate.com/docs/kongregate-apis/stats) tells you how to do this.
 
#### Setting Up
Before you use the Kongregate API, use this block to initialize it. It doesn't matter where or when this happens. Sticking it inside the first scene is best practice.

![Kong init](https://static.stencyl.com/pedia2/ch5/third/image14.png)

#### Submitting Scores
Unlike other services, Kongregate displays its scores as part of its site rather than in-game.

![Kong scores](https://static.stencyl.com/pedia2/ch5/third/image04.png)

To submit a score, use this block. You must [set up each field](http://developers.kongregate.com/docs/kongregate-apis/stats) you wish to record on Kongregate's site and adhere to its best practices.

![Kong score block](https://static.stencyl.com/pedia2/ch5/third/image05.png)

#### Player Info
With these blocks, you can test whether the player's registered, a guest and their user name, if they are registered.

![Kong player blocks](https://static.stencyl.com/pedia2/ch5/third/image12.png)

#### Achievements
The best games on Kongregate have achievements. These games are nominated by its staff. The minimum bar is a 3.5 rating (in practice, it's now 4+) and reaching at least several hundred thousand plays.

 
## Newgrounds

Newgrounds is a popular site for user-generated Flash content and games. They're also a great place to get a game sponsored.

#### Setup
Every Newgrounds game provides 2 secret values that you must set, so that Newgrounds' servers can communicate with your game. Set those values under the following page, located at **Settings > Web > Services**.

![Newgrounds setup](https://static.stencyl.com/pedia2/ch5/third/image08.png)

#### Showing an Ad
Ads can be shown at any point during the game, whether at the start or between levels.

![Newgrounds ad block](https://static.stencyl.com/pedia2/ch5/third/image15.png)

#### Leaderboards
Newgrounds supports scoreboards. In order to use them, you have to set the scoreboards up on their site before they can be tested.

![Newgrounds leaderboard](https://static.stencyl.com/pedia2/ch5/third/image16.png)

Once they are, you can opt to show the scoreboard, passing in the board's ID/name, which you defined on Newgrounds.

![Newgrounds show board block](https://static.stencyl.com/pedia2/ch5/third/image13.png)

Similarly, using that same board ID/name and passing in a value, you can submit a score to Newgrounds servers.

![Newgrounds submit score block](https://static.stencyl.com/pedia2/ch5/third/image18.png)

#### Medals
Medals are the Newgrounds term for achievements. Like scoreboards, medals must be set up on the Newgrounds site.

![medals](https://static.stencyl.com/pedia2/ch5/third/image11.png)

Two blocks can be used to work with medals. The move block is a one-time use block that you call at the start of the game (or anytime before a medal shows) to place the medal's popup at an appropriate place on screen.

![medals block](https://static.stencyl.com/pedia2/ch5/third/image06.png)

To unlock a medal (in other words, unlock the achievement), just use the unlock medal block.

![medals unlock block](https://static.stencyl.com/pedia2/ch5/third/image03.png)




## Summary

* Third party services let you increase your game's engagement and provide simple ways to monetize.
* Use services responsibly to complement a game.
