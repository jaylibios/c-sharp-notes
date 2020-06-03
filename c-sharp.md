# Data Types
### Text
String of text
``` c#
string phrase = "This is a string";
```
Single character
* Uses single quotation marks
``` c#
char grade = 'A';
```
### Numbers
Integer (whole number)
``` c#
int age = 30;
```
##### Decimal Types
float, double, decimal ranging from least accurate to most accurate, respectively.
* Decimals useful for money
### Boolean
``` c#
bool isTrue = true;
```
# Working with Strings
``` c#
string phrase = "Hello World!";
Console.WriteLine(phrase);
```

Find length of a string
`Console.WriteLine(phrase.Length);`

Convert to uppercase
`Console.WriteLine(phrase.ToUpper());`

Find if string contains specific substring
``` c#
Console.WriteLine(phrase.Contains("Hello"));
Console.WriteLine(phrase.ToLower().Contains("HELLO".ToLower()));
```

Find first character from string
`Console.WriteLine(phrase[0]);`

Get index of specific character or substring
``` c#
Console.WriteLine(phrase.IndexOf("o"));
Console.WriteLine(phrase.IndexOf("World"));
// doesn't exist, returns -1
Console.WriteLine(phrase.IndexOf("z"));
```
Get substring (starting index, length)
`Console.WriteLine(phrase.Substring(6, 2));`

# Working with Numbers












# String Formatting

### Composite Formatting
``` c#
string name = "John";
int age = 22;
Console.WriteLine("Hi, my name is {0} and I am {1} years old.", name, age);
```
Output `Hi, my name is John and I am 22 years old.`

### String Interpolation
``` c#
string name = "John";
int age = 22;
Console.WriteLine($"Hi, my name is {name} and I am {age} years old.");
```
Output
`Hi, my name is John and I am 22 years old.`
