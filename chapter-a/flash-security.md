Some games require access to the web. When?

* Linking to a website
* Pulling down high score data
* Pulling down a save game from online

Whatever the reason, to test whether your Flash game is connecting to other sites properly, you must let the Flash Player access the Internet.


## Why do we need to allow the Flash Player to access the web?

Adobe added security settings that prevent Flash Player from accessing the web without its user's permission because of possible security threats. These security settings will prevent any .SWF object on the local machine from accessing the web unless each object is given permission to do so. Here is a quote from Adobe's website:

> "Some websites may access information from other sites using an older system of security. This is usually harmless, but it is possible that some sites could obtain unauthorized information using the older system."

For more information about Security Settings and why it exists, you can visit Adobe's website.


## How do I let games created with Stencyl access the web when testing locally?

To allow games made with Stencyl to access the web when testing them locally, you need to set the permissions for your game's SWF in the [Global Security Settings Manager](http://www.macromedia.com/support/documentation/en/flashplayer/help/settings_manager04.html) on Adobe's website. Below is a screenshot of what the panel looks like as well as what the location for a Stencyl game would be.

![Flash Player Security Manager](https://static.stencyl.com/help/images/FlashPlayerSecurity.png)

Unless you maintain multiple copies of Stencyl for testing purposes, you will have just one location to specify.

The location of your SWF differs on each computer depending on the OS and where your workspace is installed. Below are some example locations that the directory could be installed in:

####Windows
[WORKSPACE]\games-generated\YOURGAME\Export\flash\bin\SOMETHING.swf

####Mac
[WORKSPACE]/games-generated/YOURGAME/Export/flash/bin/SOMETHING.swf

####Linux
[WORKSPACE]/games-generated/YOURGAME/Export/flash/bin/SOMETHING.swf

> **Tip:** Your WORKSPACE directory can be discovered by going to **Debug > View > View Workspace** from the top menu.
 

## A Quick Way to Set Permissions

To set the permission for your SWF to access the Internet, first open Stencyl. Then, you want to open a game you know will want to access the web. Test the game and have it attempt to access the web. Now, you will see a security alert display, similar to the image below, informing you that the game is attempting to access the web.

![Flash Player Security Alert](https://static.stencyl.com/help/images/FlashPlayerSecurityAlert.png)

To set the permissions, click on "settings." It will bring you to the Global Security Setting panel as noted above. When you are on this page, you want to click on "Edit Locations," which will display a dropdown menu. Next, click "Add Location." It will display a dialog box as shown below.

![Flash Player Security Add Location](https://static.stencyl.com/help/images/FlashPlayerSecurityAddLocation.png)

When you see this box, click on "Browse for files..." It should open a new dialog that contains the directory where the SWF is stored. Select the SWF and click "Open." This will add the necessary file to the permissions list. Once this is completed, any game created in Stencyl that is tested locally or in the browser will be able to access the web.
