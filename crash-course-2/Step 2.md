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

## Step 2: Create Actors
Step 3: Now that we have a blank game, it’s time to create our Actor Types. We’re going to start with our spaceship, which the player will control. Click the Actor Type button in the Dashboard menu on the left (under Resources, as shown).
![actor types](http://static.stencyl.com/pedia2/ch1/cc2/image80.png)

Step 4: Next, click the large box in the workspace on the right (shown below) to create our first Actor Type.
![actor types creation](http://static.stencyl.com/pedia2/ch1/cc2/image108.png)

Step 5: We will see the "Create New..." dialog appear (shown below). Name your Actor Type "Ship" as shown. Click the Create button.
![http://static.stencyl.com/pedia2/ch1/cc2/image07.png]

Stencyl will create our new Actor Type and then open it for us.

Step 6: Our Actor Type does not yet have any images in it, we need to fix that so it can be seen by players. All images for an Actor Type are gathered in Animations, so we need to import images for these Animations. To do this, we need to first create at least one Animation to hold the images.

Since Stencyl opened the new Actor Type for editing in the Appearance tab, we are already where we need to be. Click the large box with the dotted line in the workspace on the right (shown below).
![Add animations](http://static.stencyl.com/pedia2/ch1/cc2/image110.png)

Stencyl will create a new Animation for us and open it in the workspace.

Step 7: We are now looking at the Animation Editor for the new Animation, which by default will be named "Animation 0".

An Animation typically represents a “state” that an Actor could be in, such as Walking, Running, Jumping, etc. As such, it is ideal for us to rename our Animation so that later we can easily identify what state it represents. We need to erase "Animation 0" from the Name field and type "Flying" into it.

Now that our new Animation has been named properly, let's give it some images. We will click on the "Click here to add a frame" box to open our image importer.

![rename animation](http://static.stencyl.com/help/images/CC2_image56.png)

Step 8: The image importer dialog below will pop up for us. First we have to select an image to import; click the Choose Image button.
![add image](http://static.stencyl.com/help/images/CC2_image19.png)

We should have saved and extracted the example assets earlier somewhere on our computer, so we should navigate to that folder. We want to open the "Ship_flying.png" image for this Animation (if you still need to download the assets, click [here](http://static.stencyl.com/pedia2/ch1/cc2/assets.zip) to download them).

![select asset](http://static.stencyl.com/help/images/ship_flying_selected.png)

Step 9: Individual "frames" of an Animation image are commonly stored in a single larger image. In this case, Ship_flying.png contains four frames. Of course, Stencyl does not automatically know this, so we need to change some settings so the image is not imported as one single, large frame. Set the value in the “Columns” field to 4. This will split our image evenly into four frames separated by black lines, as shown below. Once ready, click Add and Stencyl will import the image as four frames of our Flying animation.
![Add frames](http://static.stencyl.com/help/images/CC2_image40.png)

Step 10: Now that we have our single Animation, we need to choose the correct Physics settings for our Ship Actor Type. Click the Physics tab, as shown below.

![Physics tab](http://static.stencyl.com/pedia2/ch1/cc2/image14.png)

Step 11: The first page that will appear is the “General” page under Physics. Let's leave the "What kind of Actor Type?" option set to Normal, but set "Can Rotate? and "Affected by Gravity?" both to No.

![ Physics settings](http://static.stencyl.com/pedia2/ch1/cc2/image82.png)

Step 12: Now we need to set the Collision Group that our Actor Type is a member of. This will allow us to specify what our Ship can collide with and what it can’t. Click the Properties tab (shown below).

![Properties Tab](http://static.stencyl.com/pedia2/ch1/cc2/image94.png)

Step 13: Set the Group to "Players", as shown. If we want to create more Groups, there is an Edit Groups button on the right. You can read more about creating Groups [here](http://www.stencyl.com/help/view/collisions-and-groups/). Note the Players Group is built into Stencyl and will appear by default on when we click the dropdown, so we don't need to Edit Groups at this point.

![choose a group](http://static.stencyl.com/pedia2/ch1/cc2/image13.png)

Step 14: We want to save our Ship Actor Type (and the game) by clicking File and then Save Game. Note that there is a keyboard shortcut available for this, as well as the "Save Game" disk icon.

![Save Game](https://www.dropbox.com/s/41lgiq6jieot12p/Save%20Game.png?raw=1)

We have our Ship Actor Type set up now, so it's time to move on to determining how our Ship, and the other Actor Types we'll create, can collide with one another.

***

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/viewArticle/172/">Continue to Step 3 &rarr;</a>

*** 

