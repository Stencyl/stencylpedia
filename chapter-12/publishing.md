## Contents

* Introduction
* Requirements
* Concepts
* Walkthrough
  * Step 1: Set up Certificates
  * Step 2: Export an APK
  * Step 3: Upload to Google Play
* FAQ


## Introduction

Google Play is the the primary place for distributing Android apps.

Stencyl provides a quick way of exporting a signed app for publishing to Google Play (in contrast to the more [hands-on experience](http://www.stencyl.com/help/view/ios-certificates-guide-2) that Apple requires).


## Requirements

* Ensure that you’re able to [test an app](http://www.stencyl.com/help/view/setup-android) on your Android device.
* Registration in the [Google Play Developer Program](http://developer.android.com/distribute/googleplay/publish/register.html).


## Concepts

In order to publish your game on Google Play, you must **sign** your app using a "signature" (called a private key). Much like a real signature, signing establishes that you, in fact, are the creator of the app you're uploading.

![sign-private-key](http://static.stencyl.com/help/images/ios-primer-3.png)

When an end-user plays your game, the device he's using has to verify that the game is in fact yours, rather than a forgery. This verification mechanism is called a **public key** (or coloquially called the "certificate"), and it's a code that's embedded into the game itself.

![verify-public-key](http://static.stencyl.com/help/images/ios-primer-4.png)

A **keystore** is a file on your computer that contains both your private key and public key. It isn't all that different from the [P12 for iOS](http://static.stencyl.com/help/images/ios-primer-6.png), which serves the same purpose and is in fact, just a keystore in a different format.

With this in mind, let's get started with the publishing process.


## Step 1: Setting up the Keystore

> **Note:** If you already have a keystore, flip to **Settings > Mobile > Certificates (Android)** and fill in the fields.

1) In Stencyl, go to **Settings > Mobile > Certificates (Android)**

![](http://static.stencyl.com/help/images/google-play-2.png)

2) Click on **Make an Android Certificate**

3) Fill in all fields. Pay attention to the requirements for each field.

![create-keystore](http://static.stencyl.com/help/images/google-play-3.png)

4) You’re done. Not only does this do all the hard work, it will also fill in the fields on the Certificates (Android) page for you.

You only need to go through this process just once. Your keystore persists between installs of Stencyl and can be revealed on your file system (for backup purposes) by clicking on **View Certificate**.

Keep the keystore file you generate with Keytool in a safe, secure place. You must use the same key to sign future versions of your game. If you republish your app with a new keystore, Google Play will consider it a new app.
 

## Step 2: Export an APK

An APK (Android Application PacKage) is the file you send to Google for review.

To export your game as an APK, from the main menu, go to **Publish > Mobile > Android**. Stencyl will churn for a bit and then spit out a signed APK that you'll upload to Google Play.

> **Tip:** Monitor the Log Viewer (View > Log Viewer) to check on the progress of the export process.
 

## Step 3: Upload to Google Play

At this point, you can upload your APK to Google Play. [Follow Google's instructions](http://developer.android.com/distribute/googleplay/publish/register.html) to begin that process. You'll need to sign up for a developer account if you don't have one yet.
 

## FAQ

#### My keystore got corrupted. How do I remake the keystore?
First, delete the existing keystore using the "Delete Certificate" button (the red one). Then, remake the certificate. 

#### Can I update my game if I remake the keystore (or lost it)?
No, if you overwrite or delete your Stencyl-generated keystore after publishing an app to Google Play, you won’t be able update your app. You'll need to pull the old entry down and make a new one.

#### How can I back up my keystore?
From **Settings > Mobile > Certificates (Android)**, click on **View Certificate** to reveal the keystore on your computer.

#### Can I use an existing keystore that I made outside of Stencyl?
Yes you can. Just specify the path to it under **Settings > Mobile > Certificates (Android)** and clicking the Choose... button next to the Keystore field.
