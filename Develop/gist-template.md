# An Explanation of Regular Expressions

a regular expression or regex for short are a set of patterns used for manipulating and matching strings. it usualy consists of a mix of regular and specialcharecters that may look confusing at first but are very useful once mastered

## Summary
one of the many types of regular expressions is a string that looks like this /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ which is used to matchand validate urls.
it may look like giberish but once broken down it becomes a bit more clear on what regex can do


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
 the regular expression /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/  can be boken down into its component parts 
### Anchors
/<mark>^</mark>(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?<mark>$</mark>/
these are called anchors, sort of like an opening and closing of the expression
- ^ - marks the start of a regular expression
- $ -marks the end regular expression
these two are mandatory for the expression to function 

### Quantifiers
/^(https<mark>?</mark>:\/\/)<mark>?</mark>([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/<mark>?</mark>$/
- ? this marks the preceduing expresion as optional

### OR Operator

### Character Classes
getting more complex, expressions can be used on specific types of charecters 
/^(https?:\/\/)?(<mark>[\da-z\.-]</mark>+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
- [\da-z\.-] this matches a single charecter that in order is either a digit, a lowercase character, a period, or a hyphen. this expression is used later with its surrounding parenthesies
### Flags

### Grouping and Capturing
using parentheses we can go more in depth inside the larger patern, enabling such things as repetition 
/^<mark>(https?:\/\/)</mark>?<mark>([\da-z\.-]+)</mark>\.<mark>([a-z\.]{2,6})</mark><mark>([\/\w \.-]*)</mark>*\/?$/
using grouping we can utilise much stronger operations
- (https?:\/\/) this grouping grabs a string that starts with http:// or https:// 

- ([\da-z\.-]+) this one was just explained above in charecter classes but as a group it goes from catching just one charecter to being able to catch multiple charecters.

- ([a-z\.]{2,6}) this one may look like the one above it but it has slight differences it looks for anyhere from 2 to 6 lowercase letters or periods. unlike the one before it this grouping cant look for numbers though.

- ([\/\w \.-]*) this one is looking for query parameters. slashes, periods, hypens if it has it this should find it
### Bracket Expressions

### Greedy and Lazy Match
this expression uses greedy matching, its looking for as many matches as it posiblly can.
### Boundaries

### Back-references
 this expression doesent have back-referneces to show but they are very interesting. back references let the expression match strings that where previously captured within the same pattern
### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
