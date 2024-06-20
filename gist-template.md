# An email Regex Walkthrough

## Summary

Regex, or regular expressions, act as tools to search for and identify specific patterns. In this walkthrough, I will explain the purpose of my chosen regex, the different components that make up a regex, and the functions each component performs. Below you will find a table of contents. Within each section for the regex components I will provide detailed information and examples regarding their purpose. 

The regex we will explore today is designed to validate email input or seek out emails within strings of code. It appears as : 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors in a regex act as landmarks in the regex for where the expression begins and ends. In our email regex, the '/^' is an anchor, or landmark, that signifies the beginning of the expression while '$/' is the anchor for the end of the expression. This helps our code understand where to start and stop searching.  

### Quantifiers

In a regex, quanitifiers tell the expression "numbers of characters or expressions to match." (MDN Web Docs)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Quantifiers]

### Grouping Constructs

### Bracket Expressions



### Character Classes

Literal characters - The pattern searches for a specific string of characters. For example, if an email address must end in '.com' then the pattern search would need to specify in the regex with (.com) 

Meta characters - The pattern searches for a general type of character. For example, with our email regex, we are searching for any email address domain. It can end in '.edu', '.co', '.uk', '.org'. '.com', etc. To catch any of these characters we use the search pattern \.([a-z\.]{2,6})$/. In this section of the expression, we are saying the characters from a-z and the string can be anywhere between 2 and 6 characters in length.

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

## References 
[Rex Egg - Information on quantifiers](https://www.rexegg.com/regex-quantifiers.php) 
