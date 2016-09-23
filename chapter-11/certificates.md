> This is Part 3 in a three-part series.<br/><br/>
Part 1 - [Getting Started](http://www.stencyl.com/help/view/ios-getting-started)<br/>
Part 2 - [Understanding Certificates](http://www.stencyl.com/help/view/ios-certificates-guide)<br/>
Part 3 - [Setting up Certificates](http://www.stencyl.com/help/view/ios-certificates-guide-2)


## Contents

* Introduction
* Requirements
* Keychain Access
* Walkthrough
  * Part 1: Install Apple's Intermediate Certificate
  * Part 2: Create a CSR
  * Part 3: Install your Certificate
  * Part 4: Create P12
  * Part 5: Create App ID
  * Part 6: Create Devices
  * Part 7: Install Provisioning Profile
  * Part 8: Enter in Details to Stencyl
  * Final Step: Test It
* Troubleshooting

> **Disclaimer:** Apple continually changes its website, so some aspects of this guide will not match 100% to what you see, but the overall process has remained steady. Let us know what needs updating in the comments.
 

## Introduction

In order to publish a game to the App Store, you first need to sign it with a P12 and embed the appropriate provisioning profile (.mobileprovision). 

Before doing this, please read our [Getting Started](http://www.stencyl.com/help/view/ios-getting-started) article and [primer on certificates](http://www.stencyl.com/help/view/ios-certificates-guide).


## Requirements

You must meet the minimum requirements outlined in our [Getting Started](http://www.stencyl.com/help/view/ios-getting-started) article. 


## How to Launch Keychain Access

Keychain Access is the Mac app that manages all of your certificates and keys. You'll be using it a lot during this process, so knowing how to bring it up is a requirement.

To launch it, **click the magnifying glass at the top-right of the screen** (it's called Spotlight) and type in **Keychain Access** - you'll see the app appear in the menu below. Click it to launch it. You'll want to keep it open throughought this process.

![keychain-access](http://static.stencyl.com/help/images/ios-primer2-7.png)


## Step 1 (of 8): Install Apple’s WWDR Intermediate Certificate

1) Visit the **Certificates, Identifiers & Profiles** part of the Developer Center https://developer.apple.com/account/overview.action

2) Click **Certificates**. Then, click on the "plus" button at the top-right.

3) Download the **WWDR Intermediate Certificate** (it's under the Intermediate Certificates section). Double-click it to install.

4) Verify that it's installed inside of **Keychain Access**. It should appear as "Apple Worldwide Developer Relations Certification Authority" under the "login" keychain.

![](http://static.stencyl.com/help/images/ios-primer2-1.png)


## Step 2 (of 8): Create a Certificate Signing Request (CSR)

> Recall from the [primer](http://www.stencyl.com/help/view/ios-certificates-guide) that the CSR is a file that contains your public key and is signed using your private key. Apple uses the public key to verify that you generated this request and then issues your certificate.

1) Launch **Keychain Access**.

2) From the main menu, select **Certificate Assistant > Request a Certificate From a Certificate Authority...**

![](http://static.stencyl.com/help/images/ioscerts/image00.png)

3) Enter in just your e-mail and name. Leave the CA Email Address field blank. Select “Saved to Disk” and “Let me specify key pair information”.

![](http://static.stencyl.com/help/images/ioscerts/image01.png)

4) **Save it** to a location you’ll remember such as the Desktop.

5) On the Key Pair Information screen, it should be **Key Size: 2048 bits and Algorithm: RSA**.

![](http://static.stencyl.com/help/images/ios-primer2-2.png)

6) Click **Done** on the Conclusion screen.

 

## Step 3 (of 8): Install Your Certificate

Now, you'll submit the CSR you just made to Apple and receive your certificate in return.

> **Note:**If you are using Google Chrome and find the iOS Provisioning Portal not to work, use Safari or Firefox instead.

1) Visit the **Certificates, Identifiers & Profiles** part of the Developer Center https://developer.apple.com/account/overview.action

2) Click on **Certificates**. Then, click on the "plus" button at the top-right.

3) Pick the **App Store and Ad Hoc** item. Click Continue until you are prompted for the CSR file.

4) Click **Browse...** and pick the CSR file you just created moments ago. Submit.

5) Wait a few moments, refresh, and the Certificate should be issued.

6) Download the **Distribution** certificate. Double-click to install.

7) Verify that the certificate is installed inside of Keychain Access. It will appear as **iPhone Distribution: Your Name (XXXXXXXX)** under the "login" keychain.

> **Note:** Make absolutely sure it is the **distribution** certificate. If you are working with a team/company account, then the correct certificate may bear the company's name rather than your own.

![](http://static.stencyl.com/help/images/ios-primer-2-3.png)


## Step 4 (of 8): Create a P12 file

> As mentioned in the [primer](http://www.stencyl.com/help/view/ios-certificates-guide), a P12 file combines your certificate and your private key togther into a single file. The private key is used to sign the app, while the certificate is embedded inside of that, so that an end user's device to verify that the app has not been tampered.

1) Launch **Keychain Access**.

2) Locate your **DISTRIBUTION** certificate. (Click “Certificates” in the Category pane to locate it)

![](http://static.stencyl.com/help/images/ioscerts/image02.png)

3) Right-click on that certificate. Select **Export**.

> **Note:** Again, make absolutely sure it is the distribution certificate. If you are working with a team/company account, then the correct certificate may bear the company's name rather than your own.

![](http://static.stencyl.com/help/images/ioscerts/image03.png)

4) Pick a location you’ll remember. **Provide a password (do not leave blank)**. The password itself isn’t that important (you can use "aaa" for example), but you will need to provide it when configuring your game to publish.

![](http://static.stencyl.com/help/images/ios-primer2-4.png)


## Step 5 (of 8): Add Devices (Optional)

> As mentioned in the [primer](http://www.stencyl.com/help/view/ios-certificates-guide), when distributing a game to beta testers, or when testing for your own purpose, you need to add devices to the iOS Provisioning Portal to allow these devices to run your games. If you don't need to do this, skip this section.

1) Visit the **Certificates, Identifiers & Profiles** part of the Developer Center https://developer.apple.com/account/overview.action

2) Click on **Devices**.

3) Click **Add Devices**. (It's the "plus" button at the top-right.)

4) Enter a name that you’ll be able to recognize in the future.

5) Enter in the **Device ID (UDID)**. You can find this ID by connecting your iOS device to your Mac, opening iTunes, selecting the device under DEVICES, and then clicking the Serial Number field which will then switch to Identifier (UDID).

![](http://static.stencyl.com/help/images/ioscerts/image04.png)

6) Submit. Repeat for other devices you want to add.


## Step 6 (of 8): Create an App ID

> As mentioned in the [primer](http://www.stencyl.com/help/view/ios-certificates-guide), an App ID is a unique identifier that’s used to allow your game to communicate with Apple’s services or to share data between your games. A provisioning profile uses the App ID alongside the list of authorized Device IDs to verify that your device is able to play the game.

> You must create an App ID for **EACH** app you make.

1) Visit the **Certificates, Identifiers & Profiles** part of the Developer Center https://developer.apple.com/account/overview.action

2) Click on **Identifiers**.

3) Click **New App ID**. (It's the "plus" button at the top-right.)

4) Enter in a name that you’ll remember. **(This is NOT the App ID yet!)**

5) Enter in the actual **App ID** you wish (Explicit App ID) and then submit. We strongly recommend sticking to the convention that Apple suggests of using a reverse-domain name. For example, **com.stencyl.balloons**.

> **Note:** Even though Apple may allow this, make sure your App ID doesn't have an underscore ("_") in it. This causes a failure at build-time.

6) Under Services, only check Game Center and In-App Purchase. Do not pick any other services like iCloud.

 

## Step 7 (of 8): Install Provisioning Profiles

> Recall from the [primer](http://www.stencyl.com/help/view/ios-certificates-guide) that a provisioning profile is a document that combines an App ID and a list of Devices together to form a permission policy that tells a device whether a given application will run on a given device, and for what method of distribution it will be targeted at (App Store or Ad Hoc).

> You must create a Provisioning Profile for **EACH** app you make.

1) Visit the **Certificates, Identifiers & Profiles** part of the Developer Center https://developer.apple.com/account/overview.action

2) Click on **Provisioning Profiles**.

3) Click on the **Distribution** item in the left sidebar. (Do NOT deal with the Development tab. This is a common error.)

4) Click **New Profile**. (It's the "plus" button at the top-right.)

5) Fill in the details as appropriate and submit. Do this twice, once for the **App Store** and one for **Ad Hoc**. This will result in **TWO** different provisioning proiles.

6) After you’ve created both profiles, download them to your Mac and **double-click them to install them**. They have an extension of **.mobileprovision**.

7) You can verify that the provisioning profiles have been installed by checking the **Accounts** area of Xcode (Xcode > Preferences > Accounts) and clicking on View Details at the bottom (you need to sign in with your Apple ID to enable this).

![](http://static.stencyl.com/pedia2/ch11/xcode-accounts2.png)

 

## Step 8 (of 8): Enter in the details to Stencyl

Now, you just need to tell Stencyl where your **P12** and **provisioning profiles** are located, and your Apple Team ID. This is located under **Game Settings > Mobile > iOS Certificates**.

![](https://github.com/Stencyl/stencylpedia/raw/master/chapter-11/images/stencyl-certificates-page.png)

Your Personal Team ID can be found on your [Apple Developer Membership](https://developer.apple.com/account/#/membership) page.

![](https://github.com/Stencyl/stencylpedia/raw/master/chapter-11/images/apple-team-id.png)


## Final Step: Test It!

Now that you have your certificates, it's a good idea to test them out. 

**Publish your iOS game from Stencyl** (Menu > Publish > Mobile > iOS) to generate an IPA (the package that you send to a beta tester or to Apple).

If no errors happen along the way, you're (probably) good to go and are ready to publish to the App Store.

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/view/ios-app-store/">Publishing to the App Store</a>
 

## Troubleshooting

Inevitably, things will go wrong in this process, usually because a step wasn't followed correctly. Specifically, we tend to see the following happen a lot.

* The #1 user error is a mismatch between the App ID and the provisioning profile used for the app. This can come about if you use a provisioning profile that was intended for a prior app and forgot to make a new one for your newer app. A second very common cause is forgetting to fill in the App ID field within Stencyl (so that it uses the default one, com.stencyl.test).

* Failing to install **BOTH the Development AND Distribution certificates**.

* Mixing up the App Store and Ad Hoc (Beta Testing) Provisioning Profiles. For example, we frequently see the App Store profile accidentally used for the Ad Hoc situation.

* The certificate(s) expired. You will have to remake it, uninstall the old ones and install the new ones.

* The provisioning profile(s) expired. You will have to remake it and install it.

We've written up a comprehensive troubleshooting guide that catches most of the common scenarios.

Read our [iOS Troubleshooting Guide](http://www.stencyl.com/help/view/xcode-ios-troubleshoot/).
