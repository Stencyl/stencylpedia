# Behaviors > State

***

## Is Enabled?

### <a name="is-snippet-enableda"></a> Is Behavior enabled? (for Actor)

![behavior text is enabled for actor](https://static.stencyl.com/pedia2/block-images/behavior/state/is-snippet-enableda.png)

Returns `true` if the specified behavior (using its name) is enabled for the given actor.

```
[ACTOR].isBehaviorEnabled([TEXT])
```

***

### <a name="is-snippet-enabled"></a> Is Behavior enabled? (for Scene)

![behavior text is enabled for this scene](https://static.stencyl.com/pedia2/block-images/behavior/state/is-snippet-enabled.png)

Returns `true` if the specified behavior (using its name) is enabled for the current scene.

```
isBehaviorEnabledForScene([TEXT])
```

***

## Enable / Disable

### <a name="actor-enabledisable-snippet"></a> Enable / Disable Behavior for Actor

![enable behavior text for actor](https://static.stencyl.com/pedia2/block-images/behavior/state/actor-enabledisable-snippet.png)

Enables (or disabled) the specified behavior (using its name) for the given Actor. Disabling a behavior will stop it from receiving **when updating** and **when drawing** events but does not prevent its other events and do-after/do-every tasks from running.

```
[ACTOR].enableBehavior([TEXT]);
[ACTOR].disableBehavior([TEXT]);
```

***

### <a name="scene-enabledisable-snippet"></a> Enable / Disable Behavior for Scene

![enable behavior text for this scene](https://static.stencyl.com/pedia2/block-images/behavior/state/scene-enabledisable-snippet.png)

Enables (or disabled) the specified behavior (using its name) for the current scene. Disabling a behavior will stop it from receiving **when updating** and **when drawing** events but does not prevent its other events and do-after/do-every tasks from running.

```
enableBehaviorForScene([TEXT]);
disableBehaviorForScene([TEXT]);
```

***

### <a name="disable-snippet"></a> Disable This Behavior

![disable this behavior](https://static.stencyl.com/pedia2/block-images/behavior/state/disable-snippet.png)

Disables the current behavior. Does **not** immediately stop its code from running - you'll need to use ![stop-block](https://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/stop.png) to achieve that.

Disabling a behavior will stop it from receiving **when updating** and **when drawing** events but does not prevent its other events and do-after/do-every tasks from running.

```
disableThisBehavior();
```

***

## Has Behavior?

### <a name="has-snippet"></a> Does Actor have behavior?

![actor has behavior text](https://static.stencyl.com/pedia2/block-images/behavior/state/has-snippet.png)

Returns `true` if the specified behavior (given the behavior name) is attached to the given actor.

```
[ACTOR].hasBehavior([TEXT])
```

***

### <a name="scene-has-snippet"></a> Does Scene have behavior?

![this scene has behavior text](https://static.stencyl.com/pedia2/block-images/behavior/state/scene-has-snippet.png)

Returns `true` if the specified behavior (given the behavior name) is attached to the current scene.

```
sceneHasBehavior([TEXT])
```

***
