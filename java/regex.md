# Regular Expressions in Java
[Regexps in Java](#Regexps-in-Java)<br>
[Sets, Ranges, Alternations](#Sets-Ranges-Alternations)<br>
[Shorthands](#Shorthands)<br>
[Quantifiers](#Quantifiers)<br>
[Regexes in Programs](#Regexes-in-Programs)<br>
[Patterns and Matcher](#Patterns-and-Matcher)<br>
[Replacing Characters](#Replacing-Characters)<br>
[Match Results](#Match-Results)<br>

## Regexps in Java
[Simple Matching](#Simple-Matching)<br>
[The dot character and question mark](#the-dot-character-and-question-mark)<br>
[The tricky escape character](#the-tricky-escape-character)<br>

A **regular expression** is a sequence of characters that specifies a set of strings that is used to search, edit, and manipulate text.

#### Simple Matching
`String aleRegex = "ale"; // the "ale" regex`
The **String** data type has built-in support for regular expressions. The **matches** method takes a regular expression pattern as an argument and checks whether the string matches this pattern. The method returns **true** only when the whole string matches, otherwise **false**.

Example, matching `aleRegex`
``` java
"ale".matches(aleRegex);  // true
"pale".matches(aleRegex); // false, "pale" string has an additional character
"ALE".matches(aleRegex);  // false, uppercase letters don't match lowercase and vice versa
```

Java differs from other programming languages where the regex checks whether the *whole* string can be fit, not just a substring.

Example, matching `helloRegex`
``` java
String helloRegex = "Hello, World";

"Hello, World".matches(helloRegex); // true
"Hello, world".matches(helloRegex); // false
"Hello,World".matches(helloRegex); // false
```

#### The doct character and the question mark
The `.` matches any single character including letters, digits, spaces, etc. It's only unable to match the newline character \n.

The `?` is a special character that means "the preceding character or nothing".
``` java
String pattern = "behaviou?r";

"behaviour".matches(pattern); // true
"behavior".matches(pattern);  // true
```

Combining the `.` and `?` in one pattern: "there can be any single character or no character at all".
``` java
String pattern = "..?";

"I".matches(pattern); // true
"am".matches(pattern);  // true
"".matches(pattern);  // false
```

#### The tricky escape character
If we want to use the `.` or `?` character as a regular punctuation mark, use the `\`.
``` java
String endRegex = "The End\\.";

"The End.".matches(endRegex); // true
"The End?".matches(endRegex); // false
```

## Sets, ranges, Alternations
[The set of characters](#the-set-of-characters)<br>
[The range of characters](#the-range-of-characters)<br>
[Excepting characters](#excepting-characters)<br>
[Escaping characters in sets](#escaping-characters-in-sets)<br>

#### The set of characters
Sets are written in square brackets, `[]`. For example, the set `"[abc]"` means a single character "a", "b", or "c" can match it.

``` java
String pattern = "[bcr]at";
"rat".matches(pattern); // true
"fat".matches(pattern); // false
```

You can use as many sets as you want and combine them with usual characters in a line

`String pattern = "[ab]x[12]";  // can match a or b followed by x followed by either 1 or 2`
Leads to: `"ax

## Shorthands

## Quantifiers

## Regexes in programs

## Patterns and Matcher

## Replacing Characters

## Match Results
