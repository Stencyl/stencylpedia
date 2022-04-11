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

[In-App Purchases](https://developer.android.com/google/play/billing) (IAP) let you sell goods and services from within a game. This gives developers more opportunities to monetize the free app by providing downloadable, supplementary content (new levels or game modes), an unlock for the full game and much more.

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

> **Tip:** Just want to skip to testing? It is possible to test purchases without setting **anything** up using [static product ID's](https://developer.android.com/google/play/billing/billing_testing.html#billing-testing-static). This is good for testing basic connectivity to Google Play.

#### Step 1: Set up your Keystore (if necessary)

Before doing anything, you must **set up your keystore** within Stencyl. Consult our [Publishing to Google Play](https://www.stencyl.com/help/view/google-play/) guide for details on this process.

> **Note:** If you already have a Keystore (made outside of Stencyl), you must still tell Stencyl about it. Read the [guide](https://www.stencyl.com/help/view/google-play/) for details.

#### Step 2: Set the game up on Google Play

First, you must set up your game on the [Google Play Developer Console](https://play.google.com/console/about/), the Google equivalent to iTunes Connect. If you haven't registered for the Google Play Developer Console before, you will be prompted to do so.

#### Step 3: Set up Products on Google Play

Now that you've created an entry for your game, you can begin adding products (purchases) to your game.

Consult Google's guide on [Administering In-App Billing](https://support.google.com/googleplay/android-developer/answer/1153481) for a walkthrough of this process.
 
#### Step 4: Create and Assign Test Accounts

Test accounts let real testers with real accounts make test purchases of your app without being charged. In order to do this, you can designate (via e-mail address), people with Gmail accounts who have this privilege.

In summary, the process goes as follows:

* Add and publish the [products](https://support.google.com/googleplay/android-developer/answer/1153481) you wish to test to the developer console.
* Create [test accounts](https://support.google.com/googleplay/android-developer/answer/6062777) by adding Gmail accounts to Settings > Account details in the developer console.
* Within 15 minutes, those users can begin making test purchases in your app.

Consult Google's guide on [Testing In-App Purchases](https://developer.android.com/google/play/billing/test) for a complete walkthrough.

#### Step 5: Publish the Game to Alpha/Beta Testing Channels

In order to test purchases, the game must be published. 

Google provides various channels (Alpha/Beta) for publishing the game, so that it does not show up in public listings and can only be installed by testers you designate. Consult Google's [guide](https://support.google.com/googleplay/android-developer/answer/3131213) for details.

#### Step 6: Get the Android Public Key

In order to test out purchases, you'll need to get your app's public key (now referred to as License Key on Google's end).

* Inside the Developer Console, open up the entry for your game. 

* Select **Services & APIs**.

* Scroll down to Your **License Key for this Application**. Make note of this for the next section.

![billing-app-key](https://static.stencyl.com/pedia2/ch12/billing_app_key.png)


## Setting up within Stencyl

Now that you've set everything up on Google Play, you'll need to do a few more things in Stencyl before you can begin.

* Ensure that the **Enable Purchases** checkbox is checked. It's inside **Settings > Mobile > Monetization**.

* Enter in your Android Public Key on that same page (Settings > Mobile > Monetization). This is the "**License Key for this Application**" that you obtained in the previous section.

![billing-app-key](https://static.stencyl.com/pedia2/ch12/enable-purchases.png)



## Making a Purchase

Finally, we're ready to start testing purchases.

#### Check if In-App Billing has started

Before doing anything with in-app billing, we need to check if the service has started. Use the following Purchase event (under Add Event > Mobile > Purchases) to accomplish this. Store the value inside a boolean Game Attribute, so you can refer to it in the future.

![](https://static.stencyl.com/pedia2/ch12/can-make-purchases.png)

> **Warning:** You can't do the following on Android at this time due to a bug. This was fixed on Oct 25, 2015, but we're keeping this up for now.<br/><br/>![](https://static.stencyl.com/pedia2/ch12/can-make-purchases-wrong.png)


#### Make a Purchase

With the switch over to Billing v3, it's no longer necessary to request purchases on Android. Just buy the product directly by passing in its product ID using the **buy** block, located under Game > Mobile.

The ID you use is the Product ID you entered into the Google Play dashboard.

![buy-product](https://static.stencyl.com/pedia2/ch12/buy.png)

> Recall from above that we want to check if in-app billing has started, so we used an event and stored that in a game attribute. That's where **canMakePurchases** comes from.


#### Testing for Success / Failure

Purchases are asynchronous (non-blocking), so you'll need to use an event to get notified of the purchase's success or failure.

![bought-product](https://static.stencyl.com/pedia2/ch12/buy2.png)

The following approach also works.

![bought-product-alt](https://static.stencyl.com/pedia2/ch12/buy2-alt.png)


#### Easy Test Purchases (Static Responses)

If you'd like to [test out purchases without setting up an entry](https://developer.android.com/google/play/billing/billing_testing.html#billing-testing-static) on Google Play, you can use the following product IDs that Google has designated for testing.

```
android.test.purchased
android.test.canceled
```
 
#### Purchase Events
Just like on iOS, purchase events are available, so your app is informed when purchases succeed, fail and so forth. The following events apply to Android.

* Player can purchase goods
* A purchase succeeds
* A purchase fails
* A purchase is canceled
* A product info request succeeds (required to get title/price/description, you can't use these blocks without this event)
 

## Consumables

Consumable purchases are products that can be **used**. More specifically, these are products that can be repurchased over and over again. This contrasts with regular (non-consumable) purchases that stay with the user forever. 

A common example of a consumable purchase is virtual currency. Some games (particularly those that make you wait to progress), will sell a special currency that can be used in-game to speed the game up or let you purchase special items that accomplish the same.

#### Usage

Consumables get "used" with the **use product** block (same block as **buy product**, click the dropdown). Make sure to check that the user has at least 1 of that product before using, as shown below.

![consume-product](https://static.stencyl.com/pedia2/ch12/use.png)

If consumption was successful, you will receive a purchase-succeeded event. If it failed, you will receive a purchased-failed event. **Be sure to handle these events** - do not let the user consume the products immediately.

#### FAQ: Handling Unmanaged Purchases

In Billing v3, unmanged products are treated as managed products. You don't have to create a new entry for them, but you do have to take one extra step to let a user "repurchase" them.

![unmanaged-purchase](https://static.stencyl.com/pedia2/ch12/unmanaged.png)

To replicate unmanaged products in Billing v3 for new products, create a managed, consumable product instead.
 

## Restoring Purchases

If a user installs your app in a different device, or if the user has wiped their device, they'll want to get their purchases back for your app. Restoring Purchases is the feature that enables this. The way it works is that when a restore happens, the game acts as if the player made all those purchases again.

**Restoration happens automatically when a game launches**, but you can force a restore to happen (such as providing a block to let the user request this).

Use the restore purchases block under Game > Mobile to forcefully initiate this process.

![restore-example](https://static.stencyl.com/pedia2/ch12/restore-block.png)

When this happens, you will receive a series of purchase-restored events, each corresponding to a product). It's your task to react to these events in an appropriate manner.

![restore-purchase-event](https://static.stencyl.com/pedia2/ch12/restore.png)


## FAQ / Troubleshooting

#### I uploaded my APK, but the developer console won't let me add IAPs to my game.

Before you export and upload your game, ensure that the **Enable Purchases** checkbox is checked for your game, otherwise the Google developer console will not let you add IAPs. Enable Purchases is located inside **Settings > Mobile > Monetization**.

![billing-app-key](https://static.stencyl.com/pedia2/ch12/enable-purchases.png)

#### What happened to unmanaged purchases?

Google has made everything a managed purchase. The closest thing to an unmanaged purchase is a consumable, managed purchase. To gracefully handle existing "unmanaged" purchases, do the following to let a user "repurchase" them.

![unmanaged-purchase](https://static.stencyl.com/pedia2/ch12/unmanaged.png)

#### I can't test my IAPs in-game.

* Did you remember to set up [test accounts](https://support.google.com/googleplay/android-developer/answer/6062777)?
* Did you remember to publish your game to [alpha or beta channels](https://support.google.com/googleplay/android-developer/answer/3131213) in Google Play?

Consult Google's [testing in-app billing](https://developer.android.com/google/play/billing/test) guide for further details.


## Further Reading

* [Uploading an APK to Google Play](https://support.google.com/googleplay/android-developer/answer/113469)
* [Testing In-App Billing](https://developer.android.com/google/play/billing/test)
* [Setting up Test Accounts](https://support.google.com/googleplay/android-developer/answer/6062777)
