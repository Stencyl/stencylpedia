## Contents

* What are Custom Events?
* Defining Custom Events
* Triggering Custom Events
* One Recipient vs. All
* Making the Custom Event Configurable
* Custom Events vs. Custom Blocks
 

## What are Custom Events?

Custom Events are events that happen only when you tell them to happen. Why would you want to do this?

* Reuse Logic. If you're finding that you're copying and pasting the same code, you could stick it into a Custom Event and trigger that Custom Event instead.

* Allow other behaviors to cause stuff to happen.
 
> **Aside:** In programming terms, Custom Events are equivalent to the concept of "messaging" or "indirect invocation" - they aren't quite the same as function calls since you aren't always specifying a receiver. There can be as few as 0 receivers or infinitely many.
 

## Defining Custom Events

1. Inside the Behavior Designer, go to **Add Event > Advanced > Custom Event**.

  ![](https://static.stencyl.com/pedia2/ch6/customevent/image00.png)

2. Type something into the blank. This is the text that will cause this Custom Event to **trigger**.

  ![](https://static.stencyl.com/pedia2/ch6/customevent/image01.png)

That's it! Now fill out what you want to happen inside the event.

 
## Triggering Custom Events

Custom Events are triggered by any one of the blocks under **Behavior > Triggers**. The act of telling a Custom Event to happen is called **triggering**.

**To trigger an event, put in the text you stuck into the blank when defining the event.**

![](https://static.stencyl.com/pedia2/ch6/customevent/image02.png)


 
## One Recipient vs. All

As you have may noticed, triggering Custom Events can be done **directly** (one behavior) or **indirectly** (all behaviors). That is to say:

* You can specify exactly which behavior you're targeting.<br/>
  ![](https://static.stencyl.com/pedia2/ch6/customevent/image03.png)

* You specify no target, so it **attempts to trigger the event** for all behaviors for a particular Actor or Scene.<br/>
  ![](https://static.stencyl.com/pedia2/ch6/customevent/image04.png)

> **Note:** If a behavior doesn't have a Custom Event and you try to trigger it, nothing happens. It's ignored.


## When would specifying no target ("all behaviors") be useful?

* A bunch of behaviors happen to receive the same event, and you want to target them all at once.
* You don't feel like typing in the target behavior, so you target them all. Besides a minor performance penalty, there's nothing wrong with this.
 

## Making the Custom Event Configurable

Sometimes, you may want to make a Custom Event configurable. Which is to say that you would want to stick a **Text Attribute** into the blank.

![](https://static.stencyl.com/pedia2/ch6/customevent/image05.png)

You can do this and, as you'd expect, the text for the Custom Event becomes configurable.

> **Warning:** Do not change the value of the Text Attribute at runtime during the game. The Custom Event may break if you do this.
 

## Custom Events vs. Custom Blocks

Custom Events and [Custom Blocks](https://www.stencyl.com/help/viewArticle/106/) overlap somewhat in use case. However, they differ in several respects, as summarized below.

#### Custom Events:
* Can't accept parameters.
* Can be triggered directly or indirectly.
* Easier to set up and use.

#### Custom Blocks:
* Accept parameters.
* Triggered directly.
* More difficult to set up, but more versatile in some respects.


## Summary

* Custom Events are events that you trigger yourself.
* You define the textual name that triggers the event.
* Generally speaking, it's easier and simpler to just target all behaviors rather than specifying a specific recipient.
