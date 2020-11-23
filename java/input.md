
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





## Overloading
Overloading allows changing of a method's signature. Methods with the same name but different parameters are **overloaded**.

## Static members
Class variables (static field) belong to the class and not just an instance of a class. If there are instances of a class that should share the same value (ex a global variable), it's best to delcare it as static. These can be referenced directly by the class itself.
`className.fieldName;`
In general, it's not a good idea to declare non-final static variables.
You can also access the variable through an instance of the class.
```
SomeClass.staticIntField = 10;
SomeClass instance = new SomeClass();
System.out.print(instance.staticIntField);
```

### Class methods
A class can also have static methods that can be accessed by the class name and doesn't need an object of the class.
`ClassName.staticMethodName(args);`
Special features of static methods:
* can access only static fields
* can invoke another static method, but not an instance method
* cannot use `this` keyword because there is no instance in static context
Static methods are often used as **utility methods** common for the whole project

## Protected modifier
4 access modifiers:
1. private - available **only for class**
2. default - available for classes from **same package**
3. protected - available for classes from **same package and extended classes**
4. public - available from anywhere




