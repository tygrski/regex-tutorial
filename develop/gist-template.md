# Title (replace with your title)
Explanation of "matchiing a URL" as a regular expression. 

## Summary
 
Matching a URL = /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
This tutorial will explain the code above, breaking down the componenets as descibed below. 

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
Anchors define the beginning and end of the string, but do not actually defeine any characters. Only starting and end points. So if it was an acutal string, we would be looking after the first anchor for the first character and before the last achor for the last character. The two symbols for anchors are the ^ (up carrot) and the $ (dollar sign)
- ^ is the begenning anchor
- $ is the ending anchor

### Quantifiers
Quantifiers define how often or quantity, charcater sequence appears.  
The * matches zero or more occurences that are to it's left. {2,6})([\/\w \.-]*)*\/?$/ (in our case, the {2,6} means that there can only be between 2-6 cahracters)

The other quantifier is the ? symbol which also matches the character before zero or more times.  /^(https?:\/\/)? . Meaning the https vs http is optional(zero or more times).

### OR Operator
Operators can be defined as variables, characters or null( empty). We have already mentiones the operators ^, $, * and ?. I [\da-z\.-] the [] match the characters in the brackets. And as mentioned above the {} 2,6. 

Others: /d matches single numbers 0-9. \w matches and single word character. () defines scope and precidence. 

### Character Classes
Character classes allow for a match of several characters, even if some of the listed options will not be used. They are defined inbetween the []. In the case of [\da-z\.-], because we included the hyphen,  we are allowed to match cahracters.   d = digits and  a-z = any character from a-z. 

### Flags
Flags are operators that change the type of search. g (global) searches for all occurencs, i(ignore) searches case insensitivly, s (Dot all) . matches new lines, m (multi-line) makes the ^ and $ starts the begin and end of each line ,not the whole entire string itself. 

### Grouping and Capturing
Grouning involves using the () around a pattern so we can modifly them and not the rest of the expression. (https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)  the first ()is the http. The second is the website name. Teh third is the .com portion of the url, and the last is the exact location of the page or path. 

### Bracket Expressions
Bracket expression match the snclosed characters to any of the characters listed within the brackets.

The first set [\da-z\.-] incluses a digit (d) and letters from a-z . The second bracket [a-z\.] set is giving to match any characters from a-z.

### Greedy and Lazy Match
Regex Greedy and Lazy are the ways of matching . 
Greedy will look for the longest possible string to consume, strting with the < , then looking for a . , matching any character , excluding new lines. The + to repeat the proceeding as oftern as it can. > is the end of teh string. 

### Boundaries
Bondaries are defines by the \b symbol at the begening and /b at the end. It is similar to the anchors ^ and $. 
Example if we wanted to return a match for Hello,  ,the boundries should be set as followed ...\/bHello\b/ 

### Back-references
When matching characters in a group more than once, for a repeat of a string, back-references may be used. 
For example to match a repeated words , you could use \w

### Look-ahead and Look-behind
To find occuring patterns that are next to each other look-ahead and look-behind can be used. 
Look-ahead, using ?=  is looking for a to follow to the left.
Look-behing using ?<= will look for a pattern to follow.
## Author
Travis Tybor
Full-Stack Softwaer Developer 
https://github.com/tygrski
