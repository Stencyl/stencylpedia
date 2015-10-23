## Contents

* Introduction
* Set Up an AdMob Account
* Displaying Banner Ads
* Enhanced AdMob Support
* Other Ad Networks
* FAQ
 

## Introduction

Although Android supports many ad networks, we've chosen to support AdMob, which is owned and operated by Google itself. Through 3rd-party extensions, Stencyl supports a number of other ad networks.

 
## Set Up an AdMob Account

Before you can test ads, in your game, you must set up an account with AdMob.

1. [Sign up](https://www.google.com/admob/) for an account on AdMob's site.
2. **Provide the details** they ask for (Tax Information, Personal Details, etc.)
3. **Set up a project** for your game.
4. Take note of the **Publisher ID** (sometimes called Publisher Key). You'll enter this into Stencyl.

> **Note:** Need documentation for this process? Check out [this guide](https://github.com/byrobingames/admob/wiki/2.-Configuring-your-Admob-Account).
 

## Displaying Banner Ads

Now that you've set up an account with AdMob, you can test out ads in your game.

#### Enter in the Publisher ID

1. Take note of your AdMob **Publisher ID** as mentioned above.

2. Open your game in Stencyl. Under **Settings > Mobile > Monetization**, enter in the Publisher ID.

#### Displaying the Ad

To display an ad, you must tell the ad to show. This is done using the **show/hide ad block** (under Game > Mobile). If you've read our [iOS Ads](http://www.stencyl.com/help/view/iads/) guide, you'll notice that this is the same block.

![ad-show-hide](http://static.stencyl.com/pedia2/ch11/ad-show-hide.png)

> **Note:** All the blocks that apply to iOS Ads also apply to Android Ads. Unlike iOS though, Ad Events do not work at this time.

#### Controlling Ad Position

Ad Position is set in **Settings > Mobile > Monetization** using the Ad Position dropdown. You can choose between Top or Bottom positioning.

![ad-position](http://static.stencyl.com/pedia2/ch11/ad-position.png)

 
## Enhanced AdMob Support

Through a second-party effort, Stencyl is home to a well-maintained AdMob extension that supports a much richer feature set, most notably, the ability to use full-screen interstitial ads.

[Check out the extension](http://community.stencyl.com/index.php/topic,41376.0.html).


## Other Ad Networks

Officially, Stencyl only supports AdMob on Android. Through free, user-created extensions, other ad networks besides AdMob are supported. These include...

* [Facebook Ads](http://community.stencyl.com/index.php/topic,41144.0.html)
* [Ad Colony](http://community.stencyl.com/index.php/topic,40370.0.html)
* [RevMob](http://community.stencyl.com/index.php/topic,24331.0.html)
* [Chartboost](http://community.stencyl.com/index.php/topic,25006.0.html)

Check out our [Extensions Market](http://www.stencyl.com/developers/market/) and [Extensions Forum](http://community.stencyl.com/index.php/board,70.0.html) for more details.


## FAQ

#### Why don’t the ad events fire for Android, but they do for iOS?
This is currently a limitation and is the expected behavior at this time.

#### AdMob on iOS?
The aforementioned [extension](http://community.stencyl.com/index.php/topic,41376.0.html) that provides full AdMob support for Android also supports AdMob on iOS.

#### What version of the AdMob SDK is used?
As of late 2015, we're using v7.x of the SDK.
