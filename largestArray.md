# Largest Element in Array in Java

## Problem Statement

Find the largest element in an array.

### Example

#### Input Array

```text id="a1p9xz"
[10, 25, 7, 89, 45]
```

#### Output

```text id="u4k8mn"
Largest element = 89
```

## Java Code

```java
import java.util.Scanner;
class file name{
public static int getLargest(int numbers[]){
int largest = Integer.MIN_VALUE;
for(int i=0; i<numbers.length; i++){
if(largest < numbers[i]){
largest = numbers[i];
}
}
return largest;
}
public static void main(String args[]){
int numbers[] = {10, 25, 7 , 89 , 45};
System.out.println("The largest number is: " + getLargest(numbers));

}
}
```

## Explanation

* An array is created with some integer values.
* Assume the first element as the largest value.
* Traverse the array using a loop.
* Compare each element with `largest`.
* If a bigger value is found, update `largest`.
* Finally, print the largest element.

### Working

* Compare `25` with `10` → largest = `25`
* Compare `7` with `25` → no change
* Compare `89` with `25` → largest = `89`
* Compare `45` with `89` → no change

## Time Complexity

`O(n)`

## Space Complexity

`O(1)`
