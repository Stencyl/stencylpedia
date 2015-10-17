## Contents

* Introduction
* Requirements
* Step 1: Setting up Certificates
* Step 2: Setup up an App ID
* Step 3: Enter the App ID into Stencyl
* Step 4: Export the App
* FAQ

## Introduction

The Mac App Store provides great visibility to Mac games that would otherwise fly under the radar. Publishing a game that already runs on the Mac target takes just a few additional steps. While this involves setting up certificates like on iOS, the overall process is simpler and less prone to issues.

<img alt="Mac App Store" src="http://static.stencyl.com/help/images/mac-app-store-1.png" style="height: 296px; width: 400px; padding-top:20px;">


## Requirements

* A Mac with Yosemite (10.10) or later.
* The latest version of Xcode
* Active registration in Apple’s [Mac Developer Program](https://developer.apple.com/programs/mac/)


## Step 1: Setting up Certificates

In order to publish an app to the Mac App Store, you must sign it. This requires a few certificates.

Unlike iOS, Stencyl doesn’t require a [p12 or mobileprovision file](http://www.stencyl.com/help/view/ios-certificates-guide) to sign an app for Mac. If you’ve already installed your Mac App and Mac Installer certificates (from Apple's developer portal), skip down to Step 2.

> **Explained:** The reason why a p12 or mobileprovision file is not required is because we're building the app directly from the Mac, hence it's OK to just install the certificates directly.

1. Sign up for the [Mac Developer Program](https://developer.apple.com/programs/mac/).
2. Visit the [developer portal](https://developer.apple.com/programs/mac/) and sign in.
3. Click on **Developer Certificate Utility**.
4. Click on **Certificates**.
5. Click on **Create Certificate**.
6. Click on the **WWDR Intermediate Certificate** link to download it. Then, double-click the file after it downloads to install it.
7. Select **Distribution > Mac App Store**. Tick both checkboxes (Mac App Certificate, Mac Installer Certificate)
8. Click **Create**. Then, follow the instructions to the letter. Apple guides you through this. You’ll end up creating 2 certificates, which you will each double-click after downloading to install.

If you’ve done everything correctly, you should have installed the following **3 certificates**:

* WWDR Intermediate Certificate
* Mac App Certificate
* Mac Installer Certificate

You can verify their installation through the Keychain Access app. You should find something like the following.

![Keychain Access](http://static.stencyl.com/help/images/mac-app-store-2.png)

 

## Step 2: Set up an App ID (on Apple's site)

First, you need to set up an App ID for your app, much like how you have to set up an App ID for an iOS App.

1. Go to Apple’s [Developer Certificate Utility](https://developer.apple.com/certificates/index.action#maccertrequest)
2. Click on **App IDs**
3. Create an App ID. Something of the form **com.yourcompany.gamename** is appropriate. *(Example: com.stencyl.balloons)*
4. If you’re using Game Center, you’ll need to mark the corresponding checkbox for that.


## Step 3: Specify the App ID

Once the App ID is setup, enter that App ID into Stencyl. You can do this from **Settings > Desktop > Mac App Store**.

![Within Stencyl](http://static.stencyl.com/help/images/mac-app-store-3.png)


## Step 4: Export the App from Stencyl

From the main menu, go to **Publish > Desktop > Mac App Store**.

After compiling and packaging the app, it’ll save it out as a **PKG** archive. This is what you provide to Apple in the [Mac Developer Center](https://developer.apple.com/programs/mac/).

![PKG](http://static.stencyl.com/help/images/mac-app-store-4.png)

> **Note:** You may get a couple popups in this process about codesign and product build wanting to use your keys. Click Allow or Always Allow.<br/>![Error](http://static.stencyl.com/help/images/mac-app-store-5.png)


## FAQ

#### Testing a PKG Archive
If you attempt to double-click the PKG to test the installation process, it won’t necessarily install to Applications or Launchpad. Apple prefers to install the app to the same folder where the PKG is located, so it will appear that nothing happened. This isn’t the case once the app hits the store.

#### Watch out for expired certificates
Certificates expire after a few years - the exact date is displayed in Keychain Access. You'll need to remake them if you want to update your app or publish new apps.
