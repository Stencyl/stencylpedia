# User Input > Mobile-Only

***

> **Note:** These blocks only work on iOS and Android. They have no effect on other platforms (or return 0/-1/useless values).

***

## Accelerometer

### <a name="accelerometer"></a> Accelerometer Value

![x of accelerometer](https://static.stencyl.com/pedia2/block-images/input/mobile/accelerometer.png)

Returns the current values for the [accelerometer](https://www.stencyl.com/help/view/mobile-accelerometer/).

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
Input.accelZ
```

***

## Gestures

### <a name="swipe-detect"></a> Swiped

![swiped up](https://static.stencyl.com/pedia2/block-images/input/mobile/swipe-detect.png)

Returns `true` if the user has swiped [up/down/left/right]. A swipe is defined as touching the screen, sliding the finger and then releasing.

```
Input.swipedUp
Input.swipedDown
Input.swipedLeft
Input.swipedRight
```

#### Alernate Approach: Events

![swipe-event](https://static.stencyl.com/help/images/mobile-input-5.png)

We recommend using a swipe event instead of a swipe block. It's easier to work with.

***

## Other

### <a name="show-hide-keyboard"></a> Show / Hide Keyboard

![hide keyboard](https://static.stencyl.com/pedia2/block-images/input/mobile/show-hide-keyboard.png)

Immediately shows or hides the [virtual keyboard](https://www.stencyl.com/help/view/mobile-features/). Use mobile keyboard events to track what's been typed.

![example](https://static.stencyl.com/help/images/mobile-features-3.png)

```
hideKeyboard();
showKeyboard();
```

***

### <a name="set-keyboard-text"></a> Set Keyboard Text

![set keyboard text to text](https://static.stencyl.com/pedia2/block-images/input/mobile/set-keyboard-text.png)

Imagine that the keyboard is inputting into an invisible text field. This sets the text that's in that text field.

```
setKeyboardText([TEXT]);
```

***

### <a name="clear-keyboard-text"></a> Clear Keyboard Text

![clear keyboard text](https://static.stencyl.com/pedia2/block-images/input/mobile/clear-keyboard-text.png)

Imagine that the keyboard is inputting into an invisible text field. This clears out the text that's in that text field.

```
setKeyboardText("");
```

***

### <a name="vibrate"></a> Vibrate

![vibrate for number secs](https://static.stencyl.com/pedia2/block-images/input/mobile/vibrate.png)

[Vibrates](https://www.stencyl.com/help/view/mobile-features/) the device for the given number of seconds. On some devices, vibration duration cannot be controlled.

```
vibrate([NUMBER]);
```

***
