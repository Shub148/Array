# Maximum Subarray Sum Using Prefix Sum

## Problem Statement

Given an integer array, find the maximum subarray sum using the Prefix Sum technique.

### Example

Input:

```text
[1, 4, 3, 8, -2, -5, 9, -8]
```

Output:

```text
18
```

## Concept

A Prefix Sum array stores the cumulative sum of elements from the beginning of the array.

Formula:

```text
prefix[i] = prefix[i-1] + arr[i]
```

Using Prefix Sum, we can calculate the sum of any subarray in O(1).

```text
Subarray Sum = prefix[end] - prefix[start-1]
```

If start = 0:

```text
Subarray Sum = prefix[end]
```

## Java Code

```java
import java.util.*;
class file {
public static void prefixSubarray(int numbers[]){
int currSum = 0;
int maxSum = Integer.MIN_VALUE;
int prefix[] = new int[numbers.length];
prefix[0] = numbers[0];
for(int i = 1; i<prefix.length; i++){
prefix[i] = prefix[i - 1] + numbers[i];
}
for(int i=0; i<numbers.length; i++){
int start = i;
for(int j = i; j<numbers.length; j++){
int end = j;
currSum =  start == 0 ? prefix[end]: prefix[end] - prefix[start -1];
if(maxSum<currSum){
maxSum = currSum;
}
}
}
System.out.println("The max Sum is : "+maxSum);
}
public static void main(String args[]){
int numbers[] = {1, 4, 3, 8, -2, -5, 9, -8};
prefixSubarray(numbers);
}
}

```

## Algorithm

1. Create a Prefix Sum array.
2. Store cumulative sums in the Prefix Sum array.
3. Generate all possible subarrays.
4. Calculate subarray sums using Prefix Sum in O(1).
5. Track the maximum sum found.
6. Print the maximum subarray sum.

## Dry Run

Array:

```text
[1, 4, 3, 8, -2, -5, 9, -8]
```

Prefix Sum Array:

```text
[1, 5, 8, 16, 14, 9, 18, 10]
```

Example:

Subarray:

```text
[3, 8, -2]
```

Indices:

```text
start = 2
end = 4
```

Sum:

```text
prefix[4] - prefix[1]
= 14 - 5
= 9
```

## Time Complexity

### Building Prefix Array

```text
O(n)
```

### Finding Maximum Subarray

```text
O(n²)
```

### Overall Time Complexity

```text
O(n²)
```

## Space Complexity

```text
O(n)
```

Extra space is used for the Prefix Sum array.

## Advantages

* Faster than Brute Force (O(n³)).
* Calculates subarray sums in constant time.
* Easy to understand and implement.

## Disadvantages

* Requires extra memory.
* Slower than Kadane's Algorithm.

## Optimization Path

```text
Brute Force      → O(n³)
Prefix Sum       → O(n²)
Kadane Algorithm → O(n)
```

## Related Problems

* Print All Subarrays
* Maximum Subarray Sum (Brute Force)
* Kadane's Algorithm
* Prefix Sum
* Range Sum Query
* Subarray Sum Equals K
