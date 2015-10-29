# Game > Mobile

***

## Game Center

### Start Game Center

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterInitialize();
```

***

### Game Center is Started?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-enabled.png)

aaa

```
gameCenterIsAuthenticated()
```

***

### [Name / ID] of Player

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-id-name.png)

aaa

```
gameCenterGetPlayerName()
gameCenterGetPlayerID()
```

***

### Submit Score

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-board-submit.png)

aaa

```
gameCenterSubmitScore([NUMBER], [TEXT]);
```

***

### Show Leaderboard

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-board-show.png)

aaa

```
gameCenterShowLeaderboard([TEXT]);
```

***

### Report Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-achievement-submit.png)

aaa

```
gameCenterSubmitAchievement([TEXT], [NUMBER]);
```

***

### Show Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-achievement-show-reset.png)

aaa

```
gameCenterShowAchievements();
```

***

### Show Achievement Banner

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-achievement-banner.png)

aaa

```
gameCenterShowBanner([TEXT], [TEXT]);
```

***

## Google Play Games

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

aaa

```
showAlert([TEXT}, [TEXT]);
```

***

### Set Icon Badge (iOS)

![set-badge-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/ios-badge-number.png)

aaa

```
setIconBadgeNumber([NUMBER]);
```

***
