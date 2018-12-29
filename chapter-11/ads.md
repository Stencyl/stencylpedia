## Contents

* Introduction
* Set Up an AdMob Account
* Initialize Admob in Stencyl
* Displaying Banner Ads
* Displaying Interstitial ads
* Ads Events
* Other Ad Networks
* FAQ
 

## Introduction

Although iOS supports many ad networks, we've chosen to support AdMob.
Through 3rd-party extensions, Stencyl supports a number of other ad networks.

This guide is for Stencyl build 10200 and higher

## Set Up an AdMob Account

Before you can test ads, in your game, you must set up an account with AdMob.

1. [Sign up](https://www.google.com/admob/) for an account on AdMob's site.
2. **Provide the details** they ask for (Tax Information, Personal Details, etc.)
3. **Monetise a new app** for your game. ![admob_Monetise](http://byrobin.nl/stencyl/admob/admob_Monetise.png)
3. Add your app manually or, if it's already in the store, search for it  and select your platform.
4. **Add App** and take note of the **App ID**. You'll enter this into the Initialize block in Stencyl.
5. Select ad format and name ad unit. Stencyl is only supporting Banner and Interstitial ads at the moment.
6. Save it and take note of the **Ad unit ID** (Also called Publisher Key on Stencyl Monetization page). You'll enter this into the Monetization page in Stencyl.

## Initialize Admob in Stencyl

Now that you've set up an account with AdMob, you can test out ads in your game.

#### Enable Admob

1. Open your game in Stencyl. Under **Settings > Mobile > Monetization**.
2. Enable Admob ads

#### Enable Test Ads.

Before you publish your game to the store, you want to know if the ads are working.
Google does not allow you to click on live ads when testing your game so you have to set Admob in Testmode.

1. Open your game in Stencyl. Under **Settings > Mobile > Monetization**.
2. Enable Test ads

> **Note:** Don't forget to disable Test Ads when you are ready to Publish your game, or else the test ads will show up.

#### Enter in the AppId.

1. Take note of your AdMob **AppId** as mentioned above in step 4.
2. Open your game in Stencyl. In palette under **Game > Mobile** you can find the AdMob blocks.</br>
![admob_initialize](http://byrobin.nl/stencyl/admob/admob_initialize.png)</br>
3. Fill in the **AppId** in the block. If you are using Banner Ads you can set here if you want it to show at the top or at the bottom of your game.

> **Note:** Use this block only once a session as early as possible (such as a loading scene)

## Displaying Banner Ads

#### Enter in the Ad unit ID

1. Take note of your AdMob Banner **Ad unit ID** as mentioned above in step 6 (Also called Publisher key on Stencyl Monetization page).

2. Open your game in Stencyl. Under **Settings > Mobile > Monetization**.

3. Enter the Ad unit ID in **AdMob Banner iOS key**

#### Displaying the Banner Ad

To display an ad, you must tell the ad to show. This is done using the **show/hide ad block** (under Game > Mobile). If you've read our [Android Ads](http://www.stencyl.com/help/view/android-ads//) guide, you'll notice that this is the same block.

![ad-show-hide](http://byrobin.nl/stencyl/admob/admob_banner_showhide.png)

> **Note:** All the blocks that apply to iOS Ads also apply to Android Ads.

#### Controlling Ad Position

Ad Position is set in **the Initialize block** using the dropdown. You can choose between Top or Bottom positioning.
If you want to change the position on runtime use this block:

![ad-position](http://byrobin.nl/stencyl/admob/admob_banner_position.png)

## Displaying Interstitial (Fullscreen) Ads

#### Enter in the Ad unit ID

1. Take note of your AdMob Interstitial **Ad unit ID** as mentioned above in step 6 (Also called Publisher key on Stencyl Monetization page).

2. Open your game in Stencyl. Under **Settings > Mobile > Monetization**.

3. Enter the Ad unit ID in **AdMob Interstitial iOS key**

#### Displaying Interstitial Ads

Before you can show the Interstitial ad, you have to load them first. (Its take a couple of seconds to load an ad).
You have to load the ad every after it's showed up.

For example:

1. Load the ad when player click the start play button</br>
![ad-interstitial-load](http://byrobin.nl/stencyl/admob/admob_interstitial_load.png)

2. Show the ad when it is appropriate to do so, such as at the end of a level.</br>
![ad-interstitial-show](http://byrobin.nl/stencyl/admob/admob_interstitial_show.png)

## Ads Events

Sometimes, it's useful to know when an ad has been clicked on or dismissed, so that you can provide a smooth transition between viewing the ad and resuming the game. Stencyl provides the following events for ads.

These events can be found under the **Mobile > Ads** item under the **Add Event** dropdown.

### Banner Ads Events

Event | Description
--- | ---
A banner ad is showing| The banner ad is showing on screen
A banner ad is closed | User closes the banner ad
The banner ad area loads | Called each time a banner ad loads
The banner ad area fails to load | Called when no banner ads can be loaded
A banner ad is clicked | User clicks on the banner ad


> **Tip:** We recommend [pausing](http://www.stencyl.com/help/view/pausing/) the game when an ad is clicked on and resuming it when the ad is dismissed. If you don't do this, the game will continue to run while the ad is overlayed over everything else.
![ad-events](http://byrobin.nl/stencyl/admob/admob_banner_event.png)

### Interstitial Ads Events

Event | Description
--- | ---
A fullscreen ad is showing| The Interstitial ad is showing on screen
A fullscreen ad is closed | User closes the Interstitial ad
The fullscreen ad area loads | Called each time a Interstitial ad loads
The fullscreen ad area fails to load | Called when no Interstitial ads can be loaded
A fullscreen ad is clicked | User clicks on the Interstitial ad

> **Tip:** We recommend [pausing](http://www.stencyl.com/help/view/pausing/) the game when an ad is clicked on and resuming it when the ad is dismissed. If you don't do this, the game will continue to run while the ad is overlayed over everything else.

![ad-events-interstitial-clicked](http://byrobin.nl/stencyl/admob/admob_interstitial_event_clicked.png)

![ad-events-interstitial-closed](http://byrobin.nl/stencyl/admob/admob_interstitial_event_closed.png)

### GDPR Support

The EU's General Data Protection Regulation (GDPR) requires that you gather consent from players in the EU as well as the EEA before showing personalized ads. To assist in this, you can show a Google rendered consent form that will only appear to players who are in the EEA or their location is unknown. Before showing the form, you need to set the privacy policy URL using this block:

![set-privacy-policy-url](images/set-privacy-policy-url.png)

This block can be used right after the init block. After setting the privacy policy URL, you can then show the consent form. The consent status as well as the location of the player is detected after using the init block, so you don't need to check for that before showing the form.

![show-consent-form](images/show-consent-form.png)

This block has a dropdown option that decides whether to check the existing consent status before showing the form. If "Check existing consent" is used, then the form will not show if the player has previously consented to either personalized or non-personalized ads. This option is best used at the start of the game so that players who already chose an option are not bothered by the form again. The second option "Always show" is needed to allow the player to change their consent, which is something that is required by GDPR. After the player selects an option on the form, the ads are updated to either personalized or non-personalized depending on the option chosen.

## Other Ad Networks

Officially, Stencyl only supports AdMob on Android. Through free, user-created extensions, other ad networks besides AdMob are supported. These include...

* [Facebook Ads](http://community.stencyl.com/index.php/topic,41144.0.html)
* [Ad Colony](http://community.stencyl.com/index.php/topic,40370.0.html)
* [RevMob](http://community.stencyl.com/index.php/topic,24331.0.html)
* [Chartboost](http://community.stencyl.com/index.php/topic,25006.0.html)

Check out our [Extensions Market](http://www.stencyl.com/developers/market/) and [Extensions Forum](http://community.stencyl.com/index.php/board,70.0.html) for more details.

## FAQ

#### What version of the AdMob SDK is used?
As of December 2018, we're using v7.36.0 of the AdMob iOS SDK.

## Tips
 
#### Avoid covering up the screen
When banner ads are displayed, they will cover up a small part of the screen. You should avoid displaying crucial game elements under a banner ad, such as HUD elements. 

The **height of mobile ad** block (under Game > Mobile) provides the height, so you can lay your game out accordingly.

