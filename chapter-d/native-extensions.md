> **Extending Stencyl**

> Engine ([Basics](http://www.stencyl.com/help/view/how-to-create-engine-extension/) - [iOS & Android](http://www.stencyl.com/help/view/how-to-create-native-engine-extension/) - [Flash](http://www.stencyl.com/help/view/flash-extensions/) - [Blocks](http://www.stencyl.com/help/view/adding-blocks/) - [API](http://static.stencyl.com/api/33/))

> Toolset ([Extensions](http://www.stencyl.com/help/view/creating-extensions/) - [API](http://api.stencyl.com/extensions/))


## Contents

* Introduction
* Setup
* Building from Command Line
* Including External Libraries
* Walkthrough
  * How to Create an Extension (iOS)
  * How to Create an Extension (Android)
  * Editing Build.xml
  * Sending Data back from Native to Haxe
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


## Building from the Command Line (iOS Only)

If you make a change on the iOS side of things (Android does not require this), you must compile the extension, which will output libraries to the “ndll” directory.

To do compile the extension, run the “build” script (located under the **project/** subdirectory of an extension). This compiles the iOS source and generates the .a libraries.

For example, if you are on a Mac and want to build the test-native extension, you would **cd** to [WORKSPACE]/engine-extensions/test-native/project and then run **./build**.

```
cd [WORKSPACE]/engine-extensions/test-native/project
./build
```

> **Tip:** If you get errors about Neko or Haxe not being recognized, re-read the Setup section of this doc.


## How To: Including External Libraries

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

`showSystemAlert()` is a direct call to a function in Objective-C. `val_string()` is a way of casting an arbitrary value to a String.

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

That wasn’t too bad, was it? To recap, an iOS extension effectively consists of 3 parts.

* Haxe source that fetches **function pointers** to native code and calls them.
* **ExternalInterface.cpp** provides those native calls and acts as the “glue” between Haxe and Objective-C.
* Objective-C (headers and .mm implementations) act as the implementation.

This is summarized in the following diagram.

[TODO]

Now, we’ll look at Android. Thankfully, the story is quite similar.


## How to Create an Extension (Android)

Note: This section walks through the test-native extension and explains how the system works. The test-native extension adds Alerts to iOS and Android games.
 
The 2 Parts
Every Android extension consists of 2 parts.

Haxe code that your game calls. This Haxe code fetches function pointers via JNI in order to let your Haxe code call Java code.
The Java code that does stuff in Android.
 
Part 1 - The Haxe Code
Open up NativeTest.hx. Observe that we’re getting a function “pointer” to showAlert(), a Java function on the native side of things.

androidAlert = nme.JNI.createStaticMethod("NativeTest", "showAlert", "(Ljava/lang/String;Ljava/lang/String;)V", true);
This is a little bit more complicated than the iOS case because this involves JNI, a commonly used technology for exposing native code to Java.

Don’t get bogged down in the details - accept for now that we’re getting a function “pointer” and calling it. Think of JNI as the rough equivalent to what ExternalInterface.cpp was doing for iOS, just in a more compact form.

androidAlert([title, message]);
Here, the syntax is a little different. We’re passing in an array with the parameters, rather then the parameters individually.

Aside: In some extensions, you may encounter an alternate approach where the array is pre-defined and passed in. For example, our Ads extension does this.

var args = new Array();
args.push(adwhirlCode);
args.push(position);
_init_func(args);
 
Part 2 - The Java Code
Now, peek at project/android/NativeTest.java.

public static void showAlert(final String title, final String message)
{
    [...]
}
There’s the underlying Java implementation. Recognize the showAlert function from the prior section? See that it takes two Strings are arguments? That’s why that JNI call above looked the way it did.

androidAlert = nme.JNI.createStaticMethod("NativeTest", "showAlert", "(Ljava/lang/String;Ljava/lang/String;)V", true);
 

More on JNI
It turns out that JNI is serving the same purpose that ExternalInterface.cpp did for iOS. It’s the glue that connects native code to Haxe. It just happens at the Haxe level, rather than being in a separate file.

Getting the JNI syntax correct is a topic in itself. If you'd like to learn more about it, we've written a separate article about it.

 
Recap
To recap, an Android extension consists of 2 parts.

Haxe source that fetches function pointers to native code through JNI.
The Java source files.
Now, we'll look at a few more topics.


Editing project/Build.xml (iOS Only)

You must edit project/Build.xml before creating an iOS extension. project/Build.xml controls the name of the outputted library files and also serves to specify what .mm (iOS implementation) files to include.

View existing examples for the exact fields to edit. You want to edit lines 21 and 52 in the “test-native” extension if you’re going off of that.

Line 21 contains [file name="iphone/NativeTest.mm"/]

Line 52 contains [target id="NDLL" output="${name_prefix}nativetest${name_extra}" tool="linker" toolid="${ndll-tool}"]

The portions you need to edit are emphasized like this.

Sending Data back from Native Code to Haxe

Note: This is tricky and assumes complete understanding of the prior topics. It's highly recommended to refer to the Purchases extension for an example.
What if you do something on the Objective-C or Java side of things and want that code to send data or notifications back to Haxe? For example, if you complete a purchase, you want to inform the player about it. How is that achieved?

In a gist, it involves the following concepts on iOS.

Setting a function pointer from Haxe to ExternalInterface.cpp to set up a function that will get called back, with the desired data passed in as a parameter. In other words, it's a just setting up a callback. Look for set_event_handle()
Packaging up the data to send inside ExternalInterface.cpp, using a key-value store and then sending it. Look for send_purchase_event()
To reiterate, this is an advanced use case where it’s best to view the existing source for our Purchases extension. It sounds a lot more confusing than it really is, and there’s no better explanation than viewing the source for yourself.

Note: Currently, only iOS extensions send data back. No extensions have been written so far that involve Java/Android sending data back to Haxe, but I've roughly described the process in this forum post.
 

Tips

Java - Getting the Main Class
If you need to refer to the “main class” or “Activity” in Android speak, call:

import org.haxe.nme.GameActivity;
[...]
GameActivity.getInstance()

Java - Running code on UI Thread
Note that code runs on the main, not UI thread. If you need to do UI things, like adding stuff to the screen, you do something much like SwingUtilities.invokeLater, except that it’s called:

GameActivity.getInstance().runOnUiThread(new Runnable()
{
    public void run()
    {
    }
});
Tip: There’s another method calls runOnHaxeThread that does the opposite - guarantees running on the HaXe/main thread.
