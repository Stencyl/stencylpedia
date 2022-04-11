> **Note:** This article does not talk about how to draw text. [We've got an article for that](https://www.stencyl.com/help/viewArticle/119/).

## Contents

* Introduction
* Font Types
* Creating Bitmap Fonts
* Creating Regular Fonts
 

## Introduction

Our Font Editor lets you import or create fonts for use in your games when drawing text. Fonts are considered as resources in Stencyl. Therefore, to open up the Font Editor, you either need to create a new Font, download one from StencylForge, or open an existing one up from the Dashboard.

 
## Font Types (Regular vs. Bitmap)

There are two kinds of Fonts you can create and use in Stencyl: Regular Fonts and Bitmap Fonts.

**Regular Fonts** work like the ones you use when word processing. They are based on TrueType (TTF) fonts. They're easy to set up, but they aren't very customizable, and they can take up a lot of space. We offer Regular Fonts for convenience.

![Regular Font](https://static.stencyl.com/v3/images/announcement/regular-font.png)

**Bitmap Fonts** on the other hand are based off images that you import. They take more effort to set up, but they  look better and take up less space.

![Bitmap Font](https://i.imgur.com/jLhLFQY.png)

> **Tip:** Stencyl doesn't provide tools to build the images behind bitmap fonts. We recommend using [AngelCode](http://www.angelcode.com/products/bmfont/) or [Hiero](https://code.google.com/p/libgdx/wiki/Hiero) to assist you in creating Bitmap Fonts.


## Creating Bitmap Fonts


### What are Bitmap Fonts?

Often, game developers would like to import a font as an image they created themselves or in another program such as AngelCode. This enables fonts with visual effects and character sets that TrueType fonts don't support.

![Bitmap Font](https://static.stencyl.com/v3/images/announcement/bmfont1.png)

While Stencyl doesn't provide tools for creating bitmap fonts, it does provide extensive ways for importing the image and defining the individual character data.

![Bitmap Font Editor](https://static.stencyl.com/v3/images/announcement/bmfont2.png)


### How to Create a Bitmap Font

1. **File > Create New > Font**

2. Give the a font a name. Click OK.

3. **Click** the **Import Font from Image button** at the top-right to switch to the Bitmap Font Editor.

  ![Import Font](https://static.stencyl.com/v3/images/announcement/bmfont3.png)

4. Import an image for your font.

  ![Import Image for Font](https://static.stencyl.com/pedia2/misc/font/import-image.png)

5. Define characters for your font as described in the next section.

 
### Workflow

After you've imported the backing image for the bitmap font, you'll need to tell Stencyl where each individual character is.

1. First, add a character (or multiple characters).

2. Then, adjust the character's position using one of these methods.

  * Drag and drop to move the character's box around.
  * Use the arrow keys to move the box around.
  * Use the text fields on the right to adjust the values manually.
 
### What the Properties Mean

Name | Purpose
--- | ---
**Position (X/Y)** | The left/top position of the character's image in the backing image.
**Size (Width/Height)** | The width/height of the character's image in the backing image.
**Offset (X/Y)** | Padding applied to the left/top side of a character when drawn.
**Right-Padding** | Padding applied to the right side of a character when drawn.

### Shortcuts

Importing many characters can be tedious. Use these shortcuts to speed up the process.

Command | Purpose
--- | ---
**SHIFT + Up/Down/Left/Right** | Resize the currently selected character.
**ALT + Up/Down** | Select the previous/next character in the list.

Together with the ability to nudge a character up/down/left/right with the arrow keys, these let you define a character's position and size with the keyboard.

### Other Properties
The Edit Properties button will bring up a few additional options.

![Letter Spacing](https://static.stencyl.com/pedia2/misc/font/props.png)

Name | Purpose
--- | ---
**Space (Width)** | Since you can't define space as a character, this lets you define how wide a "space" character should be.
**Line Height** | Specifies how many pixels to jump to the next line when wrapping text inside a label.
**Letter Spacing** | It can be tedious to specify padding for each character if it's going to be the same. This lets you set a global value for padding that is added to each character's right-padding value.
**Background (Color)** | lets you set the background color in the editor for easier editing. It has no effect in-game.<br/><br/>![Background Color](https://static.stencyl.com/pedia2/misc/font/bg.png)

### External Tools

As mentioned earlier, Stencyl doesn't provide tools for creating the bitmap fonts themselves. Skilled artists can make a bitmap font on their own using Photoshop or similar tools. To create a bitmap font based off a regular, TrueType font, consider using one of the following programs.

[Angelcode](http://www.angelcode.com/products/bmfont/) - A popular, Windows-only font editor.

[Hiero](https://code.google.com/p/libgdx/wiki/Hiero) - A cross-platform font editor.

> **Tip**: Looking for pre-made bitmap fonts - try [DaFont.com](http://www.dafont.com/bitmap.php)? Please respect the licensing terms of these fonts if using them in games.

 

## Creating Regular Fonts

### Overview
Regular fonts are based on TrueType fonts, the same ones you use when composing an e-mail or document. Although your options for styling them are limited, they are easy to set up and use in your game as long as you understand their limitations.

### How to Create a Regular Font
1. **File > Create New > Font**.
2. Give the a font a name.
3. Click OK. You'll now be inside the Font Editor.

### Workflow
1. Choose the **Charset** (short for character set). This defines what characters are included in the font. Choose the minimum set you need.
2. Choose the font face you'd like to use or import your own TTF.
3. Set other properties as you see fit.
4. Save. The system will churn for a bit as it generates the font's image behind the scenes.

 
###Style Properties

![Style Properties](https://github.com/Stencyl/stencylpedia/blob/master/chapter-b/images/style-properties.png)

Name | Purpose
--- | ---
**Character Set** | Choose what characters to include in this font. Choose the minimum set you need.
**Characters** | Only used when Charset is Custom and should contain all the custom characters needed.
**Font** | The kind of font you'd like to use, or import a TTF to use.
**Size** | The font size
**Style** | Bold, Italic, Both, or Normal
**Smoothing** | Choosing no will make the font appear aliased, which is useful for pixely looking fonts. (however, if you are making pixely looking fonts, we strongly recommend using a Bitmap Font instead!)
 

###Color Properties

![Font Color Properties](https://static.stencyl.com/help/images/fontColor.png)

Name | Purpose
--- | ---
**Color** | Select any color for your font. Clicking on the option opens the color chooser window.
**Gradient Color** | Lets you blend the first and second colors together vertically in your font.
**Gradient Offset** | Lets you decide how low or how high the gradient color should be, affecting the intensity of the blend.
 
###Stroke
The stroke option allows you to highlight your font with a specific color and at a specific magnitude.

![Stroke](https://static.stencyl.com/help/images/fontPreviewStroke.png)

###Shadows
Adding a shadow effect creates a copy of the drawn text with that font, offset x and y pixels away, and blurred at a specific magnitude. This is used to make the characters appear three-dimensional due to the depth between the text and the shadow. Below is an example of basic settings for a shadow effect.

![Shadows](https://static.stencyl.com/help/images/fontPreviewShadow.png)

> **Limitation:** You cannot set both a shadow and a stroke at the same time. If you need this, consider generating a Bitmap Font using an external tool and importing that in instead. See the "External Tools" section of this article for recommendations.
