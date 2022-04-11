## Contents

* Creating Actors
* Referring to the "Last Created Actor"
* Destroying Actors
* Events
 

## Creating Actors

Use the create-actor-of-type block (under Scene > Actors).

![Create Actor](https://static.stencyl.com/pedia2/ch3/destroying/image00.png)

* You can drag an actor-type block into the Choose Actor Type field. This is useful when you want to make this field configurable.

* Front / Middle / Back will place the actor on those layers, respectively. Middle will choose whatever layer is closest to the middle. If you need a specific layer, change the actor's layer after creation.

* In terms of execution order, when you create an actor, the new actor's "when created" event is run before the current behavior proceeds further.


## Referring to the "Last Created Actor"

Sometimes, you'll want to refer to the actor that you just created. Use the "last created actor" option under any Actor dropdown to do this.

![Last Created Actor](https://static.stencyl.com/pedia2/ch3/destroying/image06.png)


## Destroying Actors

Destroying actors is similar to creating them. Use the kill-actor block (under **Actors > Properties**).

![Kill Actor](https://static.stencyl.com/pedia2/ch3/destroying/image05.png)

Killing an actor is immediate. Don't attempt to refer to an actor at any point after you've killed it. Especially during timed tasks (do-after, do-every), where it's easy for this to happen by accident.
 

## Events: Knowing when actors get created or die

We provide events that let you control what happens when an actor is created or destroyed. Select one of these events via the "Add Event" button.

![Events](https://static.stencyl.com/pedia2/ch3/destroying/image04.png)

* When an actor dies, the die event happens **before** the actor actually dies, so you can still refer to it during the event. 
* When an actor is created, the actor's "when created" event always runs first. Then, the other created events pertaining to the actor are run. 

 
## Challenge 1: Create A Particle Effect

Why not try creating a particle effect using lightweight actors (or images) and along the way, compare its performance to doing this with regular actors?

([View Demo](http://dl.dropbox.com/u/42317429/Demo.swf))

To create particle effects, just spawn actors rapidly and "emit" them at a random speed and starting position and have them fade out over time. With some experimentation, you can create a fire and smoke effect with ease.

 

## Challenge 2: Create A Bullet Limiter

Many games have a mechanism that allows you to fire bullets, but only a certain number at a time, otherwise the game would become too easy.

Why not try creating a bullet limiter that allows the player to create no more than 3 bullets at once?

([View Demo](http://dl.dropbox.com/u/42317429/Demo%202.swf))

> **Hint:** Use the 'when an actor of [TYPE] is created/killed' event.
