## Contents

* Introduction
* Getting Attribute Values
* Setting Attribute Values
* Example: Revisiting the Level Selector
 

## Introduction

Attributes are often thought to be like "local variables" or variables that are linked to a behavior. What if you want to know the value of attributes from other behaviors? Or what if you want to change those other values?

![](http://static.stencyl.com/pedia2/ch7/getset/image07.png)
 
#### When would this be useful?

* An enemy might want to know a player's remaining health and pursue them more vigorously if they're low on health.
* You're creating a bunch of actors all at once, but you want to customize their values on the fly after creating them. For example, you could be making a bunch of enemies with random starting health points.
 

## Getting Attribute Values from Other Behaviors

#### Required Information

Getting an value of an attribute requires at least 2 pieces of information, sometimes 3.

* **Which Behavior** contains the attribute you want?
* **Which Attribute** do you want, for that behavior?
* (If applicable) From **which actor** do you want to pull the behavior + attribute from?


#### The Blocks
All of the blocks for getting (and setting) attribute values are located under **Behavior > Attributes**.

![](http://static.stencyl.com/pedia2/ch7/getset/image00.png)


#### How do you fill in the blanks?

This process is facilitated by Stencyl, but before we get to that, let's step back a bit and understand what each of the blanks mean, so you aren't lost when you browse your logic later on.

![](http://static.stencyl.com/pedia2/ch7/getset/image03.png)

1. The first blank lets you pick the **target Actor**. (For Scenes, there's no blank at all since it applies to the current Scene)
2. The second blank takes the [internal name](http://static.stencyl.com/pedia2/ch7/getset/image00.png) of the desired attribute.
3. The final blank takes the **name of the behavior** that contains the desired attribute.
 
Now that you know this, rest assured that **you don't need to type in the attribute and behavior names directly**.

Just click on the dropdown arrow for the blank, expand out Attribute Names and pick out the desired Attribute.

![](http://static.stencyl.com/pedia2/ch7/getset/image01.png)

Doing this will automatically fill out the field with the Attribute's internal name AND its Behavior's full name.

> **Aside:** The strange name: "ActorEvents_1" stems from the fact that the "Events" page for an Actor or a Scene is represented as a hidden behavior behind the scenes, as you may recall from Chapter 2's lesson on Events.
 

## Setting Attribute Values for Other Behaviors

Setting the value of an attribute is similar to getting it. The only difference is that you have to provide the value you wish to set the attribute to.

![](http://static.stencyl.com/pedia2/ch7/getset/image05.png)

> **Note:** Take care to set the values to the appropriate type. That is to say, don't try dumping a text value into a Boolean attribute. This will cause errors at compile-time or run-time.
 

## Example: Revisiting the Level Selector

Back in Chapter 4, we made a [Level Selector](http://www.stencyl.com/help/viewArticle/118/) for the Changing Scenes lesson.

<a href="http://static.stencyl.com/pedia2/ch4/changing/LevelSelect.swf">![](http://static.stencyl.com/pedia2/ch4/changing/image12.png)</a>

In this example, we used an Attribute setter block to assign each level button a number corresponding to the scene it would lead to (and what number it would visually display on the button itself).

![](http://static.stencyl.com/pedia2/ch7/getset/image06.png)

> **Note:** The +1 is to account for the fact that computers count, starting from 0, but it would look strange to a regular player to see "Level 0"
 

## Summary

* You can get and set the values of attributes contained in other behaviors.
* Just use the dropdowns to fill in the blanks. Don't type in names directly.
