# User Input > Keyboard & Mouse

***

## Keyboard

### Key Status

![repeat-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/RepeatBlock.png)

Repeats the wrapped blocks a given number of times.

```
for(var index0:int = 0; index0 < [NUMBER]; index0++) {
  [ACTIONS]
}
```

***

### Special Key is Down

***

### Simulate Keys

***

### Get Key Code

***

## Mouse / Touch

Mouse and Single Touch (vs. Multi-Touch) are handled using the same blocks, as described in our [Touch article](http://www.stencyl.com/help/view/mobile-input/).

### Mouse / Touch Status

![status-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/Status.png)

Returns `true` if the mouse [is down, was pressed, was released].

```
isMouseDown()
isMousePressed()
isMouseReleased()
```

***

### Mouse on Actor / Touched Actor

![actor-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/Actor.png)

Returns `true` if the mouse [is down on, was pressed on, was released on] the given actor.

```
[ACTOR].isMouseDown()
[ACTOR].isMousePressed()
[ACTOR].isMouseReleased()
```

***

### Mouse / Touch Position

![position-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/Position.png)

Returns the last known (x,y) position of the [mouse (cursor), mouse press, mouse release]. Before using mouse press/release, first check if the mouse has been pressed or released.

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

### Mouse Cursor

![cursor-block](http://static.stencyl.com/pedia2/blocks/user_input/mouse/MouseCursor.png)

Shows or hides the mouse cursor. Doesn't apply to mobile games. Useful for implementing custom cursors (using an actor that follows the mouse).

```
hideCursor()
showCursor()
```

***
