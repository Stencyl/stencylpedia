# Flow > Conditions

***

## Definite Loops

### Repeat

![repeat-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/RepeatBlock.png)

Repeats the wrapped blocks a given number of times.

```
for(index0 in 0...[NUMBER]) {
  [ACTIONS]
}
```

***

### Current Loop Count

![loop-count-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/LoopCountBlock.png)

Used with repeat. Returns the counter for the current loop.

#### Example

![loop-count-example](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/DefiniteLoopExample1.png)

Prints out [0 1 2 3 4].

***

## Indefinite Loops

### While Loop

![while-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/WhileBlock.png)

Runs the wrapped blocks while the given condition is `true`. If the condition is `false` to begin with, nothing will run.

```
while([BOOLEAN]) {
  [ACTIONS]
}
```

***

### Repeat Until Loop

![repeat-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/RepeatUntilBlock.png)

Runs the wrapped blocks while the given condition is `false`. If the condition is `true` to begin with, nothing will run.

```
while(![BOOLEAN]) {
  [ACTIONS]
}
```

#### Example

![repeat-example](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/IndefiniteLoopExample2.png)

This will add the current loop count to the running sum, until the sum is greater than 10.

Loop Count | Sums | Answer
--- | --- | ---
0 | 0 | 0
1 | 0 + 1 | 1
2 | 0 + 1 + 2 | 3
3 | 0 + 1 + 2 + 3 | 6
4 | 0 + 1 + 2 + 3 + 4 | 10
5 | 0 + 1 + 2 + 3 + 4 + 5 | 15 <-- Greater than 10, stop looping.

***

## Stopping

### Exit Loop

![exit-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/ExitLoopBlock.png)

Stops the execution of a loop's code.

```
break;
```

***

### Return to Start of Loop

![return-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/ReturnToStartBlock.png)

Skips the rest of the code for an iteration of the loop proceeds to the next iteration (if one will be done).

```
continue;
```

#### Example

![return-example](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/StoppingExample3.png)

The loop prints out even numbers between [0-9], so this will print out [1 3 5 7 9].

***

### Stop

![stop-block](http://static.stencyl.com/pedia2/blocks/flow/flow_looping/StopBlock.png)

Skips the rest of the code in this event for the current frame.

```
return;
```

***
