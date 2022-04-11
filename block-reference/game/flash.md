# Game > Flash

***

> For a walkthrough of how to integrate Kongregate and Newgrounds into your game, read [our article](https://www.stencyl.com/help/view/kongregate-mochi-newgrounds/) on Stencylpedia.

***

## Kongregate

### <a name="kong-init"></a> Start Kongregate API

![start api](https://static.stencyl.com/pedia2/block-images/game/flash/kong-init.png)

Starts up the Kongregate API. Must be used before doing anything with the API.

```
kongregateInitAPI();
```

***

### <a name="kong-submit"></a> Submit Score

![submit score number to with name text](https://static.stencyl.com/pedia2/block-images/game/flash/kong-submit.png)

Submit a [score](http://developers.kongregate.com/docs/kongregate-apis/stats) to Kongregate. First field is the name of the statistic. Second field is the value of it (a number).

```
kongregateSubmitStat([TEXT], [NUMBER]);
```

***

### <a name="kong-guest"></a> Is a Guest? (vs. logged in)

![player is a guest](https://static.stencyl.com/pedia2/block-images/game/flash/kong-guest.png)

Returns `true` if a guest is playing your game on Kongregate.

```
kongregateIsGuest()
```

***

### <a name="kong-name"></a> Name of Player

![name of player](https://static.stencyl.com/pedia2/block-images/game/flash/kong-name.png)

Returns the username of the player who is playing your game on Kongregate, if one is logged in. If it's a guest, the name will be `Guest`.

```
kongregateGetUsername()
```

***

### <a name="kong-userid"></a> User ID of Player

![id of player](https://static.stencyl.com/pedia2/block-images/game/flash/kong-userid.png)

Returns the user ID of the player who is playing your game on Kongregate, if one is logged in. If it's a guest, this will come back as blank.

```
kongregateGetUserID()
```

***

## Newgrounds

### <a name="newgrounds-ad-show"></a> Show Ad

![show ad](https://static.stencyl.com/pedia2/block-images/game/flash/newgrounds-ad-show.png)

Immediately shows a Newgrounds ad in the center of the screen. Can be shown at any point in the game.

```
newgroundsShowAd();
```

***

### <a name="newgrounds-score-submit"></a> Submit Score

![submit score number to for board text](https://static.stencyl.com/pedia2/block-images/game/flash/newgrounds-score-submit.png)

Submits a score to the specified Newgrounds leaderboard.

```
newgroundsSubmitScore([TEXT], [NUMBER]);
```

***

### <a name="newgrounds-score-show"></a> Show Scoreboard

![show scoreboard for board text](https://static.stencyl.com/pedia2/block-images/game/flash/newgrounds-score-show.png)

Shows the specified Newgrounds leaderboard.

```
newgroundsShowScore([TEXT]);
```

***

### <a name="newgrounds-medal-achieved"></a> Unlock Medal

![unlock medal for text](https://static.stencyl.com/pedia2/block-images/game/flash/newgrounds-medal-achieved.png)

Unlocks a medal (achievement) by name. Medals are set up on Newgrounds.

![medal](https://static.stencyl.com/pedia2/ch5/third/image11.png)

```
newgroundsUnlockMedal([TEXT]);
```

***

### <a name="newgrounds-medal-move"></a> Move Medal Window

![move medal to x number y number](https://static.stencyl.com/pedia2/block-images/game/flash/newgrounds-medal-move.png)

Sets the default location where the medals are shown. Call this at the beginning of the game - only has to be done once, but it has to be called before the medal shows. This cannot move medal windows that are already visible.

```
newgroundsSetMedalPosition([NUMBER], [NUMBER]);
```

***
