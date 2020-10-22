# Regular Expressions in Java
[Regexps in Java](#Regexps-in-Java)<br>
[Sets, Ranges, Alternations](#Sets-Ranges-Alternations)<br>
* [Shorthands](#Shorthands)
* [Quantifiers](#Quantifiers)
* [Regexes in Programs](#Regexes-in-Programs)
* [Patterns and Matcher](#Patterns-and-Matcher)
* [Replacing Characters](#Replacing-Characters)
* [Match Results](#Match-Results)

## Regexps in Java
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



## Sets, ranges, Alternations

## Shorthands

## Quantifiers

## Regexes in programs

## Patterns and Matcher

## Replacing Characters

## Match Results
