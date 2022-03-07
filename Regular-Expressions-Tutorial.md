# Challenge-17 Regex Tutorial:

This is a tutorial that will help you learn the basic concepts of the regular expressions tool.

### Summary

Regular expressions allow for a user to use character sequences to define search patterns, and are often in making sure the code is validated and follows the correct format. It also allows for the pulling of information.

### Table of Contents

-[Anchors](#anchors)
-[Quantifiers](#quantifiers)
-[OR Operator](#or-operator)
-[Character Classes](#character-classes)
-[Flags](#flags)
-[Grouping and Capturing](#grouping-and-capturing)
-[Bracket Expressions](#bracket-expressions)
-[Greedy and Lazy Match](#greedy-and-lazy-match)
-[Boundaries](#boundaries)
-[Back-References](#back-references)
-[Look-ahead and Look-behind](#look-ahead-and-look-behind)

### Regex 

### Regex Components

### Anchors

An anchor defines the start and end to the regular expression using `^` to start and `$` to close.

In an email sequence: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

We can see that the anchors are placed before and after the beginning and ending parentheses defining that we are using this entire block for RegEx.

### Quantifiers

A quantifier is used to determine what characters are needed in order to form a match. The quantifier `+` is used at the end of other regex sequences to show that the sequence requires the prior regex.

For Example, in the sequence `([a-z0-9_\.-]+)` we see that the quantifer `+` is being used to show that we need atleast 1 `([a-z0-9_/.-)`.

```
Greedy Quantifier     Lazy Quantifier    Description
*	                *?	              Match zero or more times.
+	                +?	              Match one or more times.
?	                ??	              Match zero or one time.
{ n }	            { n }?	          Match exactly n times.
{ n ,}	            { n ,}?	          Match at least n times.
{ n , m }	        { n , m }?	      Match from n to m times.
```

As a Note: We will define `greedy` and `lazy` operators later on in the tutorial.

### OR Operator.

The OR Operator is a vertical bar that can be used to match a number of singular characters for conditional matching

### Character Classes

Chacter classes are used for defining a set of characters from which any can be used in input strings for a successful match. 

```
\s: Whitespace
\S: Not whitespace
\w: Word
\W: Not word
\d: Digit
\D: Not digit
\x: Hexade­cimal digit
\O: Octal digit
```

### Flags

Regex has flags that may effect searches. In javascript there are 6 of them.

```
i
With this flag the search is case-insensitive: no difference between A and a.

g
With this flag the search looks for all matches, without it – only the first match is returned.

m
Multiline mode.

s
Enables “dotall” mode, that allows a dot . to match newline character \n.

u
Enables full Unicode support. The flag enables correct processing of surrogate pairs.

y
“Sticky” mode: searching at the exact position in the text.
```

### Grouping and capturing

Grouping and capturing is used to capture the substrings of input strings. 

```
.:      Any character except newline (\n)
(a|b):  a or b
(…):    Group
(?:…):  Passive (non-capturing) group
[abc]:  a, b or c
[^abc]: Not a, b or c
[a-z]:  Letters from a to z
[A-Z]:  Uppercase letters from A to Z
[0-9]:  Digits from 0 to 9 
```
Note: these are inclusive ranges.

### Bracket Expressions.

These are used to indicate a set of characters to match. Any characters inside the brackets will match, or a hyphen can be used to define a character set.

```[ ]```

```
'apple'.match(/[abcd]/) // matches 'a'
```

```{ }```

Curly brackets express the exact amount of things to match. They are often found after expressions and limit them to match only a certain amount of times. 
: \coco{2}\ will only match ‘co’ exactly twice.
```
'coconut'.match(/co{2}/) // -> matches 'coco'
```

### Greedy and Lazy Match

'Greedy' quantifiers match elements as many times as they can while `Lazy` quantifiers do the opposite.

### Back-References

Backreferences are used to allow for a way to identify repeated characters or substrings in a string. For example, if you have multiple instances of a input string than you can use a capturing group and backreference to match later occurences. 

```(captured regex inside)...\1```

```\1``` Reproduces the text of the first capturing group..

### Look-ahead and Look-behind

These are just assertions like the start and ends of lines that make regular expressions and matching results possible. They match characters and return results but are of Zero-Length. They assert whther a match is possible or not.

### Author

Prepared by Noah Negron