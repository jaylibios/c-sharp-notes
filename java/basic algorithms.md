# Implementations of basic algorithms
[Algorithms in Java](#algorithms-in-java)<br>
[Linear Search](#linear-search)<br>
[Binary Search](#binary-search)<br>

## Algorithms in Java
[Implementing algorithms in Java](#implementing-algorithms-in-java)
[Example](#example)
[Considering corner cases](#considering-corner-cases)

#### Implementing algorithms in Java
Algorithms are often represented as static methods, but it's not the only way to implement them in Java.

`Arrays` class has algorithms for manipulating arrays such as sorting and searching
`Math` class has a mathematical algorithm for calculating the square rot of a number

It's convenient to take algorithms into separate methods and then call methods from external code, passing input (arguments) and obtaining an output (result).

Algorithms in Java can take input values from arguments, files, databases, the Internet, and can output the result to a console, file, etc.

#### Example
The following algorithm finds an index of the max number in an array of ints
``` java
public static int findIndexOfMax(int[] numbers) {
  int index = 0;
  for (int i = 1; i < numbers.length; i++) {
    if (numbers[i] > numbers[index]) {
      index = i;
    }
  }
  return index;
}
```

The static method, `findIndexOfMax`, takes an array of ints and returns the index of max. The input array can be ordered or unordered.

Describing the algorithm
1. Suppose the number with index 0 (first element) is a candidate to be the max
2. In the loop, we take the following number of the array (second to laste), while the end is not reached
3. If the taken number is greater than candidate, save its index (new candidate)
4. Go to following interation (2)
5. Return index of new candidate

#### Considering corner cases
**Corner case** is a situation that occurs when an algorithm's input values may lead to incorrect or ambiguous behavior; considering these cases is important in designing algorithms.

What if the array contains several numbers equal to the max? What is the array is empty?
The presented algorithm finds the first max.
`findIndexOfMax(new int[] {3, 2, 8, 8, 1}); // 2`

If the array is empty, method returns 0 as the index of the max. It may be better to return a special value -1 to mean there is no max found.
``` java
if (numbers.length == 0) {
  return -1;
}
```
## Linear Search
[Implementation](#implementation-in-java)<br>
[Searching in sorted arrays](#searching-in-sorted-arrays)

**Linear (sequential) search** is an algorithm for searching a value in arrays or similar collections. It checks each element until it finds the one that matches the target value. If the end is reached, it terminates unsuccessfully. In the worst case: it performs *n* comparisons where *n* is the length of the array.

This algorithm can be modified to check if an array contains a target element, to search for first/last occurences, search a value in a certain range of indexes, or coutning all occurences.

#### Implementation in Java
The method takes an array of int and a number to search for.

``` java
public static int search(int[] a, int val) {
  int index = -1;
  for (int i = 0; i < a.length; i++) {
    if (a[i] == val) {
      index = i;
      break;
    }
  }
  return index;
}
```
This implementation compares each element with the passed value in a loop. If equal, the loop stops and the method returns the found index; if no value returns -1.

#### Searching in sorted arrays
This algorithm works both for **sorted** and **unsorted** arrays; this is more efficient at searching a sorted array.

``` java
public static int search(int[] a, int val) {
  int index = -1;
  for (int i = 0; i < a.length; i++) {
    if (a[i] == val) {
      index = i;
      break;
    } else if (a[i] > val) {
      break;
    }
  }
  return index;
}
```
If the next element checked is greater than the passed value, it means we will not find the value in the array and we can stop.

This algorithm performs only two comparisons to confirm the element is not contained. It checks a smaller number of elements.

## Binary Search
[Iterative implementation](#iterative-implementation)<br>
[Recursive Implementation](#recursive-implementation)<br>
[Calculating the index of a middle element(#calculating-the-index-of-a-middle-element)<br>

**Binary search** is a *fast* algorithm for finding the position of an element in a ***sorted array***. For an array of sinze *n*, the running time is *O(log n)* in the worst case.

The algorithm
1. compares the middle element with the target value
  a. if the target value matches, its position is returned
  b. if the target is less than/greater than the middle the search continues in the left or right subarray
2. the process repeats until the value is found or the search returns empty

#### Iterative implementation
``` java
public static int binarySearch(int[] a, int val, int left, int right) {
  while (left <= right) {
    int mid = left + (right - left);  // index of the middle element
    
    if (val == a[mid]) {
      return mid; // the element is found, return its index
    }
    
    else if (val < a[mid]) {
      right = mid - 1;  // go to the left subarray
    }
    
    else {
      left = mid + 1; // go to the right subarray
    }
  }
  return -1;  // element is not found
}
```

The method takes an array of int, a target element, and two boundaries of the subarray where we search the element. The last two parameters are optional but useful.

#### Recursive implementation
The recursive implementation makes a recursive call instead of using a loop. It doesn't throw `StackOverflowError` because it does not make many recursive calls even for large arrays.

``` java
public static int binarySearch(int[] a, int val, int left, int right) {
  if (left > right) {
    return -1;  // search interval is empty, value is not found
  }
  
  int mid = left + (right - left) / 2;  // index of the middle element
  
  if (val == a[mid]) {
    return mid; // the value is found, return index
  }
  
  else if (val < a[mid]) {
    return binarySearch(a, val, left, mid - 1); // go to left subarray
  }
  
  else {
    return binarySearch(a, val, mid + 1, right);  // go to right subarray
  }
}
```

#### Calculating the index of a middle element
Two different ways to calculate the index of a middle element:
1. sum both borders and divide by two
`int mid = (left + right) / 2;`

disadvantage: fails for large values of left and right when the sum is greater than the max positive int value. The sum overflows to a negative valyes, and the index will be negative when divided by two.

2. this formula protects from int overflow
`int mid = left + (right - left) /2;`


