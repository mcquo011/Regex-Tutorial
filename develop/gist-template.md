# Email Regex

Regular expressions (regex) are a powerful tool for pattern matching and string manipulation. One common use case for regex is validating and parsing email addresses. In this gist, we'll explore a regex pattern for matching email addresses and explain how it works. We'll break down the different components of the regex and provide examples of how it can be used. Whether you're building a contact form for your website or validating email addresses in your application, understanding how to use regex for email validation can be a valuable skill to have in your toolkit.

## Summary

I will describe the regular expression (regex) for matching email addresses. The regex pattern matches the typical email format, consisting of a username, the @ symbol, and a domain name. I will explain how the regex works and the different components of it. Here is the code snippet for the regex:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 

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

^ - Match the start of the string.

([a-z0-9_\.-]+) - Match one or more characters that can be lowercase letters, digits, underscores, hyphens, or periods. This represents the local part of the email address before the @ symbol.

@ - Match the @ symbol.

([\da-z\.-]+) - Match one or more characters that can be digits, lowercase letters, dots, or hyphens. This represents the domain name.

\. - Match a period.

([a-z\.]{2,6}) - Match two to six lowercase letters or periods. This represents the top-level domain (TLD), such as ".com" or ".org".

$ - Match the end of the string.

### Anchors

In this regular expression, the ^ and $ characters are anchors that ensure that the pattern matches the entire string, from the beginning to the end. 

The caret symbol ^ is an anchor that matches the start of a string. The ^ character matches the start of the string and ensures that the pattern only matches if it starts at the beginning of the string.

The $ character at the end of the regular expression matches the end of the string and ensures that the pattern only matches if it ends at the end of the string.

### Quantifiers

Quantifiers are used to indicate how many times a character or group of characters should be matched.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
