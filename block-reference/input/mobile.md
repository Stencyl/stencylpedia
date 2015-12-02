# User Input > Mobile-Only

***

> **Note:** These blocks only work on iOS and Android. They have no effect on other platforms (or return 0/-1/useless values).

***

## <a name="accelerometer"></a> Accelerometer

### Accelerometer Value

![accel-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Accel.png)

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

### <a name="swipe-detect"></a> Swiped

![swipe-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Swipe.png)

Returns `true` if the user has swiped [up/down/left/right]. A swipe is defined as touching the screen, sliding the finger and then releasing.

```
Input.swipedUp
Input.swipedDown
Input.swipedLeft
Input.swipedRight
```

#### Alernate Approach: Events

![swipe-event](http://static.stencyl.com/help/images/mobile-input-5.png)

We recommend using a swipe event instead of a swipe block. It's easier to work with.

***

## Joystick

### Add a Static Joystick

![joystick-add-static](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-add-static.png)

Adds a new joystick to the screen at the given coordinates.

```
Joystick.addJoystick(0,0,0,0,0,0,0,0,false);
```

***

### Add a Relative Joystick

![joystick-add-relative](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-add-relative.png)

Adds a new joystick to the screen, positioned relatively to the coordinates of mouse or touch presses.

```
Joystick.addJoystick(0,0,0,1,0,0,0,0,false);
```

***

### Remove a Joystick 

![joystick-remove](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-remove.png)

Removes a joystick from the screen.

```
Joystick.removeJoystick(0);
```

***

### Default Direction

![joystick-set-default-direction](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-set-default-direction.png)

The direction of the joystick will be set to this default direction when the joystick is idle.

```
Joystick.setDefaultDirection(0,0);
```

***

### Set Radius

![joystick-set-radius](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-set-radius.png)

Sets the inner or the outer radius to a given value for a joystick.

```
Joystick.setJoystickRadius(0,true,0);
```

***

### Set Touch Region (for a Relative Joystick)

![joystick-set-region](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-set-region.png)

Sets the x position, y position, the width and the height of the touch region of a joystick.

```
Joystick.setTouchRegionForRJ(0,0,0,0,0);
```

***

### Set Joystick Images

![joystick-set-image](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-set-image.png)

Sets the image of the outer or inner part of a joystick.

```
Joystick.setJoystickImage(0,true,"text");
```

***

### Set Joystick Transparency

![joystick-set-alpha](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-set-alpha.png)

Sets the joystick image transparency for a joystick.

```
Joystick.setJoystickAlpha(0,true,0,true);
```

***

### Auto-hide a Joystick

![joystick-set-always-hide](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-set-always-hide.png)

Makes a relative joystick to be always hidden when it is idle.

```
Joystick.alwaysHideRJ(0);
```

***

### Joystick is Pressed

![joystick-is-pressed](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-is-pressed.png)

Returns 'true' if the joystick is being pressed, 'false' otherwise.

```
Joystick.isJoystickPressed(0)
```

***

### Distance / Direction  

![joystick-get-distance-direction](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-get-distance-direction.png)

Returns the distance or the direction of a joystick.

```
Joystick.getJoystickDisDir(0,false)
```

***

### Jostick Center Coordinates

![joystick-get-center](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-get-center.png)

Returns the x or the y coordinate of the center of a joystick.

```
Joystick.getJoystickCenter(0,true)
```

***

### Joystick Radius

![joystick-get-radius](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-get-radius.png)

Returns the outer or inner radius value for a joystick.

```
Joystick.getJoystickRadius(0,true)
```

***

### Touch Region (for a Relative Joystick) 

![joystick-get-touch-region-property](http://static.stencyl.com/pedia2/block-images/3%20-%20User Input/2%20-%20Mobile-Only/joystick-get-touch-region-property.png)

Returns the position or size of the touch region for a relative joystick.

```
Joystick.getTouchRegionPropertyForRJ(0,1)
```
***

## Other

### <a name="show-hide-keyboard"></a> Show / Hide Keyboard

![keyboard-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Keyboard.png)

Immediately shows or hides the [virtual keyboard](http://www.stencyl.com/help/view/mobile-features/). Use mobile keyboard events to track what's been typed.

![example](http://static.stencyl.com/help/images/mobile-features-3.png)

```
showKeyboard();
hideKeyboard();
```

***

### <a name="set-keyboard-text"></a> Set Keyboard Text

![text-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/KeyboardText.png)

Imagine that the keyboard is inputting into an invisible text field. This sets the text that's in that text field.

```
setKeyboardText([TEXT]);
```

***

### <a name="clear-keyboard-text"></a> Clear Keyboard Text

![clear-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/ClearKeyboard.png)

Imagine that the keyboard is inputting into an invisible text field. This clears out the text that's in that text field.

```
setKeyboardText("");
```

***

### <a name="vibrate"></a> Vibrate

![vibrate-block](http://static.stencyl.com/pedia2/blocks/user_input/mobile/Vibrate.png)

[Vibrates](http://www.stencyl.com/help/view/mobile-features/) the device for the given number of seconds. On some devices, vibration duration cannot be controlled.

```
vibrate([NUMBER]);
```

***
