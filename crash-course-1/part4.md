## Creating a Scene (Part 4 of 5)
Now that we have our resources in place and our Actor Types configured, we're going to create a Scene.

> **Definition:** **Scenes** are game levels that get populated with the tiles and Actors we've created. You can even attach Behaviors to Scenes, although we won't be doing so in this tutorial.

### Creating a New Scene
1) From the **Dashboard**, click the **Scenes** category, followed by the large dashed rectangle that reads, **“This game contains no Scenes. Click here to create one.”**

![RESOURCES](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-37.png)

![This game contains no Scenes. Click here to create one.](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-38.png)

2) The **Create New Scene** dialog will appear. Enter a **name** of your choosing.

![Create New... Scene](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-39.png)

3) Make note of the **Tile Width** and **Tile Height** fields. It’s *imperative* for these to be consistent with the tilesize of the tilesets you’re using. Our tileset’s tilesize is 32x32, so we’ll leave these fields unchanged.

![Tile Width, Tile Height](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-40.png)

4) Let’s have Stencyl generate a sky background for us by clicking in the **Color dropdown** and selecting **Vertical Gradient**. Select two colors by clicking inside the white boxes and then clicking on the desired colors. The first box represents the starting color at the top of the screen and the second box represents the color it shifts to as it approaches the bottom of the screen.

![Gradient Fields](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-41.png)

5) When you’re all finished, the dialog should look something like the image below. Click **Create** when you’re finished.

![Create New... Scene, Final](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-42.png)

6) The **Scene Designer** will open. The interface may remind you of some popular 2D art programs, and it works quite similarly.

![Scene Designer](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-43.png)

### Placing Tiles
Let’s add some tiles to our **Scene**. They’ll form the ground that our characters will stand on. 

1) First, make sure that the **Pencil Tool** is selected from the toolbar on the left-hand side of the canvas.

![Pencil Tool](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-44.png)

2) Click on the upper left-hand grass tile in the **Tiles** section of the **Palette** (on the right side of the screen, by default).

![Top-left tile](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-45.png)

3) Place it in the bottom left-hand corner of the Scene by **left-clicking**.

![Placing tile](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-46.png)

4) Next, select the middle grass tile in the top row of the Palette.

![Middle tile](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-47.png)

5) With the left mouse button held down, click and drag to fill the bottom row, leaving just a single spot in the corner.

![Placing tile across bottom-center](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-48.png)

6) Now select the right-most grass tile in the same row of the Palette.

![Top-right tile](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-49.png)

7) Place it in the remaining empty spot of the Scene’s bottom row.

![Placing tile on right](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-50.png)

> **Tip:** When you select tiles to place, if you choose more than one tile in the Palette at a time, you can place the group of tiles you selected. See the screenshot below.

![Selecting middle tiles](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-51.png)

### Placing Actors
Now we get to add Noni and Clown to the Scene.

1) Click on the **Actors** button in the Palette and select **Noni**.

![Actor Palette](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-52.png)

If you move your mouse over the Scene, you’ll notice that Noni follows the cursor. **Left-click** near the ground to place it in the scene.

![Noni, placed in scene](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-53.png)

> **Tip:** If you hold down the **Shift** key, you can **snap the Actor to the grid**.

2) Now do the same thing with **Clown**. Place a few in the Scene.

Your final scene may look something like this:

![Scene with Noni and three Clowns](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-54.png)

### Adding Gravity
Now we just need to make sure our actors fall to the ground when they're in the air. Go to the **Physics** page by pressing the **Physics button** at the top of the editor. In the **Vertical Gravity** section, type in “85”.

![Gravity (Vertical): 85](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-56.png)

Of course, higher values will result in stronger gravity, and lower values will result in lower gravity.

### [Continue to Part 5](http://www.stencyl.com/help/viewArticle/147/)