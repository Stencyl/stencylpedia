> **Call for Help:** This article is out of date. Want to help us rewrite it? [Head over to Github](https://github.com/Stencyl/stencylpedia/blob/master/chapter-b/code-mode.md) and submit edits to this article.

Stencyl supports Code Mode, a way to write behaviors entirely using code (currently, Haxe).

This article surveys the interface and explains how to accomplish crucial tasks, such as defining attributes through annotations.

 
## Contents

* The Interface
* Using External Editors
* Switching Between Design and Code Mode
* How to Define Attributes
* The Future
 

## The Interface

![stencyl-ide-code-mode-pic](http://static.stencyl.com/help/images/CodeModeUI1.png)
 

### Top Tool Bar

![stencyl-ide-code-mode-toolbar-pic](http://static.stencyl.com/help/images/CodeModeUI2.png)

This area has four separate buttons, Check Syntax, Refresh Attributes, Open in External Editor, and View API.

* **Check Syntax:** This checks your code's syntax for errors.
* **Refresh Attributes:** This updates the attributes in your Behavior by running an annotation parser over it.
* **Open in External Editor:** This allows you to use an IDE of your choosing, such as Eclipse, Notepad++, FlashDevelop, etc.
* **View API:** Lets you view Stencyl's ActionScript-based API.
 

### Attributes Pane

The Attributes Pane stores all attributes currently defined by this behavior. To define attributes, you have to annotate them. Scroll down to the **How to Define Attributes** section below for further details.

 
### Editing Area

This area is split in to two sections, one where you add new code, and the other area that shows compiler output when you press Check Syntax.

Syntax highlighting and simple code completion are supported, as well as find/replace.

![stencyl-ide-code-mode-editing-area-pic](http://static.stencyl.com/help/images/CodeModeUI4.png)

 
## Using External Editors

Stencyl plays nicely with external editors such as Notepad and FlashDevelop.

**Configure this setting inside Preferences > Workspace**. It will open up the editor on demand and auto-sync the changes when you save in that external editor.

![stencyl-code-mode-using-an-external-ide](http://static.stencyl.com/help/images/PencylPreferencesPic.png)
 

## Switching Between Design and Code Mode

At this point in time, we don't support switching between these two modes. A behavior is designated as always being in one or another and cannot be changed after the fact.

If you want to mix the two, you need to make a design mode behavior and stick in code blocks.

 
## How to Define Attributes

In order to expose a class member for a Code Mode Behavior as a configurable attribute, you need to annotate it. The easiest way to learn the syntax is by example.

```
//Expose your attributes to Stencyl like this
[Attribute(id="1", name="Display Name", desc="An Attribute")]
public var attributeName:String = "default";
``` 

### Accepted Properties
 

Name | Description	| Required?
--- | --- | ---
id | Must be a unique integer |	Yes
order |	What order it appears in the Behavior page |	No
desc | Display name on the Behavior page |	Yes
dropdown | dropdown data |	No
type | Use this if you are defining a Control, Animation, Effect or Game Attribute attribute and set to "control" "animation" "effect" or "game-attribute" |	Yes, for certain types

### The Types
 
    Int
    Number
    Object
    String
    Boolean
    Actor
    Group
    ActorType
    Color
    Control
    Animation
    Font
    Effect
    GameAttribute
    Joint
    Region
    SoundClip
    Scene
    Array

> **TODO:** This list was drafted for 2.0 / ActionScript and may not be correct in 3.0 / Haxe.
 

## The Future

Down the road, we'd like to significantly enhance the coding experience. The best way is to improve integration of code with external editors rather than trying to build better (but still inferior) support into Stencyl itself.

For the time being, sending code mode behaviors to an external editor of your choosing is the best way to edit code in Stencyl.
