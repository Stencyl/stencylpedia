# User Input > Joystick

***

> Read our guide on [Joysticks](http://www.stencyl.com/help/view/mobile-joystick/) before consulting this reference.

***

## Joystick

### Add a Static Joystick

![joystick-add-static](http://static.stencyl.com/pedia2/block-images/joystick/joystick-add-static.png)

Adds a new static joystick to the screen at the given coordinates. A static joystick works only if you touch or click inside its outer radius. Other touches or clicks outside its outer radius will be ignored. Static doesn't mean immovable: you can move a static joystick by using the `set center for joystick` block.


```
Joystick.addJoystick(0,0,0,0,0,0,0,0,false);
```

***

### Add a Relative Joystick

![joystick-add-relative](http://static.stencyl.com/pedia2/block-images/joystick/joystick-add-relative.png)

Adds a new relative joystick to the screen. For a relative joystick its center position is relative to the coordinates of mouse or touch first press. A relative joystick works only inside its own touch region.

```
Joystick.addJoystick(0,0,0,1,0,0,0,0,false);
```

***

### Remove a Joystick 

![joystick-remove](http://static.stencyl.com/pedia2/block-images/joystick/joystick-remove.png)

Removes a joystick from the screen.

```
Joystick.removeJoystick(0);
```

***

### Default Direction

![joystick-set-default-direction](http://static.stencyl.com/pedia2/block-images/joystick/joystick-set-default-direction.png)

The direction of the joystick will be set to this default direction when the joystick is idle.

Useful when you want an actor to face towards a particular direction when the player doesn't press the joystick. The default value of default direction is 0.

```
Joystick.setDefaultDirection(0,0);
```

***

### Set Radius

![joystick-set-radius](http://static.stencyl.com/pedia2/block-images/joystick/joystick-set-radius.png)

Sets the inner or the outer radius to a given value for a joystick.

The default value of the outer radius is half the width of the outer joystick.
The default value of the inner radius is half the width of the inner joystick.

```
Joystick.setJoystickRadius(0,true,0);
```

***

### Set Touch Region (for a Relative Joystick)

![joystick-set-region](http://static.stencyl.com/pedia2/block-images/joystick/joystick-set-region.png)

Sets the x position, y position, the width and the height of the touch region of a joystick. You can use this block to update the position and/or the size of a touch region of an existing relative joystick.

```
Joystick.setTouchRegionForRJ(0,0,0,0,0);
```

***

### Set Joystick Images

![joystick-set-image](http://static.stencyl.com/pedia2/block-images/joystick/joystick-set-image.png)

Sets the image of the outer or inner part of a joystick. You need to have corresponding images inside your games "extras" folder, one for each scale:

```
imagename.png
imagename@1.5x.png
imagename@2x.png
imagename@3x.png
imagename@4x.png
```

```
Joystick.setJoystickImage(0,true,"text");
```

***

### Set Joystick Transparency

![joystick-set-alpha](http://static.stencyl.com/pedia2/block-images/joystick/joystick-set-alpha.png)

Sets the joystick image transparency for a joystick.

```
Joystick.setJoystickAlpha(0,true,0,true);
```

***

### Auto-hide a Joystick

![joystick-set-always-hide](http://static.stencyl.com/pedia2/block-images/joystick/joystick-set-always-hide.png)

Makes a relative joystick to be always hidden when it is idle. Since the position of a relative joystick is not so important, you can use this block to always hide a relative joystick id when there is no press to save some screen space. 

```
Joystick.alwaysHideRJ(0);
```

***

### Joystick is Pressed

![joystick-is-pressed](http://static.stencyl.com/pedia2/block-images/joystick/joystick-is-pressed.png)

Returns 'true' if the joystick is being pressed, 'false' otherwise.

```
Joystick.isJoystickPressed(0)
```

***

### Distance / Direction  

![joystick-get-distance-direction](http://static.stencyl.com/pedia2/block-images/joystick/joystick-get-distance-direction.png)

Returns the distance or the direction of a joystick.

Distance is always a float number between 0 and 1.
Direction is always a float number between 0 (inclusive) and 360 (exclusive), where 0 means that the joystick is facing towards right, and 90 means that the joystick is facing down.

```
Joystick.getJoystickDisDir(0,false)
```

***

### Jostick Center Coordinates

![joystick-get-center](http://static.stencyl.com/pedia2/block-images/joystick/joystick-get-center.png)

Returns the x or the y coordinate of the center of a joystick.

```
Joystick.getJoystickCenter(0,true)
```

***

### Joystick Radius

![joystick-get-radius](http://static.stencyl.com/pedia2/block-images/joystick/joystick-get-radius.png)

Returns the outer or inner radius value for a joystick.

```
Joystick.getJoystickRadius(0,true)
```

***

### Touch Region (for a Relative Joystick) 

![joystick-get-touch-region-property](http://static.stencyl.com/pedia2/block-images/joystick/joystick-get-touch-region-property.png)

Returns the position or size of the touch region for a relative joystick.

```
Joystick.getTouchRegionPropertyForRJ(0,1)
```

***
