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

![start-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-initialize.png)

Starts the Google Play Games service.

```
initGooglePlayGames();
```

***

### Connection is Estalished?

![check-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-connection.png)

Returns `true` if Google Play Games is ready to use. Other status checks are available for pending (attempting to connect), failed (to connect) and canceled (by user).

```
getGPGConnectionInfo(0) //established
getGPGConnectionInfo(1) //pending
getGPGConnectionInfo(2) //failed
getGPGConnectionInfo(3) //canceled
```

***

### Show Achievements / Leaderboards / Quests

![achievements-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-show.png)

Shows a page containing every [achivement / leaderboard / quest] for your game.

```
showGPGAchievements();
showGPGLeaderboards();
showGPGQuests();
```

***

### Show Leaderboard

![leaderboard-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-show-leaderboard.png)

Shows the specified leaderboard (given a Leaderboard ID).

```
showGPGLeaderboard([TEXT]);
```

***

### Unlock Achievement

![unlock-achievement-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-unlock-achievments.png)

Unlocks the specified achievement (given an Achievement ID).

```
unlockGPGAchievement([TEXT]);
```

***

### Make Progress Towards Incremental Achievement

![increment-achievement-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-increment-achievments.png)

Updates the player's progress towards an incremental achievement (given an achievement ID). This will add to the existing amount.

```
incrementGPGAchievement([TEXT], [NUMBER]);
```

***

### Submit Score to Leaderboard

![score-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-submit-score.png)

Submits a score to the specified leaderboard (given a Leaderboard ID).

```
submitGPGScore([TEXT], [NUMBER]);
```

***

### Update Event

![event-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-update-event.png)

Submits event data (given an Event ID) to Google. Event data is reportedi n batches, so there may be a slight delay in delivery.

```
updateGPGEvent([TEXT], [NUMBER]);
```

***

### Has Quest Completed?

![quest-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-check-requests.png)

Returns `true` if a quest has been recently completed. Once this is called, this resets, so calling it again immediately will return `false`.

```
hasNewGPGQuestCompleted()
```

***

### Get Completed Quest List

![start-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-completed-quests.png)

Returns a `list` of completed quests.

```
getCompletedGPGQuests()
```

***

### Get Reward for Quest

![reward-googleplay-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gpg-get-reward.png)

Each quest that you define contains a reward value that you can use to offer items or other benefits to players in-game. This block (given a Quest ID) returns that value as text.

```
getGPGQuestReward([TEXT])
```

***

## Ads

### [Show/Hide] Mobile Ad

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iad-show-hide.png)

Shows (or hides) a banner ad for your game. Placed at the top or bottom of the screen (this is set in Settings > Mobile > Monetization). Uses iAd on iOS, AdMob on Android.

```
showMobileAd();
hideMobileAd();
```

***

### Height of Ad

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iad-height.png)

Returns the height of the banner ad, so you can reposition your game elements accordingly.

```
(Engine.landscape ? 32 : 50)
```

***

## Purchases

### Request Info for Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-request-info.png)

In order to retrieve title/price/description information for a product, you must request that info from Google/Apple. This block sends in that request (given the Product ID). You can check for success using a Purchase event.

```
purchasesRequestProductInfo([[TEXT]]);
```

***

### Player Can Make Purchases?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-loaded.png)

Returns `true` if the purchasing API is ready to use.

```
purchasesAreInitialized()
```

***

### [Buy/Use] Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-buy-use.png)

Buy (or use) a product (given a Product ID). This makes a request to do these actions - you must check for success or failure using a Purchase Event.

```
purchasesBuy([TEXT]);
```

***

### Free Unmanaged Purchases (Android)

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-free-unmanaged.png)

Unmanaged products on Android are now treated as managed consumable purchases. This block "frees" up those purchases, so they can be repurchased by players, without having to set up new entries for them.

```
purchasesGoogleConsume([TEXT]);
```

***

### Purchased Product?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-purchased.png)

Returns `true` if the specified product (given a Product ID) has been bought by the player. For a consumable, returns `true` if the player currently owns 1 or more of that product.

```
purchasesHasBought([TEXT])
```

***

### Get Product Quantity (for consumable)

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-get-quantity.png)

For a consumable product, will return the amount of the specified product (given a Product ID) that the player owns.

```
purchasesGetQuantity([TEXT])
```

***

### Restore Purchases

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-restore.png)

Manually tell the Apple/Google to restore a player's purchases. This will emit Purchase Restored events that you will need to handle.

```
purchasesRestore();
```

***

### [Title/Price/Description] for Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/iap-title-desc-price.png)

Returns the [title/price/description] of the specified product (given a Product ID). Must use the `request info for product` block before this information is available.

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
