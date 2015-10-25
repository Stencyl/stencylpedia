<table style="border:1px solid #cccccc;"><tr>
<td width="8" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Engine Extensions</h5>
<ul class="pedia-links">
<li><a href="http://www.stencyl.com/help/view/how-to-create-engine-extension/">The Basics</a></li>
<li><a href="http://www.stencyl.com/help/view/how-to-create-native-engine-extension/">iOS / Android</a></li>
<li><a href="http://www.stencyl.com/help/view/flash-extensions/">Flash</a></li>
</ul>
</td>
<td width="30" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Advanced Topics</h5>
<ul class="pedia-links">
<li><a href="http://www.stencyl.com/help/view/native-events/">Native Events</a></li>
<li><a href="http://www.stencyl.com/help/view/adding-blocks/">Custom Blocks</a></li>
<li><a href="http://static.stencyl.com/api/33/">API</a></li>
</ul>
</td>
<td width="30" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Toolset Extensions</h5>
<ul class="pedia-links">
<li><a href="http://www.stencyl.com/help/view/creating-extensions/">Main Guide</a></li>
<li><a href="http://api.stencyl.com/extensions/">API</a></li>
</ul>
</td>
</tr>
</table>


## Contents

* Introduction
* Setup
* Walkthrough
  * How to Create an Extension (iOS)
  * How to Create an Extension (Android)
  * External Libraries
  * Building from Command Line
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


## External Libraries

If you need to include an External Library, you can specify which libraries you wish to include inside **include.xml** (in some extensions, it's called **include.nmml**).

#### For iOS Extensions

In this example, we're importing a system framework (iAd) using the `<dependency>` tag. 

> **Aside:** `<ndll>` is used to import the compiled form of your iOS extension into any projects that use it.

```
<?xml version="1.0" encoding="utf-8"?>
<project>
    <section if="ios">
        <ndll name="ads"/>
        <dependency name="iAd.framework" />
    </section>
</project>
```

In this example, we're importing a 3rd party framework that is placed under the **frameworks/** subfolder of the extension. Note that the attribute name is **path**, rather than **name** in the example above.

```
<?xml version="1.0" encoding="utf-8"?>
<project>
    <section if="ios">
        <ndll name="ads"/>
        <dependency path="frameworks/Tapdaq.framework" />
    </section>
</project>
```

#### For Android Extensions

If your Android extension includes just Java source and no libraries, just specify the (relative) path to the folder containing the source. For example, if your Java source was located under **project/android**, you'd do this:

```
<?xml version="1.0" encoding="utf-8"?>
<extension>
  <section if="android">
    <java path="project/android"/>
  </section>
</extension>
```

If your Android extension needs to import libraries, it gets more complicated.

```
<?xml version="1.0" encoding="utf-8"?>
<extension>
  <section if="android">
    <dependency name="tapdaq" path="dependencies/tapdaq"/>
    <android extension="com.byrobin.tapdaq.TapdaqEx"/>
  </section>
</extension>
```

`<dependency>` specifies what folder contains the sources and libraries for your Android extension. In this example, those are located at **dependencies/tapdaq**. [(See Example)](https://github.com/byrobingames/tapdaq/tree/master/dependencies/tapdaq)

Within that folder are two subfolders and a few extra files. One subfolder is a **libs* folder that contains the tapdaq.jar library we want to import.

`<android>` is used to specify the path to the Java sources for the extension (the portion that *you* write). The value for the `extension` attribute is the package name for your sources. You place the sources under **[DEPENDENCY]/src/** where [DEPENDENCY] is the folder specified in the `<dependency>` tag.

#### OpenFL Reference

This [page](http://www.openfl.org/documentation/projects/project-files/xml-format/) covers the purpose of each `<dependency>`, `<ios>`, and `<android>` in more detail.  

Documentation is pretty thin for this, so our recommendation is to check out [existing extensions](https://github.com/byrobingames) for examples of how to lay the files in your extension. 


## Building from the Command Line (iOS Only)

If you make a change to an iOS extension, you must **compile** the extension, which will output libraries to its **ndll** directory. This step is not required for Android.

To compile the extension, **run the `build` script** (located under the **project/** subdirectory of an extension). This compiles the iOS source and generates the .a libraries.

![build-script](http://static.stencyl.com/pedia2/chapter-d/build-script.png)

For example, if you wanted to build the test-native extension, you would **cd** to **[WORKSPACE]/engine-extensions/test-native/project** and then run **./build**.

```
cd [WORKSPACE]/engine-extensions/test-native/project
./build
```

> **Tip:** If you get errors about Neko or Haxe not being recognized, re-read the Setup section of this doc.


## Editing project/Build.xml (iOS only)

You must edit **project/Build.xml** before compiling your iOS extension. **project/Build.xml** controls the name of the outputted library files and also serves to specify what .mm (Objective-C) files to include (and compile).

Our recommendation is to view existing examples to figure out what to edit - it's a lot easier than trying to type it up from scratch.

For example, take [this sample](https://github.com/byrobingames/tapdaq/blob/master/project/Build.xml) from an extension for Tapdaq ads.

Then, you'd do two things:

1. Search for **mm**. This is where you'd specify all the .mm source files for the extension.

  ```
  <file name="ios/TapdaqEx.mm"/>
  ```

2. Search for `tapdaq` and replace each instance with the name of your extension (in lower case).

  * Line 56 contains `<target id="NDLL" output="${name_prefix}tapdaq${name_extra}" tool="linker" toolid="${ndll-tool}">`
  * Line 65 contains `<vflag name="-framework" value="Tapdaq" />`


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
