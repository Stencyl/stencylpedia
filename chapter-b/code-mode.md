
Stencyl supports Code Mode, a way to write behaviors entirely using code (currently, Haxe).

This article surveys the interface and explains how to accomplish crucial tasks, such as defining attributes through annotations.

 
## Contents

* The Basics
* The Interface
* Using External Editors
* Switching Between Design and Code Mode
* How to Define Attributes
* The Future
 
## The Basics

You have three options to write code in Stencyl:

* Use **code blocks** in **Design Mode** behaviors. This is this easiest option to include short pieces of code in your behaviors.  
* Create behaviors written in code in **Code Mode**. 
* Write arbitrary classes in **Freeform Mode**.

This article is about the latter two options. Code Mode behaviors are just like normal behaviors, you can attach them to your scenes and actors. For a scene behavior, write a class that extends SceneScript; for an actor behavior, write a class that extends ActorScript. You can also define attributes in Code Mode behaviors (explained later in this article).

In Freeform Mode, you can write arbitrary classes. They are not behaviors, so you cannot define attributes or attach them to your scenes or actors. In order to make use of a Freeform Mode class, you will need to call the code from another behavior.

## The Interface

![stencyl-ide-code-mode-pic](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-b/images/code-mode-ui.png)
 

### Top Tool Bar

![stencyl-ide-code-mode-toolbar-pic](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-b/images/code-mode-toolbar.png)

This area has three separate buttons: Refresh Attributes, Open in External Editor, and View API.

* **Refresh Attributes:** This updates the attributes in your Behavior by running an annotation parser over it. (Only available in Code Mode.)
* **Open in External Editor:** This allows you to use an IDE of your choosing, such as Eclipse, Notepad++, FlashDevelop, etc.
* **View API:** Lets you view Stencyl's Haxe API.
 

### Attributes Pane

The Attributes Pane stores all attributes currently defined by this behavior. To define attributes, you have to annotate them. Scroll down to the **How to Define Attributes** section below for further details.

In Freeform Mode you cannot define attributes, so this area does not exist.

 
### Editing Area

In this area you write your code. Syntax highlighting and find/replace are supported. For more advanced features, use an external editor.

![stencyl-ide-code-mode-editing-area-pic](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-b/images/code-mode-editarea.png)

 
## Using External Editors

Stencyl plays nicely with external editors such as Notepad and FlashDevelop.

**Configure this setting inside (File > ) Preferences > Workspace**. It will open up the editor on demand and auto-sync the changes when you save in that external editor.

![stencyl-code-mode-using-an-external-ide](https://static.stencyl.com/help/images/PencylPreferencesPic.png)
 

## Switching Between Design and Code Mode

At this point in time, we don't support switching between these two modes. A behavior is designated as always being in one or another and cannot be changed after the fact.

If you want to mix the two, you need to make a design mode behavior and stick in code blocks.

 
## How to Define Attributes

In order to expose a class member for a Code Mode Behavior as a configurable attribute, you need to annotate it. This is using the [Metadata](https://haxe.org/manual/lf-metadata.html) feature of the Haxe language. The easiest way to learn the syntax is by example.

```haxe
//Expose your attributes like this:
@:attribute("id='1' name='Display Name' desc='A Text Attribute'")
public var attributeName:String;

@:attribute("id='2' name='My Color' desc='A Color Attribute' type='color'")
public var color:Int;

@:attribute("id='3' name='Action 1' desc='A Control Attribute' type='control'")
public var action1:String;

// The "type" property can be in uppercase too, like a constant
@:attribute("id='1' name='Move Speed' desc='A Number Attribute' type='NUMBER' default='20.0'")
public var moveSpeed:Float;
``` 

### Accepted Properties
 

Name     | Description	                                   | Required?
-------- | ---------------------------------------------- | ---------
id       | Must be a unique integer                       |	Yes
order    |	What order it appears in the Behavior page     |	No
desc     | Display name on the Behavior page              |	Yes
dropdown | Name=Value pairs for Dropdowns                 |	No
type     | Use this if specify the type of your attribute |	Yes, for certain types
default  | Default value for the attribute                | No

The type is necessary for attributes that don't have a distinct type in Haxe. For example a Control is stored as a String, the same type used for Text attributes. So to define a Control attribute without ambiguity, you need to provide the type parameter. The parameter is case-insensitive.

> Note: After exposing a new attribute to a behavior, you need to reload the scenes or actors to which the behavior is attached for the changes to take effect.

The following types are supported, listed with the corresponding type in Haxe.

Attribute Type | Haxe Type
-------------- | ---------
ACTOR      			 | Actor
ACTORGROUP		   | Group
ACTORTYPE	   	 | ActorType
ANIMATION		    | String
BOOLEAN		    	 | Bool
COLOR		      	 | Int
CONTROL			     | String
FILTER			      | Dynamic
FONT			        | Font
IMAGE			       | BitmapData
IMAGE_INSTANCE	| BitmapWrapper
INT				        | Int
JOINT			       | B2Joint
LIST			        | Array<Dynamic>
MAP				        | Map<String,Dynamic>
NUMBER			      | Float
OBJECT			      | Dynamic
REGION		     	 | Region
SCENE			       | Scene
SHADER			      | Dynamic
SOUND			       | Sound
TEXT		       	 | String


## The Future

Down the road, we'd like to significantly enhance the coding experience. The best way is to improve integration of code with external editors rather than trying to build better (but still inferior) support into Stencyl itself.

For the time being, sending code mode behaviors to an external editor of your choosing is the best way to edit code in Stencyl.
