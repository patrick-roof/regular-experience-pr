# Regular Expression Tutorial

A regular expression tutorial by patrick.roof
In this tutorial we will be looking at regular expressions for emails and how they work. We will look at their different characteristics and how they are made.

## Summary

Regular expressions may seems cryptic and complicated at a glance, but once you break them up into sections and learn what each part is doing, they start to seem a lot more straightforward. The regex example we'll be looking at today is for matching an email.

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)

## Regex Components

The below regex can be used for matching an email:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
We are going to break up this regex into its different components and describe them to make it easier to understand.

### Anchors

Within the slashes `/` at the beginning and end of the regex, you can see there are two characters, `^` and `$`. The `^` always signifies the start of the regex, and the `$` signifies the end. These characters are known as anchors.

### Bracket Expressions

In our example regex, we can see there are multiple sections in brackets. The characters inside of the brackets are showing us a range of characters that our email has to match. Let's break down the first section: `[a-z0-9_\.-]`

`[a-z]` : The string can contain any characters from a to z, but only lowercase.

`[0-9]` : The string can contain any number from 0 to 9.

`[_\.-]` : The string can contain any of the listed characters, underscore, slash, period or dash.

Put all together, `[a-z0-9_\.-]` tells us the first part of our string can contain any character from a-z, 0-9, or an underscore, backslash, period or dash. It doesn't *have* to have all of these, it simply *can*.

### Quantifiers

Quantifiers are how we can narrow the amount a certain pattern is matched or given. In our case, `{2,6}` is the only quantifier in the regex. 2 is the minimum the preceding pattern will be matched, and 6 is the maximum. The preceding pattern is `[a-z\.]`, so the quantifier is finding a minimum of two characters that match that criteria, to a maximum of six.

Quantifiers are by default greedy, which means they will match as many occurrences of the pattern as possible, which in our case is 6.

### Character Classes

In our email regex there is only one character class. Common character classes include:

`.`,`\d`,`\w`,`\s`

Our email regex only has a `\d` on the middle line `([\da-z\.-]+)`. All that `\d` is doing is matching any Arabic numeral digit (0-9).

### Grouping and Capturing

Grouping, using '()', is separating the different parts of our expression into subexpressions. There are 3 different groups in are regex, which are being connected to the others with a '+' outside of the brackets but inside the parenthesis. An example of what each group is doing would be:

`/^([useremail]+)@([gmail,yahoo,etc]+)\.([com,co,etc]{2,6})$/`

## Author

Hello, my name is Patrick Ruf, and I am the author of this tutorial. At the time of writing, I am a coding student from Salt Lake County, Utah. I like to make music and learn new things.

https://github.com/patrick-roof

