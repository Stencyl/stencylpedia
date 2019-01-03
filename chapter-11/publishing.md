## Contents

* Requirements
* Walkthrough
  * Step 1: Enter in Certificate Details
  * Step 2: Export to an IPA
  * Step 3: Upload to Apple
  * Step 4: Share with Testers
* Troubleshooting
* Advanced: Deploying Apps Over the Air (OTA)
 

## Requirements

* [Set up your certificates](http://www.stencyl.com/help/view/ios-certificates-guide)
* [Being able to test your game on your device](http://www.stencyl.com/help/view/ios-getting-started)
 

## Step 1: Enter in Certificate Details

Before you can export your app, you'll need to tell Stencyl where your P12 and provision profiles are located.

Specify these two things under Game Settings > Mobile > Certificates (iOS).

![](http://static.stencyl.com/help/images/ios-primer2-6.png)


## Step 2: Export an IPA

An IPA (iPhone Archive) is the file you send to Apple or deliver to beta testers for testing. 

To export your game as an IPA, go to **Publish > Mobile > iOS** from the main Menu. The app will churn for a bit and then ask you whether you're deploying to the App Store or Testers (Ad Hoc).

Either way, you'll get an IPA file out of it.

> **Note:** Advanced users can export to an Xcode project (Publish > Mobile > Xcode Project) if they need to perform additional steps before exporting an IPA.
 

## Step 3: Upload to Apple


#### Visit iTunes Connect

First, head over to [iTunes Connect](https://itunesconnect.apple.com), the web app that lets you submit your app for review. (You may already have done all of this if your game uses Game Center and/or purchases.)

During this process, you'll be asked to enter in all of the relevant details and screenshots for the game.

#### Does this app use the Advertising Identifier (IDFA)?

You will be asked the following question on iTunes Connect: **Does this app use the Advertising Identifier (IDFA)?**

* Answer **NO** if your game has no ads.

* Answer **YES** if your game has any ads. If your game gets rejected, send a link to a YouTube video demonstrating that the ads work.

#### Launch Application Loader from Xcode

At some point, iTunes Connect will ask you to upload your game through the Application Loader app on your Mac.

1) Launch Xcode.

2) From the main menu, it's found at: **Xcode > Open Developer Tool > Application Loader**

![](http://static.stencyl.com/pedia2/ch11/app-loader2.png)

#### Using Application Loader

Application Loader is the app you'll use to send your IPA over to Apple.

1) After you launch Application Loader, sign in when asked.

2) Once you are in, choose **Deliver Your App** and locate the IPA that you just exported.

3) Now, follow the rest of the process to upload your app.

If you get stuck, we recommend checking out [Apple's page on Application Loader](https://itunesconnect.apple.com/docs/UsingApplicationLoader.pdf).


## Step 4 (Optional): Share with Testers

If you want to share your game with others for beta testing, you'll need to publish the game as an Ad Hoc build (that question is posed during publishing from Stencyl). 

After the Ad Hoc IPA is created, upload it to a service such as TestFlight or [provide it directly to your audience through a private site](https://github.com/Stencyl/stencylpedia/blob/master/chapter-11/ota.md).

> **Note:** Don't forget that you need to include any beta testers within your provision profiles. Services like TestFlight will remind you about this.
 

## Troubleshooting

If you haven't set up your certificates properly, you'll run into problems during the IPA export process.

We've devoted an entire article to [troubleshooting common issues](http://www.stencyl.com/help/view/ios-certificates-guide) with iOS, Xcode and Certificates.
