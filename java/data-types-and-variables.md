# Data Types and Variables
[Variables](#variables)
[Data Types](#data-types)
[Type Casting](#type-casting)

### Variables
**Variable** - placeholder for storing a value of a particular type: string, number, etc.

Different types of variables:
- `String` stores text
- `int` stores integers
- `float` stores floating point numbers
- `char` stores single characters
- `boolean` stores true or false

Declaring a variable: `DataType variableName = initialization;`

> Use the `final` keyword for constant values that cannot be overwritten  

```java
final int num = 10;
num = 30;   // generates an error, cannot assign to a final variable
```

### Data Types
Data types are divided into 2 groups:
- **Primitive data types** (byte, short, int, long, float, double, boolean, char)
- **Non-primitive data types** (String, Arrays)

##### Primitive Data Types

| Data Types | Size | Description |
| ---------- | ---- | ----------- |
| byte | 1 byte | whole numbers from -128 to 127 |
| short | 2 bytes | whole numbers from -32,768 to 32,767 |
| int | 4 bytes | whole numbers from -2,147,483,648 to 2,147,483,647 |
| long | 8 bytes | whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| float | 4 bytes | fractional numbers 6 to 7 decimal digits |
| double | 8 bytes | fractional numbers 15 decimal digits |
| boolean | 1 bytes | true or false values |
| char | 2 bytes | single character/letter or ASCII values |

Primitive Types are divided into 2 groups:
- **Integer** types (byte, short, int, long)
- **Floating point** types (float, double)

##### Non-Primitive Data Types
Non-primitive data types are **reference types** because they refer to objects.

Primitive vs Non-primitive
- primitives are predefined; non-primitives are created by the programmer and not defined by Java
- non-primitive used to call methods to perform operations; primitives cannot
- primitives always have a value; non-primitives can be `null`

### Type Casting
Type casting is assigning a value of one primitive data type to another
Two types of casting in Java:
- **Widening Casting** (automatically) is converting a smaller type to a larger type
- **Narrowing Casting** (manually) is converting a larger type to a smaller type

##### Widening Casting
```java
public class Main {
    public static void main(String[] args) {
        int n = 9;
        double d = n;   // automatic casting int to double
        
        System.out.println(n);  // prints 9
        System.out.println(d);  // prints 9.0
    }
}
```

##### Narrowing Casting
```java
public class Main {
    public static void main(String[] args) {
        double d = 9.78;
        int n = (int)d;     // manual casting double to int
        
        System.out.println(d);  // prints 9.78
        System.out.println(n);  //prints 9
    }
}
```
