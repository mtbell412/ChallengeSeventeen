# Regular Expressions defined

The following gist was created to provide a brief summary of regular expressions and how they work in different contexts. 


## Summary

For this tutorial we are going to focus on how to use a regular expression for a URL

Matching a URL – /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components
 The following components are included when matching a URL. Everything included in the // notation is considered a regular expression. 

### Anchors
Our URL regular expression begins with a caret symbol which denotes that everything in the following paranthesis must be at the beginning of the statement. Without the ^ caret symbol the regular expression would allow the https:// to be at any location of the URL which is incorrect.

The backslashes below are needed to include the forward slashes in the regular expression without an error
^(https?:\/\/)

### Quantifiers
The following quantifier is used to limit what comes after the . in the url such as .com or .co or .gov. The 2 is the minimum character and the 6 is the maximum character before moving on to the / part of the URL
\.([a-z\.]{2,6})

The ? quantifier is used to match the pattern afterwards 0 or 1 time. Meaning that it is required once or not at all in order to continue which in this case is being used for the https:// portion of th URL

^(https?:\/\/)?

the + quantifier is being used in this case for the www portion of the URL meaning it is required once to continue
([\da-z\.-]+)

### Grouping Constructs
Notice the number of groups in the following example
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

There are 4 different sets of paranthesis here that break up the regular expression into 4 different string constraints


### Bracket Expressions
Our URL example above contains 3 examples using bracket notation. Brackets in regular expressions contain a range of characters such as a-z as seen in our examples. the /d is a character class and will be discussed later
[\da-z\.-]

[a-z\.]

[\/\w \.-]


### Character Classes
our example URL regular expression uses 3 character classes. The '.' and '\d' and '\w'. The '.' when used inside bracket notation matches any character which is useful for the center part of our URL expression. The '\d' matches any digit which is what the d means here. The '\w' matches any character in the alphabet including _.

### Character Escapes
Character Escapes are used all throughout JavaScript as well as in regular expressions. The main one used is the \ backslash operator which ignores the literal version of what comes after and instead searches for that to match in the regular expression.

## Author
My name is Michael Bell and I am a junior Full Stack Developer focusing mainly on JavaScript. Please take a look at my repository to view projects I have completed recently in a coding bootcamp

https://github.com/mtbell412

