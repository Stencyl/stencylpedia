## Why does this happen?

Java operates by allocating a chunk of memory for the application to use before the app launches - it can't be set at runtime. There is an upper limit to this memory. If you go too high, Stencyl may lock up.

So why not just set the limit very high? It causes weaker machines with less memory to fail to open the app at all.

Although we are working to reduce memory usage and plug leaks, there are large games for which having the higher memory usage is useful.

> **Common Misconception:** The 90% memory warning has **nothing to do with how much RAM your computer has**. You could have 128 GB of RAM and still hit this since Java's upper cap sits around 4 GB and on some systems, may be as low as 2 GB.
 

## How to Safely Suppress This Warning (Windows)

(REDO THIS SECTION)

Starting with Stencyl 3.4, Java 8 comes bundled with Stencyl and defaults to 1 GB memory usage.

To change the 1 GB to something higher, download the following script and save it as **Stencyl.bat** - then, place it into your Stencyl directory.

Now, double-click the script to start Stencyl from now on.

> **Note 1:** If Stencyl fails to launch, edit the file and change the **2048** to something smaller, such as 2048 or 3072.

> **Note 2:**Note: The -Xmx setting may be overridden by the _JAVA_OPTIONS environment variable. See [this tutorial](https://www.youtube.com/watch?v=R3Hj83J0ekk) for how to delete the variable.
 
 
## How to Safely Suppress This Warning (Mac)

1) Right-click the Stencyl.app bundle and "Show Package Contents".

2) Edit Contents/MacOS/Stencyl.

3) Find the line that starts with **-Xmx1536m** and change the number to a higher number such as 4096 - the 1536 represents MB.

> **Note:** If Stencyl fails to launch after you make an edit, your number is too high. Try something smaller.


## How to Safely Suppress This Warning (Linux)

1) Edit the Stencyl shell script.

2) Change the part that looks like **-Xmx1024m** to a higher number - the 1024 represents MB.

> **Note:** If Stencyl fails to launch after you make an edit, your number is too high. Try something smaller.
