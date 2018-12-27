# Scene > World

***

## Gravity

### <a name="grav-xy"></a> Get Value of Gravity

![grav-xy](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/grav-xy.png)

Returns the value of the Horizontal (X) or Vertical (Y) components of gravity. Gravity is a force that is applied to all actors (that are affected by it).

```
getGravity().x
getGravity().y
```

***

### <a name="setgrav"></a> Set Gravity

![setgrav](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/setgrav.png)

Sets the world's gravity.

```
setGravity([NUMBER], [NUMBER]);
```

***

## Tile API

### <a name="tile-wh"></a> Tile Width / Height

![tile-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-wh.png)

Returns the current scene's tile width/height.

```
getTileWidth()
getTileHeight()
```

***

### <a name="tile-coord-at"></a> Convert to Tile Coordinates

![tile-coord-at](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-coord-at.png)

Converts a coordinate from pixels (real location) to tiles. In other words, divides the coordinate by the tile width or height respectively.

```
getTilePosition(0, [NUMBER]) //x coordinate
getTilePosition(1, [NUMBER]) //y coordinate
```

***

### <a name="set-tile-at2"></a> Set a Tile

![set-tile-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/set-tile-at2.png)

Sets a tile at the given position and layer.

```
setTileAt([NUMBER], [NUMBER], 0, [TEXT], [NUMBER], [NUMBER]); //specify layer ID
setTileAt([NUMBER], [NUMBER], 1, [TEXT], [NUMBER], [NUMBER]); //specify layer name
```

***

### <a name="tile-exists-at2"></a> Does a Tile exist at location?

![tile-exists-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-exists-at2.png)

Returns `true` if any tile exists at the given position and layer.

```
tileExistsAt([NUMBER], [NUMBER], 0, [TEXT]) //specify layer ID
tileExistsAt([NUMBER], [NUMBER], 1, [TEXT]) //specify layer name
```

***

### <a name="tileID-at2"></a> Get ID for Tile at location

![tileID-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tileID-at2.png)

Returns the ID of the tile at the given position and layer, or -1 if no tile found.

```
getTileIDAt([NUMBER], [NUMBER], 0, [TEXT]) //specify layer ID
getTileIDAt([NUMBER], [NUMBER], 1, [TEXT]) //specify layer name
```

***

### <a name="tileCollisionAt2"></a> Does a solid tile exist at location?

![tileCollisionAt2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tileCollisionAt2.png)

Returns `true` if ANY collision shape exists. If layer ID is -1, loops through all layers.

```
tileCollisionAt([NUMBER], [NUMBER], 0, [TEXT]) //specify layer ID
tileCollisionAt([NUMBER], [NUMBER], 1, [TEXT]) //specify layer name
```

***

### <a name="tileColID-at2"></a> Get Collision ID for tile at location

![tileColID-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tileColID-at2.png)

Returns the ID of the collision shape for the tile at this position and layer, or -1 if no tile found.

```
getTileColIDAt([NUMBER], [NUMBER], 0, [TEXT]) //specify layer ID
getTileColIDAt([NUMBER], [NUMBER], 1, [TEXT]) //specify layer name
```

***

### <a name="tilesetID-at2"></a> Get Tileset ID for tile at location

![tilesetID-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tilesetID-at2.png)

Returns the ID of the tileset for the tile at this position and layer, or -1 if no tile found.

```
getTilesetIDAt([NUMBER], [NUMBER], 0, [TEXT]) //specify layer ID
getTilesetIDAt([NUMBER], [NUMBER], 1, [TEXT]) //specify layer name
```

***

### <a name="remove-tile-at2"></a> Remove tile at location

![remove-tile-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/remove-tile-at2.png)

Remove the tile at this position.

```
removeTileAt([NUMBER], [NUMBER], 0, [TEXT]); //specify layer ID
removeTileAt([NUMBER], [NUMBER], 1, [TEXT]); //specify layer name
```

***

### <a name="tile-data-at2"></a> Get Metadata for tile at location

![tile-data-at2](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/tile-data-at2.png)

Get the tile data for the tile at this position. Returns empty text if no tile found.

```
getTileDataAt([NUMBER], [NUMBER], 0, [TEXT]) //specify layer ID
getTileDataAt([NUMBER], [NUMBER], 1, [TEXT]) //specify layer name
```

***

## Properties

### <a name="scene-wh"></a> Scene Width / Height

![scene-wh](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/scene-wh.png)

Returns the current scene's [width/height] in [pixels/tiles].

```
(getSceneWidth())
(getSceneHeight())
(getSceneWidth()/getTileWidth())
(getSceneHeight()/getTileHeight())
```

***

### <a name="scenename"></a> Scene Name

![scenename](http://static.stencyl.com/pedia2/block-images/2%20-%20Scene/2%20-%20World/scenename.png)

Returns the current scene's name.

```
getCurrentSceneName()
```

***
