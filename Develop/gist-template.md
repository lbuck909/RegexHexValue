# Regular Expressions: Matching a Hex Value

Regular expressions (regex) serve as indispensable tools for extracting targeted information from textual data by querying specific patterns of text. These patterns consist of a combination of both special and ordinary characters, such as the expression *"/xy-23/"*. Regular expressions find extensive application across a multitude of programming languages and facilitate the transformation of data into alternative syntax formats. The creation of a regex can be accomplished through two approaches: invoking the constructor function of the regex object or utilizing a regex literal notation.

## Summary

The focus of this article will explain regular expressions matching a Hex(hexadecimal) value. The following Hex value will be addressed : **/^#?([a-f0-9]{6}|[a-f0-9]{3})$/**. The aforementioned snippet of code is used to validate and match hex values, specifically the ones often used to represent different colors. Let’s take a deeper look at each component of the hex value.



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)


## Regex Components

### [Anchors](#anchors)
`/^` and `$/` are used to indicate the beginning and end of a pattern. These patterns by themselves do not match any regex, however they indicate the beginning or the end of the string. 
Example: ^Once specifies that the string must begin with the word Once. In the original example you will notice /^# is the beginning of the snippet. The character # operation separates a hexadecimal number from a normal decimal number.

The `$` is used to ensure the string matches the pattern overall. 
Example: `bye$/` indicates the string would need to end with `bye`

### [Quantifiers](#quantifiers)
`?` Matches the previous character zero or one time. The character before `?` is optional. The `?` also suggests a Boolean value as well.

**{ }** determine how many times the aforementioned pattern will match. Our snippet *([a-f0-9]{6}|[a-f0-9]{3})* will allow six occurrences within the first brackets of characters and 3 within the last brackets. The pattern will allow 6 characters within the string that may contain any letter between ‘a-f’ and digit 0-9. The second bracket expression will allow for 3 characters and digits respectively.

### [OR Operator](#or-operator)
The OR Operator `|` is a Boolean that directly equals the regex either before or after the OR Operator. The expression example being used indicates a matching string has to have 3 or 6 characters that are lowercase letters a-f and digits 0-9. If the pattern is not 3 or 6 characters it will be rejected.

### [Character Classes](#character-classes)
`-` represents the range of the character class. It will match any character defined within the brackets. Our snippet represents lowercase letters a-f and digits 0-9.

### [Bracket Expressions](#bracket-expressions)
**[ ]** defines the character class and matches any character listed within the brackets. The expression example being used indicates lowercase `a-f` and digits `0-9` will be recognized.


## Author

My name is E.LaiSha Buck. I have written this gist to simplify the meaning of matching Hex Value for a novice to comprehend. My [GitHub Repository](https://github.com/lbuck909/RegexHexValue.git)
