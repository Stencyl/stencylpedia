> [Introduction](https://www.stencyl.com/help/view/crash-course-invaders-1/) - [Step 1 (Create a Game)](https://www.stencyl.com/help/viewArticle/170) - [Step 2  (Create Actors)](https://www.stencyl.com/help/viewArticle/171) - [Step 3
(Actor Collisions)](https://www.stencyl.com/help/viewArticle/172/) - [Step 4 (More Actors)]
(https://www.stencyl.com/help/viewArticle/174/)-- [ Build the Game Out] -- [Step 5 (Import Sounds)]
(https://www.stencyl.com/help/viewArticle/175) - [Step 6 (Create a scene)](https://www.stencyl.com/help/viewArticle/176) - [Step 7
(Add Background Music)](https://www.stencyl.com/help/viewArticle/177) --- [Add Logic] --- [Step 8 (Make the Ship Move)]
(https://www.stencyl.com/help/viewArticle/178) - [ Step 9 (Keep the Ship on Screen)](https://www.stencyl.com/help/viewArticle/179) -
[ Step 10 (Firing Bullets)](https://www.stencyl.com/help/viewArticle/180) - [Step 11 (Destroying Bullets)]
(https://www.stencyl.com/help/viewArticle/181) [Step 12 (Destroying Enemy Ships)](https://www.stencyl.com/help/viewArticle/182)---- [
Finishing Touches ] ---- [ Step 13 (Creating a Font)](https://www.stencyl.com/help/viewArticle/183) - [Step 14 (Winning the Game)]
(https://www.stencyl.com/help/viewArticle/184) - [Step 15( Final touches)](https://www.stencyl.com/help/viewArticle/185) -----

##Part 6: Creating a Scene

Step 32: Click Scenes in the Dashboard, then we need to click the dotted line box to create a new Scene.

![Dashboard Toolbar](https://static.stencyl.com/pedia2/ch1/cc2/image85.png)

![Dotted Line](https://static.stencyl.com/pedia2/ch1/cc2/image39.png)

Step 33: After we hit that button, a dialog (shown) will pop up that lets us set some basic parameters for your Scene. Note you can choose
the size of your Scene either using Tiles (which will use the Tile Width and Height, as shown) or in pixels. In this case we’re using Tiles and
will use the default values, as shown. Let's give it a name of "Level One", and then as usual, we click Create to get Stencyl to make our new
scene for us.

![Create New](https://static.stencyl.com/pedia2/ch1/cc2/image21.png)

Once we do, Stencyl will open up our new scene in the Scene Designer.

![Scene](https://static.stencyl.com/help/images/CC2-Scene-Editor-V3.png)

Step 34: To keep things simple, we’re only going to add the background image we imported earlier rather than add any Tiles. Backgrounds
are one of the layer types we can have in our scene. To add one, we need to click the small + icon in the Layers list. In there we select
**New Background Layer.**

> Read more about [ Backgrounds Here ](https://www.stencyl.com/help/view/backgrounds-and-foregrounds/). Note this link is not part of the Crash Course

![Layer](https://static.stencyl.com/help/images/CC2_add_background_layer.png)

Step 35: The "Choose a Background" dialog box will appear for us, and we can click on our Stars background and then click OK.

![Choose Background](https://static.stencyl.com/pedia2/ch1/cc2/image02.png)

Step 36: Notice that our new Stars background layer is higher in the list than the default "Layer 0"? This means that if we try to add anything
to Layer 0 it will be underneath our Stars background! Clearly this is not ideal, so to prevent this from happening, let's move the Stars
background to the bottom of the Layers list. We can do this by clicking the down arrow at the bottom of the Layers list while the Stars
background is selected.

![Move Layer](https://static.stencyl.com/help/images/CC2_send_layer_to_back.png)

Now our intial setup of the scene is done, and the main window of the Scene Designer should look like the image below.

![Image Below](https://static.stencyl.com/pedia2/ch1/cc2/image72.png)

Step 37: We’ve got our Scene, so let’s test it. Press the green Test Scene button and after a few moments we should see our Scene appear in 
a browser or Flash.

![Test Scene](https://static.stencyl.com/pedia2/ch1/cc2/image113.png)

![Flash](https://static.stencyl.com/pedia2/ch1/cc2/image43.png)

If the Scene appears, everything is working, and we can move ahead. If not, we can help you. Please visit our [Ask A Question](https://community.stencyl.com/index.php/board,3.0.html) in Forums.Please label the title the topic **Crash Course: Part 6**. Please state your problem and what you were doing last. 
Lets keep going!

Step 38: Click the **Actors tab** in the Scene Designer, in the Palette on the right. You should see the three Actor Types you created earlier.

![Actors](https://static.stencyl.com/pedia2/ch1/cc2/image102.png)

Step 39: Now we want to place individual Actors in the Scene. When placing actors, they are put on the Layer that is currently selected. As a 
result, we need to remember to click on **Layer 0** to select it as the current layer.

To place actors, we use the **Pencil tool** as shown below; select it now if it is not already active.

![Pencil Tool](https://static.stencyl.com/pedia2/ch1/cc2/image112.png)

With the Ship selected from the Actor Type list, **Layer 0** selected (and above the background layer!) and the **Pencil tool** active, move our 
cursor over to the bottom-center of the Scene and left-click once. The Ship will appear. We only want one Ship for the player to control.

Note that we want the Ship to be within the scene boundaries, so don't put him in the grey "out of bounds" area! Put him inside the scene like in the image below.

![Ship](https://static.stencyl.com/pedia2/ch1/cc2/image90.png)

> **Tip**: To place Actors at even intervals, hold down the Shift key, which will align an Actor with the Tile grid. You can make the grid appear by pressing the Show Grid button.

![Grid](https://static.stencyl.com/help/images/CC2_grid_button.png)

Step 40: Next, select the Enemy Ship so we can place a few in the Scene. We can use the Shift key to space them evenly as shown in the image below.

![Grids](https://static.stencyl.com/pedia2/ch1/cc2/image55.png)

> **Tip** : If any of your Actors don't appear on screen even though you placed them in the Scene, make sure you check the game window's (the viewport's) settings. Its Width should be 640 and Height should be 480. Click **Settings** and then **Display** to change this. If you place an Actor outside the bounds of the viewport, you will not see the Actors you placed in your Scene. Also, note you can make a Scene that is larger than the game's viewport. To allow the player to see and move to other parts of the Scene, you'll need to implement a camera and camera scrolling, but doing that is outside the scope of this Crash Course. You can [read more about implementing a camera here](https://www.stencyl.com/help/view/the-camera/).

Step 41: Now we have a basic, complete Scene. Make sure it works via the **Test Scene** button again. We should see your Ship at the bottom of the Scene and the five Enemy Ships hanging out near the top.

![Test Scene again](https://static.stencyl.com/pedia2/ch1/cc2/image38.png)

We've got our Actors and Scene set up, so now it's time to start learning how to use Stencyl's Design Mode. To start, we're going to add background music to our Scene.

***

<a role="button" class="btn btn-primary btn-lg action-button2" href="https://www.stencyl.com/help/viewArticle/177/">Continue to Step 7 &rarr;</a>

*** 
