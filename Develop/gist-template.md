# Hex Value Match Regex

A tutorial for reading and using Regex to match a Hex value.

## Summary

This tutorial will teach you how to use the hex value regex, along with using control and find.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
This is our regular expression that we will be breaking down.
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
### Anchors
Our anchors are the `^` and the `$`
### Quantifiers
The quantifiers are `?`,`{6}`, and `3`
### OR Operator
OR Operator being the `|`
### Character Classes
Character Classes:
`[a-f0-9]`
`[a-f0-9]{6}`
`[a-f0-9]{3}`
### Flags
Flags: `^` and `$`
### Grouping and Capturing
`([a-f0-9]{6}|[a-f0-9]{3})`
### Bracket Expressions
`[a-f0-9]`
### Greedy and Lazy Match
`#FFF`
`#000`
### Boundaries
`^` and `$`
### Back-references
None 
### Look-ahead and Look-behind
None
## Author
https://github.com/malikburrus0 / MalikBurrus0


### Anchors
So, in Regex, we use `^` and the beginning of our string and `$` at the end of our string.

### Quantifiers
In the string our quantifier will be `?`. This will affect the `#` literal. This matches results with a singular `#` or none at all.

Matches are `#FFF` BUT it will not match `##FFF`

The quantifiers will make a string of `{3}` and `{6}`, to do that it needs to work with `[a-f0-9]`.
THEN it matches the pattern.

### OR OPERATOR
The or operator will be the `|` in the middle of `([a-f0-9]{6}|[a-f0-9]{3})`.

Matches are `#FFF` and `#H34G4J`
Non-Matches are `#FFFF` and `#FF`

### Capturing and Grouping
The `#` groups the expression. This will combine the two bracket expressions to the quantifiers.

### Bracket Expressions
The bracket expression is `[a-f0-9]`, This finds matches with lower case a-f and numbers 0-9.

Matches are `#FFF` and `#000`
Non-Matches are `#!!!` and  `#<<<`