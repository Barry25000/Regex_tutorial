# Regular Expression - Matching an Email

A regular expression or regex is a sequence of characters that specifies a match pattern in text. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation. Regular expression techniques are developed in theoretical computer science and formal language theory.
The concept of regular expressions began in the 1950s, when the American mathematician Stephen Cole Kleene formalized the concept of a regular language. They came into common use with Unix text-processing utilities. Different syntaxes for writing regular expressions have existed since the 1980s, one being the POSIX standard and another, widely used, being the Perl syntax.
Regular expressions are used in search engines, in search and replace dialogs of word processors and text editors, in text processing utilities such as sed and AWK, and in lexical analysis. Regular expressions are supported in many programming languages. [1]

## Summary

This tutorial will be covering the regex expression used for both matching and validating an email:

^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

Searching through code base and other documents using the regular expression shown above would quickly help find all emails. The regular expression shown above can also be implemented within the code base, as a way of matching and validating an email. Making sure that when users fill out forms requiring a valid email address, the regex string can be implemented in a way that will not allow the user to move on until they have entered a valid email format.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

The regex components that define this particular expression are anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expression. Regarding the example used in this tutorial: ^ and $ are the anchors used, + and {2, 6} are the two quantifiers, \d represents the meta escape character utilized, [a-z0-9_\.-], [\da-z\.-], and [a-z\.] represent the character classes, \_, \., - represent the single character matches used, () represents the way this regex expression utilizes grouping and capturing, and [] delinates the bracket expression used.

### Anchors

Anchors within regex mark the start and end points of the expression. In regards to this expression, the ^ marks the start of the expression and the $ marks the end of the expression.

### Quantifiers

Quantifiers are meta characters that modify the previous character in the regex and say, how many of those do I want to match in a row.

Quantifiers allow the specification of how many character or character classes should be matched.

    The + sign matches one or more preceeding character

    {min, max} create a specific numerical quantifier range (you will notice this is used at the end of the regex expression above at the end to give a specific range to the domain name system)

### Grouping Constructs

() creates a sequence or sub expression and is a way to treat multiple characters as a single unit. You will notice the regex expression being covered in this tutorial uses () to distinct groups of characters. The first set covers all characters before the @ symbol. The second group coveres all characters before the ., and the last group covers all characters from the . to the end.

### Bracket Expressions

[] create a character or group range and represent a single character. In regards to the regex expression this tutorial is covering, the brackets are used to separate each character class. The character can be anything specified within the brackets.

Example: [a-z0-9_\.-] -> this character can be matched with any lowercase letters from a-z, and digit from 0-9, an underscore \_, a period ., or a dash -.

### Character Classes

Character classes are the attribute in a regex expression that allow us to define specific sets of characters that can be used in a search pattern.

The character classes utilized in this regex expression are [a-z0-9_\.-], [\da-z\.-], and [a-z\.].

[a-z0-9_\.-]: a-z matches a single character in the range between a (index 97) and z (index 122) (case sensitive), 0-9 matches a single character in the range between 0 (index 48) and 9 (index 57) (case sensitive), _ matches the character _ with index 9510 (5F16 or 1378) literally (case sensitive), \. matches the character . with index 4610 (2E16 or 568) literally (case sensitive), and - matches the character - with index 4510 (2D16 or 558) literally (case sensitive).

[\da-z\.-]: \d can be used to match any digit (0-9), a-z matches a single character in the range between a (index 97) and z (index 122) (case sensitive), \. matches the character . with index 4610 (2E16 or 568) literally (case sensitive), and - matches the character - with index 4510 (2D16 or 558) literally (case sensitive).

[a-z\.]: a-z matches a single character in the range between a (index 97) and z (index 122) (case sensitive), and \. matches the character . with index 4610 (2E16 or 568) literally (case sensitive)

Other examples of single characters:

\d can be used to match any digit (0-9), \w to match any alphanumeric character (a-zA-Z0-9), and \s any white space such as a space or a tab

### Flags

Regex flags are used to modify an expressions behavior -> case sensitivity, etc. There are only 6 of them in JavaScript -> i: case-sensitivity, g: looks for all matches, m: multiline mode, s: enables "dotall" mode that allows a dot . to match a newline character \n, u: enables full Unicode support, and y: "sticky" mode.

The regex expression covered in this tutorial does not utilize flags.

### Character Escapes

## Author

[1] wikipedia Regular Expression https://en.wikipedia.org/wiki/Regular_expression

Barry Engler is an Electrical/Software Engineer with a Bachelors of Science degree. Barry is currently living in the suburbs of Chicago.

barryengler@gmail.com <br>
[GitHub](https://github.com/Barry25000)
