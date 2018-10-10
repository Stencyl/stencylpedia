## Contents

* What are Lists? What are Lists useful for?
* List Structure
* Gotchas
* List Operations
* How to Create Lists
* Lists as Game Attributes
* Challenge: 2D Lists
 

## What are Lists?

If you've ever written a grocery list, you're prepared to use **lists** in Stencyl.

* Eggs
* Broccoli
* Bacon
* Salmon
* Corn Flakes
* Gallon of Water

As you'd expect, lists are best used to store collections of things. You can use lists for things like:

* Inventory
* Character stats
* Status effects
* Selecting random monsters to spawn

In general, lists can be a good option any time you want to keep track of lots of information.

> **Aside:** Internally, Stencyl uses lists to keep track of created actors, what points in a collision actually collided, and so on. If you've used any block that begins with "for each", you've actually used a list already!
 
 <br/>
 
 > **For Programmers:** Lists are mutable lists. They are equivalent to ArrayLists, Vectors, NSMutableArray or whatever you like to call them.
 

## List Structure

A list is an **ordered** collection of items. Each item in a list is made up of two parts:

1. A numerical index - in other words, where an item resides
2. A value
 
Think of a list as a 2-column table.

The first column is the index.
The second column is the value.

index | value
--- | ---
0 | eggs
1 | bacon
2 | cheese
3 | apples
4 | oranges
5 | salmon


## List Gotchas

* Indexes for lists **start at 0**, so the first item in a list starts at index 0, the second item is listed at index 1, and so forth.
 
* Don't work with indices beyond the maximum one (or below 0). Your game will crash if you do.
 
* **Lists don't necesarily have to contain data all of the same type**, but it is common practice to do so. If you mix up data types, it's your responsibility to keep track of this and process your data appropriately.
 

## List Operations

All blocks related to lists are located under **Attributes > Lists**.

**Operations**
* Add [ELEMENT] to [LIST]
* Insert [ELEMENT] at [INDEX] to [LIST]
* Replace item at [INDEX] with [ELEMENT] for [LIST]
* Remove [ELEMENT] from [LIST]
* Remove element at [INDEX] from [LIST]
* Remove all elements from [LIST]

**Getters**
* Get item at [INDEX] from [LIST]
* [LIST] contains [ELEMENT]
* Number of items in [LIST]
* [LIST] is empty?

**Creators**
* Create new list
* Create (shallow) copy of [LIST]
 
> **The Future:** We don't yet support reversing, combining or sorting lists, though these are all supported in a [3rd party extension](http://community.stencyl.com/index.php/topic,23821.0.html). We do, however, support [Maps/Dictionaries](http://www.stencyl.com/help/view/maps/).
 

## How to Create Lists

How do you create a List in the first place? Lists can be Attributes, so like any attribute, there are two ways of doing this.

1. **Configuring** the attribute with initial data.
2. **Creating it** at runtime inside a behavior and setting the attribute's value to that new list.

> Assume that for both cases, we have created a List Attribute called "myList".<br/>![](http://static.stencyl.com/pedia2/ch5/lists/image01.png)

#### Method 1: Configuring a List Attribute
After attaching a behavior with a List attribute to either an Actor or a Scene, you'll see this neat interface for adding initial data to the list.

![](http://static.stencyl.com/pedia2/ch5/lists/image02.png)

> **Note:** The second icon (the one under the +) lets you import a List from a text file. One line per entry. All entries will be treated as text.
 
#### Method 2: Creating it on the Fly
Alternatively, you can create a new list on the fly and begin filling it up.

![](http://static.stencyl.com/pedia2/ch5/lists/image03.png)

 
## Lists as Game Attributes

Lists can be used as Game Attributes. This can be pretty useful for defining stat tables and other large collections of data to use throughout the game.
 
#### Creating a List as a Game Attribute
Lists can be created as Game Attributes and pre-populated the same way as other lists, namely only with Numbers and Text.

![](http://static.stencyl.com/pedia2/ch5/lists/image04.png)

> **Note:** You are also allowed to dump in Lists into Lists at runtime as well as any other kind of data. If you plan to save your lists out (via Game Attributes), there are restrictions. Skip down to "Saving & Lists"

#### Setting the Value of a Game Attribute to a List
It should come as no surprise that you're able to set the value of a Game Attribute to a List.

![](http://static.stencyl.com/pedia2/ch5/lists/image05.png)

> **Note:** Assigning values simply gets the Game Attribute to "point" to your List. No copying is done, so modifying it modifies the one and only "copy" of that list.

#### Saving & Lists
As stated earlier, be careful when saving out lists as Game Attributes. They can only contain Numbers, Text and other Lists that follow the same rules.

 
## Summary

* Lists are collections of data.
* Every item in a list has an index (number) that tells you where, in that list, that item resides.
* Indices start from 0.
* You can do lots of things to lists and change them after creation.
 

## Challenge: Two-Dimensional Lists

Lists are great for storing sequential information, but what if you need to store a "grid" of data? It turns out that lists are powerful enough that you can store a **List within a List**, thereby bringing it up to 2 dimensions.

![](http://static.stencyl.com/pedia2/ch5/lists/image06.png)

Come up with a scenario in which you need a 2D list and implement it.

> **Disclaimer:** This challenge is just an exercise for practicing what you've learned. Part of what we're doing with Stencylpedia is getting you to think about the underlying concepts. Please do not regard this as best practice - it's just an exercise.


## Looking for a 2D list extension?

A veteran Stencyler has created a [handy extension](http://community.stencyl.com/index.php/topic,28081.0.html) for 2D lists.
