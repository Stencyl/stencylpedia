# Numbers & Text > Text

***

## Conversion

### <a name="tostring"></a> Convert to Text

![object as text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/tostring.png)

Converts the given value to text.

```
("" + [VALUE])
```

***

## Constants

### <a name="str-emptystring"></a> Empty Text

![empty text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-emptystring.png)

Returns an empty text ("").

```
""
```

***

### <a name="str-space"></a> Space

![space](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-space.png)

Returns a space (" ").

```
" "
```

***

## Operations

### <a name="str-length"></a> Text Length

![text length](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-length.png)

Returns the number of characters in the given text.

```
[TEXT].length
```

***

### <a name="str-combine"></a> Combine Text

![text & text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-combine.png)

Combines the two given pieces of text into one and returns that result.

```
[TEXT] + [TEXT]
```

***

### <a name="str-trim"></a> Trim Text

![trim whitespace from text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-trim.png)

Removes spaces from the beginning and the end of the given text and returns that result. (When given an attribute, the value of the attribute remains unchanged.)

```
StringTools.trim([TEXT])
```

***

## Comparison

### <a name="eq"></a> Equals (Text)

![object = object](https://static.stencyl.com/pedia2/block-images/numbers-text/text/eq.png)

Returns `true` if both pieces of text are exactly the same.

```
([TEXT] == [TEXT])
```

***

### <a name="str-empty"></a> Is Text Empty?

![text is empty](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-empty.png)

Returns `true` if the length of the given text is 0.

```
([TEXT] == "")
```

***

### <a name="str-beforeafter"></a> Does Text come before/after?

![before-block](https://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_Before.png)
![after-block](https://static.stencyl.com/pedia2/blocks/numbers_text/text/Comparison_After.png)

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

![character at position int in text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-char-at.png)

Returns the character at the given position. Note that the first index in a text is 0, not 1. Throws a runtime error if the given position is out of bounds.

```
[TEXT].charAt([INT])
```

***

### <a name="str-indexof"></a> Get Text Position

![index of text in text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-indexof.png)

Returns the index at which the given phrase (or character) appears in the given text. Returns -1 if the phrase is not found.

> **Example:** The word "dog" corresponds to these indices: d = 0, o = 1 and g = 2. If you selected the letters "og" from the word "dog" (enter "og" in the field on the left and "dog" in the field on the right), the result would be 1.

```
[TEXT].indexOf([TEXT])
```

***

### <a name="str-replace"></a> Replace Text in Text

![replace text with text in text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-replace.png)

Replaces one phrase with another within the given text.

> **Example:** <br/>![replace-example](https://static.stencyl.com/pedia2/blocks/numbers_text/text/FindExample1.png)<br/>Returns `cheeseburger`

```
StringTools.replace([TEXT], [TEXT], [TEXT])
```

***

### <a name="str-substring"></a> Substring (Part of Text)

![part of text start int end int](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-substring.png)

Returns part of the given text, given the starting and ending indices. More specifically, this block returns the characters beginning with the **start index** and ending with **one less than** the **ending index**.

> **Example:** The word "cats" corresponds to these indices: c = 0, a = 1, t = 2, s = 3. If you enter "cats" in the field on the left, and 1, 3 as your starting and ending index numbers, the block would return the letters "at", i.e. the letters that correspond to the index numbers 1 and 2 in the word "cats."

```
[TEXT].substring([INT], [INT])
```

***

## Case

### <a name="str-toupperlower"></a> Get Text in Upper/Lower Case

![uppercase-block](https://static.stencyl.com/pedia2/blocks/numbers_text/text/CaseUp.png)
![lowercase-block](https://static.stencyl.com/pedia2/blocks/numbers_text/text/CaseLow.png)

Returns the given text in all uppercase (or lowercase).

```
[TEXT].toUpperCase()
[TEXT].toLowerCase()
```

***

## Split

### <a name="str-split-space"></a> Split into Words

![split text into words](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-split-space.png)

Splits the given text up into a [list](https://www.stencyl.com/help/view/lists/), using **space** as the separator (delimiter).

```
[TEXT].split(" ")
```

***

### <a name="str-split"></a> Split using Separator

![split text using separator text](https://static.stencyl.com/pedia2/block-images/numbers-text/text/str-split.png)

Splits the given text up into a [list](https://www.stencyl.com/help/view/lists/), using the given separator (delimiter) text.

```
[TEXT].split([TEXT])
```

***

## Fonts

### <a name="get-font-width2-new"></a> Get Width of Text using Font

![get width for text using font](https://static.stencyl.com/pedia2/block-images/numbers-text/text/get-font-width2-new.png)

Returns the width of the given text using the given font. Useful for calculating positions for drawing text.

```
[FONT].font.getTextWidth([TEXT], [FONT].letterSpacing)/Engine.SCALE
```

***

### <a name="get-font-height2-new"></a> Get Height of Font

![get height using font](https://static.stencyl.com/pedia2/block-images/numbers-text/text/get-font-height2-new.png)

Returns the height of the given font. Useful for calculating positions for drawing text.

```
[FONT].getHeight()/Engine.SCALE
```

***
