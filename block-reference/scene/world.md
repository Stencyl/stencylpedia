# Scene > World

***

## Gravity

### %0 gravity

![grav-xy](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/grav-xy.png)

Horizontal (X) or Vertical (Y) world gravity.

```
getGravity().x
```

***

### set gravity to ( xDir: %0 yDir: %1 )

![setgrav](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/setgrav.png)

Sets the world's gravity.

```
setGravity(0, 0);
```

***

## Tile API

### tile %0

![tile-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-wh.png)

The current scene's tile width/height.

```
getTileWidth()
```

***

### get %0 coordinate of %1 in scene

![tile-coord-at](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-coord-at.png)

Converts x/y coordinates to column/row in tile grid.

```
getTilePosition(0,0)
```

***

### set tile at row: %0 col: %1 layer %2 : %3 using tileID: %5 from tilesetID: %4

![set-tile-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/set-tile-at2.png)

Sets a tile into the Scene at the given position.

```
setTileAt(Std.int(0),Std.int(0),0,"" + "text",0,0);
```

***

### tile exists at row: %0 col: %1 layer %2 : %3

![tile-exists-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-exists-at2.png)

Returns true if a tile exists at the given position.

```
tileExistsAt(Std.int(0),Std.int(0),0,"" + "text")
```

***

### ID for tile at row: %0 col: %1 layer %2 : %3

![tileID-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tileID-at2.png)

The ID of the tile at the given position, or -1 if no tile found.

```
getTileIDAt(Std.int(0), Std.int(0), 0, "" + "text")
```

***

### tile collision shape found at row: %0 col: %1 layer %2 : %3

![tileCollisionAt2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tileCollisionAt2.png)

Returns true if ANY collision shape exists. If layer ID is a negative value, loops through all layers.

```
tileCollisionAt(Std.int(0),Std.int(0),0,"" + "text")
```

***

### collision ID for tile at row: %0 col: %1 layer %2 : %3

![tileColID-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tileColID-at2.png)

ID of the collision shape for the tile at this position, or -1 if no tile found.

```
getTileColIDAt(Std.int(0),Std.int(0),0,"" + "text")
```

***

### ID for tile's tileset at row: %0 col: %1 layer %2 : %3

![tilesetID-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tilesetID-at2.png)

ID of the tileset for the tile at this position, or -1 if no tile found.

```
getTilesetIDAt(Std.int(0),Std.int(0),0,"" + "text")
```

***

### remove tile at row: %0 col: %1 layer %2 : %3

![remove-tile-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/remove-tile-at2.png)

Remove tile at this position.

```
removeTileAt(Std.int(0),Std.int(0),0,"" + "text");
```

***

### data for tile at row: %0 col: %1 layer %2 : %3

![tile-data-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-data-at2.png)

Get data for tile at this position. Returns empty text if no tile found.

```
getTileDataAt(Std.int(0),Std.int(0),0,"" + "text")
```

***

## Properties

### scene %0

![scene-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/scene-wh.png)

The current scene's width/height in pixels/tiles.

```
(getSceneWidth())
```

***

### scene name

![scenename](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/scenename.png)

The current scene's name.

```
getCurrentSceneName()
```

***

