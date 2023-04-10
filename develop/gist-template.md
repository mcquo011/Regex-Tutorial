# Email Regex

Regular expressions (regex) are a powerful tool for pattern matching and string manipulation. One common use case for regex is validating and parsing email addresses. In this gist, we'll explore a regex pattern for matching email addresses and explain how it works. We'll break down the different components of the regex and provide examples of how it can be used. Whether you're building a contact form for your website or validating email addresses in your application, understanding how to use regex for email validation can be a valuable skill to have in your toolkit.

## Summary

I will describe the regular expression (regex) for matching email addresses. The regex pattern matches the typical email format, consisting of a username, the @ symbol, and a domain name. I will explain how the regex works and the different components of it. Here is the code for the regex:

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

Quantifiers are used to indicate how many times a character or group of characters should be matched. The quantifiers in the email address regex are (+) and the curly brackets ({2,6}).

The plus sign (+) applies to the character set [a-z0-9_.-]. It means that one or more of these characters can appear in the email username. The plus sign also applies to the character set [\da-z\.-] and means that one or more of these characters can appear in the email domain name.

The curly brackets apply to the character set [a-z\.] and means the top-level domain (the part after the last dot) must be two to six characters long.

### OR Operator

OR operators allow you to match one pattern or another and are represtened by the vertical bar symbol (|)

This regex does not contain and OR operators.

### Character Classes

Character classes are represented by square brackets ([]) and match any single character within the brackets. This regex contains three character classes.

* [a-z0-9_.-] matches any lowercase letter (a-z), digit (0-9), underscore (_), period (.), or hyphen (-). It is used to match characters in the username.
* [\da-z.-] matches any digit (\d), lowercase letter (a-z), period (.), or hyphen (-). It is used to match characters in the domain name.
* [a-z.]{2,6} matches any lowercase letter (a-z) or period (.) and it must appear between 2 to 6 times. It is used to match the top-level domain name including, "com", "org", "edu", etc

### Flags

Flags in regex is an optional paramater that can modify its behvaior of searching. A flag is represented by a single lowercase alphabetic character.

For example, with the email regex we could add a lowercase i at the end: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/i

The i stands for 'ignoring casing' which will carry out a case-sensitive search. 

### Grouping and Capturing

Capturing groups are used to extract and isolate specific parts of the matched string. When the regular expression is matched against a string, the values matched by each capturing group can be accessed and manipulated separately.

In this regex there are three sets of parenthesis that create three capturing groups. 

([a-z0-9_.-]+): This capturing group matches one or more lowercase letters, digits, underscores, periods, or hyphens for the email username.

([\da-z.-]+): This capturing group matches one or more digits, lowercase letters, periods, or hyphens for the email domain name.

([a-z.]{2,6}): This capturing group matches two to six lowercase letters or periods for the top-level domain.

If the email is maggie.mcquown@gmail.com, the values captured by these three groups would be:

1. The username, "maggie.mcquown"
2. The domain name, "gmail.com"
3. The top-level domain name, "com"

### Bracket Expressions

There are several bracket expressions in this regex.

* [a-z0-9_.-]
* [\da-z.-]
* [a-z.]

### Greedy and Lazy Match

In this regex, there are no greedy or lazy matches specified. 

Regular expressions have the capability to exhibit greedy or lazy behavior, causing a variation in the amount of input string that is matched. Greedy is the default behavior, where the expression matches as much input as possible. Conversely, a lazy match matches the least amount of input possible, as opposed to the greedy match that matches the most.

### Boundaries

There are two boundaries represented by the caret (^) and dollar sign ($).

* The caret (^) at the beginning of the regular expression represents the start-of-line boundary. It matches the beginning of the string and checks that the regular expression will only match email addresses that begin at the start of the line.

* The dollar sign ($) at the end of the regular expression represents the end-of-line boundary. It matches the end of the string and checks that the regular expression will only match email addresses that end at the end of the line.

### Back-references

There are no back-references in this regex. 

Back-references are represented by the backslash followed by the number of the group to be referenced. Back-refrences allow you to refer back to a previously captured group within the same regular expression.

### Look-ahead and Look-behind

## Author

I am a Full-stack Web Developer passionate about creating websites and web applications that are both functional and aesthetically pleasing. Visit my [github profile](https://github.com/mcquo011) to see what I'm working on.
