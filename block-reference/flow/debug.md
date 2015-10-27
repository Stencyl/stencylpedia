# Flow > Debug

***

## Print to Console

### Print

![print-block](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/Print2.png)

Adds the text you specify to your logs, which can be viewed in the **Log Viewer**. Use this block to verify values and debug your game when you encounter bugs. Accepts anything but will convert to text before printing.

```
print([ANYTHING]);
```

***

## Commenting

### Comment (Single Line, Multiple Lines)

![comment-block](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/CommentBlocks.png)

Comments let you mark up your behaviors. They are like sticky notes. They have no effect on a behavior.

```
/* [ANYTHING] */
```

### Comment (Wrapper)

![wrapper-comment-block](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/CommentWrapper.png)

This variant of comments wraps around a stack of blocks. It has no effect on the enclosed blocks (in other words, the code inside still runs).

```
/* [ANYTHING] */
[ACTIONS]
```

***

## Drawing

### Enable/Disable Debug Drawing

![debug-draw-block](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/DebugDrawing.png)

Outlines collision boxes, tiles, regions and terrain regions for debug purposes. Useful for testing physics/collisions. Can also be activated from the menu (prior to testing) via **Run > Enable Debug Drawing**.

```
enableDebugDrawing();
disableDebugDrawing();
```

***
