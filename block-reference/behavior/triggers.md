# Behaviors > Triggers

***

> Read our article on [Custom Events](https://www.stencyl.com/help/view/custom-events/) for an explanation of these blocks.

***

## For Actor

### <a name="say"></a> Trigger Event in Specific Behavior (for Actor)

![trigger event text in behavior text for actor](https://static.stencyl.com/pedia2/block-images/behavior/triggers/say.png)

Triggers the custom event for a specific behavior that is attached to the specified actor.

```
[ACTOR].say([TEXT], "_customEvent_" + [TEXT]);
```

***

### <a name="shout"></a> Trigger Event in All Behaviors (for Actor)

![trigger event text in all behaviors for actor](https://static.stencyl.com/pedia2/block-images/behavior/triggers/shout.png)

Triggers the custom event for all behaviors that are attached to the specified actor.

```
[ACTOR].shout("_customEvent_" + [TEXT]);
```

***

## For Scene

### <a name="scene-say"></a> Trigger Event in Specific Behavior (for Scene)

![trigger event text in behavior text for this scene](https://static.stencyl.com/pedia2/block-images/behavior/triggers/scene-say.png)

Triggers the custom event for the specified behavior that is attached to the current scene.

```
sayToScene([TEXT], "_customEvent_" + [TEXT]);
```

***

### <a name="scene-shout"></a> Trigger Event in All Behaviors (for Scene)

![trigger event text in all behaviors for this scene](https://static.stencyl.com/pedia2/block-images/behavior/triggers/scene-shout.png)

Triggers the custom event for all behaviors that are attached to the current scene.

```
shoutToScene("_customEvent_" + [TEXT]);
```

***

## In This Behavior

### <a name="say-this"></a> Trigger Event (this Behavior)

![trigger event text in this behavior](https://static.stencyl.com/pedia2/block-images/behavior/triggers/say-this.png)

Triggers a custom event in this behavior. This is a direct function call, so an event with the specified name must exist, otherwise it will cause a compilation error.

```
_customEvent_text();
```

***
