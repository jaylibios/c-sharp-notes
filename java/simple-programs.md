[Scanning input](#scanning-input)
[Formatted input](#formatted-input)
[Errors in programs](#errors-in-programs)

# Scanning input
The **standard input** is a stream of data going into a program.

Solving programs consists of:
- reading data from standard input (System.in)
- processing data to obtain a result
- outputting the result to standard output (System.out)

### Reading with a scanner
Getting data from the standard input is to use the `Scanner` class that allows a program to read values of different types.

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
```

This creates an object of `Scanner` class, enabling us to use its methods. `System.in` indicates the program will read text that you type in the standard input.

Two ways for reading strings:
- `next()` only reads the next word
- `nextLine()` reads the next line

Using `next()`

```java
String name = sc.next();
System.out.println("Hello, " + name);
```

```java
String fullName = sc.nextLine();
System.out.println("Hello, " + fullName);
```

### Reading multiline input

# Formatted output
Two methods for formatting output:
- `printf()`
- `String.format()`

### The `printf()` method
The `printf()` method has two parts: the string to format and the argument list.

`System.out.printf("My name is %s. I am %d years old.", "John", 25);`

Display integers with `%d` format specifier, floating-point values with the `%f` specifier.

You can set **precision** with the `printf()` method.
`System.out.printf("display number %f", 15.23);` prints `display number 15.230000`.

`System.out.printf("display number %.2f", 15.23);` prints `display number 15.23`.

Display characters with `%c` and strings with `%s`.

### The `String.format()` method
`String.format()` returns a string rather than prints it.

```java
int age = 22;
String str = String.format("I'm %d years old.", age);
System.out.println(str);    // prints I'm 22 years old.
```

# Errors in programs
Error groups:
- **compile-time** errors
- **run-time** errors

**Compile-time errors** prevent the java program from compiling:
- syntax error: incorrect keyword, forgotten `;`
- bad source code file name
- invoking non-existing method

**Run-time errors** (bugs) occur when the program is running.

Two types:
1. **logic** errors: when a program produces a wrong result because the code is incorrect
2. **unhandled exceptional events** like division by zero, not found files, etc.
