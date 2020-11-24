[What is Java?](#what-is-java)  
[Basic literals](#basic-literals)  
[Overview of a basic program](#overview-of-a-basic-program)  
[Printing data](#printing-data)  

# What is Java?
Java is:
- **platform independence**: the same program can be run on multiple platforms without changes; write once, run anywhere
- Used in Android smartphones, financial services industry, telecommunications, embedded systems, etc.

Java has a **garbage** collector that **automatically cleans memory** from unused objects during runtime.

# Basic Literals
## Literals
**Literals** are numbers, strings, and other values

Common literals:
- Integer
- Character
- String

# Overview of a basic program
## Hello World
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

1. **The public class** is the basic unit of a program. Every Java program must have at least one class. 
2. **The main method** makes the program runnable. `main` is the entry point in a Java program. `String[] args` represents a seuqnece of arguments passed to the program from the outside.
3. **The body of the method** consists of programming statements that determine what the program should do; this prints "Hello, world!".

### The basic terminology
- **Program**: sequence of instructions (statements) that are executed one after another (*sequential flow*)
- **Statement**: single action terminated by a semi-colon `;`
- **Block**: group of zero, one or more statements enclosed by `{}`
- **Method**: sequence of statements that represents a high-level operation
- **Syntax**: set of rules that define how a program needs to be written to be valid
- **Keyword**: word that has a special meaning in the lanugage; cannot be used as variable names
- **Identifier or name**: word that refers to something in the program (variable or function name)
- **Comment**: textual explanation of what code does
- **Whitespace**: characters not visible (space, tab, newline, etc.)

# Printing Data
**Standard output** is a receiver to which a program can send information (text).  Java provides `System.out` to work with standard output. 

`println` displays the passed string followed by a new line.
