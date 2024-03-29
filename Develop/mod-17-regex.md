# Module 17 Challenge- Regular Expressions

A regex (regular expression) is a sequence of characters that defines a search pattern in text.

You can use `ctrl + f` to bring up your search bar in your VS code.

## Summary

I will use the following regular HTML Tag expression to define the different parts of it that make it a regex:

Matching an HTML Tag - `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)

## Regex Components

### Anchors

`^` used at the beginning to match the start of the string.

`$` used at the end to match the end of the string.

### Quantifiers

`+` after `[a-z]` to specify one or more lowercase alphabetic characters.

`*` after `([^<]+)` to specify zero or more occurrences of any character except `<`.

### OR Operator

The OR operator `|` is used to provide alternative matching options:

Either `(>.*)<\/\1>` to match a complete tag with content.

Or `\s+\/>` to match a self-closing tag.

### Character Classes

`[a-z]` to match any lowercase alphabetic characters.

### Grouping and Capturing

Used with parentheses:

`([a-z]+)` captures one or more lowercase alphabetic characters.
`([^<]+)*` captures zero or more occurences of any character except `<`.

### Bracket Expressions

In other words, character classes:

`[a-z]` matches any lowercase alphabetic character.

### Greedy and Lazy Match

Greedy matching is exhibited by default:

`(.*)` matches zero or more of any character greedily.

### Boundaries

Boundaries are used implicitly with anchors, ensuring the expression matches the entire string.

### Back-references

`<\/\1>` ensures that the closing tag matches the opening tag captured in the first group.

## Author
