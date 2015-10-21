Contents

Introduction
What's Covered
Requirements
Setting Purchases up on iTunes Connect
Setting up your iOS device
Setting up Stencyl
Test it Out
Purchase Events
Consumables
Restoring Purchases
Troubleshooting
 

Introduction

In-App Purchases (IAP) are an exciting new way for mobile Stencyl games to monetize and bring success to their creators.



It’s known that given a free app and a paid app, the free app will be downloaded on average, 10x as much as the paid app. This gives the creator more opportunities to monetize the free app by providing downloadable, supplementary content (new levels or game modes), an unlock for the full game and much more.

With Stencyl, iOS developers can add In-App Purchases to their games. Like all things Apple, the challenge is entirely in setting up In-App Purchases in iTunes Connect. 

 

What this Primer Covers

This guide will show you how to set up In-App Purchases in iTunes Connect and get you up to the critical point – getting iOS to display its standard prompt for purchasing an item.

 

Requirements

Apple Developer License
All your certificates and provisioning profiles should be properly set up
For the App ID you will use, In-App Purchases must be enabled. Go to the iOS Provisioning Portal to check.
An active iOS Paid Applications Contract (check the Contracts, Tax & Banking section of iTunes Connect!)
An iOS device – In-App Purchases cannot be tested in the iOS Simulator
 

Setting Purchases Up on iTunes Connect

Step 1: Go to iTunes Connect
https://itunesconnect.apple.com

 

Step 2: Set up a Sandbox Account
Click on Manage Users
Click on Test User
Define a user. This is what you will test In-App Purchases with.
 

Step 3: Set up a new game with IAPs
Create a new game entry in iTunes Connect.
Click Manage In-App Purchases
Click Create New
Pick Non-Consumable
Fill out the form.
“Cleared for Sale” must be yes, and you must provide a screenshot. It’s OK for now to provide a blank screenshot.
Repeat Step 3 for as many items as you need.
Note: What if you want to operate on an existing game? You can, but only under certain conditions that Apple dictates. For the sake of keeping this guide simple, we're not going to cover that case.
 
Step 4: Mark Game as Ready to Upload
When you are ready to proceed, mark the game as Ready to Upload, but do NOT submit the binary!

 

Setting up your iOS Device

Step 1: Sign Out
Sign out of your “Store” account on your device (it’s under the Settings App as “Store” towards the bottom). Do NOT sign back in using the test account yet! You will sign in to the test account while you are testing your game.

 
Step 2: Delete the Existing Game
If you’re testing your game, it helps to delete the existing copy of the game from the device that never had IAPs to begin with.

 

Setting up Purchases in Stencyl

Making purchases in Stencyl requires two steps.

You must declare what goods you want to sell upfront. Just once.
Then, you can buy the goods using a block.
 

Step 1: Declare All Purchases
Use the request info for product block to declare a purchase. You can find it under Game > Mobile towards the bottom. The ID you use is the Product ID you entered into iTunes Connect.

request-product-info

Do this for each purchase in your game. You only have to do this ONCE, not every time you wish to make a purchase.

(In order to "know" when your request succeeded, use the when a product info request succeeds event under Add Event > Mobile > Purchases.)

product-info-event

 

Step 2: Make a Purchase
Now, all you have to do is create a behavior that buys the product. You can find the buy product block under Game > Mobile towards the bottom. The ID you use is the Product ID you entered into iTunes Connect.



 

Test it Out

Now, run your game on the device.

If everything was properly set up, your app should prompt you to purchase your product. Congratulations!



If you are less fortunate and nothing happens after 30 seconds, read the Troubleshooting section.

 

Purchase Events

In prior versions of Stencyl, it was challenging to determine exactly when a purchase succeeded or failed. This is no longer the case. You now can use Events (all under Add Event > Mobile > Purchases) to react to various Purchase-related happenings.

Player can purchase goods.
A purchase succeeds.
A purchase fails.
A purchase is restored.
A purchase is canceled.
 

Consumables

Stencyl supports consumable purchases in addition to non-consumables. No extra work is required on your part to support this - Stencyl will automatically keep a count for you.

For example, if you buy a consumable, we'll increment the count for that product by 1. If you use a consumable, that product's count will be decreased by 1.

Note: Although Stencyl automatically keeps count, we recommend maintaining a copy of transactions on a personal server in order to combat cheaters or using a service to track this information for you. 
 

Restoring Purchases

Restoring Purchases allow a user on a separate device who has bought non-consumable goods from your game to transfer those goods to that extra device.

Use the restore purchases block under Game > Mobile to initiate this process (connect it to a button press, for example).

When this happens, you will receive a bunch of purchase restoration events (which you can receive via Add Event > Mobile > Purchases), each corresponding to a purchase. It's your task to react to these events in an appropriate manner.

restore-event

 

Troubleshooting

So... something didn't quite go right. Check your logs.

If you see something along the lines of Cannot connect to the iTunes Store, then you know for certain that something didn’t quite go right along the way.

Here’s a list of everything we know that could go wrong.

 
Out of your control
Wait up to 24 hours for iTunes Connect to sync its data.
 
In your control
Is your iOS Paid Applications contract active? (Check Contracts, Tax and Banking in iTunes Connect)
Have you enabled In App Purchases for the App ID you are using?
Have you marked your app as ready to upload?
Did you remember to check “cleared for sale” for each product?
Did you member to submit a screenshot for each product?
Did you provide the correct product IDs, exactly as you entered them into iTunes Connect?
Did you remember to enter in the product IDs into StencylWorks?
Did you sign out of your live/real account?
Did you create a test account in iTunes Connect?
Did you sign in to the test account, only in the app-itself, NOT under Settings?
The “dumb” solutions that sometimes work
Are you testing your game on your device, not in the simulator?
Is your device jailbroken?
Can the device connect to the internet?
Have you tried deleting and than reinstalling the app? (Not just installing it!)
Have you tried rebooting your device?
If none of these solutions work, ask on the forums. In-App Purchases are challenging to add, not because they’re particularly difficult, but because of the obtuse system of setting them up. Unfortunately, we have little sway in making this process easier, besides documenting every last possibility of failure.
