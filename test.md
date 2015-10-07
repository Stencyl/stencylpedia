## Dialog Extension Command Reference

For general info and help regarding Dialog Extension tags, see the Appendix sections:

- [About Commands](#about_cmds)
- [About Command Arguments](#about_cmd_args)
- [Referring to Attributes](#ref_to_atts)

### Dialog Options

###### choice

`<choice [[optionText:String dialogID:String condition:Bool] ...]>`

Display a list of options for the player to choose from.

```example
Where would you like to go today?
<choice [
	["The Pool" "Pool Part 1"]
	["Back Home" Home]
	["Mars" "Space Center" <getattr [game "Space Unlocked"]>]
]>
//Selecting "The Pool" will take you to a dialog called "Pool Part 1"//
//"Back Home" takes you to a dialog called "Home"//
//"Mars" will go to "Space Center", but it's only shown if the game attribute "Space Unlocked" is true.//
```

***

### Extra Glyphs

###### glyph

`<glyph image:String>`

Includes an image in your dialog, inline with the text.

```example
I love you!! <glyph heart>
//Displays the image "heart.png" from the extras folder after the text "I love you!!"//
```

***

### Character Scripts

###### showname

`<showname name:String>`

Displays a character name + namebox

```example
<showname Lenny>
//Display the name Lenny in a namebox//
```

###### hidename

`<hidename>`

Removes the namebox.

###### face

`<face image:String>`

Display a character face/portrait.

```example
<face Lenny>
//This actually depends on the preference you have set for this extension. Assuming faceImagePrefix="Face ", this would show image "Face Lenny.png" from your extras folder//

<face none>
//Removes the face graphic//
```

***

### Flow Scripts

###### waitattr

`<waitattr [ATTR value:Dynamic]>`

Dialog will wait for some attribute to reach a value before proceeding.

```example
<waitattr ["game" "Cutscene Ongoing" false]>
//Will wait until the game attribute, "Cutscene Ongoing", becomes false before continuing with the dialog.//
```

See [Referring to Attributes](#ref_to_atts)

###### wait

`<wait time:Float>`

Inserts a pause into the dialog.

```example
<wait .5>
//Dialog will be paused for half a second before continuing.//
```

###### but

`<but>`

Shows a pointer and waits for user input.

```example
Oh, hello!<but> My name is Chuck.<but> And what's yours?<but>
//The player has to press the continue button, set in this extensions prefs, in order to continue the dialog at the three <but> points. Careful, this example is probably overkill as far as causing stops in the dialog.//
```

###### bc

`<bc>`

Like `<but>` but when dialog continues, the dialog box is automatically cleared.

***

### Logic

```
<if condition:Bool>
<elseif condition:Bool>
<else>
<endif>
```

Control what's seen and what isn't. Personalize messages, or give the player valuable info based on his current status in the game.

```example
<if <getattr [game "Dragon 1 Defeated Again"]>>We'll be forever in your debt, hero! Allow me to give you a special discount...
<elseif <getattr [game "Dragon 1 Defeated"]>>The legends say that the dragon will come back with a vengeance for he who sealed him... I hope it's just hearsay.
<else>Business is sure good with the dragon around, warying the townsfolk, but I have to keep an eye on my stock, make sure it doesn't steal anything.
<endif><dg "General Shop">
```

From the place you enter an `<if>` tag, it can be followed by multiple `<elseif>` tags and then a single `<else>` tag if desired.
Eventually, it has to be followed by an `<endif>` tag so that the dialog system knows where to resume normal dialog.

***

### Messaging Scripts

###### setattr

`<setattr [ATTR value:Anything]>`

Sets an attribute.

```example
<setattr [actor Player "Health Behavior" _health 100]>
```

###### getattr

`<getattr [ATTR]>`

This tag is primarily intended for use WITHIN other tags, if you want to refer to some value that can't be expressed normally in this dialog editor.

```example
//Because <getattr> is useful within other tags, let's start an example with another tag.//
<setattr [actor Player "Target Behavior" _currentTarget ...]>
//The actor we've identified as "Player" has "Target Behavior" attached. The above code will set the value of "_currentTarget" in "Target Behavior" to whatever is represented by the ellipses [...]//

//Let's fill it in with a "Boss" actor that we've previously placed in a Game Attribute called "Boss 2".//
<setattr [actor Player "Target Behavior" _currentTarget <getattr [game "Boss 2"]>]>
```

###### showattr

`<showattr [ATTR]>`

This takes the text representation of some attribute and inserts it into this position in the dialog.

```example
WOW! YOU'VE SAVED UP <showattr [game "Rupees"]> RUPEES!! AWESOME!
//...I guess that's supposed to be a Majora's Mask banker reference?//
```

###### messagescene

`<messagescene behaviorName:String message:String [argument:Anything ...]>`

Sends a message to a scene behavior attached to the current scene.

###### messageactor

`<messageactor actorName:String behaviorName:String message:String [argument:Anything ...]>`

Sends a message to an actor.

See [Referring to Attributes](#ref_to_atts)

***

### Skip Scripts

###### skip

`<skip>`

This enables the ability to skip text by holding the text skipping buttons if it was previously disabled.

###### noskip

`<noskip>`

Disables ability to skip through text. Maybe use it for a cutscene when timing of the dialog is crucial.

***

### Sound Scripts

###### playsound

`<playsound sound:String>`

Plays a sound.

```example
<playsound "Howl"><wait .1> ! ? ! <wait .5> Did you hear that??<but>
```

###### loopsound

`<loopsound sound:String>`

Loops a sound. Like above, but can be used for ambient BG sounds or music.

###### stopsound

`<stopsound>`

Stops currently playing sounds.

###### playchan

`<playchan sound:String channel:Int>`

Plays sound on a specific channel.

###### loopchan

`<loopchan sound:String channel:Int>`

Loops sound on a specific channel.

###### stopchan

`<stopchan channel:Int>`

Stops sounds on a specific channel.

***

### Dialog Base

###### clear

`<clear>`

Clears the content of the dialog box. Typing begins again at the top left corner.

###### close

`<close>`

Closes the dialog box, but doesn't remove it completely, so you can use it again without adding the dialog box back into the Dialog system.

###### end

`<end>`

Closes Dialog Box and removes it from Dialog System.

###### dg

`<dg dialogID:String>`

Opens up another Dialog Chunk.

```example
<dg Shop>
//Opens up a dialog script named #Shop in dialog.txt//
```

***

### Text Effects

###### shake

```
<shake>
</shake>
```

Begin and end the text vibration effect.

###### sine

```
<sine>
</sine>
```

Begin and end the text sinewave effect.

###### rotate

```
<rotate>
</rotate>
```

Begin and end the text revolve effect.

###### grow

```
<grow>
</grow>
```

Begin and end the text grow effect.

***

### Typing Scripts

###### font

`<font fontName:String>`

Change the Font used to type dialog. Use "none" for Stencyl default.

###### color

`<color colorCode:Int>`

Change the color of the font. -1 for default font color, or hexadecimal int in r-g-b order, such as (#ff0000) or (0xff0000) for pure red.

###### typespeed

`<typespeed speed:Float>`

Change the type speed of the dialog. 0.1 would case a character to be typed ever 10th of a second.

###### typesound

`<typesound sound:String>`

or

`<typesound [sound:String ...]>`

Change the sound that plays when a character is typed, or set it to "none" for no sound.
Using the second tag, you can provide a list of sounds, one of which will be played at random when a character is typed.

***
<a name="about_cmds"></a>

## About Commands

<commandName arguments ...>

Evaluated as they're encountered in the dialog.

***
<a name="about_cmd_args"></a>

## About Command Arguments

A **String** is normally enclosed in quotes, but if you only have one word, it's okay to omit the quotes.

```example
soup // becomes "soup" (one string) //
"soup" // becomes "soup" (one string) //
"good soup" // becomes "good soup" (one string) //
good soup // becomes "good" "soup" (two strings) //
```

A **List** is a pair of brackets with space-separated values.

```example
<setattr [dialog myList [Value1 Value2 Value3 [Value4 Is A List]]]>
```

A **Bool** is either `true` or `false`. (All characters lower-case.)

An **Int** is a whole number with no decimals, like `10`. A **Float** may contains decimals, like `.5`.

**Anything**: Can be a String, Int, Float, Bool, or List.

***
<a name="ref_to_atts"></a>

## Referring to Attributes

Any tag that expects the "ATTR" argument is actually expecting a list of arguments, depending on the attribute type.
Attribute type is specified as the first argument.

To refer to an actor from within dialog, the actor must first be registered with the Dialog Extension by executing the following code: `GlobalActorID.set("Name of Actor", _ActorAttribute);`. Then, that actor can be accessed from dialog tags by "Name of Actor".

- Game Attribute: `game gameAttributeName:String`
- Scene Behavior Attribute: `scenebhv behaviorName:String attributeName:String`
- Actor Behavior Attribute: `actorbhv actorName:String behaviorName:String attributeName:String`
- Actor Property: `actor actorName:String actorValueName:String`
- Dialog Attribute: `dialog attributeName:String` (only available for "Messaging Scripts" tags)
