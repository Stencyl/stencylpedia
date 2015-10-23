## Contents

* Requirements
* Is there an Android "simulator"?
* Walkthrough
  * Step 1: Set up your Device
  * Step 2: Install the Java JDK
  * Step 3: Install the Rest
  * Step 4: Test on Device
* Troubleshooting
* FAQ
 

## System Requirements

To test and publish to Android, you need the following.

* An Android device with Gingerbread (2.3) or better (4.0 or better strongly recommended)
* A USB cable to connect your device to your computer
* Java Development Kit 1.6 (JDK 1.6) or later

The rest of the software requirements are fetched by Stencyl directly from Google's servers.


## Is there an Android "simulator"?

No emulator or simulator is available for testing Android games on your computer. 

If you don’t have an Android device, we recommend picking up a cheap one, such as a [Moto E](https://www.motorola.com/us/smartphones/moto-e-2nd-gen/moto-e-2nd-gen.html) or [Moto G](http://www.motorola.com/us/products/moto-g). We do not recommend purchasing off-brand devices since you may be unable to test your games on them
 

## Step 1: Set up your Device

If you haven’t tested apps on your device before, you’ll need to do a few things to it before you begin.


#### Install a USB Driver

For some devices, especially those made by Samsung, a USB driver (called an OEM USB Driver) has to be installed for your PC/Mac to recognize your device. 

Google maintains a [page](http://developer.android.com/tools/extras/oem-usb.html) that lists all of these devices out.

#### Turn on USB Debugging

**USB Debugging** must be enabled, otherwise your device will be unable to communicate with your computer. The location of this option varies depending on what version of Android and what device you have.

**Do a Google search for `USB debugging [YOUR_DEVICE_HERE]`**

#### Turn on USB Mass Storage

If you don't turn off **USB Mass Storage**, your device will be treated like a USB flash drive, rather than a proper Android device. Again, the location of this option varies depending on what version of Android and what device you have.

One trick that sometimes works is to plug your device in - if you're lucky, your device will ask you whether you want to Turn off USB Mass Storage.

**Do a Google search for `USB Mass Storage [YOUR_DEVICE_HERE]`**


## Step 2: Install the Java JDK

Android requires the Java JDK (Java Development Kit), version 1.6 or later, in order to build and sign apps. You must install this on your own, although Stencyl will make a best effort to flag this if you don’t have it installed.

* [Mac](http://stackoverflow.com/a/6785545)
* [Windows](http://www.oracle.com/technetwork/java/javase/downloads/jdk6downloads-1902814.html)
* [Linux](http://www.oracle.com/technetwork/java/javase/downloads/jdk6downloads-1902814.html)
 

## Step 3: Install the Rest

The rest of the requirements (the Android SDK) are **automatically downloaded by Stencyl**. This is triggered when you attempt to run an Android app for the first time.

* **Plug in your Android device** to your computer. Turn it on (or take out of sleep mode).
* Switch the Platform dropdown's value to **Android**.
* Click **Test Game**.
 
If all goes well, you'll see Stencyl download all of the required packages. This takes a while due to the large file sizes.


## Step 4: Test on your Device

After the Android packages finish downloading, Stencyl may ask you to reboot. If it requests that, do that, reopen the game and then run the game again.

* **Plug in your Android device** to your computer. Turn it on (or take out of sleep mode).
* Switch the Platform dropdown's value to **Android**.
* Click **Test Game**.

If all goes well, your game will build for a while and then finally launch the app directly on your device.

> **Tip:** Monitor the Log Viewer (View > Log Viewer) to track the progress of your game's build. The first build will take some time depending on how fast your computer is.
 

## Troubleshooting

#### While downloading the Android SDK in Step 3, the download stops. None of my apps run - how can I reset the installation process?
Go to the following location in the main menu: **Debug > Android > Reinstall Android SDK**

#### My game doesn't launch on my device. It gets stuck at "Sending to Device"
The good news is that if you get this far, it's out of Stencyl's hands - the Android SDK is in control at this point. Failure to launch usuall indicates a hardware / operating system issue. Here are some common causes.

* Make sure the device is plugged in.
* Make sure the device is turned on (not asleep).
* Enable USB Debugging on the device.
* Turn off USB Mass Storage.
* Install the driver for your device. See: http://developer.android.com/tools/extras/oem-usb.html
* Unplug and replug the USB cable, particularly if your computer or the device went to sleep.

If you continue to have issues, view our [forum discussion](http://community.stencyl.com/index.php/topic,20337.0.html) for additional ideas.

#### My game crashes immediately on the device.

* Create a blank, one-scene game and run **that** on your device. If this crashes too, ask for help on the forums.
* If that blank games works fine, run your game on the Windows/Mac/Linux target and see if it crashes there.
* If it crashes, try one last time on Flash. If it crashes, you are (relatively) lucky since you now have logs that are readable. Ask for help on the forums.

#### My game crashes immediately on a Samsung Galaxy (anything recent)

Enable 3x scale for your game since the flagship Galaxy line requires this scale. This change has to be done in two places.

* Settings > Settings > Advanced > Project Scales
* Settings > Mobile > Display > Scales


## FAQ

#### Can I use an existing / external install of the Android SDK?

Not at this time. We'd like to support this in the future.

#### How do I view the official device logs outside of Stencyl?

Use Device Monitor, which can be launched from Stencyl (under Debug > Android > Launch Device Monitor).

#### What version of the Android SDK does Stencyl use?

As of late 2015, we're up to API Level 22 (Lollipop).
