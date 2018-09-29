> Looking for our article on [Gamepads (External Controllers)](http://www.stencyl.com/help/view/gamepads)?

## Contents

* Detecting the Keyboard
* Mouse
* Mouse Position
* Mouse over Actor
* Mouse Cursor
* Mobile Controls
* Example: 4 Way Motion
* Example: Text Input


## Detecting the Keyboard

Detecting keyboard input works differently in Stencyl than it does in other systems. We use the notion of a **Control** to make your keyboard controls **flexible** and **easy to remap**.

A Control is a name that you assign to an action in a game. For example, if we were designing a control scheme for a Mario game, it would look like this.

<img alt="NES-controller" src="http://static.stencyl.com/pedia2/ch3/controls/image05.png" style="height: 300px; width: 300px;">

Actions | Actual Buttons
--- | ---
Move Left | D-Pad (Left)
Move Right | D-Pad (Right)
Dash | B
Jump | A
Pause | Start


#### Setting up Controls in Stencyl

The same idea applies to Stencyl, through a game's Controls Page. To set Controls, click the Settings button, shown below, to open that dialog.

![Settings](http://static.stencyl.com/help/images/Settings-Button-New.png)

Next, click the Controls button to view the Controls pane. From there, you tell us the name of the Control and the button it maps to.

![Controls Page](http://static.stencyl.com/help/images/Settings-Controls.png)

Now, when you check whether a key is pressed, released or down, instead of checking directly on a certain key (such as spacebar), you check the state of the Control.

![stencyl-design-mode-check-keyboard-input](http://static.stencyl.com/pedia2/ch3/controls/image00.png)


#### Why can't we just check the key directly?

* What if you decide to change your control scheme? You'd have to change it everywhere.

* What if you wanted to make your control scheme configurable? That would be a mess. With Controls, you just change what key the Control is mapped to.

> **Note:** To reduce the amount of setup, all Stencyl games come pre-shipped with a default set of controls (arrow keys, action 1, action 2). You're free to edit them or delete them.
 

## Mouse

**Mouse Input** is detected through 3 different states.

* Pressed
* Released
* Down

![stencyl-design-mode-get-mouse-state](http://static.stencyl.com/pedia2/ch3/controls/mouse-basic.png)

**Pressed** and **Released** are one-off "events" - they **fire once per that action**, whereas "down" is a constant state that can be checked.

> Mouse presses and releases can also be detected using the **Click** event (under Add Event > Input)


## Mouse Position

You can also grab the (x,y) location of the mouse on screen or any recent presses/releases.

![stencyl-design-mode-get-mouse-location](http://static.stencyl.com/pedia2/ch3/controls/mouse-position.png)

 
## Mouse over Actor

Similarly, mouse input over an actor involves 4 different states.

* Pressed on Actor
* Released on Actor
* Down on Actor
* Over Actor

Over Actor is our term for **hovering** the mouse over the actor.

![stencyl-design-mode-get-mouse-location](http://static.stencyl.com/pedia2/ch3/controls/mouse-actor.png)

> Mouse presses and releases involving an actor can also be detected using the **On Actor** event (under Add Event > Input)

 
## Mouse Cursor

Sometimes, you want to hide the cursor or display a custom cursor. How do you do this?

To show or hide the cursor, use this block.

![stencyl-design-mode-hide-mouse-cursor](http://static.stencyl.com/pedia2/ch3/controls/hide-cursor.png)

> **Exercise:** How would you create a custom cursor? One method is to hide the cursor and create a dummy actor that continually follows the mouse but does not collide with anything.
 

## Mobile Controls

To keep things simple for you, mouse input is equivalent to single-touch input. Read our [Touch article](http://www.stencyl.com/help/view/mobile-input/) for further details and examples on both single touch, multi touch and gestures.

Other mobile input topics are covered separately.

* [Accelerometer](http://www.stencyl.com/help/view/mobile-accelerometer/)
* [Virtual Joystick](http://www.stencyl.com/help/view/mobile-joystick/)
 

## Example: 4 Way Motion

This example shows how to use the keyboard to implement a 4-way motion behavior. Up/Down/Left/Right are pre-defined controls that come with each game - they are not to be mixed up with the arrow keys with the same name.

![stencyl-design-mode-four-way-motion-example](http://static.stencyl.com/pedia2/ch3/controls/image06.png)

> **Note:** This is just an exercise to get you familiar with the blocks. We already [include](http://www.stencyl.com/help/view/pre-shipped-behaviors/) a 4-way motion behavior with Stencyl if you need one.

#### Exercises

* One drawback of this simple approach is that you can walk diagonally. How would you fix this?
* In this version, the player stops immediately after you lift the keys. Implement a version where the player slows down gradually.
 

## Example: Text Input

Sometimes the player input is not limited to a specific set of keys. Instead, the player is expected to enter in text. For example... 

* You want the player to enter in a name for a high score entry.
* A word game where the player has to enter letters.

To make this, you can use the **when any key is pressed/released** event for this kind of user input. Here is a brief example of a behavior that accepts user input and puts that into a text attribute.

![Example](http://static.stencyl.com/pedia2/ch3/controls/key-input-example.png)

#### Explanation

* The event is triggered when any key is pressed or released respectively. 
* The "character" block returns the character that has been generated by the event. 
* For example, if the player presses the A key, the character "a" is generated. 
* The example also takes modifier keys into account, so pressing A while holding the SHIFT key, generates the upper-case character "A".
* Pressing enter submits the whole phrase while pressing backspace will remove the last character. We explain this part next.

#### Gotcha: Special Keys (ENTER, BACKSPACE)

Special keys such as ENTER and BACKSPACE do not map to characters. To check if these keys have been pressed, use the **key code** block instead. This block returns a unique number for each keyboard key. 

It is best practice to compare the "key code" of the event with the "key code of [___]" block, rather than hardcoding the number directly. Like this.

![Keycode Example](http://static.stencyl.com/pedia2/ch3/controls/keycode-example.png)

For reference, the full list of key codes can be looked up [here](https://raw.githubusercontent.com/Stencyl/stencyl-engine/master/com/stencyl/Key.hx).

#### Exercise: Spot the Bug

There is a subtle bug in our example code above. Can you spot it?

> **Hint:** What happens if the text attribute has 0 characters?

#### Exercise: Create a Text Field for the player's name

* When the player clicks on the text field, wait for user input.
* Store the input in a text attribute.
* Draw the text that the player has entered.
* When the enter key is pressed, stop waiting for input.
* Challenge - Draw a blinking cursor when the text field is focused.


## Summary

* Detect key events by creating abstract controls and checking the state of those controls.
* Controls let you change the control scheme for your game from one place.
 

## Challenge: Button

Create a button that responds to Mouse controls but goes beyond just a one liner "when pressed, do something".

The button should work just like a regular button. Specifically, don't register a button click unless the gesture was both started and completed on the button.

> **Note:** Think of scenarios where simply detecting a release would be incorrect.


## Challenge: Cutscenes

We include a block for simulating key presses and releases. It's useful for creating on-screen buttons in mobile games that can act as if they were physical keyboard buttons.

![stencyl-design-mode-simulate-key-press-block](http://static.stencyl.com/pedia2/ch3/controls/image03.png)

It's also useful for creating cutscenes - in-game sequences that the player does not control but watches, like a movie. **Make a cutscene using this block**.
