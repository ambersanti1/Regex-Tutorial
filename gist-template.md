# Regex Tutorial

Regular expression or regex as is commonly known, is a sequence of characters that defines a search pattern. Let's imagine you are a doctor who have a long document with thousands of clinical cases and you want to share these cases with the medical community, but to do that you would need to delete the personal information of each patient, including their emails. It would take a long time to do this manually, but with regex it would take seconds to delete them all. 

## Summary

In this tutorial each component of the following email regex is analized and described:
Email    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


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

## regex Components

### Anchors
The email regex is enclosed by slash characters '/' because the regex is originally a literal, so the sequence of characters must be wrapped so they can be converted into a metacharacter. 

The ^ anchor is a string that begins with the characters that follow it and the $ anchor is a string that ends with the characters that precede it. The ^ and $ character, can be preceded by an exact string or a range of possible matches.

### Quantifiers
The email has a domain .com or any other, and normally is 2 to 6 characters long. For that reason, the email regex, includes a quantifier {2,6} at the domain to specify it must be between this range of characters.

### OR Operator
The OR opeator is useful to amplify the searching options. Let's consider the Hex Value, it could be 6 or 3 characters long, to write that in a regex we use | and it would be as the following:

HEX value     /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ 

### Character Classes
A character class within a regular expression sets a group of characters, any of which can be present in an input string to satisfy a match. In the email regex we have \d which is the same as [0-9].

### Flags
Flags are modifiers that indicate how the pattern matching is performed and are placed at the end of a regex, after the second slash. For example i is a flag that makes the matching case-insensitive, which means the uppercase and lowercase letters are treated as equivalent. In the email regex there are no flags.

### Grouping and Capturing
Grouping is the concept of grouping a section of a regex by using parentheses () to create a subexpession. In the email regex there are 3 subexpressions which divide the username, the mail server and the domain. The subexpessions can capture or matched the character sequences for possible re-use or do the opposite.

### Bracket Expressions
The characters inside a set of square brackets [] represent a range. In this case [a-z] means any lowercase letter from the a to the z; [0-9] means any number form 0 to 9; the underscored and the hypen inside the brackets signifies the string can include them[_-] and \. is a literal dot.

### Greedy and Lazy Match
Greedy and lazy are the concepts used to describe the behavior of quantifiers. Greedy quantifiers match as much text as possible, while lazy quantifiers match as little text as possible while still allowing all the pattern to match. In the email regex there is no greedy nor lazy match.

### Boundaries
 Boundaries are used to specify the limits of where a pattern should match within a string, meaning they are the conditions that define where a match should start or end. In the email regex the start of line is ^ and the end of line is $ anchor.

### Back-references
 Back-references are useful for finding repeated patterns or ensuring that the same text appears multiple times within a string.
 In the email regex the username part has a '+' at the end ([a-z0-9_\.-]+). The + quantifier specifies that the preceding element must occur one or more times. 

### Look-ahead and Look-behind

Look-ahead and look-behind enable the specification of the conditions that must be met ahead or behind the current matching position in the string, without incorporating those characters in the match itself. In the email regex there are no look-ahead and benind.

## Author

Amberly Sandoval
GitHub: https://github.com/ambersanti1
