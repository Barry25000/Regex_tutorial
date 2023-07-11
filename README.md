# Regular Expression - Matching an Email

Regular expression or regex is a sequence of characters that specifies a pattern in text. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation. Regular expression techniques are developed in theoretical computer science and formal language theory.
The concept of regular expressions began in the 1950s, when the American mathematician Stephen Cole Kleene formalized the concept of a regular language. They came into common use with Unix text-processing utilities. Different syntaxes for writing regular expressions have existed since the 1980s, one being the POSIX standard and another, widely used, being the Perl syntax.
Regular expressions are used in search engines, in search and replace dialogs of word processors and text editors, in text processing utilities such as sed and AWK, and in lexical analysis. Regular expressions are supported in many programming languages. [1]

## Summary

This tutorial will be covering the regex expression used for matching and validating an email:

^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

Searching through code base and other documents using the regular expression shown above would quickly enable you to find all emails discribed by the regex. The regular expression shown above can also be implemented within the code, as a way of validating an entered email address. Making sure that when the user fills out forms requiring an email address, the regex can be implemented in a way that will not allow the user to move on until they have entered a valid email format.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

The regex components that define this particular expression are anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expression. Regarding the example used in this tutorial: ^ and $ are the anchors used, + and {2, 6} are the two quantifiers, [a-z0-9_\.-], [\da-z\.-], and [a-z\.] represent the character classes, \_, \., - represent the single character matches used, () is used for grouping and capturing, and [] delinates the bracket expression used.

### Anchors

Anchors within regex mark the start and end points of the expression. In regards to this expression, the ^ marks the start of the expression and the $ marks the end of the expression.

### Quantifiers

Quantifiers are meta characters that modify the previous character in the expression.

Quantifiers allow the specification of how many character or character classes should be matched.

The + sign, the preceding item has to match 1 or more times.

{min, max}, creates a specific minimum and maximum that the expression has to match to be valid, the min, max is used
at the end of the regex expression to give a specific range to the domain name system.

### Grouping Constructs

() creates a group that treats multiple characters as a single unit. The regex expression in this tutorial uses () to create groups of characters. The first set covers all characters before the @ symbol. The second group coveres all characters before the ., and the last group covers all characters from the . to the end.

### Bracket Expressions

[] creates a character or group range and represent a single character. In this tutorial, the brackets are used to separate each character class. The characters can be anything specified within the brackets.

Example: [a-z0-9_\.-] -> this character can be matched with any lowercase letters from a-z, and any digit from 0-9, an underscore \_, a period ., or a dash -.

### Character Classes

Character classes are the attribute in a regex expression that allow us to define specific sets of characters that can be used in a search pattern.

The character classes utilized in this regex expression are [a-z0-9_\.-], [\da-z\.-], and [a-z\.].

[a-z0-9_\.-]: a-z matches a single lowercase character between a and z, 0-9 matches a single character in the range between 0 and 9, _ matches the character _, \. matches the character ., and - matches the character -.

[\da-z\.-]: \d is used to match any digit (0-9), a-z matches a single lowercase character in the range between a and z, \. matches the character ., and - matches the character -.

[a-z\.]: a-z matches a single lowercase character in the range between a and z, and \. matches the character .

Other examples of single characters:

\d can be used to match any digit (0-9), \w to match any alphanumeric character (a-zA-Z0-9).
\s any white space such as a space or a tab.

### Character Escapes

A character escape represents a character that may not be able to be conveniently represented in its literal form.

\. represents the meta escape character utilized in thie regex

## Author

[1] wikipedia Regular Expression https://en.wikipedia.org/wiki/Regular_expression

Barry Engler is an Electrical/Software Engineer with a Bachelors of Science degree. Barry is currently living in the suburbs of Chicago.

barryengler@gmail.com <br>
[GitHub](https://github.com/Barry25000)
