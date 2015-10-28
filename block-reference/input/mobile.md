# User Input > Mobile-Only

***

## Accelerometer

### Accelerometer Value

![accel-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Accelerometer.png)

Returns the current values for the [accelerometer](http://www.stencyl.com/help/view/mobile-accelerometer/). 

**Portrait Orientation**

Name | Description
--- | ---
X (Positive) | Right
X (Negative) | Left
Y (Positive) | Up
Y (Negative) | Down

**Landscape Orientation**

Name | Description
--- | ---
X (Positive) | Up
X (Negative) | Down
Y (Positive) | Left
Y (Negative) | Right

```
Input.accelX
Input.accelY
```

***

## Gestures

### Swiped

![swipe-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Swipe.png)

Returns `true` if the user has swiped [up/down/left/right]. A swipe is defined as touching the screen, sliding the finger and then releasing.

```
Input.swipedUp
Input.swipedDown
Input.swipedLeft
Input.swipedRight
```

***

## Joystick

> We will be replacing our built-in joystick plugin with this far better [third party one](http://community.stencyl.com/index.php/topic,29026.0.html) in the future. Consult our [Joysticks guide](http://www.stencyl.com/help/view/mobile-joystick/) for the moment.

***

## Other

### Show/Hide Keyboard

![keyboard-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Keyboard.png)

Immediately shows or hides the [virtual keyboard](http://www.stencyl.com/help/view/mobile-features/). Use mobile keyboard events to track what's been typed.

![example](http://static.stencyl.com/help/images/mobile-features-3.png)

```
showKeyboard();
hideKeyboard()
```

***

### Set Keyboard Text

![text-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/KeyboardText.png)

Imagine that the keyboard is inputting into an invisible text field. This sets the text that's in that text field.

```
setKeyboardText([TEXT]);
```

***

### Clear Keyboard Text

![clear-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/ClearKeyboard.png)

Imagine that the keyboard is inputting into an invisible text field. This clears out the text that's in that text field.

```
setKeyboardText("");
```

***

### Vibrate

![vibrate-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Vibrate.png)

[Vibrates](http://www.stencyl.com/help/view/mobile-features/) the device for the given number of seconds. On some devices, vibration duration cannot be controlled.

```
vibrate([NUMBER]);
```

***
