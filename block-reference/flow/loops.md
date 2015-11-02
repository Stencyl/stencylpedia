# Flow > Loops

***

## Definite Loops

### <a name="repeat"></a> Repeat

![repeat-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/repeat.png)

Repeats the wrapped blocks a given number of times. The embedded `current loop count` block returns how many times you've looped so far (starting from 0, ending at [NUMBER] - 1).

```
for(index0 in 0...[NUMBER]) {
  [ACTIONS]
}
```

#### Example

![loop-count-example](http://static.stencyl.com/pedia2/block-images/extras/flow-loop-example1.png)

Prints out [0 1 2 3 4].

***

## Indefinite Loops

### <a name="while"></a> While Loop

![while-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/while.png)

Runs the wrapped blocks while the given condition is `true`. If the condition is `false` to begin with, nothing will run. Make sure that the condition becomes `false` at some point during the evaluation of the loop (or use the `exit loop` block), otherwise it will result in an infinite loop that will crash your game.

```
while([BOOLEAN]) {
  [ACTIONS]
}
```

***

### <a name="repeatu"></a> Repeat Until Loop

![repeat-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/repeatu.png)

Runs the wrapped blocks while the given condition is `false`. If the condition is `true` to begin with, nothing will run. Make sure that the condition becomes `true` at some point during the evaluation of the loop (or use the `exit loop` block), otherwise it will result in an infinite loop that will crash your game.

```
while(![BOOLEAN]) {
  [ACTIONS]
}
```

#### Example

![repeat-example](http://static.stencyl.com/pedia2/block-images/extras/flow-loop-fibonacci.png)

This will calculate Fibonacci sequence numbers until the current number is greater than 10.

Loop Count | Result | Answer
--- | --- | ---
Prev | 1 | -
Curr | 1 | -
1 | 1 + 1 | 2
2 | 1 + 2 | 3
3 | 2 + 3 | 5
4 | 3 + 5 | 8
5 | 5 + 8 | 13 <-- Greater than 10, stop looping.

***

## Stopping

### <a name="break"></a> Exit Loop

![exit-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/break.png)

Stops the execution of a loop's code.

```
break;
```

***

### <a name="continue"></a> Return to Start of Loop

![return-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/continue.png)

Skips the rest of the code for an iteration of the loop and proceeds to the next iteration (if another iteration will be done).

```
continue;
```

#### Example

![return-example](http://static.stencyl.com/pedia2/block-images/extras/flow-loop-example2.png)

The loop prints out even numbers between [0-9], so this will print out [1 3 5 7 9].

***

### <a name="stop"></a> Stop

![stop-block](http://static.stencyl.com/pedia2/block-images/1%20-%20Flow/1%20-%20Loops/stop.png)

Skips the rest of the code in this event for the current step/frame.

```
return;
```

***
