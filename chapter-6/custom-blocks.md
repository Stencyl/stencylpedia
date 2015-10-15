## Contents

* What are Custom Blocks?
* How to Make Custom Blocks
* Using Custom Blocks
* Global Custom Blocks
 

## What are Custom Blocks?

As its name implies, a custom block is a block you implement yourself. It is a wrapper block (like the "Always" or "When Created" wrappers) that can hold virtually any blocks that you need it to. You can then use this block anywhere else in the behavior.

What's the benefit of a custom block?

#### Code Reuse
You can reuse the code across a behavior. Bugs frequently happen when you copy a portion of code and reuse it in other places. If you make a change to one copy and forget to edit all copies, that's a bug waiting to happen.

#### Data In/Out
You can pass data (parameters) to a Custom Block and take back a return value.

> Programmers: Custom Blocks are equivalent to **functions / methods.**
 

## How to Make Custom Blocks

Let's make a custom block that returns the distance between 2 actors.

 
#### Step 1: Getting Started

Pick out the "Event" for Custom Blocks.

![Events Menu](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-1.png)

The custom block will appear in the working area. Click on the Create Custom Block button...

![Created Template](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-2.png)

You'll now see a dialog like this.

![Custom Blocks Opener](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-3.png)

#### Step 2: Give the block a Name

Self explanatory.

#### Step 3: Give it Fields (Parameters)

Parameters are the values that a block takes in. In this example, the values are the two actors we're trying to calculate the distance between.

First, click the + button...

![Adding parameters](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-5.png)

Then, pick what type of parameter you want (in this case, both will be Actors) and what the name is. This is the name that will appear in the block itself, so make it descriptive.

![Adding parameters](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-4.png)


#### Step 4: Define the Block's Appearance

The spec field describes how the block will appear to the user.

![Defining the spec](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-6.png)

The % fields correspond to the parameters you defined in Step 3, and to tell what you type in, refer back to the **Reference for Block Spec Field** column above. In this case, %1 corresponds to Actor1 and %2 corresponds to Actor2.

![What the block looks like](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-8.png)

#### Final Step: Choose a "Return Type"

At the bottom, you can also select a Return Type, which is what will be reported back to the behavior whenever this block is used.

![Return Type](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-7.png)

In this example, we want the block to calculate the distance between actors and give us back a positive number, so I've selected **Number** as the return type. As a result, the custom block can now be used anywhere a Number attribute would go in the behavior!

![Return Type](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-9.png)

> Note that you can select None, in which case the block will just perform its actions but not report anything back. In programming languages, "none" is equivalent to "void" as a return type.

 

## Using Custom Blocks

Now that we've created a custom block, let's use it. Where can you find it?


#### Custom Blocks reside inside the "Custom" category of the Palette

Custom blocks are organized by behavior. Those created inside an Actor/Scene versus a standalone behavior will be under a header that looks like ActorEvents_1 or SceneEvents_1.

![Custom Blocks Palette](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-10.png)

 
#### Implementing a Custom Block

Now that we've defined the wrapper for a custom block, it's time to implement it. 

The short summary is this:

1. **Drag in the parameter blocks** to use them in your custom block's implementation.
  <br/>![Dragging in parameters](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-13.png)

2. **If your custom block returns a value, use the return block to do so.**
  <br/>![Returning a value](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-12.png)


#### Using a Custom Block

Custom blocks with "None" as a return value will work like action blocks.

Otherwise, custom blocks that return a value will act like blocks of that type. For example, our distance block acts like a number block **because we set the return type to number**.

![Usage of custom block](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-15.png)
 

## Global Custom Blocks

> **Programmers:** Global Custom Blocks are equivalent to static functions

Global Custom Blocks are custom blocks that can be used in any behavior. You may have noticed this as an option when first creating the custom block.

![Global Custom Blocks](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-11.png)

What is the catch? **You can't refer to any of a behavior's attributes from within the custom block's implementation.**

Why do you think this is the case?

A global custom block isn't tied to any behavior at all. Because it lacks a "home," it's unable to refer to a behavior's attributes. On the flip side, the advantage to a global custom block is that it can be used from anywhere in the game. This can be convenient for game-wide functionality such modifying a game's score, which is frequently stored inside of a game attribute.

![Global Custom Blocks](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-17.png)

![Global Custom Blocks](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-6/images/custom-blocks-16.png)
