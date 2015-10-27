# Flow > Time

***

## Delayed

### Do after [N] seconds

![do-after-block](http://static.stencyl.com/pedia2/blocks/flow/flow_time/DoAfterLoopBlock.png)

Runs the code after the given delay (in seconds, can be partial seconds).

```
runLater(1000 * [NUMBER], function(task:TimedTask):Void {
  [ACTIONS]
});
```

> **Warning:** Do not use this block in a `when updating` event, unless constrained by an `if` block or other conditional.

***

## Periodic

### Do every [N] seconds

![do-every-block](http://static.stencyl.com/pedia2/blocks/flow/flow_time/DoEveryLoopBlock.png)

Runs the code every [N] seconds (can be partial seconds).

```
runPeriodically(1000 * [NUMBER], function(task:TimedTask):Void {
  [ACTIONS]
});
```

> **Warning:** Do not use this block in a `when updating` event, unless constrained by an `if` block or other conditional.

#### Example

![time-example](http://static.stencyl.com/pedia2/blocks/flow/flow_time/PeriodicExample2.png)

`do-after` and `do-every` can be combined together. In this example, we implement a "blinking" effect by alternating the actor between hidden and not-hidden, without relying on a variable to store state.


### Cancel

![cancel-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/RepeatBlock.png)

Cancels the execution of a periodic (`do-every-n-seconds`) task.

```
timeTask.repeats = false; 
return;
```
