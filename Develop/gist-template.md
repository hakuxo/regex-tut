# Regex Tutorial

The following gist gives a walkthrogh of the central components with matching a given URL while utilizing expressions in Javascript.

## Summary

I will try to better understand regex along with trying to describe this line!
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

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
Anchors by definition belong to a family of regex tokens that don't match any characters, but assert something about the srtring or the matching process. There are different types of anchors! These include but are not limited to the "^" and the "$" keys. They define the beginning and end of an expresion.

This also allows us to read through the code easier! Take for example ^C will find all instances that begin with a capital C. This is case sensitive so it will not find any instances beginning with a lowercase c.

### Quantifiers
Quantifiers are used to specify how many instances of a character, group, or character class must be in the input. This allows the match to be found! A quantifier has the form of {m,n} where there is a minimum and a maximum. 

Different symbols and usage - 

(*) - Matches a pattern zero or more.

(+) - Matches a pattern once or more.

(?) - Matches a pattern zero or more.

{} - Allows limits 3 different ways -

    {c} - Will match pattern once.

    {c,} - Will match atleast once.
    
    {c,x} - Will match a minimum of c, with a maximum of x.

### OR Operator
The main OR operator used in the above regex is the []. This will match for any characters or character classes included within the brackets.For example,  "[ \da-z \ . - ]" matches any digits or characters between a and z.

### Character Classes
Character Classes can also be called a character set. To use a character class, simply place the characters you want to match between square brackets! Say youd like to match an a or an e, use "[ae]". You could use this in the word gray or grey! This makes it easier for searching through the varieties of English or any language. We can also use \d which looks for any digit and \w that looks for any alphanumeric character. 


### Flags
There are 6 flags in javascript! Flags allow us to affect the search in a certain way.

Flags -

i - This allows us to flag a search as case-insensitive: no difference between a capital letter and a lowercase

g - This allows us to look for ALL matches, without this it would only return the first match.

m - Multiline mode

s - Enables "dotall" mode. This allows a dot (.) to match newline character (\n)


## Author

This was created by Jillian Hallmark. Github: <a href="https://github.com/hakuxo">hakuxo</a>
