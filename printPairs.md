# Print All Pairs in an Array

## Problem Statement

Given an array of integers, print all possible pairs of elements.

### Example

Input:

```text
[1, 2, 3]
```

Output:

```text
(1, 2)
(1, 3)
(2, 3)
```

## Java Code

```java
import java.util.*;
class file {
public static void pairsArray(int numbers[]){
    int totalpairs = 0;
for(int i=0; i<numbers.length; i++){
 int current = numbers[i];
for(int j= i+1; j<numbers.length; j++){
System.out.print("("+current +"," +numbers[j] + ")" );
totalpairs++;
}
System.out.println();
}
System.out.println("Total pair is: " +totalpairs);
}
public static void main(String args[]){
int numbers[] = {1, 2, 3, 4, 5};

pairsArray(numbers);
}
}
```

## Algorithm

1. Traverse the array using the first loop.
2. For each element, use a second loop starting from the next index.
3. Print the pair `(arr[i], arr[j])`.
4. Continue until all pairs are printed.

## Dry Run

Array:

```text
[1, 2, 3]
```

Pairs:

```text
(1, 2)
(1, 3)
(2, 3)
```

Total Pairs:

```text
3
```

## Formula for Number of Pairs

For an array of size **n**:

```text
n × (n - 1) / 2
```

Example:

```text
n = 4

4 × 3 / 2 = 6 pairs
```

## Time Complexity

* Best Case: **O(n²)**
* Average Case: **O(n²)**
* Worst Case: **O(n²)**

## Space Complexity

* **O(1)**

## Example Output

Input:

```text
[1, 2, 3, 4]
```

Output:

```text
(1, 2)
(1, 3)
(1, 4)
(2, 3)
(2, 4)
(3, 4)
```

## Applications

* Pair Sum Problems
* Two Pointer Technique
* Brute Force Algorithms
* Competitive Programming
* Combinatorial Problems

## Related Problems

* Pair Sum
* Count Pairs with Given Sum
* Print Triplets
* Maximum Pair Sum
* Two Sum Problem
