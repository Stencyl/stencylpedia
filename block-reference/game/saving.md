# Game > Saving

***

> View our article on [Saving Games](http://www.stencyl.com/help/view/saving-and-loading-games/) for an explanation of these blocks.

***

## Actions

### Save Game

![save-game-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/1%20-%20Saving/save-game.png)

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

### Load Game

![load-game-block](http://static.stencyl.com/pedia2/block-images/8%20-%20Game/1%20-%20Saving/load-game.png)

Tells the game to load. Loading will overwrite the values of all game attributes with those in the save file (if it exists).

If the load operation succeeds, the embedded `save succeeded` block will return `true` and the enclosed blocks will run. If the save fails, the embedded `save succeeded` block will return `false`, and the enclosed blocks will still run.

```
loadGame("mySave", function(success:Bool):Void {
	[ACTIONS]
});
```

***
