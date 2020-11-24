[Types and Variables](#types-and-variables)  
[Sizes and Ranges](#sizes-and-ranges)  
[Type Casting](#type-casting)  
[Primitive and Reference Types](#primitive-and-reference-type)  
[Final Variables](#final-variables)  

# Types and Variables
### Declaring and initializing
**Variable**: placeholder for storing a value of a particular type: string, number, etc.

Declaration `DataType variableName = initialization;`

Variable names are case sensitive; `number` is not the same as `Number`

### Accessing values
Declaring a variable and printing
```java
String day = "Monday";
System.out.println(day);    // prints Monday
```

Assigning a value of one variable to another
```java
int one = 1;
int num = one;
System.out.println(num);    // prints 1
```

### Type inference
Since Java 10, you can write **var** instead of a specific type to force automatic type inference based on type of assigned value: `var variableName = initializaion;`

Examples:
```java
var language = "Java";  // String
var version = 10;   // int
```

# Sizes and ranges
Arthmetic expressions include **integers** and **fractional** numbers.

**Integer number** types:
- long: 8 bytes from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
- int: 4 bytes from -2,147,483,648 to 2,147,483,647
- short: 2 bytes from -32,768 to 32,767
- byte: 1 byte from -128 to 127

Most common: `int` and `long`

**Floating point** types:
- double: 4 bytes for 6 to 7 decimal digits
- float: 8 bytes for 15 decimal digits

```java
double pi = 3.1415;
float e = 2.71828f;
```

`float` variables usually marked with the letter 'f'.

**Characters** store single characters surrounded by single quotes. The size is the same as the `short` type, 2 bytes.

```java
char lowerCase = 'a';
char upperCase = 'A';
char dollar = '$';
```

**Booleans** store only two values, true and false.

# Type casting
**Type casting** is used to assign a value of one type to a variable of another type.

Two types of casting for primitive types: implicit and explicit.

**Implicit casting** is used when the target is wider than the source type.

`int` to `double`:
```java
int n = 9;
double d = n;   // automatic casting
System.out.println(d);  // prints 9.0
```

**Explicit casting** is used when the target type is narrower than the source type.

`(targetType) source`

`double` to `int`:
```java
double d = 9.78;
int n = (int) d;    // manual casting
System.out.println(n);  // prints 9
```

# Primitive and reference types
Data types are separated into two groups: 
- **primitive** types: value is just copied
- **reference** types: address to value is copied ( data shared between several variables)

Two main memory spaces: **stack** stores primitive types and **heap** stores reference types.

```java
int a = 100;
int b = a;  // 100 is copied to b

String lanuage = new String("java");
String java = language;
```

The variable `b` has a copy of the value stored in `a`, but the variables `language` and `java` reference to the same value, rather than copy it.

### Comparisons
Comparing reference types using `==` and `!=` is not the same as comparing primitive types. When comparing variables of the `String` type, it compares references (addresses) rather than actual values.

```java
String s1 = new String("java");
String s2 = new String("java");
String s3 = s2;

System.out.println(s1 == s2);   // false
System.out.println(s2 == s3);   // true
```

Correct way to compare:
```java
String s1 = new String("java");
String s2 = new String("java");
String s3 = s2;

System.out.println(s1.equals(s2));  // true
System.out.println(s2.equals(s3));  // true
```

### The null type
Unlike primitive types, variables of reference type can refer to special `null` values that represent that it has not initialized yet or doesn't have a value.

```java
String str = null;
System.out.println(str);    // null
str = "hello";
System.out.println(str);    // hello
```

Primitive nulls wont compile
`int n = null;  // won't compile`

# Final variables
**Constants** are variables that should not be modified during the program. Use the keyword `final` to declare.

```java
final double PI = 3.1415;
final String HELLO_MSG = "Hello";
```

### Final reference variables
The `final` keyword can be used with reference variables, but it means it is not possible to reassign a reference to the variable.

Example with `StringBuilder`, a mutable version of `String`.

```java
final StringBuilder sb = new StringBuilder();
sb = new StringBuilder();   // error
```

The second line won't compile since it is trying to reassign a reference to the final variable `sb`.

The following code is correct:
```java
final StringBuilder sb = new StringBuilder();   // ""
sb.append("Hello");
System.out.println(sb.toString());  // prints Hello
```
