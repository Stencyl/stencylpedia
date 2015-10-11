## Actor Terminology

#### Actor (Instance)

An individual object in a Scene that has a parent Actor Type. Note that each Actor shares the Behaviors, and related Attributes and Attribute values, that a user attaches to its parent Actor Type.

#### Actor Type

A template or “blueprint” that an Actor is based on. An Actor Type is the “parent” of an Actor. Each Actor Type can have its own set of Behaviors that define what its “child” Actors can do and any other related game logic characteristics.

#### Actor Group

The specific Collision Group associated with an Actor Type, and any related child Actors. An Actor Type can have more than one Collision Group associated with it.

#### Animation

A group of images that display in order over a set period of time. An Actor Type can have multiple Animations but a Tile can only have a single Animation. An individual image in an Animation is called an Animation Frame. Each Animation associated with an Actor Type can have its own Collision Group(s). An Animation can be set to play once or to repeat (looping). A Tile cannot have more than one Collision Group associated with its Animation. In addition, each Animation will have its own Collision Shape.

#### Collision Group

A Collision Group is an arbitrary category that Actor Types, and their child Actors, can belong to. A user can define which Collision Groups can interact and which cannot. A user can also create new Collision Groups and define how they interact with one another. There are five default Collision Groups that a user cannot change: Players, Tiles, Doodads/Decoration, Actors, and Regions. A user can assign any Actor Type to one of those groups or to new groups. Be default, all Actor Types belong to the “Actors” Collision Group. Tiles always belong to their own Collision Group and cannot be associated with any other group. Doodads and Regions are non-colliding groups. They are used to detect collisions but not move colliding Actors.

#### Collision Shape

A Collision Shape is the shape of one set of collision bounds for a given Animation. It can be rectangular, circular, or polygonal (i.e customizable by a user).

#### Frame

A single image within an Animation. Each Frame shares the Collision Group(s) specified for a complete Animation. A Frame cannot have its own Collision Group(s) separate from those of its Animation and Actor Type. In the case of a Frame in a Tile’s animation, the Collision Group is always Tiles.

#### Origin Point

Only used when you need to reference “origin” coordinates related to an Actor for specific operations. Two operations refer to the Origin Point’s coordinates, rotate and scale. A user can choose a number of options for the Origin Point from a dropdown menu in the Actor Type Appearance tab and create custom coordinates for an Origin Point. The Origin Point is relative to the default horizontal and vertical (x and y) coordinates of a given Actor Type’s Animation. Origin Point ONLY applies to Web games, not iOS games.

#### Sensor

An option related to the collision bounds and group(s) associated with an Actor Type. An Actor that has collision bounds set as Sensors will detect when something else collides with it but won’t produce a standard collision response (i.e. bouncing off each other). If an Actor collides with another Actor that has its collision bounds set to the Sensor option, the two Actors will appear to pass through one another. A user can still perform logic on Actors (via Behaviors) that are Sensors, though. For example, although one Actor that is a Sensor can pass through another, that Actor could still take damage from colliding with another Actor.

## Behavior Terminology

#### Behavior

Modular gameplay logic that a user can attach to an Actor Type or to a Scene. Also, when creating a Behavior, a user must specify whether the Behavior is an Actor Behavior or a Scene Behavior.

#### Actor Behavior

A Behavior attached to an Actor Type. Note that each Actor shares the Actor Behaviors, and related default Attribute values, with its parent Actor Type.

#### Scene Behavior

A Behavior attached to a Scene. Scene Behaviors use different options in Design Mode to perform logic that would only apply to a Scene. For example, in a Scene Behavior, when referring to an Actor in the Scene, you must select a specific Actor. In Actor Behaviors, the default Actor is the one the Actor Behavior is attached to.

#### Attribute

A configurable property in a Behavior, represented by a blue Block in Design Mode. Each Attribute has a category it falls into called a type. Examples include Number, Text, Control, Scene, etc. Attributes can be Hidden or Non-Hidden. A user cannot configure Hidden Attributes from an Actor Type’s Behavior tab or a Scene’s Behavior tab whereas a user can configure Non-Hidden Attributes (Attribute values can always be configured from Design Mode, though). Attributes are local to the Behavior instance they are associated with. This means if you have two Actors of the same Actor Type in your Scene, Actors created from that Actor Type will each have their own set of values for their Behaviors’ Attributes.For example, if Actor Type A has a Behavior called Move, and that Behavior has an Attribute called Speed, then each Actor created will have its own separate Speed Attribute value.

Actor ID 1
Move (Speed: 5)

Actor ID 2
Move (Speed: 5)

Because those values are independent, you can use Behavior logic to change the value for one Actor and not the other, as shown below.

Actor ID 1
Move (Speed: 5)

Actor ID 2
Move (Speed: 10)

#### Game Attribute

A “global” or “universal” Attribute that is accessible by any and all Behaviors in a game. Game Attributes are represented by purple Blocks in Design Mode.

#### Block

A single element used to perform some kind of game logic in Stencyl’s Design Mode. Each Block type is color coded, and shaped, to allow users to easily distinguish between Blocks and determine how they should interact with one another.

#### Expression Block

A Block that fits into a blank in another Block.

#### Action Block

A Block used in Design Mode that performs an in-game action of some kind. Action Blocks typically have “notches” that indicate they can fit within Event Blocks and attach to one another to perform logic in sequential order.

#### Event

A Block in Design Mode used to detect when certain conditions are met in a game or specify when certain types of logic should occur. Action Blocks can fit inside Event blocks. There are four basic types of Event blocks: When Created, Always, When Collided, and When Drawing. When Created performs logic when the game is initialized, i.e. when it starts. Always performs the logic contained in it every single step, which is a 100 times per second. When Drawing performs drawing-related logic every frame, in most games at a rate of 60 frames per second (FPS). When Collided performs the logic contained within it when the Actor (the one with a Behavior with this Block attached to it) collides with a Tile or another Actor.

#### Messaging

A way for Behavior instances to communicate with, and change the values of, other Behavior instances. Note that Behavior instances can send messages to specific other Behavior instances, to all instances of another Behavior, or to all Behavior instances in a scene, i.e. all the Behavior instances attached to the Scene itself and to all Actors in a Scene.

#### Message

An individual “phrase” sent between Behaviors is called a Message. Note that for Messages to be received properly, the Message must be spelled in the When This Hears Event Block EXACTLY as it appears in the messaging Action Block.

#### Boolean

A value that can be true or false. Also an Attribute type that can have a value of true or false. Represented by hexagonal Blocks in Design Mode. Booleans are often used to check whether or not specific in-game conditions have been met.

#### Number

A positive or negative number that can also have decimal values. This is an Attribute type in Design Mode. This is also a type of Game Attribute.

#### Text

Characters or symbols that cannot be manipulated mathematically. Also known as a “string” in programming terms. Words are a good example of Text. Text is an Attribute type in Design Mode. This is also a type of Game Attribute.

#### List

A group of objects organized in sequential order by index number. All Lists begin at index number 0 (the first item in the List has an index number of 0). This is an Attribute type in Design Mode. This is also a type of Game Attribute.

#### Control

An Attribute type in Design Mode that refers to a specific, arbitrary type of user input. Note that a Control Attribute can refer to input from a mouse click, keyboard press, or touchscreen.

#### Sound

An Attribute type in Design Mode that can refer to an arbitrary sound file (generally in MP3 format). This can be a sound effect or a music loop.

#### Channel

An independent “voice” that you can assign a Sound Attribute to. You can use Blocks in Design Mode to manipulate when Channels start and stop playing, volume, and fading.



## Development / Debugging

#### Print

A Block in Design Mode that prints the value of Attributes (or Game Attributes) to the console. This is commonly used to “debug,” i.e. troubleshoot, games by letting the developer know whether certain Attribute values are changing as they should. For example, if a Behavior is supposed to increase the value of an Attribute when that Behavior receives a Message, the Print Block can show the Attribute’s value on the Console so you can check whether it’s changing correctly or not.

#### Comment

A type of Block that you can attach to others in Design Mode that performs no in-game logic or function but can display text for others to read. Stencyl’s game engine ignores Comment Blocks entirely when running a game. This type of Block is typically used when an individual wants to explain how the logic in a Behavior works to someone else. Comment Blocks can show a single line of text or multiple lines of text.

#### Console

A special window that shows the internal functions occurring in your game. You can bring up the Console when testing a Flash-based game by pressing the ~ key. Attribute values can be tracked and displayed in the Console via the Print Block. For games made for iOS devices, the Console refers to the native Console App that appears when testing a game in the iOS Simulator on a Mac.

#### Stack Trace

A list of all the logic that has occurred when running Stencyl, in chronological order, while the program is running, including when testing a game. The Stack Trace is shown in Logs.

#### Logs

Logs are files that show text of the Stack Trace for Stencyl. When Stencyl or a game reports an error, the Logs can often help determine what the problem is. You can generate Logs for Stencyl by clicking on the Debug option and selecting Generate Logs. The Logs will be output to a location of your choice on your computer (for example, your computer’s desktop).

## Scene Terminology

#### Scene

A “level” or area in a game. A Scene can also be used for menus, cutscenes, titles, and end credits. A user can create Scenes in the Scene Editor.

#### Region

An arbitrary, invisible (unless you’re debugging your game and use a specific Block to make it visible) rectangular area in a Scene. You can perform logic on Actors (via Behaviors) that enter Regions, for example using a Region as a transition point between Scenes.

#### Terrain

Rather than using a grid of Tiles, a user can create Terrain, a surface that Actors can collide with, that has an arbitrary number of points. This is useful when a user wants to create highly customized collision shapes (though custom collision shapes are also possible with Tiles).

#### Joint

A connection between two Actors that a user can add in the Scene Editor. There are three types: Stick Joint, a straight, immobile connection between two Actors; a Hinge Joint, a connection that can bend, like a hinge; and a Sliding Joint, a connection that Actors can slide along.

#### Layer

A plane of Tiles organized by depth. The “lowest” Layer will be drawn first, and “higher” Layers will be drawn on top of the lower ones. A user can create an arbitrary number of Layers in a Scene.

#### Tile

A rectangular graphic that can have collision bounds applied to it. Tiles are organized into Tilesets and are used to make Scenes. A user can select different collision shapes to apply to a given Tile or no collision shape. A user can place Tiles on the same or different Layers. A Tile can have any arbitrary rectangular shape and size, i.e. square or rectangular. Common sizes include 16 x 16, 32 x 32, 48 x 48, and 64 x 64.

#### Tileset

A collection of Tiles used to draw collision surfaces, and scenery Actors can’t collide with, in a Scene. A Tileset has a maximum size of 2,880 x 2,880 pixels for Web (Flash) games and 1,024 x 1,024 (at standard, non-retina resolution) for iOS games. All Tiles in a Tileset will have the same rectangular dimensions a user chooses when uploading, or creating, a Tileset.

#### Camera

Where in a Scene the viewport (the screen size for a game) is focused. There are a number of Blocks that can move the viewport. For example, the Camera could be locked to the player’s Actor and follow that Actor around. The Camera can scroll automatically. The Camera could also be fixed, for example in puzzle games where the Scene’s size matches the screen size.

#### Background

An image drawn behind (below) the lowest layer of Tiles. A user can add a Background via the Background Editor.

#### Foreground

An image drawn in front of the highest Layer of Tiles.

#### Instance Customization

The ability to change the non-hidden Attribute values associated with an individual Actor’s Behavior(s). You can change an Actor’s Behavior(s)’ Attribute values by right-clicking on an Actor in the Scene Editor and clicking “Customize Behavior.”

## Game Terminology

#### Game

A type of file Stencyl uses to hold all of your game’s information, essentially the collection of graphics, sounds, and gameplay logic (Behaviors) that make up a game. There are three types of games you can make, Web, Desktop and Mobile. Web games are exportable in SWF format (for use with the Flash player) or JS format (for HTML5). Desktop games are exported as .EXE (Windows executables) and .APP (Mac app bundles). Mobile games are exportable as .IPA files for use with iOS-based (Apple) devices and .APK files for use with Android-based devices.

#### Kit

A template for a game. Kits already include a number of Behaviors to make a game in a specific genre. Kits are designed to make it easy to make a game in a given genre. Some of the Kits that Stencyl offers include the Jump & Run Kit, for making platformers; and the Space Shooter Kit, for making scrolling shoot-em-up games. Users can create new Kits to share with others.

#### Preloader

The screen that appears before a game starts. The Preloader can be used to show a custom logo in a splash screen. The Stencyl logo appears either after the preloader screen or as a badge in the lower-right corner of the preloader. You can have the default Stencyl splash screen removed by purchasing a license for Web games. The splash screen does not exist for iOS games and is instead represented by a watermark.

#### Site Lock

The ability to make a game playable only on designated websites, for example for sponsored Web games.

## Graphics / Drawing

#### Actor Space

When drawing text or custom shapes, this refers to an Actor as the point of origin for whatever is being drawn. Whatever is drawn will have its origin as the upper left corner (0, 0) of the Actor.

#### Screen Space

When drawing text or custom shapes, this refers to a the screen as the point of origin for whatever is being drawn. Whatever is drawn will have its origin as the upper left corner (0, 0) of the screen window.

## Products

#### Stencyl (previously known as StencylWorks)

Stencyl’s game development toolset.

#### StencylForge

A web-based service accessible from inside Stencyl, that allows you to share game assets with others and download game assets that others have uploaded.

## Areas of the Toolset

#### Welcome Center

The screen you see when you open Stencyl. You can select a Game or Kit to work on or create a new Game or Kit.

#### Dashboard

The hub from which you can access other Editors, and game assets, in a Game or Kit in Stencyl.

#### Actor Editor

An Editor in Stencyl that allows you to create and customize Actor Types, from Animations to the Behaviors attached to an Actor Type.

#### Background Editor

An Editor in Stencyl that allows you to upload images to use as backgrounds and foregrounds, and set scrolling speeds for them.

#### Scene Editor

An Editor in Stencyl that allows you to create and edit Scenes, and place Actors in a game’s Scenes. The Inspector pane (added in 2.x) is a properties pane that allows you to customize Actors on the fly.

#### Tileset Editor

An Editor in Stencyl that allows you to upload and edit Tilesets, including setting up Animations and collision bounds for individual Tiles.

#### Design Mode

Stencyl’s visual code editor, which uses Blocks that can snap into one another, to create game logic. Design Mode can be used to create Actor Behaviors and Scene Behaviors. Stencyl’s Design Mode visual code Block system is based on MIT’s Scratch software and is used with permission. Note that code written in specific programming languages (depending on the platform the game is targeting) can also be embedded in Blocks.

#### Code Mode

A development environment, built into Stencyl, that allows you to use different common programming languages to create Behaviors.

## Technologies

#### Haxe

A multi-platform language similar to JavaScript and ActionScript that cross-compiles to Flash bytecode, JavaScript and C++. This enables exporting to most commercially important platforms (Flash, HTML5, Windows/Mac/Linux, iOS, Android) from a single codebase.

#### OpenFL (and Lime)

A reimplementation of the Flash API within Haxe. Effectively, allows a game or an engine to be written in a Flash-like manner and exported to all platforms. OpenFL stands for Open Flash Library.

#### Box2D

A free, open-source physics engine, created by Erin Catto, that Stencyl uses to provide physics for games.

#### Objective-C

A programming language, developed by Apple, used to write software programs that can run on iOS devices (iPhone, iPad, Apple TV). In Stencyl 3.0 and beyond, Objective-C can be used in extensions to enhance games with native functionality.
