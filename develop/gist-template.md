# Email Regex

Regex, often known as regular expressions, is an effective tool for string manipulation and pattern matching. The validation and parsing of email addresses is a typical application for regex. This gist will examine and describe a regex pattern for matching email addresses. We'll dissect the various parts of the regex and give applications for each one. Understanding how to use regex for email validation can be a useful ability to have in your toolkit, whether you're creating a contact form for your website or validating email addresses in your application.

## Summary

In this gist, I'll go over the regular expression (regex) for email address matching. The typical email format consists of a username, the @ symbol, and a domain name; all of these components are contained in the regex pattern. I'll go over the different components of the regex and how it works. You can find the regex code below:

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

^ - Matches the start of the string.

([a-z0-9_\.-]+) - Matches one or more characters that can be lowercase letters, digits, underscores, hyphens, or periods. This represents the part of the email address before the @ symbol.

@ - Matches the @ symbol.

([\da-z\.-]+) - Matches one or more characters that can be digits, lowercase letters, dots, or hyphens. This represents the domain name.

\. - Matches a period.

([a-z\.]{2,6}) - Matches two to six lowercase letters or periods. This represents the top-level domain, such as ".com" or ".org".

$ - Matches the end of the string.

### Anchors

In this regular expression, the ^ and $ characters are anchors that ensure the pattern matches the entire string, from the beginning to the end. 

The ^ character matches the start of the string and ensures that the pattern only matches if it starts at the beginning of the string.

The $ character at the end of the regular expression matches the end of the string and ensures that the pattern only matches at the end of the string.

### Quantifiers

Quantifiers are used to indicate how many times a character or group of characters should be matched. The quantifiers in the email address regex are (+) and the curly brackets ({2,6}).

The plus sign (+) applies to the character set [a-z0-9_.-]. It means one or more of these characters can appear in the email username. The plus sign also applies to the character set [\da-z\.-] and means one or more of these characters can appear in the email domain name.

The curly brackets apply to the character set [a-z\.] and means the top-level domain (the part after the last dot) must be two to six characters long.

### OR Operator

OR operators allow you to match one pattern or another and are represented by the vertical bar symbol (|)

This regex does not contain any OR operators.

### Character Classes

Character classes are represented by square brackets ([]) and match any single character within the brackets. This regex contains three character classes.

* [a-z0-9_.-] matches any lowercase letter (a-z), digit (0-9), underscore (_), period (.), or hyphen (-). It is used to match characters in the username.
* [\da-z.-] matches any digit (\d), lowercase letter (a-z), period (.), or hyphen (-). It is used to match characters in the domain name.
* [a-z.]{2,6} matches any lowercase letter (a-z) or period (.) and it must appear between 2 to 6 times. It is used to match the top-level domain name including, "com", "org", "edu", etc

### Flags

Flags in regex are optional parameters that can modify its behavior of searching. A flag is represented by a single lowercase alphabetic character.

For example, with the email regex we could add a lowercase i at the end: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/i

i stands for 'ignoring casing' which will carry out a case-sensitive search. 

### Grouping and Capturing

Capturing groups are used to extract and isolate specific parts of the matched string. When the regular expression is matched against a string, the values matched by each capturing group can be accessed and manipulated separately.

In this regex, there are three sets of parenthesis that create three capturing groups. 

([a-z0-9_.-]+): This capturing group matches one or more lowercase letters, digits, underscores, periods, or hyphens for the email username.

([\da-z.-]+): This capturing group matches one or more digits, lowercase letters, periods, or hyphens for the email domain name.

([a-z.]{2,6}): This capturing group matches two to six lowercase letters or periods for the top-level domain.

If the email is maggie.mcquown@gmail.com, the values captured by these three groups would be:

1. The username, "maggie.mcquown"
2. The domain name, "gmail.com"
3. The top-level domain name, "com"

### Bracket Expressions

There are several bracket expressions in this regex.

* [a-z0-9_.-]: Matches one or more occurrences of lowercase letters (a-z), digits (0-9), underscores (_), periods (.), or dashes (-). This expression matches the username part of the email address before the @ symbol.
* [\da-z.-]: Matches one or more occurrences of digits (\d), lowercase letters (a-z), periods (.), or dashes (-). This expression matches the domain name (excluding the TLD) of the email address.
* [a-z.]: Matches two to six lowercase letters (a-z) or period occurrences (.). This expression matches the email address's top-level domain (TLD), such as.com,.org,.edu, etc.

### Greedy and Lazy Match

In this regex, there are no greedy or lazy matches specified. 

Regular expressions have the capability to exhibit greedy or lazy behavior, causing a variation in the amount of input string that is matched. Greedy is the default behavior, where the expression matches as much input as possible. Conversely, a lazy match matches the least amount of input possible, as opposed to a greedy match.

### Boundaries

There are two boundaries represented by the caret (^) and dollar sign ($).

* The caret (^) at the beginning of the regular expression represents the start-of-line boundary. It matches the beginning of the string and checks that the regular expression will only match email addresses that begin at the start of the line.

* The dollar sign ($) at the end of the regular expression represents the end-of-line boundary. It matches the end of the string and checks that the regular expression will only match email addresses that end at the end of the line.

### Back-references

Back-references are represented by the backslash followed by the number of the group to be referenced. Back-references allow you to refer back to a previously captured group within the same regular expression.

There are no back-references in this regex. 

### Look-ahead and Look-behind

Look-ahead and look-behind assertions are advanced features of regular expressions that allow you to check for a pattern ahead of or behind the current position in the input string, without actually including that pattern in the match. They can be useful for complex matching scenarios where you need to check for a certain condition without actually consuming that part of the input.

This regex does not require look-ahead or look-behind assertions because it is a simple pattern that matches an email address with a specific format. 

## Author

I am a Full-stack Web Developer passionate about creating websites and web applications that are both functional and aesthetically pleasing. Visit my [github profile](https://github.com/mcquo011) to see what I'm working on.
