# Maximum Subarray Sum (Brute Force)

## Problem Statement

Given an integer array, find the maximum sum among all possible subarrays using the Brute Force approach.

### Example

Input:

```text
[1, -2, 6, -1, 3]
```

Output:

```text
8
```

Explanation:

The subarray:

```text
[6, -1, 3]
```

has the maximum sum:

```text
6 + (-1) + 3 = 8
```

## Java Code

```java
import java.util.*;
class file {
public static void MaxSubarraySum(int numbers[]){
int currSum = 0;
int maxSum = Integer.MIN_VALUE;
for(int i = 0; i<numbers.length; i++){
int start = i;
for(int j = i; j<numbers.length; j++){
int end = j;
currSum = 0;
for(int k = start; k<=end; k++){
currSum+= numbers[k];
}
System.out.println("The current sum is : " +currSum);
if(maxSum<currSum){
maxSum = currSum;
}
}
System.out.println("The max Sum is: " +maxSum);
}
}

public static void main(String args[]){
int numbers[] = {1, -2, 6, -1, 3};
MaxSubarraySum(numbers);

}
}
```

## Algorithm

1. Generate all possible subarrays.
2. Calculate the sum of each subarray.
3. Compare the current sum with the maximum sum.
4. Update the maximum sum if a larger sum is found.
5. Print the final maximum sum.

## Dry Run

Array:

```text
[1, -2, 6, -1, 3]
```

Subarray Sums:

| Subarray          | Sum |
| ----------------- | --- |
| [1]               | 1   |
| [1, -2]           | -1  |
| [1, -2, 6]        | 5   |
| [1, -2, 6, -1]    | 4   |
| [1, -2, 6, -1, 3] | 7   |
| [-2]              | -2  |
| [-2, 6]           | 4   |
| [-2, 6, -1]       | 3   |
| [-2, 6, -1, 3]    | 6   |
| [6]               | 6   |
| [6, -1]           | 5   |
| [6, -1, 3]        | 8   |
| [-1]              | -1  |
| [-1, 3]           | 2   |
| [3]               | 3   |

Maximum Sum:

```text
8
```

## Time Complexity

### Outer Loop

```text
O(n)
```

### Middle Loop

```text
O(n)
```

### Inner Loop (Calculating Sum)

```text
O(n)
```

### Total Time Complexity

```text
O(n³)
```

## Space Complexity

```text
O(1)
```

## Advantages

* Easy to understand.
* Good for learning subarray concepts.
* Useful for beginners.

## Disadvantages

* Very slow for large arrays.
* Recalculates sums repeatedly.

## Optimization

The brute-force solution can be improved using:

1. Prefix Sum → O(n²)
2. Kadane's Algorithm → O(n)

## Related Problems

* Print All Subarrays
* Prefix Sum
* Kadane's Algorithm
* Maximum Product Subarray
* Subarray Sum Equals K
