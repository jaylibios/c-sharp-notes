[Loops](#Loops)

# Conditions

### If Statement
The `if` statement is used to specify a block of code to be executed if the condition is true
```java
if (condition) {
    // block of code to be executed
}
```

### Else Statement
The `else` statement is used to specify a block of code to executed if the condition is false
```java
if (condition) {
    // block of code to be executed if true
} else {
    // block of code to be executed if false
}
```

### Else If Statement
The `else if` statement is used to specify a new condition if the *first* condition is false
```java
if (condition1) {
    // block of code to be executed if condition1 is true
} else if (condition2) {
    // block of code to be executed if the condition1 is false and condition2 is true
} else {
    // block of code to be executed if the condition1 is false and condition2 is false
}
```

### Short Hand If Else (Ternary Operator)
`variable  = (condition) ? ifTrue : ifFalse;`

### Switch Statement
The `switch` statement is used to select one of many code blocks to be executed
```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

---

# Loops
**Loops** can execute a block of code as long as a specified condition is reached

### While Loop
The `while` loop loops through a block of code as long as the specified condition is true
```java
while (condition) {
  // code block to be executed
}
```

### Do/While Loop
The `do while` loop will execute the block of code once before checking if the condition is true, then repeats as long as the condition is true
```java
do {
  // code block to be executed
}
while (condition);
```

### For Loop
The `for` loop is useful when you know exactly how many times you want the loop to run
```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```
**Statement 1** is executed one time before the execution of the code block
**Statement 2** defines condition for code block
**Statement 3** is executed every time after code block executed

### For Each Loop
The `for each` loop is used to loop through elements in an array
```java
for (type variableName : arrayName) {
    // code block to be executed
}
```
