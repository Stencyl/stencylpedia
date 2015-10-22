> This is Part 1 in a three-part series.<br/><br/>
Part 1 - [Getting Started](http://www.stencyl.com/help/view/ios-getting-started)<br/>
Part 2 - [Understanding Certificates](http://www.stencyl.com/help/view/ios-certificates-guide)<br/>
Part 3 - [Setting up Certificates](http://www.stencyl.com/help/view/ios-certificates-guide-2)


## Contents

* Introduction
* The Key Parts
* Certificates
* Keys
* P12
* Provisioning Profiles
* Recap
 

## Introduction

Apple requires you to **sign your apps** in order to tell the end user’s iOS device that you actually developed them and that they haven’t been tampered with. Wouldn’t it be disastrous if someone else could publish an app under your identity and embed spyware into it?

Inevitably, you're going to run into problems with certificates. **Knowing the fundamentals** will spare you many hours of frustration and anger. 

Please take the time to read this article, so that when you hit a problem related to certificates, you have the knowledge required to reach a solution quickly.
 

> **Note:** To be clear, this article doesn't cover how you set up certificates. The [next article](http://www.stencyl.com/help/view/ios-certificates-guide-2) in the series covers the how-to portion.


## The Key Parts

In the realm of signing apps, you’re responsible for providing 3 key pieces in order to perform the signing.

* A **P12** - A document that contains your credentials for signing the app.
* A **Provisioning Profile** -  A “policy” (permission) that allows a specific app to run on a device while not on others.
* An App ID that uniquely identifies your app.

We’ll go over what each is about.


## Certificates

A **certificate** is a document that Apple issues to you. This certificate states that you are a trusted developer and that you are in fact, who you claim to be, rather than someone else posing as you. It’s much like how a restaurant undergoes food inspections and posts that information at its door.

![certificates-are-like-inspections](http://static.stencyl.com/help/images/ios-primer-1.png)

In order to receive a certificate, you must generate a **Certificate Signing Request (CSR)** on your Mac using the Keychain Access app. A CSR is **like filing for a permit** which you then send to Apple for verification. If they approve, they send you back your certificate.

![csr-is-like-a-permit](http://static.stencyl.com/help/images/ios-primer-2.png)

Now, we’ll talk about **keys**, the actual “things” that perform the signing and verification of apps.


## Keys

#### Private Key = Your Signature

**A private key is your signature**. It’s something you “stamp” on an app when signing it to signify that you made it.

![private-key](http://static.stencyl.com/help/images/ios-primer-3.png)

#### Public Key = Signature Checker

A **public key** is a special code that lets anybody (in this case, the end user’s iOS device) **verify that your app was published by you** and hasn’t been tampered with. It’s similar to how a cashier will [swipe a $20 bill](http://money.howstuffworks.com/question212.htm) with a marker to check that it’s not counterfeit.

![public-key](http://static.stencyl.com/help/images/ios-primer-4.png)

#### Where do these 2 keys come into play?

The **Certificate Signing Request (CSR)** that you send to Apple contains your public key, some personal information about you and is signed using your private key. Apple then uses the public key in the CSR to verify that your CSR came from you before issuing your certificate (which contains your public key).

![csr-approval](http://static.stencyl.com/help/images/ios-primer-5.png)

In the end, you have two things at this point.

* A **certificate** (.cer) that contains your public key.
* Your **private key**.

In the next section, we’ll now go into how these two parts combine to sign your app for the App Store.


## P12

A P12 file bundles a certificate (which already contains a public key) and private key into a single file.

![p12](http://static.stencyl.com/help/images/ios-primer-6.png)

When your app is “signed”, the p12 is broken apart. The **private key** is used to “sign” your app, while the **certificate** is embedded inside of the app, so that an end user’s device can use the public key within the certificate to verify the app’s authenticity.

![certificate-embedded](http://static.stencyl.com/help/images/ios-primer-4.png)

To summarize, you form a p12 by combining your certificate and your private key. Keychain Access does this for you. You then pass the P12 to Stencyl to do the hard work.


## Provisioning Profiles

A **provisioning profile** is a **permission policy** that allows certain devices to run a specific app. This is used in two ways: Ad Hoc (off-store) and App Store.

#### Ad Hoc
During beta testing, a profile lets you send your app to a tester and guarantee that only designated testers can run your app. Even if your app leaked, others wouldn’t be able to run it.

#### App Store
Ensures that officially published apps can be placed on the App Store and played on end user’s devices. (Conversely, apps that aren’t from the App Store are not allowed to run)

#### What do profiles contain?
In order for a profile to work, it must know two pieces of information.

* What the App is (**App ID**)
* Who can run the app (**Device ID**)

**App ID**’s are unique identifiers that let you tell any app apart from another. They take on a “reverse domain name” form, such as **com.stencyl.platformer**.

A **Device ID** (formally known as a UDID) is similar to a serial number for your iOS device. The UDID can be found via iTunes.

With these two facts, a profile can work its magic and only allow the devices you specify (on Apple’s site) to run your app.

 
## Recap

* Signing is Apple’s way of guaranteeing that your app was published by you and hasn’t been tampered with.
* **Certificates** represent your “signature” and present a way for you to “sign” your app and for an end user to verify that an app came from you.
* A **P12** (certificate + private key) is the actual file you provide to Stencyl.
* A **Provisioning Profile** is a permissions policy that allows a specific device (defined by a UDID) to run a specific app (defined by an App ID).

#### Given all of this, what do you do in practice?

1. Generate a Certificate Signing Request (CSR) and upload that to the Apple Developer's Portal.
2. Receive a certificate back. Download and install it.
3. Form a P12 from the certificate and private key (which is stored in Keychain Access).
4. Set up an App ID.
5. Set up Devices for beta-testing.
6. Form a pair of provisioning profiles, one for the App Store and one for Ad Hoc (beta testing) of your app. Download and install both.


## Let's Continue

Now that you understand the concepts and the general procedure, let’s go over how you carry this all out in practice.

<a role="button" class="btn btn-primary btn-lg action-button2" href="http://www.stencyl.com/help/view/ios-certificates-guide-2">Continue</a>
