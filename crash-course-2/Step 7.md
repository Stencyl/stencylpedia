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

##Part 7 : Adding Background Music to A Scene

Step 42: Now we need to add background music. Click the **Events** tab from within the Level One scene, which will bring up *Stencyl Design*
mode. We can use this to create game logic. In this case, we’re creating an Event directly rather than creating a fully modular Behavior.

> [Read more on Events](http://www.stencyl.com/help/view/events-reference/), Not part of Crash Course

> [Read more on Behaviors](http://www.stencyl.com/help/view/working-with-behaviors/), Not part of Crash Course

**Important Note**: Generally, you want to create Behaviors because you can add them to any Actor Type or Scene that you want. Behaviors are made up of Events, so think of a Behavior as a portable Event container. We’re attaching Events directly here because we won’t be re-using anything we’re making here - the movement Event for our Ship won’t apply to the Enemy Ship Actors, for example.

![ Events Tab](http://static.stencyl.com/pedia2/ch1/cc2/image86.png)

Step 43: Click the **+ Add Event** button in the Events pane on the left, move our mouse over the **Basics** option, and click on the **When Creating** Event.

![When Creating Event](http://static.stencyl.com/pedia2/ch1/cc2/image04.png)

The following "Created" event should appear as the first and only entry in our Events list.

![Created Event](http://static.stencyl.com/pedia2/ch1/cc2/image70.png)

Step 44: Now that we have the "when created" block in our workspace, we can add logic to our event. If you look all the way to the right, there is a "palette" of different logic blocks available to us, neatly organized into different categories. We are going to work with our music, so click the **Sound & Images** button in the Palette.

![Sound & Images](http://static.stencyl.com/help/images/CC2_image79.png)

Next, left click and drag the **Play Sound** block in the Playback subcategory (shown above) over into the **When Created** block in the work area, and when the white bar appears, release the button. The block will snap into place.

![block snap](http://static.stencyl.com/pedia2/ch1/cc2/image97.png)

Step 45: Left-click on the Sound dropdown button and a dialog will appear that lets you select which sound to play.

![left click](http://static.stencyl.com/pedia2/ch1/cc2/image16.png)

Step 46: Click the Choose Sound option and select the song we imported earlier.

> **Tip**: Part 5 of this tutorial covers importing sounds. You can [read about importing sounds again here](http://www.stencyl.com/help/viewArticle/175).

![Music](http://static.stencyl.com/pedia2/ch1/cc2/image69.png)

The block will change to show the song it will play.

![Play Music](http://static.stencyl.com/pedia2/ch1/cc2/image91.png)

Step 47: Save your game (press Ctrl S or option S), then press the green Test Scene button( Go to **scene** and click the green button in the top left corner). The music should be playing in the background.

Click on the image below to play a sample flash file of what your game should look like at this point.

<a href="http://static.stencyl.com/pedia2/ch1/cc2/no-movement.swf">![Test Demo](http://static.stencyl.com/pedia2/playitnow.png)</a>

We'll get to using the Explosion sound effect that we uploaded earlier when we handle destroying the Enemy ships. Now it’s time to move on to an Events that will let the player move the Ship using keyboard keys.

***

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/viewArticle/178">Continue to Step 8 &rarr;</a>

*** 
