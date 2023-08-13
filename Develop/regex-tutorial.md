# Regex Tutorial: Matching an Email

- Welcome to the Regex Tutorial: Matching an Email `(/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/)`! 
- In this tutorial, you will learn how to create a regular expression that can accurately match and validate email addresses. 

## Summary

- This tutorial focuses on a regex designed to match and validate email addresses. 
- It will cover each component of the regex, explaining its purpose and how it contributes to the overall pattern.

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

### Anchors
 In this regex the `^` and `$` are anchors. The caret `^` initiates the start of the string, while the dollar sign `$` initiates the end of the string. When used together `^...$`, the regex makes sure that the entire input string follows the email address format.

### Quantifiers
Quantifiers in a regex determine how many times a particular element should occur in the text for a match to be found. 
- In the email matching regex, the plus sign `+` and the curly braces `{2,6}` are quantifiers. The `+` indicates that the character class preceding it should occur one or more times, while `{2,6}` specifies that the character class should occur between 2 and 6 times.

### OR Operator
The OR operator in regex is represented by the vertical bar `|`. It allows you to specify alternatives for a match. It is not used in the regex example above.

### Character Classes

Character classes in regex allow you to specify a group of characters that can match a single character in the input text. 
- `[a-z0-9_\.-]`: This character class matches a single character that can be a lowercase letter `a-z`, a digit `0-9`, an underscore `_`, a dot `.`, or a hyphen `-`.
- `[\da-z\.-]`: This character class matches a single character that can be a digit `\d`, a lowercase letter `a-z`, a dot `.`, or a hyphen `-`.
- `[a-z\.]`: This character class matches a single character that can be a lowercase letter `a-z` or a dot `.`.

### Flags

This regex does not include any flags. Flags are used to modify the behavior of the regex pattern matching, such as case sensitivity, global matching, and multiline matching. Some examples of flags are:
- `i`: Case insensitive matching - When this flag is used, the regular expression will match regardless of whether the letters are uppercase or lowercase.
- `g`: Global matching - When this flag is used, the regular expression will find all occurrences of the pattern in the input text rather than stopping after the first match.
- `m`: Multiline matching - When this flag is used, the caret `^` and dollar sign `$` anchors will match the start and end of each line in the input text, rather than just the start and end of the entire text.
- `u`: Unicode matching - When this flag is used, the regular expression will treat the input text and pattern as Unicode strings, allowing for more advanced matching with Unicode characters.

### Grouping and Capturing

Parentheses `(...)` in regex define capturing groups. They allow you to extract specific parts of the matched text. In  this regex, there are three capturing groups:
- `([a-z0-9_\.-]+)`: Captures the username part of the email address.
- `([\da-z\.-]+)`: Captures the domain name part of the email address.
- `([a-z\.]{2,6})`: Captures the top-level domain part of the email address.

### Bracket Expressions

Bracket expressions are used to define character classes, as shown above. They specify a set of characters that can match a single character in the input text. For example,
- `[a-z]` matches any lowercase letter, and 
- `[0-9]` matches any digit.

### Greedy and Lazy Match

In regex, quantifiers are "greedy" meaning they try to match as much as possible. However, you can make them "lazy" by adding a question mark `?` after the quantifier. Lazy matching will find the shortest possible match. In this regex, all quantifiers are greedy. You can modify them to be lazy by adding `?` after them.

### Boundaries

Boundaries in regex are represented by `\b` and assert the position where a word boundary should occur. In this regex, there are no word boundaries used.

### Back-references

Back-references in regex allow you to refer back to a previously matched group. In this regex, there are no back-references used.

### Look-ahead and Look-behind

Look-ahead and look-behind are assertions that allow you to check if a specific pattern is followed or preceded by another pattern without including it in the match. In this regex, there are no look-ahead or look-behind assertions used.

## Author
This tutorial was written by Delia Young. To explore more of my work, visit my [GitHub profile](https://github.com/deliaswe). Here is where you can find my [Github Gist](https://gist.github.com/deliaswe/92399ab383694c73db5bad3de72223c0)
