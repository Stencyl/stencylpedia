> **Extending Stencyl**

> Engine ([Basics](http://www.stencyl.com/help/view/how-to-create-engine-extension/) - [iOS & Android](http://www.stencyl.com/help/view/how-to-create-native-engine-extension/) - [Native Events](http://www.stencyl.com/help/view/native-callbacks/) - [Flash](http://www.stencyl.com/help/view/flash-extensions/) - [Blocks](http://www.stencyl.com/help/view/adding-blocks/) - [API](http://static.stencyl.com/api/33/))

> Toolset ([Extensions](http://www.stencyl.com/help/view/creating-extensions/) - [API](http://api.stencyl.com/extensions/))


## Contents

* Introduction
* Setup
* Walkthrough
  * How to Create an Extension (iOS)
  * How to Create an Extension (Android)
  * Editing Build.xml
  * Sending Data back from Native to Haxe
* Including External Libraries
* Building from Command Line
* Tips
 

## Introduction

Native Extensions allow Haxe code to call Objective-C, C++ or Java code, thereby allowing your games to take advantage of native functionality and APIs.

These extensions accomplish this by getting **pointers** to those native functions and then calling them. Although the exact details differ slightly between iOS and Android, the underlying concepts are the same.


## Setup

#### Before You Begin

* Read our [article](http://www.stencyl.com/help/view/how-to-create-engine-extension/) on Engine Extensions.

* Check out the **test-native** extension (under [WORKSPACE]/engine-extensions) to familiarize yourself with the parts. **test-native** shows how to create an Alerts extension that works both on iOS and Android. We reference this example throughought this article.

> **[WORKSPACE]** refers to the path to your Stencyl workspace (find it using Debug > View > View Workspace Folder).


#### Add Haxe to your Path

If you’re writing an iOS or Android extension, you must add a couple items to your computer's "path" before proceeding, so that our bundled install of Haxe is recognized by the system.

> **Note:** If you prefer to use your own install of Haxe, you must use Haxe 3.1. Don't forget to install Neko too.
 

**Mac**<br/>
Run the following in Terminal.

```
export DYLD_LIBRARY_PATH=/path-to-stencyl/plaf/neko-mac
export PATH=$PATH:/path-to-stencyl/plaf/neko-mac
```

**Windows**<br/>
Add the following path to your system path.

```
/path-to-stencyl/plaf/neko-win
```

**Linux**<br/>
Run the following in the command line.

```
export LD_LIBRARY_PATH=/path-to-stencyl/plaf/neko-linux
export PATH=$PATH:/path-to-stencyl/plaf/neko-linux
```


## How to Create an Extension (iOS)

> **Note:** This section walks through the test-native extension and explains how the system works. The test-native extension adds Alerts to iOS and Android games.
 
#### The 3 Parts
Every iOS extension consists of 3 parts.

1. **Haxe code** that your game calls. This Haxe code fetches function pointers to native code and calls them
2. **C++ code** that sets up a mapping between those function pointers and Objective-C code.
3. **Objective-C code** that does stuff in iOS.
 
#### Part 1 - The Haxe code

The purpose of the Haxe portion of the extension is two fold.

* It exposes an API for your game (and blocks) to use.
* It fetches function pointers to native code and calls them.

Open up **NativeTest.hx**. Find the following code near the bottom (~line 42).

```
static var iosAlert = nme.Loader.load("ios_alert", 2);
```

In this snippet, we're getting a "function pointer" to `ios_alert`, a C++ function. The first parameter is the name of the function. The second parameter is the number of parameters that function takes.

Now look for this (~line 24).

```
#if(cpp && mobile && !android)
iosAlert(title, message);
#end
```

Here, we're calling the function, whose pointer we fetched as described above. The `#if(cpp && mobile && !android)` are pre-processor flags that only let this code execute on certain targets. In this case, this is a roundabout way of saying "only do this on ios".

 
#### Part 2 - The C++ "Mapping"

The purpose of the C++ code is to establish a mapping beween Haxe and Objective-C.

Open up **project/common/ExternalInterface.cpp**. This file is the “glue” that connects Haxe to the underlying Objective-C code. (We've shortened the code to the essential bits for brevity.)

```
using namespace nativetest;

#ifdef IPHONE
void ios_alert(value title, value message)
{
    showSystemAlert(val_string(title), val_string(message));
}
DEFINE_PRIM(ios_alert, 2);
#endif
```

As you can see `ios_alert` shows up again. This time, it's a function. That’s where that function “pointer” is coming from in the Haxe file!

The `DEFINE_PRIM` part specifies how many parameters the function has.

`showSystemAlert()` is a direct call to a function in Objective-C. `val_string()` casts an arbitrary value to a String.

Now, let's look at the Objective-C part of the extension.

 
#### Part 3 - Objective-C

Objective-C is typically where the "meat" of an iOS extension is implemented.

You may have noticed that `ExternalInterface.cpp` imports NativeTest.h (peek at the top). If you open **project/include/NativeTest.h** and **project/iphone/NativeTest.mm**, you can see that this is plain old Objective-C.

```
namespace nativetest
{
    void showSystemAlert(const char *title, const char *message)
    {
        UIAlertView* alert= [[UIAlertView alloc] initWithTitle: [[NSString alloc]
                   initWithUTF8String:title]
                   message: [[NSString alloc] initWithUTF8String:message]
                                              delegate: NULL
                                              cancelButtonTitle: @"OK"
                                              otherButtonTitles: NULL];
        [alert show];
    }
}
```


#### Recap

To recap, an iOS extension effectively consists of 3 parts.

* Haxe source that fetches **function pointers** to native code and calls them.
* **ExternalInterface.cpp** provides those native calls and acts as the “glue” between Haxe and Objective-C.
* Objective-C (headers and .mm implementations) act as the implementation.

This is summarized in the following diagram.

![stencyl-levels-of-abstraction](http://static.stencyl.com/pedia2/chapter-d/LevelsOfAbstraction.png)

Now, we’ll look at Android. Thankfully, the story is quite similar.


## How to Create an Extension (Android)

> **Note:** This section walks through the test-native extension and explains how the system works. The test-native extension adds Alerts to iOS and Android games.
 
#### The 2 Parts
Every Android extension consists of 2 parts.

* Haxe code that your game calls. This Haxe code fetches function pointers via JNI in order to let your Haxe code call Java code.
* The Java code that does stuff in Android.
 
> In contrast to iOS, Android doesn't have that intermediate layer of C++ to worry about, but the Haxe part is a little bit more complex to compensate.
 
#### Part 1 - The Haxe Code

Just like, in the iOS case, the purpose of the Haxe portion of the extension is two fold.

* It exposes an API for your game (and blocks) to use.
* It fetches function pointers to native code and calls them.

Open up **NativeTest.hx** and find this line (~line 30).

```
androidAlert = nme.JNI.createStaticMethod("NativeTest", "showAlert", "(Ljava/lang/String;Ljava/lang/String;)V", true);
```

Here, we’re getting a "function pointer" to **showAlert()**, a Java function on the native side of things. The syntax is more complicated due to the use of [JNI](http://www.stencyl.com/help/view/jni-guide), the standard way of exposing native code to Java. Think of JNI as the rough equivalent to what ExternalInterface.cpp was doing for iOS, just in a more compact form.

Now, let's look right below (~line 33)

```
androidAlert([title, message]);
```

Here, we're calling the function, but the syntax is a little different. Instead of padding in the parameters directly, we're wrapping them inside an array.

> **Aside:** In some extensions, you may encounter an alternate approach where the array is pre-defined and passed in. For example, our Ads extension does this.

> ```
var args = new Array();
args.push(adwhirlCode);
args.push(position);
_init_func(args);
```
 

#### Part 2 - The Java Code

Now, peek at **project/android/NativeTest.java**.

```
public static void showAlert(final String title, final String message)
{
    [...]
}
```

There’s the underlying Java implementation for **showAlert()**. Notice how `showAlert()` takes two Strings as its arguments? That’s why that JNI call above looked the way it did.

```
androidAlert = nme.JNI.createStaticMethod("NativeTest", "showAlert", "(Ljava/lang/String;Ljava/lang/String;)V", true);
```


#### More on JNI

It turns out that **JNI is serving the same purpose that ExternalInterface.cpp did for iOS**. It’s the glue that connects native code to Haxe. It just happens at the Haxe level, rather than being in a separate file.

Getting the JNI syntax correct is a [topic in itself](http://www.stencyl.com/help/view/jni-guide/).

 
#### Recap
To recap, an Android extension consists of 2 parts.

* Haxe source that fetches function pointers to native code through JNI.
* The Java source files.

This is summarized in the following graphic.

![stencyl-levels-of-abstraction](http://static.stencyl.com/pedia2/chapter-d/AbstractionAndroid.png)

Now, we'll look at a few more topics.


## Including External Libraries

If you need to include an External Library, you can specify this inside include.nmml.

#### For iOS Extensions

```
<dependency if="ios" name="GameKit.framework"/>
```

In this example, we import the GameKit framework that's part of iOS.

#### For Android Extensions

```
<template if="android" path="template/android/libs" rename="libs"/>
```

In this example. we're telling the system to treat all files under template/android/libs as libraries. Just place all your .jar files under that path. See the Ads extension for an example.

## Building from the Command Line (iOS Only)

If you make a change on the iOS side of things (Android does not require this), you must compile the extension, which will output libraries to the “ndll” directory.

To do compile the extension, run the “build” script (located under the **project/** subdirectory of an extension). This compiles the iOS source and generates the .a libraries.

For example, if you are on a Mac and want to build the test-native extension, you would **cd** to [WORKSPACE]/engine-extensions/test-native/project and then run **./build**.

```
cd [WORKSPACE]/engine-extensions/test-native/project
./build
```

> **Tip:** If you get errors about Neko or Haxe not being recognized, re-read the Setup section of this doc.


## Editing project/Build.xml (iOS Only)

You must edit **project/Build.xml** before creating an iOS extension. **project/Build.xml** controls the name of the outputted library files and also serves to specify what .mm (Objective-C) files to include.

View existing examples for the exact fields to edit. You want to edit lines 21 and 52 in the “test-native” extension if you’re going off of that. The portions you need to edit are **bolded**.

Line 21 contains [file name="iphone/**NativeTest**.mm"/]

Line 52 contains [target id="NDLL" output="${name_prefix}**nativetest**${name_extra}" tool="linker" toolid="${ndll-tool}"]


## Sending Data back from Native Code to Haxe

A big part of Stencyl's ease of use comes in the form of [Events](Events). As a developer, it's more convenient to be **automatically notified** that something has happened, versus having to constantly check if that something has happened.

To implement Events for your extensions, you would need to know how to get the Objective-C (or Java) code to send notifications back to Haxe. For example, if the player completed an in-app purchase, you'd want to inform the player if the purchase succeeded and do something in-game in response to that.

[Learn how to implement Events for iOS / Android](http://www.stencyl.com/help/view/native-events/).
 

## Tips

#### Android (Java) - Getting the Main Class

If you need to refer to the “main class” or “Activity” in Android speak, call `GameActivity.getInstance()`.

```
import org.haxe.nme.GameActivity;
[...]
GameActivity.getInstance()
```

#### Android (Java) - Running code on UI Thread

By default, code runs on the main thread rather than the UI thread. This can pose problems if you need to change the UI (e.g. and can lead to crashes or unexpected behavior.

If you need to do alter the UI, like adding stuff to the screen, you do something much like `SwingUtilities.invokeLater()`:

```
GameActivity.getInstance().runOnUiThread(new Runnable()
{
    public void run()
    {
    }
});
```

> **Tip:** There’s another method calls **runOnHaxeThread** that does the opposite - guarantees running on the HaXe/main thread.
