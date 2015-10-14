## Contents

* What are Custom Blocks?
* How to Make Custom Blocks
* Using Custom Blocks
* Global Custom Blocks
 

## What are Custom Blocks?

As its name implies, a custom block is a block you implement yourself. It is a wrapper block (like the "Always" or "When Created" wrappers) that can hold virtually any blocks that you need it to. You can then use this block anywhere else in the behavior.

What's the benefit of that?

####Code Reuse
You can reuse the same bunch of code across the behavior. Bugs frequently happen when you copy the same code everywhere, make a change and forget to edit it all the places.

####Data In/Out
You can pass data (parameters) to a Custom Block and take back a return value.

> Programmers: Custom Blocks are equivalent to **functions / methods.**
 

## How to Make Custom Blocks

Let's make a custom block that returns the distance between 2 actors.

 
#### Step 1: Getting Started

Pick out the "Event" for Custom Blocks.

![Events Menu](http://static.stencyl.com/pedia2/ch5/custom/image0.png)

You'll now see a dialog like this.

![Custom Blocks Opener](http://static.stencyl.com/help/images/CustomBlocks1.png)

#### Step 2: Give the block a Name

Self explanatory.

#### Step 3: Give it Fields (Parameters)

Just click the + button in the block fields and you can select what parameters will be added to the list expected by the Custom Block.

#### Step 4: Define the Block's Appearnce (some call this a "signature")

This one's tricky to put into words. Basically, this is how the block will appear to the user. The % fields are the blanks in the field. You can see in the Fields table what the % fields are.

![Block Example](http://static.stencyl.com/help/images/CustomBlocks2.png)

#### Final Step: Choose a "Return Type"

At the bottom, you can also select a Return Type, which is what will be reported back to the behavior whenever this block is used.

Note that you can select None, in which case the block will just perform its actions but not report anything back.

> **Programmers:** Selecting none is equivalent to "void" as a return type.

In this example, we want the block to calculate the distance between actors and give us back a positive number, so I've selected the Return Type of Number. As a result, the custom block can now be used anywhere a Number attribute would go in the behavior!

 

## Using Custom Blocks

Now that we've created a custom block, you can find the new block in your behavior at the very bottom below the other wrappers, and the custom block that you use to invoke it is in the palette as shown below.

#### Custom Blocks reside inside the "Custom" category of the Palette

Notice that there are other custom blocks that I made before, they're listed by the name of the behavior they're created inside of.

You may even notice that one is shaped like the True/False blocks, which is because it returns a Boolean value (which is either true or false, of course).

![Custom Blocks Palette](http://static.stencyl.com/help/images/CustomBlocks3_Palette.png)

#### Using a Custom Block
Like any ordinary block, drag a Custom Block in to use it.
 
> **Note:** The rest of this section completes the "distance between actors example that the original author started. Feel free to follow along or skip down to **Global Custom Blocks** to continue with the rest.

Now, we still haven't actually done anything yet to tell the custom block to actually DO anything. Below, you can see an image where I've grabbed all the necessary blocks for our needs. Notice there are two arrows that show you how to use the parameters.

You can grab the "Actor1" and "Actor2" blocks from the Custom Block's wrapper and use them inside of it as necessary anywhere an Actor attribute would be used. If you had used different parameter types (such as Number, etc) then you could use those in their appropriate fields instead.

![Custom Blocks Detail](http://static.stencyl.com/help/images/CustomBlocks4.png)

Below you can see it in it's final assembled state. Notice that the calculations have been put into a Return block (found under Messaging > Custom Blocks > Return Values) that will return the result of those calculations.

![Custom Blocks Assembled](http://static.stencyl.com/help/images/CustomBlocks5.png)

Now you can drag your custom block from the palette anywhere you want to use it! Using this block, I can now measure the X distance between any two actors.

![Custom Blocks Final](http://static.stencyl.com/help/images/CustomBlockFinalPic.png)

In this case I set a Number Attribute called "Distance" to the result of the custom block (the returned value), but you could just as easily use it elsewhere where numbers are needed.
 
###Examples would be things like the following:

* Inside an IF conditional check that compares the distance between two actors to another number value, such as AI trigger (have the enemy start chasing the player when he gets too close!).
* To add the distance values to a list for all enemies in the scene (using the "For each actor of type" wrapper and the "The Actor" block as the second parameter).
* As the width of a line or box being drawn between two actors.
* Converted to text and displayed on the screen as a measurement.
* And many many more!
 

## Global Custom Blocks

> **Programmers:** Global Custom Blocks are equivalent to static functions

Global Custom Blocks are custom blocks that can be "called" from any behavior. You may have noticed this as an option when first creating the custom block.

![Where to create global custom blocks](http://static.stencyl.com/pedia2/ch5/custom/image0.png)

The catch? **You can't refer to any of a behavior's attributes from within the custom block's implementation.**

Why do you think this is the case?

A global custom block isn't tied to any behavior at all. It lacks a "home," so it's unable to refer to a behavior's attributes. On the flip side, the advantage to a global custom block is that it can be used from anywhere. This can be convenient for game-wide functionality such modifying the a game's "score."
