# It's Just Email

Data validation is crucial when it comes to user input. It is essential that when prompted to enter an email address, the user must enter information that follows an email's formatting. Developers can use regular expression, or regex, to set rules that the data must follow.

## Summary

This regex ensures that an email address is formatted properly. I will be breaking down the individual components of the regex, and how they work as a whole to achieve this goal. <br>
Regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors

`^`, `$` <br>

- `^` signals the start of the regex. Anything listed immediately after the `^` is what can follow the `^`. In this case, it is a grouping (more on this later).<br>
- `$` signals the end of the regex. It is the stopping point at which no other data will be included in this string.

### Quantifiers

`+`, `{2,6}` <br>

- `+` is used at the end of the first two groups to indicate that they must be followed by whatever comes after it. For example, in this part of the regex, `([a-z0-9_\.-]+)@`, the + says that the bracket expression `([a-z0-9_\.-]` must be followed by the @ symbol.
  <br>
- `{2,6}` is the quantifier that goes with the bracket expression `[a-z\.]`. It is saying that the content in the bracket expression `[a-z\.]` must be between 2 and 6 characters long.

<!-- ### OR Operator -->

### Character Classes

`\d`, `\.`

- `\d` signals every digit 0-9. <br>
- `\.` signals every character. <br>
  In this example, `[\da-z\.-]`, it is saying any digit (`/d`), any letter a-z, any single character (`\.`), and the - symbol will be allowed as data in the string.

### Flags

`/`, `/` <br>

- Flags are not used in this example, but the opening `/` and closing `/` are in place for the user to add flags if they desire at the end.

### Grouping and Capturing

`([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, `([a-z\.]{2,6})` <br>

- The grouping achieved by () is to split string information into its own group. For example, `([a-z0-9_\.-]+)` will be stored in its own index, `([\da-z\.-]+)` will be stored in its own index, and `([a-z\.]{2,6})` will be stored in its own index.

### Bracket Expressions

`[a-z0-9_\.-]`, `[\da-z\.-]`, `[a-z\.]` <br>

- The bracket notation is used to match strings that have a given criteria. The content within the [] indicate the criteria. For example, `[a-z0-9_\.-]` means that any letters a-z, and digits 0-9, `\.` means ANY SINGLE character, `_` and `-` mean that those characters are allowed in an email entry.

## Author

Pete Hodnefield is a full-stack web developer student based out of Minneapolis, Minnesota.
[Pete's GitHub](https://github.com/petehodnefield)
