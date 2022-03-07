# Challenge-17 Regex Tutorial:

This is a tutorial that will help you learn the basic concepts of the regular expressions tool.

## Summary

Regular expressions allow for a user to use character sequences to define search patterns, and are often in making sure the code is validated and follows the correct format. It also allows for the pulling of information.

## Table of Contents

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

##Regex 

## Regex Components

## Anchors

An anchor defines the start and end to the regular expression using `^` to start and `$` to close.

In an email sequence: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

We can see that the anchors are placed before and after the beginning and ending parentheses defining that we are using this entire block for RegEx.

## Quantifier