> This is Part 1 in a three-part series.<br/><br/>
Part 1 - [Getting Started](http://www.stencyl.com/help/view/ios-getting-started)<br/>
Part 2 - [Understanding Certificates](http://www.stencyl.com/help/view/ios-certificates-guide)<br/>
Part 3 - [Setting up Certificates](http://www.stencyl.com/help/view/ios-certificates-guide-2)
 

## Contents

* System Requirements
* Step 1: Install Xcode
* Step 2: Install Xcode Additions
* Step 3: Register your System
* Step 4: Test a Game in the iOS Simulator
* Step 5: Test a Game on your iOS Device
* Next: Set up Certificates
* Troubleshooting


## System Requirements (as of 2016)

* Stencyl 3.4.0 or later
* [iOS Developer License](https://developer.apple.com/programs/ios/) from Apple
* Mac OS X Yosemite (10.10) or later
* Xcode 7 or later
* An iOS device with iOS 9 or later

> **Tip:** You can push your app to older devices by exporting an IPA and [installing the app through iTunes](http://stackoverflow.com/questions/14127576/install-ipa-with-itunes-11) on those other devices. Some have succeeded in testing on iOS devices with older versions directly from their computer.
 

## Step 1: Install Xcode

We recommend installing Xcode directly from the [Mac App Store](https://itunes.apple.com/us/app/xcode/id497799835?mt=12). This guarantees the latest version and simple, in-place updates.

Alternatively, you can grab it from [Apple's Developer Site](https://developer.apple.com/xcode/).

> **Disclaimer:** We do not officially support developer previews of Xcode. If you insist on using them, make sure that the folder in which the install resides is called "Xcode" rather than "Xcode-DP-XXX".
 

## Step 2: Install Xcode Additions

After installing Xcode, launch it. Then, do the following.

1. Open up **Preferences**. (Xcode > Preferences)
2. Flip to the **Downloads** page.
3. Under Components, install **Command Line Tools** and any **iOS Simulators** that show up.

![xcode-additions](http://static.stencyl.com/pedia2/ch11/xcode-downloads.png)

After they finish downloading, close Xcode.


## Step 3: Register Your System

If this is your very first time developing games on iOS (or if you updated Xcode), you must register your computer with Apple's system.

1. Open up **Preferences**. (Xcode > Preferences)
2. Flip to the **Accounts** page.
3. On the left should be your development account (if it isn't there, sign in and it will appear).
4. Click the refresh button at the bottom - this will register you with Apple's systems.

![](http://static.stencyl.com/pedia2/ch11/xcode-accounts.png)

*If you forgot to do this, or this has to be redone, you will find that you are unable to test on your device and get an error message along the lines of "no matching profile" (which makes no sense because you are just testing locally on your device).*

> **Still having trouble?** One user had to remove his account from the Accounts page and add it back in. 

 
## Step 4: Test in the iOS Simulator

Now, launch Stencyl and create a brand new game with a blank scene. The game's name and details don't matter -- you'll just be testing that the iOS Simulator works **before** you try out anything more complex, like your own games.

1. Launch Stencyl.
2. Click **Create a New Game**.
3. Pick **Blank Game**. Click **Next**.
4. Provide a **name**. Leave everything else as-is. Click **Create**.
5. The game now opens up to the Scenes listing. Click **Create New** (the green button).
6. Provide a name for the scene. Click **Create**.
7. **Save** the game.
8. Switch the **Platform** dropdown to **iPhone Simulator (3.5")**.
9. Click **Test Game**.

Now, the app **will build for a while**, depending on how fast your computer is. If you want to remove the suspense from this process, click Log Viewer in the top toolbar, and you'll be able to follow along. Rest assured that the process only takes long the first time and will be faster every time thereafter.

At the end of the process, the iOS simulator will automatically launch the game.

![ios-simulator](http://static.stencyl.com/pedia2/ch11/ios-simulator.png)


## Step 5: Test on an iOS Device

Now, let's do the same thing except on an iOS Device. Using the same game, do the following.

1. **Plug in your iOS device** to your computer.
2. Switch the Platform dropdown's value to **iOS Device**.
3. Click **Test Game**.

Again, it will go through a lengthy build process like explained above.

At the end of the process, the app will install to your device, and Stencyl will tell you that it's ready. You must launch it manually by tapping it - it won't auto-launch from Stencyl.

#### Gotcha: "No Matching Profile"

If you are unable to test on your device and see an error along the lines of "No Matching Profile", you need to register your system with Apple.

See **Step 3: Register Your System** earlier in this article for details.

#### Gotcha: Version Mismatch

Apple generally forces you to use the latest version of Xcode and iOS on your Mac. This may be newer than what you have on your device. Unfortunately, this can lead to a mismatch in versions.

Generally speaking, the "major" versions of iOS have to match between your Mac and your device. For example, if your Mac has iOS 9, your device must also have iOS 9 (minor version differences like iOS 9.1 vs. iOS 9.0 are usually OK). It just can't have iOS 8.


## Next: Set up Certificates

Read our comprehensive guide on [how to set up certificates](http://www.stencyl.com/help/view/ios-certificates-guide), so that you can publish your game to your friend's devices and the App Store.

 
## Aside: Why does it take so long to build the app the first time? 

Stencyl is based around Haxe. In order to build native iOS apps, Haxe is translated to C++ which in turn is compiled to machine code. Although the Stencyl engine is compact, the Haxe code it depends on is large and has to be re-compiled for each new game.

Mercifully, this is only the case the first time you run a game on a given platform (where iOS Simulator and iOS Device are considered separate platforms). Second runs and onwards are much faster. Flash games are not affected by this quirk.

 
## Troubleshooting

We've devoted an entire article to [troubleshooting common issues](http://www.stencyl.com/help/view/xcode-ios-troubleshoot/) with iOS, Xcode and Certificates.
