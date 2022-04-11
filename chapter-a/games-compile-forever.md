
> **Note:** As of Stencyl 3.2, the app catches all compile errors, so you will be informed if something went wrong. [Ask for help] on the forums.

> We're leaving this article up for those using older versions of Stencyl


## What to Do

Sometimes, a game will appear to take a long time to compile. To take the guesswork out of this, turn on the log viewer to see what's happening.

1) Turn on the Log Viewer. (It's in the top toolbar next to Settings)

2) Run the game again.

3) Watch the Log Viewer as the game builds. As long as new lines continue showing up, you're fine. If errors show up, something went wrong, and you should [ask for help](https://community.stencyl.com/index.php/board,3.0.html) on the forums.


## FAQ: Why do desktop and mobile games take a long time to run?

Stencyl is based around Haxe. In order to build mobile and desktop apps, Haxe is translated to C++ which in turn is compiled to machine code.

Although the Stencyl engine is compact, the Haxe code it depends on is large and has to be re-compiled for each new game. We don't think this is optimal, but that's how it is right now. On a fast computer, you can expect a 5-7 minute compile time. On a slower one, somewhere around 15-20 minutes is reasonable to expect.

Mercifully, this is only the case the first time you run a game on a given platform. Second runs and onwards are much faster. Flash games are not affected by this quirk.
