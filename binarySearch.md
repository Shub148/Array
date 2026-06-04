# Binary Search

## Problem Statement

Given a sorted array of integers and a target value, find the index of the target element using Binary Search.

If the target element is not present, return `-1`.

### Example

Input:

```text
Array = [2, 4, 6, 8, 10, 12, 14]
Target = 10
```

Output:

```text
4
```

Explanation:

* The target element `10` is present at index `4`.

## Prerequisite

* The array must be sorted in ascending order.

## Java Code

```java
import java.util.*;
class file name{
public static int binarySearch(int numbers[], int key){
int start = 0, end = numbers.length-1; //initialization
while(start<=end){
int mid = (start + end)/2;
if(numbers[mid]==key){ //mid
return mid;
}
if(numbers[mid]<key){//right
start=mid+1;
}else{   //left
end = mid-1;
}
}
return -1;
}
public static void main(String args[]){
int numbers[] = { 2,4 , 6, 8, 10,12,14};
int key = 10;
System.out.println("The index of the array is: "+binarySearch(numbers, key));
}
}
```

## Algorithm

1. Set `left = 0` and `right = n - 1`.
2. Find the middle index:

   ```java
   mid = left + (right - left) / 2;
   ```
3. If `arr[mid] == target`, return the index.
4. If `arr[mid] < target`, search in the right half.
5. Otherwise, search in the left half.
6. Repeat until the element is found or the search space becomes empty.

## Dry Run

Array:

```text
[2, 4, 6, 8, 10, 12, 14]
```

Target:

```text
10
```

| Left | Right | Mid | Value |
| ---- | ----- | --- | ----- |
| 0    | 6     | 3   | 8     |
| 4    | 6     | 5   | 12    |
| 4    | 4     | 4   | 10    |

Element found at index `4`.

## Time Complexity

* Best Case: **O(1)**
* Average Case: **O(log n)**
* Worst Case: **O(log n)**

## Space Complexity

* Iterative Binary Search: **O(1)**

## Advantages

* Faster than Linear Search for large sorted arrays.
* Reduces the search space by half in every iteration.

## Limitations

* Works only on sorted arrays.
* Not suitable for unsorted data without sorting first.
