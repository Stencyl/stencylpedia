Earlier in this chapter, [you learned about Attributes](http://www.stencyl.com/help/view/attributes/), which are changeable and configurable properties of Behaviors. What kinds of Attributes are at your disposal?
 

## Reference - The Types

Stencyl includes the following resource types.
 
Type | Stencylpedia Article?
--- | --- | ---
Actor | [Yes](http://www.stencyl.com/help/view/what-are-actors/)
Actor Group | [Yes](http://www.stencyl.com/help/view/collisions-and-groups/)
Actor Type | [Yes](http://www.stencyl.com/help/view/what-are-actors/)
Animation | [Yes](http://www.stencyl.com/help/view/animations/)
Anything | --- 
Boolean | ---
Collision Shape | [Yes](http://www.stencyl.com/help/view/collisions-and-groups/)
Color | ---
Control | [Yes](http://www.stencyl.com/help/view/controls/)
Font | [Yes](http://www.stencyl.com/help/view/font-editor/)
Image | [Yes](http://www.stencyl.com/help/view/image-api)
Image Instance | [Yes](http://www.stencyl.com/help/view/image-api)
List | [Yes](http://www.stencyl.com/help/view/lists/)
Joint | ---
Map | [Yes](http://www.stencyl.com/help/view/maps/)
Number | ---
Region | [Yes](http://www.stencyl.com/help/view/regions/)
Scene | [Yes](http://www.stencyl.com/help/view/scene-basics/)
Shader | [Yes](http://www.stencyl.com/help/view/shaders/)
Sound | [Yes](http://www.stencyl.com/help/view/playing-sounds-and-music/)
Text | ---


## What do the attribute configurators look like?

Here are some examples of common Attribute types and how they may appear on an Actor Type’s Behaviors page.

Attribute Type | Appearance in Actor Type Editor > Behaviors
--- | ---
Actor Group | ![stencyl-design-mode-actor-group-attribute](http://static.stencyl.com/pedia2/ch2/types/image00.png)
Actor Type | ![stencyl-design-mode-actor-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image03.png)
Animation | ![stencyl-design-mode-animation-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image01.png)
Boolean | ![stencyl-design-mode-boolean-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image04.png)
Color | ![stencyl-design-mode-color-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image07.png)
Control | ![stencyl-design-mode-control-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image11.png)
Font | ![stencyl-design-mode-font-type-attribute](http://static.stencyl.com/help/images/Font-Attribute-Pic.png)
Number | ![stencyl-design-mode-number-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image05.png)
Scene | ![stencyl-design-mode-scene-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image02.png)
Sound | ![stencyl-design-mode-sound-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image10.png)
Text | ![stencyl-design-mode-text-type-attribute](http://static.stencyl.com/pedia2/ch2/types/image06.png)

 
## Gotchas

Something you might bump into fairly early on is shown in the following image:

![Cannot configure](http://static.stencyl.com/pedia2/ch4/customize/image05.png)

Why are some Attributes unconfigurable?

* There's nothing to configure, or the configurator would be of limited value. (e.g. Image Instance, Shader)
* It's an Actor behavior, so until the actor's actually inside a scene, there's no context for being able to pick out a specific (Actor or Region)

For the latter case, this can be addressed by [customizing the Actor](http://www.stencyl.com/help/viewArticle/117/) once it's inside a scene.

