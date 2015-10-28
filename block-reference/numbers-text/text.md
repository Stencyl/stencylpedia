# Numbers & Text > Text

***

## Conversion

### Convert to Text

![convert-text-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Conversion.png)

Converts the given value to text.

```
("" + [VALUE])
```

***

## Operations

### Text Length

![length-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/TextLength.png)

Returns the number of characters in the given text.

```
[TEXT].length
```

***

### Combine Text

![combine-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Operations_TextAdd.png)

Combines the two given pieces of text into one and returns that result.

```
[TEXT] + [TEXT]
```

***

### Trim Text

![trim-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Operations_TrimSpace.png)

Removes spaces at the end of the given text.

```
StringTools.trim([TEXT])
```

***

## Comparison

### Equals (Text)

![equals-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_Equality.png)

Returns `true` if both pieces of text are exactly the same.

```
([TEXT] == [TEXT])
```

***

### Is Text Empty?

![empty-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_Empty.png)

Returns `true` if the length of the given text is 0.

```
([TEXT] == "")
```

***

### Does Text come before/after?

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

### Find Character

![char-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_Character.png)

Returns the character at the given position. Note that the first index in a text is 0, not 1. Throws a runtime error if the given position is out of bounds.

```
[TEXT].charAt([NUMBER])
```

***

### Get Text Position

![textpos-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_Index.png)

Returns the index at which the given phrase (or character) appears in the given text. Returns -1 if the phrase is not found.

> **Example:** The word "dog" corresponds to these indices: d = 0, o = 1 and g = 2. If you selected the letters "og" from the word "dog" (enter "og" in the field on the left and "dog" in the field on the right), the result would be 1.

```
[TEXT].indexOf([TEXT])
```


***

### Replace Text in Text

![replace-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_ReplaceBlock.png)

Replaces one phrase with another within the given text.

> **Example:** <br/>![replace-example](http://static.stencyl.com/pedia2/blocks/numbers_text/text/FindExample1.png)<br/>Returns `cheeseburger`

```
StringUtil.replace([TEXT], [TEXT], [TEXT])
```

***

### Substring (Part of Text)

![substring-block](http://static.stencyl.com/pedia2/blocks/numbers_text/text/Find_Substring.png0

Returns part of the given text, given the starting and ending indices. More specifically, this block returns the characters beginning with the **start index** and ending with **one less than** the **ending index**. 

> **Example:** The word "cats" corresponds to these indices: c = 0, a = 1, t = 2, s = 3. If you enter "cats" in the field on the left, and 1, 3 as your starting and ending index numbers, the block would return the letters "at", i.e. the letters that correspond to the index numbers 1 and 2 in the word "cats."

```
[TEXT].substring([NUMBER], [NUMBER])
```

***

## Case

***

## Split

***

## Fonts

***
