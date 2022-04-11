## Contents

* Introduction
* Use the Focus Event
* Best Practice - Pause the Game
* FAQ: Why does my app restart from scratch?
 

## Introduction

Many modern mobile devices support some form of multitasking -- the ability to switch between several apps by sending the currently active app to the "background."

Stencyl provides a simple but effective way of performing logic when an app enters and leaves the background.


## Use the Focus Event

The **Focus event** (under **Add Event > Input**) not only works on web/desktop games, but it also works the same way on mobile games. 

![Focus Event](https://static.stencyl.com/help/images/multitasking-2.png)

![Focus Event Block](https://static.stencyl.com/help/images/multitasking-3.png)

The Focus event will happen in two cases.

#### 1) Losing Focus
Happens just before the game is sent to the background.

#### 2) Regaining Focus
Happens just after the game resumes but before anything else happens to it.


## Best Practice - Pause the Game

When would you use the Focus event in a mobile game?

It's a good idea to **pause** a game when it enters the background. When that happens, it's also a good idea to display some appropriate graphics to indicate the game's paused status.

![Losing Focus](https://static.stencyl.com/help/images/multitasking-4.png)

![Paused](https://static.stencyl.com/help/images/multitasking-5.png)

Why is this a good idea? Imagine that a player switched away from the app but was left in a situation where he'd get hit within seconds. If the app weren't paused, the player would likely be too slow to react and would get frustrated.


## FAQ: Why does my app restart from scratch?

Multitasking on iOS or Android doesn't work the same way as it does on a PC or Mac. If the amount of free memory on the device is too little, the device will stop a backgrounded app to free up memory, so that it can support the task at hand. This causes the game to start from scratch - likely lost progress for the player.

If you wish to support true multitasking, we recommend that you **save the game upon losing focus** and offer to load the saved game if you detect that the game has restarted (similar to the "Quick Save" option in recent Mario games).
