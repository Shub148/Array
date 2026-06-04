# Print All Subarrays

## Problem Statement

Given an array of integers, print all possible contiguous subarrays.

### Example

Input:

```text
[1, 2, 3]
```

Output:

```text
[1]
[1, 2]
[1, 2, 3]
[2]
[2, 3]
[3]
```

## Java Code

```java
import java.util.*;
class file {
public static void printSubarray(int numbers[]){
for(int i=0; i<numbers.length; i++){ // used to print start
int start = i;
for(int j=i; j<numbers.length; j++){ // used to print end
int end  = j;
for(int k= start; k<=end; k++){ // used only to print start and end pair
System.out.print(numbers[k]+"");

}
System.out.println();
}
System.out.println(); // used to give more space only
}
}
public static void main(String args[]){
int numbers[] = {1 ,2 ,3 ,4 ,5};
printSubarray(numbers);
}
}
```

## Algorithm

1. Select the starting index of the subarray.
2. Select the ending index of the subarray.
3. Print all elements from the starting index to the ending index.
4. Repeat for all possible start and end positions.

## Dry Run

Array:

```text
[1, 2, 3]
```

Subarrays:

```text
[1]
[1, 2]
[1, 2, 3]
[2]
[2, 3]
[3]
```

## Number of Subarrays

For an array of size **n**:

```text
n × (n + 1) / 2
```

Example:

```text
n = 3

3 × 4 / 2 = 6
```

Total Subarrays = **6**

## Time Complexity

### Printing All Subarrays

* Outer Loop: O(n)
* Middle Loop: O(n)
* Inner Loop (Printing): O(n)

Overall Time Complexity:

```text
O(n³)
```

## Space Complexity

```text
O(1)
```

## Example Output

Input:

```text
[1, 2, 3, 4]
```

Output:

```text
[1]
[1, 2]
[1, 2, 3]
[1, 2, 3, 4]
[2]
[2, 3]
[2, 3, 4]
[3]
[3, 4]
[4]
```

## Applications

* Maximum Subarray Sum
* Minimum Subarray Sum
* Prefix Sum Problems
* Sliding Window Technique
* Dynamic Programming

## Related Problems

* Maximum Subarray Sum
* Kadane's Algorithm
* Subarray Sum Equals K
* Longest Subarray
* Prefix Sum
* Sliding Window
