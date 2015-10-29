# Behavior > State

***

## Is Enabled?

### Is Behavior enabled? (for Actor)

![behavior-enabled-actor-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/is-snippet-enableda.png)

Returns `true` if the specified behavior (using its name) is enabled for the given Actor.

```
[ACTOR].isBehaviorEnabled([TEXT])
```

***

### Is Behavior enabled? (for Scene)

![behavior-enabled-scene-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/is-snippet-enabled.png)

Returns `true` if the specified behavior (using its name) is enabled for the current scene.

```
isBehaviorEnabledForScene([TEXT])
```

***

## Enable / Disable

### [Enable/Disable] Behavior for Actor

![behavior-enabled-scene-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/actor-enabledisable-snippet.png)

Enables (or disabled) the specified behavior (using its name) for the given Actor. Disabling a behavior will stop it from receiving **when updating** and **when drawing** events but does not prevent its other events and do-after/do-every tasks from running.

```
[ACTOR].enableBehavior([TEXT]);
```

***

### [Enable/Disable] Behavior for Scene

![behavior-enabled-scene-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/scene-enabledisable-snippet.png)

Enables (or disabled) the specified behavior (using its name) for the current scene. Disabling a behavior will stop it from receiving **when updating** and **when drawing** events but does not prevent its other events and do-after/do-every tasks from running.

```
enableBehaviorForScene([TEXT]);
```

***

### Disable This Behavior

![behavior-enabled-scene-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/disable-snippet.png)

Disables the current behavior. Does **not** immediately stop its code from running - you'll need to use ![stop-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/stop.png) to achieve that.

Disabling a behavior will stop it from receiving **when updating** and **when drawing** events but does not prevent its other events and do-after/do-every tasks from running.

```
disableThisBehavior();
```

***

## Has Behavior?

### Does Actor have behavior?

![scene-has-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/has-snippet.png)

Returns `true` if the specified behavior (given the behavior name) exists for the given Actor.

```
[ACTOR].hasBehavior([TEXT])
```

***

### Does Scene have behavior?

![actor-has-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/2%20-%20State/scene-has-snippet.png)

Returns `true` if the specified behavior (given the behavior name) exists for the current scene.

```
sceneHasBehavior([TEXT])
```

***
