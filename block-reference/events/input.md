# Events > Input

***

> Read our articles on [Controls](https://www.stencyl.com/help/view/controls/), [Touch & Gestures](https://www.stencyl.com/help/view/mobile-input/) and [Gamepads](https://www.stencyl.com/help/view/gamepads/) for more information on handling user input.

***

## Universal

### <a name="event-key-press-release"></a> Keyboard

![when control is pressed](https://static.stencyl.com/pedia2/block-images/events/input/event-key-press-release.png)

Triggers when any [Control](https://www.stencyl.com/help/view/controls/) is pressed or released.

***

### <a name="event-key-any-press-release"></a> Any Key

![when any key is pressed](https://static.stencyl.com/pedia2/block-images/events/input/event-key-any-press-release.png)

Triggers when any key is pressed/released (even those not mapped to controls). This is useful for creating user input fields.

The embedded `key code` block tells you the hardware code for the key. This is useful for special keys (such as backspace, enter, etc.) that can't be recognized as a letter or number.

![example](https://static.stencyl.com/pedia2/ch3/controls/keycode-example.png)

The embedded `character` block tells you what letter, number or character was pressed, if one was pressed.

***

### <a name="event-focus-changed"></a> Focus

![when the game loses focus](https://static.stencyl.com/pedia2/block-images/events/input/event-focus-changed.png)

Triggers when the game gains/loses focus. Useful for mobile apps for telling when your game has been sent to the background and later resumed.

***

## Universal (Works for Mouse & Touch)

### <a name="event-mouse-press-release"></a> Clicked / Moved

![when the mouse is pressed](https://static.stencyl.com/pedia2/block-images/events/input/event-mouse-press-release.png)

Triggers whenever the mouse pressed/released/moved/dragged. For mobile-devices, triggers whenever a finger touches, releases or is dragged around the screen.

***

### <a name="event-mouse-enter-exit-actor"></a> Clicked / Moved on Actor

![when the mouse enters actor](https://static.stencyl.com/pedia2/block-images/events/input/event-mouse-enter-exit-actor.png)

Triggers whenever the mouse enters/exits/presses/releases/drags on an actor. For mobile-devices, triggers whenever a finger touches, releases or drags an actor.

***

### <a name="event-mouse-enter-exit-region"></a> Clicked / Moved on Region

![when the mouse enters region](https://static.stencyl.com/pedia2/block-images/events/input/event-mouse-enter-exit-region.png)

Triggers whenever the mouse enters/exits/presses/releases/drags on a region. For mobile-devices, triggers whenever a finger touches, releases or drags a region.

***

## Mobile-Only

### <a name="event-device-swipe"></a> Swipe

![when the device is swiped up](https://static.stencyl.com/pedia2/block-images/events/input/event-device-swipe.png)

Triggers whenever the device is swiped in the specified direction.

***

### <a name="event-device-multitouch"></a> Multi-Touch

![when touch is started](https://static.stencyl.com/pedia2/block-images/events/input/event-device-multitouch.png)

Detects multi-touch events. Use the mouse events for regular, single-touch detection. The embedded block tells you the position of the touch and the ID of the touch (so you can track a touch throughout its lifecycle).

Useful for on-screen virtual buttons (use the **On Screen Button** that we [ship](https://www.stencyl.com/help/view/pre-shipped-behaviors/) with Stencyl) or air hockey like games that require detection of independent finger motions.

***

## Desktop-Only

### <a name="event-gamepad-any-press-release"></a> Any Button (Gamepad)

![when any gamepad button is pressed](https://static.stencyl.com/pedia2/block-images/events/input/event-gamepad-any-press-release.png)

Triggers when any gamepad button pressed/released.

Read our [Gamepad article](https://www.stencyl.com/help/view/gamepads/) for further details -- you are not meant to use this to implement gamepad controls, only to detect what controls to map to or to build a control configuration component.

***
