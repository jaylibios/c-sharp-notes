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
