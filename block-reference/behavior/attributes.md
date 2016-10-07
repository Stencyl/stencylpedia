# Behavior > Attributes

***

> Read our article on [Getting / Setting Remote Attributes](http://www.stencyl.com/help/view/set-get-attributes-remotely/) for an explanation of these blocks.

***

## For Actor

### <a name="get-attribute"></a> Get Attribute (for Actor)

![actor-get-att-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/1%20-%20Attributes/get-attribute.png)

Gets the value of an attribute (from the specified behavior) from the actor you specify.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill everything out for you automatically.

![example](http://static.stencyl.com/pedia2/ch7/getset/image01.png)

```
[ACTOR].getValue([TEXT], [TEXT])
```

***

### <a name="set-attribute"></a> Set Attribute (for Actor)

![actor-set-att-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/1%20-%20Attributes/set-attribute.png)

Sets the value of an attribute (from the specified behavior) for the actor you specify.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill the first and third fields out for you automatically.

```
[ACTOR].setValue([TEXT], [TEXT], [VALUE]);
```

***

## For Scene

### <a name="scene-get-attribute"></a> Get Attribute (for Scene)

![scene-get-att-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/1%20-%20Attributes/scene-get-attribute.png)

Gets the value of an attribute (from the specified behavior) from the current scene.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill everything out for you automatically.

```
getValueForScene([TEXT], [TEXT])
```

***

### <a name="scene-set-attribute"></a> Set Attribute (for Scene)

![scene-set-att-block](http://static.stencyl.com/pedia2/block-images/7%20-%20Behavior/1%20-%20Attributes/scene-set-attribute.png)

Sets the value of an attribute (from the specified behavior) for the current scene.

We strongly recommend clicking the dropdown arrow for the first blank and selecting the desired entry under **Attribute Names** -- this will fill the first and third fields out for you automatically.

```
setValueForScene([TEXT], [TEXT], [VALUE]);
```

***

