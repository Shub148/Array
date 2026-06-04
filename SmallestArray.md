# Problem 1: Find Smallest Element in an Array

## Problem Statement

Given an array of integers, find the smallest element present in the array.

### Example

Input:
[5, 2, 8, 1, 9]

Output:
1

## Java Code

```java
import java.util.*;
class file name{
public static int getSmallest(int numbers[]){
int Smallest = Integer.MAX_VALUE;
for(int i=0;i<numbers.length; i++){
if(Smallest > numbers[i]){
Smallest = numbers[i];
}
}
return Smallest ;
}
public static void main(String args[]){
int numbers[] = {5, 2, 8, 1, 9};
System.out.println("The Smallest Number is: " +getSmallest(numbers));
}
}
```

## Time Complexity

* Best Case: O(n)
* Average Case: O(n)
* Worst Case: O(n)

## Space Complexity

* O(1)

## Approach

1. Assume the first element is the smallest.
2. Traverse the array from the second element.
3. If a smaller element is found, update the smallest value.
4. Print the smallest element.
   

                  #Problem-2 Find Index of Smallest Element in an Array

## Problem Statement

Given an array of integers, find the index of the smallest element present in the array.

### Example

Input:

```text
[5, 2, 8, 1, 9]
```

Output:

```text
3
```

Explanation:

* The smallest element is `1`.
* Its index is `3` (0-based indexing).

## Java Code

```java
import java.util.*;
class file name{
public static int getSmallest(int numbers[]){
int smallest = Integer.MAX_VALUE;
int index = -1;
for(int i=0; i<numbers.length; i++){
if(smallest>numbers[i]){
smallest=numbers[i];
index = i;
}
}
return index;
}
public static void main(String args[]){
int numbers[] = {5, 2, 8, 1, 9};
int index = getSmallest(numbers);
if(index != -1){
System.out.println("The smallest number is: "+numbers[index]);
System.out.println("The index is:  "+index);
}else{
System.out.println("Array is empty");
}
}
}
```

## Approach

1. Assume the first element's index (`0`) is the index of the smallest element.
2. Traverse the array from index `1`.
3. Compare the current element with the element at `minIndex`.
4. If a smaller element is found, update `minIndex`.
5. After traversal, print `minIndex`.

## Time Complexity

* Best Case: **O(n)**
* Average Case: **O(n)**
* Worst Case: **O(n)**

## Space Complexity

* **O(1)**

## Dry Run

Array:

```text
[5, 2, 8, 1, 9]
```

| Index | Value | minIndex |
| ----- | ----- | -------- |
| 0     | 5     | 0        |
| 1     | 2     | 1        |
| 2     | 8     | 1        |
| 3     | 1     | 3        |
| 4     | 9     | 3        |

Final Answer:

```text
Index of Smallest Element = 3
```

