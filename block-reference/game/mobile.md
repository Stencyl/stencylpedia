# Game > Mobile

***

## Game Center (iOS-only)

### Start Game Center

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

Initializes the Game Center service. Use a Game Center event to know if initialization has succeeded.

```
gameCenterInitialize();
```

***

### Game Center is Started?

![started-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-enabled.png)

Returns `true` if Game Center is currently active.

```
gameCenterIsAuthenticated()
```

***

### [Name / ID] of Player

![name-id-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-id-name.png)

Returns the [Name / ID] of the current player.

```
gameCenterGetPlayerName()
gameCenterGetPlayerID()
```

***

### Submit Score

![submit-score-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-board-submit.png)

Submits a score to the given leaderboard (by leaderboard ID).

```
gameCenterSubmitScore([NUMBER], [TEXT]);
```

***

### Show Leaderboard

![show-leaderboard-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-board-show.png)

Shows the given leaderboard (by leaderboard ID).

```
gameCenterShowLeaderboard([TEXT]);
```

***

### Report Achievement

![report-achievement-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-achievement-submit.png)

Reports the completion status for an achievement (given an achievement ID). Number must be between [0 - 100] inclusive.

```
gameCenterSubmitAchievement([TEXT], [NUMBER]);
```

***

### Show All Achievements / Reset Achievements

![show-achievement-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-achievement-show-reset.png)

Shows a page containing all of the game's achievements. This block can also reset (erase) all of a game's achievements.

```
gameCenterShowAchievements();
gameCenterResetAchievements();
```

***

### Show Achievement Banner

![show-banner-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-achievement-banner.png)

Shows an achievement banner. Provide the title and text for this banner.

```
gameCenterShowBanner([TEXT], [TEXT]);
```

***

## Google Play Games (Android-only)

### Start Google Play Games

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-initialize.png)

aaa

```
initGooglePlayGames();
```

***

### Connection is Estalished?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-connection.png)

aaa

```
getGPGConnectionInfo(0) //established
getGPGConnectionInfo(1) //pending
getGPGConnectionInfo(2) //failed
getGPGConnectionInfo(3) //canceled
```

***

### Show Achievements

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-show.png)

aaa

```
showGPGAchievements();
```

***

### Show Leaderboard

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-show-leaderboard.png)

aaa

```
showGPGLeaderboard([TEXT]);
```

***

### Unlock Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-unlock-achievments.png)

aaa

```
unlockGPGAchievement([TEXT]);
```

***

### Make Progress Towards Incremental Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-increment-achievments.png)

aaa

```
incrementGPGAchievement([TEXT], [NUMBER]);
```

***

### Submit Score to Leaderboard

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-submit-score.png)

aaa

```
submitGPGScore([TEXT], [NUMBER]);
```

***

### Update Event

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-update-event.png)

aaa

```
updateGPGEvent([TEXT], [NUMBER]);
```

***

### Has Quest Completed?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-check-requests.png)

aaa

```
hasNewGPGQuestCompleted()
```

***

### Get Completed Quest List

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-completed-quests.png)

aaa

```
getCompletedGPGQuests()
```

***

### Get Reward for Quest

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-get-reward.png)

aaa

```
getGPGQuestReward("text")
```

***

## Ads

### [Show/Hide] Mobile Ad

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iad-show-hide.png)

aaa

```
showMobileAd();
hideMobileAd();
```

***

### Height of Ad

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iad-height.png)

aaa

```
(Engine.landscape ? 32 : 50)
```

***

## Purchases

### Request Info for Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-request-info.png)

aaa

```
purchasesRequestProductInfo([[TEXT]]);
```

***

### Player Can Make Purchases?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-loaded.png)

aaa

```
purchasesAreInitialized()
```

***

### [Buy/Use] Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-buy-use.png)

aaa

```
purchasesBuy([TEXT]);
```

***

### Free Unmanaged Purchases (Android)

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-free-unmanaged.png)

aaa

```
purchasesGoogleConsume([TEXT]);
```

***

### Purchased Product?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-purchased.png)

aaa

```
purchasesHasBought([TEXT])
```

***

### Get Product Quantity (for consumable)

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-get-quantity.png)

aaa

```
purchasesGetQuantity([TEXT])
```

***

### Restore Purchases

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-restore.png)

aaa

```
purchasesRestore();
```

***

### [Title/Price/Description] for Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-title-desc-price.png)

aaa

```
purchasesGetTitle([TEXT])
purchasesGetPrice([TEXT])
purchasesGetDescription([TEXT])
```

***

## Other

### Show Alert

![show-alert-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/show-alert.png)

Displays a native modal (blocking) dialog to the user. Provide the title and message.

```
showAlert([TEXT], [TEXT]);
```

***

### Set Icon Badge (iOS)

![set-badge-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/ios-badge-number.png)

iOS-only. Sets your app icon's badge number. For example, on an e-mail app, this would report the number of unread messages. For a game, perhaps the number of notifications / events that have happened in your game. 

```
setIconBadgeNumber([NUMBER]);
```

***
