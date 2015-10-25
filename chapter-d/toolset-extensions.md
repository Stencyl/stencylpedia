<table style="border:1px solid #cccccc;"><tr>
<td width="8" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Engine Extensions</h5>
<ul class="pedia-links">
<li><a href="http://www.stencyl.com/help/view/how-to-create-engine-extension/">The Basics</a></li>
<li><a href="http://www.stencyl.com/help/view/how-to-create-native-engine-extension/">iOS / Android</a></li>
<li><a href="http://www.stencyl.com/help/view/flash-extensions/">Flash</a></li>
</ul>
</td>
<td width="30" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Advanced Topics</h5>
<ul class="pedia-links">
<li><a href="http://www.stencyl.com/help/view/native-events/">Native Events</a></li>
<li><a href="http://www.stencyl.com/help/view/adding-blocks/">Custom Blocks</a></li>
<li><a href="http://static.stencyl.com/api/33/">API</a></li>
</ul>
</td>
<td width="30" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Toolset Extensions</h5>
<ul class="pedia-links">
<li><a href="http://www.stencyl.com/help/view/creating-extensions/">Main Guide</a></li>
<li><a href="http://api.stencyl.com/extensions/">API</a></li>
</ul>
</td>
</tr>
</table>


## Contents

* Introduction
* Concepts - Hooks and Callbacks
* Getting Started
* Publishing an Extension
* Reference
  * Javadocs (API)
  * Callback Reference
  * GUI API Reference
  * Data API Reference
 

## Introduction

Extensions are small applications or controls that add new functionality to Stencyl. They serve the same purpose as extensions for web browsers, such as Firefox and Chrome. Extensions allow the community to extend the utility of Stencyl itself to fit its unique needs. 

#### Our Best Extension - Dialog System

The most notable extension created with Stencyl at the moment is the [Dialog Extension](http://dialogextension.com/), a powerful, easy to use dialog system that supports pretty much every feature you'd need.

![dialog-extension](http://static.stencyl.com/pedia2/ch4/text/dialog.png)
 
#### What do you need to know?

* Java
* Swing and/or some experience creating GUIs

Although we provide an API that makes it simple to build a GUI with no Swing knowledge, knowing it will give you the ability to create more powerful extensions.

#### Can ___ be an extension?

As long as the extension has something to do with Stencyl, it's generally doable. If you're looking to extend the engine, [look here](http://www.stencyl.com/help/view/how-to-create-engine-extension) instead.

For source code examples of existing extensions, you can see the [polydes](https://github.com/justin-espedal/polydes) collection of extensions.

If you have an idea for an extension but you need some new hooks, callbacks, or capabilities on Stencyl's side, [let us know](http://community.stencyl.com/index.php/topic,3491.0.html) and we'd be happy to work together to bring your extension to life!

## Concepts - Hooks and Callbacks

Developing an extension is simple once you master two key concepts: hooks and callbacks.

#### Hooks

Hooks determine **where your extension is displayed** in Stencyl's GUI. At this time, the available places where an extension an hook into include:

* Extensions menu in the menu bar
* Extensions menu in the dashboard sidebar

#### Callbacks

Callbacks are functions that you implement inside your extension. These callback functions are called at specific times in Stencyl's lifecycle. 

For example, there are callbacks for these activities:

* User opens Stencyl
* User opens a game
* User saves a game

Every callback is documented at the end of this manual and inside our API docs.

 
## Getting Started - How to Create an Extension

#### Requirements

You will need the following before you begin.

* Java Development Kit (JDK) 1.8. Do not use anything older.
* The latest version of Stencyl. Avoid targeting old versions of Stencyl.
* Eclipse, Netbeans or any setup that can run an ANT Build. 

> ANT is a task running system for Java. We'll go through it when we reach the point where it's needed.
 
#### Download the Toolset SDK

[Download](http://static.stencyl.com/extensions/Stencyl-SDK-1.0.0.zip)

The SDK consists of a sample project and our API docs for extensions.

> TODO JUSTIN: Switch over to Github for this. Decouple the API docs.

#### Start a New Project

1. Go to [WORKSPACE]/extensions/ - This folder contains all of your toolset extensions.

2. Open up the Sample Project in your IDE by creating a new, existing project. 
  * Peek at the README, which contains specific instructions for the nitty gritty project setup. 
  * Add sw.jar to the project's classpath and edit build.xml as directed.

3. After that is done, run the **dist** ANT task from the IDE. This builds a Java **JAR file** that Stencyl recognizes as an extension.

4. Launch your copy of Stencyl, and you will see the Sample Extension appear in the Extensions menu and also inside the Extensions Manager. Play around with it.
 
#### Test a Change

1. Now that the sample extension runs, flip to SampleExtension.java, the source that defines the extension itself.

```
TODO JUSTIN: INSERT FILE HERE. IT MUST BE A LOT MORE EXTENSIVE THAN THE EXISTING ONE.
```

2. Do you see how it implements a bunch of callback functions that all start with "on"?
3. Make a simple edit to it.
4. Rebuild and rerun in Stencyl. Does your change show up?

#### Modifying Extension Details

The name, description, icon location, and other basic details of the extension are saved in `{extension}.jar/META-INF/MANIFEST.MF`. These details can be edited in the ant task used to build your extension by using the nested `<manifest>` element. [Example](https://github.com/justin-espedal/polydes/blob/master/Common/build-helper.xml#L115-L131).

Attribute | Value
--- | ---
Extension-ID | Unique ID for the extension, such as com.example.extension
Extension-Main-Class | Main class extends BaseExtension or GameExtension. ex: com.example.extension.MyExtension
Extension-Version | 1.0.0 (use a valid semantic version)
Extension-Icon | Path to icon image from base folder. ex: resources/icon.png
Extension-Dependencies | Comma-seperated list of dependencies
Extension-Type | normal, game, or java_library
Extension-Name | The common name for your extension. ex: "My Extension"
Extension-Description | A short description
Extension-Author | Name of the autor
Extension-Website | http://extension.example.com/
Extension-Repository | Optional, connect to this repository for extension updates
Extension-Internal-Version | 1 (increasing this causes `updateFromVersion` to be called for GameExtensions)

## Publishing an Extension

Extensions are distributed through our [Developer Center](http://www.stencyl.com/developers/market/). Extensions must be manually approved to show up on that site. To do this, you must do two things.

1. Post your extension on the [Forums](http://community.stencyl.com/index.php/board,11.0.html) for a community review.
2. If the community response is positive, we may post up your extension without any action on your part. If not, [contact us](http://www.stencyl.com/about/contact/) and point out your forum topic.

Include the following details in the forum topic.

* A **description** of your extension
* Your extension in JAR form
* A **48x48 PNG** icon for your extension
* At least **1 screenshot** of your extension

It's preferable that you either build documentation into the forum topic or provide a link to a site that does.


## API Documentation

View the [Java-based API](http://api.stencyl.com/extensions/).

We cover the main parts of this API in the following sections.


## Callback Reference

Callbacks are functions that you implement inside your extension. These callback functions are called at specific times in Stencyl's lifecycle. Consult the [API](http://api.stencyl.com/extensions/) for the full list of callbacks.

***

**onStartup()**<br/>
Called when Stencyl is launching. Try not to do anything intense, or it will slow down launch.

***

**onActivate()**<br/>
Called when the extension is told to display or "do work"

***

**onDestroy()**<br/>
Called when Stencyl is being quit out of. Usually, you'd use this to save stuff out.

***

**onGameSave(Game game)**<br/>
Happens whenever a game is saved.

***

**onGameOpened(Game game)**<br/>
Happens whenever a game is opened.

***

**onGameClosed(Game game)**<br/>
Happens whenever a game is closed.

***

**onGameBuild(Game game)**<br/>
Happens whenever a game is compiled. Use this to modify the resulting project.

***

**DefinitionMap getDesignModeBlocks()**<br/>
Provide a set of blocks to be added to the palette.

***

**boolean hasOptions()**<br/>
Return true if this extension has options that can be configured with the `onOptions` panel.

***

**OptionsPanel onOptions()**<br/>
Returns a configuration panel for this extension that's shown when the Options button is clicked in the extensions manager. View the [API for the Options Panel](http://api.stencyl.com/extensions/stencyl/sw/ext/OptionsPanel.html) as well as the source to the Sample Extension for usage samples.

***

**onInstall()**<br/>
Happens when the extension is first installed.

***

**onUninstall()**<br/>
Happens when the extension is uninstalled. Do cleanup.

***


## GUI API Reference

We provide a set of functions to help you build a GUI or perform common tasks.

***

**showMessageDialog(String title, String text)**
<br/>
Pops up a modal dialog with the given title and text.

***

**doLongTask(final Runnable mainTask, final Runnable onFinish)**
<br/>
Perform a long task that would have hung/frozen the GUI. Pass in 2 Runnables. Runnables look like this:

```
Runnable r = new Runnable() {
    public void run() {
        //Do Stuff
    }
};
```

***

**setProgressMessage(final String msg)**
<br/>
Sets the message shown inside the progress spinner. Keep it brief!

***

**showProgressSpinner()**
<br/>
Shows the progress spinner. Use it in conjunction with doLongTask.

***

**hideProgressSpinner()**
<br/>
Hides the progress spinner.

*** 

## Data API Reference

Extensions store data in the following locations:

Name | Location | Purpose
--- | --- | ---
Prefs | {workspace}/prefs/{id}.eprefs | Dictionary of key-value pairs
Data | {workspace}/prefs/{id}.edata | Any data (as a single file)
Game Prefs | {workspace}/games/{game}/extension-data/{name}/.prefs | Game-specific preferences
Game Data | {workspace}/games/{game}/extension-data/{name} | Folder containing game-specific data
Game Extras | {workspace}/games/{game}/extras/{name} | Game-specific data needed by the engine at runtime

If you need to store data, use our data API to save out this data to disk. Do not attempt to write out to other locations using the plain Java API's. We may reject your extension if you do so.

***

**int readIntProp(String key, int defaultValue)**
<br/>
**double readDoubleProp(String key, double defaultValue)**
<br/>
**float readFloatProp(String key, float defaultValue)**
<br/>
**String readStringProp(String key, String defaultValue)**
<br/>
Read properties as different data types from `Prefs`.

***

**properties.put(String key, Object value)**
<br/>
Add a property to `Prefs`.

***

**String readData()**
<br/>
Reads `Data` into a String.

***

**byte[] readDataAsBytes()**
<br/>
Reads `Data` into a byte array.

***

**boolean saveData(String data)**
<br/>
Saves data, provided as text, to `Data`.

***

**boolean saveDataAsBytes(byte[] b)**
<br/>
Saves data, provided as a byte array, to `Data`.

*** 

## Data API Reference (Game Extensions)

In addition to the above data stores, you can store data that is game-specific if you're creating a `GameExtension`.

Name | Location | Purpose
--- | --- | ---
Game Prefs | {workspace}/games/{game}/extension-data/{name}/.prefs | Game-specific preferences
Game Data | {workspace}/games/{game}/extension-data/{name} | Folder containing game-specific data
Game Extras | {workspace}/games/{game}/extras/{name} | Game-specific data needed by the engine at runtime

***

**int readIntGameProp(String key, int defaultValue)**
<br/>
**double readDoubleGameProp(String key, double defaultValue)**
<br/>
**float readFloatGameProp(String key, float defaultValue)**
<br/>
**String readStringGameProp(String key, String defaultValue)**
<br/>
Read properties as different data types from `Game Prefs`.

***

**extensionGameProperties.put(String key, Object value)**
<br/>
Add a property to `Game Prefs`.

***

**File getDataFolder()**
<br/>
Returns the file `Game Data`.

***

**File getExtrasFolder()**
<br/>
Returns the file `Game Extras`.

***
