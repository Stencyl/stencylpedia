# Game > Flash

***

> For a walkthrough of how to integrate Kongregate and Newgrounds into your game, read [our article](http://www.stencyl.com/help/view/kongregate-mochi-newgrounds/) on Stencylpedia.

***

## Kongregate

### <a name="kong-init"></a> Start Kongregate API

![kong-init-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/kong-init.png)

Starts up the Kongregate API. Must be used before doing anything with the API.

```
kongregateInitAPI();
```

***

### <a name="kong-submit"></a> Submit Score

![kong-init-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/kong-submit.png)

Submit a [score](http://developers.kongregate.com/docs/kongregate-apis/stats) to Kongregate. First field is the name of the statistic. Second field is the value of it (a number).

```
kongregateSubmitStat([TEXT], [NUMBER]);
```

***

### <a name="kong-guest"></a> Is a Guest? (vs. logged in)

![kong-init-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/kong-guest.png)

Returns `true` if a guest is playing your game on Kongregate.

```
kongregateIsGuest()
```

***

### <a name="kong-name"></a> Name of Player

![kong-init-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/kong-name.png)

Returns the username of the player who is playing your game on Kongregate, if one is logged in. If it's a guest, the name will be `Guest`.

```
kongregateGetUsername()
```

***

### <a name="kong-userid"></a> User ID of Player

![kong-init-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/kong-userid.png)

Returns the user ID of the player who is playing your game on Kongregate, if one is logged in. If it's a guest, this will come back as blank.

```
kongregateGetUserID()
```

***

## Newgrounds

### <a name="newgrounds-ad-show"></a> Show Ad

![show-ad-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/newgrounds-ad-show.png)

Immediately shows a Newgrounds ad in the center of the screen. Can be shown at any point in the game.

```
newgroundsShowAd();
```

***

### <a name="newgrounds-score-submit"></a> Submit Score

![submit-score-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/newgrounds-score-submit.png)

Submits a score to the specified Newgrounds leaderboard.

```
newgroundsSubmitScore([TEXT], [NUMBER]);
```

***

### <a name="newgrounds-score-show"></a> Show Scoreboard

![show-scoreboard-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/newgrounds-score-show.png)

Shows the specified Newgrounds leaderboard.

```
newgroundsShowScore([TEXT]);
```

***

### <a name="newgrounds-medal-achieved"></a> Unlock Medal

![unlock-medal-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/newgrounds-medal-achieved.png)

Unlocks a medal (achievement) by name. Medals are set up on Newgrounds.

![medal](http://static.stencyl.com/pedia2/ch5/third/image11.png)

```
newgroundsUnlockMedal([TEXT]);
```

***

### <a name="newgrounds-medal-move"></a> Move Medal Window

![move-medal-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/3%20-%20Flash/newgrounds-medal-move.png)

Sets the default location where the medals are shown. Call this at the beginning of the game - only has to be done once, but it has to be called before the medal shows. This cannot move medal windows that are already visible.

```
newgroundsSetMedalPosition([NUMBER], [NUMBER]);
```

***
