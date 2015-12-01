## Contents

* Introduction
* Quick Guide
* Best Practices
* Reference
  * Main Page
  * Resources Page
  * Scenes Page
  * Preferences Page
  * Using Blocks
* FAQ
* Challenge


## Introduction

Stencyl allows you to group resources into categories and bind those categories to specific scenes in order to minimize memory usage. These "categories" are called **Atlases**.

Atlases work on both desktop and mobile games. A game that's been set up to use atlases will function properly on other platforms, but it won't take advantage of the feature.

## Quick Guide

In this Quick Guide, we'll go through the basic steps to convert a simple single-atlas game into a multi-atlas one.

1. With a game open, let's open up our **Game Settings**, either from the Toolbar or the View menu.

	![Atlases Section](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-0.png)

1. Let's click over to the **Atlases** section via the left sidebar in Game Settings.

	![Atlases Section](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-1.png)
	
1. We'll double click on Atlas 2 in the right sidebar and rename it to "Pirate Ship"

1. We'll do the same for Atlas 3, except we'll change its name to "Island" instead.

	![Main Sidebar](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-2.png)

1. Now let's switch over to **Resources** page

	![Resources Button in Toolbar](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-3.png)
	
1. The Main Atlas should be open by default. This is where we'll put our most common resources that we'll want available in almost every scene. Whenever you add a new resource to the game, it will be placed in the Main Atlas by default.

	![Resources, Main Atlas](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-4.png)
	
1. We can view other atlases from the **Atlas dropdown menu**. Let's switch over to **Pirate Ship**.

	![Resources, Pirate Ship](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-5.png)

1. On the right, we have every resource not in the currently open atlas, Pirate Ship. We're going to drag over all of the resources we want to have in Pirate Ship.

	![Pirate Ship with resources](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-6.png)
	
	Keep in mind that these resources will *only* be available in scenes that have Pirate Ship atlas bound to them. Common resources (such as the player, interface elements and pickups) will typically stay in the Main Atlas.

1. Now, we're going to switch over to **Island** (from the Atlas dropdown, just as we did in Step 7) and drag all of the Island-exclusive resources over.

	![Island with resources](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-7.png)

1. Let's check out our **Main Atlas** now. As you can see, this atlas contains Health Pickup, Player and Sky Background, which are indeed elements we'll want to have available all across our game.

	![Main Atlas with remaining resources](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-8.png)

1. Now we're going to switch over to the **Preferences** page.

	![Preferences Button in Toolbar](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-9.png)
	
1. Scenes have atlas binding disabled by default, which means that every atlas will be loaded when we switch to those scenes. However, we want to be able to specify which atlases we want loaded for each scene. To change this for every currently existing scene, we'll click on **Enable Atlas bindings for all Scenes**.

	![Preferences, Enable Atlas bindings for all Scenes](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-10.png)
	
1. Now, let's switch over to the "Scenes" page.
	
	![Scenes Button in Toolbar](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-11.png)
	![Scenes](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-12.png)

1. We want to switch the **Primary View dropdown** from Scenes over to **Atlases**.

	![](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-13.png)

1. We're gonna switch over to the Pirate Ship atlas from the list on the left

	![Pirate Ship item](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-14.png)

1. We only want the resources in this atlas to be available in pirate-ship-themed levels, so we'll *uncheck* **Include in all Scenes** on the right. If we were to leave it checked, the Pirate Ship atlas would load in every scene.

	![](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-15.png)

1. Below that, we'll *check* **Ship Interior** and **Ship Deck**. We've now made it so the resources within the Pirate Ship atlas will be available to those two scenes, but no others. This is fine since we're not using our Pirate Ship resources in any other scenes.

	![](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-16.png)

1. From the list on the left, we'll switch the current atlas to **Island** and *uncheck* **Include in all Scenes**, just as you did with the Pirate Ship atlas, except this time we'll check Island Beach and Island Jungle as the scenes to bind this atlas to.

	![](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-9/images/atlases-17.png)
	
### We're All Set Up!

We've successfully converted our single-atlas game to a multi-atlas one! Assuming we don't try and use resources from atlases that aren't available to our current scene, everything should work as intended.


## Best Practices

Our goal is to minimize our game's memory footprint. You do that by only loading what you're going to use in your scene.

However, realize that **every game is different**. What works best for one game won't necessarily work that well for another. Because of that, we can't tell you exactly how to divide and categorize your resources. It's up to you to figure that part out. Nonetheless, here are some general tips:

### Combine Related Resources Together Into Atlases

If you're fairly sure you'll usually be using a certain group of resources in conjunction with each other, consider grouping them into the same atlas.

For example, you could have an "Underwater" atlas that features seabed tiles, various fish actors and a water-themed music track. Or if you wanted to be more specific in your atlas assignments, you could even give individual enemies their own atlases (especially if individual enemies use multiple resources).

### Watch Your Memory Usage

Take note of how much memory rises by using the FPS Monitor or telemetry.

### Be Organized

Although most games probably won't require too many atlases, [large, intensive games](http://community.stencyl.com/index.php/topic,30809.0.html) could possibly require hundreds. Keep your atlases and resources named and organized in a logical fashion to make things easier on yourself.

## Reference

(Cover the whole UI - leave this part for later)


## FAQ

### Is there a limit to how many resources can go into an atlas?

Nope.

### Is there a performance penalty for having too many atlases?

No. The only disadvantage is that it becomes harder for you (the creator) to keep track.

### Is there a way to load/unload an atlas during a scene?

No.

### Are atlases actually stored in one big, combined image?

Not anymore. They were in the past but that no longer is the case.

### What platforms do atlases apply to?

iOS, Android, Windows, Mac and Linux.


## Challenge: Making a Preloader

At the time of writing, Stencyl doesn't support preloaders on mobile and desktop platforms. For some games, this may generate an awkward pause at the start. Let's create a preloader from scratch using what we know.

* Tell all atlases not to initially load besides the main atlas.
* Make the first scene show a loading graphic of your choice (bonus points if it's animated or moves across the screen to give the semblance of progress).
* Load the atlases you need.
* Then, switch to the "real" first scene.

That will get you a basic preloader, albeit one without a progress bar. Now, here's the second part of the challenge - add an accurate loading bar, using just the basic facilities described in this article.

> **Hint**: Load your game, one atlas at a time. Preferably make it so you have one master loading scene rather than many.