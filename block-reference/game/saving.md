# Game > Saving

***

> View our article on [Saving Games](https://www.stencyl.com/help/view/saving-and-loading-games/) for an explanation of these blocks.

***

## Actions

### <a name="save-game"></a> Save Game

![save game and then...](https://static.stencyl.com/pedia2/block-images/game/saving/save-game.png)

Tells the game to save. Saving will store the state of all game attributes into a file.

If the save operation succeeds, the embedded `save succeeded` block will return `true` and the enclosed blocks will run. If the save fails, the embedded `save succeeded` block will return `false`, and the enclosed blocks will still run.

```
saveGame("mySave", function(success:Bool):Void {
  [ACTIONS]
});
```

#### Example

![example](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-5/images/saving-2.png)

***

### <a name="load-game"></a> Load Game

![load save file and then...](https://static.stencyl.com/pedia2/block-images/game/saving/load-game.png)

Tells the game to load. Loading will overwrite the values of all game attributes with those in the save file (if it exists).

If the load operation succeeds, the embedded `save succeeded` block will return `true` and the enclosed blocks will run. If the save fails, the embedded `save succeeded` block will return `false`, and the enclosed blocks will still run.

```
loadGame("mySave", function(success:Bool):Void {
  [ACTIONS]
});
```

***
