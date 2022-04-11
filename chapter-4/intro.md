> Looking instead for a guide on [**how** to use our Scene Designer?](https://www.stencyl.com/help/view/scene-designer/)

## Contents

* Introduction
* Scenes and Game Flow
* Tiles
* Layers
* Coordinates
* Boundaries
 
 
## Introduction

Scenes are a game's **worlds** or **levels**. Scenes are where everything in a game takes place. This article talks about the fundamental concepts of Scenes.
 

## Scenes Control a Game's Flow

Think about a game such as Super Mario Bros. When you play through the first level and reach the flagpole at the end, there's a brief victory sequence, and then Mario proceeds to the next level.

Sometimes, scenes aren't levels at all. Even a main menu itself can be a scene.

![Title Screen](https://static.stencyl.com/pedia2/ch4/basics/image10.png)

Putting this together, scenes can be thought of as various **states in a game** that you transition between, making up something like a **story**.

![Storyboard](https://static.stencyl.com/pedia2/ch4/basics/image16.png)

#### Switching Scenes

[Switching scenes](https://www.stencyl.com/help/view/changing-scenes/) is described later in this chapter, but in short, use the following blocks to switch scenes. (under Scene > Game Flow).

![Switching Scene Blocks](https://static.stencyl.com/pedia2/ch4/basics/image14.png)

Switching scenes involves an "outgoing" transition (such as a fade out), the scene you are switching to, and then an "incoming" transition (such as a fade in).


## Tiles

What are the building blocks of a scene? The scene's terrain or "land" is typically made up of Tiles.

![Tileset](https://static.stencyl.com/pedia2/ch4/basics/image05.png)

Much like the tiles on your kitchen counter or bathroom, Tiles in a game are uniformly sized pieces of land that conform to a grid. That is to say...

* Every tile is the same size.
* Tiles are spaced equally apart - by the tile size.

Why are tiles a great way to build levels? Imagine that you're building an action game such as this: 

![Reaching Finality](https://static.stencyl.com/v3/images/showcase/finality.png)

It would be impractical to create separate sprites for each land mass. After a while, you'd run out of space trying to pre-render all of that!

Tiles are a cheap, reusable way of creating worlds. You'll find that with tiles, virtually any kind of land form can be re-created with ease. Using this tileset...

![Tileset](https://static.stencyl.com/pedia2/ch4/basics/image00.png)

We can make a rich landscape like this.

![Landscape](https://static.stencyl.com/pedia2/ch4/basics/image13.png)

Tiles need not be square. You can define tiles as triangles and any kind of convex polygon in order to support slopes and other complex forms of terrain.

![Sloped Tiles](https://static.stencyl.com/pedia2/ch4/basics/image01.png)

#### What if my game isn't a fit for tiles?

What if you're building a game where tiles are inappropriate, as pictured below? You're able to define custom terrain to satisfy this use case.

![Icarus](https://static.stencyl.com/pedia2/ch4/basics/image17.png)

(Not a tile-based game, use the Custom Terrain tool!)

![Custom Terrain](https://static.stencyl.com/pedia2/ch4/basics/image03.png)

#### Importing Tilesets

For information on how to import tiles and work with our Tile Editor, [read our article on that](https://www.stencyl.com/help/view/tiles/).


## Layers

What if you want some parts of the scene to draw on top of other parts? For example, you may want a guarantee that the player draws in **front** of the game's scenery.

![Layer Example](https://static.stencyl.com/pedia2/ch4/basics/image07.png)

A Layer is a **group of both Actors and Tiles** that are **drawn at the same time**. In this way, Layers provide you a flexible yet simple way to determine what order things are drawn in.

To take the example above, here's the breakdown of what's on which layer.

![Layer Breakdown](https://static.stencyl.com/pedia2/ch4/basics/image09.png)

Scenes can have an arbitrary number of layers. There's no limit and no performance hit to having more layers as opposed to fewer.

#### Managing Layers

Use the Layers Pane inside the Scene Designer to manage layers. You can create, remove, rename and re-arrange layers using this interface.

![Layers Pane](https://static.stencyl.com/pedia2/ch4/basics/image15.png)


#### Switching Layers

Sometimes, you'll want to change what layer an Actor is on. To do this, use the following blocks. (under Actor > Draw)

![Switch Layer Blocks](https://static.stencyl.com/pedia2/ch4/basics/image02.png)

When sending an Actor to a particular layer, specify the Layer's ID. You can find this inside the Layers Pane inside the Scene Designer.

![Layers Pane](https://static.stencyl.com/pedia2/ch4/basics/image11.png)


## Coordinates

Every element inside a Scene has a **position**. This position consists of an X (horizontal) and Y (vertical) component and corresponds to the **top left corner** of that element.

**(0,0) is the top left most point in the scene.**

![Coordinates](https://static.stencyl.com/pedia2/ch4/basics/image12.png)

A **higher X value** moves you towards the **right**, while a **higher Y value** moves you towards the **bottom**.

 
## Boundaries

Every scene has boundaries (a size) that you define when you first create the scene. These boundaries control how far the Camera can travel and how far Tiles can extend.

![Bounds](https://static.stencyl.com/pedia2/ch4/basics/image06.png)

Although actors can go beyond a scene's boundaries, actors that are not designated as always active will "freeze" upon doing this.

Imagine boundaries to be like the limits of a level in a Mario level. Going beyond certain bounds is either not permitted (left & right) or leads to death (off the bottom).


## Summary

* Scenes control the flow of a game, like a storyboard.
* Tiles are equal-sized building blocks. They define the terrain.
* Layers group together tiles & actors in order to control drawing order.
* (0,0) is top left in our coordinate system.
* Scenes have boundaries (a size) that define how far actors and terrain can be placed.
