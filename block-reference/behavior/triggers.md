# Behavior > Triggers

***

> Read our article on [Custom Events](http://www.stencyl.com/help/view/custom-events/) for an explanation of these blocks.

***

## For Actor

### <a name="say"></a> Trigger Event in Specific Behavior (for Actor)

![say-trigger-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/0%20-%20Triggers/say.png)

Triggers the custom event for a specific behavior that is attached to the specified actor.

```
[ACTOR].say([TEXT], "_customEvent_" + [TEXT]);
```

***

### <a name="shout"></a> Trigger Event in All Behaviors (for Actor)

![shout-trigger-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/0%20-%20Triggers/shout.png)

Triggers the custom event for all behaviors that are attached to the specified actor.

```
[ACTOR].shout("_customEvent_" + [TEXT]);
```

***

## For Scene

### <a name="scene-say"></a> Trigger Event in Specific Behavior (for Scene)

![say-trigger-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/0%20-%20Triggers/scene-say.png)

Triggers the custom event for the specified behavior that is attached to the current scene.

```
sayToScene([TEXT], "_customEvent_" + [TEXT]);
```

***

### <a name="scene-shout"></a> Trigger Event in All Behaviors (for Scene)

![shout-trigger-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/0%20-%20Triggers/scene-shout.png)

Triggers the custom event for all behaviors that are attached to the current scene.

```
shoutToScene("_customEvent_" + [TEXT]);
```

***

## For Both

### <a name="say-this"></a> Trigger Event (Global)

![global-trigger-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/0%20-%20Triggers/say-this.png)

Triggers the custom event for all behaviors attached to every actor in the current scene and the current scene.

```
_customEvent_text();
```

***
