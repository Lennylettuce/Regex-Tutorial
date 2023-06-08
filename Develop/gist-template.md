# Email-Matching Regular Expressions!

This tutorial is about the expression /^([a-z0-9_/.-]+)@([/da-z/.-]+)/.([a-z/.]{2,6})$/ which is used in validation to identify matching emails. Without this there would be no log-in!

## Summary

A regular expression is by definition a sequence of symbols and characters expressing a string or pattern to be searched for within a longer piece of text. (cited source:google!) This tutorial will cover the components of this expression and how it is used to identify matching string patterns within a larger string.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
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
Anchors in an expression are symbols used to indicate the beginning and end of a string. In this case the ^ indicated the beginning and $ for the end.
### Quantifiers
Quantifiers in this expression include + which will link the user's email name+email service+.com. Another is {2,6} which gives a 2-6 character range from charset of [a-z/.].
### Character Classes
Character class for this expression is /d which matching a single digit from range 0-9.
### Flags
Flags are used in regular expressions to further narrow the search by using specific letters to denote the specific search parameters.
i - means the search is case sensitive A=a
g - means the search looks are all matches
m - means multiline mode
s - enables 'dotall' mode that allows a dot . to match newline char \n.
u - enables unicode support which processes surrogate pairs.
y - is for 'sticky' mode which searches an exact position within text.
### Grouping and Capturing
Capturing groups in regular expressions are a range of symbols set within parenthesis which are used in this case to match first the user email name, then the email service, then to match .com.
### Bracket Expressions
The bracket expressions used for email validation include all ranges within each set of brackets in the expression. The first of which matches letters a-z, digits 0-9 and different allowed charcters. The second of which matches a single digit from 0-9 and letters from a-z along with the allowed characters . and -. The final bracket expression matches characters a-z and . character.
### Greedy and Lazy Match
This expression doesn't use lazy match, it uses greedy match which uses the quantifier to match a specific character in a string as many times as needed until a match is found. In doing this it uses dot '.' as a placeholder in it's search until it finds a match or has to back track to find it's match.
### Boundaries
Boundaries appear like \b word \b so you can search whole words in a string.
### Back-references
Back references are used to match a previous capturing group and is denoted by operators that define the first and second groups with operators in between to signify function and note which is to be compared to another.
### Look-ahead and Look-behind
The lookaround is a zero-length assertion just like anchors that is used to define groups and return whether a match is there or not-it doesn't actually give a proper result, only like a boolean true or false match or no match.
## Author
I used the website regular-expressions.info as a guide for the definitions in this tutorial. 
Link to the author's GitHub profile : https://github.com/Lennylettuce
