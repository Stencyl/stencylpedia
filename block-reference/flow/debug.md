# Flow > Debug

***

## Print to Console

### <a name="print"></a> Print

![print object](http://static.stencyl.com/pedia2/block-images/flow/debug/print.png)

Adds the text you specify to your logs, which can be viewed in the **Log Viewer**. Use this block to verify values and debug your game when you encounter bugs. Accepts anything but will convert to text before printing.

```
trace([ANYTHING]);
```

***

## Commenting

### <a name="comment-short"></a> <a name="comment-long"></a> Comment (Single Line, Multiple Lines)

![comment text](http://static.stencyl.com/pedia2/block-images/flow/debug/comment-short.png)<br/>
![comment text](http://static.stencyl.com/pedia2/block-images/flow/debug/comment-long.png)

Comments let you mark up your behaviors. They are like sticky notes. They have no effect on a behavior.

```
/* [ANYTHING] */
```

***

### <a name="comment-wrapper"></a> Comment (Wrapper)

![comment text](http://static.stencyl.com/pedia2/block-images/flow/debug/comment-wrapper.png)

This variant of comments wraps around a stack of blocks. It has no effect on the enclosed blocks (in other words, the code inside still runs).

```
/* [ANYTHING] */
[ACTIONS]
```

***

## Debug Drawing

### <a name="debug-draw"></a> Enable / Disable Debug Drawing

![enable debug drawing](http://static.stencyl.com/pedia2/block-images/flow/debug/debug-draw.png)

Outlines collision boxes, tiles, regions and terrain regions for debug purposes. Useful for testing physics/collisions. Can also be activated from the menu (prior to testing) via **Run > Enable Debug Drawing**.

![debug-draw-example](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/DrawingExample1Thumb.png)

```
enableDebugDrawing();
disableDebugDrawing();
```

***
