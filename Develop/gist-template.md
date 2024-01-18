# What is the regex?

Introductory paragraph (replace this with your text)

## Summary
What is regex?
Regex is a programming language that allows you to match patterns in text.
Regex is a powerful tool that can be used to search for patterns in text.

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
Regex Components are the basic building blocks of regex.
These components consist of: Anchors, Quantifiers, OR Operator, Character Classes, Flags, Grouping and Capturing, Bracket Expressions, Greedy and Lazy Match, Boundaries, Back-references, Look-ahead and Look-behind.
### Anchors
Anchors are used to match the beginning or end of a string.
### Quantifiers
Quantifiers are used to match a specific number of characters.
### OR Operator
 OR Operators are used to match one of two or more options.
### Character Classes
Character Classes are used to match a specific set of characters.
Example: [abc] matches a, b or c. 

If you want to match a range of digits you can use the following: [0-9]. If you want to match a range of letters you can use the following: [a-z].

\w Matches a word character (letters, numbers, and underscores). \W Matches any non-word character. 
\s Matches a whitespace character. \S Matches any non-whitespace character.

\uhhhh Matches any unicode character.(four hex characters)
While \xhh matches any two hexidecimal   character.

\p{UnicodeProperty} Matches any character in the specified Unicode property. For example, japanese characters can be matched using \p{IsHiragana}
### Flags

Flags are used to modify the behavior of regex.
A flag changes the default searching behavior.

There are a total of 6 flags: g, i, m, s, u, and y.

i = Case-insensitive
g = Global
s = Dotall
m = Multiline
y = Sticky
u = Unicode
In JS regex uses the global flag by default.

Using these flags can be very useful.
To use a flag you need to add it to the regex.
For example: /pattern/ig or /regex/gi or /regex/igm.

Also using a flag in an expressing created as RegExp(), flags go as a string the second argument.

```new RegExp("pattern", "flags")```

For example, ```i``` could be used in this code below: 
``` var str = "Hello world!"; var patt = /hello/i;  var newStr = str.replace(regex,'(hello)'); console.log(newStr); ```

### Grouping and Capturing
Grouping and Capturing are used to create subexpressions.
Also capturing Groups can be quantified.
In this case the match information corresponding to the capturing group will be overwritten.
Example: /([ab])+/.exec("abc"); // ['ab', 'b']; because "b" comes after "a", this result overwrites the previous one
### Bracket Expressions
'panama'.match(/na{2}/) // -> no match
'banana'.match(/na{2}/) // -> matches 'nana'
'banana'.match(/na{2,3}/) // -> matches 'nana'
'bananaaaaaaaaaaa'.match(/a{2,4}/) // -> matches 'aaaa'
### Greedy and Lazy Match

### Boundaries
Regex boundaries such as ^ and $ are called anchors while \b is a word boundary.
The difference between anchors and word boundaries is that anchors match at the beginning or end of a string while word boundaries match at the beginning or end of a word.
### Back-references
A backreference refers to the submatch of a previous capturing group and matches the same text as that group. For named capturing groups, you may prefer to use the named backreference syntax.
For example: /\d{3}-\d{3}-\d{4}/.exec("123-456-7890"); // -> ['123-456-7890', '123', '456', '7890']
### Look-ahead and Look-behind
A lookahead assertion "looks ahead": it attempts to match the subsequent input with the given pattern, but it does not consume any of the input — if the match is successful, the current position in the input stays the same.
Syntax of this is (?=pattern) or (?!pattern). This syntax is used in conjunction with the lookbehind assertion (?<=pattern) or (?<!pattern)
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
