## Contents

* Introduction
* How To: Importing a Tileset
* Overview of the Tileset Editor
* Collision Shapes
* Animated Tiles
* Working with the Tileset
* Mobile Games & Tilesets
* Troubleshooting
* The Tile API
 
 
## Introduction

What are the building blocks of a scene? The scene’s terrain or “land” is typically made up of Tiles. Much like the tiles on your kitchen counter or bathroom, Tiles in a game are uniformly sized pieces of land that conform to a grid.

This article will cover the basics of importing and working with tiles.


## How To: Importing a Tileset

#### Step 1 - Create It

Go to this menu item: **File > Create New > Tileset**

![](http://static.stencyl.com/pedia2/ch4/tiles/image01.png)

 
#### Step 2 - Name It

![](http://static.stencyl.com/help/images/NameTiles1.png)

 
#### Step 3 - Import the Tile Sheet

You'll now see this window.

![](http://static.stencyl.com/help/images/ImportTileset.png)

1. Click **Choose Image** to pick out the tile sheet you want to import. *(You can also copy it to the clipboard and paste it in.)*

2. **Pick out the Tile Width/Height**. This will determine how your tile sheet is cut up. In most cases, this is 32x32 or 16x16.

3. The spacing and border fields are for cases where your tiles are spaced apart. *This is rare.*

4. That's it. Click **Add** to finish the import.

Now, you'll see the main page for your newly imported Tileset.


#### Overview of the Tileset Editor

(TODO: Do a run through of the interface. Link to sections that cover each in more detail.)

 

#### Collision Shapes

Now that you've uploaded your tileset, you will want to set the collision shapes for your tiles. You can either...

1. Choose an existing collision shape (or none at all)
2. Create a custom collision shape.

Picking a shape is simple - **just click on any entry within the Collision Bounds pane**. This even works when multiple tiles are selected (click and drag to select multiple tiles in the left pane).

![](http://static.stencyl.com/help/images/SetTriangleCollision.png)

If you prefer to make a custom shape, click the + button. You'll get a choice between creating a box (rectangle) or a convex polygon.

![](http://static.stencyl.com/help/images/BoxCollision.png) ![](http://static.stencyl.com/help/images/PolygonCollision.png)

To learn more about tile collision shapes and how to define custom shapes, view our [Setting Tile Collision Shapes](http://www.stencyl.com/help/viewArticle/37/) article.
 

## Animated Tiles

Some games use Animated Tiles to bring a scene to life. Here's how you convert a plain tile to an animated one.

1. Open up a Tileset.

2. Click on the Tile you'd like to animate in the left pane.<br/><br/>![](http://static.stencyl.com/help/images/TileFrameToEdit.png)<br/>

3. You'll now see information in the right-hand pane. The bottom part of this pane should look familiar. **It's the same as the one you use for managing an Actor's animations.**

![](http://static.stencyl.com/help/images/TileAnimationEditors.png)

From this point, it's the same process and user interface as working with [Actor Animations](http://www.stencyl.com/help/view/animations/). As a refresher, you...

1. Import frames from an image strip/sheet.
2. Edit the frame durations, if necessary.
 

## Working with the Tileset

#### Adding/Removing Rows & Columns
You can alter a tileset's row and column count by clicking directly on the row and column headers.

![](http://static.stencyl.com/pedia2/ch4/tiles/image00.png)

#### Adding More Tiles
You may add additional tiles to a tileset after the initial import.

For best results, we recommend importing using an image that is the **same width as the existing tileset**, so additions don't get "offset" and break the layout. 

> For example, if your tileset is 6 columns wide, ensure that what you are importing is also 6 columns wide.

#### Rearranging Tiles
You can drag and drop tiles to rearrange them. Here's how.

1) With the **Select Tiles mode** active, select the tile(s) you wish to move. In this example, we've selected some tiles in row 1.

![](http://static.stencyl.com/pedia2/ch4/tiles/tileset-dnd1.png)

2) Now, switch to the Move Tiles mode.

![](http://static.stencyl.com/pedia2/ch4/tiles/tileset-dnd2.png)

3) **Drag and drop** your selection to the desired location. This will **perform a swap** between the tiles you have selected and the tiles in the desired location.

![](http://static.stencyl.com/pedia2/ch4/tiles/tileset-dnd3.png)

> In this example, we've moved the tiles 3 positions over from their original position.

#### Working with Multiple Tiles at a Time
You can select multiple tiles at a time by clicking and dragging a box over those tiles. What's the use of this?

You can edit multiple collision bounds at the same time, a major time saver. As described above, you can also move/rearrange multiple tiles at a time.

![](http://static.stencyl.com/features/tileset-3.2.png)

#### Modifying the Tile Sheet Directly
You can...

* Edit the tileset's backing image directly in an external editor.
* Reimport the image, provided that it's the same size as the existing one.
* Replace the images for selected tiles.

This allows you to make visual tweaks to the tileset without having to reimport everything or manually edit the image from the game's directory.

#### Tile Metadata
You can tag tiles with textual data that can be accessed during game. For example, a lava tile could convey that it's deadly to the touch, or a healing tile in an RPG could heal the character passing over it.

![](http://static.stencyl.com/pedia2/ch4/tiles/tile-metadata.png)

To access this data from a behavior, you can use one of two methods.

1. Use the **data for tile** block under **Scene > World > Tile API**.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/tiles/tile-metadata-2.png)<br/>

2. Use the **data for collided tile** block under **Collision > Collision Points**.<br/><br/>![](http://static.stencyl.com/pedia2/ch4/tiles/tile-metadata-3.png)<br/>


## Mobile Games & Tilesets

If you've worked with mobile games, you'll know by now that all graphics should be [imported at quadruple the standard resolution](http://www.stencyl.com/help/view/mobile-app-scaling/), in order to support larger resolution displays and tablets.

Tilesets follow this same rule.

1. Import Tilesets at 4x the native resolution.

2. However, when you actually import, you still specify the Tile Width, Tile Height and other parameters in 1x. It's just the **IMAGE ITSELF** that you import at 4x.

> **Example:** For example, if your game's regular tile size is 32 x 32, you should import a tile sheet where the tiles are 128 x 128 and specify that you are importing at 4x. The Tile Size is still stated to be 32 x 32.
 

## Troubleshooting

* **Keep the tile size for all tilesets and scenes the same**. For example, if your tilesets have a tile size of 32 x 32, make sure that the scenes also have a tile size of 32 x 32.

* When defining custom polygon shapes for Tiles, **you can only use convex polygons**. If you need to make a concave polygon, use multiple tiles to achieve this.

* In very rare situations, a scene may crash in game if the terrain is **complex** enough to exceed our engine's internal limit - there's no exact number, but it's on the order of hundreds, possibly thousands of sides. This happens because we combine all of the shapes into larger ones to improve performance. This can be worked around by altering the terrain to break up the large, offending shape into 2 smaller land masses.
 

## The Tile API

What if you want to change a scene's terrain at runtime? For example, you're making a game with automatically-generated dungeons. Use the [Tile API](http://www.stencyl.com/help/view/tile-api), a special set of blocks, to accomplish this.
 

## Summary

* Tiles are uniform building blocks for scenes.
* You can specify custom collision shapes for tiles and animate them.
* Tiles get auto-combined by Stencyl into large land masses in order to improve performance.
