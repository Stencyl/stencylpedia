## Contents

* Introduction
* Setup
  * Step 1: Set Up your Keystore 
  * Step 2: Google Play Developer Console
  * Step 3: Setup within Stencyl
  * Step 4: Initialize Google Play Games using blocks
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

#### Step 1: Set up your Keystore (if necessary)

Before doing anything, you must **set up your keystore** within Stencyl. Consult our [Publishing to Google Play](http://www.stencyl.com/help/view/google-play/) guide for details on this process.

> **Note:** If you already have a Keystore (made outside of Stencyl), you must still tell Stencyl about it. Read the [guide](http://www.stencyl.com/help/view/google-play/) for details.

#### Step 2: Set the game up on Google Play

First, you must set up your game on the [Google Play Developer Console](https://play.google.com/apps/publish/), the Google equivalent to iTunes Connect. If you haven't registered for the Google Play Developer Console before, you will be prompted to do so.

Once you're in, we strongly recommend following the [official documentation](https://developers.google.com/games/services/console/enabling) to learn how to set up your game. You must complete all steps mentioned in Google's guide before continuing.

> **Note 1:** When Google requests **SHA1 fingerprints** for your game (during the Client ID creation process), go to **Settings > Mobile > Certificates (Android)** and click View Fingerprints. Use the Release fingerprint for the Release Client ID and the Debug fingerprint for the Debug Client ID.

> **Note 2:** Don't forget to [add test accounts](https://developers.google.com/games/services/console/testpub) to the Testing section of the Google Play Developer Console, otherwise you will not be able to sign in to your game.


#### Step 3: Setup Within Stencyl

Once you've set up your game on the Google Play Developer Console, you're ready to set things up in Stencyl. All you have to do is navigate to **Settings > Mobile > Certificates (Android)** and do the following 2 things.

* Click on the **Enable Google Play Games** checkbox.
* Enter in your **Google Play Application ID**.

![stencyl-google-play-games-id](http://static.stencyl.com/pedia2/ch12/google-play-id.png)

> **Note:** The **Application ID is a 12-or-13-digit number** ([View Example](http://static.stencyl.com/pedia2/ch12/app-id.png)). It is NOT the Client ID.

#### Step 4: Initialize Google Play with blocks

Once you've entered in your Google Play App ID into Stencyl, you must initialize the service using the following block (under Game > Mobile). Use this block as early as possible - preferably in your game's first scene or loading sequence.

![stencyl-google-play-init](http://static.stencyl.com/pedia2/ch12/init-google-play.png)

After using this block, you'll want to know when the Google Play service has succeeded in connecting with your game or whether it has failed. The following block (under Game > Mobile) lets you check on this status.

![stencyl-google-play-events](http://static.stencyl.com/pedia2/ch12/google-play-events.png)

Unfortunately, no events exist at this time, so you must manually check for success/failure using this block. What we recommend doing is checking for success or failure every few seconds, as shown in the following example.

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

Events, Quests and Rewards must be set up on the [Google Play Developer Console](https://play.google.com/apps/publish/). Read Google's guide on [Events and Quests](https://developers.google.com/games/services/common/concepts/quests) to learn how to set these up.

#### Reporting Events (Analytics)

Once you have defined Events on the Google Play Developer Console, you can begin capturing and reporting these events in your game. Note that events are reported to Google's servers in batches, so there may be a delay in delivering them.

Block | Description | Where to Find
--- | --- | ---
![stencyl-report-event](http://static.stencyl.com/pedia2/ch12/update-event.png)  | ID = Event ID | Game > Mobile

#### Quests

Quests let you create in-game challenges for players to attempt to complete within a predefined time period.

Block | Description | Where to Find
--- | --- | ---
![stencyl-quest-completed](http://static.stencyl.com/pedia2/ch12/quest-completed.png)  | Checks if a new quest has been completed. | Game > Mobile
![stencyl-quest-list](http://static.stencyl.com/pedia2/ch12/quest-list.png)  | Reports back a **list** of completed quests. | Game > Mobile

#### Rewards

Each quest that you define contains a reward value that you can use to offer items or other benefits to players in-game. The reward amount can come back as a number or text - it's just a piece of data that you specified in the Developer Console, so you can do whatever you see fit with it.

Block | Description | Where to Find
--- | --- | ---
![stencyl-get-reward](http://static.stencyl.com/pedia2/ch12/get-reward.png)  | ID = Quest ID<br/>Reports back the reward amount. | Game > Mobile


## Troubleshooting

#### Consult the [Official Guide](https://developers.google.com/games/services/console/enabling)
Specifically, skip down to **Avoiding common setup problems**, which lists out the most common reasons why Google Play Games will fail to work for your app.

#### Does support Events (as in Stencyl Events) for Google Play Games?
Not at this time. We'd like to in the future.

#### Hitting other issues? Ask for help.
If you continue to experience issues after consulting the resources above, please ask for help on the forums ([customer area](http://community.stencyl.com/index.php/board,46.0.html) - [public area](http://community.stencyl.com/index.php/board,3.0.html)). This feature is still on the new side, so we haven't gotten enough feedback yet to build out our troubleshooting section.
