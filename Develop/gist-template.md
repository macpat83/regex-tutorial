# Regular Expressions Tutorial

This gist will explain what a regular expression is and how to use it. The purpose of Regular Expressions, Regex for short, are used when you are trying to match a particular set of character combinations with a string. One of the uses would be for pulling out data from a code and being able to add validation. In this tutorial we will follow a sample of code snippet that can be used to match an email. We will follow different components of Regex.


## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Email-

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The above code will be used in this tutorial to display specific examples of how regex is used. This particular code can be used for matching email addresses. A primary use of this code is to validate someone entered in an email address in the correct format when prompted to enter in an email address. 

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

The anchor begins and ends the regular expression. In the code, the anchors are `^` and `$`.

### Quantifiers

Quantifiers are used to determine how many times a character or group of characters are needed to have a match. If we break down our code:

`([a-z0-9_\.-]+)`

this will match any string that contains the letters a-z, numbers 0-9, and the following special characters _, ., or -. The `+` means that at least one of the following is requiresd to verify a match. 


### OR Operator

An or operator isn't required for matching an email address, so we will explore another piece of code. 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This is a hex code that includes the OR operator. 
The way this works is it will match where the code begins with `#` that is followed by `[a-f0-9]{6}` which is a six character string that contains a combination of letters and numbers. 

The OR operator is `|` followed by 

`[a-f0-9]{3}` which is a three character long string that includes a combination of letters and numbers.

### Character Classes

The `\d` is used in the matching email code and it's purpose is to match a single letter character, a-z, after the @ sign in the email address. This is to ensure that a letter is present after the `@` in the email address and not numbers or special characters. 

### Flags
Our email address example doesn't use a flag so we will use a simple piece of code to demonstrate.

`/email/`

A flag is normally used to apply more guidelines for verification where as the slashes designate where the experession begins and ends. 

* g is for "global" which allows for matching of all of the instances within a string that follows the matching guidelines in a regular expression.
* m is for "multiline" which searches line by line instead of searching through an entire string.
* i is for "insentitive" which makes the regular expression non case-sensitive, so upper or lower case letters will not be a part of the decison making.


### Grouping and Capturing

Lets look at the matching email code again.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The first group is `([a-z0-9_\.-]+)` which is what comes in between the beginning anchor `^` and the `@`. This portion must be true before we attempt to match the second part of the expression.
The second group is `([\da-z\.-]+)` which is what comes after the `@` but before the `.` , and then we have our third group `([a-z\.]{2,6})` which is what comes after the `.` but before the `$`.
Each group has to be verified as a match in succession.

### Bracket Expressions
Lets look at the matching email code again.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Let's look at the first group to explore brackets.

`[a-z0-9_\.-]`

The guidelines for a match is as follows. For a match it can contain any letter, any number, an underscore, hyphen, or period. But because the period is an escaped character a `\` is needed for it to be matched. 

### Greedy and Lazy Match

Our email code for matching does not include a greedy or lazy match feature.

### Boundaries

Boundaries are used for matching specific words in a string. This isn't required in an email matching code. 

### Back-references

Email matching does not include back-references. 

### Look-ahead and Look-behind

Look-ahead and look-behind are used when a match has to include a certain order. This is not needed for email matching 

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

This tutorial was created by McKinley Wiltz.

Conatct McKinley:

[GitHub](https://github.com/macpat83)
