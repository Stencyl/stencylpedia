## Contents

* Introduction
* Windows
* Mac
* Linux
* FAQ


## Introduction

Stencyl supports the creation of native, standalone apps for Windows, Mac and Linux. These apps feature hardware accelerated graphics and consequently, better performance than their web or mobile counterparts.

> **Note:** Publishing desktop games is a paid feature. [Purchase a license](https://www.stencyl.com/pricing/) to access this functionality.


## Windows

#### Requirements
* Windows 7 or better
* We recommend Visual Studio 2013 for best results. The free editions are fine.

> You can either install Visual Studio on your own, or if you attempt to run a Windows app from Stencyl, we'll download the Visual Studio installer for you and then ask you to run it. We'll assume the latter.
 
#### Setup
1. After opening up a game in Stencyl, select **Run > Windows** from the main menu. 

2. Stencyl will download the Visual Studio installer to your system. After that finishes, **run the installer**.

3. Once you install Visual Studio, you’ll need to **reboot your computer** for Stencyl to recognize it.

#### Testing
To test your game, select **Run > Windows** from the main menu.

> This step may take a while. You may find it useful to turn on the **Log Viewer (View > Log Viewer)** prior to running to see what's going on and catch any unforeseen errors.
 
#### Publishing
To publish your game, select **Publish > Desktop > Windows** from the main menu. This will export your game as a ZIP containing an EXE and the resources associated with the game.

> **Note:** We don't support exporting the game to a single, bundled EXE. We tried to wrap them in the past using free solutions, but they were (wrongly) flagged by AV software, so we discontinued that experiment. If you must wrap an EXE, you can use a thid party utility such as Molebox to do this.


## Mac

#### Requirements
* A Mac with Yosemite (OS X 10.10) or better
* The latest release of Xcode
* Registration in the [Mac Developer Program](https://developer.apple.com/programs/mac/) (if publishing to the Mac App Store)
 
#### Setup

1. If you don't have Xcode, [install it from the Mac App Store](https://developer.apple.com/xcode/).

2. Launch Xcode, go to its Preferences, flip to the Downloads Tab and **install Command Line Tools**.

  ![xcode-command-line-tools](https://static.stencyl.com/pedia2/ch11/xcode-downloads.png)

3. If you are publishing to the Mac App Store, you must [set up your App](https://www.stencyl.com/help/view/mac-app-store/) on iTunes Connect.

#### Testing
To test your game, select **Run > Mac** from the main menu.

> This step may take a while. You may find it useful to turn on the **Log Viewer (View > Log Viewer)** prior to running to see what's going on and catch any unforeseen errors.
 
#### Publishing
When publishing for Mac, you have two options. You can publish for the **Mac App Store (.PKG)** or export the game as an **App Bundle (.APP)** for providing on a personal website.

* If you are publishing to the Mac App Store, [view our dedicated article](https://www.stencyl.com/help/view/mac-app-store/) on that process.
* If you are publishing an App Bundle (.APP), you can do so by selecting **Publish > Desktop > Mac** from the main menu.

 
## Linux

> **Note:** We're not Linux experts, so if you run into issues or have edits to propose, please submit a pull request on Github. For additional tips, visit our [Installing on Linux](https://www.stencyl.com/help/view/install-stencyl-linux/) article.
 
#### Requirements and Setup
* Ubuntu 11.04 or better
* All standard build tools such as gcc/g++ should be installed.

Run `sudo apt-get install ia32-libs-multiarch gcc-multilib g++-multilib` to fetch those build tools if you are unsure.

On Ubuntu 12.04 or better? Run `sudo apt-get install gcc-multilib g++-multilib` instead.
 
#### Testing
To test your game, select **Run > Linux** from the main menu.

> This step may take a while. You may find it useful to turn on the **Log Viewer (View > Log Viewer)** prior to running to see what's going on and catch any unforeseen errors.
 
#### Publishing
To publish your game, select **Publish > Desktop > Linux** from the main menu.


## FAQ

#### Can I publish a Mac app from a Windows computer?
No. You'll need to use a friend's Mac or figure out other ways to do this. The same goes for any "cross" platform combination. You can only publish to the platform of your host computer.

#### Can I publish to the Mac App Store?
Yes. We have an [article](https://www.stencyl.com/help/view/mac-app-store/) on that. 

#### How about the Windows Store?
You can, but we don't directly export to a Windows Store ready format. You'll need to wrap the app up on your own.

#### I just installed Visual Studio, but Stencyl claims I didn't.
Reboot after installing Visual Studio. 
