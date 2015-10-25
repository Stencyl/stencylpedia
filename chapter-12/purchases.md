## Contents

* Introduction
* Requirements
* Walkthrough
  * Setup: Google Play
  * Setup: Stencyl
  * Making a Purchase
  * Purchase Events
  * Consumables
  * Restoring Purchases
* Troubleshooting
* Further Reading
 

## Introduction

[In-App Purchases](https://developer.android.com/google/play/billing/billing_overview.html) (IAP) let you sell goods and services from within a game. This gives developers more opportunities to monetize the free app by providing downloadable, supplementary content (new levels or game modes), an unlock for the full game and much more.

#### Supported Features

Feature | Supported?
--- | ---
Regular Purchases | Yes
Consumables | Yes
Restoring Purchases | Yes
Susbcriptions | No
 

## Requirements

* A Google Play developer account.
* A Google Payments merchant account. You can create one at the same time that you create a dev account.
* A non-rooted Android device running 4.0 or later.
* The **most current** version of Google Play must be installed.
 

## Setting up on Google Play

#### Step 1: Set up your Keystore (if necessary)

Before doing anything, you must **set up your keystore** within Stencyl. Consult our [Publishing to Google Play](http://www.stencyl.com/help/view/google-play/) guide for details on this process.

> **Note:** If you already have a Keystore (made outside of Stencyl), you must still tell Stencyl about it. Read the [guide](http://www.stencyl.com/help/view/google-play/) for details.

#### Step 2: Set the game up on Google Play

First, you must set up your game on the [Google Play Developer Console](https://play.google.com/apps/publish/), the Google equivalent to iTunes Connect. If you haven't registered for the Google Play Developer Console before, you will be prompted to do so.

#### Step 3: Set up Products on Google Play

Now that you've created an entry for your game, you can begin adding products (purchases) to your game.

Consult Google's guide on [Administering In-App Billing](https://developer.android.com/google/play/billing/billing_admin.html) for a walkthrough of this process.
 
#### Step 4: Create and Assign Test Accounts

Test accounts let real testers with real accounts make test purchases of your app without being charged. In order to do this, you can designate (via e-mail address), people with Gmail accounts who have this privilege.

In summary, the process goes as follows:

* Add and publish the [products](https://developer.android.com/google/play/billing/billing_admin.html#billing-list-setup) you wish to test to the developer console.
* Create [test accounts](https://developer.android.com/google/play/billing/billing_admin.html#billing-testing-setup) by adding Gmail accounts to Settings > Account details in the developer console.
* Within 15 minutes, those users can begin making test purchases in your app.

Consult Google's guide on [Testing In-App Purchases](https://developer.android.com/google/play/billing/billing_testing.html#testing-purchases) for a complete walkthrough.

#### Step 5: Getting the Android Public Key

In order to test out purchases, you'll need to get your app's public key (now referred to as License Key on Google's end).

* Inside the Developer Console, open up the entry for your game. 

* Select **Services & APIs**.

* Scroll down to Your **License Key for this Application**. Make note of this for the next section.

![billing-app-key](http://static.stencyl.com/pedia2/ch12/billing_app_key.png)


## Setting up within Stencyl

Now that you've set everything up on Google Play, you'll need to do a few more things in Stencyl before you can begin.

1) Ensure that the Enable Purchases checkbox is checked. It's inside Settings > Mobile > Monetization.

2) Enter in your Android Public Key on that same page (Settings > Mobile > Monetization). This is the key you obtained in the previous section.

 

Making a Purchase

Step 1: Declare All Purchases
Use the request info for product block to declare a purchase. You can find it under Game > Mobile towards the bottom. The ID you use is the Product ID you entered into the Google Play dashboard.

request-product-info

Do this for each purchase in your game. You only have to do this ONCE, not every time you wish to make a purchase.

(In order to "know" when your request succeeded, use the when a product info request succeeds event under Add Event > Mobile > Purchases.)

product-info-event

 

Step 2: Make a Purchase
You can find the buy product block under Game > Mobile towards the bottom. The ID you use is the Product ID you entered into the Google Play dashboard.

buy-product-block

Tip: If you'd like to test out purchases without setting up an entry on Google Play, you can use the following product IDs that Google has designated for testing.

android.test.purchased
android.test.canceled
 

Other Operations

Purchase Events
Just like on iOS, purchase events are available, so your app is informed when purchases succeed, fail and so forth. The following events apply to Android.

Player can purchase goods
A purchase succeeds
A purchase fails
A purchase is canceled
A product info request succeeds
 

Consumables
Stencyl supports consumable purchases in addition to non-consumables. No extra work is required on your part to support this - Stencyl will automatically keep a count for you.

For example, if you buy a consumable, we'll increment the count for that product by 1. If you use a consumable, that product's count will be decreased by 1.

Note: Although Stencyl automatically keeps count, we recommend maintaining a copy of transactions on a personal server in order to combat cheaters or using a service to track this information for you.
 

Restoring Purchases
Restoring Purchases allow a user on a separate device who has bought non-consumable goods from your game to transfer those goods to that extra device.

Use the restore purchases block under Game > Mobile to initiate this process (connect it to a button press, for example).

When this happens, you will receive a bunch of purchase restoration events (which you can receive via Add Event > Mobile > Purchases), each corresponding to a purchase. It's your task to react to these events in an appropriate manner.

restore-purchase-event

 




## Troubleshooting

#### I uploaded my APK, but the developer console won't let me add IAPs to my game.
Before you export and upload your game, ensure that the **Enable Purchases** checkbox is checked for your game, otherwise the Google developer console will not let you add IAPs. Enable Purchases is located inside **Settings > Mobile > Monetization**.


## Further Reading

* [Uploading an APK to Google Play](https://support.google.com/googleplay/android-developer/answer/113469?hl=en)
* [Testing In-App Billing](https://developer.android.com/google/play/billing/billing_testing.html)
* [Setting up Test Accounts](http://developer.android.com/google/play/billing/billing_admin.html#billing-testing-setup)
