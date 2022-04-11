# Game Attributes

***

> The following blocks are useful if you want to build a behavior that can get/set game attributes by name, using a text attribute or other means. They can also be useful as a general way of storing data (pass in a name that isn't used), without specifying it in the toolset. For regular usage, we recommend sticking to the blocks that Stencyl auto-generates for your [Game Attributes](https://www.stencyl.com/help/view/game-attributes/).

***

## Game Attribute Getter / Setter

### <a name="get-game-att"></a> Get Game Attribute

![value of game attribute with name text](https://static.stencyl.com/pedia2/block-images/attributes/game-attributes/get-game-att.png)

Gets the value of the specified game attribute (using its name).

```
(getGameAttribute([TEXT]))
```

***

### <a name="set-game-att"></a> Set Game Attribute

![set game attribute with name text to object](https://static.stencyl.com/pedia2/block-images/attributes/game-attributes/set-game-att.png)

Sets the value of the specified game attribute (using its name). You are responsible for making sure that you don't set the value to a different type. For example, if the game attribute is a number, don't stick text into that slot.

```
setGameAttribute([TEXT], [VALUE]);
```

***
