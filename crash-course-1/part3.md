> [Part 1 (Intro)](http://www.stencyl.com/help/viewArticle/143/) - [Part 2  (Resources)](http://www.stencyl.com/help/viewArticle/144/) - [Part 3  (Actors)](http://www.stencyl.com/help/viewArticle/145/) - [Part 4 (Create a Scene)](http://www.stencyl.com/help/viewArticle/146/) - [Part 5 (Test your Game)](http://www.stencyl.com/help/viewArticle/147/)

## Customizing Actors (Part 3 of 5)
We’ve already got some Actor Types in our game, but they aren’t very interesting yet, as without Behaviors, Actor Types can’t do very much.

### Creating an “Enemies” Group
Before we jump into customizing our actors, let’s quickly create a **Group** to categorize our enemies into.

> **Definition:** **Groups** are used to determine what kinds of Actor Types collide with each other. Groups can also allow you to treat different classes of Actor Types differently. We've got an [entire article](http://www.stencyl.com/help/view/collisions-and-groups/) devoted to Groups and how they affect collisions.

1) Click on the **Settings** button in the toolbar. The **Game Settings** window should appear. This is where practically all of your game-wide settings are configured.

![Game Settings](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-28.png)

2) Switch to the **Groups** section by clicking the relevant button in the Settings sidebar.

![Collision Groups](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-29.png)

3) Click the green **Create New** button around the top of the window.

![Create New](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-30.png)

4) Type **Enemies** in the name field and hit **Create**

![Create a New Group...](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-31.png)

5) Under **Collides With**, click on **Players** and **Tiles**. The buttons you clicked should turn green. This indicates that Enemies can collide with Players and Tiles.

![Collides With](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-32.png)

6) Click the **OK** button in the bottom-right to dismiss the window.

![OK](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-33.png)


### Customizing Noni
To breathe some life into our main character, Noni, and our enemy, Clown, let’s take a more in-depth look at the Actor Type Editor and add the Behaviors included in the Crash Course Kit.

If you haven’t closed the **Noni** Actor Type yet, click its tab to select it. Otherwise, navigate to the Dashboard and double-click on Noni from the Actor Types section of the Dashboard.

![Actor Types](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-7.png)

1) The Appearance page of the Actor Editor appears by default. Skip over to the **Properties** page by clicking its button at the top of the editor.

![Properties](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-17.png)

2) Check to see that Noni is a member of the **Players Group**. This will ensure that Stencyl will handle the collisions how we intend.

![Choose Group](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-18.png)

3) Visit the **Physics** page by clicking the **Physics button** at the top of the editor.

![Physics Button](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-19.png)

4) Under **General**, toggle the **Can Rotate?** setting to **"No"**. This will ensure that our actor is always oriented with its feet facing the ground, no matter what.

![Can Rotate?](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-20.png)

5) We’re going to move on to the **Behaviors** section, where the real crux of the customization takes place. Get there by clicking the **Behaviors button** (right next to the Appearance button). The following screen will appear:

![Behaviors](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-21.png)

6) Click on the **Add Behavior button** in the lower-left hand corner.

7) When the dialog appears, double-click the **Walking Behavior**.

![Choose a Behavior](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-22.png)

7) We’re taken back to the Behaviors page of Noni. Notice the addition of the Walking Behavior in the list on the left, as well as all of its configurable **Attributes** in the main pane.

> **Definition:** **Attributes** are customizable values that make Behaviors reusable and easy to modify. For more about Attributes, see our [introductory article](http://www.stencyl.com/help/view/attributes/) about them.

![Walking](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-23.png)

8) Let’s start customizing these **Attributes**. Some of the Attributes have default values that we can use, like Speed, whereas others we will have to set ourselves.

First, change **Move Right Key** and **Move Left Key** to the _**right**_ and _**left**_ Controls respectively.

![Control Attributes](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-24.png)

> **Definition:** **Controls** map physical keyboard keys or gamepad buttons to names you can refer to in your behaviors. If you ever decide to change the actual key, you just have to change it in one place. See our Controls article for more information.

9) Then choose the desired animations by clicking on the **Choose an Animation** button and selecting the animation sequences you want.

![Animation Attributes](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-25.png)

That’s it for the first Behavior!

10) Let’s add the rest and customize them in a similar way. To add more Behaviors, click the **Add Behavior** button at the lower left-hand corner of the editor.

![Add Behavior](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-26.png)

**Add and configure the following Behaviors:**

* **Jumping:** Make the following modifications to the default values: Choose _**action1**_ for **Jump Key**. Add the **Jump Sound** so Stencyl will play a sound effect when Noni jumps. Finally, choose _**Jump Right**_ and _**Jump Left**_ for the **Jump Right** and **Jump Left** animations, respectively. 

 ![Jumping](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-27.png)

* **Stomp on Enemies:** Set **Stompable Group** to _**Enemies**_ (the group we created at the beginning of this section) and **Jump Key** to _**action1**_.
    
 > **Note:** You might have to reload the document in order for the Enemies group to show up as an option. Do this by using the keyboard shortcut Ctrl-R (Command-R on Mac), or by navigating to File > Reload Document.
<a name="part5reference"></a>
 ![Stomp on Enemies](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-34.png)

* **Die in Pit and Reload:** Nothing to configure here. Just make sure you add it.

Here are all the Behaviors you should have added to Noni:

![All Behaviors for Noni](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-59.png)

### Customizing Clown

**Clown** will be simpler to set up than Noni. Switch over to its tab (or open it from the Dashboard, if need be).

![Actor Types](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-10.png)

1) Click on the **Properties button**, as we did with Noni.

2) Go ahead and change Clown’s group to **Enemies**.

![Choose Group: Enemies](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-35.png)

3) All that’s left to do with Clown is to add a single Behavior. Click the **Behaviors button** and add the **Stompable** Behavior. Customize the following Attributes as such:

![Stompable Behavior](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/crash-course-1/images/crash-course-36.png)

> **Note:** As you may be able to tell, this Behavior makes Clown "stompable" like a Goomba in Super Mario Bros. Clown will "die" when hit from above and play a sound when this happens. If you click the Edit Behavior button, you can peek at the "code" behind this Behavior.

***

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/viewArticle/146/">Continue to Part 4 &rarr;</a>

***
