As we described in the Scene Basics section, scenes control a game's flow and can be thought of as various **states** in a **game** that you transition between, like a story.

![stencyl-scene-flow-diagram](https://static.stencyl.com/pedia2/ch4/changing/image06.png)


## Contents

* How To: Changing Scenes
* Gotchas
* Transitions
* Example: Enter Door, Switch Scene
* Example: Level Selector


## How To: Changing Scenes

Changing a scene involves 3 parts.

* What scene you want to go to next (or reload the same scene)
* The exit transition
* The entry transition

Use the following blocks (under Scene > Game Flow) to perform a scene change.

![stencyl-design-mode-switch-scene-blocks](https://static.stencyl.com/pedia2/ch4/changing/image01.png)

> If it isn't apparent, a reload will "switch" to the current scene.

 
## Gotchas

* **Don't perform 0 second transitions**. Instead, go with a low number such as 0.01, for stability.

* You cannot perform multiple scene changes at the same time. **Once a scene change is in progress, it must reach completion before another scene change is initiated**. Any new requests for scene changes will be ignored.


## Transitions

Transitions are visual effects that are applied during a scene change. You can select different transitions for the "out" and the "in" portion of a change.

Stencyl supports these transition types.

* Fade
* Blinds
* Bubbles
* Spotlight
* Blur
* Box
* Crossfade
 

## Example: Enter Door, Switch Scene

In this simple example, we'll make the hero enter the cave once he steps into the cave's door, represented by a [Region](https://www.stencyl.com/help/view/regions/).

I opted to use a "Actor Type Enters Region" event and placed a Region over the door to detect entry.

![stencyl-design-mode-switch-scene-using-door](https://static.stencyl.com/pedia2/ch4/changing/image05.png)


## Example: Level Selector

Building a Level Select screen is common to many games. Here's a simple and elegant way to make one.

<a href="https://static.stencyl.com/pedia2/ch4/changing/LevelSelect.swf">![stencyl-design-mode-level-selector-example](https://static.stencyl.com/pedia2/ch4/changing/image12.png)</a>
 

## The Concepts
To pull this off, I'll use the "get scene with name" block (Scene > World). This block returns a scene, given a name.

![stencyl-design-mode-get-scene-name-block](https://static.stencyl.com/pedia2/ch4/changing/image00.png)

Now, I can drag this block into our regular scene switch block. *(If you didn't know you could do that, now you know.)*

![stencyl-design-mode-switch-scene-drag-block](https://static.stencyl.com/pedia2/ch4/changing/image02.png)

Our goal is to make a simple behavior that we can reuse. To pull off a clean Level Select, our scenes have to have a predictable naming scheme. **How about we just give each level a number as a name, starting from 1**?

![stencyl-assigning-level-names](https://static.stencyl.com/pedia2/ch4/changing/image09.png)

If we do that, we can then pass a Number Attribute into the "get scene with name" block, and it will magically switch to the scene with that "name".

![stencyl-design-mode-switch-scene-get-scene-names](https://static.stencyl.com/pedia2/ch4/changing/image04.png)

 

#### The Implementation: Creating the Buttons
Putting this all together, here's a behavior that creates 5 Level Select buttons in a row, spaced apart by 100 pixels.

> **Exercise:** You should extend this, so that it wraps over and starts a new line upon hitting the 6th button)

![stencyl-design-mode-create-scene-switching-buttons](https://static.stencyl.com/pedia2/ch7/getset/image06.png)

> **Note:** The "for Last Created Actor, set ..." block is a [special block](https://www.stencyl.com/help/viewArticle/149/) that sets the value of a different Behavior's attribute. In this case, we're telling the block what Scene it's associated with, otherwise it wouldn't know which Scene to switch to and what to draw. We cover the concept of [setting attribute values of other behaviors](https://www.stencyl.com/help/viewArticle/149/) in Chapter 5.
 

#### The Implementation: The Buttons' Logic

Each Level Select button contains 2 Events and a single Number Attribute (called "SceneNumber" that tells the button what scene it should represent in the Level Select.

1) One event that draws the button.

![stencyl-design-mode-draw-button](https://static.stencyl.com/pedia2/ch4/changing/image03.png)

2) One event that switches the scene when the button is pressed.

![stencyl-design-mode-switch-scene-on-mouse-click](https://static.stencyl.com/pedia2/ch4/changing/image07.png)

That's it!

 

## Summary

* Scenes are the states in a game.
* Changing scenes involves an exit transition and entry transition.
* You can only perform one scene change at a time.


## Challenge: Actor's Position in "Next" Scene

In Zelda, when Link walks off the edge of a room, he naturally appears at the "right" spot in the next room.

For example, if he steps off the right side of a room, he will usually appear at the left side of the next room.

<object height="315" width="420"><param name="movie" value="http://www.youtube.com/v/o0I1TScPRMM?version=3&amp;hl=en_US"><param name="allowFullScreen" value="true"><param name="allowscriptaccess" value="always"><embed allowfullscreen="true" allowscriptaccess="always" height="315" src="http://www.youtube.com/v/o0I1TScPRMM?version=3&amp;hl=en_US" type="application/x-shockwave-flash" width="420"></object>

This turns out to be a challenge because you need to reposition your hero, based on where he came from before.
Fortunately, there's a block that can help you out (Scene > Game Flow).

![stencyl-design-mode-get-scene-name-block](https://static.stencyl.com/pedia2/ch4/changing/image00.png)

Use this block to implement a generic, reliable system for placing an actor at the "right" spot, much like the Zelda game does.
