# Scenes > World

***

## Gravity

### <a name="grav-xy"></a> Get Value of Gravity

![horizontal gravity](http://static.stencyl.com/pedia2/block-images/scene/world/grav-xy.png)

Returns the value of the Horizontal (X) or Vertical (Y) components of gravity. Gravity is a force that is applied to all actors (that are affected by it).

```
getGravity().x
getGravity().y
```

***

### <a name="setgrav"></a> Set Gravity

![set gravity to x dir number y dir number](http://static.stencyl.com/pedia2/block-images/scene/world/setgrav.png)

Sets the world's gravity.

```
setGravity([NUMBER], [NUMBER]);
```

***

## Properties

### <a name="scene-wh"></a> Scene Width / Height

![scene width pixels](http://static.stencyl.com/pedia2/block-images/scene/world/scene-wh.png)

Returns the current scene's [width/height] in [pixels/tiles].

```
getSceneWidth()
getSceneHeight()
Std.int(getSceneWidth()/getTileWidth())
Std.int(getSceneHeight()/getTileHeight())
```

***

### <a name="scenename"></a> Scene Name

![scene name](http://static.stencyl.com/pedia2/block-images/scene/world/scenename.png)

Returns the current scene's name.

```
getCurrentSceneName()
```

***

## Tile API

### <a name="tile-wh"></a> Tile Width / Height

![tile width](http://static.stencyl.com/pedia2/block-images/scene/world/tile-wh.png)

Returns the current scene's tile width/height.

```
getTileWidth()
getTileHeight()
```

***

### <a name="tile-coord-at"></a> Convert to Tile Coordinates

![get column x coordinate of number in scene](http://static.stencyl.com/pedia2/block-images/scene/world/tile-coord-at.png)

Converts a coordinate from pixels (real location) to tiles. In other words, divides the coordinate by the tile width or height respectively.

```
getTilePosition(0, [NUMBER]) //x coordinate
getTilePosition(1, [NUMBER]) //y coordinate
```

***

### <a name="set-tile-at2"></a> Set a Tile

![set tile at row int col int layer id object using tile id int from tileset id int](http://static.stencyl.com/pedia2/block-images/scene/world/set-tile-at2.png)

Sets a tile at the given position and layer.

```
setTileAt([INT], [INT], engine.getLayerById([INT]), [INT], [INT]);
setTileAt([INT], [INT], engine.getLayerByName([TEXT]), [INT], [INT]);
```

***

### <a name="tile-exists-at2"></a> Does a Tile exist at location?

![tile exists at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/tile-exists-at2.png)

Returns `true` if any tile exists at the given position and layer.

```
tileExistsAt([INT], [INT], engine.getLayerById([INT]))
tileExistsAt([INT], [INT], engine.getLayerByName([TEXT]))
```

***

### <a name="tileID-at2"></a> Get ID for Tile at location

![id for tile at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/tileID-at2.png)

Returns the ID of the tile at the given position and layer, or -1 if no tile found.

```
getTileIDAt([INT], [INT], engine.getLayerById([INT]))
getTileIDAt([INT], [INT], engine.getLayerByName([TEXT]))
```

***

### <a name="tileCollisionAt2"></a> Does a solid tile exist at location?

![tile collision shape found at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/tileCollisionAt2.png)

Returns `true` if ANY collision shape exists. If layer ID is -1, loops through all layers.

```
tileCollisionAt([INT], [INT], engine.getLayerById([INT]))
tileCollisionAt([INT], [INT], engine.getLayerByName([TEXT]))
```

***

### <a name="tileColID-at2"></a> Get Collision ID for tile at location

![collision id for tile at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/tileColID-at2.png)

Returns the ID of the collision shape for the tile at this position and layer, or -1 if no tile found.

```
getTileColIDAt([INT], [INT], engine.getLayerById([INT]))
getTileColIDAt([INT], [INT], engine.getLayerByName([TEXT]))
```

***

### <a name="tilesetID-at2"></a> Get Tileset ID for tile at location

![id for tile's tileset at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/tilesetID-at2.png)

Returns the ID of the tileset for the tile at this position and layer, or -1 if no tile found.

```
getTilesetIDAt([INT], [INT], engine.getLayerById([INT]))
getTilesetIDAt([INT], [INT], engine.getLayerByName([TEXT]))
```

***

### <a name="remove-tile-at2"></a> Remove tile at location

![remove tile at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/remove-tile-at2.png)

Remove the tile at this position.

```
removeTileAt([INT], [INT], engine.getLayerById([INT]));
removeTileAt([INT], [INT], engine.getLayerByName([TEXT]));
```

***

### <a name="tile-data-at2"></a> Get Metadata for tile at location

![data for tile at row int col int layer id object](http://static.stencyl.com/pedia2/block-images/scene/world/tile-data-at2.png)

Get the tile data for the tile at this position. Returns empty text if no tile found.

```
getTileDataAt([INT], [INT], engine.getLayerById([INT]))
getTileDataAt([INT], [INT], engine.getLayerByName([TEXT]))
```

***
