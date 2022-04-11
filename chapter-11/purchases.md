## Contents

* Introduction
* Requirements
* Walkthrough
  * Setting up on iTunes Connect
  * Setting up your iOS device
  * Setting up Purchases in Stencyl
  * Purchase Events
  * Consumables
  * Restoring Purchases
* Troubleshooting
 

## Introduction

In-App Purchases (IAP) let you sell goods and services from within a game. This gives developers more opportunities to monetize the free app by providing downloadable, supplementary content (new levels or game modes), an unlock for the full game and much more.

#### What's Covered?

Most of the work involves setting up the purchases on iTunes Connect. Once you get past that part, it's just a matter of setting up a few blocks inside of Stencyl.

This guide will show you how to set up In-App Purchases in iTunes Connect and get you up to the critical point - getting iOS to display its standard prompt for purchasing an item.

#### Supported Features

Feature | Supported?
--- | ---
Regular Purchases | Yes
Consumables | Yes
Restoring Purchases | Yes
Susbcriptions | No

 
## Requirements

* An active iOS Developer License from Apple
* All your certificates and provisioning profiles should be properly set up
* For the App ID you will use, In-App Purchases must be enabled. Go to the iOS Provisioning Portal to check.
* An active **iOS Paid Applications Contract** (check the Contracts, Tax & Banking section of iTunes Connect!)
* A compatible iOS device - **In-App Purchases cannot be tested in the iOS Simulator**

> **Note:** You do not need a Studio license with us to test this feature. You only need it to publish your game.


## Setting Up on iTunes Connect

> **Disclaimer:** Apple continually changes the process, making it difficult for us to maintain this portion. The general ideas should remain the same, but the specifics and names can and will change over time.

#### Step 1: Go to iTunes Connect

https://itunesconnect.apple.com

#### Step 2: Set up a Sandbox Account

1. Click on **Manage Users**
2. Click on **Test User**
3. **Define a user**. This is the account you will test In-App Purchases with.
 
#### Step 3: Set up a new game with IAPs

1. Create a new game entry in iTunes Connect.
2. Click **Manage In-App Purchases**
3. Click **Create New**
  * Pick **Non-Consumable**
  * Fill out the form
  * **"Cleared for Sale" must be yes**, and you must provide a screenshot. It's OK for now to provide a blank screenshot.
3. Repeat Step 3 for as many items as you need.

> **Note:** What if you want to operate on an existing game? You can, but only under certain conditions that Apple dictates. Consult Apple's documentation for details.
 
#### Step 4: Mark Game as Ready to Upload
When you are ready to proceed, mark the game as **Ready to Upload**, but do NOT submit the binary yet.


## Setting up your iOS Device

#### Step 1: Sign Out
**Sign out of your "Store" account** on your device (it's under the Settings App as "Store" towards the bottom). Do NOT sign back in using the test account yet! You will sign in to the test account while you are testing your game.

#### Step 2: Delete the Existing Game
If you're testing your game, it helps to **delete the existing copy of the game** from the device that never had IAPs to begin with.

 
## Setting up Purchases in Stencyl

Making purchases in Stencyl requires two steps. One is setup related.

1. First, you must declare what goods you want to sell upfront. Just once.
2. Then, you can buy the goods using the buy block.
 
#### Step 1: Declare All Purchases
Use the request info for product block to declare a purchase. You can find it under Game > Mobile towards the bottom. The ID you use is the **Product ID** you entered into iTunes Connect.

![request-product-info](https://static.stencyl.com/pedia2/ch11/request-product-info.png)

Do this for each purchase in your game. You only have to do this ONCE, not every time you wish to make a purchase.

(In order to "know" when your request succeeded, use the **when a product info request succeeds** event under **Add Event > Mobile > Purchases**)

![product-info-event](https://static.stencyl.com/pedia2/ch11/product-event.png)
 
#### Step 2: Make a Purchase
Now, all you have to do is create a behavior that buys the product. You can find the **buy product block** under **Game > Mobile** towards the bottom. The ID you use is the **Product ID** you entered into iTunes Connect.

![buy-product](https://static.stencyl.com/pedia2/ch11/purchase.png)

You should always check if a purchase succeeded (or failed) using the purchase events we provide (under Add Event > Mobile > Purchases). Only if a purchase succeeds should you proceed to unlock or provide the promised functionality.


#### Step 3: Test it Out

Now, run your game on your iOS device. If everything was properly set up, your app should prompt you to purchase your product. Congratulations!

If you are less fortunate and nothing happens after 30 seconds or so, read the **Troubleshooting** section.

 
## Purchase Events

In prior versions of Stencyl, it was challenging to determine exactly when a purchase succeeded or failed. This is no longer the case. You now can use **Events** (all under Add Event > Mobile > Purchases) to react to various Purchase-related happenings.

* Player can purchase goods.
* A purchase succeeds.
* A purchase fails.
* A purchase is restored.
* A purchase is canceled.
* A product info request succeeds (required to get title/price/description, you can't use these blocks without this event)
 

## Consumables

Consumable purchases are products that can be used. More specifically, these are products that can be repurchased over and over again. This contrasts with regular (non-consumable) purchases that stay with the user forever.

A common example of a consumable purchase is virtual currency. Some games (particularly those that make you wait to progress), will sell a special currency that can be used in game to speed the game up or let you purchase special items that accomplish the same.

#### Usage
Consumables are "used" using the **use product** block (same block as **buy product**, click the dropdown). Make sure to check that the user has at least 1 of that product before using, as shown below.

![consume-product](https://static.stencyl.com/pedia2/ch12/use.png)

If consumption was successful, you will receive a purchase-succeeded event. If it failed, you will receive a purchased-failed event. **Be sure to handle these events** - do not let the user consume the products immediately.
 

## Restoring Purchases

If a user installs your app in a different device, or if the user has wiped their device, they'll want to get their purchases back for your app. Restoring Purchases is the feature that enables this. The way it works is that when a restore happens, the game acts as if the player made all those purchases again.

#### Usage

Use the **restore purchases block** under **Game > Mobile** to initiate this process (connect it to a button press, for example).

![restore-purchases](https://static.stencyl.com/pedia2/ch12/restore-block.png)

When this happens, you will receive a bunch of **purchase is restored events** (which you can receive via Add Event > Mobile > Purchases), each corresponding to a purchase. It's your task to react to these events in an appropriate manner.

![restore-event](https://static.stencyl.com/pedia2/ch12/restore.png)


## Troubleshooting

So... something didn't quite go right. First, **check your logs**.

If you see something along the lines of "**Cannot connect to the iTunes Store**", then you know for certain that something didn't quite go right along the way.

Here's a list of everything we know that could go wrong.

#### Out of your control
* Wait up to 24 hours for iTunes Connect to sync its data.
 
#### In your control
* Is your iOS Paid Applications contract active? (Check Contracts, Tax and Banking in iTunes Connect)
* Have you enabled In App Purchases for the App ID you are using?
* Have you marked your app as ready to upload?
* Did you remember to check "cleared for sale" for each product?
* Did you member to submit a screenshot for each product?
* Did you provide the correct product IDs, exactly as you entered them into iTunes Connect?
* Did you remember to enter in the product IDs into StencylWorks?
* Did you sign out of your live/real account?
* Did you create a test account in iTunes Connect?
* Did you sign in to the test account, only in the app-itself, NOT under Settings?
* The "dumb" solutions that sometimes work
  * Are you testing your game on your device, not in the simulator?
  Is your device jailbroken?
  Can the device connect to the internet?
  Have you tried deleting and then reinstalling the app? (Not just installing it!)
  Have you tried rebooting your device?

#### Ask for help

If none of these solutions work, [ask for help](https://community.stencyl.com/index.php/board,3.0.html) on the forums. 

In-App Purchases are **challenging** to add because of the obtuse system of setting them up on iTunes Connect. Unfortunately, there's little we can do to make this process easier besides providing help and documenting solutions to common problems as they come along.
