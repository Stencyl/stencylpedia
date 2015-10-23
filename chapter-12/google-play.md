## Contents

* Introduction
* Setup
  * Google Play Dashboard
  * Stencyl
* Leaderboards and Achievements
* Events, Quests and Rewards
* Troubleshooting
 

## Introduction

aaa

#### Supported Features

Feature | Supported?
--- | ---
Achievements | Yes
Leaderboards | Yes
Quests | Yes
Events | Yes 
Rewards | Yes
Saved Games | No
Multiplayer | No


## Setup

> **Note:** The [official documentation](https://developers.google.com/games/services/console/enabling) for Google Play Games is a good reference point if you're unsure about how the service works and what it offers.

#### Google Play Dashboard

aaa

#### Within Stencyl

- enable google play games
- google app ID
- fingerprints (?)

![stencyl-google-play-games-id](http://static.stencyl.com/pedia2/ch12/google-play-id.png)

#### Initialize the Service

- use the block
- no events at the moment - check if connection is initialized via boolean block


## Leaderboards and Achievements

Both Leaderboards and Achievements encourage light-hearted competition between players. **Leaderboards** are a place for all players to post their high scores while **achievements** increase your players' engagement by encouraging them to explore parts of the game or take on certain styles of play they may not have otherwise used.

#### Setup

Both Leaderboards and Achievements must be set up on the [Google Play Developer Console](https://play.google.com/apps/publish/). Read the following pages to learn about the setup process for these features.

* Setting up [Achievements](https://developers.google.com/games/services/common/concepts/achievements)
* Setting up [Leaderboards](https://developers.google.com/games/services/common/concepts/leaderboards)

#### Reporting Scores

Block | Description | Where to Find
--- | --- | ---
![stencyl-report-score](http://static.stencyl.com/pedia2/ch12/submit-score.png) | ID = Leaderboard ID<br/>Score must be a number | Game > Mobile

#### Reporting Achievements

Achievements can be designated as standard or incremental. An **incremental achievement** involves a player making gradual progress towards earning the achievement over a longer period of time. When creating an incremental achievement, you must define the total number of steps required to unlock it (this must be a number between 2 and 10,000). You can report the player's progress towards an incremental achievement using the **increase** achievement block.

Block | Description | Where to Find
--- | --- | ---
![stencyl-unlock-achievement](http://static.stencyl.com/pedia2/ch12/unlock-achievement.png)  | ID = Achievement ID | Game > Mobile
![stencyl-increase-achievement](http://static.stencyl.com/pedia2/ch12/increase-achievement.png)  | ID = Achievement ID<br/>Number must be less than the remaining number of steps required | Game > Mobile

#### Showing Leaderboards / Achievements

Block | Description | Where to Find
--- | --- | ---
![stencyl-show-leaderboard](http://static.stencyl.com/pedia2/ch12/show-leaderboard.png) | ID = Leaderboard ID | Game > Mobile
![stencyl-show-all](http://static.stencyl.com/pedia2/ch12/show-all.png) | Shows all achievements or leaderboards or quests | Game > Mobile


## Events, Quests and Rewards

Events are like **analytics**. They let you collect data from your players during a game, so that you can use this data as feedback to let you improve your game. For example, you can adjust the difficulty level of certain levels in your game that players are finding too hard to complete.

**Quests** build on top of events by letting you form time-restricted challenges based on event data. Quests are useful to letting you lure players back in your game, if used in conjunction with **Rewards**, an in-game benefit that is awarded upon completing a Quest.

#### Setup

Events, Quests and Rewards must be set up on the [Google Play Developer Console](https://play.google.com/apps/publish/). Read Google's guide on [Events and Quests](https://developers.google.com/games/services/common/concepts/quests) to learn h ow set these up.

#### Events

aaa

#### Rewards

aaa

#### Quests

aaa


## Troubleshooting

- fingerprints seem to be a hard area

- for issues with the features not working or showing up, please ask for help on the forums. we haven't gotten enough feedback on this feature yet to post anything here.
