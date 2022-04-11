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
* Prerequisites
* How To: Creating a Flash Extension
* Example: Base 64 Encoding/Decoding

## Introduction

Creating a Flash extension is necessary if you wish to **import a custom SWF or SWC**. For example, a common use case is to import a sponsor's API.


## Prerequisites

Please read our main [extensions guide](https://www.stencyl.com/help/view/how-to-create-engine-extension/) before reading this one. It covers the basic concepts behind engine extensions.


## How To: Creating a Flash Extension

> Assume that **[WORKSPACE]** refers to the path to your Stencyl workspace (find it using **Debug > View > View Workspace Folder**).

#### Step 1: Copy the Template
Under [WORKSPACE]/engine-extensions/, copy the "test-flash" extension to a new folder. Give that folder a new name.

#### Step 2: Copy in the Flash library
Replace **library.swf** with the SWF you wish to import.

If you have a SWC library, you need to extract the SWF that resides inside of it. To do this, rename the SWC to a ZIP and extract its contents. The SWF will be inside. Use that.

#### Step 3: The Rest

1. Edit **info.txt** with your extension's details.

2. Replace **icon.png** with your own 32 x 32 icon.

3. Rename and edit **TestFlash.hx** to meet your needs (e.g. you want to build an API around the library). If you don't want or need a source file, you can safely delete it and call the SWF's functions directly from the game.

4. (Optional) Edit blocks.xml if you want to add some custom blocks that expose the Flash library's functionality.

That's it. Once your extension is ready, open a game, enable the extension, and test the game. If you've done everything correctly, the extension will work.


## Example: Base 64 Encoding/Decoding

The test-flash extension is built around a base64 encoding/decoding library. If you open up TestFlash.hx, you'll find the following source.

```
import by.blooddy.crypto.Base64;
import flash.utils.ByteArray;

class TestFlash
{
    public static function base64Encode(s:String)
	  {
		    var byteArray = new ByteArray();
		    byteArray.writeMultiByte(s, "iso-8859-1");
		    trace(Base64.encode(byteArray, true));
	  }
}
```

The big idea is that **Haxe can directly make calls to functions in the SWF / SWC** you've imported. This is pretty powerful and makes it relatively easy to integrate sponsors' APIs.

