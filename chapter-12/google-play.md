## Contents

* Introduction
* Setup
  * Step 1: Google Play Developer Console
  * Step 2: Setup within Stencyl
  * Step 3: Initialize Google Play Games using blocks
* Leaderboards and Achievements
* Events, Quests and Rewards
* Troubleshooting
 

## Introduction

[Google Play Games Services](https://developers.google.com/games/services/) is Google's equivalent to Apple's Game Center. It is a service that provides leaderboards, achievements, analytics and other features that help you find and retain players for your games.


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

#### Step 1: Set the game up on Google Play

First, you must set up your game on the [Google Play Developer Console](https://play.google.com/apps/publish/), the Google equivalent to iTunes Connect. If you haven't registered for the Google Play Developer Console before, you will be prompted to do so.

Once you're in, we strongly recommend following the [official documentation](https://developers.google.com/games/services/console/enabling) to learn how to set up your game. You must complete all steps mentioned in Google's guide before continuing.

#### Step 2: Setup Within Stencyl

Once you've set up your game on the Google Play Developer Console, you're ready to set things up in Stencyl. All you have to do is navigate to **Settings > Mobile > Certificates (Android)** and do the following 2 things.

* Click on the **Enable Google Play Games** checkbox.
* Enter in your **Google Play Application ID**.

![stencyl-google-play-games-id](http://static.stencyl.com/pedia2/ch12/google-play-id.png)

> **Note:** The **Application ID is a 12-or-13-digit number** ([View Example](http://static.stencyl.com/pedia2/ch12/app-id.png)). It is NOT the Client ID.

#### Step 3: Initialize Google Play with blocks

Once you've entered in your Google Play App ID into Stencyl, you must initialize the service using the following block (under Game > Mobile). Use this block as early as possible - preferably in your game's first scene or loading sequence.

![stencyl-google-play-init](http://static.stencyl.com/pedia2/ch12/init-google-play.png)

After using this block, you'll want to know when the Google Play service has succeeded in connecting with your game or whether it has failed. The following block (under Game > Mobile) lets you check on this status.

![stencyl-google-play-events](http://static.stencyl.com/pedia2/ch12/google-play-events.png)

Unfortunately, no events exist at this time. What we recommend doing is checking for success or failure every few seconds, as shown in the following example.

![stencyl-google-play-example](http://static.stencyl.com/pedia2/ch12/google-play-example.png)


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

#### Consult the [Official Guide](https://developers.google.com/games/services/console/enabling)
Specifically, skip down to **Avoiding common setup problems**, which list out the most common reasons why Google Play Games will fail to work for your app.

- fingerprints seem to be a hard area

- for issues with the features not working or showing up, please ask for help on the forums. we haven't gotten enough feedback on this feature yet to post anything here.
