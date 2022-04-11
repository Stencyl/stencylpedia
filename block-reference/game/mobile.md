# Game > Mobile

***

## Game Center (iOS-only)

### <a name="gamecenter-init"></a> Start Game Center

![start game center](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-init.png)

Initializes the Game Center service. Use a Game Center event to know if initialization has succeeded.

```
gameCenterInitialize();
```

***

### <a name="gamecenter-enabled"></a> Game Center is Started?

![game center is started](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-enabled.png)

Returns `true` if Game Center is currently active.

```
gameCenterIsAuthenticated()
```

***

### <a name="gamecenter-id-name"></a> Name / ID of Player

![name of player](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-id-name.png)

Returns the [Name / ID] of the current player.

```
gameCenterGetPlayerName()
gameCenterGetPlayerID()
```

***

### <a name="gamecenter-board-submit"></a> Submit Score

![submit score number to with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-board-submit.png)

Submits a score to the given leaderboard (by leaderboard ID).

```
gameCenterSubmitScore([NUMBER], [TEXT]);
```

***

### <a name="gamecenter-board-show"></a> Show Leaderboard

![show leaderboard for text](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-board-show.png)

Shows the given leaderboard (by leaderboard ID).

```
gameCenterShowLeaderboard([TEXT]);
```

***

### <a name="gamecenter-achievement-submit"></a> Report Achievement

![report achievement text as number % complete](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-achievement-submit.png)

Reports the completion status for an achievement (given an achievement ID). Number must be between [0 - 100] inclusive.

```
gameCenterSubmitAchievement([TEXT], [NUMBER]);
```

***

### <a name="gamecenter-achievement-show-reset"></a> Show All Achievements / Reset Achievements

![show achievements](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-achievement-show-reset.png)

Shows a page containing all of the game's achievements. This block can also reset (erase) all of a game's achievements.

```
gameCenterShowAchievements();
gameCenterResetAchievements();
```

***

### <a name="gamecenter-achievement-banner"></a> Show Achievement Banner

![show banner with title text and message text](https://static.stencyl.com/pedia2/block-images/game/mobile/gamecenter-achievement-banner.png)

Shows an achievement banner. Provide the title and text for this banner.

```
gameCenterShowBanner([TEXT], [TEXT]);
```

***

## Google Play Games (Android-only)

### <a name="gpg-initialize"></a> Start Google Play Games

![initialize google play games](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-initialize.png)

Starts the Google Play Games service.

```
initGooglePlayGames();
stopGooglePlayGames();
```

***

### <a name="gpg-connection"></a> Connection is Estalished?

![connection is established](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-connection.png)

Returns `true` if Google Play Games is ready to use. Other status checks are available for pending (attempting to connect), failed (to connect) and canceled (by user).

```
getGPGConnectionInfo(0) //established
getGPGConnectionInfo(1) //pending
getGPGConnectionInfo(2) //failed
getGPGConnectionInfo(3) //canceled
```

***

### <a name="gpg-show"></a> Show Achievements / Leaderboards / Quests

![show achievements](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-show.png)

Shows a page containing every [achivement / leaderboard / quest] for your game.

```
showGPGAchievements();
showGPGLeaderboards();
showGPGQuests();
```

***

### <a name="gpg-show-leaderboard"></a> Show Leaderboard

![show leaderboard with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-show-leaderboard.png)

Shows the specified leaderboard (given a Leaderboard ID).

```
showGPGLeaderboard([TEXT]);
```

***

### <a name="gpg-unlock-achievments"></a> Unlock Achievement

![unlock achievement with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-unlock-achievments.png)

Unlocks the specified achievement (given an Achievement ID).

```
unlockGPGAchievement([TEXT]);
```

***

### <a name="gpg-increment-achievments"></a> Make Progress Towards Incremental Achievement

![increase achievement with id text by int](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-increment-achievments.png)

Updates the player's progress towards an incremental achievement (given an achievement ID). This will add to the existing amount.

```
incrementGPGAchievement([TEXT], [INT]);
```

***

### <a name="gpg-submit-score"></a> Submit Score to Leaderboard

![submit score int to leaderboard with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-submit-score.png)

Submits a score to the specified leaderboard (given a Leaderboard ID).

```
submitGPGScore([TEXT], [INT]);
```

***

### <a name="gpg-update-event"></a> Update Event

![update event with id text with value int](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-update-event.png)

Submits event data (given an Event ID) to Google. Event data is reportedi n batches, so there may be a slight delay in delivery.

```
updateGPGEvent([TEXT], [INT]);
```

***

### <a name="gpg-check-quests"></a> Has Quest Completed?

![has new quest completed](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-check-quests.png)

Returns `true` if a quest has been recently completed. Once this is called, this resets, so calling it again immediately will return `false`.

```
hasNewGPGQuestCompleted()
```

***

### <a name="gpg-completed-quests"></a> Get Completed Quest List

![completed quest list](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-completed-quests.png)

Returns a `list` of completed quests.

```
getCompletedGPGQuests()
```

***

### <a name="gpg-get-reward"></a> Get Reward for Quest

![reward for quest with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/gpg-get-reward.png)

Each quest that you define contains a reward value that you can use to offer items or other benefits to players in-game. This block (given a Quest ID) returns that value as text.

```
getGPGQuestReward([TEXT])
```

***

## Ads

### <a name="admob-initialize"></a> Initialize Admob

![initialize admob ads with app id text set banner position to bottom](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-initialize.png)

Initialize Admob banner and/or fullscreen ads. Use this block only once in your first scene.

Set banner position if you are using banners. If you are only using fullscreen ads, banner position can be ignored.

```
AdMob.init([TEXT], 0);
AdMob.init([TEXT], 1);
```

***

### <a name="admob-show-hide-banner"></a> Show / Hide Mobile Ad

![show admob banner ad](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-show-hide-banner.png)

Shows (or hides) a banner ad for your game. Placed at the top or bottom of the screen (this is set in Settings > Mobile > Monetization). Uses iAd on iOS, AdMob on Android.

```
AdMob.showBanner();
AdMob.hideBanner();
```

***

### <a name="admob-show-fullscreen"></a> Show Fullscreen Ad

![load admob fullscreen ad](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-show-fullscreen.png)

Load / show a fullscreen ad for your game. Uses iAd on iOS, AdMob on Android.

```
AdMob.loadInterstitial();
AdMob.showInterstitial();
```

***

### <a name="admob-reinit-banner"></a> Reinitialize AdMob banner

![reinitialize admob banner](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-reinit-banner.png)

Reinitialize the banner. This may help if a banner failed to load.

```
AdMob.onResize();
```

***

### <a name="admob-setbanner-position"></a> Move AdMob Banner

![move banner to bottom](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-setbanner-position.png)

Use this block to change the banner position at runtime.

```
AdMob.setBannerPosition(0);
AdMob.setBannerPosition(1);
```

***

### <a name="iad-height"></a> Height of Ad

![height of mobile ad](https://static.stencyl.com/pedia2/block-images/game/mobile/iad-height.png)

Returns the height of the banner ad, so you can reposition your game elements accordingly.

```
(Engine.landscape ? 32 : 50)
```

***

### <a name="admob-setPrivacyURL"></a> Set Privacy Policy URL

![set privacy policy url to text](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-setPrivacyURL.png)

Set your privacy policy URL that is used by the consent SDK.

This block is part of GDPR compliance in AdMob.

```
AdMob.setPrivacyURL([TEXT]);
```

***

### <a name="admob-showConsentForm"></a> Show Advertisement Consent Form

![show consent form check existing consent](https://static.stencyl.com/pedia2/block-images/game/mobile/admob-showConsentForm.png)

Show the consent form (will only appear to players in the EEA).

This block is part of GDPR compliance in AdMob.

```
AdMob.showConsentForm(true);
AdMob.showConsentForm(false);
```

***

## Purchases

### <a name="iap-request-info"></a> Request Info for Product

![request info for product with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-request-info.png)

In order to retrieve title/price/description information for a product, you must request that info from Google/Apple. This block sends in that request (given the Product ID). You can check for success using a Purchase event.

```
purchasesRequestProductInfo([[TEXT]]);
```

***

### <a name="iap-loaded"></a> Player Can Make Purchases?

![player can make purchases](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-loaded.png)

Returns `true` if the purchasing API is ready to use.

```
purchasesAreInitialized()
```

***

### <a name="iap-buy-use"></a> Buy / Use Product

![buy product with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-buy-use.png)

Buy (or use) a product (given a Product ID). This makes a request to do these actions - you must check for success or failure using a Purchase Event.

```
purchasesBuy([TEXT]);
purchasesUse([TEXT]);
```

***

### <a name="iap-free-unmanaged"></a> Free Unmanaged Purchases (Android)

![free unmanaged android purchase with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-free-unmanaged.png)

Unmanaged products on Android are now treated as managed consumable purchases. This block "frees" up those purchases, so they can be repurchased by players, without having to set up new entries for them.

```
purchasesGoogleConsume([TEXT]);
```

***

### <a name="iap-purchased"></a> Purchased Product?

![purchased product with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-purchased.png)

Returns `true` if the specified product (given a Product ID) has been bought by the player. For a consumable, returns `true` if the player currently owns 1 or more of that product.

```
purchasesHasBought([TEXT])
```

***

### <a name="iap-get-quantity"></a> Get Product Quantity (for Consumable)

![get product quantity for id text](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-get-quantity.png)

For a consumable product, will return the amount of the specified product (given a Product ID) that the player owns.

```
purchasesGetQuantity([TEXT])
```

***

### <a name="iap-validated"></a> Validate Receipt for Product

![ios validate receipt for product with id object with shared secret key text in production](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-validated.png)

Optional: Validate Receipt with Itunes before player gets items.

ID:'productID'<br/>
Shared Secret:'ITunesConnect->Your game->In-App Purchases->View Shared Secret' select Sandbox when testing

```
Purchases.validateReceipt([VALUE],[TEXT],true);
Purchases.validateReceipt([VALUE],[TEXT],false);
```

***

### <a name="iap-restore"></a> Restore Purchases

![restore purchases](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-restore.png)

Manually tell the Apple/Google to restore a player's purchases. This will emit Purchase Restored events that you will need to handle.

```
purchasesRestore();
```

***

### <a name="iap-title-desc-price"></a> Get Title / Price / Description for Product

![title for product with id text](https://static.stencyl.com/pedia2/block-images/game/mobile/iap-title-desc-price.png)

Returns the [title/price/description] of the specified product (given a Product ID). Must use the `request info for product` block before this information is available.

```
purchasesGetTitle([TEXT])
purchasesGetDescription([TEXT])
purchasesGetPrice([TEXT])
```

***

## Other

### <a name="show-alert"></a> Show Alert

![show alert with title text and message text](https://static.stencyl.com/pedia2/block-images/game/mobile/show-alert.png)

Displays a native modal (blocking) dialog to the user. Provide the title and message.

```
showAlert([TEXT], [TEXT]);
```

***

### <a name="ios-badge-number"></a> Set Icon Badge (iOS)

![set icon badge number to number](https://static.stencyl.com/pedia2/block-images/game/mobile/ios-badge-number.png)

iOS-only. Sets your app icon's badge number. For example, on an e-mail app, this would report the number of unread messages. For a game, perhaps the number of notifications / events that have happened in your game. 

```
setIconBadgeNumber([NUMBER]);
```

***
