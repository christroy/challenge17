# Regex Tutorial



## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  is an email verification regular expression example. 



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

There are two types of anchors. Anchors are used to tell the regular expression whether to match the beginning or the end of the string. 
The ^ symbol is used to match the start of a string as well as after each line break. The $ symbol is used to match the end of a string and also before each line break. In our example Regex, we see both anchors used to properly match the beginning and end of our email verification string. 

### Quantifiers

Quantifiers are used in a regular expression (Regex) to specify how many instances of a character, group, or class must be present in the string for the match to be found. It depends on what the quantifier is attached to. Some examples of quantifiers are the * which matches 0 or more times, + which matches 1 or more times, ? which matches 0 or one time. In our example regex, you can see a quantifier towards the end of the string where we try to match 2 to 6 characters after the period in the email. 

### OR Operator

The OR allows us to search for multiple scenarios within the same group of text. The OR Operator is similar to what you use with a javascript "if" statement, where one of multiple conditions can be true. The OR is signified by a single verticle line. For example, if I wanted to search for the words "cat" or "dog" in a string, i could use the regex \(cat|dog)\g. 

### Character Classes

Character Classes are specific pre-defined groups of characters that help minimize the amount of text that needs to go into a regular expression. Some common character classes include: "\d" for digits, "\s" for spaces which include tabs and new lines, and "\w" for words. For instance, if I wanted to find the first number in a phone number string, (ex: (123)456-7890), I would use the regular expression "/\d/". 

### Flags

Regular expressions flags help specify the way we search for items in the string. There are six of them in javascript. These flags include: "i" which causes the search to be case-insensitive, "g" which allows us to return all results within a string, "m" which turns our search into a multi-line mode, "s" which allows us to use a dot to match a new line character, "u" which enables full unicode support, "y" which enables sticky mode to search an exact position in the text.

### Grouping and Capturing

Grouping allows us to isolate a search for part of a regular expression. For instance, when searching for dog or cat, we used grouping parenthesis to tell the regular expression to search for either cat or dog. Capturing groups allow us to return the results of items between parenthesis in a separate index of the results array. Capturing groups are numbered from left to right in the regular expression. 

### Bracket Expressions

Bracket expressions are a special type of character class. They are annotated by [] brackets and do not accept meta-characters between them. For instance, if you type [\d] this would search for either a backslash or the letter d in the character group. 

### Greedy and Lazy Match

Greedy matches are matches where all possible matches are returned to the result array. Lazy matches return as few results as possible. Regular expressions are greedy by default and we can limit our search by adding an * asterisk ot any part of our regular expression which then causes it to be lazy. 

### Boundaries

Word boundaries are annotated by a "\b" and are a type of test just like the ^ carrot and $ sign. There are three different positions that qualify as a word boundary: (1) at the start of the string, where the first character is a word character, (2) between two characters in a string where one is a word character and the other is not, (3) at the end of a string where the last character is a word character. 

### Back-references

Back-references allow us to reference a previous capturing group so that we don't need to re-write the same capturing group in the same regular expression. Back-references are annotated by a less than and greater than symbol <, >.  For instance, if I was wanting to match an html tag with everything inside of it, I would use the following expression <([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>  which includes a back-reference to the beginning of the html tag. 

### Look-ahead and Look-behind

Look-ahead regular expression is one that matches the current condition as long as it is followed by another condition. A look-behind regular expression is one that matches a current condition as long as it is preceeded by another condition. For example, if I wanted to match the letter x, only if it is followed by the letter y, I would type: /x?=y/g.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
