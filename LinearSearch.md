### Linear Search


``` Java
import java.util.Scanner;
class file name{
public static int linearSearch(int numbers[], int key){ // applying linear search for number and key
// now run cases to search this
for(int i=0; i<=numbers.length; i++){ // search the array list and search each array till the last length of array untill key is found 
if(numbers[i]==key){
return i; // if found then return index value of that
}
}
return -1; // if not found then return - 1
}

public static void main(String args[]){ // we used [] on args it means we are going to create an array
int numbers[]={7, 8, 9, 10, 11, 15}; // this are the array list
int key = 10; //we have to search this number
// used if loop for -1 condition
int index = linearSearch(numbers , key);

if(index == -1){
System.out.println("Array is not found ");
}else{

System.out.println("Array is in list at index: " +index);
}
}
}
```
