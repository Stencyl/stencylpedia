# Flow > Time

***

## Delayed

### <a name="dolater"></a> Do after N seconds

![do after number seconds](http://static.stencyl.com/pedia2/block-images/flow/time/dolater.png)

Runs the code after the given delay (in seconds, can be partial seconds).

```
runLater(1000 * [NUMBER], function(task:TimedTask):Void {
  [ACTIONS]
}, [ACTOR]);
```

> **Warning:** Do not use this block in a `when updating` event, unless constrained by an `if` block or other conditional.

***

## Periodic

### <a name="periodic"></a> Do every N seconds

![do every number seconds](http://static.stencyl.com/pedia2/block-images/flow/time/periodic.png)

Runs the code every [N] seconds (can be partial seconds).

```
runPeriodically(1000 * [NUMBER], function(task:TimedTask):Void {
  [ACTIONS]
}, [ACTOR]);
```

> **Warning:** Do not use this block in a `when updating` event, unless constrained by an `if` block or other conditional.

#### Example

![time-example](http://static.stencyl.com/pedia2/blocks/flow/flow_time/PeriodicExample2.png)

`do after n seconds` and `do every n seconds` can be combined together. In this example, we implement a "blinking" effect by alternating the actor between hidden and not-hidden, without relying on a variable to store state.

***

### <a name="cancel"></a> Cancel

![cancel](http://static.stencyl.com/pedia2/block-images/flow/time/cancel.png)

Cancels the execution of a periodic (`do every n seconds`) task.

```
timeTask.repeats = false;
return;
```

***
