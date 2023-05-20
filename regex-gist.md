# Regex Tutorial: Matching an Email

Regular expressions play a crucial role in web developement, enabling us to match patterns within strings. 
In this tutorial, I will focus on understanding the "Matching and Email" regex and how it verifies email addresses. Email verification is a a common requirement in many web applications, and by breaking down each component of the regex, and explaining its function, we will gain understanding to how it verifies an email address.


## Summary

Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This tutorial will cover the following componenets of the regex:

1. `^([a-z0-9_\.-]+)` : This component captures username consisting of lowercase letters, digits, underscores, dots, and hyphens.

2. `@([\da-z\.-]+)` : This component matches the literal symbol `@`, and captures the domain name. The domain name consists of lowercase letters, digits, dots, and hyphens.

3. `\.([a-z\.]{2,6})` : This component matches the dot `.` character, and captures the Top-Level Domain. The TLD consists of lowercase letters and dots ranging between 2 and 6 characters.

4. `$` : This component signals the end of the string, so that the regex may match the entire email address.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


## Regex Components

### Anchors

The `^` anchor matches the start of the string. The `$` anchor matches the end of the string. These two anchors work together to ensure the regex matches the entire email address.
Example in the regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.

### Quantifiers

The `+` quantifier matches one, or more than one preceding element occurences. `{2,6}` quantifier gives a rance of between 2 and 6 occurences.
Example in the regex: `([a-z0-9_\.-]+)`. This example ensures the username consists of one, or more than one lowercase letters, digits, underscores, dots, and hyphens.

### Grouping Constructs

The `()` are grouping constructs, creating multiple elements to be used as a single unit.
Example in the regex: `([a-z0-9_\.-]+)` and `([\da-z\.-]+) `.

### Bracket Expressions

The `[]` are bracket expressions. They define an character set and allow mathcing any single character from the set.
Example in the regex: `[a-z\.]` matches any lowercase letter or dot in the TLD.

### Character Classes

Character classes represent a set of characters that are predefined, and are special characters that match a single character from a set.
Example in the regex: `\d`, which matches the `\d` class, and `\a-z` which matches any lowercase letter.

### The OR Operator

The `|` is an OR operator, which allows for alternative mathcing patterns. 
Example in the regex: `[a-f0-9]{6} | [a-f0-9]{3}` matches a 6-digit hex value OR a 3-digit hex value.

### Flags

Flags can modify the behavior of the regex matching. Matching an Email regex does not use any flags.

### Character Escapes

The `\` denotes a character escape which matches special characters that have special meanings. 
Example in the regex: `\.` is a character escape which matches the dot `.` character. 


## Author

https://github.com/LydRod206
