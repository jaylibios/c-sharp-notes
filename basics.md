# Computer algorithms
Algorithms are just a step-by-step sequence of actions

### General properties of computer algorithms
* specified input - an algorithm has one or more input values
* specified output - an algorithm produces a result
* definiteness - each step must be precisely defined
* correctness - must product correct output for each input value
* finiteness - must terminate after a finite number of steps
* generality - solves problems of a certain type

--------------------------------------------------

# The big O notation
### The complexity of an algorithm
**Big O** notation is used to classify algorithms based on how their running/space requirements grow as input size grows. It is written as **O(T(n))** where **T(n)** is a time complexity function that defines how running time grows as input grows; and the symbol **O** shows that when the input is large enough, the running time grows not faster than the function in parenthesis.
### Essential features
* describes the upper bound of the growth rate of a function
* describes the situation for large inputs
### Common growth rates (best to worst)
* constant time **O(1)** - the number of operations *does not depend on input size*. Examples: accessing array element by index, printing a single value.
* logarithmic time **O(log n)** - the number of operations is *proportional to input size*. Example: binary search of sorted array.
* square root time **O(sqrt(n))** - the number of operations is *proportional to the square root of input size*.
* linear time **O(n)** - the number of operations is *proportional to input size (time grows linearly as input increases)*.
* log linear time **O(n log n)** - 
* quadratic time **O(n^2)**
* exponential time **O(2^n)**

--------------------------------------------------

# Data structures
### What are they?
Data structures are a way of organizing data and providing convenient access to it. There are two types of operations:
1. interal operations that support data organization
2. operations available to users for storing, retrieving, or modifying data

--------------------------------------------------

# Stack
### Stack essentials
Stacks are an abstract data type that follow the LIFO rule. The **push** operation inserts an item at the top of the stack, the **pop** operation removes an item from the top of the stack, the **peek** operation returns the top element.
