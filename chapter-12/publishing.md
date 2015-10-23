## Contents

* Introduction
* Requirements
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


## Step 1: Setting up Certificates

Like other mobile apps, a certificate of some kind is required. In this case, Stencyl does most of the work for you.


1) In Stencyl, go to Game Settings > Mobile > Certificates (Android)



2) Click on Generate an Android Certificate

3) Fill in all fields. Take note of any requirements for the fields.



4) You’re done. Not only does this do all the hard work, it will also fill in the fields on the Certificates (Android) field for you.

You only need to go through this process just once, ever. Your keystore persists between installs of Stencyl.

Warning: Keep the keystore file you generate with Keytool in a safe, secure place. You must use the same key to sign future versions of your application. If you republish your app with a new key, Google Play will consider it a new app.
 

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
The keystore is located at [WORKSPACE]/android-sdk/android-sdk-[PLATFORM]/stencyl.keystore. [WORKSPACE] can be found by going to Debug > View > View Workspace Folder from the main menu.

#### Can I use an existing keystore that I made outside of Stencyl?
Yes you can. Just specify the path to it under Settings > Mobile > Certificates (Android) > Keystore.
