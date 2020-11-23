# Introduction to Java
[What is Java?](#what-is-java)<br>
[Overview of a basic program](#basic-program)<br>
[Basic terminology](#basic-terminology)

## What is Java? {#what-is-java}
A key feature of Java is **platform independence**:
  the same Java program can be run on multiple platforms without any changes
  also known as **write once, run anywhere (WORA)**

Java is used in Android smartphones, the financial services industry, telecommunications, embedded systems, etc.

## Important features
Simple and clear syntax
Garbage collector that automatically cleans memory from unused projects
Based on the object-oriented concept: **almost every part of a program is an object**

## Overview of a basic program {#basic-program}
#### Hello World
```java
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
