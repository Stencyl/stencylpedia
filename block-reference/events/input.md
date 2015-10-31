# Events > Input

***

> Read our articles on [Controls](http://www.stencyl.com/help/view/controls/), [Touch & Gestures](http://www.stencyl.com/help/view/mobile-input/) and [Gamepads](http://www.stencyl.com/help/view/gamepads/) for more information on handling user input.

***

## Universal

### Keyboard

![event-key-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/1%20-%20Input/event-key-press-release.png)

Triggers when any [Control](http://www.stencyl.com/help/view/controls/) is pressed or released.

***

### Any Key

![event-key-any-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/1%20-%20Input/event-key-any-press-release.png)

Triggers when any key is pressed/released (even those not mapped to controls). This is useful for creating user input fields.

The embedded `key code` block tells you the hardware code for the key. This is useful for special keys (such as backspace, enter, etc.) that can't be recognized as a letter or number.

![example](http://static.stencyl.com/pedia2/ch3/controls/keycode-example.png)

The embedded `character` block tells you what letter, number or character was pressed, if one was pressed.

***

### Focus

![event-focus-changed](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/1%20-%20Input/event-focus-changed.png)

Triggers when the game gains/loses focus. Useful for mobile apps for telling when your game has been sent to the background and later resumed.

***

## Universal (Works for Mouse & Touch)

### (Mouse) Click

![event-mouse-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/2%20-%20Input/event-mouse-press-release.png)

Triggers whenever the mouse pressed/released/moved/dragged.

***

### (Mouse) Click on Actor

![event-mouse-enter-exit-actor](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/2%20-%20Input/event-mouse-enter-exit-actor.png)

Triggers whenever the mouse enters/exits/presses/releases/drags on an actor.

***

### (Mouse) Click on Region

![event-mouse-enter-exit-region](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/2%20-%20Input/event-mouse-enter-exit-region.png)

Triggers whenever the mouse enters/exits/presses/releases/drags on a region.

***

## Mobile-Only

### Swipe

![event-device-swipe](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/3%20-%20Input/event-device-swipe.png)

Triggers whenever the device is swiped in the specified direction.

***

### Multi-Touch

![event-device-multitouch](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/3%20-%20Input/event-device-multitouch.png)

Detects multi-touch events. Use the mouse events for regular, single-touch detection. The embedded block tells you the position of the touch and the ID of the touch (so you can track a touch throughout its lifecycle).

Useful for on-screen virtual buttons (use the **On Screen Button** that we [ship](http://www.stencyl.com/help/view/pre-shipped-behaviors/) with Stencyl) or air hockey like games that require detection of independent finger motions.

***

## Desktop-Only

### Any Button (Gamepad)

![event-gamepad-any-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/4%20-%20Input/event-gamepad-any-press-release.png)

Triggers when any gamepad button pressed/released. Read our [Gamepad article](http://www.stencyl.com/help/view/gamepads/) for further details -- you are not meant to use this to implement gamepad controls, only to detect what controls to map to.

***
