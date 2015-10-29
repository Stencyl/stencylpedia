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

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterIsAuthenticated()
```

***

### [Name / ID] of Player

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterGetPlayerName()
gameCenterGetPlayerID()
```

***

### Submit Score

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterSubmitScore([NUMBER], [TEXT]);
```

***

### Show Leaderboard

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterShowLeaderboard([TEXT]);
```

***

### Report Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterSubmitAchievement([TEXT], [NUMBER]);
```

***

### Show Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterShowAchievements();
```

***

### Show Achievement Banner

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
gameCenterShowBanner([TEXT], [TEXT]);
```

***

## Google Play Games

### Start Google Play Games

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
initGooglePlayGames();
```

***

### Connection is Estalished?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
getGPGConnectionInfo(0) //established
getGPGConnectionInfo(1) //pending
getGPGConnectionInfo(2) //failed
getGPGConnectionInfo(3) //canceled
```

***

### Show Achievements

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
showGPGAchievements();
```

***

### Show Leaderboard

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
showGPGLeaderboard([TEXT]);
```

***

### Unlock Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
unlockGPGAchievement([TEXT]);
```

***

### Make Progress Towards Incremental Achievement

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
incrementGPGAchievement([TEXT], [NUMBER]);
```

***

### Submit Score to Leaderboard

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
submitGPGScore([TEXT], [NUMBER]);
```

***

### Update Event

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
updateGPGEvent([TEXT], [NUMBER]);
```

***

### Has Quest Completed?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
hasNewGPGQuestCompleted()
```

***

### Get Completed Quest List

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
getCompletedGPGQuests()
```

***

### Get Reward for Quest

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
getGPGQuestReward("text")
```

***

## Ads

### [Show/Hide] Mobile Ad

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
showMobileAd();
hideMobileAd();
```

***

### Height of Ad

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
(Engine.landscape ? 32 : 50)
```

***

## Purchases

### Request Info for Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
purchasesRequestProductInfo([[TEXT]]);
```

***

### Player Can Make Purchases?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

### [Buy/Use] Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

### Free Unmanaged Purchases (Android)

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

### Purchased Product?

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

### Get Product Quantity (for consumable)

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

### Restore Purchases

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

### [Title/Price/Description] for Product

![start-gamecenter-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/gamecenter-init.png)

aaa

```
aaa
```

***

## Other

### Show Alert

![show-alert-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/show-alert.png)

aaa

```
aaa
```

***

### Set Icon Badge (iOS)

![set-badge-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/2%20-%20Mobile/ios-badge-number.png)

aaa

```
aaa
```

***
