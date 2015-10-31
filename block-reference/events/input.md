# Events > Input

***

## Universal

### when %0 is %1 [e:keyboard]

![event-key-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/1%20-%20Input/event-key-press-release.png)

Key pressed/released.

```

/* =========================== Keyboard =========================== */
addKeyStateListener(!ERROR!, function(pressed:Bool, released:Bool, list:Array<Dynamic>):Void
{
	if(wrapper.enabled && pressed)
	{
		
	}
});
```

***

### when any key is %0 [e:dash] %2 %3 [e:keyboard]

![event-key-any-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/1%20-%20Input/event-key-any-press-release.png)

Any key pressed/released.

```

/* =========================== Any Key ============================ */
addAnyKeyPressedListener(function(event:KeyboardEvent, list:Array<Dynamic>):Void
{
	if(wrapper.enabled)
	{
		
	}
});
```

***

### when the game %0 focus [e:target]

![event-focus-changed](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/1%20-%20Input/event-focus-changed.png)

Game gains/loses focus.

```

/* ============================ Focus ============================= */
addFocusChangeListener(function(lost:Bool, list:Array<Dynamic>):Void
{
	if(wrapper.enabled && lost)
	{
		
	}
});
```

***

## Universal (Works for Mouse & Touch)

### when the mouse is %0 [e:mouse]

![event-mouse-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/2%20-%20Input/event-mouse-press-release.png)

Mouse pressed/released/moved/dragged.

```

/* ============================ Click ============================= */
addMousePressedListener(function(list:Array<Dynamic>):Void
{
	if(wrapper.enabled)
	{
		
	}
});
```

***

### when the mouse %1 %0 [e:mouse-actor]

![event-mouse-enter-exit-actor](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/2%20-%20Input/event-mouse-enter-exit-actor.png)

Mouse enters/exits/presses/releases/drags on an actor.

```

/* =========================== On Actor =========================== */
addMouseOverActorListener(__, function(mouseState:Int, list:Array<Dynamic>):Void
{
	if(wrapper.enabled && 1 == mouseState)
	{
		
	}
});
```

***

### when the mouse %1 %0 [e:mouse-region]

![event-mouse-enter-exit-region](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/2%20-%20Input/event-mouse-enter-exit-region.png)

Mouse enters/exits/presses/releases/drags on a region.

```

/* ========================== On Region =========================== */
addMouseOverActorListener(__, function(mouseState:Int, list:Array<Dynamic>):Void
{
	if(wrapper.enabled && 1 == mouseState)
	{
		
	}
});
```

***

## Mobile-Only

### when the device is swiped %0 [e:tilt]

![event-device-swipe](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/3%20-%20Input/event-device-swipe.png)

Device is swiped.

```

/* ============================ Swipe ============================= */
addSwipeListener(function(list:Array<Dynamic>):Void
{
	if(wrapper.enabled && Input.swipedUp)
	{
		
	}
});
```

***

### when touch is %0 [e:dash] %2

![event-device-multitouch](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/3%20-%20Input/event-device-multitouch.png)

Detects multi-touch events. Use the mouse events for regular, single-touch detection.

```

/* ========================= Multi-Touch ========================== */
addMultiTouchStartListener(function(event:TouchEvent, list:Array<Dynamic>):Void
{
	if(wrapper.enabled)
	{
		
	}
});
```

***

## Desktop-Only

### when any gamepad button is %0 [e:dash] %2

![event-gamepad-any-press-release](http://static.stencyl.com/pedia2/block-images/13%20-%20Events/4%20-%20Input/event-gamepad-any-press-release.png)

Any gamepad button pressed/released.

```

/* ========================== Any Button ========================== */
addAnyGamepadPressedListener(function(input:String, list:Array<Dynamic>):Void
{
	if(wrapper.enabled)
	{
		
	}
});
```

***


