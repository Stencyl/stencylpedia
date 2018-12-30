# User Input > Gamepad

***

> Read our guide on [Gamepads](http://www.stencyl.com/help/view/gamepads/) before consulting this reference.

***

## Gamepad

### <a name="map-gamepad-control"></a> Map Button to Control

![map button text to control control](http://static.stencyl.com/pedia2/block-images/input/gamepad/map-gamepad-control.png)

Binds a physical button on the gamepad to a Stencyl [control](http://www.stencyl.com/help/view/controls/). Each model of controller has different names for its buttons, so you must either let the user configure their controls or [discover](http://www.stencyl.com/help/view/gamepads/) those names.

```
Input.mapJoystickButton([TEXT], [CONTROL]);
```

#### Example (for XBox 360 Controller)

![example](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-mapping.png)

Read [our guide](http://www.stencyl.com/help/view/gamepads/) on Gamepads for an explanation.

***

### <a name="unmap-gamepad-button"></a> Unmap Button

![unmap button text](http://static.stencyl.com/pedia2/block-images/input/gamepad/unmap-gamepad-button.png)

Unbinds a gamepad button from its current control.

```
Input.unmapJoystickButton([TEXT]);
```

***

### <a name="unmap-gamepad-control"></a> Unmap Control

![unmap all buttons for control control](http://static.stencyl.com/pedia2/block-images/input/gamepad/unmap-gamepad-control.png)

Unbinds all gamepad buttons for a given control.

```
Input.unmapJoystickFromControl([CONTROL]);
```

***

### <a name="set-gamepad-sensitivity"></a> Set Analog Sensitivity

![set analog sensitivity to number %](http://static.stencyl.com/pedia2/block-images/input/gamepad/set-gamepad-sensitivity.png)

Sets the **deadzone** for an analog button (usually a joystick), so that a small tilt doesn't get interpreted as actions. Defaults to 0. Provide a value between [0-100], inclusive, where 0 means that any amount of tilt/press will be detected and 100 effectively disables the button. 

```
Input.setJoySensitivity([NUMBER] / 100);
```

***

### <a name="get-button-pressure"></a> Get Pressure for Control

![get pressure for control control](http://static.stencyl.com/pedia2/block-images/input/gamepad/get-button-pressure.png)

Gets the pressure for a given control as a value between 0 and 1, inclusive, where 0 means no tilt/press and 1 means full tilt/press. Assumes that said control is an analog control (such as joystick), not a digital control like a regular button.

```
Input.getButtonPressure([CONTROL])
```

***

### <a name="save-gamepad-config"></a> <a name="load-gamepad-config"></a> Save / Load Gamepad Configuration

![save gamepad configuration to text](http://static.stencyl.com/pedia2/block-images/input/gamepad/save-gamepad-config.png)<br/>
![load gamepad configuration from text](http://static.stencyl.com/pedia2/block-images/input/gamepad/load-gamepad-config.png)

Players using a less common controller will need to manually configure their controller during the game. This block lets you save and load those mappings, so they don't have to repeat the process each time they play your game. The name provided is a virtual filename. For most cases, it doesn't matter what you put in.

```
Input.saveJoystickConfig([TEXT]);
Input.loadJoystickConfig([TEXT]);
```

***
