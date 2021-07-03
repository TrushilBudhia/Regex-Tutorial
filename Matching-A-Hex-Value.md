# Matching A Hexadecimal Value

The following file will explain the particular components of the regular expression, Matching a Hexadecimal Value, and detail how each component works. Regular expressions are patterns used to match character combinations in strings.

## Summary

The regular expression I will be evaluating in this file is the Matching a Hexadecimal Value regular expression. The regular expression is as follows:
```js
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

In hexadecimal, each digit can be 16 values. The standard numeral system is called decimal (base 10) and uses ten symbols: 0,1,2,3,4,5,6,7,8,9. Hexadecimal uses the decimal numbers and six extra symbols. There are no numerical symbols that represent values greater than nine, so letters taken from the English alphabet are used, specifically A, B, C, D, E and F. Hexadecimal A = decimal 10, and hexadecimal F = decimal 15.

One way the hex system can be used is defining colour hex codes. A colour hex code is a hexadecimal way to represent a color in RGB format by combining three values – the amounts of red, green and blue in a particular shade of color. A colour hex code is written using six characters and in some cases can be written with three characters e.g. for the colour white, the colour hex code can be either #ffffff or #fff.

Below will be descriptions for the anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR Operator, flags and character escapes.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs) 
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Author](#author)

## Regex Components

### Anchors
Anchors indicate the beginnings and endings of lines and words. The Matching a Hex Value anchors are `^` and `$`.

`^` matches the beginning of input. `$` matches the end of input.

For example, `^Hello ` will match any line or string that begins with `Hello `, while `World$` will match any line or string that ends with `World`.

### Quantifiers
Quantifiers indicate numbers of characters or expressions to match. The quantifiers used in the Matching a Hex Value regular expression are `?` and `{n}`.

`?` matches the preceding item character 0 or 1 times. The regular expression will match a string that either begins with `#` or not. For example `/ou?r/` matches both "colour" and "color".

As for `{n}`, "n" is a positive integer and it matches exactly "n" occurrences of the preceding item. In the Matching a Hex Value regular expression, the `{6}` and `{3}` are quantifiers. The numbers inside specify the number of characters that need to be matched in the preceding character class `[a-f0-9]`. For example, `/r{2}/` doesn't match the "r" in "Thor", but it matches all of the "r"'s in "Thorr".

### Grouping Constructs
Grouping constructs indicate groups and ranges of expression characters. The grouping construct in the Matching a Hex Value regular expression is `([a-f0-9]{6}|[a-f0-9]{3})`. Inside the grouping construct is the OR Operator (`|`), the charater classes and the quantifiers. For example, /(John)/ matches and remembers "John" in "John Wick". 

### Bracket Expressions
A bracket expression is a list of characters enclosed by `[` and `]`. Within a bracket expression, a range expression consists of characters separated by a hyphen. In the Matching a Hex Value regular expression, it is the `[a-f0-9]` component where the inside value is made up of character between `a-f` and/or `0-9`. The amount of characters will match the amount detailed in the proceding quantifier. For example, `[a-e]` is equivalent to `[abcde]`.

### Character Classes
Character classes distinguish kinds of characters such as, for example, distinguishing between letters and digits. For Matching a Hex Value regular expression, the `[a-f0-9]` is the character class which is repeated twice with different quantifiers attached to each one.

Inside the character class there are two ranges mentioned, `a-f` and `0-9`. As long as the characters used in the character classes are `a-f` and/or `0-9` and as long as the proceding quantifier is matched, the value used as the hex value will work in the regular expression. 

If the character class were `[t-z]`, the character that would match would be: 't', 'u', 'v', 'w', 'x', 'y' or 'z'. 

### The OR Operator
The OR Operator in the Matching a Hex Value regular expression is the `|` character. It is contained within the grouping construct between the two character classes with their quantifiers. It means that either `[a-f0-9]{6}` or `[a-f0-9]{3}` will need to be matched for the Matching a Hex Value regular expression to function. Both do not have to be satisfied. For example, `/blue|red/` matches "blue" in "blue pill" and "red" in "red pill".

## Author
I am a web developer who enjoys learning about advances in development technologies and building user friendly applications.

- Github: [@Trushil](https://github.com/TrushilBudhia)
- Portfolio: [@Trushil](https://trushilbudhia.github.io/Portfolio/)
- Email: trushil.budhia@gmail.com
