## Why does this happen?

The Java runtime reserves a chunk of memory for Stencyl to use before launching -- it can't be raised after the fact. If you exceed this limit, Stencyl locks up.

So why not just set the limit very high? It causes machines with less memory to fail to launch Stencyl at all.

Although we are working to reduce memory usage and plug leaks, there are large games for which having the higher memory usage is useful. This guide explains how you can raise the limit.

> **Common Misconception:** The 90% memory warning has **nothing to do with how much RAM your computer has**. You could have 128 GB of RAM and still hit this since Java's upper cap sits around 4 GB and on some systems, may be as low as 2 GB.
 

## How to Raise the Memory Limit (Windows)

1. [Install](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) the 64-bit version (x64) of Java 8 to your computer.

2. Download one of the following scripts and place it into your Stencyl installation directory. (For best results, pick 1-2 tiers below what you have -- e.g. If you have 4 GB, choose the 2 or 3 GB option.)

* [2 GB](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-a/stencyl-2gb.bat)
* [3 GB](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-a/stencyl-3gb.bat)
* [4 GB](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-a/stencyl-4gb.bat)
* [6 GB](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-a/stencyl-6gb.bat)
* [8 GB](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-a/stencyl-8gb.bat)

3. Double-click the script to launch Stencyl from now on.  

> **Note 1:** If Stencyl fails to launch, choose a script with a lower amount of memory.

> **Note 2:**Note: The -Xmx setting in the script may be overridden by the _JAVA_OPTIONS environment variable. See [this tutorial](https://www.youtube.com/watch?v=R3Hj83J0ekk) for how to delete the variable.
 
 
## How to Raise the Memory Limit (Mac)

1. Right-click the Stencyl.app bundle and pick **Show Package Contents**. 

2. Using a text editor, open up **Contents/MacOS/Stencyl**.

3. Search for **-Xmx1536m** and change the number to something higher such as 4096 - the 1536 represents MB (1.5 GB).

4. Save the file, then relaunch Stencyl. (If your Mac complains that the app is "damaged", go to **System Preferences > Security and Privacy** and allow apps to be downloaded from **Anywhere**.)

> **Note:** If Stencyl fails to launch after you make an edit, your number is too high. Try something smaller such as 2048 or 3072.


## How to Raise the Memory Limit (Linux)

1. Edit the Stencyl shell script.

2. Change the part that looks like **-Xmx1024m** to a higher number - the 1024 represents MB.

> **Note:** If Stencyl fails to launch after you make an edit, your number is too high. Try something smaller such as 2048 or 3072.
