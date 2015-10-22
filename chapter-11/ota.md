## Deploying Apps Over the Air (OTA)

> **Note:** This material is provided as-is for advanced users who know how to work with a web server. We do not recommend this method for casual developers.

## Introduction

Most developers use services like TestFlight in order to put their app out for beta testing. We recommend the same. If you'd like to roll your own solution for personal use (such as installing to devices without having to plug them in), it's not hard to do this.

## Concepts
OTA (over the air) deployment lets you install an Ad Hoc app on an device by visiting a link from the device. The app installs wirelessly. It's convenient for everybody involved, since it's a matter of hosting the IPA on a server (local or remote) and creating a simple web page.

## Determining Your Computer's Name
If you're hosting the server locally, you'll need to determine your computer's name. This can be found by going to (Apple Menu) > About this Mac > More Info... and looking at the piece of text at the top left. Alternatively, you can run "ipconfig" in Terminal to get the IP address for your computer.

## Walkthrough

1) Install a web server, like MAMP or WAMP if you're hosting locally. If you're hosting remotely, any web server will do.

> **Note:** For the remaining steps, we are assuming that you place the files under the server's www folder.

2) Create a **game.plist** file under the folder. This tells the iOS device what the game is about.

> **Instructions**

> 1) Download this [template](https://dl.dropbox.com/u/2769678/game.plist).<br/>
> 2) Replace **YOUR-BUNDLE-ID** and **GAME-NAME** with the appropriate values. (3 spots total)<br/>
> 3) Replace **localhost** with the appropriate value.

3) Create an HTML webpage under the folder. The link to the game will take on the following form.

> **Instructions:** Download this [template](https://dl.dropbox.com/u/2769678/game.html) and replace **localhost** with an appropriate value.

4) Create a **icon.png** image. Stick under the folder.

5) Finally, anytime you export your game from Stencyl, export it under the folder as **game.ipa**.

6) Now, **visit the webpage from your iOS device**. Click on the link, and it'll install magically.

 
## Troubleshooting

If something goes wrong, frequently, the app will appear to download when then error out and say that it can't download. If you're sure that everything's there, it could actually mean a certificate-related error. For example...

* A mismatch between App ID (entered into Stencyl) and the provision profile's App ID.
* You used the App Store profile rather than the Ad Hoc one.
* The profile has expired.

More potential causes exist - check our [Troubleshooting guide](http://www.stencyl.com/help/view/xcode-ios-troubleshoot/) for more ideas.
