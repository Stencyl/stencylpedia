> **Extending Stencyl**

> Engine ([Basics](http://www.stencyl.com/help/view/how-to-create-engine-extension/) - [iOS & Android](http://www.stencyl.com/help/view/how-to-create-native-engine-extension/) - [Flash](http://www.stencyl.com/help/view/flash-extensions/) - [Blocks](http://www.stencyl.com/help/view/adding-blocks/) - [API](http://static.stencyl.com/api/33/))

> Toolset ([Extensions](http://www.stencyl.com/help/view/creating-extensions/) - [API](http://api.stencyl.com/extensions/))


## Introduction

This is the spec for blocks.xml, the file used to add custom blocks to an extension. 


## Example (for reference)

Suppose that we wanted to remake the `print` block. This is what the definition would look like.

![](http://static.stencyl.com/pedia2/blocks/flow/flow_debug/Print.png)

Don't worry about the details for now. This will be useful to refer back to as you read through this article.

```
<palette>
  <block tag="print" spec="print %0" code="System.print(~);" type="action" color="gray" returns="void">
    <fields>
      <text order="0"></text>
    </fields>
  </block>
</palette>
```


## Adding a Block

`<palette>` is the root tag for the document -- it contains a list of `<block>` entries. 

```
<palette>
    <block></block>
    <block></block>
    <block></block>
</palette>
```

To **add** a block, add a `<block>` tag with the following properties.

Property | Description
--- | ---
tag | Unique name for block, only ABC and - (dash) allowed (no spaces!)
spec | Like what you see in our language files, use %0, %1, etc. to specify where the spaces go
code | Output code, use ~ to specify the blanks. Must match the order in which fields are specified.
type | Any of these [normal, action, wrapper, event]
color | Any of these [blue, cyan, green, lime, purple, red, gray, charcoal]
returns | A **type** (see available types below)

For example...

```
<block tag="print" spec="print %0" code="System.print(~);" type="action" color="gray" returns="void"></block>
```


## Types

These are the available types you can use for the **returns** property of `<block>` and the list of `<fields>`.

* void (does not apply to `fields`)
* actor
* actortype
* boolean
* camera
* color
* control
* font
* group
* number
* list
* anything
* region
* scene
* sound
* text
* dropdown (does not apply to `returns`)


## Fields

Each `<block>` contains `<fields>` as a child. `<fields>` is a list of block fields (the blank spaces in a block).

```
<block tag="print" spec="print %0" code="System.print(~);" type="action" color="gray" returns="void">
  <fields>
    <text order="0"></text>
  </fields>
</block>
```

Each child of `<fields>` is a tag, whose name corresponds to a type (the ones mentioned above). For example, if you want to make a number field, the tag would be `<number>`.


## Ordering Fields

Fields are ordered using `order` attribute, starting at zero and incremented by 1. Don't skip numbers.

```
<fields>
  <text order="0"></text>
  <text order="1"></text>
  <text order="2"></text>
</fields>
```


## Dropdown Fields

If you wish to use a dropdown, look at the example below for syntax.

The `text` attribute specifies what's visible to the end user.
The `code` attribute specifies the literal value that will be output into code.

```
<dropdown order="1">
  <choices>
    <c text="Pressed" code="1"></c>
    <c text="Released" code="2"></c>
  </choices>
</dropdown>
```


## Limitations

* No support for embedded blocks (such as those you see attached to events).
* No support for events.
