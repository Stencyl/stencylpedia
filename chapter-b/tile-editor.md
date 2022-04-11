> **Note:** If you're coming here from the [Tiles and Tilesets article](https://www.stencyl.com/help/viewArticle/36/), read on. If you found this through a search, we urge you to read the [main Tiles article](https://www.stencyl.com/help/viewArticle/36/) first.

> **Note:** If using simple physics for the global physics setting, this article does not apply and all tiles will have a collision box equal to the tile size.
 

## Contents

* Introduction
* Setting the Collision Shape
* Custom Collision Shapes
* Boxes
* Polygons
 

## Introduction

Tiles can take on more than just square shapes or blank areas. You can define their collision shapes as non-square  **boxes**, **slopes** (triangles) or even arbitrary **polygons**.

 
## Setting the Collision Shape

Suppose that we want to set the collision shape for the tile selected below. It's a sloped tile at about a 60 degree grade.

![60-degree-tile-selected](https://static.stencyl.com/help/images/TileSelection.png)

1. To set the collision shape, go over to the **Collision Bounds** window, scroll using the scroll bars to find the shape you need, and click on it.

  ![Set collision shape to a 60 degree triangle](https://static.stencyl.com/help/images/SetTriangleCollision.png)

  > **Tip:** You can edit the collision shapes for multiple tiles at a time if you select multiple tiles in the left (tiles) pane. You can do this by clicking and dragging to expand your selection rectangle.

2. Save your Tileset to confirm the changes.

  > **Tip:** If you've placed a tile inside a scene and change its collision bounds, you'll need to open that scene and save it to make the change get reflected.
 

## Custom Collision Shapes

Sometimes, you will need a custom collision shape for a tile that isn't reflected in any of the standard shapes we provide.

If this is the case, you can define a Custom Collision Shape by clicking on the + button. You can create either a **Box** or a **Polygon**.

 
## Box Shapes

X and Y dictate the relative position of the box, in case you want it to be shifted off the origin (0,0).

All values are in percentages (0 - 100 inclusive). We do this so that you don't have to worry about how big the tiles are.

![Creating a collision box](https://static.stencyl.com/help/images/BoxCollision.png)

 
## Polygon Shapes

Create a Polygon by defining points and setting their x,y values, either through the table or through drag and drop. A polygon must have 3 or more points but no more than 12.

> **Note:** Define points in counter-clockwise order. If you don't, the engine may crash and warn you about a polygon having negative area.

![Creating a polygonal collision shape](https://static.stencyl.com/help/images/PolygonCollision.png)

> **Gotcha:** Only convex polygons are supported. Do not enter in a concave polygon, such as an "L" shape. Instead, use an actor or split the tile into two or more separate tiles that you place on top of each other.
