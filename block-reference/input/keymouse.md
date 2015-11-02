# User Input > Keyboard & Mouse

***

> Read our article on [Controls](http://www.stencyl.com/help/view/controls/) for more information on handling user input.

***

## Keyboard

### <a name="keystate"></a> Key Status

![key-block](http://static.stencyl.com/pedia2/blocks/user_input/keyboard/KeyState.png)

Returns `true` if the given [control](http://www.stencyl.com/help/view/controls/) [is down, was pressed, was released].

State | Description
--- | ---
is down | Key is currently pressed down.
was pressed | Key was **just** pressed down. Called once per press-release cycle.
was released | Key was **just** released. Called once per press-release cycle.

```
isKeyDown([CONTROL])
isKeyPressed([CONTROL])
isKeyReleased([CONTROL])
```

***

### <a name="is-special-down"></a> Special Key is Down

![special-block](http://static.stencyl.com/pedia2/blocks/user_input/keyboard/Special.png)

Returns `true` if [shift / ctrl] is currently being held down. On a Mac, ctrl is equivalent to command.

```
isShiftDown()
isCtrlDown()
```

***

### <a name="simulate-key"></a> Simulate Keys

![special-block](http://static.stencyl.com/pedia2/blocks/user_input/keyboard/Simulate.png)

Simulates a key [press / release] using the given control. Primarily used for implementing virtual controls as on-screen buttons in mobile games. Could also be used to make cutscenes.

```
simulateKeyPress([CONTROL]);
simulateKeyRelease([CONTROL]);
```

***

### <a name="keycode"></a> Get Key Code

![special-block](http://static.stencyl.com/pedia2/blocks/user_input/keyboard/Code.png)

Returns the hardware code for certain keys [enter, backspace, shift, delete, ctrl / command]. Compare this number with the code returned by an **Any Key** event. Could be used to implement a text field.

```
Key.ENTER
Key.BACKSPACE
Key.SHIFT
Key.DELETE
Key.CTRL
```

#### Example

![keycode-example](http://static.stencyl.com/pedia2/ch3/controls/key-input-example.png)

A simple implementation of a text-field behavior. See the "Example: Text Input" section of our [Controls guide](http://www.stencyl.com/help/view/controls/) for an explanation.

***

## Mouse / Touch

Mouse and Single Touch (vs. Multi-Touch) are handled using the same blocks, as described in our [Touch article](http://www.stencyl.com/help/view/mobile-input/).

### <a name="mousestate"></a> Mouse / Touch Status

![status-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/Status.png)

Returns `true` if the mouse [is down, was pressed, was released].

State | Description
--- | ---
is down | Mouse button is currently pressed down.
was pressed | Mouse button was **just** pressed down. Called once per click-release cycle.
was released | Mouse button was **just** released. Called once per click-release cycle.


```
isMouseDown()
isMousePressed()
isMouseReleased()
```

***

### <a name="amousestate"></a> Mouse on Actor / Touched Actor

![actor-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/Actor.png)

Returns `true` if the mouse [is down on, was pressed on, was released on] the given actor.

State | Description
--- | ---
is down | Mouse button is currently pressed down.
was pressed | Mouse button was **just** pressed down. Called once per click-release cycle.
was released | Mouse button was **just** released. Called once per click-release cycle.

```
[ACTOR].isMouseDown()
[ACTOR].isMousePressed()
[ACTOR].isMouseReleased()
```

***

### <a name="mousexy"></a> Mouse / Touch Position

![position-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/Position.png)

Returns the last known (x, y) position of the [mouse (cursor), mouse press, mouse release]. Before using mouse press/release, first check if the mouse has been pressed or released.

> On mobile, only mouse press/release are available since there's no concept of a mouse hovering over the screen.

```
getMouseX()
getMouseY()
getMousePressedX()
getMousePressedY()
getMouseReleasedX()
getMouseReleasedY()
```

***

### <a name="mousedisp"></a> Mouse Cursor

![cursor-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/MouseCursor.png)

Shows or hides the mouse cursor. Doesn't apply to mobile games. Useful for implementing custom cursors (using an actor that follows the mouse).

```
hideCursor();
showCursor();
```

***
