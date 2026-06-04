# Reverse Array

## Problem Statement

Given an array of integers, reverse the array in-place.

### Example

Input:

```text
[1, 2, 3, 4, 5]
```

Output:

```text
[5, 4, 3, 2, 1]
```

## Java Code

```java
import java.util.*;
class fileName{
public static void reverse(int numbers[]){
int start=0, end=numbers.length-1;
while(start<end){
int temp = numbers[end];
numbers[end] = numbers[start];
numbers[start] = temp;
start++;
end--;
}
}
public static void main(String args[]){
int numbers[]={1,2 , 3, 4, 5};
reverse(numbers);

for(int i=0; i<numbers.length; i++){
System.out.print(numbers[i]+"");
}
System.out.println();
}
}
```

## Algorithm

1. Initialize two pointers:

   * `left = 0`
   * `right = n - 1`
2. Swap elements at `left` and `right`.
3. Increment `left` and decrement `right`.
4. Repeat until `left >= right`.
5. Print the reversed array.

## Dry Run

Initial Array:

```text
[1, 2, 3, 4, 5]
```

### Iteration 1

Swap index 0 and 4

```text
[5, 2, 3, 4, 1]
```

### Iteration 2

Swap index 1 and 3

```text
[5, 4, 3, 2, 1]
```

### Iteration 3

`left == right`, stop.

Final Array:

```text
[5, 4, 3, 2, 1]
```

## Time Complexity

* Best Case: **O(n)**
* Average Case: **O(n)**
* Worst Case: **O(n)**

## Space Complexity

* **O(1)**

## Advantages

* No extra array required.
* Efficient in-place reversal.
* Uses the Two Pointer technique.

## Applications

* Array manipulation
* String reversal
* Data processing
* Competitive programming problems
