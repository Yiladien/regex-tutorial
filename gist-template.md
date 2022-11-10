# Regex Tutorial

Regex, short for regular expression, is a sequence of characters to match a specific pattern to capture and collect or change text. This tutorial will guide you through using some of the regex commands.

---

## Summary

This tutorial will demonstrate how to use regex to capture a Hex Value using the expression below:

`#ee80ee`

```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

---

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)

---

## Regex Components

### Anchors

```
/^$/ or {6}
```

Forward slash `/` starts and ends the regex. The `^` and `$` are regex anchors. Using `^` will look for the pattern at the start of a line. The `$` will match the end of the line text.

If your value is in the middle of a line, you will omit the `^` and/or the `$`.

### Quantifiers

```
#?
```

Quantifiers match the amount of a character or group in the pattern. `*` will match 1 or more, `?` will match 1 or 0. If looking for color or colour, you can use the regex `/colou?r/` which will look for the word with or without the character `u` in the word.

Curly braces `{}` with a number provide how many characters to match.

### OR Operator

```
|
```

The pipe character will allow different patterns criteria to be used to match within a group.

### Character Classes

```
[a-f0-9]
```

Character class is created using brackets `[]` that search for a single character within the text using a list or range of characters. If you use `[aeg]`, it will look for 1 character of a or e or g. If you use `[a-z]`, it will look for a single character from a through z.

You can combine the range as `[a-z0-9]` to look for a single character with a through z or 0 through 9.

### Grouping and Capturing

```
([a-f0-9]{6}|[a-f0-9]{3})
```

Paranthesis `()` allow different types of captures to be grouped, allowing the OR operator to consider different patterns to match within the sequence of characters.

---

## Author

Written by Gabriel Cordova at https://github.com/Yiladien
