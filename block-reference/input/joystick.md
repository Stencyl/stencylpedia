# User Input > Joystick

***

> Read our guide on [Joysticks](http://www.stencyl.com/help/view/mobile-joystick/) before consulting this reference.

***

## Joystick

### <a name="joystick-add-static"></a> Add a Static Joystick

![create static joystick int at x number y number](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-add-static.png)

Adds a new static joystick to the screen at the given coordinates. A static joystick works only if you touch or click inside its outer radius. Other touches or clicks outside its outer radius will be ignored. Static doesn't mean immovable: you can move a static joystick by using the `set center for joystick` block.

```
Joystick.addJoystick([INT], [NUMBER], [NUMBER], 0, 0, 0, 0, 0, false);
```

***

### <a name="joystick-add-relative"></a> Add a Relative Joystick

![create relative joystick int at x number y number with touch region x number y number w number h number](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-add-relative.png)

Adds a new relative joystick to the screen. For a relative joystick its center position is relative to the coordinates of mouse or touch first press. A relative joystick works only inside its own touch region.

```
Joystick.addJoystick([INT], [NUMBER], [NUMBER], 1, [NUMBER], [NUMBER], [NUMBER], [NUMBER], false);
```

***

### <a name="joystick-remove"></a> Remove a Joystick

![remove joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-remove.png)

Removes a joystick from the screen.

```
Joystick.removeJoystick([INT]);
```

***

### <a name="joystick-set-default-direction"></a> Default Direction

![set default direction to number in degrees for joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-default-direction.png)

The direction of the joystick will be set to this default direction when the joystick is idle.

Useful when you want an actor to face towards a particular direction when the player doesn't press the joystick. The default value of default direction is 0.

```
Joystick.setDefaultDirection([INT], [NUMBER]);
```

***

### <a name="joystick-set-radius"></a> Set Radius

![set outer radius to number for joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-radius.png)

Sets the inner or the outer radius to a given value for a joystick.

The default value of the outer radius is half the width of the outer joystick.
The default value of the inner radius is half the width of the inner joystick.

```
Joystick.setJoystickRadius([INT], true, [NUMBER]); //outer joystick
Joystick.setJoystickRadius([INT], false, [NUMBER]); //inner joystick
```

***

### <a name="joystick-set-region"></a> Set Touch Region (for a Relative Joystick)

![set touch region to x number y number w number h number for relative joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-region.png)

Sets the x position, y position, the width and the height of the touch region of a joystick. You can use this block to update the position and/or the size of a touch region of an existing relative joystick.

```
Joystick.setTouchRegionForRJ([INT], [NUMBER], [NUMBER], [NUMBER], [NUMBER]);
```

***

### <a name="joystick-set-center"></a> Set Center Coordinates

![set center to x number y number for joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-center.png)

Sets the center position of a joystick.

```
Joystick.setJoystickCenter([INT], [NUMBER], [NUMBER]);
```

***

### <a name="joystick-set-image"></a> Set Joystick Images

![set image to text for outer joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-image.png)

Sets the image of the outer or inner part of a joystick. You need to have corresponding images inside your games "extras" folder, one for each scale:

```
imagename.png
imagename@1.5x.png
imagename@2x.png
imagename@3x.png
imagename@4x.png
```

```
Joystick.setJoystickImage([INT], true, [TEXT]); //outer joystick
Joystick.setJoystickImage([INT], false, [TEXT]); //inner joystick
```

***

### <a name="joystick-set-alpha"></a> Set Joystick Transparency

![set opacity to number for released outer joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-alpha.png)

Sets the joystick image transparency for a joystick.

```
Joystick.setJoystickAlpha([INT], true, [NUMBER], true); //outer joystick when released
Joystick.setJoystickAlpha([INT], true, [NUMBER], false); //outer joystick when pressed
Joystick.setJoystickAlpha([INT], false, [NUMBER], true); //inner joystick when released
Joystick.setJoystickAlpha([INT], false, [NUMBER], false); //inner joystick when pressed
```

***

### <a name="joystick-set-always-hide"></a> Auto-hide a Joystick

![always hide joystick int when touch or mouse is released](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-set-always-hide.png)

Makes a relative joystick to be always hidden when it is idle. Since the position of a relative joystick is not so important, you can use this block to always hide a relative joystick id when there is no press to save some screen space.

```
Joystick.alwaysHideRJ([INT]);
```

***

### <a name="joystick-is-pressed"></a> Joystick is Pressed

![joystick int is pressed](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-is-pressed.png)

Returns 'true' if the joystick is being pressed, 'false' otherwise.

```
Joystick.isJoystickPressed([INT])
```

***

### <a name="joystick-get-distance-direction"></a> Distance / Direction

![direction of joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-get-distance-direction.png)

Returns the distance or the direction of a joystick.

Distance is always a float number between 0 and 1.
Direction is always a float number between 0 (inclusive) and 360 (exclusive), where 0 means that the joystick is facing towards right, and 90 means that the joystick is facing down.

```
Joystick.getJoystickDisDir([INT], false) //direction
Joystick.getJoystickDisDir([INT], true) //distance
```

***

### <a name="joystick-get-center"></a> Jostick Center Coordinates

![x center of joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-get-center.png)

Returns the x or the y coordinate of the center of a joystick.

```
Joystick.getJoystickCenter([INT], true) //x
Joystick.getJoystickCenter([INT], false) //y
```

***

### <a name="joystick-get-radius"></a> Joystick Radius

![outer radius of joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-get-radius.png)

Returns the outer or inner radius value for a joystick.

```
Joystick.getJoystickRadius([INT], true) //outer joystick
Joystick.getJoystickRadius([INT], false) //inner joystick
```

***

### <a name="joystick-get-touch-region-property"></a> Touch Region (for a Relative Joystick)

![touch region x for relative joystick int](http://static.stencyl.com/pedia2/block-images/input/joystick/joystick-get-touch-region-property.png)

Returns the position or size of the touch region for a relative joystick.

```
Joystick.getTouchRegionPropertyForRJ([INT], 1) //x
Joystick.getTouchRegionPropertyForRJ([INT], 2) //y
Joystick.getTouchRegionPropertyForRJ([INT], 3) //width
Joystick.getTouchRegionPropertyForRJ([INT], 4) //height
```

***
