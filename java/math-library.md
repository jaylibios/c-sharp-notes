# Essential Standard Classes
[Math Library](#Math-Library)  
[Big Integer](#BigInteger)  


### Math Library
###### Rounding Methods

`Math.min(..., ...)` returns the smaller of two arguments

``` java
int min = Math.min(11, 81); // returns 11
int max = Math.max(20, 30); // returns 30
```

`Math.max(..., ...)` returns the greater value of two arguments
`Math.abs(...)` returns the absolute value of its argument

`Math.floor(...)` returns the largest double value less than/equal to its argument and is equal to an integer
`Math.ceil(...)` returns the smallest double value greater than/equal to its argument and equal to an integer

``` java
double floor = Math.floor(3.78);  // floor is 3.0
double ceil = Math.ceil(4.15);  //ceil is 5.0
```

###### Exponential Functions
These functions are used to calculate a square or cube root of a given number
`Math.sqrt(...)` returns the square root of its argument
`Math.cbrt(...)` returns the cube root of its argument

``` java
double sqrt = Math.sqrt(2); // sqrt is 1.4142...
double cbrt = Math.cbrt(27.0);  // cbrt is 3.0
```

`Math.pow(...,...)` returns the value of its first argument raised to the power of the second argument

``` java
double square = Math.pow(5, 2); //the square of 5 is 25
double cube = Math.pow(2, 3); // the cube of 2 is 8.0
```

### BigInteger
###### Using large numbers in Java
The standard primitive integer types cannot store very large numebrs; it's not possible to assign the following:
` int y = 62123458797564213545687;  // compilation error`

Operations with numbers can sometimes lead to **type overflow**.

``` java
int a = Integer.MAX_VALUE; // 2147483647
a += 2; // -2147483647
```

Java provides a class called **BigInteger** for processing very large numbers (positive and negative). **BigInteger** is immutable; methods of the class returns new instances instead of changing existing ones. It should only be used if *absolutely necessary*, it is slower than built-in integer types.

###### Creating objects of BigInteger
**BigInteger** belongs to the **java.math** package.
How to import: `import java.math.BigInteger;`

Creating an instance of the class that stores a large number
`BigInteger number = new BigInteger("62957291795228763406253098");`

Creating an instance by passing a long value using **valueOf**
`BigInteger number = BigInteger.valueOf(1_000_000_000);`

**BigInteger** also has useful constants
``` java
BigInteger zero = BigInteger.ZERO; // 0
BigInteger one = BigInteger.ONE;   // 1
BigInteger ten = BigInteger.TEN;   // 10
```

Constants allow the reuse of already created objects. Code with constants are easier to read.

Comparisons
``` java
if (something) {
  return new BigInteger("1");
}
```
vs
``` java
if (something) {
  return BigInteger.ONE;
}
```

###### Methods of BigInteger
The class has non-static methdos to perform standard arithmetic operations.
``` java
BigInteger eleven = ten.add(one);
System.out.println(eleven); // 11
System.out.println(ten);  // 10, did not change
```

Arithmetic methods do not change instances, but create new ones

**negate** returns a new **BigInteger** with the changed sign.
`nine.negate(); // -9`

**divideAndRemainder** returns an array of two numbers: the result of integer division and the remainder
`BigInteger[] pair = oneHundredTen.divideAndRemainder(nine); // 12 and 2`
