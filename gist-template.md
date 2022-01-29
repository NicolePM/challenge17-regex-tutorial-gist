# Purpose of tutorial

Regex stands for regular expression (regex) for simplicity.  These expressions represent a sequence of characters that specify search pattern or validation criteria for a particular piece of pattern in text that they are searching.  In this tutorial I will cover aspects of Regex, and highlight a real world example of when a regular expression can be used in a piece of code for validating user input.


## Summary

BAs a developer, regex can be a very powereful tool in the code that we write.  It helps with efficiency and maintenance because many of the regex experssions in Javascript are already define and ready to use.  A few examples of regex in JavaScript are:match(), matchAll(), replace(), replaceAll(), search(), and split()
A real world example of regex would be for form validations, such as for email:
When a user is filling out a form, and an email address is required, it would be a good practice to validate if the email met certain criteria.  A functional piece of code would be presented as below:

## Table of Contents

- [Regex Example](#regex-example)
- [Regex components](#components)
- [Character Classes](#character-classes)
- [Parameters](#parameters)
- [Flags](#flags)
- [Bracket Expressions](#bracket-xpressions)
- [Return value](#return-value)
- [Author](#author)

## Regex Example:
As stated previously in the summary section, regex can be employed in real world examples.  Here is a piece of code that validates user input:

*******************************************************************
- let user_email = 'user001@email.com'
- const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
- const validate_email = user_email.match(regex);

- console.log(found);
- // expected output: ["user001@email.com", "user001", "email", "com"]
*******************************************************************

### Components
The regex expression match() matches a string to a regular expression and returns true (1) if it matches and false (0) if it does not match. Additionally the expression is opened with a forward slash "/" and closed by a forward slash "/". 

### Character Classes
Must include the "@" character "\." to specify the need for a "." in between a regex section

### Parameters
If you don't give any parameter and use the match() method directly, you will get an Array with an empty string: [""].

### Flags
flag indicates that the regular expression should be tested against all possible matches in a string. A regular expression defined as both global (" g ") and sticky (" y ") will ignore the global flag and perform sticky matches.

### Bracket Expressions
A bracket expression defines what characters can be present in a specific section of an email. For example, "[a-z0-9_\.-]" this shows the email can contain letters A - Z, numbers 0 through 9, and then _|.- at the end means they can have either of these characters within the username. The bracket expression for email server criteria must follow this pattern: "[\da-z\.-]" which means it can contain any digit and any letter in the range "a" to "z" and end with a dot or a dash.  [a-z\.]{2,6} this bracket expression can contain A through Z and a dot that must be between 2 and 6 characters.

### Return value
An Array whose contents depend on the presence or absence of the global (g) flag, or null if no matches are found. If the g flag is used, all results matching the complete regular expression will be returned, but capturing groups will not. if the g flag is not used, only the first complete match and its related capturing groups are returned. In this case, the returned item will have additional properties as described below.

## Author
This tutorial was created by Nicole Mitchell
Github: https://github.com/NicolePM
Gist: https://github.com/NicolePM/challenge17-regex-tutorial-gist
