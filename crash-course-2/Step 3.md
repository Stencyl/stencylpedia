> [Introduction](https://www.stencyl.com/help/viewArticle/170) - [Step 1 (Create a Game)]
(https://www.stencyl.com/help/viewArticle/171) - [Step 2  (Create Actors)](https://www.stencyl.com/help/viewArticle/171) - [Step 3
(Actor Collisions)](https://www.stencyl.com/help/viewArticle/172/) - [Step 4 (More Actors)]
(https://www.stencyl.com/help/viewArticle/174/)-- [ Build the Game Out] -- [Step 5 (Import Sounds)]
(https://www.stencyl.com/help/viewArticle/175) - [Step 6 (Create a scene)](https://www.stencyl.com/help/viewArticle/176) - [Step 7
(Add Background Music)](https://www.stencyl.com/help/viewArticle/177) --- [Add Logic] --- [Step 8 (Make the Ship Move)]
(https://www.stencyl.com/help/viewArticle/178) - [ Step 9 (Keep the Ship on Screen)](https://www.stencyl.com/help/viewArticle/179) -
[ Step 10 (Firing Bullets)](https://www.stencyl.com/help/viewArticle/180) - [Step 11 (Destroying Bullets)]
(https://www.stencyl.com/help/viewArticle/181) [Step 12 (Destroying Enemy Ships)](https://www.stencyl.com/help/viewArticle/182)---- [
Finishing Touches ] ---- [ Step 13 (Creating a Font)](https://www.stencyl.com/help/viewArticle/183) - [Step 14 (Winning the Game)]
(https://www.stencyl.com/help/viewArticle/184) - [Step 15( Final touches)](https://www.stencyl.com/help/viewArticle/185) -----

## Step 3: Actor Collisions
Step 15: We’ve got one Actor Type so far, but before we can go further, we need to organize our Actor Types into what are called Collision 
Groups. The Collision Group an Actor belongs to determines what other Actors it can (and can’t) collide with. To start, we click the Settings
button at the top of Stencyl's interface, in the upper left.

![settings](https://static.stencyl.com/help/images/CC2-Settings-Button.png)

Step 16: A new dialog will pop up that shows the settings in our game. Different options are down the left side, we want to go to the car icon 
with the label Groups. The center area of the Game Settings dialog will change to show us our Collision Group settings for this game.

![Game Settings dialog](https://static.stencyl.com/help/images/CC2-Collision-Groups-Settings.png)

(Note in the screenshot we already created Enemies and Bullets as Groups - we'll show you how to create a Group in the following steps).

Step 17: Click the green Create New button along the top of the window to create a new Collision Group.

![Create New](https://static.stencyl.com/pedia2/ch1/cc2/image71.png)

Step 18: When the dialog box pops up, name it "Enemies", as shown, and hit the Create button. We can leave the Description field blank.

![New Group](https://static.stencyl.com/pedia2/ch1/cc2/image57.png)

Step 19: Next, let's click the green Create New button again and create another group. This time let's call it "Bullets".

![Another New Group](https://static.stencyl.com/pedia2/ch1/cc2/image109.png)

Step 20: By default, our new groups are not set to collide with anything else. Let's change their settings so they do.

We should have the Bullets group selected in the list to the right (if not, click on it). In the central settings area, we can see the "Bullets" 
name, the description, and a "Collides With" grid of buttons - one for every other group that we have in our game.

Within the "Bullets" group's settings, click the Enemies button once so it turns green, as shown below. Leave all the other buttons grey. This 
means any Actor Types that belong to the Bullets Group will only be able to collide with Actor Types in the Enemies Group.

![Groups](https://static.stencyl.com/pedia2/ch1/cc2/image44.png)

Click the OK button in the bottom-right corner of the Game Settings dialog box to close the window.

Now that we have our Collision Groups set so our Bullets will collide with any Actors that belong to the Enemies Group, it's time to create 
two new Actor Types, our "Bullets" Actor Type and our "Enemy Ship" Actor Type.

***

<a role="button" class="btn btn-primary btn-lg action-button2" href="https://www.stencyl.com/help/viewArticle/173/">Continue to Step 4 &rarr;</a>

*** 
