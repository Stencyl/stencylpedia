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


## Introduction

This is the spec for blocks.xml, the file used to add custom blocks to an extension. 

> **Note:** Making changes to **blocks.xml** requires you to close and reopen the game for your changes to be reflected in the block palette.
> 
> **Credit:** Thanks to ETHproductions for documenting this feature. We've based portions of this guide on his [forum guide](https://community.stencyl.com/index.php/topic,39934.0.html).


## Example (for reference)

Suppose that we wanted to remake the `print` block. This is what the definition would look like.

![](https://static.stencyl.com/pedia2/blocks/flow/flow_debug/Print.png)

Don't worry about the details for now. This will be useful to refer back to as you read through this article.

```xml
<palette>
  <block tag="print" spec="print %0" code="System.print(~);" type="action" color="gray" returns="void">
    <fields>
      <text order="0"/>
    </fields>
  </block>
</palette>
```


## Adding a Block

`<palette>` is the root tag for the document -- it contains a list of `<block>` entries. 

```xml
<palette>
    <block></block>
    <block></block>
    <block></block>
</palette>
```

To **add** a block, add a `<block>` tag with the following properties.

**REQUIRED**

Property | Description
--- | ---
tag | Unique name for block, only ABC and - (dash) allowed (no spaces!)
spec | Like what you see in our language files, use %0, %1, etc. to specify where the spaces go
code | Output code, use ~ to specify the blanks. Must match the order in which fields are specified.
type | Any of these [normal, action, wrapper, event]
returns | A **type** (see available types below)

**OPTIONAL**

Property | Description
--- | ---
help | Displayed in the bottom bar when the mouse hovers over this block.
color | Any of these [blue, cyan, green, lime, purple, red, gray, charcoal, yellow]
hidden | If `true`, the block will not display in the palette. Used in conjunction with **attached-block**
helpURL | If included, this is the url that will be opened by the **View Help** action on the block.<br/>Otherwise, it'll go to the site in the info.txt file.

**EXAMPLE**

```xml
<block tag="print" spec="print %0" code="System.print(~);" type="action" color="gray" returns="void"></block>
```


## Types

These are the available types you can use for the **returns** property of `<block>` and the list of `<fields>`.

* actor
* actortype
* animation
* anything
* boolean
* color
* control
* filter
* font
* group
* image
* image-instance
* joint
* list
* map
* number
* region
* scene
* shader
* sound
* text
* void (only applies to `returns`)
* dropdown (only applies to `fields`)
* code-block (only applies to `fields` - see explanation under **Code Blocks**)
* attached-block (only applies to `fields` - see explanation under **Attached Blocks**)

![](https://static.stencyl.com/pedia2/chapter-d/all-types.png)


## Input Fields

Each `<block>` contains `<fields>` as a child. `<fields>` is a list of **block input fields** (the blank spaces in a block).

```xml
<block tag="print" spec="print %0" code="System.print(~);" type="action" color="gray" returns="void">
  <fields>
    <text order="0"/>
  </fields>
</block>
```

Each child of `<fields>` is a tag, whose name corresponds to a type (the ones mentioned above). For example, if you want to make a number field, the tag would be `<number>`.


## Ordering Fields

Fields are ordered using `order` attribute, starting at zero and incremented by 1. Don't skip numbers.

```xml
<fields>
  <text order="0"/>
  <text order="1"/>
  <text order="2"/>
</fields>
```


## Dropdown Fields

If you wish to use a dropdown, look at the example below for syntax.

The `text` attribute specifies what's visible to the end user.
The `code` attribute specifies the literal value that will be output into code.

```xml
<block tag="number-dropdown" spec="%0" code="~" type="normal" returns="number">
  <fields>
    <dropdown order="0">
      <choices>
        <c text="Pressed" code="1"/>
        <c text="Released" code="2"/>
      </choices>
    </dropdown>
  </fields>
</block>
```


## Attached Blocks

Attached Blocks are the embedded blocks in wrapper blocks that are meant to be used only within the context of the wrapper block.

![](https://static.stencyl.com/pedia2/chapter-d/save-example.png)

Here's how you define one.

* First, define the inner (embedded) block. It must be **above** the definition for the wrapper.

* Set the inner block's `hidden` attribute to `true`, so it won't show up in the palette.

* Add an `<attached-block>` field to the wrapper block definition.

* Inside the tag for `<attached-block>`, add a `tag` attribute whose value is the tag for the inner block.

Here's an example of this in action.

```xml
<block tag="save-successful" spec="save successful" code="success" type="normal" returns="boolean" hidden="true">
	<fields/>
</block>

<block tag="save-game" spec="save game and then... %1" code="saveGame('mySave', function(success:Bool){~});" type="wrapper" returns="void">
	<fields>
		<code-block order="0"/>
		<attached-block order="1" tag="save-successful"/>
	</fields>
</block>
```


## Code Blocks

This is a special type of `field` that can only show up inside a wrapper block (such as if). It has nothing to do with literal code and is used to allow a wrapper block to contain a bunch of fields before the wrapped stack of blocks is accepted (in other words, this field always comes last).

```xml
<block tag="if" spec="if %0" code="if (~) {~}" type="wrapper" returns="void">
	<fields>
		<boolean order="0"/>
		<code-block order="1"/>
	</fields>
</block>
```


## Translation

It's possible to provide the blocks.xml file in multiple languages.

Include a file in your extension folder at `lang/{locale code}/*.lang`. It doesn't matter what the `.lang` file is called. For example, to include English, Spanish, and Russian:

```
extension/
- blocks.xml
- lang/
  - en/
    - my-extension.lang
  - es/
    - my-extension.lang
  - ru/
    - my-extension.lang
```

The format of the .lang files is the same as Stencyl's .lang files: `key=value` pairs.

For each block, you can translate the `spec` and `help` properties. Additionally, you can specify that dropdown choices are translated by starting them with `@`.

Here's an example block, being taken from the original English-only block, to a new, translatable block.

Original:
```xml
<block tag="my-dropdown-example" spec="set my dropdown to %0" code="var myDropdown = ~;" type="action" returns="void" help="A simple example block to show translation.">
  <fields>
    <dropdown order="0">
      <choices>
        <c text="a number" code="1"/>
        <c text="a boolean" code="true"/>
	<c text="a string" code="\"text\""/>
      </choices>
    </dropdown>
  </fields>
</block>
```

Translatable:
```xml
<block tag="my-dropdown-example" code="var myDropdown = ~;" type="action" returns="void">
  <fields>
    <dropdown order="0">
      <choices>
        <c text="@number" code="1"/>
        <c text="@bool" code="true"/>
	<c text="@string" code="\"text\""/>
      </choices>
    </dropdown>
  </fields>
</block>
```

Accompanying `lang/en/blocks.lang`:
```
my-dropdown-example=set my dropdown to %0
my-dropdown-example.help=A simple example block to show translation.

number=a number
bool=a boolean
string=a string
```

## Additional Reading

A more thorough reference is available [here](https://community.stencyl.com/index.php/topic,39934.0.html).
