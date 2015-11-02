# User Input > Gamepad

***

> Read [our guide](http://www.stencyl.com/help/view/gamepads/) on Gamepads before consulting this reference.

***

## Gamepad

### <a name="enable-gamepad"></a> Enable Gamepad

![enable-gamepad-block](http://static.stencyl.com/pedia2/blocks/user_input/gamepad/Enable.png)

Turns on the gamepad framework. Must be used before any gamepad functionality will work.

```
Input.enableJoystick();
```

***

### <a name="map-gamepad-control"></a> Map Button to Control

![map-gamepad-block](http://static.stencyl.com/pedia2/blocks/user_input/gamepad/Map.png)

Binds a physical button on the gamepad to a Stencyl [control](http://www.stencyl.com/help/view/controls/). Each model of controller has different names for its buttons, so you must either let the user configure their controls or [discover](http://www.stencyl.com/help/view/gamepads/) those names.

```
Input.mapJoystickButton([TEXT],[CONTROL]);
```

#### Example (for XBox 360 Controller)

![example](http://static.stencyl.com/pedia2/ch6/gamepad/gamepad-mapping.png)

Read [our guide](http://www.stencyl.com/help/view/gamepads/) on Gamepads for an explanation.

***

### <a name="set-gamepad-sensitivity"></a> Set Analog Sensitivity

![analog-gamepad-block](http://static.stencyl.com/pedia2/blocks/user_input/gamepad/Analog.png)

Sets the **deadzone** for an analog button (usually a joystick), so that a small tilt doesn't get interpreted as actions. Defaults to 0. Provide a value between [0-100], inclusive, where 0 means that any amount of tilt/press will be detected and 100 effectively disables the button. 

```
Input.setJoySensitivity([NUMBER]/100);
```

***

### <a name="get-button-pressure"></a> Get Pressure for Control

![pressure-gamepad-block](http://static.stencyl.com/pedia2/blocks/user_input/gamepad/Pressure.png)

Gets the pressure for a given control as a value between 0 and 1, inclusive, where 0 means no tilt/press and 1 means full tilt/press. Assumes that said control is an analog control (such as joystick), not a digital control like a regular button.

```
Input.getButtonPressure([CONTROL])
```

***

### <a name="save-gamepad-config"></a> <a name="load-gamepad-config"></a> Save/Load Gamepad Configuration

![saveload-gamepad-block](http://static.stencyl.com/pedia2/blocks/user_input/gamepad/SaveLoad.png)

Players using a less common controller will need to manually configure their controller during the game. This block lets you save and load those mappings, so they don't have to repeat the process each time they play your game. The name provided is a virtual filename. For most cases, it doesn't matter what you put in.

```
Input.saveJoystickConfig([TEXT]);
Input.loadJoystickConfig([TEXT]);
```

***
