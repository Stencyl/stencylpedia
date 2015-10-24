> #### Extending Stencyl

> Engine ([Basics](http://www.stencyl.com/help/view/how-to-create-engine-extension/) - [iOS & Android](http://www.stencyl.com/help/view/how-to-create-native-engine-extension/) - [Flash](http://www.stencyl.com/help/view/flash-extensions/) - [Blocks](http://www.stencyl.com/help/view/adding-blocks/) - [API](http://static.stencyl.com/api/33/))

> Toolset ([Extensions](http://www.stencyl.com/help/view/creating-extensions/) - [API](http://api.stencyl.com/extensions/))


## Contents

* Introduction
* How To: Installing Extensions
* Anatomy of an Extension
* How to Create an Extension (Haxe)
* How to Create an Extension (Flash)
* Native Extensions (iOS, Android)
* Publishing Extensions
* FAQ
 

## Introduction

Stencyl supports user-written extensions for its the [engine](https://github.com/Stencyl/stencyl-engine). Using either Haxe or a combination of Haxe and native code, extensions can be written for all of our supported targets, including iOS, Android, Windows, Mac, Linux and Flash.

Even if you don't intend to write any code, extensions can define custom blocks that expose features of Haxe (and our engine) that we don't currently have in block form.
 

## Requirements

#### Overall

* Unless you are just adding custom blocks, you need to know how to code using Haxe.
* You need to know how to use the command line.

#### Platform-Specific

* For iOS extensions, you need to know Objective-C and some C++.
* For Android extensions, you need to know Java and some C++.

No additional software is required to build pure Haxe or Flash extensions. Native extensions require [Haxe 3.1](http://www.haxe.org) to be installed.
 

## How To: Installing Extensions

Before we dive into how to create an extension, it’s good to know where to get them and how to turn them on and off.

#### Where to Get Extensions

* [Stencyl.com](http://www.stencyl.com/developers/market/)
* [Stencyl Forums](http://community.stencyl.com/index.php/board,70.0.html)

#### How to Install Extensions (Recommended)
After downloading an extension, do the following.

1. Open any game.
2. Go to **Settings > Extensions**.
3. Click **Install Extension...** and pick the extension you downloaded.

The extension is now installed. You'll need to enable it in each game that needs to use it.

> **Note:** While extensions are enabled on a per-game basis, they are installed globally, meaning that you only need to install them once.

#### How to Install Extensions (Alternate)

1. Locate the Stencyl workspace folder (**Debug > View > View Workspace Folder**). We'll refer to this as **[WORKSPACE]**.
2. Unzip the Extension and copy it into **[WORKSPACE]/engine-extensions/**

The extension is now installed. You'll need to enable it in each game that needs to use it.

> **Note:** While extensions are enabled on a per-game basis, they are installed globally, meaning that you only need to install them once.
 

#### How To: Enabling / Disabling an Extension

1. Open a game.
2. Go to **Settings > Extensions**.
3. Click **Enable/Disable** for the extensions you wish to enable/disable.
4. Save your game. Close it. Reopen it. The extensions will now be enabled/disabled.

![enable-disable-extensions](http://static.stencyl.com/help/images/extensions-1.png)


## Anatomy of an Extension

> Assume that **[WORKSPACE]** refers to the path to your Stencyl workspace (find it using **Debug > View > View Workspace Folder**).

All extensions reside inside subfolders of [WORKSPACE]/engine-extensions/. For example, check out the **test-flash** extension as an example.

Each extension consists of the following parts:

Part | Description
--- | ---
**blocks.xml** | Defines custom blocks. More powerful than the in-editor custom blocks.
**icon.png** | 32x32 PNG icon
**include.nmml** | Used to specify properties for native extensions.
**info.txt** | Various metadata for the extension. All fields are required.
**Source files and DLL’s** | The meat of the extension


## How To: Creating a Haxe Extension

With a Haxe (cross-platform) extension, you are just adding new functionality to the engine (using just Haxe) or exposing Haxe / Stencyl-engine features in block form. For example, extensions have been written to add pathfinding, AI or date formatting.

#### Creating a New Extension

To create a new extension, it's easiest to copy an existing one. We've created the "test" extension for this purpose.

1. Under [WORKSPACE]/engine-extensions/, copy the “test” extension into a new folder. Give that folder a name.

2. Edit **info.txt** and fill in the details.

  ```
  name=Test Extension
  description=A test extension
  author=Jon
  website=http://www.stencyl.com
  version=1.0
  compatibility=all
  ```

3. Replace **icon.png** with your own 32 x 32 icon.

4. Modify **Test.hx** and implement whatever it is you want to implement. You can create additional source files and reference them. Note that in many cases, your public API calls will need to be **static**.

5. Edit **blocks.xml** if you wish to add custom blocks for your extension. The **spec** for this file's format can be found [here](http://www.stencyl.com/help/view/adding-blocks/).


That’s it. Once your extension is ready, open a game, enable the extension, save -> close -> reopen and finally test the game. If you’ve done everything correctly, the extension will work.

#### Testing an Extension

Once an extension is enabled for a game, you can test the game (and the extension) immediately each time you make an edit.

You do not need to close and reopen Stencyl or the game to get those edits recognized, **UNLESS** you have made changes to the block definitions (**blocks.xml**).

#### Debugging an Extension

If you encounter compile errors, use the Log Viewer to see what went wrong.


## How To: Creating a Flash Extension

Creating a Flash extension is necessary if you wish to **import a custom SWF or SWC**. For example, a common use case is to import a sponsor’s API.

Read our article on [Flash Extensions](https://github.com/Stencyl/stencylpedia/blob/master/chapter-d/flash-extensions.md) to learn how to create them.


## How To: Creating Native Extensions (iOS / Android)

Native Extensions allow Haxe code to call Objective-C, C++ or Java code, thereby allowing hooks to native functionality and APIs.

Read our article on [Native Extensions](http://www.stencyl.com/help/view/how-to-create-native-engine-extension/) to learn how to create them.


## Publishing an Extension

You've now finished up an extension and want to share it with the community. Here's what you need to do.

#### Step 1: Remove the Source (optional)

If you aren't going to open-source your extension, you should omit the **project/** subfolder from your redistributed extension.

#### Step 2: ZIP it up

Now, ZIP up the folder containing your extension.

#### Step 3: Post it to our forums

[Start a forum topic](http://community.stencyl.com/index.php/board,70.0.html) in our Extensions forum to get feedback.

#### Step 4: Tell us about it

*Once your extension receives sufficient feedback*, [contact us](http://www.stencyl.com/about/contact/) about getting it added to our official repository.


## FAQ

#### Do you have to reload your game each time you edit an extension?

No. All extensions can be edited and tested without closing and reopening your game. **The only exception is if you edit blocks.xml** in order to change the Design Mode blocks associated with the extension.
 
#### My game refuses to run.

If you hit a compile-time error, check out the Log Viewer to see what it says. Chances are good that you either goofed in the Haxe portion of the extension or possibly the custom block portion.

 
#### My blocks look wrong or my game doesn't load.

If your custom blocks don't load, don't come out right or prevent your game from loading at all, again, open up the Log Viewer before you load up your game to see if any errors. You probably goofed up in the custom block portion (blocks.xml).
 
#### Asking for Help

If you get stuck creating an extension, [ask a question on the Extensions forum](http://community.stencyl.com/index.php/board,70.0.html). Please refrain from asking here -- article comments are intended for pointing out errors in the article and suggesting improvements.

