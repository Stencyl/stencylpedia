<table style="border:1px solid #cccccc;"><tr>
<td width="8" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Engine Extensions</h5>
<ul class="pedia-links">
<li><a href="https://www.stencyl.com/help/view/how-to-create-engine-extension/">The Basics</a></li>
<li><a href="https://www.stencyl.com/help/view/how-to-create-native-engine-extension/">iOS / Android</a></li>
<li><a href="https://www.stencyl.com/help/view/flash-extensions/">Flash</a></li>
</ul>
</td>
<td width="30" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Advanced Topics</h5>
<ul class="pedia-links">
<li><a href="https://www.stencyl.com/help/view/native-events/">Native Events</a></li>
<li><a href="https://www.stencyl.com/help/view/adding-blocks/">Custom Blocks</a></li>
<li><a href="https://static.stencyl.com/api/33/">API</a></li>
</ul>
</td>
<td width="30" style="border:0px;"></td>
<td width="180" valign="top" style="border:0px;">
<h5>Toolset Extensions</h5>
<ul class="pedia-links">
<li><a href="https://www.stencyl.com/help/view/creating-extensions/">Main Guide</a></li>
<li><a href="http://api.stencyl.com/extensions/">API</a></li>
</ul>
</td>
</tr>
</table>


## Contents

* Introduction
* Walkthrough
* JNI Types / Classes
* Static vs. Non-Static Methods
* Shortcut - Autogenerating JNI
 

## Introduction

JNI bindings let Haxe code call Java code. The JNI syntax can be confusing to understand. This document explains the syntax and offers an alternative to writing it out by hand.

> **Note:** This is a supplement to our [Native Extensions](https://www.stencyl.com/help/view/how-to-create-native-engine-extension/) guide. It's rough and intended for advanced users.


## Walkthrough

> For this document, we'll be referring to **NativeTest.hx** within the **test-native** extension.

JNI is used to grab the "pointers" to Java code from Haxe. Let's peek at **NativeTest.hx**. Look for the following code.

```
androidAlert = nme.JNI.createStaticMethod("NativeTest", "showAlert", "(Ljava/lang/String;Ljava/lang/String;)V", true);
```

* First parameter is the fully qualified name of the class. For example, **com/mysite/MyClass**. Packages use / rather than . as the delimiter. To make your life easier, it's best to not use packages at all.

* Second parameter is the method name.

* Third parameter is the JNI syntax for the arguments list and return value. It goes like this:

   ```
   (ARGUMENTS)RETURNVALUE
   ```
  * Return Value Format
    * int = I
    * void = V
    * boolean = Z

* Fourth parameter is always `true`.


## JNI Types / Classes

Any class, including String is the fully qualified name, using forward slashes and suffixed by ;
For example, java/lang/String;

Multiple arguments are also separated by semicolons ;

It is only possible to pass in and return primitives, Strings and Arrays thereof. Specifically...

* void
* String
* Array
* bool
* byte
* char
* short
* int
* long
* float
* double

If the function has 0 arguments, then you include the parens but put nothing in between. For example, if your function takes no arguments and returns `void`, it would come out as `()V`.

> **Tip:** If you need to toss around binary data (took an image with the camera and pass back to Haxe?), use Base64 to encode and decode.


## Static vs. Non-Static Methods

Is it possible to use JNI with a regular (non-static) method? It probably is, but we haven't attempted this and haven't seen cases of this. We recommend sticking to static methods if you can.


## Shortcut - Autogenerating JNI

There is a way to auto-generate the JNI syntax using a script. To make this work, you must add "lime" to your path. (If you haven't installed it separately, that is.)

lime is located under [STENCYL_INSTALL]/plaf/haxe/lime (or lime.bat)

1. cd to the .class file for your Java source. You can find it at **[WORKSPACE]/games-generated/[YOUR GAME]/Export/android/bin/bin/classes/**

2. Run the following command. **Do not omit the period**.

  ```
  lime generate -java-externs [FILENAME_OF_CLASS] .
  ```

3. This will spit out a .hx file, which will contain the JNI calls you desire.
