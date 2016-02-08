> [Introduction](http://www.stencyl.com/help/view/crash-course-invaders-1/) - [Step 1 (Create a Game)](http://www.stencyl.com/help/viewArticle/170) - [Step 2  (Create Actors)](http://www.stencyl.com/help/viewArticle/171) - [Step 3
(Actor Collisions)](http://www.stencyl.com/help/viewArticle/172/) - [Step 4 (More Actors)]
(http://www.stencyl.com/help/viewArticle/174/)-- [ Build the Game Out] -- [Step 5 (Import Sounds)]
(http://www.stencyl.com/help/viewArticle/175) - [Step 6 (Create a scene)](http://www.stencyl.com/help/viewArticle/176) - [Step 7
(Add Background Music)](http://www.stencyl.com/help/viewArticle/177) --- [Add Logic] --- [Step 8 (Make the Ship Move)]
(http://www.stencyl.com/help/viewArticle/178) - [ Step 9 (Keep the Ship on Screen)](http://www.stencyl.com/help/viewArticle/179) -
[ Step 10 (Firing Bullets)](http://www.stencyl.com/help/viewArticle/180) - [Step 11 (Destroying Bullets)]
(http://www.stencyl.com/help/viewArticle/181) [Step 12 (Destroying Enemy Ships)](http://www.stencyl.com/help/viewArticle/182)---- [
Finishing Touches ] ---- [ Step 13 (Creating a Font)](http://www.stencyl.com/help/viewArticle/183) - [Step 14 (Winning the Game)]
(http://www.stencyl.com/help/viewArticle/184) - [Step 15( Final touches)](http://www.stencyl.com/help/viewArticle/185) -----

## Step 4: Creating More Actor Types and Importing a Background

Step 21: Now that we have our new Collision Groups, we need to create our Enemy Ship Actor Type. Use the same steps as you used to 
create the Ship Actor Type to create the Enemy Ship. Here’s a brief reminder of the steps involved:

1. Click the Dashboard tab.
2. Click on Actor Types (this may already be highlighted).
3. Click the dotted line box to create a new Actor Type.
4. Name the new Actor Type "Enemy Ship".
5. Add an animation and Add a frame to import the "Alien_grabber.png" image.
6. Rename our first animation to "Normal".

![Preview](http://static.stencyl.com/pedia2/ch1/cc2/image08.png)

Step 23: We’ve created our "Enemy Ship" Actor Type and added an animation. Like we did with the Ship in previous steps, we need to set its
Physics settings. Let's change our Enemy Ship to the following settings:

 * What kind of Actor Type? Cannot be pushed
 * Can Rotate? No
 * Affected by Gravity? Disabled by Stencyl (you do not have to change it)
 
![Physics settings](http://static.stencyl.com/pedia2/ch1/cc2/image96.png)

Step 24: Choose its Collision Group by clicking the Properties tab and setting its Group to Enemies, as shown.

![Properties tab](http://static.stencyl.com/pedia2/ch1/cc2/image61.png)

> Are you missing the Enemies and Bullets groups? You need to go back to Part 3 and create them!

Step 25: Next, we need to create the "Bullet" Actor Type. Follow the same steps as you did to create the Ship and Enemy Ship but name the 
new Actor Type "Bullet". Note that when importing the graphic for the Animation, set the number of Columns to 3, as shown below.

![Set Animation](http://static.stencyl.com/pedia2/ch1/cc2/image29.png)

Step 26: We want to have slightly different Physics settings for the Bullets.

* What kind of Actor Type? Normal
* Can Rotate? No
* Affected by Gravity? No

Lastly, we set our Bullet Actor Type’s Collision Group (in the Properties tab) to Bullets.

Step 27: With our Actor Types created, we need to import a Background image to use in the Scene we’ll create later. Click the Dashboard
and then on Backgrounds.

![ Dashboard](http://static.stencyl.com/pedia2/ch1/cc2/image98.png)

Step 28: In the dialog that pops up, name the Background image Stars and press the Create button.

![ dialog](http://static.stencyl.com/pedia2/ch1/cc2/image32.png)

Step 29: Click on the "Click here to add a frame" on the left, then on Choose Image, and select the "Space Background.png" image from the assets.
> Remember " your assets are in the zip file you download earlier

![ Add Frames](http://static.stencyl.com/pedia2/ch1/cc2/image33.png)

>Have you saved recently? Now would be a great time to do so if you haven't!
Now it's time to import our sound assets.

***

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/viewArticle/173/">Continue to Step 5 &rarr;</a>

*** 
