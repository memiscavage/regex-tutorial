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

In a regex, quanitifiers tell the expression "numbers of characters or expressions to match." [(MDN Web Docs)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Quantifiers) Quantifiers are preceded by the specifications they are meant to operate on. For example, this section, ([a-z0-9_\.-]+), in our email regex contains a quantifier of '+'. This symbol tells our expression that the string can match any character a-z, 0-9 any number of times. We can refer to sample emails such as 'example123@mail.com' or 'exaaaampplleee11233@mail.com' and know they will be caught by our regex because we have told it to seach for alphabetic and numeric strings and those characters are allowed to repeat within the string.

In the section following the '@' symbol, we see a similar expression '([\da-z\.-]+)'. One difference is our a-z section has a '\d' preceding it. This quantifier looks for any digit or any letter. In our expression, we are only listing letters for the domain name for our email.

### Grouping Constructs

As the name implies, grouping constructs group subexpressions within the regex. In our email regex, we will find 3 different subgroups:

Section 1. /^([a-z0-9_\.-]+) @ Section 2. ([\da-z\.-]+)\ and Section 3. .([a-z\.]{2,6})$/

Section 1 - This subgroup is the user's email handle. 

Section 2 - This subgroup is for the email domain, such as google, aol, yahoo, hotmail. It is preceded by an @ symbol.

Section 3 - This subgroup is for the top-level domain, such as .org, .com, .edu, .uk. It is preceded by a period.

### Bracket Expressions



### Character Classes

Literal characters - The pattern searches for a specific string of characters. For example, if an email address must end in '.com' then the pattern search would need to specify in the regex with (.com) 

Meta characters - The pattern searches for a general type of character. For example, with our email regex, we are searching for any email address domain. It can end in '.edu', '.co', '.uk', '.org'. '.com', etc. To catch any of these characters we use the search pattern \.([a-z\.]{2,6})$/. In this section of the expression, we are saying the characters from a-z and the string can be anywhere between 2 and 6 characters in length.

### The OR Operator

### Flags

### Character Escapes

## Author

[Mariel Miscavage](https://github.com/memiscavage) is a full-stack web developer located in Austin TX. 

## References 
[Rex Egg - Information on quantifiers](https://www.rexegg.com/regex-quantifiers.php) 

[GitHub Docs - Grouping Constructs in Regular Expressions](https://github.com/dotnet/docs/blob/main/docs/standard/base-types/grouping-constructs-in-regular-expressions.md)
