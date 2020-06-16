# Java

## What is Java?
A key feature of Java is **platform independence**:
  the same Java program can be run on multiple platforms without any changes
  also known as **write once, run anywhere (WORA)**

Java is used in Android smartphones, the financial services industry, telecommunications, embedded systems, etc.

## Important features
Simple and clear syntax
Garbage collector that automatically cleans memory from unused projects
Based on the object-oriented concept: **almost every part of a program is an object**

## Overview of a basic program
#### Hello World
```
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World!");
  }
}
```

**The public class.** 
Basic unit of a program. Every Java program must have at least 1 class. 
**The main method.**
The main method is used to make the program runnable. The entry point of a Java program. The name `main` is predefined and should not be anything else.
The element `String[] args` represents a sequence of arguments passed to the program from the outside world.
**Printing "Hello World!"**
The body of the method consists of a statement that will print the phrase "Hello World!" to the console.

#### Basic terminology
* Program - sequence of instructions (statements) that are executed one after another
* Statement - single action terminated by a semicolon (`;`)
* Block - group of statements enclosed by curly brackets (`{...}`)
* Method - sequence of statements that represent a high-level operation
* Syntax - set of rules that defines how a program needs to be written in order to be valid
* Keyword - a work that has a special meaning in the program language (`public`, `class`, etc.)
* Identifier or name - word that refers to something in a program (such as a variable or function name)
* Comment - textual explanation of what the code does
* Whitespace all characters that are not visible (space, tab, newline, etc.)

## Scanning input
Standard input is a stream of data going into a program supported by the operating system.

### Reading data with a scanner
Scanners allow a program to read a value of different types from the standard input. To use this class, import it at the top of a program.
`import java.util.Scanner;`
Then add the following constructor:
`Scanner scanner = new Scanner(System.in);`
This line creates an object of the `Scanner` class and names it `scanner`. `System.in` indicates that the program will read text that you type in the standard input.
If the text is an integer or a single word, use the `next()` method.
```
String name = scanner.next();
System.out.println("Hello " + name + "!");
```
If the `name` is a compound name such as Jane Doe, the program would only print the first name. This is when to use the `nextLine()` method, which reads and outputs the whole line.

## Defining methods
### The program decomposition
A method is a sequence of statements grouped together to perform an operation. Its purpose is to decompose a program into small reusable subroutines that can be used multiple time instead of rewriting code.
### The base syntax of methods
Methods have the following components:
1. set of modifiers (`public`, `static`, etc.)
2. type of return value
3. a name
4. list of parameters
5. list of exceptions
6. body containing statements to perform the operation
### Defining a simple method
A simple method that calculates the sum of two integers
```
public static int sum(int a, int b) {
  return a + b;
}
```
### Signatures
The combination of a method and its parameters is called a signature. The previous method has the following signature `sum(int, int)`.
### The type of a returning value and its parameters
A method can return a single value or nothing. To declare a method that returns nothing, use the `void` keyword.
```
public static void printSum(int a, int b) {
  System.out.println(a + b);
}
```

## Ternary operator
The ternary operator, also called the conditional operator is an operator that evaluates a condition and choose one of the two to execute.
Example of finding the max of two variables, a and b:
Conditional statement
```
int a = 4;
int b = 9;
int max = 0;

if (a > b) {
  max = a;
} else {
  max = b;
}
```
Ternary operator
`int max = a > b ? a : b;`
The general syntax of the ternary operator is the following:
`result = condition ? trueCase : elseCase;`



