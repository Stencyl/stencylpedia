## Flow > Conditions

***

#### If

![](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/If.png)

Checks whether the condition is `true` or `false`. If the condition is `true`, the blocks wrapped inside will execute.

```
if([BOOLEAN]) {
  [ACTIONS]
}
```

***

#### Otherwise

![](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/Otherwise.png)

Used directly below an "If" block. If the condition in the preceding "If" block is `false`, the blocks wrapped inside the "Otherwise" block will execute.

```
else {
  [ACTIONS]
}
```

***

#### Otherwise If

![](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/OtherwiseIf.png)

Equivalent to doing the following.

![](http://static.stencyl.com/pedia2/blocks/flow/flow_conditionals/OtherwiseIf2.png)

```
else if([BOOLEAN]) {
  [ACTIONS]
}
```
