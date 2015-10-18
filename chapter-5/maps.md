## Contents

* What are Maps?
* Creating Maps
* Operations
* Maps as Game Attributes
 

## What are Maps?

Maps (also known as dictionaries) let you store and access data using names as keys. Unlike lists, which are ordered and use numbers as keys, maps don't care about order and let you use textual names as keys.

For example, if you wanted to make a Map that associated Stencyl members with post counts, it'd look like this.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-basics-1.png)

Maps can also mix and match different types as values.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-basics-2.png)

Or, you could get fancier and use Maps as the data itself.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-basics-3.png)

 
## Maps vs. Lists

Maps are useful when you want to...

* Store many things but don't care about the order.
* Want to access things instantly.
* Prefer to refer to things by name.

Lists are better if you want to...

* Store things in a particular order.
* Sort or search for specific items in the list.
 

## Creating Maps

How do you create a Map in the first place? Maps can be attributes, so like any attribute, there are two ways of doing this.

1. Configuring the attribute with initial data.
2. Creating the map at runtime inside a behavior and setting the attribute's value to that newly created map.

> Assume that for both cases, we have created a Map Attribute called "myMap"

#### Method 1: Configuring a Map attribute
After attaching a behavior with a Map attribute to either an Actor or a Scene, you'll see this interface for adding initial data to the Map.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-setup.png)

#### Method 2: Creating a Map using blocks
Alternatively, you can create a new Map using blocks and begin filling it up.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-setup2.png)


## Operations

All blocks related to maps are located under **Attributes > Maps**.

**Operations**
* Set [KEY] to [VALUE] for [MAP]
* Remove [KEY] from [MAP]
* Remove all items from [MAP]

**Getters**
* Value of [KEY] from [MAP]
* [MAP] has [KEY]?
* [MAP] has [VALUE]?
* Number of items in [MAP]
* [MAP] is empty?
* Keys of [MAP] as list

**Create/Copy**
* Create new map
* Copy of [MAP]

**Looping**
* For each [KEY] in [MAP]
 

## Maps as Game Attributes

Maps can be used as Game Attributes. This can be useful for defining tables and other large collections of data to use throughout the game.


#### Creating a Map as a Game Attribute
Maps can be created as Game Attributes and pre-populated the same way as other Maps, namely only with Numbers and Text.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-gameatt.png)

> **Note:** You may also dump Lists & Maps into Maps at runtime as well as any other kind of data. If you plan to save your Maps out (via Game Attributes), there are restrictions. Skip down to "Saving & Maps" under Caveats.
 
#### Setting the Value of a Game Attribute to a Map
As you may expect, you can set the value of a Game Attribute to a Map.

![](http://static.stencyl.com/pedia2/ch6/maps/maps-gameatt2.png)

> **Note:** Assigning values simply gets the Game Attribute to "point" to your Map. No copying is done, so modifying it modifies the one and only "copy" of that Map.
 
#### Gotcha: Saving & Maps
Be careful when saving out Maps as Game Attributes. Just like lists, they can only contain contain Numbers and Text.
