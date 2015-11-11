### Changelog ###

November 10, 2015

 - (b8825) Remove lang/br (incorrect lang code and very incomplete)

November 09, 2015
 - (b8820) Fix: error dialog for parsing code mode attribute definitions
 - (b8818) Fix: name instead of internal name in remove attribute dialog
 - (b8814) Fix: Ask user to confirm before deleting Android Keystore
 - (b8813) Fix: resize yes/no dialogs to fit text
 - (b8809) Fix: use fallback icon for fonts that cannot display char 'A'
 - (b8808) Fix: use the actual fonts for the default font previews (Newspaper, Sans Serif, and Typewriter)
 - (b8807) Fix: only show displayable chars in font preview
 - (b8806) Fix: error when selecting custom font without choosing one
 - (b8805) Fix: warn and fall back if font contains no displayable chars
 - (b8804) Fix: misleading preview image if font has no displayable chars
 - (b8802) enable 3x scale by default
 - (b8801) Fix: catch exceptions during parsing of engine extension definitions
 - (b8799) success/fail dialogs for Run -> Clean Project

November 05, 2015
 - (b8796) Fix: Can't drag embedded blocks out of wrappers.

November 04, 2015
 - (b8793) Fix: clarify font character sets in dropdown
 - (b8791) Fix: warn instead of erroring out for attached blocks in extensions
 - (b8787) Fix: Mac OS X sometimes says that we're an unregistered developer (and won't let Stencyl launch)
 - (b8786) Fix: FileNotFoundException when copying freeform code
 - (b8785) Fix: use NIO to avoid "Failed to copy full contents" in SnippetsWriter
 - (b8784) Fix: warning "Could not add block for tag toggle-flxpause to menu."

November 03, 2015
 - (b8783) Fix: Can drag blocks into design mode work area without an event.
 - (b8782) Fix: groups with return block not snapping into top of event wrapper.

November 02, 2015
 - (b8781) Fix: "Attribute doesn't exist" warning for unassigned values
 - (b8780) Fix: uncaught exception when taking a screenshot of a behavior without events
 - (b8778) Fix: Actors and Players collide with Tiles even when not set to collide
 - (b8773) Fix: cannot export actor type that has no animation
 - (b8772) Fix: parsing numbers in locales using "," as decimal point

[Block Guide](http://www.stencyl.com/blocks/)
- Brand new and rewritten from scratch .
- EVERY block in the toolset is documented.
- Right-click a block > View Help will open the block guide and highlight that block's entry for you.

November 1, 2015
- Full Screen (Interstitial) Ads for iOS and Android ([Feedback Wanted](http://community.stencyl.com/index.php/topic,44958.0.html))
- Events for Android Ads ([Feedback Wanted](http://community.stencyl.com/index.php/topic,44958.0.html))

October 31, 2015
 - (b8769) Add anchors (using Definition.tag) for [block] > View Help.
 - (b8768) Hook up block help url's to new block reference.

October 30, 2015
 - (b8762) Allow base palette and event lists to be overwritten with user-defined lists.

October 28, 2015
 - (b8761) Fix actors recreated have shorter first frames of animation
 - Fix: error "Array<Int> should be Array<Float>" when building HTML5 games

October 27, 2015
 - (b8760) Fix: Exporting a sound only exports MP3
 - (b8759) Fix: internal Java error when highlighting a block on Linux
 - (b8758) Fix: "exit game" block not working on Flash

October 24, 2015
- (b8748) Fixed ConcurrentModificationExceptions in extension repo browser, don't show header for empty extension lists.
- (b8747) Expand Deisgn Mode EditArea by dragging blocks near the edge.
- (b8746) Fix block drag behavior on multiple monitor setups.

October 21, 2015
- (b8745) Fixed actor customization title not filling horizontal space.

October 17, 2015
 - (b8744) Remove misleading "real world gravity" hint

October 14, 2015
 - (b8741) Fix: "Games" counter doesn't decrease when deleting games
 - (b8740) Fix: broken "copy of image" block

October 13, 2015
 - (b8739) Broken toolset extensions prevent Stencyl from opening.

October 12, 2015
- (b8738) Android Soft Keyboard support

October 10, 2015
- Follow up work on extensions framework.

_**(Weekly Release - b8734 - October 10th)**_

October 08, 2015
- (b8734) Final touches and fixes to extensions framework.

October 08, 2015
-  (b8733) Update openfl (3.3.8) and lime (2.6.8).
-  (b8732) Fix: Re-sign the Mac launcher
-  (b8731) Fix: add Java 8 version check on Mac

October 07, 2015
- (b8730) Finished work on extension repositories and dependencies.
- (b8723) Fix: Random error upon opening game (get/set attribute)
- (b8722) Fix: Improvements to neko installer (for El Capitan)

October 06, 2015
- (b8719) Fix: Add UIRequiresFullScreen to Info.plist template. This fixes an issue with App Store submissions with the latest Xcode.

October 04, 2015
- (b8718) Fix: Issue with workspace resetting and missing OS/Java info.

October 03, 2015
- (b8716) Fix: Can't create/remove game attributes when multiple resources are open
- (b8715) Fix: Fixes for supporting Xcode 7 / iOS 9
- (b8714) Fix: Stencyl stops responding when clicked inside log viewer

October 01, 2015
 - (b8711) Extension repositories for downloads and updates.
 - (b8710) Fix: push/twist blocks do not work with magnitude <= 0
 - (b8709) Fix: Windows 8.1 and 10 Flash log location
 - (b8708) Fix: Windows and OS X version detection

September 30, 2015
 - (b8705) Install neko when running on OSX El Capitan.

September 29, 2015
 - (b8698) Fix: Move to Folder grayed out
 - (b8696) Fix: atlas settings are not saved

September 26, 2015
- (b8693) Fix: regression in [Actor Group] chooser in design mode.
- (b8691) Fix: Tile collision shapes stopped showing up in Tileset Editor
- (b8690) Fix: Bitmap Font image importing

September 25, 2015
- (b8682) Fix: Fix up rendering issues on Game Settings page on Mac
 - (b8681) Fix: error in refreshing inventory after deleting scene
 - (b8680) Fix: ConcurrentModificationException in SceneWriter
 - (b8679) show option to test HTML5 (experimental)

_**(Weekly Release - b8678 - September 24)**_

September 23, 2015 (b8678)
- Fix: Palette Search Bar is broken
- Fix: Searching for a block, then switching event throws error

September 22, 2015 (b8676)
- Fix: RasterFormatException if characters are defined outside of bitmap font image
- Fix: "ArrayIndexOutOfBoundsException: null" without stack trace on Linux with Java 8

September 21, 2015
- Fix up toolbar color inconsistency on Mac + Java 1.8.
- Fix up anti-aliasing on buttons in top toolbar on Mac + Java 1.8.

September 16, 2015
 - (b8672) Fix bug iterating over files on Mac when looking for xcode.

September 10, 2015
-  (b8671) Fixed gravity not resetting on recycle

_**(Weekly Release - b8670 - September 9)**_

September 07, 2015
(b8670)
- Block palette and events are stored as xml. Later we'll let them be completely customized or replaced.
- Engine extensions can be added without closing game.
- All changes to palette are dynamic. Don't need to refresh behavior after adding game attributes, for example.
- Context hinting: places where a block will probably cause an error will be highlighted in red when placing the block.

September 05, 2015
 - (b8658) Fix: regression: can't select animations other than the first
 - (b8657) Use bundled Java 8 JRE in .bat script

September 03, 2015
 - (b8648) Fix: regression: StackOverflowError in Layer.getActorsAtPoint
 
September 3, 2015
- Fix: don't show generic error dialog if another error dialog has been shown already
- Fix: catch generic Android build failures

September 2, 2015
- Fix: Fixed sync'd anims repeating too early.
- Fix: Exporting sprite uses old format, can't import back in.
- Fix: Updated NanoHTTPD to fix server-caused errors when running html5 games.
- Fix: NPE when looking for Xcode.

Stencyl requires Java 8 from now on. A Java 8 JRE comes bundled on Windows and Linux. On Mac, you can get the latest Java from Oracle: https://www.java.com/en/download/

_**(Weekly Release - b8627 - September 1)**_

September 1, 2015
- Add Block Code Viewer.
- Add onGameBuild hook for extensions. It wasn't being called anywhere before.
- Fix: Delete resource dialog popping up when it shouldn't.
- Fix: Resource opening upon double click, Windows + Java 8
- Fix: Error (in log) if XMLGroup.list is empty
- Fix: ImageUtil.ensureSize for non-BufferedImages
- Fix: Remove extra semicolon from custom block's sayToScene.

August 30, 2015
- Major speedup to Haxe code generation time.
- Fix: NullPointerException when adding favorite blocks
- Fix: Unexpected error when adding polygon shape to animation with no frames
- Fix: scaled fonts not being generated after a new scale is enabled
- Fix: Error 1009 when loading a null map
- Add support for filters in html5

August 27, 2015
- [Added beta support for html5 back in](http://community.stencyl.com/index.php/topic,43557.0.html) (thanks to letmethink)
- Lime -> 2.6.1, Openfl -> 3.3.2.

August 26, 2015
- Show splash screen earlier during startup sequence
- Not part of Stencyl, but the [Virtual Joysticks extension has been completely rewritten](http://community.stencyl.com/index.php/topic,29026.45.html). Please help us test it out, so we can replace the built in support with this much better version.

August 25, 2015
- Preview code shows same line numbers as generated haxe files.

August 24, 2015
- Fixed sound length blocks for desktop and iOS.

August 23, 2015
- Telemetry support. Download hxscout to take advantage of it.
- Fixed scale to fit (fill) and scale to fit (letterbox) modes for different game resolutions.

August 22, 2015
- Upgrade hxcpp to development release, openfl to 3.3.1, lime to 2.6.0.
- Refreshed [Stencyl/stencyl-engine](https://github.com/Stencyl/stencyl-engine) on github. Feel free to contribute!

August 18, 2015
- Fix regression: Graphics grow when editing frame

_**(Weekly Release - b8529 - August 17)**_

- Allow creating a tileset without importing image.
- Set a tileset to be 1 across x 1 down if no image was selected.
- Don't attempt to load images of a tileset that hasn't been created yet.
- Fix: can't edit frames if import scale is set to an unchecked project scale
- Trimmed down size of Windows distribution.
- Allow games to compile when path is lost on subprocesses in OS X El Capitan.
- Fixed some exceptions related to deleting tiles and trying to open/delete when no resource is selected.
- Fix: Don't throw exception when pasting non-design mode data in events pane.
- Fix: Show Play/Pause instead of "<0>" in scene editor animations button.
- Fix: Don't show Mac OS X version warning for 10.10.5.
- Don't allow using "none" as a font's main color.

_**(Quick Release - b8502 - August 12 - addresses regressions in weekly)**_

- Fixed regression: broken flash compile, allow swipe on desktop targets.
- Fix: Missing language strings

_**(Quick Release - b8500 - August 12 - addresses regressions in weekly)**_

August 11, 2015
- Fixed regression: Can't create new tileset
- Fixed regression: Android build freezing on "adb devices"
- Fixed regression: Mobile swipe gesture not working

_**(Weekly Release - b8495)**_

August 8, 2015
- Fix: uncaught exceptions when entering 0 into tile width/height fields when creating a new tileset
- Fix: cannot open game if tileset image is missing (fallback to empty image)
- Fix: catch "Agreeing to the Xcode/iOS license requires admin privileges"

August 7, 2015
- Fix: uncaught exception when removing actor group
- Fix: Flash log location changed on Windows 10 (?)

August 5, 2015
- Fix: Don't allow a game name to become empty due to illegal characters when importing a game.

_**(Weekly Release - b8471)**_

August 2, 2015
- Fix: Parallax Background not animating

July 30, 2015
- Fix: Sliding Transitions not using color backgrounds when active

July 28, 2015
- Fix: Catch error "max_string_size reached"

July 27, 2015
- Change JRE bundled with linux 64-bit version from 32-bit JRE to 64-bit JRE.
- Allow grid color to be specified in Scene Designer.
- Improved xcode detection.

July 26, 2015
- [Fix] iOS version code incrementing automatically, ignoring value in game settings.

July 25, 2015
- Updated packaged haxe, haxelib, openfl, lime, hxcpp to latest versions.
- [Fix] Invalid Operation (+) when testing without HOMEDRIVE or HOMEPATH variables set on Windows.
- [Fix] Simple Physics not giving collisions to tiles with Square collision.
- [Fix] Remove all items from map block not working.

July 24, 2015
- Added Stencyl.bat file to windows builds by default with same vm arguments used in the .exe.

July 19, 2015
- [Fix] NPE in Scene Designer when trying to draw rectangle with no brush.

July 18, 2015
- [Fix] Controls not saved in behavior settings.
- [Fix] NPE when mouse release occurs before mouse press on Tileset Palette.
- [Fix] When blank images are created because animations can't be loaded, save them out right away to prevent later errors.

July 17, 2015
- Fixed compilation issues on Linux 32 bit release.
- Warn user about having parenthesis in install path on Mac/Linux.

July 16, 2015
- [Fix] Trying to import a large gif ( > 4096 px ) causes an exception.
- [Fix] Don't attempt to draw an editable background with no image.
- [Fix] NPE when updating sprites before atlas manager is initialized.
- [Fix] NPE upon new game creation when xcode isn't detected on Mac.
- Added rectangle tool to Scene Designer.

July 8, 2015
- [Fix] Getting null instead of normal blendmode when updating old games.
- [Fix] Can't save/compile game due to file access conflicts.

July 5, 2015
- [Fix] iAds - ad shows after it was hidden

June 29, 2015
- Add 3x support to the engine
- Fix: generic error dialog for android compilation errors
- Fix: catch error if game format version cannot be parsed

June 22, 2015
- Fix: trying to load OSX metadata file as an extension
- Fix: behavior attributes resetting
- Fix: catch engine compilation errors
- Fix: error loading/saving maps

June 21, 2015
- Fix: cannot upgrade kit made with earlier version (blendmode is null)
- Fix: a preference from 3.3 causes uncaught exception when opening earlier version
- Fix: wrong image dimension written when exporting actors (revert multi-row sprites)
- Fix: Show warning if game cannot be written because destination file is in use

June 20, 2015
- Update: Rewrote our iAd support from scratch. [Please help us test it.](http://community.stencyl.com/index.php/topic,41938.0.html)
- Fix: uncaught exception when opening game made with 3.3.1 in an earlier version

June 19, 2015
- Fix: game doesn't open if actor has a missing sprite
- Fix: exception on mobile page if no Xcode is installed

June 13, 2015
- Fix: Update Windows Launcher with VM arguments to prevent stackless ArrayIndexOutOfBounds exception
- Log all error and warning dialog messages

June 11, 2015
- Fix: uncaught exception if attribute dropdown data contains entry not in the form of "name=value"
- Fix: fall back to empty sprite if actor sprite is missing

June 9, 2015
- Fix: catch "Invalid Keystore Format" error
- Fix: catch ".hxcpp_config.xml (Access Is Denied)" error
- Fix: catch engine extension compilation errors
- Fix: catch layer-I or layer-II mp3 error
- Add warning if engine extension compatibility is set to an unexpected value
- Allow "desktop" compatibility value
- Fix: choosing "cancel" on game format prompt doesn't close the game

May 31, 2015
- Add prompt for game format upgrade.

May 20, 2015
- Upgrades and fixes to Google Play Games support.

May 11, 2015
- Fix: cannot load game attribute of type map (serialize and unserialize game attributes on save/load)
- Fix: detect error "Unable to resolve project target 'android-##'" and show info dialog
- Fix: bundled Endless Animation behavior (com.stencyl.models.Actor has no field currAnimationAsAnim)
- When duplicating use "<name> Copy" instead of "Copy of <name>"

May 6, 2015
- Fix: Stencyl not opening if preview platform index is out of bounds

May 2, 2015
- Fix: "ArrayIndexOutOfBoundsException: null" without stack trace on Mac with Java 8 (-XX:CompileCommand=exclude,javax/swing/text/GlyphView,getBreakSpot)
- Disable preallocated exceptions on Mac and Linux (-XX:-OmitStackTraceInFastThrow)
- Fix: guard against empty names in alphabetized menus

April 30, 2015
- Fix: Error closing newly created, unsaved resource
- Fix: progress window is grabbing focus whenever the message changes

April 29, 2015
- Fix: non-hidden boolean attribute defaults and game attribute boolean defaults regressions
- Fix: uncaught exception when not using "Apply New Category" for game attribute

April 26, 2015
- Fix: attribute getter/setter regressions
- Fix: ClassCastException: ... cannot be cast to stencyl.core.lib.tile.Tileset

April 26, 2015
- Fix: Stencyl version logged as "null"
- Fix: No progress dialog while changing workspace

April 25, 2015
- Fix: remove illegal chars from game name when importing

April 24, 2015
- Fix: Can’t get application "iPhone Simulator" (now called "iOS Simulator")
- Fix: missing return statements for non-Android

April 23, 2015
- Google Play Services extension

April 22, 2015
- Fix: splash spinner color

April 21, 2015
- Fix: uncaught exception preventing opening of scene and settings when an actor references an non-existing actor type
- Fix: remember last used directory in file dialogs
- Adjust font character offsets by 1

April 20, 2015
- Revert latest Simply Physics changes
- Fix: error when trying to exit non-projector flash game with the exit game block

April 19, 2015
- Fix: can't open behaviors, actors or scenes because of an error in creating custom blocks
- Fix: allow to open folder with FileDialog on OS X

April 17, 2015
- Fix: "installed package" is incorrectly reported as an error
- Fix: regression: kits are not shown

April 15, 2015
- Add "exit game", "game URL" and "step size" blocks
- Additional workspace permission check on startup
- Fix: catch single character haxe syntax errors
- Fix: text wrapping on sign-up dialog

April 13, 2015
- Show build date in About dialog
- Show "generate logs" button on error dialogs that ask for logs
- Show languages from install folder in language chooser (workspace languages take preference)
- Hide "update language packs" button (currently not supported)
- Add clarifying note and overlay icons to sign in and sign up dialogs
- Fix: uncaught exception when creating a new kit
- Fix: uncaught exception when leaving screen width/height fields empty

April 6, 2015
- Fix: uncaught exception when adding a behavior and the "behaviors" dir is missing in the install dir
- Warn about renaming a game folder to an invalid name

April 1, 2015
- Fix: cropped screenshots; still doesn't work in all cases (Thanks, Max Glocking!)

March 28, 2015
- Fix: Illegal collision groups (from an old bug) prevent game to run
- Add message about deprecated Tile API extension

March 26, 2015
- Fix: Detect "Error: Could not guess MINGW_ROOT" (missing Visual Studio)
- Add menu item Debug->Windows->Reinstall Visual Studio

March 25, 2015
- Fix: Can't save game if favorite block is missing a definition

_**3.3 Update (1st)**_

March 21, 2015
- Fix: Blocks with text fields getting cut off.

March 19, 2015
- Fix: Simulated key presses in mouse events can cause key press/release events to fire twice.

March 18, 2015
- Fix: Fix up Chrome Web Store support
- Fix: wrong line delimiter in mm.cfg

_**3.3 Public Release (Initial)**_

March 17, 2015
- Fix: "Starting: Intent" is incorrectly interpreted as an error
- Fix: Windows installer version number
- Fix: Drawing error when large code blocks have the red error effect applied.
- Fix: Bad type conversion, empty non-hidden map attributes initialized as text.
- Fix: Game name verification being applied to game description caused hanging in settings dialog

March 15, 2015
- Implemented copy of map block.
- Fix: "on screen" area being initialized to location of camera in previous scene.
- Fix: Camera position getter not updating until next game loop.

March 14, 2015
- Fix: launch image resizing regression

March 13, 2015
- Fix: Performance regression on iOS / Android / Desktop due to HXCPP (3rd-party) bug.
- Fix: Auto-clicking glitch when dragging blocks by field.
- Fix: Error when opening block menu on dragged block.
- Fix: Added converters for "enable-tile-wire" and "disable-tile-wire".
- Fix: Error when saving code in external editor after closing Stencyl tab for that code.
- Fix: Error when switching layers in Scene Designer.
- Fix: Android min and target versions in game settings being ignored.

March 12, 2015
- Fix: iAds top/bottom mixup
- Fix: iAds - bottom ads (post-correction) not displaying in landscape
- Fix: regression reading custom blocks

March 11, 2015
- Add "Don't show again" button to unexpected problem dialog
- Fix: change name of game folder manually breaks the game
- Fix: uncaught exception for illegal custom block definitions

March 10, 2015
- Fix: "newSize must be lower than the image width" when accessing attribute dropdown

March 8, 2015
- Fix: Add Engine parameter to new() in code mode templates

March 1, 2015
- Fix: uncaught exceptions with corrupted bitmap font

February 28, 2015
- Improve error message for missing MP3s for Flash

February 27, 2015
- Partial Fix: Fonts Page / Font Picker is broken

February 26, 2015
- Fix: Android build fails when changing app ID
  (Multiple dex files define Lcom/yourname/gamename/BuildConfig;)
- Fix: save game before publishing
- Change to current dir in Linux launch script to make it runnable from anywhere (Thanks, yoplalala!)

February 25, 2015
- Fix: Prompt for game format update and clean project to prevent build failing with "too many arguments"
- Fix: uncaught exception if actor sprite image is missing
- Fix: hide progress when error dialog is shown
- Fix: don't allow leading or trailing spaces in game or resource names

February 24, 2015
- Fix: old build may be launched when building for Flash fails
- Fix: error in exception handler when stack trace is empty
- Hide non-functional Check Syntax button in code mode behaviors

February 22, 2015
- Fix: log viewer popping up when testing in browser, even when there was no error

February 20, 2015
- Fix: exception on the event-dispatch-thread aren't shown

February 19, 2015
- Fix: long text is cropped in message dialogs
- Warn about unclean install over an old installation
- Warn about missing write permissions for workspace (and suggets to run "as administrator" on Windows)
- Allow most blocks to be used globally.

February 18, 2015
- Fix: Iterating over null list when an actor group doesn't collide with other groups.

February 17, 2015
- Update detection of Visual Studio to include non-Express and 2013 versions
- Improve detection of JDK on non-English Windows systems
- Fix: native FileDialog does not allow selection of folders on Windows
- Fix: Block errors can be hidden behind blocks.

February 16, 2015
- Fix: Editing one tile from frame edit dialog replaces whole tileset.
- Update Java JDK installation instructions
- Fix: Collision points not updating for continuous (sliding) collisions.
- Fix: Layers with custom scrollfactor don't always draw tiles at edge of screen.
- Fix: NPE in tileset editor when closing context menu by clicking on tile.
- Fix: Design Mode blocks being cut off.
- Fix: Don't allow blocks to be released outside of work area bounds.
- Fix: Block under mouse detection not checking top-most blocks first.
- Engine extensions: show custom icons on blocks. [c:icon-name] = extension/block-icons/icon-name.png

February 15, 2015
- Fix: Cannot compile games or download resources if user name contains non-ASCII chars on Windows
   ("unknown protocol: c")
- Fix: fresh workspace has empty locale setting
- Fix: Atlas-scene binding being reset.
- Fix: uncaught exception when canceling export of resource
- Fix: uncaught exception in when changing physics settings

February 14, 2015
- Fix: Tile collisions in Simple Physics.
- Fix: Cannot add listener function to null region.

February 11, 2015
- Fix: Hitboxes not colliding with correct hitboxes.

February 10, 2015
- Fix: prevent NPE when image from StencylForge cannot be read

February 9, 2015
- Fix: Cannot determine bundle ID from provisioning profile if keys are ordered differently

February 7, 2015
- Fix: missing scene XML when the scene resource has same ID as another resource
- Fix: uncaught exception when collapsing "From your game" or "From your library" in behavior chooser
- Fix: uncaught exception when duplicating scene that has not been opened before
- Fix: symbolic links are not preserved when installing Android SDK
- Use "Copy x of" instead of "Copy of Copy of" after duplicating multiple times

February 6, 2015
- Fix: detection of toolset exceptions might produce false positives

February 5, 2015
- Fix: Scale to Fit (Full Screen) (full fix)
- Force-add beta-reports-active = true to entitlements. If you get an error upon publishing your game, you need to remake your provision profiles. See: https://developer.apple.com/library/ios/qa/qa1830/_index.html

February 4, 2015
- Fix: error when creating thumbnail for scenes smaller than 120x90
- Fix: Scale to Fit (Full Screen)

February 3, 2015
- Fix: uncaught exception after downloading a toolset exception
- Detect exceptions from toolset extensions and show more informative error message
- Initially hide details from uncaught exception dialogs

January 31, 2015
- Fix: Fix scaling issues on mobile targets caused by OpenFL changes. (should now work)

January 30, 2015
- Fix: Fix scaling issues on mobile targets caused by OpenFL changes. (Undone since the fix caused more issues than it fixed)

January 28, 2015
- Fix: simulator always launches as a 3.5" device
- Fix: no logs from iOS games

January 26, 2015
- Fixes to Google Purchases v3.

January 25, 2015
- Fix: Remove CFBundleIconFile and CFBundleIcons from Info.plist templates
- Fix: Cannot get/set game attribute in global custom blocks
- Fix: Increase width of Palette to make space for Maps in Attributes category
- Fix: Workaround for uncaught exception when dragging a palette tab
- Automate Android SDK installation on Linux (don't require user to run script manually)

January 23, 2015
- Fix: attachImageToActor not working with 3x scale (Thanks, RedEvo!)

January 21, 2015
- Better error message for out-of-memory errors
- Use monospaced font in log viewer
- Avoid logging new OpenFL and hxcpp logos
- Fix: uncaught exception when using the dropdown of behavior blocks
   (DelayedMenuLayout cannot be cast to GridBagLayout)
- Fix: file ... has been modified since the precompiled header ... was built
   (Disable GCC_PRECOMPILE_PREFIX_HEADER in lime's project.pbxproj)

- [Not part of the build] Fix: Pencyl not working on Windows.
   (To get the new version, delete <your workspace>/tools/Pencyl.jar and reinstall it from within Stencyl.)

_**(As of this point, 64-bit builds for iOS are now enabled, and you should be able to submit your game to remain in compliance with Apple's new requirements.)**_

January 20, 2015
- Rebuild extension libraries to include 64-bit versions for iOS builds
- Fix: Use 64-bit version of neko on Mac, required by the latest haxe
- Fix: NPE when dragging block with parentgroup == null over events pane

January 18, 2015
- Upgrade haxe to 3.1.3, OpenFL to 2.2.4, hxcpp to 3.1.48, and lime to 2.0.5

January 16, 2015
- Kill haxe processes on Windows
- Fix: error when opening resource after opening it in quick succession
  ('Document "<name> + <ID>" is not opened.')
- Fix: "RasterFormatException: (y + height) is outside raster" when importing actors(?)
- Fix: Don't use bold font for non-English

January 13, 2015
- Fall back to English for missing translations instead of showing [Missing]
- Fix: Show an error dialog for missing/corrupted scenes
- Fix: Don't warn about being unable to refresh, when closing a tab
- Fix: Regions and Doodads buttons should not have buttons in collision group settings
- Game-specific extension data
[Design Mode Changes]
- Find Block in behaviors.
- Drag block to palette to throw away.
- Hover block over event pane to navigate to another event.
- Improve block dragging performance for huge events.
- Misc. fixes to dragging blocks from palette.

January 12, 2015
- Fix: consume block for android v3 purchases

January 9, 2015
- Fix: workaround for uncaught exceptions in GameLibrary.refreshCounts
- Fix: uncaught exception in Atlas.memoryUsageUpdated

January 6, 2015
- Change log level of Android device logs to debug

January 2, 2015
- Add process name to log statements of external processes

December 29, 2014
- Fix: Shaking scene when not zoomed in
- Add option to hide columns in log viewer
- Add milliseconds to time column and hide date from time column in log viewer

December 28, 2014
- Fix: importing Map entries from a text file adds "key -> |" instead of "key -> value"

December 26, 2014
- Fix: show error dialog when memory exceeded while searching StencylForge

December 25, 2014
- Fix: Stencyl fails to launch when the 'extensions' folder is missing and can't be created

December 24, 2014
- Fix: import scale preference not being saved
- Fix: phone-only setting not being saved

December 22, 2014
- [Not part of the build] Fix: Pencyl not working on Mac and Linux.
   (To get the new version, delete <your workspace>/tools/Pencyl.jar and reinstall it from within Stencyl.)

December 21, 2014
- Fix: all cases of IllegalArgumentException: Width (-1) and height (-1) cannot be <= 0 in getBufferedImage
- Fix: unexpected problem in palette search
   (ClassCastException stencyl.core.engine.actor.ActorGroup cannot be cast to java.lang.String)
- Fix: unexpected problem when failing to read an image
   (workaround for ImageIO.read throwing undocumented IndexOutOfBoundsException)

December 20, 2014
- (Another) Fix to compile error caused by Android Purchases upgrade.
- Remove references to old billing plugin from Android manifest.
- Fix: iOS tabled-only builds fail because of incorrect LaunchImage names

December 19, 2014
- Fix to compile error caused by Android Purchases upgrade.
- Draw native scrollbars on Macs.
- Draw (some) native buttons on all platforms.
- Fix: "keys of <map> as list" returns values
- Add "Generate Logs" and "Force Quit" button to the Unexpected Problem dialog

December 18, 2014
- First Cut: Upgrade Android Purchases to v3. Clean your project before attempting to use.
- Fix: corrupted or missing background images prevent game from opening.
- Fix: "running on" block doesn't detect iPhone 6+ with Display Zoom mode enabled

December 17, 2014
- Fix: "data for collided tile" block doesn't work in scene behaviors
- Fix: uncaught exception when right-clicking "This game contains no [...]. Click here to create one."

December 16, 2014
- Fix: uncaught exception when closing a bitmap font without image
- Fix: hide unimplemented font spacing tab

_**3.2 Public Release (Second  Update)**_

December 15, 2014
- Fix: Stencyl fails to launch when there is an error reading the extensions dir
- Fix: Error when creating IPA (NPE in IOUtils.copyLarge because of custom Entitlements.plist)
- Fix: cannot save game when resource pack icon size cannot be determined
   (IllegalArgumentException: Width (-1) and height (-1) cannot be <= 0)
- Fix: uncaught exception for out-of-sync blocks with no fields
   (IndexOutOfBoundsException: Index: 0, Size: 0 at RangeCheck)
- Fix: Unknown action: menu.gameedit: "Download" and others (wrong action listener registered)
- Fix: unexpected problem when right-clicking to close a tab
- Fix: frame rate drop and random crashes when putting "always active" in a "when updating" event

December 14, 2014
- Fix: Missing block help texts (event.helper.thisactor.help and event.helper.otheractor.help)

December 13, 2014
- Stop showing the What's New dialog
- Fix: Null pointer when an actor still exists even though it's layer was removed.
- Fix: Animated tiles not saving to the right filename.

December 12, 2014
- Fix: "Unknown action: menu.gameedit" (wrong action listener registered)
- Fix: misleading error message when a resource file is missing
- Colored Tabs preference

_**3.2 Public Release (First  Update)**_

December 12, 2014
- Fix: extension blocks don't show up in palette (Blocks.xml not reading properly)

_**3.2 Public Release**_

December 10, 2014
- Fix up launcher on Mac to work with Java 6/7/8. (Take 2)
- Updated Education site. Put up Education Kit for distribution (but that requires 3.2...)

December 7, 2014
- Fix up launcher on Mac to work with Java 6/7/8.

December 2-6, 2014
- Updated Stencylpedia to match all the new material and improvements in 3.2.
- http://www.stencyl.com/help/view/shaders
- http://www.stencyl.com/help/view/gamepads
- http://www.stencyl.com/help/view/maps
- http://www.stencyl.com/help/view/tiles
- http://www.stencyl.com/help/view/backgrounds-and-foregrounds

November 28, 2014
- Fix: uncaught exception when a font has color none

November 27, 2014
- Fix: update iOS troubleshoot URL

November 26, 2014
- Fix: for TestFlight support.
 
November 25, 2014
- Fix: properly detect if game had disabled high-res graphics when upgrading to new format (avoids taking really long to recreate assets)

November 24, 2014
- Not part of a build but dusted off our MSI packager for educators who want 3.x (and beyond) in MSI form.

November 23, 2014
- Switch over to using assets catalogs for iOS splash screens.
- Fix: 1px black bars on top/bottom of screen on iPhone 6/6+.

November 18, 2014
- Fix: Map block pickers are empty/missing
- Fix: "Create New Game Attribute" dialog is cropped on Mac

November 16, 2014
- Fix: "visit URL" block freezes on Android when there is no connection
- Fix: uncaught exception in SpriteWriter

November 13, 2014
- Fix: CPMStar preloader option doesn't work (incorrectly expects a custom SWF)
- Allow extension blocks to be yellow

November 12, 2014
- Warn if opening a game written with a newer version of Stencyl
- Add "private-build" to the version number in the about dialog

November 8, 2014
- Add back legacy iOS versions to dropdown.

November 6, 2014
- Fix: uncaught exception in HXWriter.importIOSCertificates

November 5, 2014
- Fix up iOS (Simulator) version detection, so the Mobile > Versions page will now properly show what you have.
- Clean up some faulty logic with detecting whether Yosemite was detected or not.

November 4, 2014
- Fix up toolbar coloring on OS X Yosemite.
- Fix up iOS Simulator support for all device types.

November 3, 2014
- Fix: catch IndexOutOfBoundsException from ImageIO.read

October 28, 2014
- View SHA1 Fingerprints for Android Certification

October 27, 2014
- Fix: "Override back button" option isn't saved
- Fix: pixel-snapping option isn't saved
- Fix: uncaught exception in Cleanup Unused Files if PNG name doesn't end with scale, e.g. 0-0@4x (1).png

October 24, 2014
- Support for iPhone 6/6+ simulators (still a work in progress)

October 21, 2014
- Fix: regression - cannot switch back to font style tab
- Fix: regression - font toolbar alignment

October 20, 2014
- Fix: uncaught exception in BlockSceneObjectChooser.update

October 19, 2014
- Option for snapping actors to pixel grid
- Fix: uncaught exception when trying to clean simulator folder

October 18, 2014
- Fix: Error when shift-dragging top block

October 17, 2014
- Ship a patched PackageApplication script to prevent "resource envelope is obsolete" and "Warning: usage of
    --preserve-metadata with option "resource-rules"" when exporting iOS with Xcode 6
- Add options for attached block definitions and hidden blocks to extension blocks
- Fix: uncaught exception if bitmap font has background color "none"

October 15, 2014
- Fix: uncaught exception in Cleanup Unused Files, if using bitmap font
- Fix: improve warning message if failing to parse iPhoneSimulator SDK version

October 13, 2014
- Fix: Another attempt to fix the resource envelope warning on iOS 8.

October 12, 2014
- Fix: uncaught exception when missing resource is selected in dropdown
- Fix: tabbed pane on preloader page looks bad
- Fix: too big font causes buttons to be cropped on Linux in several places (game settings, create new, ...)

October 10, 2014
- Option to exclude scales for each platform individually
- Support for 3x scaling
- Fix: Remove unused .ttfs when calling Debug -> Game -> Cleanup Unused Files

October 4, 2014
- Fix: cannot create new tile layer after deleting all tile layers
- Fix: uncaught exception when clicking New Background Layer -> Cancel
- Fix: uncaught exception when no Xcode is installed

October 2, 2014
- Fix: uncaught exception prevents opening settings (NullPointerException in AtlasEditor.verifyText)
- Fix: uncaught exception when uploading an actor type to StencylForge

October 1, 2014
- Fix: regression: cannot use space in snippet names

September 30, 2014
- Fix: uncaught exception when extension block has no fields

September 29, 2014
- Fix: "Free" the sound channel after using the "stop sound" block by setting sound to null
- Fix: Run in browser ignores web scale setting
- Fix: exception thrown when trying to read non-existent block favorites XML when creating a new game
- Fix: uncaught exceptions in ImageUtil.readImage when opening game settings

September 20, 2014
- Fix: Update ios-sim, so the iOS simulator can be used with both Xcode 5 and 6.

September 18, 2014
- Fix: build problems with Xcode 6 (turn off GCC_PRECOMPILE_PREFIX_HEADER)

September 15, 2014
- Add options for iPhone 6 / 6+ to "running on" block
- Sort collision groups in groups page and shape dropdown
- Fix: .hx files not copied on resource import

September 14, 2014
- Fix: Uncaught NumberFormatExceptions in inspector

September 13, 2014
- Add support for iPhone 6/6p splash images
- Fix: Scale splash images to correct size if necessary instead of erroring out
- Fix: Errors trying to load non-existent images in joint inspector
- Fix: Joint inspector doesn't accept floating point numbers

September 12, 2014
- Fix: Android Tips dialog image fails to load and has missing title and wrong URL

September 11, 2014
- Fix: Uncaught exceptions when creating new scene or accessing atlases

September 9, 2014
- Fix: Uncaught exception when modifying grid properties
- Fix: Prevent null pointer exception on Palette.createAndAddElement

September 8, 2014
- Close log viewer with escape key

September 7, 2014
- Fix: Error when loading "What's new" page
- Fix: "Get More Extensions" button is grayed out
- Fix: Update iOS Troubleshoot URL in error dialogs

September 7, 2014
- Sort preference keys in boot.txt
- Fix: bogus no games/kits message
- Fix: lazy initialization in preferences dialog causes NPE

September 5, 2014
- Sort system properties log file

September 3, 2014
- Fix: Uncaught exception on CircleEditor/PolygonEditor.verify() when deleting an actor
- Fix: Custom/extension blocks break with 10 or more parameters

September 2, 2014
- Fix: Positioning after Actor->Actor collisions in Simple Physics

September 1, 2014
- Color pickers for scene transition blocks
- Let the log viewer remember its size
- Let the log viewer scroll horizontally
- Add "Generate Logs" and "Always on Top" options to log viewer
- Add "Copy to Clipboard" button to "Unexpected problem" dialog
- Fix: Don't scroll to bottom in dialog with text area
- Fix: Closing Actor when Collision box values has focus causes error
- Fix: Prevent game attribute list initialization from throwing error when opening snippet
- Fix: Lines with '/' as second character are not logged
- Fix: Exception thrown when trying to read a scene thumbnail that hasn't been created yet

August 29, 2014
- Fix: Prevent Print Screen and Numlock from crashing games.

August 25, 2014
- Fix: Simple Physics bugs

August 22, 2014
- Fix: Backgrounds were using wrong default parallax at scales > 1.

August 20, 2014
- Fix: Backwards compatibility for scrollfactor setting.

August 19, 2014
- Fix: Repeated backgrounds not scrolling when parallax was 1,1.

August 18, 2014
- New block: get z-order of image instance
- Fix: No tiles optimization is turned off if tiles are added by Tile API.
- Fix: get button pressure causes crash if no gamepad buttons have been pressed yet
- Fix: Repeated backgrounds no longer repeated after being unloaded once
- Tilesets: Replace tiles now only replaces selected tiles
- Fix: Tile metadata was buggy with multi-tile selections

August 16, 2014
- New blocks: Add and remove background layer, set layer order
- Fix: NullPointerException when MP3 files have no ID3v2 layer

August 15, 2014
- Fix: Andoird build error (Called from BuildTool.hx line 1536, line 673, line 708, line 845, line 942)
- Fix: Exception when closing scene with map attribute (MapElement cannot be cast to ListElement)
- Fix: Exception when importing MP3 files
- Fix: Sound import dialog doesn't show directories on Linux

August 13, 2014
- Fix: Folders are lost on save game (ClassCastException for folder icon)
- Fix: Uncaught exception when right-clicking in an empty folder
- Fix: Double separator in context menu
- Fix: Don't open "create new..." dialog on right-click
- Fix: Show context menu only-when right-clicking an item (not empty space or "create new...")

August 11, 2014
- The tile line fix now affects all scale modes.
- More control over backgrounds and layers.

August 9, 2014
- Fix: parsing for errors trips over unexpected message format (String index out of range: -2 at stencyl.sw.io.write.resource.HXWriter.parseErrors)
- Fix: compiler error message is truncated if it contains colon(s)

August 7, 2014
- Fix: Backslash in list or text attribute's default value break behavior

August 6, 2014
- Fix: Can't remove lists entries in the interface that include $ or \

August 3, 2014
- Make Flash runtime errors visible in the logs (register an uncaughtErrorHandler with trace statements)
- Fix: [Missing] header in Number block picker under User Input

August 2, 2014
- Fix: show layer, hide layer, set blend mode for layer block, don't accept attributes for layer ID (Float should be int)

August 1, 2014
- Fix: "fade layer [_] to [_] % over [_] secs" block doesn't accept attributes for layer ID (Float should be int)
- Fix: Select color for scene background bug (side effect of Yosemite/Java 7 fix)
- Fix: Prevent unexpected error popup when a block cannot be error-highlighted

July 30, 2014
- Fix: custom haxe flags are not honored
- Fix: Image API "move by" block now works properly with higher game scales.
- Fix: Stencyl doesn't start on Yosemite with Java 7 (java.util.HashMap cannot be cast to java.awt.RenderingHints)

July 29, 2014
- Fix: check for internal attribute name clashes with haxe keywords
- Added origin point (for rotating and growing) to Image API

July 28, 2014
- Externally edit multiple animation frames at once.
- Folder dropdown in Scene Designer Actor Palette.

July 27, 2014
- Disable the check for in-app updates
- Fix: Font resources not found (... /fontwriter/out.fnt (No such file or directory))
- Fix: Game breaking when scenes not saved to include atlas binding.
- Fix: Exporting games wasn't automatically attaching .stencyl
- Fix: After opening a game, app title only contains build number but not the word "Build"
- Fix: Atlases missing in-game when Main Atlas had "every scene" enabled.

July 26, 2014
- Update Android SDK to support Java 8. If you get "Class not found: javac1.8" when building for Android, reinstall the Android SDK.
-The "for each member of group" block now works with "actor group" attributes.
- Centralized Atlas Management. Atlases can now be bound to scenes.

July 23, 2014
- Add function to set font spacing: _Font.setLetterSpacing(10)
- Fix: Auto-convert sin/cos blocks to new version with degrees/radians dropdown

July 22, 2014
- Fix: Prevent 'Clear Logs' from deleting the log file of the current session
- Fix: 'Clean Project' fails to delete some files
- Fix: Uncaught exception when trying to undo or redo with nothing to undo or redp

July 21, 2014
- Fix: Can't create custom block with image instance argument
- Fix: Can't create custom block with argument containing 'i' (like List) under Turkish locale
- Fix: Missing type names (missing cat.variables.type.lıst, etc.) under Turkish locale

July 20, 2014
- Update built-in AdMob extension. In compliance with August 1st requirements, fixes some old bugs with placement, appearance when game's state changes. (Thanks Abliblablobla!)
- Show some more details for compiler errors
- Popup dialog for unexpected problems (i.e. uncaught exceptions)
- Fix: NullPointerException when closing a game while having StencylForge open
- Fix: Add transitional class for toolset extensions that still use the old Debug system

July 17, 2014
- New log viewer

July 16, 2014
- Adopt a new logging framework (for more detailed and flexible logs)

July 14, 2014
- Fixed Image API screenshot block scaling.

July 10, 2014
- Use monospaced font with wider Unicode support in block fields

July 9, 2014
- Fix: Extension blocks not appearing for users of Turkish locale
- Fix: Force using English locale in Dashboard if UI language is English (fixes strange upper case i for users of Turkish locale)
- Fixed x/y center of camera block.
- Fix: Mac OS X user interface glitches (black background behind rounded corners)
- Bundled Behaviors: Follow the Mouse and Face the Mouse are not Flash-only anymore.

July 4, 2014
- Fix: Assigning multiple gamepad buttons to a single control
- Fix: Scene's behavior page is blank if any of it's behaviors have been deleted

July 3, 2014
- Gamepad support.
- [Fix] Remove attached images when recycling actors.

July 1, 2014
- Disable feature where hitting ESC will exit a desktop game.

June 24, 2014
- Fix to Scale to Fit (Full Screen) - Thanks abi!

June 21, 2014
- Added blocks and engine support for Map attributes.
- Prevent bad prefs values from breaking Stencyl

June 20, 2014
- Added ability to re-arrange tiles within the Tileset Editor. Ask Justin for details.

June 12, 2014
- Fix - Divide a number by Scene width(tiles) gives wrong result

June 9, 2014
- Blocks to get/set frame duration
- Replace begin/end polygon drawing blocks with a wrapper block
- Fix some missing block helps
- Tileset zooming

June 8, 2014
- New collision shape blocks
- Add font width/height blocks to palette under text
- Fix - Some Unicode chars break bitmap fonts - force UTF-8 encoding for fonts XML
- Fix - Web Maximum Scale Doesn't Save
- View tile shapes overlay over tileset image
- Added half-square default shapes to tileset editor
- Send animated tile to external editor

June 5, 2014
- Integrate Tile API blocks into the main block set. (Scene > World)
- Add metadata to tiles. Accessible using the Tile API.

June 3, 2014
- Adjust toolbar color on OS X 10.10.

June 1, 2014
- New Shader: Sharpen
- Add method to check if a font contains a character: _Font.font.containsCharacter("x")
- Fix - Install Extensions dialog accepts only images instead of zip files on Linux
- Fix - "character" block in "any key" event returns unprintable chars instead of empty string
- Fix - Desktop Maximum Scale Doesn't Save

May 28, 2014
- Fix - setFrameDurations affects all actors of the same type

May 24, 2014
- Fix - Some characters break bitmap fonts (<, >, &, ', ")

May 23, 2014
- Send Tileset Image to External Editor
- Reimport Tileset image
- Fix the "add new tiles into tileset" feature
- Fix "Property delete not found on haxe.ds.IntMap" on collisions in Flash
- Sort engine extensions by name in settings dialog

_**3.1 Revision 3**_

May 22, 2014
- Desktop Full Screen was causing Flash games to draw as blank.

_**3.1 Revision 2**_

May 20, 2014
- Scale to Fit (Full Screen) was applying wrong scaling logic in some cases.
- Fix height of ad block.
- Fix actor type and scene attribute setters.

May 18, 2014
- Create new preferences file (boot.txt) if it is missing at startup
- Add blocks to get/set actor opacity

_**3.1 Revision 1**_

May 16, 2014
- Fix issue when using a Scale > 1 and Max Scale = 0 on Flash.

_**3.1 Public Release**_

May 14, 2014
- Load default extensions from install directory instead of from workspace
- Warn the user if an enabled engine extension is missing when opening a game
- Fix - FileNotFoundExceptions when switching workspace and subfolder doesn't exist

May 13, 2014
- Fix - Also copy engine extensions when switching workspace

May 12, 2014
- Add right-click->Find Setter/Getter in Palette to attributes pane
- Add Find in Palette option to search results
- Fix - scene reverts to old name when opening after right-click->rename

May 11, 2014
- Sort attached behaviors by folder and name
- Enable debug drawing for joints

May 10, 2014
- Support for favorites in the block picker
- Fix - Create Game Attribute button in Palette shows Game Settings even if canceled
- Fix - Show home directory in import resource dialog

May 9, 2014
- Sort games in welcome center by name
- Add Anything and Joint attribute types
- Fix - Extension block fields of type anything have an empty block picker
- Fix - Testing in browser on Linux opens the SWF in a text editor if not running Gnome
- Fix - Temporary logs folder (stencylTempLogs) is not deleted when you cancel generating logs

May 8, 2014
- When creating a new event, place the new event right after the last selected and not to the bottom.
- When creating a new attribute, place the new attribute right after the last selected and not to the bottom.
- When deleting an attribute, select the next attribute instead of the first.
- Fix - First time opening object type dropdown the image and image instance menus are not displaced
- Fix - Can't access quick commands
- Prevent getting stuck on  "Got deadlocked while loading languages" forever, if workspace is moved/missing

May 7, 2014
- Fix - Icon is lost if smaller than 1024 x 1024.
- Turn off caching for image from file block.

May 6, 2014
- Fit preloader preview and add zoom buttons
- Fix - Duplicating an event puts the event block in the clipboard
- Fix - Assigning some keys as controls prevent game from launching
- Fix - SWF scaling is wrong in Flash Player if player size is different than SWF size (this fixes the need to reload the SWF when testing in Flash Player on Linux)
- Fix - Generate Logs shows success even if logs could not be generated

May 5, 2014
- Sort attributes in block picker
- Fix layout problems in block picker
- Fix missing headers for number and text game attributes in block picker
- Fix close button not being grayed out when tab isn't closeable
- Add Reset Layout option to View menu in for scene designer
- Clarify wording on generic game attribute getter/setter blocks
- Fix - List default values not adding

May 4, 2014
- Add shortcuts for flipping between Palette/Attributes/Favorites.
- Add a search bar to the code preview
- Show custom blocks in palette search results
- Fix actor duplication bug.
- Fix - Freezing actors in "for each actor on screen" loop
- Fix - Default collision groups reset after closing and re-opening a project
- Move the Toggle/Show items and Code Preview from the Edit to the View Menu.
- Hide Collision and Drawing tabs when opening a snippet

May 3, 2014
- Engine Extensions get their own palette section
- Honor the color field of extension blocks
- New "actor type with name" block
- Add space to blocks that only consist of a dropdown
- Add some missing block help texts

May 2, 2014
- [Fix] Atlases were all loading initially on standalone target.
- Fix - Custom grid setting don't work in scene editor
- Fix - Attribute Block Names Aren't Renamed In Events
- Making folder opening on exporting game/snippet optional
- Add comments for all events to code to make it more readable
- Refresh tab after right-click rename
- Fix size of polygon collision editor
- Added right and middle mouse button support to desktop for the engine.

May 1, 2014
- Atlas is loaded block.
- [New Scale Mode: Scale to Fit (Full Screen)](http://community.stencyl.com/index.php/topic,31729.0.html)
- Report multiple collision points per collision
- Add rename to right-click menu for Events
- Add rename to right-click menu for resources (actor, scene, behavior, ...)
- Add create circular region block
- Add degrees/radians dropdown to sin/cos block

April 30, 2014
- Fix category of attribute setters for actor type, control, scene and sound in palette
- Fix mouse coordinates don't match Zoom setting in Collision tab
- Full screen scale mode on desktop now works. (previously was defaulting to No Scaling)
- Fixed clear image block.
- Save layout after closing scene designer (remember width of side panel).

April 29, 2014
- Fix logic bug in preloaders caused by removal of Mochi.
- Fix semi-transparent windows when using JDK7/8
- Fix - Cannot create a list a Game Attribute as a List
- Fix text game attribute not accepting empty values

April 28, 2014
- Clarify wording on camera move blocks; add x/y-center options to camera getter.
- Guard against selecting scales that don't exist in Bitmap Font image importer.
- Fix NPE when entering/exiting full screen in standalone when not using any shaders.

April 27, 2014
- Increased performance when using tint filter by itself on desktop/mobile.

April 26, 2014
- Guard against selecting scales that don't exist in FrameImportDialog.
- Improve layout of game attributes and atlas pages
- Fix - Game Attribute - No Naming Restriction - Corrupts Project
- Fix - X of collision and Y of collision giving half coordinates.

April 25, 2014
- Add getter/setter blocks for physics properties to core palette
- Add z-index blocks to core palette
- Make space for for a third column in controls page
- Widen actor name box.
- Comment wrapper block is now gray.
- Fix - Bottom pane of DM attributes tab has a min-width wider than default sidebar size
- Auto-insert code block in “import” and “code” events.

April 23, 2014
- Fixed a bug affecting images attached to actors in 1.5 scale.
- Added a text-to-sound block
- Support rollover help for extension blocks via help attribute.

April 22, 2014
- Fix a NPE with animated tiles. (?)
- Fixed conversion for languages that are completely non-Latin characters.  Also optimized out one array for faster speed and less memory. (out2lunch)
- Fix bug in retainImageForMask (runimals)
- Improve image resizing algorithm when downsizing images.

April 21, 2014
- Nix the compiler error detector because of complaints about logging slowing Stencyl down. Replaced with just a message and a request to re-rerun the game to see what's wrong.
- Honor atlases for standalone desktop games.

April 19, 2014
- Add resize image block.

April 16, 2014
- Enhance compile error detection and reporting for general users. It will now pop up the log viewer with a message when you hit a compile error rather than leaving it undetected. (thereby no longer leading lay users to think the game is "compiling" for "hours" when in reality, it died seconds into compilation)
- Auto-clear logs at the start of every run. Don't force logging outside the compile/run process.

April 15, 2014
- Add block picker (right-click in Design Mode) entries for the Image API.
- [Fix one off errors in Utils.hx (spotted by out2lunch)](http://community.stencyl.com/index.php/topic,30826.0.html)

April 14, 2014
- Move extensions over to the workspace folder.
- Fix bug in animated tiles.

April 13, 2014
- Fixed compile error if you use a number attribute with attach image to layer block.
- Flagged all effect-related blocks in the Image API as Flash only. We'll support them on desktop/mobile using shaders in the  future.
- Add missing block drop down entries for the Image API.

April 11, 2014
- Mouseover block help for Shaders
- Dropdowns for Shader fields
- Fix shader behavior when you flip between full screen and windowed.
- Fix FPS monitor position when you flip between full screen and windowed.

April 10, 2014
- Fix bug when importing bitmap font images @ scale > 1.
- Support Unicode in downloaded text or text from external files via Script.convertToPseudoUnicode()
- Shaders now work in full-screen mode.

April 9, 2014
- [Full Screen Shader support.](http://community.stencyl.com/index.php/topic,31060.0.html)

April 6, 2014
- Remove Mochi blocks / preloader.

April 4, 2014
- [Clean up Actor listeners more thoroughly](http://community.stencyl.com/index.php/topic,30826.0.html)

April 3, 2014
- Fix up productID reported back on Android. In more general terms, fix up OpenFL bug where any data reported back from Java -> Haxe came back incorrect.
- Fixed toolset screenshots failing to prompt for saving the file to disk.

April 1, 2014
- Add null check to swipe listeners to avoid crash.

March 30, 2014
- Fix "rolling animation" bug caused by the switch over to square animation sheets.

March 29, 2014
- Two toolset extension callbacks added; onScreenCapture and getSaveImageRequest

March 27, 2014
- Android/iOS/Standalone - Pull in memory leak fix for music playback from OpenFL's Github. Confirmed to be THE fix we've been waiting for.
- Image API - Attached images now honor the anti-alias setting.
- Image API - Fixed draw text on C++ targets.
- Show build number in app title and logs for more accurate/useful user reporting.

March 26, 2014
- New Block under Flow > Advanced: current scale
- Image API - Support scaling/mobiles.
- If you were previously using the set X/Y/rotation for image block, you need to check a

_[A part of the changelog is missing]_

December 22, 2013
- Scaling algorithm wasn't preserving alpha transparency. Make it do that.

December 19, 2013
- Force all iOS icons to not apply gloss.

December 17, 2013
- Fix to actor duplication bug.

December 16, 2013
- Properly honor web scale field when publishing to the arcade.
- Fixed a problem with the "is animation playing for __" block and recycled actors on mobile/desktop.

December 10, 2013
- Fixed Android setup script on Linux. (Thanks benthepoet!)
- "Closed Newgrounds Ad" no longer appears on the screen when using the Newgrounds preloader.

December 6, 2013
- Fix up site locking by not pre-pending with http:// when that is not present.
- The "is animation playing for __" block will now return false after the end of the last frame, including single-frame animations.

December 3, 2013
- Fixes to Game Center extension.

December 2, 2013
- Scaling can revert to 1x for web/desktop games for some settings.
- Added an option to snap the actor to the position of the "Set x/y" block when using smooth motion.

November 27, 2013
- Rename HAXE_LIBRARY_PATH to HAXE_STD_PATH to fix OpenFL stup on Linux

(Detouring to start working on a much-needed rework of Stencylpedia and redesign Stencyl.com.)

November 21, 2013
- Add button to generate logs directly from Log Viewer

November 20, 2013
- Filters are now cleared when actors are recycled.

November 19, 2013
- Fixed a crash when more than 16 actors are anchored (limit changed to 64 for now).
- Stretching modes no longer break tiles on Flash.

November 18, 2013
- Fixed tile shaking in 1.5x scale on Flash.

November 17, 2013
- Set android:debuggable true when exporting APK's, otherwise Google Play will reject the apps.
- Add 1.5x scaling for Web/Desktop. (Use a setting of Scale: 1.5x, Stretch to Fit, Max Scale: 1x, Antialiasing: Off)
- Fixed a missing class error with the Newgrounds preloader.
- Fixed alignment/size problems with preloaders.

November 15, 2013
- Fixed rotation for the "draw image for actor" block in Flash.

November 14, 2013 (Other Changes)
- Readded smooth movement change to Engine.hx and raised the default of maxMove in Actor.hx

November 14, 2013 (OpenFL branch merged into main branch)
- Upgrade from NME to OpenFL 1.1.
- Support Xcode 5 / iOS 7.
- Definitively fixes all sound playback issues, especially on iOS/Android.
- Greatly improved performance on mobile, some improvement on others.
- Reduced memory usage and frame to frame churn.
- Reduced CPU usage.
- Plugged memory leaks, especially when switching scenes.
- Proper full-screen mode + scaling for web and desktop.

_**(End OpenFL branchoff.)**_

November 4, 2013
- [Pull in fix from OpenFL to smooth timing/updates in order to reduce jitter.](http://community.stencyl.com/index.php/topic,26091.msg151207#msg151207)
- Lock games to 65 FPS in order to maintain 60 FPS. (It's a quirk of NME/OpenFL)

October 30, 2013
- Not part of the build, but we have [experimental support for Spine (skeletal animations) as an extension.](http://community.stencyl.com/index.php/topic,26183.0.html)

October 27, 2013
- The mouse x/y block now returns the correct values in scale dynamically mode (NME branch).

October 22, 2013
- Backgrounds now refer to the antialias setting when stretched (NME branch only).

October 20, 2013
- Plug major memory leak causing all actors to leak beyond the scenes in which they were created (both branches).
- Plug secondary leak related to the one above.

October 19, 2013
- Make the log viewer resizable (both branches)
- Fixed camera and screen size blocks for full screen mobile games using low max scales (NME branch only)

October 18, 2013
- Implemented scale dynamically mode (NME branch only).

October 2, 2013
- Animated backgrounds now use the correct animation durations.

October 1, 2013
- Ad preloaders and custom preloaders now use the correct engine scale.

_**(Begin OpenFL branchoff. Activity on main branch will be slim to none. All activity will happen to the OpenFL branch.)**_

September 26, 2013
- Catch and present solution to case of missing Command Line Tools on iOS 7

September 25, 2013
- Android ads no longer start if the user has not entered the Admob key.

September 24, 2013
- Mouse detection for actors now works with rotation and with any origin point (but not when using the grow block).
- Fix to wrong tilesets bug

September 23, 2013
- Add option (to Mobile Settings > Input) to override Android back button's behavior.
- Warn iOS 7 users to launch app manually since fruitstrap is broken.

September 22, 2013
- Further compile fixes for iOS 7 / Xcode 5

September 21, 2013
- Support for 76x76 and 152x152 icons for iOS 7 / Xcode 5
- Partial fix for compiler changes for iOS 7 / Xcode 5 that broke our system
- Support alternate simulator modes (3.5" Retina, 4" Retina, iPad Retina)

September 20, 2013
- Android purchases are fully working now
- Status bar no longer shows up on iOS 7 / Xcode 5
- Simulator now auto-launches properly on iOS 7 / Xcode 5

September 19, 2013
- Use publisher public key for Android purchases

September 18, 2013
- Labels now fade in/out correctly.
- Fix NPE in Android purchases

September 16, 2013
- Fix problem with duplicating tiles/tilesets
- Effects no longer change all actors of the same type.
- Fix - Rotation tweening now always ends at the target value.

September 14, 2013
- Fix prefix for custom events with attributes as name

September 13, 2013
- Generate 120 x 120 icons in order to comply with iOS 7

September 11, 2013
- Fix - "Unknown Identifier" error in behaviors with custom events (prefix for custom events missing in some cases)
- Fix - Joystick would stick to screen when switching scenes.

September 10, 2013
- Fix - Accelerometer value on iOS/Android are opposites. Went with Android's value.
- Speed up the tint filter

September 9, 2013
- Fix up swipe detection by switching to a pure Haxe gesture detection library.
- Fix - iOS Device Version Doesn't Save

September 8, 2013
- Add visual installer for engine extensions.
- Start up a directory that lists out all the engine extensions written so far.
- All 7 filter blocks now work for standalone and mobile platforms.

September 7, 2013
- Chartboost Extension (contributed by rob1221/out2lunch)

September 6, 2013
- Added support for third party iOS libraries in extensions.

September 5, 2013
- Some further work on memory usage/performance.
- Let user export to free/web targets even if the site goes down.

September 4, 2013
- Fix to iAd flashing issue.
- Phase out experimental feature to have Windows users test iOS locally using AIR.

September 3, 2013
- Fix equals operator is formatted incorrectly in code preview.

August 31, 2013
- Fixed a casting error that affected Windows while using the Tile API.

August 30, 2013
- [Provide instructions on how to embed arbitrary text, images and SWF's in projects.](http://community.stencyl.com/index.php/topic,24729.0.html) Fully verified to work.

August 29, 2013
- Fix error highlighting broken by code formatting
- Add prefixes to custom block and event function names to avoid naming conflicts
- Allow Unicode characters in default attribute values
- Rename haxe class name when renaming design mode behavior

August 27, 2013
- Fix regression in Fade tweening.
- [Provide a makeshift way to include arbitrary files in projects.](http://community.stencyl.com/index.php/topic,24652.0.html)

August 26, 2013
- Catch another case of Haxe 3.0 being installed (separate installs mess up Stencyl)

August 25, 2013
- Fixed a bug affecting animated tiles and the Tile API.

August 24, 2013
- Replace all usage of HashMap with Array, Hash, or IntHash. (Performance fixes). Thorough testing of games is strongly advised due to amount of code changes.
- Hook up/fully implement billing setting added on Aug 23rd

August 23, 2013
- Add setting to enable/disable billing on Android apps. Can't auto-include billing permission because Google blocks apps from countries without billing support.

August 22, 2013
- Fix camera stutter when locked to actor.
- Fix simple physics collisions + performance improvements

August 21, 2013
- Switch over from AdWhirl to AdMob ads (on Android).
- Fix regression in tweening behavior.

August 20, 2013
- Fix Simple Physics collisions
- Fix micro stutter issues involving camera/scrolling (only tested with simple physics).

August 19, 2013
- [Reimplement iAd extension to fix all outstanding issues with orienatation, display, etc.](http://community.stencyl.com/index.php/topic,24066.30.html)

August 17, 2013
- Fix to bug where touch input stops after dismissing game center
- Prevent iOS games from using 1.5x scale

August 16, 2013
- Fix to tweening sometimes not reaching target value

August 15, 2013
- Option to delete Android keystore if it goes [corrupt](http://community.stencyl.com/index.php/topic,24405.0.html).
- Option to view the keystore.

August 14, 2013
- New Event: Request product info succeeded
- Catch Haxe 3.0 installs (which would render Stencyl inoperable) and ask user to uninstall them.
- Catch and warn against out of memory condition for Android builds
- Catch and warn against keystore errors for Android builds
- [Fix to full screen mode](http://community.stencyl.com/index.php/topic,23921.0.html)

August 13, 2013
- Get iOS purchase title/desc/price
- Add block for requesting product info to accomplish the above
- Add block to check if purchases can be made

August 12, 2013
- Fix - Stretching Causes Lines Between Tiles
- Fixes to the Tile API
- Add get collision ID block to tile API

August 11, 2013
- Fix for Stretch to Fit + Fonts

August 10, 2013
- Memory Usage Improvements (scene loading)

August 8, 2013
- Fix to scene transitions

July 24, 2013
- Fix to get x/y function

July 22, 2013
- Jaggy movement fix

July 21, 2013
- Fix up full screen mode

July 20, 2013
- Fix up bugs related to the first point on July 19th.

July 19, 2013
- When determining when to use 1/1.5/2/4 scale, base it off the game's resolution, not off 320 x 480.
- Force Perfect Fit / No Scaling to use the game's resolution rather than 320 x 480. This may alter some games, which would need to specify a resolution of 320 x 480 to switch back to the existing behavior.

July 17, 2013
- Make scale to fit respect the game's resolution rather than forcing 320 x 480.
- Add stubs for running in retina 4" and iPad retina simulator. Can't enable because of below.
- Hide regular retina simulator option since I noticed it stopped working reliably in Lion/ML. If someone knows why, let me know.
- Fix up text field appearance on ML.
- Fix up spinner appearance on ML.

July 13, 2013
- Fix up scale to fit on screens with aspect ratio > 3:2
- Forcibly delete bin/assets to make Android builds not hold on to unused assets
- Set the default max scale to 4 for iOS and Android

July 12, 2013
- Nix universal scale mode field in favor of separate iOS/Android fields.

July 11, 2013
- Maximum Scale for iOS and Android games
- Scale to fit (both types) for mobile games. Hook into existing field for now.
- [Fix] Jerky movement for Box2D actors.

July 9, 2013
- Properly record and load back in scale mode and max scale settings. Does not touch/affect current functionality!

July 5, 2013
- Switch default setting for show FPS to false.

July 2, 2013
- Add configuration options for Max Scale. Tool-side only for now, no engine implementation yet.
- Add configuration options for Scale Modes. Tool-side only for now, no engine implementation yet.

June 27, 2013
- Show Actor/Scene names instead of behavior names for events in Behavior Name chooser.

June 21st, 2013
- When there are many collision groups, show a scrollbar.

June 20th, 2013
- Retired the Adobe AIR-based iOS target due to poor performance/experience
- Remove export to single EXE option because the 3rd party utility we were using generated false positives in AV programs

June 18th, 2013
- Performance improvements to the Actor kill/recreate cycle

June 15th, 2013
- Tie Check Syntax button to selected platform
- Fix Show popup in events pane not only over selected event
- Fix Behaviors that include custom blocks break when importing
- Fix Stacktrace on entity with no animations
- Fix On Screen Button getting stuck

June 14th, 2013
- Fix HTML5 sounds not throwing SOUND_COMPLETE events

June 12th, 2013
- "Phone-Only" mode for iOS apps that don't need "4x" graphics
- Exclude 4x graphics in Phone only mode (for iOS)
- Always include 4x graphics on Android, because some "phone" devices can be high-res enough to use them

June 11th, 2013
- Reset number of active tweens when canceled
- Reset alpha after scene switch.

June 9, 2013
- Show/Hide/Fade layer fix for tiles.

June 8, 2013
- Enable 1.5x scaling support in the engine.

June 6, 2013
- When launching DDMS from Stencyl, prevent DDMS from locking up Stencyl (fork the process)

June 4, 2013
- Warn users against using sound effects larger than 100 KB for mobile games. (Limitation of NME)
- If iOS testing fails due to host / device version mismatch, display that to the user. ("AMDeviceInstallApplication failed: -402653058")
- If Xcode's command line tools are not installed, flag that and ask user to install.
- If "Unable to locate DeviceSupport directory" error shows, tell user how to fix it

June 1, 2013
- Fix Android Sound playback

May 28, 2013
- Further performance fixes
- [Fix] When type/group created not called for recycled actors

May 25, 2013
- [Toolset] Support Full Screen mode on Mac.

May 24, 2013
- Further performance fixes.
- No longer allow switching scene while IN transition is active.
- [Fix] Update Bitmap called on actor sprite creation for Flash/HTML5
- [Fix] Deleting Joints in Scene causes errors preventing deletion.
- [Fix] Set Region Size moved region.
- [Fix] Deleting Region during own region update causes runtime error.

May 20, 2013
- More performance/memory fixes to help increase FPS. Games that were previously unplayable now work OK.

May 19, 2013
- Performance fixes to help increase FPS.

May 14, 2013
- Greatly reduce memory usage for games with multiple/many scenes.
- Cleanup unused sprites from Actors, Backgrounds, and Tilesets.

May 13, 2013
- Allow Game Attributes to be usable as dropdown data for text attributes.
- Change how tile drawing is handled in Flash/HTML5 to remove unintentional scene size limit.
- Negative of a negative (XOR) on a sprite not working

May 12, 2013
- Only call updateBitmap on setFrame if the frame is different from the current
- [Fix] Clear logs would cause logs to fail to show up again.
- [Fix] "Cancel" when saving compiled file isn't handled
- [Fix] Behavior code disappears with "Actor Type" attribute. Stencyl 3.0

May 10, 2013
- Remove UDID usage from NME to comply with Apple's new guidelines.

May 9, 2013
- Add in 4.3 as a fake iOS version, so user who has newer SDK than devices have can still test

Sometime in the first week of May
- [Fix] Memory Leaks in the engine

April 21, 2013
- [Fix] Collision listener overwrites one contact with another if occurs at exact same time

April 16, 2013
- [Fix] Honor the iOS versions field, so that apps can build against SDK 6.0.
- [Fix] Duplicating then saving on game close corrupted duplicate resource.
- [Fix] Set volume not working for already playing sounds.
- [Fix] Show Layer broken
- [Fix] Animated Tileset editing doesn't save edit to correct frame.


April 15, 2013
- [Fix] Safeguard against thumbnails going lower than 1 pixel.
- [Fix] Background ID not assigned correctly.

April 9, 2013
- [Fix] Each sound play lowers volume if volume is not 100.
- [Fix] Brightness filter doesn't use percentages.

April 8, 2013
- [Fix] Anchored actor drawing.
- [Fix] Screen states not reset on recycle, causing screen events to fire early.
- [Fix] NaN error when simple physics actor uses gravity in Box2D mode
- [Fix] Recycled actor's collision boxes were placed in top left corner, causing collisions.
- [Fix] Anchored actor moved to another layer before being removed from anchor layer, causing double removal error.
- [Fix] Actor scripts initialized before being moved to layer, causing creation blocks to override layer/anchor blocks.

April 1, 2013
- [Fix] Duplicate scales when duplicating actor animation.
- [Fix] Delete extra scales for standalone if "Scale Dynamically" is chosen.
- [Fix] Prevent filters from breaking Windows/CPP output games.
- [Fix] Animation declared finished before completing final duration.

March 26, 2013
- [Fix] Layers drawn to on HTML5 not cleared unless drawn to again.
- [i18n] Begin localizing all the unlocalized strings in the app (there are about 700-800 of them) in order to bring Stencyl to 100% localizability.

March 24, 2013
- [i18n] Add Language Debug mode to show keys (helps translators out)
- [i18n] Update Language Packs (and pulls from the online tool)

March 23, 2013
- [Fix] Behaviors disabled before initialization don't go through initialization phase when enabled.

March 22, 2013
- [Fix] Prevent spinners from erroring due to value out of range

March 19, 2013
- [Fix] Animated tiles don't scale

March 18, 2013
- [Fix] External image editing with scaled images

March 11, 2013
- [Fix] Memory leak when changing scenes for Flash/HTML5
- [Fix] Circle -> Edge collisions.

March 9, 2013
- Add region support for Simple Physics.

March 5, 2013
- Add 3rd optional parameter to setScrollSpeedForBackground to apply to just 1 background
- [Fix] Duplicating actors / animation scaling bug
- [Fix] Sensor objects acting buggy for movement

March 1, 2013
- [Fix] Sensors Still Have Physical Collision

February 23, 2013
- [Fix] "random number between a and b" doesn't work as expected if a>b

February 21, 2013
- [Fix] Simple Physics actors in Box2D didn't use Hitbox settings.

February 18, 2013
- [Fix] Box2D Poly -> Edge collision bouncing

February 12, 2013
- [Fix] Deleting a scene will change which scene is marked as the starting scene

February 9, 2013
- [Fix] Adjustment for full screen mouse input affecting touch
- [Fix] Wrong indent on import statement formatting

February 7, 2013
- [Fix] Error when compiling Actor of Group Enters Screen Event

February 1, 2013
- Field for Android version code

January 31, 2013
- [Fix] Don't initialize hidden attributes at runtime (always keep default value)
- [Fix] `, ~ and # are escaped in behaviors but don't get converted back
- [Fix] Add adjacency info to edges for smooth transitions
- [Fix] Make Mac app's honor the mobile app title (for now - going to add a dedicated field in the future)

January 30, 2013
- Support for Poly <-> Edge collisions
- Wrapper comment block
- Use default values to initialize attributes

January 28, 2013
- Prep work for getting the Remote Builder back. It is NOT ready at this time though.

January 27, 2013
- [Fix] Make multi-touch work properly on iOS and Android (thanks JasonIrby!)
- Add a block to enable/disable gesture detection
- [Fix] Mac crashes on Lion and above when entering full screen mode
- [Fix] "Who uses this?" function not working correctly for scene behaviors
- [Fix] Full screen (web/desktop) mouse input can sometimes be incorrect
- [Fix] Can't seem to view print statements anymore in Log Viewer (particularly in Flash)

January 26, 2013
- [Fix] Edit frame (external) messes up image scale
- [Fix] Don't show error indicator for empty text fields in blocks
- [Fix] Code formatting messed up error highlighting
- [Fix] No sound selected in sound attribute setter causes empty code preview
- [Fix] Xcode 4.5.x doesn't output a certain phrase we're looking for when exporting IPAs, so detect one that does come.
- [Fix] Catch and give resolution to 'typeinfo' error (install cmd line tools, create symlink for clang)

January 25, 2013
- [Fix] Post to URL block
- [Fix] Remove deprecated menu items from View menu for behavior
- [Fix] Solve issue of errored behaviors sometimes opening up in XML
- [Fix] Honor the framerate field for mobile rather than hardcoding to 60/65

January 24, 2013
- [Fix] DDMS Launcher (debug menu)

_**(As of this point, Mac App Store exporting is working and verfified.)**_

January 23, 2013
- [Fix] Mac App Store Entitlements (again)
- [Fix] Tile API - auto-round row/col input

January 22, 2013
- [Fix] Scenes that reference non-existent tiles will fail to load
- [Fix] Mac App Store Entitlements

January 20, 2013
- Revamped Debug menu (in order to provide better self-support and support)
- Launch DDMS (Android) option
- Reinstall Android SDK option
- Install Java JDK option

January 19, 2013
- [Fix] Rotation in editor not rotate around origin point of actor - in android it does
- [Fix] Labels don't top-align on C++ targets.
- [Fix] Simple Physics + get/set gravity causes NPE

January 18, 2013
- [Fix] Having the 'disable hotkeys' enabled causes game build failure
- Improve in-app explanation of Sounds vs. Music.
- [Fix] Corrupt or non-existent game icon messes up game listing

January 17, 2013
- [Fix] iAd that fails to load can momentarily flash a blank/white banner
- [Fix] On iOS 6, landscape games display ads that don't stretch to fill the width of the screen

January 15, 2013
- Catch code sign errors and report them to the user
- [Fix] Further fixes to collision + tweening

January 14, 2013
- [Fix] How to disable particular collision shape or collision type for separate actor?
- Mark set blend mode blocks as Flash-only.
- [Fix] Tell user to install Haxe when exporting Xcode projects.
- [Fix] "touch is started" -> "mouse is pressed"
- [Fix] Convert "is running on iphone/ipad" blocks to the 3.0 equivalents.

January 13, 2013
- [Fix] Joystick dir/dist gives compile error on non-mobile targets
- [Fix] Various regressions from supporting 1.5x scale

January 9, 2013
- [Fix] Unable to create an attribute 
- [Fix] Better handling of case where Xcode directory needs to be switched to Application directory.
- [Fix] Null Reference with play sound in sound channel
- [Fix] 1.5x scale is missing 

January 8, 2013
- [Fix] Null object error when using Simple Physics
- [Fix] Hidden animation attribute still shows up in the inspector

January 7, 2013
- [Fix] Several changes to edit variable pane

January 6, 2013
- [Fix] Freeform code script name can include spaces, nor is the name utilized.
- [Fix] "Type name should start with an uppercase letter"

January 5, 2013
- [Fix] Exporting game does not warn if overwriting
- [Fix] Missing ) on draw rect block {cosmetic only}

_**(Cleaning house. Working on Renewals system and "deal")**_

January 2, 2013
- [Fix] Annotation Processing for 3.0
- [Fix] Save Game As overwrites existing file without warning

January 1, 2013
- [Fix] Freeform - Opened as ActionScript source file
- [Fix] Typo - ActionScript 3 -> Haxe

December 31, 2012
- [Fix] No warning when deleting animation
- [Fix] Freeform - First line is discarded
- [Fix] ClassCastException when Importing Game in Linux
- [Fix] Formatter not applied to all code in code preview (take 2)
- [Fix] Dates of Exported Games are all identical
- [Fix] Exporting game does not warn if overwriting
- [Fix] Can't export game on to different file systems

_**(Christmas -> New Year's Recess)**_

December 24, 2012
- [Fix] Make tweens end up at the exact target value.

December 23, 2012
- [Fix] Formatter not applied to all code in code preview

December 22, 2012
- [Fix] Parallax fields for backgrounds
- [Fix] Backgrounds not looping properly
- [Fix] Repeating Background bug
- [Fix] Flash will no longer freeze up when you print/trace too much at a time
- [Fix] Add keyboard entry for PERIOD (HTML5)
- [Fix] Make scene transitioning more lenient

December 21, 2012
- [Fix] Sync Tweens to the Engine

December 20, 2012
- [Fix] Fix issue with anchored actors + draw image for actor + camera scroll
- [Fix] Fix issue with anchored actors + draw text + camera scroll
- [Fix] Fix issue with switch frame + draw image for actor in Flash.
- [Fix] Properly reset graphics state before when drawing calls.
- [Fix] Fade layer to passes in incorrect alpha pct value
- [Fix] Touch Events don't work for simple physics
- [Fix] Copying and pasting a frame in a 2x or 1x animation makes the pasted frame grow
- [Fix] Slide to and by tweens

December 19, 2012
- [Fix] Honor opacity for "draw image for actor"

December 17, 2012
- [Fix] [Guard against NPE in actor custom draw to a non-existent layer](http://community.stencyl.com/index.php/topic,17602.0.html)
- [Fix] Honor opacity for text/labels

December 16, 2012
- [Fix] Neatly handle group <-> string comparisons (which are wrong but frequently made)
- [Fix] Multitouch ID block
- [Fix] Generate 96x96 icons to satisfy some app cases
- Actors on Screen block

December 15, 2012
- Set/Clear mobile keyboard text
- [Fix] Labels attached to actors with a width/height don't position properly.
- [Fix] Mouse Is Dragged event fires even when there is no movement
- [Fix] animation images wrapping to right

December 14, 2012
- [Fix] Local Windows -> iOS Builds - Fix Scale to Fit Mode
- [Fix] Local Windows -> iOS Builds - Fix Full Screen Mode
- [Fix] Local Windows -> iOS Builds - Show Icon
- [Fix] Tilesets are deleting themselves 
- [Fix] App Name field should be reflected in iOS app (not game name)
- [Fix] Remote build app name's are always "game"
- [Fix] Android version format issue
- [Fix] Actors getting getting corrupt in project (Take 2)

December 13, 2012
- [Fix, HTML5] Can't Point to 0
- [Fix] Multitouch event X and Y incorrect on some devices
- [Fix] enable App Sandbox for Mac apps

December 12, 2012
- Support for high-res joysticks (up to 4x)
- [Fix] Fully honor app version on iOS
- [Fix] Custom Drawing + Rotation = Buggy
- [Fix] ClassCastException when Importing Game in Linux
- [Fix] FPS monitor off screen in Flash Player in some cases
- [Fix] Set LSApplicationCategoryType for mac apps

December 11, 2012
- Update bundled Flash Player to 11.x
- [Fix] Exit region detection could introduce duplicates. Filter out.
- [Fix] Don't delete OGG files when using game crusher.

December 10, 2012
- [Fix] Honor app version

December 9, 2012
- [API] Add functions to get/set animation frame durations
- [Fix] Scene loading fix
- [Fix] Right-click events pane should refer to the moused over row

December 8, 2012
- [Fix] "e" mathematical constant

December 7, 2012
- [Fix] NPE when trying to comment out atlases

December 6, 2012
- [Fix] Grow Tween
- [Fix] Set x/y in simple physics

December 5, 2012
- [Fix] Follow up fixes to simple physics
- [Fix, SIMPLE PHYS] side of collision
- [Fix] Actors spawn in corner
- [Fix] Change Android install location from preferExternal to auto to avoid app rejection on Nook store.

December 3, 2012
- [Fix, Simple Physics/Lightweight] Actors appear "offset" if they're touching another actor due to faulty collision detection.

December 1, 2012
- Tween Number Block
- [Fix] Errors in behaviors mention a "null" behavior a lot of the time
- [Fix] load/unload atlas block can't accept number attributes
- [Fix] Conflict when saving atlas property for Actors
- [Fix] Repeat Background fix
- [Fix] Some fonts truncate in game

November 30, 2012
- Polygonal Terrain
- Polygonal Regions
- Animated Backgrounds (non-scrolling)
- [Fix] Joystick set x/y couldn't accept number attributes
- [Fix] NPE in Simple Physics
- [Fix] Region casting error for circular regions

November 29, 2012
- [Fix] In some cases, lists could be uninitialized (null)
- [Fix] ArrayIndexOutOfBounds when opening Tileset from Forge
- [Fix] Simple Physics, set x, y position blocks cause collision issues
- [Fix] Fixes to Atlas picking, especially if you add/remove some
- New debug menu options
- [Fix, Flash] If image is over 2880x2880, it fails to load in Flash. Gracefully fall back in-game.
- [Fix] Recycling Fix for "kill leave actor" in when created
- [Fix] Icon can reset to default under some circumstances
- [Fix] Scene Loading - Invalid Cast
- [Fix] Null Sound Playback - Invalid Cast
- [Fix] Correct rotation of ipad splashes

November 28, 2012
- Consolidate icon support for all platforms and require a 1024 x 1024 icon
- Modernize the Game Settings page when viewed from game settings
- Modernize the "Web" page for Game Settings
- Make printing the Actor Type return just the name

November 25, 2012
- Specify the resize method for imported graphics
- [Fix] Actor anchored to screen will draw relative to the scene rather than itself
- [Fix] Duplicating actor doesn't transfer some physics settings.
- [Fix] "kill leave screen" inside when created prevents actors from respawning

November 24, 2012
- [Fix] Invalid Cast in switchAnimation()
- [Fix] NPE in switchAnimation()
- [Fix] Fixed issue with atlas dropdown referencing atlases improperly.
- [Fix] Corrupting Actors [Mike]
- [Fix] Edit frame (external) messes up image scale [Mike]
- [Fix] When I update a frames duration, the graphic shrinks [Mike] 

November 22, 2012
- Only switch the animation shape if it's different from before. (Fixes nasty collision bug)
- Timed Tasks on actor behaviors/events should auto-mount to actor, rather than lastcreatedactor.

November 21, 2012
- Catch cryptic insufficient memory error on Android
- [Fix] Prevent deleted actor types from being read in for scenes
- Catch missing Xcode / wrong directory case
- [Fix] iOS - Starting a purchase before prior was complete would crash.

November 20, 2012
- [Fix] Repeat + Scrolling backgrounds
- [Fix] Actor Offscreen Behavior
- [Fix] Actors spawn in corner when switching scenes
- Remove Publish item from toolbar (dialog was inconsistent with Publish menu)
- [Fix] Apply basic default values to event-based attributes. (num, bool, text)
- Upsize the default icon to 144 x 144.
- [Fix] Fix stage size on mobile full screen mode games (also fixes camera issues)
- [Fix] Boolean name inconsistencies
- [Fix] Animation Syncing turned off by default (will become a setting)
- [Fix] Add a setting for synchronizing animations
- Remove the Accelerometer FPS field

November 19, 2012
- [Fix] Fix NPE in actor collision handling
- [Fix] typed text block for Mobile Keyboard Event was the wrong type
- [Fix] Keyboard detect [ and ]
- [Fix] font switch slowdown bug
- [Fix] Auto-resize ads (for iOS 6 compliance)

November 18, 2012
- iPhone 5 Splash Screen
- Mobile Keyboard Events
* when keyboard is shown
* when keyboard is hidden
* when keyboard is typed
* when keyboard is submitted
Should be sufficient to create text-field like functionality and more. Works on iOS - Android not yet.

November 17, 2012
- Mobile Ad Positioning
- [Fix] Game Center Leaderboard crash on iOS 5/6
- [Fix] Set offscreen tolerance doesn't accept number atts

November 16, 2012
- In-App Purchases for Android

November 14, 2012
- Update the What's New? dialog
- Fix up iPad Landscape splash screens

November 13, 2012
- [Fix] Respect the isPausable property for actors.
- [Kit] Drop Block Kit updated to 3.0 standards
- [Kit] Jump & Run Kit updated to 3.0 standards
- [Kit] Shooter Kit updated to 3.0 standards
- [Kit] Balloons Kit updated to 3.0 standards
- Export to Single EXE demoted to debug option (false positive AV scans)
- Linux 64-bit Support
- [Fix] Enter transitions of 0 duration keep the screen black

November 12, 2012
- [Fix] Make platform dropdown not have scrollbars
- [Fix] Make attribute type dropdown not have scrollbars
- [Fix] Font stroke color is none is problematic (save problems, inaccurate preview)
- [Fix] Make simulate key press/release properly trigger events
- [Fix] Kill any timed-tasks connected to actors when those actors are killed

November 11, 2012
- [Fix] Exported Android app was assuming wrong location
- [Fix] Tile API fixed for simple physics
- [Fix] Auto-Init a blank list for events with list attributes
- [Fix] Actor recycling should reset speeds (simple physics) and actor values.

November 10, 2012
- [Fix] iOS Accelerometer fix
- [Fix] Region click is off by a half dimension
- Honor the default import scale when importing graphics
- Honor the default import scale when drag and drop graphics

November 9, 2012
- [Fix] Wrapping width fix for labels extension @ high scales
- [Fix] Force replace block's params to be strings
- [Fix] Force convert set camera location to ints
- [Fix] Off-screen calculation for actors is off
- [Fix] Divide-by-zero error for games with 0 resources (for standalone/mobile)
- Add Preference item for default import scale
- Allow published games to show FPS monitor and debug draw

November 8, 2012
- Fix local ios exporting
- [Fix] Fill Pixel block
- [Fix] Timed tasks continue to "run" while app is backgrounded (not really but it appears that way)
- [Fix] Prevent freezing from happening when you background and resume an app after a long time
- [Fix] multi-touch x/y blocks now report in 1x
- [Fix] Fix regression in circle collisions

November 5, 2012
- Fix for Parallax Scrolling Background
- Fix - Duplicate Tiles frame when importing
- Fix - Game doesn't auto-save when testing

November 4, 2012
- Remote Builds are finally operational for 3.0
- Enable 4x mode in engine (if device is iPad 3/4)

October 31, 2012
- [Fix] Fix to single-EXE exporter.

October 30, 2012
- [Fix] Prevent Flash player from running when there's a compiler error (happens only on Windows)
- Auto-delete older versions of app in iOS simulator before running.
- [Fix] Circle collisions report halved coordinates

October 29, 2012
- [Fix] Don't sync non-looping animations otherwise they'll always be on the final frame to start
- [Fix] Work around asNumber issue caused by bug in Haxe's C++ generator.
- [Fix] Work around issues with clearValue and how its code is generated for non-Flash targets

October 28, 2012
- High-Res Graphics Importing returns to functional form
- Re-enable 4x graphics importing
- [Fix] Was accidentally reusing lists when recycling. Fixed.
- [Fix] Auto-initialize list to blank if none is provided in editor.
- [Fix] Make animations share timing.

October 27, 2012
- [Fix] Force "part of text"'s blanks to be integers
- [Fix] Force character at's blank to be an integer
- [Fix] Regression with has value block
- [Fix] Gracefully handle missing extensions
- [Fix] Update tile map when using Tile API
- [Fix] Fixes to internalgetgroup (inherit groupID from parent actor)
- [Fix] Catch "contains 2 projects" error
- [Fix] Fix choppy scrolling on slower devices / platforms
- [Fix] Honor the font smoothing property. But looks awful for most fonts when off.
- [Fix] Site Locking
- [Fix] Games with no graphical assets don't run
- [Fix] Spotlight transitions wanted ints for some reason - switch to floats
- [Fix] Group-group event for html5

October 26, 2012
- Update version number to 3.0.0 / b1000
- Delete 1.5x graphics on iOS
- Delete 4x graphics on Android
- [Fix] Clip screen bounds on non-mobile targets
- [Fix] Auto-Cast attribute setters to numbers
- [Fix] Fix enable/disable actor drawing
- [Fix] Fix up the "has value" block
- [Fix] Fix up the "clear value" block
- [Fix] Set remote attribute when attribute is an object and is currently null fails on C++ targets

October 25, 2012
- Fix Xcode 4.5 support for iOS Simulator
- Fix Xcode 4.5 support for Device testing
- Detect if Android certificate details are missing and bump user to page
- [Fix] Simple physics - actors cannot be anchored to screen (Gravity issue)
- [Fix] Simple physics - Can't make actor ignore gravity
- [Fix] Simple physics - x coordinate is off

October 24, 2012
- Up Android certificate validity to 50 years
- Export Android release APK, not Android debug APK
- [Win8] Fix case of checking for Windows 8 SDK when you already have it but don't have a dev license yet

October 23, 2012
- Create a test extension showing how to import external SWF/SWC libraries for Flash
- [Mobile] Scale Mode that uses only 1x graphics and dynamically scales up, instead of using hi-res graphics. Good for retro games.
- [Win 8 publishing] Search for 64-bit path if on a 64-bit system
- [Win 8 publishing] Visit Stencylpedia when Windows 8 publishing fails due to the SDK not being installed
- [Win8] Don't allow spaces in app names

October 22, 2012
- [Fix] scale to fit breaks if the background = scene dimensions (due to div by 0)
- Support standalone app icons
- [Fix] Custom blocks that return text

October 21, 2012
- [Fix] Fixed layering issues that could occur if you deleted layers and made new ones in the scene designer.
- [Fix] Fixed bug where moving an actor between layers would fail since it thought it was moving to the same layer.
- [Fix] Recycled actors not showing non-default animations
- [Fix] Fix up scene behavior group-group collision event
- [Fix] Recycling actors that are always active leads to strange behavior
- [Fix] Follow up fix to group - group collisions
- [Fix] On screen checks fail when camera scrolls in > 1x games
- [Fix] Fix mouse detection for scaled actors
- [Fix] Set proper volume when playing a clip
- [Fix] Fix fade tween + recycling not resetting to 100% opacity
- [Fix] Background placement
- [Fix] Force setx/y for actors to only work with ints

October 20, 2012
- [Fix] Metadata-free sounds were failing to import
- [Fix] Music player doesn't reset button states after finishing playback
- [Fix] Music player doesn't reset button states after pressing the reset button

October 19, 2012
- StencylForge Revamp for 3.0
* Hide 1.x/2.x Games, Kits, Behaviors, Actors, Packs from 3.0
* Hide 3.0 Games, Kits, Behaviors, Actors, Packs from 1.x/2.x
* New Landing Page
* Re-enable uploading games to StencylForge
- [Fix] get font width/height should return in 1x terms, not in absolute (current scale) terms
- [Fix] Game Center - Submit score required cast to int
- Remove list casting blocks (they are no longer needed)
- [Fix] Guard against engine trying to access a non-existent layer

October 18, 2012
- FPS counter for HTML5
- [Fix] Type cast error for actor enters screen event
- [Fix] catch a class cast error that happens when loading actor types in scene that no longer exist
- [Fix] UTF-8 support for exported resources
- [Fix] touched actor block wasn't properly converting
- [Fix] Pausing should freeze motion too
- [Fix] Pausing wasn't suspending actor motion in Box2D
- [Fix] Don't auto-cast game attribute getters (was causing unnecessary errors)
- [Fix] HTML5 text drawing
- [Fix] Text drawing in screen space actually happens in scene space
- [Fix] Custom drawing in > 1x scale games (including retina) would draw incorrectly
- [Fix] Detect metadata in imported sounds

October 17, 2012
- Toggle for Graphics Scale mode (use hi-res gfx vs. scale from 1x graphics)
- Android Keystore / Certificate Generator
- Redo the Android Certificates page
- [Fix] Mobile Full Screen Mode wasn't working on larger resolution devices
- [Fix] Default font was always drawing at 1x even on higher scale games

October 16, 2012
- Brand New Sound Editor
- Import multiple formats per sound. Use OGG to enable proper sound playback on desktop targets.
- [Fix] Can now play multiple (non-music) sounds on desktop without then overriding each other.
- [Fix] Region reading fix

October 15, 2012
- [Fix] Simple Physics mode is fixed up for the most part
- [Fix] Scaled Debug Drawing

October 13, 2012
- [Win 8] Set Splash Background color
- [Win 8] Set Tile Image
- [Win 8] Set Splash Image
- [Win 8] Catch missing information before building and jump to page for entering this info in
- [Win 8] Auto-detect the Win 8 sdk path if it's installed. If can't find it (and we know it isn't installed), prompt for it.
- [Win 8] Proper HTML5 app template.
- Make an extension block's View Help option go to author's site
- Improve the Add Attribute dialog
- [Fix] Unknown bug with actors and atlases causing failure to build
- Foregrounds
- Let user choose between a single EXE or a bundle

October 12, 2012
- Windows 8 / Windows Store Exporting (first cut)

October 11, 2012
- [Fix] Restrict Windows Store exporting to Windows 8
- [Fix] Tweaks to Android installer for Linux
- [Fix] Specifying Android certificate was preventing that from building

October 10, 2012
- [API] setScrollSpeedForBackground
- [Fix] Add Atlas fix to default name

October 9, 2012
- Add/Remove atlases
- [Fix] Run Garbage Collection immediately after unloading atlases, so memory is freed up.

October 8, 2012
- [Fix] HTML5 sound playback now works when testing
- [Fix] Standalone app crash when sound ends and you switch scenes at the same time

October 7, 2012
- [Fix] Could only play 32 sounds. After that, nothing plays
- [Fix] Effects marked as "sound" are now preloaded
- [Fix] Android sounds can now loop
- [Fix] Using UTF-8 characters in DM, closing resource and reopening would show garble
- [Fix] Copying & Pasting UTF-8 blocks in DM would show garble
- [Fix] Copying & Pasting UTF-8 blocks as image in DM would show garble
- [Fix] Fix to Windows local iOS building

October 6, 2012
- Single EXE Packaging for Windows
- Antialias Setting (Under Settings > Settings)
- [Fix] Running app on Android device that's currently asleep (pretty much all the time?)

October 5, 2012
- ["Atlases"](http://community.stencyl.com/index.php/topic,15012.0.html)
- Auto-Scaling Bodies
- Disable tracing on published targets (web-only - NME bug for C++ targets)

October 4, 2012
- Mobile Preloader
- iOS Splash Screens (+ support iPhone 5 style splash screen)
- Support UTF-8 characters in design mode
- Support UTF-8 characters for text drawing
- Labels Extension (cross-platform, more fully featured than the old behavior from 2.x)

October 3, 2012
- Specify Android Certificate (under Settings > Mobile > Certificates)
- is running on iphone/iphone5/ipad block
- Make Pencyl an optional module, unbundle Smultron from Mac builds
- [Fix] Game Center is initialized syntax error in block

October 2, 2012
- Engine Extensions
- Tile API is now an engine extension
- Created Test and Native Test extensions
- Detect whether Visual Studio is installed (so it doesn't ask twice)
- [Fix] Multi-touch reporter block was designated to return actor rather than number

September 30, 2012
- Publish to the Mac App Store
- Stencyl is now signed for Mountain Lion, so you won't get the Gatekeeper error anymore.
- Enable/Disable Debug Drawing toggle in Run menu
- New Event: Multi-Touch

September 29, 2012
- Tile API
- Site Lock
- Preloader Click URL
- Custom SWF Preloader
- [Fix] Choosing special web preloaders will no longer prevent non-web targets from running
- [Fix] Various Web Preloader fixes
- [Fix] Import/Export over an existing game was buggy
- [Fix] Fixes to origin points
- [Fix] Debug Drawing (Box2D Mode)
- [Fix] Simultaneously spin/slide is buggy

September 28, 2012
- [Mobile] Dual Virtual Joysticks
- [Fix] CPMStar is now working
- Remove the Actor is touchable setting (no longer needed)

September 27, 2012
- [Fix] Fixes to full screen mode
- [Fix] Honor mobile app name.
- [Fix] Honor animation loop setting.
- [Fix] Make 2.x code mode behaviors openable in 3.0
- [Fix] Mouse-Touch-Actor blocks weren't regarding camera location
- [Fix] Move to Layer functionality
- [Fix] Hide unmarked languages from prefs dropdown
- [Fix] substring not implemented in C++ targets
- [Fix] Custom Drawing Fixes to screen space, actor space, draw image and more
- [Fix] Don't allow anchored actors to change layers

September 26, 2012
- Full Screen Mode
- Set Blend Mode for Actor and Layer (by ID)
- Toggle FPS Monitor (under Run)
- Partial Retina Display support for the toolset itself
- [Fix] set attribute wasn't setting if the field wasn't initially populated
- [Fix] Switch Frame block

September 25, 2012
- [Mobile] Vibrate
- [Mobile] Show Alert
- [Mobile] Set icon badge number (iOS)
- [Mobile] Swipe Detection & Events
- [Mobile] Show/Hide the Keyboard
- [Mobile] Make mobile keyboard spew out keyboard events (iOS & Android)
- [Mobile] Set Certificates/Profile on a per-game basis

September 24, 2012
- [Fix] Scaling Problems with 1X vs 2X
- [Fix] Opening and closing games causes compiling to slow down
- [Fix] substring block was start->len rather than start->end
- [Fix] list contains block
- [Fix] Gracefully handle frameless animations. Fix some errors related to them.
- [Fix] Don't require user to change and resave fonts to upgrade them
- [Fix] Don't require user to press enter to confirm collision shape changes.

September 23, 2012
- Test iOS apps on Windows without remote builds
- [Fix] Fixes to the Windows iOS building to honor orientation, platform-identification, full screen, and more.
- [Fix] Windows iOS building now catches common errors and reports them.
- [Fix] grow tween fix

September 21, 2012
- [Fix] iAds touch implementation fix
- [Fix] Catch MP3 encoding errors and present to user.
- [Fix] Present a more helpful error message if game fails to load at startup.
- Inserted stub for purchase info. Not re-implemented yet.

September 20, 2012
- AdWhirl support for Android - Includes AdMob and House Ads.
- Published games hide console/fps monitor and make no logs.
- Auto-convert single touch to mouse blocks.
- [Fix] Implement GET/POST block
- [Fix] Anchored actors still show up after scene change
- [Fix] ClassCastException in AdWhirl extension
- [Fix] Allow for-each to iterate over lists that are elements of lists
- [Fix] White Background Color becomes transparent on Browser
- [Fix] Properly honor the "No Color" and Solid Color -> None choices

September 17, 2012
- Blocks for referring to the product, board, achievement ID.
- [Fix] Game Center extension swapped events for success/failed score submission
- [Fix] HTML5 target explicitly excludes .scn files, or else older browsers complain
- [Fix] Honor the bundleID for Android

September 16, 2012
- Events for Ads
- Events for Game Center
- Events for In-App Purchases

September 15, 2012
- Improved logging functionality for Flash and iOS simulator

September 14, 2012
- In-App Purchases (Non-Consumable, Consumable, Restoration)
- I think the freezing bug in the app is fixed.
- Fixed relative path error in NME.

September 13, 2012
- Full Newgrounds API and preloader support
- Game Center (first cut)
- Fixes to regressions

September 10-12, 2012
- Initial iAd support
- Transition fixes
- Xcode Export Fixes

September 9, 2012
- (Nearly) Universal Log Viewer
- Make the HTML5 test page nicer.
- [Fix] Saving for HTML5 now works.
- [Fix] Get HTML5 target running on Firefox 14 < again.
- Auto-convert old blocks to new forms.
- Run all iOS apps on device in Release mode
- iOS - Display "Sending to Device" to tell user that that's happening
- More proactive error detection
- Be more proactive in killing external processes after we're done with them

September 8, 2012
- Brand new maze game sample. Redownload using link in first post.
- Clean up palette.
- Fix - Camera scrolling now works for scales > 1x
- Fix - Show preloader background on HTML5
- Fix - C++-based platforms sometimes didn't detect certain key presses
- Fix - Simulate key press/release wouldn't work on C++ based targets for certain keys
- Fix - Mobile - mouse pressed on actor required 2 clicks to be detected
- Fix - [DM] Block picker sometimes does not work
- Fix - [DM] Right-click not on a block does not work
- Fix - For Each Actor Type error when sought type has no instances
- Change default scale choices back to 1x/2x.

September 7, 2012
- do only on <PLATFORM> block
- is running on <PLATFORM> block
- Removed touch-specific events because we folded them into mouse events
- Fix - Can't set screen resolution in new game dialog
- Fix - camera follow actor is broken
- Fix - Linux HTML5 now launches

September 6, 2012
- Honor user-defined icons
- Fix for non-subscribers with access to beta
- Set ANDROID_HOST flag on all platforms
- Fix path issue on Linux to get Flash target working
- Fix tile drawing for game scales > 1x on desktop and mobile targets
- Fix for bug with HUD actors + click/touch once camera is off origin

September 5, 2012
- Mochi Preloader
- Newgrounds Preloader (but disabled due to error)
- CPMStar Preloader
- Newgrounds API / Blocks (but disabled due to error)
- [FIX] HTML5 target now runnable again
- [FIX] Flash MP3 fix
- [FIX] Rotated actors flipped 180 degrees on Flash, HTML5 and Android.

September 4, 2012
- Remove AS3 and Objective-C code preview pages.
- Kongregate blocks
- Mochi blocks

September 3, 2012
- Fixed Mac App publishing for 10.6 and below.
- Ctrl + Q now closes a Mac App.
- Fix for Windows users running most targets. 'Program Files' causes it to fail in many cases due to space in name.

September 2, 2012
- Upgraded to NME 3.4.2 as the base SDK. Lots of changes and improvements. [See this topic for the changes and caveats.](http://community.stencyl.com/index.php/topic,13602.0.html)

August 31, 2012
- [FEATURE] Redid the Android SDK installer. Should be a lot more robust.

August 30, 2012
- [FEATURE] [MUCH faster building for native and mobile targets.](http://community.stencyl.com/index.php/topic,13603.0.html)
- [FEATURE] Redownload Caches (for feature above)
- [FEATURE] Clean Project
- Improvements to the Live Log Viewer (clear logs, copy to clipboard)
- [FIX] Fix to :Error: Source path "Export/android/obj/libApplicationMain.so" does not exist

August 29, 2012
- [FIX] Set JAVA_HOME explicitly on Mac and exhaustively search all Java locations to locate the JDK.

August 28, 2012
- [FIX] Compiler errors not involving behaviors (for example, involving StencylPreloader) no longer generate a tool-based error and properly report the culprit class.
- [FIX] Changing from scene with joint would lock up game.
- [FIX] Don't begin an Android build accidentally while installing the SDK or JDK.
- [FIX] Fix Mac/Linux Android NDK file location. Delete any folders mentioning "android" under ext-tools/ as well as ext-tools/apache-ant/
- [FEATURE] Console Viewer (under debug menu)
- [FIX] Use bundled Flash player rather than file associated one (like Flash Professional)


=====

Initial Version

[Big Things]
- Test and Publish to Flash, HTML5, iOS, Android, native Desktop and Chrome.
- Choose between Box2D and a simple box-based collision engine.
- Even web/desktop games can now run at higher scales using "retina" graphics
- Brand new HaXe-based engine. Can use code on all platforms.

[Smaller Things]
- Controls can now be mapped to multiple keys.
- All iOS publishing happens locally, if you're on a Mac.
- Touch and Mouse input are merged.
- Fonts now support custom character sets.
- No requirement to use Atlases if you hate 'em.
- Localizers: We've broken up the language files into many smaller ones to make it easier to tackle.

