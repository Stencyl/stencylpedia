# Numbers & Text > Text

***

## Conversion

### <a name="tostring"></a> Convert to Text

![convert-text-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Conversion.png)

Converts the given value to text.

```
("" + [VALUE])
```

***

## Operations

### <a name="str-length"></a> Text Length

![length-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/TextLength.png)

Returns the number of characters in the given text.

```
[TEXT].length
```

***

### <a name="str-combine"></a> Combine Text

![combine-block](http://static.stencyl.com/pedia2/block-images/4%20-%20Numbers%20%20Text/2%20-%20Text/str-combine.png)

Combines the two given pieces of text into one and returns that result.

```
[TEXT] + [TEXT]
```

***

### <a name="str-trim"></a> Trim Text

![trim-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Operations_TrimSpace.png)

Removes spaces from the beginning and the end of the given text and returns that result. (When given an attribute, the value of the attribute remains unchanged.)

```
StringTools.trim([TEXT])
```

***

## Comparison

### <a name="eq"></a>  Equals (Text)

![equals-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_Equality.png)

Returns `true` if both pieces of text are exactly the same.

```
([TEXT] == [TEXT])
```

***

### <a name="str-empty"></a> Is Text Empty?

![empty-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_Empty.png)

Returns `true` if the length of the given text is 0.

```
([TEXT] == "")
```

***

### <a name="str-beforeafter"></a> Does Text come before/after?

![before-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_Before.png)
![after-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_After.png)

Returns `true` if the first given text alphabetically comes before (or after) the second given text.

```
//A comes BEFORE B
strCompare([TEXT], [TEXT], -1);

//A comes AFTER B
strCompare([TEXT], [TEXT], 1);
```

***

## Find / Replace

### <a name="str-char-at"></a> Find Character

![char-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_Character.png)

Returns the character at the given position. Note that the first index in a text is 0, not 1. Throws a runtime error if the given position is out of bounds.

```
[TEXT].charAt([NUMBER])
```

***

### <a name="str-indexof"></a> Get Text Position

![textpos-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_Index.png)

Returns the index at which the given phrase (or character) appears in the given text. Returns -1 if the phrase is not found.

> **Example:** The word "dog" corresponds to these indices: d = 0, o = 1 and g = 2. If you selected the letters "og" from the word "dog" (enter "og" in the field on the left and "dog" in the field on the right), the result would be 1.

```
[TEXT].indexOf([TEXT])
```


***

### <a name="str-replace"></a> Replace Text in Text

![replace-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_ReplaceBlock.png)

Replaces one phrase with another within the given text.

> **Example:** <br/>![replace-example](http://static.stencyl.com/pedia2/blocks/numbers_text/text/FindExample1.png)<br/>Returns `cheeseburger`

```
StringUtil.replace([TEXT], [TEXT], [TEXT])
```

***

### <a name="str-substring"></a> Substring (Part of Text)

![substring-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_Substring.png)

Returns part of the given text, given the starting and ending indices. More specifically, this block returns the characters beginning with the **start index** and ending with **one less than** the **ending index**. 

> **Example:** The word "cats" corresponds to these indices: c = 0, a = 1, t = 2, s = 3. If you enter "cats" in the field on the left, and 1, 3 as your starting and ending index numbers, the block would return the letters "at", i.e. the letters that correspond to the index numbers 1 and 2 in the word "cats."

```
[TEXT].substring([NUMBER], [NUMBER])
```

***

## Case

### <a name="str-toupperlower"></a> Get Text in Upper/Lower Case

![uppercase-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/CaseUp.png)
![lowercase-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/CaseLow.png)

Returns the given text in all uppercase (or lowercase).

```
[TEXT].toUpperCase()
[TEXT].toLowerCase()
```

***

## Split

### <a name="str-split-space"></a> Split into Words

![split-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Split.png)

Splits the given text up into a [list](http://www.stencyl.com/help/view/lists/), using **space** as the separator (delimiter).

```
[TEXT].split(" ")
```

***

### <a name="str-split"></a> Split using Separator

![split-block2](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Split2.png)

Splits the given text up into a [list](http://www.stencyl.com/help/view/lists/), using the given separator (delimiter) text.

```
[TEXT].split([TEXT])
```

***

## Fonts

### <a name="get-font-width2-new"></a> Get Width of Text using Font

![text-width-block](http://static.stencyl.com/pedia2/block-images/4%20-%20Numbers%20%20Text/2%20-%20Text/get-font-width2-new.png)

Returns the width of the given text using the given font. Useful for calculating positions for drawing text.

```
[FONT].font.getTextWidth([TEXT])
```

***

### <a name="get-font-height2-new"></a> Get Height of Font

![text-height-block](http://static.stencyl.com/pedia2/block-images/4%20-%20Numbers%20%20Text/2%20-%20Text/get-font-height2-new.png)

Returns the height of the given font. Useful for calculating positions for drawing text.

```
[FONT].getHeight()
```

***
