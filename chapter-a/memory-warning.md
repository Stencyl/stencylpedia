## Why does this happen?

The Java runtime reserves a chunk of memory for Stencyl to use before launching -- it can't be raised after the fact. If you exceed this limit, Stencyl locks up.

So why not just set the limit very high? It causes machines with less memory to fail to launch Stencyl at all.

Although we are working to reduce memory usage and plug leaks, there are large games for which having the higher memory usage is useful. This guide explains how you can raise the limit.

> **Common Misconception:** The 90% memory warning has **nothing to do with how much RAM your computer has**. You could have 128 GB of RAM and still hit this since Java's upper cap sits around 4 GB and on some systems, may be as low as 2 GB.

> **Note:** If Stencyl fails to launch after you make one of the below edits, your number is too high. Try something smaller.

## How to Raise the Memory Limit (All systems, using script launchers)

1. Open the appropriate launcher for your operating system in a text editor:
   - `Windows`: `Stencyl-windows.bat`
   - `macOS`: `Stencyl-macos.command`
   - `Linux`: `launcher/Stencyl-linux`

2. Find the place where the amount of memory Stencyl uses is specified. It's near the top.
   - Windows: `:: set "_MAX_MEM_=4096"`
   - macOS/Linux: `# _MAX_MEM_="4096"`
   
3. Uncomment that line (remove the `::` or `#` at the start), and increase the number on the right. Then save the file.

## How to Raise the Memory Limit (Windows, using Stencyl.exe)

1. Create a new file called `Stencyl.l4j.ini`.

2. Add the following line to it, setting the number on the right to the desired number of MB.
   ```
   -Xmx4096m
   ```

## How to Raise the Memory Limit (macOS, using Stencyl.app)

1. Right-click the Stencyl.app bundle and pick **Show Package Contents**. 

2. Using a text editor, open up **Contents/MacOS/Stencyl**.

3. Find the place where the amount of memory Stencyl uses is specified. It's near the top: `# _MAX_MEM_="4096"`. Remove the comment marker on the left (`#`) and change the number on the right.

4. Save the file, then relaunch Stencyl. (If your Mac complains that the app is "damaged", go to **System Preferences > Security and Privacy** and allow apps to be downloaded from **Anywhere**.)
