## Contents

* Export to a SWF
* Publish to our Arcade
* How to Remove the Splash Screen
* Site Locking
* Reducing File Size
* Troubleshooting
 

## Export to a SWF

A SWF (Shockwave Flash) file is the format for all exported Flash games. This is the file that you upload to portals such as [Kongregate](http://www.kongregate.com) and [Newgrounds](http://www.newgrounds.com).

1. To export a SWF, go to **Publish > Web > Flash** in the main menu.
2. You'll be asked where to save the game out to. Pick a directory where you have write access.

After a brief wait, your SWF will export. That's it!

> **Tip:** If the game fails to export, consult the troubleshooting section below.
 

## Publish to the Stencyl Arcade

In addition to publishing a SWF, you can publish your game directly to our [Arcade](https://www.stencyl.com/game/) to share it with the community and receive useful feedback.

To publish to our Arcade, go to **Publish > Stencyl > Arcade** in the main menu.

This will generate the SWF and automatically upload it to our site. If you've already published this game in the past, it will update the existing entry.

> **Note:** There is an 8 MB limit on games published to our Arcade. If your game is larger, publish to a 3rd party sites like itch.io and Game Jolt.
 

## How to Remove the Splash Screen

Every Flash game published with Stencyl displays a small badge in the loading screen.

If you'd like to remove this branding (because a sponsor requires it, for example), [purchase a license](https://www.stencyl.com/pricing/), which includes many other benefits besides splash screen removal.

 
## Site Locking

If your game is popular, people will snatch it and upload it to other sites, causing you to give others ad revenue off your game without your permission.

This can be deterred through **site locking**, a feature that prevents the game from starting if it's hosted on a different domain from any on a "whitelist" that you create.

1. In the Settings dialog with your game open, click on **Loader** button on the left sidebar.

   ![Settings Loader Button](https://static.stencyl.com/help/images/Settings-PreloaderPic-SiteLock.png)

2. Fill in the sites **that you want the game to work on**. If you have multiple, put a comma between them. Do not insert any white space.

   ```
   kongregate.com,newgrounds.com
   ```

   ![site lock](https://static.stencyl.com/pedia2/ch7/flash/image0.png)

 
## Reducing File Size

Games delivered over the web, even in today's age of widespread broadband internet, are better smaller rather than larger. If your game exceeds 8 MB, you may want to consider cutting it down. The longer the wait, the less likely the game will be played. Here are a couple tips.

1. **Reduce the quality of your sounds/music**. Switch to Mono (from Stereo) and export at a lesser bitrate. This generates the biggest savings.

2. **Ensure that you aren't exporting hi-res graphics**. Check that your game's **Max Scale for web is 1x** (this is under Settings > Web > Maximum Scale).


## Troubleshooting

On occasion, your game will fail to export with no obvious error.

#### Enable the Log Viewer
The first rule when encountering this is to **enable the Log Viewer (View > Log Viewer)**. Retry the export, and you can see if any errors pop up towards the bottom.

#### In many cases, it's due to an incompatible sound.
If you remove sounds from your game until it successfully exports, you can identify which sound is at fault. Once you do, a safe solution is simply to re-export it from a program such as Audacity while taking heed of the [basic requirements](https://www.stencyl.com/help/viewArticle/115/) of sounds that we talked about in the Sounds article.

* 44.1 KHz
* 16-bit
* Constant bitrate (versus VBR)
* No metadata
 
#### No Write Permissions
A second, less common cause is that the game is able to export to a SWF (you get a file chooser dialog) but fails to write the SWF out to the location you picked. This can be caused by insufficient file permissions. Choose a directory to which you can save files out to.

#### Still stuck? Ask for help on the forums.
Describe the problem and attach your logs on the [forums](https://community.stencyl.com/index.php/board,3.0.html).
