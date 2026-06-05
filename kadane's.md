# Kadane's Algorithm

## What is Kadane's Algorithm?

Kadane's Algorithm is an efficient technique used to find the **maximum sum subarray** in an array.

### Problem Statement

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

### Example

Input:

```
[-2, -3, 4, -1, -2, 1, 5, -3]
```

Output:

```
7
```

Explanation:

```
[4, -1, -2, 1, 5] = 7
```

## Algorithm

1. Initialize:

   * currentSum = 0
   * maxSum = Integer.MIN_VALUE

2. Traverse the array:

   * Add current element to currentSum.
   * Update maxSum if currentSum is greater.
   * If currentSum becomes negative, set it to 0.

3. Return maxSum.

## Java Code

```java
import java.util.*;
class file{
public static void kadanes(int numbers[]){
int currSum = 0;
int maxSum = Integer.MIN_VALUE;
for(int i=0; i<numbers.length; i++){ // Used kadanes algorithm 
currSum = currSum + numbers[i];
if(maxSum<0){
maxSum = 0;
}
maxSum = Math.max(currSum , maxSum);
}
System.out.println("THe max Sum is : " +maxSum);
}
public static void main(String args[]){
int numbers[] = { 4, -1, -2, 1, 5 };
kadanes(numbers);
}
}
```

## Time Complexity

```
O(n)
```

## Space Complexity

```
O(1)
```

## Applications

* Maximum Subarray Sum
* Stock Profit Analysis
* Dynamic Programming Problems
* Signal Processing
* Financial Data Analysis

## Key Points

* Traverses the array only once.
* Uses constant extra space.
* More efficient than brute force approaches.
* One of the most important array algorithms for coding interviews.
