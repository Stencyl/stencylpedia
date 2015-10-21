## Contents

* Introduction
* Showing / Hiding Ads
* Ad Events
* Controlling the Position
* Tips
* Limitations
* AdMob
* Alternative Networks
 

## Introduction

Games on the App Store can make money by displaying ads. For the iOS platform, your best bet for making money is to display iAds, Apple’s own ad network. It may not pay the absolute most out of all networks, but it is easy to integrate and support. 
 

## Showing / Hiding Ads

To display an ad, **you must tell the ad to show**. We don't automatically show ads under any circumstance. This is done using the **show/hide mobile ad block** under **Game > Mobile**.

![ad-show-hide](http://static.stencyl.com/pedia2/ch11/ad-show-hide.png)

> **Note:** An ad may not immediately show for a variety of reasons. See the Tips section below to learn why.
 

## Ad Events

Sometimes, it's useful to know when an ad has been clicked on or dismissed, so that you can provide a smooth transition between viewing the ad and resuming the game. Stencyl provides the following events for ads.

* An ad is viewed (clicked on)
* An ad is closed
* The ad area loads
* The ad area fails to load

These events can be found under the **Mobile > Ads** item under the **Add Event** dropdown.

![ad-events](http://static.stencyl.com/pedia2/ch11/ad-events.png)

> **Tip:** We recommend [pausing](http://www.stencyl.com/help/view/pausing/) the game when an ad is clicked on and resuming it when the ad is dismissed. If you don't do this, the game will continue to run while the ad is overlayed over everything else.
 

## Controlling Ad Position

Ad Position is set in **Game Settings > Mobile > Monetization** using the **Ad Position dropdown**. You can choose to place the ad at the Top or the Bottom of the screen.

![stencyl-iad-position](http://static.stencyl.com/pedia2/ch11/ad-position.png)

 
## Tips

#### Why doesn't the ad show?
During testing, ads can randomly fail to show. This is because **Apple randomly causes them to fail**, so that you can test how your app performs in these scenarios.

Even in cases where an ad displays in production, it may take 30 seconds, a minute or even longer for the ad to display **if the ad inventory is empty at the time**.

 
#### Avoid covering up the screen
When ads are displayed, they will cover up a small part of the screen. You should avoid displaying crucial game elements under an ad, such as HUD elements. 

The **height of mobile ad** block (under Game > Mobile) provides the height, so you can lay your game out accordingly.

![stencyl-iad-dont-cover-up](http://static.stencyl.com/help/images/iads/image03.png)


## Limitations

Stencyl does not support full-screen (interstitial) ads for the iAd network at this time. If you need this functionality, consider using AdMob or an alternative network.


## AdMob

AdMob support for iOS is supported through a well-maintained 2nd party extension. [Learn more](http://community.stencyl.com/index.php/topic,41376.0.html).


## Alternate Networks

Through free, user-created extensions, other ad networks besides AdMob are supported. These include...

* [Ad Colony](http://community.stencyl.com/index.php/topic,40370.0.html)
* [Facebook Ads](http://community.stencyl.com/index.php/topic,41144.0.html)
* [Chartboost](http://community.stencyl.com/index.php/topic,25006.0.html)

Check out our [Extensions Market](http://www.stencyl.com/developers/market/) and [Extensions Forum](http://community.stencyl.com/index.php/board,70.0.html) for more details.
