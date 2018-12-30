# Behaviors > Attributes

***

> Read our article on [Getting / Setting Remote Attributes](http://www.stencyl.com/help/view/set-get-attributes-remotely/) for an explanation of these blocks.

***

## For Actor

### <a name="get-attribute"></a> Get Attribute (for Actor)

![for actor , get text from behavior text](http://static.stencyl.com/pedia2/block-images/behavior/attributes/get-attribute.png)

Gets the value of an attribute (from the specified behavior) from the actor you specify.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill everything out for you automatically.

![example](http://static.stencyl.com/pedia2/ch7/getset/image01.png)

```
[ACTOR].getValue([TEXT], [TEXT])
```

***

### <a name="set-attribute"></a> Set Attribute (for Actor)

![for actor , set text to object for behavior text](http://static.stencyl.com/pedia2/block-images/behavior/attributes/set-attribute.png)

Sets the value of an attribute (from the specified behavior) for the actor you specify.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill the first and third fields out for you automatically.

```
[ACTOR].setValue([TEXT], [TEXT], [VALUE]);
```

***

## For Scene

### <a name="scene-get-attribute"></a> Get Attribute (for Scene)

![for this scene, get text from behavior text](http://static.stencyl.com/pedia2/block-images/behavior/attributes/scene-get-attribute.png)

Gets the value of an attribute (from the specified behavior) from the current scene.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill everything out for you automatically.

```
getValueForScene([TEXT], [TEXT])
```

***

### <a name="scene-set-attribute"></a> Set Attribute (for Scene)

![for this scene, set text to object for behavior text](http://static.stencyl.com/pedia2/block-images/behavior/attributes/scene-set-attribute.png)

Sets the value of an attribute (from the specified behavior) for the current scene.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill the first and third fields out for you automatically.

```
setValueForScene([TEXT], [TEXT], [VALUE]);
```

***
