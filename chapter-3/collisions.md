## Contents

* Collisions are Automatic
* Groups
* Shapes
* Sensors
* Handling Collisions
* More Collision Handling (Sides, Groups, Points)


## Collisions are Automatic

Because Stencyl is powered by [Box2D](http://www.stencyl.com/help/view/working-with-physics/), collisions happen automatically, as if every object existed in "real-life." For the default cases, no action is required on your part to make collisions happen.

<a href="http://www.stencyl.com/game/play/10715">![Ragdoll Demo](http://static.stencyl.com/pedia2/ch3/ragdoll.png)</a>

 
## Groups

However, what if you **only want certain collisions to happen**? For example, if any enemy shoots a bullet, the bullet should only collide with the player, not other enemies.

![stencyl-collision-groups-diagram](http://static.stencyl.com/help/images/CollisionGroupsIllustration2.png)

To do this, you have to set up Groups.

Groups are **arbitrary collections of Actors**. Groups tend to be named after certain classes of Actors, such as "Players" and "Enemies."

![stencyl-players-enemies-collision-groups-pic](http://static.stencyl.com/pedia2/ch3/collisions/image09.png)

**Collisions happen between groups that are set up to collide with each other**. Conversely, collisions are ignored between groups that are not set up to collide with each other.

 
#### How To: Setting up Groups
You can set up Groups in the Settings dialog. Click the **Settings** button to open the dialog.

![Settings Button](http://static.stencyl.com/help/images/Settings-Button-New.png)

Next, click the **Groups** button (shown below), and you'll see a dialog that shows the Collision Groups in your game, the green Create New button that lets you make a new Group, and other settings.

![Collision Groups Dialog](http://static.stencyl.com/help/images/Settings-CollisionGroupsPic.png)
 
#### How To: Assigning Actors to Groups
You can set an Actor's collision properties, and specify the group it belongs to, in the Properties page of the Actor Editor.

![stencyl-assign-actor-to-collision-group](http://static.stencyl.com/help/images/Collisions_ActorProperties.png)

#### Default Groups

Every Stencyl game starts out with a default set of Groups to help you get started. These groups have a lock next to them. Default groups cannot be edited or removed.

* Players
* Tiles
* Doodads (Scenery)
* Actors
* Regions

By default, Doodads and Regions never get involved in collisions. They may be useful if you want a quick way to designate an actor as "non-colliding"


## Shapes

As we talked about in the Animations section, Actors can take on different Animation states. For each Animation state, the Actor can have different collision bounds.

For example, if a character is standing, he may be taller. If he's ducking, he may be shorter.

![squid-game-sprite](http://static.stencyl.com/pedia2/ch3/collisions/image02.png)

Stencyl supports 3 kinds of collision shapes: Boxes, Circles and Polygons. (For Polygons, only convex shapes are allowed!)

![stencyl-collision-shapes-buttons](http://static.stencyl.com/pedia2/ch3/collisions/image01.png)

You can place an arbitrary number of these shapes, in order to form more complex ones.

![stencyl-place-collision-bounds](http://static.stencyl.com/pedia2/ch3/collisions/image04.png)

> In this example, we've made an "L" shape using 2 boxes.


## Sensors

What if you want to detect collisions, without the shapes actually colliding? For example, in Tower Defense games, the towers shoot at targets that come into range.


You'd use Sensors to make this happen. Sensors are special kinds of shapes (a yes/no flag on any shape to be precise), in which an Actor **does not physically collide** with another Actor, but **still detects the collision**.

![stencyl-collisions-sensor-option-pic](http://static.stencyl.com/pedia2/ch3/collisions/image13.png)

Just check this box in the right-hand pane of an Actor's Collision Page to make a certain shape a Sensor.

 
## Handling Collisions

**Use Events** to handle collisions. By "handling", we mean **responding to collisions with logic**. For example, if a Fireball crashes into Mario, Mario will die.

We support the following collision events.

![stencyl-collision-events](http://static.stencyl.com/pedia2/ch3/collisions/image11.png)

Regardless of which Event you pick, you'll typically see a block similar to this.

![stencyl-design-mode-collision-event-block](http://static.stencyl.com/pedia2/ch3/collisions/image06.png)

1st actor always pertains to the first actor in the "sentence." The same goes for the 2nd actor.

For example....

![stencyl-design-mode-collision-event-block-example](http://static.stencyl.com/pedia2/ch3/collisions/image15.png)

Then, when this kind of collision happens, the 1st actor will refer to the Hero and the 2nd actor will refer to the Button.

![stencyl-design-mode-collision-event-block-example-actor-references](http://static.stencyl.com/pedia2/ch3/collisions/image16.png)

Just in case, you didn't know, you can drag the "1st actor" and "2nd actor" blocks out and use them anywhere within this event.

![stencyl-design-mode-collision-event-dragging-actor-reference-blocks](http://static.stencyl.com/pedia2/ch3/collisions/image17.png)


## More Collision Handling

For any kind of collision, you can check on 3 additional bits of info.

* What side the collisions happened on
* What Groups were involved
* Collision Points (where the collisions happened)
 

#### Collision Sides
One point to watch out for is that **collision sides are based on the rectangular, bounding box** of the *shape* that collided, so if you used a circle or a polygon, pay attention to the results.

![stencyl-design-mode-collision-side-blocks](http://static.stencyl.com/pedia2/ch3/collisions/image03.png)

> **Exercise:** Stomping is one common use case for collision sides. Something is "stomped" if it was hit from the top. Can you think of other use cases for collision sides?
 

#### Groups for Colliding Shapes

![stencyl-design-mode-collision-shape-group-block](http://static.stencyl.com/pedia2/ch3/collisions/image12.png)

What is this "colliding shape" business about? It stems from the ability to **override an Actor's default group on a per-shape basis**, so that a particular shape can take on a different group.

![stencyl-design-mode-changing-collision-group-for-shape](http://static.stencyl.com/pedia2/ch3/collisions/image10.png)

When working with the "Collision Group for colliding shape" block, be sure to **compare groups directly**, rather than comparing the textual name of the Group, which can lead to bugs and crashes.

![stencyl-design-mode-collision-example-right-way](http://static.stencyl.com/pedia2/ch3/collisions/image00.png)
<br/>(This is the right way)

![stencyl-design-mode-collision-example-wrong-way](http://static.stencyl.com/pedia2/ch3/collisions/image08.png)
<br/>(This is the wrong way, don't do this!)


You can find all Group and Type "getter" blocks under Actor > Properties.

![stencyl-design-mode-collision-group-getter-blocks](http://static.stencyl.com/pedia2/ch3/collisions/image05.png)


#### Collision Points
Last but not least, you can grab exactly where collisions happened. This isn't done very often, but it's here in case you want to do any additional logic based on the collision location.

![stencyl-design-mode-collision-points-blocks](http://static.stencyl.com/pedia2/ch3/collisions/image07.png) 

## Summary

* Thanks to physics, collisions are automatic.
* Groups help you filter out collisions by specifying who collides with whom else.
* Use sensors to detect collisions without the actor being "solid."
