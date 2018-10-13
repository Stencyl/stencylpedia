> **Note:** This guide is adapted from this [ongoing forum topic](http://community.stencyl.com/index.php/topic,28260.0.html). Please [ask all of your questions](http://community.stencyl.com/index.php/topic,28260.0.html) about the Tile API in that forum discussion.
 

## What is the Tile API?

The Tile API is a collection of functions that let you modify a scene's terrain at runtime. The Tile API is essential for games that dynamically generate terrain. Here's what the Tile API can do:

* Change tile at a location.
* Remove tile at a location.
* Determine whether a tile exists at a given location.
* Determine what tile exists at a given location. Determine which collision group it belongs to. Determine which tileset it belongs to?
 

## How do you install the Tile API?

In Stencyl 3.2 and above, the Tile API is part of the regular block set. You can find the blocks under *Scene > World > Tile API*.

 
## Additional Notes

Tile coordinates are measured in Rows and Columns. It is important to note that a Row coordinate is a measure of the tile's position on the Y axis, while Columns are measured on the X axis. Initially this may appear to be incorrect, but it is necessary to remember that "10 rows" means 10 tiles vertically (rows are stacked), but "10 columns" means 10 tiles horizontally.

Row and column coordinates start at 0 (zero), at the top-left corner of the scene, and increase in number going down (for rows) and to the right (for columns).

Tileset ID numbers can be found by looking at the bottom bar in the Tileset Editor. If a single tile is selected you will also see the Tile ID of the selected tile.

Layer ID numbers can be found in the Scene Designer's Layer box.

> **Aside:** For performance reasons, layers cannot contain tiles unless they have one already at compile time (from the Scene Designer). Attempting to place a tile with the Tile API into a non-tile layer will fail. To resolve, include at least one tile (it can be invisible and without a collision shape) on the desired layer.


## Individual Block Information

#### Get (Column/Row) Coordinate Of (number) In Scene
Type: Number

![](http://i.imgur.com/PxUu5aE.png)

This blocks produces the tilemap coordinate of a position in the scene. To get the coordinate in Rows, use a positive Y value. To get the coordinate in Columns, use a positive X value. Negative values are accepted, however they represent tile coordinates that are out-of-bounds of the scene (to the left of or above the top left corner of the scene).

***

#### Set Tile At Row: (number) Col: (number) LayerID: (number) Using TileID: (number) From TilesetID: (number)
Type: Action

![](http://i.imgur.com/W68ENgo.png)

This block creates a new tile in the scene at the designated coordinate and layer. The tile to be used is determined by the other two ID's given; the Tileset ID and Tile ID of the desired tile from that tileset. Note that placing a tile into the scene in this manner will create a new collision shape each time if the tile placed has a collision shape assigned to it. Significant numbers of these tiles can incur a performance penalty due to the many collision shapes

***

#### Tile Exists At Row: (number) Col: (number) LayerID: (number)
Type: Boolean (True/False)

![](http://i.imgur.com/vRqXOyI.png)

This block indicates if there is a tile of any kind at the given coordinate and layer.


#### ID For Tile At Row: (number) Col: (number) LayerID: (number)
Type: Number

![](http://i.imgur.com/AvkCA8p.png)

This block produces the Tile ID for a tile at the given coordinate and layer. If there is no tile at the position, this block returns the value -1 instead.

***

#### Tile Collision Shape Found At Row: (number) Col: (number) LayerID: (number)
Type: Boolean (True/False)

![](http://i.imgur.com/XelTRZh.png)

This block indicates if the tile at the given coordinate and layer has a collision shape or not. If a negative value (e.g. -1) is used for the Layer ID, it will check all tile layers automatically. Note that to do so, the block must loop through all tile layers in a scene to check; doing so could incur a performance penalty.

***

#### Collision ID For Tile At Row: (number) Col: (number) LayerID: (number)
Type: Number

![](http://i.imgur.com/vg2cNQo.png)

This block provides the numeric value of the collision ID for a tile at the given coordinate and layer. If there is no collision shape found, it will return a value of -1 instead. This includes if there is no tile, or if a tile exists but lacks a collision shape.

***

#### ID For Tile's Tileset At Row: (number) Col: (number) LayerID: (number)
Type: Number

![](http://i.imgur.com/4RgsY5D.png)

This block provides the numeric value of the Tileset ID of the tile at the given coordinate and layer. If there is no tile found, it will return a value of -1 instead.

***

#### Remove Tile At Row: (number) Col: (number) LayerID: (number)
Type: Action

![](http://i.imgur.com/Nxind46.png)

This block will delete the tile at the given coordinate and layer. Note that deleting a tile will only remove it's collision shape from the scene if it was added through the Tile API. If the tile was placed in Scene Designer, the tile's visual image will be removed but the collision shape will remain behind (invisible unless Debug Drawing is enabled).


## Example Usage

The following image demonstrates how these blocks might be combined to produce a behavior that places, or removes, a tile in the scene when the player clicks the mouse

<a href="http://i.imgur.com/0U9dQ1Y.png"><img alt="Example" src="http://i.imgur.com/0U9dQ1Y.png" style="width: 800px; height: 262px;"></a>
