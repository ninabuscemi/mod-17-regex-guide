# Regular Expressions Tutorial

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

Anchors are crucial in defining where a pattern should match within a string. The `^` anchor asserts the position at the beginning of the string, ensuring the pattern starts matching from the very start.

Also, the `$` anchor asserts the position at the end of the string, ensuring the pattern matches until the very end of the input string.

### Quantifiers

Quantifiers control the number of occurrences a particular element in the pattern can match. The `+` quantifier specifies that the preceding element (in this case, `[a-z]`) should match one or more times. Similarly, the `*` quantifier after `([^<]+)` specifies that zero or more occurrences of any character except `<` should be matched.

### OR Operator

The OR operator `|` provides flexibility in matching patterns by allowing alternative options. In this regular expression, it provides two options for matching tags: `(>.*)<\/\1>` to match a complete tag with content, or `\s+\/>` to match a self-closing tag.

### Character Classes

Character classes, such as `[a-z]`, specify a set of characters that the pattern can match. In this case, `[a-z]` matches any lowercase alphabetic character, allowing flexibility in matching tag names or other lowercase text.

### Grouping and Capturing

Grouping and capturing with parentheses `()` allow specific parts of the matched text to be captured for later reference or extraction. For instance, `([a-z]+)` captures one or more lowercase alphabetic characters, while `([^<]+)*` captures zero or more occurrences of any character except `<`.

### Bracket Expressions

Bracket expressions, or character classes, specify a set of characters that the pattern can match. In this regular expression, `[a-z]` matches any lowercase alphabetic character, providing specificity in matching certain types of characters within the string.

### Greedy and Lazy Match

Greedy matching, exhibited by default, attempts to match as much text as possible while still allowing the overall pattern to match. For example, `(.*)` matches zero or more of any character greedily, consuming as much text as possible until it reaches the end of the string or encounters a condition that causes it to backtrack.

### Boundaries

Boundaries, in conjunction with anchors, ensure that the pattern matches specific positions within the string. Anchors like `^` and `$` implicitly define boundaries by indicating the start and end of the string, respectively. This ensures that the expression matches the entire string, rather than just a portion of it.

### Back-references

Back-references, indicated by `\1`, allow referencing previously captured groups within the regular expression. In this case, `<\/\1>` ensures that the closing tag matches the opening tag captured in the first group `(([a-z]+))`, maintaining consistency in HTML/XML-like tag structures.

## Author

If you have any questions regarding the project, please, feel free to contact me:

GitHub: [ninabuscemi](https://github.com/ninabuscemi)