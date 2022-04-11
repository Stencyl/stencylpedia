## Contents

* Keyboard
* Alerts
* Vibrate
* Other Features
 

## Keyboard

At times, it's useful to display the on-screen keyboard in order to support text entry. For example, you may want the player to enter in a name when upon achieving a high score.

<img src="https://static.stencyl.com/help/images/mobile-features-1.png" alt="On Screen Keyboard" style="width:300px;"/>

#### Showing/Hiding the Keyboard
Use the show keyboard block under User Input > Mobile to show or hide the Keyboard. When you do this, the keyboard will immediately display.

![Show Keyboard block](https://static.stencyl.com/help/images/mobile-features-2.png)

#### Keyboard Events (knowing what's been typed)
Pressing the keys will fire keyboard events, which you can pick up on using a keyboard event (**Add Event > Mobile > Keyboard**). **Each event will receive the complete text typed in so far**, not the individual letters.

For example, you can record the currently typed in text and store that in an attribute...

![Key Input](https://static.stencyl.com/help/images/mobile-features-3.png)

So that you can then draw it on screen.

![Key Input](https://static.stencyl.com/help/images/mobile-features-4.png)

When the user's done (hits return), you can get the final result and act accordingly.

![Key Input](https://static.stencyl.com/help/images/mobile-features-5.png)

#### Other Operations
Besides receiving events, you can perform a few operations on the keyboard.

* **Set** the keyboard's current text.
* **Clear** the keyboard's text.
 

## Alerts

Alerts are modal dialogs that display information to the user. When they appear, everything about the game pauses. Alerts are a blunt way of grabbing the user's attention and should be used sparingly.

<img src="https://static.stencyl.com/help/images/mobile-features-6.png" alt="Alerts" style="width:300px;"/>

To display an Alert, use the **alert** block at the bottom of **Game > Mobile**.

![Display Alert block](https://static.stencyl.com/help/images/mobile-features-7.png)


## Vibrate

Vibrations provide haptic (tactile) feedback to a user, if a device supports them. To vibrate a device, use the vibrate block at the bottom of **User Input > Mobile-Only**.

![Vibrate](https://static.stencyl.com/help/images/mobile-features-8.png)

> **Notes:** If a device doesn't support vibrate (iPad, iPod Touch), nothing will happen. iOS devices may only vibrate for 2 seconds. In other words, you have no control over the duration.
 

## Other Features

Stencyl supports additional mobile features through user-created extensions. These currently include:

* Local Notifications
* Web Views
* Alternative Ad Networks
* Rate My Game
* Online Video Playback

Extensions found in our [Extensions Market](https://www.stencyl.com/developers/market/) and our [Extensions forum](https://community.stencyl.com/index.php/board,70.0.html).

As these extensions mature and see further uptake, we'll selectively pull them into the core engine.

## Want to create your own extension?

If you wish to contribute an extension and have some technical expertise, consider [creating an Extension](https://www.stencyl.com/help/view/how-to-create-engine-extension/) which allows you to extend the Stencyl engine with native code (Objective-C, C++, Java).

