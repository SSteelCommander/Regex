# How to match a email in regex 

This tutorial explains how to use regex to match an email `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This is used to validate emails.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Summary

A regular expression is a search that uses sequence of characters. This is used to find patterns of characters without strings. This tutortial will go walk through the components of a regex and how it applies to matching an email.

## Regex Components

### Grouping and Capturing
Capturing group #1 in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the `.com`.

### Quantifiers
Quantifiers use the `+` operator, which connect the users name, service and `.com`. `{2,6}`, allows a match range of 2-6 characters for the character set of `[a-z\.]`.

### Character Classes
The character class is `\d`, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44". 

### Anchors
The anchors are that show the beggining of a string are `^ `, are the end of the string `$`. `(m)`, or multiline is not enabled, so the regex will end at `$`.

### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6} for the last capture group.

### Bracket Expressions
Bracked expressios for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case senstive) and the character ".". 
