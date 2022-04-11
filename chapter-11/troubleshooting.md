## Introduction

Let's be honest - the entire iOS toolchain and Xcode can be a pain to work with. For the non-technical amongst us, the errors that Xcode can spit out can be as confusing as a foreign language.

This is a list of practically every error we've ever seen our users hit. Chances are good that an error you hit will be on here. If isn't, let us know in the comments or a forum post, and we'll add it.

> **Note:** Much of this guide assumes you've followed the instructions in our iOS certificates primer and know the general concepts behind certificates. 
 

## What *NOT* to do

* **Don't blindly reinstall Stencyl**. Unless you've tampered with the install, it has nothing to do with these errors. Certificate errors are always (unfortunately) caused by user error or confusion from Apple's part.

* **Don't blindly reinstall your certificates or profiles**. Sometimes, this helps - if you see something about a certificate expiring, then this is what you do. But more often than not, certificates don't become  "corrupt" (at worst, they've expired, and you can verify this in Keychain Access or from Apple's site), and a cycle of reinstalling them won't help.

* **Don't panic** and go on a forum posting binge. Instead, pick apart what the error message is saying, see if this guide already covers it and check on Google before posting on the forums.
 

## The Errors

> **Note:** We've linked in forum topics that inspired these entries. Some may link to our private customer forums.

#### iOS Simulator
**Q: The iOS Simulator does not open.**
<br/>A: Try reinstalling Xcode from the App Store.
https://community.stencyl.com/index.php/topic,16959.0.html

**Q: The iOS Simulator opens but the app never runs. You see "iOS Simulator failed to install the application" in the logs.**
<br/>A: Use the "Reset Content & Settings" option in the simulator.
https://community.stencyl.com/index.php/topic,17139.0.html

 
#### Xcode / Installation
**Q: Can't build (and the logs don't have anything useful). Somewhere in the proces, you upgraded or downgraded Xcode.**
<br/>A: https://community.stencyl.com/index.php/topic,17227.0.html

**Q: You see an error in the logs about "object file format unrecognized, invalid, or unsuitable"**
<br/>A: Install Xcode Command Line Tools through the Preferences > Downloads screen in Xcode.
https://community.stencyl.com/index.php/topic,18001.0.html

**Q: You see an error in the logs about "fatal error: 'typeinfo' file not found"**
<br/>A: Install Command Line Tools from Xcode's Preferences, and run `sudo ln -s /usr/bin/clang /Applications/Xcode.app/Contents/Developer/usr/bin/clang`
https://community.stencyl.com/index.php/topic,15476.15.html

 
#### Certificates & Signing
**Q: You see an error in the logs about "codesign: ambiguous"**
<br/>A: https://community.stencyl.com/index.php/topic,16959.0.html (check Keychain Access and delete the duplicate certificates that are NOT in the Login keychain)

**Q: You see an error in the logs about "Code Sign error: The identity 'iPhone Developer' doesn't match any valid, non-expired certificate/private key pair in your keychains"**
<br/>A: Two or more possibilities here.

- You didn't specify a password when exporting the p12 file or entered in an incorrect password.

- Your p12 was exported from the Developer certificate, rather than the Distribution certificate. Reexport it. This mistake is very common. https://community.stencyl.com/index.php/topic,18087.0.html

**Q: You see an error in the logs about "no identity found"**
<br/>A: Several possibilities similar to the above.

- Your certificate expired (check Keychain Access or the Apple Developer Portal).

- You exported the Development, rather than Distribution certificate or provisioning profile.

- You didn't specify a password when exporting the p12 file or entered in an incorrect password.

**Q: You see an error in the logs about "No unexpired provisioning profiles found that contain any of the keychain's signing certificates"**
<br/>A: From Xcode's application menu, go to Xcode > Preferences -> Accounts, then refresh. [SOURCE](https://community.stencyl.com/index.php/topic,22143.0.html)

 
#### Testing on a Device
**Q: You see "Code Sign error: No code signing identities found: No valid signing identities (i.e. certificate and private key pair) matching the team ID “(null)” were found."**
<br/>A: Go to Xcode > Preferences > View Account Details and update and reinstall your certificates from within Xcode. [SOURCE](https://community.stencyl.com/index.php/topic,38831.0.html)

**Q: You see something like "AMDeviceInstallApplication failed: -402620395"**
<br/>A: Three (or more!) possible solutions to this.

- Add your device to the iOS Member Center. To do this, launch Xcode, open up Window > Organizer. Select your device from the DEVICES section of the left pane. Click Add to Member Center (wording may change between versions). [SOURCE](https://community.stencyl.com/index.php/topic,31888.0.html)

- Delete the game you're trying to play on your device. Then run again. [SOURCE](https://community.stencyl.com/index.php/topic,19606.0.html)

- View the Device's logs in Xcode's Organizer to figure out an alternate reason. In one case, the user's device had a lower iOS version than what he'd specified in Game Settings > Mobile > Versions. [SOURCE](https://community.stencyl.com/index.php/topic,19606.msg126690.html#new)
 

## Tip: Just Google it!

We're hardly experts in deciphering what Xcode has said. If we did, we could pre-emptively detect these errors for you. Everything you've seen here was discovered via Google, usually from StackOverflow, a popular questions and answers site for programmers.

If ever in doubt, **type the error in Google and see what comes up**. Chances are high that someone's hit the same error that you have. Even if you don't know what to do, you'll at least share what you've found when you make a forum post and help reach a resolution quicker.
